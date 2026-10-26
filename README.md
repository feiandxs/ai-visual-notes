[English](README.en.md)

# ai-visual-notes

把文章做成图文并茂、带动画的可视化讲解页面，供初学者学习。内容涵盖 AI、软件、物理、科学、数学、哲学、语言、文化、社会、设计等个人学习笔记。每篇一个子目录，均为单文件 HTML，可直接用浏览器打开。

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
| 关于 Mooncake 的碎碎念 | 许欣然，知乎专栏（2024-06-28） | [`ai/mooncake-overview-notes/`](ai/mooncake-overview-notes/index.html) | Kimi 推理系统 Mooncake 背后的几条「暴论」：P/D 分离、KVCache 瓶颈与异构集群。 |
| Mooncake：Kimi 以 KVCache 为中心的分离式推理架构 | ZHANG Mingxing（章明星），知乎专栏 KVCache.AI（2024-06，2024-11-28 编辑）；补充参考 Mooncake 论文（FAST '25） | [`ai/mooncake-1-kvcache-centric-disaggregation/`](ai/mooncake-1-kvcache-centric-disaggregation/index.html) | 可步进的三池架构流程、TBT 与 TPOT 对比、chunked prefill 显存代价、Chunked PP 流水线，以及 KVCache 搬运与重算的现场计算。 |
| Mooncake (2)：Kimi 的「泼天流量」怎么接，分离架构下基于预测的调度 | ZHANG Mingxing，知乎专栏《KVCache.AI》（2024-11-28 编辑）；补充参考 Mooncake 论文 (2024) | [`ai/mooncake-2-prediction-based-scheduling/`](ai/mooncake-2-prediction-based-scheduling/index.html) | 过载时的 Early Reject、负载跷跷板效应与基于预测的拒绝策略，附可调参数的过载调度模拟器。 |
| OIBench 与 CoreCodeBench：大模型编程能力的真实水平 | Meituan-M17，美团技术团队博客（2025-07-17） | [`ai/meituan-oibench-corecodebench/`](ai/meituan-oibench-corecodebench/index.html) | 奥赛级算法题与真实仓库工程题两套基准：可排序可切换的榜单、伪代码提升、人机对比、单/多函数与相关性热力图。 |
| 产品经理的 AI 智能体架构指南：能力强为什么不等于用户爱用 | Umang Sehgal，Product Curious（2025-09-04）；中文编译：公众号「宝玉AI」（2025-09-05） | [`ai/ai-agent-architecture-guide-for-pms/`](ai/ai-agent-architecture-guide-for-pms/index.html) | 四个架构层、四种编排模式与「坦诚胜过自信」的信任策略，贯穿一个客服智能体案例。 |
| 拆解 Cline 的系统提示词 | Cline 项目，GitHub cline/cline，src/core/prompts/system.ts（剪藏于 2025-04-26） | [`ai/cline-system-prompt-anatomy/`](ai/cline-system-prompt-anatomy/index.html) | 把 Cline 的系统提示词拆成结构图：工具定义、XML 调用协议、编辑规则、模式、规则与目标循环。 |
| Manus 的六条上下文工程法则 | @frxiaobei，X（2025-07-21） | [`ai/manus-context-engineering-six-laws/`](ai/manus-context-engineering-six-laws/index.html) | KV 缓存、工具掩码、文件系统外置、todo 复述、保留错误、避免少样本模仿，六条智能体上下文法则各配一个可操作实验。 |
| R1-Zero 的纯 RL，为什么看起来像监督学习？ | 本仓库整理，参考：卡卡罗特（知乎）问题摘要、DeepSeek-R1 论文、DeepSeekMath（GRPO）、Liu 等（2025）、Yue 等（2025） | [`ai/deepseek-r1-zero-rl-or-supervised-learning/`](ai/deepseek-r1-zero-rl-or-supervised-learning/index.html) | 数据流对比、GRPO 组内优势演示、RL 推成加权 SFT、on-policy 玩具模拟：R1-Zero 与 SFT 的同与不同。 |
| Transformer：大语言模型背后的机器 | 3Blue1Brown，YouTube《Transformers, the tech behind LLMs》（深度学习第 5 章） | [`ai/transformers-3b1b-tech-behind-llms/`](ai/transformers-3b1b-tech-behind-llms/index.html) | 逐词采样、词嵌入与语义方向、点积、上下文长度、softmax 与温度，并现场算出 GPT-3 的 1750 亿参数花在哪些矩阵上；10 个可操作的演示。 |
| 注意力机制：词与词之间怎样互相“更新” | 3Blue1Brown，YouTube《Attention in transformers, step-by-step》（深度学习第 6 章） | [`ai/attention-in-transformers-3b1b/`](ai/attention-in-transformers-3b1b/index.html) | 改写自 3Blue1Brown 第 6 章，用可拖动的 Query/Key、因果遮罩热力图、逐步更新演示、多头切换和参数量计算器弄清注意力。 |
| 智能体循环到底是什么：目标、校验与停止条件 | Nate Herk \| AI Automation，YouTube《Finally. Agent Loops Clearly Explained.》 | [`ai/agent-loops-clearly-explained/`](ai/agent-loops-clearly-explained/index.html) | 从「写循环，不写提示词」讲起：质量曲线、推理-行动-观察逐步模拟、三种形态、停止条件与失败模式、八个要素，以及不必 24/7 的时长标尺。 |

