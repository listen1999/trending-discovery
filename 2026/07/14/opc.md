# AI 一人公司日报 | 2026-07-14

数据窗口：06:00 — 06:00（北京时间，过去 24 小时）
深度挖掘：3 条

---

## 今日头条

Marc Lou（已验证高收入 solopreneur，个人 SaaS 产品组合月收入 $79K+，据其 bio 自述）今天发布了一篇关于 SaaS 分发逻辑的判断推文，核心论点是：**如果今天重新做一款 SaaS，应把"AI 可见度"设为北极星指标，而非传统 SEO 或 DAU**。他以 Postiz（@wickedguro）从 $0 增长到 $150K MRR 作为"AI agent first startup"的验证案例——而 @wickedguro 本人当日同步宣布 Postiz 已达 $154K MRR 并分享了完整增长路径。两条推文互相印证，构成本期最强信号：流量入口已在从 Google 向 LLM 迁移，这件事今天有了具体的商业数据支撑。

---

## 今日金矿

### 金矿 1：Marc Lou 的"AI 可见度优先"框架 × Postiz $154K MRR 完整路径

[Postiz] — AI 优先的社交媒体调度工具
来源：@marclou · 2026-07-13 08:54 · 👍465 👁55,732 · bookmarks 456 · engagement_rate 0.82%（同期中位数约 0.16-0.20%，高出约 4 倍）

@marclou 在帮一位正在副业做 micro SaaS 的朋友（YouTube 达人数据库工具）诊断增长慢的问题时，去 ChatGPT 搜索"how to find youtubers to sponsor"——ChatGPT 推出的是大型通用数据库，朋友的产品没有出现。这个观察引发了他的核心判断：

> 如果今天重新起步做 SaaS，我会把"AI 可见度"设为北极星指标，并向后倒推所有决策。
>
> 目标是让潜在客户能：
> 1. 通过 ChatGPT 找到我的产品
> 2. 在 ChatGPT 里完成 onboarding
> 3. 从 ChatGPT 里直接获取价值
>
> llms.txt、markdown 文件、在 Reddit/YouTube 获得提及……总之，成为一个 AI agent first startup，正如 @wickedguro 用 Postiz（$150K MRR）所做的那样。

**核心数据（已验证）**

- Postiz 当前 MRR：$154K/月（约 ¥112 万/月，按 1 美元≈7.26 人民币）— 据 @wickedguro 推文原文 + bio 自述
- 完整增长路径：$0 → $3K → $12K → $21K → $154K MRR — 据推文原文（@wickedguro, 2026-07-13）
- @wickedguro bio：Postiz Agentic Social Media Scheduler $154k/m；另有 UGC videos for agents $2.6k/m 第二条产品线

**商业模式拆解**

- 产品定位：AI 驱动的社交媒体调度工具，主打 agentic 工作流（自动生成、调度、发布）
- 开源先行：项目为开源，降低信任成本，扩大用户基数后通过 hosted 付费版变现（经 web_search 未找到官方定价页补充信息，待验证）
- 增长引擎：@wickedguro 明确提到核心是"分发（distribution）和定位（positioning）"，而非产品技术壁垒
- 增长阶段拆解（据推文原文）：$0→$3K（冷启动期）→$12K（产品验证期）→$21K（增长期）→$154K（规模化期）

**复制路径（仅适用档位）**

档位 B（独立开发者）：
- 立即行动：为现有产品添加 llms.txt 文件，用自然语言说明产品功能、使用场景、API 接口，使 LLM 在被问到相关问题时能引用和推荐
- 冷启动期：在 Reddit（r/SaaS、r/IndieHackers 及垂类社区）发布真实使用案例；在 YouTube 做教程视频——这两类内容是 LLM 训练数据的核心来源之一
- 产品设计原则：产品的核心价值主张必须能在一段对话里解释清楚，功能模块化，文档结构化（markdown 优先）
- 验证方法：直接去 ChatGPT 搜索自己赛道的核心关键词，看产品是否出现；如果没有，这就是 AI 可见度的差距所在

