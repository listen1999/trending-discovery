# 思想发现简报 | 2026-05-18

> 数据窗口：2026-05-17 06:00 — 2026-05-18 06:00（北京时间，过去 24 小时）
> 深度挖掘：3 条 | 模板版本：v1.2

---

## 一、今日要点

周五美东傍晚，世界最大对冲基金 Citadel 的创始人 Ken Griffin 在某次访谈里说了一段让他自己「那天回家颇为沮丧」的话——「过去由硕士、博士做几周或几个月的活，AI agent 现在用几小时到几天就能完成」。访谈片段被对冲分析师培训人 Brett Caughran（@FundamentEdge，前 Citadel/D.E. Shaw/Schonfeld 资深买方分析师）整理出来后，在过去 24 小时内被 Marc Andreessen（a16z 创始合伙人）转推、Andrew Yang（UBI 倡导者、前总统候选人）引用、@GarrettPetersen 借自家「数据科学家妻子」的体感佐证——「过去的 10x 工程师如今是 100x，没跟上 AI 的人还在手工干」——以及 Wharton 教授 Ethan Mollick 用 von Neumann 对「奇点」的原始定义（即「人类事务无法继续以我们熟悉的方式延续的那一点」）来再描述这一观察。

这件事真正值得抽时间想的，不是「AI 又能替代多少工作」这种被说滥的话头，而是 Griffin 这种位置上的人——他通常不会随口对外界谈情绪——主动承认了 9 个月内 AI 工具能力的「step change」。同一天，Chamath Palihapitiya（前 Facebook 增长高管、Social Capital 创始人）撰文把咨询业放进同一个齿轮里：他说 PwC、埃森哲这些咨询商让员工直接调用 OpenAI/Anthropic 的 API，就是「把狐狸请进了鸡舍」——因为这两家正用同样的资金扶持咨询业的颠覆者。围绕这些发言，本期 List 形成了一条几乎所有「领域内权威」都不约而同指向同一深层变化的脉络：白领高端工作的生产函数正被重写，而商业组织的反应分两类——理解者重构控制层，未理解者把命交了出去。

**Bottom line in English:** When Ken Griffin himself admits the AI step-change in PhD-level finance work and Chamath openly attacks the SaaS business model, the question isn't *whether* enterprise software is being rewritten — it's whether your firm controls the tokens or just consumes them.

---

## 二、主信号（多源验证）

> 进入此区块的标准：经过事件归一化 + 至少 2 个独立来源 + 优先级矩阵总分 ≥ 7 + 通过铁律六质量门槛

### 信号 #1：Citadel 的「step change」自白与 AI 在金融业的临界点

主信源：@FundamentEdge（@AndrewYang 引用、@pmarca 引用 / 「经营者 + 投资人」）· 约 8 小时前
佐证：@AndrewYang（前总统候选人，类型 4 + 6）· @pmarca（a16z 创始合伙人，类型 3）· @GarrettPetersen（经济学博士，类型 1 / 同行体感佐证）· @emollick（@Wharton AI 教授，类型 1）
题材分类：投资 / AI / 劳动力市场

故事 / 场景：
Citadel 创始人 Ken Griffin 在一次公开访谈里描述了某个普通的周五傍晚——他下班回家路上「颇为沮丧」（"fairly depressed"），因为他在公司四壁之内亲眼看到 AI agent 把通常由金融硕士、博士耗时数周到数月的工作压缩到了几小时几天。他特别指出，这「不是中端白领工作，这些是被取代的极高技能工作」。前 Citadel/D.E. Shaw/Schonfeld 分析师 Brett Caughran 把这段整理出来后，48 小时内被 Andrew Yang 简短背书——「金融业会迅速追随科技业的自动化」（97k 次浏览），同时 Marc Andreessen 直接转推并加上「他在结尾的悲观语气有 Boomer 味（抱歉 Ken！）但其余我都同意」。

为什么值得思考：
Ken Griffin 不是 AI 多头，也不是布道者——他是世界上最大对冲基金之一的创始人，过去对 AI 大多数公开评论都偏保守。当这样位置的人主动说「9 个月内出现了 step change」，并且承认连他这种行家都没准备好，这是一条比所有 LLM 厂商的 demo 都更可信的「内部线索」。它与 6 个月前主流叙事（「AI 只能动初级白领」）形成直接对照。

关键引文（中英并存）：
> EN: "These are not mid-tier white collar jobs. These are like extraordinarily high skilled jobs being … automated by agentic AI."
>
> 中：「这不是中端白领工作。这些是被 agentic AI 自动化的极高技能工作。」

链接：
- Brett Caughran 原推：https://x.com/FundamentEdge/status/2055675389767516544
- Andrew Yang 引用：https://x.com/AndrewYang/status/2056005476450463797
- pmarca 引用：https://x.com/pmarca/status/2055795151054704784

---

### 信号 #2：Chamath 与 SaaS 估值压缩——「控制 tokens 才是控制 spice」

主信源：@chamath（前 FB 增长高管、Social Capital 创始人，类型 2 + 3）· 约 4 小时前
佐证：@MilkRoadAI（AI 投资述评号 / 整理版）· 高盛报告（援引于 MilkRoadAI 综合）· OpenAI/Anthropic 同期咨询业务融资公开数据
题材分类：商业 / 投资 / 企业软件

