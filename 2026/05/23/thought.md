# 思想发现简报 | 2026-05-23

> 数据窗口：2026-05-22 06:00 — 2026-05-23 06:00（北京时间，过去 24 小时）
> 深度挖掘：3 条 | 模板版本：v1.2

---

## 一、今日要点

5 月 22 日凌晨，匿名分析师账号 @HedgieMarkets 发布的一段长贴被图灵奖得主、Meta 前首席 AI 科学家 Yann LeCun（@ylecun，纽约大学教授）转发：微软本周正式取消其内部对 Anthropic 公司编程助手 Claude Code 的全部许可证；与此同时，Uber 首席技术官内部备忘录承认，公司 2026 全年的 AI 预算在四个月内被烧光。这条推文 24 小时内被收藏 1.06 万次，是本期 List 中收藏量最高的"思想类"信号——远高于同期 Starship V3 试飞实况或欧冠夺冠等高浏览娱乐推文。

这是一件值得读者今晚停下来想一会儿的事。过去三年里，企业级 AI 工具的"补贴定价"塑造了所有人的直觉：编程助手、对话模型、视觉工具的价格似乎只会向下。但 Claude Code 改成按 token（每次 AI 推理消耗的字符量 × 单价）付费之后，连微软这种"算力近乎无限"的公司也算出了"不划算"。投资人 Chamath Palihapitiya（@chamath，Social Capital 创始人）同日跟进评论：问题不是工具没用，而是"没有上下文与监督的智能体（agent，能自主调用工具完成任务的 AI 程序）会无限空转"，把账单推到企业不能承受的规模。两条独立信号在同一天指向同一个判断——AI 的"补贴时代"正在以肉眼可见的速度结束。

**Bottom line in English:** The AI subsidy era is ending in real time — when Microsoft itself can't justify a competitor's token bill, the unit-economics question is no longer hypothetical.

---

## 二、主信号（多源验证）

### 信号 #1：微软取消 Claude Code 许可——AI 补贴时代结束的标志性时刻

主信源：@ylecun（领域内权威 / Turing 奖得主，转发 @HedgieMarkets 长帖）· 约 11 小时前
佐证：@chamath（投资人 / Social Capital 创始人）· @michaeljburry（投资人 / 大空头）从空头视角的同步质疑 · 媒体核实见下方深挖
题材分类：科技 / 商业

故事 / 场景：
Hedgie 在帖子里写出几个具体数字：微软"本周"通知近 10 万工程师在 2026 年 6 月底前停用 Claude Code，转用自家 GitHub Copilot CLI；同期 Uber CTO 在内部备忘录中说，按"重度用户每月最高 2000 美元"的实际单价，全公司 5000 名工程师的 AI 预算 4 个月就烧光；美国 AI 软件价格过去半年涨了 20%–37%；GitHub 也在把"包月制"换成"按用量计价"。

为什么值得思考：
过去两年企业 AI 战略的隐性假设是"AI 成本会持续下降"。这条信号一次性把这个假设撕开了：在按 token 计价的真实账单下，AI 一点都不便宜——便宜的只是被补贴的早期阶段。Chamath 进一步指出"工具空转"问题：智能体在缺乏上下文时会反复试错，把账单推向几何级数。这与去年同期讨论的"AI 让边际成本归零"完全相反。

关键引文：
> EN: "The AI subsidy era is ending in real time."
>
> 中：AI 的补贴时代正在实时结束。
> （来源：@HedgieMarkets 长帖，@ylecun 转发；多家媒体核实，详见深挖一）

链接：
- 推文：https://x.com/ylecun/status/2057782982757257330
- @chamath 评论：https://x.com/chamath/status/2057848053202305506

---

### 信号 #2：Polsia 完成 3000 万美元融资，估值 2.5 亿美元——"一人公司 + 自主智能体"成为可定价的资产类别

主信源：@Scobleizer（Robert Scoble，前微软福音传道者、八本科技书作者）转发 @Bencera（Polsia 创始人 Ben Cera）· 约 5 小时前
佐证：Apple 前产品负责人 Josh Elman（@joshelman）与著名投资人 Tony Conrad（@tonysphere）公开背书（Scoble 引用其推文）
题材分类：商业 / 创业 / 投资

故事 / 场景：
Polsia 创始人 Ben Cera 自述：完成 3000 万美元融资、估值 2.5 亿美元、年化收入接近 1000 万美元——"一个创始人加上 AI，零员工。Polsia 自主运营公司，它甚至自己完成了这轮融资，我只是出现在签字现场"。这条推文 24 小时收藏 2440 次，engagement_rate 0.29%，明显高于同时段其他融资类推文。

为什么值得思考：
"一人公司"过去是博客词汇，今天变成了带审计师签字的 cap table（股权结构表）。这与去年讨论的"AI 让小团队跑出独角兽"叙事不同——这条主张的是"AI 跑出收入流，人只是法律意义上的签名人"。如果属实，VC 对"管理层"与"团队规模"的估值模型需要重写。但要警惕：所有数字均出自当事方口径，未经独立审计披露，应作为"营销叙事"而非已验证事实对待 [未经多源验证]。

关键引文：
> EN: "One Founder + AI. Zero employees. Polsia runs companies autonomously."
>
> 中：一个创始人加上 AI，零员工。Polsia 自主运营公司。
> （来源：@Bencera，当事方原话）

链接：
- 主推文：https://x.com/Scobleizer/status/2057864509742850414
- Scoble 的二次评论（援引 Elman/Conrad 背书）：https://x.com/Scobleizer/status/2057870983281902060

---

### 信号 #3：美国新绿卡政策"必须回原籍国申请"——硅谷 AI 圈罕见集体表态

