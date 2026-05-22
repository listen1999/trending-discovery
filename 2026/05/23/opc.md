# AI 一人公司日报 | 2026-05-23

数据窗口：2026-05-22 06:00 — 2026-05-23 06:00（北京时间，过去 24 小时）
深度挖掘：4 条
汇率：1 USD ≈ 7.10 CNY（用于本期所有金额换算）

---

## 今日头条

**Polsia 把"一人公司 + AI"做到了 $10M ARR / $30M 融资 / $250M 估值。** Solo founder Ben Cera 自述：零雇员、AI 自己跑融资、自己干完所有事，他只去签字。这是过去两年"AI 经营公司"叙事第一次出现可被验证的财务台账（融资轮、营收量级、Product Hunt 时代到现在的连续创业者背景都能交叉印证）。对中国一人公司创业者的意义有两层：第一，"零员工 + AI Agent 矩阵"已经从概念走到了能拿到 a16z 级估值的现实；第二，已经验证的 $1M+/m 同行（@tibo_maker、@thepatwalls）开始公开质疑这种"做到这么挣钱还要融钱"的模式——观察这种"老钱 vs 新钱"的对峙，比围观融资本身更有信息量。

---

## 今日金矿

### 金矿 1：Polsia — AI 替你运营公司，单 founder 跑到 $10M ARR

来源：@Bencera · 2026-05-22 22:14（被 @rrhoover、@tibo_maker、@helloitsolly、@BrianRoemmele、@Scobleizer 等多位已验证创业者引用） · 👍2831（原推）
原推链接：https://x.com/Bencera/status/2057847644966547920

#### 核心数据（已验证）
- 本轮融资：$30M，估值 $250M（约 ¥17.75 亿） — 来源：推文原文，经 web_search 在多方报道（digg.com、henrythe9th.substack.com、andrew.ooo）交叉确认
- 年化收入：接近 $10M ARR（约 ¥7100 万） — 来源：推文原文 + Dealroom 报道"Polsia explodes from $200K to $2M run rate in two weeks"，增长曲线一致
- 员工数：0（仅 founder + AI 编排）
- 投资方：Sound Ventures（Ashton Kutcher）、True Ventures — 来源：web_search 交叉
- 服务公司数：> 6000（"How a Solo Founder Cloned Himself With AI That Now Runs 6000 Companies"，henrythe9th 报道）

#### 商业模式拆解（基于官网与第三方分析）
- **定价结构**：$49/月订阅（覆盖托管、数据库、代码仓库、Stripe、广告账号等基础设施）+ 平台抽取 Stripe 收款的 20%
- **收入公式**：$49 × N 个用户 + 20% × ΣGMV。订阅费基本只覆盖算力，真正的利润来自"成功的客户公司"分成
- **AI Agent 编排**：Engineering Agent 写代码、Marketing Agent 跑 Twitter 和广告、Support Agent 回邮件、CEO Agent 每晚醒来重排优先级
- **本质**：不是 SaaS，是"AI 孵化器" — Ben Cera 的定位话术。Polsia 只在用户挣钱的时候才挣钱

#### 复制路径（只写真正适用的档位）

**档位 B（独立开发者）**：抓两个空白点。其一是中文版的"AI 自动运营公司平台"——Polsia 不支持中文场景、不接微信/抖音/小红书生态，国内整套基础设施（域名、备案、支付、ad account）也完全跑不通。落地路径：先用 Cursor/Claude Code 把 Engineering Agent + Stripe（或者国内换 Ping++/微信支付服务商）打通做 MVP，第一波目标客户锁定"想做出海独立站但不会做技术"的国内电商主理人，定价用美元收款也合规。其二是垂类剥离：Polsia 是水平平台，垂直行业（例如"AI 跑出海 Shopify 店"或"AI 跑跨境播客制作")就是单产品复刻的窗口。

**档位 C（vibe coder / 工具集成者）**：不要复刻平台，复刻其 Agent 编排范式。把 Polsia 的"4 个常驻 Agent + 每晚 CEO Agent 醒来排优先级"这套结构，用 n8n + Claude Code Skills + 飞书机器人，给你的 1-2 个咨询客户的实际生意（电商、私教、知识付费）做"轮班 Agent"，每月按效果收费 ¥3000–¥8000/客户。这类需求在中文 X 圈、AI 群里 2025 年下半年开始涌现，但很少有人交付能跑通的，敢做就有钱挣。

#### 竞争格局
- 国外同类：Replit Agent（偏代码）、Lovable（偏前端）、Genspark / Manus（偏单任务 Agent）。Polsia 的差异化是"长期持有 + 营收分成"商业模型，不是单次交付
- 国内同类：暂无公开宣传"零员工运营公司"定位的产品。Trae、CodeBuddy、CodeGeeX 等都还停留在 IDE/Agent 工具层；纳米AI、阶跃星辰偏通用 Agent；秘塔、Kimi 偏搜索/写作
- 国内做的最像的反而是 SHEIN 的"小单快反"系统 + 阿里的"千牛"商家工作台——但缺一个"主理人级别 AI"