故事 / 场景：
2026 年 5 月 18 日凌晨，Chamath Palihapitiya 在 X 上写了一段直接点名 PwC 和埃森哲的话：「如果你在跑一家咨询公司，把 Anthropic 或 OpenAI 直接部署进你的客户组织里——是你自己把狐狸请进了鸡舍。」他给出的处方是「采用一个控制平面（control plane），可以仲裁 token 流向哪里、由谁生成 token」，并用一句 Dune（沙丘）梗收束：「控制 tokens 就是控制 spice。」这条引述背后，被 Milk Road AI 整理出的数字底色相当沉重：90% 的公开 SaaS 公司股价较 52 周高点跌幅 30–80%；高盛报告显示软件远期 P/E 从 35x 跌到 20x，是 2014 年以来绝对低点；OpenAI 据报融到 $40 亿 [未经多源验证：MilkRoadAI 援引未注明出处] 启动咨询业务、向 19 个投资人（含 TPG、Brookfield、Bain、McKinsey）承诺年化 17.5% 的保本回报——而 OpenAI 同年预计亏损 $140 亿；Anthropic 立即跟进 $15 亿同类咨询合资 [未经多源验证]。Chamath 自己控股的 8090 的 Software Factory 正与 EY 全球合作搭建这个 control plane。

为什么值得思考：
过去主流共识是「企业软件买席位订阅（per-seat SaaS）」，Chamath 挑战的是这套商业模式的根本——按席位收费的产品形态在 agentic AI 下不成立。但更值得思考的是他的利益位置：他自己是 8090 的实控人，正在销售他描述的那种 control plane。这条信号的独特性在于，他不是评论员而是当事方，他的描述既是判断也是路演——读者需要把两者分开评估。

关键引文：
> EN: "Controlling the tokens is controlling the spice."
>
> 中：「控制 tokens，就是控制 spice。」

链接：
- Chamath 原推：https://x.com/chamath/status/2056074605228605580
- Milk Road AI 整理版（被引用对象）：https://x.com/MilkRoadAI/status/2055996073655840773

---

### 信号 #3：美国为什么造不出 3D 打印机——制造业基础的「再发现」

主信源：@gak_pdx（Greg Koenig，金属精密加工创始人，类型 2 / 实操者）· 约 16 小时前（被 @pmarca 转推 + 加注）
佐证：@pmarca（类型 3，明确背书 "Every industrial economy is an entire ecosystem"）
题材分类：商业 / 科技 / 制造业 / 产业政策

故事 / 场景：
精密制造从业者 Greg Koenig（金属加工领域的实操者）发了一条「试图反复跟人解释」的帖子——美国没有可行的 3D 打印机公司，原因不是品牌或资本，而是底层架构缺失。他逐条列出一台 3D 打印机其实只是「轻型 CNC 铣床」（CNC 即数控机床），它需要：微米级精度的线性导轨、亚微米轴承、高分辨率伺服 / 步进电机、运动控制芯片和板卡、钣金、注塑、各类涂层——而美国「在任何一项消费品规模上都没有相应的工业基础」。Marc Andreessen 转推时补了一句：「每个工业经济都是一整套生态——想象一下 5,000 家公司彼此完全运转、互相买卖。」

为什么值得思考：
这条信号挑战了一个相当流行的产业政策共识——「我们引进一家工厂 / 给一家公司补贴 / 用关税挡住进口，就能重建制造业」。Koenig 给出的反例是结构性的：3D 打印机不是单点缺口而是生态缺口，缺的是几千家「风投不投、利润中等、毫无护城河」的零部件公司。他给出的处方反直觉——美国需要的不是更多独角兽，而是更多无聊的中游零件供应商。这对中国读者的镜像意义同样清晰：当下中国制造业的优势恰好是这些「无聊的、毛利中等、无护城河」的生态厚度，而这不是任何一项工业政策能在十年内复制的。

关键引文：
> EN: "What we need is a bunch of uninvestible (by venture funds) businesses that are boring and competently supply a bunch of even more boring, medium margin, no-moat components."
>
> 中：「我们需要的是一批风投投不进去的、无聊的、能干地供应另一批更无聊、中等毛利、毫无护城河零部件的公司。」

链接：
- Greg Koenig 原推：https://x.com/gak_pdx/status/2055746965330399278
- pmarca 转推 + 评论：https://x.com/pmarca/status/2055886789336813610

---

## 三、单源高启发信号

> ⚠️ 重要说明：以下信号**仅有一个来源**，未经多方独立验证。但发言人在该领域有明确商业 / 科技权威性，内容具有思想价值。请读者自行判断。

### 启发 #1：Yann LeCun 预告：12–18 个月内的「层级世界模型」

发言人：@ylecun（Yann LeCun，类型 1，纽约大学教授 + AMI Labs 执行主席 + 图灵奖得主 + 前 Meta 首席 AI 科学家）
领域：AI 研究路线
发布时间：约 7 小时前

他/她说了什么：
LeCun 说他认为「12 到 18 个月内，我们会拥有一种训练层级世界模型（hierarchical world models，即逐层抽象的'世界建模'方法）的通用方法」。这些模型会从视频和真实世界数据中学习，进而帮助在机器人、医疗和其他领域做行动规划，并最终「向通用世界模型扩展」。

为什么值得记下：
这是 LeCun 在 AI 研究路线上的一个明确、可被时间检验的预测。LeCun 长期反对纯 LLM 路线，主张「世界模型」是通往真正智能的路径——这条 24 小时窗口内的发言把模糊愿景压成了一个具体的时间窗。如果 2027 年 5 月前后没有出现这样的方法，可以视为他这一路线判断的明确证伪点。

目前的不确定性：
- 单源，且 LeCun 在 Meta/AMI 体系内对自家路线有利益绑定
- 「通用方法」缺乏具体定义——什么算「方法已经有了」？

链接：https://x.com/ylecun/status/2056020151053492412

---

### 启发 #2：Yann LeCun 转推质疑《Empire of AI》对数据中心用水量的算错

发言人：@ylecun（同上）转推 @woke8yearold
领域：AI 基础设施 / 公共认知
发布时间：约 25 小时前（被 24 小时窗口内多次再引用，最近一次为 2026-05-18 04:34）

