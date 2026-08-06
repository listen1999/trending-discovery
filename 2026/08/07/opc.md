# AI 一人公司日报 | 2026-08-07

数据窗口：2026-08-06 06:00 — 2026-08-07 06:00（北京时间，过去 24 小时）
深度挖掘：3 条

---

## 今日头条

过去 24 小时至少四条独立信号指向同一件事：SKILL.md 正在变成 AI 时代的"技能打包"标准格式。@levelsio 转发朋友 @marckohlbrugge / @andreyazimov 的想法，把自己的创业书《MAKE》(readmake.com) 做成可加载进 Claude Code / Codex / Cursor 的 SKILL.md；产品经理 @vista8 开源了一个靠问答生成大学生求职简历的 Claude Skill（GitHub 47 star）；@xiaohua_888 开源了把公众号长文转成小红书图文的 Skill；营销顾问 @theandreboso 直接把"15 天营销冲刺"打包成付费 Skill 在 Gumroad 出售。这意味着知识和方法论正在从电子书、课程、模板，迁移成一种能被 AI 编程助手直接调用、复用、二次分发的新产品形态——对内容创作者是新的变现容器，对独立开发者和工具集成者是新的轻量分发方式。

---

## 今日金矿

### 金矿 1：Reclip.io — 一笔 1.3 倍营收成交的 AI 剪辑工具退出案例

来源：@marclou 转发 @trust_mrr 官方账号 · 2026-08-06 12:14（北京时间）· 👍129 👁16,668 · 收藏57
engagement_rate 0.34%，约为本期中位数（0.10%，基于本期 320 条推文计算）的 3 倍。

核心数据（已验证，据推文原文）
- 成交价：$30,000（约 ¥202,500，按 1 美元≈6.75 人民币，2026-08-06 汇率，来源 exchange-rates.org）
- 过去 30 天营收：$1,900（约 ¥12,825）
- 交易倍数：1.3x（$1.9K×12=$22.8K 年化营收，$30K÷$22.8K≈1.3 倍，与推文标注的 1.3x 吻合）
- 上架到成交耗时：121 天，为 TrustMRR 平台第 145 笔完成交易
- 卖家 @deivcodes，买家 @jianping_liu，经纪人为 TrustMRR 平台创始人 @marclou 本人

产品是什么（经 web_search / web_fetch 核实，来源 reclip.io 官网）：AI 短视频二创工具——自动从长视频里识别高光片段剪成短视频、AI 配音、去除视频内嵌字幕、按 TikTok/Instagram/YouTube 比例智能重构裁剪、AI 生成缩略图，定位是面向创作者的"一键出片"工具。定价层级未能完整核实——官网定价页返回 403 Forbidden，公开渠道仅确认存在 Starter/Pro/Creator 三档，具体金额 [未经验证]。

商业模式拆解
- 收入公式：月收入 $1.9K，若参考同赛道 SaaS 常见 $15-$49/月定价倒推，付费用户规模大致在 40-120 人区间 [未经验证，仅为区间推算]。
- 交易发生在 TrustMRR——marclou 本人用 ShipFast 搭建的"已验证收入 SaaS 交易市场"，通过 Stripe/RevenueCat 等支付渠道核实卖家真实流水，官网显示月访问量 20 万，在售项目估值倍数区间多在 1.9x-2.7x（据 trustmrr.com 官网信息，经 web_fetch 核实）。Reclip.io 这笔交易的 1.3x 明显低于平台均值，说明卖家更看重"尽快脱手"而非"卖出高价"，121 天的挂牌周期也印证了这不是一笔抢手交易。

复制路径
- 档位B（独立开发者）：AI 短视频剪辑是已被验证但玩家众多的红海赛道（Reclip.io、Eklipse、Opus Clip 等已是成熟竞品），新入局者靠"功能对齐"很难取胜，需要找更窄的切入点；如果目标是"做完就卖"，1.9x-2.7x 年化营收是这类工具型 SaaS 在 TrustMRR 上的合理估值锚点。
- 档位C（工具集成者）：这类"自动化剪辑管线"本质是把语音转写、镜头检测、字幕 API、渲染服务串起来的工作流，用 n8n/Make + 现成视觉/语音模型也能拼出雏形，建议先做垂直场景（比如播客切片）验证需求，而不是对标 Reclip.io 的全功能。

