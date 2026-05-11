# AI 一人公司日报 | 2026-05-11

数据窗口：09:14 — 09:14（北京时间，过去 24 小时）
深度挖掘：2 条

---

## 今日头条

Starter Story 创始人 Pat Walls 发布了一期访谈视频：一个做 Microsoft Intune 应用打包自动化工具的独立开发者 Thomas，靠这个"无聊"的 IT SaaS 做到月入 $60K。engagement_rate 高达 3.05%（同期中位数约 0.15%-0.20%），是本期收藏率最高的推文，说明这类"无聊但赚钱"的路径对一人公司群体有极强的行动号召力。同期另一条重要信号来自玉伯（Frank Wang）：AI 产品没有规模效应，用互联网思维烧 AI 应用是死路一条——对正在做 AI 产品的创业者是一个值得认真对待的警告。

---

## 今日金矿

> 数量按真实信号定，今日 2 条。

### 金矿 1：月入 $60K 的"无聊" IT SaaS——Intune 应用打包工具

**来源：**@thepatwalls（Pat Walls，Starter Story 创始人）· 2026-05-11 04:42 · 👍371 👁23,544
engagement_rate：3.05%（极高，Top 1%）

**核心数据（已验证）**
- 月收入：$60,000（约 ¥432,000，按 1 USD = 7.2 CNY）[据推文原文 + Starter Story 视频]
- 产品定位：Microsoft Intune 应用打包自动化工具，将 IT 管理员手动打包 Win32 应用的流程（原本每个应用需约 1 小时）缩短到一键完成 [据 Starter Story 视频描述]
- 订阅价格：$25/月 [据推文原文]
- 推算用户规模：约 2,400 付费用户（$60K ÷ $25）[推算，未经验证]

**商业模式拆解**
- 定价结构：$25/月订阅制（入门级），可能有更高层级 [未经验证]
- 收入公式：纯 SaaS 订阅，~2,400 用户 × $25/月 = $60K/月
- 目标客户：企业 IT 管理员，使用 Microsoft Intune 做设备管理的中大型企业
- 护城河：极度垂直的利基市场，竞争者少，客户粘性高（一旦纳入 IT 运维流程很难替换）

**复制路径**

档位 B（独立开发者）：
- 核心逻辑：找一个企业 IT 管理中"手动、重复、痛苦但必须做"的环节，用软件自动化。不追新，不追 AI 概念，而是解决已存在多年的行政性痛点。
- 方向参考：国内企业 IT 场景中，MDM（移动设备管理）、企业微信/钉钉应用分发、等保合规检查自动化、IT 资产盘点工具等领域都存在类似机会。
- 冷启动：Reddit（r/sysadmin、r/Intune）是 Thomas 的冷启动渠道。国内对应的社区是 V2EX、运维圈子（ITIL 相关论坛）、企业微信群。
- 技术栈：无需 AI，传统 Web + API 集成即可。关键是深入理解目标用户的工作流程。

档位 C（工具集成者）：
- 可以用 n8n / Make 构建类似的"IT 运维自动化"工作流，打包成服务卖给中小企业 IT 部门。不需要写完整 SaaS，先以"自动化服务"形式验证需求。

**竞争格局**
- 国内 Intune 用户基数远小于海外（微软企业产品在中国的渗透率有限），直接复制 Intune 打包工具市场空间不足。
- 但"无聊 IT 工具"的方法论完全可迁移：找到企业 IT 管理中被忽视的手动环节，做一个自动化工具，按月订阅收费。

**成本与时间预期**
- 需进一步调研。Thomas 的产品不依赖 AI 推理成本，纯 SaaS 利润率预计较高。

**深度综述**

这条信号最有价值的不是"又一个月入 $60K 的产品"，而是它揭示的路径选择逻辑。当 timeline 上所有人都在讨论 AI wrapper、Agent 框架、vibe coding 的时候，Thomas 选了一个完全不性感的赛道——给 IT 管理员省时间。

**商业模式拆解：** $25/月的定价在 B2B SaaS 里属于"不需要审批"的价位带——IT 管理员可以直接用公司信用卡付费，不需要走采购流程。这个定价策略本身就是一种增长机制：降低购买决策摩擦。2,400 个付费用户意味着 Thomas 不需要做大规模营销，靠 Reddit 社区口碑和 SEO 就够了。

**意外与反直觉：** engagement_rate 3.05% 是本期所有推文中最高的，远超第二名。这说明一人公司社群对"无聊但赚钱"的故事有着极高的行动意愿——不是"看完就忘"，而是存下来准备照做。这种信号反复出现（Starter Story 的核心内容策略就是挖掘此类故事），说明市场对"可复制的小生意"的需求远大于对"下一个独角兽"的幻想。

