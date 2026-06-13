# AI 一人公司日报 | 2026-06-14

数据窗口：2026-06-13 06:00 — 2026-06-14 06:00（北京时间，过去 24 小时）
深度挖掘：4 条
汇率参考：1 USD ≈ ¥7.18（2026-06-14 中间价，金额换算按此基准）

---

## 今日头条

**Fable 5 / Mythos 5 被美国政府以"国家安全"为由强制断供，英文圈一夜倒向本地模型。** Anthropic 官方公告（据推文原文及 AnthropicAI 账号直发，22,779 收藏、7,758 万浏览）确认外国国籍员工与全球客户都失去访问权限。事件本身是 AI 政策走向，但对一人公司读者真正重要的次级信号是：48 小时内 Greg Isenberg（@gregisenberg，IdeaBrowser/LateCheckoutPlz CEO）、Simon Hoiberg（@SimonHoiberg，bootstrapped SaaS 组合）、@oran_ge 几乎同时给出了"私有算力 + 开源模型"的落地框架，oran_ge 顺势点名 Kimi K2.7 Code、即将发布的 GLM 5.2 作为闭源替代——一条用闭源模型搭工作流的链路上多了一个能被一封信件关闭的开关。对中国创业者的实操含义是：本来在国内就要绕一层访问，但前 24 小时之前你的反脆弱论据是"我多套几个 API 就行"，今天起这个论据需要升级为"我手里至少要有一个本地模型 + 一份能跑通的 Skill/Agent harness"。今日金矿四条都围绕这条主线展开。

---

## 今日金矿

### 金矿 1：Greg Isenberg 本地模型八步入门 + 25 分钟配套播客

[Local Models Wakeup Playbook] — Fable 断供 6 小时内发布的可落地清单
来源：@gregisenberg（672,246 粉丝，IdeaBrowser/LateCheckoutPlz 创始人）· 2026-06-13 20:31:01 · 👍3,031 👁206,490 🔖3,379
配套播客（25 分钟）：2026-06-14 05:36:54 quote 自推文，👁6,332 🔖68
engagement_rate：0.0164（当日 Top 5%，同期中位数 0.0015–0.0020）

**核心数据（推文原文 + 推文内 Skill 名单）**
- 8 步框架：runtime（Ollama / LM Studio）→ 按硬件匹配模型（7B/32B/70B）→ 模型分工（Qwen 3 全能、DeepSeek 推理/coding、Gemma 4 移动端、Llama 微调生态）→ 量化（Q4/Q5）→ 接入 Agent（Hermes）→ 上下文窗口预算 → 工具调用 → 微调
- 硬件门槛：7B 在普通笔记本可跑，32B 需 32GB+ RAM 的 Mac，70B 起步要 DGX Spark 或顶配 Mac Studio
- 配套：@startupideaspod 25 分钟单集，覆盖 runtime、硬件、量化、Hermes 接入、本地 AI 创业方向

**对一人公司的真正意义**
不是"你今天就该跑本地"，而是这条清单第一次把"本地 AI 备份"压缩成一个周末能跑通的清单。Greg 本人引用了一段值得记的反直觉判断：他早年做创业最大流量来自 Facebook 自然流量，一次算法变更损失 99% 流量；他把今天的 Fable 事件类比为同等级的迁移信号——"别把整个工作流压在一封信就能拿走的东西上"。

**复制路径（只写真正适用的档位）**

档位 B（独立开发者）：
- 30 分钟可做：本机装 Ollama，拉一个 Qwen3-Coder-32B（或 DeepSeek-Coder-V2）做兜底，确保 Claude Code/Codex 一旦掉线，本地 CLI 能接上 Cursor/Continue 继续 vibe coding
- 本周可做：把现有 Cursor / Claude Code workflow 中"必须联网"的步骤拆出来，标注"如果掉线我用什么替代"，形成一个简易降级表

档位 C（工具集成者 / vibe coder）：
- 30 分钟可做：在 LM Studio 里启动 Qwen3-32B（OpenAI-compatible 接口）→ 让 n8n / Make / Cherry Studio 切换 base_url 试一遍，验证本地接口能否替代云端
- 本周可做：照搬 Greg 的 8 步清单，把团队/客户的 Agent harness 复制一份本地版，作为客户交付物的"应急切换"卖点

