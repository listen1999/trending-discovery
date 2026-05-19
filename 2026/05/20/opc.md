# AI 一人公司日报 | 2026-05-20

数据窗口：2026-05-19 06:00 — 2026-05-20 06:00（北京时间，过去 24 小时）
深度挖掘：3 条
当日汇率参考：1 USD ≈ ¥7.18（人民银行中间价附近，下同）

---

## 今日头条

Viktor 拿下 7500 万美元 A 轮（约 ¥5.39 亿），10 周冲到 1500 万美元年化收入（约 ¥1.08 亿 ARR），由 Accel 领投——"AI 同事"作为细分品类，被一线 VC 和 Shaan Puri 这种连续创业者同时用真金白银背书。Cursor 占住代码、Sierra 占住客服、Viktor 自己定位是吃掉剩下 70% 的"非代码非客服"工作（运营、市场、财务、销售、BD、CS、行政），native 集成 Slack 和 Teams，按 schedule 输出"成品"而不是 chat 答案。这条信号对中国一人公司创业者的现实意义在于：不必再追前沿模型，**"特定岗位的 AI 员工 + 在客户已有沟通工具里交付"** 这一形态，今天就能定价、能融资、能验证。本期同时出现的 Chatbase 突破 $10M ARR、AI21 Labs 裁掉 110 人（61%）转型 agent 平台、Tony Dinh 24 小时 vibe code 出 iOS 应用——指向同一个共识：模型本身不再是产品，"模型 + 上下文 + 工作流 + 交付物" 才是。

---

## 今日金矿

### 金矿 1：Viktor —— 10 周做到 $15M ARR 的"AI 同事"，VC 与连续创业者同时下场

来源：@frydwia（Viktor 联合创始人，原文）· 2026-05-19 · 👍616 转推 by @ecomchasedimond / @ShaanVP / @itsolelehmann / @Prathkum
交叉信源：@ShaanVP（46.9 万粉，连续创业者）"Viktor is the most useful ai tool I've used since Claude——cold called the founder and invested 2 days after using it level good"，👍230 👁93,903 收藏 389，engagement_rate 0.41%
互动数据对比：当日 Top 10 收藏率（中位数约 0.18%），ShaanVP 这条收藏率 0.41%，属于"读者真的存档"的强候选。

**核心数据（据推文原文）**
- A 轮：$75M（约 ¥5.39 亿），Accel 领投——@itsolelehmann 称这是波兰创业历史上最大 A 轮
- ARR run-rate：$15M（约 ¥1.08 亿），从产品发布到这个数字用了 10 周
- 客户口径："小公司省下百万美元 / 头 30 天源出几十万美元新收入 / 整团队拿回一半工作周 / 公司团队精简 40% 而不减少产出"——均来自创始人自述，未单独核实
- 公司从 2023 年成立，前几年反复失败、改方向、做过 Jace.ai 

**商业模式拆解**
- 定位：不是 chatbot，是"按 schedule 在 Slack / Teams 频道里交付成品"的 AI 员工
- 入口策略：让 AI 员工生活在客户已有的工作通道里，而不是再开一个 web app（这一点是与 ChatGPT/Claude 通用助手最大的差异化）
- 收入公式：典型企业 SaaS 路径——按 seats / workflows / outcomes 三选一计费（官方页面 getviktor.com 列出"免费试用"入口，定价层级未在推文里披露）
- 利润逻辑：B2B SaaS，毛利由 LLM 推理 + 工具调用成本决定，关键指标是单个 workflow 的 token 边际成本能否随用量摊薄

**复制路径（只写真正适用的档位）**
- 档位 B（独立开发者）：Viktor 的护城河不在模型，而在"Slack/Teams 原生体验 + 持续交付物 + 工作流模板库"。中国独立开发者可对应做"飞书 / 钉钉 / 企微原生的某一岗位 AI 员工"——比如"飞书原生的电商客服周报员"、"企微原生的销售线索追踪员"。技术栈用 Hermes Agent 或 Claude Code Skills 做工作流，国内向通过飞书机器人 / 企微自建应用接入，海外向走 Slack App Directory + Stripe 收费。冷启动建议从"一个工种 + 一个交付物"切，不要复制 Viktor 的"全能 AI 同事"叙事，那需要 $75M 的弹药
- 档位 C（工具集成者）：把 Viktor 当成"成品工作流公司"的标杆研究对象，自己用 n8n / Make / Hermes 拼"非代码非客服"的工作流给中小企业，按 outcome 计费（比如"每发送一份合规的周报 ¥X"）。差异化点：服务深度（接 SOP / 流程 / 已有系统）比 SaaS 公司更灵活

**竞争格局**
- 海外：Cursor（代码）、Sierra（客服）、Viktor（运营财务销售）已经形成三角，剩余空白是"垂直行业 AI 员工"（医疗诊所、律所、电商代运营、SEO 代运营等）
- 国内：暂无明确对标，飞书 OpenAPI 上有零散尝试但缺品类共识；360 已上线"龙虾"（自然语言搭工作流）但定位偏 to C；钉钉 AI 助理偏内部知识库。Viktor 这种"原生在沟通工具里交付成品"的国内空位明显存在

**[关键约束]**
- 不要误以为"做个类似产品就能复刻"。Viktor 这条曲线 = 2-3 年方向失败 + Polish 创业者执行力 + Slack/Teams 渠道红利 + Accel 网络。中国版本必须先解决"客户为什么愿意把权限交给一个新公司的机器人"这个信任前置——可能比海外更难
- "$15M ARR in 10 weeks" 是 annualized run-rate（年化跑率），不是实际过去 10 周收入 $15M，理解时不要算错