竞争格局：国内对应工具——剪映"图文成片/一键成片"、度加AI剪辑、腾讯智影，均为大厂免费或近乎免费提供，直接复制 Reclip.io 模式的独立收费产品在国内定价空间会被严重压缩，出海仍是更现实的路径。

成本与时间预期：需进一步调研（未查到 Reclip.io 具体运营成本或早期获客渠道的公开数据）。

深度综述：多数"一人公司"叙事强调"做到多少 MRR"，但这笔交易展示的是退出端的真实议价——1.3x 远低于平台常见的 1.9x-2.7x，说明"能退出"和"卖个好价钱"是两件事。一个月入 $1.9K 的工具型 SaaS，天花板往往卡在获客成本和产品同质化上：AI 视频剪辑的核心技术（转写、切片、裁剪）已被多个大厂和创业公司做成 commodity，护城河基本只剩"社区/工作流集成"，这也是为什么它更适合被小步快跑地"卖给下一个愿意接手的人"，而不是死磕到更大规模。这也是"传统一人公司叙事"（做产品→做增长→滚雪球）之外的另一条路径——"做产品→验证营收→打包卖掉→再做下一个"，更接近连续创业者的资产周转打法；marclou 本人既是这套打法的践行者（个人产品组合覆盖 $1K-$44K/月），又是这套打法的基础设施提供者（TrustMRR 本身）。但这类案例容易被过度浪漫化：121 天挂牌、1.3 倍营收的价格，换算下来卖家实际拿到的钱（$30K）已经接近继续运营 13 个月的收入总和（$1.9K×13≈$24.7K），"卖掉套现"未必比"继续运营"更划算，除非卖家有更紧迫的时间置换需求或想彻底退出这个赛道。

### 金矿 2：qiaomu-campus-resume — 用问答对话生成求职简历的 Claude Skill

来源：@vista8（向阳乔木，产品经理）· 2026-08-06 11:09（北京时间）· 👍130 👁11,881 · 收藏177
engagement_rate 1.49%，是本期中位数（0.10%）的近 15 倍，属本期 engagement_rate Top 10 信号。

发布/更新日期：2026-08-06（据推文发布时间）
国内可用：直接访问（GitHub、npm 在国内均可直接访问；需要能正常使用 Claude Code/Codex/Cursor 等编程助手账号）

核心功能（聚焦对一人公司的价值，据 GitHub README 经 web_fetch 核实）
- 一问一答式挖掘用户的实习/项目/校园经历，而非让用户自己填表；AI 给出判断后用户可直接修正
- 支持三种模式：从零生成简历、针对 JD 定向修改、优化已有简历排版
- 内置六种排版主题（ATS 经典版、极简版、瑞士风、科技风、校园清新版、紧凑版）
- 全程本地处理，不上传云端、不需要额外 API Key
- 简历优化逻辑参考了清华、MIT、伯克利等高校就业中心的公开实践（据推文原文，未逐项核实具体参考细则）

定价
- 免费层：完全开源，GitHub 仓库 47 star / 8 fork（经 web_fetch 核实于 2026-08-07）
- 付费层：无

10 分钟上手
1. 安装 Python 3、Chrome/Chromium/Edge 浏览器、Poppler 工具（用于生成 PDF）
2. 终端执行：`npx skills add joeseesun/qiaomu-campus-resume`（据推文原文）
3. 在 Claude Code / Codex / Cursor 中新建对话触发该 Skill，按 AI 提问逐一回答实习、项目、校园经历
4. 如需针对特定岗位优化，提供 JD 文本，让 Skill 做定向改写
5. 导出验证过的 PDF 简历，六种主题任选

与现有工具链配合：可以和公众号/知乎/小红书的求职经验内容打包成"简历诊断"服务，适合档位D（服务变现者）做低成本获客钩子；对独立开发者/工具集成者，理解它"单问单答挖掘信息"的交互设计比复用代码本身更值钱。

