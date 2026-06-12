# AI 行业情报简报 | 2026-06-13

> 数据窗口：2026-06-12 06:00 — 2026-06-13 06:00（北京时间，过去 `24 小时`）
> 深度分析：3 条 | 模板版本：v2.3

本期推文池 149 条 / 活跃账号 33 个。SpaceX IPO 占据 timeline 注意力主流，但与 AI 无直接关联部分按预筛规则剔除，仅保留 NVIDIA × SpaceX 合作与"AI 取代货币"等 AI 相关切面。

---

## 1. 重大新闻 & 突发事件

- Meta 大幅削减 token 预算，企业 AI 支出降温信号扩散

  来源：@amir（The Information，已被 @GaryMarcus 引述，约 1 小时前）
  关键数字：Meta 数月前还被视为 Claude 的"亿级年支出"客户，本轮做了 180 度调头；具体削减幅度 [未经验证]
  行业影响：对 Anthropic 直接利空——Meta 此前被多方报道为其前列付费客户。更广义的信号是，本季度多家大厂在重估"token = 算力 = 增长"的等式，2026 上半年随意烧 token 的窗口正在关闭，对所有按调用量收费的前沿厂商都有压力。

- MiniMax M3 与 Kimi K2.7-Code 同窗口期登陆 Hugging Face

  来源：@huggingface、@ClementDelangue（约 6 小时前）
  关键数字：MiniMax M3 ~428B 总参 / ~23B 激活，附带的 MSA（MiniMax Sparse Attention）kernel 在 1M 上下文下宣称比 M2 prefill 9×、decode 15× 提速（来源：huggingface.co/MiniMaxAI/MiniMax-M3，当事方口径）；Kimi K2.7-Code 定位"frontier code open source model"，权重 huggingface.co/moonshotai/Kimi-K2.7-Code
  行业影响：两家中国实验室在同 24 小时内放出两个偏 agent / 偏 code 的前沿开源模型，且都附带可直接落地的工程化组件（kernel、weights）。叠加 Meta 削减 token 信号，企业自托管开源模型的吸引力在数据点层面被进一步加强。

- Claude Fable 5 评测透明度争议，Vals AI 上线"无 fallback 视图"

  来源：@ClementDelangue 多条原贴 + 转推 @ValsAI（约 3–8 小时前）
  关键数字：Fable 5 在 FrontierMath v2 上 Tier 1–3 达 87%、Tier 4 达 88%（来源：@EpochAIResearch，当事方口径）；Fable 5 公开 API 定价 $10 / $50 每百万 input/output token（来源：codersera.com / venturebeat.com，已核实），约为 Opus 4.8 的 2 倍
  行业影响：Hugging Face CEO 公开指控 Artificial Analysis 在榜单中将"Fable 5 + Opus 4.8 fallback"组合与单模型同框比较结构上偏向闭源 API；Vals AI 已上线"fallback 关闭"视图（拒答=0 分）。这是 2026 第三方榜单首次因路由/fallback 机制被迫调整公开方法学，会影响后续所有 leaderboard 的可比口径。

- Anthropic 新数据保留政策引研究侧大面积反弹

  来源：@ylecun 转 @NaveenGRao、@Thom_Wolf 转 @natolambert（约 10–12 小时前）
  关键数字：Naveen Rao 公开宣布团队不再使用新版 Claude，原因是"prompt 包含我们全部 IP（设计文件和文档）"（来源：@NaveenGRao，当事方口径）
  行业影响：保留默认策略改成"保留 prompt 和使用数据"叠加上周"对 AI 研究类查询的隐性 fallback"两件事，让一批前 Meta / Anthropic / DeepMind 研究者公开表态降级或退出。这是闭源前沿厂商 vs 研究社区之间一次结构性裂痕，会加速 Olmo 等开放科学项目的资源聚集。

- Gemini Omni Flash 登顶 Video Arena（T2V & I2V 双榜）

  来源：@demishassabis 转 @arena（约 17 小时前）
  关键数字：T2V 较 Veo 3.1（1080p）领先 +158 pt，较第二名 Seedance 2.0 领先 +61 pt（来源：@arena，当事方口径，未经独立验证）
  行业影响：Veo 3.1 才是 Google 自家的"上一代旗舰"，被自家新模型砍掉 158 分意味着视频生成代际差扩大；对 Pika / Runway / Kling 等同赛道厂商定价和保留率会有直接压力。