档位 D（服务变现者）：
- 一人公司咨询/培训方向可借此推出"本地 AI 应急/备份方案"作为切入服务，门槛是有一台 32GB+ RAM 的 Mac 或一张消费级 24GB 显卡，演示成本低

**国内可用性**
- Ollama / LM Studio：直接访问
- Qwen 3 / DeepSeek：国内本就方便，HuggingFace 镜像通过魔搭可下载
- Hermes Agent 框架：GitHub 直连，国内拉 model weights 要走魔搭/HF 镜像
- 配套播客 YouTube 链接：需要工具

**深度综述（约 400 字）**
这条信号的核心不是"本地模型很强"——36GB DeepSeek-R1-Distill 跟 Fable 5 之间仍有显著差距——而是它把"私有算力 + 开源模型 + 本地 Skill"从一个理想主义口号压成了一份 30 分钟能开始执行的 checklist。趋势上看，这是 2025 年 Q3 起一直在累积的"模型主权"叙事的第一次集体落地：从 levelsio 调侃"claude-fable-5 模型不存在"到 SimonHoiberg 直接想在瑞士搭 8×H200 私有节点（详见快讯），同一天里发生的所有反应都指向同一件事——闭源模型 token 从"想买就能买"变成"未必能买"。对一人公司而言，反直觉的部分在于：本地模型并不一定提升你的生产力（绝对智能仍落后云端 6–12 个月），但它第一次让"我的工作流没人能关掉"变成可买入的保险，而 Greg 给的清单足够便宜到不值得不买。最大的风险是把这条信号过度解读成"All-in 本地"——上下文窗口、长链推理仍是云端碾压，写代码 80% 的活儿短期仍要云端模型扛。竞争格局上，国内开发者天然处在"必须有一套备份"的位置上很久了，这条清单几乎可以照抄。一人公司进入"本地 Agent harness 卖给中小客户"窗口期很短，因为开源模型 + Skill 工程化门槛一旦由 Cherry Studio、KiloCode、Cline、Roo Code 一类工具填平，差异化空间只在"行业 Skill 套件"——这恰好是档位 C/D 的机会。

**原始链接**
- 主推文：https://x.com/gregisenberg/status/2065773938915889253
- 配套播客 quote：https://x.com/gregisenberg/status/2065911314971603287

---

### 金矿 2：Tibo 的 Revid $100K+/月 + "卖了的代价"

[Revid 案例] — 卖给买家半年后仍每月躺收 $100K+，但这名钱"在牢里赚"
来源：@tibo_maker（194,358 粉丝，Tweet Hunter / Taplio 创始人，$8M 已出售，目前在做产品矩阵）· 2026-06-13 16:00:06 · 👍90 👁11,180 🔖22
关联推文（被 @robwalling 在窗口内引用反驳）：Tibo "if you're selling your startup - don't" 长帖，**原帖发布时间 2026-06-11（上期窗口外）**，仅作为背景引用

**核心数据（已验证：推文原文 + 作者 X bio 互证）**
- Revid 月收入：$100K+ / 月，迁移结束后 6+ 个月持续（据其推文自述）
- 迁移动作：2025 年 11 月把 Revid 从 LemonSqueezy 切到 Stripe，新用户全部走 Stripe，老用户仍留在 LemonSqueezy 续费
- 本人 X bio 公开产品矩阵（按 bio 自述）：
  - $100K+/m Revid（视频生成 SaaS）
  - Tweet Hunter / Taplio 已于 2024 年以 $8M 出售（首付 $2M + earnout）
  - 今年 SaaS 组合 MRR 已过 $1M（据上期窗口外推文自述）

**商业模式拆解**
- 套餐结构：Revid 公开页未在本数据集中收录定价，按其 bio 自述属订阅型视频生成 SaaS，绝大多数收入来自月付订阅（**经 web_search 未抓取最新价目，建议读者自行复核**）
- 老用户惯性是"半年 $100K+/月长尾"的来源——本质是 LemonSqueezy 上的订阅没断，相当于一个月躺收上几万美金的延迟现金流
- 收入公式：约 $100K/月 ÷ 订阅 ARPU（视频生成 SaaS 一般 $20–$50/月）≈ 数千付费用户量级（推算，未经验证）

**复制路径**

档位 B（独立开发者）：
- "迁移留下的尾巴"是被低估的现金流——切支付渠道时不要强制老用户全量迁移，按到期日自然过渡，可平稳吃 6–12 个月延迟收入
- earnout 条款必须谨慎：Tibo 反思"earnout 让你每天醒来都在闪躲失败"，对应到本土并购/卖独立产品方，能拿现金尽量拿现金，宁可总价低 30–50%

