# AI 一人公司日报 | 2026-07-04

数据窗口：06:00 — 06:00（北京时间，2026-07-03 至 2026-07-04）
深度挖掘：2 条

---

## 今日头条

Postiz——一个 AI Agent 优先的社交媒体调度工具——宣布月收入达 $145K MRR（约 ¥105.3 万/月，参考汇率 7.26，未经实时核验），日增 $1K MRR，即将本周突破 $2M ARR。@marclou 同期转发并提炼出一条战略公式：**「选一个商品化 SaaS → 改造为 AI Agent 优先 → 卖的是价值而非产品」**。这条公式配合真实收入数据一起发出，把抽象的商业建议落地成可复制路径，是今日最高质量信号。

---

## 今日金矿

> 数量按真实信号定：2 条。

### 金矿 1：Postiz — AI Agent 优先的社交调度器，$145K MRR 实战解析

Postiz — AI 驱动的社交媒体内容调度与发布工具（Agentic Social Media Scheduler）
来源：@wickedguro（Nevo David）[原始推文时间可能早于本期窗口] · 引用方 @marclou · 2026-07-03 23:19 · 👍530 📑651 👁62,552
engagement_rate：1.04%（同期中位数约 0.15%–0.20%，约为 5–7 倍）

**核心数据（据推文原文，@wickedguro 自述）**
- 当前 MRR：$145,000（约 ¥1,052,700/月）[据推文原文]
- 增速：约 $1,000 MRR/天（据推文原文，部分天更高）[据推文原文]
- 预计本周内突破 $2M ARR（约 ¥14,520,000/年）[据推文原文]
- 第二产品 UGC videos for agents：$2,600/月 [据 @wickedguro bio]

注：上述数字均为创始人自述，经 web_search 未能补充第三方数据（本报告在非交互模式下运行，无法执行实时网络搜索）。

**商业模式拆解**

Postiz 定位于 AI Agent 驱动的社交媒体内容调度（Twitter/X、LinkedIn、Instagram 等）。@marclou 给出的诊断是"commodity SaaS + AI Agent first"——传统社交调度工具（如 Buffer、Hootsuite）本质是管道，Postiz 在管道之上加了 AI 代理层，把"安排内容"升级为"AI 生成 + 排程 + 执行一体化"。

Marc Lou 提炼的公式（据推文原文）：
1. 选一个已有需求、竞争充分的 SaaS 品类（不是空白市场）
2. 不从底层重写，而是在其之上铺 AI Agent 逻辑
3. 卖的不是工具订阅费，而是"你不用动脑就能运转的自动化结果"

**复制路径（仅写真正适用的档位）**

档位 B（独立开发者）：
- 找一个已有玩家但无 AI Agent 层的细分 SaaS（如发票管理、合同追踪、EDM 工具、用户调研分析）
- 用已有开源组件做基础功能，AI 层做差异化（内容生成 + 自动调度 + 报告）
- MVP 第一步：接一个 AI 写作 API + 一个发布/操作 API，跑通最小自动化闭环
- 国内可访问性：Postiz 调用 Twitter API，国内需要工具；但"AI Agent + SaaS"这个模式完全可以用国内社媒平台（微博/小红书/视频号）复刻，各平台 API 开放程度需单独核实

档位 C（工具集成者 / vibe coder）：
- 用 n8n / Make 拼接：国内自媒体平台 API + 大模型写作 API + 定时发布逻辑
- 核心是把内容生产 → 排程 → 分发三件事用 AI 打通，卖"代运营结果"而非工具使用权
- 冷启动路径：目标是 3–5 个内容创作者客户，帮他们跑自动化方案，收月固定费；定价需参考市场，本报告不给具体数字（无公开基线）

**竞争格局**

国内有道互动、微盟、帷幄等在做多平台内容分发，但 AI Agent 优先的方向几乎没有人在做。差异化窗口仍在，但头部工具投入 AI 能力的速度在加快，时间敏感。

**深度综述**

Postiz 能跑到 $145K MRR 并不偶然，它踩在了三个趋势的交叉点：社媒内容生产的大众化需求、AI 写作能力的成熟化、以及内容调度工具市场的长期存在。但最值得关注的不是数字本身，而是 @marclou 提炼的框架——这是少见的能从案例里直接抽象出可复制公式的时刻。

传统 SaaS 创业建议是"找痛点 → 做产品 → 找市场"，而这个框架倒过来：先找有市场的"无聊品类"，再用 AI 在上面打一层新的价值层，跳过从零教育市场的阶段。这和过去几年"平台电商 + AI"、"教育 SaaS + AI"的思路相似，但执行门槛更低——现在任何一个能调 API 的人都能做这件事。

