# AI 行业情报简报 | 2026-05-18

> 数据窗口：2026-05-17 06:00 — 2026-05-18 06:00（北京时间，过去 24 小时）
> 深度分析：3 条 | 模板版本：v2.3

---

## 1. 重大新闻 & 突发事件

- OpenAI 与马耳他签署首个国家级 ChatGPT Plus 合作

  来源：@gdb · 约 23 小时前（引用 @Reuters）
  关键数字：覆盖全体马耳他公民、提供 1 年免费 ChatGPT Plus（来源：openai.com/index/malta-chatgpt-plus-partnership，官方口径）；财务条款未披露。
  行业影响：这是 OpenAI for Countries 计划下首个以全民为单位的订阅合作，前置条件是马耳他大学开发的「AI for All」必修课。对其他主权政府而言，这是一份可直接复制的「AI 国家部署」样板；对欧盟内部、对其他 AI 实验室（Anthropic、Google、Mistral）而言，OpenAI 正在用国家级渠道锁定 default 心智份额。

- xAI Grok 接入 Nous Research 开源 Hermes Agent

  来源：@xai（@elonmusk 转发）· 约 15 小时前
  关键数字：Hermes Agent 5 月 10 日已在 OpenRouter 单日推理量榜单登顶，单日处理 2240 亿 tokens（来源：marktechpost.com，二手核实）。
  行业影响：xAI 把订阅（SuperGrok）和 X Premium 都开放给一个第三方开源 agent，意味着模型方主动把分发让位给 agent 层。对开发者：可以用 OAuth 而非 API key 调 Grok 4.3；对 agent 创业公司：开源 agent 第一次拿到了头部模型订阅入口，封闭 agent（Claude Cowork、Perplexity Computer 等）的护城河被部分稀释。

- Figure Helix-02 完成 80+ 小时不间断自主分拣，处理超 10 万件包裹

  来源：@adcock_brett 转发 @coreylynch · 约 20 小时前
  关键数字：80 小时连续自主作业、>100,000 件包裹（来源：@coreylynch、@adcock_brett，当事方口径）；外部媒体最新口径为 81 小时 / 101,391 件（来源：interestingengineering.com、sedaily.com）。
  行业影响：与上一代 8 小时班次相比，作业时长扩大约 10 倍且具备自动恢复机制（卡住后自重置）。这是当周 humanoid 厂商最具数字密度的工作证明，A 股机器人减速器、电机板块 5 月 15 日单日上涨约 5%（来源：finance.biggo.com）。对物流和仓储 SaaS：买家方对「真人工时替代」的尽调标准被抬高；对国内厂商（绿的谐波、三花智控等供应链）：直接利好。

- OpenAI 承认 Codex 中 GPT-5.5 能力衰退并已修复

  来源：@sherwinwu（OpenAI）转发自 @thsottiaux · 约 18 小时前
  关键数字：过去约 48 小时存在能力衰退，已定位并修复两个问题（来源：@sherwinwu，当事方口径）；将于当日重置用量上限。
  行业影响：付费用户实际体验到的「模型变笨」首次被 OpenAI 一线工程负责人公开承认，且承诺补偿用量。对 Codex 重度用户：意味着可以重新提交此前在该窗口失败的任务；对评测口径：提醒「同一模型名」在不同时间段并不等价，外部 benchmark 在该 48 小时窗口的结果需打折看。

---

## 深挖：OpenAI 与马耳他签署首个国家级 ChatGPT Plus 合作

背景补充：
合作通过 OpenAI for Countries 计划落地，OpenAI 此前已与爱沙尼亚（中学生 / 教师 ChatGPT Edu）、希腊地方机构合作，但马耳他是首个把 ChatGPT Plus 推到全体公民的国家。前置条件是马耳他大学开发的「AI for All」基础课程，覆盖 AI 能做什么 / 不能做什么 / 如何负责任地使用。境外马耳他公民同样可以加入。