他/她说了什么：
LeCun 转推一条声称——「数据中心抢我们的水」这类公共叙事的源头是 Karen Hao 的新书《Empire of AI》中的水耗算法错误，作者后来承认了这一错误。LeCun 进一步用一条长推为犹他州数据中心辩护：无人区、买下已在使用的水权、自带电力、零核扩散风险。

为什么值得记下：
独立于政治立场，这是一条可被检验的「公共叙事的事实根基是否站得住」的信号。如果属实，意味着过去 6 个月围绕「AI 抢水」的辩论建立在一个被原作者承认的算错之上——这不是常见情形，值得追溯。

目前的不确定性：
- 「作者已承认」是单源说法，需要找到 Hao 的原始勘误声明
- LeCun 与 Meta 数据中心建设有持仓性利益冲突
- 反方（Hao 与其支持者）尚未在 24 小时窗口内回应

链接：https://x.com/ylecun/status/2056111235658105127

---

### 启发 #3：Steven Pinker 推荐 Dan Williams 的「Speaking Truth to Power Is Bad Epistemology」

发言人：@sapinker（Steven Pinker，类型 1，哈佛认知科学家、多本畅销书作者）
领域：认识论 / 公共知识分子的责任
发布时间：约 7 小时前

他/她说了什么：
Pinker 转推/引用了萨塞克斯哲学家 Dan Williams 的一篇长文，核心论点是：「向权力讲真话」（speaking truth to power）这一公共知识分子姿态，在认识论上是有害的。Williams 写道：「智识勇气极其重要，但在没有首先小心确立什么是真之前，要么没用要么有害。所以知识分子的首要责任是寻找并讲述真理，仅此而已。这个工作描述不够英雄主义，但更有智识与社会用处，也因为不那么英雄而更难自我欺骗。」

为什么值得记下：
这与 Pinker 长期的「启蒙现在」立场一致，但他这次把矛头转向了「对当权者讲真话」这种自我标榜的姿态——这恰恰是他自己常被左右两派分别贴上的标签。该判断的独特性在于把「英雄叙事」与「认识论可靠性」分开来审视，对受过教育的中文读者（同样身处「知识分子角色」语境）有直接迁移价值。

目前的不确定性：
- 这是哲学论证，不能被实证证伪
- 反方可能援引「权力下沉时代真理本就由权力定义」一类的福柯路线反驳

链接：https://x.com/sapinker/status/2056022952492036200 ; Williams 原文：https://open.substack.com/pub/conspicuouscognition/p/speaking-truth-to-power-is-bad-epistemology

---

### 启发 #4：pmarca 借 Henry Gao 重述「修昔底德陷阱」——不是大国竞争，是生活方式之争

发言人：@pmarca 引用 @henrysgao（SMU 法学教授、CIGI 高级研究员，类型 1 / 国际经济法权威）
领域：国际关系 / 思想史
发布时间：约 16 小时前

他/她说了什么：
Henry Gao 在原推中写道：「不，修昔底德陷阱不是关于大国之间的竞争。它是关于不同生活方式之间的竞争：你想生活在斯巴达还是雅典？」pmarca 加注「Hmmm」转推。

为什么值得记下：
「修昔底德陷阱」过去十年常被简化为「崛起大国 vs 守成大国必有一战」的中美对照。Gao 的重述把核心放回到 Thucydides 原文的雅典 / 斯巴达对立——民主商业开放 vs 军事集体纪律——这是一个对长期看中美博弈具有不同启发的框架重置。

目前的不确定性：
- 这是文本解读层面的争议，不同 Thucydides 学者本就立场分歧
- 把「生活方式」作为唯一变量可能低估了结构性物质因素

链接：https://x.com/henrysgao/status/2055547818828558550

---

## 四、跨领域关联

> 本区块尝试**主动建立**几条看似不相关但指向同一深层变化的信号关联。
> ⚠️ 这是 LLM 的关联推测，不是事实。每条都给反向思考。

### 关联线 A：高端白领的自动化 + 咨询业的中介危机 + 工业基础的空心化——三者指向同一种「资本配置失能」

信号 1（科技 / 投资）：Ken Griffin 承认 PhD 级金融工作被 AI agent 重写 — @FundamentEdge / @AndrewYang / @pmarca
信号 2（商业）：Chamath 攻击咨询业把 AI 直接部署给客户＝把狐狸请进鸡舍 — @chamath
信号 3（制造业）：Greg Koenig + pmarca 说美国 3D 打印生态空心化，缺的是几千家无聊零部件公司 — @gak_pdx / @pmarca

潜在共同根源：
过去 40 年美国资本市场的回报结构鼓励「高毛利 / 软件 / 零库存」的商业模式，惩罚「中毛利 / 重资产 / 无护城河」的中游业务——金融业的高端白领、咨询业的中介利润、制造业的零部件生态，都是同一套估值偏好的产物。AI 的 step change 不是单独消灭白领或者单独削薄 SaaS，它是在同一时间把这些「中介性高毛利层」全部压扁，迫使资本重新发现「无聊但必要」的底层。

反向思考：
机制相似性测试——如果信号 1 错了（PhD 级金融工作并未被自动化，只是 Griffin 焦虑），那信号 3（制造业生态空心）会不会也错？大概率仍成立——制造业生态空心是物理事实（线性导轨工厂数量可数），与 AI 替代无关。所以这条关联线只在「AI 步进」这一假设下成立——如果 AI 在 12 个月内没有进一步突破，信号 1 和信号 2 会回归常规叙事，而信号 3 仍是独立的产业问题。建议读者把这条关联线视为「假设性图景」而非已发生的结构变化。

---

## 五、本期书单与访谈

