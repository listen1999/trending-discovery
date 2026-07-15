# AI 一人公司日报 | 2026-07-16

数据窗口：06:00 — 06:00（北京时间，2026-07-15 至 2026-07-16，过去 24 小时）
深度挖掘：3 条

---

## 今日头条

@gregisenberg 在推文里拆解了朋友 Corey Ganim 的"AI 处方医生"生意：45 分钟诊断收 $999，帮中小企业主找出该用哪些现成 AI 工具，约一半客户会追加订阅式陪跑服务，做到 $1,000/小时。经 web_search 交叉核实，Corey 本人此前自述该订阅业务"10 天做到 $8K MRR"。这条信号之所以重要，不在于工具或代码，而在于它证明"知道用哪些现成工具"本身就能定价——对既想入局又没有技术栈的档位 D（服务变现者）来说，这是目前信息密度最高的一条可复制路径，但复制的是方法论框架，不是价格数字。

---

## 今日金矿

> 本期共 3 条金矿：1 条 A 级收入信号 + 2 条 B 级工具/开源信号，均已完成 web_search / web_fetch 交叉核实。

### 金矿 1：Corey Ganim — $999 起步的"AI 处方医生"生意，自述 10 天做到 $8K MRR

来源：@gregisenberg（转述 @coreyganim 的方法论）· 2026-07-16 03:11 · 👍644 👁58,488 · 收藏1,368 · engagement_rate 2.34%（同期中位数约 0.15%-0.2%，属于"读者在存档使用"级别的强信号）

核心数据（部分已验证，部分为其本人自述）
- AI Concierge 订阅服务：$1,500-$2,000/月（约 ¥10,157-¥13,543，按 1 USD=6.7716 CNY，2026-07-15 汇率），每月两次 45 分钟策略通话 + Voxer 即时通讯支持，折合约 $1,000/小时（约 ¥6,772）。经 web_search 检索到 Corey Ganim 本人 2026 年发布的推文自述"该项目 10 天做到 $8K MRR"（约合 ¥54,173），该表述在其个人 X 账号及第三方文章（ryandoser.com、LinkedIn）中被多次引用，但具体数字仍属自述，未见第三方审计。
- 前置产品"AI 审计"：$999/次（约 ¥6,767）的一次性评估。据 LinkedIn 帖子及 ryandoser.com 报道，Corey 已为保险代理、房产经纪、理发学校老板、企业经纪、电商药房等做过评估。

商业模式拆解
- 漏斗结构：AI 审计（一次性 $999，获客入口）→ 约 50% 转化为 AI Concierge 订阅（$1,500-2,000/月，据其自述近 100% 成交率）。
- 收入公式：审计单价 × 潜在客户数 + 订阅单价 × 转化客户数 × 留存月数。
- 成本结构：几乎零边际成本（Opus 4.8 做辅助 + 创始人本人时间），核心成本就是创始人自己的时间，规模化天花板等于创始人个人能承受的客户数量上限（目前公开信息显示约 5 个订阅客户）。

复制路径
- 档位 D（服务变现者）：可参考"一次性诊断→订阅制陪跑"两段式漏斗设计自己的服务清单，但目前没有公开的中国同类服务定价基线，不建议直接把 $999/$1,500 换算成人民币价格照搬，需要通过实际报价自行测试。
- 档位 C（工具集成者/vibe coder）：审计交付物的本质是"找到企业里最耗时的 5-10 项重复流程，推荐现成 AI 工具组合"，国内可以把 Zapier/Make 换成扣子、Dify 等国内可直接访问的工作流工具作为交付方案。

竞争格局
- 这类"AI 审计/AI 礼宾"打法在英文创业圈已有多个跟随者和拆解文章（如 ryandoser.com 专门写文章复盘），信号正从早期阶段转向中期验证阶段，但尚未看到明显的国内对标产品或社群。

成本与时间预期：需进一步调研（无公开的国内同类定价基线可参考）。

