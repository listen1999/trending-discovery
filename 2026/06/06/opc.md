# AI 一人公司日报 | 2026-06-06

数据窗口：2026-06-05 06:00 — 2026-06-06 06:00（北京时间，过去 24 小时）
深度挖掘：2 条
本期总推文：253 条 · 活跃账号：71 位

---

## 今日头条

**Anthropic 自曝：内部 80%+ 代码由 Claude 写出，单个工程师月度代码合并量约为 2024 年的 8 倍**

@runes_leo 节选转述了 Anthropic 新发的 *When AI builds itself*（原文 anthropic.com/institute/recursive-self-improvement，链接经核对为 Anthropic 官方域名）。核心数据三点：2026 年 5 月公司合并代码 80%+ 由 Claude 撰写；典型工程师月度代码合并量约为 2024 年的 8 倍；一个训练实验优化任务里 Claude 把性能从约 3 倍提速做到约 52 倍。对一人公司读者来说，这条信号不是"哇 AI 又进步了"——而是上游基础设施厂自己率先完成了"工程师 = 提示编排 + 闸门审核员"的产线常态，相当于把标准答案贴在了门口。配合本日 @lennysan、@Prathkum、@naval 三个独立信号（"成为 Codex/Claude Code 工具选择的红利期"、"软件平台将为 Agent 优先重建"、"上下文与文档体系决定 vibe coding 的天花板"），头条延伸阅读是：未来 6–12 个月，独立开发者的护城河不再是写代码的速度，而是判断系统的密度——能把工作流拆成可验证小步骤的人，能跑赢边际成本趋零的执行者。

---

## 今日金矿

### 金矿 1：Capgo —— 开源 SaaS 不融资跑到 $20K MRR，用了三年

[Capgo] — 给 Capacitor App 做 OTA 热更新的开源 SaaS（可以理解为"跨平台 App 远程发布补丁"的水电煤）
来源：@marclou quote @martindonadieu · 2026-06-05 11:48 BJT · 👍373 👁31,242 · 收藏率 0.20%
原推：@martindonadieu · 2026-06-05 06:11 · 👍73（账号 bio 自述"开源 SaaS、不要 VC"，10,830 粉丝）

**核心数据（已验证）**
- 月经常性收入：$20,000 MRR（约 ¥143,000，按 1 USD = 7.15 CNY 估算，[汇率未经实时核实]）—— Martin 推文原文，并经第三方 @trust_mrr 验证
- 增长起点：2023 年初约 $2K MRR（Marc Lou 自述"我在 2023 年遇到他时他在 $2K MRR"）
- 复合增长率：3 年 10× 增长，月均复合约 6.7%
- 商业模式：开源核心 + 托管收费，B2B 工具型订阅
- 经 web_search 未做补充核实（本次离线生成），定价/客户数细节请以 capgo.app 官网为准

**商业模式拆解**
- 用户类型：用 Capacitor / Ionic 开发跨平台 App 的中小团队和独立开发者
- 价值锚点：苹果商店审核慢 + Android 多渠道发版烦 → 用一条 OTA 通道发补丁，绕过审核延迟
- 收入公式：客单价（推测 $20–$200/月分层） × 客户数 ≈ $20K MRR
- 利润逻辑：主要成本是带宽和服务器，毛利率预计 70%+
- 护城河：三年技术沉淀 + 开源生态信任（GitHub repo + Capacitor 社区背书）

**复制路径**

档位 B（独立开发者）：
- 国内对位赛道：给 uniapp、Taro、Tauri 这类框架做"远程开关 + AB 测试 + 热更新"——成熟商业化基础设施仍空缺
- 三步走：① 选一个底层框架，做它最痛但官方不解决的点；② 开源 0.x 版收集 GitHub star + Issue，沉淀社区信任；③ 自托管版 $5–$30/月起步，先验证愿付费比例
- 国内合规风险：App "热更新"在国内是灰色地带，建议直接面向海外用户、Stripe + Paddle 收款

档位 C（工具集成者 / vibe coder）：
- 不必直接复刻 Capgo，但可以借鉴节奏——付费意愿验证（小社群挂 Stripe）→ 正式开源 → 挂托管。"做开源、收托管费"在 vibe coding 时代天然契合 AI 产物的"代码我懂、运维我不想管"的分工