### 软件（`software/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| 为什么 React Hooks 依赖调用顺序 | Dan Abramov，overreacted.io（2018-12-13） | [`software/why-react-hooks-rely-on-call-order/`](software/why-react-hooks-rely-on-call-order/index.html) | Hooks 按调用顺序存成链表；字符串 key、Symbol、闭包工厂等替代方案逐个失效的可操作演示。 |
| Linear 带我掉进了 local-first 的兔子洞 | Jye Cusch，bytemash.net（2025-08-04） | [`software/linear-local-first-rabbit-hole/`](software/linear-local-first-rabbit-hole/index.html) | Linear 为何快：延迟赛跑、离线冲突同步模拟、Jazz CoValue 与加密、Electric Shape、生态对比与适用性自测。 |
| 暗网市场的安全模型：一次安全工程案例分析 | Evan Boehs，boehs.org（2024-11-30） | [`software/dark-web-marketplace-security-model/`](software/dark-web-marketplace-security-model/index.html) | 无 JS 验证码、PGP 签名镜像与双因素、分层私人镜像、托管跑路风险与 Monero，按威胁模型拆解一个长寿市场的设计。 |

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

### 科学（`science/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| 为什么鸟类看不见玻璃？ | 剁椒鹿，知乎（2025-02-24）；本页重新组织，补充参考 Loss 等 (2014)、Klem & Saenger (2013) | [`science/why-birds-cannot-see-glass/`](science/why-birds-cannot-see-glass/index.html) | 从「假装擦玻璃」的玩笑讲起：人靠线索看见玻璃，鸟眼缺线索，反射与透视两种陷阱，及防撞标记的间距规则。 |
| 太阳能烟囱：可行方案，还是一堆热空气？ | Lewin Day，Hackaday（2024-01-15） | [`science/solar-chimneys/`](science/solar-chimneys/index.html) | 集热大棚、烟囱与涡轮的剖面原理，功率为何依赖巨大尺度，Manzanares 原型与金沙湾项目的教训，以及它为何敌不过光伏。 |

### 数学（`math/`）

