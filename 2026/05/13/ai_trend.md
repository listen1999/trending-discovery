# AI 行业情报简报 | 2026-05-13

> 数据窗口：2026-05-12 07:11 — 2026-05-13 07:11（北京时间，过去 `24 小时`）
> 深度分析：3 条 | 模板版本：v2.3

---

## 1. 重大新闻 & 突发事件

- **Isomorphic Labs 完成 21 亿美元 Series B，扩张 IsoDDE 药物设计引擎**

  来源：@kchonyc 转推 @maxjaderberg · 约 9 小时前
  关键数字：21 亿美元（来源：isomorphiclabs.com / Reuters / PRNewswire）；本轮由 Thrive Capital 领投，Alphabet、GV、MGX、Temasek、CapitalG、UK Sovereign AI Fund 跟投（来源：isomorphiclabs.com）
  行业影响：AI 药物发现首次出现"单轮 20 亿美元+"级别，资金集中度进一步向 Alphabet 系倾斜；主权 AI 资本（UK Sovereign AI Fund）首次出现在 biotech 投资名单上，意味着 AI×制药已从风险投资题材升级为国家战略。

- **xAI 同日上线 Grok Skills + Grok Voice Think Fast 1.0 取得 τ-Voice 第一**

  来源：@elonmusk · 约 2 小时前；@ArtificialAnlys（基准方）· 约 6 小时前
  关键数字：Grok Voice Think Fast 1.0 在 τ-Voice 上 52.1%、平均 5.6 分钟/对话；GPT-Realtime-2 (High) 39.8%、3.0 分钟；GPT-Realtime-1.5 38.8%、4.8 分钟；Gemini 3.1 Flash Live Preview - High 37.7%、3.8 分钟（来源：@ArtificialAnlys，第三方基准）
  行业影响：Skills 把 Grok 从单次对话推到"可重用工作流 + Connectors（Gmail/GitHub/Notion）"层，直接对标 Claude Skills；Voice 在客服 agent 基准上甩开 OpenAI 最新模型 12+ 个百分点，且 xAI 称该模型已承接 Starlink 电话客服。语音 agent 真正具备替代人工坐席的能力分水岭被改写。

- **Sundar Pichai 在 The Android Show (I/O Edition) 发布 Gemini Intelligence**

  来源：@sundarpichai · 约 5 小时前
  关键数字：本季度先在最新 Pixel 和 Samsung Galaxy 推送，年内扩展到 watch、car、glasses、laptop（来源：blog.google）
  行业影响：Gemini 由独立应用升级为 Android 的"系统智能层"，提供跨 app 多步任务执行、表单自动填写、Rambler 语音转书面文本、自定义 widget 生成等能力；同时 Google 官宣 Googlebook 笔记本系列（秋季上市），把 Gemini Intelligence 作为出厂底座，正面挑战 Apple Intelligence 的硬件—OS—模型一体路径。

- **Thinking Machines 公开发布 Interaction Models（TML-Interaction-Small）**

  来源：@miramurati 转推 @thinkymachines · 约 23 小时前；@soumithchintala 转推 @ScaleAILabs · 约 7 小时前
  关键数字：TML-Interaction-Small 在 Scale AI 的 Audio MC S2S 排行榜上 43.4% APR，与既有全双工模型并列第一（来源：@ScaleAILabs，第三方基准）；技术博客 thinkingmachines.ai/blog/interaction-models
  行业影响：这是 Mira Murati 团队成立以来第一个公开发布并跑通第三方榜单的模型，定位是"边听边想边说"的实时全双工 agent，能识别说话人停顿、自我修正、邀请回应——把语音 agent 从轮流式（turn-taking）推进到自然对话式，叠加 OpenAI GPT-Realtime-2、Sakana KAME，构成本周实时语音的多源共振信号。