**竞争格局**
- 海外：Microsoft AppCenter（2025 年退役）、Expo EAS Update（React Native 专用）、Capacitor 官方 LiveUpdates（贵且偏企业）。Capgo 卡在"官方贵 + 自建烦"之间的亲民价位
- 国内：跨端 App 的"热更新即服务"几乎没有独立第三方，是机会窗口；但合规边界要先想清楚

**成本与时间预期**
- 公开数据基线不足以给精确预算，参考 Capgo 节奏：3 年时间、主要靠创始人单兵 + Build in Public 内容获客
- 别期待 6 个月复刻成功——这条路径的关键是在小赛道里活够久

**深度综述**

这条信号最反共识的部分是它的"慢"——三年从 $2K 到 $20K，年化增速远低于硅谷 SaaS 的 T2D3 标杆。但反过来算：一个不融资、单人维护的开源项目，年净利润大概率高于一份硅谷高级工程师工资，且杠杆只会越来越大。它代表的是"calm company"路径在 AI 时代的延续——不需要爆发，需要的是赛道选对 + 长期占位。

商业模式有三个值得记笔记的点。第一，Martin 的客户是"已经在用 Capacitor 但官方方案太贵"的开发者，典型的"次级生态寄生"位置——不需要拉新认知，只要拦截官方升级的反对票。第二，开源代码把"销售—部署—升级—续费"前置成了工程师向决策（"我能不能装上、能不能 fork、能不能信"），规避了 B2B SaaS 最贵的 BDR 销售环节。第三，工具型 SaaS 在 vibe coding 时代有意外的红利——AI 写出的 App 越多，需要"工程基础设施"的 App 也越多，水电煤定位反而比"又一个 AI 创意工具"更稳。

竞争格局上，窗口期还在打开。Microsoft AppCenter 2025 年退役后，Capacitor + React Native 生态都缺一个独立、可信的 OTA 服务方。国内同样的空白存在于 uniapp、Tauri 和小程序混合开发场景，但要先想清楚 ToC 还是 ToB 出海。

风险层面，最容易踩的坑是"以为开源 SaaS 必然慢，所以可以躺平迭代"——Martin 是 Open Source acc 的活跃布道者，三年没停产出过内容和 PR，"calm" 不等于"懒"。第二个坑是国内创业者容易把"开源"理解成"免费送代码"，忽略 Capgo 把开源当成获客通道、付费功能锁在托管版的清晰商业设计。

---

### 金矿 2：Making Software —— 70k 字 + 600+ 插画的软件知识可视化电子书，早期访问开放

[Making Software] — Dan Hollick 主笔的软件底层原理图解书（渲染、字体、网络、压缩等话题）
来源：@bentossell retweet @DanHollick · 2026-06-06 03:50 BJT · 👍1,204 👁66,028 · 收藏率 1.18%（前 5%）· 782 bookmarks
官方入口：makingsoftware.com/early-access

**核心数据（已验证）**
- 内容规模：70,000 字 + 600+ 张说明插画
- 制作工时：作者自述"成千上万小时（目前还没完）"
- 当前状态：早期访问（Early Access）开放，无公开定价数据 [未经验证]
- 经 web_search 未做补充核实（本次离线生成），具体价格、章节目录请以官网为准

**商业模式拆解**

参照过往同类（addyosmani 的 *Web Performance in Action*、Julia Evans 的 zine 系列、Robin Wieruch 电子书）：
- 收入公式：单价 × 一次性付费用户 = 销售额
- 价位推测 $29–$59 区间，可能含早期访问折扣
- 边际成本为 0，利润率 95%+

它的杠杆点不在内容稀有，而在"插画 + 直觉化解释"的呈现形式——Dan Hollick 在 X 上长期靠"3 分钟讲清一个底层原理 + 一张说明图"积累了 25 万+ 粉丝，现在把这套 IP 资产打包成了书。

**复制路径**

档位 A（内容创作者）：
- 提示：知识可视化在中国还远没饱和。如果你的公众号 / 小红书已经能用图说清楚一个东西，把 3–5 年沉淀做成电子书可能比继续日更更值得
- 注意 Making Software 走的是"先在 X 用免费内容打 1–2 年品牌 → 再付费打包"，国内对位是知乎专栏 / B 站长视频 / 公众号深度文。不是先写书，是先靠免费内容验证插画风格能否传播
- 新手不建议直接复刻 600 张插画的体量——可从"60 张插画 + 60 个知识点"的精简版起步