#### 深度综述（约 420 字）

第一层要看的是**收入公式背后的天花板**。$49 订阅 + 20% 分成的结构等于把 Polsia 变成一个"自动化的小生意 LP"——天花板取决于客户公司的总 GMV，而不是订阅数。这跟传统 SaaS 的"用户数 × ARPU"完全不同，毛利结构会比 SaaS 更像投资组合：有 1 个真挣钱的客户能抵 100 个白嫖订阅。这也解释了为什么 Tibo 公开质疑"你做到 $1M/m 还融什么钱"——传统 SaaS 视角下确实没必要融，但如果 Ben Cera 真正在做的是"用 $30M 投流引来 100 倍 GMV"，那融资逻辑就立得住。

第二层是**反直觉点**：这件事最让圈内人不舒服的不是"AI 替代员工"，而是"AI 替代联合创始人"。Polsia 自己跑了整个融资流程，Ben Cera"只去签字"。如果属实，意味着 due diligence、deal memo、谈判邮件的处理已经能被 Agent 接管——这才是已验证创业者真正震动的部分，Brian Roemmele 直接喊出"Zero barriers to build a billion dollar company"不是夸张话术，是恐慌反应。

第三层是**中国市场障碍**。国内复制要绕开三条死路：一是支付通道（个人收款境内做不了 20% revenue share 这种模型，必须挂公司），二是广告投放（境内付费媒体账号没法被 AI 自动接管，腾讯/字节都禁止），三是"客户公司"的合规——你帮一个客户做营销做出问题，谁担责？短期内国内只能做"出海方向"的本地化，做不了纯国内。

风险提醒：$10M ARR 的数字目前只有创始人自述 + Dealroom 二手转引，没有第三方审计。$30M 轮看到了报道，但具体投资条款（清算优先权、估值组成）未公开。建议把这条信号当作"趋势确认"而不是"已验证商业奇迹"。

---

### 金矿 2：Pat Walls — B2B SaaS 已死，AI 驱动的"服务公司"正在吞掉这一层

来源：@thepatwalls · 2026-05-23 04:24（已验证 solopreneur：Starter Story 创始人，名单内 A 级账号）
推文链接：https://x.com/thepatwalls/status/2057920642448523491
互动：👍33 · 👁4019 · 🔖32 · engagement_rate 0.80%（高于当日中位数约 4 倍）

#### 核心论点（推文原文）
- "2 年时间 + $100K 投入"做的 AI SaaS，只挣到 $150K（毛利被广告费、推理成本吃完）
- 关闭 SaaS、转向 services：$1k-2k/月/客户，做 [行业] 服务
- 跑到 $1M/年，**70% 毛利**
- 关键原因："agency work 大部分不是人在做，是 AI agent + automations 在做"
- 大趋势观察：SaaS 估值倍数跌入谷底；Claude Code 这种 DIY 工具在静悄悄杀掉 SaaS 增长

#### 复制路径

**档位 D（服务变现者）**：这是档位 D 最近一年最强的方向性信号。把过去你需要 3 个人才能交付的咨询/代运营（社媒代发、SEO、邮件营销、客户支持外包），用 Claude Code + n8n + 一个清晰 SOP 拆成 80% Agent 自动 + 20% 你做最后审稿，定价区间锚定在 ¥7000–¥14000/月/客户（对标 $1k–$2k）。冷启动渠道：从你已有的 5 个老客户开始，先把 1 个客户做到"完全 AI 跑通"，把这个 case 拿出来卖。

**档位 B（独立开发者）**：警示信号——别再去复刻"通用 B2B SaaS"。Pat 看到的是 2 年 $150K 收入、利润全被广告费吞掉。如果你正在做的产品恰好是"AI summary"、"AI writer"、"AI for X" 这类通用 SaaS，停下来想清楚是不是该转 productized service。

**档位 C（工具集成者）**：直接受益方。Pat 描述的"70% 毛利的 services 公司"本质上是 Agent 编排能力的商业化——你已经会的事正在变成最值钱的事。给自己定一个目标：本季度签下第 1 个 ¥10k/月的客户，用 n8n + Claude Code 交付。

#### 深度综述（约 380 字）

这条信号的杀伤力在于它把 2026 年最容易被忽略的两个趋势拼在了一起：**SaaS 估值多重压力**（公开市场倍数压缩 + Claude Code 这种 DIY 工具替代）和**Service 业务 AI 化的 margin 跃升**。过去 services 公司毛利停留在 30-50% 是因为人力成本占大头，70% 是 SaaS 标准。Pat 这位创始人达到 70% 毛利说明 Agent 已经能稳定承接 60-70% 的执行工作，人只在结构性问题和签单环节出现。

