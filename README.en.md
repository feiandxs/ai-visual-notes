[中文](README.md)

# ai-visual-notes

Illustrated, animated visual explainers of articles, made for beginners. Content is not limited to AI; it covers personal study notes on AI, software, physics, science, mathematics, philosophy, language, culture, society, design and more. One subdirectory per article, each a single HTML file you can open directly in a browser.

## Index

### AI (`ai/`)

| Title | Original author / source | Page | Summary |
| --- | --- | --- | --- |
| What Is ChatGPT Doing … and Why Does It Work? | Stephen Wolfram | [`ai/wolfram-what-is-chatgpt-doing/`](ai/wolfram-what-is-chatgpt-doing/index.html) | How ChatGPT generates text one token at a time, and why it works, in diagrams and animations. |
| AI Coding Editors Aren't Magic: How Cline Works | nazha, nazha.co (2025-01-24) | [`ai/how-cline-works/`](ai/how-cline-works/index.html) | A visual teardown of Cline: system prompt, XML tool protocol, environment snapshots, and the multi-turn loop. |
| Inside Cline + DeepSeek R1: How Autonomous Coding Actually Works | Heycc, Heycc's blog (2025-02-11) | [`ai/deepseek-r1-cline-autonomous-coding/`](ai/deepseek-r1-cline-autonomous-coding/index.html) | Proxying every prompt Cline sends to DeepSeek R1 and dissecting a real coding task round by round. |
| Building Effective Claude Agents with Code, MCP, and Skills (Anthropic Podcast) | Anthropic Podcast, Alex Albert in conversation with Erik Schluntz; Chinese write-up: 莫尔索随笔 (2025-11-04) | [`ai/anthropic-podcast-building-agents/`](ai/anthropic-podcast-building-agents/index.html) | From “coding is the core agent skill” to “tools should mirror the UI, not the API”: agent architecture evolution and three best practices. |
| What AI Applications Teach Us About Engineering Cognition | Li Peigen (Academician, Chinese Academy of Engineering; Huazhong University of Science and Technology), Research in Higher Education of Engineering | [`ai/li-peigen-ai-engineering-cognition/`](ai/li-peigen-ai-engineering-cognition/index.html) | Kant's thing-in-itself, tacit and dark knowledge, process view, chain-of-thought and the objective paradox: how AI reshapes engineering cognition. |
| There Are No Tokens in the Semantic Computer | 孔某人, WeChat account 「孔某人的低维认知」 (2025-01) | [`ai/semantic-computer-no-token/`](ai/semantic-computer-no-token/index.html) | Just as C has no registers: the context as a semantic program and the LLM as the computer that runs it, covering test-time compute, reward design and A*-like exploration. |
| Notes on Mooncake | Xu Xinran, Zhihu column (2024-06-28) | [`ai/mooncake-overview-notes/`](ai/mooncake-overview-notes/index.html) | The bold claims behind Kimi's Mooncake serving system: prefill/decode disaggregation, the KVCache bottleneck, and heterogeneous clusters. |
| Mooncake: Kimi's KVCache-centric Disaggregated Serving Architecture | ZHANG Mingxing, Zhihu column KVCache.AI (2024-06, edited 2024-11-28); supplemented with the Mooncake paper (FAST '25) | [`ai/mooncake-1-kvcache-centric-disaggregation/`](ai/mooncake-1-kvcache-centric-disaggregation/index.html) | Step through a request across the Prefill, Decode and KVCache pools; compare TBT vs TPOT, chunked prefill's VRAM cost and Chunked PP, and compute when fetching KVCache beats recomputing it. |
| Mooncake (2): Handling Kimi's Traffic Flood with Prediction-based Scheduling in a Disaggregated Architecture | ZHANG Mingxing, Zhihu column KVCache.AI (edited 2024-11-28); supplemented with the Mooncake paper (2024) | [`ai/mooncake-2-prediction-based-scheduling/`](ai/mooncake-2-prediction-based-scheduling/index.html) | Early Reject under overload, the prefill/decode seesaw effect and prediction-based rejection, with a tunable overload-scheduling simulator. |
| OIBench and CoreCodeBench: How Good Are LLMs at Coding, Really? | Meituan-M17, Meituan Tech Blog (2025-07-17) | [`ai/meituan-oibench-corecodebench/`](ai/meituan-oibench-corecodebench/index.html) | Two benchmarks, Olympiad-level algorithms and repository-level engineering tasks, with sortable leaderboards, pseudocode gains, human comparison, single vs multi-function results and a correlation heatmap. |
| A PM's Guide to AI Agent Architecture: Why Capability Doesn't Equal Adoption | Umang Sehgal, Product Curious (2025-09-04); Chinese translation by WeChat account 宝玉AI (2025-09-05) | [`ai/ai-agent-architecture-guide-for-pms/`](ai/ai-agent-architecture-guide-for-pms/index.html) | Four architecture layers, four orchestration patterns and why calibrated honesty beats confident accuracy, told through one customer-support agent. |
| Anatomy of Cline's System Prompt | Cline project, GitHub cline/cline, src/core/prompts/system.ts (clipped 2025-04-26) | [`ai/cline-system-prompt-anatomy/`](ai/cline-system-prompt-anatomy/index.html) | Cline's system prompt taken apart section by section: tool definitions, the XML tool-call protocol, editing rules, ACT/PLAN modes, rules and the objective loop. |
| Manus's Six Laws of Context Engineering | @frxiaobei, X (2025-07-21) | [`ai/manus-context-engineering-six-laws/`](ai/manus-context-engineering-six-laws/index.html) | Six context-engineering rules for AI agents (KV-cache, tool masking, file system as memory, todo recitation, keeping errors, avoiding few-shot mimicry), each with a hands-on toy experiment. |
| Is DeepSeek-R1-Zero's Pure RL Just Supervised Learning? | Compiled in this repo; references: 卡卡罗特 (Zhihu answer excerpt), DeepSeek-R1 paper, DeepSeekMath (GRPO), Liu et al. (2025), Yue et al. (2025) | [`ai/deepseek-r1-zero-rl-or-supervised-learning/`](ai/deepseek-r1-zero-rl-or-supervised-learning/index.html) | Data-flow comparison, an interactive GRPO group-advantage demo, deriving RL as weighted SFT, and a toy on-policy simulation showing where R1-Zero and SFT agree and differ. |

