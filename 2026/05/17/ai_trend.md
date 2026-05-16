# AI 行业情报简报 | 2026-05-17

> 数据窗口：2026-05-16 06:00 — 2026-05-17 06:00（北京时间，过去 `24 小时`）
> 深度分析：3 条 | 模板版本：v2.3

本期 timeline 被 elonmusk 35 条政治/文化推文（French Theory、UK 言论自由、woke 议题等）刷屏，按"第零步：先过滤"已剔除非 AI 相关内容。下文仅基于剩余的 AI 相关信号写作。

---

## 1. 重大新闻 & 突发事件

- Google I/O 2026 倒计时启动，5 月 19 日 10:00 PT 开场

  来源：@GoogleDeepMind（转推 @Google）· 约 8 小时前
  关键数字：keynote 时间为 5 月 19 日 10:00 PT / 北京时间 5 月 20 日 01:00（来源：@GoogleDeepMind，已与 io.google/2026 keynote 页核实）
  行业影响：Gemini 系列、Veo、Nano Banana、Lyria、Gemma 的年度更新窗口集中在此，外部预期还有 agentic coding 与 Project Astra 进展。对 AI 应用层创业者意味着下周一会有一批 API/价格/能力变化需要快速跟进，再决定是否调整路线图。

- NVIDIA Nemotron 3 Super（120B / 25T tokens / NVFP4）官方推广再发声，Ultra（≈500B）尚未上线

  来源：@jeremyphoward 转推 @ctnzr（Bryan Catanzaro，NVIDIA 应用深度学习副总裁）· 约 24 小时前
  关键数字：Super 为 120B 总参 / 12B 激活，原生 NVFP4 4-bit 预训练 25T tokens，1M 上下文（来源：research.nvidia.com Nemotron-3-Super 技术报告）；Ultra 约 500B 总参 / 50B 激活，"still coming"（来源：NVIDIA 官方页，当事方口径）
  行业影响：原生 4-bit 预训练把"算力成本"和"显存成本"同步压低，是开源权重模型首次在这一规模上做到。对部署侧的实际意义是：在同等显存下推理吞吐显著高于 GPT-OSS-120B、Qwen3.5-122B，对在 H100/B100 上做 agentic 工作流的团队具有立刻可评估的成本/性能改写空间。

- xAI Grok Build CLI 上线 3 天，推出 /memory、/flush、/dream 三个记忆原语

  来源：@elonmusk 转推 @tetsuoai · 约 5 小时前
  关键数字：Grok Build CLI 定价 99 美元（来源：martincid.com，二手；NVIDIA Catanzaro 推文未涉及该数字，仅作背景）；记忆命令 /memory（读写全局/工作区/会话三层存储）、/flush（在压缩前保存当前会话摘要）、/dream（后台对历史会话做去重合并）（来源：@tetsuoai，当事方口径，未在 xAI 官方 changelog 找到对应条目，存疑）
  行业影响：把"长时记忆"作为一等公民的 CLI 原语，是当前 agentic coding 工具中较少见的做法，直接对标 Claude Code 与 Codex。对自研 agent 框架的团队意味着：可以把 capture / consolidation 拆开做，而不是把所有上下文压进 RAG。

- 资深 LLM reasoning 研究者 Julia Kempe 宣布即将离开 Meta FAIR

  来源：@ylecun 转推 @KempeLab · 约 4.5 小时前
  关键数字：在 FAIR 时间"将近两年"（来源：@KempeLab 原推，当事方口径）；只能看到 1/3 thread，后续内容缺失
  行业影响：继 LeCun 本人离开 Meta FAIR 转任 AMI Labs 之后，FAIR 推理方向人员持续流出。对正在评估 Meta 系基础模型路线（Llama 系列、Nemotron 合作之外）确定性的团队，是一个值得继续观察的弱信号。