- 通用前沿 LLM 在医学评测中击败专用临床工具（Nature Medicine）

  来源：@EricTopol 经 @kchonyc 转发（约 2 小时前）
  关键数字：Google、OpenAI、Anthropic 前沿模型在 12 名美国临床医生盲评中击败 @EvidenceOpen 和 @UpToDate（来源：nature.com/articles/s41591-026-04431-5，已核实期刊）
  行业影响：对垂类医疗 AI 创业的估值假设直接挑战——若通用模型 + 通用 RAG 已能压过专用工具，专用产品的差异化必须从"基础模型能力"上移到"工作流嵌入 / 责任承担 / 数据接入"。

---

## 6. TOP 新闻深挖

#### 深挖：Meta 削减 token 预算，企业 AI 支出降温信号扩散

背景补充：
The Information 的报道核心是 Meta 几个月前曾被认为是 Anthropic 前几大年度客户之一，本轮转为"token-minimizing"立场。同期 Pragmatic Engineer 的"a trend of trying to cut back on AI spend within eng departments"博文与 Cisco 副总 Jeetu Patel 在 Semafor 的发言（"The costs of tokens are far higher than the actual value these tokens are generating at scale"）形成共振——这条 Cisco 引述原文发于 2026-06-11，今日被 @GaryMarcus 引用。背景中还有一条之前可核实的事实：Uber CTO 公开承认 2026 年 AI 预算 4 个月内烧光（来源：cloudzero.com / axios.com，已核实）。

数字核实：
"Meta 此前数十亿美元/年 Claude 支出" → 与 The Information 原文一致，但绝对数字 [未经验证]；Fable 5 定价 $10/$50 → 已验证（来源：codersera.com、venturebeat.com）。

扩展影响：
开源端三天内同时放出 MiniMax M3、Kimi K2.7-Code、MiniMax MSA kernel，以及 Hugging Face Command Code"30 天突破 10K 付费"（来源：@ClementDelangue，当事方口径）。供给侧（前沿闭源）涨价 + 需求侧（大厂）压缩，开源/自托管的 ROI 视窗被推开。

对国内从业者的意义：
1）出海 API 业务可借此机会用 MiniMax M3 / Kimi K2.7-Code 重新定位"性价比层"；2）国内做 agent 类 SaaS 的公司应主动给客户提供 token 上限可见性和 fallback 选项，避免重蹈 ServiceNow / Uber 半年烧光预算的故事；3）对 GPU 租赁、推理服务赛道是顺风。

延伸阅读：
https://blog.pragmaticengineer.com/the-pulse-a-trend-of-trying-to-cut-back-on-ai-spend-within-eng-departments/

#### 深挖：MiniMax M3 与 Kimi K2.7-Code 同窗口期开源

背景补充：
MiniMax M3 早在 2026-06-01 即由 MiniMax（上海）发布预告，本次上 Hugging Face 是正式权重开放（来源：felloai.com / codersera.com，已核实）。架构上为 sparse MoE：~428B 总参、~23B 激活、原生 1M 上下文，且配套 MSA（MiniMax Sparse Attention）kernel 一并开源在 Hugging Face Kernel Hub 上，可直接被 transformers 调用。Kimi K2.7-Code 来自 Moonshot AI，公开口径为"frontier code open source model"，目前可在 huggingface.co/moonshotai/Kimi-K2.7-Code 拉取，详细 benchmark 尚未集中披露。

数字核实：
~428B / ~23B 激活、1M context、MSA 1M 上下文下 prefill 9× / decode 15× 提速 → 与 MiniMax 官方一致（已验证）。Kimi K2.7-Code 的代码能力评测分数 [未经验证]，需观察未来 1–2 周第三方榜单。

扩展影响：
两个模型都明确指向"agent / 代码"场景，叠合 Anthropic Fable 5 高价 + 数据保留政策的争议，会推动一部分原本默认走 Claude Code / Codex 的工程团队评估"开源 + 路由"替代方案。Hugging Face CEO 已公开倡议"美国需要开源 champion"，且点名 Apple 新 CEO 应在工作站上跑本地开源模型。

对国内从业者的意义：
1）国产模型在 agent / 代码两个最贵的 token 场景上首次形成开源连击，对国内 ToB 落地是直接利好；2）MSA 思路（1M 上下文 sparse attention）可被国内做长上下文/长文档 RAG 的团队直接借鉴；3）建议把 MiniMax M3 + Kimi K2.7-Code 作为本周必须做的 PoC 对照组。

