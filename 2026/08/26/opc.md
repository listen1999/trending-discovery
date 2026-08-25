# AI 一人公司日报 | 2026-08-26

数据窗口：08-25 06:00 — 08-26 06:00（北京时间，过去 24 小时，共采集 359 条推文，79 位活跃发布账号）
深度挖掘：3 条

---

## 今日头条

今天最值得记住的不是某个新模型，而是一个正在成型的新变量："跑同一个任务，换个 agent 执行层，成本能差 75 倍"。@oran_ge 转发的 AgentSky.dev 发布贴给出对比：同一任务在 Claude Code 上花 $150，在 DeepSeek 新 agent harness 上只花 $2；同一天 @bentossell 也贴出 Factory Droid 与 Claude Code 跑同任务的成本/耗时对比（$1.60/8 分钟 vs $1.87/19 分钟）。两条独立信号指向同一个结论：agent 执行层（harness）本身正在变成一个可以被单独优化、单独套利的成本维度，而不是"选哪个大模型"这一个变量就能决定的。对每天在用 Claude Code / Codex / Cursor 干活的独立开发者和工具集成者来说，这意味着"多花的钱"里，有一部分可能只是没换 harness。

---

## 今日金矿

### 金矿 1：AgentSky — 一个 API 调用 Claude Code / Codex / DeepSeek / Kimi 等全部主流 agent

来源：@oran_ge（转推 @quxiaoyin 原贴）· 2026-08-25 10:39 · 👍1,260 👁2,128,963 🔖1,145

**发布/更新日期**：2026-08-25（Product Hunt 显示 8 月 3 日曾拿到 Day #1，本次为 X 上的正式发布贴，432 upvotes，经 web_search 交叉核实）
**国内可用：需要工具**（agentsky.dev 为新注册海外域名，未进入已知白名单，建议实测后再判断是否需要代理；其调用的 DeepSeek / Kimi / GLM 等国产模型本身国内可直连，但 Claude Code / Codex 等海外 agent harness 大概率仍需代理）

**核心功能（聚焦对一人公司的价值）**
- 一个 API 统一调用 Claude Code、Codex、Hermes、Pi、DeepSeek Harness、Opencode、Kimi Code、OpenClaw 等云端 agent；上层可选模型包括 Claude Opus/Sonnet/Fable 5 系列、Gemini、GPT-5.6 系列、DeepSeek V4、Kimi K3、GLM-5.3、Grok 4.6（经官网 web_fetch 核实）
- 自带 Agent Playground：接入真实工具（GitHub、Gmail 等），让多个 agent 在同一任务上并排跑，实时对比时间、成本、token 消耗
- 计费模型是"按 agent 运行时长 + 模型 token 用量"付费，不是按坐席收订阅费；如果本身已有 Claude Pro/Max 或 ChatGPT 订阅，可以在 AgentSky 里绑定，模型部分按官网说法可以做到"$0 model usage"（经官网 web_fetch 核实，具体绑定细则未验证）

**定价**
- 免费层：官网明确写"Pay only for what you use · No card required"，可直接进 Playground 试跑，未看到额度上限说明 [未经验证]
- 付费层：未查到公开费率表，按 agent 运行分钟数 + token 用量动态计费，具体单价需登录后台查看 [未经验证]

**10 分钟上手**
1. 打开 agentsky.dev，无需信用卡即可进入 Agent Playground
2. 选一个真实任务（比如给自己项目提一个具体 issue），分别用两个 harness（例如 Claude Code vs DeepSeek Harness）各跑一遍
3. 对比 Playground 给出的时间、成本、token 消耗，决定日常默认用哪个 harness、什么场景切换

**与现有工具链配合**：可以作为 Claude Code / Codex 的"云端跑腿"替代——不用在本地长时间挂机等 agent 跑完，也不用为了省钱单独去接 DeepSeek/Kimi 的 API 再自己写一套 harness 封装。

