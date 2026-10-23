# 三处索引的精确格式

每新增一篇页面，必须同步三个文件（都在仓库根目录）：`README.md`（中文）、`README.en.md`（英文）、`index.html`（落地页，内含中英两组数据）。三处的条目数量、顺序、路径必须一致。动手前先 `git show f6302b1 -- README.md README.en.md index.html` 看一次真实的新增长什么样。

## 1. README 表格

表格列固定四列，路径用反引号 + 相对链接，链接目标是 `index.html`：

中文 `README.md`：

```
| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| <中文标题> | <作者，站点/刊物（日期）> | [`<分类路径>/<slug>/`](<分类路径>/<slug>/index.html) | <一两句中文简介> |
```

英文 `README.en.md`：

```
| Title | Original author / source | Page | Summary |
| --- | --- | --- | --- |
| <English title> | <Author, site/publication (date)> | [`<分类路径>/<slug>/`](<分类路径>/<slug>/index.html) | <1-2 sentence English summary> |
```

要点：
- 出处列写「作者，站点/刊物（日期）」。多位作者用顿号（英文用逗号）并列；知乎多回答写「知乎答主 A（主）、B」。作者名拿不到时写「知乎答主（页面未存档作者名）」这类，见 research-checklist.md。有补充参考文献时可追加「；补充参考 Tymoczko (2006)」。
- 英文行里的作者名、刊物名保持原文，不要翻译；标题与简介要翻译成自然的英文。
- 页面列的路径两处写法一致：反引号里是带结尾斜杠的目录，括号里是 `.../index.html`。
- 表格单元格里不要出现未转义的 `|`。

## 2. 分类小节标题

结构（以现有文件为准）：

```
## 索引
### AI（`ai/`）
### 物理 · 天文（`physics/astrophysics/`）
### 物理 · 理论物理（`physics/theoretical/`）
### 数学（`math/`）
#### 数学哲学（`math/philosophy-of-math/`）
#### 大数（`math/large-numbers/`）
#### 抽象代数（`math/abstract-algebra/`）
#### 决策（`math/decision/`）
#### 通识（`math/general/`）
### 哲学（`philosophy/general/`）
### 语言（`language/`）
### 设计（`design/`）
```

- 标题写法：`### 中文名（`目录/`）`，括号为全角，目录用反引号。英文：`### English Name (`dir/`)`，括号为半角。
- 一级目录下直接放页面的（如 `ai/`），用 `###`；一级目录下再分子类的（如 `math/`），一级写 `### 数学（`math/`）`（下面不放表格），子类写 `#### 子类名（`math/xxx/`）`，后面跟表格。物理是例外：它在 README 里被拆成两个 `###`（`物理 · 天文`、`物理 · 理论物理`），沿用这个写法，不要合并。
- 英文名对照：数学哲学 Philosophy of Mathematics，大数 Large Numbers，抽象代数 Abstract Algebra，决策 Decision，通识 General。新子类自己起一个对应的英文名。
- 空行规则：标题后空一行再接表格，表格后空一行再接下一个标题；文件末尾「---」分隔线及其后的声明句不动。

## 3. 顺序规则

- 同一张表内：新条目追加到该表最后一行。
- 子类顺序：没有严格字母序，是按添加历史。新子类插在同一一级目录下合理的位置即可，约定 `通识（general）` 始终放在该一级目录的最后。新的一级目录默认放在 `### 设计` 之前（「语言」之后）。
- README.md、README.en.md、index.html 里的分类顺序必须完全一致。

## 4. index.html 的 `var D`

`index.html` 里有一行（约第 65 行）`var D={"zh":[...],"en":[...]};`，是一个 JSON 对象：

```
D = { "zh": [ 分组, ... ], "en": [ 分组, ... ] }
分组 = { "name": "<分组名>", "items": [ 条目, ... ] }
条目 = [ "<标题>", "<出处>", "<简介>", "<路径，相对根目录，带结尾斜杠>" ]
```