**深度综述**

这条信号最被低估的部分，是 Viktor 的 distribution 选择。绝大多数 AI 创业者还在"做一个新 web 应用让用户来"，而 Viktor 直接钻进 Slack 和 Teams 的频道里——这是企业每天打开次数最多的入口，比任何独立产品页都先天接近"工作流"。Cursor 之所以能跑通，也是因为它寄生在 VSCode 这个开发者每天 8 小时不离的 IDE 里。这暗示一个普适规律：在 AI 同事这个品类，**渠道选择 ≥ 模型选择 ≥ 提示词工程**。对中国一人公司创业者来说，飞书 / 企微 / 钉钉的"机器人入口"是同等量级的金矿，但目前几乎无人把它当"主战场"打——大家还在做 web SaaS。

第二个值得拆解的是创始人轨迹。Fryd Wiatrowski 之前在 Meta、Oxford、HFT，并不是经典的 SaaS founder 出身。他用 2-3 年和"非常小但忠诚的团队"反复迭代失败——这与 levelsio、marclou 这种"build in public 多产品矩阵"的打法完全不同，反而像传统 VC SaaS 路径。这条信号对一人公司读者的反向启示是：**如果你确信品类，但没有 VC 资源也没有 levelsio 那种公众影响力，就不要选这种需要长期资金的方向**。AI 员工平台是 VC 战场，不是 bootstrap 战场。bootstrap 路线该选的是 Tony Dinh 那种"单产品 + Paddle / Stripe 收费 + 1 万到 10 万月入"的形态。

第三是趋势位置判断。本期 Chatbase 宣布 $10M ARR、AI21 Labs 裁员转 agent 平台、Yasser 把 Chatbase 重定义为"customer-facing agent harness"——三条信号叠加，说明"卖原始模型/API"这层正在快速变成低毛利商品（Damon Chen 直接评论"answer to those who said wrappers are dead"）。**真正赚钱的是包裹层：harness、workflow、integration、UI、SOP。** 这与 7-10 天前 Claude Code 团队博客"harness matters as much as the model"的判断在同一条曲线上。一人公司今天该做的，是把自己最熟悉的某个垂直岗位的 SOP 写成 agent skill / workflow，而不是去微调一个 7B 模型。

**风险与本土化盲区**：Viktor 在欧美能跑通，部分原因是 Slack / Teams 已经把企业沟通通道高度标准化。中国对应的飞书 / 企微 / 钉钉三选一未定胜负，机器人接口能力、权限模型、数据出境合规都更严。**直接把 Viktor 当模板"在飞书上做一个 Viktor"** 这条路径，最大的坑是低估了合规和权限成本——不要把跑通时间预算定在 10 周，按 12-18 个月规划更现实。

---

### 金矿 2：Tony Dinh 用 24 小时 + Telegram 一个对话框，造出 iOS 应用 PulseRevenue 并卖出第一份源代码

来源：@tdinh_me · 2026-05-19 15:59 BJT · 👍149 转推 3 收藏 60 浏览 18,596
作者信源可信度：bio 公开列出 5 款产品月收入，其中 TypingMind $137K/m（约 ¥98 万/月），多年 Paddle 用户。同日另一条更新：App Store 还没批，已经卖出第一份 $19 源代码（约 ¥136）
互动数据：engagement_rate 0.32%，超过当日中位数（0.18%）约 78%；同 thread 后续收入贴 engagement_rate 0.13%——金矿信号集中在第一条"完整复盘"上

**内容类型：原创长帖 + 自我引用**
**国内可用性**：Claude Code（claude.ai）境内可访问；Telegram、TestFlight、GitHub Pages、Cloudflare、Polar 都需要工具；GPT Image 2 经 OpenAI 走需要工具。整套流程在国内独立完成需稳定海外网络
**预计耗时**：作者本人 24 小时（已熟悉 Claude Code 远程 + Mac Mini 配置），新人首次完整复刻预计 5-7 天

**完整步骤（逐条还原，不压缩）**
1. 在自家 Mac Mini 上常驻 Claude Code，配好 AI 助手远程访问（Tony 之前发过 Tailscale + Termius + Claude Code on Mac Mini 的搭配，本期 vista8 也提到同套方案）
2. 通过 Telegram 给 Claude Code 下任务："给我做一个查 Paddle 收入的 iOS App"——Telegram 仅作为通讯层，不写代码
3. AI 用 GPT Image 2 出设计图，全程不打开 Xcode
4. Claude Code 用 Swift UI 写代码，用模拟器跑通后通过截图判断 UI 是否正确
5. AI 自动把 Build 推上 TestFlight，邀请 Tony 在 iPhone 上测试
6. 给 AI 一个 App Store Connect 的访问权，AI 自己提交审核
7. 让 AI 想个域名 → Tony 手动买 → 给 AI Cloudflare API 访问权
8. AI 在 GitHub 上设计 + 写静态站，用 lighthouse CLI 自测性能，部署到 GitHub Pages，配置 DNS
9. Tony 手动注册 Polar 账号 → 给 AI API key → AI 在站点接好支付、关联账号、上架 $19 源代码