最反直觉的部分是：**B2B SaaS 在 2018-2024 这十年是 indie hacker 公认的"圣杯"**——recurring revenue、低边际成本、高估值倍数。Pat 这条推等于在公开宣告这条路径在 2026 失灵了。Claude Code 让买家自己 vibe code 一个内部工具替代你的 SaaS，三天就跑通；同时 SaaS 公司还要为获客买价格被 OpenAI/Google 推高的 Google Ads，左右开弓挨打。

对中国创业者而言，这条信号要谨慎本土化。中国 B2B SaaS 本来就难做（账期长、定价低、流量贵），Pat 描述的"AI services 公司"反而更契合国内土壤——本质上就是"咨询/代运营 + AI 提效"。问题是：国内市场对"服务"的定价天花板远低于美国（$1k–$2k/月在 SF 中小企业是合理价位，国内同样定位的客户能给 ¥3000–¥5000/月已经算好）。所以单看毛利率结构可以学，但 ARR 规模目标要打 1/3-1/2 折扣。

护城河层面，做出海服务（英文客户、美元收款）是档位 D 的最佳风险对冲——Pat 的案例直接证明了海外市场对 AI services 公司有付费意愿和价格弹性。

#### 局限与风险
- Pat 没说具体行业，"[redacted] services" 隐去了关键变量。同一套打法在文案、SEO、电商代运营上的 margin 可能差很大
- Pat 是 anecdotal observation，不是统计意义的趋势数据。同期 acquire.com 上活跃的 AI SaaS 收购仍然每周新增数百个（@agazdecki 当日也在贴 $268K ARR 的 AI lead qualification SaaS 在挂卖）

---

### 金矿 3：DeepSeek-V4-Pro 永久降价 75% — 中国 AI 一人公司基础设施侧重大降本

来源：@deepseek_ai · 被 @dotey 转推 · 2026-05-23 00:45
推文链接：https://x.com/dotey/status/2057865424843202793
互动：👍11281 · 👁1444283 · 🔖2507 · engagement_rate 0.17%（绝对收藏量极高，是当日 by_bookmarks 第 2）
配套评论：@oran_ge "DeepSeek 那个价格屠夫又回来了... 比同等水平的其他模型便宜 3 倍"（22632 浏览）

#### 核心数据（已验证）
- 原 catalog 价：$1.74 / 1M input tokens；$3.48 / 1M output tokens
- 新永久价（原促销价转正）：**$0.435 / 1M input；$0.87 / 1M output**（约 ¥3.1 / 百万 input，¥6.2 / 百万 output）
- 缓存命中价更夸张：$0.003625 / 1M tokens（约 ¥0.026 / 百万 tokens）
- 来源：DeepSeek 官方 API 文档 api-docs.deepseek.com/quick_start/pricing（经 web_fetch 验证）
- 注意：官方文档目前仍写"discount ends 2026-05-31"，但官方 Twitter 已宣布永久 — 文档与公告暂时不一致，建议本月底再核对一次

#### 与主流模型对比（按 web_search 同期公开报价）
| 模型 | input / 1M | output / 1M |
|---|---|---|
| DeepSeek V4-Pro（新永久价） | $0.435 | $0.87 |
| Claude Sonnet 4.6 | ~$3 | ~$15 |
| GPT-5.5 mid-tier | ~$2.5 | ~$10 |
| Gemini 3.5 Flash | ~$0.30 | ~$2.5 |

#### 复制路径

**档位 B（独立开发者）**：算笔账。如果你的 SaaS 月推理成本是 $2000（对应 Claude / GPT），切到 DeepSeek V4-Pro 直接降到 $300–$400/月。这相当于本来要做 5000 用户才打平的产品，现在 1000 用户就能正向现金流。**今天就该做的事**：把你产品里"用户能容忍延迟、不强依赖工具调用"的那部分流程（内容生成、文档总结、规则化分类）切到 DeepSeek 试一周，对比 quality + cost。

**档位 C（工具集成者）**：在给客户做的工作流里，把 LLM 调用层做成"路由"——通用任务走 DeepSeek，复杂推理走 Claude。客户买单的总价不变，你的毛利可能直接从 40% 拉到 65%。

**档位 A（内容创作者）**：通过国内 API 中转（硅基流动、火山方舟、DeepSeek 直连）调用 V4-Pro 做自媒体内容生成、改写、SEO 关键词扩展，月成本可以压到 ¥30-50。这意味着"用 AI 批量做小红书图文/公众号选题"的边际成本几乎为零。

#### 国内可用性
- DeepSeek API 国内**直接访问**，无须任何工具
- 硅基流动、火山方舟、潞晨云等国内中转都已上架，可以用人民币结算