主信源：@reidhoffman（Reid Hoffman，LinkedIn 联合创始人、微软董事、AI 公司 Manas 投资人）· 约 5 小时前
佐证：@AndrewYNg（Andrew Ng，Coursera 联合创始人、Google Brain / 百度 AI 前负责人、斯坦福兼职教授）独立发声 · DHS 政策原文（@DHSgov）
题材分类：科技 / 经济 / 监管

故事 / 场景：
美国国土安全部（DHS）宣布：在美临时居留的外国人申请绿卡时必须先回母国办理。Reid Hoffman 当晚发问："这意味着 AI 研究员、员工、学生都要离境，等候积压的程序？对科技、商业、美国整体都是有害之举。"Andrew Ng 同步发推：这是"对合法移民的任意打击"，将"伤害家庭，让我们少医生、少教师、少科学家，损害美国在 AI 上的竞争力"。

为什么值得思考：
两位发言人都有具体雇佣经验——他们的判断不是政治站队，是"我招人时实际发生什么"的口径。这条信号与微软 Claude Code 事件叠加：美国 AI 产业同一周遭遇成本侧（token 账单）与人才侧（签证）的双重挤压。对中国读者而言，这是判断 2026 下半年中美 AI 人才流向的关键参考点之一。

关键引文：
> EN: "Harmful move for tech, business, and America broadly..."
>
> 中：对科技、商业、美国整体都是有害之举……
> （来源：@reidhoffman）

链接：
- Hoffman：https://x.com/reidhoffman/status/2057875188176531766
- Ng：https://x.com/AndrewYNg/status/2057907324380217821

---

## 三、单源高启发信号

> ⚠️ 重要说明：以下信号仅有一个来源，未经多方独立验证。但发言人在该领域有明确权威性，内容具有思想价值。请读者自行判断。

### 启发 #1：Kevin Kelly——"程序员不真正写代码，数学家不真正做证明"

发言人：@kevin2kelly（Kevin Kelly，《连线》资深 maverick、《必然》作者，被视作硅谷"长期思考者"代表）
领域：技术哲学 / 工作未来
发布时间：约 23 小时前

他说了什么：
"令我们意外的是，今天的程序员不真正在写代码、数学家不真正在做证明、作家不真正在写词句。我们的未来不是岗位被替代，而是一种一年前都难以想象的'新工作'形态正在出现。"（"We have been surprised that coders still code without actually coding, mathematicans do not do math proofs, and writers who write without actually writing words. Our future is not job replacement but a kind of new work we have trouble imagining only a year ago."）

为什么值得记下：
这是 Kelly 在本 List 过去 7 天里的唯一一条原创推文（稀缺度加分）。他没有给出新框架，但提出了一个比"AI 取代工作"更精细的问题：每个职业的"动作"被 AI 接管之后，"职业"这个名词本身意味着什么？这是 Kelly 长期关注的"技术想要什么"（What Technology Wants）思路的延伸。

目前的不确定性：
- Kelly 没有给出具体案例，只是直觉描述
- 与同期 Andy Hall（斯坦福 GSB）的"学生用 AI 写评估"案例可以互补印证，但未直接连接

链接：https://x.com/kevin2kelly/status/2057593995296211215

---

### 启发 #2：Greg Brockman——"模型本身已不再是产品"

发言人：@gdb（Greg Brockman，OpenAI 总裁、联合创始人）
领域：AI 产品策略
发布时间：约 18 小时前

他说了什么：
"the model alone is no longer the product"——模型本身已不再是产品。
该推文 6095 likes、579 bookmarks、engagement_rate 0.09%。配合他当天对 OpenAI Codex "Appshots"（双 ⌘ 键把当前应用上下文发给 Codex）和 "Remote Computer Use"（手机远程操作锁屏状态下的本地 Mac）的连续转发。

为什么值得记下：
这是 OpenAI 一号位人物 7 天内首次明确表态"模型不是终点"。他没有点名 Anthropic，但语境与 Cursor Composer 2.5、Anthropic Claude Code 等"工具层"产品的争夺密切相关——OpenAI 在用 Codex 重新定义"AI 工具 = 工作流（harness，把模型嵌入开发流程的容器）+ 模型"的复合体。这与同日 Yann LeCun 转发的"AI 单位经济学"问题正面相关：如果模型不能再独立卖钱，订阅价格必须由更厚的"工具层"价值支撑。

目前的不确定性：
- 这是 OpenAI 自己的策略表态，可能服务于其抢占"工具层"叙事的商业目的
- 微软 Claude Code 事件是否反过来证明"工具层"也无法消化 token 成本？两个判断暂时无法在 24 小时窗口内闭环

链接：https://x.com/gdb/status/2057670776803996110

---

### 启发 #3：Michael Burry——"海底数据中心比天上数据中心合理得多"

发言人：@michaeljburry（即"Cassandra Unchained"，电影《大空头》原型、近期关闭 Scion 基金转 Substack 付费写作）
领域：投资 / 基础设施
发布时间：约 6 分钟前（窗口边缘）

他说了什么：
"在跨大西洋数据线缆附近的海底布数据中心，不会让我卖掉 SpaceX 股票，但比把数据中心放到太空里合理得多。"

为什么值得记下：
这是 Burry 当天第二条直指"AI 资本支出方向"的推文。前一条是他的 Substack 系列《The Heretic's Guide to AI's Stars Part III: Tracepalooza & The Bezzle》，专门解构 NVIDIA 客户集中度与"循环融资"——他借用经济学家 J.K. Galbraith 的"bezzle"（账面已盗但尚未暴露的资产）概念，主张 NVIDIA 当前需求是被"训练与跑分阶段"扭曲的"鞭打效应"（bullwhip，需求小幅波动在供应链上层放大数倍）。
当天 Elon Musk 转发了 Walter Isaacson 在 CNBC 上的话——"听起来最离谱的就是在低地球轨道甚至月球上建数据中心"——Burry 这条推文几乎是直接接茬。