**前置条件 / 适用人群**
- 有一台常开的 Mac（M 系列推荐），iCloud / Apple Developer 账号
- 熟悉 Claude Code 的项目结构和 Skill 配置
- 海外支付通道：Polar、Paddle、Stripe（均境内不可直接注册，需海外身份/银行）
- 适合：档位 C（vibe coder）和档位 B（独立开发者）想做 iOS 副业的人。**完全不适合档位 A 内容创作者**——这条不是"任何人都能做"

**可直接使用的命令片段**
作者未公开完整 prompt，但工作流的核心是"给 AI 一个真正的写权限 + 一个外部反馈通道"：
```
# 远程访问 Claude Code (作者既往提及的搭配)
brew install tailscale && tailscale up
# Mac Mini 上常驻 Claude Code
claude --dangerously-skip-permissions  # 仅限你自己的隔离环境
# Telegram 端：通过 webhook / 第三方桥接 (本期未给出具体桥接方案)
```

**踩坑预警 / 已知限制**
- @tdinh_me 同日另一条提到："试着用 @stripe projects.dev 时 Claude 拒绝自动开账号"——目前 AI 自动注册新账号（特别是金融类）会被模型安全机制拦截。Stripe / Polar / Paddle 需要人工完成 KYC，**别把"全自动"理解成"完全不动手"**
- App Store 审核仍由 Apple 决定，本案例发推时审核未通过，第一份 $19 源代码已经卖出但 App 还没上线——商业风险是 App 被拒后退款问题

**与现有工具链配合**
- Claude Code Skills（本期多条相关：vista8 的 seo-audit、Shpigford 的 security-audit、dotey 的 baoyu-comic）可以作为"可复用专家"插到这个流程里
- 如果只做单页静态站 + 支付，可以省掉 GitHub Pages 步骤，改用 Lovable / Stitch（Google）/ Bolt 等 vibe 平台

**官方链接 / 验证入口**
- 产品：pulserevenue.app（本期未独立 web_fetch 验证页面状态，作者本人在推文 thread 里贴出）
- 作者另两款主力产品定价基线：TypingMind 个人版历史价 $39（约 ¥280）一次性 + 订阅；DevUtils ¥99-¥219 区间——读者参考 ARPU 时这是公开基线

**深度综述**

这条信号最值钱的不是"24 小时做出 App"，而是它把 vibe coding 工作流的颗粒度推到了一个新的极限：**人只做三件事——授权、付费、点确认；剩下全部由 AI 完成**。Tony 自己强调"我没读过这个项目的任何一行代码，从没打开过 Xcode"。这是 Claude Code Skills + Telegram 远程控制 + 已有海外支付/域名/Cloudflare 账号 体系下的复合产物，**不是模型能力的胜利，是工具链整合的胜利**。

为什么 Tony 能做到，绝大多数中国独立开发者做不到？因为他已经在 Paddle / Cloudflare / GitHub Pages / Apple Developer 这套海外栈里跑了多年，所有账号、支付、域名都是现成的——AI 拿到的是一套"已经预热好的火炉"。国内对应的痛点是：**支付出海 + Apple 海外账号 + 稳定网络环境**，这三个前置成本如果没有提前几年布好，AI 再聪明也走不通。这条信号对档位 B 的真实启示是：**先花 1-2 个月把出海账号 / 支付 / 域名体系搭好，再谈 vibe code 速度**。

第二个值得拆的是"产品定位"。PulseRevenue 不是新品类，它是"Paddle 官方没有手机端"这个具体痛点的补丁——非常小、非常具体、用户精准（Paddle 用户群）。Tony 之前所有副业（TypingMind 是 ChatGPT 的另一个壳、DevUtils 是程序员工具集）的共同模式都是这种"在某个工作流里挖一条窄槽"，不是叙事大、估值大的方向。**一人公司不该和 Viktor 比"做大 AI 同事"，该和 Tony 比"在你已经熟悉的工具周围找窄槽"**。中国对应的窄槽可能是："飞书审批查询小程序"、"企微销售排行实时表"、"拼多多店铺利润预警 iOS App"。

第三个反直觉点：作者明确表态"$19 源代码 + 免费 App + 引流到 TypingMind"——他完全不是靠这个 App 赚钱，他是在用一次 vibe code 表演给自己的旗舰产品 TypingMind 做 demo。**24 小时做 App 是内容素材，TypingMind 才是变现**。把这条信号当成"我也照做就能赚钱"的人，会忽略掉"你需要一个已经在赚钱的旗舰产品来承接这次表演的流量"这个隐藏前提。

**风险与本土化**：直接照搬这套流程做"24 小时做一款国内 App"会撞墙——iOS 国内上架需要资质和工信部备案，安卓需要应用商店审核，支付要走微信/支付宝。**国内可行的等价物**：用同样工作流做"飞书机器人 + Cloudflare Worker + 微信/支付宝商户接入"的小工具卖给个体老板，单价 ¥99-¥499，挂在小红书或抖音"独立开发"标签下出货。需进一步调研验证：Apple Developer 个人账号在新规下境内能不能开（建议本周 web_search 一次"Apple Developer 个人账号 2026"）。

---

### 金矿 3：木马人 2.0 —— 9 个月 X 月入 5 位数后一夜清零，给中文自媒体新人的"三道坎 + 一道致命坎"

来源：@mumaren_2 原帖被 @vista8 / @lxfater 同日引用并背书 · 2026-05-19 18:23 BJT · 原帖 👍203 转推 17 收藏 不公开
信源可信度：账号信息简单（粉丝 1145，原账号刚被封后开新号），但被两位高粉 Chinese AI / 独立开发圈成员（vista8 10.9 万粉、lxfater 10.1 万粉）公开背书并附上自己的相同经验。lxfater 评论："互联网信息排泄链那张图我也发过跑到 100 万浏览"——验证了原帖关键事实

