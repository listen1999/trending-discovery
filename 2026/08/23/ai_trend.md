# AI 行业情报简报 | 2026-08-23

> 数据窗口：2026-08-22 06:00 — 2026-08-23 06:00（北京时间，过去 24 小时）
> 深度分析：3 条 | 模板版本：v2.3

---

## 1. 重大新闻 & 突发事件

- OpenAI 将 GPT-5.6 Sol API 及积分定价下调超 20%，为期三个月

  来源：@sama（转 @OpenAI 官方公告）· 约 14 小时前
  关键数字：输入价格降至 $4/百万 tokens、输出价格降至 $20/百万 tokens（来源：@sherwinwu，当事方口径；经 web_search 交叉核实，openrouter.ai 与 orcarouter.ai 的定价追踪页确认该区间，原始费率为 $5/$30，可视为已核实数字）
  行业影响：这是 Sol 自发布以来首次降价，紧接 7 月 30 日对 Luna（降 80%）、Terra（降 20%）的调价之后，直接回应 Anthropic 与 DeepSeek 对企业 API 市场份额的挤压。对所有基于 GPT-5.6 系列构建产品的开发者，意味着调用成本结构在本季度内直接变化。

- NVIDIA Vera Rubin 进入满产，首批交付微软 Azure 数据中心

  来源：@satyanadella（@nvidia 官方账号同日确认）· 约 23 小时前
  关键数字：[未经验证]（推文未给出具体交付台数或产能数字）
  行业影响：新一代 GPU 平台开始向云厂商规模化出货，直接影响明年大模型训练与推理的成本曲线；对 Azure 客户意味着更早拿到下一代算力，对追赶中的其他云厂商构成新的算力代差压力。

- Google Gemini 3.7 Flash 成为 Gemini 系列史上增长最快模型，ARC-AGI 基准性价比领先

  来源：@sundarpichai（引用 @arcprize 基准测试结果，原始基准发布时间未知，今日被引用扩散）· 约 18 小时前
  关键数字：ARC-AGI-2 得分 84.6%、单任务成本 $0.25；ARC-AGI-1 得分 95.5%、单任务成本 $0.12（来源：@arcprize，权威基准测试机构，已核实数字）
  行业影响：用远低于顶级模型的单任务成本追平主流基准分数，直接冲击"高分只能靠高价模型"的定价逻辑，对成本敏感型 Agent 与编码工具开发者是可直接替换的选项。

---

## TOP 新闻深挖

#### 深挖：OpenAI 将 GPT-5.6 Sol API 及积分定价下调超 20%

背景补充：
经 web_search 核实，此次降价自 8 月 21 日起生效，促销价格至少持续到 11 月 21 日。这是 Sol 自发布以来的首次降价，此前 7 月 30 日 OpenAI 已下调过同系列 Luna（降 80%）与 Terra（降 20%）两款低阶模型价格，这次轮到旗舰模型 Sol。OpenAI 方面的说法是，Sol 被用于重写和优化自身推理基础设施、自动改进 GPU 利用率与生产代码，带来端到端服务成本降低 20%、通过投机解码使 token 生成吞吐量提升 15% 以上（来源：venturebeat.com、mlq.ai 综合报道）。

数字核实：
推文中的价格（输入 $4、输出 $20，每百万 tokens）→ 已验证（来源：openrouter.ai GPT-5.6 Sol 定价页、orcarouter.ai 定价追踪），相较原始费率 $5/$30，输入降 20%、输出降约 33%，与 @sama 推文所述"20%"基本一致（实际输出端降幅更大）。

扩展影响：
Anthropic 并未直接下调 Opus 系列标价，而是以同价发布能力更强的新版本、并新增可调节推理深度的"effort"设置来变相降低单位能力成本；DeepSeek 反而将 API 价格上调最多 12 倍，理由是基础设施成本上升及为可能的 IPO 做准备（来源：venturebeat.com、finance.biggo.com）。价格战的方向出现分化：美系大厂打包降价维持份额，部分中国厂商转向涨价追求盈利。

对国内从业者的意义：
对使用海外 API 中转/代理调用 GPT-5.6 系列的国内开发者，直接降低调用成本；DeepSeek 涨价若持续，会削弱其"低价替代"叙事，对 GLM、Kimi 等其他低价开源/国产模型可能是抢占中低端市场份额的窗口。