- **Open Defense Initiative 推出，向开源项目派发 500 万美元自动漏洞挖掘信用**

  来源：@JeffDean 转推 @andreamichi · 约 3 小时前
  关键数字：500 万美元 depthfirstlabs 信用（来源：@andreamichi，当事方口径，未经独立验证）；在 FFmpeg 上自动发现 12 个漏洞，所耗算力为 Anthropic Mythos 同任务的 1/10（当事方口径）
  行业影响：开源关键基础设施的漏洞挖掘正快速从"少数安全研究员手工 + LLM 辅助"切到"专用 harness + 后训练安全模型"。Jeff Dean 公开背书并以前 GoogleDeepMind 研究员身份点名 Anthropic Mythos 的算力低效，意味着主流 AI 实验室已把 agent 安全工具链当作可定价的产品赛道。

- **Notion Q1 收入连续第 7 个季度加速，AI 业务已占 60%**

  来源：@ivanhzhao · 约 4 小时前
  关键数字：AI 占公司业务 60%（来源：@ivanhzhao，当事方口径，未经独立验证）；公司现金流为正
  行业影响：SaaS 厂商从"AI 是附加功能"过渡到"AI 是主营收入"的最清晰样本之一。Notion CEO 同时强调正在被 Claude desktop 的项目协作能力倒逼出 agent 共享平台，给出"工作空间型 SaaS 是否能挡住 LLM 厂商工作流入侵"的早期答卷。

---

## TOP 新闻深挖

#### 深挖：Isomorphic Labs 21 亿美元 Series B

背景补充：
本轮由 Thrive Capital 领投，Alphabet、GV、MGX、Temasek、CapitalG、UK Sovereign AI Fund 跟投。Isomorphic Labs 由 Demis Hassabis 创立于 2021 年，CEO 为 Hassabis、总裁为 Max Jaderberg（前 DeepMind）。资金用于扩张 IsoDDE 药物设计引擎并推进自有管线进入临床。

数字核实：
21 亿美元 → 已验证（来源：isomorphiclabs.com、Reuters/Yahoo Finance、PRNewswire）。Hassabis 此前公开目标是 2025 年底前让 AI 设计的药物进入临床，最新口径推迟到 2026 年底进入首批临床（来源：搜索结果，与原推文未冲突但补充时间线松动）。

扩展影响：
本轮估值与具体管线细节未披露，但跟投方阵容（含一只主权 AI 基金）显示 AI biotech 正在从风险资本议题转为国家战略议题。对比同业，Recursion、Insilico 此前最大单轮均显著小于该体量，资金落差将影响中型 AI biotech 的并购窗口。

对国内从业者的意义：
晶泰科技、英矽智能等国内 AI 制药公司在数据壁垒和合作管线规模上将面对更明显的资本差距，差异化需要更聚焦在中国特异的疾病谱、临床数据资源和成本结构上。同时 UK Sovereign AI Fund 出手意味着出海融资可能需要面对更多主权资本审查路径，跨境数据合规是首要关注点。

延伸阅读：
https://www.isomorphiclabs.com/articles/isomorphic-labs-announces-series-b-investment-round

---

#### 深挖：xAI Grok Skills + Grok Voice 双发

背景补充：
Skills 让用户在 grok.com 内创建可复用的自定义指令集，运行在 Grok 沙盒中，可调用 Connectors（Gmail、GitHub、Notion 等），可直接导入 skills.md 跨工具迁移。Voice 部分采用 Artificial Analysis 与 ScaleLM 团队联合提出的 τ-Voice 基准，覆盖航空、零售、电信三个客服域共 278 个真实场景。

数字核实：
Grok Voice 52.1% → 已验证（来源：@ArtificialAnlys 基准方推文）。Skills 状态存在矛盾：CryptoBriefing 等于 3 月 27 日基于 Nima Owji 泄露截图报道为"未发布的功能 flag"；本周 myrhex、Tech Dev Notes 与 Elon Musk 已展示在 grok.com Web 端通过 `/` 触发使用，但 x.ai 官方博客在 5 月 13 日之前未见正式公告。结论：处于灰度 rollout 阶段，未见正式发布稿，保留双方说法。