- Mark Cuban 提议在 token 层面征联邦税，引发千条以上讨论

  来源：@EthanJPerez 转推 @mcuban · 约 14 小时前
  关键数字：建议税率 < 50 美分/百万 tokens，预测 10 年内年税收从 100 亿增长至 3000 亿—1 万亿美元（来源：@mcuban，当事方口径，未经独立验证）
  行业影响：单一观点而非政策动议，但已在开发者社区引发 2034 条回复。若未来真的进入立法讨论，对 LLM 推理服务的 unit economics 将是直接冲击。目前仅作观察，不构成定性的"行业新闻"。

---

## 深挖

#### 深挖：Google I/O 2026 keynote 启动

背景补充：
2026 年 I/O 主线确认是 Gemini 4 可能性发布、Veo 文本到视频更新、Project Astra 通用 AI 助理进展、Android 17 与 Wear OS 7（来源：tomsguide.com、androidauthority.com、io.google）。Google 在过去 24 小时内的官方动作是放出"feeling lucky"倒计时素材，不含具体功能预告。

数字核实：
keynote 时间 5 月 19 日 10:00 PT → 已验证（来源：io.google/2026、tomsguide.com、androidheadlines.com 一致）；其它具体 SKU/价格/能力数字本期暂无可核实信息。

扩展影响：
独立媒体集中讨论"agentic coding"将是大会重点之一（来源：T3、Beebom），与本期数据中 OpenAI Codex、xAI Grok Build 的密集动作呼应——三大厂同周内争夺 agentic CLI 心智份额。

对国内从业者的意义：
若 Gemini 4 / Veo 新版的 API 价格大幅下调，会拉低国内做多模态应用对火山引擎、阿里通义等的成本心理锚点；若 Project Astra 真有手机端 always-on 形态，安卓侧国内代理模式（厂商 ROM 内置）会比 Pixel 略晚但路径相似。建议把周一晚到周二早的 keynote 直播作为下周一项必看任务。

延伸阅读：
https://io.google/2026/explore/pa-keynote-1

#### 深挖：NVIDIA Nemotron 3 Super 与 Ultra

背景补充：
Nemotron 3 Super 实际发布日期为 2026-03-11 GTC（来源：research.nvidia.com 技术报告封面 2026-4-3），非本期窗口内的新发布；本期是 NVIDIA 应用深度学习 VP Bryan Catanzaro 再次广告其 NVFP4 训练策略，并首次公开 Ultra 也将以 NVFP4 预训练。这意味着本期窗口的真实新信号是 Ultra（约 500B 总参 / 50B 激活）的训练策略，而非 Super 本身。

数字核实：
Super 25T tokens NVFP4 预训练 → 已验证（来源：NVIDIA 技术报告）；Super 1M 上下文超过 GPT-OSS-120B 与 Qwen3.5-122B → 已验证（来源：NVIDIA 官方 blog）；Ultra ≈500B 总参 / 50B 激活 → 当事方口径（来源：@ctnzr 推文 + NVIDIA Nemotron 页），独立媒体尚未实测。

扩展影响：
社区把 Nemotron 3 Super 与 GPT-OSS-120B、Qwen3.5-122B 同档对比，主流意见是其优势集中在 long-context 推理吞吐与原生 4-bit 训练带来的部署成本（来源：computertech.co、toolhalla.ai）。对自建推理团队意味着：在 H100/B200 上做 1M context agentic workload 时，应把 Nemotron 3 Super 加入候选池实测。

对国内从业者的意义：
1) 由于 NVFP4 依赖 Blackwell 一代 4-bit Tensor Core，国内出口管制版（H20、H200）上是否能拿到等效收益需要独立 benchmark；
2) DeepSeek、Qwen3.5 等国内开源权重在同类参数段保持竞争，但在原生低精度训练这条工程路径上 NVIDIA 已先一步交付权重，国内团队若仅在 BF16/FP8 训练上跟随，部署侧成本差距会持续拉大；
3) Hugging Face 上的 NVFP4 权重（nvidia/NVIDIA-Nemotron-3-Super-120B-A12B-NVFP4）当前国内可下载但需 modelscope 镜像同步。