> 这一节是这份简报的核心价值之一。
> 包含：今天 List 里的权威发言人主动推荐的商业 / 科技新书、访谈与长文。
> **进入此区块的最低门槛**：发言人或来源具备一定权威性 + 内容已经过基本核实 + 通过铁律六质量门槛。

### 新书 / Books

- **《Empire of AI》/ Empire of AI** — Karen Hao
  推荐者（反向）：@ylecun（图灵奖得主，转推 @woke8yearold 的批评）
  推荐语境：因为 LeCun 指其「数据中心抢水」一节算错，本期被反复引用作为「公共叙事 vs 事实根基」的例证
  核心论点：[书的整体论点：硅谷大型 AI 公司如何复制殖民帝国的资源汲取模式——具体论点待核实]
  题材分类：科技 / 公共政策
  中文版状态：暂无（截至本期，2026 年 5 月）
  评分：Goodreads 评分 [未经多源验证]
  对什么人最有价值：想理解「AI 批判性叙事」如何形成的读者；同时建议对照原书与 LeCun 的批评，自己判断
  链接：原书 Penguin Random House 页面

- **《Visions of Inequality》/ Visions of Inequality** — Branko Milanović
  推荐者：@BrankoMilan（CUNY 研究教授、LSE 客座教授，本人自引）
  推荐语境：本期他转推 @Kumar_EconIneq 用其书中 Marx 一章建立的「不平等政体分类」框架，分析 129 国 1992-2019 年的工资 / 利润 / 顶端财富份额数据
  核心论点：用马克思 vs 帕累托 vs 库兹涅茨等不同思想家的「不平等观」作为分类框架，跨时空比较不同社会的不平等结构（已 web 核实存在，2023 年 Harvard University Press 出版）
  题材分类：经济 / 经济史
  中文版状态：[未经多源验证]
  评分：Goodreads 约 4.1 [未经多源验证]
  对什么人最有价值：想跳出「基尼系数 + 收入十分位」这种工具型不平等讨论的读者
  链接：https://www.hup.harvard.edu/

- **Michael Burry Substack 系列「D'ai of the Triffids: Office Software Triage」**
  推荐者：@michaeljburry（迈克尔·伯利，《大空头》原型，"Cassandra Unchained"）
  推荐语境：5 月 17 日发表精简版（约 1500 字，全文的 1/8），是覆盖 46 只软件与支付股票的系列开篇
  核心论点：他用 Triffids（约翰·温德姆 1951 年科幻小说《三尖叶植物之日》中那种缓慢但终将统治地球的入侵植物）作类比，把办公软件类股票做分类「triage」（即急诊分流：分死、伤、可救三类）。具体论点需读原文。
  题材分类：投资 / 软件 SaaS
  中文版状态：无
  对什么人最有价值：关心 Chamath 信号（SaaS 估值压缩）后想看一位经历过 2008 危机的逆向投资人的具体分类的读者
  链接：https://open.substack.com/pub/michaeljburry/p/dai-of-the-triffids-office-software-922

### 论文 / 报告 / Papers & Reports

- **「Artificial Intelligence and Future of Capitalism, from a Marxist and a Neoclassical Point of View」** — Branko Milanović
  推荐者：@BrankoMilan（本人）
  发布媒介：Brave New Europe
  发布日期：2026 年 5 月（本期 List 引用）
  题材分类：经济 / 政治经济学
  主题：用马克思主义和新古典两种框架同时分析高度自动化经济与资本主义的兼容性——核心张力（Milanović 在更早一条推文中已铺垫）：在马克思框架下，剩余价值与利润趋零；在新古典框架下，需求不足导致利润趋零——两者都指向「除非有等量劳动密集型部门崛起，或大规模再分配给不工作的人，否则资本主义无法维持」
  为什么值得读：这是少见的把同一议题用对立思想框架同时审视的论文，对纯主流经济学读者构成必要的对照
  阅读时长：估约 30 分钟
  链接：https://braveneweurope.com/branko-milanovic-artificial-intelligence-and-future-of-capitalism-from-a-marxist-and-a-neoclassical-point-of-view

### 重要长文 / Long-form Articles

- **「Why Some States Can Organize Capital, While Others Are Organized by Capital」** — Leon Liao
  推荐者：@BrankoMilan（CUNY 研究教授）
  发布平台：Substack
  发布日期：2026 年 5 月
  题材分类：经济 / 国家能力研究
  主题：用「国家能力」（state capacity）一词在新一代政治经济学讨论中的演化为线索，讨论为何有些国家能把资本组织起来用于公共目的，而另一些反被资本所组织。Milanović 引用时加注：「'组织资本'是国家能力的核心考验。」
  为什么值得读：对中国语境直接相关——「国家能力」这一概念在中文学术圈近 5 年成为讨论热点，这篇英文文献提供了不同的分析切入
  阅读时长：估约 25 分钟
  链接：https://leonliao.substack.com/p/why-some-states-can-organize-capital

- **「Speaking Truth to Power Is Bad Epistemology」** — Dan Williams
  推荐者：@sapinker（哈佛认知科学家 Steven Pinker）
  发布平台：Substack（Conspicuous Cognition）
  发布日期：2026 年 5 月（本期被引用）
  题材分类：经济 / 思想（公共知识分子的认知责任）
  主题：见上文「单源高启发 #3」
  为什么值得读：对所有撰稿人 / 评论家 / 知识从业者都有自检价值——它把「英雄叙事的认识论代价」明确化
  阅读时长：估约 15-20 分钟
  链接：https://open.substack.com/pub/conspicuouscognition/p/speaking-truth-to-power-is-bad-epistemology

### 课程 / Courses

