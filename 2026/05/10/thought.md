# 思想发现简报 | 2026-05-10

> 数据窗口：2026-05-09 10:13 — 2026-05-10 10:13（北京时间，过去 24 小时）
> 处理推文：195 条 | 经过噪音过滤后剩余：约 65 条 | 通过题材范围（商业 / 科技）筛选：约 28 条 | 模板版本：v1.2

---

## 一、今日要点

凌晨一点四十六分，François Chollet（深度学习开源框架 Keras 的作者、Google 高级研究员，长期质疑大语言模型"是不是真的在思考"的少数几位严肃声音之一）在他的账号上抛出一句话："Agentic coding is a form of machine learning."（智能体编程是机器学习的一种形态。）四个多小时后他给出更尖锐的判断：生成的代码最好被当作黑箱产物，应当像评估任何 ML 模型那样以经验数据评估，而不是像审一段人写的代码那样去 review。

几乎同一时间，Sam Altman（OpenAI CEO）发了一条家庭式短文：起一堆 codex 任务，带孩子去阳光下跑一圈，回来午睡时它们都已完成。OpenAI 总裁 Greg Brockman 转出一份用户截图：codex 自己抓 Drive 票据、Gmail 邮件、用 Chrome 插件填表，把整个月的报销端到端处理完。把这几条放在一起读，今天 List 里四条原本互不相关的发言（再加上沃顿商学院的 Ethan Mollick 关于"模型仍在用 2022 年的脑子说话"的判断、以及 fchollet 自己的另一句"AI 把自主性的复利效应放大了——低自主性的用户更被动，高自主性的用户更有杠杆"）共同指向一个问题：当生成代码不再像写代码、而像训练模型，软件公司里"工程师"这个角色就不再是手艺人，而是评估器。这件事三个月前没人会这样说；今天有四个独立来源在同一窗口里这样说。

**Bottom line in English:** When code generation starts behaving like model training, "engineer" stops being a craftsman role and becomes an evaluator role — and four independent voices on the List converged on this view today.

---

## 二、主信号（多源验证）

### 信号 #1：智能体编程已经不是软件工程——它是机器学习

主信源：@fchollet（类型 1 领域内权威：Keras 框架作者、Google 高级研究员、ARC 抽象推理数据集发起人，长年公开质疑 LLM 推理能力的最严谨声音之一）· 约 8 小时前
佐证：@sama（OpenAI CEO，同窗口） · @gdb（OpenAI 总裁，同窗口） · @emollick（沃顿商学院教授，同窗口）
题材分类：科技 / AI / 软件工程方法论

故事 / 场景：
今天凌晨一点四十六分，fchollet 先发了一条短句："自主性本来就是会自我复利的，AI 只是把这个效应放大了。"四小时后他给出更尖锐的判断：智能体（即代表用户自主执行任务的 AI 代理）编程本质上是一种机器学习——你设定优化目标和约束（即代码规范和测试），让 agent 反复迭代直到达成目标，最后产出的代码是一个"黑箱产物"，应当用经验数据评估，而不是逐行 code review。同一窗口里，Sam Altman 描述自己周末"开了一堆 codex 任务、带孩子去阳光下跑一圈、回来发现都做完了"；Greg Brockman 转出一份截图：codex 用 Drive 抓票据、Gmail 抓邮件、Chrome 插件填表，把整个月的报销自己处理完。

为什么值得思考：
过去主流共识是"AI 辅助编码 ≈ 更聪明的 IDE"——它仍然是程序员的工具。fchollet 的判断挑战了这一共识的核心：如果生成代码已经是黑箱，那"软件工程"的最佳实践（结对评审、可读性、规范模式）大部分不再适用，应当被替换为 ML 的实践（可观测性、评估集、回归测试覆盖率、漂移监控，即模型表现随时间偏离基线的监测）。Mollick 在同一天补了一句旁证："任何在 2022-2023 年公开发表的关于 AI 的内容，今天仍在影响当前模型的行为；从那之后，开放互联网对训练已经不再是关键变量，但模型仍以'2022 年的脑子'说话"——也就是说，同一个 LLM 既是写代码的工具，也是被一段过时世界观所雕刻的产物。这是商业意义上的"工艺断裂"信号：如果 fchollet 是对的，那么靠"工程师人头"做项目预算、做生产力衡量的整套体系都要重写。

关键引文（中英并存）：
> EN: "Agentic coding is a form of machine learning. Generated code is best treated as a blackbox artifact whose behavior and generalization should be managed via empirical evaluation, like with any ML model."
>
> 中：智能体编程是机器学习的一种形态。生成的代码最好被当作黑箱产物，其行为与泛化应当通过经验评估来管理，就像对待任何 ML 模型一样。

链接：
- https://x.com/fchollet/status/（2026-05-10 06:04 BJT 原推）
- https://x.com/fchollet/status/（同日 01:46 BJT "agency self-compounding"）
- https://x.com/sama/status/2053191344999604409
- https://x.com/gdb/status/（同日 05:11 BJT codex 报销转推）

---

### 信号 #2：AI 能力的"地理时差"——四级阶梯被画出来了