- 分组名：一级目录直接放页面的就是它的名字（`AI`、`哲学`、`语言`、`设计`）；有子类的写成「一级 · 子类」，中文如 `数学 · 抽象代数`，英文如 `Mathematics · Abstract Algebra`；物理的两个分组是 `物理 · 天文`、`物理 · 理论物理`。
- 路径形如 `math/abstract-algebra/music-and-abstract-algebra/`（结尾斜杠，不含 index.html）。
- `zh` 与 `en` 两组都要加，分组顺序与 README 一致，分组内条目顺序与 README 表格一致。中文组用中文标题/简介；英文组用英文标题/简介，出处列的人名和刊物名保持原文。
- 新分组：在 `zh` 与 `en` 的数组里各插入一个新 `{"name":...,"items":[...]}`，位置与 README 的小节顺序对应。
- 该行很长，不要手改。用下面脚本编辑，它保证只改 `var D`，并且读写往返逐字节一致（已验证）。

```bash
python3 - <<'PY'
import re, json
p = 'index.html'
s = open(p, encoding='utf-8').read()
m = re.search(r'var D=(\{.*\});\nvar T', s)
d = json.loads(m.group(1))

def add(lang, group, item, after_group=None):
    gs = d[lang]
    g = next((x for x in gs if x['name'] == group), None)
    if g is None:                       # 新分组：插在 after_group 之后，没给就插到最后一个分组之前（即 设计/Design 之前）
        g = {'name': group, 'items': []}
        idx = next((i for i, x in enumerate(gs) if x['name'] == after_group), len(gs) - 2) + 1
        gs.insert(idx, g)
    g['items'].append(item)

path = 'math/abstract-algebra/music-and-abstract-algebra/'
add('zh', '数学 · 抽象代数',
    ['用音乐体会抽象代数：ℤ₁₂、五度圈与 PLR 群',
     '知乎答主（页面未存档作者名），2025-03-02 编辑；补充参考 Tymoczko (2006)',
     '十二平均律与五度相生律的钢琴对比、ℤ₁₂ 时钟与生成元……',
     path], after_group='数学 · 大数')
add('en', 'Mathematics · Abstract Algebra',
    ['Music and Abstract Algebra: ℤ₁₂, the Circle of Fifths and the PLR Group',
     'Zhihu answerer (name not archived), edited 2025-03-02; supplemented with Tymoczko (2006)',
     'Equal temperament vs Pythagorean tuning on a piano, a ℤ₁₂ clock ……',
     path], after_group='Mathematics · Large Numbers')

new = json.dumps(d, ensure_ascii=False, separators=(',', ':'))
s = s[:m.start(1)] + new + s[m.end(1):]
open(p, 'w', encoding='utf-8').write(s)
PY
git diff --stat index.html   # 应只有 1 行变化（var D 那一行）
```

示例是上面这篇的真实内容，仅作格式参考；你要把标题、出处、简介、路径、分组名换成自己这篇的。若分组已存在，`after_group` 被忽略，条目直接追加到该分组末尾。

## 5. 自检

```bash
# 三处都出现了新路径，且数量一致
for f in README.md README.en.md index.html; do echo "$f: $(grep -o '<分类路径>/<slug>/' $f | wc -l)"; done
# README 两份的条目总数、index.html 中 zh/en 条目数应相等
grep -c 'index.html) |' README.md README.en.md
python3 - <<'PY'
import re, json
d = json.loads(re.search(r'var D=(\{.*\});\nvar T', open('index.html', encoding='utf-8').read()).group(1))
print({k: sum(len(g['items']) for g in v) for k, v in d.items()})
PY
```
（把第一行的 `<分类路径>/<slug>/` 换成真实路径。README 里每个路径出现 2 次：反引号与链接；index.html 里出现 2 次：zh 与 en。）
