# 验证清单与命令

端口任选一个空闲的（下面用 8765；被占就换一个端口，不要去结束占用者）。`<dir>` 是新页面目录，如 `math/abstract-algebra/music-and-abstract-algebra`。

## 1. 静态检查（先做，几秒钟）

```bash
cd <仓库根>
# 无外链资源：前两条应当没有输出
grep -n 'zhimg\|<img' <dir>/index.html
grep -nE 'url\(https?:|@import|<script[^>]+src=|<link[^>]+href="http|<iframe' <dir>/index.html
# 其余 http：只应出现在 footer 的来源/参考文献文本链接（<a href>），人工看一眼
grep -nE '(src|href)="https?:' <dir>/index.html
# 残留占位
grep -n 'TODO' <dir>/index.html
# 基本信息
grep -n '<html lang="zh-CN">\|<title>\|name="viewport"' <dir>/index.html
```

## 2. 起本地服务（后台，记下 PID）

```bash
cd <仓库根> && python3 -m http.server 8765 >/dev/null 2>&1 &
echo $!      # 这个 PID 是你自己的，结束时只结束这个
```
用 Bash 的 `run_in_background` 起也行，结束时用 TaskStop。

## 3. Playwright MCP 三种截图

页面 URL：`http://localhost:8765/<dir>/index.html`。依次做：

1. 桌面浅色：`browser_resize` 1280x900；`browser_emulate_media` colorScheme=light；`browser_navigate`；滚动整页让入场动画触发（或 `browser_evaluate` 给所有 `.ch` 加 `seen` 类）；`browser_take_screenshot` fullPage。
2. 桌面深色：`browser_emulate_media` colorScheme=dark；重新截图。检查文字对比、SVG 颜色是否跟随变量（不要写死 `#fff`/`#000` 做底色）。
3. 手机 390px：`browser_resize` 390x844；截图。
4. 逐个交互点一遍：`browser_click` 每个按钮和可点选元素，确认状态栏、高亮、数值有变化，且确实回答了原文的那个问题。声音类：确认页面加载后不自动出声，点按钮才出声。
5. `browser_console_messages`（error/warning）必须为空；`browser_network_requests` 里不应有 localhost 之外的请求。
6. 手机无横向滚动：
   ```js
   // browser_evaluate
   () => ({sw: document.documentElement.scrollWidth, cw: document.documentElement.clientWidth})
   ```
   `sw <= cw` 才算通过；超出就用 `[...document.querySelectorAll('*')].filter(e=>e.getBoundingClientRect().right>innerWidth)` 找肇事元素（常见：长公式、宽 SVG、`.seg` 按钮组，给它们加 `overflow-x:auto` 容器或 `max-width:100%`）。
7. 落地页也看一眼：打开 `http://localhost:8765/`，中英文切换都能看到新条目，点卡片能进新页面。

Playwright 会在仓库根生成 `.playwright-mcp/`，已在 `.gitignore` 里（若没有就加上 `.playwright-mcp/`）；它和截图不能进 commit。截图存 scratchpad，不存仓库。

## 4. 收尾本地服务

```bash
ps -o pid,lstart,command -p <PID>   # 确认是自己刚起的那个 http.server
kill <PID>
```
只按具体 PID 结束；来历不明的进程不要动。

## 5. 推送后确认线上部署

```bash
git push origin main
gh run list --limit 3                       # 找到最新的 pages build and deployment
gh run watch <run-id> --exit-status         # 等它成功；失败就 gh run view <run-id> --log-failed，报告原文
curl -s -o /dev/null -w '%{http_code}\n' https://feiandxs.github.io/ai-visual-notes/<dir>/
curl -s -o /dev/null -w '%{http_code}\n' https://feiandxs.github.io/ai-visual-notes/
```
两个都要返回 200。刚部署完偶尔还是 404，等 20 到 30 秒重试几次（最多约 3 分钟），仍不行就在报告里写明现象，不要谎报成功。再 `curl -s https://feiandxs.github.io/ai-visual-notes/ | grep -c '<新页面路径>'` 确认落地页已含新条目。