踩坑预警：需要本地安装 Poppler、Chrome 等依赖，非技术用户上手有门槛，不是纯网页工具；GitHub 仓库仅 8 个 fork、4 次 commit，属早期项目，稳定性和长期维护需观察。

竞品对比：国内同类工具（超级简历、五百丁、WonderCV 等）多是网页表单 + 模板库模式，付费拿 PDF；这个 Skill 的差异化在于"AI 访谈式"生成逻辑和本地免费开源，但没有网页版这么"傻瓜化"。

官方链接：https://github.com/joeseesun/qiaomu-campus-resume

深度综述：@vista8 本人是产品经理而非专业开发者，本期活跃度很高（12 条推文，本期第 7 活跃账号），此前也发过 DeepSeek V4 测评、豆包语音测试等内容，是"用 AI 工具做轻量产品"这条路线的典型践行者——这印证了 vibe coding 正在把"做一个能用的工具"的门槛降到产品经理甚至非技术人群可以独立完成的程度。这是本期至少 4 条独立信号中的一条，共同指向"SKILL.md/Claude Skill 正在成为新的轻量产品分发单元"（详见今日头条）：相比做一个完整 SaaS，"开源一个 Skill"的开发和分发成本都低一个数量级，不需要维护后端、不需要处理支付，直接靠 GitHub star 和转发获取关注。这类工具最大的价值也不是"帮大学生写简历"这个功能本身（市面同类工具已经很多），而是"单问单答、逐步修正"的信息收集设计模式——这个交互范式可以被复制到任何"帮用户整理内容"的场景，是比代码本身更值得学习复制的部分。风险在于：47 star、8 fork、4 次 commit 的早期项目距离"成熟可靠工具"还有距离，免费开源也意味着没有直接变现路径，更适合作为个人品牌/技术展示而非商业产品来看待。

### 金矿 3：bb — 会自己给自己写功能的开源 Agent 编排 IDE

来源：@bentossell 引用 @sawyerhood 原帖 · 2026-08-06 17:44（北京时间）· 👍183 👁64,203 · 收藏344
engagement_rate 0.54%，约为本期中位数（0.10%）的 5 倍。@sawyerhood 简介显示其为前 Figma/Facebook 软件工程师，@bentossell 简介自称"不会写代码但做产品/投资开发者工具"，两者背书都指向真实在用而非广告。

发布/更新日期：项目持续更新中，本期热度来自 sawyerhood 2026-08-06 的自然转发
国内可用：直接访问（GitHub、npm 均可直接访问；桌面端目前仅支持 macOS Apple Silicon，其他系统需通过 `npx bb-app@latest` 运行）

核心功能（聚焦对一人公司的价值，据 GitHub README 经 web_fetch 核实）
- 一个"会自己开发自己"的 Agent 编排 IDE：核心功能（跨模型工作流、提问工具、侧边对话、定时任务、内联预览、远程访问）都是用同一套扩展系统构建的
- 可以同时编排 Claude Code、Codex、Cursor 等多个编程 Agent 协同工作，并让它们反过来调用 bb 自己
- 桌面端 App、网页端、CLI、HTTP API 四种入口都是一等公民，任务以"线程"形式运行，可实时跟随、随时插手引导、或转手给另一个 Agent
- 开发者 Michael Yong（@_ymichael，新加坡人，常驻旧金山，前 Figma/Facebook 工程师）此前还做过 Terragon（Claude Code 后台 Agent 工具），是这条"Agent 编排/后台 Agent"路线的连续实践者（经 web_search 核实）

定价
- 免费层：完全开源，MIT 协议，GitHub 996 star（经 web_fetch 核实于 2026-08-07）
- 付费层：无独立收费，实际使用成本取决于用户已有的 Claude Code/Codex/Cursor 等底层 Agent 订阅（"on your own subscriptions"，据 GitHub README）