**踩坑预警 / 已知限制**：$150 vs $2 的对比来自作者一次性个人测试，任务内容、Claude Code 是否用了默认最贵模型等细节未公开，不能直接当作"DeepSeek harness 比 Claude Code 便宜 75 倍"的普遍结论；国内支付通道、能否用支付宝/微信绑定订阅未验证。

**竞品对比**：核心差异化不是"路由到哪个大模型"（这块 OpenRouter 已经做得很成熟），而是把 Claude Code、Codex 这类完整 agent 执行环境本身也做成了可切换、可对比的对象。经 web_search 未找到国内已有对标的"agent harness 聚合平台"，是否已有同类国内产品需要进一步调研。

官方链接：https://agentsky.dev/ ｜ Product Hunt：https://www.producthunt.com/products/agentsky

**深度综述**：这条信号有意思的地方不在 AgentSky 这个产品本身多惊艳，而在于它把"agent 执行层成本"这个此前没人单独拎出来看的变量摆到台面上。过去一年围绕"用 AI 写代码"的讨论基本都在比模型能力（谁的代码质量更高），很少有人系统性地比"同样能力水平下，跑一遍要花多少钱、多长时间"。今天同一批数据里恰好还有 @bentossell 贴出的 Factory Droid vs Claude Code 成本对比，两条互不相关的信号指向同一个新趋势：agent 编排/执行层正在从"模型的附属品"变成一个独立赛道，这是早期信号而非共识——AgentSky 上线不到一个月，432 个 Product Hunt upvote 在同类产品里不算爆款级别。对独立开发者和 vibe coder 来说，最大的意外是：你以为在为"AI 能力"付费，其实可能只是在为某个特定 harness 的默认配置付溢价。风险在于，$150 vs $2 这个数字本身经不起深究，任务复杂度、模型选择、上下文长度都能轻易让这个比例翻好几倍，读者不应该直接把这条信号当作"换个 harness 立省 98%"的操作指南，而应该当作"每个月花一小时给自己的常用任务做一次 harness 成本比价"的提醒。

---

### 金矿 2：Apodex 1.1 — 陈天桥出资、可执行代码做"可核查结论"的开源深度研究模型

来源：@vista8、@oran_ge、@lxfater（三位独立账号同日分别转发/评论，交叉印证）· 2026-08-25 09:47 - 17:41 · 三条合计 👍88 👁30,533

**发布/更新日期**：Apodex 1.1 于 2026-08-25 前后发布（官方博客 apodex.com/blog/apodex-1.1... 及 X 官方账号 @Apodex_AI 同步发布，经 web_search 核实）
**国内可用：需要工具**（apodex.ai / platform.apodex.ai 为新站点，未进入已知白名单，未实测国内直连情况，建议先用代理确认；开源模型权重和 FrontierAgent 代码托管在 GitHub / Hugging Face，均为国内可直接访问的平台）

**核心数据（已验证）**
- 创始人：Tianqiao Chen 陈天桥，Apodex 的 Founder / Chairman / CEO（经 LinkedIn 页面核实）。陈天桥此前已通过 Chen Institute 承诺投入 10 亿美元做"Discoverative Intelligence"脑科学+AI 研究、并被彭博社报道追加 20 亿美元投入 AI 研究（2026-03 报道，经 web_search 交叉核实，但该 20 亿美元投入是否全部/部分流向 Apodex 未获确证 [未经验证]）
- FrontierAgent（开源 agent 执行框架）GitHub star 539，Apache 2.0 协议，命令行 TUI，支持 ReAct 单 agent 模式和 Agent Team 多 agent协调模式（经 web_fetch 核实）
- 开源权重模型 Apodex-1.1-mini，35B 参数，可本地部署，官方宣称"在专业任务、金融研究、科研方向进入第一梯队"（据官方博客表述，未找到第三方独立跑分佐证 [未经验证]）