扩展影响：
Artificial Analysis 同时指出，即使最强 S2S 模型也只能端到端解决约一半真实客服场景，文本 agent 与语音 agent 仍存在能力差距。但 Grok Voice 与第二名 12+ 百分点的差距，加上据 xAI 表述已在 Starlink 电话客服走真实流量，意味着 BPO/呼叫中心采购侧首次有明确"非 OpenAI 选项"可对比。Skills 则把 Claude Skills 的优势在两个月内被拉平，customizable workspace 已是 chatbot 主战场标配。

对国内从业者的意义：
- 模型：S2S 实时语音 agent 头部模型差距收窄，国内豆包语音、智谱清言语音、阿里通义有必要尽快接入 τ²-bench/τ-Voice 类基准，缺少独立基准的国内宣称难以获得海外客户信任。
- 产品：Skills 类自定义工作流 + Connectors 入口已成 chatbot 标准能力，国内 chatbot 厂商若仍只做"角色扮演 Prompt 商店"将快速落后。
- 商业：Starlink 客服自动化反向证明"自家高频业务作为模型训练真实流量"的循环，对国内厂商意味着自营业务（客服、电商售前、保险定损等）是数据飞轮的最优入口。

延伸阅读：
https://artificialanalysis.ai/

---

#### 深挖：Gemini Intelligence 进入 Android 系统层

背景补充：
The Android Show (I/O Edition) 上 Sundar Pichai 把 Gemini 从"应用层"重定位为"系统智能层"，首批能力包括跨 app 多步任务执行、Rambler 口语转书面、Magic Pointer（在 Googlebook 上"框选即问 Gemini"）、AI 生成自定义 widget、表单自动填写。Googlebook 笔记本系列将于秋季上市，作为 Gemini Intelligence 的旗舰硬件载体。

数字核实：
原推文未给出具体数字（用户量、覆盖设备数），无需核实。来源已充分，背景核实跳过。

扩展影响：
Android 阵营首次把 OEM ROM 的 AI 能力上收到 OS，Pixel 与 Samsung Galaxy 先行的策略意味着其他 OEM（包括出海的小米、OPPO、vivo、传音）在第一波 Gemini Intelligence 中处于"等待 Google 排期"的状态。同时 Googlebook 进入"AI PC"窄道，与 Apple 自研芯片 + Apple Intelligence 路径正面对位。

对国内从业者的意义：
- 出海手机厂商：当前自研 ROM AI（HyperOS、ColorOS 等）的差异化窗口在缩短，需要在海外发行版决定是否让出 Gemini Intelligence 入口位，或维持双轨。
- 国内 Android 生态：受限于 GMS 不可用，国内厂商需要加速本土 OS 层 AI（如 HyperAI、ColorOS AI、华为小艺）的"系统层 agent"叙事和实测能力对比，否则海外口碑回流可能导致国内品牌定位被动。
- 应用厂商：表单自动填写、跨 app 任务、widget 生成都可能蚕食国内独立 AI 助手 app 流量，需要尽早布局"系统 agent 时代下的 super app/工具型 app"角色定位。

延伸阅读：
https://blog.google/products-and-platforms/platforms/android/gemini-intelligence/

---

## 2. 新产品 & 功能发布

- **Grok Skills** — xAI

  核心能力：
  - 可复用、可导入 `.skills.md`、跨对话调用
  - 沙盒内可编辑文件、调用 Gmail/GitHub/Notion 等 Connectors
  - 通过 `/` 在 Web 端触发

  链接：https://grok.com
  立即试用优先级：今天就试
  理由：Claude Skills 用户可直接导入存量 skills.md，无新学习成本；Pro 订阅用户当下就能验证 Connector 链路是否替代得了 Claude Projects。