主信源：@eladgil（类型 3 投资人：Elad Gil，曾任 Twitter / Color 高管，现为活跃 AI 早期投资人，著有 *High Growth Handbook*）· 约 12 小时前
佐证：@pmarca（Marc Andreessen，a16z 创始合伙人 · 类型 3 + 6） · @rileybrown · @tanayj
题材分类：科技 / AI / 风险投资

故事 / 场景：
昨晚（北京时间 5月10日凌晨 5 点 55 分前后），Elad Gil 发了一段后来被 Marc Andreessen "Co-sign（联署）"的判断：用内部模型的前沿 AI 实验室员工，比硅谷创业公司工程师领先 3-4 个月；硅谷的创始人 / 工程师比纽约的领先 3-6 个月；纽约比世界其他地方领先 6-12 个月。pmarca 紧接着补了一句："你还可以把这个阶梯往后再延伸几节。"半小时后另一位创始人 Riley Brown 加进来："只要你正确地用好 X，就可以抵消掉物理距离——X.com 已经比硅谷创始人圈子提前两个月。"

为什么值得思考：
这条信号挑战的是中文 AI 圈一个普遍假设："只要拿到顶尖开源模型 + 部分英文社区资源，与硅谷的差距就可以被弥合。"Gil 的判断把"差距"明确量化：差距不是模型本身，而是经验积累、内部工具链和场景反馈的时间差。pmarca 在另一窗口里抛出"Harness Hyper War"概念——OpenAI / Anthropic 通过 ChatGPT、Codex 等应用每天产出"数万亿 token（即模型处理的最小语言单位）"的真实使用轨迹，这是任何上层应用层公司无法获得的训练 / 评测原料。两条信号在机制上互为骨架。

关键引文：
> EN: "People at major AI labs (using internal models) 3-4 months ahead of startup silicon valley engineers. SV founders/eng 3-6 months ahead of NY. NY founders/eng 6-12 months ahead of rest of world."
>
> 中：在主要 AI 实验室使用内部模型的人比硅谷创业公司工程师领先 3-4 个月；硅谷创始人 / 工程师比纽约领先 3-6 个月；纽约比世界其他地方领先 6-12 个月。

链接：
- https://x.com/eladgil/status/（原推，2026-05-10 05:55 BJT）
- https://x.com/pmarca/status/（同日 05:55 / 06:55 联署与扩展）

---

### 信号 #3：Palantir 被 AI 实验室"反向蚕食"——Burry 把这个判断挑明

主信源：@michaeljburry（类型 3 投资人：Michael Burry，《大空头》原型，Scion Asset Management 创始人，对科技股估值长期持空头立场）· 约 1 小时前
佐证：《华尔街日报》同日报道 · @WSJbusiness
题材分类：投资 / 科技 / AI 商业模式

故事 / 场景：
今天上午（北京时间 09:33），Burry 转出《华尔街日报》一篇 5月9日刊出的报道，加了一句"Credit, where credit is due（该给的肯定要给）"。报道要点：Palantir CEO Alex Karp 这段时间在公开场合反复嘲讽 AI 实验室的产物是"slop（垃圾）"——但据 AI 公司高管、Palantir 现任和前任员工以及分析师的访谈，Palantir 自己正面临被 AI 模型边缘化的真实风险，因为 OpenAI / Anthropic 等可以直接给到曾被认为是 Palantir 护城河的"政府 / 军事数据集成"工作。

为什么值得思考：
过去半年的主流叙事是"Palantir 是国防 AI 龙头，与 LLM 厂商互补"。Burry 这条信号挑战了一个并不细的细节但是关键的细节：当 Karp 在公开嘲讽 AI 实验室时，他可能在防守，不是在进攻。这与上一条 pmarca 的"Harness Hyper War"形成机制对照——如果应用层的护城河来自 AI 实验室还没接到的真实使用轨迹，那么一旦实验室进入，应用层 SaaS 估值就要重拉。

关键引文：
> EN: "As Palantir CEO Alex Karp derides AI 'slop,' investors and some employees see a real threat of the company ceding business to artificial-intelligence models."
>
> 中：当 Palantir CEO Alex Karp 公开嘲讽 AI 是"垃圾"时，投资者与一些员工却看到一个真实的威胁——公司正在把业务让渡给 AI 模型。

链接：
- https://www.wsj.com/tech/ai/for-palantir-ai-is-a-product-a-punching-bagand-a-problem-a4cfea77
- https://x.com/michaeljburry/status/（2026-05-10 09:33 BJT）

---

## 三、单源高启发信号

> ⚠️ 以下信号仅有一个权威来源，未经多方独立验证。但发言人在该领域有明确商业 / 科技权威性，内容具有思想价值。请读者自行判断。

### 启发 #1：Tim Gowers 说他的最新论文里"一章 PhD 级结果"是 AI 在两小时内做出的

发言人：@wtgowers（Sir Timothy Gowers，剑桥大学数学家，1998 年菲尔兹奖得主，理论计算机科学—组合数学交叉领域权威，Polymath 协作研究项目发起人）
领域：数学 / AI 推理
发布时间：约 21 小时前（pmarca 转出于北京时间 5月9日 13:13 / 13:14）