目前的不确定性：
- Burry 在投资上有 SOXX（半导体 ETF）的看跌期权头寸（到期 2027-01），存在持仓利益冲突，需要打折读
- "海底数据中心"在工程上有冷却优势，但跨大西洋线缆附近的实现成本与延迟优势尚无独立估算

链接：https://x.com/michaeljburry/status/2057943084353171906

---

### 启发 #4：nic carter（经 Marc Andreessen 转发）——"否认 AGI 已经存在，是一种'人类例外论'的精神托底"

发言人：@nic_carter（Castle Island Ventures 合伙人、长期写作密码学与货币），由 @pmarca（Marc Andreessen，a16z 联合创始人）转发并 "co-sign"
领域：AI 认识论
发布时间：约 9 小时前

他说了什么：
"如果你有一个朋友智商 130、能完美写生产代码、能写出高水准学术论文、能解出重大未解数学问题，你会说他是世界级天才。AI 已经具备这种'通用智能'，剩下的'代理能力、长期目标、具身性、自主行动'确实是人类有而 AI 没有的，但那已经不是 intelligence 本身。否认 AGI 已经到来，本质是一种'人类例外论'——心理上需要相信人类在一切维度都优越。"

为什么值得记下：
nic carter 不是 AI 圈核心，但他的论点把"jagged intelligence"（参差不齐的智能，指 AI 在不同任务上能力差异极大）这个术语从"反对 AGI"的盾，翻成了"承认 AGI"的矛。Andreessen 转出去并明确"co-sign"——这意味着 a16z 内部把"AGI 已到来"作为投资语境的工作假设，与多数 AI 实验室"AGI 5–10 年内"的口径有出入。

目前的不确定性：
- 这本质是定义之争而非事实之争，"AGI"本身没有统一标准
- carter 的论证回避了一个关键问题：jagged intelligence 在落地中会带来不同于人类的失败模式，"等同人类天才"的类比有缺陷

链接：https://x.com/pmarca/status/2057902018673684840

---

### 启发 #5：Andy Hall（经 pmarca 转发）——大学应训练学生"自己写 AI 评估"而非禁用 AI

发言人：@ahall_research（Andy Hall，斯坦福商学院教授、Hoover Institution 资深研究员）
领域：教育 / AI 治理
发布时间：约 19 小时前

他说了什么：
他的 Stanford GSB 学生从零代码经验起步，一学期内每人用 Claude Code 写出自己的 AI evals（评估，指对 AI 行为是否符合特定价值或标准的可重复测试）——涵盖巴西大选信息处理、缅甸语翻译、逻辑谜题、是否坚持效用主义伦理价值等。他主张：与其在大学禁用 AI，不如训练"一支会写自己评估的公民军队"，让民主社会有人能对 AI 系统问责。

为什么值得记下：
这是把"AI 治理"从政策辩论拉回到"教室里能做的事"的具体方案。Andreessen 转发并加一句"大学会越来越多禁用 AI——可以理解但是个错误"。这条与同日 Andrew Ng 长文（反对 Harvard 把 A 的比例硬限制在 20%）形成同一主题的二度共振：在 AI 时代，教育的角色应是"扩大成功"而非"分配稀缺"。

目前的不确定性：
- 学生作品的评估方法学质量、稳健性尚未独立审查
- "公民军队"愿景在投票、问责机制上仍未落地

链接：https://x.com/pmarca/status/2057735460060004732 ｜原文：https://freesystems.substack.com/p/an-army-of-citizens-building-evals

---

## 四、跨领域关联

> ⚠️ 这是 LLM 的关联推测，不是事实。每条都附反向思考。

### 关联线 A：AI 资本时代的"价格信号同步重置"

信号 1：微软取消 Claude Code 许可，token 计价让企业算出"不划算" — @ylecun
信号 2：Polsia 用 AI 跑出 1000 万 ARR，融资估值 2.5 亿，0 员工 — @Scobleizer
信号 3：Burry 在 Substack 解构 NVIDIA "bezzle"，主张训练阶段的客户需求扭曲被供应链放大 — @michaeljburry

潜在共同根源：
2024–2025 年的"AI 无限补贴 + 算力无限扩张"前提同时遭到三种不同方向的质疑——企业买家（微软）、新型卖家（Polsia 这类无员工公司）、二级市场空头（Burry）——三者从不同位置同时看到"价格信号失真"，把市场重新拉回到"单位经济学"。这与 2000 年互联网时期"光纤过剩 + 应用扩张"曾出现的回归节奏在机制上相似。

反向思考：
如果信号 1 错了（Hedgie 的内部消息被夸大、微软只是局部调整），信号 3 的 NVIDIA bezzle 也不一定崩——NVIDIA 营收增长可能由推理工作量而非训练工作量支撑，机制完全不同。这条关联线的"机制相似性"只在"训练阶段补贴退潮"这一窄路径上成立，不能扩展为"AI 估值整体见顶"。

### 关联线 B：教育与能力评估在 AI 时代的角色重写

信号 1：Andrew Ng 长文反对 Harvard 把 A 比例硬限制在 20% — @AndrewYNg
信号 2：Andy Hall 让斯坦福学生用 Claude Code 自写 AI 评估 — @pmarca 转发
信号 3：Kevin Kelly——"程序员不真正写代码"，新工作形态正在出现 — @kevin2kelly

潜在共同根源：
当 AI 把"做出某个产物"的边际成本降至接近零时，传统教育所信奉的"通过稀缺评分排序天赋"逻辑开始失效。Ng 反对"评分稀缺化"、Hall 把"评估"本身变成可学习的公民能力、Kelly 描述"做事但不做产物"的新工作形态——三条都指向"成功的定义在从'排他性产物'转向'与 AI 协作出的判断力'"。