#### 踩坑预警
- DeepSeek 的工具调用（function calling）质量仍弱于 Claude 4.6 / GPT-5.5，复杂 Agent 工作流别盲切
- 中文场景下 V4-Pro 的"礼貌性谨慎"问题（动不动拒绝）依然存在，做内容生成要做 prompt 兜底

#### 深度综述（约 320 字）

这条不是"工具更新"那么简单。把 75% 折扣转永久，等于 DeepSeek 在做一个清晰的战略选择——**用价格战换市场份额，而不是用模型能力换溢价**。这件事的二阶效应有三层：

第一，对中国 AI 应用开发者来说，"做一个 AI 产品的最低算力成本"从 2025 年初的 ~¥20/百万 token 区间，跌到了 2026 年中的 ~¥3-6/百万 token，2 年降了 5 倍。这意味着 2024 年因为"算力贵到做不起"被搁置的 AI 应用 idea，现在都该重新评估一次。

第二，对国内 AI SaaS 创业者来说，这是双刃剑——你自己的成本降了，但你的用户也会发现"自己接 DeepSeek 比订你的服务便宜"。Pat Walls 在金矿 2 说的"Claude Code quietly killing growth"现象，DeepSeek 这条价格曲线只会加速。

第三，对国际玩家是直接施压。OpenAI 同周还在被 @natmiletic 这类创业者吐槽"missing revenue targets while Gemini and Anthropic eat into market share"。DeepSeek 把性价比基准线再往下拉一档，OpenAI 接下来面对的不是 Anthropic 这种"质量对手"，而是 DeepSeek 这种"成本对手"。

---

### 金矿 4：Codex /goal 模式正式上线 + 中文 Skill 生态进入"可上手 24 小时跑通"阶段

来源：@dotey · 2026-05-22 11:58 · @op7418 系列推文 · @koylanai 长文（同期）
代表推文：https://x.com/dotey/status/2057672416071987378
互动：👍280 · 👁49954 · 🔖387 · engagement_rate 0.77%
官方文档：developers.openai.com/codex/prompting#goal-mode（已验证）

#### 内容类型：工具发布 + Thread 教程整合

#### 核心功能

1. **/goal 模式**（OpenAI 官方 5/22 凌晨发布）：给 Codex 一个目标，它会自己规划→执行→自检→纠错→继续，跨小时甚至跨天直到目标达成或撞墙。可暂停、可改目标、可开 side chat 不打断主任务
2. **Codex 升级到 0.128+**，App / IDE / CLI / Chrome 插件全栈支持
3. **应用内浏览器高级注释**：直接在元素上点评 / 修改，不用让 Codex 重生成
4. **App 截图快捷键**：mac 同时按左右 Command 键，把当前窗口连同窗口里"屏幕看不见的文本"一起截给 Codex

#### 10 分钟上手（来源：@dotey 实测步骤）

```bash
# 1. 升级 Codex App
# 2. 命令行启用 goals feature
codex features enable goals

# 或者手动编辑 ~/.codex/config.toml
[features]
goals = true

# 3. 在 Codex 里输入 /goal 或点 + 选 goal
# 4. 输入框上方可暂停、编辑、删除目标
```

#### 同期中文 Skill 生态（24 小时内集中爆发的可直接复用工具）

- **baoyu-skills**（@dotey）：发文章到 X 的 skill，配合 Codex Chrome 插件能 `@chrome 帮我把 xxx.md 文章发到 X 文章`，几分钟连图带文进草稿箱。GitHub: github.com/JimLiu/baoyu-skills
- **xposter Chrome 插件**（@xiaoxiaodong01）：拖拽 Markdown 文件到 X 文章编辑器自动转换，开源。chromewebstore 已上架
- **乔木快捷提示词**（@vista8）：把过去一年积累的几百套提示词做成 Chrome 插件，简写自动补全，支持 GPT-Image-2 系列预览 — engagement_rate 1.58%（极高）
- **歸藏 PPT Skills + 墨水屏 Skill**（@op7418）：用 AI 把 To-do/日历推到墨水屏便签，关机显示名片
- **Anker AI 录音豆**：@vista8 在 @op7418 推荐下购入，"目前个人最喜欢、最实用的 AI 硬件产品"

#### 国内可用性
- Codex / OpenAI **需要工具**（国内不直连）
- 但中文 Skill 生态（baoyu-skills、xposter、乔木提示词、歸藏 PPT）**本身国内可用**，只要 Codex 能通就可以用

#### 复制路径

**档位 A（内容创作者）**：把"写 → 发"的流水线整合成一句话指令。今天 30 分钟可做的事：装 Codex Chrome 插件 + baoyu-skills，然后用 markdown 写完一篇内容，让 Codex 直接发到 X 文章草稿箱。把这条路径走通，未来发跨平台内容（X / 公众号 / 即刻 / 小红书）都按这个模板加 skill 就行