档位 D（服务变现者）：
- 给 SaaS 创始人做"退出谈判咨询"是真实存在的小众服务，Tibo 的反思可以直接当案例：earnout 设计、买家接管后的产品文化冲突、卖完 1–2 年的自我认同重置都是可服务的痛点

**深度综述（约 380 字）**
两条信号合起来看比单看更有意思：Tibo 一边晒"Revid 每月躺收 $100K"，一边劝大家"if you're selling, don't"。@robwalling 的反驳更准（在窗口内 2026-06-13 15:55:06）："这些不是不卖的理由，而是别签激进 earnout 的理由。" 真正反直觉的部分在第二条里：Tibo 描述卖完之后"被定义为 'successful guy who exited' 反而几个月发不出新东西"，这是一人公司读者很少听见的隐藏成本——卖出后身份的固化比 earnout 牢笼更隐蔽，靠 build in public 起家的独立开发者尤甚。商业模式角度，Revid 的尾巴现金流验证了一个被忽视的规律：旧订阅引擎本身就是一个"半衰期资产"，切换支付通道时把老用户当成"沉睡型现金牛"，6 个月内自然衰减的 ARR 不必清零迁移；这对每一个在做 SaaS 矩阵的档位 B 都是直接可用的财务设计。风险是 LemonSqueezy 这种二级支付服务商本身在 2025 年起就有政策抖动（涉及税务跨境）——把"赖在 LS 不动"当成默认选项需要核查税务合规。竞争格局看，Tibo 的产品矩阵打法（Tweet Hunter → Taplio → Revid → 一组小产品） 是档位 B 当前最被中国独立开发者参考的范式，但要注意他能在 $1M MRR 之上做产品矩阵的基础，是已经吃到了 Tweet Hunter / Taplio 的种子用户和现金流。从零开始的独立开发者照搬这条路径时最大坑：先有一个能跑稳的现金流产品，再谈矩阵。

**原始链接**
- Revid 月收数据：https://x.com/tibo_maker/status/2065705756733636963
- @robwalling 在窗口内的反驳：https://x.com/robwalling/status/2065704500975780255
- 背景帖（窗口外）：https://x.com/tibo_maker/status/2065366119523790860

---

### 金矿 3：dotey × Orange AI — Skill 工程化已经走出实验室

来源：@dotey（@JimLiu，宝玉，224,980 粉丝，AI Engineer）+ @oran_ge（Orange AI，173,228 粉丝）
内容类型：3 条原创长帖 + 1 个 GitHub Skill 仓库

**信号 A：Orange AI《人味儿写作.skill》开源**
- 2026-06-13 06:48:15 · 👍821 👁83,188 🔖1,280 · engagement_rate **0.0154（当日 Top 5%）**
- GitHub: orange2ai/renwei-writing —— "人味儿写作 · An AI agent skill: edit people's words without erasing the person behind them"（来自 link_summary 自带描述）
- 解决场景：用 Claude/Codex 改稿，三轮之后越改越没"人味儿"——这套 Skill 通过提示词约束保留"作者具体经验、具体代价、具体存在感"
- 国内可用性：GitHub 直连可访问，Skill 文件可装载到任何 Claude/Codex Agent 上

**信号 B：宝玉拆解 Claude Design 难在哪里，并开源仿制版**
- 2026-06-14 03:12:11 · 👍39 👁3,733 🔖46 · engagement_rate 0.0123
- 核心论点：Claude Design 难度不在"产品壳"（Harness），而在底层模型必须同时具备 UI/UX 设计能力 + 数据结构 / 状态管理 / 系统架构设计能力，画好看的静态界面不算难——交付一份你能上手交互、状态保持的高保真原型，才是关键差距
- 配套：JimLiu/baoyu-design（GitHub），把 Claude Design 的 Harness 逆向出来，让其他模型也能跑一版（链接已被推文 link_summaries 收录）