[关键约束] 这条收入数据的核心支撑是 Corey Ganim 个人的销售能力和获客渠道（播客曝光、免费内容引流），不是某个可复制的软件或产品——复制"审计+订阅"框架，不等于复制他的获客渠道和个人信任背书，读者群体需要自己解决"谁会来找你做审计"这个更难的问题。

深度综述
Corey Ganim 是 YouTube 频道 Build With AI 的主理人，长期定位"非技术创业者如何用现成 AI 工具"，不是程序员出身，卖点恰恰是"我不写代码，我只负责诊断"——这和多数独立开发者靠写代码变现的叙事方向相反。反直觉的地方在于，多数人默认 AI 创业要做产品、要有技术护城河，而这条信号里 Corey 反复强调"工具已经存在，我只是知道用哪些"，本质上卖的是信息不对称和执行力，客户买的是省下自己研究工具的时间，而不是某个具体软件。风险与局限也很直接：这类生意高度依赖创始人本人的时间和信任背书，很难脱离创始人独立运作；中国市场的特殊障碍在于，中小企业主对"付费买咨询建议"的接受度、以及把业务流程数据交给外部人诊断的顾虑，都和欧美市场不同，加上没有公开的中国同类定价基线，直接套用美元定价换算既可能定高（相对本地消费力）也可能定低（相对咨询行业惯例），需要独立测试而非照搬。

---

### 金矿 2：Open Design — 开源版"Claude Design"，11 周做到 7.8 万+ GitHub Star

来源：@itsolelehmann（介绍/转发）· 2026-07-15 07:25 · 👍190 👁17,406 · 收藏335 · engagement_rate 1.92%（远高于同期中位数）

核心数据（已验证）
- 项目地址：github.com/nexu-io/open-design，官网 opendesigner.io。经 GitHub API 核实：截至 2026-07-15，star 数 78,582、fork 数 9,044，仓库创建于 2026-04-28（距推文发布约 11 周），与推文所述"78,000+ stars"基本吻合；第三方报道 augmentcode.com 中"8 周做到"的说法与仓库实际创建时间存在约 3 周误差，属于自媒体转述偏差，非仓库真实时间线。

商业模式拆解
- 完全免费，Apache-2.0 开源协议，采用自带模型/账号的方式（用户可用已有的 Claude Code、Codex、Cursor、Gemini CLI 等 20+ 编码 Agent 订阅额度驱动它），无需单独为 Claude Design 官方托管服务付费。
- 项目本身不直接产生收入，价值主张是帮用户省下官方托管设计工具的订阅成本，同时把设计流程、模板、Skill 都变成本地可编辑文件。

复制路径
- 档位 C（工具集成者/vibe coder）：如果已经在用 Claude Code/Cursor/Codex 做产品原型，可以直接把 Open Design 接入现有工作流，先用便宜模型出草稿方案、再切到强模型做细化，控制 token 成本。
- 档位 B（独立开发者）：可以用它快速产出落地页、后台 Dashboard、幻灯片等原型交付物，再自己或交给团队做代码实现，省掉前期设计沟通成本。

竞争格局
- 短短几周内已出现多个同类竞品（如 OpenCoworkAI/open-codesign、manalkaff/opendesign），说明这个赛道复制门槛很低，先发优势主要体现在生态和 Skill/设计系统积累（Open Design 号称 259+ Skill、142+ 设计系统），一人公司想进入的窗口期更多在"做出差异化设计系统模板"，而不是重新做一个同类壳子。

成本与时间预期：需进一步调研（开源项目本身免费，使用成本主要是使用者自己的 Agent 订阅/API 费用，无统一基线）。

[关键约束] 这条信号的关键支撑是"开源+社区"而非某个人的收入能力，78,582 星的增长速度说明的是"AI 编码 Agent + 设计工作流"这个方向的真实需求，而不是这个具体项目已经形成商业护城河——它随时可能被 Anthropic 官方功能更新，或被其中一个竞品反超。