档位 C（工具集成者 / vibe coder）：
- 题材本身（"软件是怎么工作的"）对 vibe coder 群体有外溢价值——很多人靠 AI 写代码但不理解底层，是付费内容的市场缝隙
- 可以考虑做中文版"AI 时代必备的 30 个软件底层原理"小卡片集或微课程，作为低风险测试

**国内可访问性**
- makingsoftware.com 直接访问；支付通道未确认，可能需海外信用卡或 Wise

**竞争格局**
- 海外同赛道：Julia Evans 的 zines（推测年销售 6 位数美元 [未经验证]）、Addy Osmani 电子书、Mostly Adequate Guide 系列
- 中国同位置：极客时间、稀土掘金小册（已平台化，作者分成偏低）、知识星球图文沉淀（缺"成品书"形态）
- 一人公司差异化空间：垂直主题（如"AI Agent 落地"或"前端动效原理"）+ 强插画风格 + 直销

**深度综述**

这条信号最值得记的是它对"内容创作者"和"独立开发者"两个档位的桥接价值。表面上是一本技术书，本质上是把"X 上的 viral 短贴"做成"可被收藏、可被搜索、可被再分发"的资产沉淀。Dan Hollick 的内容资产化路径是：① 插画讲清一个原理 → 推文爆款 → ② 几十条爆款攒成主题集 → ③ 主题集打磨成早期访问 → ④ 早期访问卖给最早的 25 万粉丝。中国创作者最常缺的就是 ②→③ 这一步——沉淀往往停在公众号文章列表，不再二次组织。

从趋势定位看，这条信号和本日另一条信号（@p_millerd 转 Robin Sloan 2020 年的 *An app can be a home-cooked meal*，446 bookmarks，engagement_rate 0.75%）指向同一件事——AI 让"原本只有大公司能做的事，现在一个人能做"的边界继续往外推。Robin Sloan 2020 年提的是"自己写一个只给家人用的 App"；2026 年的延展是"自己写一本只给同行看的书"。两条信号叠在一起读，对一人公司的提示是：在 AI 把通用内容变成商品的同时，"高密度、高个性、高视觉成本"的内容反而被推到了溢价位置。

风险有两点。一，国内"电子书"支付意愿仍偏低，参考豆瓣读书近年公开数据，技术类电子书中文版定价多在 ¥39–¥99 区间，年销过万册的非平台书极少。直接套 Making Software 的"单本 $40"模型在中国跑通难度较大，更可能要走付费社群 / 订阅专栏的形态。二，插画 + 长内容的制作门槛高，AI 辅助插画能减一半工，但风格统一性、信息密度仍要人手把控，存量内容沉淀的时间成本不可低估。

竞争格局上，国内不缺"懂技术的写作者"，缺的是"愿意花一年时间打磨一本图文都成立的小书"的耐心。窗口期估计还有 18–24 个月，再晚 AI 生成的同类内容会把入门门槛拉低、把溢价拉平。

---

## 快讯区

> 未进入深度分析但值得知道，每条 1-2 句

**收入信号**
- Acquire.com 上架一个 bootstrapped 邮件营销 SaaS：$376K ARR、$917K TTM 营收、$696K TTM 利润，净利率约 76%——成熟一人/小团队产品退出参考 — @agazdecki · 6-6 02:47
- @tdinh_me（Tony Dinh）自述 Otto 项目用 Claude Code + Telegram 远程交付，其 bio 公开月收入合计约 $142K（$137K + $5K + $518 + $50） — 6-5 16:39 · [可能与上期重叠]
- @levelsio 的 Vibe Jam 2026 阶段数据：945 件参赛作品、累计 1,000,000+ 玩家、5,000 万 X 曝光、奖金池 $40K（$25K + $10K + $5K + 其他）— 6-5 21:39
- @lennysan 引述 @zenorocha：Codex 周活用户从 60 万跳到 500 万，"agents 正在替开发者选技术栈"——做 Codex/Claude Code 推荐位红利窗口已打开 — 6-5 07:17 · 188 bookmarks