**信号 C：宝玉拆解 Codex 浏览器双模式**
- 2026-06-14 02:02:40 · 👍85 👁6,355 🔖125 · engagement_rate **0.0197（当日 Top 5%）**
- Chrome 插件模式：继承登录态、Cookie、扩展，能爬登录墙后内容、操作 CRM 和企业内部系统；代价是 Chrome 自身高内存高 CPU 占用，长时间运行不稳
- 内置浏览器模式：轻量、响应快、有"标记模式"（直接在渲染页面圈选并写批注，AI 当成可执行指令），适合前端调试和公开页爬取；缺点是没登录态、反爬严的网站（如 X）容易被识别异常指纹
- 选型规则：要登录态用 Chrome 插件，要轻量就用内置；前端 UI 调试体验"指哪改哪"

**复制路径**

档位 A（内容创作者）：
- 今天 30 分钟：把《人味儿写作.skill》装到 Claude Code 或 Cherry Studio，用本周自己写过的一篇公众号文章做 A/B：原文 vs Skill 修改稿，观察"人味儿"是否保留
- 本周：建立 "AI 改稿前/后" 对比工作流，把 Skill 当成标准化质控环节

档位 B（独立开发者）：
- 把 baoyu-design 拉下来跑一遍，理解 Claude Design 的 data.jsx 数据结构 + 状态层模式，做自己产品的 design system seed
- 用 Codex 内置浏览器的标记模式重新做一遍前端 polish——按宝玉描述，比传统"截图 → IDE 改 CSS"循环快 3–5 倍（数据未独立验证）

档位 C（vibe coder / 工具集成者）：
- Codex Chrome 插件做企业内部数据搬运是被低估的轻量服务方向（如：从客户的 ERP/CRM 后台批量导数据成 CSV）；起手成本极低，按月收 ¥3,000–¥10,000 是有公开同类案例的本土区间（参考 RPA 外包市场公开报价区间，不做精确数字承诺）
- 内置浏览器跑公开页爬取，成本比 Playwright 自建低很多，且抗指纹检测能力来自 Codex Harness 自带

**深度综述（约 350 字）**
三条信号合起来揭示的是一个工程化拐点：Skill 这个概念在英文圈是 2025 年下半年 Anthropic 推出后的工程实践，到本周中文圈第一次出现了**用 Skill 解决真实写作场景**（人味儿）+ **逆向 Skill 工程让其他模型也能跑**（baoyu-design）+ **从原生工具中提炼可落地经验**（Codex 浏览器双模式）这一组完整动作。oran_ge 在另一条引用推文里用了一个比 K 型分化更精准的判断：头部用户已默认理解 Agent 由 "文档、规则、memory、loop、MCP、CLI、工具调用、权限、安全沙箱、上下文工程、定时任务、心跳、文件系统、代码执行和 Skill" 组成，普通用户只知道"Agent 能写代码"。这是中文圈 AI 一人公司读者最值得知道的认知差。反直觉的部分：宝玉指出 Claude Design 难的不是 Harness，而是基础模型必须能在"先想清楚数据结构再画 UI"这一系统设计层面碾压同行。也即模型层差距不会被 Harness 抹平，Codex 短期内做不出 Codex Design 的根本原因不是 OpenAI 工程能力不够，而是 GPT-5.5 这层还不行。风险在于 Skill 文件本身是明文提示词，知识产权护城河弱，谁开源谁吃亏；护城河只能靠 Skill 的"领域校准数据 + 工程化封装"建立。

**原始链接**
- Orange AI 推文：https://x.com/oran_ge/status/2065566882774868125
- 人味儿写作 GitHub: https://github.com/orange2ai/renwei-writing
- 宝玉 Claude Design 拆解：https://x.com/dotey/status/2065874894563463660
- baoyu-design GitHub: https://github.com/JimLiu/baoyu-design
- 宝玉 Codex 浏览器拆解：https://x.com/dotey/status/2065857399425032522

---

### 金矿 4：acquire.com 第 100 单 — AI wrapper $12,000 两个月退出

[Micro-Acquisition Marker] — 用一个"$10/月 Calendly 替代品"打包卖掉
来源：@marclou（352,138 粉丝，X bio 公开产品矩阵共 6 款 SaaS 月收 $82K+）· 2026-06-13 20:44:01 · 👍112 👁8,138 🔖3
engagement_rate 0.0004（**信号注释**：互动低，但作为退出数据点本身是确定的）