#### 数学哲学（`math/philosophy-of-math/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| 数学是真理吗？古典柏拉图主义的困境（数学哲学系列 7） | 贾明子，知乎专栏《何为现实？拉普拉斯之妖与薛定谔猫之决战》 | [`math/philosophy-of-math/is-math-truth-platonism-dilemma/`](math/philosophy-of-math/is-math-truth-platonism-dilemma/index.html) | 从毕达哥拉斯、柏拉图、欧几里得到微积分、无穷、虚数与非欧几何，讲“数学是绝对真理”的信念如何建立又如何被动摇。 |
| 数学的三个纲领：逻辑、形式语言，以及直觉（数学哲学系列 8） | 贾明子，知乎专栏《何为现实？拉普拉斯之妖与薛定谔猫之决战》 | [`math/philosophy-of-math/three-programs-logic-formalism-intuition/`](math/philosophy-of-math/three-programs-logic-formalism-intuition/index.html) | 逻辑主义、形式主义、直觉主义三条路各自撞上罗素悖论、哥德尔不完备与“令人汗颜的尴尬”。 |
| 数学是实在还是工具？工作日的柏拉图主义和周末的形式主义（数学哲学系列 9） | 贾明子，知乎专栏《何为现实？拉普拉斯之妖与薛定谔猫之决战》 | [`math/philosophy-of-math/platonist-weekdays-formalist-weekends/`](math/philosophy-of-math/platonist-weekdays-formalist-weekends/index.html) | 从“发现还是发明”到三个纲领的困境，用 Mandelbrot 集、弗雷格与哥德尔的论证讲数学柏拉图主义及其两大诘难。 |
| 客观宇宙的唯一可能是数学？（数学哲学系列 10） | 贾明子，知乎专栏《何为现实？拉普拉斯之妖与薛定谔猫之决战》 | [`math/philosophy-of-math/is-the-universe-mathematics/`](math/philosophy-of-math/is-the-universe-mathematics/index.html) | 结构主义、一首曲子的无数载体、一朵黄花的五种现实，一路走到 Tegmark 的数学宇宙假说，再绕回老子的“道”与康德。 |

#### 大数（`math/large-numbers/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| TREE(3) 的规则那么简单，为什么它的值那么离谱的大？ | 知乎答主 HypCos（主）、大老李 | [`math/large-numbers/why-tree3-is-so-large/`](math/large-numbers/why-tree3-is-so-large/index.html) | 先讲 TREE 游戏与良拟序为什么保证有限，再沿 JavaScript 大数高尔夫的字符数阶梯爬上 ε₀、Γ₀、ψ(Ω_ω)。 |

#### 抽象代数（`math/abstract-algebra/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| 用音乐体会抽象代数：ℤ₁₂、五度圈与 PLR 群 | 知乎回答「怎么让不懂数学的人体会到抽象代数的魅力？」（答主：知乎答主，页面未存档作者名；2025-03-02 编辑）；补充参考 Tymoczko (2006)、Crans–Fiore–Satyendra (2009) | [`math/abstract-algebra/music-and-abstract-algebra/`](math/abstract-algebra/music-and-abstract-algebra/index.html) | 十二平均律与五度相生律的钢琴对比、ℤ₁₂ 时钟与生成元、音网上的 P/L/R 翻转、PLR 群与二面体群 D₁₂ 的凯莱图及现场验证，附螃蟹卡农与十二音列。 |

#### 决策（`math/decision/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| 37% 法则：秘书问题与最优停止 | 个人学习笔记，参考 Ferguson (1989)、Christian & Griffiths《Algorithms to Live By》等 | [`math/decision/optimal-stopping-37-percent-rule/`](math/decision/optimal-stopping-37-percent-rule/index.html) | 从秘书问题的四条规则到 1/e 的推导，可玩的蒙特卡洛模拟器、八种变体对比，并逐条审视"相亲、租房、读书 37 页"哪些是真应用、哪些是误用。 |