**商业模式拆解**
- 收入结构：网页版 Apodex 1.1（full model + Agent Team 协调能力）走 pay-as-you-go 的 credit 制，官网 pricing 页明确写"credit 消耗根据每次请求实际成本动态计算"，未公开具体单价表 [未经验证]；此前曾推出 Frontier Program，向科研机构/深科技创业公司提供每月 10 万美元 AI credit（经 web_search 核实，属于生态获客动作而非直接营收）
- 35B mini 模型完全开源免费，本质上是用陈天桥的资本把"能自己本地跑的深度研究模型"这条护城河先填平，网页版的 Agent Team 编排能力才是收费点

**复制路径（只写真正适用的档位）**
- 档位 C（工具集成者/vibe coder）：FrontierAgent 是 Apache 2.0 开源框架，可以直接 `git clone` 下来参考它的 Agent Team 协调实现（一个 coordinator 维护任务看板，拆给多个子 agent 并行做，最后汇总结论），拿来给自己做的"调研类""尽调类"小工具打地基，不用从零设计多 agent 协调逻辑
- 档位 D（服务变现者）：如果本身做金融尽调、科研数据整理、行业调研这类专业服务，可以把 Apodex 网页版当作"能读本地文件、能跑代码、结论可回溯核查"的深度研究工具试用，或者参考它"verified briefs（可核查简报）+ 逐句可溯源引用"的产品形态，用于设计自己的报告类交付物模板，提升客户对"AI 生成结论"的信任度

**竞争格局**：直接对标 OpenAI/Google/Perplexity 的 Deep Research 类功能，但 Apodex 强调"真的去跑代码分析原始文件"而非纯网页检索总结（据官网及推文描述）。中国资本主导、以开源模型+开源 agent 框架方式切入前沿深度研究赛道，目前国内还没有看到对等量级的同类产品，经 web_search 未找到直接对标项目。

**成本与时间预期**：网页版无公开定价基线，需登录后台查看；FrontierAgent 本地部署除 API/算力成本外无额外费用，35B 模型本地推理对硬件要求较高，具体部署成本需进一步调研。

**[关键约束]**：这条信号的可信度建立在陈天桥本人资金实力（公开报道过 10-20 亿美元级别的 AI 投入）和多位独立中国 AI 从业者（@vista8、@oran_ge、@lxfater）同日各自转发验证之上，不是靠单一账号的自嗨传播。但对绝大多数一人公司读者来说，这更像是一件"可以白嫖的重资本基建"，而不是一条可以直接复刻的商业模式——普通开发者复刻不了陈天桥的资金体量，能复刻的只是"把 FrontierAgent 的多 agent 协调思路搬进自己的小工具"这一层。

**深度综述**：这条信号最大的信息量在"谁在做"而不是"做了什么"——中国互联网上一代造富者（盛大网络创始人）正在把真金白银砸向前沿开源 AI 研究基础设施，而且选择了"开源模型 + 开源框架 + 付费网页版"这个此前更多由硅谷实验室在玩的打法，这本身是一个值得关注的早期信号：中国资本进入"给全球开发者用的开源 agent 基建"这个赛道，而不是像过去几年更常见的"做一个对标 ChatGPT 的产品"。反直觉的地方在于，Apodex 选的切入点不是 C 端聊天产品，而是"金融尽调、蛋白质对接、临床数据生存分析"这类偏专业、偏 B 端重度研究场景——这和大部分一人公司读者的日常需求（写公众号、做小程序、接私活）距离较远，属于早期信号，还看不出对独立开发者的直接商业机会，更多是"值得关注但暂时用不上"的一类信息，风险在于容易被"陈天桥"这个大名头带偏预期，误以为很快会有平价的一人公司复刻路径，目前看不到这样的迹象。

---

### 金矿 3：marketingskills — 45.6K star 的开源营销技能包，一句话生成 SEO 审计/转化率优化/冷启动邮件

来源：@indie_maker_fox · 2026-08-25 08:00（原贴）/ 14:01（转发放量）· 👍29 👁2,548 🔖50（engagement_rate 1.96%，同期中位数约 0.15%-0.2%，属高收藏率信号）

**发布/更新日期**：项目持续更新中，本次为 indie_maker_fox 在 24 小时内两次分享（原贴+转发），非当天首发但为当天新增信号（经 web_fetch 核实项目仍在活跃维护）
**国内可用：直接访问**（GitHub 属已知白名单内可直连平台）

