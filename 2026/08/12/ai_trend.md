# AI 行业情报简报 | 2026-08-12

> 数据窗口：2026-08-11 06:00 — 2026-08-12 06:00（北京时间，过去 24 小时）
> 深度分析：3 条 | 模板版本：v2.3

---

## 1. 重大新闻 & 突发事件

- Meta 重返开源阵营，发布 300 亿参数模型 Muse Glimmer

  来源：@AIatMeta · 约 24 小时前
  关键数字：30B 参数、Apache 2.0 许可、单张 24GB 显存消费级 GPU 可运行（来源：developer.meta.com 官方页面，已核实）
  行业影响：这是 Meta 自 Llama 4 以来首次开放权重发布，直接对标 Qwen3.6、Kimi K2.5 等中国开源模型，对所有依赖开源基座做本地 Agent 开发的团队都构成新的选型基准。

- NVIDIA 联合华尔街六大机构设立超 5000 亿美元 AI 基建融资平台

  来源：@GaryMarcus（转发 @HedgieMarkets 分析）· 约 6 小时前；原始事件发布于 2026-08-10（NVIDIA 官方新闻稿），本期为窗口期内的转发点评
  关键数字：超 5000 亿美元第三方资本撬动目标（来源：nvidianews.nvidia.com 官方新闻稿，已核实；注意这是"计划撬动规模"而非六家机构已承诺的现金）
  行业影响：将 GPU 采购的融资风险转移到 Apollo、BlackRock、Blackstone、Brookfield、Goldman Sachs、KKR 等外部资本方的资产负债表上，直接影响所有依赖大厂算力采购节奏的下游创业公司与云服务商。

- xAI 上线 Grok Bot 公测，押注"AI 数字同事"赛道

  来源：@bot · 约 5 小时前
  关键数字：接入 SuperGrok Heavy、Cursor Ultra、Cursor Teams Premium 三档现有订阅（来源：x.ai/news 官方公告，已核实），具体新增费用未标注 [未经验证]
  行业影响：与 Anthropic 的 Claude Cowork 直接竞争，标志着头部实验室开始把"能独立完成多步任务的常驻 Agent"当作下一个消费级战场，而不只是聊天界面的迭代。

- Gemini App 月活突破 10 亿

  来源：@sundarpichai · 约 5 小时前
  关键数字：月活跃用户超 10 亿，为 Google 第 14 款突破 10 亿用户的产品（来源：@sundarpichai，当事方口径，未经独立验证）
  行业影响：确认 Gemini App 是 Google 增长最快的消费产品，为其在与 ChatGPT 的用户规模竞争中提供了官方口径的最新锚点。

- Databricks 收购 ElectricSQL（PGlite 团队）

  来源：@alighodsi · 约 6 小时前
  关键数字：交易金额未披露 [未经验证]
  行业影响：目标是把 WASM 版 Postgres 能力整合进 Lakebase，直接服务"AI Agent 需要本地高速可同步数据库"这一新兴基础设施需求，是本期"Agent 基建"趋势的组成部分之一。

---

#### 深挖：Meta 重返开源阵营，发布 Muse Glimmer

背景补充：
Muse Glimmer 由 Meta Superintelligence Labs 发布，是从内部闭源系统 Muse Spark 蒸馏而来的 300 亿参数模型，采用 Apache 2.0 许可（该团队自 Llama 4 以来的首次开放权重发布）。可在单张 24GB 显存消费级 GPU 上以 4bit 量化运行，上下文窗口 131,072 tokens 起，知识截止日期为 2026 年 1 月 4 日。Zuckerberg 借发布同时呼吁美国放宽对开源 AI 的政策限制以应对中国厂商竞争，并预告未来数周将开源旗舰模型 Muse Spark 1.2 的权重。（来源：Meta 官方 developer.meta.com、CNBC、TechCrunch）

数字核实：
"30B 参数、Apache 2.0、单 GPU 可跑" → 已验证（来源：developer.meta.com 官方页面，CNBC/TechCrunch/MarkTechPost 报道一致）。第三方基准 Artificial Analysis Intelligence Index 给出 35 分（高于 Llama4 Maverick 的 14 分，略低于 Qwen3.6 27B 的 38 分）与推文中转引的数字一致；但 Meta 自称"24 项基准中 19 项超过 Gemma4-31B、14 项超过 Qwen3.6-27B"这一说法，与独立评测存在出入——该对比表由 Meta 自行运行，对手模型未经调优，第三方复现显示 Qwen3.6-27B 在终端操作、多模态等实测项目上反超（来源：Data Science in Your Pocket/Medium 独立评测、kingy.ai、orcarouter.ai）。