延伸阅读：
- https://venturebeat.com/technology/ai-price-wars-openai-cuts-gpt-5-6-luna-prices-by-80-as-model-competition-shifts-toward-cost
- https://finance.biggo.com/news/7e9f1d12-cf40-4852-a49a-ed69b6925090

#### 深挖：NVIDIA Vera Rubin 进入满产，首批交付微软 Azure 数据中心

背景补充：
经 web_search 核实，NVIDIA Vera Rubin 平台已于 2026 年 6 月 1 日在 GTC 台北主题演讲上宣布进入满产状态，今年秋季起向 AWS、Google Cloud、Microsoft Azure、Oracle Cloud、CoreWeave、Lambda、Nebius、Nscale 八家云合作伙伴出货，官方宣称推理成本可降低 10 倍、训练效率提升 4 倍（来源：nvidianews.nvidia.com 官方新闻稿）。微软披露其位于威斯康星与亚特兰大的 Fairwater AI 超级工厂已按 Rubin 所需的电力、散热与网络规格提前设计，可直接部署无需大改（来源：azure.microsoft.com 官方博客）。

数字核实：
推文未给出具体交付台数/产能数字，[未经验证]；"满产"（full production）这一表述与 NVIDIA 官方新闻稿一致，可确认为已验证事实（来源：nvidianews.nvidia.com）。

扩展影响：
与推文原文形成一个值得注意的对照：就在 Vera Rubin 向八家云厂商放量的同时，NVIDIA 已停止面向中国市场的 H200 芯片生产，并将相应台积电产能转移给 Vera Rubin（来源：semiwiki.com）。这轮"满产"扩张中，有一部分产能是从中国市场腾挪出来的，而非纯增量。

对国内从业者的意义：
据 Jensen Huang 表态，NVIDIA 高端 GPU 在中国市场份额已接近于零（来源：insidermonkey.com），Vera Rubin 满产不会缓解国内算力紧张，反而可能因产能优先向海外八大云厂商倾斜而进一步拉大代差。NVIDIA 转向在中国推广不受出口管制约束的 Vera CPU 作为替代路径，值得关注国内厂商是否会跟进适配这类非 GPU 算力方案。

延伸阅读：
- https://nvidianews.nvidia.com/news/vera-rubin-full-production-agentic-ai-factory
- https://semiwiki.com/forum/threads/nvidia-halts-china-bound-h200-production-shifts-tsmc-capacity-to-vera-rubin.24722/

#### 深挖：Google Gemini 3.7 Flash 成为增长最快模型，ARC-AGI 性价比领先

背景补充：
经 web_search 核实，Gemini 3.7 Flash 于 8 月 13 日发布，距上一代 Gemini 3.6 Flash 仅三周，定位为主打编码与 Agent 场景的"工作马"模型，发布时提供半价促销。早期测试/接入方包括 Box、Browser Use、Cartwheel、Databricks、Harvey、Hebbia、LangChain、Pydantic 及斯坦福大学生物系等（来源：blog.google 官方博客）。

数字核实：
ARC-AGI-2 得分 84.6%、单任务成本 $0.25；ARC-AGI-1 得分 95.5%、单任务成本 $0.12 → 已验证（来源：officechai.com、benchlm.ai 对 ARC Prize 官方数据的转述，与 @arcprize 原始推文一致）。对比高分模型 Fable 5（Max）与 GPT-5.6 Sol（Max），Gemini 3.7 Flash 分数接近但成本低出"数倍甚至数量级"，具体倍数第三方报道未给出精确数字，此处不做数字补全。

扩展影响：
行业解读普遍将其定位为"低成本 Agent 工作马"而非单纯的性能冠军——用可接受的分数换取数量级更低的调用成本，直接影响 Agent 类产品在推理阶段的模型选型逻辑（来源：nxcode.io、infoworld.com）。

对国内从业者的意义：
Gemini 系列在国内需通过代理访问，直接使用受限；但其"高性价比 Flash 模型做 Agent 工作马"的产品定位，是国内开源模型（Qwen、GLM、DeepSeek 系列）对标海外产品矩阵、制定分层定价策略时的一个直接参照对象。

延伸阅读：
- https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/
- https://www.infoworld.com/article/4209622/google-cuts-gemini-3-7-flash-prices-as-enterprise-ai-economics-diverge-and-pro-cadence-slows.html