10 分钟上手
1. macOS Apple Silicon：直接下载桌面端 App
2. 其他系统/快速试用：终端执行 `npx bb-app@latest`（或 `npx bb-app@nightly` 尝鲜版）
3. 用已有的 Claude Code/Codex/Cursor 账号登录授权（复用已认证的 Provider CLI）
4. 新建线程，把任务拆给不同 Agent 并行跑，随时查看/插手

与现有工具链配合：对已经在用多个编程 Agent（比如同时开 Claude Code 和 Cursor）的独立开发者/工具集成者，bb 提供了一个"总调度台"，避免来回切换窗口手动同步上下文。

踩坑预警：项目自述"核心架构稳定，但工作流和界面仍在演进"，属早期阶段，生产环境使用需谨慎；桌面端目前只支持 macOS Apple Silicon，Windows/Linux 用户依赖 npx 运行的 CLI/网页端体验。

竞品对比：与 Windsurf 的 Cascade 多文件编排、Antigravity 2.0 的多 Agent + 内置浏览器路线是同类竞品，差异化在于完全开源、可自我扩展，且不绑定单一底层模型/IDE。

官方链接：https://github.com/ymichael/bb

深度综述：Michael Yong 除 bb 外还做过 Terragon（同样是 Claude Code 周边的后台 Agent 工具）以及一系列轻量游戏类小项目（Sheetdoku、Crosswordle 等）。这种"大厂履历 + 持续做小而美工具"的背景，和 marclou、levelsio 这类知名独立开发者的路径高度相似，说明"前大厂工程师转型做被验证需求的小工具"仍是当下最稳的独立开发路径之一。这也是"Agent 编排"这个细分方向进一步获得关注的信号——从早前"单个编程 Agent 能不能用"的阶段，走到现在"多个 Agent 怎么协同"的阶段，bb、Windsurf Cascade、Antigravity 2.0 是同一时间窗口内出现的不同解法，说明市场判断已从"选哪个 Agent"转向"怎么调度多个 Agent"。护城河目前更多在"开发者心智"而非技术壁垒——多 Agent 编排的核心技术（任务分发、上下文同步、人工介入点）门槛不算高，真正的壁垒是能不能持续吸引像 sawyerhood 这样的真实重度用户，形成口碑传播；这次信号本身就是一次自然的口碑放大，而非官方营销。对国内开发者而言，"复用已认证的 Provider CLI"意味着底层仍依赖 Claude Code/Codex/Cursor 等海外账号和订阅，bb 本身虽直接可用，但没有解决底层 Agent 在国内的可访问性问题（Claude Code 需要科学上网 + 海外支付方式）。

---

## 快讯区

**收入信号**
- @agazdecki（Acquire.com 创始人）转发案例称 IntentPost（实体信件 + AI B2B 获客工具）曾 6 周做到 $120K ARR 并被收购，创始人 Faiz Imran 此前已有 6 次退出经历 — 经 web_search 核实，该案例来自 Acquire.com 官方博客此前已发布的复盘文章（blog.acquire.com/a-startup-sale-built-on-demand-not-guesswork），今日属营销素材二次传播，非本期新交易 [可能与更早案例重叠]，故未列入金矿 — @agazdecki · 2026-08-06 21:49
- @agazdecki 发布 acquire.com 一则"年营收 $20M+"数字礼品卡 SaaS 挂牌信息（推文称 $21.9M TTM 营收，同时又标注 $30 万 ARR），两个数字量级明显不一致 [未经验证，疑为口径混用或笔误] — @agazdecki · 2026-08-07 04:49

**产品发布**
- @xiaohua_888（公众号"硅基思维"作者）开源了把公众号长文自动转换成小红书 3:4 图文（1242×1656px）的 Claude Skill，用于修复小红书官方"一键生图"功能会丢图的 bug，GitHub: lampooo/xhs-article-images-skill — @xiaohua_888 · 2026-08-06 11:41
- @theandreboso（marketer）把"15 天营销冲刺"打包成付费 Claude Skill 在 Gumroad 出售，教新手创始人一步步完成冷启动获客 — @theandreboso · 2026-08-06 17:26