意外之处：Postiz 创始人 @wickedguro（Nevo David，粉丝 9,979）不是海外知名 solopreneur，没有大量的个人 IP 背书，但产品已做到月收入 ¥100 万级。这说明做好某个垂直 + AI 加持后，创始人的"网红身份"不再是必要条件，产品本身的分发力可以替代个人 IP 在早期所需的流量。

最大风险：调度工具的护城河天然较浅。Twitter/LinkedIn/Instagram 等平台随时可以收紧 API 政策，把第三方工具挡在门外。国内市场这个风险更大——平台对第三方接入的控制更严格。做这个方向必须准备好平台风险预案：当平台收紧 API 时，是否有办法快速切换或提供替代路径？如果没有，这个生意的天花板就是平台的善意。

趋势定位：这条信号属于"AI + commodity SaaS"赛道的中期验证阶段。已有多个收入案例（Postiz、各类 AI 写作/SEO 工具等），但中国市场实质性成功案例仍少，早进有优势窗口，但竞争正在加速进入。

---

### 金矿 2：Claude Code 前端设计 Skill 横测——42 个页面的对比报告

来源：@vista8（向阳乔木）· 2026-07-04 01:42 · 👍106 📑156 👁4,772
engagement_rate：3.27%（极高，全场第一，约为同期中位数的 15–20 倍）
内容类型：原创推文 + 系列追踪（含测试结果展示页）

**完整测试结论（据推文原文，@vista8 自述）**

测试方法：
- 模型：Fable 5（在 Happycapy 平台上运行）
- 规模：5 个 Skill + 模型默认 = 6 个 Sub Agent，并行生成 42 个对比页面
- 3 套测试 Prompt，变量控制：完全相同的模型，不同的 Skill

5 个被测 Skill 及结论：

| Skill 名称 | 出品方 | 综合评价 |
|---|---|---|
| ui-ux-pro-max | 社区 | 一般——自带模板和规则过多，反而限制模型发挥 |
| emil-design-eng | 社区 | **动效最好**（推荐用于注重交互动效的页面）|
| web-design-guidelines | Vercel 团队 | **Web 规范 + 无障碍最好**（推荐用于合规要求高的工具产品）|
| taste-skill | 社区 | **AI 味最小，文案最简洁**（推荐用于追求"不像 AI 做的"视觉感）|
| frontend-design | Anthropic 自带 | 万金油，但"用的人太多，正在成为新的 AI 味"；同质化风险上升 |

线上对比页面（据推文附链）：https://designskill.qiaomu.ai/（国内可访问性[未经验证]）

前置条件：
- 需有 Claude Code 访问权限（或 Claude API 调用能力）
- 国内使用需要工具

**复制路径（仅写真正适用的档位）**

档位 B（独立开发者）：
- 按场景选 Skill：动效需求 → emil-design-eng；合规/无障碍 → web-design-guidelines；追求自然感 → taste-skill
- 明确不建议不加思考地用 Anthropic 自带 frontend-design——产出物视觉同质化严重
- 最优实践：根据不同页面类型混用 Skill（落地页用 taste-skill，功能页用 web-design-guidelines，交互演示页用 emil-design-eng）

档位 C（工具集成者）：
- 把这份测评结论直接写入 CLAUDE.md 或团队 system prompt 里，作为 Skill 选择规范
- 用 Sub Agent 并行生成多版本后人工做最终选择，降低 prompt 调试时间成本
- 在 Fable 5 使用窗口（至 7 月 7 日）内批量完成设计测试，切换计费后成本大幅上升

**深度综述**

这条信号的真正价值不只是哪个 Skill 更好，而是揭示了一个更重要的现象：**Skill 生态正在进入质量分化阶段**。在 Claude Code 生态早期，Skill 的选择差别不大；现在随着 Skill 数量爆炸，如何选择 Skill 本身已经成为一项生产力技能，会用和不会用的人在产出质量上的差距在拉大。

3.27% 的 engagement rate 说明 @vista8 的受众是真正在用工具的人——他们存档这条推文是因为准备马上用，不是消费内容。向阳乔木（@vista8，粉丝 11.5 万）的定位是"爱钓鱼的 PM"，持续在 X 上做 AI 工具横测，这类"实践者测评"比厂商公告的信息密度更高，可信度也更强。

