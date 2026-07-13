# AI 行业情报简报 | 2026-07-14

> 数据窗口：2026-07-13 06:00 — 2026-07-14 06:00（北京时间，过去 `24 小时`）
> 深度分析：6 条 | 模板版本：v2.3

---

## 1. 重大新闻 & 突发事件

- **OpenAI Codex + ChatGPT Work 突破 7M 活跃用户，GPT-5.6 Sol 确认保留在订阅**

  来源：@thsottiaux（Codex & ChatGPT @OpenAI） · 约 4 小时前；@sama 转发确认
  关键数字：7M 活跃用户（来源：@thsottiaux，当事方口径，未经独立验证）；所有用户获得额外使用配额补充
  行业影响：7M 这一数字验证了 agentic 工作流已从"演示阶段"进入大规模日常使用。同时，@thsottiaux 明确承诺"GPT-5.6 Sol 将在你付费的 ChatGPT 订阅中保留，至少到下一个更好的模型发布"，这条声明直接平息了过去 48 小时用户担心被强制降级的担忧，对订阅续费决策有即时影响。

- **Grok Build 数据安全风波：Musk 宣布删除所有 SpaceXAI 历史用户数据**

  来源：@elonmusk · 约 3 小时前；@SpaceXAI · @milichab（@xai）同步澄清
  关键数字：无可核实数字
  行业影响：用户发现 SpaceXAI ZDR（零数据保留）条款细则中仍有数据保留条款，引发争议。Musk 随即承诺"此前上传到 SpaceXAI 的所有用户数据将被完全彻底删除"。@milichab 解释 `/privacy` 命令可切换状态且溯及删除。此事件说明企业级 AI coding 工具的数据合规条款正在受到高强度公众审查，ZDR 能力已成为 B2B 采购的关键门槛——@AravSrinivas 明确表示 Perplexity 选择集成 Grok 4.5 的两大原因之一正是 ZDR 从一开始就可用。

- **Richard Sutton 离开 Keen Technologies，成立 Oak Lab，公开批评深度学习"积弱低效"**

  来源：@RichardSSutton（Richard Sutton，Turing Award 得主，RL 奠基人） · 约 8 小时前
  关键数字：无
  行业影响：Sutton 与 Khurram Javed 从 John Carmack 的 Keen Technologies 独立出来，成立 Oak Lab，方向是"从运行时经验中创造和维持智能"。最具分量的判断是他的直接表态："当前深度学习方法积弱低效，需要的不是更多调整，而是全新基础性想法和彻底重构，才能为 AI 的雄心目标提供坚实基础。"这不是网红发言，这是 RL 领域最重要的奠基者之一在打出新旗帜。

- **Anthropic Claude 限额政策引发知名从业者强烈批评**

  来源：@omarsar0（elvis）原推；@jeremyphoward（Fast.AI 联创）转发并批评 · 约 24 小时前；@GaryMarcus 表示已切换到免费 Gemini
  关键数字：无
  行业影响：@jeremyphoward 直言"Anthropic 没有意识到这些变化对用户有多破坏性，请停止玩游戏——要么把它放进订阅，要么放进 API"。三个独立的高可信来源在同一时间窗口表达了相同指向，已构成趋势信号。对于当前付费 Claude 用户，切换摩擦成本正在降低。

- **Meta Muse Spark 1.1：Debate Benchmark 全球第三，医疗 RadLE-H 排名第一**

  来源：@alexandr_wang（Meta Chief AI Officer，Scale AI 创始人） · 约 3-6 小时前；@LechMazur（16 个 LLM 基准维护者）；@DrDatta_AIIMS（RadLE-H 测试创建方）
  关键数字：Debate Benchmark 1688 分，第三位，仅次于 Fable 5 和 Opus 4.7（来源：@LechMazur）；RadLE-H 48.5，第一位，人类专家基线 52.0（来源：@DrDatta_AIIMS，测试方口径）
  行业影响：Meta 重新以有竞争力的分数进入前沿模型视野。医疗 AI 赛道的 Handover Readiness Index（判断 AI 何时应该交接给专家）排名第一，说明 Muse Spark 1.1 在特定高风险应用场景的可控性上有特殊优化。

