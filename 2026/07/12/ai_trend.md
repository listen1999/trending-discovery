# AI 行业情报简报 | 2026-07-12

> 数据窗口：2026-07-11 06:00 — 2026-07-12 06:00（北京时间，过去 `24 小时`）
> 深度分析：3 条 | 模板版本：v2.3

---

## 1. 重大新闻 & 突发事件

- **GPT-5.6 Sol/Luna/Terra 家族正式发布：医疗超越医生、50 年数学猜想证明、25 倍降本**

  来源：@OpenAI 官号 · 约 22 小时前；@gdb（Greg Brockman，OpenAI 联合创始人）；@thekaransinghal（OpenAI Health AI）；@polynoamial（Noam Brown，OpenAI 研究员）
  关键数字：Luna 在最低推理配置下超越 GPT-5.5 最高推理配置，成本降低 25 倍（来源：@OpenAI，当事方口径，未经独立验证）；医生在 Sol 回复中发现的缺陷少于自写回复，覆盖 20,000 个评分维度（来源：@thekaransinghal，当事方口径，未经独立验证）；Sol Ultra 证明一项 50 年未解数学猜想（来源：@polynoamial/Noam Brown，当事方相关，具体猜想名未披露）
  行业影响：三个变体中 Sol 和 Luna 同时 Pareto 优于 Terra（@ArtificialAnlys 独立评测）；Luna 成为当前 cost-per-task 最优解，直接压缩同价位竞品空间；医疗和数学突破打开了两类高价值垂直部署的商业说服路径。

- **Apple 正式起诉 OpenAI，指控系统性硬件商业机密盗窃**

  来源：Apple 诉状，经 @aakashgupta（详细分析线程，7654 点赞）引述；@ZeffMax（Wired 记者）；@elonmusk 转发评论
  关键数字：超 400 名前 Apple 员工目前在 OpenAI 任职（来源：Apple 诉状引述，未经独立验证）
  行业影响：Apple 申请的禁令若获批，OpenAI 须在 IPO 前逐部件证明首款硬件设备不依赖被盗知识产权；硬件主管 Tang Tan（24 年 Apple 老将）被指控引导在职 Apple 员工携实体零部件参加面试并传阅内部规避手册，若指控成立，OpenAI 硬件业务的合规基础将被直接撬动。

- **Meta Muse Spark 1.1 正式发布：Fable 成本约 8.5%，具备 1M context 与 computer use**

  来源：@AIatMeta 官号（多条推文）；@alexandr_wang（Meta Chief AI Officer，大量转发背书）；Meta 研究员 @yashvarpatel、@arnal_charles 等多人确认
  关键数字：output 定价 $4.25/M vs Fable 5 约 $50/M，约便宜 91%（来源：@_MaxBlade 测评，@alexandr_wang 转发背书，非官方定价文档，未经独立验证）；OS-World（computer use）53.5 → 80.8（来源：@yashvarpatel，Meta FAIR 高级研究员，当事方口径）；ProofBench 17% → 39%（来源：@arnal_charles，Meta 团队成员）
  行业影响：若价格属实，这是当前成本最低的 Opus 级竞争模型；@alexandr_wang 公开表示 "Anthropic 如果取消 Fable 订阅，麻烦大了，因为 Grok 4.5 和 Muse 都已经接近 Opus 水平，成本约为其 20%"。Meta 开放首个公共 API（Meta Model API 进入预览）。

- **Grok 4.5 + Grok Build 免费上线：APEX-SWE 排第二，编码提升 30 pp**

  来源：@grok 官号；@elonmusk；@mercor_ai（第三方 APEX-SWE 评测）；@perplexity_ai
  关键数字：APEX-SWE leaderboard #2，51.2% Pass@1（Fable 5：65.5%，来源：@mercor_ai，第三方评测）；一年内提升 30.2 pp（Grok 4：21.0% → Grok 4.5：51.2%，来源：@mercor_ai）；Perplexity WANDR 评测最高分，费用约 Opus 4.8 的一半，约 $4.76/trial（来源：@perplexity_ai，平台方口径）
  行业影响：Grok Build CLI 推出免费试用层，显著降低切换门槛；与 Cursor 深度集成使其在 agentic coding 场景有明确的使用路径；Elon Musk 同步澄清媒体误报：仅要求 Tesla/SpaceX "尝试" Grok 4.5，并非强制。