数字核实：
覆盖人口及 1 年期限 → 已验证（来源：openai.com 官方公告 / euronews / engadget）；财务条款未披露 → 与原推一致。

扩展影响：
社交反馈两极：部分声音肯定 AI literacy 模式，另一部分质疑隐私、纳税人成本以及该计划本质上是 OpenAI 的获客通路（来源：cryptobriefing、cointribune 等）。对其他 AI 厂商：Anthropic、Google、Mistral 缺乏对应「国家级订阅」标准品，相当于在主权部署赛道被先发占位。

对国内从业者的意义：
直接影响有限——国内 AI 团队不会和 OpenAI 直接签政府合同。但有两个外溢值得关注：(1) 出海做 AI 教育 / 政企培训的中国公司可参照「免费课程 + 订阅捆绑」打包；(2) 中东、东南亚小型经济体若跟进类似国家级 AI 部署，将抬高国内大模型出海的合规与品牌门槛，需要前置国家定制化能力。

延伸阅读：
https://openai.com/index/malta-chatgpt-plus-partnership/
https://www.euronews.com/next/2026/05/16/malta-offers-free-chatgpt-plus-access-to-its-citizens-through-a-national-ai-program

---

## 深挖：xAI Grok 接入 Nous Research 开源 Hermes Agent

背景补充：
Hermes Agent 是 Nous Research 的常驻型开源 agent，本地运行、跨会话长期记忆、自动蒸馏可复用 Skills。本次集成默认接入 grok-4.3，复用 xAI 的 Responses 风格接口 codex_responses，引入 prompt caching（x-grok-conv-id 头），并移除 reasoning_effort 参数。所有套餐均可用，无需独立 API key。

数字核实：
「Hermes Agent 单日 2240 亿 tokens、5 月 10 日超 OpenClaw」→ 已验证（来源：marktechpost.com）；Nous 内部基准称 20+ 自学技能后同类任务完成速度快 40%（来源：hermes-agent.nousresearch.com，当事方口径，未经独立验证）。

扩展影响：
对模型方：xAI 是首个把订阅而非仅 API 开放给第三方开源 agent 的头部实验室，分发权进一步移到 agent 层。对竞品：OpenClaw、Claude Cowork、Perplexity Computer、Manus 都将面对「订阅可移植性」这一新比较维度。

对国内从业者的意义：
Hermes Agent 已支持 Xiaomi MiMo、z.ai/GLM、Kimi/Moonshot、MiniMax 等国产模型作为后端（来源：marktechpost.com / quasa.io）。对国内 agent 项目：(1) 出海团队可直接以 Hermes 为壳承接国产模型，绕开自建 agent 框架的工程成本；(2) 国内政企部署需注意，OpenClaw 已在 2026 年 3 月被国资 / 银行 / 政府办公场景禁用，Hermes 在国内部署同样需要做合规预审。

延伸阅读：
https://x.ai/news/grok-hermes
https://hermes-agent.nousresearch.com/docs/guides/xai-grok-oauth

---

## 深挖：Figure Helix-02 完成 80+ 小时不间断自主分拣

背景补充：
Helix-02 是 Figure 的 vision-language-action 全身自主系统，本轮直播在真实物流仓内运行，单机执行从识包、扫码到分拣的完整流程，并具备自动恢复（卡住自重置）。Figure 的同代型号 8 小时班次实验仅 4 天前才宣布，84 小时是公司自主跑出的延长测试，尚未经第三方审计。

数字核实：
原推「>80h / >100k 件」→ 与外部媒体口径基本一致（已验证为 81 小时 / 101,391 件，来源：sedaily.com、interestingengineering.com）。需要保留的差异：之前 Figure 官方曾披露 38 小时 / 47,000 件版本（来源：figure.ai/news/scaling-helix-logistics），不同口径源自不同测试批次。