反向思考：
如果 AI 的稳定性比预期慢（@jeremyphoward 当日转发的 Will McGugan：连 Anthropic 自己也修不掉 Claude Code 里几周未修的文本换行 bug——"差不多就行"的标准在被新一代默许），那么"评估能力"反而比"产物能力"更重要，"评分稀缺"不必然过时，Ng 的批评可能在 2–3 年后被部分撤回。

---

## 五、本期书单与访谈

### 新书 / Books

- **《Incorruptible: Why Good Companies Go Bad… and How Great Companies Stay Great》** — Eric Ries
  推荐者：作者本人 @ericries（《精益创业》/ The Lean Startup 作者、长期股票交易所 LTSE 创始人）；YC 总裁 @garrytan 在播客中长谈推荐
  推荐语境：5 月 21 日 ProductCon NY 现场签售爆满；5 月 22 日 YC Main Function 播客访谈上线
  核心论点：公司治理失败首先是结构问题，不是道德问题——当组织变大，"所有权、激励、章程、问责、决策机制"会悄悄重塑行为。书中专章讨论 Novo Nordisk 工业基金会（控制 Novo Nordisk 6000 亿美元市值的丹麦基金会模式）、Anthropic 的 LTBT（Long-Term Benefit Trust，长期受益人信托）治理结构、Costco 创始人 Sol Price 的"使命控制公司"。（来源：Simon & Schuster 官方页面，已 web 验证；播客章节目录来自 @ycombinator 推文原文）
  题材分类：商业 / 治理
  中文版状态：暂无中文版（截至 2026-05-23 经 web 搜索未检索到中信、湛庐等大社引进信息）
  Amazon/Goodreads 评分：尚未发售（出版日 2026-05-26）
  对什么人最有价值：A 轮以后想避免"使命漂移"的创始人；研究公司治理与基金会持股的投资人
  链接：https://www.simonandschuster.com/books/Incorruptible/Eric-Ries/9798893311860

- **《Founder's Fire: 1776 to the Age of Trump》** — Arthur Herman
  推荐者：@pmarca（Marc Andreessen）当日转发微软研究员 Ash Jogalekar（@curiouswavefn）的读书笔记
  推荐语境：把"founder mindset"（创办者心态）作为美国国民性的核心，从开国元勋到 Rockefeller、Carnegie、Gates、Jobs，强调"绝不把流程当成产物"，对 McNamara 在越南的"流程执念"做反面案例
  核心论点：Herman 担心"managerial class"（管理者阶层）的兴起正在压制"founder mindset"
  题材分类：商业 / 历史
  中文版状态：暂无中文版（截至 2026-05-23 经 web 搜索未见）
  对什么人最有价值：对美国创业精神历史感兴趣的读者；想分析创始人/管理者权力之争的投资人
  链接：https://www.amazon.com/Founders-Fire-1776-Age-Trump/dp/1546011293

### 访谈 / 播客 / Interviews & Podcasts

- **Main Function（YC 播客）EP — Eric Ries × Garry Tan**
  主持人：@garrytan（Y Combinator 总裁）
  发布日期：2026-05-22
  题材分类：商业 / 治理
  核心话题：为何创始人在公司成长后失去控制；shareholder primacy（股东至上）的来源（不是法律强制）；如何用 Anthropic、Novo Nordisk、Costco 的治理结构反向设计"使命控制公司"
  关键时间戳（精选）：
  - [05:12] — 股东至上主义解释
  - [22:26] — "直接成为 PBC"（Public Benefit Corporation，公益公司，可以在章程里平衡使命与利润的法人形式）
  - [34:47] — Novo Nordisk 与 6000 亿美元的工业基金会模式
  - [42:08] — VC 基金结构本身的治理问题
  - [45:03] — Anthropic 的治理故事
  收听链接：YC 推文 https://x.com/ycombinator/status/2057844527239676015
  为什么值得听：把"治理"从枯燥章程话题写成了具体的 founder 选择题，与 Incorruptible 一起听信息密度极高

- **The Knowledge Project — 投资专题集** — @shaneparrish（Shane Parrish，Farnam Street 创始人）"已重看 3 次每次都有新收获"
  发布日期：当日转发（原集为 2025 年初）
  题材分类：投资
  核心话题：失败作为信息、错误的复利、长期持有的反人性逻辑
  收听链接：YouTube https://www.youtube.com/watch?v=zyvuM3J9QqQ
  为什么值得听：Parrish 公开推荐"重复收听"的内容很少，三次重听本身是一个稀缺信号

### 重要长文 / Long-form Articles

- **The Prehistory of A.I. Slop** — Jill Lepore（The New Yorker，2026-05-25 期）
  发布日期：2026-05-22 上线网络版
  题材分类：科技 / 历史
  主题：作者用 1961 年《Life》杂志"机器即将超越人"标题作引，回顾"机器写作"自 20 世纪 30 年代起的百年焦虑史。文章注意到一个数字："2025 年秋天，互联网英文文章约一半由机器写成"（来源：The New Yorker，引用了未具名研究）
  为什么值得读：把当下"AI slop"（AI 灌水内容）的恐慌放回历史脉络——这种恐慌至少出现过四五轮
  阅读时长：约 25–30 分钟
  链接：https://www.newyorker.com/magazine/2026/05/25/the-prehistory-of-ai-slop

### 论文 / 报告 / Papers & Reports

- **The Alien Space of Science: 通过 LLM 识别认知空缺**（arXiv 2603.01092）
  推荐者：@hugo_larochelle（Mila 科学主任、前 Google DeepMind）转发作者 Alejandro H. Artiles
  核心：当前 LLM 在科研创意生成上偏向"该领域已经容易想到的方向"。论文把这种偏向形式化为"认知可得性"（cognitive availability），并用它定位被忽视但内在自洽的研究方向
  题材分类：科技 / 科研方法
  链接：https://x.com/hugo_larochelle/status/2057876503858155766