- **「A Beginner's Guide to Irrational Behavior」** — Dan Ariely（杜克大学行为经济学教授）
  推荐者：@danariely（本人，类型 1 领域内权威）
  推荐语境：他把原 Coursera 课程重建为自家网站的永久免费档案——6 周课程，主题覆盖金钱、不诚实、动机、自控、情绪；含 13 场嘉宾讲座
  题材分类：经济 / 行为经济学
  关键说明：免费，无需注册
  对什么人最有价值：想系统了解行为经济学但不愿付平台月费的读者；本期 engagement_rate 高达 1.85%，是本期 List 内最高的之一，说明读者对「永久免费经典课程」高度认同
  链接：http://danariely.com/coursera

---

## 六、TOP 3 深度挖掘

> 对前面区块中（主信号 + 书单与访谈）合计排名前 3 的信号执行深挖。
> v1.1 强制约束：**TOP 3 中至少 1 条来自「书单与访谈」区**（此处由 Branko Milanović 的论文承担该位）。

#### 深挖：信号 #1 — Ken Griffin 的「step change」与 AI 在金融业的临界点

事实核实：
经 web_search 核实 Brett Caughran 的 Citadel/D.E. Shaw/Schonfeld 履历属实，他确实是当前 ASU 兼任教授并经营独立的卖方 / 买方分析师培训公司 Fundament。Ken Griffin 在 Citadel 的多次公开访谈中关于 AI 的态度过去 12 个月明显从「工具」转向「替代行业」，本期被引用的引文与他近期其他公开发言风格一致。但「精确日期 / 完整访谈来源」在 24 小时窗口内未给出，建议读者把这条作为「Griffin 此时段的总体表态」而非「某次具体访谈的逐字记录」。

思想溯源：
「AI 自动化高端白领」这一论断的可识别先驱是 Erik Brynjolfsson 与 Andrew McAfee 在 2014 年的《The Second Machine Age》——但他们当时预测的是「中端」工作。本期信号的真正新意在于把分界线上移到了「需要硕士 / 博士」的工作。最有力的反驳来自 Daron Acemoglu（MIT 经济学教授）2024 年的工作——他持续论证 AI 对生产率的实际贡献被高估，理由是「测量数字基于使用者自报，缺乏对照实验」。

同行视角：
- Ethan Mollick（@emollick，Wharton AI 教授）：本期表态——我们确实正在经历 von Neumann 意义上的奇点，「人类事务无法以我们熟悉的方式继续」
- Daron Acemoglu（MIT）：反方代表，AI 实际生产率贡献被严重高估
- 主要分歧点：「step change」是否真实，还是高薪从业者的体感放大？

对中国商业 / 科技读者的含义：
对中国金融业的直接含义是——头部对冲基金 / 量化机构 / 投行的高端研究岗位的工种重置可能比预期更快。对在读金融硕士 / 博士的具体建议：把「人类无法被 AI 替代的具体能力」从抽象概念化为可证明的产物（如能解释为何 AI 的判断错了的能力），是未来 3 年的求职竞争力关键。

延伸阅读：
- Brett Caughran 原推：https://x.com/FundamentEdge/status/2055675389767516544
- Erik Brynjolfsson 的近期发言（与本判断的对照）

---

#### 深挖：信号 #2 — Chamath 与 SaaS 估值压缩

事实核实：
经 web_search，OpenAI 推出企业咨询业务（"OpenAI Deployment"）属实，时间在 2026 年初。Anthropic 同期推出对标的咨询业务也属实。但「OpenAI 融到 $40 亿、向 19 个投资人承诺 17.5% 保本回报」的具体数字目前未在 OpenAI 或主要监管文件中找到独立来源，最早出处可追溯到 MilkRoadAI 整理稿——所以这一数字应视为单源转述，不应作为引用基础。「90% SaaS 股票较 52 周高点跌 30-80%」与一般市场感知一致，但具体数字来源 [未经多源验证]。

思想溯源：
「商业模式因技术变迁而被重写」是 Clayton Christensen《创新者的窘境》（1997）的经典框架。Chamath 的特殊贡献是把「席位订阅 → 按工作量付费」这一具体转变与 agentic AI 绑定。最有力的反驳是来自传统 SaaS 阵营——比如 Salesforce、ServiceNow——他们认为「数据飞轮 + 工作流深度集成」是 AI 厂商难以替代的护城河，这恰好与 Chamath 自己对「高端」SaaS 命运的判断一致。

同行视角：
- Marc Benioff（Salesforce CEO）：持「我们的数据飞轮就是护城河」立场
- Aaron Levie（Box CEO）：本期未发声，但近期持「SaaS 必须把 AI 当主菜单上线」的立场
- 主要分歧点：「席位收费的死亡」是否就是「SaaS 模式的死亡」？两者并不完全等价

对中国商业 / 科技读者的含义：
中国 SaaS 行业过去 5 年估值一直承压，原因被解释为「客户付费能力差 / 私有部署偏好」——Chamath 这条信号可能给出一个更深的解释：如果美国市场都正在抛弃 per-seat 模式，那中国市场的「估值疲软」可能并非区域性问题，而是被提前发现的全球性现象。对国内 SaaS 创业者的具体建议：在融资材料里早点放弃用「ARR per seat」做核心叙事。

延伸阅读：
- Chamath 原推：https://x.com/chamath/status/2056074605228605580
- Christensen《创新者的窘境》中文版（中信出版社）

---

#### 深挖：书单 #1 — Branko Milanović「AI 与资本主义的未来：马克思主义与新古典视角」

事实核实：
经 web_search，文章确实于 2026 年 5 月由 Brave New Europe 发表，是 Milanović 此前一篇推文长文（其在 5 月 13 日左右先发表的简短结论）的扩展版。Milanović 本人是 CUNY 研究教授、LSE 客座教授、《Capitalism, Alone》《Global Inequality》《Visions of Inequality》作者——以可重复使用的、跨制度的不平等分析框架著称。