他说了什么：
> EN: "The model proved a result that in my assessment would have made a perfectly reasonable chapter in a PhD thesis. It did this in a total of a couple of hours, with a few prompts from me that contained no mathematical input whatsoever."
>
> 中：模型证明了一个结果。以我的判断，它足以构成一份博士论文中合格的一章。整个过程花了几小时，而我给的提示（即给 AI 的指令模板）里完全没有任何数学内容。

并在另一条中说："如果 AI 数学的进展速度保持下去——这是我预期会发生的——我们很快就会面对一场危机；数学系出于对学生的责任，应当紧急做准备。"

为什么值得记下：
这是 Gowers 本人的领域内观察，不是新闻稿。Gowers 因他在 Polymath 项目中的清醒立场，长期被视为对 AI 在数学中作用最严肃的评估者之一。"PhD 论文中合格的一章"是一个具体可验证的标准，不是空话。

目前的不确定性：
- 该论文的标题、所用模型名称、所证结果的具体陈述均未在推文中给出
- 同等量级的同行（如 Terence Tao 陶哲轩）尚未对该具体说法公开回应
- pmarca 的转发只是评论性的"Cc the AI Cope brigade"，不构成第二独立来源

链接：原推 https://x.com/wtgowers/status/，pmarca 转推 https://x.com/pmarca/status/

---

### 启发 #2：Ethan Mollick——当前模型仍在用"2022 年的脑子"说话

发言人：@emollick（沃顿商学院 Ethan Mollick 教授，《Co-Intelligence》作者，业内最常被引用的 AI 商业应用观察者之一）
领域：AI / 知识管理
发布时间：约 2 小时前

他说了什么：
"我怀疑在 2022-2023 年那段时间，凡是当时被广泛传播的关于 AI 的公开内容，今天仍在影响当前模型的行为。从那之后，开放互联网对训练已经不再是关键变量，但模型在很多方面仍然带着 2022 年的脑子。"

为什么值得记下：
这是 Mollick 的领域内直觉观察，没有第二来源做佐证。但若属实，对内容创作者意味着一个非显然的判断："2022-2023 年 AI 大爆发期间被高度传播的判断"对今日模型仍有不成比例的影响——这暗示一种"训练时间锁定"的现象，可被用作模型行为分析的工具。

目前的不确定性：
- 没有引用具体训练数据集来证实
- "2022-brained" 是直觉描述，不是定量结论

链接：https://x.com/emollick/status/

---

### 启发 #3：Saylor——把 BTC 储备从"债务支撑"重写成"优先股工程"

发言人：@saylor（Michael Saylor，Strategy / 原 MicroStrategy 创始人，企业级比特币储备方案的设计与代言人）
领域：投资 / 比特币 / 公司财务结构
发布时间：约 7 小时前

他说了什么：
> EN: "$STRC is credit engineered for income, stability, liquidity, and principal protection. It is backed by our BTC and USD assets and supported by active treasury operations. We structured it as preferred equity rather than debt to make it more scalable, durable, global, and useful."
>
> 中：$STRC 是一种为收益、稳定、流动性和本金保护工程化设计的信用产品，由我们的 BTC 与 USD 资产支撑，并通过主动财库操作维护。我们把它设计为优先股而非债，使其更易扩展、更耐久、更国际化、更有用。

并补充："BPS（Bitcoin Per Share，每股比特币）是 EPS（Earnings Per Share，每股盈利）在比特币本位下的对应物——MSTR 现在的真北。"

为什么值得记下：
Saylor 本人提出"BPS = EPS on the Bitcoin Standard"是一种新会计语言尝试。把 STRC 工程化为优先股而非债的具体动机也很值得思考——以加密资产为主要支撑的优先股在公司财务史上罕见。

目前的不确定性：
- 单一来源是 Strategy 自己（@saylor 与 @phongle）
- "$STRC 募资 5.58B USD、+189% 增长、23 个连续月度股息共付出 $693M"（来源：@phongle 转发 Strategy Q1 文件，[未经多源验证]）
- "9.4% YTD BTC Yield、$5B BTC Gain" 同样出自 Strategy 自身披露

链接：https://x.com/saylor/status/2053190051983503425

---

### 启发 #4：pmarca——"Harness Hyper War"，护城河不在模型，在部署轨迹

发言人：@pmarca（Marc Andreessen，a16z 创始合伙人，互联网早期 Mosaic / Netscape 创始人）
领域：AI / 平台战略
发布时间：约 21 小时前

他说了什么：
"这种说法完全忽略了 OAI 和 Ant 在所有垂直领域有真实部署，每天产出数万亿 token 的轨迹数据用于评估和训练，覆盖从'研究员级别'到'普通用户级别'到'极罕见'用例。这就是 Harness Hyper War（用户行为—模型迭代闭环之战）。"

为什么值得记下：
这是 Andreessen 的反共识判断：能力差距不是参数大小或训练算力的差距，而是已部署模型每天接收到的、真实用户—任务的反馈轨迹的差距。这条与主信号 #2（AI 能力地理时差）和 #3（Palantir 被反向蚕食）在机制上同构。

目前的不确定性：
- "数万亿 token 的轨迹数据"未在 OpenAI / Anthropic 公开披露中出现
- 仅为 Andreessen 个人的产业判断