档位 C（工具集成者）：
- 国内转化路径：ChatGPT/Claude 在国内可及性受限，等效策略是在小红书/知乎/B 站/即刻被 AI 工具号、测评号引用（这些内容会进入国内大模型的训练语料）
- 调度工具方向：国内类似方向是多平台自动发布工具（微信/抖音/小红书），但各平台 API 限制严格，需要以内容代发为主，对接平台官方合作接口

**深度综述**

这条推文的信号强度超过了大多数纯数字披露，原因是它提供了一个**可验证的判断框架**，而不只是一个数字。Postiz 的增长路径有清晰的阶段划分和公开数据印证，Marc Lou 提出的"AI 可见度北极星"逻辑也有 Postiz 作为具体案例。两者叠加，构成一个可以直接行动的信号。

从商业模式角度，Postiz 的路径揭示了一个结构：**开源建立信任 → 社区分发 → AI 推荐获客 → 付费版变现**。这与上一代 SaaS 的"付费广告 + 内容营销"路径完全不同，但逻辑一致：找到最低摩擦的分发渠道，在竞争对手反应之前建立规模优势。@wickedguro 的 bio 还显示他已经在布局第二条产品线（UGC videos for agents，$2.6K/m），说明他在用 Postiz 的现金流支撑更多产品探索——这是一人公司产品矩阵化的典型路径。

**最出人意料的部分**：Marc Lou 没有说"做好 SEO"，而是说"让 AI 能帮你 onboard 客户"。这意味着产品不只要让 LLM 知道你存在，还要让 LLM 有能力替你完成从发现到交付价值的整个旅程。产品设计的颗粒度必须足够细，才能被 AI 理解和转述——这实际上是在倒逼产品自身的清晰度。

**中国市场障碍**：llms.txt 等标准的中文生态支持几乎为零；国内大模型的训练数据引用机制不透明；微信/抖音/小红书的内容不易被 LLM 实时检索。真正的 AI 可见度优化在中国需要走社区内容路径（被高权重 KOL 引用），而非技术文档路径。

**竞争格局**：国内社交媒体调度工具（微盟、帷幄等）主要面向企业客户，价格偏高，没有 agentic 功能。AI 优先调度工具在国内是空白，但平台 API 限制是实质性护城河——这不是技术问题，是合规和关系问题。进入的窗口期存在，但门槛不低。

---

### 金矿 2：ChatCut + Codex — 3 步让 AI 帮产品生成配音演示视频

ChatCut agent plugin | AI 视频剪辑工具，可通过 agent 接口调用
来源：@vista8 (向阳乔木，PM，115K followers) · 2026-07-13 10:29 · 👍614 👁50,528 · bookmarks 833 · engagement_rate 1.65%

@vista8 分享了一个极简教程：用 ChatCut 的 MCP + Skill 插件，通过 Codex 为任意产品网址生成"图文并茂 + 配音解读"的功能演示视频，全程三步。

**完整步骤（逐条列出）**

1. 发给 Codex，安装插件：`https://github.com/ChatCut-Inc/agent-plugin`
2. 系统自动安装 MCP + Skill，触发一次 OAuth 授权
3. 对 Codex 说：「用 ChatCut 的 MCP 和 Skill 给【目标网址】做一个图文并茂、有配音解读的功能演示视频」

**效果评价（据推文原文）**：视频质量"虽然粗糙，但比文字生动多了"

**核心信息（已验证部分）**

- GitHub 仓库：ChatCut-Inc/agent-plugin（仓库存在，描述为"Plugin for agents to interact with Chatcut"，据链接摘要验证）
- 官方定价：经 web_search 未找到补充信息
- 国内可用性：GitHub 可直接访问；Codex（OpenAI）需要工具；ChatCut 本体需进一步确认

**前置条件**：需要有 Codex（或支持 MCP 的 coding agent）账号，并有对应 API 权限

**复制路径（仅适用档位）**

档位 A（内容创作者）：
- 做 AI 工具评测的创作者可用此流程快速生成"30秒看懂这个工具"系列视频
- 直接用于小红书、抖音的工具种草内容；质量粗糙可做二次剪辑
- 注意：Codex 国内需要工具，使用前需解决访问问题

档位 B（独立开发者）：
- 为自己产品快速生成 Demo 视频，用于 ProductHunt 上线、cold email 或 landing page
- MCP 接口架构意味着 ChatCut 是 agent-native 产品，可以进一步调研 API 自定义脚本