- **Heretic's Guide to AI's Stars Part III: Tracepalooza & The Bezzle**（Michael Burry Substack）
  推荐者：作者本人
  核心：NVIDIA 客户集中度 + 训练/跑分阶段需求扭曲 + 自定义供应承诺与数据中心融资的下游放大；Galbraith "bezzle" 框架
  题材分类：投资 / 金融
  注：作者近期已关闭 Scion 基金、转向 $379/年付费 Substack；本系列与他持有 SOXX 看跌期权的事实可同时阅读
  链接：https://open.substack.com/pub/michaeljburry/p/the-heretics-guide-to-ais-stars-part

---

## 六、TOP 3 深度挖掘

> 强制：3 条中至少 1 条来自「书单与访谈」区。本期 #2 满足该约束。

#### 深挖 #1：微软取消 Claude Code 许可

事实核实：
经 web_search 多源核实（aiweekly.co、biggo.com、36kr 国际版、TheTradable）：微软确实在 2025 年 12 月启动 Claude Code 内部试点（Experiences & Devices 部门），并已下达"2026 年 6 月 30 日前停用"指令，覆盖约 10 万名工程师。Uber CTO 内部备忘录"4 个月烧光全年 AI 预算"被同期媒体引述，但具体数字来自二级转引——未见 Uber 官方披露。"重度用户每月 2000 美元"是单点数据，未做行业横向核对。

思想溯源：
"补贴期 → 真实定价 → 需求收缩 → 再补贴"的循环并不新——Amazon Web Services 在 2010–2014 年也走过类似阶段。真正的新意是它发生在"算力买家本身就是云提供商"这一最不应该出问题的角色上——这是过去 SaaS 单位经济学讨论里没有的情况。最有力的反驳是：微软取消 Claude Code 同时是策略性动作（推自家 Copilot CLI），并非纯成本判断；并且 token 单价是工具层"卖方定价"，与"使用价值"不必然挂钩。

同行视角：
- Chamath Palihapitiya（@chamath）：问题不是 token 价格，是"agent 在缺乏上下文与监督时无限空转"——他主张通过 8090 这样的"软件工厂"管控（持仓利益冲突需标注）
- Yann LeCun（@ylecun）：训练阶段补贴退潮 → AI 实验室估值缺乏支撑
- Greg Brockman（@gdb）："the model alone is no longer the product"——OpenAI 一侧的对冲叙事：用工具层赎回模型层的利润空间
- 主要分歧点：是"模型本身定价不可持续"，还是"模型 + 工具层组合定价仍可持续"

对中国商业 / 科技读者的含义：
中国大模型同行（DeepSeek、阿里 Qwen、智谱）当下的低价路径，事实上等于在美国的镜像位置——同期 @jeremyphoward 转发了 DeepSeek-V4-Pro 永久降价公告。如果美国 AI labs 被迫从订阅价格上涨，中国低价策略会获得更明显的"性价比窗口"，但相应地，国内企业 AI 预算的"按用量付费"教育也应提前启动——否则一旦补贴退潮，会重演微软现场的尴尬。

延伸阅读：
- BigGo Finance 综合报道：https://finance.biggo.com/news/Xi3vTp4B-PfaobXfN2Wn
- AI Weekly：https://aiweekly.co/alerts/microsoft-drops-claude-code-after-budget-overrun

#### 深挖 #2：Eric Ries《Incorruptible》（书单 / 访谈区代表条目）

事实核实：
经 web_search 核实（Simon & Schuster 官页、Authors Equity、incorruptible.co、New Books Network）：图书 ISBN 9798893311860，2026 年 5 月 26 日由 Authors Equity 出版，432 页。作者 Eric Ries 是《精益创业》（The Lean Startup）作者，2019 年创办长期股票交易所（LTSE，Long-Term Stock Exchange，一家以"鼓励长期持有"为设计目标的美国证券交易所）。

思想溯源：
"治理失败是结构而非道德"这条主张并非完全原创——它在 Lynn Stout 的《The Shareholder Value Myth》（2012）、Colin Mayer 的《Prosperity》（2018）里都被论证过。但 Ries 的独特贡献是把 Lean Startup 的"假设—验证"框架延伸到了"治理本身可以被设计"——他用 Anthropic 的 LTBT 和 Novo Nordisk 工业基金会作为可复用案例，把"使命—利润"冲突从哲学问题降为可执行的章程问题。最有力的反驳来自股东价值学派：基金会持股结构在面对快速颠覆性技术变迁时反应慢，可能让公司错过转型窗口。

同行视角：
- Garry Tan（YC 总裁）：在访谈中将该书定位为"下一代创始人保护自己的必读"
- Lynn Stout（已故，Cornell 法学）：早在 2012 年就主张股东至上没有法律强制力——Ries 的实践派与这一学派形成方法论闭环
- 主要分歧点：Anthropic 的 LTBT 是否真的能在压力下守住章程？经 web_search 未找到关于 LTBT 在治理压力测试下表现的独立评估

对中国商业 / 科技读者的含义：
中国语境对"公司治理 = 合规"理解远多于"治理 = 设计"——但近年华为的工会持股、字节跳动的双层股权、海尔的人单合一，都是在做类似探索。本书对在科创板/港股 18A 上市后想保留"使命控制权"的创始人有直接参考价值。中文版尚未签约。

延伸阅读：
- 官方页：https://www.simonandschuster.com/books/Incorruptible/Eric-Ries/9798893311860
- New Books Network 访谈：https://newbooksnetwork.com/eric-ries-incorruptible-authors-equity-2026
- Long Now 演讲 "Incorruptible by Design"：https://longnow.org/talks/02026-ries/