深度综述
这是"开源社区绕开大厂订阅"这个趋势在设计工具领域的最新案例，此前类似模式已经在编码 Agent 领域反复出现，说明当大厂把某个能力包装成订阅制产品后，社区几乎必然在几周到几个月内做出一个本地优先、自带模型的版本，这条信号处于这个大趋势的中期验证阶段，不是孤立事件。反直觉的地方在于，一个刚创建 11 周的仓库能积累近 8 万 star、9 千 fork，增长速度远超多数运营多年的项目，说明当下开源社区对"设计类 Agent 工具"的需求被严重低估了——多数人以为设计是最后一道需要专业软件（如 Figma）才能跨过的关卡，这个项目证明只要把编码 Agent 的输出物（HTML/PDF/PPTX/MP4）当作设计交付物，很多设计需求可以直接被"本地 Agent + Skill"替代。对国内读者而言，最大的障碍不是访问 GitHub 的问题，而是驱动它所需要的编码 Agent 本身大多需要额外配置才能在国内环境跑通完整流程，技术门槛不适合非技术背景的档位 A、D 读者直接上手。

---

### 金矿 3：BaoCut — 宝玉用"App + CLI + Agent Skill"模式做的字幕转录翻译工具

来源：@dotey · 2026-07-15 14:37 / 2026-07-15 23:09 · 👍116 / 21 👁23,048 / 4,777 · 收藏171 / 36 · engagement_rate 0.74% / 0.75%（高于同期中位数）

核心数据（已验证）
- GitHub：github.com/jimliu/baocut。经 GitHub API 核实：105 star、8 fork，仓库创建于 2026-07-13（推文发布前 2 天），最近一次推送 2026-07-14，非常新。
- 官网 baocut.app：经 web_fetch 核实，App 完全免费、无付费层，仅支持 macOS 15+ Apple Silicon（不支持 Windows/Linux/Intel Mac），核心处理在本地设备完成，仅在用户主动开启时才调用云端模型。

商业模式拆解
- 目前完全免费，无直接变现动作，更像是宝玉个人内容矩阵的一部分（此前已有 baoyu-design、baoyu-skills 等同系列开源 Skill 项目），推测其价值在于用高质量开源工具持续积累技术影响力和粉丝信任，为后续知识付费/课程/咨询铺垫——此为推测，非官方证实。

复制路径
- 档位 A（内容创作者/搬运党、跨境电商）：BaoCut 面向的场景正是把海外演讲/视频转录、翻译、加字幕后搬运到国内平台，或跨境电商需要多语言字幕，可直接下载使用（仅限 Mac）。
- 档位 C（工具集成者/vibe coder）：更值得学习的是它的产品架构——把一个 GUI App 的核心能力封装成命令行 CLI，再包一层 Agent Skill 说明文档，让 Claude Code / Codex 这类 Agent 可以直接调用 CLI 完成任务，GUI 只负责人工预览和二次编辑。据宝玉本人描述，这个组合比纯 LLM API 方案（需自己配置 API Key、单次转写成本可达数美元）更省钱、更适合普通用户。

竞争格局
- 据宝玉本人在推文中的对比，同类"字幕/剪辑 Agent 化"产品目前有三种技术路线：ChatCut 给闭源编辑器外挂 MCP 插件、OpenCut 计划把 MCP 写进重写路线图、Palmier 原生支持 MCP，BaoCut 选择了更轻的"CLI + Agent Skill"路线，不依赖 MCP 协议，安装和调用门槛更低。

成本与时间预期：需进一步调研（项目本身免费，暂无官方明确的时间/预算基线）。

[关键约束] 这条信号目前规模很小（105 星、3 天历史），核心价值不是"BaoCut 这个产品能不能赚钱"，而是宝玉展示的完整一人开发流程——原型（baoyu-design Skill + Opus 4.8）→ 功能实现（Claude Code + Fable 5）→ 发布上线（Codex + Cloudflare 插件），产品本身能否变现仍是未知数。

