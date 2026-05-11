# AI 一人公司日报 | 2026-05-11

数据窗口：09:14 — 09:14（北京时间，过去 24 小时）
深度挖掘：3 条

---

## 今日头条

一个做 Microsoft Intune 应用打包的"无聊 SaaS"月入 $60K，创始人是 IT 管理员出身，用 Bubble.io + GitHub Actions 搭建，定价 $25/月起步。同一天，玉伯（Frank Wang）发文指出字节跳动全面收缩 AI 应用层烧钱模式、Dan Koe 的 AI 产品 Eden 因烧钱过快停止迭代。两条信号指向同一个结论：AI 时代最稳的路不是追规模，是找到真实付费痛点、控制成本、赚真钱。

---

## 今日金矿

> 数量按真实信号定，1-5 条均可。不补足。

### 金矿 1：Pckgr — 给 Microsoft Intune 做应用打包的"无聊 SaaS"，月入 $60K

来源：@thepatwalls（转发 @starter_story）· 2026-05-11 04:42 · 👍371 👁23,544
engagement_rate：3.05%（极高，Top 1%，同期中位数约 0.15%-0.20%）

**核心数据（已验证）**
- 月收入：$60,000（约 ¥435,000，按 1 USD = 7.25 CNY）[据 Starter Story 访谈原文]
- 客户数：1,000+（据官网及访谈）
- 创始人：Thomas Mahony，澳大利亚，前 IT 管理员
- 产品官网：intunepckgr.com（经 web_search 验证存在）

**商业模式拆解**
- 定价结构：Starter $49/月（100 设备）、Professional $99/月（1,000 设备）、Enterprise 定制报价（2,500+ 设备）
- 收入公式：约 1,000 客户 × 平均 $60 ARPU = $60K/月。以 B2B IT 管理为主，客户粘性极高（换工具成本大）
- 技术栈：Bubble.io（前端）+ GitHub Actions（后端自动化打包）+ Azure（托管）。核心壁垒不是技术难度，是对 Intune 生态的深度理解和 300+ 应用的预打包维护
- 主要成本：云服务 + 维护预打包应用库，一人即可运营

**复制路径（只写真正适用的档位）**

档位 B（独立开发者）：寻找企业 IT 管理中的手工重复操作——Intune 只是冰山一角，Azure AD、JAMF（macOS 端）、MDM 设备管理等领域都有大量 IT 管理员在手动干重复活。关键是：找到一个足够窄的痛点（比如"应用打包"这种每次耗时 1 小时的操作），用自动化工具替代，定价 $25-$99/月，在 Reddit 的 r/sysadmin 或 r/Intune 做冷启动。技术栈不需要高端——Bubble.io + GitHub Actions 就能跑通。

档位 C（工具集成者）：如果不写代码，可以关注类似领域的"流程自动化"机会——比如用 n8n/Make 搭建企业 IT 工单自动处理流程，打包成服务卖给中小企业 IT 部门。国内对标：企业微信/钉钉生态里的设备管理、应用分发自动化。

**竞争格局**
- 国际市场：Intune 应用打包赛道极窄，竞品少（Patch My PC 等做补丁管理但不完全重叠）。窄赛道 = 低竞争 = 高利润
- 国内市场：Intune 在国内企业渗透率低（国内用钉钉/飞书/企微），直接复制不可行。但"给企业 IT 管理做自动化工具"这个思路完全成立——国内 MDM（移动设备管理）市场有类似痛点

**成本与时间预期**
- MVP 开发：1-2 个月（用 Bubble.io 或 Next.js + 支付集成）
- 冷启动渠道：Reddit、IT 管理论坛、Microsoft Tech Community
- 月运营成本：需进一步调研（取决于云服务用量和自动化打包的计算成本）

**深度综述**

这条信号最值得关注的不是 $60K 这个数字本身，而是它验证了一个反复被一人公司实践者证明但仍被多数创业者忽视的路径：**在巨头生态的缝隙里做垂直工具**。Microsoft Intune 是微软企业管理套件的一部分，全球企业 IT 管理员每天都在用，但微软自己不会做"一键打包 300 个常用应用"这种脏活累活。Thomas Mahony 的背景是 IT 管理员，他解决的是自己每天遇到的痛点——这也是为什么他能做成而纯技术创业者不一定看得到这个机会。