**风险与局限：** 最大风险是微软自己做这个功能。Intune 打包工具之所以能存在，是因为微软把这个功能做得足够难用。但微软随时可能优化 Intune 的打包体验，届时第三方工具的价值会大幅缩水。在中国市场，企业 IT 管理工具的付费意愿整体偏低，SaaS 订阅模式的接受度不如海外。

**趋势定位：** 这是"反 AI hype"的信号——不用 AI 也能做出高利润 SaaS。处于持续验证阶段，不是新趋势，而是一直存在但被 AI 浪潮淹没的路径。Pat Walls 的 Starter Story 于 2026 年 2 月被 HubSpot 收购（据公开报道），说明这类"挖掘无聊生意"的内容平台本身也具有商业价值。

**原始链接：** https://x.com/thepatwalls/status/2053576470220419404

---

### 金矿 2：AI 产品没有规模效应——字节收缩传闻与一人公司的反面教材

**来源：**@lifesinger（Frank Wang 玉伯，前蚂蚁集团工程师）via @oran_ge（Orange AI）转发 · 2026-05-10 14:35 · 👍357 👁94,485
engagement_rate：0.26%（中等偏高）

**核心论点**
玉伯提出三个关联信号：
1. 传闻字节跳动收缩 AI 应用层投入，应用层聚焦豆包，硬件层押注 PICO + AI 硬件 [未经验证——见下方说明]
2. 多家 ARR 过亿美元的 AI 应用公司开始裁员，现金流压力极大 [未经验证]
3. 百万粉丝博主 Dan Koe 的创业产品 Eden 因烧钱太快，大幅裁员并停止迭代 [未经验证——经 web_search 未找到 Eden 关停的公开报道，Dan Koe 的 X 账号仍在正常更新]

核心结论："用互联网的思维去做 AI 产品创业，死路一条。AI 产品没有规模效应。"

**验证与交叉检查**

关于字节收缩传闻：**与公开数据矛盾。** 据南华早报报道，字节跳动 2026 年资本开支计划提升至超 2000 亿人民币（约 $300 亿），较原计划增加 25%+，主要用于 AI 基础设施。豆包 MAU 已达 3.45 亿（据 TechNode），且 2026 年 5 月开始测试付费订阅。因此"字节撑不过 2027"的说法缺乏公开数据支持。

关于 Dan Koe Eden 关停：**未能验证。** Dan Koe 此前确实放弃了 Kortex 项目并重建为 Eden，但截至目前未找到 Eden 关停或大幅裁员的公开消息。

关于"AI 产品没有规模效应"这一论点本身：**有部分数据支撑。**
- OpenAI 2026 年预计亏损 $140 亿，现金流转正不早于 2030 年（据 FutureSearch）
- Amazon 自由现金流从 $260 亿降至 $12 亿，直接原因是 AI 资本开支超过回报
- AI wrapper/应用市场 80%-95% 失败率，仅 2%-5% 达到 $10K/月 ARR（据 Market Clarity）
- 反例：Cursor 24 个月内年化收入突破 $10 亿；Lovable 从 $700 万 ARR 增长到 $2.06 亿 ARR

**对一人公司的核心启示**

这条信号的价值不在于"字节是否真的在收缩"，而在于一个更本质的判断：**AI 产品的边际成本不趋近于零。** 传统 SaaS 多卖一个用户几乎不增加成本，但 AI 产品每多一个用户就多一份推理成本。这意味着：
- 追求 DAU 的互联网增长模型在 AI 产品上可能是自杀
- 对一人公司而言，高定价 + 精准客群 + 控制推理成本，比烧钱抢用户更可持续
- 金矿 1 中 Thomas 的 Intune 工具恰好是反面参照：不用 AI，纯 SaaS，边际成本趋近于零

**复制路径**

档位 B（独立开发者）：
- 如果正在做 AI 产品，立刻计算每用户每月的推理成本占 ARPU 的比例。如果超过 30%，定价模型需要重新设计。
- 考虑"AI 增强"而非"AI 驱动"：核心价值用传统代码实现，只在关键环节调用 AI，把推理成本控制在可预测范围内。

档位 C（工具集成者）：
- 用 AI 做交付工具（帮客户完成任务），而不是做 AI 产品（让用户自己用 AI）。前者的成本是一次性的且可控，后者的成本随用户量线性增长。

**深度综述**