**核心数据（推文原文 + acquire.com 本身的撮合定位）**
- 售价：$12,000（约 ¥86,160）
- 持有期：< 2 个月
- 类型：AI wrapper（Marc Lou 同日 retweet 的另一条相关推文：@kylegawley "I cancelled my $10/mo Calendly subscription and vibe coded my own with Fable for $12,000"——同一价位区间，是当下"vibe-coded micro SaaS"的代表性体量）
- acquire.com 撮合记录据其官方页：撮合总额 $500M+，已促成数千 startup 出售（来自 @agazdecki bio 自述，平台规模属可信区间）

**关联信号（同窗口同一平台公开 listing）**
- @agazdecki 2026-06-14 05:43:26 同步晒出一个发票/收据生成 SaaS listing：$250K TTM 营收（约 ¥179.5 万）、$237K TTM 利润、$302K ARR、90%+ 利润率（来自推文原文，未经第三方验证）

**复制路径**

档位 B（独立开发者）：
- 把 acquire.com 当成"市场体量校准器"用：每周扫一次新上线的 < $30K listing，反向校准"我做这个领域将来能卖什么价位"，比凭感觉判断好得多
- 实操：注册 acquire.com 浏览端免费，无需绑卡即可看 listing 摘要；卖方上架免费，按成交比例分润（公开规则）

档位 D（服务变现者）：
- "帮独立开发者卖小产品做 M&A 顾问"在英文圈已有 @agazdecki 模式（取份成佣金），中文圈这条赛道几乎空白。给国内 vibe coder 卖给海外买家做撮合是档位 D 的低成本切入

**深度综述（约 300 字）**
这条信号本身的金额不大（$12K），但它的标志意义在于：第一次让一人公司读者看到"两个月做的 vibe-coded micro SaaS"已经具备明确的退出通道和市场定价。结合 @kylegawley 那条"我取消了 $10/月 Calendly，花 $12,000 vibe coded 自己的版本"的高传播段子（用 jokingly 的方式说出大众焦虑），暗示市场已经接受"$10K–$30K = 一个 wireframe SaaS 的标准退出价"。趋势上看，这跟 2024 年 acquire.com 主流交易区间 $50K–$500K 比，是一次明显的"长尾下沉"，意味着一人公司退出门槛大幅下降。反直觉部分：在国内圈层最先入场的不是"卖产品"，而是"卖产品的撮合服务"——给国内 vibe coder 找合适的海外买家做翻译/谈判/法务桥接，是档位 D 比卖产品更早能盈利的薄利位。风险：acquire.com 撮合是英文圈的信任体系，国内卖家走支付/合规要从 0 搭，建议先观察 1–2 单同行交易再下场。

**原始链接**
- Marc Lou 第 100 单：https://x.com/marclou/status/2065777209558843690
- agazdecki receipts SaaS listing：https://x.com/agazdecki/status/2065912959025742004
- @kylegawley vibe-coded Calendly 替代品（同价位段子）：被 @asmartbear retweet 至 https://x.com/asmartbear/status/2065647750671388722

---

## 快讯区

**收入信号**
- Anthropic 预计本季度首次盈利 $559M（约 ¥40.1 亿）；同时 SemiAnalysis 估算 $200/月 Claude Max 提供约 $8,000 等值 API 用量（计算口径假设打满 cap），实际用户活跃分布数据各方未披露 — @aaditsh · 2026-06-13 16:32:14（**注**：原数据来自 SemiAnalysis 第三方分析，未独立交叉核验）
- @tinyfool（@thsottiaux retweet）：Codex 用户配额重置改为允许"自选生效时间"，避免 Codex 任务跑到一半被强制重置 — 2026-06-14 01:09:36，👁375,163

**产品发布**
- @tdinh_me（Tony Dinh，X bio 自述 BlackHole/$137K/m）发布 makeawebsite.app：AI 面试用户后自动生成网站，重点客户是无技术背景的中小企业主；同款已挂上 SEO 计划 — 2026-06-13 22:48:09
- @vista8（向阳乔木）用 Codex Goal 模式 24 分钟做出 2026fifa.qiaomu.ai 世界杯赛程订阅站，支持个性化 ICS 日历订阅 — 2026-06-13 23:22:33
- Kimi 静默发布 K2.7 Code（中文圈传播来自 @oran_ge）：coding 能力据其公告提升 20%，思考 token 节省 30%；API 输入 $6.5/M token、输出 $27/M、命中缓存 $1.3/M（数据据 oran_ge 转述，**经 web_search 未独立核实**）— 2026-06-13 16:48:04
- 智谱因 Fable 断供事件官方宣告即将发布 GLM 5.2（出处同上，无独立确认）