**核心事实（据原帖与背书推文）**
- 大厂程序员副业起号，9 个月做到 X 月均"5 位数"（人民币推断）
- 平台试错顺序：小红书 → 公众号 → 抖音 → X，前三个都没做起来，只有 X 有正反馈
- 9 个月内容量：9,749 条推文，11,897 粉
- 首次商单：2026 年 1 月，¥1,915（约 $267）——价格不大但确认了"商业闭环已跑通"
- X 创作者激励：累计提现 HKD 7,000+（约 ¥6,500）
- 上周五（2026-05-15 左右）账号因"违反禁止虚假行为规定"被永封，申诉两次未回应

**三道坎 + 一道致命坎（按可复制性排序）**

1. **抠门的坎**：前几个月卡在 2,500 粉。开蓝 V（X Premium，国内价 $8/月约 ¥58）当天涨 100 粉，一周涨粉量超过前一个月。**结论：基础设施别省**
2. **搞流量的坎**：唯一爆款是"互联网信息排泄链"那张图，单帖 130 万 X 浏览 + 46 万公众号阅读，把账号从 3,000 拉到 4,000 粉。**结论：火过的内容会再火，可复用是涨粉最大的杠杆**
3. **盈利的坎**：达到创作者收益门槛后，接到第一个商单。**结论：先做内容到达门槛，钱会自己找上来**
4. **致命坎（封号）**：商单未在推文里标注"广告/合作"，违反 X 的 disclosure 规则；或被举报。9 个月、9749 条、11897 粉一夜清零。**结论：商单必须在推文里 disclosure，X 对此越来越严**

**复制路径（只写真正适用的档位）**

- 档位 A（内容创作者）：
  - 30 分钟可做的事：把当前 X 账号最近 10 条商单/付费推广推文检查一遍，加上"#ad / 合作 / sponsored"明确标注，规避同款封号
  - 本周可验证的事：选 1-2 张你以前发过 50 万+ 浏览的图，重新拼一个新角度，再发一次（这是"火过的会再火"的最低成本测试）
  - 中期：开蓝 V 是基础设施，不要用"先看看反馈再说"的逻辑——@mumaren_2 自己的复盘明确说这是"9 个月最贵的一个决策"
- 档位 D（服务变现者）：
  - 这条信号是反面教材：**如果你给客户做"X 账号代运营 + 商单接洽"服务，必须把 disclosure 流程写入 SOP，否则封号了客户找你赔损失**

**原始链接**
- 原帖被引用：x.com/mumaren_2/status/2056663511036748116（账号已封，链接可能 404）
- vista8 引用版：x.com/vista8/status/2056726090182488319

**深度综述**

这条信号在本期所有"自媒体变现"贴里是唯一一条带具体数字 + 具体失败的——大多数同主题推文都是空洞鸡汤（"坚持就是胜利"、"内容为王"）。木马人 2.0 给出的三个具体阈值——**2,500 粉的蓝 V 临界点 / 创作者收益的提现门槛（约 HKD 100/$13）/ 第一个商单 ¥1,915**——比任何一篇 X 涨粉教程都更接近"中国普通程序员真实可达的副业天花板"。这是非常稀缺的"基线数据"，值得档位 A 读者直接收藏。

但这条信号最需要警惕的是封号机制。9 个月、9,749 条内容一夜清零，不是个例——本期 @levelsio 同样在抱怨 AI 回复 spam 已经迫使他把回复权限限制到"互关账号"。**X 平台的内容资产风险，在 2026 年明显高于 2024 年**：AI 自动回复、自动 QT、刷粉刷量的整治力度上来了，"虚假行为"的判定线下移了。对中国创作者来说更不友好——一旦被判定为机器人/低质量账号，几乎不可能申诉成功。**真正可行的对冲是：X 内容必须沉淀到自己的公众号 / Newsletter / 小红书 / 微信社群**，不能把全部资产押在 X 一个篮子里。

**趋势位置判断**：自媒体副业进入"中后期共识"阶段。早期红利（2023 年的 X 中文创作激励）已经消失，现在是"既要持续输出又要规避平台风控"的双重压力。@lxfater 在引用里直接说"财不外露，不要老是说自己变现多少钱了"——这一条对档位 A 也值得直接抄走。**展示太多收入数据 → 引来举报 → 触发风控** 的链条，是 2026 年 X 中文区的新常态。

**反直觉点**：原帖隐含一个反直觉判断——"先做最容易火的平台，看哪个能让你坚持下去"，而不是"先选你最熟悉的平台"。木马人 2.0 在小红书 / 公众号 / 抖音都失败过，只有 X 给了正反馈。这指向一个被低估的事实：**平台与个人风格的匹配度，比平台总量大小重要得多**。档位 A 创作者如果在某个平台连发 30 条都没有正反馈，应该换平台，而不是更努力。

---

## 快讯区

> 未进入深度分析但值得知道