玉伯的帖子引发了大量讨论（67 条回复），@weijunext 的转评"揭示了一个事实：每天重度使用 AI 的人也难以分辨 AI 生成的垃圾"从另一个角度点出了问题——AI 应用的质量控制成本也在上升。

**商业模式拆解：** 核心矛盾在于 AI 应用的成本结构和互联网应用完全不同。互联网时代的边际成本接近零让"先亏损后盈利"成为可行策略，但 AI 时代每一次推理都有真实成本。即使是 OpenAI 这样的头部玩家，2026 年的亏损规模也在扩大而非缩小。对一人公司而言，这其实是好消息：大公司烧钱抢市场的策略在 AI 领域失效，精准服务小众高付费客群的一人公司反而有生存空间。

**竞争格局：** Cursor、Lovable 等少数 AI 开发工具实现了爆发式增长，但它们的共同特征是：用户付费意愿极强（开发者愿意为效率付费）、使用场景明确（代码生成）、替代路径清晰（替代传统 IDE 或低代码平台）。大多数 AI 应用不具备这些条件。

**风险提示：** 玉伯的帖子中具体的字节收缩传闻和 Dan Koe Eden 关停均未能通过公开渠道验证。"AI 产品没有规模效应"作为一个笼统判断也有例外。建议将其作为一个思考框架而非定论。

**原始链接：** https://x.com/oran_ge/status/2053363322632933556（@oran_ge 转发原帖来自 @lifesinger）

---

## 快讯区

> 未进入深度分析但值得知道，每条 1-2 句

**收入信号**
- Tony Dinh（@tdinh_me）bio 更新显示 TypingMind 月收入 $137K/月（约 ¥986K），较此前公开的 $100K+ 有显著增长。TypingMind 是一个 ChatGPT/LLM 的替代前端界面，B2B 团队订阅占比已超 50%。[据其 bio，已通过 GetLatka 等渠道交叉验证] — @tdinh_me · 2026-05-11 07:29
- Marc Lou（@marclou）bio 显示产品矩阵月收入约 $76K（$36K TrustMRR + $21K DataFast + $9K CodeFast + $8K ShipFast + $2K 其他）。2025 全年收入 $1,032,000。[据其 newsletter 公开数据] — @marclou · 持续更新
- Marc Lou 在 TrustMRR 上分享了一个案例：@ritiksharmarj 做了一个 AI 音乐生成器，月收入约 $100，以 $3,000 卖出。微型收购市场的活跃度信号。 — @marclou · 2026-05-10 23:18
- Tibo（@tibo_maker，已验证 solopreneur，Tweet Hunter/Taplio 以 $800 万卖出）称 X 平台最新一期分成是他收到的最高金额。 — @tibo_maker · 2026-05-10 14:00

**产品发布**
- Josh Pigford（@Shpigford）称用 LLM（Claude Code）不打开 Xcode 就完成了 3 个 iOS App 和 2 个 Mac App 的开发，并将分享完整 iOS/macOS AI 开发设置教程，包含使用视觉模拟器验证工作的 MCP 配置。[已部分验证：其开源项目 Clearly 和 Chops 确认通过此方式构建] — @Shpigford · 2026-05-11 03:22 / 03:32
- Dickie Bush（@dickiebush）将 102 个写作模板打包为 5 个 Claude Skills，覆盖 hook 写作、X 内容创作和代写客户服务。engagement_rate 1.03%（极高）。[Dickie Bush 确认在运营 Write With AI newsletter，120K+ 订阅者，Claude Skills 整合方向已验证] — @dickiebush · 2026-05-11 02:10
- 歸藏（@op7418）发布 PPT Skill 新主题预览，基于 Claude Skills 生成演示文稿。engagement_rate 0.59%。 — @op7418 · 2026-05-10 15:46
- 3DCellForge 开源（@servasyy_ai）：image to 3D 模型工具，对接 tripo3d.ai，@lxfater 转发点评"不错"。GitHub 已开源。 — @lxfater · 2026-05-10 19:20