扩展影响：
开发者社群反应呈"审慎乐观"：有开发者反馈其单次完成三个 JS 任务、零失败，优于同量级 Qwen3.6-27B-Q4；但也有独立评测显示 Qwen3.6-27B 在终端操作与多模态任务上仍占优，Gemma4-31B 安全性记录更好——这是一次三方混战，而非单边胜出。（来源：kingy.ai、orcarouter.ai）

对国内从业者的意义：
Muse Glimmer 的直接竞品就是 Qwen3.6、Kimi K2.5 等国产开源模型——目前中国团队在 Hugging Face 开源模型下载量中占比已达 41%（Kimi K3、Qwen3.8-Max、DeepSeek V4-Flash 均为一线竞品）。Zuckerberg 公开将此次发布与"防止中国夺取开源 AI 领先地位"的政策游说绑定，意味着国内厂商的开源优势正被美国大厂正面视为竞争对手；对国内开发者而言，Apache 2.0、可单卡部署的 Muse Glimmer 本身也是可直接拿来做基线对比的新选项。

延伸阅读：
https://techcrunch.com/2026/08/10/metas-new-glimmer-ai-model-offers-a-hint-at-zuckerbergs-personal-intelligence-vision/

---

#### 深挖：NVIDIA 联合华尔街六大机构设立超 5000 亿美元 AI 基建融资平台

背景补充：
NVIDIA 于 2026 年 8 月 10 日官方宣布，与 Apollo、BlackRock、Blackstone、Brookfield、Goldman Sachs、KKR 六家机构建立独立的"AI 计算基础设施融资平台"，目标是在一段时间内撬动超 5000 亿美元第三方资本，用于数据中心、电力等 AI 基础设施建设。这是以谅解备忘录（MOU）形式达成的安排，具体条款尚未最终确定，设计目的是让外部投资者出资建设基础设施，不直接计入 NVIDIA 自身资产负债表。黄仁勋透露此次只接触了这六家机构，且无一拒绝。（来源：nvidianews.nvidia.com 官方新闻稿）

数字核实：
"超 5000 亿美元" → 已验证（来源：NVIDIA 官方新闻稿），但需明确这是"计划撬动的第三方资本规模上限"，不是六家机构已承诺的现金或已到账资金，与部分社交媒体上"六大机构承诺 5000 亿美元"的简化表述有出入。

扩展影响：
市场反应偏负面：消息公布后 NVIDIA 股价盘中一度跌超 3.2%，5 年期信用违约互换（CDS）价格单日上涨约 5.3 个基点，为两周以来最大单日涨幅，反映市场对其信用风险敞口的关注上升。核心争议是"循环融资"（circular financing）：NVIDIA 出资帮助客户购买自家芯片，被批评为变相自我造血式营收。做空机构代表人物 Jim Chanos 将其类比 2008 年金融危机前的金融工程操作；Gary Marcus 在转发中援引 1990 年代末 Lucent、Nortel 向客户放贷买设备、最终导致两家公司史上最大规模破产的先例作为警示。NVIDIA CEO 黄仁勋公开回应称需求来自前沿实验室、AI 原生创业公司、企业客户、云服务商与主权国家，并非单纯左手倒右手。（来源：Fortune、CNBC、ZeroHedge、Investing.com）

对国内从业者的意义：
该融资结构的最大风险变量被外部分析明确指向中国——NVIDIA 在中国 AI GPU 市场份额已因出口管制从约 95% 降至 0（A800/H800/H20 等中国特供芯片相继受限），而中国正加速自建算力产能，一旦中国厂商以低价芯片打价格战，用作抵押品的 GPU 资产贬值速度可能快于 5000 亿美元债务的偿还周期，这一风险会传导至所有参与该融资链条的机构投资者与云厂商。对国内从业者而言，这既印证了海外算力成本与供给的不确定性正在系统性上升，也意味着国产算力自主可控路线在这场博弈中获得了新的筹码。（来源：CNBC《Why Jensen Huang's $500 billion AI financing plan faces a big risk from China》）