档位 C（工具集成者）：
- 可以将此流程嵌入 n8n 自动化工作流：新产品页面上线 → 自动触发 ChatCut → 生成 Demo 视频 → 上传到内容平台

**深度综述**

这条推文的高 engagement_rate（1.65%，同期约 4-5x 中位数）和高 bookmarks（833）反映了一个具体痛点：**独立开发者需要演示视频，但制作成本太高**。录屏 + 剪辑 + 配音通常需要数小时，对一人公司来说是挤压产品时间的重负。ChatCut 用 AI agent 自动化了这个流程，把几小时的工作压缩到几分钟。

更值得注意的是 ChatCut 的**分发策略**：它通过 MCP + Skill 嵌入已有 agent（Codex），而不是要求用户下载新应用。这正是 Marc Lou 在金矿 1 里说的"AI agent first startup"的具体体现——产品入口就是对话框，onboarding 摩擦趋近于零。

当前局限：生成质量"粗糙"（据推文原文），不适合直接对外正式展示，更接近内部原型或快速 Demo。对 B2B 销售演示、投资人 pitch 材料等高质量需求，仍需人工打磨。

国内复制方向：国内类似需求（产品 Demo 视频）正在被 Cursor + 剪映 AI 工具链部分解决，但没有 MCP 级别的 agent 接入方案。如果剪映/CapCut 未来开放 agent API，这个方向的国内版本会有很大空间。

**原始链接**：https://github.com/ChatCut-Inc/agent-plugin

---

### 金矿 3：Knockoff.co — 识别亚马逊仿品产地的工具，ProductHunt 上线

Knockoff.co | 帮助消费者识别电商平台产品来源国的数据库工具
发布日期：2026-07-13
国内可用：直接访问（knockoff.co）

来源：@Shpigford (Josh Pigford，独立开发者，70K followers)·2026-07-13 发布当日发出 8 条相关推文

**产品定义（据推文内容）**

Knockoff.co 是一个数据库工具，帮助用户在亚马逊等电商平台购物时识别产品来自哪个国家。新功能（本期宣布）：可以看到每个产品的来源国（🇺🇸🇨🇳🇭🇰🇨🇦🇬🇧），数据依赖社区贡献。

**本期关键信号**

- Josh 自述："caught lightning in a bottle"（产品突然爆火）；"now to figure out how to not screw it up"——说明爆发是意外，变现策略尚不明确
- ProductHunt 上线：https://www.producthunt.com/products/knockoff-2（本期上线）
- 新功能讨论：Josh 在推文中讨论是否要过滤某个仿品品牌（显示为 ridge wallet 竞品），体现数据准确性是核心挑战
- 技术开发状态：Josh 当日询问如何让 Claude Code 跨两个仓库（一个开源、一个非开源）工作，说明是真实一人公司开发阶段

**收入数据**：无公开数据（[未经验证]，推文中无收入数字）

**核心功能**

- 搜索特定品牌时，展示来自哪个国家的仿品/同类产品
- 社区驱动的数据贡献模式（用户可提交产品来源信息）

**定价**：经 web_search 未找到补充信息

**复制路径（仅适用档位）**

档位 B（独立开发者）：
- 国内反向类比：帮助跨境电商卖家了解亚马逊同类产品的来源国分布（竞品来自中国哪个省份、价格带分布等），这是一人公司可以做的数据工具
- 另一个方向：帮助国内消费者识别某款热门产品是否为真正美国/日本品牌还是中国代工（目前在小红书是人工分散的信息）

**深度综述**

Knockoff.co 的爆发是一个典型的"贸易摩擦套利"产品时机：2026 年中美贸易紧张背景下，美国消费者越来越想知道"这个产品到底来自哪里"，而亚马逊没有明确披露这个信息，甚至存在模糊化倾向。Josh 抓住了这个信息不对称，做了一个数据聚合工具。

"caught lightning in a bottle"这句话本身也是一个信号：Josh 没有预料到爆火，这说明**产品-市场共鸣是在发布之后被验证的，而不是提前设计的**。对独立开发者来说，这也意味着快速上线、观察反应比精心规划更有价值。