深度综述
宝玉（@dotey）是拥有 23 万+粉丝的 AI 工程师和内容创作者，长期专注于向中文读者普及 AI 工程与软件工程实践，此前已发布过 baoyu-design（本地跑 Claude Design 替代方案）等多个开源 Skill 项目，属于"用开源项目做内容影响力"的典型代表，而非纯粹的独立开发者创业者。意外与反直觉之处在于，多数人做 AI 字幕工具会优先选"纯 LLM API"方案（整体翻译→句子配对→拆分），但宝玉实测后放弃了这条路——不只是因为拆分效果不理想，还因为要求普通用户自己配置 API Key 并不友好，且长视频用 Gemini 3.5 Flash 可能要几美元一条；最终选择"Agent + Skill + CLI + GUI"组合，本质是把"通用但脆弱的 LLM 直接调用"换成"Agent 调用工具 + 人工二次校对"，提示做工具类产品时技术上更先进的方案不一定是对普通用户更友好的方案。风险在于目前仅支持 macOS 15+ Apple Silicon，直接排除了 Windows 用户和跨境电商团队常见的非 Mac 办公环境，加上仓库只有 3 天历史，规模化和稳定性都有待观察。

---

## 快讯区

**收入信号**
- 独立开发者交易平台 TrustMRR 完成第 127 笔收购：一款"男性变帅（looksmaxxing）社群"App 以 $7.8K（约 ¥5.28 万）成交，过去 30 天流水 $607（约 ¥4,111），交易倍数 1.1x，从挂牌到成交历时 55 天 — @marclou · 据推文原文

**产品发布**
- AI 建站/低代码平台 Emergent 宣布完成 $130M（约 ¥8.80 亿）C 轮融资，估值 $1.5B（约 ¥101.57 亿），距其公开上线约一年；转述中提及"一名屋顶承包商老板用 Emergent 自建工具替代 5 个软件、每年省 $22K"的案例 [未经验证，无法核实具体身份及数字真实性] — @mukundjha（原发）/ 经 @itsolelehmann 转述
- Josh Pigford（Baremetrics 创始人）的 Amazon"过滤杂牌"浏览器插件 Knockoff.co 本周扩展到 Safari 桌面版和 iOS App，此前已被 Digital Trends、Fast Company、Gizmodo、Slashdot、TechPP 等多家外媒报道，核心的"帮你找美国替代品"功能 24 小时内被点击超过 1.3 万次；经 web_fetch 官方 FAQ 核实，插件完全免费、无付费层，目前未看到明确变现方式 — @Shpigford

**工具更新**
- Josh Pigford 同期发布付费 Claude Code 技能 /ship-check：上线前跑六道自动检查（清理调试代码、补全半成品、纠正 AI 味文案、review 潜在 bug 等），每道检查是独立 subagent，完整技能包仅向其付费社群 Founding Club 成员开放（经 web_fetch 官方页面核实） — @Shpigford
- Agent Skills for Context Engineering（经 GitHub API 核实：17,256 星、1,421 fork）新增 long-horizon-prompting 技能，用于给长时间跨会话运行的 Agent 写任务简报，参考了 OpenAI/Anthropic 关于长程 Agent 提示词设计的公开实践 — @muratcan
- 语音输入工具 HeyClicky 升级为"屏幕感知语音输入"，能读取当前屏幕内容并结合上下文生成回复（邮件、演示文稿融资材料等场景）[产品细节未经进一步核实] — @xiaohu
- OpenAI 官方"晒 GPT-5.6 推文送 $100（约 ¥677）额度"营销活动引发国内技术圈跟风参与，仅限 Go/Plus/Pro 订阅用户，限前 1 万名 — @xiaohu @akokoi1
- Codex 周活用户据 OpenAI 官方数据从 1M 增长到 8M 只用了约 5 个月，其中 6M→8M 仅用 3 天 — @tinyfool（转述 OpenAI Developers 数据）