---

## 2. 新产品 & 功能发布

- Grok Bot 企业版接入 — xAI

  核心能力：
  - 面向"一小部分企业"开放 Grok Bot 访问权限，本周末开始试点
  - 官方团队计划实地前往旧金山企业办公室协助上手，推文未提供更多技术细节

  链接：链接未提供
  立即试用优先级：观望
  理由：仅面向受邀企业开放，尚未公开注册入口，个人开发者暂时无法直接试用。

- Codex CLI 启动速度优化 — OpenAI

  核心能力：
  - 重写生命周期管理逻辑，`codex` 命令启动速度提升约 25 倍
  - 从"需要等待"变为"即时响应"

  链接：链接未提供
  立即试用优先级：今天就试
  理由：已在最新版本中生效，现有 Codex CLI 用户升级即可体验，零迁移成本。

- FreeToken — Berkeley AI Research 社区项目

  核心能力：
  - 使用官方权重、无需极端量化，在消费级 GPU 上跑前沿模型：Qwen3.6 35B 在 8GB RTX 4060 笔记本上可跑到 39 tok/s
  - DeepSeek-V4-Flash 284B 在 RTX 5090 桌面端跑到 22-25 tok/s，GLM-5.2 753B 在 RTX PRO 6000 工作站跑到 15 tok/s
  - 可直接接入 Claude Code、Codex 等编码工具

  链接：链接未提供
  立即试用优先级：本周内试
  理由：若推文所述基准属实，个人开发者可零 API 成本跑前沿级模型做编码任务，但推文未给出官方仓库直链，建议先小范围验证再全面切换。

- NVIDIA Nemotron-Labs-Teacher-Instruction-Following（550B） — NVIDIA

  核心能力：
  - 550B 参数教师模型，专攻指令遵循、约束满足、结构化输出与格式控制
  - 面向蒸馏与合成数据生成场景优化

  链接：https://huggingface.co/nvidia/NVIDIA-Nemotron-Labs-Teacher-Instruction-Following
  立即试用优先级：本周内试
  理由：已在 Hugging Face 开放下载，做数据蒸馏/合成数据管线的团队可直接接入测试。

- PRISM 文本到动作模型（1.4B） — Hugging Apps

  核心能力：
  - 支持按精确指令顺序生成人体动作序列（如"先走路，再坐下"）
  - 输出 SMPL-X 参数，可直接接入现有骨架绑定

  链接：https://hf.co/spaces/hugging-apps/prism-text-to-motion
  立即试用优先级：本周内试
  理由：Hugging Face Spaces 上有在线 Demo，做数字人/动画管线的团队可直接上手验证效果。

- Google Antigravity 远程控制 — Google

  核心能力：
  - 支持通过任意现代浏览器或 iOS/Android 移动端访问已启动的 Antigravity 会话
  - 面向 Ultra 订阅用户率先开放，逐步推广至全部用户

  链接：链接未提供
  立即试用优先级：本周内试
  理由：对已在用 Antigravity 做 Agent 编排的团队，移动端接入改变了"离开电脑就断线"的既有工作流。

---

## 3. 行业趋势 & 热议话题

- 开源模型在生产环境的 token 占比快速上升

  参与讨论的主要声音：@rauchg（Vercel CEO，数据来源方）、@ClementDelangue（Hugging Face CEO）、@berkeley_ai（转 @istoica05 评论）
  主流观点：Vercel AI Gateway 平台上开放权重模型的 token 占比从约两个月前的 28.4% 升至今日的 62%，闭源模型份额相应从 71.6% 降至 38%（来源：@rauchg，当事方口径，未经独立验证）；同一时段内，FreeToken 等工具让消费级 GPU 也能跑动前沿开源大模型（详见第 2 节），Berkeley AI Research 认为这从根本上改变了 AI 的成本结构。
  主要分歧：@ClementDelangue 断言"绝大多数 AI 负载最终会跑在开放模型上"，但这一预测仅代表 Hugging Face 一方立场，缺少独立数据源验证是否可推广到 Vercel Gateway 之外的场景。
  信号强度：中
  判断依据：三个不同机构（Vercel、Hugging Face、Berkeley AI Research）在同一 24 小时窗口内从不同角度指向同一现象，但核心数字来自单一平台，尚不能代表全行业口径。