扩展影响：
中国 A 股机器人指数 5 月 15 日上涨约 5%，谐波减速器、电机板块出现明显资金流入（来源：finance.biggo.com）；行业聚焦于 28–32 个关节 × 电机+减速器构成单机 50%–60% 成本。

对国内从业者的意义：
直接影响国内人形机器人供应链估值与订单——绿的谐波（688017）被市场视为 Helix-02 灵巧手谐波减速器核心供应商，其后续公告需要重点跟踪。对国内人形整机厂（宇树、Unitree、智元、银河通用等）：作业时长指标已被显式刷到 80+ 小时，下一轮 demo 周期内若无相应数字会在投资端被对标压价。

延伸阅读：
https://www.figure.ai/news/helix-02
https://en.sedaily.com/international/2026/05/17/figure-ai-robot-sorts-100000-packages-in-81-hours-without

---

## 2. 新产品 & 功能发布

- Codex 移动端 + 多设备互联 — OpenAI

  核心能力：
  - ChatGPT 应用内可直接用 Codex 从手机发起任务
  - MacBook、Mac mini、手机均可作为同一 Codex 线程的入口，线程状态跨设备共享
  - 支持「常驻心跳线程」，离开桌面任务不中断

  链接：链接未提供（演示与说明来自 @gdb、@nickbaumann_）
  立即试用优先级：本周内试
  理由：现 ChatGPT 付费用户可零门槛接入；对每天用 Codex 跑后台任务的开发者，是替换原有 SSH / tmux 工作流的关键一步。

- Grok Build（xAI 编程产品）— xAI

  核心能力：
  - 长任务稳定性大幅提升（@morganlinton 描述「一天内从 6/10 到 8/10」，当事方口径）
  - 任务可长时运行直至完成
  - 仍处 beta，迭代频率以「过夜更新」为节奏

  链接：链接未提供
  立即试用优先级：观望
  理由：仅有 xAI 单方与一名 beta 测试者口径，缺乏对比基准；非 Codex / Cursor 重度用户暂无切换理由。

- Grok Imagine SELFIE 模板批 — xAI

  核心能力：
  - 一次性发布 20+ 套自拍 / 服装场景视频模板
  - 套用即出动效，无需手写 prompt
  - 入口在 grok.com/imagine/templates

  链接：https://grok.com/imagine/templates（系列）
  立即试用优先级：今天就试
  理由：对短视频 / 营销内容团队，模板化降低 video gen 的上手成本；对评估 Grok Imagine vs Sora、Veo 的内容团队，是一份现成的横评素材包。

- FrontierSmith — Stanford AI Lab × FrontierCS

  核心能力：
  - 从「封闭式编程任务」自动 mutate / filter 生成「开放式优化任务」用于训练长程编码 agent
  - 论文称在 FrontierCS、ALE-bench 上训练效果优于人工策划的开放式数据
  - 同时开源 blog、论文、代码、模型权重

  链接：https://frontier-cs.org/blog/frontiersmith/ ｜ https://arxiv.org/abs/2605.14445 ｜ https://github.com/FrontierCS/FrontierSmith ｜ https://huggingface.co/runyuanhe/qwen35-9b-frontiersmith
  立即试用优先级：本周内试
  理由：长程编码 agent 训练数据是当前业界痛点，开源完整 pipeline 可直接复用。

---

## 4. 值得关注的洞察 & 观点

- @ylecun（Meta 前首席 AI 科学家 / NYU）：

  「Within a year to 18 months, we'll have a general method for training hierarchical world models … then scale them toward a universal world model」
  为什么值得关注：在 LeCun 长期主张「LLM 是死胡同、世界模型才是路径」的语境下，第一次给出明确时间窗（12–18 个月）；该判断若部分成立，将牵动 Meta AMI Labs 与 FAIR 后续叙事，也会被对手实验室作为 benchmark target。