**核心功能（聚焦对一人公司的价值）**
- 60+ 个营销技能，覆盖转化率优化（CRO）、内容与文案、SEO 与站内发现、付费投放与分发、数据度量与测试、留存、增长工程、策略与变现、销售与 RevOps 九大类（经 web_fetch README 核实）
- 遵循 Agent Skills 规范，可被 Claude Code、OpenAI Codex、Cursor、Windsurf 等支持该规范的 agent 直接调用，用自然语言下指令即可，比如"帮我的网站做个 SEO 审计""帮我设计 5 封欢迎邮件"
- 作者 Corey Haines 本人经营 Conversion Factory（转化率优化代理机构），marketingskills 相当于把他自己的顾问方法论开源打包成可执行技能

**定价**
- 免费层：完全免费，MIT 协议，"Use these however you want"（经 web_fetch 核实）
- 付费层：无。作者的付费产品是另外的 Swipe Files 内容订阅、AI Marketing Training 课程、以及 Magister（自主 AI Agent CMO 工具），marketingskills 本身不收费

**10 分钟上手**
1. 在项目目录执行 `npx skills add coreyhaines31/marketingskills`（也可用 Claude Code Plugin marketplace 一键安装）
2. 在 Claude Code / Codex 里直接用自然语言调用，比如"用 /cro 审查我的落地页"
3. 挑一个真实页面（自己产品或客户的）跑一次，人工复核输出结果再采用

**与现有工具链配合**：可以直接嵌入日常在用的 Claude Code / Codex 工作流，作为营销侧的技能补充，不需要额外开一个营销顾问工具的订阅。

**踩坑预警 / 已知限制**：技能包本质是 Prompt + 流程模板，效果高度依赖底层大模型能力，不能指望"一句话产出可以直接上线的 SEO 审计"，仍需人工复核；内容和案例基于英文语境积累，国内百度 SEO 规则、私域打法等本土实操细节大概率需要自己改写补充。

**竞品对比**：同类还有 mysticaltech 基于此项目的 fork（打包了预构建 .skill 文件方便安装），核心功能高度重合，选哪个更多取决于安装偏好而非能力差异（经 web_search 核实存在该 fork）。

官方链接：https://github.com/coreyhaines31/marketingskills

**深度综述**：这条信号的价值不在技能包写得多好，而在于它验证了一个正在发生的替代关系——过去要花钱订阅的"营销顾问模板""付费 SEO 审计工具"，正在被"开源 + agent 调用"的组合免费替代掉一部分。Corey Haines 的商业逻辑很清楚：marketingskills 是引流层，免费、开源、star 数够高就能在 GitHub 上持续曝光；往下一层是 Swipe Files 内容和 AI Marketing Training 课程，再往下是 Magister 这个付费 SaaS 产品——一条从免费工具到内容到课程再到软件的变现链路，是内容创作者和服务变现者都可以直接抄的结构，而不只是抄这个技能包本身。反直觉的地方在于：45.6K star 意味着这套东西已经被验证足够好用，但它同时也在压缩"卖营销方法论"这门生意的定价空间——如果读者的服务里有一部分就是"帮客户做次 SEO 审计"，现在客户自己花十分钟装个技能包也能做到七八成，真正能收费的部分正在往"人工判断、行业经验、执行落地"这些技能包做不了的环节收缩。这对档位 D 的服务变现者是一个需要认真对待的信号，而不只是一个"薅羊毛"的工具推荐。

---

## 快讯区

**收入信号**
- Acquire.com 挂牌一个 SaaS：$27K 上月收入 / $298K TTM 营收 / $241K TTM 利润 / $298K ARR（约合 ¥18.3万 / ¥202.3万 / ¥163.6万，按 1 美元≈6.79 元人民币换算；数据来自挂牌页面自述，非独立审计）— @agazdecki · 2026-08-25 09:19
- 几个"出价竞拍类"网站的"经验证收入"排行：第一 $5.2K（2.1万访客）、第二 $1.7K（1800访客）、第三 $1.6K（4600访客），另有 $1K、$842 两条 — @marclou · 2026-08-25 15:11 [未独立核实"verified"依据]