延伸阅读：
https://nvidianews.nvidia.com/news/nvidia-partners-with-apollo-blackrock-blackstone-brookfield-goldman-sachs-and-kkr-to-establish-ai-compute-infrastructure-financing-platforms-to-mobilize-over-500-billion-of-third-party-capital

---

#### 深挖：xAI 上线 Grok Bot 公测

背景补充：
Grok Bot 是一组"常驻"AI Agent，每个 Bot 拥有独立云端计算环境，可登录用户现有工具、执行多步任务并在无人监督下完成工作；支持通过演示学习工作流程并保存为可复用例程，多个 Bot 之间可共享上下文协作完成同一项目。目前接入方式为绑定 SuperGrok Heavy、Cursor Ultra、Cursor Teams Premium 三档已有订阅，桌面端（含 Linux 构建）与 iOS 端同步开放。（来源：x.ai/news 官方公告、Unite.AI、9to5Mac）

数字核实：
推文中"接入 SuperGrok Heavy / Cursor Ultra / Cursor Teams Premium 三档订阅"→ 已验证（来源：x.ai/news 官方公告）；是否需要额外付费或有独立定价，公开信息中未明确标注 [未经验证]。

扩展影响：
多家科技媒体将 Grok Bot 定位为对标 Anthropic Claude Cowork 的正面竞品；早期体验者 Matt Shumer（AI 投资人）给出的评价是"细节做得好、路由模型选择环节体验一般"，Cursor 创始人 Michael Truell 公开背书为"迈向数字同事的第一步"。Elon Musk 同时确认将在本周内发布 Grok 4.6 并扩大公测范围。（来源：trendingtopics.eu、@mattshumer_、@mntruell、@elonmusk）

对国内从业者的意义：
Grok Bot 依附于 X（Twitter）生态，在中国大陆访问需通过 VPN 等代理方式，不属于可直接落地的产品形态；但其"绑定现有订阅、多 Bot 协作、工作流可复用"的产品设计思路，对国内正在做 Agent 编排/协作产品的团队有直接的功能对标价值。

延伸阅读：
https://x.ai/news/introducing-grok-bot

---

## 2. 新产品 & 功能发布

- NVIDIA Nemotron 3.5 Lightning + NeMo Switchyard — NVIDIA

  核心能力：
  - 300 亿参数 MoE 模型，仅 3B 激活参数，面向高频、专业化 Agent 任务
  - 官方称输出速度可达同规模模型的 4 倍（来源：@nvidia，当事方口径，未经独立验证）
  - NeMo Switchyard 可在多个模型间按工作流步骤自动路由

  链接：链接未提供（官方文章见推文内嵌 X Article）
  立即试用优先级：本周内试
  理由：开源权重可在 Hugging Face 直接获取，@AravSrinivas 已确认可在 Perplexity 与 DGX Spark 等本地硬件上运行更大版本 Nemotron Ultra。

- webAI TwiL-LM3 — webAI Intelligence Lab

  核心能力：
  - 30 亿参数的形式化推理模型，专用训练数据管线而非爬取的互联网数据
  - 官方称在 5 项形式化推理基准中的 4 项超过 OpenAI GPT-OSS-120B（来源：@huggingface 转发 webAI 官方口径，未经独立验证）
  - 面向边缘设备，可在 Raspberry Pi、iPhone 上运行

  链接：https://www.webai.com/blog/webai-releases-twil-lm-a-family-of-formal-logic-models-that-outreason-a-120b-model-and-run-on-an-iphone
  立即试用优先级：本周内试
  理由：模型已在 Hugging Face 开源，适合需要可靠工具调用/结构化输出但缺乏云端算力预算的团队直接下载测试。

- LTX-2.5 — LTX.io（Lightricks）

  核心能力：
  - 视频世界模型升级，支持多镜头场景的跨镜连贯性
  - 新增 Diffusion Fidelity Rendering，逐帧画质在影院大屏下仍保持稳定
  - 定位为可微调的基础模型，而非按次付费的封闭工具

  链接：链接未提供
  立即试用优先级：观望
  理由：面向影视/机器人/实时工作流的专业场景，个人开发者短期试用价值有限，需要评估微调成本后再决定。