- **ChatGPT 重返 WhatsApp EEA 市场，同步上线 Kakao（韩国）和 Viber**

  来源：@ChatGPTapp / @OpenAI 官方 · 约 8 小时前
  关键数字：无
  行业影响：EEA（欧洲经济区）是全球监管最严格的市场之一，此次重回意味着 OpenAI 在欧洲监管合规上取得阶段性突破。同步进入 Kakao（韩国主导即时通讯）说明 OpenAI 加速本土化渗透策略，把 ChatGPT 植入用户已有的高频使用 app，而非要求用户切换到新 app。

---

## TOP 新闻深挖

#### 深挖：OpenAI Codex + ChatGPT Work 7M 活跃用户 & GPT-5.6 Sol 订阅保留

背景补充：
@thsottiaux 同一时间发出两条推文，分别宣布 7M 里程碑和 Sol 订阅保留。前者附带对所有账户的使用配额补充，后者给出明确时间条件"at least until we ship an even better model"。Sam Altman 转发两条并附文"we love our users"和"clarity is nice"，这在风格上属于 OpenAI 应对用户不满时的公开表态模式。@gdb（Greg Brockman）当天同步发布多条 Codex/Sol 使用案例（客户发现、网页设计、电脑控制），属于密集产品宣传节奏。

数字核实：
7M 活跃用户 → 当事方口径（@thsottiaux，@OpenAI），未经独立验证；经本轮深挖尝试外部搜索，因非交互生成环境限制未能获取第三方核实数据。

扩展影响：
Sol 订阅保留承诺发出后，当天 timeline 中出现多个用户分享 Sol 和 Codex 完成实际工作任务的案例：@emollick 报告 Codex PC 端计算机使用能力在 Slay the Spire 2 上连续工作 5 小时并赢得胜利；@gdb 分享调试笔记本电源问题的真实用例。这些案例集中出现于承诺后数小时，属于协同宣传节奏而非自然流量。

对国内从业者的意义：
GPT-5.6 Sol 确认留在订阅，意味着通过 ChatGPT Plus/Pro 订阅访问旗舰模型的路径在短期内稳定。国内使用 OpenAI API 的团队需注意：Sol 的订阅保留承诺与 API 定价是两套体系，API 成本依然是主要约束。

延伸阅读：暂无高可信外部链接

---

#### 深挖：Grok Build 数据安全风波

背景补充：
来源已充分，背景核实跳过。事件链：用户 @RomanGuy20 发现 SpaceXAI ZDR 细则存在保留条款 → Elon Musk 引用该推文并明确承诺删除历史数据 → @SpaceXAI 官方发声明解释 ZDR 机制 → @milichab（xAI 员工）详细说明 `/privacy` 命令的技术实现 → Elon Musk 再次转推 milichab 的解释，补充说明 CLI 在 ZDR 模式下的行为。整个事件从用户发现到官方完整响应大约在 2-3 小时内完成，响应速度快。

数字核实：
无具体数字需核实。

扩展影响：
@AravSrinivas（Perplexity CEO）在风波期间主动表态，称 Perplexity 集成 Grok 4.5 的两大原因之一正是"ZDR 从第一天就可用，这是我们客户的需求"。这一声明强化了 ZDR 在 B2B 市场的硬性门槛地位，对 OpenAI 和 Anthropic 的企业产品线构成间接压力——两者的数据策略同样将面临对标。

对国内从业者的意义：
国内部署环境中数据本地化和零数据保留是企业合规的核心要求，Grok Build 此次风波展示的快速响应机制（用户发现 → 承诺删除 → CLI 命令实现 → 官方确认，2-3 小时内闭环）是产品数据治理值得参考的案例。对出海产品而言，合规响应速度本身也是竞争力的一部分。

---

#### 深挖：Richard Sutton 成立 Oak Lab，批评深度学习基础

背景补充：
@RichardSSutton 原推明确提到与 Khurram Javed 共同离开 Keen，在保留"强化学习"和"从运行时经验创造智能"这两个核心方向的同时，与 Keen 走了"稍微不同的路"。Oak Lab 的方向暗示 Sutton 认为当前神经网络范式（包括 LLM）在实现智能的更宏大目标上存在根本性局限，需要的不是更多工程优化而是理论突破。Gary Marcus 援引此推文，称之为"Seismic"，并指出这印证了他自 2018 年《深度学习：批判性审视》以来持续主张的立场——具有讽刺意义的是，LeCun 当年称该论文"大部分是错的"。经本轮深挖尝试外部搜索，因非交互生成环境限制未能获取 Oak Lab 官网或更多背景信息。