延伸阅读：
https://research.nvidia.com/labs/nemotron/Nemotron-3-Super/

#### 深挖：xAI Grok Build CLI 的记忆原语

背景补充：
Grok Build CLI 于 2026-05-14 上线（来源：x.ai/news/grok-build-cli、devops.com），定位为 agentic coding CLI，对标 Claude Code 和 OpenAI Codex。本期窗口的核心增量信号是：用户 @tetsuoai 描述了三个具名的 memory 命令——/memory（三层存储读写）、/flush（手动保存当前会话）、/dream（后台合并历史）；@elonmusk 转推视为隐性官方确认。

数字核实：
99 美元定价 → 二手报道（来源：martincid.com），xAI 官方页未直接列出该数字，存疑；/memory /flush /dream 三命令名称 → 经 web_search 未在官方文档命中，仅在用户帖中出现，当前可信度等级为"当事方/用户口径"，需以下周 Build 实测为准。

扩展影响：
社区把"editable memory + 后台合并"视为对当前 RAG-only 记忆方案的工程级反思（来源：@tetsuoai 推文 234 条收藏）。Anthropic、OpenAI 在同一周也密集发布 Codex 体验更新（Chronicle、自定义快捷键、ChatGPT 应用集成），三家在 agentic CLI 心智占位上的节奏明显加速。

对国内从业者的意义：
对国内做 AI Coding IDE / Cursor 类产品的团队，长时记忆原语是下一阶段的必答题。可参考的工程切面：把 capture（写入）、consolidation（去重合并）、inspection（用户可见可编辑）拆成独立命令，而不是塞进同一个 RAG pipeline。出海团队则需要直接对比 Grok Build / Claude Code / Codex 的命令体验差。

延伸阅读：
https://x.ai/news/grok-build-cli

---

## 2. 新产品 & 功能发布

- Codex 快捷键自定义 — OpenAI

  核心能力：
  - 全部 keyboard shortcut 可在 settings 内重映射
  - 不再强迫用户适配默认绑定
  - 与 Chronicle 等其他近期更新联动

  链接：https://x.com/OpenAIDevs/status/2055717793841221796
  立即试用优先级：今天就试
  理由：已在用 Codex 的工程师 5 分钟即可改完一组快捷键，直接降低切换成本。

- Codex Chronicle — OpenAI

  核心能力：
  - 自动记录"今天做了什么"
  - 一行 prompt 即可让 Codex 把重复工作流转为 Skills
  - 在 ChatGPT 应用内即可使用，脱离桌面端

  链接：https://x.com/gdb/status/2055769256399114677
  立即试用优先级：今天就试
  理由：是 OpenAI 在 agentic memory 上的对应动作，免费层即可体验，适合做与 Grok Build 的横向对比。

- Notion CLI（ntn） — Notion / NotionDevs

  核心能力：
  - 将整个 Notion API 接入终端
  - 支持构建并部署 Workers
  - 面向"人类 + coding agent"双用

  链接：https://ntn.dev / https://x.com/NotionDevs/status/2054594852818764178
  立即试用优先级：本周内试
  理由：curl 一键安装；如果团队已用 Notion 做知识库，则 agent 直接接入 Notion 的可行路径多了一个。

- Grok CLI + Vercel Plugin — xAI + Vercel

  核心能力：
  - Grok CLI 已支持 Plugins 与 Skills 扩展
  - 安装 Vercel 插件后可一键生成站点并部署到 Vercel
  - demo 站点 vgrok.vercel.app

  链接：https://x.com/elonmusk/status/2055530618759573769
  立即试用优先级：本周内试
  理由：从 prompt 到 production URL 的链路缩到分钟级，适合做内部 demo / landing page。