#### 深挖 #3：Michael Burry 的 NVIDIA "bezzle" 框架

事实核实：
经 web_search 多源核实（Benzinga、24/7 Wall St.、Stocktwits、Elite Trader 讨论区）：Burry 2025 年 10–11 月起在新 Substack "Cassandra Unchained" 上发表《Heretic's Guide to AI's Stars》系列，首篇《Supply-Side Gluttony Recurrence》上线后 NVIDIA 曾发出 Wall Street 备忘录反驳。Burry 已关闭 Scion Asset Management、转 Substack 付费写作（$379/年）；2026 年 5 月通过 SOXX 看跌期权（到期 2027-01）建立显著空头仓位。Part III "Tracepalooza & The Bezzle" 5 月 22 日发布。

思想溯源：
"bezzle"（账面已盗但尚未暴露的资产）出自 J.K. Galbraith 1955 年《The Great Crash, 1929》，原指牛市掩盖的会计虚增。Burry 把它用到 AI 资本开支，思路有先驱：Jim Chanos 2024 年下半年也类似质疑 NVIDIA 客户集中度。"鞭打效应"（bullwhip）来自麻省理工 Hau Lee 1997 年的供应链理论。Burry 的新意是把会计学概念与供应链效应叠加，主张训练/跑分阶段的需求是一种"会被供应链放大的临时需求"。最有力的反驳：推理（inference）需求才是 NVIDIA 主要营收来源，与训练补贴退潮的传导路径不同。

同行视角：
- Cathie Wood（@CathieDWood，未在本 List 但同期持续公开看多 NVIDIA）：训练 → 推理的算力总盘还在扩张
- Yann LeCun（@ylecun，间接同向）：从 AI 单位经济学角度同步质疑
- NVIDIA 官方：曾分发备忘录给卖方分析师反驳 Burry（Stocktwits 报道）
- 主要分歧点：训练 vs 推理在 NVIDIA 营收结构中的真实比例——目前的 10-Q（季报）未公开拆分

对中国商业 / 科技读者的含义：
对持有美股科技 ADR 或科技基金的中国投资人，这是必须读的反向阅读材料。对国内云厂商（阿里、腾讯、火山）的 AI 资本开支决策，Burry 的"bullwhip"框架是个有用的检查清单：本期算力订单中有多少是为"跑分 + 训练展示"、多少是真实推理需求？

延伸阅读：
- Burry Substack：https://michaeljburry.substack.com/p/the-supply-side-gluttony-recurrence
- Benzinga 综述：https://www.benzinga.com/markets/tech/25/11/49036800/michael-burry-unchained-big-short-attacks-nvidia-on-substack

---

## 七、决策与思考清单

**今晚值得再看一遍的（30–60 分钟内可消化）**：
基于「主信号 #1」与「书单 - 访谈」—— 听 Y Combinator 的 Main Function 播客 Eric Ries × Garry Tan 一集（约 50 分钟），重点听 22:26（"成为 PBC"）和 45:03（Anthropic 治理）。

**今晚值得想一想的（适合通勤或临睡前回味）**：
基于「主信号 #1」与「单源 #2」—— 如果"模型本身已不是产品、token 计价让企业算账"两件事都成立，那么我所在的行业里，谁在拿"AI 工具"的差价利润？这个差价能维持多久？
基于「单源 #1」（Kevin Kelly）—— 我自己的工作里，哪些动作已经在 AI 之后"看起来还在做、其实不再做"？这种"虚位的动作"在简历上还能挂多久？

**本周值得追踪的**：
基于「主信号 #1」—— 建立一张"AI 单位经济学跟踪表"：每周记录主要模型的 token 单价 / 主要企业的 AI 月账单 / 公开披露的"AI ROI"案例。
基于「单源 #4」（nic carter / Andreessen）—— 关注 a16z 投资组合里是否开始出现"承认 AGI 已存在"的语言转向（这会影响他们对"通用智能 vs 垂直智能"创业的估值偏好）。

**今天值得重新审视的旧判断**：
本期为首次系统输出（无累积上期对照），此项暂缺。

---

## 八、本期发言人画像更新

| 账号 | 类型标签 | 题材覆盖 | 本期表现 | 建议优先级 |
|------|---------|---------|---------|-----------|
| @ylecun | 类型 1 领域内权威（Turing 奖）+ 类型 5 述评 | AI 单位经济学 / 美国政治 | 高效信号过滤器；选中 Hedgie 长帖把"AI 补贴时代结束"放上去 | **高** |
| @ericries | 类型 2 经营者（LTSE 创始人）+ 类型 6 跨界（书 + 交易所） | 公司治理 / 创业 | 新书 + YC 播客，构成本期最完整的"书单 + 访谈"组合 | **高** |
| @michaeljburry | 类型 3 投资人 | 投资 / AI 资本支出 | 同日 Substack 长文 + 直怼 SpaceX 海底/太空数据中心；稀缺度高 | **高** |
| @chamath | 类型 3 投资人 + 类型 2 经营者（8090 投资） | AI 工具 / 企业 IT | 对 Claude Code 事件做"agent 空转"框架补充；潜在利益冲突需标注 | 中 |
| @reidhoffman | 类型 2 经营者（LinkedIn）+ 类型 3 投资人 | 科技移民 / AI | 罕见就政策直接发声 | 中 |
| @AndrewYNg | 类型 1 领域内权威（教育 / 深度学习） | AI 教育 / 政策 | 长文反对 Harvard 控 A；与移民政策表态形成互补 | 中 |
| @pmarca | 类型 3 投资人 + 类型 6 跨界 | 创业 / 教育 / 科技史 | 当日大量转发（42 条），多为"Interesting" 一字评——信号过滤器价值高 | 中 |
| @kevin2kelly | 类型 1（科技长期思考者） | 工作未来 | 7 天内唯一原创推文，稀缺加分 | 中 |
| @gdb | 类型 2 经营者（OpenAI 总裁） | AI 产品策略 | "模型本身已不是产品"一句信号密度高 | 中 |
| @balajis | 类型 3 投资人 + 类型 6 跨界 | AI 社会效应 | 与 Tabarrok 的"AI 是海啸"形成对照，提"数字部族化" | 中 |
| @DanielaGabor | 类型 1 学者（宏观金融） | 央行 / 债市 | 一系列推文聚焦英国央行借贷成本与"Bailey premium"；信源稀缺 | 中 |
| @adam_tooze | 类型 1 学者（经济史） | 宏观 / 债市 | 转发 Daniela Gabor，作为信号过滤器 | 中 |
| @Scobleizer | 类型 5 述评号 | AI 创业 / 工具 | 选出 Polsia 案例 + 多个 AI 工具评测；本人推文常带广告色彩 | 低-中 |
| @NewYorker | 类型 5b 长文媒体（v1.2 后已收窄为商业/科技） | 文学 / 文化 | 当日 29 条，本简报仅采纳 Jill Lepore 的 AI slop 长文，其余文学/政治/艺术内容按 v1.2 不进入主区块 | 低-中 |