链接：https://x.com/pmarca/status/

---

## 四、跨领域关联

> ⚠️ 这是 LLM 的关联推测，不是事实。每条都给反向思考。

### 关联线 A：从"工程"到"评估"——三个独立来源指向同一种工艺转移

信号 1：fchollet 称智能体编程本质是 ML（科技 / AI）— @fchollet
信号 2：Gowers 称 AI 在数学中接近 PhD 级产出（科技 / AI）— @wtgowers via @pmarca
信号 3：Burry 转 WSJ 称 Palantir 担忧被 AI 实验室代替（投资 / 科技）— @michaeljburry

潜在共同根源：
这三条信号背后可能共享同一个变化：**"研究 / 工程 / 服务交付"在过去五十年靠人力雕琢的部分正在被压缩，剩下的是"问题描述（prompt）+ 评估 / 验证（eval）"两端。** fchollet 把这套变化命名为 ML 实践、Gowers 把它命名为数学家育人责任的危机、Burry 把它命名为 Palantir 估值风险——同一个机制在三个层级显化。

反向思考（机制相似性测试）：
如果"评估端的核心能力是稀缺且不可被自动化的"这个隐含假设错了，那么 fchollet 的"工程师→评估器"判断会同时崩塌——因为评估端也会被 AI agents 接管。Gowers 的"数学系应当作准备"也会同时无效——因为数学系本身的评估职能会失去意义。Burry 的判断也会变弱。换句话说：这三条要么都对，要么都错。这是一个值得继续观察的"同存同灭"信号。

---

### 关联线 B：知识资本的"地理时差"叠加"轨迹数据壁垒"

信号 1：eladgil 描述的 AI 能力地理时差（科技 / AI）— @eladgil + @pmarca
信号 2：pmarca 提出的 "Harness Hyper War"（科技 / AI 平台经济）— @pmarca
信号 3：emollick 的 "2022-brained models" 观察（科技 / AI）— @emollick

潜在共同根源：
**前沿能力的稀缺资源已经从"模型权重"切换到"模型权重 + 部署轨迹 + 工具链知识"的复合资本。** 地理时差是这个复合资本可观测的外显，Harness Hyper War 是它的产业逻辑，"2022-brained" 提醒我们这个复合资本里还包含了"早期被广泛讨论的内容产生的训练痕迹"——三者从三个角度刻画同一个新型壁垒。

反向思考（机制相似性测试）：
如果"部署轨迹是壁垒"这个机制错了——比如开源社区通过合成数据 / 蒸馏可以低成本复现出同等效果——那么地理时差也会自然消解，"2022-brained" 同样会被新一轮训练覆盖掉。这条关联线对中文读者的实际意义在第六节里展开。

---

## 五、本期书单与访谈

### 新书 / Books

- **《New Rules for the New Economy》（1998 年版）** — Kevin Kelly
  推荐者：@kevin2kelly（Kelly 本人，Wired 杂志创始执行主编、《必然 The Inevitable》作者、技术哲学领域长期出版人）
  推荐语境：5月10日，Kelly 在自己的账号上贴出 1998 年这本书的一个章节，并附"Full book can be read at..."的全文开放阅读地址
  核心论点：在网络经济中，价值产生于充裕（abundance）而非稀缺；网络效应是新的资本品；标准从中央设计转向自下而上的协同
  题材分类：科技 / 互联网 / 平台经济
  中文版状态：曾有早期中译《新经济，新规则》[未经多源验证]
  对什么人最有价值：希望理解今日 AI 平台争论与 1990 年代互联网平台争论之间共性的读者
  链接：https://kk.org/newrules/category/this_new_economy/

### 访谈 / 播客 / Interviews & Podcasts

- **Saylor on $BTC, $STRC, $MSTR — Consensus 2026**
  嘉宾：Michael Saylor（Strategy / MicroStrategy 创始人）
  主持人：@TheBonnieChang、@davidlin_TV
  发布日期：2026-05-10（Saylor 在自己账号公开）
  题材分类：投资 / 公司财务结构 / 比特币
  核心话题：Strategy 的"BTC 出售争议"、"永远不卖 BTC"哲学的具体含义、BPS（每股比特币）作为真北、用 STRC 做出比单纯持有更复杂的资本结构
  关键时间戳（精选）：
  - 0:00 — Strategy 的比特币出售争议
  - 3:12 — "Never sell your Bitcoin" 这句话的具体含义
  - 8:04 — 用比特币流动性与市场套利
  - 11:14 — 回应"庞氏"指控
  - 17:58 — 比特币、宏观风险、美联储政策的关系
  - 19:43 — 比特币作为数字资本（Saylor 推文中给出的目录在此处节略）
  收听链接：见 Saylor 5月10日 05:28 BJT 推文中的视频附件
  为什么值得听：这是 BPS / STRC / 优先股替代债结构这套话语在公开访谈中最完整的一次自述

### 重要长文 / Long-form Articles