**收入信号**
- Chatbase 突破 $10M ARR（约 ¥7,180 万），创始人 @yasser_elsaid_ 同时把产品重定义为"客服 agent 的 harness"。@damengchen 转引并评论"answer to those who said wrappers are dead" — 2026-05-19 09:16 BJT · 收藏 21
- @PierreDeWulf 宣布离开 ScrapingBee：2025 年 2 月 Oxylabs 全现金收购（八位数美金），完成 12 个月锁定期后离任，转入董事会身份；下一步 acquire SaaS（dev tools / API / 数据方向，$500K-$2M ARR 区间） — 2026-05-19 23:44 BJT · 👍191 收藏 46
- acquire.com 上线新标的：AI SEO 代理公司，$569K ARR / $1.2M TTM 收入 / $593K TTM 利润（净利率约 49%） — @agazdecki · 2026-05-20 04:14 BJT
- @tdinh_me PulseRevenue 上线即售：App Store 审核尚未通过，已售出第一份 $19 源代码（约 ¥136）— 2026-05-19 23:00 BJT · 👍36

**产品发布**
- Viktor（getviktor.com）：宣布 $75M A 轮 + $15M ARR，详见金矿 1
- Cursor Composer 2.5：cursor_ai 自研模型升级，下周双倍配额，@levelsio 等多人转推 · 浏览 1,800 万 收藏 2,504（被 levelsio 转推的版本）
- Gemini Omni（labs.google）：Google I/O 2026 发布的视频生成模型，@xiaohu 现场实测墨比斯风格效果差，@op7418 称视频编辑能力是亮点；同期发布 Gemini 3.5 Flash · "Google's Vera"（Nvidia 首款自研通用 CPU，专为 agent 编排设计）也已交付给 Anthropic / OpenAI / xAI / OCI
- Netlify Database：scale-to-zero 数据库 + Postgres 分支预览环境，专为 AI agent 时代设计 — @thisiskp_ 解读 · 收藏 8
- Laravel Cloud：$5/月新档位 + spend caps + 毫秒级唤醒的 scale-to-zero compute + 托管队列 — @taylorotwell 由 @arvidkahl 转推 · 浏览 4.2 万 收藏 39
- Kit MCP：邮件平台 Kit 推出 MCP server，AI 工具可直接给订阅者打标签、构建序列、起草并排期 broadcast — @nathanbarry · 收藏 12
- PulseRevenue（pulserevenue.app）：详见金矿 2
- Granite（granite.co）：@Shpigford 的新产品早期 access，定位"长期文档保险柜"（非知识库），自然语言搜索 — 收藏 1（暂为早期）

**工具更新**
- Claude Code Skills 生态本期密集动作：
  - dotey 的 "baoyu-comic" skill 被官方移植进 Hermes Agent（NousResearch/hermes-agent），生成多页知识漫画，6 风格 / 7 语气 / 7 版式 — 👍1,021 收藏 604
  - @vista8 的 seo-audit Skill：`npx skills add github.com/coreyhaines31/marketingskills --skill seo-audit`，能检查 Sitemap / 301 / noindex / canonical — 👍196 收藏 299
  - @Shpigford 的 security-audit Skill（initialcommit.co/library/skills/security-audit）：扫描代码库 vs 安全卫生基线 — 收藏 13
  - @lxfater 推荐的学术 Claude Skill（github.com/Imbad0202/academic-research-skills）— 👍118 收藏 116
  - @levelsio 实测"让 Claude Code 给本机做安全审计"，发现自己 2025 年新 MBP 居然没启用 FileVault — 👍1,863 收藏 2,127 engagement_rate 1.61%（当日 Top 5%）
- @itsolelehmann 整理 Hermes Agent 必备 12 个集成（Firecrawl / Browserbase / YouTube Transcripts / Bland / Stripe / Reddit / Google Workspace / Discord / GitHub / Readwise / Granola / Obsidian）— 👍345 收藏 820 engagement_rate 1.69%（当日 Top 5%）
- @itsolelehmann 同日发 Hermes 10 个高频 slash command 列表（/goal、/cron、/background、/queue、/steer、/skill、/model、/reasoning、/branch、/rollback）— 浏览 11,099 收藏 376 engagement_rate 3.39%（当日 Top 1%）
- @itsolelehmann X 上的 6 大 Hermes workflow（Narrative Builder / Trend Mining / Customer Pain Mining / Auto Swipe File / Replyguy Opportunity Scanner / Lead Discovery）— 收藏 22
- Cursor 自研 Composer 2.5 据 @runes_leo 解读：Kimi K2.5 底座 + Cursor 真实 IDE 数据做 SFT/RL — [未经验证]
- /fast 模式默认切到 Opus 4.7（Claude Code），@Shpigford 实测一晚上不知情用了 $100 — 收藏 5

**值得关注的观点（仅收录已验证 solopreneur 的判断）**
- @tdinh_me："如果你 2026 年还没让产品对 AI agent 100% 可用，你就跑不下去" — 👍98 收藏 13
- @p_millerd："最好的 AI 时代咨询公司原型不是'McKinsey for AI'，而是 SemiAnalysis——数据 + 研究 + 内容是核心，工具和咨询在下游" — 👍64 收藏 56（高收藏率 1.08%）
- @SimonHoiberg："只庆祝 MRR 增长是新手思维。3 小时做一个客服自动化，每周省 6 小时——这才是 functional founder 该庆祝的" — 👍21 收藏 1
- @PierreDeWulf 回顾出售经验："合同里管不到的事——品牌怎么活下来、团队怎么被对待、文化怎么变——签完字就只能祈祷。Oxylabs 在这些不能强制的承诺上都兑现了" — 创业者退出后的稀缺反思
- @koylanai：AI21 Labs 裁掉 110 人（61%）转型 agent 平台，原因是"卖语言模型不是可持续收入来源"——对一人公司读者意味着：连半个 B 美金融过的实验室都判定纯模型生意做不了，更别说独立开发者 — 浏览 5,378
- @thejustinwelsh："经常有人说'你能 scale 10 倍'，但我不想 scale 10 倍。Lifestyle business 是 quality time 和 quality revenue 的平衡" — @ItsKieranDrew 同主题呼应 — 👍262