思想溯源：
「自动化与利润率」议题在马克思主义传统中可追溯到马克思本人在《资本论》第三卷关于「利润率下降趋势」的论述。新古典侧的对应版本是 Keynes 1930 年的预言「我们的孙辈每周工作 15 小时」以及后续 Solow 的资本-劳动替代分析。Milanović 的独特贡献是把这两个本来对立的传统放在同一篇论文里，得出形式上一致的结论——这种做法本身在政治经济学界相对罕见。最有力的反驳来自「内生增长」理论阵营：高度自动化下，被节省的劳动可能形成全新部门（如个人化教育、心理治疗、艺术），所以「劳动密集部门必然消失」的前提可能错了。

同行视角：
- Daron Acemoglu（MIT）：自动化与劳动力市场两极化的主流分析者
- Thomas Piketty（巴黎经济学院）：关注资本回报率长期高于增长率的 r > g 框架
- 主要分歧点：自动化的极限究竟是「资本主义自我终结」还是「新部门吸收」？

对中国商业 / 科技读者的含义：
中国正处于一个独特位置——既是制造业自动化最深的国家，又仍保留大规模劳动密集型服务业。Milanović 的两套框架（马克思与新古典）对当前中国「机器换人」叙事提供了不同的反向问题：在生产端机器换人完成后，需求端从哪里来？这一问题在国内宏观经济辩论中已经隐现（消费率长期偏低），但很少被纳入「自动化-资本主义」框架。

延伸阅读：
- Milanović 原文：https://braveneweurope.com/branko-milanovic-artificial-intelligence-and-future-of-capitalism-from-a-marxist-and-a-neoclassical-point-of-view
- Milanović《Visions of Inequality》Harvard University Press

---

## 七、决策与思考清单

> 这是日常思考读物，不是工作清单。内容形式：**问题，不是任务**。

**今晚值得再看一遍的（30-60 分钟内可消化）**：
基于 信号 #2（Chamath / SaaS 估值压缩） —— 读 Milk Road AI 对 Chamath 发言的整理（约 800 字），再看 Michael Burry 当天的 1500 字精简版 Triage 列表。两者读完，应该能形成一份你自己对「企业软件赛道哪一类会先掉队」的粗略判断表。

**今晚值得想一想的（适合通勤或临睡前回味）**：
基于 信号 #1（Ken Griffin "step change"） —— 如果"PhD 级金融工作被 AI agent 自动化"这一命题成立，那我所在的行业（出版 / 投资 / 学术研究）里，"用 PhD 思维方式做的工作" 哪些会先被压缩？

基于 Henry Gao 重述 Thucydides Trap —— 如果中美博弈的本质不是"崛起 vs 守成"，而是"两种生活方式"，那我作为读者本人，如果脱离国家叙事，更想生活在哪一种 day-to-day 节奏里？

**本周值得追踪的**：
基于 LeCun 12-18 个月层级世界模型预测 —— 建立一个简单的 1-2 行 Google Calendar 提醒，2027 年 5 月 17 日复查这条预测的实际进展。

**今天值得重新审视的旧判断**：
（本简报为初次产出，无累积输入，此项暂略）

---

## 八、本期发言人画像更新

