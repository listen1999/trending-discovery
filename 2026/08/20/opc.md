# AI 一人公司日报 | 2026-08-20

数据窗口：06:00 — 06:00（次日，北京时间，过去24小时）
深度挖掘：3 条

---

## 今日头条

过去24小时里，Agent Harness 这一层的开源化速度肉眼可见：Apache 软件基金会正式接纳了第一个 Agent Harness 项目 Maka 进入孵化器，同一时间窗口内，DeepSeek Harness（dsh）的插件生态今天又新增177个插件（据 @vista8），独立开发者 @indie_maker_fox 也基于 Pi Agent 的开源特性做出了自己的 agent 开发框架 mkagent。三条线索指向同一件事：造 agent 产品不再需要依附某一家模型厂商的私有 CLI，个人开发者拿开源 harness 直接二次开发、包装成垂直行业产品的技术门槛正在快速下降。这条线索与金矿区的 Maka 案例互为印证。

---

## 今日金矿

### 金矿 1：TrustMRR — 独立开发者产品的退出流动性正在被标准化

来源：@marclou（Marc Lou，已知高收入 solopreneur，见附录名单）· 2026-08-19 20:47 · ~9h ago · 👍185 👁14,655
关联来源：@trust_mrr（TrustMRR 官方账号，经 @marclou 于 2026-08-19 11:57 转发，~18h ago）· 👍227（转发帖）

**核心数据（已验证 / 据推文原文）**
- TrustMRR 上线8个月，累计完成150笔收购（据推文原文，@trust_mrr 8月19日公告，经 @marclou 转发）
- 今日案例（#150）：一款图片生成类 SaaS 以 $5,000（约 ¥33,700，按 1 USD≈6.74 CNY，2026年8月19日汇率）售出，过去30天营收 $423（约 ¥2,851），成交倍数 1.0x，从上架到成交耗时35天（据 @trust_mrr 原文）
- 历史最大单笔成交：$85,000（约 ¥572,900），发生在平台上线45天时（2026年1月14日，买家 @fattbabakay，经 web_search 交叉验证，来源见下）
- 平台数据：挂牌总值超 $12 亿（约 ¥80.9 亿）；月访问量约20万；报价合理的项目平均48小时内收到3个报价；平均成交周期23天（经官网 trustmrr.com web_fetch 验证）
- engagement_rate：原帖 0.18%，处于同期中位数（0.15%-0.20%）区间，信号强度并非来自病毒式传播，而是来自数据本身的可核实性与信源可信度

**商业模式拆解**
- TrustMRR 本身也是 marclou 的一人产品，用他自己的 ShipFast 模板搭建，2025年底开始收费，变现方式是「escrow 托管费 + 3% 成交中介费」，marclou 本人即是撮合经纪人（经 web_search 验证）
- 收入公式：中介费 = 成交总额 × 3%，随平台交易量线性增长；此外还有站内广告位收入（20个广告位常年满位，经 web_search 的历史推文验证）
- 平台的核心卖点是「信任」——所有挂牌收入均通过 Stripe / RevenueCat / Superwall 等第三方支付数据验证，直接回应了微小 SaaS 收购市场里买家最大的顾虑（卖家自称收入无法核实）

**复制路径（只写真正适用的档位）**
- 档位 B（独立开发者）：TrustMRR 证明了微小 SaaS 存在真实的退出流动性——月流水 $423 的产品也能以约1倍年化流水的价格卖掉套现，这为「做完就卖、不必陪产品终老」提供了一个可参照的退出坐标系。
- 档位 C（工具集成者 / vibe coder）：平台型一人公司的样本——用现成的 SaaS 模板（如 ShipFast 类脚手架）搭建垂直细分的撮合市场，靠中介费/广告位变现，而不是自己做被撮合的那一方。
- 国内可行性：直接复制该平台模式在中国市场存在两道现实门槛——一是缺少 Stripe/RevenueCat 级别的、可被第三方核验的收款数据基础设施（国内主流收款渠道尚无对标的公开验证接口）；二是跨境资产/股权转让涉及外汇与合规问题 [此判断基于现有支付生态观察，未经法律专业验证，需要进一步调研]。