- **"For Palantir, AI Is a Product, a Punching Bag — and a Problem"** — *The Wall Street Journal*（2026-05-09）
  发布日期：2026-05-09
  题材分类：科技 / 投资 / AI 商业模式
  主题：报道 Palantir CEO Alex Karp 公开嘲讽 AI 实验室的"slop"，但 AI 实验室高管 / Palantir 内部员工 / 分析师都看到 Palantir 主营业务正被 AI 模型边缘化
  为什么值得读：本期"主信号 #3"的完整一手依据
  链接：https://www.wsj.com/tech/ai/for-palantir-ai-is-a-product-a-punching-bagand-a-problem-a4cfea77

- **"The Immense Power of the New Plutocracy"** — *El País English*（2026-05-09）
  发布日期：2026-05-09
  题材分类：经济 / 政治经济学
  主题：分析 Musk / Bezos / Zuckerberg 等亿万富豪如何塑造现代民主与日常生活——典型的现代财富集中政治经济学叙事
  为什么值得读：本日 List 中 Branko Milanovic（CUNY 经济学家、《Capitalism, Alone》《全球不平等》作者）转发并稍作背书，可作为"超大富豪—政治权力"题材的经济学骨架
  链接：https://english.elpais.com/economy-and-business/2026-05-09/the-immense-power-of-the-new-plutocracy-how-billionaires-like-musk-bezos-and-zuckerberg-shape-our-lives-and-our-democracies.html

### 论文 / 报告 / Papers & Reports

- **"Adam Smith and the Role of the Towns in Feudal Europe"** — Mark Koyama（2026，forthcoming in *Public Choice*）
  推荐者：@BrankoMilan 转发 @MarkKoyama（乔治梅森大学经济史学家，《How the World Became Rich》作者之一）
  推荐语境：为纪念《国富论》250 周年，乔治梅森大学举办"Wealth of Nations 250: The Long Arc of Smithian Economics"会议时的会议论文
  核心论点：Smith 关于中世纪欧洲"城镇崛起—封建体制松动"的判断，今天在新经济史与制度经济学的视角下仍然成立。具体细节待原文核实
  题材分类：经济史 / 商业史
  对什么人最有价值：对"今天的中国 / 印度城镇化与 18 世纪欧洲城镇崛起的可比性"感兴趣的读者
  链接：见 BrankoMilan 5月10日 07:17 BJT 转推

- **"Il y a un large consensus sur l'économie chinoise, mais il est erroné"**（《关于中国经济存在广泛共识，但它是错的》）— Arvind Subramanian（2026，原文经法语博客转译）
  推荐者：@BrankoMilan（转发 @martin_anota 法译版）
  推荐语境：Subramanian（曾任印度首席经济顾问、彼得森国际经济研究所高级研究员）撰写的中国经济判断，挑战"中国增长见顶 / 内需结构性疲软是定论"的主流叙事
  核心论点：当前主流"中国经济共识"过度悲观；Subramanian 指出几个被忽略的经济与制度变量。详细论点待核实
  题材分类：经济 / 中国研究
  链接：https://annotationsbis.blogspot.com/2026/05/il-y-a-un-large-consensus-sur-leconomie-chinoise.html

### 课程 / Courses

本期无明显商业 / 科技课程信号。

---

## 六、TOP 3 深度挖掘

> v1.2 强制约束：所有 TOP 3 必须为商业 / 科技题材；至少 1 条来自「书单与访谈」区。

### 深挖 #1：智能体编程已经不是软件工程——它是机器学习

事实核实：
fchollet 当日两条推文的时间戳与原文一致；他作为 Keras 框架作者、Google 高级研究员的身份可在 keras.io 与 Google 学术页面验证。Sam Altman 与 Greg Brockman 的两条 codex 自述在他们各自账号同窗口可查。"codex 全链路报销"具体功能由原推用户和 gdb 转推背书，[未经多源验证]。

思想溯源：
"软件工程是一种工艺，不是科学"这个判断早在 1986 年 David Parnas、1994 年 Fred Brooks "No Silver Bullet" 中就被讨论过；将"代码生成"看作搜索而非编辑可追溯到 1980 年代的程序合成（program synthesis）研究——MIT 的 Solar-Lezama 在 2008 年的 Sketch 系统是当代代表。fchollet 的新意在于把"agentic coding"明确等同于"机器学习的训练循环"，而不只是工程范式之一。最有力的反驳来自经验：今日大量 LLM 生成的代码仍由人复审、修改、入库——它没真的像 ML 模型那样被丢进 prod 接受漂移监控。

同行视角：
- DHH（Basecamp / Ruby on Rails 作者，类型 2）今日并未直接评论本话题，但他过去半年公开的态度更接近"人写代码仍然不可被替代"
- Andrej Karpathy（前 OpenAI / Tesla AI 首席）近一年公开多次说"prompt 即新代码"，与 fchollet 立场互补但侧重不同——他强调指令侧的工艺，fchollet 强调输出侧的黑箱化
- 主要分歧点：生成代码是否需要 review（fchollet：不需要——按 ML 评估即可；Karpathy：需要——但 review 工作本身也会被 AI 接管）