反直觉的部分：表面上功能最强、规则最多的 Skill（ui-ux-pro-max）评分最低，因为过度结构化限制了模型的创意空间。这和大模型提示词设计的普遍规律一致：约束越多 → 模型越走固定路径 → 输出越同质化。"少就是多"在 Skill 设计上也适用。

对于一人公司创业者：这份测评省去了数小时的自行测试时间，可以直接把结论写进工作流配置。更重要的是，这个"用 Sub Agent 并行测试然后人工筛选"的方法论本身可以复用到任何需要比较多个方案的场景（产品定位、文案方向、用户界面）。

竞争格局与窗口期：Fable 5 在功能上明显强于前代（据 @Shpigford 的实际体验，连续数小时使用未触发安全降级），但使用窗口只到 7 月 7 日。如果要系统性地建立自己的 Skill 使用规范，现在是最低成本的时间窗口。

---

## 快讯区

> 未进入深度分析但值得知道，每条 1–2 句。

**收入信号**
- Marc Lou TrustMRR 里程碑：churn 达全时最低 5.56%，30 天内 183K 用户访问，3 个赞助位全部售罄（赞助商包括支付商 Creem、COMMUNE、Context.dev）。Marc Lou 同天分享：当年 ShipFast 被嘲讽"只是个样板"，反而促使他做了更硬的 DataFast 和 TrustMRR，两年后睡觉时日收 $8K（据推文原文，@marclou 自述）。— @marclou · 2026-07-04 05:50

**工具发布**
- @levelsio 发布 levels.io/bubble-detector：实时股市泡沫指标工具，每天多次更新，聚合历史泡沫前已知预警指标（据 link_summaries 摘要）。engagement_rate 0.71%，bookmarks 640。国内访问需工具（.io 域名）。— @levelsio · 2026-07-04 01:24

- @shl（Sahil Lavingia，Gumroad 创始人）发布开源项目 antiwork/chromeless：github.com/antiwork/chromeless，具体功能主要在配图中（文字原文仅"new oss"），无法从文本分析详细功能。engagement_rate 0.91%，bookmarks 70，经 web_search 未能获取补充信息（非交互模式）。— @shl · 2026-07-04 03:25

- MistTrack 发布 x402 API：区块链地址风险分析 API，无需注册无需 API Key，通过 x402 支付协议按调用付费，地址标签 $0.10/次起，定位 AI Agent 自动化场景。国内可用性需自行核验（区块链工具）。— @evilcos 转发 @MistTrack_io · 2026-07-03 22:10

**工具更新**
- @gregisenberg 提醒：Fable 5 目前包含在 Claude Max 订阅内，窗口至 7 月 7 日结束，之后转按量计费（$10/$50 per million tokens，Anthropic 定价最高模型）。建议在截止前完成大型重构、深度研究、长上下文分析等高消耗任务，并使用 $200 Max 20x 计划获取足够额度。[据推文原文，具体价格以 Anthropic 官方公告为准]— @gregisenberg · 2026-07-04 01:56

**值得关注的观点**（仅收录信息密度足够高的内容）

- @SimonHoiberg（bootstrapped SaaS 创始人，粉丝 15.9 万）：「"Just use Vercel. Just use Supabase. Just use Clerk."——现在你的认证、数据库、部署各属 3 家公司，他们随时可以改价格。剩下的产品是在 wrap OpenAI。你到底拥有什么？」——对 AI SaaS 技术栈过度依赖三方的精准警告。👍681 👁62,707，engagement_rate 0.24%。— @SimonHoiberg · 2026-07-03 23:22

- @lidangzzz（HedgehogLab 联创，粉丝 160.7 万）：「RAG + vector database 是死路一条。正确做法：① 正确用好 memory；② 正确分块 + indexing + summarization；③ 给 agent 提供 search 工具让 agent 自己模糊搜索；④ 用 SRAM-only inference 提供商（如 Groq、Cerebras）提速。」— engagement_rate 0.67%，bookmarks 315。— @lidangzzz · 2026-07-03 20:56

- @vista8 一天四个网站的 vibe coding 实践：用 Codex Sub Agent 一天开发 YouTube AI 播客摘要站、GitHub Top100 站、Skill 精选站、FDE 资源站；发现 Codex 在内容量大时会自动套模板填废话，强制加 memory + Sub Agent 可缓解。— @vista8 · 2026-07-03 23:04