- Figure F.03 humanoid robot 24/7 自主运行直播 — Figure（@adcock_brett）

  核心能力：
  - F.03（昵称 Jim）四日连续无人干预运转
  - 累计搬运 76,940 件包裹，约 1 件/2.9 秒（来源：@adcock_brett，当事方口径，未经独立验证）
  - 直播持续到机器人故障为止

  链接：https://x.com/i/broadcasts/1AKEmOrBgokKL
  立即试用优先级：观望
  理由：是 marketing 与稳定性测试合一的演示，仍是单家公司单一场景，未对外开放试用。

- DTap（DecodingTrust-Agent Platform） — UC Berkeley / Dawn Song 团队

  核心能力：
  - 首个可控、全栈的 AI Agent 红队仿真平台，覆盖 50+ 真实环境
  - 支持环境/工具/技能/prompt 四种注入及其组合攻击
  - 配套 DTap-Bench，约 7K 任务，已在 OpenClaw 与 Claude Code 上发现零日失效模式

  链接：https://decodingtrust-agent.com / https://arxiv.org/pdf/2605.04808
  立即试用优先级：本周内试
  理由：做 agent 产品的安全团队下周就需要把这个平台加入回归测试栈。

- Aleph（EBM 形式推理模型） — Logical Intelligence（@logic_int）

  核心能力：
  - 基于 EBM（能量基模型）路径，对结构进行检查后再回答
  - 在主要 formal reasoning 榜单上领先（来源：@ylecun、@logic_int 转推，当事方口径）
  - 视频演示见 @Kseniase_ 解读

  链接：https://x.com/ylecun/status/2055664727758401700
  立即试用优先级：观望
  理由：榜单领先但缺乏第三方实测；定位偏研究侧，未公开 API。

---

## 3. 行业趋势 & 热议话题

- agentic coding CLI 进入"记忆 + 自定义快捷键 + 嵌入主入口"密集迭代期

  参与讨论的主要声音：@gdb（OpenAI）、@OpenAIDevs、@thsottiaux（OpenAI Codex）、@swyx、@steipete（OpenClaw）、@Kappaemme1926、@elonmusk 转推 @tetsuoai（xAI Grok Build）、@thom_wolf
  主流观点：Codex、Grok Build、Claude Code 三家在同一周分别推出"记忆原语 / 快捷键自定义 / ChatGPT 应用集成 / 复杂度分析 Skill / 每次 commit 跑 review"等更新；agentic coding 的竞争重心从"能不能写代码"转向"能不能像同事一样持续记住上下文并被定制"。
  主要分歧：steipete 主张"token 不再重要时怎么构建软件"——大量 background agent 并行；其他声音更关注个人开发者层的延展性而非 100 个 agent 同时跑的成本曲线。
  信号强度：强
  判断依据：6 个独立信源、3 家厂商、同周内 6 条以上具体产品动作，已超过"3 个独立来源 + 明确产品动作"的门槛。

- "超越 LLM、回到 World Model"的学术与产业回潮

  参与讨论的主要声音：@GaryMarcus、@ylecun（转推 EBM/Aleph）、@adamsafron 与 Royal Society Phil. Trans. A 专辑全体作者（含 Hofstadter、Tenenbaum、Gershman、Mitchell、Hardmaru、Levin 等）、@rohanpaul_ai 转 Fei-Fei Li
  主流观点：LLM 在语言性推理（数学、代码）上仍是最强工具，但在物理、视觉、空间、具身智能等占经济多数的领域上需要 world model；纯 scaling 不会带来 AGI。
  主要分歧：LeCun / Marcus 是显式的"need different paradigm"派；OpenAI、Anthropic 等仍在用 scaling + tool use 推动 agentic 形态。
  信号强度：中
  判断依据：3 个独立来源（学术专辑、LeCun、Marcus）+ 1 个 high-engagement 二手转述（Fei-Fei Li 通过 rohanpaul_ai），并有同周内 EBM 路线（Aleph）落地榜单。