- FLUX 3 Video 限时免费开放 — Black Forest Labs

  核心能力：
  - 官方 Playground 免费试用至 8 月 16 日 23:59（太平洋时间）
  - 号称视频生成模型全球排名第 2（来源：@giffmana 转发 @bfl_ai，当事方口径，未经独立验证）
  - 后续将支持 4K、视频编辑及多图/多视频参考输入

  链接：链接未提供
  立即试用优先级：今天就试
  理由：限时免费窗口明确（8 月 16 日截止），有直接试用成本为零的时间压力。

- MAI-Image-2.6 — Microsoft

  核心能力：
  - 官方称已成为 Arena 榜单文生图第 2 名，超过 Nano Banana、Meta、Grok 相关模型（来源：@satyanadella 转发 @mustafasuleyman，当事方口径，未经独立验证）

  链接：链接未提供
  立即试用优先级：本周内试
  理由：可在 Arena 直接对比测试，适合正在评估文生图供应商的团队快速验证排名说法是否符合自身场景。

- Notion 模型选择器改版 — Notion

  核心能力：
  - 新增"收藏常用模型"功能
  - 新增思考强度（effort）调节滑块，按任务复杂度控制推理开销

  链接：链接未提供
  立即试用优先级：今天就试
  理由：现有 Notion 用户可直接在设置中启用，无额外成本，直接影响日常调用的推理成本控制。

---

## 3. 行业趋势 & 热议话题

- 美国大厂重新拥抱开源模型，并与"对抗中国"的政策叙事绑定

  参与讨论的主要声音：@AIatMeta、@nvidia、@huggingface（转引 webAI 与白宫 AI 政策顾问 @mkratsios47）、@ylecun、@ClementDelangue
  主流观点：Meta（Muse Glimmer）、NVIDIA（Nemotron 3.5 Lightning）、webAI（TwiL-LM3）在同一窗口期内接连开源权重模型，HuggingFace CEO 与白宫 AI 政策顾问 Michael Kratsios 均将其与"POTUS's AI Action Plan"的政策导向直接挂钩。
  主要分歧：Yann LeCun 认为这本质是 Meta 的"话语权重构"策略（把竞争维度从"谁的模型最强"改写为"谁的分发最广"），而非单纯的技术开放姿态。
  信号强度：强
  判断依据：三家独立机构（Meta、NVIDIA、webAI）在 24 小时内密集开源模型权重，且均有官方或政策层面表态佐证，满足多源共振门槛。

- "AI 数字同事"型 Agent 产品成为新的产品战场

  参与讨论的主要声音：@bot（xAI）、@nvidia（NeMo Switchyard）、@alighodsi（Databricks/ElectricSQL）、@NotionHQ、@adcock_brett（Figure/Hark Handoff）
  主流观点：从 xAI 的 Grok Bot、NVIDIA 的跨模型工作流路由，到 Databricks 收购 ElectricSQL 补齐"Agent 需要的高速本地数据库"、Notion 把 Agent 对话嵌入任意页面、Figure CEO 公开使用 AI 招聘助理处理月度周期的招聘任务——多家公司在同一窗口期内不约而同地把"能独立跑完整工作流的常驻 Agent"作为产品重点。
  信号强度：中
  判断依据：5 家独立公司（xAI、NVIDIA、Databricks、Notion、Figure）分别从模型层、基础设施层、应用层同时推进 Agent 产品化，满足多源共振门槛，但尚未形成统一的技术标准或竞争焦点，处于探索期。

---

## 4. 值得关注的洞察 & 观点

- @ylecun（AMI Labs 创始人，前 Meta 首席 AI 科学家）：

  「Meta 把 AI 竞赛的评判标准从"谁的模型能力最强"改写为"谁的分发最广"；把竞争对手从"掌握技术领先优势"改写为"掌握过多集中权力"；把安全议题从"更安全 vs 更不安全"改写为"乐观派 vs 末日论者"；把 Meta 自身从"东一榔头西一棒槌"改写为"为所有人服务的未来"。」
  为什么值得关注：作为 Meta 前首席 AI 科学家，LeCun 提供了一个跳出"跑分竞赛"框架看待 Muse Glimmer 发布的视角——揭示大厂开源姿态背后是一套完整的叙事重构策略，而不只是技术决策。