**工具更新**
- @ecomchasedimond 推广 AI 邮件营销工具 getallanai.com，称其能为每个订阅者实时生成个性化邮件内容并做多变量测试；推文带明显推广口吻且在窗口内重复发布相同文案两次，未标注是否为赞助内容 [需审慎判断] — @ecomchasedimond · 2026-08-07 01:00 / 03:50
- @eyishazyer（西语 AI 资讯账号）转发 NotebookLM 的 7 个实用设置技巧 — @eyishazyer · 2026-08-06 21:20
- @vista8 分享用 `brew install --cask qlmarkdown` 让 Mac 访达空格键预览支持 Markdown 文件 — @vista8 · 2026-08-06 23:51
- @muratcan 分享提示词工程技巧："让模型 think hard" 比设置高推理档位更有效，附技术博客 — @muratcan · 2026-08-06 07:53
- @gregisenberg 发布 43 分钟营销 Agent 实操课视频，讲如何用 AI Agent 做营销并给出 2 个真实案例及工具清单 — @gregisenberg · 2026-08-06 20:45

**值得关注的观点**
- @MakadiaHarsh（AI 自动化系统开发者）拆解同样的自动化技能在"$2K 一次性项目"和"$5K 月度 retainer"两种定价下客户实际买的是什么——一次性交付 vs. 容错 + 人工审核 + 异常报警的持续服务，客户为"不用再操心"付费 — @MakadiaHarsh · 2026-08-07 05:38
- @matt_gray_（FounderOS 创始人）发布个人品牌入门指南短视频《How to win at personal branding》 — @matt_gray_ · 2026-08-06 11:10

**传播力素材**（适合自媒体改写的高互动观点）
- "Normal reward function: work hard → struggle → win in the end → get money and power → develop personality. Rich kid reward function: don't work at all... get money anyway... They essentially remain children forever!"（正常人的奖励函数：努力→挣扎→最终获胜→得到金钱和权力→形成人格；富家子弟的奖励函数：几乎不用努力→反正都能拿到钱→永远保持孩子的人格）— @levelsio · 👍1779 👁196,679 · engagement_rate 0.29%
  改写方向：适合公众号夹叙夹议长文——把"两种奖励函数"作为对比框架，延展到"财务自由后如何避免丧失驱动力"的自我提醒，适合创业者/自由职业者群体。
  点评：这条判断的杀伤力在于用"奖励函数"这个技术词汇重新包装了"寒门/富家子弟"的老话题，戳中独立开发者/创业者群体对"延迟满足驱动成长"的自我认同。局限是它把复杂的家庭结构问题简化成单一因果链，也忽略了"没有资源支持"同样可能扼杀试错空间这个反面情况——不是所有挣扎都通向成长。

- "How to build a network (non-cringe way): if you see something you like, tell the creator / if you think of someone, tell them / if you come across a helpful resource, share it with a friend / ask for feedback AND IMPLEMENT it / buy your friend's products / start a group chat with a shared goal / TLDR: to get a friend, be a friend"（非尬聊式人脉经营法：看到喜欢的东西就告诉创作者/想起某人就联系 TA/遇到有用资源就分享给朋友/寻求反馈并真的去落实/购买朋友的产品/发起一个有共同目标的群聊……总结：想交到朋友，先做朋友）— @Jayyanginspires · 👍344 👁18,184 · engagement_rate 1.58%
  改写方向：适合小红书清单体图文——拆成可执行的"人脉经营"动作清单，配合"社恐友好版人脉经营法"标题，适合内容创作者/服务变现者积累早期客户关系。
  点评：价值在于把抽象的"搞人脉"拆成具体、低压力的日常动作，符合独立创作者圈子里"弱关系变现"的实际打法。局限是这套方法建立在"本身已在持续产出内容/资源"的前提上，对完全没有内容积累的人，操作门槛被低估了。

---

## 延伸资源库

### 播客 / 视频 / 访谈
本期无完整播客/长音频访谈类内容。@gregisenberg 发布的 43 分钟 YouTube 营销 Agent 实操课因未进入金矿深挖，链接汇总于下方供参考。

### 图书 / 课程
本期无新发布图书/课程（@levelsio 提到的《MAKE》为此前已出版的旧作，本期新变化是给它加上 SKILL.md，相关信息见"今日头条"与"产品发布"）。