- humanoid robot 进入"连续运行天数"作为新对比指标

  参与讨论的主要声音：@adcock_brett（Figure，多条）、@giffmana 转 @m_wulfmeier（Nomagic 在 Zürich/Warsaw 招聘 VLA/foundation models）、@berkeley_ai（RSS 2026 post-training robot foundation models workshop、Ken Goldberg ICRA 2026 agentic coding for robotics plenary）
  主流观点：行业开始用"连续运行小时数 / 包裹数"替代单点 demo 作为评估指标；同时学界把"agentic coding 用于机器人控制"作为下一节点。
  信号强度：中
  判断依据：3 个独立组织来源（Figure 公司、Nomagic、Berkeley AI），但 Figure 占大头，需要警惕单家厂商主导话语。

---

## 4. 值得关注的洞察 & 观点

- @ylecun（图灵奖得主，离开 Meta FAIR 加入 AMI Labs）：

  「LLMs are strongest in domains where language itself is the substrate of reasoning, like math and code. They can solve problems, prove theorems, and write programs — but they are not creative mathematicians, software architects, or computer scientists. Their role is to help humans build.」
  为什么值得关注：LeCun 把"LLM 擅长什么"和"LLM 不会变成什么"分开表述，是当前 hype 周期里少见的双向边界判断；与其后续转推 EBM/Aleph 的动作形成一致信号。

- @OwainEvans_UK（Truthful AI，Berkeley AI Safety）：

  「We finetuned models on documents that discuss an implausible claim and warn that the claim is false. Models ended up believing the claim! 例：Ed Sheeran 赢了奥运 100m，伊丽莎白二世写了 Python 教材。」
  为什么值得关注：揭示了一个反直觉但重要的现象——在文档中"提到再否认"会被模型当成事实学进去。对所有做 alignment、RAG、合成数据训练的团队都是直接威胁，远比"模型胡说"更难防。

- @jeremyphoward 转 @Dan_Jeffries1（fast.ai 联创转推）：

  「对中国出口管制的全部结果是把 Huawei、SMIC、国产光刻、封装、HBM 等本来萎靡的产业全部点燃……一边给中国做了 Manhattan Project for chips，一边让台湾的战略价值更高。」
  为什么值得关注：把"AI 政策类白皮书的话术"和"19 世纪东印度公司"对齐，并把芯片制裁的反向激励效果说透。视角偏激进但有具体事实链（Huawei 量产、DeepSeek v4 在国产卡上训练），适合作为路线讨论时的反方观点。

- @Thom_Wolf（Hugging Face 联创）：

  「我家 13 岁的孩子前几天说：'我们不想付钱买这个游戏，就用 Codex 重写了一个。'我 13 岁时是 HEX 编辑可执行文件把 license check 改成 NOP——times they are a-changin'.」
  为什么值得关注：用一句话说出 agentic coding 真正改变的世代行为：从"绕过别人的软件"到"重做一个自己的软件"。对教育与软件产业的成本结构都有结构性含义。

- @tobi（Shopify CEO）转 Startup Archive：

  「Goodhart's law is real. The moment a metric becomes a goal, it's no longer a useful metric…… The overlap of the most valuable things you can do with a product and the things that happen to be fully quantifiable are like maybe 20%. Which leaves 80% of a value space unaddressable by the people who only look at quantifiable things.」
  为什么值得关注：对当前所有把 AI 产品成功度量塞进单一 benchmark（HumanEval / LiveCodeBench / SWE-Bench）的团队是一种警示；不是反对评测，而是反对让评测变成目标本身。

---

## 5. 实用资源 & 教程

- Recent Developments in LLM Architectures（Gemma 4 → DeepSeek V4）

  类型：技术综述文章
  用途：可视化梳理近一年开源权重模型在长上下文效率上的工程取舍——KV sharing、per-layer embeddings、layer-wise attention budgets、compressed attention、mHC。
  链接：https://magazine.sebastianraschka.com/p/recent-developments-in-llm-architectures
  上手难度：中