- **KAME（Sakana AI）** — Sakana AI / @hardmaru

  核心能力：
  - Tandem 架构：前端 S2S 模型即时回应，后端 LLM 异步注入"oracle"信号
  - 后端 LLM 可热插拔（GPT-4.1 / Claude Opus / Gemini 2.5 Flash）
  - ICASSP 2026 接收，模型权重已开源

  链接：https://huggingface.co/SakanaAI/kame
  立即试用优先级：本周内试
  理由：把"思考再说"切到"边说边思考"的真实代码可跑，权重已在 Hugging Face 上；语音产品团队可在一天内做基准对比。

- **TML-Interaction-Small** — Thinking Machines

  核心能力：
  - 全双工：实时识别说话人犹豫、自我修正、回合切换
  - Scale AI Audio MC S2S 排行榜并列第一（43.4% APR）
  - 配套博客发布 demo 视频

  链接：https://thinkingmachines.ai/blog/interaction-models
  立即试用优先级：本周内试
  理由：Mira Murati 团队首个公开模型并通过第三方基准验证，可作为评估其他 S2S 模型的"上限对照组"。

- **Marionette + Reachy Mini 整套** — Hugging Face / Pollen Robotics

  核心能力：
  - 浏览器端用手势握住机器人录制动作
  - 同源 emotions 数据集格式，社区可共享动作
  - 6 月 1 日因 RAM + 关税涨价（早鸟价至 5 月 31 日）

  链接：https://hf.co/reachy-mini
  立即试用优先级：观望
  理由：单价对个人开发者偏高，价值在于打通"开源消费级机器人"叙事；考虑做家庭/教育原型时再下手。

- **OpenMed Agent (Preview)** — Hugging Face / OpenMed

  核心能力：
  - 1000+ OpenMed 医学模型在 HF 上
  - 临床抽取 + 术语对齐由 HF endpoints 驱动
  - 全程工具调用与 plan 可视，可挂 MCP 服务

  链接：https://huggingface.co/openmed
  立即试用优先级：本周内试
  理由：医疗 AI 团队可直接评估能否替代自建临床抽取流水线，省去 NER + UMLS 自研。

- **Meta Sapiens2** — Meta（社区 @mervenoyann 整理）

  核心能力：
  - 在 10 亿人像图像上训练
  - 0.1B → 5B 参数共 6 个尺寸，统一 ViT/patch16
  - 输出 pose / part segmentation / surface normals / pointmaps，1024×768 与 4K
  
  链接：链接未提供
  立即试用优先级：本周内试
  理由：替代或叠加 OpenPose、DensePose 等老模型，适用于虚拟试衣、动捕、AR 内容生产链路。

- **Qwen3.6-35B-A3B-MTP GGUF** — Unsloth（Hugging Face 转推）

  核心能力：
  - 多 token 预测（MTP）量化版本
  - 提供 GGUF，本地推理友好

  链接：https://huggingface.co/unsloth/Qwen3.6-35B-A3B-MTP-GGUF
  立即试用优先级：本周内试
  理由：本地推理用户可直接对比 MTP 在 35B-A3B（MoE 激活 3B）模型上的解码加速。

- **physics-intern** — Stanford / Sakana 协作（@dlouapre 发布，@Thom_Wolf 转推）

  核心能力：
  - Agentic 框架，把 Gemini 3.1 Pro 在 CritPt 理论物理基准上从 17.7% 提到 31.4%
  - 分解问题并派发给专家 agent

  链接：链接未提供
  立即试用优先级：观望
  理由：方法在窄域可重用，但需有 Gemini 3.1 Pro 配额；适合做"agent 编排能否撑起 SOTA"的内部论证。

---

## 3. 行业趋势 & 热议话题