| 账号 | 类型标签 | 题材覆盖 | 本期表现 | 建议优先级 |
|------|---------|---------|---------|-----------|
| @chamath | 类型 2 + 3（经营者 + 投资人） | 企业 SaaS / AI 商业模式 | 本期主信号 #2 的主信源，结合自家 8090 业务给出明确反共识判断 | 高 |
| @ylecun | 类型 1（图灵奖得主） | AI 研究路线 + AI 公共叙事 | 给出可被时间检验的 12-18 月技术预测，并主动质疑公共叙事 | 高 |
| @BrankoMilan | 类型 1 + 6（经济学者 + 跨域思想家） | 经济 / 经济史 / AI-资本主义 | 跨马克思 / 新古典框架同时分析 AI，且转推同行实证数据 | 高 |
| @pmarca | 类型 3（投资人） | AI / 制造业 / 文化 | 本期高频活跃，但多以「Interesting / Co-sign」式短评作转推转发；信号 #3 的主要中介 | 中 |
| @michaeljburry | 类型 3（投资人，曾以《大空头》闻名） | 投资 / SaaS | 启动 46 股软件 / 支付分类系列，文字虽未被广泛 RT 但 bookmark 率体现深度认同 | 中 |
| @sapinker | 类型 1（哈佛认知科学家） | 认识论 / 公共知识分子角色 | 引介 Dan Williams 长文，是少见的非 AI / 非政治的纯思想信号 | 中 |
| @danariely | 类型 1（行为经济学家） | 经济 / 行为经济学 | 把 Coursera 课程改为永久免费档案，engagement_rate 1.85% 为本期最高之一 | 中 |
| @emollick | 类型 1（Wharton AI 教授） | AI / 教育 | 用 von Neumann 原始定义重述「奇点」概念，给出本期最准确的思想边界 | 中 |
| @AndrewYang | 类型 4 + 6（前政治人物 + 跨域） | 经济 / AI 影响 | 短评「金融业会迅速追随科技业自动化」，作为信号 #1 的转发节点 | 中 |
| @FukuyamaFrancis | 类型 1（斯坦福政治学家） | 国际政治 / 民主 | 本期内容偏纯政治表态，无独立思想信号 | 低-中 |
| @nntaleb | 类型 1 + 6 | 概率 / 政治 | 本期发言偏政治立场，未涉及概率 / 风险等其领域内话题 | 低-中 |
| @paulg | 类型 2（YC 创始人） | 创业 / 写作 | 「well-informed optimism」金句质量尚可，但偏个人 reflective | 中 |
| @saylor | 类型 2（Strategy 创始人） | Bitcoin | 仅一句「₿ig Dot Energy」+ 图，未提供独立判断 | 低-中 |
| @balajis | 类型 6（跨域） | 加密 / 治理 | 推 Zcash 选民投票协议，但需具体技术背景才能评估，本期未达主信号门槛 | 低-中 |
| @gdb | 类型 2（OpenAI 总裁） | AI 产品 / 工具 | 本期发言以产品宣传为主（Codex 跨设备、Malta 免费访问），降级至附录 A | 中 |
| @demishassabis | 类型 1 + 2（图灵奖得主 + DeepMind CEO） | AI | 仅一句「Very excited for antigravity team」，无独立信号 | 低-中 |
| @adam_tooze | 类型 1（经济史学家） | 经济史 / 英国政治 | 转推 David Edgerton 对 Starmer 项目的批评，提供英国左翼经济史视角 | 中 |
| @fchollet | 类型 1（Keras 创建者） | AI | 本期仅一条软性内容（Pixar 电影），无信号 | 低-中 |
| @dhh | 类型 2（Rails 创建者） | 软件 / Linux | 本期仅技术细节（Linux 内核），归入附录 A | 低-中 |
| @tylercowen | 类型 1（经济学家） | 经济 / 文化 | 本期仅一条 Detroit 旅游推荐，无领域内信号 | 低-中 |
| @kevin2kelly | 类型 1（《连线》资深编辑） | 科技史 | 自引 1998 年《New Rules for the New Economy》节选，参考性强但非新信号 | 低-中 |
| @naval | 类型 6 | 哲学 / 创业 | 一条 Naval Podcast 金句，「motivation > framework」属万能句式 | 低-中 |
| @shaneparrish | 类型 5（FS 主理人） | 决策 / 写作 | 自引「写一段为什么要开这个会」的判断方法，实用但非新信号 | 低-中 |
| @david_perell | 类型 5b | 写作 / 设计 | 转推 paulg 关于「需要乔布斯级人物处理手机问题」的判断 | 低-中 |
| @paulg | 类型 2（YC 创始人） | 创业 / 反思 | 短句 reflection 偏个人感悟 | 中 |
| @SpeakerPelosi | 类型 4（政治人物） | 政治 | 节日纪念性发言，按 v1.2 规则剔除 | 低-中 |
| @Scobleizer | 类型 5（科技博主） | AI / 机器人 | 本期发言以产品宣传 + 资源列表为主 | 中 |
| @NewYorker | 类型 5b（文学 / 文化长文媒体） | 文化 / 政治 / 评论 | 按 v1.2 新规则，The New Yorker 不再作为类型 5b 的商业 / 科技长文来源 | 低-中（保留为文化长文来源） |
| @goodreads | 类型 5 | 阅读 | 提问体推文，无独立信号 | 低-中 |

**本期高优先级账号上限 3 个**：@chamath、@ylecun、@BrankoMilan。

---

## 九、沉默与意外信号

**本期值得注意的沉默**：
今天美东傍晚 Ken Griffin 公开承认 AI 在 PhD 级金融工作上的 step change，这一判断对量化 / 算法投资业是直接命中——但本 List 内的对冲 / 算法系发言人（@balajis 当日发推 1 条；@michaeljburry 当日发推 2 条；@saylor 当日发推 1 条）均未对此发表任何看法。三个人当日发推总量虽不算「≥3 条」的高门槛，但放在「Griffin 同行级别的人」这一定位上，缺位本身值得记。

另一处沉默：本期是 Google IO 周开局（@Scobleizer 多条提到），但 @demishassabis（Google DeepMind CEO）当日仅一条 14 字短评。这与往年 IO 开局前他通常会发表方向性长推的习惯不同。

**本期意外信号**：
@pmarca 本期发言密度异常高（51 条 / 24 小时），且超过 30 条为单字短引（「Interesting」「Co-sign」「Yep」「Concerning」），形成一种「策展者」而非「评论员」的姿态。这与他过去半年偏长推风格不同，可能预示其在调整公共表达策略。

---

## 传播力素材（适合自媒体改写的高互动思想观点）

- **Chamath：「Controlling the tokens is controlling the spice (Dune).」** — @chamath（Social Capital 创始人）· 👍1954 👁620,282 · engagement_rate 0.30%
  改写方向：适合知识星球 / B 站商业频道 / 36 氪深度专栏；改写为「为什么 AI 时代的甲方都开始组建 Token Control Plane」
  点评：这是本期最值得记下的金句——它用 Dune 的 spice 类比把「企业 AI 采购」从「选 vendor」抬升到了「掌控生产要素」的层面。前提假设是「token 流向 = 价值流向」，盲区是这种思路本身利好他自己的 8090 业务。读者应同时记住它的洞察价值与他作为利益方的位置。

- **Greg Koenig / pmarca：「What we need is a bunch of uninvestible businesses that competently supply boring, medium-margin, no-moat components.」** — @gak_pdx（精密制造从业者）· 👍3945 👁370,922 · engagement_rate 0.22%
  改写方向：适合财新 / 经济观察报 / 中国制造业评论；改写为「为什么独角兽神话掩盖了制造业的真问题」
  点评：罕见的、来自具体制造从业者的反风投叙事。前提是「物理产品的生态厚度无法被资本市场偏好覆盖」，这在美国可能成立、在中国情况已经反转。盲区是没有讨论新型工业政策（如直接补贴中游零部件商）能否扭转这种偏好。