延伸阅读：
https://huggingface.co/MiniMaxAI/MiniMax-M3
https://huggingface.co/moonshotai/Kimi-K2.7-Code

#### 深挖：Claude Fable 5 评测透明度争议

背景补充：
Fable 5 于 2026-06-09 发布，是 Anthropic 首个公开可用的"Mythos-class"模型，与受限的 Mythos 5 共享权重，但通过 safety classifier 在高风险场景下静默 fallback 到 Opus 4.8（来源：venturebeat.com / techcrunch.com，已核实）。Hugging Face CEO 在过去 24 小时内连发数条质疑 Artificial Analysis 把"Fable 5 + Opus 4.8 fallback"组合与其它单一模型同框打分"结构上偏袒闭源 API"。Vals AI 已在 24 小时内上线"fallback 关闭"视图，将 refusal 计为 0 分。

数字核实：
Fable 5 FrontierMath v2 Tier 1–3 87% / Tier 4 88% → 已验证（来源：@EpochAIResearch，当事方口径）。"成本是 Opus 4.8 的 2 倍"→ 与公开定价 $10/$50 vs $5/$25 一致（已验证）。"4.5× GPT 5.5 high 价格、benchmark 仅高 10%"→ 来自单一推文（@JakeKAllDay），属二手对比，[未经验证]。

扩展影响：
1）Fable 5 + fallback 与 GPT-5.5 high 的"代际差"在剥离 fallback 后会明显收窄，影响 Anthropic 在企业评测口径上的优势；2）Vals AI / Artificial Analysis 之后的所有榜单都需要披露"是否存在动态路由 / fallback"；3）Naveen Rao、Thom Wolf 提出的"silent manipulation"问题与本次 fallback 是同一根逻辑——闭源服务对外公布的能力≠用户实际拿到的能力。

对国内从业者的意义：
1）国内做闭源 API 产品的厂商应警觉"静默 fallback"将被列为不诚信行为，提前在控制面板里把路由策略公开化；2）国内评测榜（OpenCompass、SuperCLUE 等）应同步引入"是否单一模型 / 是否含 fallback"列；3）使用海外前沿 API 的产品需要在合规与可控性之间重新定权重，必要时考虑双供应链。

延伸阅读：
https://venturebeat.com/technology/anthropic-brings-mythos-to-the-masses-with-claude-fable-5-its-most-powerful-generally-available-model-ever

---

## 2. 新产品 & 功能发布

- MiniMax M3 — MiniMax AI（已在第 1 节展开，此处不重复）

- Kimi K2.7-Code — Moonshot AI（已在第 1 节展开，此处不重复）

- Google AI 本周一揽子更新 — Google AI（@GoogleAI 官方汇总）

  核心能力：
  - Gemini 3.5 Live Translate：实时语音→语音翻译音频模型
  - NotebookLM：chat 内置 agentic 能力 + 高阶推理 + 多种新输出格式
  - DiffusionGemma：开源文本扩散模型实验版（极快生成）
  - Project Genie：今日起对全球 Google AI Ultra 5X 订阅用户开放（来源：@GoogleDeepMind 转 @GoogleLabs，当事方口径）

  链接：labs.google/projectgenie
  立即试用优先级：本周内试
  理由：DiffusionGemma 与 Live Translate 是两个对现有产品流可能直接改写的方向；Project Genie 解锁全球后是首次可对照 Sora/Veo 的开放渠道。

- NVIDIA MotionBricks — NVIDIA Research（SIGGRAPH 2026）

  核心能力：
  - 35 万+ 动作片段单一开放模型
  - 实时角色动画 15,000 FPS（来源：@nvidia，当事方口径）
  - 无需手动 transition / fine-tune，并可迁移到机器人

  链接：nvlabs.github.io/motionbricks
  立即试用优先级：本周内试
  理由：游戏 / 数字人 / 仿真用户可直接评估替换现有 motion library。

- Amazon Simple Strands Agent（SSA）— Amazon Science

  核心能力：
  - 轻量、开源 agent harness
  - 同时在 SWE-Bench-Verified、SWE-Bench-Pro、Terminal-Bench2 上拿到 SOTA（来源：@AmazonScience，当事方口径）
  - 主打"弥合模型 intent 与 harness 执行的 gap"

  链接：amazon.science/blog/bridging-intent-and-execution-in-agentic-systems
  立即试用优先级：今天就试
  理由：harness 层是 agent 性能与成本的主战场之一，且 SSA 是开源轻量级，30 分钟可跑起来对照现有 Cline / OpenHands 配置。