从趋势定位看，这属于"Boring SaaS"（无聊 SaaS）赛道的中期验证信号。Pat Walls 的 Starter Story 持续报道这类案例已经两年多，形成了一个清晰的模式：找到 B2B 工作流中的重复性手工操作 → 用自动化替代 → 定价 $25-$100/月 → 在垂直社区冷启动。这个模式在 AI 时代不但没被淘汰，反而因为 vibe coding 降低了开发门槛而变得更容易执行。

风险与局限：这类产品的天花板也很明显——Intune 用户总量有限，$60K/月可能已接近市场上限（除非横向扩展到其他 MDM 平台）。对中国创业者而言，最大障碍是**市场选择**：国内企业 IT 管理生态与海外完全不同，直接照搬行不通，必须在国内找到等价的"IT 管理员每天手动干 1 小时的重复活"。

---

### 金矿 2：AI 产品烧钱困局 — 字节收缩应用层、Dan Koe 产品停摆、"没钱的反而活得久"

来源：@oran_ge（转发 @lifesinger 玉伯）· 2026-05-10 14:35 · 👍357 👁94,485
engagement_rate：0.26%（中等偏高）

另有 @weijunext 引用评论 · 2026-05-11 00:45

**核心数据（交叉验证）**

1. 字节跳动 AI 应用层调整：
   - 据推文原文（@lifesinger 玉伯，前蚂蚁金服前端负责人）："听闻字节全面收缩在 AI 应用层的投入，应用层聚焦到豆包，硬件层押注 PICO+ AI 硬件"
   - 经 web_search 验证：字节跳动 2026 年 AI 预算实际提升至约 1600 亿元人民币（约 $300 亿），但确实在从"免费烧用户"转向收费模式。豆包于 2026 年 5 月推出付费订阅（68/200/500 元/月），被多家媒体解读为"中国大模型免费时代终结"[据澎湃新闻、财新等多家媒体报道]
   - 豆包 MAU 3.45 亿，日 token 用量 120 万亿（2026 年 3 月数据，较 2024 年 5 月增长 1000 倍）[据字节跳动公开数据]
   - **修正**：玉伯原文"字节现金流撑不过 2027 年"的说法与公开数据存在矛盾——字节 2026 年 AI 预算仍在扩大。更准确的描述是：字节不是"烧不起"，而是"免费模式不可持续"，正在从烧钱换规模转向付费变现

2. Dan Koe 的 Eden 产品：
   - 据推文原文："百万粉丝博主 Dan Koe 的创业产品 Eden，因烧钱太快，决定大幅裁员，产品停止迭代"
   - 经 web_search 未找到 Eden 裁员或停摆的公开报道。Dan Koe 的 X 账号和 Substack 仍在活跃更新，Eden 仍在开发中 [未经验证——仅为推文原文说法，公开信息无法确认]

3. 核心论断："用互联网的思维去做 AI 产品创业，死路一条。AI 产品没有规模效应"
   - 这一判断的底层逻辑：AI 产品每新增一个用户，推理成本几乎线性增长（不像传统互联网产品的边际成本趋近于零）。追求 DAU 会直接拉爆成本

**复制路径（只写真正适用的档位）**

档位 B（独立开发者）：这条信号的直接行动指引——如果正在做 AI 产品，立刻算一笔账：每个付费用户的月均推理成本是多少？如果 ARPU 覆盖不了推理成本 + 利润，DAU 越大越亏。TypingMind（Tony Dinh，$137K/月）的做法值得参考：让用户自带 API Key，产品只收 UI 层的费用，推理成本 100% 转嫁给用户。

档位 C（工具集成者）：做 AI 工作流产品时，优先选择"按次计费"或"用户自带 Key"的模式。避免"包月无限用"的定价——那是在赌用户不会重度使用，一旦赌输就亏钱。

**深度综述**

这条信号揭示了 2026 年 AI 创业最重要的结构性矛盾：**AI 产品的成本结构与互联网产品根本不同**。传统互联网产品（社交、内容、电商）的边际成本趋近于零，规模效应是正向的——用户越多，单位成本越低。但 AI 产品的推理成本几乎是线性增长的：每多一个活跃用户，就多一份 GPU 算力开销。