**教训与反思**
- @arvidkahl 转引 npm 供应链攻击警报：size-sensor / echarts-for-react / @antv 系列等多个高下载量 npm 包被注入 Shai-Hulud 风格恶意代码，问题持续中 — 浏览 1.7 万 — 详见避坑指南
- @sweatystartup：自存仓市场打开机会窗口，"我需要钱"——直接公开找 $5-10M 股权 — 浏览 6.3 万（高净值创业者的资源对接公开化趋势）
- @thesamparr 总结上百位卖公司创始人三大理财错误：1) 不投指数基金，2) 太多钱进入非流动资产，3) 头 6-12 个月乱买豪车豪宅 — 详见避坑指南

**传播力素材**（适合自媒体改写的高互动观点）

- "John D. Rockefeller had a chill work life. By his mid-thirties, he installed a telegraph wire between his home and office so he could work from home three or four afternoons a week, gardening, planting trees, moving at what his biographer Ron Chernow described as an 'aggressively leisurely' pace." — @p_millerd · 2026-05-19 22:43 BJT · 👍2,085 浏览 154,059 收藏 527 · engagement_rate 0.34%
  改写方向：适合公众号或视频号——做"反 996 历史考据"专题。把"aggressively leisurely"翻译成"侵略性闲适"作为标题，搭配 Rockefeller 老照片 + 现代 996 工位对比。
  点评：这条之所以在大量 AI 推文里跑出来，是因为它在"AI 取代工作"恐慌的反面提供了一个具体历史锚——读者不需要被告知"放松一点"，而是被一个 19 世纪首富的具体生活方式说服。但要注意 Rockefeller 是工业垄断时代的产物，他能"aggressively leisurely" 的前提是 Standard Oil 当时几乎垄断美国炼油——直接照搬"少工作多享受"的结论，在没有同等护城河的情况下是危险的。这是它的盲区。

- "My perfect day looks extremely boring: 4:30am wake up / 4:30-5am reading / 5-8am deep work / 8-9am family breakfast / 9-11am lift/run / 11-12pm family walk / 12-5pm deep work / 5-7pm family dinner / 7-8pm sauna/cold/reading / 8-8:30pm hang/show / 8:30pm sleep. I wouldn't change a thing. Boring is seriously underrated." — @SahilBloom · 2026-05-20 00:48 BJT · 👍1,287 浏览 150,912 收藏 712 · engagement_rate 0.47%
  改写方向：适合小红书图文——做"百万级博主的极简一天 vs 普通人的混乱一天" 对比卡片，每个时段一张图。读者在小红书最爱看"作息表"类型的内容。
  点评：这条引发共鸣是因为它击中了"成功的人是不是过得很爽"这个普遍好奇——结果发现是无聊的、规律的。这是反直觉的部分。但局限性也很明显：Sahil Bloom 现在已经财务自由，他的"boring"是有 1,100 万美金净资产支撑的 boring。直接照搬作息表的读者可能会发现 4:30 起床本身解决不了任何问题——成功不是因为作息，作息是结果不是原因。

- "Your entire life will change when you realize that nobody is thinking about you. You aren't afraid of failure. You're afraid of other people seeing you fail. But nobody is thinking about you. Everybody is too busy thinking about themselves." — @SahilBloom · 2026-05-19 20:06 BJT · 👍3,001 浏览 118,486 收藏 1,190 · engagement_rate 1.00%
  改写方向：适合视频号/抖音——口播 + 弹幕效果，30 秒内讲完。也适合公众号做"为什么你不敢辞职做副业"的引子。
  点评：1.00% 的 engagement_rate 是当日 Top 1%，说明真的有读者在存档。这条之所以能引发共鸣，是因为打中了"想做副业但怕被嘲笑"这个最普遍的心理障碍。但盲区是：现实中"别人"的注意力虽然分散，但"亲近的人（父母、配偶、同事）"的注意力是真实存在的——直接告诉读者"nobody is thinking about you"会让一部分人忽略亲密关系成本。是 70% 真理 + 30% 简化。

- "Learn to take a beat. Anyone can react instantly. But most damage is done in moments of impulse. Anger wants speed. Ego wants the last word. But wisdom is giving yourself space to think." — @blakeaburge · 2026-05-19 20:37 BJT · 👍1,129 浏览 23,165 收藏 220 · engagement_rate 0.95%
  改写方向：适合小红书——做"职场冲动后悔瞬间"图文，每张图一个 anger/ego 场景。
  点评：高 engagement_rate（0.95%）说明这条带行动力。它的独创性在于把"慢半拍"区分成两个细颗粒动机——"anger wants speed / ego wants the last word"。一般成功学只会说"冷静"，这条把"为什么你冷静不下来"拆成两个具体心理位置，这是它能跑赢同类金句的原因。盲区是：在某些行业（创业谈判、销售收尾）反应速度本身就是优势，不是所有场景都该 take a beat。