- 公众舆论对 AI 大厂高管的负面情绪加剧，与实际使用率背离

  参与讨论的主要声音：@GaryMarcus（转 Financial Times、Futurism 报道）、@emollick（独立评论）
  主流观点：Financial Times 提出"Techlash"一词，称公众舆论、美国法院和国会正在转向对抗大科技公司；Futurism 援引一项针对 1000 名美国年轻人的调查称，多位科技高管的厌恶度甚至超过数据中心本身；Ethan Mollick 则指出另一层矛盾——民调显示大众整体厌恶 AI，但同时几乎所有人都在高频使用 AI，部分用户还会对自己常用的模型产生真实的情感依赖。
  主要分歧：Gary Marcus 引用的信源侧重强调"厌恶"这一面，Mollick 强调"言行不一"，两者对同一现象的解读侧重点不同。
  信号强度：中
  判断依据：两家权威媒体（FT、Futurism）加一位独立学者（Wharton 教授 Mollick）在同一窗口内各自独立提及同一主题，满足"至少 2 个独立来源且其中 1 个为权威媒体"的门槛。

---

## 4. 值得关注的洞察 & 观点

- @giffmana（Lucas Beyer，Meta 研究员，前 OpenAI/DeepMind）：

  「转述对本人一场题为《Vision in the Age of LLMs》讲座的整理：放弃自监督学习（SSL）路线的关键原因是，同等条件下"SSL + 少量标注样本"的效果远超纯 SSL，这条实验曲线让他把研究重心转向如何低成本获取标注数据并用好它们。」
  为什么值得关注：这是一位一线视觉大模型研究者对"数据路线选择"给出的具体、可复现实验依据，而不是空泛表态，该推文 engagement_rate 达到 1.57%，属于从业者高强度存档级别的信号。

- @giffmana（同上）：

  「关于数据过滤 vs 数据选择的区分：能明显判断是垃圾的数据（如 unknown.jpg）该过滤没问题，但很多看起来像垃圾的数据其实不是（如 2012-03-21.jpg）。除非算力不够训不完全部数据、或不想要一个通用模型，否则任何"更聪明"的过滤都该被当作数据选择而非过滤来对待。」
  为什么值得关注：这是对预训练数据处理中一个容易被混淆的方法论问题的精确澄清，反直觉之处在于它反对业内默认的"过滤等于清洗数据"思路，主张过滤本质上是一种选择偏差，需要被显式对待。

- @addyosmani（前 Google Chrome/Gemini 工程与开发者关系负责人）：

  「"i really don't want to use your agent, i want to use my agent to use your thing."（我不想用你的 Agent，我想用我自己的 Agent 去用你的产品。）」
  为什么值得关注：这句话点出了当前 Agent 生态的真实张力——各家都想做"入口级 Agent"，但开发者真正想要的是可控的个人 Agent 加开放的被调用接口，而非被锁死在某个厂商的 Agent 界面里，这与几乎所有 SaaS 厂商正在推的"内置 Agent"策略方向相反。

- @jeremyphoward（fast.ai 联合创始人）：

  「针对某类检索/embedding 服务大幅降价（推文提及"1400x cheaper"，具体降价对象未在推文中说明）的回应：仍会继续用 embeddings（dense、sparse、multi-vector）加混合检索（含 bm25）和 reranker，甚至可能开始用 listwise cross-encoder。」
  为什么值得关注：在检索成本骤降的情况下，一位有大规模工程实践经验的从业者仍认为传统检索栈值得坚持，是对"降价即颠覆现有架构"这类简单叙事的一个反例。

- @GaryMarcus（AI 批评者，曾在美国参议院作证，AVERI 创始人）：

  「在《卫报》撰文回应"Pacing the Frontier"联名信（多家 AI 公司员工联署，呼吁政府介入行业节奏管控），提出企业当下就能做、不必等监管的 4 件事：1）对各公司做审计试点；2）主动参与/建立跨行业治理机构、共享安全经验；3）投资可用于对华核查"减速协议"是否被遵守的技术手段；4）推动为关键治理机构建立法律基础的立法。」
  为什么值得关注：这不是泛泛的监管呼吁，而是给出了企业方在没有强制监管的情况下今天就能落地的具体动作清单，并明确点出了对华技术核查这一容易被忽略的维度。

---

## 5. 实用资源 & 教程