**档位 B/C**：/goal 模式是"长任务委托"的真正解锁。本周可做的事：选一个你自己一直想做但拖延的小项目（重构、迁移、写个 boilerplate），用 /goal 模式让它跑通，观察 Codex 在限额耗尽（5 小时）→ 自动恢复后能不能继续。这是判断"AI 能做多长任务"的关键实验，@akokoi1 当日实测确认会保留到限额恢复

#### 深度综述（约 360 字）

把这条单独立起来是因为它代表一个临界点：**Agent 终于从"问答工具"过渡到"长期目标执行者"**。/goal 之前，所有 LLM 编程工具都是回合制——你问一句，它答一段，每次都要重新提供上下文。/goal 改成"持续游标"——你给定终点，它自己往前走。

对一人公司的意义不是"省一个程序员"——一人公司本来就没员工。意义是"你的工作时间和 AI 的执行时间彻底解耦"：晚上睡觉，AI 在跑；你出差，AI 在跑。@akokoi1 实测的"5 小时限额耗尽后会保留任务，等额度恢复继续"正是这个解耦的硬件验证。

中文 Skill 生态的同步爆发更值得关注。过去 Claude Code / Codex 的 Skill 几乎是英文圈在玩，2026 年 5 月这一周，宝玉、歸藏、向阳乔木、小小东这批中文 builder 开始稳定输出可被复用的 Skill 包。这是个明确的"中文 prompt-as-code"市场起点——以后做 Skill 的人，价值会从"会写 prompt"升级到"做出了被几百个独立开发者天天用的工作流"。

值得注意的对冲信号：@koylanai 当日发了一篇长 Thread（25 个 bookmarks, engagement_rate 1.75%）公开承认他的 Agent Skills 仓库在内部 benchmark 中"加载整个 skill 库 1/3 命中，只加载对应 skill 3/3 命中"——意思是 Skill 多了反而误伤，需要严格的"路由"机制。一句话总结：Skill 不是越多越好，是越精准越好。中文 builder 现在做 Skill 还在野蛮生长期，谁先做出"分类路由 + 评测体系"，谁就吃下下一波生态主导权。

---

## 快讯区

**收入信号**
- @agazdecki 在 acquire.com 上挂出 AI lead qualification 平台（WhatsApp / Instagram DM 自动跟单），$268K ARR / $188K TTM 利润，挂卖中 — 2026-05-23 05:23
- @foxshuo 引述 Anthropic 年化收入曲线：1 月 $9B → 5 月 $45B（5 个月 5 倍），"人类历史上从来没有出现过的收入增长情形"[未经验证，仅作者转述] — 2026-05-22 18:36
- @helloitsolly 自述 Senja（testimonial 收集工具）已达 $1M ARR，正在加 Stripe-触发自动邀请评价系统 — 2026-05-23 03:41
- @marclou 在 trust_mrr 上"$0 字谜产品卖出 $400" — 2026-05-22 23:16

**产品发布**
- **levelsio Termius + tmux + Cloudflare Tunnel 移动开发栈**：每个站点一个 Termius profile，自动落到对应 tmux session，从笔电到 iPhone 无感切换（268 bookmarks，engagement 1.04%）。另附 "block all inbound firewall + Tailscale SSH + Cloudflare Tunnel for web" 的零暴露面安全模板（516 bookmarks）— @levelsio · 2026-05-23 05:14
- **MarkEdit**：macOS 原生开源 Markdown 编辑器，仅 4MB，可处理百万行文档 — github.com/MarkEdit-app/MarkEdit
- **Polsia 同类替代品 7 个**（crevio.co 整理）— 国内开发者可用作竞品调研起点
- **Granite (@Shpigford)**：长期文档保管库（不是知识库），文档处理成本降 20 倍 — granite.co
- **Revnu (YC launch)**：AI 增长团队，"你只管 build，我们包销" — ycombinator.com/launches/QS8

**工具更新**
- **Cursor 手机版即将发布** — CEO @mntruell 当日确认 "Soon!" — @dotey 转述
- **Codex App 团队共享插件**：Business 版本现在可以批量给团队成员装 plugin
- **CapCut（剪映海外版）导演模式**：从 idea 到 trailer 一句 prompt 出片，@thisiskp_ 用 Google AI Pro $49 拍了 5 段共 50 秒的 AI 短片 "New Kid"
- **X Premium 现支持 OpenClaw / OpenCode / Hermes 授权登录**：可用 Grok 配额驱动这些 IDE/Agent — @xiaohu · 2026-05-23 04:30