**值得关注的观点**（已验证 solopreneur 判断）
- Nicolas Cole（@Nicolascole77，据公开报道内容变现累计 $6M ARR）总结文案原则：不要"卖"，要帮客户完成转变；说人话不说官话；做止痛药不做保健品；对着 1 个人说话而非"所有人"
- Dickie Bush（@dickiebush，经 web_search 核实其 Ship 30 for 30 等业务累计营收超 $10M）给出 2026 版写作生意路线图：X 日更 3 条推文 → LinkedIn 日更 1 篇 → 同步 Substack → 周报深挖爆款推文 → 3 个月后开始接 B2B 咨询变现 → 1000 订阅后再上数字产品/付费社群
- Jason Cohen（@asmartbear，WP Engine 创始人）建议：找那些正在公开抱怨竞品或抱怨你要解决的问题的人做客户开发，他们已经用行动证明自己在乎这件事

**教训与反思**
- 独立开发者 @runes_leo 实测"发现需求 → AI 做 MVP → 上线"全流程：选了红海赛道"证件照代做"，按公安部 GA461-2004 标准做完 MVP，闲鱼定价 9.9 元挂出，目前 0 成交、仅 1 人点击"想要"；他的结论是这条打法本身可以反复复用于验证下一个新想法，价值不在这一单生意赚不赚钱

**传播力素材**

- ["Building a $50/month pet drone that hunts mosquitoes by their wingbeat sound; 10 drones can clear a full square kilometer" 原发 @alextoussss，经 @itsolelehmann 转发] — @itsolelehmann · 👍8,595 👁1,344,967 · engagement_rate 0.17%
  改写方向：适合小红书/视频号科技猎奇选题——"造一个专杀蚊子的无人机"配合捕杀视频截图，标题可做成"这年头创业公司都在干什么"系列。
  点评：传播力来自"荒诞但真实"的反差感，容易引发"这也能是门生意"的猎奇转发；局限是它离"一人公司/AI 变现"主题较远，更多是猎奇谈资而非可复制的商业信号，改写时不宜延伸出"你也能做无人机生意"这类误导性结论。

- ["Only in Europe: this guy makes $400/day sending notifications when an AC is available to buy"] — @marclou · 👍1,942 👁271,620 · engagement_rate 0.30%
  改写方向：适合公众号"冷门副业"系列——把"库存/补货监控+推送提醒"这类轻量套利型小生意结构化成一篇"信息差如何变现"的选题，配合国内类似案例（如演唱会/紧俏商品补货提醒）。
  点评："监控页面变化+自动通知"是低代码自动化的经典范式，容易复制的是技术实现，难的是找到供给稀缺、需求焦虑的细分场景；推文本身未提供产品名和创始人身份，$400/day 的数字来自转发者转述，无法核实来源，不应当作确定性数据使用。

- ["Every marketing team should do this simple test: ask 100 existing customers to describe your product in their own words, no leading the witness"] — @jasonfried · 👍65 👁5,916 · engagement_rate 0.85%
  改写方向：适合公众号"产品/营销方法论"选题——包装成"3 步自测产品定位是否清晰"的实操清单，配合"你以为的卖点 vs 客户嘴里的卖点"对比图。
  点评：Jason Fried（Basecamp 联合创始人）这条建议具体、可执行、门槛低（不需要预算，只需要发消息问 100 个客户），局限在于对早期没有 100 个客户的独立开发者/内容创作者不完全适用，需要改造成"问现有 10-20 个种子用户"的小样本版本。

---

## 延伸资源库

### 播客 / 视频 / 访谈
- Build With AI 播客（@startupideaspod）—— Corey Ganim 分享 AI Concierge/AI 审计完整方法论，1 小时完整课程，YouTube 链接：youtube.com/watch?v=dhbcVxYhWaQ

### 图书 / 课程
本期无

### 链接汇总（已 web_fetch / web_search 验证）
工具类：
- Open Design：opendesigner.io ｜ github.com/nexu-io/open-design
- BaoCut：baocut.app ｜ github.com/jimliu/baocut
- ship-check：initialcommit.co/library/skills/ship-check
- Knockoff：knockoff.co/faq
- Agent Skills for Context Engineering：github.com/muratcankoylan/Agent-Skills-for-Context-Engineering

