---
name: visual-explainer
description: 用户给一篇文章（本地 md/pdf、链接、视频链接、装着若干 md 的文件夹）或只给一个主题，要做成本仓库（ai-visual-notes）里那种带动画与交互的单文件可视化讲解页并上线时使用。触发词：可视化讲解、讲解页、explainer、做成页面、加到仓库、visual explainer、turn this article into an interactive page.
---

# visual-explainer：把一篇文章做成可视化讲解页并上线

仓库 `ai-visual-notes`（远程 `origin` = github.com/feiandxs/ai-visual-notes，线上 https://feiandxs.github.io/ai-visual-notes/）。每篇讲解页是「分类目录/slug/index.html」单文件，由 agent 基于原文生成。范本：`math/abstract-algebra/music-and-abstract-algebra/index.html`（commit f6302b1，`git show --stat f6302b1` 可见一次新增改了哪些文件）。开工前至少完整读一篇范本和 `index.html`、`README.md`，学风格。

文件在 `references/`：`page-template.html`（页面骨架）、`index-format.md`（三处索引）、`research-checklist.md`（调研/署名/三档示例）、`verification.md`（验证与部署命令）。

## 原料 x 档位（先定这两个，再动手）

| 原料 | 怎么拿 | 默认档位 |
| --- | --- | --- |
| 本地文件 md/pdf/txt/docx | 直接读，pdf 用 Read 按页读 | 转换 |
| 网页链接（任意站点） | WebFetch，被拦走退路（见阶段 1） | 转换 |
| 视频链接（YouTube/B 站/播客） | yt-dlp 取字幕，无字幕转写音频 | 转换（字幕即原文） |
| 只有一句话命题 | 自己 WebSearch 多源调研 | 原创 |

档位：**转换**＝严格按原文结构、顺序、观点，只补核对/署名/延伸，补充标「本页补充（非原文）」；**改写**＝原文当骨架，可重排、砍冗余、换例子、多篇合并，改写/补充处用同一种虚线框标注，出处列全部原文；**原创**＝只有命题，自己调研、先写提纲，出处写「本仓库整理，参考：A、B、C」。
定档：用户说「照原文做/直接转」→ 转换；「自己发挥/重新组织/这几篇合一下」→ 改写；「帮我讲讲 X」→ 原创；没信号就用上表默认。不要为了档位打断用户，在回报里写明用了哪档、为什么。各档署名示例见 `references/research-checklist.md` 第 9 节。

## 阶段 0：硬约束（全程有效）

- 单文件 `index.html`，无任何外链资源（脚本、样式、字体、图片、iframe 都不外链）；页面中文（`lang="zh-CN"`）；浅色/深色都正常；390px 手机宽度无横向滚动。
- 只 `git add` 本篇相关文件（新页面 + README.md、README.en.md、index.html）。禁止 `git add -A` / `git add .`。根目录其他未跟踪文件夹（如 `solar-chimney/`、`clips/`）是用户自己的，不碰。
- 结束进程铁则：禁止按名字、模式、端口批量结束进程（pkill、killall、`kill $(pgrep ...)`、`lsof -ti:端口 | xargs kill` 都不行）。只能 `kill <具体PID>`，且只能是自己启动的进程，先 `ps -o pid,lstart,command -p <PID>` 确认。端口被占就换端口。给子代理派活时把这条原样写进提示词。
- 声音类交互必须用户点按钮才出声，页面加载与滚动不得自动发声。
- 多篇（文件夹）时每篇单独走完阶段 2 到 8，一篇一个 commit。

## 阶段 1：输入识别与获取

做什么：判定原料类型与档位，拿到全文。网页链接按 `research-checklist.md` 第 1 节的顺序：WebFetch → 被拦（403/登录墙/JS 空页）时 WebSearch 找标题与摘要 → 浏览器 MCP（Playwright）打开 → 请用户用 Obsidian Web Clipper 存成 md。视频按该文件第 8 节取字幕/转写。署名按 frontmatter author → 页面 byline → 站点+标题搜索 → 「<站点名>作者（未存档作者名）」的顺序，绝不猜名字；多回答/多作者分别列出。下载物只放 scratchpad 或 /tmp，不进仓库。
怎么判断做对了：能说出标题、作者（或兜底署名）、日期、原文链接和全文大意；原料确实拿不到全文时才停下来问用户，其余情况不打断。

## 阶段 2：通读与拆解（先写 outline 再动手）

做什么：通读全文，列一份简短 outline（可写在回复里或 scratchpad，不进仓库）：每个章节一行，写清「原文这一段在说什么 → 用什么可视化表达 → 读者能操作什么」。外文原文：关键术语首次出现括注原文。
怎么判断做对了：outline 里至少 3 到 5 个交互，每个交互能写出一句「它回答了原文的哪个具体问题」（例：「步长为什么必须与 12 互素」）；写不出这句话的交互删掉，只会自动播放的动画不算交互。原文的图片全部有对应的重绘方案（内联 SVG/canvas）。

## 阶段 3：调研补充