- "🌡️ Sucking the CO2 out of my bedroom turned out to be the final thing improving my already good sleep to great...Most people have way too high CO2 in their bedroom (1500 to 2500 ppm)..." — @levelsio · 2026-05-19 18:04 BJT · 👍1,817 浏览 417,342 收藏 2,320 · engagement_rate 0.56%
  改写方向：适合小红书图文 + 公众号长文——"百万年入老板教你睡眠优化"类标题，把卧室 CO2 / 17°C 空调 / 9kg 加重毯子 / 凌晨补一层薄被 这几个细节拆成 5 张图。
  点评：超长（2000 字以上）原帖能拿到 2,320 收藏，engagement_rate 0.56%，证明"高细节 + 个人实测"类内容在中文/英文都吃香——比纯金句更耐用。但盲区是：levelsio 提到的"卧室温度低 GDP 才高"这种判断带种族/地理刻板印象，国内自媒体不宜照搬，需要本土化重写。

---

## 延伸资源库

### 播客 / 视频 / 访谈
- @gregisenberg 36 startup opportunities 深度拆解播客单集：YouTube `youtu.be/IFLY6L3YPGo`，时长未在推文披露——重点拆 AI + 移动 App + IRL 这 9 个方向，浏览 70,039，收藏 765（高收藏率 1.09%）。
- Lenny Rachitsky × Claire Vo「Code w/ Claude」节目：讨论"如何与长期运行的 agent 保持同步"，由 @trq212 转推，浏览 99,848 收藏 392。Lenny 同时宣布 Lenny & Friends Summit 2026-09-10 在 SF 举办（不在本期 24 小时内属于预告型信号）。
- Nathan Barry Show × @grantbaldwin："突破 $1M 创作者的关键转折是从兼职合同工切到全职高薪员工"——视频未给具体链接，Nathan 提示"YouTube 搜 Nathan Barry Show"。
- Acquired Podcast × Howard Schultz：被 @thesamparr 重新引用——讲 2008 年星巴克距离破产仅 7 个月的复活全过程（已不在 24 小时窗口，仅作背景参考）。

### 图书 / 课程
- 本期无新书推荐进入金矿门槛。@tinyfool 转引一本清史新作（孙立天，关于雍正历史档案）但与一人公司主题无关，不收录。

### 链接汇总（按类别）

**工具类**
- getviktor.com — Viktor AI 同事（金矿 1）
- pulserevenue.app — Tony Dinh 24 小时 vibe code 出品（金矿 2）
- granite.co — Shpigford 的长期文档保险柜（早期 access）
- gamma.app — AI PPT 工具（@ecomchasedimond 推广）
- claw.360.cn — 360 安全龙虾（国内 Hermes/OpenClaw 即用方案，@vista8 评测）
- MissionControlHQ.ai — @tibo_maker 新平台，72 集成
- labs.google/fx/projectgenie — Google DeepMind Genie 视频/世界生成

**GitHub Skills**
- github.com/NousResearch/hermes-agent/tree/main/skills/creative/baoyu-comic — 知识漫画 Skill（dotey 移植版）
- github.com/coreyhaines31/marketingskills — 营销 Claude Skills 集合（含 SEO audit）
- initialcommit.co/library/skills/security-audit — 安全审计 Skill
- github.com/Imbad0202/academic-research-skills — 学术研究 Skill

**报道 / 长文**
- claude.com/blog/how-claude-code-works-in-large-codebases-best-practices-and-where-to-start — Anthropic 官方"在大代码库使用 Claude Code 最佳实践"（核心句："harness matters as much as the model"）
- longform.asmartbear.com/great-strategy — @asmartbear 长文 "Great Strategy"，关于个人独有洞察与盲区
- wsj.com/tech/apple-is-making-hit-products-and-high-profits-from-imperfect-chips-d32c21d8 — Apple 用次品芯片造 MacBook Neo 的工业逻辑（@TrungTPhan 引用）

**收购市场**
- app.acquire.com listing AI SEO agency $569K ARR / $593K TTM profit（@agazdecki）
- TrustMRR 联盟计划：50/50 拆 3% 佣金，$100K 交易 → $1,500 payout（@marclou）

---

## 行动建议

> 仅在金矿能直接转化为行动时给

**档位 B（独立开发者）**
- 今天 30 分钟内：在 Slack App Directory 或飞书 OpenAPI 文档里挑出 1 个你已经熟悉的垂直岗位（比如"周报员"、"销售线索追踪员"），写一段不超过 3 行的产品定位描述。这是测试你能否做"AI 同事"窄槽的最低成本检验
- 本周可验证：把 Tony Dinh 的工作流抄一遍——选一个 Paddle / Stripe / Polar 的小痛点（"看实时收入"、"分账拆单"、"汇率换算"），24-48 小时内用 Claude Code + Telegram 远控 + 现有海外账号产出一个能跑的 demo

**档位 C（工具集成者 / vibe coder）**
- 今天 30 分钟内：把 @itsolelehmann 列的 Hermes 12 个集成里你最常用的 3 个跑通（推荐组合：Firecrawl + Reddit + Google Workspace）。这是把"你的 agent"从 chatbot 升级到能 do stuff 的最小成本路径
- 本周可验证：把 @vista8 的 seo-audit Skill 跑在你自己的网站或客户网站上：`npx skills add github.com/coreyhaines31/marketingskills --skill seo-audit`，把输出报告做成 ¥299-¥999 的标准化交付物，挂到小红书/朋友圈

**档位 A（内容创作者）**
- 今天 30 分钟内：检查最近 30 天的所有商单/付费推广帖，加上明确的 disclosure 标注（"#ad"、"广告"、"合作"），避开木马人 2.0 同款封号
- 本周可验证：选 1-2 张以前 50 万+ 浏览量的图，重新拼一个新角度，再发一次——这是 9 个月真实数据验证过的"火过的还会再火"杠杆