**竞争格局**
- 海外同类平台有 Acquire.com（原 MicroAcquire）、Flippa，体量均大于 TrustMRR，但 TrustMRR 的差异化窄而深：只收录经第三方支付数据验证的项目，且创始人自带 indie hacker 圈层分发能力（37万+粉丝、长期 build in public）。国内暂无对标产品，闲鱼等二手交易平台不覆盖已验证收入的 SaaS 资产交易场景。

**成本与时间预期**
- 平台没有披露启动成本，marclou 是在已有多款产品和流量基础上孵化的 TrustMRR，冷启动依赖既有粉丝盘，不具备可直接套用的预算基线，标注「需要进一步调研」。

**深度综述**

marclou 的打法值得单独说一句：他从不是靠单一爆款产品说话，而是把「快速验证 + 边车产品互相导流」做成了体系——ShipFast（SaaS 脚手架）、DataFast（分析工具）等产品线互相导流，TrustMRR 是这条产品线最新的一环，本质是把他长期输出的「公开构建」人设和分发能力，转化成了撮合平台的冷启动流量。这也是这类平台很难被简单复制的原因：护城河不是技术，是创始人本身的关注度。从趋势位置看，这条信号处于「验证期」而非「早期」——marketplace 已经跑了8个月、150笔交易，规则、托管、经纪费模式都已经跑通，读者能学到的不是「抄一个类似平台」，而是「退出流动性确实存在」这个事实本身，可以纳入自己产品的长期规划。最反直觉的地方是今天的具体成交：一款月流水仅 $423 的图片生成 SaaS，只卖出了1倍年化流水（$5,000），与2026年初那笔 $85,000 的标杆交易相差17倍——说明媒体愿意转发的「大额退出」只是分布的尾部，多数微小 SaaS 的真实退出价格朴素得多，退出的意义更多是「停止维护、拿回时间成本」而非「暴富」。对国内读者而言，最大的障碍不是技术，是基础设施缺位：TrustMRR 的信任机制建立在 Stripe/RevenueCat 收入验证之上，国内独立开发者大多依赖微信支付/支付宝收款，缺少同等程度的第三方可验证收入凭证，直接照搬平台模式在信任建立这一端会先卡住。