对中国商业 / 科技读者的含义：
中国 SaaS 与互联网公司在过去十年的人头预算 / 项目预算 / OKR 体系大量基于"工程师工时"。如果 fchollet 是对的，那么 IT 与产研 OKR 在 2026—2027 年需要重写为"评估覆盖率 / 漂移检测率 / 故障重现率"等 ML 指标。CTO / VP Engineering 是受冲击最早的角色。

延伸阅读：
- François Chollet, "On the Measure of Intelligence"（2019）——他对"通用智能 = 经验 + 抽象"的最系统论述
- Solar-Lezama 等，《Sketch: A Programming Language for Synthesis》（2008）——程序合成历史源头之一
- Ethan Mollick《Co-Intelligence: Living and Working with AI》（2024）

---

### 深挖 #2：AI 能力的"地理时差"

事实核实：
Elad Gil 的原推时间戳为 2026-05-10 05:55 BJT；Andreessen 的"Co-sign"于约一小时后跟进。Gil 给出的具体数字（实验室 vs SV 3-4 月、SV vs NY 3-6 月、NY vs ROW 6-12 月）来自 Gil 本人的产业观察，无法多源核实。

思想溯源：
"创新的地理集中"这一判断最早可追溯到 Alfred Marshall 1890 年《经济学原理》中的"产业地区性"分析；当代版本是 AnnaLee Saxenian 1994 年《Regional Advantage》（硅谷 vs 128 公路）；近十年最相关的是 Enrico Moretti 2012 年《The New Geography of Jobs》。Gil 这条的新颖性在于把"知识时差"以月为单位量化，而不是以"产业集群效应"做定性描述。最有力的反驳来自远程主义：远程工具与开源社区可以打破地理时差，Riley Brown 的回复正是这种立场——只要 Twitter 用得正确，就可以提前两个月。

同行视角：
- Sam Altman（OpenAI CEO，类型 2）今日的"codex 任务自动完成"叙述间接支持时差论
- Marc Andreessen 直接 Co-sign
- 反向声音来自远程主义者（Patrick Collison、DHH——后者今日未就此发言）

对中国商业 / 科技读者的含义：
对中文 AI 团队，这条判断意味着"看论文 + 看开源代码 + 看 GitHub trending"已不足以追上前沿；需要刻意补足"前沿团队的工具链 / 提示工程 / 评估流程"知识，这些只能在私人渠道（X 私聊、Discord、内部博客）中获得。换句话说：差距是知识获取渠道的差距，更大于研究能力的差距。

延伸阅读：
- AnnaLee Saxenian, *Regional Advantage*（1994）
- Enrico Moretti, *The New Geography of Jobs*（2012）
- Stratechery 近一年关于"frontier labs as platforms"的系列分析

---

### 深挖 #3（来自第五节）：Saylor on $BTC, $STRC, $MSTR — Consensus 2026 访谈

事实核实：
Saylor 的 Consensus 2026 视频访谈链接在他个人账号 5月10日 05:28 BJT 发布；时间戳目录由 Saylor 本人写出，故时间戳准确性可信。$STRC 募资数据 ($5.58B YTD, +189% 增长, 23 个连续月度股息共付出 $693M) 来自 @phongle 转推 Strategy Q1 文件——[未经多源验证：Strategy 自身披露，非第三方核数]。

思想溯源：
Saylor 把 BPS（每股比特币）作为公司"真北"的做法在公司治理史上没有完全先例。最近的对照物是 1990 年代以来 Berkshire Hathaway（巴菲特控股公司）使用的"book value per share（每股账面价值）"作为治理 KPI——但 Berkshire 的 book value 由审计标准定义，BPS 由 Strategy 自己定义。"用优先股而非债"做加密资产支撑的工程结构，早期可对照 2022 年 Genesis / Celsius 危机中的"硬币本位债权"探索——但 Saylor 的版本是把这个工具机构化、上市公司化。最有力的反驳来自 Cliff Asness（AQR Capital 创始人，量化投资学派代表）等价值投资人传统："任何用资产价格波动支撑的优先股，本质上就是杠杆，名字怎么换不影响经济实质"。

同行视角：
- Bill Miller（已退休对冲基金经理）公开支持类似的 BTC 储备策略（旧立场）
- Cliff Asness 历来对加密资产作公司财务工具持否定态度
- 主要分歧点：BTC 在 5-10 年时间维度上是否仍可作为"真北 KPI"还是必须回归现金流口径

对中国商业 / 科技读者的含义：
对中文上市公司财务高管，BPS 与 STRC 的工程化结构提供了一种可借鉴的"非传统资产支撑型优先股"思路——但需注意：中国 A 股上市公司与境外加密资产之间存在监管隔离，直接复制不可能；可借鉴的是"用工程化资本结构在主营业务之外建立第二曲线"的设计逻辑。

延伸阅读：
- Saylor 的 Consensus 2026 完整访谈（链接见上）
- Strategy Q1 2026 季报（公司官网）
- Cliff Asness 历年关于"加密作公司财务工具"的批评文章

---

## 七、决策与思考清单

**今晚值得再看一遍的（30-60 分钟内可消化）**：
基于「信号 #1 智能体编程是机器学习」—— 把 fchollet 今天两条推文与 Sam Altman、Greg Brockman 的两条 codex 自述并排放进同一份笔记，再读一遍 fchollet 2019 年 "On the Measure of Intelligence" 的摘要部分，看是否能复现你自己工作流中的"目标—评估"双端结构。

