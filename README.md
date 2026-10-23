[English](README.en.md)

# ai-visual-notes

把文章做成图文并茂、带动画的可视化讲解页面，供初学者学习。内容涵盖 AI、物理、数学、哲学、设计等个人学习笔记。每篇一个子目录，均为单文件 HTML，可直接用浏览器打开。

## 索引

### AI（`ai/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| ChatGPT 在做什么，为什么它有效？ | Stephen Wolfram | [`ai/wolfram-what-is-chatgpt-doing/`](ai/wolfram-what-is-chatgpt-doing/index.html) | 用图示和动画讲解 ChatGPT 如何逐词生成文本，以及它为什么有效。 |
| AI Coding 编辑器没有那么神秘：Cline 是怎么工作的 | nazha，nazha.co（2025-01-24） | [`ai/how-cline-works/`](ai/how-cline-works/index.html) | 拆开开源 AI 编程插件 Cline：系统提示词、XML 工具协议、环境快照、多轮循环。 |
| 深度解密：DeepSeek R1 + Cline 是如何做到全自动化编程的？ | Heycc，Heycc's blog（2025-02-11） | [`ai/deepseek-r1-cline-autonomous-coding/`](ai/deepseek-r1-cline-autonomous-coding/index.html) | 用本地代理截获 Cline 发给 DeepSeek R1 的每一轮 prompt，逐轮拆解 ReAct 循环、工具调用、失败恢复与 token 消耗。 |
| 用代码、MCP、Skills 构建高效 Claude 智能体（Anthropic 播客） | Anthropic 播客，Alex Albert 与 Erik Schluntz 对谈；中文整理：莫尔索随笔（2025-11-04） | [`ai/anthropic-podcast-building-agents/`](ai/anthropic-podcast-building-agents/index.html) | 从“编码是核心技能”到“工具映射 UI 而非 API”，讲清智能体架构演进与三条最佳实践。 |
| AI 应用对工程技术认知的启示 | 李培根（中国工程院院士，华中科技大学），《高等工程教育研究》 | [`ai/li-peigen-ai-engineering-cognition/`](ai/li-peigen-ai-engineering-cognition/index.html) | 从康德“物自体”、默会知识与暗知识、过程视角到思维链与目标悖论，讲 AI 如何改变工程师认识世界的方式。 |
| 语义计算机中没有 Token | 孔某人，公众号「孔某人的低维认知」（2025-01） | [`ai/semantic-computer-no-token/`](ai/semantic-computer-no-token/index.html) | 正如 C 语言里没有寄存器：把 context 当语义程序、LLM 当执行它的语义计算机，讲推理期计算 LLM 的价值、训练与 A* 式探索。 |

### 物理 · 天文（`physics/astrophysics/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| 既然物质不能凭空产生，宇宙最初的物质是从哪里来的？ | 知乎答主 时空通讯、我喜欢小笼包、王清扬 | [`physics/astrophysics/where-did-matter-come-from/`](physics/astrophysics/where-did-matter-come-from/index.html) | 从大爆炸奇点、真空零点能和宇宙学尺度上的能量不守恒三个角度回答物质的来源。 |
| 时间会不会是一个以虚数为单位的维度？ | 知乎答主 Timothy Liu、零者 | [`physics/astrophysics/is-time-an-imaginary-dimension/`](physics/astrophysics/is-time-an-imaginary-dimension/index.html) | 从矢量协变性和光速不变推出时空间隔不变，解释为什么可以把时间写成 ict。 |

### 物理 · 理论物理（`physics/theoretical/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| 时间的本质：一个计算的视角 | Stephen Wolfram（2024-10-08） | [`physics/theoretical/wolfram-on-the-nature-of-time/`](physics/theoretical/wolfram-on-the-nature-of-time/index.html) | 时间是宇宙逐步做的计算；计算不可约加上观察者算力有限，时间才显得单线、不可跳、有方向。 |
| 量子力学中，为什么观测会导致坍缩？ | 知乎答主 贾明子、陈童 | [`physics/theoretical/why-observation-collapses/`](physics/theoretical/why-observation-collapses/index.html) | 三公设、U/R 过程、冯诺依曼链、三类诠释，退相干能回答偏好基却回答不了输出值。 |
| 量子纠缠意味着宇宙间存在超越距离的联系吗？ | 知乎答主 拉格朗日的忧郁 | [`physics/theoretical/quantum-entanglement-nonlocality/`](physics/theoretical/quantum-entanglement-nonlocality/index.html) | 纠缠是非定域关联，但 no-communication 定理说明它传不了信息。 |
| 所有电子都一模一样吗？ | 知乎答主 酱紫君 | [`physics/theoretical/are-all-electrons-identical/`](physics/theoretical/are-all-electrons-identical/index.html) | 电子是同一个狄拉克场的激发，像“单例模式”；由反对易关系推出泡利不相容。 |
| 怎么把光子一个一个打出来？单光子源 | 未署名问答整理 | [`physics/theoretical/single-photon-sources/`](physics/theoretical/single-photon-sources/index.html) | 量子点、单原子、参量下转换、电路 QED 四种单光子源，以及量子点为何最主流。 |
| 诺顿穹顶：牛顿力学也会“不确定”？ | 东方既白，知乎专栏「数理灵感笔记」 | [`physics/theoretical/nortons-dome/`](physics/theoretical/nortons-dome/index.html) | 牛顿方程在特殊穹顶上出现多解，解释解不唯一的数学根源与物理理想化。 |
| 广义坐标为什么“不是时间的函数”？ | 知乎答主 東雲正樹、Skadiologist | [`physics/theoretical/generalized-coordinates-lagrangian/`](physics/theoretical/generalized-coordinates-lagrangian/index.html) | 区分“态空间的坐标”与“路径上的函数”，讲清 q、q̇、作用量原理与偏导/全导。 |
| 原子没有意识，人为什么有？ | 知乎答主 清人 及同一问题下另一回答 | [`physics/theoretical/consciousness-from-atoms/`](physics/theoretical/consciousness-from-atoms/index.html) | 用自由能原理解释意识的还原论框架，并对比泛心论与涌现论、注意力模式理论。 |