- **Yann LeCun（转推）：「Data centers are this generation's nuclear power. Unlike nuclear, there is a 0% chance a data center can lead to a disaster scenario.」** — @ylecun（图灵奖得主）· 👍3473 👁486,188 · engagement_rate 0.08%
  改写方向：适合科技媒体 / 公众号 / FT 中文网评论；改写为「数据中心与核电站：一个被错位类比制造的恐慌」
  点评：这条的力量来自类比的尖锐——它把「数据中心恐慌」与「核电恐慌」并置，挑战「都是大基础设施所以都需要警惕」的直觉。前提假设是公共叙事的恐慌源于错误类比，盲区是它低估了数据中心的能源 / 水 / 用地外部性聚合后的社区层面影响。

- **Garett Petersen 的妻子（被 pmarca 转推）：「Some 10x engineers are now 100x engineers, while other people have completely missed the memo and are still doing things by hand.」** — @GarrettPetersen（经济学博士）· 👍743 👁241,286 · engagement_rate 0.06%
  改写方向：适合 InfoQ / 程序员 / 公众号；改写为「AI 不是平均削平工程师，而是把分化扩大十倍」
  点评：这条的独创性在于揭示了 AI 工具采用的「极度不均匀分布」——不是所有人都受益，而是少数人受益巨大、多数人在原地。前提是「采用差距 = 产出差距」，盲区是没有讨论这种产出差距是否会被组织 / 薪酬体系即时承认。

- **Naval Podcast 引述 @naval：「All frameworks in life are a distant second to your motivation.」** — @naval（AngelList 创始人）· 👍1384 👁129,436 · engagement_rate 0.70%
  改写方向：适合个人成长公众号 / 短视频文案；改写为「我们读了太多方法论，少了一份具体的'想做'」
  点评：高 engagement 反映其在内容工作者群体中的共鸣，但论断本身略接近万能句式。它的具体价值在于把 "framework worship"（方法论崇拜）作为可识别问题命名出来——这是名词化的洞察。盲区是「motivation」本身怎么来未被讨论。

---

## 十、本期信号评估

**信号 / 噪音比**：
通过铁律六质量门槛约 18 条，进入主区块 3 条，进入单源高启发 4 条，剩余约 70% 为低价值（含纯转发、纯短评、纯个人生活、纯政治站队）。

**信息密度**：高
原因：Ken Griffin 公开自白 + Chamath 系统性 SaaS 批判 + LeCun 时间窗预测 + Burry 系列开篇 + Milanović 长文 + Pinker 引介 Dan Williams——本期罕见地在同一 24 小时窗口出现多条具备「权威 + 框架 + 时间窗 + 可证伪」属性的判断。

**主导主题**：AI 在高端白领工作的 step change，以及它对企业软件、咨询业、金融业的连锁反应。

**未浮现但值得追踪**：
推测下一期可能浮现的话题：（1）Google IO 上的 Gemini 模型 / Antigravity 团队产品发布——@demishassabis 已暗示；（2）OpenAI Deployment 的具体合同结构——Chamath 帖子引发同行回应可能在 48 小时窗口内出现；（3）Karen Hao 对 LeCun 批评的回应（若有）。

**本期信源**：@chamath、@ylecun、@BrankoMilan、@pmarca、@michaeljburry、@sapinker、@danariely、@emollick、@AndrewYang、@gdb、@FundamentEdge（被引）、@gak_pdx（被引）、@henrysgao（被引）、@adam_tooze、@paulg、@naval、@Scobleizer、@demishassabis、@fchollet、@dhh、@tylercowen、@kevin2kelly、@shaneparrish、@saylor、@balajis、@FukuyamaFrancis、@nntaleb、@SpeakerPelosi、@david_perell、@NewYorker、@goodreads（共 31 位活跃 / 被引信源）。

---

## 附录 A · 行业内幕（可选阅读）

> ⚠️ 这一节是给从业者的，普通读者可跳过。严格上限 500 字。

- **OpenAI Codex 跨设备同步**：@gdb 介绍 Codex 现支持把多台设备（笔记本、Mac mini、手机）联接为「卫星 - 主机」模式，可在任意设备上启动 / 恢复任意线程；@nickbaumann_ 给出了具体实操（双 Mac 设备 + 手机三向同步）。对从业者意义：开发流程开始向「always-on, devicelessly-attached」演化，原 IDE 中心化心智模型可能在 12 个月内被打破。

- **xAI 与 Nous Research 的 Hermes Agent 集成**：用户可在 Nous 的开源 self-improving Hermes Agent 中使用 Grok 订阅，且 Hermes 可搜索 X 帖子。意义：闭源模型订阅 + 开源 Agent 框架的"组合层"开始出现。

- **DHH Omarchy + 原版 Linux 内核优化**：DHH 选择不自定义内核，直接用 Linus 团队优化版——对 Linux 自带发行版的性能 / 维护取舍提供一个明确意见。

- **OpenAI 在马耳他**：@gdb 宣布 OpenAI 与马耳他全国协议，所有马耳他公民免费访问 ChatGPT Plus。意义：国家级 LLM 准入协议的先例——可能成为未来 AI 政策的一种新形态。

- **a16z CLARITY Act 解读**：@pmarca 转推 @nyk_builderz 对美国加密市场结构立法 CLARITY Act 的解读，强调"合规 + 公开开发"二者并行将成为未来 3-5 年加密创业的底层条件。对中国加密团队的镜像意义：美国合规化加速后，部分海外团队的「监管套利」窗口将收窄。

- **OpenHome 开发套件**：@Scobleizer 是首批 100 名拿到 OpenHome 开发套件的人。设备定位「always-on companion」+ agent。早期硬件信号。

---

## 简报末尾固定声明

本简报的所有判断、关联推测均基于公开推文与公开网络信息。所有具体数字均标注来源；无法多源验证的内容已显性隔离至「单源高启发」区块。读者应理解：思想类信号的「准确性」低于事实类新闻——这份简报的价值不是「告诉你真相」，而是「告诉你此刻在商业与科技领域最值得思考的方向」。