**今晚值得想一想的（适合通勤或临睡前回味）**：
基于「信号 #2 AI 能力的地理时差」—— 如果"前沿能力差距 = 工具链知识差距 + 部署轨迹差距"成立，那么作为一个在中文世界工作的从业者，我此刻补足差距最有效率的渠道是什么？是参加哪几个英文社区？是订阅哪几位前沿团队成员的私博客？

**本周值得追踪的**：
基于「信号 #3 Palantir 被 AI 实验室反向蚕食」—— 建立一份"应用层 SaaS 公司被基础模型层蚕食风险表"，列出过去一周国内外被定义为"AI 应用龙头"的公司，给每家加一列：它的护城河是数据、品牌、合规、还是工艺？哪一列最容易被基础模型层吞掉？

**今天值得重新审视的旧判断**：
"开源模型 + 公开论文 = 可以追上前沿"这个 2024-2025 年中文 AI 圈的常见判断，在今天 Elad Gil + pmarca + Mollick 的三个独立视角下都需要修正。修正方向是把"前沿能力"从"模型"扩展到"模型 + 工具链 + 部署轨迹 + 评估实践"四个并列层。

---

## 八、本期发言人画像更新

| 账号 | 类型标签 | 题材覆盖 | 本期表现 | 建议优先级 |
|------|---------|---------|---------|-----------|
| @fchollet | 类型 1（领域内权威） | AI / 软件工程方法论 | 提出"agentic coding = ML"判断，触发本期最强思想信号 | 高 |
| @eladgil | 类型 3（投资人） | AI / 风险投资 | 提出"AI 能力地理时差"四级阶梯，被 pmarca 联署 | 高 |
| @michaeljburry | 类型 3（投资人） | 投资 / 科技 | 转 WSJ Palantir 报道，挑明应用层 SaaS 估值风险 | 高 |
| @pmarca | 类型 3 + 6（投资人 / Polymath） | AI / 平台战略 | "Harness Hyper War" + 联署 Gil；其他多为政治站队 | 中 |
| @sama | 类型 2（OpenAI CEO） | AI / 智能体 | 一条家庭式 codex 自述，间接强化信号 #1 | 中 |
| @gdb | 类型 2（OpenAI 总裁） | AI / 智能体 | 转报销自动化截图，间接强化信号 #1 | 中 |
| @saylor | 类型 2（Strategy CEO） | 投资 / 公司财务结构 | 公开 Consensus 2026 完整访谈与 STRC 工程化逻辑 | 中 |
| @emollick | 类型 1（沃顿教授） | AI / 知识管理 | 提出 "2022-brained models" 单源观察 | 中 |
| @wtgowers | 类型 1（数学家） | AI 推理 / 数学 | 报告 PhD 章节级 AI 数学产出（单源） | 中 |
| @kevin2kelly | 类型 1（科技史 / 技术哲学） | 互联网 / 平台经济史 | 把 1998 年 *New Rules* 完整开放阅读 | 中 |
| @BrankoMilan | 类型 1（经济学家） | 经济史 / 中国研究 | 转推 Koyama（亚当·斯密 250 年）与 Subramanian（中国经济） | 中 |
| @jeremyphoward | 类型 1（fast.ai） | AI 训练 / 开源平台 | 转 Fireworks 与 ERNIE 5.1 信号 | 中 |
| @Scobleizer | 类型 5（科技述评号） | 机器人 / AI / 硬件 | 转 Wuji 灵巧手、YC robotics demo、ASI-Arch 等多条产业进展 | 中 |
| @elonmusk | 类型 2（Tesla / SpaceX CEO） | 自动驾驶 / 火箭 / Grok | Tesla AI Vision 光子重建 + Starship V3 满堆 + Grok Imagine；其他为政治转推 | 低-中 |
| @NickSzabo4 | 类型 1（密码学先驱） | 政治 / 历史 | 当日多为政治站队转推；唯一商业 / 科技含金量来自旧推（"信任去中心化"） | 低-中 |

**优先级定义**：
- **高**：本期产生了至少 1 条进入主区块或书单区的商业 / 科技信号，且发言人类型在画像上有更新。本期高优先级 = 3 个（fchollet / eladgil / michaeljburry），符合上限
- **中**：本期是高效信号过滤器、重要资源信源、或本期表现稳定的常规信号源
- **低-中**：本期未提供足够独立判断或语境敏感

---

## 九、沉默与意外信号

**本期值得注意的沉默**：
今日（2026-05-10）是西方母亲节，OpenAI 系（sama / gdb）在母亲节叙事框架下顺带提及 codex 与家庭，但 List 内的另几位 AI 研究权威——Yann LeCun（@ylecun，3 条推文，全部为美国政治讽刺转推）、Jeff Dean（@JeffDean，1 条推文，关于美式医保的政治转推）、Satya Nadella（@satyanadella，1 条推文，关于 Microsoft Foundry 工具）——当日都没有就 fchollet "agentic coding = ML" 这一基础范式提出任何回应或反驳。这本身是个信号——要么这个判断尚未被研究界视为值得回应，要么它已被默认接受到无需回应。