### Software (`software/`)

| Title | Original author / source | Page | Summary |
| --- | --- | --- | --- |
| Why Do React Hooks Rely on Call Order? | Dan Abramov, overreacted.io (2018-12-13) | [`software/why-react-hooks-rely-on-call-order/`](software/why-react-hooks-rely-on-call-order/index.html) | Hooks stored as an ordered list, and interactive demos of how keyed, Symbol, factory and other alternative designs break down. |
| Linear Sent Me Down a Local-First Rabbit Hole | Jye Cusch, bytemash.net (2025-08-04) | [`software/linear-local-first-rabbit-hole/`](software/linear-local-first-rabbit-hole/index.html) | Why Linear feels instant: a latency race, an offline/conflict sync simulator, Jazz CoValues and encryption, Electric Shapes, an ecosystem table and a fit checker. |
| The Security Model of Dark Web Marketplaces: A Security Engineering Case Study | Evan Boehs, boehs.org (2024-11-30) | [`software/dark-web-marketplace-security-model/`](software/dark-web-marketplace-security-model/index.html) | JavaScript-free captchas, PGP-signed mirror lists and 2FA, tiered private mirrors, escrow exit-scam risk and Monero, unpacked as a threat model with interactive demos. |

### Physics · Astrophysics (`physics/astrophysics/`)

| Title | Original author / source | Page | Summary |
| --- | --- | --- | --- |
| Where Did the Universe's First Matter Come From? | Zhihu answerers 时空通讯, 我喜欢小笼包, 王清扬 | [`physics/astrophysics/where-did-matter-come-from/`](physics/astrophysics/where-did-matter-come-from/index.html) | The Big Bang singularity, vacuum zero-point energy, and why energy need not be conserved on cosmological scales. |
| Is Time an Imaginary Dimension? | Zhihu answerers Timothy Liu, 零者 | [`physics/astrophysics/is-time-an-imaginary-dimension/`](physics/astrophysics/is-time-an-imaginary-dimension/index.html) | From vector covariance and the constancy of light speed to the invariant spacetime interval and why time can be written as ict. |