- @asmartbear（Jason Cohen，两个 unicorn 创始人，粉丝 4.7 万）：「与其优化节省 $1000/月，不如获取新增 $1000/月 MRR——前者是一次性的，后者是复利的。把产品重新定位为"让增长更快"而不是"让运营省钱"。」附文章链接 longform.asmartbear.com。— @asmartbear · 2026-07-03 06:54

**教训与反思**

- Acquire.com 上正在出售一家"网站转 App"无代码工具（$1M ARR，TTM 收入 $1.2M，TTM 利润 $761K），列表链接：app.acquire.com/startup/...。作为参考数据点：$1M ARR 利润率约 63%，这类技术壁垒较低但执行到位的工具仍有人愿意买单。国内复制可行性存疑（iOS/Android 上架政策不同）。— @agazdecki · 2026-07-04 04:50

**传播力素材**（适合自媒体改写的高互动观点）

- [原文] "This dead-simple system will help you say 1 idea in 1,000 unique ways (so you never stare at a blank page again). It's called the 4A Framework – here's how it works:" — @dickiebush · 👍4,568 📑7,136（views 数据显示为 0，系统异常，可能是 Thread 抓取限制）· engagement_rate：[数据异常，bookmarks 数量极高]
  改写方向：适合小红书/视频号——「内容创作者的反空白页公式：4A 框架，1 个想法衍生 1000 种选题」，配流程图或步骤卡片可做高收藏内容
  点评：7,136 bookmarks 说明这条内容击中了内容创作者的核心焦虑——"不知道写什么"。其局限是框架本身没在这条推文里展示（在 Thread 后续），直接改写需要先获取完整 Thread，否则只有标题没有内容，质量无法保证。不建议仅凭这句话就写内容。

- [原文] "What happens when you die: They divide up your shit. They summarize your life in 500-1000 words. People who knew you less say sorry to people who knew you more. Everyone eats, drives home, and wakes up the next day and goes to work. Whatever you're worried about won't be in those 500 words. You can dare greatly or not at all, but you're gonna die either way. Might as well squeeze every motherfucking drop out." — @AlexHormozi · 👍5,097 📑1,511 👁223,673 · engagement_rate 0.68%
  改写方向：适合视频号/公众号短文——「你死之后，没有人会把你现在焦虑的那件事写进追悼词」，结合"该不该辞职创业"或"为什么迟迟不行动"的转型场景
  点评：击中的是"过度在乎他人评价"的普遍焦虑，在创业/转型犹豫期共鸣强。1511 bookmarks 说明读者存档是为了将来某个决策时刻使用，而不是当下消费。局限在于这类死亡哲学内容容易变成励志滥调，有效改写需要加具体场景（如"那个让你迟迟不敢辞职的顾虑，出现在你葬礼上的概率是多少"）而非直接翻译原文。

- [原文] "Underrated life advice: Have more hobbies and fewer opinions. Learn an instrument. Plant a garden. Build something with your hands. Cook. Paint. Run. The happiest people I know spend less time debating life and more time actually living it." — @blakeaburge · 👍3,044 📑706 👁58,570 · engagement_rate 1.21%
  改写方向：适合小红书——「少一点意见，多一点爱好」，用"爱好 vs. 刷 X 争论"对比体，配产品/手工/运动图，目标 20–30 岁从业者
  点评：1.21% engagement rate 显示有真实认同感，但独创性有限。"少看手机多做实事"是常见主题，容易被读者感觉"又是这种"。有效改写需要找到更具体的切入角度，比如针对"整天刷 AI 创业信息却什么都没做的人"这个具体人群，反差会更强。

---

## 延伸资源库

### 播客 / 视频 / 访谈
- @lennysan 发布 Andrew Ambrosino（OpenAI Codex App 负责人）访谈片段，内容包括：Codex 自 2026 年 2 月以来使用量增长 6 倍，周活跃用户超 500 万，近 100% 的 OpenAI 员工使用 Codex App。核心话题：PM 在 OpenAI 的工作方式、AI 为什么不擅长设计、"品味"作为专业技能的真正含义。YouTube 链接：youtu.be/P3KDebPTUrw（需工具）。原始推文发布于本期窗口内（2026-07-04 00:12），但 @lennysan 的访谈主推文发布时间更早（[可能与上期重叠]）。

### 图书 / 课程
本期无相关推荐。

### 链接汇总（来源标注）

工具类：
- https://levels.io/bubble-detector — 实时股市泡沫指标（@levelsio · 需工具）
- https://github.com/antiwork/chromeless — Gumroad/antiwork 新开源项目（@shl · 需确认具体功能）
- https://designskill.qiaomu.ai/ — Claude Code 设计 Skill 对比测试展示页（@vista8）
- https://souplings.fun — Josh Pigford 用 Fable 5 构建的 Spore 风格 MMO（@Shpigford · 当日发布）