- **实时语音 agent 从轮流式跨入"边说边想"阶段**

  参与讨论的主要声音：@thinkymachines、@miramurati、@SakanaAILabs / @hardmaru、@ArtificialAnlys、@elonmusk、@OpenAIDevs、@lilianweng
  主流观点：S2S 模型不能只靠提速，要在响应过程中后台并行注入推理或事实校验。Sakana KAME（异步后端 LLM 注入）、Thinking Machines Interaction Models（全双工 + dialogue management 隐式建模）、xAI Grok Voice Think Fast（实时后台 reasoning）、OpenAI GPT-Realtime-2（agent 客服）四条独立路径同时出现。
  主要分歧：是用单一大模型 + 实时推理（xAI 路径），还是前后端拆分（KAME 路径），还是把交互建模本身作为模型能力（Thinking Machines 路径）。
  信号强度：强
  判断依据：4 个独立组织、3 个第三方基准（τ-Voice、Audio MC S2S、ICASSP 2026 接收）、且与重大新闻 #2、#4 多源共振。

- **大 MoE 推理基础设施完成 GB200 NVL72 迁移**

  参与讨论的主要声音：@perplexity_ai / @AravSrinivas、@NVIDIADC、@huggingface（DeepSeek V4 GGUF on M3 Max）
  主流观点：服务大 MoE（Qwen3 235B 类）已经从 Hopper 切到 Blackwell GB200 NVL72，prefill/decode 解耦带来吞吐显著提升；同时本地端推理（M3 Max + DeepSeek V4 GGUF）也走通可用。
  信号强度：中
  判断依据：Perplexity 公开技术博客，NVIDIA 数据中心账号背书；本地侧 DeepSeek V4 GGUF 在 HF 上线，构成"云端最大化吞吐 + 端侧最小化部署"双向印证。

- **AI agent 基础设施正在分赛道立项**

  参与讨论的主要声音：@JudgmentLabs / @alexshander03、@JeffDean（Open Defense）、@huggingface（OpenMed Agent）、@NotionHQ / @ivanhzhao
  主流观点：agent 不再只是 chatbot 包装，而是按垂直域生成可定价的"基础设施"——评估 & 改进（Judgment Labs $32M）、安全漏洞挖掘（depthfirst Open Defense）、医疗（OpenMed Agent）、知识工作平台（Notion AI 60% 业务占比）。
  信号强度：中
  判断依据：4 个独立组织在 24 小时内分别给出融资、补贴、产品发布、财务披露四类不同信号。

---

## 4. 值得关注的洞察 & 观点

- @AndrewYNg（Coursera 联合创始人 / 斯坦福 CS 兼职教授）：

  「There will be no AI jobpocalypse... I predict the opposite: There will be an AI jobapalooza!」
  为什么值得关注：以美国失业率仍维持 4.3% 为锚点，指出 AI 实验室和 SaaS 厂商各自有动机夸大替代叙事——前者抬估值、后者按年薪而非按 SaaS 计价收费；提供反对"AI 失业末日"叙事的产业利益结构性分析框架。

- @GaryMarcus：

  「Claude Code... is the most neurosymbolic thing I have ever seen in my life. 53 symbolic tools, 500,000 lines of symbolic code, combined with a state-of-the-art LLM. It is categorically *not* a victory for pure LLMs.」
  为什么值得关注：Marcus 长期主张神经符号路线，把 Claude Code 的工程实现（参考 ccunpacked.dev 源码梳理：50+ 工具、agent loop、多 agent orchestration）当作其立场的实证。指出"前沿 agent 的能力主要来自外部确定性工具调用 + LLM 决策"，而非模型自身能力跃迁——影响产品决策：复刻 agent 的核心成本在工具集设计而非换模型。