- QWM（Q-Learning with World Models） — Physical Intelligence / Stanford（Chelsea Finn 团队）

  类型：论文
  用途：将世界模型与强化学习微调结合，试图同时获得世界模型的样本效率与 RL 微调突破预训练能力上限的优势
  链接：链接未提供（推文为系列串第 1/7 条，未给出论文/代码直链）
  上手难度：高

- RankBALD — Mila / COLM 2026

  类型：论文 + 开源代码
  用途：用贝叶斯主动学习减少模型评测所需的基准题目数量，聚焦"排序是否正确"而非"绝对分数是否精确"；在 2802 个模型-基准组合上验证，10 题预算下排序误差从 46.9 降至 35.3
  链接：https://github.com/bonaventuredossou/al_rankbald
  上手难度：中

- Physics of Agents 可视化站点 — Stanford AI Lab

  类型：工具 / 演示项目
  用途：可视化多智能体实验中 Agent 之间的实际对话内容与社会动态
  链接：https://batu-el.github.io/physics-of-agents/
  上手难度：低

- Measuring Agents in Production（ICML 2026 Oral） — Berkeley AI Research

  类型：论文 / 演讲视频
  用途：探讨生产环境中衡量 Agent 表现这一尚未被充分研究的方向
  链接：https://icml.cc/virtual/2026/oral/71172
  上手难度：中

- AI 辅助扫描美国法律条文中的过时歧视性条款 — Stanford RegLab

  类型：其他（应用案例，Washington Post 专栏文章）
  用途：用 AI 处理超过 30 亿字的美国地方法律条文，找出仍存在的种族隔离学校、人头税、限制女性投票权等已失效但未被正式废除的条款
  链接：https://www.washingtonpost.com/opinions/2026/08/19/us-legal-code-is-more-than-3-billion-words-ai-read-them-all/
  上手难度：低（阅读案例，非工具本身）

---

## 一句话总结

今天最大的变化是价格：OpenAI 把 GPT-5.6 Sol 降价超 20%，Gemini 3.7 Flash 用远低于顶级模型的单任务成本追平其 ARC-AGI 分数，两条线同时把"性价比"重新推回模型选型的第一位。与此同时，Vercel 数据显示生产环境里开源模型的 token 占比两个月内从 28.4% 升到 62%，而 NVIDIA 一边把 Vera Rubin 满产铺给八大海外云厂商，一边把原本面向中国的产能转向了这条新产线。

---

## 今日行动建议

今天（30 分钟内）：
基于 OpenAI GPT-5.6 Sol 降价——在现有 API 面板里用同一任务跑一次 GPT-5.6 Sol 与当前主力模型的对比，记录延迟、输出质量与实际每千 token 成本三行笔记。

本周内：
基于"FreeToken 消费级 GPU 跑前沿模型"与"开源模型 token 占比两个月内从 28.4% 升到 62%（Vercel AI Gateway）"——为团队现有 Agent/编码工作流做一页竞品评估，对比继续使用闭源 API 与切换部分任务到本地/开源模型（如 Qwen3.6、DeepSeek-V4-Flash、GLM-5.2）在成本和延迟上的实际差异，产出一页决策备忘录。

月内验证：
基于"NVIDIA Vera Rubin 满产但同步收缩中国产能"——持续跟踪国内云厂商（阿里云、腾讯云、字节火山引擎等）是否公布新一代自研芯片或对海外算力代差的应对路线图，作为判断算力代差是否扩大的观察指标。

---

## 传播力素材

- "Claude, the AI model, is named after Claude Shannon, the mathematician who laid the foundation for the digital world we rely on today."（整条 thread 回顾了香农生平，以及信息论如何演变为今天的 cross-entropy loss、perplexity 等 AI 基础概念） — @techNmak（经 @elonmusk 转发）· 👍9632 👁773120 · engagement_rate 0.45%
  改写方向：适合科普向自媒体（知乎/小红书/公众号）做"AI 你不知道的历史"系列，可拆成信息论→熵→交叉熵损失函数的知识科普贴。
  点评：把香农生平和"AI 术语溯源"结合是很讨喜的科普角度，容易引发转发；局限在于这是三手科普整理而非权威一手来源，"Claude 模型命名"这个钩子容易让读者误以为整条 thread 的所有历史细节都已被严格核实，改写时建议标注为科普整理而非权威考据。