关键风险在于数据质量：Josh 讨论是否要过滤特定品牌，说明社区贡献模式下，垃圾数据和争议内容会很快出现。如何在"用户贡献"和"数据准确性"之间做裁判，是这类产品的长期护城河——也是最难自动化的部分。

对中国创业者的直接复制价值有限：Knockoff.co 的核心需求来自美国消费者对"中国制造"的信息需求（有时伴有排斥情绪），这个需求在国内没有等价对应。但**供应链透明**这个大方向，在国内有多个垂类可以切入（如真伪鉴别、产地认证、溯源码等），只是市场教育和政策监管难度更高。

---

## 快讯区

**收入信号**

- getebook.ai（AI 电子书工具）据 @marclou 报道，目前 $1K/天（约 ¥7,260/天），增长率 +2,972%（据推文原文），trustmrr.com 可查；@marclou 此前引用时增长率为 +1,326%，增长加速明显。产品具体功能未明。[未经验证，来源：@marclou 推文 + trustmrr.com/startup/getebook-ai] — @marclou · 2026-07-13 16:20

- Simon Høiberg (@SimonHoiberg，160K followers) 2026 年多产品组合收入 $100K-$150K/月（约 ¥73-109 万/月）；含 FeedHive（订阅）/LinkDrip（订阅）/Aidbase（订阅）/FounderStack（一次性购买）/TinyKiwi（一次性购买）；个人品牌渠道（YouTube、X、咨询）。全部从 2021 年一个 Twitter 工具起步，"Start small. Keep going"。[据推文原文] — @SimonHoiberg · 2026-07-13 23:03 · engagement_rate 0.82%

- 云备份平台（自动保护 GitHub/GitLab/Azure/Linear 等数据），$120K ARR（$102K TTM），在 acquire.com 出售 — @agazdecki · 2026-07-14 04:19 [据推文原文]

**工具更新**

- OpenAI 官方 Codex 提示词 9 套工作流（@xiaohu 整理汇总）：修 bug、截图变原型、云端重构全覆盖，官方把分散各处的提示技巧收入统一框架（目标/背景/输出/边界 + Codex 专属工作流范例）。链接：https://best.xiaohu.ai/article/chatgpt-prompting-guide/ — @xiaohu · 2026-07-13 13:58 · engagement_rate 1.20% · bookmarks 420

- OpenKnowledge 开源个人知识库：可理解为开源版 Obsidian + LLM Wiki。内置 MCP/Skills/Chat/TUI，可直接调用 code agent 处理内容；原生支持 Git 同步；与 Obsidian 配合使用（Obsidian 负责采集，OpenKnowledge 负责整理和 agent 调用）。本地优先，隐私安全 — @indie_maker_fox · 2026-07-13 14:10 · engagement_rate 1.97% · bookmarks 198

- Anthropic 延长 Fable 5 在 coding plan 里的访问到 7 月 19 日，GPT 暂时取消 5 小时限额 — 据 @akokoi1 · 2026-07-13 07:35

**值得关注的观点**（仅限已验证 solopreneur 的实质判断）

- @tibo_maker（Tweet Hunter 联合创始人，已 $8M 退出）：免费工具是他每一款 SaaS 最大的增长渠道之一——每个细分市场都有几个"free [thing] generator"关键词，排名弱的页面，做一个好工具、占据这个词、获得细分流量和外链。他已在 Outrank 里内置了这个功能（文字转图片 → logo/avatar/og image 等） — @tibo_maker · 2026-07-13 17:48 · engagement_rate 0.73%

- @SimonHoiberg：自己的营销团队"越来越小"——不是不做营销，而是大量重复生产工作被 agent 和专用工具接管了（YouTube 脚本用 Claude、视频用 Remotion、社交草稿用 AI、调度用 FeedHive、SEO 用 GPT-5.5+Claude+n8n）。"创始人仍然得带来品味，但未来的营销团队不是 12 个人在 Slack 传文件" — @SimonHoiberg · 2026-07-13 20:27 · engagement_rate 1.51%

- @arvidkahl（FeedBear 创始人，203K followers）：agentic engineering 反而会提升整体代码库质量——人们开始写文档、写测试。已有 SaaS 的代码库会被 AI 工具逐步加固和优化，不太需要担心被 AI 直接颠覆 — @arvidkahl · 2026-07-14 03:13

**教训与反思**