SaaS / 收购相关：
- https://x.com/wickedguro/status/2072654822449586327 — Postiz $145K MRR 原始推文
- https://app.acquire.com/startup/R9rKDTiUT1WWoUkG3Bz38sV3Omq2/E09Miug2fK0uQAl8Fg3l/ — Acquire.com 在售"网站转 App"工具（$1M ARR，$761K TTM 利润）

---

## 行动建议（按档位分组，不超过 4 条）

> 仅基于今日金矿可直接转化的行动。

档位 B（独立开发者）
- **本周最优先**：Fable 5 使用窗口至 7 月 7 日（据 @gregisenberg），用这 3 天集中完成一件高消耗任务：完整 codebase 重构、设计 Skill 系统测试、或一个需要 1M 上下文的深度分析。7 月 8 日后付单价，成本压力上升。
- 参照 Postiz 框架找一个国内复制方向：找 1 个国内有真实需求但无 AI Agent 层的 SaaS 品类，做最小 MVP（AI 生成 + 自动发布 + 报告），先跑通一个客户的闭环。

档位 C（工具集成者 / vibe coder）
- 把 @vista8 的 Skill 测评结论写入 CLAUDE.md 或工作流配置：动效优先 → emil-design-eng，规范合规 → web-design-guidelines，追求自然感 → taste-skill，不建议默认使用 Anthropic 自带 frontend-design。
- 向 2–3 个内容创作者提案"社媒自动化方案"，明确交付的是运营结果（如每周固定发布 N 条）而非工具使用权，收月固定费。

---

## 避坑指南

> 本期无真实失败案例，跳过此节。

---

## 本期情报评估

**信息密度**：正常偏低
今日为美国独立日（7 月 4 日节假日），信号密度低于工作日。timeline 被世界杯比赛内容（葡萄牙/西班牙相关）和政治观点推文大量占据，有效信号集中在 23:00–02:00 BJT 的时段。

**趋势信号**：
"AI Agent 包裹 commodity SaaS"已进入中期验证阶段——Postiz 是继 AI 写作/SEO 工具之后又一个有具体数字的案例，但竞争加速，进入窗口正在收窄。

**横向对比**（本期有两个收入数据点）：
- Postiz（@wickedguro）：$145K MRR，单产品，AI Agent 调度方向，快速增长期
- Marc Lou 矩阵：ShipFast $30K/m + DataFast $21K/m + TrustMRR $15K/m + 其他，多产品稳定矩阵，发展成熟但相对更重

单产品冲量 vs. 多产品矩阵，两条路径均有验证中的案例，不同阶段的创始人参考不同。

**当日强信号数 vs. 噪音比**：
2 条强信号（Postiz A 级、vista8 设计 Skill B 级）/ 约 220 条噪音（噪音率约 80%，主因节假日 + 世界杯占据 timeline）

**信号覆盖说明**（by_bookmarks Top 5）：
- @dickiebush 4A Framework（7,136 bookmarks）→ 传播力素材区 ✓
- @naval 反资本主义左翼评论（2,963 bookmarks）→ 噪音，政治观点，不收录
- @levelsio 转发旧 AI 视频"AI video - 3 years ago"（2,467 bookmarks）→ 旧素材被回炉，非新信号，不收录
- @AlexHormozi 死亡沉思（1,511 bookmarks）→ 传播力素材区 ✓
- @naval 社会主义评论（713 bookmarks）→ 噪音，政治观点，不收录

engagement_rate Top 5 覆盖说明：
- @Jayyanginspires 转发（1.76%）→ 内容在图片/视频中，无法从文本分析，不收录
- @ecomchasedimond 4th of July email inspo（1.61%）→ 电商营销工具，与一人公司相关性弱，不收录
- @blakeaburge 爱好 vs 意见（1.21%）→ 传播力素材区 ✓
- @dklineii "你不是靠努力获得回报"（1.08%）→ 管理/职场建议，金句类，不收录
- @marclou 引用 Postiz（1.04%）→ 金矿 1 ✓

**本期信源**：@wickedguro @marclou @vista8 @levelsio @gregisenberg @shl @lidangzzz @SimonHoiberg @asmartbear @dickiebush @AlexHormozi @blakeaburge @evilcos @agazdecki（共 14 位）