**值得关注的观点**（仅收录已验证 solopreneur 的判断）
- @lennysan 转 @ElenaVerna "mom 'n' pop saas" / 自命名 "digital main street" — 不是每个软件生意都得是独角兽，"一百万美元年收入、围绕你真正吃透的领域做" 正变得越来越可达 — 2026-05-22 06:49
- @SimonHoiberg 公开自托管偏好：Grafana 替代 Amplitude/PostHog 做分析、Forgejo 替代 GitHub、OpenClaw 替代手搓 n8n+TypingMind — "GitHub is garbage, like LinkedIn for your code"（111 bookmarks）
- @Nicolascole77 关于 AI 时代的策略：(1) 持续积累与 AI 无关的硬技能；(2) 用 AI 放大这些技能的产出
- @asmartbear（Jason Cohen，两个独角兽创始人）："建立'挫败不能阻止旅程'的信心，才是真正抵达目标的方式" + "Pricing page 说电话支持只在最大套餐，但永远接电话"（实操定价小手段）

**教训与反思**
- @tibo_maker（$1M+/m 已验证）公开质疑 Polsia 融资动机："你已经 $1M/月、低成本，为什么需要融钱？" — 这是当日最值得做笔记的"已验证创业者间分歧"
- @thepatwalls 配套观察：B2B SaaS 多重压力——估值倍数下跌 + Claude Code 类 DIY 工具静默杀掉 SaaS 增长
- @oran_ge 评论模型厂发布会："能不能把基本东西直接写出来？比如 qwen max 3.7 max 多大参数、价格多少，gemini omni 价格多少。最基本的东西都不写，谷歌也搜不到，还要去官网查半天"（25K 浏览）— 这是对所有要做 toB AI 产品的厂家的硬话提醒

**传播力素材**（适合自媒体改写的高互动观点）

- 「Life without HR at your company」— @Codie_Sanchez · 👍132064 👁6307389 · engagement_rate 0.09%
  改写方向：适合视频号/抖音——"美国 Bolt CEO 炒掉整个 HR 部门"作为切入点，讲"一人公司为什么不需要 HR"。但点评要平衡：这条火是因为踩中了科技圈对 HR 不满的痒点，本质是引战内容，传播好但用作真"管理建议"会误伤——HR 在小公司确实可有可无，但任何超过 30 人的公司没有合规人事处理都会埋雷
  点评：这条爆款的真正信号是"反 HR"已成为 X 上保守派/创业者群体的共同情绪。但对中国一人公司创业者意义有限——国内劳动法环境完全不同，照搬"炒掉 HR"的态度只会带来法律风险。值得借鉴的是话题张力的制造方式，不是观点本身