### Physics · Theoretical Physics (`physics/theoretical/`)

| Title | Original author / source | Page | Summary |
| --- | --- | --- | --- |
| On the Nature of Time: A Computational View | Stephen Wolfram (2024-10-08) | [`physics/theoretical/wolfram-on-the-nature-of-time/`](physics/theoretical/wolfram-on-the-nature-of-time/index.html) | Time is the universe doing computation; irreducibility plus bounded observers make it one-threaded, unskippable and directional. |
| Why Does Observation Cause Wavefunction Collapse? | Zhihu answerers 贾明子, 陈童 | [`physics/theoretical/why-observation-collapses/`](physics/theoretical/why-observation-collapses/index.html) | The three postulates, U vs R processes, the von Neumann chain, three interpretations, and what decoherence can and cannot explain. |
| Does Quantum Entanglement Mean Faster-than-Distance Connections? | Zhihu answerer 拉格朗日的忧郁 | [`physics/theoretical/quantum-entanglement-nonlocality/`](physics/theoretical/quantum-entanglement-nonlocality/index.html) | Entanglement is nonlocal, yet the no-communication theorem means it cannot carry information. |
| Are All Electrons Identical? | Zhihu answerer 酱紫君 | [`physics/theoretical/are-all-electrons-identical/`](physics/theoretical/are-all-electrons-identical/index.html) | Every electron is an excitation of one Dirac field, a “singleton”; anticommutation yields Pauli exclusion. |
| How Do Scientists Emit Photons One at a Time? | Unattributed Q&A compilation | [`physics/theoretical/single-photon-sources/`](physics/theoretical/single-photon-sources/index.html) | Four ways to make single photons on demand and why quantum dots dominate. |
| Norton's Dome: Can Newtonian Mechanics Be Indeterministic? | 东方既白, Zhihu column 「数理灵感笔记」 | [`physics/theoretical/nortons-dome/`](physics/theoretical/nortons-dome/index.html) | A dome where Newton's equation admits multiple solutions, and why uniqueness fails. |
| Why Generalized Coordinates Are Not Functions of Time | Zhihu answerers 東雲正樹, Skadiologist | [`physics/theoretical/generalized-coordinates-lagrangian/`](physics/theoretical/generalized-coordinates-lagrangian/index.html) | Coordinates on state space vs functions along a path: q, q̇, the action principle, partial vs total derivatives. |
| Atoms Aren't Conscious, So Why Are We? | Zhihu answerer 清人 and another answer to the same question | [`physics/theoretical/consciousness-from-atoms/`](physics/theoretical/consciousness-from-atoms/index.html) | The free-energy principle as a framework for consciousness, plus panpsychism vs emergence and attention-schema theory. |

### Science (`science/`)

| Title | Original author / source | Page | Summary |
| --- | --- | --- | --- |
| Why Can't Birds See Glass? | 剁椒鹿, Zhihu (2025-02-24); reorganized, supplemented with Loss et al. (2014), Klem & Saenger (2013) | [`science/why-birds-cannot-see-glass/`](science/why-birds-cannot-see-glass/index.html) | Starting from a joke about miming window-cleaning: humans infer glass from cues, birds lack them, the reflection and transparency traps, and how marker spacing rules make glass visible to birds. |
| Solar Chimneys: Viable Energy Solution or a Lot of Hot Air? | Lewin Day, Hackaday (2024-01-15) | [`science/solar-chimneys/`](science/solar-chimneys/index.html) | How a greenhouse collector, chimney and turbine make power, why output demands enormous scale, lessons from the Manzanares prototype and the Jinshawan project, and why solar PV wins. |

### Mathematics (`math/`)

#### Philosophy of Mathematics (`math/philosophy-of-math/`)