### 数学（`math/`）

#### 数学哲学（`math/philosophy-of-math/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| 数学是真理吗？古典柏拉图主义的困境（数学哲学系列 7） | 贾明子，知乎专栏《何为现实？拉普拉斯之妖与薛定谔猫之决战》 | [`math/philosophy-of-math/is-math-truth-platonism-dilemma/`](math/philosophy-of-math/is-math-truth-platonism-dilemma/index.html) | 从毕达哥拉斯、柏拉图、欧几里得到微积分、无穷、虚数与非欧几何，讲“数学是绝对真理”的信念如何建立又如何被动摇。 |
| 数学的三个纲领：逻辑、形式语言，以及直觉（数学哲学系列 8） | 同上 | [`math/philosophy-of-math/three-programs-logic-formalism-intuition/`](math/philosophy-of-math/three-programs-logic-formalism-intuition/index.html) | 逻辑主义、形式主义、直觉主义三条路各自撞上罗素悖论、哥德尔不完备与“令人汗颜的尴尬”。 |
| 数学是实在还是工具？工作日的柏拉图主义和周末的形式主义（数学哲学系列 9） | 同上 | [`math/philosophy-of-math/platonist-weekdays-formalist-weekends/`](math/philosophy-of-math/platonist-weekdays-formalist-weekends/index.html) | 从“发现还是发明”到三个纲领的困境，用 Mandelbrot 集、弗雷格与哥德尔的论证讲数学柏拉图主义及其两大诘难。 |
| 客观宇宙的唯一可能是数学？（数学哲学系列 10） | 同上 | [`math/philosophy-of-math/is-the-universe-mathematics/`](math/philosophy-of-math/is-the-universe-mathematics/index.html) | 结构主义、一首曲子的无数载体、一朵黄花的五种现实，一路走到 Tegmark 的数学宇宙假说，再绕回老子的“道”与康德。 |

#### 大数（`math/large-numbers/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| TREE(3) 的规则那么简单，为什么它的值那么离谱的大？ | 知乎答主 HypCos（主）、大老李 | [`math/large-numbers/why-tree3-is-so-large/`](math/large-numbers/why-tree3-is-so-large/index.html) | 先讲 TREE 游戏与良拟序为什么保证有限，再沿 JavaScript 大数高尔夫的字符数阶梯爬上 ε₀、Γ₀、ψ(Ω_ω)。 |

#### 通识（`math/general/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| 素数分布：欧拉一维，黎曼二维，有没有人在更高维度思考？ | 知乎答主 清人（主）、lliog、南方 | [`math/general/primes-in-higher-dimensions-langlands/`](math/general/primes-in-higher-dimensions-langlands/index.html) | 朗兰兹纲领把素数问题升到无穷维对称空间：伽罗瓦表示与自守表示是同一件事的 AB 面。 |
| 格罗腾迪克与格罗腾迪克宇宙：从「宇宙」到「母题」 | 知乎专栏「缘法无情」整理；含 Colin McLarty（2010）摘译与 J. S. Milne《母题——Grothendieck 的梦想》中译 | [`math/general/grothendieck-universes/`](math/general/grothendieck-universes/index.html) | 先讲清格罗腾迪克宇宙为何比 ZFC 模型强得多，再走完 Milne 的母题综述：猜想 C、D，Weil 猜想，模性与 BSD。 |

### 哲学（`philosophy/general/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| 哲学上从 0 到 1 这个奇点是如何发生的？ | 知乎答主 高大早，及同一问题下另一位答主 | [`philosophy/general/from-zero-to-one-singularity/`](philosophy/general/from-zero-to-one-singularity/index.html) | 冯·诺伊曼序数用「空集 → {空集}」造出 0 和 1；拉康说 0 是体系的自指。 |

### 设计（`design/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| 计算器上用的是什么字体？段码字 | oooooohmygosh，知乎日报（由微梨《一起来玩段码字》升级而来） | [`design/segment-display-fonts/`](design/segment-display-fonts/index.html) | 从辉光管到 7、9、16、22 段码，用可交互的段码显示器讲 BEGHILOSZ 翻转字谜、传呼机语和段码字的艺术设计。 |

---

这些页面由 Claude Code 基于原文生成，仅供学习。