做什么：核对原文的关键事实、数字、人名年代，补背景和延伸阅读，按 `research-checklist.md` 第 4 到 6 节执行。补充内容一律放 `.note-add`，标「本页补充（非原文）」，参考文献编号用 `<sup class="c">[n]</sup>`。
怎么判断做对了：补充块都有来源；凭记忆写的、没核对的事实在最终报告里逐条列为「未核对」；能用 JS 现场算的数值现场算。

## 阶段 4：归类与命名

做什么：目录树现状用 `ls`/README 小节看，就近归类到现有分类（`ai/`、`physics/astrophysics|theoretical/`、`math/<子类>/`、`philosophy/general/`、`language/`、`design/`）。拿不准自己决定，不打断用户；确实没有合适的才新开子类，目录名 kebab-case 英文（如 `math/abstract-algebra/`），README 中英文小节名对应起一个。slug 也是 kebab-case 英文，概括主题，不带日期，例 `optimal-stopping-37-percent-rule`。
怎么判断做对了：新路径 `<分类>/<slug>/index.html` 与同级兄弟风格一致；新开的子类在回报里写明并给出理由。

## 阶段 5：写页面

做什么：复制 `references/page-template.html` 到新路径起步。设计令牌（`:root` 与两个暗色块）原样保留不改色值。结构：标题区（含来源署名）→ 目录（桌面侧栏、手机底部抽屉）→ 章节（`section.ch`，`data-title` 供目录用）→ 页脚（来源与署名、参考文献）。交互用模板里 `reg('名字', node => ({start, stop}))` 的形式，离开视口要 `stop`。SVG 颜色全部走 CSS 变量；尊重 `prefers-reduced-motion`；演示要有文字状态栏说明当前结果；可点选元素加 `tabindex` 和键盘 Enter/空格。原文图片用 SVG/canvas 重绘，不外链。
怎么判断做对了：`grep -n 'TODO' index.html` 为空；没有未使用的示例组件；每章首句 `.lead` 抛出一个问题，章内的交互在回答它。

## 阶段 6：验证

做什么：按 `references/verification.md` 执行：静态 grep（无 `zhimg`、无 http 外链资源）→ 本地 `python3 -m http.server <端口>` → Playwright MCP 截桌面浅色、桌面深色、390px 手机三种 → 逐个交互点击 → 控制台无错 → 手机宽度无横向滚动 → 用完结束自己起的服务（按 PID）。
怎么判断做对了：三张截图都看过且排版正常；`browser_console_messages` 为空；`scrollWidth <= clientWidth`；发现问题先修再继续，不带病提交。

## 阶段 7：索引同步

做什么：按 `references/index-format.md` 同步三处：`README.md`、`README.en.md`、`index.html` 的 `var D`（zh 与 en 两组都加）。页面始终中文，README.en.md 与 `D.en` 写英文标题与简介，出处里的人名刊名保持原文。用文档里的脚本改 `var D`，不要手改那一长行。
怎么判断做对了：三处顺序一致；文档第 5 节自检命令数目对得上；`git diff --stat index.html` 只改 1 行；本地落地页中英文切换都能看到新条目。

## 阶段 8：提交推送与部署确认

做什么：确认 `.gitignore` 含 `.playwright-mcp/`。`git status` 检查后只 add 本篇文件：`git add <新页面目录> README.md README.en.md index.html`。提交信息 `Add <topic> explainer`（`<topic>` 用英文短语，参照 `git log --oneline`），末尾按本会话系统提示给的归因行结尾（若有）。`git push origin main`，失败就把报错原文报告，不强推。然后 `gh run list` / `gh run watch` 等 Pages 部署完成，`curl` 新页面与落地页都返回 200（命令见 verification.md 第 5 节）。
怎么判断做对了：`git show --stat HEAD` 恰好是 1 个新页面 + 3 个索引文件；两个 curl 都是 200。

## 阶段 9：回报模板

用下面的字段回报，简短即可：

- 页面路径与线上地址（https://feiandxs.github.io/ai-visual-notes/<分类>/<slug>/）、commit hash、push 与部署结果（200）
- 原料类型与使用的档位，以及为什么选这档
- 署名来源（frontmatter / byline / 搜索 / 兜底署名）；兜底署名要明说
- 补充了什么（「本页补充」各条）；哪些凭记忆未核对
- 交互清单：每个交互回答了原文的哪个问题
- 新开了什么分类、为什么
- 未提交的杂项文件（`git status` 里不属于本篇的未跟踪项，如 `solar-chimney/`；明确说明没碰）
- 验证情况：三种截图是否都看了、有无遗留问题

## 常见坑（来自实际踩过）

- 知乎 WebFetch 常返回 403，拿不到答主昵称：按阶段 1 的退路，最后署「知乎答主（页面未存档作者名）」，原文链接放页脚。
- Clipper 存下来的 md 里图片是 zhimg 等外链，别带进页面。交付前必须 grep 确认。
- 补充调研写进页面必须标「本页补充（非原文）」；没核对的事实宁可不写。
- Playwright 会在仓库生成 `.playwright-mcp/`，不能进 commit。
- 声音交互：只在用户点击后创建 AudioContext/发声。