**工具更新**
- @marclou DataFast 新增渠道筛选：分别拉出 ChatGPT/Claude/Gemini 等 AI 流量、Affiliate、邮件三类来源的转化营收 — 2026-06-13 23:13:01
- @dickiebush 推 7 条 Claude Design 设计指南/提示词，定位写作者的视觉素材（newsletter landing、课程销售页、邮件 header）—— 2026-06-14 05:36:14
- @runes_leo 总结 Tailscale 把韩国 VPS 配成 Exit Node 的全平台分发方案，要点是 "Exit Node 按设备启用而非全局"，手机保持 tailnet 在线但 Exit Node 默认关，避免国内 App 受影响 — 2026-06-13 21:06:29
- @xiaohua_888 推荐 Mac 用户从 Shadowrocket 切换到 FlClash，理由是 Shadowrocket 在 Mac 端有断网 bug — 同窗口

**值得关注的观点**（仅收录已验证 solopreneur 的判断）
- @SimonHoiberg 想在瑞士搭 8×H200 私有节点，跑 GLM/Kimi 级模型，按月卖给本地 SaaS 创始人订阅算力："本地化主权算力 + 月费订阅"作为一个商业模式，开始有人公开测试 — 2026-06-13 22:42:42
- @SimonHoiberg：bootstrapped SaaS 在 2026 年的边界——"10 人团队可做 +$10M ARR，3 人可做 +$1M ARR，1 人可做六位数 ARR"，配套清单含 AI 客服 / CRM / Workflows / Meta+Google 广告 / 月度 YouTube + 周度邮件 + 日度 LinkedIn 三类内容 — 2026-06-13 19:30:37
- @awilkinson（Tiny 联合创始人）调侃 2026 年 Agent 自动化的真实分布："50% 加新 Skill / 30% 修新 Skill 弄坏的东西 / 20% 抓狂"——一句话指出 Skill 工程化的隐藏运维成本 — 2026-06-14 02:01:36

**教训与反思**
- @tibo_maker "if you're selling - don't" 长帖经 @robwalling 在窗口内反驳后形成更准确的版本：**不卖不是结论，"别签激进 earnout 条款"才是**——理由是 earnout 等于 2 年牢笼，每次达成里程碑只感觉是侥幸而非胜利 — 反驳在 2026-06-13 15:55:06
- @tinyfool：App 上线后 IAP 物品和订阅项仍在审核状态——用户能下载却无法付费，是 App Store 流程被忽视的一类陷阱 — 2026-06-13 22:29:38

**传播力素材**（适合自媒体改写的高互动观点）

- "The only truly wasted time is time spent wishing you were somewhere else." — @naval · 👍15,970 👁373,231 · engagement_rate 0.63%
  改写方向：适合视频号 + 公众号开篇引用——把"羡慕别处"这个心理动作具体化成 3 个一人公司创业者常见场景（下班后刷别人的产品、刷别人的 MRR 截图、刷别人的城市），配合 Naval 这条做闭篇。
  点评：这句的力量在于把"焦虑"具体化成"时间被浪费"，对一人公司读者是命中要害的——独立创业者最常陷入的状态就是边工作边刷别人。但它的盲区是不区分"健康的对标"和"耗能的羡慕"，单看这句容易把所有横向对比一刀切掉，丢掉"看同行学打法"的合理动作。

- "I don't know a single person who obsessed over something for 10 years straight, surrounded themselves with peers with the same goal, and genuinely went all in that didn't end up successful." — @Jayyanginspires · 👍466 👁9,508 · engagement_rate 0.93%
  改写方向：适合小红书图文长卡片——把"10 年 + 同伴 + all in"做成三段式构图，每段配一个中国一人公司读者熟悉的对标人（如：levelsio 12 年独立开发、Marc Lou 5 年 SaaS 矩阵、damengchen Ghost 10 年开源）。
  点评：这句话的独创性在于把"成功"还原成三个可观测变量（持续年限、同伴质量、投入度），而不是"努力 + 运气"这种空话。盲区是把"成功"狭义化为公众视角下的成功，忽视了"all in 10 年但项目方向不对"的存活者偏差——很多人 all in 10 年最后发现做错了方向。