**"高"优先级上限 3 个，已用尽。**

---

## 九、沉默与意外信号

**本期值得注意的沉默**：
当天 List 中讨论度最高的"AI 单位经济学崩塌"话题（微软 Claude Code、Uber 烧光预算），AI 实验室一号位人物中：@sama（Sam Altman / OpenAI CEO，当日 1 条原创——"你最希望 AI 解决什么问题？"，纯互动）、@sundarpichai（Google CEO，当日 2 条，仅讨论 Antigravity 用量上限）、@demishassabis（DeepMind CEO，当日 4 条，均为 Gemini Omni 演示）、@jeremyphoward（fast.ai 联合创始人，当日 6 条，未直接评论），全部回避正面回应。

四个账号当日各自发推 ≥1 条，且话题完全围绕自家产品。集体回避 token 定价话题本身是一个信号——"补贴时代结束"在 AI 实验室一侧是不便公开承认的现实。

**本期意外信号**：
- @michaeljburry 罕见出来直接调侃 SpaceX："海底数据中心比天上数据中心合理得多"——Burry 通常聚焦半导体与房地产，正面挑战 Elon 的"太空数据中心"叙事是稀缺动作
- @adam_tooze 转发 @DanielaGabor 的英国央行批评——经济史学者转发宏观金融学者的"政策态度"，不是 Tooze 的常规题材

---

## 传播力素材（适合自媒体改写的高互动思想观点）

> 从被噪音过滤的金句/观点类推文中回捞，必须有独创性 + 商业/科技相关。

- **"the model alone is no longer the product"** — @gdb（Greg Brockman，OpenAI 总裁）· 👍6095 👁611K · engagement_rate 0.09%
  改写方向：商业号短评，"AI 商业化进入第二幕：从卖模型到卖工作流"
  点评：极短极锋利。它的前提假设是"AI 工作流（agent harness）的差价空间足够厚"，盲区是——如果"工作流"也成为标准品（Cursor、Copilot 都在做），这句话半年内可能被反噬为"工具也不是产品"。

- **"It can't be the case that AI is only good enough if we lower our standards."** — Will McGugan（Textualize 创始人）经 @jeremyphoward 转发 · 👍177 👁32K · engagement_rate 0.07%
  改写方向：科技评论，"我们正在用 AI 当借口降低软件质量标准吗"
  点评：以 Anthropic Claude Code 几周未修文本换行 bug 起手，把"AI 时代'差不多就行'"问题具体化。前提假设是"高标准必然带来高用户价值"——但在 winner-takes-most 的工具市场，"够用 + 速度"经常击败"完美 + 慢"，盲区在这里。

- **"the median American took zero flights last year"** — @paulg（Paul Graham 转发 @AlecStapp）· 👍55749 👁2.45M · engagement_rate 0.11%
  改写方向：经济直觉校准，"那些'人人都在飞'的市场叙事，可能服务的是少数高频用户"
  点评：本期 List 收藏量最高的"反直觉数据"。前提假设是 Alec Stapp 引用的数据为真——但"零航班"统计口径（是否含商务出差报销、是否含家庭中其他成员代订）值得追问。盲区：用来推论"国内消费市场结构"时，需要谨慎换算到中国语境。

- **"How to Convert Between Wealth and Income Tax"** — @paulg（Paul Graham，自己撰写）· 👍293 👁31K · engagement_rate 0.69%
  改写方向：财经长文/解读，"财富税与所得税的等价换算公式"
  点评：当天 List 中 engagement_rate 最高的原创长文之一。Graham 把财富税转换为"等价的所得税倍数"。前提假设是资产组合的预期回报率稳定——在 AI 资本周期的高波动期，这一假设需要打折。

- **"AI accelerates digital tribalism"** — @balajis（Balaji Srinivasan，Network State 作者）· 👍259 👁50K · engagement_rate 0.24%
  改写方向：社科评论，"AI 不止创造市场，也在破坏市场——尤其是信任市场"
  点评：把"AI 是经济海啸"和"AI 是制度风险"两条叙事合并。前提假设是"信任成本可以量化为交易成本"——这与 Coase 的交易成本框架兼容，但盲区在于：信任的崩塌往往是非线性的，量化模型可能严重低估尾部风险。