#### 通识（`math/general/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| 素数分布：欧拉一维，黎曼二维，有没有人在更高维度思考？ | 知乎答主 清人（主）、lliog、南方 | [`math/general/primes-in-higher-dimensions-langlands/`](math/general/primes-in-higher-dimensions-langlands/index.html) | 朗兰兹纲领把素数问题升到无穷维对称空间：伽罗瓦表示与自守表示是同一件事的 AB 面。 |
| 格罗腾迪克与格罗腾迪克宇宙：从「宇宙」到「母题」 | 知乎专栏「缘法无情」整理；含 Colin McLarty（2010）摘译与 J. S. Milne《母题——Grothendieck 的梦想》中译 | [`math/general/grothendieck-universes/`](math/general/grothendieck-universes/index.html) | 先讲清格罗腾迪克宇宙为何比 ZFC 模型强得多，再走完 Milne 的母题综述：猜想 C、D，Weil 猜想，模性与 BSD。 |

### 哲学（`philosophy/general/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| 哲学上从 0 到 1 这个奇点是如何发生的？ | 知乎答主 高大早，及同一问题下另一位答主 | [`philosophy/general/from-zero-to-one-singularity/`](philosophy/general/from-zero-to-one-singularity/index.html) | 冯·诺伊曼序数用「空集 → {空集}」造出 0 和 1；拉康说 0 是体系的自指。 |

### 语言（`language/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| 汉语名字怎样读起来好听？声调、声母与韵母的搭配规律 | 个人学习笔记，参考公安部《全国姓名报告》2019–2021、Cao et al. (2002)、van de Weijer et al. (2020) 等 | [`language/chinese-name-phonetics/`](language/chinese-name-phonetics/index.html) | 可输入名字的声调试验台、声母与韵母矩阵、热门名字的声调统计，讲清平仄、变调、拗口的三种来源，并修正常见的"清浊对比"等误解。 |
| 英语里如果要删掉一个字母，删哪个影响最小？ | 知乎答主 软箭攻城师（主）、杞鋂、汪萌玉盘（2023-10-29） | [`language/english-which-letter-to-delete/`](language/english-which-letter-to-delete/index.html) | 跑一遍「欧洲英语五年计划」段子，看字母频率、亲手删字母、检测漏字文，再看敲击码为何删了 K。 |

### 文化 · 历史（`culture/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| 什么是柴油朋克？ | 攀刀，知乎专栏《APAN呼叫地面》（2020-11-26） | [`culture/what-is-dieselpunk/`](culture/what-is-dieselpunk/index.html) | 一战前后的技术情绪曲线、三种朋克对比、真实历史到架空世界、故事骨架拼装、同一艘飞艇三种风格与代表作品。 |
| 马匹细节与知识的诅咒 | 知乎答主（页面未存档作者名），引马伯庸《知识的诅咒》（2025-01-03） | [`culture/rdr2-horse-detail-curse-of-knowledge/`](culture/rdr2-horse-detail-curse-of-knowledge/index.html) | 从《荒野大镖客 2》的马匹细节之问，到马伯庸笔下越写越细的七版客栈结账：细节做到哪一步算够。 |
| 《洛基》里那些很酷的电脑终端，哪台是真的？ | Sascha Segan，PCMag（2021-06-10） | [`culture/loki-computer-terminals/`](culture/loki-computer-terminals/index.html) | TVA 大厅的橙色终端原型 ADM-3A、少了 P 键的全息投影仪，附终端模拟器与复古 CRT 效果台。 |
| 绝命航线：Wager 号沉船与叛乱 | Alan Bellows，Damn Interesting（2019-09）/ 宝玉译，baoyu.io（2025-05-10） | [`culture/hms-wager-shipwreck-and-mutiny/`](culture/hms-wager-shipwreck-and-mutiny/index.html) | 1741 年 Wager 号在智利外海触礁，幸存者分裂为舰长与炮手两派各自返航：航线地图、死算模拟、人物关系与人数点阵。 |
| 祖先的「决定」：未接触部落是「原始」还是「选择」 | fivestone，fieldnotes（anthropology.fivest.one，2020-05-11）；本页重新组织 | [`culture/ancestors-decision-anthropology/`](culture/ancestors-decision-anthropology/index.html) | 从一张亚马逊隔绝村落航拍照出发，核对「两万年前」说法，看隔绝如何是祖辈在压力下的选择。 |
| 科幻电影里的电脑：银幕背后是什么，又改变了什么 | 本仓库整理，参考：ASC、Propstore、BFI Screenonline、NASM（Ceruzzi）、PCMag、Yanko Design、Wikipedia 等 | [`culture/sci-fi-movie-computers/`](culture/sci-fi-movie-computers/index.html) | 《异形》的废料面板与线框地形、《妙想天开》、Pip-Boy、HAL 9000、《少数派报告》、LCARS、代码雨、《战争游戏》、《创》：哪些是真机、哪些是道具，以及电影与现实的双向影响；含线框地形、放大镜、手势面板、代码雨、电话扫描等演示。 |

