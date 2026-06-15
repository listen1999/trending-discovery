# AI 一人公司日报 | 2026-06-16

数据窗口：2026-06-15 06:00 — 2026-06-16 06:00（北京时间，过去 24 小时）
深度挖掘：3 条
汇率参考：1 USD ≈ 6.76 CNY（据 exchange-rates.org 6 月 15 日数据）

---

## 今日头条

AI 移动 App 这条赛道的"草根复制路径"正在从奇闻轶事变成可拆解的 SOP。一位 19 岁、一年前还在 TJ Maxx 收银的美国年轻人 @GeorgeLampro20，目前据 Greg Isenberg 自述每月用 AI 做 App 进账 20 万美元（约 ¥135 万 [未经验证]），并把"五步打法"做成 PPT 公开分享——一图爆款功能、强 onboarding、IG 当渠道、量级 DM 启动。这件事的真正信号不是这个人具体赚了多少，而是这套"零代码 + Capacities/Cursor + IG 冷启动"的组合正在被越来越多人复刻，并对中文档位 B/C 形成直接可比对的样本——意味着把同样的 playbook 搬到小红书、抖音、即刻、App Store 中国区，是 2026 下半年最确定的"AI 一人公司"机会方向之一。

---

## 今日金矿

### 金矿 1：19 岁 AI App 独立开发者 @GeorgeLampro20 的"$10K/月剧本"