- **学术研究证实 Boko Haram 恐怖组织使用前沿 AI 获取炸弹制作指令**

  来源：@AntoniaJuelich（主导研究者）；合作方 @GaryMarcus + @CamAISciPolicy；@nytimes 报道；推文约 12 小时前（bookmarks 3961，engagement_rate 0.0019，本期非 Elon 内容最高信号）
  关键数字：[未经验证] — 研究覆盖规模、受访人数等定量数据未在推文中提供
  行业影响：此研究是有现场访谈支撑的实证性证据——一名前 Boko Haram 指挥官直接演示通过 AI chatbot 获取武器制作方法。配合 NYT 报道，标志着 AI 安全风险从理论进入有文件记录的现役武装应用，极大增加了近期监管机构对内容安全提出新合规要求的可能性。

- **美国非正式 AI 模型审查机制或威胁开源生存**

  来源：@AdamThierer（科技政策研究员）；@ylecun（Yann LeCun，NYU/AMI Labs，图灵奖得主）转发；@ClementDelangue（HuggingFace CEO）转发支持
  关键数字：无
  行业影响：LeCun 警告：若 "非正式审查机制" 固化为 "restrict-until-permitted" 默认逻辑，开源 AI 将面临 1990 年代 Clipper Chip 式政治对抗；HuggingFace CEO 公开表态支持开源 AI 默认化，两个独立行业信源同时指向同一监管风险敞口。

---

#### 深挖：GPT-5.6 Sol/Luna/Terra 家族正式发布

背景补充：
GPT-5.6 家族共三个变体：Sol（旗舰，最高性能）、Luna（最小、最高性价比）、Terra（中间层，但被 Sol 和 Luna 在能力/成本双维度 Pareto 主导）。@ArtificialAnlys 独立评测图表显示 "for any Terra effort level, there is a Luna or Sol effort level that is more intelligent at no extra cost, or as intelligent at lower cost"，这是少见的中间档次被彻底边缘化的情形。ChatGPT Work + Codex 整合同步推出，首版存在已知 UX 问题（Codex 入口变难、usage limit 不透明、部分 multi-agent workflow 出现回归），OpenAI 官方（@thsottiaux）承诺当周和下周修复。GPT-Live 同步全量覆盖所有 ChatGPT 用户。

数字核实：
- Luna 25x 降本 → 来源：@OpenAI 官号（当事方口径，未经独立验证）；@ArtificialAnlys 的 Pareto 图表间接支持 Luna 的极高性价比定性
- 医生 "fewer flaws" → 来源：@thekaransinghal（OpenAI Health AI，当事方）；样本量 20,000 个 axis ratings 同源，未经第三方重复实验
- 50 年数学猜想 → 来源：@polynoamial（Noam Brown，OpenAI 研究员），推文中未提供猜想名称或论文链接，[未经独立验证]
- 本次自动化生成中未执行外部 web_search，无法获取独立媒体的完整评测报告。

扩展影响：
@thdxr（opencode 开发者）分享第一周实际使用数据：Sol + Fable 并存时，Fable 占了 30% 的 API 成本——Sam Altman 转发并提问，显示出 Sol 在实际工作流中对 Fable 的快速替代趋势。ChatGPT 安装量发布当日增长超过前两周合计（@thsottiaux，OpenAI 团队，当事方口径）。Perplexity 立即将 GPT-5.6 家族集成进 Agent API presets（xHigh/High/Medium），官方称 "更高准确率、更低成本"；Grok 4.5 同时也进入 Perplexity Enterprise，说明平台层正在进行多模型并行接入。

对国内从业者的意义：
GPT-5.6 API 对国内开发者暂无直接访问路径；但 Luna 的成本结构（25x cheaper than GPT-5.5 at same performance）对国内模型厂商定价战略形成直接参照压力，尤其是在 MaaS（模型即服务）赛道的中端价格带上。Sol 的医疗能力突破（超越医生）若被国内医疗监管机构引用，将加速国内 AI 医疗合规框架的成型。

---

#### 深挖：Apple 正式起诉 OpenAI，指控系统性硬件商业机密盗窃