数字核实：
无可核实具体数字。

扩展影响：
暂无有效补充。但从行业格局看，2026 年已有多家新创公司在 Keen 系（ex-DeepMind、ex-Atari 研究人员）路线上布局，Sutton 此次独立可能吸引一批认同"当前 LLM 路线不够用"的研究人员和投资人聚合到 Oak Lab 旗帜下。

对国内从业者的意义：
短期内无直接影响。中期来看，如果 Oak Lab 的路线产生可落地的新框架，将影响模型架构研究方向。国内有基础研究能力的团队值得持续跟踪 Oak Lab 的论文输出。

---

## 2. 新产品 & 功能发布

- **HuggingFace Transformers + vLLM 原生速度集成** — Hugging Face

  核心能力：
  - Transformers 模型现在可直接在 vLLM 中以原生速度运行，无需再单独为 vLLM 手写实现
  - 基准测试显示在 4B 至 235B 参数（含 tensor parallel 和 MoE 配置）上匹配或超过手写实现
  - 一个模型实现可同时覆盖训练、微调、评估、RL rollout 和生产推理

  链接：https://huggingface.co/blog/native-speed-vllm-transformers-backend
  立即试用优先级：本周内试
  理由：消除了架构新模型时"在 Transformers 实现一遍、在 vLLM 再实现一遍"的重复工作，对有自定义模型推理需求的团队直接节省工程成本。

- **Grok 4.5 进入 Perplexity Computer harness** — Perplexity AI

  核心能力：
  - Grok 4.5 作为 Perplexity Computer（AI 控制计算机）的推理模型
  - 选择依据：在 Perplexity 内部 eval 上得分最高且成本效益最佳，ZDR 从上线首日即可用
  - 集成完成时间为数小时（来源：@AravSrinivas，当事方口径）

  链接：链接未提供
  立即试用优先级：今天就试
  理由：Grok 4.5 官方对比数据显示在 SWE-Atlas-QnA 基准上领先（[未经独立验证]），有 Perplexity 订阅的用户可直接在现有 harness 下对比效果。

- **OpenAI Codex PC 端计算机使用能力（Computer Use）显著提升** — OpenAI

  核心能力：
  - PC 端 computer use 能力大幅提升（来源：@emollick，Wharton 教授，实测报告）
  - 在未知随机条件的 Slay the Spire 2 每日挑战中，持续运行 5 小时并取得胜利
  - 体感描述："像是一个无躯体的智能在用鼠标和键盘工作"

  链接：链接未提供
  立即试用优先级：本周内试
  理由：Codex computer use 相比代码执行更接近真实工作流，能测试桌面自动化潜力。

- **HuggingFace ZeroGPU 向所有用户开放** — Hugging Face

  核心能力：
  - ZeroGPU demo 创建权限从受邀用户扩展到全体 HuggingFace 用户
  - 可通过 agent 指令直接创建：`"Build a HF ZeroGPU demo for this model"`

  链接：https://huggingface.co/new-space
  立即试用优先级：今天就试
  理由：有免费 GPU 配额，5 分钟可创建可分享的模型 demo，直接影响模型展示和原型验证工作流。

- **Notion Calendar AI agent 整合** — Notion

  核心能力：
  - 桌面端日历操作新增交互式富文本 UI
  - agent 可执行日历查询和快速操作（如跳转会议链接）而无需离开对话界面

  链接：链接未提供
  立即试用优先级：观望
  理由：功能点不大，但 Notion 作为知识库 + 日历 + agent 的整合平台叙事正在成型，是中期趋势的早期信号。

- **Perplexity Computer 多账户切换** — Perplexity AI

  核心能力：
  - Mac App 新增账户切换功能，类似 Gmail 多账户模式
  - 支持侧边栏快速切换或账户管理

  链接：链接未提供
  立即试用优先级：观望
  理由：功能实用但属于体验优化，对多账户工作流有即时价值。

- **Grok Build v0.2.99 键盘工作流优化** — xAI

  核心能力：
  - Agent Dashboard 支持多行输入
  - PageUp/PageDown 在 prompt 聚焦时滚动对话
  - Keyboard Shortcuts modal 支持 Vim 模式导航键

  链接：链接未提供
  立即试用优先级：观望
  理由：轻量更新，对重度键盘用户有体验改善。

---

## 3. 行业趋势 & 热议话题