---

## 避坑指南

> 仅基于本期实际内容

- **npm 供应链攻击进行中**：本期 @abh1sek 警报多个高下载量 npm 包（size-sensor 4.2M/月、echarts-for-react 3.8M/月、@antv 全家桶）被注入 Shai-Hulud 风格恶意代码。@arvidkahl 直接质问"npm 什么时候管？"。**自查动作**：今天就在你的项目目录跑 `npm audit` + 检查 `package-lock.json` 最近一周的依赖更新，特别注意上面这几个包。本期没有 dev-specific "antivirus" 工具的现成方案，@arvidkahl 也在公开求推荐——临时方案是 vibe code 项目用独立的 Docker / Devcontainer 环境，避免污染主机

- **X 商单未标注 = 9 个月内容资产一夜清零**：木马人 2.0 案例（金矿 3）核心教训。X 对"虚假行为"判定门槛在 2026 年明显下移，AI 自动回复、刷量、未披露广告都可能触发永封。**自查动作**：所有过去 12 个月的付费推广帖必须补上 disclosure；订阅/产品推荐如果有联盟链接，也要明确标"#ad"

- **卖公司后 6-12 个月的现金陷阱**：@thesamparr 基于 100+ 创始人样本总结：1) 不投指数基金（一位 2012 年套现 $400M 的创始人若全压标普 500 现在应该有 $1.2B，实际只剩 $500-600M）；2) 把太多钱锁进流动性差的资产（房产、天使投资 > 50%）；3) 头 6-12 个月乱买豪车豪宅别墅。本期 @PierreDeWulf（ScrapingBee 8 位数出售）刚进入"卖完一年"窗口期，正在选择 acquire SaaS 路径——可以作为正面对照

- **/fast 模式不走订阅 token 池**：@Shpigford 实测一晚上不知情产生 $100（约 ¥718）的 usage credit 账单。ClaudeDevs 官方确认 fast mode 直接走 usage credit，**不会**因为你有 Max 20x 订阅而免费。**自查动作**：在 Anthropic 账户里设 spend cap，或者关闭 usage credit 自动充值

- **AI 自动注册金融账号会被拦截**：@tdinh_me 实测——Claude 拒绝自动给他注册 Stripe 账号。即使是 vibe coding 工作流也要预留人工 KYC 节点，**不要假设"全自动"**

---

## 本期情报评估

**信息密度**：高密度。Google I/O 2026 当日开幕 + Karpathy 跳槽 Anthropic + Viktor A 轮 + Chatbase $10M ARR 多事件叠加，但与一人公司主题强相关的信号也密集出现（4 条收入数据点 + 多条工作流升级）。

**趋势信号**：
- "AI 员工 / AI 同事"作为细分品类已经从 demo 阶段走向 VC 共识——Viktor $75M 是分水岭
- 卖原始模型/API 的路径正在快速变成低毛利商品（AI21 裁员 + Chatbase 重定义为 harness 是同一条曲线的两端）
- vibe coding 工作流的颗粒度推到极限——Tony Dinh 在 Telegram 一个对话框里造 iOS App + 站点 + 支付一条龙
- Claude Code Skills 生态本周密集动作，"skill 即可复用专家"形成共识
- X 中文区平台风控趋紧，自媒体单平台资产风险显著上升

**横向对比（本期 4 个收入数据点路径对比）**：
| 路径 | 代表 | 收入级别 | 资金来源 | 团队规模 | 启动门槛 |
|---|---|---|---|---|---|
| VC 加速 AI 平台 | Viktor | $15M ARR (10 周) | $75M A 轮 | 团队 | 极高（需 VC 网络 + 多年品类研究） |
| Bootstrap 多产品矩阵 | Tony Dinh | $137K/m + 多个 $5K-$50/m | 自筹 | 1 人 + AI | 高（需多年出海账号体系） |
| Wrapper / harness 平台 | Chatbase | $10M ARR | 中等融资 | 小团队 | 中等（需精准品类切入） |
| 内容副业 | 木马人 2.0 | 月入 5 位数 ¥ | 0 启动资金 | 1 人 | 低（但天花板低 + 平台风险高） |

启示：从"内容副业 → wrapper/harness 平台 → bootstrap 多产品矩阵 → VC 加速 AI 平台"是一条阶梯式扩张路径。**不要跳级**——直接做 Viktor 是赌博，从内容/wrapper 起步是路径依赖更短的选择。

**当日强信号数 vs 噪音比**：约 4 条强信号 + 8 条中等信号 / Google I/O 刷屏 + Karpathy 跳槽 + 个人健康/作息感悟（levelsio CO2 / Sahil Bloom 完美一天等）属于刷屏型噪音。整体信号强度高于上周末平均水平。

**本期信源**：@frydwia @ShaanVP @ecomchasedimond @itsolelehmann @Prathkum @tdinh_me @vista8 @lxfater @mumaren_2 @PierreDeWulf @damengchen @yasser_elsaid_ @koylanai @p_millerd @SahilBloom @blakeaburge @levelsio @marclou @gregisenberg @lennysan @dotey @Shpigford @arvidkahl @nathanbarry @SimonHoiberg @agazdecki @TrungTPhan @runes_leo @cursor_ai @OfficialLoganK @ClaudeDevs @taylorotwell @thejustinwelsh @ItsKieranDrew @abh1sek @thesamparr @asmartbear @bentossell @op7418 @xiaohu（共 40 位）