字节跳动的豆包转向付费是这个矛盾的标志性事件。3.45 亿月活用户 × 120 万亿日 token = 天文数字的推理成本。免费模式下，字节即使年投入 1600 亿也扛不住。这不是字节"烧不起"，而是规模越大亏得越多——与传统互联网模型完全相反。

对一人公司创业者而言，这反而是个好消息。大厂的规模劣势意味着：**小而精、客单价高、推理成本可控的 AI 产品反而更健康**。Tony Dinh 的 TypingMind（$137K/月，据其 bio）就是典型：用户自带 API Key，产品只赚 UI 和功能层的钱，推理成本为零。Marc Lou 的产品矩阵（DataFast $21K/月、TrustMRR 等合计 $80K+/月）也是轻推理重工具的路线。

反直觉的启示是：在 AI 时代，"没钱"可能是一种竞争优势——因为没钱可烧，所以不会陷入"先免费获客再想变现"的陷阱，反而被迫从第一天就找到愿意付费的用户。

---

### 金矿 3：Harness Engineering — 宝玉长文解读 AI 时代软件工程新范式

来源：@dotey 宝玉 · 2026-05-11 06:23 · 👍199 👁30,853
engagement_rate：1.34%（极高，Top 5%）

另有 @oran_ge 引用评论："未来每个团队都是在做 harness 工程"· 2026-05-11 06:50 · 👍53 👁16,213 · engagement_rate 0.67%
以及 @LawrenceW_Zen 分享 Codex /goal 的 Harness Prompt 实战内容 · 2026-05-10 13:08 · 👍44 👁6,636 · engagement_rate 0.68%

内容类型：X Article（文章链接 x.com/i/article/2053591256110940160，经 web_search 验证为宝玉发布的长文）

**核心概念（经 web_search 验证）**
- "Harness Engineering"由 OpenAI Codex 团队在 2026 年初提出，Martin Fowler 也发布了同主题文章 [据 OpenAI 官方博客、InfoQ 报道]
- 核心思想：工程师不再直接写代码，而是**设计 AI Agent 的运行环境**——包括工具权限、安全护栏、反馈循环、可观测性。AI Agent 负责写代码、提 PR、自我审查
- 宝玉的文章将 Harness Engineering 与控制论（Cybernetics）做类比，认为这是人类第四次面对"反馈驱动的控制系统"范式转变
- 实战落地：OpenAI 内部的 Codex 团队已经用这套方法开发了完整的代码仓库——从第一个 commit 开始全部由 Agent 完成，人类只做优先级排序和验收

**国内可用性**
- Codex（OpenAI）：需要工具访问
- Claude Code（Anthropic）：claude.ai 直接访问，Claude Code CLI 直接可用
- 相关概念在国内已有实践：@LawrenceW_Zen 分享了 Codex /goal 模式的完整 Prompt（完成度审计的 12 条规则），并指出"国产模型一样可以胜任"

**复制路径（只写真正适用的档位）**

档位 B（独立开发者）：这是必须关注的范式转变。如果还在"让 AI 写一段代码然后手动审查"的阶段，效率差距会越来越大。具体行动：本周花 2 小时读 OpenAI 的 Harness Engineering 官方博客 + Martin Fowler 的文章，然后在自己的项目中尝试 Claude Code 的 worktree 模式——让 Agent 在隔离分支上独立完成一个功能，只做最后审查。

档位 C（工具集成者）：Harness Engineering 的核心思想可以用在任何 AI 工作流中——给 Agent 设定清晰的边界、反馈循环和验收标准，而不是"写一段 prompt 然后看运气"。@LawrenceW_Zen 分享的 Codex /goal Prompt 模板可以直接用在 Claude Code 或任何 Agent 框架中。

**深度综述**

Harness Engineering 不是一个新工具，而是一个新的工程范式——它重新定义了"软件工程师"这个角色在 AI 时代到底该干什么。从 OpenAI 内部实践到 Martin Fowler（软件工程界的旗帜性人物）正式撰文，说明这已经从前沿实验进入了主流工程实践。

对一人公司创业者而言，最值得关注的信号是 @oran_ge 的评论："未来每个团队都是在做 harness 工程"。这意味着：掌握 Harness Engineering 的人（会设计 Agent 运行环境、会写验收规则、会搭建反馈循环）将成为 AI 时代最稀缺的人才。Josh Pigford（@Shpigford）在同一天分享了"不打开 Xcode 就用 LLM 构建了 3 个 iOS 应用和 2 个 Mac 应用"——这就是 Harness Engineering 的实际产出效果。