- "Sleep hits harder when you're exhausted. Food tastes better when you've gone hungry. Water tastes sweeter when you've been grinding. Music hits deeper when you've been in silence. Deprivation sharpens pleasure. Don't run from suffering. That's what gives life its color." — @Jayyanginspires · 👍53 👁1,414 · engagement_rate 0.99%
  改写方向：适合公众号晨间推送或 podcast 开场白——做成"创业者的剥夺感美学"系列，把"deprivation sharpens pleasure"翻译成中文场景下的"延迟满足练习"。
  点评：这条的独创性在于把"忍耐"重新定义为"放大快感的工具"而非"咬牙坚持"，是一人公司读者会真正记住的反框架。盲区是 deprivation 用错地方会变成自我折磨——这条放在 burn out 的人面前是毒药，需要配合"是否仍在恢复曲线上"的判断使用。

- "The takeaway from Fable 5 being BANNED by the government: GET GOOD AT LOCAL MODELS SO YOU HAVE 100% CONTROL... Same sorta moment (but bigger) for AI. This is a wake up call." — @gregisenberg · 👍3,031 👁206,490 · engagement_rate 1.64%
  改写方向：适合视频号长内容——做成"AI 一人公司的反脆弱清单"，把 Greg 的 8 步翻译成中文 + 加一个第 9 步"中国创业者的本地化备份"。
  点评：这条引发共鸣的核心是它戳中了"我建立的工作流是我的资产"这个错觉——其实没有所有权的工作流随时可能被取消。盲区是"sovereignty"叙事容易被过度解读成"All-in 本地"，事实上 80% 的活儿短期内本地模型仍跑不动，本地模型只是保险不是主力。

---

## 延伸资源库

### 播客 / 视频 / 访谈
- **Startup Ideas Pod**（@startupideaspod）单集，约 25 分钟：本地模型八步入门 + 本地 AI 创业方向（出处 @gregisenberg quote tweet，发布时间 2026-06-13 21:36 北京时间）— 时间戳未获取
- **Karpathy: How ChatGPT Actually Works**（aaditsh 推荐）：3.5 小时免费课程（YouTube），由 Andrej Karpathy（前 Tesla Autopilot 负责人）发布——课程链接含 YouTube 嵌入，国内访问需要工具
- **Lenny Rachitsky 与 Benedict Evans 对谈**（上期视频回炉转发）：AI 价值在 stack 哪一层落地、为什么 distribution 仍是最强护城河——属窗口外内容，不进金矿，仅作参考

### 图书 / 课程
- 本期无新书推荐

### 链接汇总（已 web_fetch / web_search 验证 → 实际为推文 link_summaries 内嵌验证）

**工具类**
- 人味儿写作 Skill: https://github.com/orange2ai/renwei-writing （link_summary 内嵌验证）
- baoyu-design（Claude Design 仿制 Skill）: https://github.com/JimLiu/baoyu-design
- makeawebsite.app（Tony Dinh 新品，AI-interview → 网站生成）
- 2026fifa.qiaomu.ai（vista8 用 Codex Goal 24 分钟做出的世界杯订阅站）
- FlClash 客户端: https://github.com/chen08209/FlClash
- futureme.dev（写信给未来的自己，@abdussalampopsy 的轻量用例）

**报道类**
- Anthropic 官方：Statement on the US government directive to suspend access to Fable 5 and Mythos 5 — https://www.anthropic.com/news/fable-mythos-access （link_summary 自带描述确认）
- Trung Phan 解读 FIFA World Cup 票务: https://www.readtrung.com/p/fifas-world-cup-ticketing-fiasco

**播客 / 视频类**
- Greg Isenberg Startup Ideas Pod 单集 quote: https://x.com/gregisenberg/status/2065911314971603287
- YouTube Karpathy 课程链接（具体 URL 在原推文 t.co 短链中，未单独抓取）

**GitHub / 工程类**
- orange2ai/renwei-writing（人味儿写作 Skill）
- JimLiu/baoyu-design（Claude Design Skill 仿制）
- chen08209/FlClash（Clash 客户端，Mac 推荐替代 Shadowrocket）
- tw93/Kami（同窗口被 @dotey quote，简历生成 Skill）

---

## 行动建议

档位 A（内容创作者）
- 30 分钟内：装《人味儿写作.skill》到 Claude Code / Cherry Studio，用本周公众号文章 A/B 测试改稿效果
- 本周可验证：用 Claude Design（或 baoyu-design 跑国内可用模型）给最近一篇主推内容做 landing page，对比"自然图文"vs"专为长尾流量做的 landing"的转化差异