- World Labs 3D 生成三连发 — World Labs（@drfeifei）

  核心能力：
  - 三篇论文同日发布，方向均为利用大规模生成模型 + 2D prior 生成 3D 内容
  - 团队由 @HaoZhang623、@BDuisterhof、@DrTunnels 主导

  链接：theworldlabs（见 @drfeifei 原帖串）
  立即试用优先级：观望
  理由：偏研究侧；商业落地节奏仍未公开。

- OpenAI Codex 引荐返额度 + Docs Agent — OpenAI（@gdb、@OpenAIDevs）

  核心能力：
  - Codex 接下来两周内可通过推荐好友"攒一次 rate limit 重置"
  - developers.openai.com 上线 docs agent，可直接定位文档位置

  链接：developers.openai.com
  立即试用优先级：观望
  理由：推荐机制属增长玩法；docs agent 与 Anthropic、Cursor 等同类已有差距不大。

- Notion 数据库属性置顶上限 4 → 15 — Notion

  核心能力：
  - database page 现可置顶最多 15 个属性（来源：@NotionHQ，当事方口径）

  链接：链接未提供
  立即试用优先级：观望
  理由：纯产品微更新；适合既有重度用户。

- Tesla FSD 14.3.4 — Tesla（@elonmusk）

  核心能力：
  - 14.3.x 主版本继续推送；具体改动 [未经验证]
  - 同日 @Tesla 宣布比利时成为第 5 个批准 FSD Supervised 的欧洲国家

  链接：链接未提供
  立即试用优先级：观望
  理由：当事方未给具体能力差分。

---

## 3. 行业趋势 & 热议话题

- token 经济性反扑：从大厂削预算到第三方榜单透明化

  参与讨论的主要声音：@GaryMarcus、@ClementDelangue、@GergelyOrosz、@Cisco（jpatel41，via @semafor）、@amir、@emollick
  主流观点：单 token ROI 在企业侧首次进入"必须算账"阶段，开源 + 路由 + 本地化的组合在工程团队中迅速变成默认讨论选项。
  主要分歧：乐观派（如 NVIDIA @Konstantine Sequoia 访谈）仍把这看作"5 层蛋糕"中的中间扰动，看 5–10 年；悲观派（GaryMarcus 等）认为这会反向波及数据中心投资规模。
  信号强度：强
  判断依据：4 个独立信源 + 2 个权威媒体（Semafor、The Information）+ Pragmatic Engineer 博客 + 多家公司案例（Meta、Uber、ServiceNow）共同指向"压缩 token 支出"的真实动作，不是单点观点。

- 开源前沿模型聚焦"代码 + agent"双场景

  参与讨论的主要声音：@huggingface、@ClementDelangue、@MiniMax_AI、Kimi.ai（@Kimi_Moonshot）、@AmazonScience
  主流观点：1M 上下文 / sparse attention / 轻量 agent harness 在 24 小时内集中放出，对前沿闭源 API 形成第一次系统化替代选项。
  主要分歧：开源能否在 agent 工作流的端到端可靠性上追上闭源仍待验证。
  信号强度：强
  判断依据：MiniMax M3 权重 + MSA kernel + Kimi K2.7-Code + Amazon SSA harness 在同窗口期独立出现，方向高度一致。

- Fable 5 驱动的"AI 辅助 CAD / 仿真 / 工程"工作流可用性突破

  参与讨论的主要声音：@NandoDF（×3）、@emollick、@mattshumer_
  主流观点：用 Claude Fable 5（含其 confBuild / Rork / 自定义脚本）一次性"造出"涡扇发动机参数模型、QDD actuator、六足步行机器人、SimRefinery 仿真游戏、Hogwarts 城堡，且 30 分钟 / 400k token 量级即可。
  信号强度：中
  判断依据：3 位独立 KOL（含 1 位前 DeepMind 研究负责人）在 24 小时内独立发出可执行 demo，且关注者群体不重叠；但商业化样本尚未出现，故为中。

---

## 4. 值得关注的洞察 & 观点