- @gdb（OpenAI 联创）：

  「Tokens are rapidly becoming the universal input for solving problems」
  为什么值得关注：Brockman 罕见把整个产品论调收敛为一句话——所有问题都可被映射为 token 输入。这是 OpenAI 推 Codex 跨设备、Agentic SDK、Memory 等动作背后的统一抽象，比口号更接近内部 north star。

- @GaryMarcus（AI 怀疑派）：

  「OpenAI can't even align their systems well enough to get them to stop talking about goblins … 'never talk about goblins, gremlins, raccoons, trolls, ogres, pigeons …' Instead of actual computer science, we are left with alchemy.」
  为什么值得关注：援引 OpenAI 自家 audit 报告中「Nerdy persona 偏向输出 goblin」的怪相，攻击点不是模型差，而是 OpenAI 通过 system prompt 写死黑名单这一「炼金术式」对齐路径。对 alignment / safety 团队而言，是一个具体可验证的反例。

- @nickaturley（ChatGPT 负责人）转发 @nivi：

  「Memory in ChatGPT has gotten INSANELY good and nobody is talking about it. It shocks me daily.」
  为什么值得关注：来自 ChatGPT 产品一号位的「主动喊话」，对照同窗口内 @GaryMarcus 引用的 UIUC 论文（连续更新的 agent memory 会变得不可靠），形成一组同主题反向证词，提示 memory 是下一阶段产品对照的关键维度。

- @emollick（Wharton）：

  「In the original von Neumann sense of a singularity as the point 'beyond which human affairs, as we know them, could not continue,' it seems true … By definition, we can't know what that means in advance」
  为什么值得关注：把「奇点」概念重新拉回 von Neumann 原意——不是「AGI 来了」的爆点，而是「人类社会模式断裂点」。对从业者：在投资 / 创业判断中区分「能力 singularity」与「社会 singularity」是两类不同时间尺度。

---

## 5. 实用资源 & 教程

- Useful Memories Become Faulty When Continuously Updated by LLMs

  类型：论文
  用途：研究 LLM agent 在持续整合记忆时为何反而退化；提示 episodic memory 比 consolidated memory 更可靠
  链接：https://arxiv.org/pdf/2605.12978
  上手难度：中

- Project Tapestry

  类型：开源项目 / 倡议
  用途：The AI Alliance 主导，目标是为西方建立可信开源前沿模型协同（针对 @Dan_Jeffries1「西方需要开源冠军」叙事）
  链接：https://thealliance.ai/projects/tapestry
  上手难度：中

---

## 一句话总结

OpenAI 在马耳他完成首个「国家级 ChatGPT Plus」落地，xAI 把 Grok 订阅开放给第三方开源 Hermes Agent；与此同时 Figure 用 80+ 小时、10 万件包裹的连续自主作业把人形机器人「真实工时」基线推进到 8 小时班次的 10 倍。三条线同时指向：AI 的分发与执行入口正在从「产品」迁到「主权 / agent / 机器人」三类新载体。

---

## 今日行动建议

今天（30 分钟内）：
基于 [xAI Grok 接入 Nous Research 开源 Hermes Agent]——访问 https://x.ai/news/grok-hermes 用 SuperGrok / X Premium 账号完成 OAuth，在 Hermes Agent 里跑一个跨会话的小任务（如「每天 9 点抓 X 上 AI 关键账号 top tweets」），亲测订阅可移植性是否如官方所述。

本周内：
基于 [Figure Helix-02 完成 80+ 小时不间断自主分拣]——出一页内部备忘录，列出本团队 / 投资标的中所有声称「自主作业」的产品，强制按「连续作业时长、单位时间产出、自动恢复机制」三列对齐，识别哪些 demo 的指标已被 Figure 80h / 100k 件标准甩开半个量级。

月内验证：
基于 [OpenAI 与马耳他签署首个国家级 ChatGPT Plus 合作]——跟踪两个信号：(1) 是否有第二个国家在 30 天内签下类似协议（爱沙尼亚、希腊已是 OpenAI for Countries 节点，下一步看 Anthropic / Google 是否反制）；(2) 国内大模型厂商在中东 / 东南亚的政企招标中是否出现「国家级 AI 部署」对标条款。