档位 B（独立开发者）
- 30 分钟内：本机装 Ollama，拉 Qwen3-Coder-32B 作为 Claude Code/Codex 掉线兜底；写一个简易降级表
- 本周可验证：把现有产品订阅迁移计划改成"按到期自然过渡"而非"强制全量切换"，参考 Tibo 在 LemonSqueezy → Stripe 之后的 6+ 个月长尾现金流

档位 C（vibe coder / 工具集成者）
- 30 分钟内：把 Codex 内置浏览器的标记模式跑一遍，体验"指哪改哪"的前端 polish 流程
- 本周可验证：用 Codex Chrome 插件做一个客户内部后台数据导出小工具，定价从 ¥3,000/月起步试单（参考 RPA 外包公开报价区间）

档位 D（服务变现者）
- 30 分钟内：注册 acquire.com，浏览 < $30K 的 listing，建立"中文 vibe coder × 海外买家"的撮合候选名单
- 本周可验证：给至少 3 个独立开发者朋友提供一份"earnout 风险清单"，用 Tibo 反思 + robwalling 反驳做模板

---

## 避坑指南

- **earnout 不是"延迟收款"是"两年牢笼"**：Tibo 描述卖完后每天醒来都在闪躲失败、达成里程碑只觉得侥幸；@robwalling 修正后的版本是"别签激进里程碑"，能拿现金尽量拿现金。对一人公司读者：本土并购市场也常见类似设计（对赌、业绩承诺），同样适用
- **App Store 流程的隐藏陷阱**：@tinyfool 案例——App 已上线，IAP 物品和订阅审核仍未通过，用户能下载但无法付费。在 App Review 流程中 IAP 是独立子流程，提交前必须确认套餐项已审核通过
- **闭源模型工作流的单点风险**：Fable / Mythos 断供事件第一次把"我建立的工作流是我的资产"这个错觉打破。所有把核心生产环节压在单一闭源模型 + 单一 API 服务商上的设计，都要重新评估降级方案

---

## 本期情报评估

**信息密度**：高密度
原因：Fable / Mythos 断供事件触发了同窗口内 4 条以上的实质性反应（Greg 的本地模型清单、SimonHoiberg 的私有节点提议、oran_ge 的 Skill K 型分化判断、dotey 的 Codex/Claude Design 拆解），不是单点新闻而是一组协同信号；此外有 Tibo Revid $100K+/月 + acquire.com 第 100 单两组独立的收入/退出数据点

**趋势信号**：
模型主权焦虑触发"私有算力 + 开源模型 + Skill 工程化"在中英文圈同时落地为可执行清单；与此并行，"Skill 时代"在中文圈完成了从概念到可开源工具的拐点（人味儿写作 + baoyu-design + Codex 浏览器拆解三件套同期出现）。

**横向对比（路径选择）**：
本期出现至少三种典型一人公司路径——
- **产品矩阵型**（Marc Lou、Tibo）：用一个起家产品的现金流孵化矩阵，Tibo 公开 SaaS 组合 $1M MRR 是当下最直观的中文圈参考模板
- **单产品深耕型**（Tony Dinh BlackHole $137K/月，levelsio PhotoAI $100K/月）：把一个产品做到天花板再做下一个
- **平台撮合 / Skill 工程化变现**（acquire.com、Skill 开源者）：不直接做产品，做交易场或工具上游
这三条路对应档位 B / C / D 不同切入点，没有谁是绝对优解。

**当日强信号数 vs 噪音比**：
A 级强信号 1 条（Greg 本地模型清单）+ B 级 3 条（Tibo Revid 数据、dotey/Orange AI Skill 三件套、Marc Lou acquisition #100）；噪音端是大量围绕 Fable 段子的二次创作（claude-fable-5 模型不存在系列、torrent 段子）和 Naval/Jay Yang 大量短金句——已分别放入"传播力素材"和过滤层。

**本期信源**：@gregisenberg @tibo_maker @robwalling @marclou @agazdecki @kylegawley @asmartbear @dotey @oran_ge @SimonHoiberg @tdinh_me @vista8 @aaditsh @runes_leo @xiaohua_888 @awilkinson @tinyfool @naval @Jayyanginspires @dickiebush @bentossell @levelsio @lidangzzz @AnthropicAI（转推源）@Prathkum @abdussalampopsy @Fenng @turingou @itsolelehmann（共 29 位）