- **AI coding 工具竞争加速：Grok Build、Codex Work、Claude Code 三方同时加码**

  参与讨论的主要声音：@elonmusk、@AravSrinivas、@gdb、@jeremyphoward、@emollick、@GaryMarcus
  主流观点：Grok Build 在增长速度和基准上主动挑战 Claude Code；Codex 强调 agent 跨设备持续运行和 computer use；Claude Code 正面临限额政策引发的用户流失风险。三个工具正在快速从"代码补全"演变为"agentic 工作站"，比拼维度不再只是补全质量，而是 agent 持久化、background 任务、多设备接力和数据安全。
  主要分歧：基准排名争议持续（SWE-Atlas-QnA 上 Grok 4.5 宣称 #1，但来源为非官方追踪账号；Codex 通过 Design Arena 等多个用户导向基准建立存在感），不同基准侧重不同能力，结论依赖于任务类型。
  信号强度：强
  判断依据：三个来自不同公司的产品在同一时间窗口均有实质动作（发布/宣传/批评），且多个独立用户账户报告真实工作流切换，构成趋势而非单点噪音。

- **AI 推理成本下降与基础设施利润再分配**

  参与讨论的主要声音：@GavinSBaker（Artisan Capital 合伙人，被 @elonmusk 转推，2222 书签）、@AravSrinivas
  主流观点：Gavin Baker 提出：如果市场份额从 90%+ 毛利率的前沿实验室向开源或低成本模型转移，推理成本降低将增加终端客户 ROI，推动 token 需求增量，利润从模型层向基础设施层流动。Jensen 着力推动开源，部分动机可能是加速这一再分配。@AravSrinivas 提出 AI 数据中心推理的能源瓶颈有两条出路：本地模型分流 token 流量，或太空太阳能数据中心。
  信号强度：中
  判断依据：两个独立来源从不同角度（利润结构、能源约束）指向同一方向：inference cost 是 AI 行业的核心压力点，当前格局尚未稳定。但具体走向仍取决于开源模型质量提升速度，数字预期不明确。

---

## 4. 值得关注的洞察 & 观点

- @GavinSBaker（Artisan Capital 合伙人）：

  「The mega bull case for AI infrastructure would be *if* market share shifted away from certain frontier labs with 90%+ inference margins toward cheaper models... Margin dollars would effectively get redistributed from the frontier labs to AI infrastructure providers. The infra winners would be those with the lowest per token cost and the winners at the model layer would be those with the highest token efficiency.」
  为什么值得关注：这是从资本角度给出的 AI 产业链利润流向预判框架，2222 个书签说明从业者在存档。前提条件是"如果市场份额转移"，当前这一转移"尚未发生"，Gavin 本人也加了这个限定。

- @andrewchen（a16z 合伙人，被 @ClementDelangue 转推）：

  「consumer grade graphics cards will be running Fable-equivalent models by 2029... 'Densing Law' found capability-per-parameter doubles every ~3.3 months.」
  为什么值得关注：这是基于"Densing Law"（每 3.3 个月模型能力/参数效率翻倍）的外推，结论是 consumer GPU 可能在 2028-29 年运行 Fable-equivalent 模型。作者承认可能存在渐近线，且视频等多模态数据对这一压缩比的挑战尚未解决，这个预测是乐观场景而非基准场景。

- @emollick（Wharton 教授，AI 研究）：

  「I think OpenRouter is not a good measure of actual model usage in a world of agentic tools... We really need better data indicators for AI!」
  为什么值得关注：OpenRouter token 数据显示中国开源模型使用量飙升至美国企业约 50%，但 @emollick 指出这可能是使用向 Codex/Claude Code 等 agentic 工具迁移的假象，而非真正的模型选择偏好转变。这是一个对常被引用的行业数据的方法论质疑，提示需要更好的 agentic 时代 AI 使用指标。

- @RichardSocher（CEO @recursive_si @youdotcom，前 Salesforce Chief Scientist）：

  「A huge chunk of the economy just does not require that much intelligence and won't materially change at its core with intelligence being abundant and cheap, eg. tourism, real estate, luxury goods, food supply chain, sports...」
  为什么值得关注：这是对 AI 尚未大幅拉动 GDP 的结构性解释——并非技术局限，而是相当大部分的经济活动（旅游、奢侈品、农业、体育等）本身不依赖智能密集的工作。对创业者的含义是：在上述行业找 AI 应用时，问题不是能力够不够，而是这些行业的核心价值创造链条中智能需求本来就有限。