- @ivanhzhao（Notion CEO）：

  「2 weeks ago my team and I spent most of our time in the Claude desktop app trying to collaborate on Claude projects. As I started dabbling in Notion AI agents, I quickly realized this was the software layer that was missing between myself, my team, and AI.」
  为什么值得关注：来自 SaaS 平台 CEO 的一手观察，揭示 Claude/ChatGPT 桌面应用在"团队级 agent 协作"层缺位，开放了"SaaS 工作空间作为多 agent 编排底座"的产品窗口；同时表态在 Notion 内"GPT-5.5 表现优于 Opus 4.7"，提示团队应保留多模型路由灵活性。

- @tobi（Shopify CEO）：

  「AI-referred shoppers convert better and spend more」
  为什么值得关注：电商场景内首批可公开引用的 AI 流量质量数据。来自平台自身（shopify.com/enterprise/blog/ai-search-insights），可作为衡量"ChatGPT/Perplexity/Gemini 等作为新 SEO 入口"的早期信号；具体数字未在推文中给出，需自行查阅原文。

---

## 5. 实用资源 & 教程

- **Open Athena: Scaling Laws That Extrapolate 300× Past the Fit**

  类型：技术博客
  用途：当下被 @NandoDF 推荐"理解 scaling laws 最好的资源"，给出可外推 300 倍的拟合方法
  链接：https://openathena.ai/blog/delphi/
  上手难度：中

- **Claude Code Unpacked**

  类型：源码导读
  用途：把 Claude Code 的 agent loop、50+ 工具、多 agent 编排、未发布功能从源码梳理出来——做 agent 产品的工程参考
  链接：https://ccunpacked.dev/
  上手难度：中

- **Claude Constitution 音频版**

  类型：音频
  用途：Anthropic 把 Claude Constitution 由两位作者（Amanda Askell、Joe Carlsmith）朗读为 audiobook，并附写作过程 Q&A
  链接：anthropic.com/constitution
  上手难度：低

- **Hugging Face 数据集破 100 万**

  类型：平台公告
  用途：开放数据集总量从 0→50 万用 4 年，过去 8 个月翻倍到 100 万，agent 主导的数据生成是主要驱动
  链接：https://huggingface.co/datasets
  上手难度：低

- **The Ultimate Guide to RL Environments**

  类型：教程
  用途：HF Spaces #1 趋势，专门讲为 LLM 构建并扩展 RL 环境——agent + RL 团队的实操教程
  链接：链接未提供（HF Spaces 上检索"RL Environments"）
  上手难度：中

---

## 传播力素材

- "There will be no AI jobpocalypse... I predict the opposite: There will be an AI jobapalooza!" — @AndrewYNg · 👍1988 👁186387 · engagement_rate 0.69%
  改写方向：适合公众号 / 知乎专栏改写为"AI 替代论的三个利益结构性谬误"——把 Ng 的"实验室/SaaS/企业三方动机分析"翻成中文产业语境。
  点评：Andrew Ng 的"反末日"观点本身不新，但首次把"为何这种叙事盛行"做成结构性归因，是其能广泛传播的关键。盲点是 4.3% 失业率本身就受到统计口径的争议，且软件工程师招聘强劲掩盖了应届招聘骤减的事实；只看这句话会忽略不同岗位类型受 AI 影响速度的极大差异。

- "Claude Code (still not AGI but biggest advance since GPT-4) is the most neurosymbolic thing I have ever seen in my life. 53 symbolic tools, 500,000 lines of symbolic code, combined with a state-of-the-art LLM." — @GaryMarcus · 👍568 👁122144 · engagement_rate 0.60%
  改写方向：知乎 / 小红书科普向，"为什么 Claude Code 是 AI 真正进步的样子——不是模型变强，是把工具用好了"。
  点评：把工程现实（大量工具调用 + 模型决策）说成"神经符号 AI 的胜利"在策略上很取巧，本质是借 Claude Code 这一公认强产品反向佐证自身立场。盲区是忽略了模型本身在 tool calling、planning 上的能力提升才让 53 个工具能被有效使用——脱离模型谈工具同样片面。