背景补充：
依据推文对诉状的详细引述，Apple 指控包含四条独立证据链：（1）招募管道中的主动引导——Tang Tan 要求受访的在职 Apple 员工携带实体零部件（电池、逻辑板）到 OpenAI 进行展示；（2）入职规避手册——Tan 向新员工传阅 Apple 内部离职安全绕过指南；（3）云存储漏洞利用——一名离职工程师在加入 OpenAI 后发现仍可访问 Apple 云存储，下载数十份机密硬件文件并在短信中嘲笑；（4）供应链欺骗——让 Apple 制造合作方误信 Apple 已批准，演示专有金属精加工技术。Apple 于 2026 年 2 月通知 OpenAI，5 个月未获回应后提起诉讼。

数字核实：
- "超 400 名前 Apple 员工在 OpenAI" → 来源：@aakashgupta 对 Apple 诉状的引述（7654 点赞），@ZeffMax（Wired 记者）也引用了原诉状文字；为当事方法律文件引述，可信度中等；本次自动化生成中未执行外部 web_search，无法补充 Bloomberg/Reuters 等权威媒体的独立核实。

扩展影响：
Apple 诉求揭示了法律策略：求赔偿之外，同时申请禁止 OpenAI 使用相关机密 + 返还所有文件 + 对 "io" 项目（OpenAI 首款硬件）进行全面证据开示。若法院支持临时禁令，OpenAI 须在 IPO 前证明设备开发路径不依赖被盗 IP，将深度影响 IPO 估值叙事。Elon Musk 与 Gary Marcus 的舆论放大效应（各自在 Twitter 上评论此案）进一步提升了本案公众曝光，有利于 Apple 的谈判筹码。

对国内从业者的意义：
若 OpenAI io 设备被法院叫停，参与其硬件供应链（精密连接器、金属件等）的国内供应商面临订单风险。更广泛的意义：此案是 AI 大厂对人才流动中 IP 合规性实施 "系统性追溯" 的首例，国内模型公司出海招募大厂工程师时的法律操作需要对照本案评估风险。

---

#### 深挖：学术研究证实 Boko Haram 使用前沿 AI 获取炸弹制作方法

背景补充：
研究由 Antonia Juelich 主导，与 Gary Marcus（曾在美国参议院出席 AI 证词）及剑桥 AI 科学政策团队（@CamAISciPolicy）合作完成，覆盖尼日利亚东北部现场调研。Gary Marcus 描述了直接访谈场景：在酒店房间内，一名前 Boko Haram 指挥官向 AI chatbot 询问 "如何制作炸弹" 并获得具体指导。研究被 @nytimes 报道，是本期收藏量最高的非 Elon 内容（3961 bookmarks，engagement_rate 0.0019）。

数字核实：
- 研究规模、使用频率等定量数据：[未经验证] — 未在推文中披露
- 本次自动化生成中未执行外部 web_search，无法获取 NYT 原文或论文摘要中的具体数据。

扩展影响：
核心信号是：主流 chatbot 在无明显 jailbreak 的自然对话中已向武器查询提供实质性帮助，且已进入监管薄弱地区现役武装组织的实际工作流。这类有文献记录的实证案例远比抽象的 "misuse 风险" 更具监管触发效力，短期内可能成为美国、欧盟提出新内容安全合规要求的具体依据。

对国内从业者的意义：
国内大模型出海部署（尤其是中东、非洲、东南亚市场）时，类似研究可能成为当地监管机构或国际合规框架引用的证据基础；国内已出台《生成式 AI 服务管理暂行办法》等规定，但跨境武装冲突场景的防护要求尚无具体标准，出海产品团队应提前评估武器相关 prompt 的防护层并留存审计记录。

---

## 2. 新产品 & 功能发布

- **ChatGPT Work + Codex 一体化工作区** — OpenAI

  核心能力：
  - ChatGPT 对话与 Codex agent 任务整合到同一界面，支持人与 agent 协同
  - GPT-5.6 Sol 作为旗舰模型接入，附带数据分析、多文件操作能力
  - 首版存在 UX 回归（Codex 入口变难找、usage limit 显示不透明），官方承诺当周和下周修复

  链接：https://chatgpt.com/download/
  立即试用优先级：本周内试
  理由：首版 UX 问题已明确，官方承诺修复；等第一轮 patch 落地后评估更有效率，避免用负面初体验影响判断