报道类：
- Corey Ganim AI 审计业务拆解：ryandoser.com/ai-audit-business/
- Corey Ganim 个人博客《How I'm making $1,000/hour as an AI Concierge》：corey-ganim.kit.com
- Knockoff 相关外媒报道：Digital Trends、Fast Company、Gizmodo、Slashdot、TechPP、Family Handyman

GitHub：
- jimliu/baocut（105★ / 8 fork，2026-07-13 创建）
- nexu-io/open-design（78,582★ / 9,044 fork，2026-04-28 创建）
- muratcankoylan/Agent-Skills-for-Context-Engineering（17,256★ / 1,421 fork）

---

## 行动建议

档位 A（内容创作者）
- 本周找一条准备搬运的海外视频，用 BaoCut（仅限 Mac）跑一遍转录+翻译+字幕流程，和现在用的自动字幕工具做效果对比。

档位 B（独立开发者）
- 参考 BaoCut"GUI 核心能力封装成 CLI，再包一层 Agent Skill"的架构，评估能否把自己现有产品的某个功能改造成可被 Claude Code/Codex 直接调用的 Skill。

档位 C（工具集成者/vibe coder）
- 今天用 Open Design 接入自己已有的编码 Agent 订阅跑一次完整原型，对比它和官方付费设计工具在效果和 token 消耗上的差异。

档位 D（服务变现者）
- 参考 Corey Ganim 的"一次性诊断→订阅制陪跑"两段式漏斗结构，本周给 1 个熟人客户免费做一次 45 分钟业务流程诊断练手，暂不设定价格，先验证诊断本身的交付质量。

---

## 避坑指南

- 红海创意不等于失败信号：@runes_leo 的证件照 MVP 零成交，但完整跑通了"筛需求→做 MVP→上线"的流程，这套流程本身比这一单生意值钱——容易把"这单没赚到钱"等同于"这次尝试失败了"，其实该看的是流程是否可复用。
- 病毒式关注度不等于商业模式：Knockoff.co 拿到多家外媒报道、单个功能 24 小时被点击超 1.3 万次，但产品完全免费、无付费层，暂时看不出清晰的变现路径——热度和收入是两回事，不应把"上了热搜/被科技媒体报道"直接等同于"这是个赚钱生意"。

---

## 本期情报评估

**信息密度**：正常。今日没有出现颠覆性大新闻，但有 1 条经多方交叉验证的收入型信号（Corey Ganim）、2 条经 GitHub API 核实的开源工具信号（Open Design、BaoCut），整体质量高于纯内容农场式的一天。

**趋势信号**：
本期同时出现"服务化变现"（Corey Ganim 用 45 分钟诊断收费 + 订阅制陪跑）和"开源抄近道"（Open Design 用社区力量绕开官方订阅设计工具）两条路径，说明在"用现成 AI 工具而非自己造轮子"这件事上，卖时间的服务型玩家和做工具的产品型玩家，都在往降低对单一大厂订阅的依赖这个方向走。

**横向对比**：
服务型（Corey Ganim，靠个人信任背书，天花板是创始人精力）vs 工具型（BaoCut，靠开源积累影响力，暂无变现）vs 平台型（Emergent，靠融资和用户规模，$130M C 轮）——三种规模完全不同的起步路径，服务型启动成本最低但最难摆脱创始人本人，平台型启动成本最高但增长曲线最陡。

**当日强信号数 vs 噪音比**：
约 4 条 A/B 级强信号，对比当日 360 条推文总量（含大量励志金句、加密货币行情、生活分享等），噪音占比很高，属于正常的日常 timeline 构成，不属于信号枯竭或刷屏事件。

**本期信源**：@gregisenberg @coreyganim @itsolelehmann @dotey @Shpigford @marclou @mukundjha @muratcan @xiaohu @tinyfool @Nicolascole77 @dickiebush @asmartbear @jasonfried @runes_leo @akokoi1（共 15 位）