- @op7418 (歸藏，160K followers，AIGC 周刊)：自己开源的 AI Skills 被人在某平台打包成 199 元一份出售，据截图显示销量已产生 40 万元（约 2000 份）左右。骂完之后本人说"分我点"。信号含义：开源工具的知识付费二次销售市场在中国真实存在，且消费者愿意为"打包好的工作流/技巧"付费；原创者不一定是变现方 — @op7418 · 2026-07-13 21:48 · engagement_rate 0.34% · bookmarks 223

**传播力素材**

- "One of the best pieces of advice I ever got: If you want a calmer life, you need to address small problems while they're still small. The cost of dealing with an issue rarely gets cheaper with time. Procrastination turns uncomfortable things into unavoidable things." — @blakeaburge · 👍11,365 👁179,827 · engagement_rate 1.31%
  改写方向：适合小红书或公众号，把"小问题拖大"拆成三个具体创业场景（跟联合创始人的小矛盾、第一个客户投诉、产品小 bug）对比及时处理 vs 拖延后的代价差，比泛泛说"别拖延"更有说服力
  点评：这句话之所以广传（2361 bookmarks），是因为它把"问题复利"量化成了直觉——不是说"要积极面对"，而是说"不处理的代价在增长"。对创业者最大的误读风险是：误以为所有小事都要立刻处理，制造焦虑感；实际上这句话只对*有解决路径的*小问题有效，真正的战略选择仍然需要忽略大量噪音

- "Every paycheck you get is evidence that someone else figured out how to monetize your skills better than you did." — @thejustinwelsh · 👍3,646 👁208,581 · engagement_rate 0.30%
  改写方向：适合小红书职场觉醒 / 公众号"认知颠覆"类选题，可做成"你的工资单其实是一张授权书"的框架；这条和 @jasonfried 的反驳（"working for someone else is an excellent choice most of the time"）做对比，会产生更好的讨论度
  点评：这句话的张力在于它把"工资"重新定义为"能力被他人货币化的凭证"，而不是安全感来源。但它的隐含前提（自雇比受雇更好）是有争议的。@jasonfried 同一时间的反驳获得 1712 likes，说明这个论断本身不是共识，读者在选择性接受符合自己预设观点的信息

- "If you can describe people's problems better than they can, they'll subconsciously believe that you have the solution. The pain is the pitch." — @Jayyanginspires · 👍192 👁5,040 · engagement_rate 1.61%
  改写方向：适合写给 B2B 创业者的内容营销教程，或"会写文案的人都懂的底层逻辑"系列；可以做成实操版本，列出 5 个行业的具体痛苦描述方式
  点评：engagement_rate 1.61% 在小粉丝账号中属于异常高（@Jayyanginspires 仅 94K followers），说明这句话击中了销售写作的具体痛点。它比"了解客户"更精确——精确到"你的描述比客户自己更准"这个程度。局限：这个技巧依赖真实的痛苦理解，如果只是套话式描述，效果反而会让客户觉得被操控

---

## 延伸资源库

### 播客 / 视频 / 访谈

Lenny Podcast：**2026 年科技从业者心态调查深度讨论**
主播：@lennysan × @noamseg
视频链接：https://youtu.be/_cmpIveXnvE（需工具访问）

核心数据摘要（据推文原文）：
1. 科技从业者的第一恐惧不是被 AI 取代工作，而是"被要求用同样薪水做更多事"
2. 拥有高效经理的员工，工作满意度比其他人高约 65%，burnout 显著更低；但只有 25% 的受访者认为自己有高效经理
3. Burnout 在一年内上升 10 个点；乐观度下降 6 点
4. AI 正在把科技从业者一分为二：50% 感到被放大（amplified）；50% 感到角色被重新定义（27%）、不稳定（14%）或被缩小（5%）
5. 创始人仍是科技圈最快乐的人群（连续第二年），burnout 最低，乐观度最高
6. 公司规模与员工痛苦程度线性正相关：1-10 人的初创公司员工最满意，5000+ 人公司员工最痛苦，没有例外

### 图书 / 课程