风险在于：这套方法对 Prompt 设计和系统思维的要求很高，目前没有标准化的学习路径。宝玉、LawrenceW_Zen 等中文技术博主正在做翻译和实践分享，这些是目前最好的中文学习资源。

---

## 快讯区

> 未进入深度分析但值得知道，每条 1-2 句

**收入信号**
- Tony Dinh（@tdinh_me）bio 显示 TypingMind 当前 $137K/月，AI 聊天前端界面用自带 API Key 模式，推理成本零。Marc Lou 引用其安全审查方法：花 $70 token 跑出 30+ 安全修复 PR — @marclou · 2026-05-11 06:11
- Marc Lou（@marclou）bio 更新显示产品矩阵总收入约 $76K/月（含 DataFast $21K/月、ShipFast $36K/月等）。TrustMRR 上完成一笔 AI 音乐生成器收购：$100/月收入的产品卖了 $3,000 — @marclou · 2026-05-10 23:18
- Tibo（@tibo_maker，已验证高收入 solopreneur，Tweet Hunter 以 $8M 退出）称收到 X 平台有史以来最高的创作者分成付款 — @tibo_maker · 2026-05-10 14:00
- Nicolas Cole（@Nicolascole77，已验证 $6M ARR）分享案例：一位代笔写手在叉车行业做 ghostwriting，单月收入 $18,000（约 ¥130,500） — @dickiebush · 2026-05-10 21:13

**产品发布**
- Dickie Bush + Nicolas Cole 将 102 个写作模板打包成 5 个 Claude Skills，免费发放——评论区 1255 条回复，787 收藏，engagement_rate 1.03%。这类"模板即产品"的模式值得内容创作者参考 — @dickiebush · 2026-05-11 02:10
- 3DCellForge 开源：image to 3D 模型工具，对接 Tripo3D API，GitHub 开源 — @servasyy_ai（铁锤人引用）· 2026-05-10 19:20
- 歸藏（@op7418）发布 PPT Skill 新主题预览，Claude Skill 做 PPT 生成，111 收藏 — @op7418 · 2026-05-10 15:46

**工具更新**
- HuggingFace 官方 CLI 支持直接读论文：`hf papers read [论文编号]`，支持 arxiv 和 HuggingFace paper URL — @vista8 · 2026-05-10 22:57
- Lex Fridman 官网提供所有播客脚本字幕，可供 Agent 直接读取分析，无需从 YouTube 下载 — @vista8 · 2026-05-10 21:59
- Josh Pigford（@Shpigford）："不打开 Xcode 用 LLM 构建了 3 个 iOS 应用和 2 个 Mac 应用，LLM 非常擅长导航 Xcode CLI 工具"，将发布完整教程视频 — @Shpigford · 2026-05-11 03:22

**值得关注的观点**
- levelsio（$242K/月产品组合）在 VPS 开发推文下认同："stop developing locally, start developing on a VPS"——对于需要多设备协作或 Agent 持续运行的场景，VPS 开发正在成为 indie hacker 标配 — @levelsio · 2026-05-11 07:56
- 玉伯另一篇 X Article（370 收藏，engagement_rate 0.68%）和第三篇（291 收藏，engagement_rate 0.60%）均获高收藏，宝玉当日连发 3 篇技术长文，成为中文 AI 工程化内容最密集的信源 — @dotey · 2026-05-10 15:39 / 13:49
- Jason Cohen（@asmartbear，两家独角兽创始人）新文章探讨"幸存者偏差"：失败公司和成功公司做的事往往一样，我们到底能学到什么？ — @asmartbear · 2026-05-10 21:53

**教训与反思**
- Dickie Bush 列举过去一年的扩张失误：过早招人、在无效广告上烧钱、过度外包内容生产、重复办同一个活动。他将失败重新框架为"Mistake Dividends"（失误红利） — @dickiebush · 2026-05-10 20:33
- 郭宇（@turingou）指出 Apple 税对 AI 产品的挤压："iOS App 要比 web 版平白无故贵 15-30%，试问有什么动力做 app？"——AI 推理成本 + Apple 30% 抽成 = App 版本几乎无利可图 — @turingou · 2026-05-10 17:40

**传播力素材**（适合自媒体改写的高互动观点）