### 社会（`society/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| 三分之二同意加装电梯后，是否无力回天？ | 知乎答主（页面未存档作者名）；补充参考《民法典》第 278 条、最高法 2023 加梯典型案例 | [`society/elevator-installation-two-thirds-consent/`](society/elevator-installation-two-thirds-consent/index.html) | 把一套「拖黄加梯」的反对策略放回民法典双三分之二、双四分之三规则、地方办法与判例里逐条检验。 |

### 设计（`design/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| 计算器上用的是什么字体？段码字 | oooooohmygosh，知乎日报（由微梨《一起来玩段码字》升级而来） | [`design/segment-display-fonts/`](design/segment-display-fonts/index.html) | 从辉光管到 7、9、16、22 段码，用可交互的段码显示器讲 BEGHILOSZ 翻转字谜、传呼机语和段码字的艺术设计。 |
| 大家把语法高亮搞错了 | Nikita Prokopov（tonsky），tonsky.me（2025-10-15） | [`design/syntax-highlighting-wrong/`](design/syntax-highlighting-wrong/index.html) | 语法高亮是扫描工具不是圣诞彩灯：限时查找对比、四色预算、该亮什么、亮注释与浅色主题陷阱，一步步剥出一个极简主题。 |

#### GUI 设计史（`design/gui-history/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| Mac 视觉史（一）：从 Macintosh 到 Mac OS | 陈子木，少数派（2020-05-19，首发优设网） | [`design/gui-history/mac-visual-history-1-macintosh-to-mac-os/`](design/gui-history/mac-visual-history-1-macintosh-to-mac-os/index.html) | 年代滑块看 System 1 到 Mac OS 9 的桌面线框演变，外加命名时间线、像素预算、抗锯齿与控件跨版本对比。 |
| Mac 视觉史（二）：90 年代失败 Mac 操作系统大赏 | 陈子木，少数派（2020-05-27，首发优设网） | [`design/gui-history/mac-visual-history-2-failed-90s-mac-os/`](design/gui-history/mac-visual-history-2-failed-90s-mac-os/index.html) | Pink/Taligent、Star Trek、Copland 接连失败，BeOS 与 NeXTSTEP 终局对决：可点谱系图、Pink 膨胀曲线与界面线框对比。 |
| Mac 视觉史 vol.2.5：山中俊治的「手绘板」DrawingBoard | 陈子木，少数派（2024-02-07） | [`design/gui-history/mac-visual-history-2-5-yamanaka-drawingboard/`](design/gui-history/mac-visual-history-2-5-yamanaka-drawingboard/index.html) | 工业设计师山中俊治 1994 年为苹果提案的手绘风 GUI：视觉语法拆解、设计稿到实装、8.5 测试版四套主题对比。 |
| Mac 视觉史（三）：浴「水」重生的 Mac 视觉美学 | 陈子木，少数派（2020-06-10，首发于优设网） | [`design/gui-history/mac-visual-history-3-aqua-mac-os-x/`](design/gui-history/mac-visual-history-3-aqua-mac-os-x/index.html) | 从 90 年代灰色斜切界面、Rhapsody、iMac G3 到 Aqua：窗口线框对比、分栏浏览演示与可调参数的水滴按钮。 |
| Windows 设计史 01：从青涩到成熟（Windows 1.0 – 95） | SUNTRISE，少数派（2024-05-06） | [`design/gui-history/windows-design-history-1-from-1-0-to-95/`](design/gui-history/windows-design-history-1-from-1-0-to-95/index.html) | 平铺与重叠窗口、Kare 图标、3D 按钮、TrueType，到可用性测试催生的开始菜单与任务栏。 |
| Windows 设计史 02：「海王星」项目，「稳定」表象背后的求索 | SUNTRISE，少数派（2024-05-13） | [`design/gui-history/windows-design-history-2-neptune/`](design/gui-history/windows-design-history-2-neptune/index.html) | 从 Windows 98 桌面更新到 RedShark 与 Neptune 活动中心：微软一次以页面和任务替代桌面与窗口的未竟探索。 |
| Windows 设计史 03：Windows XP，摆脱机械，拥抱自然 | SUNTRISE，少数派 | [`design/gui-history/windows-design-history-3-windows-xp/`](design/gui-history/windows-design-history-3-windows-xp/index.html) | Win95 与 Luna 线框对比、「睫毛膏」3D 滑块、诱饵主题与 Luna 配色、Bliss 取色、旗帜徽标与开始按钮的菲茨定律。 |
| 35 年的 Windows 界面设计演变（1.0 到 3.11） | Dmitrii Eliuseev，UX Collective（2021-03-20）/ 优设网译（译者署名土拨鼠） | [`design/gui-history/windows-35-years-ui-evolution/`](design/gui-history/windows-35-years-ui-evolution/index.html) | 在模拟器里重走 Windows 1.01 到 3.11：平铺与层叠窗口、8.3 文件名、TrueType 缩放、VB 1.0 事件演示。 |
| Windows 98 的新用户引导 | Benjamin Brandall，Usersnap 博客（2016-09-27）/ 优设译（陈子木） | [`design/gui-history/windows-98-onboarding/`](design/gui-history/windows-98-onboarding/index.html) | 亲手点一遍「欢迎使用 Windows 98」：渐进式档案、回收站空状态、典型安装、小练习与一致性原则。 |
| Apple Lisa：被埋掉的 GUI 先驱 | YellowColr，少数派（2025-04-28） | [`design/gui-history/apple-lisa-forgotten-gui-pioneer/`](design/gui-history/apple-lisa-forgotten-gui-pioneer/index.html) | Lisa 四十周年：Do It 改 OK、模态与非模态、二十个问题与文件夹、文档中心交互，以及 1989 年的埋葬。 |
| 10 年过去了，我依然很想念你：palm webOS 的人和事 | 陈子木，少数派（2021-08-19） | [`design/gui-history/webos-ten-years-later/`](design/gui-history/webos-ten-years-later/index.html) | 写给 webOS 的一封信：手势区、卡片甩出关闭、底部通知、点金石与 Touch2Share 的可操作示意，及团队人物图谱。 |

#### 字体排印（`design/typography/`）

| 标题 | 原文作者 / 出处 | 页面 | 简介 |
| --- | --- | --- | --- |
| 中文排版网格系统的五大迷思 | Eric Q. Liu（刘庆）、钱争予，The Type（2020-01-28） | [`design/typography/chinese-typesetting-grid-five-myths/`](design/typography/chinese-typesetting-grid-five-myths/index.html) | 用真实中文和 CSS 现场排版，讲字格网格、先算版心再余白、占字占行、纵横对齐的代价与半宽标点的取舍。 |

---

这些页面由 Claude Code 基于原文生成，仅供学习。