- @Cisco / jpatel41（Cisco 副总，via @semafor，原文发于 2026-06-11，今日被引用）：

  「The costs of tokens are far higher than the actual value these tokens are generating at scale. The big risk is, if you don't create an equilibrium there, then people just pull back on using tokens.」
  为什么值得关注：这是大厂高管首次明确把"token 经济崩塌"作为系统性风险点公开喊话，且与 Meta 削预算的事实形成证据闭环。

- @Thom_Wolf（Hugging Face 联合创始人）：

  「Don't release the model if you can't hit your safety targets. Silent manipulation of users is baking in a misalignment to the system at its face level. This comes with a permanent degradation in user trust.」
  为什么值得关注：来自一个不在该利益相关方的前沿厂商高管，把"静默 fallback"重新定义为"对齐失败"，把行业舆论从"功能取舍"拉回"产品诚实性"。

- @ClementDelangue（Hugging Face CEO）：

  「Given token economics, we really need Apple's new CEO to go all in on workstations that can run local, open source models—ideally with a router that can flip between local and frontier models when the former gets stuck. America needs an open source champion.」
  为什么值得关注：在中国开源模型连发的同一天点名 Apple，是把端侧 + 开源路由作为美国主权 AI 路线主张的明确化表态。

- @GaryMarcus（NYU，AI 怀疑派）：

  「Many people are finding that the advantages of Fable often aren't worth the cost… newer, immense models will be niche that customers usually won't pay for. Even bigger models might not be worth building at all.」
  为什么值得关注：与 token 削预算趋势在结论上同向，但论证路径是"模型 ROI 衰减 → 数据中心可能过剩"，提出了少见的"算力供给端长期看空"假设。

- @NaveenGRao（前 MosaicML/Databricks）：

  「My team loves Claude. But this new policy of retaining prompts and usage is a red line... we simply can't give over our usage. Prompts contain our IP—literally all our design files and docs.」
  为什么值得关注：研究/工程团队公开拒绝升级，且 Yann LeCun 转发，预示研究侧大客户流失风险落地。

---

## 5. 实用资源 & 教程

- MIT 计算机科学数学基础免费课程（含 Erik Demaine 状态机 Lecture 4）

  类型：教程
  用途：CS 数学基础系统补课
  链接：bit.ly/4kXuqQ6（v/@MITOCW）
  上手难度：低

- Stanford Canaries Dashboard（ADP × Stanford Digital Economy Lab）

  类型：数据集 / 仪表盘
  用途：跟踪 AI 对不同岗位、不同资历的就业影响（早期 vs 中期职业、AI 高 vs 低暴露行业）
  链接：canaries.stanford.edu
  上手难度：低

- Volt（3D 场景理解的纯 Transformer 架构）

  类型：论文
  用途：把 ViT 思路最小改动迁移到 3D 场景理解
  链接：yilmazkadir.github.io/Volt/ ; arxiv.org/abs/2604.19609
  上手难度：中

- FACTR 2（NEXT + FIRST：低成本机械臂的力感知策略学习）

  类型：论文
  用途：在不加额外力传感器的前提下，让消费级机械臂学到 contact-rich 任务
  链接：见 @NandoDF 原帖串
  上手难度：中

- Hugging Face 视觉新教程（RF-DETR-Seg 卫星图像分割、RF-DETR 手机 UI 目标检测）

  类型：教程
  用途：在 Transformers 中开箱微调，目标"在 toaster 上能跑"
  链接：见 @huggingface 原帖（transformers 文档）
  上手难度：低

- SandboxAQ AQCat25（催化剂大规模 DFT + ML 势函数）

  类型：论文（Nature Computational Materials）
  用途：1350 万 DFT 计算训练，专用化学场景不破坏跨域泛化
  链接：pub.sandboxaq.com/publications/aqcat25-unlocking-spin-aware-high-fidelity-machine-learning-potentials-for-heterogeneous-catalysis
  上手难度：高

---

## 传播力素材

- 「The costs of tokens are far higher than the actual value these tokens are generating at scale. The big risk is, if you don't create an equilibrium there, then people just pull back on using tokens.」 — @semafor 引述 Cisco 副总 jpatel41 · 👍401 👁[未提供] · engagement_rate [未提供]
  改写方向：适合公众号 / LinkedIn 长文开篇钩子，标题方向"token 经济到了第一次还账时刻"。
  点评：原话来自硬件/网络背景的 CISCO 高管而非 AI 厂商，立场可信。局限在于"价值≠成本"的论述把分布式收益（生产力、留存）压缩成单一报价；只看这句话容易低估 LLM 在已落地工作流里仍在创造的间接价值。