- 《World models, A(G)I, and the Hard problems of life-mind continuity》专辑

  类型：学术论文集（Royal Society Philosophical Transactions A，384/2320）
  用途：18 位作者从世界模型、自我建模、能量基模型、复杂系统、人类认知到 LLM 评估的系统性论文集，是当前理解"LLM 之外的路径"最完整的入口。
  链接：https://royalsocietypublishing.org/rsta/issue/384/2320
  上手难度：高

- DecodingTrust-Agent（DTap）

  类型：开源平台 + benchmark + 论文
  用途：对 agentic 系统做注入攻击红队测试，覆盖环境/工具/技能/prompt 四种向量。
  链接：https://decodingtrust-agent.com、https://arxiv.org/pdf/2605.04808
  上手难度：中

- codex-complexity-optimizer

  类型：开源 Codex Skill
  用途：扫描代码库中的复杂度热点（O(n²)、N+1、重复 lookup、render heavy），给出 before/after 复杂度估计与改写建议，默认只读报告。安装：npx --yes codex-complexity-optimizer
  链接：https://x.com/Kappaemme1926/status/2055343704467206506
  上手难度：低

- Nemotron 3 Super 技术报告

  类型：论文 + Hugging Face 权重
  用途：完整描述 hybrid Mamba-Transformer MoE 架构与 NVFP4 原生预训练流程；NVFP4 量化权重已上 HF。
  链接：https://research.nvidia.com/labs/nemotron/Nemotron-3-Super/、https://huggingface.co/nvidia/NVIDIA-Nemotron-3-Super-120B-A12B-NVFP4
  上手难度：中

- "AI's Moral Compass and Red Lines"（Tegmark 父女联名）

  类型：评论文章（CNET）
  用途：把 Albert Bandura 的 moral disengagement 心理学框架套到 AI 研究者群体——为什么善意研究者会被诱导参与造成伤害的工作。
  链接：https://www.cnet.com/tech/services-and-software/ai-research-moral-compass-red-lines-albert-bandura/
  上手难度：低

---

## 传播力素材

- 「using codex from the ChatGPT app is such a freeing experience. makes you realize how tethered you normally are to your computer.」 — @gdb · 👍994 👁51118 · engagement_rate 0.10%

  改写方向：短视频/朋友圈金句，配 Codex 移动端使用场景图；适合中文公众号开篇钩子。
  点评：戳中"AI agent 应该跟随人而不是跟随设备"这一行为变化的关键点。局限在于："桌面端束缚"对真正 power user 并不存在——他们更需要的是大屏多窗口而不是移动端单线程。

- 「My job is to make a company worthy for the best and brightest to work for. Talent eventually takes care of itself. There are not that many good companies to work for.」 — @tobi（转 @davidsenra）· 👍778 👁92346 · engagement_rate 0.39%

  改写方向：HR/创业向公众号专栏；可改写为"招聘的本质不是筛人而是配得上人"的标题党型短文。
  点评：把招聘问题反过来定义为"公司能配得上谁"，确实是一种少见的逆视角。局限是：对早期/小公司只是漂亮话——你的"配得上"建立在已经有显著差异化产品和品牌势能之上，否则容易变成自我安慰。

- 「We finetuned models on documents that discuss an implausible claim and warn that the claim is false. Models ended up believing the claim!」 — @OwainEvans_UK · 👍1226 · engagement_rate ~0.5%（quoted 推文数据）

  改写方向：技术向公众号；适合做 "LLM 训练里被忽视的反向 RAG 风险"主题深度文。
  点评：把"否认即播种"这一现象做成 1 句话钩子非常有传播力，但只看这一句容易误以为"任何提到都会强化"——原文是 finetune 场景下的极端案例，普通 inference 没那么严重。