| Title | Original author / source | Page | Summary |
| --- | --- | --- | --- |
| Is Mathematics Truth? The Dilemma of Classical Platonism (Part 7) | 贾明子, Zhihu column《何为现实？拉普拉斯之妖与薛定谔猫之决战》 | [`math/philosophy-of-math/is-math-truth-platonism-dilemma/`](math/philosophy-of-math/is-math-truth-platonism-dilemma/index.html) | From Pythagoras, Plato and Euclid to calculus, infinity, imaginary numbers and non-Euclidean geometry: how the belief that mathematics is absolute truth was built, then shaken. |
| Three Programs for Mathematics: Logic, Formal Language, and Intuition (Part 8) | 贾明子, Zhihu column《何为现实？拉普拉斯之妖与薛定谔猫之决战》 | [`math/philosophy-of-math/three-programs-logic-formalism-intuition/`](math/philosophy-of-math/three-programs-logic-formalism-intuition/index.html) | Logicism, formalism and intuitionism each hit their own wall: Russell's paradox, Gödel's incompleteness, and an "embarrassing" reconstruction. |
| Is Mathematics Real or a Tool? Platonist on Weekdays, Formalist on Weekends (Part 9) | 贾明子, Zhihu column《何为现实？拉普拉斯之妖与薛定谔猫之决战》 | [`math/philosophy-of-math/platonist-weekdays-formalist-weekends/`](math/philosophy-of-math/platonist-weekdays-formalist-weekends/index.html) | From "discovered or invented" to mathematical platonism via the Mandelbrot set, Frege and Gödel, and its two big objections. |
| Is Mathematics the Only Possible Objective Universe? (Part 10) | 贾明子, Zhihu column《何为现实？拉普拉斯之妖与薛定谔猫之决战》 | [`math/philosophy-of-math/is-the-universe-mathematics/`](math/philosophy-of-math/is-the-universe-mathematics/index.html) | Structuralism, one melody in many carriers, one flower in five realities, up to Tegmark's Mathematical Universe Hypothesis, and back to the Dao and Kant. |

#### Large Numbers (`math/large-numbers/`)

| Title | Original author / source | Page | Summary |
| --- | --- | --- | --- |
| Why Is TREE(3) So Absurdly Large? | Zhihu answerers HypCos (primary), 大老李 | [`math/large-numbers/why-tree3-is-so-large/`](math/large-numbers/why-tree3-is-so-large/index.html) | From the TREE game and well-quasi-ordering to a JavaScript big-number golf ladder climbing past ε₀, Γ₀ and ψ(Ω_ω). |

#### Abstract Algebra (`math/abstract-algebra/`)

| Title | Original author / source | Page | Summary |
| --- | --- | --- | --- |
| Music and Abstract Algebra: ℤ₁₂, the Circle of Fifths and the PLR Group | Zhihu answer "How to let people who don't know math feel the charm of abstract algebra?" (answerer: Zhihu user, name not archived; edited 2025-03-02); supplemented with Tymoczko (2006) and Crans–Fiore–Satyendra (2009) | [`math/abstract-algebra/music-and-abstract-algebra/`](math/abstract-algebra/music-and-abstract-algebra/index.html) | Equal temperament vs Pythagorean tuning on a piano, a ℤ₁₂ clock with generators, P/L/R flips on the Tonnetz, and the Cayley graph showing the PLR group is the dihedral group D₁₂ (verified live), plus crab canon and twelve-tone rows. |

#### Decision (`math/decision/`)

| Title | Original author / source | Page | Summary |
| --- | --- | --- | --- |
| The 37% Rule: The Secretary Problem and Optimal Stopping | Personal study note, drawing on Ferguson (1989), Christian & Griffiths "Algorithms to Live By" and others | [`math/decision/optimal-stopping-37-percent-rule/`](math/decision/optimal-stopping-37-percent-rule/index.html) | From the four rules of the secretary problem to the 1/e derivation, with a playable Monte Carlo simulator, eight variants, and a check of which everyday "37%" uses are real and which are misuses. |

#### General (`math/general/`)