**产品发布 / 工具更新**
- Cursor Design Mode：浏览器端点 / 画 / 说话改 UI，agent 直接生成代码 — @cursor_ai · 6-6 02:02
- Codex Build iOS Apps 插件：在 Codex 浏览器中查看 iOS Simulator、热重载 SwiftUI Preview，形成完整 iOS 开发闭环。@tinyfool 给了一段技术拆解（180 bookmarks，engagement 0.53%） — @OpenAIDevs · 6-5 17:33
- Felix Rieseberg 开源 Relic：能在 Windows 95 / Wii / 原版 Xbox 上跑的极简 coding agent，4MB 内存、软盘可装，levelsio 转推 303 bookmarks — github.com/felixrieseberg/relic
- Codex Profile 个人卡片可分享：展示 token 消耗、连续记录、活动图 — @OpenAIDevs · 6-5 23:38
- Hermes Agent Desktop 增加中文支持，@dotey 提交的 PR 已被 @Teknium 合并 — github.com/NousResearch/hermes-agent/pull/38241
- Testimonial.to 新增智能 NPS 路由（高分自动转推荐请求、低分转客服） — @damengchen · 6-5 09:41
- @idoubicc 的 shipany-tanstack 模板 Cloudflare 部署首次跑出 Lighthouse 四项满分 — 6-5 21:19
- @Prathkum 观察：Anthropic 服务很少维持四天以上不间断运行——稳定性仍是它的短板 — 6-6 03:48

**值得关注的观点**（仅收录有可验证背景的判断）
- @naval："软件平台会被重建为 Agent 优先" — 6-5 17:32 · 866 bookmarks
- @oran_ge："听完段永平那期播客很震撼，比他自己的问答录还系统"——整理了 11 条金句，含"做对的事，把事情做对"、"看懂一家公司不比读一个本科容易" — 6-5 09:48 · 203 bookmarks · engagement 0.98%
- @lennysan 引述一位 10x 工程师："以前我经常卡住，现在不再卡住了，所有难题都变得可能" — 6-5 09:18
- @op7418：CodePilot 项目 26 万行代码、5.6 万行文档（占比 21%），"文档即 Harness，其他都不重要"——给 vibe coding 大型项目一个量化基准 — 6-5 11:04
- @arvidkahl："最不解的是大家用 AI 抢着做有趣的事，却没人让它去查税、过滤邮件、做枯燥的查找分析" — 6-6 00:08
- @lxfater："自由职业两年，不够别人独立站一个月赚得多——单干赛道要选对" — 6-5 16:41 · 31k views

**教训与反思**
- @Shpigford 自嘲："注册了一个号称识别欺诈/小号注册的服务，结果立刻把我自己标成了欺诈"——产品没用上就知道它不工作 — 6-6 04:14
- @tdinh_me 反思 Otto：用 Claude Code 全程 vibe coding 一气呵成，回头看代码后悔了。下一个项目要让它"从一开始就可测试可验证"，AI 自修复才有支点 — 6-5 16:39
- @vista8：Claude 4.8 / GPT 5.5 的写作能力反而不如 Claude 4.6，质疑 "All in Coding" 的训练取向是否伤害了文字风格 — 6-5 10:29 · 47k views

**传播力素材**（适合自媒体改写的高互动观点）

- "Co-founder is marriage without the sex."（联合创始人就像没有性的婚姻） — @naval · 👍14,247 👁924,492 · engagement_rate 0.17%
  改写方向：适合公众号 / 知乎专栏改写为"为什么找联合创始人比找对象还难？"长文，把"无性婚姻"做钩子，正文拆"股权稀释 / 决策权摩擦 / 退出难度 / 信任脆性"四个维度
  点评：Naval 一句话击中了创业者群体里"联合创始人比配偶难处"的共识焦虑。反直觉点在于把婚姻和合伙作类比。但局限也明显——它对早期合伙的必要性几乎没说，对"无合伙人 = 一人公司"的复杂性回避了。只看这句容易被诱导成"一个人干最纯净"，忽略合伙能解决的现金流、心理支持、技能互补的现实问题

- "Imagine how good you'd be if you kept doing what you're doing for 20 years straight. Right. Pretty darn good. So why do you keep hopping around, chasing shiny distractions? FOCUS."（想象一下，如果你把现在做的事坚持做 20 年，你会有多厉害？非常厉害。那你为什么还在到处跳？专注） — @Jayyanginspires · 👍111 👁2,604 · engagement_rate 0.54%
  改写方向：适合小红书图文卡片——"20 年同件事" vs "每年换赛道"双栏对比，结尾留白让读者数自己已经坚持了几年
  点评：独创性中等，但击中 AI 时代"什么都想试一下"的焦虑面。盲区是没提"专注的前提是选对赛道"——如果方向错了，20 年只会越陷越深。更合理的版本应该是"先用 3–6 个月小投入验证，再决定要不要专注 20 年"