---

## 传播力素材

- 「Tokens are rapidly becoming the universal input for solving problems」 — @gdb · 👍2213 👁125017 · engagement_rate 0.14%
  改写方向：适合做技术公众号 / X 长帖开头金句，可在「为什么所有 AI 产品最终都长得像 ChatGPT」类专题中作为论点抓手。
  点评：Brockman 把 OpenAI 整个堆栈抽象为一句话，传播性极强；但局限在于「universal input」掩盖了非文本模态（视频、机器人 sensor 流）所需的截然不同的工程实现，单看这句话会高估 LLM-only 路径的覆盖面。

- 「I don't know why data centers have become this generations nuclear power. Unlike nuclear power, there is a 0% chance that a data center can lead to any sort of disaster scenario」 — @ylecun (转 @Seanfrank) · 👍3473 👁485919 · engagement_rate 0.08%
  改写方向：可拆为「AI 基建科普 vs 公众焦虑」中视频脚本，反驳「AI 用水」叙事时引用。
  点评：句式有传播力且立场鲜明，但「0% 灾难概率」是修辞而非工程结论——能源调度失稳、就业冲击、地缘集中化都是数据中心可能放大的二阶风险，单看这条会过度反向。

- 「OpenAI can't even align their systems well enough to get them to stop talking about goblins …」 — @GaryMarcus · 👍54 👁2631 · engagement_rate 0.42%
  改写方向：适合 alignment / safety 圈层深度文章引用，作为「为何 RLHF + system prompt 黑名单不可持续」的具体案例。
  点评：批评点踩得很实——OpenAI 自家 audit 报告承认 Nerdy persona 在 76.2% 数据集中偏好输出 goblin。Marcus 借此把「炼金术」标签贴回 frontier lab；但只读此条容易忽视 RLHF + tool use + verifier 组合在大量实际任务上确实有效，不能仅凭一个 goblin 病例推论整个 paradigm 失败。

- 「Memory in ChatGPT has gotten INSANELY good and nobody is talking about it. It shocks me daily」 — @nickaturley (转 @nivi) · 👍1623 👁91872 · engagement_rate 0.12%
  改写方向：适合做产品评测 / 横评内容的钩子，对比 ChatGPT Memory vs Claude Projects vs Gemini personal context。
  点评：来自 ChatGPT 产品负责人本人，权威度高；盲区在于同窗口内 UIUC 论文证明连续更新的 agent memory 会退化，「INSANELY good」更多是体感而非可比 benchmark，记忆质量缺乏行业统一评测方法。

- 「Within a year to 18 months, we'll have a general method for training hierarchical world models」 — @ylecun (转 @haider1 转述) · 👍784 👁90883 · engagement_rate 0.33%
  改写方向：适合做长文「LLM 是否走到尽头」专题开头的时间锚，对照 GPT-5.5 当下表现做时间表追踪。
  点评：罕见来自 LeCun 的明确时间承诺，可被读者用作判分点；但 hierarchical world model 至今缺乏被广泛接受的评测基准，12–18 个月后的「general method」是否成立，将取决于 LeCun 团队自定义的标准而非公开 benchmark。

---

## 信号 / 噪音比

进入第 1 节的有效新闻 4 条，进入第 2、4、5 节的有效信号 11 条，剩余约 78% 为低价值或噪音（Musk 当日推文以非 AI 内容为主，含大量政治、体育、太空、X 平台运营噪音）。今日整体信号密度：偏低。

---

**本期信源**：@gdb @sherwinwu @ylecun @StanfordAILab @nickaturley @GaryMarcus @demishassabis @emollick @adcock_brett @Thom_Wolf @xai @elonmusk @fchollet @mattshumer_ @aidangomez @tobi @NotionHQ @MIT_CSAIL @addyosmani（共 19 位）