| Title | Original author / source | Page | Summary |
| --- | --- | --- | --- |
| Primes in Higher Dimensions: The Langlands Program | Zhihu answerers 清人 (primary), lliog, 南方 | [`math/general/primes-in-higher-dimensions-langlands/`](math/general/primes-in-higher-dimensions-langlands/index.html) | The Langlands program lifts primes into infinite-dimensional symmetry: Galois and automorphic representations as two sides of one coin. |
| Grothendieck Universes and Motives: Grothendieck's Dream | Compiled by Zhihu column 「缘法无情」; includes excerpts translated from Colin McLarty (2010) and a Chinese translation of J. S. Milne, "Motives: Grothendieck's Dream" | [`math/general/grothendieck-universes/`](math/general/grothendieck-universes/index.html) | Why a Grothendieck universe is far stronger than a ZFC model, then Milne's survey of motives: Conjectures C and D, the Weil conjectures, modularity and BSD. |

### Philosophy (`philosophy/general/`)

| Title | Original author / source | Page | Summary |
| --- | --- | --- | --- |
| How Does the Leap from 0 to 1 Happen? | Zhihu answerer 高大早, and another answer to the same question | [`philosophy/general/from-zero-to-one-singularity/`](philosophy/general/from-zero-to-one-singularity/index.html) | Von Neumann ordinals build 0 and 1 from the empty set; Lacan reads 0 as the system's self-reference. |

### Language (`language/`)

| Title | Original author / source | Page | Summary |
| --- | --- | --- | --- |
| What Makes a Chinese Name Sound Good? Tones, Initials and Finals | Personal study note, drawing on the Ministry of Public Security national name reports 2019–2021, Cao et al. (2002), van de Weijer et al. (2020) and others | [`language/chinese-name-phonetics/`](language/chinese-name-phonetics/index.html) | A tone sandbox for any name, initial/final matrices, tone statistics of popular names: pingze, tone sandhi, the three sources of tongue-twisting, and corrections to common myths like "voiced vs voiceless contrast". |
| Which English Letter Could We Delete with the Least Harm? | Zhihu answerers 软箭攻城师 (main), 杞鋂, 汪萌玉盘 (2023-10-29) | [`language/english-which-letter-to-delete/`](language/english-which-letter-to-delete/index.html) | Runs the 'EuroEnglish five-year plan' spelling joke as code, charts letter frequencies, lets you delete any letter, detects lipograms, and shows why the POW tap code dropped K. |

### Culture & History (`culture/`)

| Title | Original author / source | Page | Summary |
| --- | --- | --- | --- |
| What Is Dieselpunk? | 攀刀 (Pan Dao), Zhihu column APAN呼叫地面 (2020-11-26) | [`culture/what-is-dieselpunk/`](culture/what-is-dieselpunk/index.html) | A techno-mood curve around WWI, steampunk vs dieselpunk vs cyberpunk, from real history to alternate worlds, a story-premise builder, one airship in three styles, and key works. |
| Horse Details and the Curse of Knowledge | Zhihu answerer (name not archived), quoting Ma Boyong's "The Curse of Knowledge" (2025-01-03) | [`culture/rdr2-horse-detail-curse-of-knowledge/`](culture/rdr2-horse-detail-curse-of-knowledge/index.html) | Why build details in Red Dead Redemption 2's horses that almost no one notices? Ma Boyong's seven ever-more-detailed drafts of an inn checkout show where detail turns into a curse. |
| Which of the Cool Computer Terminals in Marvel's Loki Are Real? | Sascha Segan, PCMag (2021-06-10) | [`culture/loki-computer-terminals/`](culture/loki-computer-terminals/index.html) | The TVA lobby's orange ADM-3A terminals, a holoprojector keyboard with no P key, plus an ADM-3A simulator and a retro CRT effects playground. |
| Dead Reckoning: The Wreck and Mutiny of HMS Wager | Alan Bellows, Damn Interesting (2019-09) / Chinese translation by 宝玉, baoyu.io (2025-05-10) | [`culture/hms-wager-shipwreck-and-mutiny/`](culture/hms-wager-shipwreck-and-mutiny/index.html) | HMS Wager wrecks off Chile in 1741 and the survivors split between captain and gunner: a steppable route map, a dead-reckoning error simulator, a relationship graph, and the two escape routes compared. |
| The Ancestors' "Decision": Are Uncontacted Tribes "Primitive" or Making a Choice? | fivestone, fieldnotes (anthropology.fivest.one, 2020-05-11); reorganized in this repo | [`culture/ancestors-decision-anthropology/`](culture/ancestors-decision-anthropology/index.html) | Starting from Ricardo Stuckert's aerial photos of an isolated Amazon village, this page checks the "living like 20,000 years ago" claim and reframes isolation as a choice made under pressure. |
| Computers in Sci-Fi Movies: What Was Behind the Screen, and What Changed Because of It | Compiled in this repo; references: ASC, Propstore, BFI Screenonline, NASM (Ceruzzi), PCMag, Yanko Design, Wikipedia and others | [`culture/sci-fi-movie-computers/`](culture/sci-fi-movie-computers/index.html) | From Alien's junk-built panels and wireframe terrain to Brazil, Pip-Boy, HAL 9000, Minority Report, LCARS, digital rain, WarGames and Tron: which were real machines, which were props, and how film and reality influenced each other; with wireframe terrain, magnifier, gesture panels, digital rain and war-dialer demos. |