### 链接汇总（已 web_fetch / web_search 验证）
工具类：
- Reclip.io — https://www.reclip.io/
- TrustMRR — https://trustmrr.com/
- bb（Agent 编排 IDE）— https://github.com/ymichael/bb
- qiaomu-campus-resume（简历 Skill）— https://github.com/joeseesun/qiaomu-campus-resume
- xhs-article-images-skill（小红书图文 Skill）— https://github.com/lampooo/xhs-article-images-skill
- Skills CLI 注册中心 — https://www.skills.sh/agent/claude-code

报道类：
- Acquire.com 官方博客《IntentPost Acquisition Story: Demand Before Product》— https://blog.acquire.com/a-startup-sale-built-on-demand-not-guesswork/

视频类：
- @gregisenberg 营销 Agent 实操课 — https://youtube.com/watch?v=mD7JpNHLT70

---

## 行动建议（按档位分组）

档位A（内容创作者）
- 今天花 30 分钟安装 @xiaohua_888 开源的小红书图文 Skill（github.com/lampooo/xhs-article-images-skill），把最近一篇公众号长文转成图文测试效果，对比小红书官方"一键生图"功能。

档位B（独立开发者）
- 如果手上有一个月流水在 $1K-$5K 区间、增长停滞的小工具，去 TrustMRR（trustmrr.com）挂个价，用 Reclip.io 这笔 1.3x 成交的交易做心理锚点，判断"卖掉重新开始"是否比"死磕"更划算。

档位C（工具集成者）
- 本周完整跑一遍 vista8 的简历 Skill（`npx skills add joeseesun/qiaomu-campus-resume`），重点学习它"单问单答"的信息收集设计，这个交互模式比代码本身更值得复用到自己的场景里。

档位D（服务变现者）
- 参考 @MakadiaHarsh 的定价拆解，本周重新审视手上的一次性项目报价，尝试把其中一个转成"带容错/人工审核/异常报警"的月度 retainer 方案，用同样的技能收更高的价。

---

## 本期情报评估

**信息密度**：正常
本期 320 条推文的 engagement_rate 中位数约为 0.10%，略低于历史参考区间（0.15%-0.20%）；Timeline 明显被"华为舆论""Jeff Dean 离职 Google 创业""Meta 抓取风波"等非一人公司话题占据较大比例，纯 OPC 相关的强信号数量中等，够撑起 3 条金矿但不算爆发日。

**趋势信号**：
SKILL.md/Claude Skill 正在从单一工具的辅助功能，变成独立的轻量产品分发单元——今天至少 4 条独立信号（levelsio 的书、vista8 的简历工具、xiaohua_888 的图文工具、theandreboso 的付费营销 Skill）指向同一方向，值得在未来 1-2 周持续跟踪其变现效果是否能落地为真实收入，而不只是开源关注度。

**横向对比**：
本期两条尝试性的收入/交易数据点分别来自"资产交易"（Reclip.io，$30K 成交 / 1.3x 营收倍数，卖方视角）和"营销素材"（IntentPost，$120K ARR，经核实是旧案例二次传播）。前者更具参考价值，因为是真实、当天新公布的交易细节；后者的时间线经不起推敲，提醒读者对"创始人 6 周做到 XX 万 ARR"这类故事保持警惕，多查一层案例的原始发布时间。

**当日强信号数 vs 噪音比**：
3 条强信号（1 条 A 级收入/交易信号 + 2 条 B 级工具信号）进入金矿；快讯区收录约 10 条中等价值信号；被过滤掉的噪音（政治/影视宣传/纯励志金句/大厂高管人事变动等与一人公司无关内容）占比明显更高，320 条原始推文中进入分析范围的不足一成，属正常水平的信息密度。

**本期信源**：@marclou @vista8 @agazdecki @xiaohua_888 @theandreboso @levelsio @sawyerhood @bentossell @ecomchasedimond @MakadiaHarsh @Jayyanginspires @matt_gray_ @gregisenberg @muratcan @eyishazyer（共 15 位）