- **Grok Build CLI（含 Grok 4.5 免费试用）** — xAI

  核心能力：
  - CLI 工具支持 agentic coding 工作流，内置 Grok 4.5 模型
  - 免费试用层，`curl -fsSL https://x.ai/cli/install.sh | bash` 即可安装
  - 与 Cursor 深度集成，针对多步 build 任务优化

  链接：https://x.ai/cli/install.sh
  立即试用优先级：今天就试
  理由：零成本、5 分钟内可上手，APEX-SWE benchmark 排第二，对现有 Cursor 工作流有直接对比价值

- **Perplexity Agent API 集成 GPT-5.6 + Grok 4.5** — Perplexity

  核心能力：
  - xHigh/High/Medium 三个 preset 升级为 GPT-5.6 家族，官方称准确率提升、成本下降
  - 企业用户可选 Grok 4.5 作为 orchestrator 模型，WANDR 评测得分最高

  链接：https://docs.perplexity.ai/docs/agent-api/presets
  立即试用优先级：本周内试
  理由：对已接入 Perplexity Agent API 的开发者，presets 已自动升级，可直接对比前后 cost-per-task 变化

- **GPT-Live 全量推出** — OpenAI

  核心能力：
  - 实时语音对话能力全面开放给所有 ChatGPT 用户（含免费层）
  - 发布周末 usage limit 临时翻倍

  链接：https://chatgpt.com/download/
  立即试用优先级：今天就试
  理由：免费可用，30 分钟内可完成体验；对实时语音交互产品的开发者有参考价值

- **MuScriptor — 开源多乐器 MIDI 转录模型** — Kyutai Labs + MireloAI

  核心能力：
  - 将任意风格录音（流行、古典、金属、爵士）转录为逐乐器 MIDI
  - 当前最强开源多乐器转录模型（来源：@kyutai_labs，当事方口径）
  - Yann LeCun 转发，engagement_rate 0.0075（极高信号）

  链接：链接未提供（Kyutai 推文线程中，需前往 @kyutai_labs 查找）
  上手难度：中

- **APK Arena — 手机操作 Agent 前沿 Benchmark** — Jan Schnyder 等

  核心能力：
  - 50+ 关卡评估 AI agent 在真实手机任务上的表现（点击、视觉、记忆、游戏、真实应用操作）
  - 当前排名：GPT-5.6 领先所有其他模型（来源：@jjschnyder，@giffmana 转发，非官方来源，待验证）

  链接：链接未提供
  立即试用优先级：观望
  理由：benchmark 用于模型评估，适合选型参考而非直接上手；关注后续数据开放

---

## 3. 行业趋势 & 热议话题

- **AI 模型竞争轴从参数规模转向成本效率**

  参与讨论的主要声音：@AravSrinivas（Perplexity CEO）、@rasbt（ML 研究员）、@michaeljburry（Cassandra Unchained，转发 CNBC 报道）、CNBC 媒体报道
  主流观点：同等甚至更强能力正以快速速度降价——当日发布的三款主要模型（GPT-5.6 Luna、Muse Spark 1.1、Grok 4.5）均以 "低价高性能" 为核心卖点；CNBC 报道 "The AI race is shifting from bigger models to cheaper, smarter systems"，Perplexity CEO 确认 "from contacts in the Valley"。
  信号强度：强
  判断依据：CNBC 媒体报道（权威媒体）+ Perplexity CEO 亲口确认 Valley 信源 + 当日三款新模型定价结构均指向同一方向，满足多源共振门槛

- **Verification（验证能力）成为 LLM 的第四条 scaling 轴**

  参与讨论的主要声音：@drmapavone（Marco Pavone，Stanford 机器人学教授）、@StanfordAILab（Stanford AI Lab 官号转发）
  主流观点：继 pre-training、post-training、test-time compute 之后，"让模型判断解答是否正确" 的验证能力正成为独立的性能提升路径；LLM-as-a-Verifier 无需额外训练，三个简单成分（更细分评分粒度、重复评估、标准分解）在机器人、编程、医疗 AI 均达到 SOTA。
  信号强度：中
  判断依据：正式论文（arxiv.org/abs/2607.05391）+ GitHub 代码库（已开源），满足 "明确开源动向" 门槛；但仅 Stanford 实验室内部讨论，需跟踪社区采纳情况

---

## 4. 值得关注的洞察 & 观点