**工具更新**
- 向阳乔木（@vista8）分享 HuggingFace 官方 CLI 工具，可通过命令行直接阅读 AI 论文：`hf papers read [论文编号/URL]`，支持 arxiv 和 HF Paper。engagement_rate 0.97%。 — @vista8 · 2026-05-10 22:57
- 向阳乔木分享 Lex Fridman 播客官网提供所有节目的完整文字脚本，可直接让 Agent 读取处理，无需从 YouTube 下载。engagement_rate 1.38%。 — @vista8 · 2026-05-10 21:59
- 向阳乔木分享 Vibe Coding 时让 AI 设计 UX 交互的实用 Prompt 技巧：让 AI 搜索参考最佳实践。engagement_rate 1.08%。 — @vista8 · 2026-05-10 09:19
- 郭宇（@turingou）推荐 Portless 新更新，解决了本地开发的大部分问题，模拟器也可访问本机服务。 — @turingou · 2026-05-10 21:27
- 宝玉（@dotey）发布至少 3 篇 X Article，收藏量分别为 414、370、291。其中一篇关于 AI Agent Harness 架构的深度拆解（同时被 @oran_ge 转评："未来每个团队都是在做 harness 工程"）。"Harness 工程"概念已被 Martin Fowler 网站正式收录，指 AI Agent 系统中模型之外的一切——工具、记忆、上下文管理、反馈循环。 — @dotey · 2026-05-10 ~ 2026-05-11

**值得关注的观点**
- levelsio（@levelsio，已验证 solopreneur，产品矩阵月入 ~$242K）："全球只有美国和中国让我感受到这种野心。数字游民聚集地如巴厘岛和泰国的人容易卡在 $5K MRR，因为生活成本低到'够了'就停下。旧金山/纽约因为生活成本极高，自然筛选出极度有野心或已经成功的人。中国不是因为贵，而是文化中有一种要在所有事情上做到第一的天然野心。" — @levelsio · 2026-05-10 22:18
- Jason Cohen（@asmartbear，WP Engine 和两家独角兽创始人）发布长文探讨"幸存者偏差"：失败公司做的事和成功公司几乎一样，那我们到底能学到什么？ — @asmartbear · 2026-05-10 21:53
- 郭宇质疑 Apple 对 AI 应用收取 IAP 税的合理性："Apple 自己不负责推理，但 AI 相关收入仍要缴 15-30% Apple 税，导致 App 版本比 Web 版本平白贵出一截。"这对做 AI 产品的独立开发者是真实的成本约束。 — @turingou · 2026-05-10 17:40

**教训与反思**
- Dickie Bush 分享了过去一年扩张业务时犯的战略错误：过快招人、在无效广告上花钱而非加倍做有效的有机增长、过度外包内容生产、重复办活动而非创新。他把失败重新定义为"错误红利"（Mistake Dividends）。 — @dickiebush · 2026-05-10 20:33
- Tony Dinh 和 Marc Lou 都提到用 AI 做安全审计：花 ~$70 token 成本，对代码库做了一次安全扫描，产出 30+ PR，全部是合法的非关键安全问题。 — @tdinh_me · 引用，@marclou 转评 · 2026-05-11 06:11

**传播力素材**（适合自媒体改写的高互动观点）

- "Unpopular opinion: AI made the world super competitive for mediocre people." — @Prathkum · 👍3,464 👁162,473 · engagement_rate 0.18%
  改写方向：适合公众号/视频号——"AI 让平庸者的竞争更激烈了"这个角度可以展开为：AI 不会取代所有人，但会让"还行"的人变得不够用。配合具体案例（AI 写的代码/文案 vs 高手写的）做对比。
  点评：这条之所以引发共鸣，是因为它击中了大量中间层从业者的焦虑——不是最差被淘汰，而是"还行"不再够用。局限性在于把问题过度简化了：AI 同样在降低优秀人才的进入门槛，而非只挤压平庸者。

- "The only 2 places where I felt ambition like this are the US and China" — @levelsio · 👍829 👁271,674 · engagement_rate 0.13%
  改写方向：适合小红书图文——把"只有美国和中国有这种野心"这个判断拆成对比体，配上中美创业者日常对比照，加上"为什么数字游民聚集地反而容易'够了就好'"的反直觉角度。
  点评：levelsio 的观察有真实经验基础（他在全球多地生活和工作过），"高生活成本 = 天然野心筛选器"这个框架有一定解释力。但把中国的野心归因于"文化天然"过于简化，忽略了经济结构、就业竞争压力等更现实的驱动因素。

- "Network events are for losers" — @levelsio · 👍979 👁151,205 · engagement_rate 0.11%（引用 @signulll 长文："networking as activity is mostly cope... do the work, then publish it loudly enough that the right ppl can find you"）
  改写方向：适合视频号/公众号——"为什么社交活动是浪费时间"这个话题天然有争议性，可以做成正反辩论体。核心论点：值得认识的人太忙了不会出现在社交活动上，而出现在社交活动上的人往往是因为没有更好的事做。
  点评：这个观点来自一个不需要社交的人（levelsio 靠产品和 Twitter 就有足够的人脉），对已经有影响力的人是正确的，但对冷启动阶段的创业者来说，线下社交仍然是获取最初信任和客户的有效方式。观点本身就是幸存者偏差。