- "the same architecture that makes grok bot useful is what makes it dangerous to configure casually... keep irreversible actions behind human approval: sending, publishing, spending and production changes" — @monokern（经 @elonmusk 转发）· 👍1410 👁718615 · engagement_rate 0.23%
  改写方向：适合面向企业 IT/安全团队的技术公众号，改写成"多 Agent 系统权限设计 checklist"。
  点评：把"多个 Agent 共享同一持久化环境"类比为"一次登录变成了基础设施"，抓住了当前 Agent 编排产品共同的安全盲区，"不可逆操作必须人工审批"这类建议具体可执行；局限是内容基于单一产品的个人使用体验，尚未验证是否适用于其他 Agent 编排框架。

- "add a self-check pass before it returns anything... define 'DONE' explicitly... force structured output... scope tool access per task, not globally" — @deezzex（经 @elonmusk 转发）· 👍1329 👁601043 · engagement_rate 0.26%
  改写方向：适合做成"Agent Prompt 工程四条军规"类型的信息图或短视频脚本。
  点评：四条建议（自检、明确"完成"定义、结构化输出、按任务分权限）都具体可执行，符合高收藏率内容的特征；局限是账号背景信息不明，改写时不宜包装成"官方最佳实践"，只作为个人经验分享处理。

- "How hard could it possibly be to predict the next token" — @ericmitchellai（OpenAI post-training 研究员）· 👍339 👁53245 · engagement_rate 0.01%
  改写方向：适合作为技术类推文/短视频的开场梗，吐槽"预测下一个词"这个听起来简单的任务如何催生了整个大模型行业。
  点评：来自 OpenAI 内部研究人员的自嘲式反讽，梗的杀伤力建立在读者已理解 next token prediction 背后的复杂度，脱离语境单独传播容易变成没头没脑的一句话，改写时建议保留身份背景标注。

- "The operating system can become another surface your agents can help you modify." — @tobi（Shopify CEO，转发 Omarchy 相关内容并评论）· 👍518 👁30576 · engagement_rate 0.71%
  改写方向：适合桌面工具/开发者生产力类自媒体，作为"AI agent 正在从应用层下沉到操作系统层"的话题引子。
  点评：把操作系统重新定义为"可被 agent 修改的界面"是个有延展性的框架；局限是论据来自个人切换 Linux 发行版的一次性体验，还不构成可推广的产品趋势，改写时不宜直接当作行业结论使用。

- "Not even a year ago, 10B tokens in a year was a big achievement and got you a plaque. Now I do >10B tokens a week."（@gdb 转评："agentic adoption has been super fast, easy to forget how far the field has come"） — @xeophon，@gdb 转评 · 👍546 👁45942 · engagement_rate 0.09%
  改写方向：适合做成"AI token 消耗量级对比"类型的数据可视化内容，直观展示 agentic 工作流的用量爆发。
  点评："年度里程碑"变成"周度日常"的对比很有冲击力，能直观传达 agentic 采用速度；局限是这是单一开发者的个人用量，不代表行业平均水平，也未说明具体任务类型，读者容易把个例误当成普遍现象。

---

## 信号 / 噪音比

进入第 1 节的有效新闻 3 条，进入第 2-5 节的有效信号约 19 条（产品 6 条、趋势 2 条、洞察 5 条、资源 5 条，此外传播力素材回捞 6 条），合计约 28 条内容进入本期简报；抓取到的 116 条推文中，约 76% 为与 AI 行业无关的噪音，主要集中在 @elonmusk（41 条中仅约 5 条与 AI 行业相关，其余为美国政治站队、Tesla FSD 车评、个人生活内容）与 @ylecun（5 条均为政治类转发，0 条与 AI 行业直接相关）两个账号。今日整体信号密度：正常。

**本期信源**：@sama @OpenAI @sherwinwu @gdb @satyanadella @nvidia @sundarpichai @arcprize @mntruell @berkeley_ai @huggingface @HuggingApps @NotionHQ @ClementDelangue @rauchg @istoica05 @GaryMarcus @emollick @giffmana @addyosmani @jeremyphoward @chelseabfinn @hugo_larochelle @StanfordAILab @StanfordHAI @tobi @elonmusk @techNmak @monokern @deezzex @ericmitchellai @xeophon（共 31 位）