### Society (`society/`)

| Title | Original author / source | Page | Summary |
| --- | --- | --- | --- |
| After Two-Thirds Agree to Install an Elevator, Is It Too Late to Stop It? | Zhihu answerer (name not archived); supplemented with Civil Code Art. 278 and the SPC's 2023 elevator retrofit cases | [`society/elevator-installation-two-thirds-consent/`](society/elevator-installation-two-thirds-consent/index.html) | A Zhihu playbook for stalling an elevator retrofit, checked step by step against China's Civil Code voting thresholds, city rules and court cases, with a vote calculator and cost-sharing tool. |

### Design (`design/`)

| Title | Original author / source | Page | Summary |
| --- | --- | --- | --- |
| What Font Do Calculators Use? Segment Display Fonts | oooooohmygosh, Zhihu Daily (upgraded from 微梨's "Let's Play with Segment Fonts") | [`design/segment-display-fonts/`](design/segment-display-fonts/index.html) | From Nixie tubes to 7-, 9-, 16- and 22-segment displays: interactive displays explain the BEGHILOSZ puzzle, pager-speak and the art of segment fonts. |
| I Am Sorry, but Everyone Is Getting Syntax Highlighting Wrong | Nikita Prokopov (tonsky), tonsky.me (2025-10-15) | [`design/syntax-highlighting-wrong/`](design/syntax-highlighting-wrong/index.html) | Syntax highlighting is a scanning tool, not Christmas lights: a timed lookup race, a four-color budget, what deserves color, bright comments, light-theme pitfalls, and stripping a theme down step by step. |

#### GUI Design History (`design/gui-history/`)

| Title | Original author / source | Page | Summary |
| --- | --- | --- | --- |
| Mac Visual History (1): From Macintosh to Mac OS | 陈子木, sspai (2020-05-19, first published on uisdc) | [`design/gui-history/mac-visual-history-1-macintosh-to-mac-os/`](design/gui-history/mac-visual-history-1-macintosh-to-mac-os/index.html) | An era slider redraws the Classic Mac desktop from System 1 to Mac OS 9 as wireframes, with a naming timeline, the 512×342 pixel budget, MFS vs HFS folders, font smoothing and a side-by-side control comparison. |
| Mac Visual History (2): The Failed Mac Operating Systems of the 1990s | 陈子木, sspai (2020-05-27; first published on uisdc) | [`design/gui-history/mac-visual-history-2-failed-90s-mac-os/`](design/gui-history/mac-visual-history-2-failed-90s-mac-os/index.html) | Pink/Taligent, Star Trek and Copland fail one after another before BeOS and NeXTSTEP face off: a clickable lineage map, Pink's headcount bloat curve and wireframe UI comparisons. |
| Mac Visual History vol.2.5: Shunji Yamanaka's DrawingBoard | 陈子木, sspai (2024-02-07) | [`design/gui-history/mac-visual-history-2-5-yamanaka-drawingboard/`](design/gui-history/mac-visual-history-2-5-yamanaka-drawingboard/index.html) | The sketch-style Mac GUI industrial designer Shunji Yamanaka pitched to Apple around 1994: its visual grammar, concept vs. shipped theme, and the four Mac OS 8.5 beta themes compared. |
| Mac Visual History (3): Aqua and the Water-Reborn Look of Mac OS X | 陈子木, sspai (2020-06-10; first published on uisdc) | [`design/gui-history/mac-visual-history-3-aqua-mac-os-x/`](design/gui-history/mac-visual-history-3-aqua-mac-os-x/index.html) | From grey bevelled 90s GUIs through Rhapsody and the iMac G3 to Aqua, with side-by-side window wireframes, a column-view demo and a tunable gel-button lab. |
| Windows Design History 01: From Awkward to Mature (Windows 1.0 – 95) | SUNTRISE, sspai (2024-05-06) | [`design/gui-history/windows-design-history-1-from-1-0-to-95/`](design/gui-history/windows-design-history-1-from-1-0-to-95/index.html) | Tiled vs overlapping windows, Susan Kare's icons, 3D bevels, TrueType, and how usability testing produced the Start menu and taskbar. |
| Windows Design History 02: Project Neptune, the Search Behind the "Stable" Surface | SUNTRISE, sspai (2024-05-13) | [`design/gui-history/windows-design-history-2-neptune/`](design/gui-history/windows-design-history-2-neptune/index.html) | From the Windows 98 Desktop Update to RedShark and Neptune's Activity Centers: Microsoft's unfinished attempt to replace desktop and windows with task-centered pages. |
| Windows Design History 03: Windows XP, From Mechanical to Natural | SUNTRISE, sspai | [`design/gui-history/windows-design-history-3-windows-xp/`](design/gui-history/windows-design-history-3-windows-xp/index.html) | Win95 vs Luna wireframes, a 3D 'mascara' slider, decoy themes and Luna color schemes, Bliss color picking, the waving-flag logo and Fitts' law at the Start button. |
| Windows 1.0 to 3.11: How the First Decade of Windows UI Evolved | Dmitrii Eliuseev, UX Collective (2021-03-20) / Chinese translation by uisdc.com | [`design/gui-history/windows-35-years-ui-evolution/`](design/gui-history/windows-35-years-ui-evolution/index.html) | Revisiting Windows 1.01 to 3.11 in an emulator: tiled vs overlapping windows, DOS vs Windows programs, a 1200 bit/s modem, 8.3 filenames, TrueType scaling and a Visual Basic 1.0 event demo. |
| Windows 98's User Onboarding | Benjamin Brandall, Usersnap blog (2016-09-27) / Chinese translation by uisdc.com | [`design/gui-history/windows-98-onboarding/`](design/gui-history/windows-98-onboarding/index.html) | Click through a Welcome to Windows 98 re-enactment: progressive profiling, the Recycle Bin empty state, Typical setup, practice exercises and consistency. |
| Apple Lisa: The Buried GUI Pioneer | YellowColr, sspai (2025-04-28) | [`design/gui-history/apple-lisa-forgotten-gui-pioneer/`](design/gui-history/apple-lisa-forgotten-gui-pioneer/index.html) | Lisa at 40: from 'Do It' to OK, modal vs modeless editing, Twenty Questions vs icons and folders, document-centric stationery, Lisa vs Macintosh specs and price, and the 1989 landfill burial. |
| Ten Years On, I Still Miss You: The People and Ideas Behind Palm webOS | 陈子木, sspai (2021-08-19) | [`design/gui-history/webos-ten-years-later/`](design/gui-history/webos-ten-years-later/index.html) | A letter to webOS made interactive: gesture area, flick-to-close cards, bottom notifications, Touchstone and Touch2Share, and where the team went next. |

#### Typography (`design/typography/`)

| Title | Original author / source | Page | Summary |
| --- | --- | --- | --- |
| Five Myths About Grid Systems in Chinese Typesetting | Eric Q. Liu, 钱争予, The Type (2020-01-28) | [`design/typography/chinese-typesetting-grid-five-myths/`](design/typography/chinese-typesetting-grid-five-myths/index.html) | Live Chinese text and CSS demos of the character-cell grid, sizing the text block before margins, counting in characters and lines, and the trade-offs of strict grid alignment. |

---

These pages were generated by Claude Code from the original articles, for learning purposes only.