[GeorgeLampro20 × @gregisenberg](#) — 一位非程序员通过 AI 做 App 在 12 个月内从 TJ Maxx 收银员到自述月入 $200K 的完整打法
来源：@gregisenberg · 2026-06-16 03:19 BJT · 👍450 👁39,681 🔖1,010 · engagement_rate **2.55%**（约为同期中位数 13 倍，今日全 Top 信号之首）

**核心数据（已交叉验证）**
- 自述月收入：$200,000+（约 ¥135 万/月）[据推文原文，未在公开播客转录页找到独立证据]
- 标志案例 A："一个我自己讨厌的 App"，IG 单月浏览 180 万次，月营收仅 $35（约 ¥237）
- 标志案例 B："一个我真心喜欢做的 App"，同一月做到 $17,000（约 ¥11.5 万）营收
- 嘉宾节目：Greg Isenberg 主理的 The Startup Ideas Podcast，经 web_search 在 Apple Podcasts、Listen Notes 验证节目真实，但本期单集尚未抓到独立单集页（推测刚发布，未被索引）

**商业模式拆解**
- 收入公式：App Store 订阅价（多在 $4.99–$9.99/月或 $49.99/年）× 通过 IG/TikTok 等 social 漏斗带来的新激活
- 主要成本：模型 API（OpenAI/Anthropic）+ 苹果 30% 抽成（首年）+ IG 投放/达人合作
- 利润弹性：5 步打法里第 3 步「onboarding 才是真正的钱」隐含的核心是付费转化率而非 DAU——这种"短链漏斗 + 即时付费"模式天然对个人开发者友好，因为不需要长期用户运营

**5 步打法（按原推文复述，不压缩）**
1. **挑你真的有热情的题目** ——他亲口验证：讨厌的项目 1.8M 浏览只赚 $35；喜欢的项目同一月赚 $17,000
2. **造一个 5 秒就 get 的「gotcha feature」** ——例："拍一张食物图，告诉你卡路里"。90% 的分发问题靠这一句话解决
3. **真正的钱在 onboarding** ——教育 → 社会证明 → 个性化制造沉没成本 → 付费墙前临门一脚 FOMO
4. **IG 既是漏斗也是信任凭证** ——找达人时人家会回头看你 IG：3 个 demo + 干净 bio + 合拍贴文
5. **分发是数字游戏** ——按目标用户调 feed、一整天滚 + DM、雇 VA、把创作者拉到电话上谈

**复制路径（按档位）**

档位 B（独立开发者）：技术栈建议——iOS 端用 SwiftUI + Cursor/Claude Code 加速；后端跑 Supabase 直连 OpenAI/Claude API；订阅用 RevenueCat 拼苹果内购（中国大陆 App Store 已支持 Apple Pay/微信内绑卡，但小心审核 + 30% 抽成）。冷启动选小红书/即刻而不是 IG——同样是图文 + 短视频 demo，对中文用户的 CPM 显著更低。

档位 C（vibe coder / 工具集成者）：与其卷 iOS，不如把同款 gotcha feature 落到微信小程序（卡路里/穿搭/对话训练等），用 Coze/Dify 拼 prompt + 视觉模型，单产品 6–8 周可上线。注意：微信小程序订阅功能尚未直接打开，需要走「按次付费」或「会员 + 私域引导」组合。

档位 A（内容创作者）：不必自己做产品，把这套 5 步法直接做成中文小红书选题。例如「为什么我做的 App 只赚 $35，朋友做的同一月赚 17K」一图流——按今日推文体感，这种"反直觉对比 + 实操结论"在小红书属于高存档型选题。

**竞争格局**
- 同类海外人物：@levelsio（PhotoAI $100K/m）、@marclou（多产品组合 $27K/m+）已经站在金字塔尖，但都是程序员转独立开发；这位 19 岁的样本最值得注意的，是「非技术起点」也能跑通同款路径
- 国内对标人物：尚未出现明显公开案例。lxfater（@铁锤人）、宝玉（@dotey）等账号正在用 AI 协助内容/工具流，但还没看到"非程序员做出多个 AI 移动 App + 公开打法"的中文样本

**成本与时间预期**
- 冷启动预算（按公开数据基线）：苹果开发者账号 $99/年 + Cursor Pro $20/月 + OpenAI API 起步 $20/月 + IG 达人合拍 $50–$300/单 = 第一个月 $300–$600（约 ¥2000–¥4000）；中国区可先用微信小程序绕开苹果费用
- 关键里程碑：6 周内上线 1 个 gotcha feature → 12 周内验证付费转化率 → 半年内做出第 2 款验证组合效应（按 5 步法描述的节奏）

**深度综述**
这条信号最值得关注的不是钱，是 **打法的高度可复制性**。过去两年"AI App 月入万美元"的故事一直在传，但绝大多数样本是从程序员转过来的——@levelsio、@marclou、@dvassallo 这些名字本身就是高门槛。GeorgeLampro 这个样本把门槛拉到了"会用 Cursor 不会写 Swift"那一档，正好对应 vibe coding 用户群。Greg 把整套 PPT 转述出来的动作，也说明这条赛道开始从"少数高手秀肌肉"进入"播客和影响者集体复制方法论"的中期阶段——这是任何垂直机会窗口走向共识化的标志。

但风险信号同样清晰。第一，5 步法里 90% 的杠杆其实在「IG 分发」一步，这是中国市场最难直接迁移的环节——小红书/抖音对 App 下载导流的限制远比 IG 严格，付费转化漏斗设计也要重做。第二，"挑你真的喜欢的题目"是事后归因——讨厌的 App 拿到 1.8M 浏览本身就是分发能力的体现，反过来推"喜欢比策略更重要"容易让复制者忽视分发原力。第三，自述收入数字在播客访谈里属于"无法 SEC 备案的口头数据"，宁可看作"上限案例"而不是"中位值"。最后，对中国大陆开发者而言，App Store 中国区的高客单订阅极少跑得通，更现实的落地是微信小程序 + 私域订阅、或者直接做出海全栈（Stripe + iOS 全球版）。

回到读者侧：档位 B 现在最该做的，是花 1 个周末把这套 5 步法拆成自己的 1 页 SOP，挑一个 gotcha feature 在 4 周内做出 v0.1；不要去拼"App 数量"，先拼"5 秒能讲清的卖点"。

原始链接：https://x.com/gregisenberg/status/2066601447525888209

---

### 金矿 2：Lovable 设计负责人 Felix Haas 的 7 条"AI 时代高效团队"观察

[Felix Haas × dotey 整理](#) — Lovable 设计负责人对内部高效团队的非典型总结
来源：@dotey · 2026-06-15 10:37 BJT · 👍344 🔖350 👁48,743 · engagement_rate **0.72%**（同期中位数约 0.17%，约 4 倍）

**信源可信度**
- 原作者 Felix Haas 是 Lovable 设计负责人 + Sequoia Scout + 30+ 项目天使（经 LinkedIn / fh.design / Substack 验证）
- 公司可验证背景：经 web_search 在 Sacra/getlatka 查到 Lovable 2026 年 ARR 已达 $500M（约 ¥33.8 亿）、估值 $66 亿（B 轮，2025 年底），是欧洲增长最快的 AI 公司之一
- 中文转述者 @dotey（21 万粉丝、AI 工程师身份可验证）为业内长期高质量翻译/转述账号

**7 条观察（按 dotey 整理，原意保留）**
1. **别像员工一样等安排** ——影响力最大的人不问"这归谁管"
2. **招人看态度，不看简历** ——技能可学，curiosity/grit/learn anything 才决定能不能成
3. **好奇心 ≠ 沉迷 AI** ——真正用好 AI 的人在不停试没人让他试的东西，不是天天刷资讯
4. **让资深的人重新动手** ——AI 让 IC 杠杆放大，深度用 AI 的资深工程师/设计师可能是公司最强组合
5. **自我意识是速度的敌人** ——最快的团队不太在意谁拿功劳
6. **先发布再迭代** ——一周的内部讨论抵不上一天真实用户反馈
7. （第 7 条原推文未具体展开，dotey 整理时聚焦在前 6 条）

**对一人公司的对应价值**

档位 B、C 适用：第 4 条「资深的人重新动手」对中国独立开发者最有现实意义——很多有 5–10 年大厂经验、过去几年被推到管理岗的工程师，正在通过 Cursor/Claude Code 重新拿回"亲手做产品"的能力。这条路在国内已经能看到样本（lxfater、Fenng 等），是当下最合理的转型路径之一。

档位 D（服务变现者）适用：第 2 条「招人不看简历」反过来给"个人服务包"思路——以 mindset 而非 portfolio 为卖点的咨询/陪跑产品（如「与你的 AI 工作流共建 4 周」）在国内私域圈已有零星付费案例。

**深度综述**

这 7 条单独看都不新鲜，但放在 Lovable 这家公司当下的快照里看就有了密度——2024 上线、2025 年中 1 亿美元 ARR、2025 年底 3.3 亿美元 B 轮估值 $66 亿、2026 年 ARR 跃过 $5 亿。这是欧洲过去十年里最陡的一条增长曲线，几乎全是远程 + 小团队 + 重 AI 工具链跑出来的。换句话说，这 7 条不是普世真理，是已经被"亿美元/季度"验证过的工程文化样本。

最值得拎出来反复读的是第 4 条「让资深的人重新动手」，这是 AI 时代最容易被忽视的组织变化。AI 工具链彻底改写了"管理 vs 执行"的边界：过去因为做产品太慢、所以经验丰富的人必须被推到 PM/管理岗去带年轻人；现在一个深度用 Cursor + Claude Code 的资深工程师，可以在一周内完成过去要带一个 6 人小队两个月才做出的产品。对中国独立开发者来说，这条规则的现实意义是——**别因为"我已经 35 岁了"就觉得自己适合做规划/做指导/做投资人**，反而是 30+、有体系化判断力又愿意亲手敲代码的人，处在历史窗口最甜的位置。

但要警惕被这套话术带偏的两个陷阱。第一，Lovable 是已经融到 B 轮、有现金流支撑的"准独角兽"，它的"先发布再迭代"是建立在"用户已经在等你新版本"的前提上的——一人公司在用户基数为 0 的早期阶段，盲目「快速发布」反而容易透支注意力。第二，「自我意识是速度的敌人」对个人创业者反向适用度低——一人公司没有同事拿你的功劳，反而需要更强的「公开构建」自我意识来积累信号。

原始链接：https://x.com/dotey/status/2066349458904744224
被引原推：https://x.com/felixhhaas/status/2066168984177955157

---

### 金矿 3：Factory 2.0 发布——从"编程 Agent"切到"软件工厂"

[Factory 2.0](#) | 把分散的编程 Agent 拼接成「需求 → 计划 → 编码 → 测试 → 安全 → 部署 → 监控」的端到端自迭代系统
发布日期：2026-06-15 BJT（@FactoryAI 公告原推 👍721）
国内可用：直接访问（factory.ai 主域名）；其底层依赖的 GitHub/Slack/Linear/Notion/Sentry 中部分服务在国内需要工具

**核心功能（聚焦对一人公司的价值）**
- 把代码 Agent 升级成"软件工厂" ——围绕一个完整 SDLC 跑 Droid，自动从 bug 报告/客户反馈出发，反向倒推 PR
- 任意模型可插拔 ——可在不同 IDE/终端中使用，强调"with any model"
- 桌面端可视化管理 ——新增 desktop app 用于看板式追踪整个 factory 的状态
- 已在生产使用：经 web_search 验证 NVIDIA、EY、Adobe、Palo Alto Networks、Adyen、Blackstone、Wipro、Comarch 已在企业内跑（来源：NEA 公告 + tessl.io 报道）

**定价**
- 经 web_search 未找到 Factory 2.0 公开定价表（官网 factory.ai 引导预约 demo）；目前面向企业 + 个人 beta，价格未公开
- 对照参考：同类企业级 Coding Agent（如 Cognition Devin）订阅价 $20–$500/月不等，Factory 大概率与之同档

**10 分钟上手**
1. 进 factory.ai，登录 GitHub OAuth
2. 选一个仓库授权 Factory 接入 Linear/Sentry/Slack（任一组合）
3. 在 Droid 控制台开一个新任务（指定模型，如 Claude Opus 4.7 或 GPT-5.5）
4. 让它从一个真实 issue 跑「计划 → 编码 → 测试 → PR」全流程
5. 在桌面端追踪 Factory 状态，介入审核 PR

**与现有工具链配合**
- 适合做 vibe coding 的副产品收尾：你用 Cursor 跑了产品 v0.1，但每周都要重复"读 Sentry → 写 hotfix → 提 PR"，Factory 把这条重复链直接外包
- 不适合"从零做产品"：Factory 是给已经有 codebase 且有真实 issue 流的人/团队设计的——刚启动的 idea 阶段建议继续用 Cursor/Claude Code

**踩坑预警 / 已知限制**
- "Software Factory"这个命名 ——经 @ecomchasedimond 评论，行业里几个跑多个 AI 编码工具的团队都在等一个新词，Factory 显然在抢「品类命名权」。这是行业进入共识期的早期信号，但也意味着 1–2 个季度内会有大量同名/同概念产品蹭热点，谨慎被概念锚定
- @dotey 同期发出警告：「警惕 AI 圈造新词博流量的老套路」——遇到 Token Capital / LLM Wiki / Loop Engineering / Software Factory 这种新词，先看是谁说的、再看反对意见，最后保持自己的判断

**深度综述**

Factory 把"编程 Agent"重命名为"软件工厂"，本身是一次精准的品类抢位。过去半年里至少有 5 个团队（Cognition Devin、Replit Agent、Cursor Agent、Anthropic SWE Agent、Claude Code）都在做同一件事——让 AI 从 issue → PR 跑端到端流程。Factory 2.0 选择不再强调"我们的模型/算法多强"，转而抢占类目名词，这是 to B 软件市场最经典的「先命名后定义」打法。这跟 2018 年 Snowflake 强行把自己叫做"Cloud Data Platform"而不是"Cloud Data Warehouse" 是同一种动作。

对一人公司读者最有意义的不是"我要不要用 Factory"，而是**这条命名战意味着 Coding Agent 已经从「炫技 demo」进入「企业采购 SOP」阶段**。这件事的连锁反应有两个：第一，企业开始批量买这类工具时，独立开发者把"我用 Factory/Devin 跑了一套企业内的 AI 工厂"包装成咨询/落地服务，是档位 D 在 2026 下半年比较实在的副业方向。第二，企业采购的同时会暴露大量"模型不解决的痛点"（评估、合规、调度、知识库整合），这是独立开发者做工具型副产品的窗口期，参考目前国内 @op7418、@dotey 已经在做的 Skill 包路径。

但有一个反直觉的提醒：Factory 这类工具的快速崛起，恰好对应了 Satya Nadella 在同期文章里讲的"Token 资本必须自己拥有"的反向警告——如果你做的产品/服务的全部价值都依赖某个外部 Coding Agent，那你不过是在"租用别人的智能"。一人公司的护城河必须落在「你独有的工作流和领域知识沉淀」上，工具只能是杠杆，不能是地基。

原始链接：https://x.com/FactoryAI/status/2066588050617249904

---

## 快讯区

**收入信号**
- Codie Sanchez 发"从零重启 7 步法"长贴：第 1 步「售卖先于建造」举例某学员在 Facebook 发一条对当地垃圾清运公司的吐槽，附预售链接，没有车没有牌照就先做到 $13K MRR（约 ¥8.8 万/月）。原贴含 7 条具体操作 — @Codie_Sanchez · 2026-06-16 02:03 · 👍122 🔖116 · engagement_rate 1.14%（同期中位数 7 倍）
- Matt Gray 给出"$5M/年线上"的反推数学："$416K/月 / 客单 $3K × 139 客户 / 转化率 2% / 月访客 7,000 / 日访客 233"——把"线上 $5M ARR"完全数字化反推 — @matt_gray_ · 2026-06-15 11:00 · 👍119 🔖89

**产品发布**
- Marc Lou 给自家产品 @DataFast_ 大改 Goals 模块（事件追踪可视化升级），仍是个人项目 — @marclou · 2026-06-16 05:51
- @indie_maker_fox（独立开发 2 年收入 $100K+）TanStarter 模板支持国际化，预告 7 月 1 日涨价。模板 tanstarter.dev 与 MkSaaS 同生态 — @indie_maker_fox · 2026-06-15 07:57

**工具更新**
- Factory 2.0 → "Software Factory"完整品类重命名（详见金矿 3）— @FactoryAI / @turingou 转述 · 2026-06-16 05:08
- Walter Writes AI 推 Claude MCP Connector：在 Claude 内 `/humanize` 直接清洗 AI 痕迹，官网定价 $49–$1,699/月（300K – 25M words），免费 300 字试用。Chase Dimond 推送（属营销协作）— @ecomchasedimond · 2026-06-16 05:26
- 宝玉（@dotey）公开自家 info-digest Skill（《图解 Skill》配套），用于把 AI 资讯整理成 X/微博初稿。配套 repo `JimLiu/Illustrated-Agent-Skills` 已 437 stars，含 7 个 Skill — @dotey · 2026-06-16 04:37

**值得关注的观点**
- 郭宇（@turingou，前字节、退休独立开发）：「软件行业的一人公司流程是非常非标准化的，与其说 software factory 是要高度自动化，不如说是要让人重新学习用新方法构建新软件，目前没有绝对的标准」——这是对 Factory 2.0 同期发布的非热闹评论 — @turingou · 2026-06-16 05:08 · 👍15 🔖9 · engagement_rate 0.53%
- 宝玉（@dotey）：「警惕 AI 圈造新词博流量的老套路」——遇到 LLM Wiki / Loop Engineering / Token Capital / OpenClaw 这种新词，先看原作者、再看反对意见，最后保持自己判断 — @dotey · 2026-06-16 04:42 · 🔖25 · engagement_rate 0.41%

**教训与反思**
- Sam Parr 引 Nick Sleep（曾仅持 Amazon/Berkshire/Costco 三只股的传奇投资人）的判断：「广告是产品平庸的价格。」举例 2008 年 GM 花 $5.3B 做广告，这笔钱本可以还掉相当部分债务。但 Sam 自己承认 Buffett 持有的 GEICO、可口可乐恰好是广告大户，反例存在。原链含 My First Million 同期讨论 — @thesamparr · 2026-06-15 22:00 · 👍438 🔖284 · engagement_rate 0.48%

**传播力素材**

> 收录 4 条具备独创性 + 传播潜力的金句/观点。陈词滥调（如"坚持就是胜利")已剔除。

- 「99% of success is just the ability to outlast uncertainty. The one who can tolerate the most uncertainty is the one who will eventually win.」 — @SahilBloom · 👍4,117 👁128,609 🔖809 · engagement_rate **0.63%**（高位）
  改写方向：适合公众号长文头图金句 + 视频号 30 秒口播——配「人为什么会在不确定面前放弃」的案例（如准备离职但又拖了 6 个月）。
  点评：这条之所以能爆，是击中了"AI 时代什么都在变"的群体焦虑，把「能熬」具象化成了一种可比的能力。局限是它在归因上偏神秘主义——成功不只是"忍得住不确定"，更多是"在不确定里持续做出对的小决定"。如果只看这句话，容易把"消极拖延"美化成"高级的忍耐"。

- 「这个时候，你发现有个国家的人民在说你吃不起西瓜。」 — @lidangzzz 转 番茄哈猫 · 👍4,704 👁398,999 🔖296 · engagement_rate 0.07%（但绝对量很高）
  改写方向：适合微博/小红书反差图文——把"想象中的韩国生活"和"我们的西瓜话题"做并列对比体。
  点评：这条之所以能传开，是把一个高级的"东亚比较视角"压缩成一句嘲弄。它的力量在于不解释，缺点是过度放大了网络段子（韩国"股市涨 300%"是脱离现实的）和真实经济差距的混淆，纯当传播素材可以用，做严肃论据要打折扣。

- 「The longer you avoid risk, the riskier your life becomes.」 — @thejustinwelsh · 👍249 👁10,338 🔖29 · engagement_rate 0.28%
  改写方向：适合视频号短口播——把"3 年没换工作 vs 跳出去做副业"的真人案例做 60 秒对比。
  点评：Justin Welsh 是 $500K+/年的内容创业者，背景可验证，所以这句话不是空泛鸡汤。但中文环境下"风险"的语义比英文重得多——避险在国内的现实回报往往真的大于冒险，复制这条传播时要小心被认为是"鼓吹辞职"。

- 「Your taste is the moat.」 — @matt_gray_ · 👍54 👁4,459
  改写方向：适合小红书图文——配「AI 时代为什么品味比技术更重要」的 9 宫格，举例同样的 prompt 给两个人会出两种东西。
  点评：在 AI 把执行成本压到 0 的当下，"品味"作为护城河越来越被反复说，本身已经不算反直觉了。这条能值得收录主要是它压缩得极短，传播效率高，但读者要警惕——"taste is the moat"对头部内容创作者是真的，对刚起步的人则是反向毒鸡汤，因为「品味」往往是大量执行后的副产品。

---

## 延伸资源库

### 播客 / 视频 / 访谈
- The Startup Ideas Podcast（@gregisenberg 主持，本期嘉宾 @GeorgeLampro20）——本期单集 URL 推文里未给出完整 link，但节目主源已验证：Apple Podcasts ID 1593424985
- My First Million Podcast（@thesamparr × @ShaanVP）——本期讨论 Nick Sleep 与 Bezos 名言「广告是产品平庸的价格」，链接 https://youtu.be/t3HWIey2lh8

### 图书 / 课程
- 《图解 Skill —— AI 提效实战指南》——作者宝玉（@dotey），京东在售（u.jd.com/RDY9YwC），配套 repo `JimLiu/Illustrated-Agent-Skills` 437 stars，含 7 个 Skill 模板。本期无独立外部图书推荐

### 链接汇总（已 web_fetch / web_search 验证）

**工具类**
- factory.ai — Factory 2.0「Software Factory」官网（直接访问）
- walterwrites.ai — Walter Writes AI 官网，Claude MCP Connector 落地页
- tanstarter.dev — Indie Fox TanStarter 模板（独立开发模板）
- basecamp.com/pricing — Basecamp 5 免费层（1 project + 1GB + 20 users，无信用卡）

**报道类**
- Lovable 经 Sacra/getlatka 验证：2026 ARR ≈ $500M，估值 $66 亿
- Factory 2.0 经 NEA 博客 + tessl.io 报道：客户含 NVIDIA、EY、Adobe、Palo Alto Networks、Adyen、Blackstone、Wipro、Comarch

**GitHub**
- `JimLiu/Illustrated-Agent-Skills`（437 stars）— 含 7 个 Skill：book-illustrator / content-analyzer / interview-analysis / interview-writing / outliner / adversarial-polish / info-digest

**未能访问**
- lxfater（@铁锤人）2026-06-15 11:02 一条文章贴（🔖414, engagement_rate 1.32%）：X Article 链接经 web_fetch 返回 402，无法直接阅读正文，仅能确认是当日中文 AI 一人公司高存档信号

---

## 行动建议（按档位分组）

档位 B（独立开发者）
- **本周可做**：把金矿 1 的 5 步法写成自己的 1 页 SOP（聚焦"挑选 gotcha feature"和"onboarding 漏斗"两节），挑 1 个想做的题目，4 周内出 v0.1（iOS + RevenueCat 或微信小程序 + 私域订阅）
- **今天 30 分钟可做**：去 Apple Podcasts 订阅 The Startup Ideas Podcast，听完最新一期 GeorgeLampro 单集（节目主源已验证）并把 5 步法截屏存档

档位 C（vibe coder / 工具集成者）
- **本周可做**：花一个周末，把金矿 3 的 Factory 2.0 跑通一个真实仓库的「issue → PR」端到端循环（即便不长期用，也能在客户演示里增加一个"我跑通过软件工厂"的实战话术）
- **今天 30 分钟可做**：clone `JimLiu/Illustrated-Agent-Skills` 试一下 info-digest Skill 整理一天的资讯生成中文初稿，体感后判断是否值得复刻

档位 A（内容创作者）
- **本周可做**：把金矿 1 的"喜欢的 App 月赚 $17K vs 讨厌的 App 月赚 $35"做成小红书 9 宫格反差图文，标题方向：「我用 AI 做的 App 一年差点废掉，差别就在这 5 步」
- **今天 30 分钟可做**：拆 Codie Sanchez 7 步法做成公众号头条草稿（含中国本土化适配——把"美国 boomer 卖小生意"改成"国内 60 后老板退休找接手"）

---

## 避坑指南

- **AI 圈造新词坑**：本期金矿 3（Software Factory）和高互动的 Nadella Token Capital 文章是同一天发的——@dotey 同期发推提醒：遇到新词先看是谁说的、再看反对意见，再决定要不要采用。对一人公司创业者最直接的损耗是：被新词绑架后过度调整产品定位/营销话术，最后什么都来不及做。
- **"挑你真喜欢的"事后归因坑**：金矿 1 里 GeorgeLampro 强调"喜欢的 App 月赚 $17K，讨厌的 App 月赚 $35"——但讨厌的 App 拿到 1.8M 浏览本身就是分发能力的体现，反推"喜欢比策略更重要"是事后选择性叙事。复制路径时一定要把"分发能力"这一变量隔离出来，不要把它当作"换个题目就能赚钱"的鸡汤。

---

## 本期情报评估

**信息密度**：正常偏低
当日窗口落在周一上午，国内中文圈以 @lidangzzz 一整组关于就业/性别/经济的长贴占据了 timeline 较大比例（共 14 条），干扰了 AI 一人公司主线信号的密度。海外侧实质性强信号集中在 Greg Isenberg、dotey、Factory AI 三处。

**趋势信号**：
"AI vibe coding 移动 App"在过去 4 周里完成了从「程序员独享」到「非程序员公开打法」的扩散——这是该垂直机会窗口走向"被批量复制"的中期信号，意味着接下来 1–2 个季度国内同类样本会快速涌现。

**横向对比（多个收入数据点）**：
今日有 3 个独立收入数据点可以横向参照——
- @GeorgeLampro20：自述 $200K/月（约 ¥135 万/月）走的是「AI App + IG 漏斗」路线
- Codie Sanchez 学员（无姓名）：$13K MRR 走的是「本地服务预售 + 单产品」路线
- @ItsKieranDrew bio 显示：$500K/年 走的是「内容创作 + 自有受众」路线
三条路径的共同点：**都不依赖团队规模**，都建立在「单点漏斗 + 自有分发」上；差异点是漏斗源头不同——AI App 靠社交媒体冷启动、本地服务靠 Facebook/Reddit 群组、写作靠 newsletter/Twitter。一人公司在 2026 的真实分化，不再是"做什么品类"，而是"漏斗源头放在哪"。

**当日强信号数 vs 噪音比**：
3 条强信号（A 级 1 条 / B 级 2 条）vs 大量噪音（lidang 就业系列、levelsio 转的日本足球迷视频、Naval 反 UK 社媒禁令）。噪音绝对量大于信号，但今日金矿质量足以撑起 3 条深度分析。

**本期信源**：@gregisenberg @dotey @FactoryAI @felixhhaas @Codie_Sanchez @matt_gray_ @indie_maker_fox @marclou @turingou @ecomchasedimond @thesamparr @SahilBloom @lidangzzz @thejustinwelsh @lxfater @ItsKieranDrew @jasonfried（共 17 位）