**本期意外信号**：
- Steven Pinker（@sapinker，类型 1：哈佛认知心理学家）今天发了一条"Waymo and the advancement of women"——把自动驾驶与女性夜间出行安全连起来评论，落在科技与社会学交叉地带。这与他通常的语言/认知/启蒙叙事不同，可作为他对"科技作为社会进步工具"立场的更新。本身不进主区块，但作为人物画像更新值得记下
- Patrick Collison（@patrickc，Stripe CEO，类型 2）今天没谈支付 / Fintech，而是抛出一份"我们不真正理解的日常现象"清单（闪电、睡眠、玻璃、湍流、形态发生、雨、冰、静电、麻醉），并附上 Quanta Magazine 的雷电研究新文。商业 / 科技 CEO 公开展示这种基础科学好奇心，本身可作为 Stripe 文化的一个侧写信号

---

## 十、本期信号评估

**信号 / 噪音比**：
本期处理 195 条推文，去除纯 retweet 与无认知信息的政治站队、生活流后剩约 65 条；通过铁律六（商业 / 科技题材）筛查约 28 条；进入主区块 3 条，进入单源高启发 4 条，剩余约 70% 为低价值或题材范围外（其中相当部分为美国—中东时政相关转推、文学—文化—宗教评论）。

**信息密度**：高
今天 List 难得在窗口内出现一组"机制相互对照"的多源信号（fchollet + eladgil + emollick + Burry + pmarca），且至少一条来自顶级权威（fchollet）。

**主导主题**：智能体编程范式与 AI 能力地理 / 数据壁垒——AI / agentic stack 占据了今天最有思想含金量的发言。

**未浮现但值得追踪**（推测）：
- Tim Gowers 的 PhD-章节-级 AI 数学论文具体身份与同行回应
- Andrew Yang "Is college still worth it" 长文是否会引发其他 List 成员（Cowen / Caplan / Yglesias）的连环回应
- Mark Koyama "Wealth of Nations 250" 会议论文 PDF 是否公开

---

## 附录 A · 行业内幕（可选阅读）

- **Tesla AI Vision 光子重建** — Elon Musk 公开 Tesla FSD 的"photon count reconstruction（光子计数重建）"图像，把人眼可见的 RGB 与 Tesla AI 用的光子计数图并排展示，解释 FSD 在夜间或强眩光中视觉表现优于人眼的具体原因
- **Starship V3 满堆** — SpaceX Starship V3 与 Super Heavy V3 首次合体在 Starbase 发射台亮相
- **Omarchy 3.8 发布** — DHH 的 Omarchy（Linux 桌面发行版）3.8 增加 reminders / weather / 浏览器 - 终端 - 编辑器系统级默认设置；可选无加密安装；集成转码工作流
- **Fireworks AI Train** — 提供"开源模型自有训练"平台，挑战"你只能租用前沿模型"的 frontier-lab 模式（jeremyphoward 转推）
- **ERNIE 5.1（百度）** — 总参数压缩到 1/3、激活参数压缩到 1/2；预训练成本仅约同规模模型的 6%（来源：@ErnieforDevs，当事方原话）；声称在某些 benchmark（即性能评测基准）上超过 DeepSeek-V4-Pro [未经多源验证]
- **ASI-Arch / "AlphaGo Moment for Model Architecture Discovery"** — 自动模型架构发现系统的论文（Scobleizer 转推）
- **Wuji Glove × Wuji Hand** — 远程操作灵巧手机器人 1:1 动作映射演示（具身智能 / 远程遥操方向，Scobleizer 转推）
- **Telegram Bots → Callable Agents** — Telegram bot 升级为可在群聊中以 @ 触发的可调用 agent（Scobleizer 转推）
- **GPT-Realtime-2 实时翻译** — gdb 转推 Chormex Chrome 扩展集成 GPT-Realtime-2 做 YouTube / 直播 / 会议实时翻译

---

## 附录 B · 范围外但值得知道的信号

- *Steve Kerr 在 The New Yorker 的长访谈*（NBA 教练谈未来与政治意向）——非商业 / 科技
- *Spirit Airlines 关闭* — 可争论是否商业题材，本期作为消费经济与美国低成本航空时代落幕的文化注脚收录于此，不进入评估
- *Péter Magyar 击败 Orbán* / *Pope Leo XIV 与 Trump 在伊朗议题上的对峙* / *英国 Reform UK 上升* — 纯政治时政，不入主区块
- *Francis Fukuyama 预售《In the Realm of the Last Man》* — 政治哲学延续《历史之终结》主题，与商业 / 科技无直接关联，不入书单区
- *Steven Pinker 推荐 Richard Carrier 关于"黑暗时代是否真实存在"的史学评论* — 一般史，与商业 / 科技无直接关联

---

## 简报末尾固定声明

本简报的所有判断、关联推测均基于公开推文与公开网络信息。所有具体数字均标注来源；无法多源验证的内容已显性隔离至「单源高启发」区块。读者应理解：思想类信号的"准确性"低于事实类新闻——这份简报的价值不是"告诉你真相"，而是"告诉你此刻在商业与科技领域最值得思考的方向"。