**产品发布**
- OpenStory：开源 AI 视频制作平台，输入剧本自动拆分场景、生成统一风格画面、转成动态视频并配音，主打解决"AI 视频里每个镜头像不同作品"的一致性问题；GitHub 432 star，MIT 协议，TanStack Start 技术栈，需自备 Fal.ai 和 OpenRouter 的 API Key（经 web_fetch 核实）— @indie_maker_fox · 2026-08-25 11:30
- MkAgent：可交互的项目架构图生成工具，分析代码后生成可点击查看节点详情的动态 HTML 架构图 — @indie_maker_fox · 2026-08-25 17:40 [未做进一步核实]
- Anthropic 发布《AI 原生 SDLC 实施指南》，原文于 2026-08-21 发布在 claude.com/blog，按 Plan/Design/Build/Test/Deploy/Maintain 六阶段讲解如何把 Agent 接入软件开发全流程，来自 Anthropic Applied AI 团队实践（经 web_search 核实，[可能与上期重叠]）— @xiaohu 转发扩散 · 2026-08-25 13:48
- Netlify 与 OpenAI 联合发起 WebMCP Challenge，鼓励开发者构建 agent-native 网页应用，提供 300 万 Netlify 积分和 5000 美元奖金池（约 ¥3.4 万）— @thisiskp_ · 2026-08-26 04:46

**工具更新**
- marclou 给自己的 TrustMRR 加了 Whoop 集成，在创始人主页展示睡眠/恢复/消耗数据，用来观察睡眠运动习惯与营收的关系（功能还在审核中）— @marclou · 2026-08-26 05:51
- damonchen 公开自己的"xAI 技术栈"月度成本：Cursor Ultra $200 + X Premium+ $40，合计 $240/月（约 ¥1,630/月），Grok Bot 和 Grok 均靠前两者订阅覆盖不再单独付费 — @damonchen · 2026-08-25 11:45
- indie_maker_fox 分享用 Matt Pocock 开源的 skills 库（github.com/mattpocock/skills）驱动 Codex 长时间稳定跑项目的实操经验：先用 wayfinder / grill-with-docs 对齐需求，再 to-spec / to-tickets 拆票，最后进入 implement（带 TDD + code review），自述已完整跑完 2 个项目 — @indie_maker_fox · 2026-08-25 09:01 [经 web_search 核实 skills 库确为 Matt Pocock 本人维护]

**值得关注的观点**（仅收录已验证 solopreneur 的判断）
- @levelsio："App 数量比以往任何时候都多，但成交比以往任何时候都少"——他同时转发的数据显示：美国 App Store 收入历史上首次下降（含游戏），非游戏类应用仍同比增长 14.6%，游戏下降 4.5%；RevenueCat 上 web 端收入份额一年内从 20% 涨到 26%，"app2web"正在发生 — @levelsio · 2026-08-26 00:45 [数据引自推文本身，未独立核实 RevenueCat 原始报告]

**教训与反思**
- @AndrewWriteCopy 自述文案代写生涯真实时间线：2009 年 7 月开始接活，直到 2010 年 3 月才拿到第一个客户，首单一周只赚 $100（约 ¥679），花了"好几年"才做到年入六位数（后来七位数），提醒读者"文案代写不是快钱" — 2026-08-26 01:00

**传播力素材**（适合自媒体改写的高互动观点）

- "30 min book reading every day (15 yrs) / 45 min workout (12 yrs) / 30 min meditation (7 yrs) / 60 min tennis (6 yrs) / 1 IG reel every day (4 yrs) / 1 youtube shorts every day (4 yrs) / 2 youtube long form videos every week (6 yrs)... consistency" — @warikoo · 👍1,041 👁128,524 · engagement_rate 0.81%
  改写方向：适合小红书/视频号做"自媒体人的作息表"图文——把这份长达十几项、跨度最长 15 年的习惯清单做成一张信息图，配文"普通人坚持不到一年，他坚持了十五年"。
  点评：这条能火是因为它用具体年限（而非"坚持很重要"这种空话）把"长期主义"落到了可信的细节上，尤其最后几项直接对应内容创作的日更节奏，对内容创作者有直接借鉴意义。局限是读者容易只看到"结果"而忽略这份清单背后大概率有团队/助理支持，个人照搬全部 13 项的执行难度会被严重低估。