- 「kinda crazy that someone's full-time job was to steer claude to sabotage ML research capabilities for paying customers」 — @joannejang（OpenAI），@jeremyphoward 转推 · 👍3,342 👁127,944 · engagement_rate 0.17%
  改写方向：适合 X / 知乎"AI 厂商不告诉用户的那些 fallback"主题改写。
  点评：尖锐、画面感强，能瞬间引发研究员/付费客户共鸣。但需注意"sabotage"是有立场的措辞，原意是 fallback 与 silent classifier 对研究类查询降级，不等于厂商主观破坏；引用时应保留上下文，避免被理解为蓄意攻击。

- 「The world is moving from retrieval to generation… we move from the carpenters to the architects.」 — @nvidia 转述 Jensen Huang × @Sequoia Konstantine Buhler · 👍66 👁10,990 · engagement_rate 0.12%
  改写方向：适合企业内部分享 / 战略备忘录引用。
  点评：Jensen 把"生成"框架化为基础设施转移，叙事张力大，对非技术高管尤其好用。盲区在于"5 层蛋糕"以 NVIDIA 视角组织，忽略了开源 / 端侧 / 路由层带来的横向价值再分配。

- 「Given token economics, we really need Apple's new CEO to go all in on workstations that can run local, open source models.」 — @ClementDelangue · 👍1,265 👁88,569 · engagement_rate 0.12%
  改写方向：适合科技政策 / 端侧 AI 主题专栏改写为"为什么 2027 是端侧 AI 之年"。
  点评：自带"美国 vs 中国开源主权"叙事钩子，传播力强。局限在于把 Apple 一家承担"美国开源 champion"是一厢情愿，硬件不等于模型生态——Apple 历史上对开源态度有限。

- 「Open Source and On device about to make a generational run in 2027.」 — @ClementDelangue 转 @Ranidu · 👍14 👁3,449 · engagement_rate 0.09%
  改写方向：适合年度趋势预测稿件引用为"业内一线表态"。
  点评：胜在"generational run"+ 时间点的具体性。局限是缺乏定量支撑，单独引用容易被读作 cheer-leading；建议与"Meta 削 token、开源模型连发"等本期事实并陈。

---

## 今日行动建议

今天（30 分钟内）：
基于 [MiniMax M3 与 Kimi K2.7-Code 同窗口期开源]——在 huggingface.co/MiniMaxAI/MiniMax-M3 和 huggingface.co/moonshotai/Kimi-K2.7-Code 各拉一份权重 / 接 Inference Provider，用自己一段最贵的真实代码 / agent prompt 跑对照，记录三项数字：单次延迟、单次 token 成本、与现用闭源 API 的输出 diff。

本周内：
基于 [Meta 削减 token 预算 + Fable 5 评测争议]——做一份 1–2 页 PDF 内部备忘录，给团队/客户重算当前线上 agent 工作流的"token 单价 × 月调用量 × Anthropic / OpenAI / 开源替代"三档成本，并附"是否存在 fallback 风险"专项；输出物：一张三方对比表 + 一条季度预算调整建议。

月内验证：
基于 [Fable 5 评测透明度争议]——持续跟踪 Artificial Analysis、Vals AI、OpenCompass 在本月内是否新增"单一模型 / 含 fallback"披露列；衡量指标：1）公开榜单是否新增"is_routed"列；2）Fable 5 在禁用 fallback 后相对 GPT-5.5 high、Opus 4.8、MiniMax M3 的相对排名变动幅度；3）国内有无团队跟进发出"无 fallback 复测"报告。

---

## 信号 / 噪音比

进入第 1 节的有效新闻 6 条，进入第 2-5 节的有效信号约 22 条，剩余约 60% 为低价值或噪音（主要由 SpaceX IPO 与相关情绪类推文构成）。今日整体信号密度：正常。

**本期信源**：@GaryMarcus @ClementDelangue @huggingface @nvidia @StanfordHAI @emollick @ylecun @NandoDF @mattshumer_ @ClementDelangue @gdb @JeffDean @drfeifei @karpathy @AmazonScience @GoogleAI @demishassabis @GoogleDeepMind @MIT_CSAIL @StanfordAILab @adcock_brett @jackhidary @kchonyc @EricTopol @giffmana @Thom_Wolf @jeremyphoward @AravSrinivas @NotionHQ @vkhosla @berkeley_ai @EthanJPerez @__nmca__（共 32 位）