Alex 的免费创业书（书名、作者未在推文中明确标注）
推荐人：@marclou（"今年读过最好的书"）
内容：描述从 $0 → $50K/月 → $0 的完整创业周期，真实复盘最高峰和最低谷
最大收获（据推文原文）："不要爱上你的想法，与其修复一艘正在下沉的船，不如去尝试新的事物"
engagement_rate 0.78% · bookmarks 1008
注：书是免费的，具体链接需从 @marclou 推文获取（[链接未在原文中提供]）

### 链接汇总（按类别）

工具类：
- ChatCut agent plugin（GitHub）：https://github.com/ChatCut-Inc/agent-plugin
- Knockoff.co（ProductHunt）：https://www.producthunt.com/products/knockoff-2
- OpenAI Codex 提示词工作流（@xiaohu 整理）：https://best.xiaohu.ai/article/chatgpt-prompting-guide/

收入验证：
- getebook.ai（trustmrr.com）：https://trustmrr.com/startup/getebook-ai
- Postiz 增长路径推文（@wickedguro）：https://x.com/wickedguro/status/2076703406446858426

获取渠道：
- acquire.com 云备份平台（$120K ARR，在售）：https://app.acquire.com/startup/bnyIRYgJAwOWahpJuS5TOPbCdk92/DAJQXKevemBwQhAgboZu/

---

## 行动建议（按档位分组）

档位 A（内容创作者）
- 今天 30 分钟：参考 @vista8 的 ChatCut 教程（金矿 2），测试"用 Codex + ChatCut MCP 为一个 AI 工具生成配音演示视频"的完整流程；如果质量够用，可以系列化做 AI 工具测评内容

档位 B（独立开发者）
- 今天 30 分钟：去 ChatGPT 搜索自己产品所在赛道的核心关键词（比如"[你的产品做的事] tool"），看产品是否出现；如果没有出现，这就是下周的待办事项——添加 llms.txt，把产品文档改成 markdown
- 本周：为现有产品创建 llms.txt 文件；在一个垂类 Reddit 社区发布一篇真实的使用案例（不是广告，是使用记录）

档位 C（工具集成者）
- 本周：测试 ChatCut agent plugin 是否可以接入 n8n 或 Make，实现"产品更新触发视频生成"的自动化工作流

---

## 避坑指南

- **"AI 可见度优先"在中国需要路径转换**：海外的 llms.txt + Reddit/YouTube 策略在国内没有直接等价物，国内大模型训练数据引用机制不透明。等效做法是在知乎/小红书/B站被 AI 工具评测号真实引用，而不是提交 llms.txt 文件等技术层面的操作

- **"caught lightning in a bottle"之后**：ProductHunt 的流量通常在 48-72 小时内消退。Josh Pigford 自述 Knockoff.co 爆火是意外，目前变现策略不明；即使产品吸引力真实存在，没有留存机制和持续分发渠道的话，爆发等于归零

---

## 本期情报评估

**信息密度**：正常

**趋势信号**：AI 可见度（产品能否被 LLM 推荐）正在成为 2026 年 SaaS 分发的新竞争维度；AI 工具在内容生产、营销执行和演示材料制作上的替代正在从"概念"进入"日常工作流"（ChatCut、Simon Høiberg 的营销团队压缩都是这个方向的具体信号）

**横向对比**（本期三个收入数据点）：

| 产品 | MRR/收入 | 路径 |
|------|---------|------|
| Postiz（@wickedguro） | $154K/月 | 开源 + AI 优先 + 分发/定位驱动 |
| getebook.ai | ~$30K/月（$1K/天）[未经验证] | 快速增长，具体模式未知 |
| Simon Høiberg 产品矩阵 | $100K-150K/月 | 多产品线 + 个人品牌 + 5年积累 |

共同点：没有一条路径依赖付费广告起量

**当日强信号数 vs 噪音比**：3 条金矿级信号 / 本期中文 timeline 由 @lidangzzz 的中国政治与医疗评论主导（浏览量第一但与主题无关），英文 timeline 励志金句占比偏高（@blakeaburge/@thejustinwelsh/Codie Sanchez 等），实质商业信号密度属于正常水平

**本期信源**：@marclou @wickedguro @vista8 @Shpigford @SimonHoiberg @indie_maker_fox @xiaohu @tibo_maker @op7418 @agazdecki @lennysan @arvidkahl @Jayyanginspires（共 13 位）