- "Underrated truth: You'd make more money if you were delusionally confident, there is no better way" — @Codie_Sanchez · 👍2,640 👁40,608 · engagement_rate 0.89%
  改写方向：适合小红书——"盲目自信为什么有用"这个话题可以配合心理学研究（邓宁-克鲁格效应的反面运用）做成知识型内容。
  点评：Codie Sanchez（703K followers，多家公司创始人）说这话有幸存者偏差的底色——盲目自信在她的案例里确实有用，但对大多数人来说，没有执行力的自信只是幻觉。这条金句的真正价值在于"行动偏好"而非"自信本身"。

---

## 延伸资源库

### 播客 / 视频 / 访谈
- Starter Story 视频："I Make $60K/Month From the Most Boring SaaS on the Internet"（Pat Walls 访谈 Thomas）— YouTube
- Lex Fridman 播客完整文字脚本库：https://lexfridman.com/podcast/

### 图书 / 课程
- 《命运的求索》— 复旦大学教授著，讲述中国各种算命流派和逻辑。@vista8 推荐，微信读书可读。engagement_rate 1.44%（极高）。非 AI 相关，但因极高互动收录。
- 《The Pathless Path》重新设计版 — Paul Millerd（@p_millerd）开放预购，同时在 books.pmillerd.com/gift 免费赠送电子版（限量 100 本/月）。

### 链接汇总

**工具类**
- HuggingFace CLI 安装：`curl -LsSf https://hf.co/cli/install.sh | bash`
- Tripo 3D（图像转 3D 模型）：tripo3d.ai — 国内可直接访问
- 3DCellForge 开源仓库：https://github.com/huangserva/3DCellForge
- Lex Fridman 播客脚本：https://lexfridman.com/podcast/

**报道类**
- Jason Cohen 幸存者偏差长文：https://longform.asmartbear.com/survivor-bias/
- Martin Fowler 网站 Harness Engineering 定义：martinfowler.com/articles/harness-engineering.html
- AI slop 对社区的影响（Robin Moffatt 博客）：https://rmoff.net/2026/05/06/ai-slop-is-killing-online-communities/

**社区类**
- Initial Commit（Josh Pigford 的 AI 原生开发者社区）：initialcommit.co

---

## 行动建议（按档位分组）

> 仅与本期金矿直接关联的档位。

档位 B（独立开发者）
- **本周可验证的事：** 列出 3 个企业 IT 管理中"手动、重复、痛苦"的环节（参考金矿 1 的 Intune 打包思路），在 V2EX 或目标行业论坛搜索相关吐槽帖，评估哪个痛点足够尖锐到让人愿意付 $25/月。
- **今天 30 分钟可做的事：** 如果已有 AI 产品，打开后台算一下每用户每月的推理成本占 ARPU 的比例（参考金矿 2）。超过 30% 需要重新评估定价或架构。

档位 C（工具集成者）
- **本周可验证的事：** 用 Claude Code 尝试不打开 Xcode 构建一个简单的 iOS App（参考 @Shpigford 的方法）。如果能跑通，这本身就是一个可以打包成教程或服务卖的技能。

---

## 本期情报评估

**信息密度**：低密度
周日 + 美国母亲节，timeline 被生活类内容（levelsio 连发 5 条餐厅讨论）和励志金句大量占据。@TrungTPhan 的高浏览量内容全部为娱乐/讽刺类（DeepMind 纪录片回顾、假的 AP × 麦当劳联名鸡块新闻），均已过滤。@lidangzzz 11 条推文中与 AI/一人公司相关的为 0 条。

**趋势信号**：
"不用 AI 也能赚钱的 SaaS" 和 "AI 产品烧钱困局" 这两个信号同日出现，形成了一个值得关注的张力：一人公司群体正在从 AI hype 中退一步，重新审视基本的商业逻辑——利润率、边际成本、客户付费意愿。

**当日强信号数 vs 噪音比**：
2 条强信号 / ~160 条噪音（大量生活类内容、励志金句、母亲节祝福、餐厅食品讨论）。信号密度显著低于工作日。

**本期信源**：@thepatwalls @lifesinger @oran_ge @levelsio @marclou @tdinh_me @tibo_maker @Shpigford @dickiebush @vista8 @dotey @turingou @Prathkum @Codie_Sanchez @asmartbear @op7418 @lxfater @weijunext @runes_leo @Nicolascole77（共 20 位）