- "No one is doing as well as you think they are. But you're not doing as well as they think you are. So, you're doing better than you think but worse than they think." — @AlexHormozi · 👍3,177 👁471,657 · engagement_rate 0.67%
  改写方向：适合公众号做"创业焦虑"选题的开头引语，用三段式认知对比引出"停止和别人的滤镜比较"的论述。
  点评：这句话的传播力来自它精巧的逻辑对仗结构，直接命中创业者/自媒体人普遍存在的"社交媒体比较焦虑"。局限是它是纯观点句，没有给出任何可执行的应对方法，改写时需要自己补充"怎么办"的部分才有实用价值，否则容易停留在"说得对但然后呢"的层面。

- "Precedent-setting moment in news media. The editor of the second most important opinion page in the country greenlights the use of AI for drafting pieces, no disclosure necessary." — @david_perell · 👍709 👁709,169 · engagement_rate 0.1%
  改写方向：适合公众号做"AI 写作是否要标注"的媒体伦理讨论选题，可以延伸到国内自媒体/公众号是否该标注 AI 辅助写作。
  点评：这条抓住了内容创作者普遍关心但没有定论的问题——AI 辅助创作要不要透明披露。价值在于给出了一个具体的行业先例作为讨论支点，而不是空谈立场；局限是原文没有点名具体是哪家媒体、哪位编辑，可信度依赖 david_perell 本人信誉，缺乏可独立核实的信源，改写时应注明"据传"而非当作确凿事实转述。

- "A founder pulling $250k a month in profit, investing $150k of it: 10 years at a boring 10% and the portfolio approaches $30M while the business keeps running. The business is the engine. The portfolio is the flywheel. You are the fuel." — @matt_gray_ · 👍346 👁51,642 · engagement_rate 0.67%
  改写方向：适合小红书/公众号做"利润再投资"选题，用具体数字（月利润25万美元、投资15万美元、10年后$30M）做一张复利增长信息图。
  点评：三句话把"业务造血—利润再投资—复利增长"的逻辑讲清楚，数字具体、逻辑闭环，容易被服务变现者和独立开发者当作长期目标参照。局限是这是一个理想化的假设案例（10年稳定10%年化收益是理想模型，非真实追踪案例），并非某个真实创始人的可核实经历，读者不应把"10年$30M"当作确定性结论。

---

## 延伸资源库

### 播客 / 视频 / 访谈
本期无播客 / 视频内容进入深度分析（Codie_Sanchez 与 David Adelman 的访谈、Nathan Barry 与 Ben Greenfield 的访谈片段互动数据一般且缺乏具体时间戳/节目详情，未纳入）。

### 图书 / 课程
本期无。

### 链接汇总（已 web_fetch / web_search 验证）

**工具类**
- AgentSky：https://agentsky.dev/
- Apodex：https://www.apodex.ai/ ｜ FrontierAgent（开源框架）：https://github.com/ApodexAI/FrontierAgent
- marketingskills：https://github.com/coreyhaines31/marketingskills
- OpenStory：https://github.com/openstory-so/openstory
- Matt Pocock skills：https://github.com/mattpocock/skills

**报道类**
- AgentSky Product Hunt 页：https://www.producthunt.com/products/agentsky
- 陈天桥 20 亿美元 AI 投入报道（Bloomberg，2026-03）：https://www.bloomberg.com/news/features/2026-03-05/chinese-gaming-tycoon-chen-invests-2-billion-to-build-ai-smarter-than-humans
- Anthropic《AI 原生 SDLC 实施指南》：https://claude.com/blog/the-ai-native-sdlc-playbook