- @pwang（Anaconda 联合创始人兼首席 AI 官）：

  「有传闻称中国实验室在 2026 年初找到了从 Claude Code 和 Codex 中逆向提取推理轨迹的方法，并借此收集了大量带推理过程的长程数据，这可能是过去几个月一批开源模型质量跃升的原因之一……如果这个说法成立，"如何近似前沿模型的推理轨迹"可能会成为开放权重模型阵营生死攸关的问题。」
  为什么值得关注：作者本人明确标注这是"推测"，但结合其自身在推理链重建方向的研究（论文显示即使没有推理轨迹，仅凭输入输出也能较容易重建可用的推理过程），这一判断为"隐藏推理链能否真正保护模型能力"这一未有定论的问题提供了一个具体、可检验的技术论点，而非单纯站队。

- @giffmana（Meta 研究员，前 OpenAI/DeepMind/Google Brain）：

  「文本水印是对 LLM 采样算法的一种修改：在多种表达方式都成立时，倾向选择与伪随机密钥一致的那一种。这是隐藏在任意 LLM 文本用词习惯中的本地不可见签名，文本被复制后依然保留。」
  为什么值得关注：作为 Meta 研究员，giffmana 用十点 FAQ 逐一拆解了关于 LLM 文本水印的常见误解（是否影响推理质量、是否可被复制、是否能反过来被用于识别 AI Agent 集群等），在水印技术被简化为"阴谋论"式传播的背景下提供了一份技术含量较高的辟谣材料。

- @giffmana（Meta 研究员，前 DeepMind/Google Brain）：

  「谷歌员工认为"去年夏天"才是 Gemini 错过编程赛道的起点，这个说法本身就说明问题——实验室内部对编程 Agent 的训练布局比这更早就已经落后，更别提 Cursor 早已抢跑。」（评论对象：Fortune《Behind the exit of DeepMind's CEO》，原文报道的 Hassabis 卸任 Google DeepMind CEO 事件发生于 2026-08-05 至 08-10 期间，今日经 @giffmana 引用讨论，非本期新发生新闻）
  为什么值得关注：作为 DeepMind/Google Brain 前员工，giffmana 的判断指向一个比"高管换人"更深的结构性问题——谷歌在编程 Agent 赛道的落后早于外界报道的时间线，积累周期比高管变动本身更值得追踪。

- @GaryMarcus（AI 评论家，长期批评生成式 AI 炒作）：

  「The only solution to this drama would start with a change at the top. @sama, for the benefit of humanity, and the benefit of the mission, maybe it's time to let someone else take the reins.」
  为什么值得关注：该言论回应的是"OpenAI 伦理负责人、安全系统负责人与使命对齐负责人近期相继离职"的说法——但这一说法目前仅来自单一非机构信源（@ns123abc），未经 OpenAI 官方或权威媒体证实，本简报不对其真实性做背书；Gary Marcus 借此重申其一贯的"Altman 应让位"立场，这一立场本身独立于传闻是否属实，但读者需明确区分二者。

---

## 5. 实用资源 & 教程

- How to Steal Reasoning Without Reasoning Traces（论文）

  类型：论文
  用途：提出"推理反演模型"，证明即使前沿模型隐藏完整推理链，仅凭输入、输出和简要推理摘要也能重建出可用的合成推理轨迹，直接关联开放权重模型能否被蒸馏的争论。
  链接：http://arxiv.org/abs/2603.07267
  上手难度：高

- Regulating Data Brokers in the Age of AI: A California Case Study（政策简报）

  类型：论文
  用途：分析加州数据经纪商监管现状及其对 AI 训练数据合规的影响，适合做数据合规/隐私风险评估的产品与法务团队参考。
  链接：https://hai.stanford.edu/policy/regulating-data-brokers-in-the-age-of-ai-a-california-case-study
  上手难度：中

- 数据约束下的预训练效率研究（论文）

  类型：论文
  用途：提出"重复数据等效新鲜 token 数"的度量方式，把重复数据与新鲜数据放在同一尺度上比较，用于指导预训练数据配比决策。
  链接：链接未提供
  上手难度：高

- GeoPT 物理基础模型（研究工具）

  类型：论文
  用途：教模型理解水、风等真实物理机制的基础规律，用于提升物体动力学模拟的效率与准确性，是构建物理基础模型的早期尝试。
  链接：https://bit.ly/4bKjFii
  上手难度：高