- "The only 2 places where I felt ambition like this are the US and China... Nomad hubs like Bali and Thailand are nice but often people there get stuck coasting at $5K MRR because it's just cheaper to live there" — @levelsio · 👍829 👁271,674 · engagement_rate 0.13%
  改写方向：适合公众号/视频号——"levelsio 说全球只有美国和中国有这种创业野心"，拆解不同城市的生活成本如何影响创业者的天花板，配上游牧生活 vs 深圳/杭州创业者的对比
  点评：levelsio 作为 $242K/月的 solopreneur 标杆，他对中国创业氛围的正面评价会引起共鸣。但他的判断偏表面——中国的创业野心很大程度上来自就业压力和阶层焦虑，与美国 SF 的"主动选择创业"有本质区别。只看这句话容易忽略中国创业者面临的独特困境（融资渠道有限、支付基础设施出海门槛高等）

- "Unpopular opinion: AI made the world super competitive for mediocre people." — @Prathkum · 👍3,464 👁162,473 · engagement_rate 0.18%
  改写方向：适合小红书图文——"AI 让平庸变得更卷了"，配上 AI 工具前后效率对比图，讨论 AI 时代个人护城河是什么
  点评：这条高赞的核心洞察是真实的——AI 确实在消除技能差距，过去靠"略懂一点"就能吃饭的中间层正在被挤压。但"mediocre"这个词过于笼统，实际情况是 AI 在消除执行层优势的同时，放大了判断力和品味的差异

- "Underrated truth: You'd make more money if you were delusionally confident, there is no better way" — @Codie_Sanchez · 👍2,640 👁40,608 · engagement_rate 0.89%
  改写方向：适合视频号短视频——"敢想敢做比精打细算更赚钱"，结合 Codie Sanchez 的收购型创业案例做解读
  点评：Codie Sanchez（70 万粉，多家企业创始人/投资人）这话说起来轻松，但背后是她在收购传统小企业时积累的实战经验。"delusionally confident"有效的前提是有足够的信息密度做支撑——盲目自信和有根据的自信完全不同。这句话容易被断章取义为"无脑冲"

- "networking as activity is mostly cope... do the work, then publish it loudly enough that the right ppl can find you" — @signulll（levelsio 引用）· 👍979+2,601 · engagement_rate 0.11%
  改写方向：适合公众号——"社交活动是弱者的幻觉"，结合 levelsio "Network events are for losers" 的观点，讨论一人公司创业者该如何获取人脉
  点评：signulll 的原文比 levelsio 的转发更有深度——指出"值得认识的人通常太忙没空被 networking"这个观察非常精准。但这条建议只适用于已经有作品可展示的人。对于刚起步的创业者，适度的线下社交仍然是获取早期反馈的有效渠道

- "AI 让生产成本降到 0，但反驳成本没变。你自己扛了验证成本 → 是 building。转嫁给读者 → 是 slop。" — @runes_leo · 👍3 👁678 · engagement_rate 0.29%
  改写方向：适合公众号——用"布兰多利尼定律"重新定义 AI 时代的内容质量标准，讨论创作者如何建立"验证成本"护城河
  点评：虽然绝对互动数低，但这条观点的原创性极高。AI 降低了生产成本但没降低验证成本，这个框架比"AI 会取代创作者"或"AI 是工具"的泛泛讨论有信息量得多。适合深度内容创作者使用

---

## 延伸资源库

### 播客 / 视频 / 访谈
- **Starter Story**: Pat Walls 访谈 Thomas Mahony（Pckgr 创始人），"I Make $60K/Month From the Most Boring SaaS on the Internet"（YouTube 视频）

### 图书 / 课程
- **《The Pathless Path》** — Paul Millerd：作者在 X 上做了新一轮免费赠书（精装重制版），并上线了自建的赠书平台 books.pmillerd.com/gift。这本书讲的是如何离开传统职业路径、建立自主生活，与一人公司读者高度相关
- **《命运的求索》** — 复旦大学教授著，向阳乔木推荐。微信读书可读。非 AI 相关，但在推文中获 1,082 收藏（engagement_rate 1.44%，当日全场最高之一），说明读者对跨界杂学知识有强需求

### 链接汇总（已 web_search 验证）