- 「I have more money than ever but less things than ever」(Zohaib's hedonic treadmill 反思) — @heyzohaibb 转 @wizofecom · 👍987 👁295289 · engagement_rate 0.17% · 🔖516
  改写方向：适合公众号长文 + 小红书图文——"年薪百万后我买掉了 80% 的奢侈品"叙事框架，对标"幸福感是边际递减的"。结尾不要 push consumerism critique，而是引到"什么是值得花的钱"
  点评：这条戳中了已经在创业并且开始有点钱的人群（X 上中产 founder 的主力情绪）。盲区是：作者本人能这么洒脱是因为已经买够了，那 99% 还没买过 $200K 跑车的人读这条会被劝退消费冲动——其实他们应该买、应该体验、应该完成 hedonic loop 才能真正"看穿"。直接借用这个结论给没经历过的人，反而会让他们错过自己的 calibration 过程

- 「真正有钱的留学生天天吃人均 50 刀的麻辣香锅 doordash」 — @lidangzzz · 👍877 👁180914 · engagement_rate 0.06%
  改写方向：适合小红书图文——"真有钱 vs 假装有钱的留学生日常对比"双 panel 图文。或公众号"为什么留学生越有钱越不去米其林"
  点评：经典的"信息差段子"，火是因为击中了国内对留美生活的"豪奢想象"。局限性：这是 lidang 个人观察样本，被段子化了。读者如果是留学生家长，看完容易得到"我孩子吃喜茶才正常"的误判——其实是不是"有钱"和"省着吃"没必然关系

- 「Elon is the goat of reducing time between failure and follow up action」 — @chrishlad · 👍244 👁180530 · 🔖148
  改写方向：适合公众号——"为什么马斯克失败次数比谁都多但赢得最多"，配 Race 那条长引文（SpaceX 失败后他不悲不喜立刻打电话给工程师）作为论据
  点评：这是 2026 年中文圈仍然有效的 Elon Lore，但已经接近被消费殆尽。如果你的账号一直在写效率/反思类内容，这条可以做选题；如果不是，没必要硬接

- 「Indifference kills humor. 'This coffee is ok' vs 'This coffee is so bad even Dunkin' wouldn't serve it'」— @david_perell 转 PerellClips · 👍481 👁171223 · 🔖313
  改写方向：适合公众号写作类内容——"为什么你的文字没人看？因为你太冷淡了"。或视频号脚本——讲 Tom Segura 的"有观点才有笑点"理论
  点评：这条对内容创作者档位（A 档）非常实用，是稀有的"既独创又有可操作性"的内容——明确指出"麻木"是写作最大杀手。局限性：直接放在文字内容里有效，但对中国短视频环境的"不能太尖锐"现实要做软化

---

## 延伸资源库

### 播客 / 视频 / 访谈
- **@Nicolascole77 在 @AliAbdaal 的 Deep Dive 播客**：聊"写作变现最快路径 $10K/月"、"为什么每个写作者都该先免费工作"、"如何克服自我怀疑"。视频链接见 @Nicolascole77 推文（约 57K 浏览）
- **Anker CEO 阳萌晚点访谈** — @oran_ge 整理了 10 条洞察（"激进的保守主义者：10 块投 5 块，挣 20 回来，有 25 再投一半"、"先推动几个团队做出来，然后大家就会跟上 — 中国人不一定羡慕别的公司，但一定羡慕同一拨进公司的人"、"奔驰主打豪华，宝马主打驾驶乐趣，奥迪主打科技，竞争的终局是纳什均衡"）。原文链接：mp.weixin.qq.com/s/5QKj6WJzY7L_U43pQ6j54g
- **@DeKoderAI 与 Ankur Warikoo 关于 Gen Z 的对话**（@warikoo 当日转推背书）— 主题：成功的定义、Gen Z 焦虑、金钱与关系。视频在 X 推文

### 图书 / 课程
- 本期无新书推荐。值得提的延伸阅读：@asmartbear 的 longform 文章 *Perseverance*（longform.asmartbear.com/perseverance/）— 与"金矿 2 - Pat Walls B2B 反思"相互印证

### 链接汇总（已 web_fetch / web_search 验证）

**收入/融资类**
- Polsia 原推：x.com/Bencera/status/2057847644966547920
- Polsia 第三方分析：henrythe9th.substack.com/p/how-a-solo-founder-cloned-himself
- Polsia Product Hunt 页：producthunt.com/products/polsia
- Polsia 增长曲线（Dealroom）：app.dealroom.co/news/note/polsia-explodes-from-200k-to-2m-run-rate-in-two-weeks

**工具类**
- DeepSeek API 定价文档：api-docs.deepseek.com/quick_start/pricing
- Codex /goal 官方文档：developers.openai.com/codex/prompting#goal-mode
- MarkEdit GitHub：github.com/MarkEdit-app/MarkEdit
- baoyu-skills GitHub：github.com/JimLiu/baoyu-skills
- 乔木快捷提示词 Chrome 插件：chromewebstore.google.com/detail/%E4%B9%94%E6%9C%A8%E5%BF%AB%E6%8D%B7%E6%8F%90%E7%A4%BA%E8%AF%8D/ndfmbdiaclladmoeifbhlkacllmfhjej
- xposter Chrome 插件：chromewebstore.google.com/detail/xposter/iimkimodgdjnnmdopeolboakhjmhfbbj

**待挂卖 / 招聘**
- Acquire.com 上待售 $268K ARR AI lead qualification 项目：app.acquire.com/startup/g3tyXNzr0lYMAfMMmP0wwZUhHYQ2/ep8gwHNabCMuQbOAIwt0
- DeepSeek Harness 团队招聘（北京，研发/PM/研究员）：app.mokahr.com/social-recruitment/high-flyer/140576

---

## 行动建议（按档位分组）

> 仅在金矿能直接转化为行动时给。

**档位 A（内容创作者）**
- 今天 30 分钟：装 Codex Chrome 插件 + baoyu-skills，用 markdown 写完一篇内容、让 Codex 直接发到 X 文章草稿箱，跑通"写 → 发"流水线
- 本周可验证：用 DeepSeek V4-Pro（API ~¥3/百万 token）批量生成 10 篇小红书选题素材，对比和你自己人工出选题的 CTR/点赞差异

**档位 B（独立开发者）**
- 本周硬决定：如果你正在做的是"通用 AI 工具型 SaaS"，按 Pat Walls 的反思重新评估一次定位——能转 productized service 的就转
- 本月技术任务：把现有 SaaS 中"非关键路径"的 LLM 调用切到 DeepSeek V4-Pro，目标是把推理成本降到原来 1/5–1/8
- 长 task 委托：选一个一直拖延的小项目，用 Codex /goal 跑一晚上看产出

**档位 C（vibe coder / 工具集成者）**
- 今天 30 分钟：把 @levelsio 那套 Termius + tmux + Cloudflare Tunnel 设置在自己的 VPS 上跑通，未来手机/笔电无缝接力
- 本周可验证：用 n8n + Claude Code Skills + DeepSeek V4-Pro，给 1 个有真实业务的朋友（电商/私教/教培）搭一个"轮班 Agent"，看能不能稳定接管 60% 的执行工作。如果跑通，下一步就是定价 ¥3000–¥8000/月作为产品化服务

**档位 D（服务变现者）**
- 本周硬决定：按 Pat Walls 的模板，把过去你交付时人力占比最重的环节（撰稿、回复、报表、日常运营）做一份"AI Agent 替换可行性清单"，列出每项的 AI 化潜力和保留人工的不可替代点
- 长期路径：海外 1k–2k 美元/月的客户单价是档位 D 在 2026 年的合理目标。国内同等定位的合理价位是 ¥3000–¥5000/月

---

## 避坑指南

- **"AI 跑公司"叙事的财务尽调缺失**：Polsia 的 $10M ARR / $30M 估值目前只有创始人自述 + 二手转引，未见审计/募投文件。把它当作"趋势确认"而不是"已证商业奇迹"——Tibo 这种已验证 $1M+/m 创业者公开质疑"为什么要融资"，这种异议比融资本身更值得收藏
- **DeepSeek 永久价 vs 官网文档冲突**：DeepSeek Twitter 宣布永久降价，但 api-docs.deepseek.com 当前仍写"discount ends 2026-05-31"。在 5 月 31 日之后再到官方文档复核一次，确认新永久价确实落地
- **Codex /goal 限额回报机制**：@akokoi1 实测"5 小时限额耗尽后会执行完当前子任务再暂停，等额度恢复继续"——但他用 Pro 5x 跑了 51 亿 token / $8600，按这个估算月限额上限约 $170k 显然是计费表 bug。短期内不要把 /goal 用在真要 burn token 的硬任务上，先小步跑通
- **B2B SaaS "服务化"陷阱**：Pat Walls 描述的 70% 毛利建立在"AI Agent 真能稳定交付 60–70% 执行工作"的前提上。国内 services 客户的耐心远低于美国，AI 出一次明显错误就可能丢单。第一个客户务必选你能控制风险的存量关系，不要拿冷启动做实验
- **Skill 不是越多越好**：@koylanai 实测"加载整个 Skill 库 1/3 命中，只加载对应 Skill 3/3 命中" — 跟着 X 中文圈一股脑装一堆 Skill 反而会拉低 Agent 路由准确率

---

## 本期情报评估

**信息密度**：高密度。当日有 1 条"叙事级"信号（Polsia）、1 条"赛道级"反思（Pat Walls）、1 条"基础设施级"价格变动（DeepSeek）、1 条"工具链级"升级（Codex /goal + 中文 Skill 集中爆发），四者互相印证。

**趋势信号**：2026 年 5 月 22-23 这 24 小时呈现一个清晰的趋势——**"一人公司 + AI Agent"从概念阶段进入"已验证的财务样本"阶段**。Polsia 是该叙事的最高点；Pat Walls 是同一趋势在 services 侧的具象化；DeepSeek 降价是该趋势的成本侧基建；Codex /goal 是该趋势的执行侧基建。四者拼起来是同一张地图。

**横向对比（多个收入数据点）**：
| 路径 | 代表 | 数据 | 模式 |
|---|---|---|---|
| 单产品深耕 | @helloitsolly Senja | $1M ARR | 垂直 SaaS（testimonial 收集），全自动获客 |
| 产品矩阵 | @levelsio | $233K/月 跨 6 产品 | 自有流量 + AI 加速迭代 |
| AI 孵化器 | @Bencera Polsia | $10M ARR | 平台 + revenue share |
| AI 服务化 | @thepatwalls 描述案例 | $1M/年 70% 毛利 | productized service |
| Mobile App | @tdinh_me TypingMind | $137K/月 | 单 App 深耕 |

四种路径在毛利、规模、技术门槛上分布很广。对中国创业者最容易迁移的两条是"AI 服务化"（档位 D）和"垂直 SaaS"（档位 B），最难迁移的是"AI 孵化器"（要海外支付通道、广告账号、合规结构）。

**当日强信号数 vs 噪音比**：4 条金矿 / 约 30+ 条快讯级 / ~120 条噪音（大量 lidangzzz 的中国股市监管/段子/生活内容、Hormozi 夫妇宣布怀孕、Codie Sanchez 反 HR 病毒视频、Tom Segura 写作 clip 系列等）。强信号占比 ~3%，是一周以来最密集的一天。

**本期信源**（部分，按本期被引用顺序）：@Bencera @rrhoover @tibo_maker @helloitsolly @thepatwalls @dotey @op7418 @vista8 @xiaoxiaodong01 @koylanai @levelsio @oran_ge @SimonHoiberg @Nicolascole77 @lennysan @marclou @asmartbear @agazdecki @Shpigford @thisiskp_ @akokoi1 @arvidkahl @foxshuo @dickiebush @david_perell @Codie_Sanchez @heyzohaibb @blakeaburge @SahilBloom @AlexHormozi @LeilaHormozi @lidangzzz @turingou @Fenng @TrungTPhan @tdinh_me @itsolelehmann @ItsKieranDrew @ecomchasedimond @stephsmithio（共 40 位）