- "1/ The '20 tokens per parameter' Chinchilla scaling law is flawed. It is an artifact of your tokenizer. Scaling shouldn't be measured in tokens at all. It should be measured in bytes." — @NandoDF 转 @che_shr_cat · 👍239 👁10867 · engagement_rate 1.95%
  改写方向：小红书技术圈/即刻短贴，引导读者重新审视"参数 vs 数据"经典命题；可改写为"Chinchilla 法则错在哪：tokenizer 让你高估了模型的数据需求"。
  点评：engagement_rate 极高（近 2%）说明从业者在收藏深读。观点本身在学术圈已酝酿一段时间，但用一句话扣到"用字节而不是 token 衡量"是绝佳传播版本。盲区是字节计量对非英语语种（CJK、Arabic）的相对优势在工程上还需要更严谨比较，否则会被误读为"非英语数据被低估了多少倍"。

- "We're dropping two open source SLMs this week. 1. One of them matches SOTA accuracy at up to 93x smaller. 2. The other one beats a recent OpenAI model." — @huggingface 转 @ash_csx · 👍584 👁44335 · engagement_rate 0.90%
  改写方向：科技自媒体悬念预告改写——"本周 HF 要发的两个小模型可能改写端侧 AI 格局"，配 SLM 概念解释。
  点评：典型的"双悬念营销"——SOTA + 93× 更小、击败 OpenAI 模型——精准命中"端侧/小模型"赛道讨论热度。盲区是未公布具体基准、模型类型、推理预算；如果不交叉发布日和实际数字，单看这句话会把读者拉到过高预期。

---

## 信号 / 噪音比

进入第 1 节的有效新闻 6 条，进入第 2-5 节的有效信号 约 22 条，剩余约 50% 为低价值或噪音（主要为 Elon Musk 大量 SpaceX/Tesla/政治转推、Yann LeCun 转推 Trump-Obama 政治内容、Gary Marcus 多条短评级补充推文）。今日整体信号密度：正常。

---

**今日行动建议**

今天（30 分钟内）：
基于 [xAI 同日上线 Grok Skills + Grok Voice Think Fast 1.0 取得 τ-Voice 第一]——登录 grok.com，用 `/` 触发 Skills 入口；若是 Claude Skills 已有 skills.md，直接导入一份做端到端跑通，对比 Skills 与 Claude Projects 在同一个工作流上的产物质量。

本周内：
基于 [实时语音 agent 从轮流式跨入"边说边想"阶段]——产出一份不超过 1 页的内部备忘录，把 Grok Voice Think Fast 1.0（52.1%）、GPT-Realtime-2 (High)（39.8%）、Gemini 3.1 Flash Live（37.7%）、Thinking Machines Interaction Models（43.4% APR）四条路线对照成本/能力/部署形态表，标注自家语音产品要切换或并轨的决策点。

月内验证：
基于 [Sundar Pichai 在 The Android Show (I/O Edition) 发布 Gemini Intelligence]——跟踪两个指标：(1) Pixel / Samsung Galaxy 在 GSMArena / 安兔兔上的"AI 评分"专栏出现节奏；(2) 自家 Android 应用在 Gemini Intelligence 系统层切走"打开应用 / 跨应用任务"流量后的 DAU 变化幅度，月底对照是否需要重写应用入口设计。

---

**本期信源**：@elonmusk @ylecun @AndrewYNg @ID_AA_Carmack @GaryMarcus @ClementDelangue @huggingface @sundarpichai @demishassabis @JeffDean @gdb @miramurati @hardmaru @soumithchintala @NandoDF @ivanhzhao @tobi @AravSrinivas @AmandaAskell @nickaturley @adcock_brett @kchonyc @giffmana @nvidia @cohere @StanfordHAI @StanfordAILab @AI21Labs @lilianweng @tegmark @chrmanning @jeremyphoward @Thom_Wolf @NotionHQ @emollick @OpenAI @__nmca__（共 37 位）