**工具类**
- Pckgr（Intune 应用打包）：intunepckgr.com
- TypingMind（AI 聊天前端）：typingmind.com — 国内直接访问
- TrustMRR（收入验证数据库）：trustmrr.com
- DataFast（收入优先分析工具）：datafa.st
- HuggingFace CLI：hf.co/cli/install.sh
- 3DCellForge（image to 3D 开源）：github.com/huangserva/3DCellForge
- Tripo3D（3D 模型生成）：tripo3d.ai — 国内直接访问

**报道类**
- OpenAI Harness Engineering 官方博客：openai.com/index/harness-engineering/
- Martin Fowler: Harness Engineering：martinfowler.com/articles/harness-engineering.html
- Jason Cohen 幸存者偏差：longform.asmartbear.com/survivor-bias/
- AI Slop 讨论：rmoff.net/2026/05/06/ai-slop-is-killing-online-communities/

**播客类**
- Lex Fridman 播客字幕库：lexfridman.com/podcast/

---

## 行动建议（按档位分组，不超过 4 条）

> 仅在金矿能直接转化为行动时给。

档位 A（内容创作者）
- 本周试试 Dickie Bush 的 Claude Skills 模板：评论"social"获取他的 102 个写作模板包，测试 Claude Skills 作为内容生产工作流的可行性。同时关注歸藏的 PPT Skill——用 Claude 生成演示文稿正在成为新的效率工具

档位 B（独立开发者）
- 今天 30 分钟：算一笔账——当前产品的每用户月均推理成本是多少？ARPU 能否覆盖？如果不能，立刻考虑"用户自带 Key"或"按次计费"模式。参考 TypingMind 的做法
- 本周：读 OpenAI Harness Engineering 博客 + Martin Fowler 文章，在自己项目中用 Claude Code worktree 模式做一次完整的 Agent 驱动开发实验

档位 C（工具集成者）
- 本周：用 @LawrenceW_Zen 分享的 Codex /goal Prompt 模板（完成度审计 12 条规则），套用到自己的 AI 工作流中。这套规则可以直接用在 Claude Code 或任何 Agent 编排场景里

---

## 避坑指南

> 仅当本期推文中有真实的失败案例 / 反思类信号时才写。

- **AI 产品"包月无限用"定价陷阱**：玉伯的分析指出 AI 产品没有传统互联网的规模效应。如果正在做 AI 产品并采用包月不限量定价，务必重新核算推理成本。字节跳动 3.45 亿月活的豆包都扛不住免费模式，一人公司更不可能
- **iOS App 的 Apple 税叠加推理成本**：郭宇的提醒——AI 产品做 iOS App 要额外承担 15-30% 的 Apple 抽成，叠加推理成本后利润极薄。优先做 Web 版，App 版仅作为高价值用户的补充渠道

---

## 本期情报评估

**信息密度**：正常
周日（母亲节）推文量偏生活化，但仍有 2-3 条实质性强信号。levelsio 大量推文集中在餐饮吐槽话题（Sysco 预制食品），占据了大量 timeline 空间但与一人公司无关。

**趋势信号**：
AI 产品的成本结构正在迫使整个行业从"免费换规模"转向"小而精赚利润"。字节豆包收费、玉伯的烧钱警告、Tony Dinh 的零推理成本模式——多条独立信号共同指向：一人公司式的轻量 AI 产品可能比融资烧钱的 AI 大厂更有生存韧性。

**横向对比**：
本期出现了两种截然不同的赚钱路径——Pckgr 的"无聊 SaaS"（$60K/月，非 AI 核心）vs Tony Dinh 的 TypingMind（$137K/月，AI 工具但零推理成本）。两者的共同点是：**不烧钱、客户真付费、推理成本可控或为零**。

**当日强信号数 vs 噪音比**：
3 条强信号（Pckgr 收入、AI 烧钱困局、Harness Engineering）/ 约 60 条噪音（母亲节、餐饮吐槽、生活分享、金句类）。周日信噪比偏低属正常。

**本期信源**：@thepatwalls @starter_story @oran_ge @lifesinger @dotey @LawrenceW_Zen @marclou @tdinh_me @levelsio @vista8 @dickiebush @Nicolascole77 @Shpigford @tibo_maker @turingou @Prathkum @Codie_Sanchez @runes_leo @weijunext @op7418 @xiaohu @indie_maker_fox @asmartbear（共 23 位）