- 「The overlap of the most valuable things you can do with a product and the things that happen to be fully quantifiable are like maybe 20%. Which leaves 80% of a value space unaddressable by the people who only look at quantifiable things.」 — @tobi（转 Goodhart's law 短片）· 👍1631 👁367691 · engagement_rate 0.56%

  改写方向：产品向公众号或 LinkedIn；可作为反 OKR/反 KPI 流派的精炼引用。
  点评：把 Goodhart's law 翻译成 80/20 直觉非常有效；盲点是这条原则被滥用时会变成"我们不做 metrics"的合理化借口——Shopify 仍在大量投入 BI 系统，原话强调的是 metrics 不应当被设为目标，而不是不做 metrics。

- 「times they are a-changin'：我儿子 13 岁不想付钱买游戏，就用 Codex 重做了一个；我 13 岁时是 HEX 编辑 NOP 掉 license check。」 — @Thom_Wolf · 👍82 👁5195 · engagement_rate 0.13%

  改写方向：教育/技术变迁主题；适合知乎、即刻、小红书三平台同步——"AI 一代的童年"。
  点评：从"破解"到"重做"是一种代际生产力跃迁的具体写照；盲点是要小心读者代入"以后人人都能编程"——Codex 上手仍要懂提需求，并非真的 0 门槛。

---

## 一句话总结

过去 24 小时的真实 AI 信号集中在两条主线：一是 Codex / Grok Build / Claude Code 三家在同一周抢占 agentic CLI 心智份额，记忆原语和快捷键自定义成为新战场；二是 NVIDIA Nemotron 3 Ultra（≈500B）首次确认沿用 NVFP4 原生 4-bit 预训练路线，把"低精度训练"从论文推到 frontier 规模。

---

## 今日行动建议

今天（30 分钟内）：
基于 [Codex 快捷键自定义与 Chronicle 上线]——打开 ChatGPT 应用里的 Codex，跑一次 "Look through my Chronicle memories and check for workflows that I'm repeating multiple times. Turn them into skills." 这一条 prompt，亲身体验 Chronicle + Skills 的"日内自动总结"链路，对照你团队目前的脚本/Snippet 工具差距。

本周内：
基于 [NVIDIA Nemotron 3 Super NVFP4 推广再发声]——在你现有 H100/B100/B200 推理集群上跑一组对比：Nemotron 3 Super 120B-A12B-NVFP4 vs. 你当前主用的 70B+ 模型，在 1) 8k 输入/64k 输出，2) 1M context 这两个设定下做单卡吞吐与显存对比，输出一页备忘录给团队作为下一季度推理选型依据。

月内验证：
基于 [agentic CLI 记忆原语成趋势]——把"Codex / Claude Code / Grok Build"三家在记忆能力、Plugin/Skill 生态、价格上的更新跟踪到一张共享表格里，每周更新；衡量指标：3 个 CLI 的 GitHub stars 增速、Hacker News 提及次数、付费 tier 调价频率，4 周后输出一份内部对比报告决定团队默认使用哪一家。

---

## 信号 / 噪音比

进入第 1 节的有效新闻 5 条，进入第 2-5 节的有效信号 23 条，剩余约 65% 为低价值或噪音（主要是 elonmusk 35 条政治/文化推文与 SpaceX 4 条非 AI 转推）。今日整体信号密度：正常。

**本期信源**：@gdb @OpenAIDevs @GoogleDeepMind @ylecun @KempeLab @GaryMarcus @adcock_brett @ivanhzhao @NotionHQ @NotionDevs @ClementDelangue @hardmaru @rasbt @giffmana @m_wulfmeier @berkeley_ai @logic_int @adamsafron @drmichaellevin @OwainEvans_UK @EthanJPerez @mcuban @jeremyphoward @Dan_Jeffries1 @ctnzr @Thom_Wolf @fchollet @tegmark @alighodsi @ericmitchellai @thsottiaux @steipete @rauchg @Kappaemme1926 @tetsuoai @swyx @MIT_CSAIL @NandoDF（共 38 位）