---

## 5. 实用资源 & 教程

- **Codex first-customer-finder skill**

  类型：开源工具 / Codex skill
  用途：分析创业公司并从公开信号中找到潜在第一批客户，输出 HTML 报告和个性化外联开场白
  链接：`npx --yes codex-first-customer-finder-skill`（@Kappaemme1926 开源，@gdb 转发，2857 书签，engagement_rate 0.0082）
  上手难度：低

- **Morpheus — 持续强化学习大世界基准**

  类型：开源基准 / 论文
  用途：提供永不重置的企业仿真环境，测试 AI 在动态、持续变化任务中的表现（而非 Atari/MuJoCo 这类周期性小世界）；测试结果：当前前沿 LLM 不是持续学习者
  链接：https://morpheus.skyfall.ai/（论文：https://openreview.net/pdf?id=31P1VAfLkJ）
  上手难度：中

- **LLM-as-a-Verifier — 验证作为第四 scaling 轴**

  类型：论文 + 开源框架
  用途：用 LLM 作通用验证器，通过更细粒度评分、重复评估和标准分解来提升验证效果；在机器人、编程（SWE-Bench Verified）、医疗 AI（MedAgentBench）等多领域达到 SOTA
  链接：https://llm-as-a-verifier.com/（代码：https://github.com/llm-as-a-verifier/llm-as-a-verifier；论文：https://arxiv.org/abs/2607.05391）
  上手难度：中

- **Smart Cellular Bricks — 去中心化形状识别与自修复物理模块**

  类型：论文（Nature Communications）
  用途：每块砖运行同一小型神经网络，仅与直接邻居通信，集体收敛到正确全局形状；故障容忍 15%，损伤方向预测准确率 95%，首次物理实现大规模去中心化 3D 自识别
  链接：https://sakana.ai/smart-cellular-bricks（论文：https://www.nature.com/articles/s41467-026-75166-7）
  上手难度：高（研究阶段）

- **atp（Adaptive Transport Protocol）— 基于 fountain codes 的高性能文件传输**

  类型：开源工具
  用途：基于 RaptorQ fountain codes（RFC 6330）的文件传输，在 10% 丢包率下仍比 rsync 快 1.9×，支持多机并行 bonding；含 agent 适配的安装 skill
  链接：`curl -fsSL https://raw.githubusercontent.com/Dicklesworthstone/atp/main/install.sh | bash`（John Carmack 推荐，engagement_rate 0.0037）
  上手难度：低（一键安装）

- **NotebookLM 20 个学习提示**

  类型：教程
  用途：帮助用户更深度地在 NotebookLM 中学习研究论文，包含 20 个预设提示
  链接：链接未提供（来源：@MIT_CSAIL，engagement_rate 0.0112，小众高精准信号）
  上手难度：低

---

## 传播力素材（适合自媒体改写的高互动 AI 观点）

- 「The mega bull case for AI infrastructure would be *if* market share shifted away from certain frontier labs with 90%+ inference margins toward cheaper models...」 — @GavinSBaker · 👍 4749 👁 2126797 · engagement_rate 0.10%
  改写方向：适合微信/小红书的 AI 投资视角长文，或"谁会是 AI 时代真正的赢家"主题讨论
  点评：这条推文给出了一个思考 AI 产业利润分布的清晰框架：高利润前沿模型 vs. 低成本基础设施的博弈。引发共鸣是因为它道出了很多人隐约感受到但没有系统化表达的判断。局限在于"if"这个前提：市场份额是否真的会从前沿模型转移仍不确定，且 Gavin 本人也说"这还没发生"。只看这句话容易误以为"前沿实验室的利润时代要结束了"——但他的结论要保守得多。

- 「The process of trying, failing, updating a mental model, and trying again is the core of intelligence. We should celebrate models that fail gracefully and adapt instantly.」 — @fchollet · 👍 1199 👁 62928 · engagement_rate 0.33%
  改写方向：适合 AI 产品哲学类文章，或 agent 设计原则讨论
  点评：François Chollet（ARC-AGI 创始人，Keras 作者）从认知角度定义"真正的智能"，有充分的技术背景支撑这个判断——他整个职业生涯都在研究什么是 LLM 做不到的智能。引发共鸣是因为它暗合当前 AI 系统"成功率高但不会从失败中学习"的真实局限。但"fail gracefully"本身是个难以量化的要求，只看这句话可能被误读成"多犯错就是更智能"。