- @AravSrinivas（Perplexity CEO，与多家模型厂商有直接合作）：

  「Imagine a fable 5 quality model that's 3-4x less expensive in less than 6 months. And an Opus 4.8 grade model that can run on a local device in less than 12 months. Greater than 50% chance that these events will happen.」
  为什么值得关注：来自与多家模型厂商合作的 AI 平台 CEO，给出了带概率区间的时间线预测（"大于 50% 的概率"、"6 个月内"），是当前少有的量化性预测而非定性展望，可设置为追踪指标。

- @AravSrinivas（Perplexity CEO，Perplexity Computer 产品定位）：

  「The durable value is in a secure multi-model harness that takes care of orchestration and model routing in a secure compliant manner.」
  为什么值得关注：这是对 "单模型时代终结后护城河在哪里" 的直接回答——企业级安全合规的编排层，而非底层模型能力本身；当日三款竞争模型密集发布恰好佐证了这一判断，对中间层工具产品的产品路线图有直接参考意义。

- @sama（Sam Altman，OpenAI CEO）：

  「so far at least, i'm pretty sure AI has been net job-creating. this was not what i expected--although i was much less pessimistic than others, i thought by this level of capability we'd have seen some impact. it is possible this direction keeps going!」
  为什么值得关注：OpenAI CEO 自己承认当前 AI 净创造就业且超出了他的预期——这同时是对 "AI 已经取代工作" 叙事的内部反驳，也暗示当前 agent 能力尚未达到大规模劳动替代的门槛；值得与实际 agent 部署成效的数据对照。

- @binarybits（Timothy B. Lee，AI 记者），@GaryMarcus（AI 安全研究员）背书：

  「There's an epistemic chasm between those who think superintelligence implies near-omnipotence and those (like me) who don't.」
  为什么值得关注：清晰点出了当前 AI 讨论中最根本的认识论分歧——从 "超级智能" 到 "可以做任何事" 的跳跃是否成立，这一分歧直接决定了 AI safety 优先级、监管强度和产品路线图的判断分叉，是理解当前监管分歧的底层逻辑。

---

## 5. 实用资源 & 教程

- **MIT CSAIL 强化学习免费指南**

  类型：教程
  用途：系统回答 RL 领域核心问题，覆盖算法选择与训练稳定性等
  链接：https://shorturl.at/zcciv
  上手难度：中
  备注：engagement_rate 0.0276（本期最高），bookmarks 540，极高从业者存档信号

- **LLM-as-a-Verifier 开源框架**

  类型：开源项目 + 论文
  用途：无需额外训练的通用 LLM 验证框架，可作为 dense reward signal 接入 RL pipeline（机器人、编程、医疗 AI），RoboRewardBench、SWE-Bench Verified、MedAgentBench 均达 SOTA
  链接：论文 https://arxiv.org/abs/2607.05391；代码 https://github.com/llm-as-a-verifier/llm-as-a-verifier；网站 https://llm-as-a-verifier.com/
  上手难度：高

- **Grok Build CLI**

  类型：工具
  用途：免费试用 Grok 4.5 的 agentic coding 工具，与 Cursor 集成，适合多步骤编程任务
  链接：`curl -fsSL https://x.ai/cli/install.sh | bash`
  上手难度：低

- **MuScriptor 多乐器 MIDI 转录模型**

  类型：开源项目
  用途：将任意风格音频转录为多乐器 MIDI，当前最强开源转录模型
  链接：链接未提供（前往 @kyutai_labs 推文线程获取）
  上手难度：中

- **Ethan Mollick 的 DEEP TIME 城市游戏 Demo（Fable 生成）**

  类型：演示项目
  用途：展示 Fable 5 在创意重构任务上的能力边界——从同一个基础游戏出发，一句 prompt 生成完整可玩的历史叙事游戏
  链接：https://monument-deep-time.netlify.app/（原游戏：https://monument-brutalist-city-builder.netlify.app/）
  上手难度：低
  备注：engagement_rate 0.0035，对创意 AI 产品开发者有参考价值

---

## 传播力素材（适合自媒体改写的高互动 AI 观点）

- 「there are a lot of benchmarks that suggest 5.6 sol is the best model in the world right now, but the most reliable way to tell is that elon is obsessed with me again」 — @sama · 👍37,243 👁1,968,596 · engagement_rate 0.10%
  改写方向：适合 AI 竞争格局分析账号，可切入 "如何用大 V 互撕判断模型强弱" 或 "AI 圈的注意力经济学" 角度
  点评：Sam Altman 用 Elon 的攻击频率作为模型质量的代理指标，这一反常识逻辑精准描述了 AI 圈特有的注意力经济——竞争对手的敌意节奏确实与模型发布周期强相关。盲区：把 "竞争对手关注我" 等同于 "我是第一" 是循环论证；在不了解 xAI 竞争利益的读者那里，这句话容易产生误读。只看这句话会误以为这是模型质量的客观信号，实际上只是一个情绪化的语境标记。

