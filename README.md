[English](README.en.md)

# ai-visual-notes

把文章做成图文并茂、带动画的可视化讲解页面，供初学者学习。内容不限于 AI，也有物理等个人学习笔记。每篇一个子目录，均为单文件 HTML，可直接用浏览器打开。

## 索引

### AI（`ai/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| ChatGPT 在做什么，为什么它有效？ | Stephen Wolfram | [`ai/wolfram-what-is-chatgpt-doing/`](ai/wolfram-what-is-chatgpt-doing/index.html) | 用图示和动画讲解 ChatGPT 如何逐词生成文本，以及它为什么有效。 |
| AI Coding 编辑器没有那么神秘：Cline 是怎么工作的 | nazha，nazha.co（2025-01-24） | [`ai/how-cline-works/`](ai/how-cline-works/index.html) | 拆开开源 AI 编程插件 Cline：系统提示词、XML 工具协议、环境快照、多轮循环。 |
| 深度解密：DeepSeek R1 + Cline 是如何做到全自动化编程的？ | Heycc，Heycc's blog（2025-02-11） | [`ai/deepseek-r1-cline-autonomous-coding/`](ai/deepseek-r1-cline-autonomous-coding/index.html) | 用本地代理截获 Cline 发给 DeepSeek R1 的每一轮 prompt，逐轮拆解 ReAct 循环、工具调用、失败恢复与 token 消耗。 |
| 用代码、MCP、Skills 构建高效 Claude 智能体（Anthropic 播客） | Anthropic 播客，Alex Albert 与 Erik Schluntz 对谈；中文整理：莫尔索随笔（2025-11-04） | [`ai/anthropic-podcast-building-agents/`](ai/anthropic-podcast-building-agents/index.html) | 从“编码是核心技能”到“工具映射 UI 而非 API”，讲清智能体架构演进与三条最佳实践。 |
| AI 应用对工程技术认知的启示 | 李培根（中国工程院院士，华中科技大学），《高等工程教育研究》 | [`ai/li-peigen-ai-engineering-cognition/`](ai/li-peigen-ai-engineering-cognition/index.html) | 从康德“物自体”、默会知识与暗知识、过程视角到思维链与目标悖论，讲 AI 如何改变工程师认识世界的方式。 |

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

---

这些页面由 Claude Code 基于原文生成，仅供学习。