Sources：
- [Marc Lou on X: "TrustMRR is now monetized"](https://x.com/marclou/status/2011723035800453526)
- [Marc Lou on X: "✅ SOLD FOR $85,000"](https://x.com/marclou/status/2016892441237082209)
- [TrustMRR - Buy and Sell SaaS Startups](https://trustmrr.com/)

---

### 金矿 2：canivibecodeit — 给「这个订阅该不该自己写」做了一个可检索的判断库

来源：@indie_maker_fox（转发分享，独立开发者，产品出海2年收入破10万美元，见 bio）· 2026-08-19 15:50 · ~14h ago · 👍89 👁9,387 🔖132 · engagement_rate 1.41%（远高于同期中位数0.15%-0.20%，属于 Top 5% 极高档，绝对浏览量不大，属于「小众但精准」的信号）

国内可用：需要工具（该站点为 Astro 静态站，未在国内主要云厂商备案，实际访问速度和稳定性以现场结果为准，判断为需科学上网访问 [基于同类独立开发者出海项目的一般访问经验，未逐一实测]）

**核心功能（聚焦对一人公司的价值）**
- 收录976款付费 SaaS（74个分类，经 GitHub 仓库 web_fetch 验证），对每一款给出判断：YES（可一次性 vibe code 复刻）/ KINDA（需要一个周末）/ NOT REALLY（有真正护城河）
- 每个条目配一份可直接粘贴进 Claude Code / Cursor / Codex 的 prompt
- 社区可标记「I replaced it」为已复刻项目投票，数据完全开源、社区共建

**定价**
- 免费层：整站免费使用，无付费墙（据 indie_maker_fox 原文与站点结构）
- 付费层：无面向用户的付费层；官方变现方式是出售站内广告位（据 indie_maker_fox 原文）

**10分钟上手**
1. 打开 canivibecodeit.com，搜索想复刻或正在犹豫要不要退订的 SaaS 名字
2. 查看社区 verdict（YES / KINDA / NOT REALLY）
3. 复制配套 prompt，粘贴进 Claude Code / Cursor / Codex 执行
4. 复刻成功后回站点标记「I replaced it」

**与现有工具链配合**
可作为独立开发者选题的前置筛选器：先查目标方向是否已经有 NOT REALLY 的判断（说明存在真正壁垒，值得深入而非浅尝辄止）；也可反向用于练手项目或内部工具选型，避免重复造轮子。

**踩坑预警**
verdict 是社区众包判断，主观性强，不能替代真实竞品分析；「能被一次性 vibe code 出来」不等于「能做成生意」，工具只回答技术可行性，不回答商业可行性。

**竞品对比**
定位接近 openalternatives.co（开源软件平替目录），差异在于 canivibecodeit 更进一步提供了可直接执行的 AI coding prompt，而非只列替代品名单。

**官方链接**
- https://canivibecodeit.com
- GitHub：https://github.com/canivibecodeit/canivibecodeit（261 stars，MIT 协议，经 web_fetch 验证）

**深度综述**

这个工具值得关注不是因为技术新颖（Astro + SQLite 的静态站，一个周末就能搭出来），而是它精准踩中了 vibe coding 时代的一个新焦虑：AI 编程能力越来越强之后，「这个订阅要不要退掉、自己写一个」变成了很多人会真实想到的问题，但一直缺一个系统性的判断框架。它把这个模糊的直觉变成了一个可检索的数据库，976个应用、74个分类，每条都给 verdict 配上可执行的 prompt——这比单纯罗列「开源平替」的老牌网站（如 openalternatives）更进一步，把「能不能做」和「具体怎么做」打包在了一起。反直觉的地方在于，这类工具的存在本身反过来提示了一个问题：如果一个 SaaS 的护城河能被一份公开 prompt 轻易复刻，它原本的商业模式可能就没有想象中稳固——页面上大量「YES 可以 vibe code」的判断，某种程度上是在给功能单一、定价 $10-20/月的效率工具类订阅产品提前打预警。对独立开发者和 vibe coder 而言，更现实的用法是反过来查：自己想做的方向有没有已经被标成 NOT REALLY，如果有，说明可能存在更深的技术或数据壁垒，值得深入；如果一片都是 YES，说明这个赛道已经是红海中的红海，光「能做出来」赚不到钱，护城河得从分发、品牌或服务里找。开源、社区共建的冷启动打法也值得留意：作者本人不需要维护数据准确性，976个条目基本靠贡献者提交 PR 完成，这是低成本启动信息类产品的经典打法。

Sources：
- [GitHub - canivibecodeit/canivibecodeit](https://github.com/canivibecodeit/canivibecodeit)
- [Can I Vibecode It: 950+ SaaS apps you can replace with a prompt](https://lucadidomenico.studio/en/blog/can-i-vibecode-it-replace-saas-prompt)

---

### 金矿 3：Apache Maka — Agent Harness 层第一次有了「厂商中立」的开源选项

来源：@dotey（宝玉，AI领域中文 KOL，24万+粉丝）转发官方公告 · 2026-08-20 01:14 · ~5h ago · 👍165 👁12,290 🔖104 · engagement_rate 0.85%（高于同期中位数，属于 Top15% 高互动区间）

国内可用：直接访问（GitHub 仓库，需科学上网访问 GitHub 本身，但项目无额外地域限制；本地部署运行不依赖境外服务）

**核心功能（聚焦对一人公司的价值）**
Maka 是一个「本地优先」的 Agent 工作区/Harness，将模型消息、工具调用、工具结果、终止信号统一记录进本地 Runtime Event Log，会话与记录默认本地保存。今天的信号是：Apache 软件基金会正式接纳 Maka 成为孵化器项目，是 ASF 迎来的第一个 Agent Harness 类项目（据 @dotey 转发的官方公告）。

**已验证数据**
- 据推文原文（@dotey，引用的是仓库2026年5月27日创建到7月底、约10周的窗口数据）：71万行 TypeScript（其中35万行为测试代码，949个测试文件）、2,439次提交、1,218个已合并 PR、合并率93.8%、PR合并耗时中位数33.5分钟
- 经 web_fetch 独立核查 GitHub 页面（核查时间晚于上述窗口）：1.4k stars、3,593次提交、179个 fork、116个开放 issue、100个开放 PR，Apache License 2.0（与推文原文的时间窗口不同，数字更大属于正常增长，并非矛盾）

**10分钟参与方式**
1. 访问 github.com/maka-agent/maka-agent 了解项目结构
2. 阅读 README 的架构文档（8章节索引）
3. 认领一个 good first issue 或直接提 PR

**与现有工具链配合**
和当前市面上厂商私有 CLI（Claude Code、Codex 各自的官方 harness）形成对照：Maka 走完全开源、Apache 中立治理路线，不绑定任何一家模型厂商，适合想要「一套 harness 配置多套模型」而不想被单一厂商生态锁死的开发者。

**踩坑预警**
这一层目前变化速度极快——同期 DeepSeek 开源的 dsh（MIT协议）在4天内冲到13万+星标，创下同类项目最快纪录（经 web_search 验证）。过早绑定某一个 harness 框架，可能很快就要面对生态迁移成本。

**竞品对比**
dsh（DeepSeek Harness，MIT协议，由 DeepSeek 主导，插件生态爆发式增长）与 Maka（Apache 2.0，社区中立治理）代表了开源 harness 层的两条路线——前者靠单一厂商的模型热度驱动生态，后者靠基金会中立性换开发者长期信任。

**官方链接**
- https://github.com/maka-agent/maka-agent

**深度综述**

这条信号真正的重量不在 Maka 这一个项目本身，而在于它是「Harness 层开源化」这个更大趋势里第一个被 Apache 基金会正式接纳孵化的项目。今年这一层出现了戏剧性分化：DeepSeek 8月中旬开源 dsh，四天冲到13万+星标；同时 Pi Agent、Claude Code、Codex 等厂商仍把 harness 当作自己 CLI 的私有资产。Maka 选择了另一条路——完全开源、不依附任何一家模型厂，用 Apache 基金会的中立治理换取开发者信任，这是它与 dsh（MIT协议但由 DeepSeek 主导）的核心差异。意外之处在于捐赠孵化后仓库反而更活跃：dotey 引用的是仓库5月27日创建到7月底、10周窗口的数据，而今天独立核查 GitHub 页面，仓库已涨到3,593次提交、179个 fork、100个开放 PR，说明进入孵化流程并没有拖慢开发节奏，反而吸引了更多外部贡献者。对国内独立开发者和 vibe coder 而言，这一层的开源化直接决定了自己造 agent 产品的门槛：@indie_maker_fox 在同一时间窗口分享的自研框架 mkagent，就是直接基于 Pi Agent 开源特性二次开发的产物——如果 harness 层继续保持中立开源，未来在这层之上做垂直行业 agent 产品（如客服、法律文书、电商选品）的个人开发者会越来越多，窗口期正在缩短而不是拉长。

Sources：
- [GitHub - maka-agent/maka-agent](https://github.com/maka-agent/maka-agent)
- [DeepSeek Harness: Why 95,000 GitHub Stars in 2 Days Matters](https://flowtivity.ai/blog/deepseek-harness-open-source-agent-explained/)

---

## 快讯区

**收入信号**
- 除金矿1 TrustMRR 外，本期无其他标注具体金额的收入披露信号。

**产品发布**
- Ramp 旗下 Router.com 今日正式向所有开发者开放：单一 API/更换 base URL 即可路由到 OpenAI、Anthropic 等及 DeepSeek、Qwen、GLM 等开源模型，早期用户平均降低40%推理成本，2026年内免费使用 — @packyM 转发 · ~1h ago（经 web_search 核实为 Ramp 官方8月19日发布，非独立开发者项目；国内可用性未经验证，涉及连接海外多家模型厂商 API，实际连通性存疑 [需要进一步调研]）
- @dhh 的个人 Linux 发行版 Omarchy 成立了「Core Team」核心团队（含6名成员），并启动首届插件竞赛，奖金 $4,000（约 ¥26,960），即日起至周一9点CEST — ~9h ago / ~6h ago
- OpenRouter 被 Stripe 以约 $8B+ 收购的消息持续发酵，与 Cursor 近期约 $60B 的收购一起被多个账号并列讨论（@aaditsh @rrhoover 等）— ~3h ago（具体收购金额来自媒体报道与"泄露"投资人信函截图，未经 Stripe/OpenRouter 官方确认最终数字，标注 [未经验证]）

**工具更新**
- @indie_maker_fox（已验证独立开发者，产品出海2年收入破10万美元）本期连续分享多个工具：Blume（Mintlify 开源平替文档框架）、Rebased（JetBrains 系 Git 客户端）、backlink_skills（自动化外链提交 skill）、deepseek-harness-desktop（dsh 桌面客户端）— 均为开源项目，链接见延伸资源库
- @gregisenberg 分享团队 AI 技能管理方法论：把最佳 Claude/Codex skills 放进 GitHub 仓库、打包成插件、团队安装并开启自动更新，可实现版本控制、技能共享和团队沉淀，方法来自其播客嘉宾 @aiwithremy — ~1h ago（方法论本身未经第三方复现验证）
- @heyblake（定位于 SaaS 定位/转化咨询）分享5步竞品定位审计法：读对手首页H1和副标题→看定价页套餐命名→看客户证言里反复出现的问题→搜"[对手] vs"看真实竞品集→查对手招聘岗位判断增长打法 — ~1h ago，engagement_rate 1.85%（本期最高，但绝对浏览量仅2,756，小众精准信号）
- @evilcos（慢雾科技创始人）披露个人 agent 部署架构：Telegram + 云上部署的 Hermes Agent + 主流大模型配置 + 针对性 harness 沉淀，配置多套以避免单点故障、实现任务隔离 — ~10h ago
- @evilcos（慢雾科技）安全提醒：VSCode 插件市场的 Solidity Pro 曾被发现在历史版本中植入凭证窃取与远程代码执行能力，且当前版本"洗白"后不易被检测，提醒 Web3 开发者对插件历史版本保持警惕，不能只看当前版本是否干净 — ~10h ago

**值得关注的观点**
- Jason Cohen（WP Engine 创始人，两次退出、参与打造两家独角兽，经 web_search 验证）："不性感的市场里往往藏着真钱，因为大机构 VC 不会进场、老玩家也懒得创新，代价可能是客户高度 zero-sum、锁定成本极高" — @asmartbear · ~9h ago
- @yongfook（Bannerbear 创始人，Bootstrapping SaaS @ $81K MRR，经 web_search 验证其 2025年9月已达 $1M ARR）提出待讨论的问题：营销官网上关于 MCP、聊天插件等"AI"能力信息该放在导航的哪个位置——放进 Integrations、Developers，还是每个产品站都需要一个一级"AI Agents"导航项 — ~14h ago

**教训与反思**
- @indie_maker_fox 把刚启动一天的新项目按下暂停："回头一想大概率又是个自嗨项目，哪怕成本不高也挺耗时间，与其继续消磨不如及时止损"，转而把接下来几周投入到吃透 agent 开发、打磨可复用技能库上 — ~18h ago

**传播力素材**
- [The next $1T company will be an AI-native services firm. But it must begin in a vertical with these traits: 1) Document-driven 2) Rules-bound 3) Verifiable] — @chrishlad · 👍427 👁35,880 · engagement_rate 0.95%
  改写方向：适合公众号/知识星球选题——把"文档驱动、规则约束、可验证"这三个筛选标准拆成一张自查表，帮读者判断自己所在行业/业务环节是否属于"最先被 AI 服务化"的类型。
  点评：这条判断的价值在于给出了三个具体可操作的筛选维度，而不是空喊"AI 将改变一切"，因此有一定独创性；局限在于它是一个未经数据验证的预测性判断（作者是 hanoverpark 联合创始人/CEO，非已知高收入 solopreneur 名单成员），"$1T 公司"这个数字本身更像修辞而非可核实预测，读者应把它当作行业筛选框架来用，而非当作确定性预言。

---

## 延伸资源库

### 播客 / 视频 / 访谈
- Rogue Startups EP352《Hidden Multipliers with Jason Cohen》— 嘉宾 Jason Cohen（WP Engine 创始人）与主持人 @thecraighewitt 谈 SaaS 创始人该如何看待 AI 在产品中的角色，来源 @asmartbear 转发（~2h ago）。经 web_search 定位到节目详情页，但未能进一步 fetch 到具体时间戳与章节内容 [时间戳未获取]。
  链接：https://roguestartups.com/episodes/rs352-hidden-multipliers-with-jason-cohen

### 图书 / 课程
本期无。

### 链接汇总（已 web_fetch / web_search 验证）
- 工具类：[canivibecodeit.com](https://canivibecodeit.com) · [Router.com](https://router.com) · [TrustMRR](https://trustmrr.com)
- GitHub类：[maka-agent/maka-agent](https://github.com/maka-agent/maka-agent)（1.4k stars）· [canivibecodeit/canivibecodeit](https://github.com/canivibecodeit/canivibecodeit)（261 stars）· [DetachHead/rebased](https://github.com/DetachHead/rebased) · [flaqai/backlink_skills](https://github.com/flaqai/backlink_skills) · [useblume.dev](https://useblume.dev)
- 报道类：[Reddit citations are dropping in ChatGPT](https://promptwatch.com/data/reddit-citations-are-dropping-in-chatgpt) — 据 promptwatch.com 监测数据，Reddit 在 ChatGPT 引用中的占比从约3.8%降至0.52%（8月14-17日均值），一周内跌幅约86%，同期 Google 系平台仅缓慢下降（经 web_fetch 验证，@levelsio @Shpigford 分别转发，~8h ago）。对依赖 Reddit 铺内容做 AI 答案引擎优化（GEO/AEO）的内容创作者（档位A）是一个值得关注的渠道风险信号。
- 播客类：见上「播客/视频/访谈」

---

## 行动建议（按档位分组）

档位 B（独立开发者）
- 本周花30分钟浏览 TrustMRR 的历史成交记录页，看看自己所在赛道有没有同类产品的成交价参照，建立一个"如果不想做了，值多少钱"的心理坐标，而不是只有"死磕到底"一个选项。

档位 C（工具集成者 / vibe coder）
- 今天花30分钟打开 canivibecodeit.com，搜索自己正在考虑复刻的3-5款订阅工具，查看社区 verdict 是 YES/KINDA 还是 NOT REALLY，避免把时间投入到已被公开验证"能一次性 vibe code 出来"、因而红海化的方向。
- 本周留意 DeepSeek Harness（dsh）和 Apache Maka 这类开源 harness 的插件生态，评估是否要把现有 AI 工作流迁移到不绑定单一模型厂商的开源 harness 上，降低未来生态迁移成本。

---

## 避坑指南

- 自嗨项目陷阱：@indie_maker_fox 在新项目启动仅一天后就主动暂停，判断依据是"哪怕成本不高也挺耗时间"——没有外部验证（用户/订单/流量）支撑的新项目，及时止损比死磕更划算，这条经验来自一位过去2年海外产品收入破10万美元的独立开发者。
- 退出金额的幸存者偏差：TrustMRR 上被转发报道的往往是 $85,000 这类标杆成交，但今天平台真实撮合的一笔是 $5,000（1倍年化流水）——参考"退出案例"时应关注中位数而非头条案例，避免对自己产品的估值产生不切实际的预期。

---

## 本期情报评估

**信息密度**：正常。本期314条推文、78个活跃账号，没有单一事件刷屏，信号分散在几个平行主题（Agent Harness 开源化、TrustMRR 退出市场、AI 一人公司方法论）中，属于正常工作日密度。

**趋势信号**：Agent Harness 这一层正从厂商私有 CLI 快速转向开源、插件化的基础设施；同时以 TrustMRR 为代表的微小 SaaS 二级交易市场，正在把"退出"变成一件有价格参照系的常规操作。两条线都在降低个人开发者做产品、做完再退出的门槛。

**横向对比**：TrustMRR 一天内出现的两个参照点——历史标杆 $85,000（1月，上线45天成交）vs 今天的 $5,000（1.0倍流水，上架35天成交）——相差17倍，提示"退出"的真实分布是重尾的，多数案例更接近后者而非头条案例。

**当日强信号数 vs 噪音比**：314条推文中，进入 A/B 级候选池并最终写入报告的信号约10条（TrustMRR、canivibecodeit、Apache Maka、Router.com、gregisenberg方法论、heyblake方法论、Jason Cohen判断、yongfook观点、evilcos架构分享与安全提醒、indie_maker_fox反思），其余多为个人生活分享、通用励志句式、以及无新数据的旧素材转发（如 @dickiebush 本期最高收藏量的推文即为空洞的自我转发，未计入分析）。噪音占比明显更高，属于典型工作日的信号密度。

**本期信源**：@marclou @trust_mrr @indie_maker_fox @dotey @gregisenberg @asmartbear @dhh @packyM @yongfook @evilcos @chrishlad @heyblake @vista8 @oran_ge @levelsio @aaditsh @rrhoover（共17位）