- "Kanye West locked himself in his room, making five beats a day for three summers straight. Sit in your room and create, and eventually you'll be invited into new rooms."（Kanye West 把自己关在房间里，连续三个夏天每天做五首伴奏。坐在自己的房间里创作，最终会被请进新的房间） — @Jayyanginspires · 👍403 👁7,235 · engagement_rate 1.06%
  改写方向：适合视频号短视频脚本——"为什么 Kanye 三年闷在房间里每天做 5 首伴奏？"引出"积累不是熬时间，是熬作品数"，结尾接到"你今年完成了几件真正能拿出手的作品"
  点评：独创性较高，靠"五首伴奏 × 三个夏天 = 1350 首"的具体数字给共鸣，比通用版"坚持就有结果"有信息量。盲区是没说 Kanye 的早期产出大部分都没成品质量，过滤率极低——直接套用的人会很快疲惫。更可靠的版本是"持续产出 + 公开发布 + 接收反馈"三件套，单靠闭门高产不一定有用

---

## 延伸资源库

### 播客 / 视频 / 访谈
- *Token Town* EP004 "Claude 5x is all you need"（嘉宾 @Shpigford） · 主持 @aarondfrancis、@IanLandsman · 重点谈了 Josh 用单个 Claude 5x 套餐做完所有项目的工作流。链接：tokentown.com/episodes/004-claude-5x-is-all-you-need-w-josh-pigford
- *My First Million*：本期录的 Lloyd Blankfein（前高盛 CEO） · @thesamparr 6-5 整理了 11 条录制现场观察（"穿 Suit Supply 西装、用带广告的 Netflix、退休后在做日内交易、25% 资产在指数 + 75% 个股、推崇 Robert Caro 的历史书"） · 节目尚未上线
- 段永平专题播客：@oran_ge 听后整理了 11 条核心金句 · 推文未注明具体期数和主播 · 需要时可在播客平台搜"段永平 + 哲学" · [可能与近期播客重叠]
- @tinyfool YouTube："Codex 进入 ChatGPT：普通人的超级工作流时代来了" · youtu.be/_q_-vL1stPA · 6-5 09:01

### 图书 / 课程
- *Making Software* — Dan Hollick · 早期访问开放 · makingsoftware.com/early-access（详见金矿 2）
- *1929* — Andrew Ross Sorkin · @thesamparr 引用其中一段"1929 年顶级银行家年入 1 亿美元、每天工作 6 小时" · 中文版状态未确认 [未经验证]
- *You Can Just Do Things* — Jay Yang · 作者本期持续推送 · 中文版状态未确认

### 链接汇总（已读到 / 可访问）

**工具类**
- github.com/felixrieseberg/relic（Relic 古老设备 coding agent）
- github.com/chaos-xxl/zelda-hyrule-ui（83 个塞尔达风格 UI 组件，开源带 Skill）
- github.com/NousResearch/hermes-agent/pull/38241（Hermes Agent 中文 PR）
- capgo.app（Capacitor OTA 热更新，详见金矿 1）
- testflight.apple.com/join/FGV3JcvV（@turingou vibelab iOS 公测）
- demo.mkimage.ai（MkImage 开源 AI 生图站演示）
- Poke.com（Apple 官方批准的 Apple Messages AI 代理）

**报道 / 长文类**
- anthropic.com/institute/recursive-self-improvement（Anthropic *When AI builds itself*，本期头条来源）
- robinsloan.com/notes/home-cooked-app/（2020 年原文"An app can be a home-cooked meal"，被本期回炉转推 446 bookmarks）
- smbfinanceos.com/post/the-complexity-tax-where-profit-and-cash-quietly-disappear（Kurtis Hanni "复杂性税"长文）
- longform.asmartbear.com/explore-execute（Jason Cohen "Explore vs Execute 两种工作模式"）

**收购 / 收入披露类**
- app.acquire.com/.../UlNUINwK45sHRyFGp4NC（$376K ARR、76% 净利率的邮件营销 SaaS 退出清单）

**播客类**
- tokentown.com/episodes/004-claude-5x-is-all-you-need-w-josh-pigford

---