**GitHub**
- coreyhaines31/marketingskills（45.6K★，MIT）
- ApodexAI/FrontierAgent（539★，Apache 2.0）
- openstory-so/openstory（432★，MIT）
- mattpocock/skills

---

## 行动建议

档位 B（独立开发者）
- 今天 30 分钟内，挑一个自己正在用 Claude Code / Codex 跑的真实任务，在 AgentSky Playground（或手动切换到 DeepSeek/Kimi 等国产 harness）跑一遍，记录时间、成本、结果质量差异，建立自己的 agent 选型参考表，不要直接相信"75 倍"这个数字，自己测一遍再说。

档位 C（工具集成者 / vibe coder）
- 本周花 1 小时，用 `npx skills add coreyhaines31/marketingskills` 在 Claude Code 里装上营销技能包，挑一个真实项目的落地页跑一次 SEO 审计和转化率优化建议，评估这套流程能不能塞进现有客户交付流程里。

档位 D（服务变现者）
- 参考 Corey Haines"开源工具引流 + 内容 + 课程 + SaaS"的四级火箭结构，把自己最擅长的一项专业判断（哪怕只是一份 checklist）开源或免费放出来，测试是否能带来咨询/服务询盘，而不是一上来就想收费。

档位 A（内容创作者）
- 本周用 marketingskills 技能包给自己的公众号/小红书主页做一次转化率审查（优化置顶内容和简介 CTA），不需要额外营销预算，验证 AI 生成建议是否可用后再决定要不要采纳。

---

## 避坑指南

- 想靠文案/写作代写快速变现：@AndrewWriteCopy 的真实时间线是接活到第一个客户花了 8 个月，首单一周只赚 $100，从入行到年入六位数花了"好几年"。如果看到"AI + 文案"速成变现的宣传话术，可以用这条真实经历做校准，警惕对起步速度和早期收入的过高预期。
- AgentSky 的 "$150 vs $2" 对比来自作者一次性个人测试，任务细节、模型配置均未公开，不宜直接当作"换 harness 能省 98% 成本"的确定性结论去做预算决策，建议自己用真实任务测一遍再下判断。

---

## 本期情报评估

**信息密度**：正常。本期没有出现 A 级的个人收入实锤数据（MRR/ARR + 产品名 + 具体时间点的组合），但 3 条金矿信号均为 B 级工具/项目发布，且都经过独立 web_search / web_fetch 交叉验证，质量扎实，不是靠数量凑出来的一期。

**趋势信号**：agent 执行成本正在从"选哪个大模型"这一单一变量，分化出"选哪个执行/编排层（harness）"这个新的独立可套利维度（AgentSky + Factory Droid/Claude Code 对比数据互相印证）；与此同时，中国资本（陈天桥）开始在前沿开源 AI 研究基建上投入真金白银，用"开源模型 + 开源框架 + 付费网页版"的打法切入原本由硅谷主导的深度研究 Agent 赛道。

**横向对比**：今天三条金矿分别代表三种完全不同的"开源逻辑"——AgentSky 靠"基础设施套利"帮用户省执行成本；marketingskills 靠"知识开源化"把顾问方法论打包成免费技能包再倒流转化；Apodex 靠"重资本砸出来的能力开源"用 35B 模型开源建立生态、网页版收费。三条路径对应的读者档位也基本不重叠（B/C 档、A/D 档、C/D 档中偏专业服务的一小部分），可以按自己所在赛道对号入座，不必三条都追。

**当日强信号数 vs 噪音比**：3 条金矿信号（均为 B 级，经验证）/ 全天 359 条推文中大量为无关政治评论、生活方式金句、与 AI 一人公司无主题关联的内容——大盘噪音占比高，属正常水平，未见明显的话题刷屏挤占信号空间的情况。

**本期信源**：@oran_ge @vista8 @lxfater @indie_maker_fox @xiaohu @agazdecki @marclou @damonchen @bentossell @levelsio @AndrewWriteCopy @matt_gray_ @warikoo @AlexHormozi @david_perell（共 15 位）