- **"如果你有一个智商 130、能完美写生产代码 [...] 的朋友，你会说他是世界级天才——AI 已经是 AGI 了。"** — @nic_carter 经 @pmarca 转发 · 👍1024 👁153K · engagement_rate 0.14%
  改写方向：AI 哲学评论，"我们为什么不愿承认 AGI 已经到来"
  点评：把"AGI 标准模糊"这个问题从技术争论变成心理学问题（"人类例外论"）。前提是"智能"可以与"代理性、长期目标"切割——这恰恰是反对意见的核心，论证回避了关键反驳。但作为传播文本极有冲击力。

---

## 十、本期信号评估

**信号 / 噪音比**：
本期 24 小时窗口 278 条推文，通过铁律六质量门槛约 28 条；进入主区块 3 条；进入单源高启发 5 条；进入书单/访谈 6 条；进入附录 5 条；剩余约 87% 为低价值（@elonmusk 个人 55 条中绝大多数为 Starship V3 试飞实况、欧冠夺冠转发、Grok 工具迭代、政治站队；@NewYorker 当日 29 条仅 1 条进入；@KirkusReviews 7 条主要为通俗小说推荐）。

**信息密度**：高
单日同时出现"微软取消 Claude Code + Burry NVIDIA bezzle + Eric Ries Incorruptible 出版 + 美国绿卡政策 + Polsia 单人公司融资"五条独立但相关的强信号——本期信噪比明显高于普通工作日。

**主导主题**：AI 单位经济学转折点——同一现象在企业买家、二级市场空头、新型卖家、政策面同时显现。

**未浮现但值得追踪**：
- 中国 AI 公司对"按 token 收费"模式的实际跟进路径（DeepSeek 永久降价的反向意义）（推测）
- Anthropic 是否对微软取消许可做正面回应（截至窗口结束未见）（推测）

**本期信源**：@elonmusk @pmarca @ylecun @ericries @michaeljburry @chamath @reidhoffman @AndrewYNg @gdb @kevin2kelly @Scobleizer @sapinker @balajis @DanielaGabor @adam_tooze @rcbregman @hugo_larochelle @NandoDF @jeremyphoward @fchollet @sundarpichai @demishassabis @sama @paulg @david_perell @tylercowen @TimHarford @shaneparrish @saylor @bfeld @tferriss @patrick_oshag @nntaleb @BrankoMilan @AndrewYang @BernieSanders @SenSanders @KamalaHarris @HillaryClinton @SpeakerPelosi @JamesClear @goodreads @KirkusReviews @NewYorker @Cmdr_Hadfield @jack @dhh @naval（共 48 位）

---

## 附录 A · 行业内幕（可选阅读，约 480 字）

- **Cursor Composer 2.5 性能/价格对比**：经 Artificial Analysis 评测，在 Coding Agent Index benchmark 中，Composer 2.5 比 Claude Opus 4.7（Claude Code 中等推理档）便宜 3–18 倍、比 GPT-5.5（Codex 中等档）便宜 5–32 倍；同任务 token 用量 1.6M vs 同行最高 5.7M；平均完成任务时间约 9 分钟，Composer 2.5 Fast 约 7 分钟（@elonmusk 转发 @ArtificialAnlys）。这与主信号 #1 直接相关：工具层的真实差价主要来自"用更少 token 完成同等任务"。

- **OpenAI Codex Appshots + Remote Computer Use**：Codex iOS 新增"双 ⌘ 键"快捷键，把当前桌面应用的"屏内 + 屏外"上下文（如 Google Docs 中已滚动出可视区域的文本）打包发给 Codex；同时上线 Remote Computer Use——锁屏状态下手机可远程操作家中 Mac 的所有应用（@AriX 推文，@gdb 转发评论"the model alone is no longer the product"）。

- **xAI Grok Build / Grok Imagine Agent Mode**：xAI 同日发布 grok inspect 命令（查看配置）、新连接器（Vercel/Canva/Gamma/S&P Global）、网站重设计。Grok Imagine 在 iOS 上引入 Agent Mode，可在不同生成间保持角色一致性。@elonmusk 当日累计转发约 30 条相关内容，构成本期"硬推"主题。

- **DeepSeek V4 Pro 永久降价**：@jeremyphoward 转发 @deepseek_ai 永久折扣公告——这是中国大模型对美国 token 涨价潮的反向运动。👁144 万。

- **Gated DeltaNet-2 论文**：NVIDIA 团队（@ahatamiz1，与 @YejinChoinka、@jankautz 合作）发布。把线性注意力（linear attention，把传统注意力的 O(n²) 复杂度压到 O(n)）的"擦除门"与"写入门"在通道维度上解耦：擦除门 b_t 决定读写哪些键侧坐标、写入门 w_t 决定提交哪些值侧坐标。在 1.3B 参数 + 100B token FineWeb-Edu 上，长上下文 RULER 检索表现尤其好（S-NIAH-3 从 63 → 90，多键针检索 28 → 38）。@jeremyphoward 转发评论：Gated DeltaNet-2 几乎等同于 RWKV-7 的 DPLR 递推，"房间里的大象没人提"（@BlinkDL_AI 转发）。

- **Andreessen 的 "AI 知识爬虫" 转发**：a16z 创始人转发 @glukianoff 的 Replication Radar 项目，主张用 AI 大规模交叉验证社科 / 人文领域"已被引用但从未被检验"的论点。这是 @ahall_research 的 evals 教学路径的"成人版"。

---

---

## 简报末尾固定声明

本简报的所有判断、关联推测均基于公开推文与公开网络信息。所有具体数字均标注来源；无法多源验证的内容已显性隔离至「单源高启发」区块或标注 [未经多源验证]。读者应理解：思想类信号的"准确性"低于事实类新闻——这份简报的价值不是"告诉你真相"，而是"告诉你此刻在商业与科技领域最值得思考的方向"。