- Amazon 自动推理十年回顾（技术博客）

  类型：其他
  用途：回顾 Amazon Automated Reasoning Group 用形式化验证方法证明 AWS Nitro 隔离引擎、加密代码、S3 正确性的十年历程，及其如何被应用到 AI 系统验证。
  链接：https://www.amazon.science/blog/a-decade-of-mathematical-certainty-reflections-on-the-automated-reasoning-group
  上手难度：中

- 离散扩散语言模型现状综述（技术博客）

  类型：教程
  用途：梳理当前离散扩散语言模型的技术现状及权衡取舍，为理解"扩散模型是否会成为下一代推理并行化路径"提供背景知识。
  链接：链接未提供
  上手难度：中

---

## 一句话总结

今天最大的变化不是某个模型跑分领先，而是三条独立新闻同时指向同一个方向：AI 行业的重心正从"模型能力竞赛"转向"谁能把算力、资本和人才留住"——Meta 重返开源阵营正面对抗中国模型份额，NVIDIA 把 5000 亿美元级别的 GPU 采购风险转移给华尔街六大机构以维持增长叙事，而 Google DeepMind 在 Gemini 路线图连续延期后完成了一次罕见的创始人卸任式换帅。

## 今日行动建议

今天（30 分钟内）：
基于「Meta 重返开源阵营，发布 Muse Glimmer」——在 Hugging Face 下载 Muse Glimmer 30B 的 4bit 量化版本（约 18GB），用一个工具调用类的真实任务，与团队已在用的 Qwen3.6-27B 跑一次并排对比。

本周内：
基于「NVIDIA 联合华尔街六大机构设立超 5000 亿美元 AI 基建融资平台」——写一页备忘录，梳理团队当前的 GPU 采购或云算力合同是否涉及类似的表外融资结构供应商，标注潜在的算力价格/供给波动风险敞口。

月内验证：
基于「xAI 上线 Grok Bot 公测」——持续跟踪 Grok Bot 从 SuperGrok/Cursor 订阅捆绑走向独立定价的进度，以及 Anthropic Claude Cowork 是否针对性调整功能或价格，作为判断"常驻 Agent"产品是否跑通商业模式的观察指标。

---

## 传播力素材

- 「The first few paragraphs are human written and the remaining wall of text is slop. I noticed as i kept losing focus...」— @giffmana · 👍312 👁51270 · engagement_rate 0.08%
  改写方向：适合改写成中文短评，吐槽"企业高管用 AI 代笔长文"现象，配合具体案例（本条评论对象是 Jensen Huang 的一篇长文）发在小红书/即刻等平台。
  点评：这条评论精准命中了一个普遍体验——AI 生成内容存在"开头认真、后面注水"的可辨识模式。局限在于它是主观阅读感受，没有给出可复现的检测方法，读者容易把"我觉得像 AI 写的"当成确凿判断，实际上人类长文注水现象同样存在。

- 「"we have sandboxed the agent" —— the agent: [视频]」— @saneord（经 @elonmusk 转发）· 👍10850 👁2762528 · engagement_rate 0.04%
  改写方向：适合做成图文/短视频类科普素材，用来解释"Agent 沙箱隔离"为什么在实践中经常不如宣传的可靠，配合具体的沙箱逃逸案例效果更好。
  点评：这条梗精准戳中了 AI 安全圈内部的一个真实痛点——"已沙箱化"经常只是营销话术,而非可验证的安全保证。局限是原视频具体展示的是什么失败场景，本简报未能获取，脱离视频语境单独转发容易被过度解读为"所有 Agent 沙箱都不可靠"。

---

## 信号 / 噪音比

进入第 1 节的有效新闻 5 条，进入第 2-5 节的有效信号 19 条，剩余约 48% 为低价值或噪音（主要为 @elonmusk 账号的非 AI 政治/个人生活内容、无独立评论的重复转推，以及缺乏信息增量的情绪化表达）。今日整体信号密度：高（Meta 开源模型、NVIDIA 巨额融资平台、xAI 新品发布同日集中出现，较为少见）。

**本期信源**：@AIatMeta @giffmana @ylecun @rasbt @ClementDelangue @nvidia @AravSrinivas @huggingface @bot @mntruell @mattshumer_ @elonmusk @sundarpichai @demishassabis @alighodsi @pwang @GaryMarcus @NotionHQ @satyanadella @StanfordHAI @StanfordAILab @MIT_CSAIL @AmazonScience @NandoDF @saneord（共 24 位）