- 「so far at least, i'm pretty sure AI has been net job-creating. this was not what i expected--although i was much less pessimistic than others, i thought by this level of capability we'd have seen some impact.」 — @sama · 👍5,114 👁420,788 · engagement_rate 0.11%
  改写方向：适合 "AI 与就业" 议题账号，可配合具体行业数据延伸；也适合 "AI CEO 最反直觉的公开承认" 类内容
  点评：传播力来自来源权威性（OpenAI CEO 亲口说）和内容的反叙事性（承认 AI 还没有在就业上造成他预期的冲击）。局限性："net job-creating" 是总量概念，遮蔽了结构性位移（特定职业的就业已显著受影响）；"at these levels of capability" 也为未来转折留了出口，解读时需带上这个条件。

- 「I gave Fable the code: 'take this game and do something incredible with it to make it something very different. Be creative' / It created DEEP TIME: create a city, watch it be abandoned and forgotten, and then dig it up as a future archeologist.」 — @emollick · 👍686 👁88,893 · engagement_rate 0.35%
  改写方向：适合 AI 创意应用账号，可配合 DEEP TIME 游戏链接（https://monument-deep-time.netlify.app/）提供可互动的体验
  点评：高 engagement_rate（0.35%）说明大量从业者在存档这个案例。传播力来自具体性（一句 prompt → 可玩游戏）和情感层（被废弃城市 + 未来考古学家有强烈叙事感）。局限性：展示的是最优情况；Fable 5 的一致性在复杂任务上差异较大，实际使用体验会有波动。

---

## 一句话总结

今日 AI 行业同时迎来三款重量级模型发布（GPT-5.6、Muse Spark 1.1、Grok 4.5），竞争焦点明确转向 "同等或更好性能下的成本压缩"，Fable 级性能的单价已可降至其约 8.5%；与此同时，Apple 对 OpenAI 的系统性 IP 盗窃诉讼直接威胁其 IPO 前的硬件合规基础，而 Boko Haram 使用 AI 制作武器的实证研究将 AI 安全风险从理论讨论拉入政策触发阈值。

## 今日行动建议

今天（30 分钟内）：
基于 [Grok 4.5 + Grok Build 免费上线] — 执行 `curl -fsSL https://x.ai/cli/install.sh | bash` 安装 Grok Build CLI，在 3 个现有开发任务上对比 Grok 4.5 与当前默认模型的速度和质量，记录每任务成本差异

本周内：
基于 [GPT-5.6 Sol/Luna/Terra 家族正式发布] — 用 Perplexity Agent API 升级后的 presets 对当前主要 agent 工作流跑一轮 cost-per-task 对比，产出一份 "GPT-5.5 vs GPT-5.6 成本与质量变化" 内部备忘录，判断是否需要更新调用策略

月内验证：
基于 [Apple 正式起诉 OpenAI] — 持续追踪两个节点：（1）法院是否批准临时禁令（直接影响 OpenAI io 硬件上市时间线）；（2）OpenAI IPO 招股说明书对此诉讼的披露方式——这两个节点将决定该事件对整个 AI 硬件赛道的影响烈度

---

## 信号 / 噪音比

进入第 1 节的有效新闻 6 条，进入第 2-5 节的有效信号 14 条，剩余约 51% 为低价值或噪音（主要来自 Elon Musk 的 SpaceX/Tesla 非 AI 内容、Musk 与 Altman 的人身攻击类互撕、Character.AI 剧情推广、无附加评论的纯转发）。今日整体信号密度：高。

**本期信源**：@elonmusk @sama @GaryMarcus @AravSrinivas @alexandr_wang @character_ai @StanfordAILab @gdb @giffmana @ylecun @emollick @ericmitchellai @rasbt @MIT_CSAIL @NotionHQ @adcock_brett @cohere @kchonyc @OpenAI @hugo_larochelle @StanfordHAI @sherwinwu @ClementDelangue（共 23 位）