- 「current deep learning methods are weak and inefficient, and need not more tweaks, but fundamentally new ideas and a thorough reworking before they can provide a solid foundation for achieving the more ambitious goals of AI」 — @RichardSSutton · 👍 1562 👁 [来自原推] · engagement_rate [原推未入样本]
  改写方向：适合"AI 行业自我质疑"主题，或 RL vs. LLM 路线争论
  点评：说这话的不是 AI 悲观主义者，而是强化学习领域最重要的奠基者——这是判断力的关键前提。引发共鸣是因为它道出了很多人对当前 scaling 路线隐藏的不确定感。局限在于 Sutton 本人的新路线（Oak Lab）尚未产出任何成果，批评现有范式不等于新范式已经成立；且他的判断针对的是"更宏大的 AI 目标"，而非 LLM 在当前应用场景的实用价值。

- 「I don't think Anthropic realizes how disruptive these changes are to users. I appreciate the extension, but please stop playing games. Either keep it under the subscriptions or put it under the API already.」 — @jeremyphoward（转推 @omarsar0）· 👍 6233 👁 374846 · engagement_rate 0.05%
  改写方向：适合"AI 订阅制产品的用户权益"话题，或 Anthropic vs. 竞品对比讨论
  点评：Jeremy Howard（fast.ai 联创，机器学习社区重要声音）的不满代表了一类核心用户——重度依赖 API 和订阅的开发者。引发共鸣是因为限额不透明是很多 Claude 用户的真实痛点。局限在于这条推文发出的具体背景（针对哪一项限额政策变化）在数据中不完全清晰，且 Anthropic 是否确实做出了承诺保留或延期的回应也需要进一步核实。

---

## 信号 / 噪音比

进入第 1 节的有效新闻 6 条，进入第 2-5 节的有效信号 22 条，剩余约 52% 为低价值或噪音（主要来自 Elon Musk 的非 AI 转推、motorsport 内容、非 AI 时评、以及无法分析内容在视频/图片中的推文）。今日整体信号密度：正常。

**本期信源**：@GavinSBaker @elonmusk @milichab @SpaceXAI @AravSrinivas @thsottiaux @sama @gdb @jeremyphoward @omarsar0 @GaryMarcus @RichardSSutton @alexandr_wang @LechMazur @DrDatta_AIIMS @ChatGPTapp @OpenAI @ClementDelangue @emollick @fchollet @hardmaru @RichardSocher @StanfordAILab @huggingface @ID_AA_Carmack @andrewchen @MIT_CSAIL @NotionCalendar（共 28 位）

---

## 一句话总结

今日最密集的信号来自三个方向同时爆发：OpenAI 以 Codex 7M 用户和 Sol 订阅保留承诺稳住了付费基础；Grok Build 在流量增长和基准上主动出击，同时因隐私细则爆出公关危机；RL 奠基人 Richard Sutton 公开与当前深度学习路线切割，成立 Oak Lab，这是近年来学术权威对主流范式发出的最直接挑战。Anthropic Claude 正面临限额透明度压力，用户迁移摩擦在下降。

---

## 今日行动建议

今天（30 分钟内）：
基于「HuggingFace Transformers + vLLM 原生速度集成」——如果团队有自定义模型需 vLLM 部署，今天读 https://huggingface.co/blog/native-speed-vllm-transformers-backend，评估是否可以省去维护独立 vLLM 实现的工程成本。

本周内：
基于「Codex + ChatGPT Work 7M 活跃用户 & Sol 订阅保留」——如果团队当前在 Claude Code 和 Codex 之间有取舍，本周做一次直接对比测试：选 3 个真实工作任务，分别在 Codex Work（agentic 模式）和 Claude Code 上跑，记录完成质量、耗时和成本，输出一页内部对比备忘录，在当前 Claude 限额政策不透明的背景下做出有数据支撑的选择。

月内验证：
基于「Richard Sutton 成立 Oak Lab，批评深度学习基础」——持续跟踪 Oak Lab 的论文和技术博客输出，衡量指标：1）Oak Lab 是否在 30 天内发布预印本或技术报告；2）是否有来自 DeepMind/OpenAI 等顶级实验室的研究人员跟进表态；3）GitHub 和 ArXiv 上"continual learning + reinforcement learning + non-deep-learning"相关论文的引用热度变化。