## 行动建议（按档位分组）

档位 A（内容创作者）
- 本周可做：列出过去 12 个月互动最高的 5 篇内容，看是否能围绕同一主题攒成一本小书或图文卡片集——参考 Making Software 的"插画 + 知识点"形态
- 30 分钟可做：把最近一条爆款推文 / 笔记的核心比喻拆解出来，看它能否扩成 600 字的长内容雏形

档位 B（独立开发者）
- 本周可做：盘点自己熟悉的某个开源框架（uniapp / Tauri / TanStack / Capacitor 等），找它官方方案最贵或缺位的功能，估算自托管版的 0→1 工作量。Capgo 提供的是"次级生态寄生 + 开源做信任 + 托管收钱"的可复制模板
- 30 分钟可做：去对应框架的 Discord / GitHub Discussions 翻一周内的 high-upvote issue，看用户在抱怨什么没人解决

档位 C（工具集成者 / vibe coder）
- 本周可做：参考 @op7418 给的"26 万行代码 / 5.6 万行文档 = 21% 文档占比"基准，给自己最大的 vibe coding 项目做一次文档体系审计
- 30 分钟可做：把现有一个项目的 README 改成"AI 接手时需要的 7 个 prompt"结构，验证下次冷启动是否能让 AI 5 分钟内进入状态

---

## 避坑指南

- **vibe coding 后回头读代码很痛苦，前置 testability 比事后补救便宜**（@tdinh_me 本期反思）：Otto 项目全程 Claude Code vibe coding，回头看代码"做了很多次优设计选择"。教训是从一开始就让 AI 输出可测试、可验证的产物，因为只有验证通过的代码 AI 才能持续自我修复——否则项目越复杂越没救
- **国内大厂内部项目缺乏"批判性否决"机制**（@lidangzzz 6-5 关于阿里钉钉某产品的观察）：PE / VC 一句"出来融不到一分钱"就能拍死的反馈环路，在大厂内部 director / VP 那里不会发生，项目即使是垃圾也能跑一年烧上亿。这条对一人公司的反面教材是——自己的项目自己要扮 VC，敢杀掉做了一半但走错方向的产品

---

## 本期情报评估

**信息密度**：正常偏高 — 253 条推文中有 2 条 A/B 级强信号、5–6 条 C 级中信号；金句和情绪类内容占比较高（"co-founder is marriage..." 等占据了 top views 但收藏率低），但金矿候选数量真实

**趋势信号**：本期最清晰的趋势是"Agent 作为开发劳动主力"在不同层级同时被验证——Anthropic 自曝 80%+ 代码自动化（基础设施层）、Cursor + Codex 新功能轮番出现（工具层）、@tdinh_me / @op7418 / @vista8 在真实项目上的工程实践和反思（应用层）。"Build for agents first"（@naval）从一句口号变成跨层共识

**横向对比**：本日有两条独立的"开源 SaaS 长尾"案例可以对照——Capgo（3 年 $20K MRR、单干 + Open Source）vs Acquire.com 在售的邮件营销 SaaS（$917K TTM 营收、76% 净利率，已成熟、待出售）。一个代表"建中"，一个代表"建好等卖"。两种路径对应一人公司不同生命阶段，前者更适合 0→1 阶段的独立开发者复盘节奏，后者更适合已有现金流的运营者参考退出估值区间

**当日强信号数 vs 噪音比**：约 2 条 A/B 级强信号 + 10–15 条 C 级中信号 + 大量金句类内容。@naval 当日发了 5 条，其中 3 条 ZCash 相关、1 条政治转推，只有最后一条"agent-first"判断进了视野；@lidangzzz 当日发了 12 条，大量国内娱乐 / 房产 / 政治调侃，与一人公司主题相关的只有"小语种 + 电类专业"和"数学系应学 Lean"两条，分别进了快讯和避坑分类

**本期信源**：@runes_leo @marclou @martindonadieu @bentossell @DanHollick @lennysan @zenorocha @naval @oran_ge @tdinh_me @op7418 @vista8 @agazdecki @cursor_ai @OpenAIDevs @felixrieseberg @levelsio @tinyfool @dotey @Jayyanginspires @lidangzzz @arvidkahl @damengchen @Shpigford @p_millerd @asmartbear @ItsKieranDrew @Prathkum @thesamparr @lxfater @vista8 @idoubicc @turingou（共 30+ 位被引用）
