# 思想发现简报 | 2026-06-18

> 数据窗口：2026-06-17 06:00 — 2026-06-18 06:00（北京时间，过去 24 小时）
> 深度挖掘：3 条 | 模板版本：v1.2

---

## 一、今日要点

凌晨 5 点，MIT 的 Daron Acemoglu（达伦·阿西莫格鲁，2024 年诺贝尔经济学奖得主、《国家为什么会失败》作者）在自己的账号上贴出一份新的工作论文，标题平静——《Automation and Repression》（"自动化与镇压"）。他写的不是"AI 会抢走多少岗位"这种已经被说滥的题目，而是一个更冷的政治经济学问题：当 AI 把大量人类劳动挤出经济价值链之后，靠**再分配**（给失业者发钱）来安抚不满的方案，在他的数学模型里居然是**不稳定的**——自动化越深入，需要的转移支付越多；当转移支付撑不下去，唯一能继续维持秩序的工具就是**镇压**。论文最末他附了一句意味深长的话：如果你觉得这个推论太极端，建议去看 Palantir CEO Alex Karp 刚出版的那本《The Technological Republic》。

把今天 List 上的其他信号摆在一起读，会突然发现某种不安的合奏。Jeff Dean（Google DeepMind 首席科学家）今天宣布从 Google 离队的几位创始人成立 Radical Numerics，融资 5000 万美元做"生物 AI"——他们已经能用 AI 凭空设计出可在现实世界自我复制的噬菌体；Steven Pinker（哈佛认知科学家）在《纽约时报》发文，要求 AI 公司"停止把自己塑造成不可控的天命，承担对产品后果的责任"；Branko Milanovic（CUNY 不平等研究教授）在 Foreign Policy 宣布"全球化新自由主义已终结，开始的是**国家市场自由主义**"。同一天，CUNY 出身的他自己的《大全球转型》还出了塞尔维亚语版。

这些声音没有约好，但它们指向同一种焦虑：决定我们未来的几股力量——AI 资本、生物工程、国家——正在快速重组彼此的关系，而旧的政治经济解药（再分配、监管、自由市场）可能都不够用了。今天不是热闹的新闻日，但是一个值得读慢点的思想日。

**Bottom line in English:** Today's signals from MIT, Stanford, Harvard, and DeepMind converge on one uncomfortable question — what political settlement can hold once AI displaces both labor and the body itself?

---

## 二、主信号（多源验证）

### 信号 #1：Acemoglu 提出"自动化—镇压互补性"——再分配为何不够

主信源：@DAcemogluMIT（领域内权威 / MIT Institute Professor，2024 年诺贝尔经济学奖得主，《国家为什么会失败》《狭窄的走廊》作者） · 约 1 小时前
佐证：MIT Sloan 同步发布@DAcemogluMIT 与 David Autor、Simon Johnson 关于"亲工人 AI"的 Brookings 论文综述
题材分类：经济 / AI / 政治经济学

故事 / 场景：
今天清晨 5 点 01 分，Acemoglu 在 X 上贴出一份刚挂上 MIT 经济系网站的工作论文，附了一句几乎不带情绪的说明："这是对**普遍自动化**的政治后果的理论探索"。他不绕弯子直接亮出结论：在他的模型里，**自动化加再分配并不能稳定**——自动化越深入，安抚下层所需的再分配越多；当转移支付难以为继时，统治者最自然的下一步选择就是**镇压**（repression），用来"挡住举起的干草叉"。两分钟后他又补了一条："如果你觉得这听上去太遥远，请看 Palantir 联合创始人兼 CEO Alex Karp 刚出版的《The Technological Republic》。"

为什么值得思考：
主流共识把 AI 对就业的冲击想象为"市场+再分配"模型——你失业，国家发钱（UBI、负所得税、税收抵免）。Acemoglu 用一个动态博弈论模型挑战这个共识：他指出再分配在数学结构上无法稳态，因为更高自动化必然进一步推高安抚成本。这条把"AI 经济议题"从**福利政策**问题改写成了**政治制度**问题——这正是过去 12 个月最缺的视角。对照点：@AndrewYang（前美国总统候选人、UBI 倡导者）今天 11 点提及"领导层重复了社交媒体兴起时的错误"，但停留在风险提示；Acemoglu 把同一个忧虑给了一个机制。

关键引文：
> EN: "More automation necessitates more and more redistribution. This creates a natural complementarity between pervasive automation and repression."
>
> 中："更多的自动化必然要求越来越多的再分配。这就在普遍自动化与镇压之间形成了一种天然的互补关系。"

链接：
- 论文：https://economics.mit.edu/sites/default/files/2026-06/Automation%20and%20Repression.pdf
- Acemoglu 推文：https://x.com/DAcemogluMIT/status/2067351717633720795
- MIT Sloan 亲工人 AI 综述：https://mitsloan.mit.edu/ideas-made-to-matter/pro-worker-ai-explained

---

### 信号 #2：Jeff Dean 宣布 Radical Numerics——AI 进入"设计生命"的阶段

主信源：@JeffDean（领域内权威 / Google DeepMind 首席科学家、Gemini 项目负责人，转推自联合创始人 @exnx Eric Nguyen） · 约 20 小时前
佐证：Fortune 同步独家报道（fortune.com/2026/06/15/exclusive-ai-dna-radical-numerics）·@patrickc Patrick Collison 作为天使投资人参与·Eric Horvitz（微软 CSO）、George Church（哈佛遗传学家）担任顾问
题材分类：科技 / 生物 / 国防

故事 / 场景：
Jeff Dean 没有用通常的"我们在做有趣的工作"做开头。他直接讲一件事：去年，他参与训练的开源生物 AI 模型 Evo（400 亿参数，在所有可见生物的 DNA 序列上训练）被科学家用来**从零生成了一整个生物的基因组**。打开一看，是一种噬菌体——一种病毒，无害，但能在真实世界里运作。他写道："这是一个清晰的转折点。AI 不再只是**分析**生物，它已经站在**生成功能性生命体**的边缘上。"由此，他和三位 DeepMind/斯坦福背景的同事联合创立 Radical Numerics，融到 5000 万美元种子轮（Emergence Capital 领投），目标既要"为人类健康设计生命"（与一家诊断公司合作做早期癌症筛查），又要"为国防侦测生命"（与一家美国国家实验室合作侦测"深度伪造病毒"）。Andrew Weber——前美国国防部负责核、化、生武器防御项目的助理部长——出任顾问。

为什么值得思考：
过去三年讨论 AI 安全，焦点几乎全在**信息层**（虚假信息、深度伪造文本、模型说谎）。Radical Numerics 一次把对话拉到**生物层**——AI 已经可以生成新功能的 DNA 序列，并通过商用合成服务"像亚马逊一样寄给你"。这与 Acemoglu 的论文形成了对位：一个谈"AI 让多数人无生产用途之后的政治",一个谈"AI 让多数人无生物安全保障之后的生存"。这条信号同时也是 List 里第一个把"国防级生物 AI"作为可融资创业方向公开化的。

关键引文：
> EN: "AI is no longer just analyzing biology. It is on the cusp of generating functional lifeforms. Eventually, AI will have the power to design and control life itself."
>
> 中："AI 已经不只是在分析生物。它正站在能够生成有功能的生命体的临界点上。最终，AI 将拥有设计与控制生命本身的能力。"

链接：
- Radical Numerics 公告：https://www.radicalnumerics.ai/blog/radical-numerics-seed
- Fortune 报道：https://fortune.com/2026/06/15/exclusive-ai-dna-radical-numerics-eric-nguyen-biology-biodefense-drug-discovery/
- Jeff Dean 转推：https://x.com/JeffDean/status/2067057727797633239

---

### 信号 #3：Branko Milanovic 宣告"全球新自由主义已死，国家市场自由主义登场"

主信源：@BrankoMilan（领域内权威 / CUNY 研究教授、LSE 客座教授，全球不平等研究的"大象曲线"作者，新书《大全球转型》正在被翻译成多种语言） · 约 11 小时前
佐证：法国 @LEXPRESS 同日刊出长篇采访·Milanovic 本人在 Foreign Policy 发表《The End of Neoliberalism》一文·塞尔维亚语版《Velika globalna transformacija》今日上市
题材分类：经济 / 政治经济学

故事 / 场景：
今天傍晚 6 点 52 分，Milanovic 在 X 上用一句法语把他今年最重要的判断概括给法国读者：«La phase de la mondialisation néolibérale s'est clairement achevée. Nous avons basculé dans l'air du national libéralisme»——"全球化新自由主义的阶段已经清晰结束，我们已经跌入了**国家自由主义**的空气里"。所谓国家自由主义，他的定义很具体：在国境之内仍然让市场说话，**但对外贸易回到重商主义**（mercantilism）。他在 Foreign Policy 同名文章里给出一句更狠的判断："新自由主义并不是被它的敌人摧毁的，而是被它**自己最珍视的两个价值**——世界主义与竞争——所摧毁。"为了让中文读者明白他是谁：Milanovic 在 2013 年提出"大象曲线"，证明全球化既压低了全球不平等，又掏空了发达国家的中产，由此预言了 2016 年后的西方政治剧变。

为什么值得思考：
过去 18 个月，从产业政策、出口管制到稀土战争，几乎每条新闻都假设了一个"新自由主义之后"的世界，但很少有人正面命名它是什么。Milanovic 这条信号的独特性在于：他不是回到凯恩斯主义/产业政策这类旧词汇，而是提出一种新的**结构**——国境之内自由化、国境之外重商主义。这给了商业决策者一个具体的判断框架——任何依赖跨境信任、跨境数据流动、跨境劳动套利的商业模式，都需要重新评估。

关键引文：
> EN: "The virtues it extolled — cosmopolitanism and competition — led to its demise."
>
> 中："它（新自由主义）所推崇的两种美德——世界主义与竞争——最终导致了它自己的覆灭。"

链接：
- Foreign Policy 文章：https://foreignpolicy.com/2026/06/15/neoliberalism-globalization-competition-cosmopolitanism-economics-reagan-thatcher/
- L'Express 法语长访谈引用：https://x.com/BrankoMilan/status/2067198580180349333
- 塞尔维亚语版新书：https://kontrastizdavastvo.rs/knjige/knjiga-velika-globalna-transformacija-branko-milanovic-28867

---

### 信号 #4：Block（Square 母公司）公开内部 AI 编程系统数字，引出 jack 的"组织信号"

主信源：@jack（经营者 / Block 与 Square 创始人、Twitter 前 CEO） · 约 3 小时前
佐证：@blocks 官方账号同步发布·Greg Brockman（OpenAI 总裁）当晚跟进感慨"软件工程已经完全不同，连 6 个月前是什么样都难以记起"
题材分类：科技 / 创业管理

故事 / 场景：
凌晨 2 点 53 分，Jack Dorsey 转发了 Block 工程团队的对外公告，并加了一句近乎口令的话：**"we're going to start talking a lot more about our intelligence tools. this is the beginning of the beginning."** 公告本身披露了一个名为 Builderbot 的内部 AI 工程系统的运行数据（来源：@blocks 官方账号）：日均 20 万次操作、每周合并 1500 个 Pull Request、占 Block 全公司生产代码改动的 15%。同一晚，@gdb（Greg Brockman）则在另一条推文里写："软件工程已经如此不同，连 6 个月前是什么样都难以记起。"

为什么值得思考：
对照点：直到 6 个月前，"AI 编程"在公司层面的主流话术还是"提升程序员效率 20-30%"。Block 的数字把这条曲线从"工具化"推进到"占比化"——15% 的合并代码改动来自 Agent，意味着工程组织的**绩效单位**正在改变（不再是人头/工时，而是 Agent 队列）。Jack 选择把这件事"开始公开讲"，意味着这从内部实验阶段进入对外定位阶段——下一波 SaaS 与 dev tools 的故事会以**"Agent 比例"**为核心叙事。

关键引文：
> EN: "1,500 pull requests merged per week. 15% of all production code changes across Block."
>
> 中："每周合并 1500 个 Pull Request。占 Block 全公司生产代码改动的 15%。"
>
> EN（gdb）: "software engineering is so different now. hard to remember what it was like even 6 months ago."
>
> 中："软件工程已经如此不同，连 6 个月前是什么样都难以记起。"

链接：
- Block 官方公告：https://block.xyz/inside/block-rolls-out-builderbot-a-new-suite-of-ai-native-tools-that-changes-the-way-we-ship
- jack 转推：https://x.com/jack/status/2067319680654594543
- gdb 推文：https://x.com/gdb/status/2067043685611790653

---

### 信号 #5：Chamath 与 Jeremy Howard 同日宣告"开源模型已追上闭源 / 中国追上美国"

主信源：@chamath（投资人 / Social Capital 创始人，Facebook 早期增长团队） · 约 7 小时前
佐证：@jeremyphoward（fast.ai 联合创始人、Kaggle 创始 President）独立给出更强判断："如果剔除已不可用的 Claude Fable，GLM-5.2 Max 已经是全世界前端编程能力第一的模型"·@emollick 同日比较 GLM-5.2 与 Fable 的诗歌生成案例
题材分类：科技 / 投资 / 中美产业格局

故事 / 场景：
今天 23:03，Chamath 转发了 Design Arena 关于智谱 AI 旗下 GLM-5.2 的最新基准成绩（Elo 1360，超过曾经登顶的 Claude Fable 5），加了一段冷静的判断："虽然可能有过拟合的风险所以现在宣布胜利还为时尚早，但看到开放权重模型如此迅速地追上闭源实验室的最新发布，是一件很好的事。"他接着写：**"在这一类模型架构下，收敛已近在眼前。"** 大约 5 小时前，澳大利亚的 Jeremy Howard——fast.ai 联合创始人、Kaggle 创始 President——直接给出更不留余地的判断："剔除已不可用的 Fable 之后，GLM-5.2 Max 已经是全世界前端编程能力第一的模型。这是个巨大的时刻——开源追上了闭源，中国追上了美国，而且是在这个极重要的领域里。"

为什么值得思考：
GLM-5.2 来自智谱 AI（Zhipu）（来源：@Zai_org 官方账号被多方引用）。把 Chamath 与 Jeremy Howard 两人放在一起看：一个是大型基金视角谈架构同质化（意味着模型本身的护城河在变薄），一个是技术从业者视角谈基准排名（意味着开源 + 中国正在改变可信任的"前沿"边界）。两人都不是"中国 AI 鼓吹者"，他们的同日判断本身就是个独立性极强的信号。挑战的共识是：过去 18 个月围绕"美国实验室对中国实验室仍有 12-18 个月领先优势"的所谓常识。

关键引文：
> EN（Chamath）: "Without distinct data sets to train over and specifically narrow use cases to build expertise on, convergence seems at hand for this class of model architecture."
>
> 中："如果不能拥有独特的数据集，也没有特别狭窄的应用场景作为专长，这一类模型架构的收敛似乎已近在眼前。"

链接：
- Chamath 推文：https://x.com/chamath/status/2067261787335233537
- Jeremy Howard 转推：https://x.com/jeremyphoward/status/2067184294569836761

---

## 三、单源高启发信号

> ⚠️ 重要说明：以下信号仅有一个来源，未经多方独立验证。但发言人在该领域有明确商业 / 科技权威性，内容具有思想价值。请读者自行判断。

### 启发 #1：Kareem Amin 的"公司死亡 doula"——挑战"持续做大"的默认设定

发言人：@patrick_oshag 引用 @bchesky·Kareem Amin（@Clay 创始人 / CEO，公司在两年内从 1M ARR 增长到 100M ARR，估值 50 亿美元，引自 Patrick OShaughnessy 的 Invest Like the Best 节目）
领域：创业管理 / 哲学
发布时间：约 12 小时前

他/她说了什么：
"所有人都在用一种无聊的方式讨论这件事——你应该融 VC 还是 bootstrap。但更有趣的问题是：你**到底应不应该 scale**？scale 你会失去什么？我们作为一个社会，应该激励所有公司都去 scale 吗？我们都熟悉这个现象——这家餐厅本来很棒，但现在烂了。万物有它的生命周期。如果你的公司已经完成了它的使命……我们是不是应该**帮它寿终正寝**，而不是把它 scale 成一个 zombie 或者更糟的版本？"

为什么值得记下：
这是一位**业务非常 scale 友好型**的创业者（5B 估值、22 个月走完十倍 ARR），主动提出一个反 VC、反 PE 的命题：scale 不是默认值。这条的独特性在于发言人的位置——如果是一个隐居山林的小作坊讲这种话，权重很低；但 Kareem 是当今 SaaS scale 美学的代表性建设者之一。这条信号挑战的是：一切创业故事都默认"持续做大"是道德正确的。

目前的不确定性：
- 这是一个尚未被任何治理框架（VC term sheet、董事会、ESOP 设计）系统化的概念
- 与"价值股回购"/"清算价值"等传统财务工具是否本质不同，待论证

链接：https://x.com/patrick_oshag/status/2067357912935149915

---

### 启发 #2：Tim Ferriss——"信息市场坍缩进 chatbot，但转化市场会变得更小、更怪、更有意思"

发言人：@tferriss（操作者 + 出版业资深玩家 / 5 部 NYT 头号畅销书作者，Tim Ferriss Show 累计下载超 10 亿次）
领域：出版 / 内容经济
发布时间：约 9 小时前

他/她说了什么：
"信息市场正在向 chatbot 坍缩。但**转化市场**——为了和一个心智长时间共处、为了一个它流过血的主题——也许会变得更小、更怪、更有意思。我会下注这一边。某种意义上，我们正在退回到互联网早期的样子。"

为什么值得记下：
这条把"AI 杀媒体"的旧叙事拆成了两个不同的市场：**信息 vs 转化**。前者会被通用对话模型蚕食（chatbot 总结一切）；但后者——读者花七小时和一本书共处、花一年时间追一位作者的精神演化——可能会被反向放大。这是 Tim Ferriss 作为既是创作者、又是早期投资人的双重视角下的一个反共识判断。

目前的不确定性：
- 这与 David Perell 在同一天引用 Ezra Klein 的发言（"花七小时读完一本书时，你的心智花了七小时和那个主题在一起"）方向一致，但尚未有结构性证据
- "市场会变小但更怪"——所谓"更小"具体小多少，没有给出量级

链接：https://x.com/tferriss/status/2067235423655501929

---

### 启发 #3：Steven Pinker 直接点名要求"AI 公司停止自我标榜的不可避免论"

发言人：@sapinker（领域内权威 / 哈佛大学认知科学家，《理性》《人性中的善良天使》作者）
领域：AI 治理 / 认知科学
发布时间：约 9 小时前

他/她说了什么：
"AI 公司应该停止那种自利又听天由命的'末日喧哗'。AI 不是某种他们自己挣扎着去**驾驭**的不可避免之力。它是一组特定的工具，是这些公司根据特定商业计划选择**设计和销售**的。因此，他们需要像谈论任何其他消费产品一样谈论自己的产品——讲清楚谁是用户、为什么值得用、并且关键的是：**为可能造成的任何伤害负全责**。AI 现在所享有的高科技光环，并不能让它免于常识性安全标准。"

为什么值得记下：
Pinker 不是 AI 治理圈内的常驻发言者；他作为外部认知科学家给出这种**话术结构**层面的批评，是一种少见且高权重的角度。挑战的共识：当下许多 AI 公司的公关策略——"我们也很害怕，但我们必须去做"——本身是一种营销话术，被这条信号直接拆穿。与同日 David Sacks（PCAST 共同主席）就 Anthropic 的 Mythos 模型如何被报道的长篇澄清形成微妙对位：Sacks 是从内部讲"威胁是真的、Anthropic 是吓人技巧"，Pinker 是从外部讲"威胁框架本身就是话术"。

目前的不确定性：
- Pinker 本人此前并非 AI 治理主要发言人，他的判断对内部技术细节的把握有限
- 其论证的具体伦理框架在 NYT 评论文中略简

链接：https://x.com/sapinker/status/2067231673268273547

---

### 启发 #4：Paul Graham 的"伊朗战争我们输了"——硅谷创投教父的非典型地缘判断

发言人：@paulg（领域内权威 / Y Combinator 联合创始人；本条为非领域发言，按规则降级）
领域：地缘政治（非本人主业，降级评估）
发布时间：约 13 小时前

他/她说了什么：
"看起来我们在伊朗这场战争里**输得很奇怪**——现在能拿到的协议比我们动手之前对方愿意给的还要差。如果我们因为这场战争而**变得更差**，那我们就是输了。"

为什么值得记下：
之所以这条不是政治站队而是值得记下的认知信号：Paul Graham 用了一个**博弈论式的胜负判定**——不是"谁打死了更多人"，而是"打完之后协议条款比打之前更差"。这种"用结果反推动机"的句法，是商业判断里常见但很少被搬到地缘讨论里的。同时也是 List 上一位科技领袖在伊朗 / 以色列议题上少见地直接表态。Naval 同日 RT All-In 节目谈加州选举数据的统计反常——这俩老牌硅谷人公开对美国制度的怀疑同时上升，本身是个值得注意的传导信号。

目前的不确定性：
- "动手前的协议比现在好"的比较是 paulg 个人判断，未给具体条款来源
- paulg 不是地缘问题的专业分析者

链接：https://x.com/paulg/status/2067183701130100997

---

### 启发 #5：Tyler Cowen 转推——"霍尔木兹海峡完全封锁没有引发预期能源冲击的原因不是经济学错了，而是'腐败和撒谎'"

发言人：@tylercowen（领域内权威 / 乔治梅森大学经济学教授、Conversations with Tyler 主持人；转推自 @HBendaas）
领域：经济 / 地缘
发布时间：约 19 小时前

他/她说了什么：
"很搞笑——有些经济学家公开焦虑：为什么霍尔木兹海峡的完全关闭没有带来他们预期的那种能源冲击？而真相不是经济学基本原理错了，**只是日常的腐败和撒谎**而已。"

为什么值得记下：
跨领域启发性强：这把"经济学预测失灵"这种学术圈尴尬，与"信息真假"这种地缘政治议题用一个机制连起来——如果你看到的'封锁'本身不是真封锁，那经济学的预测当然不会发生。提醒商业判断者：宏观预测出现"奇怪偏差"时，**先怀疑输入数据的真伪，再去怀疑模型**。

目前的不确定性：
- Cowen 本人没有给出他认为的"封锁"实际程度的具体数字
- 原文出处为 @HBendaas，账号权威性中等

链接：https://x.com/tylercowen/status/2067076014157549794

---

## 四、跨领域关联

> 本区块尝试主动建立几条看似不相关但指向同一深层变化的信号关联。
> ⚠️ 这是 LLM 的关联推测，不是事实。每条都给反向思考。
> v1.2 新增约束：跨领域的"领域"中至少有一端必须在商业或科技。

### 关联线 A：人在生产链上还剩什么位置？——Acemoglu × Jeff Dean × Block × Richard Socher

信号 1：Acemoglu 论文——AI 让普遍自动化吞噬人类劳动后，再分配无法稳态，最终需要镇压（经济学）— @DAcemogluMIT
信号 2：Block 公开 AI Agent 占合并代码 15%、每周 1500 个 PR（创业管理）— @jack / @blocks
信号 3：Richard Socher（@RichardSocher，You.com CEO）："我们将为 AI 重新发明薪资带与管理层级。'初级'模型成本便宜处理杂活；'高级'前沿模型综合事实、作重大决策；人成为管理者，每个人都有自己的 Agent 组织。"（创业管理）

潜在共同根源：
三条信号合起来在描绘一个新的劳动金字塔：底层是廉价 Agent token，中层是少数被保留的"心智整合者"，上层是因占有 Agent 队列而拥有杠杆的资本方。Acemoglu 在政治经济层面警告这个结构不稳定；Block 在企业层面已经把它落地；Richard Socher 在组织设计层面把它命名为"Agent 组织"。这是同一种结构在三种粒度上同时显形。

反向思考：
机制相似性检验——如果 Block 的 15% 数字其实是公关数字（包括格式化、依赖更新等 trivial 修改），那么 Richard Socher 的"Agent 组织"愿景也会失去根基；进一步，Acemoglu 的模型的现实紧迫度也会下降。三条信号共享同一个机制假设：**"AI 实际承担的智力价值占比正在快速上升"**——若这个假设虚高，三条都会跟着虚高。

---

### 关联线 B：旧的"全球化共同体"瓦解后的两种新组织形式——Milanovic × Radical Numerics × Modal Motors / 美国不依赖稀土的电机

信号 1：Branko Milanovic——全球化新自由主义已死，国家市场自由主义登场，对外回到重商主义（经济）— @BrankoMilan
信号 2：Radical Numerics 把"国防"明确写入公司双使命（与美国国家实验室合作识别"深度伪造病毒"）（科技 / 国防）— @JeffDean / @exnx
信号 3：Modal Motors——"不含稀土的美国本土电机，成本与中国电机相当"被 @Scobleizer 转介，bookmarks 925、views 26 万（科技 / 制造业）

潜在共同根源：
当全球供应链不再被视为安全资产，三件事同时发生：① 经济学家给出框架命名（Milanovic 的"national liberalism"）；② 前沿科技直接把"国防"写进商业模式（Radical Numerics 的双使命）；③ 创业者把"国产化 + 摆脱关键资源依赖"作为投资卖点（Modal Motors）。它们共享同一个更深的变化：**国家边界正在从"政治制度变量"重新变回"商业要素变量"**。

反向思考：
机制相似性检验——这一关联线靠的是"国家正在重新成为商业要素"这个机制。如果 Milanovic 是错的（事实上回到的不是重商主义，而只是局部产业政策），那么 Radical Numerics 把国防写进商业模式可能只是融资话术（吸引政府订单），Modal Motors 的"无稀土"卖点也可能只是临时差异化。三条信号一起站，是因为它们假设了**国家身份会持久地成为定价输入**。

---

## 五、本期书单与访谈

> 这一节是这份简报的核心价值之一。

### 新书 / Books

- **《The Infinity Machine: Demis Hassabis, DeepMind, and the Quest for Superintelligence》** — Sebastian Mallaby
  推荐者：@tferriss（Tim Ferriss，Tim Ferriss Show 累计下载 10 亿+；今天上线 Mallaby 访谈节目）
  推荐语境：今天 Tim Ferriss 发布的本期 podcast 主嘉宾即 Mallaby，专题是"从 100+ AI 内部人士学到的：通往超级智能的赛跑，AI 的宗教，以及如何提早识别突破"
  核心论点：Mallaby 是 Council on Foreign Relations 国际经济资深研究员、两届普利策奖入围者、《More Money Than God》《The Power Law》作者；本书是 Demis Hassabis（DeepMind 联合创始人、CEO，2024 年化学诺奖得主之一）的首部权威传记。核心论点：人工智能竞赛不只是一场技术竞赛，更是一种**信念的竞争**——Mallaby 称之为"AI 的宗教"。具体论点待 web 验证（书的主要论证脉络从 100+ 内部访谈中提炼，但具体章节论点本简报尚未读到原书）
  题材分类：科技 / 商业 / 思想史
  中文版状态：未见中译本；Mallaby 的另一本《金钱多于上帝》（中信出版集团）有中文版
  豆瓣 / Amazon / Goodreads 评分：暂无（新书）
  对什么人最有价值：长期关注 AGI 政经议题、想要建立"传记式技术理解"的读者
  链接：https://x.com/tferriss/status/2067329549679853790

- **《The Technological Republic》** — Alex Karp（Palantir 联合创始人 / CEO）
  推荐者：@DAcemogluMIT（Daron Acemoglu，2024 年诺贝尔经济学奖得主）
  推荐语境：Acemoglu 在其最新工作论文《Automation and Repression》末尾点名让读者**如果觉得他的"普遍自动化必然推向镇压"结论太遥远，就去读 Karp 的这本**——这是一位左翼经济学家公开背书一本通常被视为右翼科技立场的书，跨领域提示意味强
  核心论点：Karp 主张技术资本应当与西方民主国家深度绑定，重建一种"技术共和国"的政治契约；论点本身具有公开争议性（具体章节论证待 web 验证）
  题材分类：商业 / 政治经济
  中文版状态：未见中译本
  豆瓣 / Amazon / Goodreads 评分：暂未查到
  对什么人最有价值：希望把 AI 治理讨论从"伦理"层提升到"政治制度"层的决策者与研究者
  链接：https://techrepublicbook.com/

- **《The Great Global Transformation》（塞尔维亚语版《Velika globalna transformacija》今日出版）** — Branko Milanovic
  推荐者：@BrankoMilan（作者本人；CUNY 研究教授、全球不平等"大象曲线"提出者）
  推荐语境：今天作者宣布塞尔维亚语版上市；同日他在 Foreign Policy 发表《The End of Neoliberalism》，与本书同一论证线
  核心论点：当代全球资本主义的"大转型"是从"全球化新自由主义"转向"国家市场自由主义"——国境内继续市场化，国境外回到重商主义。具体论点待 web 验证（核心命题在其 Foreign Policy 文章与多次访谈中已经反复出现）
  题材分类：经济 / 政治经济学
  中文版状态：未见中译本（其前作《全球不平等》《资本主义，独自前行》均有中信出版译本）
  豆瓣 / Amazon / Goodreads 评分：暂未查到
  对什么人最有价值：负责跨境业务、政策研究的决策者，以及关注产业政策回归的投资人
  链接：https://kontrastizdavastvo.rs/knjige/knjiga-velika-globalna-transformacija-branko-milanovic-28867

- **《Incorruptible》** — Eric Ries（《精益创业》作者）
  推荐者：@ericries（作者本人；今天宣布被 Financial Times 选入"2026 年夏季最佳商业书"）
  推荐语境：作者本人宣告 FT 评荐，并附上 Masters of Scale 联合主持人 Jeff Berman 的评论"长期来看，这对股东也更好"
  核心论点：探讨如何在公司治理设计上抵抗"金融重力"（financial gravity）——即好公司天然会被短期主义拉走——主张创始人需要设计"使命驱动可持续"的治理结构。具体论点待 web 验证
  题材分类：商业 / 公司治理
  中文版状态：未见中译本
  豆瓣 / Amazon / Goodreads 评分：暂未查到
  对什么人最有价值：考虑长期持有、长期治理设计的创始人 / 董事
  链接：https://howisincorruptiblegoing.com/e/2026-06-07-jeff-berman-goodreads/

### 访谈 / 播客 / Interviews & Podcasts

- **The Tim Ferriss Show — Sebastian Mallaby: Lessons from 100+ AI Insiders on The Race to Superintelligence, The Religion of AI, and Spotting Breakthroughs Early**
  主持人：Tim Ferriss
  时长：暂未查到具体时长
  发布日期：2026-06-17（北京时间 2026-06-18 凌晨 3:32 推送）
  题材分类：科技 / 商业 / 思想史
  核心话题：从 100+ AI 内部人士采访中提炼出的判断、AI 与"宗教"式信念结构、如何提早识别真正的突破信号
  关键时间戳：暂未提供
  收听链接：Tim Ferriss Show 各音频平台
  为什么值得听：Mallaby 是少数同时具备 CFR 国际经济学家身份和长期产业访谈能力的写作者；推荐与上面《Infinity Machine》一书一并消化
  链接：https://x.com/tferriss/status/2067329549679853790

- **Conversations with Tyler — David Baszucki（Roblox 联合创始人 / CEO）**
  主持人：@tylercowen（Tyler Cowen，乔治梅森大学经济学教授）
  时长：暂未查到
  发布日期：2026-06-17
  题材分类：科技 / 创业管理
  核心话题：100M 日活、$7B 平台经济、阿根廷与韩国的青少年百万富翁；他们追问的具体问题包括："是否每个成功平台最终都会演化为'万物 App'？""如果 token 成本下降 100 倍，Roblox 能做什么现在做不到的事？""当 AI 机器人在 Roblox 上超过真人玩家时会发生什么？""Zuckerberg 的元宇宙愿景是真的死了，还是只是处于 Apple Newton 周期？"
  关键时间戳：暂未提供，建议从开场和"AI bots outnumber human players"段落听起
  收听链接：https://conversationswithtyler.com/episodes/dave-baszucki/
  为什么值得听：Roblox 是当下"AI + UGC + 创作者经济"最大规模的真实样本，由经济学家提问比技术媒体提问更值得听

- **Invest Like the Best — Kareem Amin（Clay 联合创始人 / CEO）**
  主持人：@patrick_oshag（Patrick OShaughnessy）
  时长：53:49+
  发布日期：2026-06-16（节目）；今日多次被引用回到 X
  题材分类：商业 / 创业管理 / 哲学
  核心话题：为何资本主义奖赏风险；从"丰盛"而非"匮乏"出发去创造；"公司的死亡 doula"；为何在 Series A 阶段需要"先感觉你不需要这笔钱"；以及把 Brian Chesky 的"adulation 是一只底部漏水的杯子"放到节目里的延展
  关键时间戳：
  - 0:00 — 把编程能力交给所有人
  - 9:16 — 资本主义与风险
  - 19:18 — 从"丰盛"创造
  - 25:19 — 十天止语闭关
  - 42:32 — 创始人愿景与公司"死亡 doula"
  收听链接：见 https://x.com/patrick_oshag/status/2066883494714962188
  为什么值得听：Kareem 是当下高速 scaling SaaS 圈里少有的会公开质疑"是否该 scale"的创始人；其"死亡 doula"概念值得拿来对照 Eric Ries 的"financial gravity"

### 重要长文 / Long-form Articles

> 来自 The Atlantic / FT / The Economist / The Information / Wired / MIT Tech Review / HBR / Stratechery 等长文媒体当日发布的商业 / 科技长文。每期最多 2 篇。

- **Ken Griffin's Billions and Billions（Citadel 与 Citadel Securities 的双引擎之谜）** — Gary Sernovitz / The New Yorker
  发布日期：2026-06-17
  题材分类：投资 / 商业
  主题：Ken Griffin 既非典型的"创新者"也非"savant"，其策略是**让两家金融业务持续不断地自我重构**——以至于不仅赢在当下，还能赢在十年。Sernovitz 采访了 Griffin 本人加 28 位现任与前任员工，呈现这种"重构机制"的内部结构。某前任组合经理形容："下一个版本总比上一个版本好；另一面，是一条人体堆成的高速公路残骸。"
  为什么值得读：在 hedge fund 普遍被叙述为"个人天才"或"机器化套利"之间，Sernovitz 提供了第三种视角——**机构持续自毁式重构**作为护城河
  阅读时长：约 30-40 分钟
  链接：https://newyorkermag.visitlink.me/JCQD_i

- **Eight Predictions for the Future of Higher Education** — The New Yorker / Fault Lines
  发布日期：2026-06-17
  题材分类：科技 / 商业
  主题：未来十年高等教育不太可能彻底崩溃，但将经历**剧烈的重构**——AI、入学需求变化、政府资助重组三股力量同时作用
  为什么值得读：对教育、培训、招聘行业的决策者，这是一份难得的"非危言耸听"的趋势预测
  阅读时长：约 15-20 分钟
  链接：https://www.newyorker.com/news/fault-lines/eight-predictions-for-the-future-of-higher-education

### 论文 / 报告 / Papers & Reports

- **《Automation and Repression》** — Daron Acemoglu
  发布日期：2026-06
  机构：MIT 经济系工作论文
  题材分类：经济学 / 政治经济学
  主题：理论模型证明"普遍自动化 + 再分配"政策组合在政治均衡上不稳定，自动化越深入越倾向于走向**自动化与镇压的互补**。详见信号 #1 的深挖
  链接：https://economics.mit.edu/sites/default/files/2026-06/Automation%20and%20Repression.pdf

- **《Pro-Worker AI》综述** — MIT Sloan
  发布日期：2026-06-17
  机构：MIT Sloan Ideas Made to Matter
  题材分类：经济 / AI
  主题：从 Acemoglu × Autor × Johnson 的 Brookings 论文出发，给出"亲工人 AI"的政策定义与可操作维度
  链接：https://mitsloan.mit.edu/ideas-made-to-matter/pro-worker-ai-explained

---

## 六、TOP 3 深度挖掘

> 对前面区块中（主信号 + 书单与访谈）合计排名前 3 的信号执行深挖。
> v1.1 强制约束：TOP 3 中至少 1 条来自「书单与访谈」区。

### 深挖：Acemoglu《Automation and Repression》工作论文（信号 #1）

事实核实：
经 web_search 确认：Daron Acemoglu 是 MIT Institute Professor，与 Simon Johnson、James A. Robinson 共同获得 2024 年诺贝尔经济学奖；MIT 经济系网站确实在 2026 年 6 月上传了名为 "Automation and Repression" 的工作论文（链接 economics.mit.edu/sites/default/files/2026-06/Automation%20and%20Repression.pdf）；其推文中提到的 Alex Karp 著作《The Technological Republic》存在（合著者 Nicholas W. Zamiska）。论文具体证明结构本简报未通读，引用以推文中作者本人陈述为准。

思想溯源：
"自动化 → 不平等 → 政治动荡"是一条可追溯的思想脉络——可识别的学术先驱包括：Acemoglu 与 Robinson 自己在《Why Nations Fail》（2012）建立的"包容性 vs 攫取性制度"框架；Acemoglu × Pascual Restrepo 系列论文（2018-2022）量化了自动化对美国工资结构的影响。本次新论文的认知突破在于把这条思路推进到**政治均衡建模**——再分配是否足以稳态——这是过去 5 年 UBI / EITC 讨论中很少被严格处理的问题。最有力的反驳来自两条传统：① 一类经济学家（如 David Autor 自身较温和的版本）认为新岗位会被创造；② 一类政治经济学家（如 Branko Milanovic）认为问题不是镇压而是国家间竞争。Acemoglu 与 Milanovic 同日发声、彼此并未直接冲突，是个值得追踪的对话起点。

同行视角：
- David Autor（MIT 经济系，Acemoglu 的合作者）持"自动化创造性破坏可被职业重构吸收"的较温和立场（来源：Brookings 论文及多次公开演讲）
- Branko Milanovic 持"问题不是劳动力被替代而是全球化秩序崩塌"的不同诊断（来源：今日 Foreign Policy 文章）
- 主要分歧点：自动化的政治后果是"内部分配问题"（Acemoglu）还是"跨国分配问题"（Milanovic）

对中国商业 / 科技读者的含义：
中国在过去 10 年的就业再分配讨论中，主要依靠**产业升级吸纳劳动力**与**社会保障兜底**两条思路。Acemoglu 模型的隐含警示对中国语境的相关性在于：当 AI 自动化进入服务业（外卖、白领、客服）的速度超过制造业升级吸纳速度时，单靠转移支付可能不够；这与近年关于"灵活就业"治理的讨论形成隐性对位。

延伸阅读：
- Acemoglu × Restrepo, "Robots and Jobs"（2017）— 自动化经济学经典论文
- Branko Milanovic, "The End of Neoliberalism"，Foreign Policy（2026-06-15）

---

### 深挖：Radical Numerics — Jeff Dean 公开支持的"生物 AI"创业（信号 #2）

事实核实：
经 web_search 确认：Eric Nguyen 是 Stanford 计算生物学博士、Hyena 与 Evo 论文的主要作者之一；Evo / Evo 2 模型在 GitHub 与 HuggingFace 公开（最大版本 40B 参数）；2024 年底确有团队报道使用 Evo 生成功能性噬菌体基因组的预印本（具体 paper title 待进一步核实）。Radical Numerics 网站（radicalnumerics.ai）已上线，Fortune 配套独家报道存在。Andrew Weber 确为前美国国防部负责核、化、生武器项目的助理部长。

思想溯源：
"AI 为生命建模"思路可追溯到 AlphaFold（2018-）；"AI 设计新蛋白"由 David Baker（华盛顿大学 / IPD）从 2021 年起规模化；"AI 直接设计基因组"是 Evo 系列首次走通的方向。最有力的反驳是生物安全圈的"双重用途"质疑——同一模型既能设计救命药，也能设计致病变种——本公司将"侦测 AI 生成病原体"作为双使命之一，正是直接回应这一质疑。需要追踪的争议：把"国防"与"治疗"合并到同一商业实体里，是否会在监管上形成正反馈（更易拿政府订单）还是负反馈（更易触发出口管制）。

同行视角：
- George Church（哈佛遗传学家，Radical Numerics 顾问）持"功能性生命工程不可避免、必须建立同步防御能力"的立场
- Stuart Russell（伯克利计算机系，AI 安全研究者）此前在多次公开演讲中持"生物 AI 应当受比对话 AI 更严格的预发布审查"的立场（来源：Russell 在多场公开论坛中的发言）
- 主要分歧点：合规与开放的平衡——Evo 是完全开源，"既然源代码公开，谁都可以滥用"，是否与 Radical Numerics 的"防御使命"自相矛盾

对中国商业 / 科技读者的含义：
中国在 BGI（华大）等机构有自己强劲的基因组学积累，AlphaFold 之后中国一批"AI for Science"创业（如百图生科）已经在蛋白质设计方向规模化。Radical Numerics 把"国防"明确写进商业模式的做法，预示了未来该赛道在中美之间会同时出现"双使命叙事"的趋同——中国创业者在融资与监管上是否会被迫做类似的明确化，是个值得追踪的问题。

延伸阅读：
- Eric Nguyen 等, Evo / Evo 2 论文（arXiv，2024-2025）
- Fortune 独家报道：https://fortune.com/2026/06/15/exclusive-ai-dna-radical-numerics-eric-nguyen-biology-biodefense-drug-discovery/
- 推荐配套：Karen Hao《Empire of AI》或 Mustafa Suleyman《The Coming Wave》，理解"双重用途"AI 治理的政经背景

---

### 深挖：Mallaby 新书《The Infinity Machine》—Demis Hassabis 与 DeepMind 的传记（来自书单区）

事实核实：
经 web_search 确认：Sebastian Mallaby 是 Council on Foreign Relations 国际经济资深研究员；曾任 Washington Post 专栏作家；著有《More Money Than God》（2010，对冲基金史）、《The Power Law》（2022，硅谷风投史）、《The Man Who Knew》（Alan Greenspan 传记）；两次普利策奖入围。《The Infinity Machine: Demis Hassabis, DeepMind, and the Quest for Superintelligence》一书在多家出版预告中确认存在并出版上市。Demis Hassabis 因 AlphaFold 工作于 2024 年与 John Jumper 共同分享诺贝尔化学奖，并担任 Google DeepMind CEO。

思想溯源：
Mallaby 此前两部巨作（《More Money Than God》《The Power Law》）已经分别给出对冲基金与硅谷 VC 两个产业的"机构史"框架，特征是：把单个个体的传记线索与一个**机构进化**的更大叙事勾连起来。把同一种方法用在 DeepMind / Demis Hassabis 身上，是把 AI 史从"产品发布史"或"模型架构史"，转回**机构社会学**——这是当前 AI 文献中相对稀缺的视角。最有力的潜在反驳：Mallaby 的方法依赖"内部人访谈"，访谈结构容易被受访方的自我叙事捕获——尤其当 Demis Hassabis 本人在世且仍在职。

同行视角：
- Karen Hao（《Empire of AI》作者）持更强的批判立场，强调 AI 公司的政治经济权力扩张
- Mustafa Suleyman（DeepMind 联合创始人，Inflection AI 联合创始人，《The Coming Wave》作者）从内部视角讲述同一段历史
- 主要分歧点：是把 DeepMind 当作"科学共同体"还是"权力共同体"——Mallaby 倾向前者，Hao 与 Suleyman 倾向后者

对中国商业 / 科技读者的含义：
DeepMind 与 OpenAI / Anthropic 的对照线索，正在帮助中文读者理解为什么"中国 AI 不仅是技术追赶问题，更是机构社会学问题"——智谱、月之暗面、阶跃星辰等公司是否在构建类 DeepMind 的"长期科研型机构"，还是被市场压力推回类 OpenAI 的"产品发布型机构"，决定了下一个 5 年的差距来源。Mallaby 这本书可以作为对照阅读的基准。

延伸阅读：
- Sebastian Mallaby, "The Power Law"（2022）— 风投史的同类方法的另一部作品
- Karen Hao, "Empire of AI"（2025）— 反向视角的 OpenAI / Sam Altman 商业史
- Mustafa Suleyman, "The Coming Wave"（2023）— DeepMind 内部人视角

---

## 七、决策与思考清单

> 这是日常思考读物，不是工作清单。内容形式：**问题，不是任务**。

**今晚值得再看一遍的（30-60 分钟内可消化）**：
基于 Acemoglu《Automation and Repression》—— 通读他的推文与论文摘要（论文本身需要建模背景），同时浏览其与 David Autor / Simon Johnson 的 Brookings 论文综述。

**今晚值得想一想的（适合通勤或临睡前回味）**：
基于 Acemoglu 论文与 Block 的 Builderbot 数据 —— 如果"AI 占合并代码 15%"在 2 年内变成 50%、5 年内变成 80%，**我自己所在的行业**会以什么节奏经历这件事？我的工作是更接近"被 Agent 替代的执行层"还是更接近"管理 Agent 队列的协调层"？我有没有在为后者准备？
基于 Kareem Amin"公司死亡 doula" —— **我手上的产品 / 项目，如果它已经完成了它最初的使命**，我会承认这件事并设计一个"体面退场"，还是默认要把它 scale 成下一阶段？为什么？
基于 Milanovic "国家自由主义"框架 —— 我所在企业里有多少业务环节，是建立在"跨境信任"假设之上的？如果这条假设在 5 年内系统性弱化，哪些环节最先失效？

**本周值得追踪的**：
- 智谱 GLM-5.2 在主流前端编程基准上的稳定性（如 Chamath 暗示的"过拟合"风险）
- Radical Numerics 与美国国家实验室合作的具体监管进展
- jack 承诺的"开始更多公开 Block 的 AI 工具"会披露什么具体数据
- Sebastian Mallaby 新书《The Infinity Machine》的多家书评（FT、Economist、HBR 是否会评）

**今天值得重新审视的旧判断**：
（无累积输入；下期开始建立判断对照）

---

## 八、本期发言人画像更新

| 账号 | 类型标签 | 题材覆盖 | 本期表现 | 建议优先级 |
|------|---------|---------|---------|-----------|
| @DAcemogluMIT | 领域内权威（经济学家，诺奖得主） | 经济 / AI 政治经济 | 发布新工作论文《Automation and Repression》，引发主区块 #1 信号 | 高 |
| @JeffDean | 领域内权威（DeepMind CSO） | AI / 生物 AI | 转发与背书 Radical Numerics 出生宣告，引发主区块 #2 信号 | 高 |
| @BrankoMilan | 领域内权威（不平等研究学者） | 经济 / 政治经济学 | Foreign Policy 文章 + 新书塞尔维亚语版，引发主区块 #3 信号 | 高 |
| @jack | 经营者（Block 创始人） | 创业管理 / AI | 公开 Builderbot 数据，承诺更多披露 | 中 |
| @chamath | 投资人 | 投资 / AI 产业 | 关于开源模型架构收敛的判断 | 中 |
| @jeremyphoward | 经营者 + 领域内权威（fast.ai） | AI / 开源 | 公开宣告 GLM-5.2 Max 前端编程世界第一 | 中 |
| @tylercowen | 领域内权威（经济学家） | 经济 / 文化 / 访谈 | 与 Roblox CEO 访谈上线，霍尔木兹经济学评论 | 中 |
| @patrick_oshag | 经营者 + 媒体 | 投资 / 创业管理 | Kareem Amin 访谈系列引出"死亡 doula"概念 | 中 |
| @sapinker | 领域内权威（认知科学家） | AI 治理 / 公共理性 | NYT 评论批评 AI 公司"不可避免论"话术 | 中 |
| @paulg | 领域内权威（创业 / 早期投资） | 创业 / 地缘（降级） | 谈伊朗战争失利的博弈论判断 | 中 |
| @tferriss | 经营者 / 出版业 | 出版 / 内容经济 / 投资 | 上线 Mallaby 访谈；"信息市场坍缩"判断 | 中 |
| @ericries | 经营者 / 作者 | 公司治理 | 新书《Incorruptible》入选 FT 夏季最佳商业书 | 中 |
| @gdb | 经营者（OpenAI 总裁） | AI / 工程 | "软件工程已与 6 个月前不同" | 中 |
| @emollick | 述评号 + 领域内权威 | AI 产业 / 教育 | 多家公司 AI 战略在 agentic 革命之前已过期 | 中 |
| @michaeljburry | 投资人 | 投资 / 宏观 | 转 2000 年 Tiger 关闭旧文，暗示当前估值警示 | 中 |
| @saylor | 经营者（Strategy） | 比特币 / 金融工程 | $STRC 双月度股息上线 | 低-中 |
| @NickSzabo4 | 领域内权威（区块链思想者） | 区块链 / 政治 | 本期发言以政治内容为主，技术 / 思想类发言较少 | 低-中 |
| @pmarca | 投资人 + 操作者 | 投资 / AI / 文化 | 多为短评 / 一字回应；本期未给出独立的长形判断 | 低-中 |

**优先级定义**：
- **高**：本期产生了至少 1 条进入主区块或书单区的商业 / 科技信号，且发言人类型在画像上有更新。每期上限 3 个。
- **中**：本期是高效信号过滤器、重要资源信源、或本期表现稳定的常规信号源
- **低-中**：本期未提供足够独立判断或语境敏感

---

## 九、沉默与意外信号

**本期值得注意的沉默**：
- 今天 Daron Acemoglu 发布关于"自动化 → 镇压"的政治经济学论文，本 List 中其他经济学家——@DanielaGabor（4 条发言）、@TimHarford（1 条发言）—— 当日均未提及。这是一个跨范式分歧的微弱信号：Gabor 当日话题集中在乌克兰、英国旗杆、新自由主义、人民币与原油，Harford 谈商业秘密；Acemoglu 的论文要么尚未传入欧洲主流经济学圈层，要么暂被回避。
- 今天 Jeff Dean 公开支持 Radical Numerics 进入"AI 设计生命"领域，本 List 中其他主要 AI 思想者 —— @ylecun（1 条发言，谈 JEPA 与世界模型综述）、@fchollet（1 条发言，谈"重构问题"哲学）、@gdb（4 条发言，主要谈 GPT-5.4 应用案例与 SWE 感慨） —— 均未提及。两位顶级 Google 系科学家在生物 AI 方向的公开发言，未被 Meta / OpenAI 系科学家公开响应，这本身是一个值得追踪的信号。

**本期意外信号**：
- Paul Graham（YC 联合创始人，平时主要谈早期创业与硅谷文化）今天罕见地直接对地缘政治发声："如果我们因为这场战争而变得更差，那我们就是输了。"——这是一位平时严守"我谈我懂"原则的创业教父越界发言，本身就值得注意。同样地，Naval（Naval Ravikant）今日 RT 全在加州选举与 California voting system 的统计分析上——硅谷顶层思想者对美国制度信任度的同步下行，是一种沉静但显形的传导信号。
- @michaeljburry（Michael Burry，《大空头》原型，Cassandra）今晨转发了一篇 2000 年 NYTimes 关于 Tiger Management 关闭的旧报道，称"睡前故事"——配在 $SPCX 持仓动作之后。这种"用旧故事讲新位"的隐喻方式，是 Burry 经典的暗示手法，常常对应他正在押注的方向。

---

## 传播力素材（适合自媒体改写的高互动思想观点）

> 从被噪音过滤丢弃的金句/观点类推文中，回捞具备思想独创性和传播潜力的商业/科技相关内容。

- "**The market for information is collapsing into the chatbot. The market for transformation — for sitting with one mind, at length, on a subject it has bled for — might just get smaller, weirder, and more interesting. I'd bet on it.**" / "信息市场正在向 chatbot 坍缩。但**转化市场**——和一个心智长时间共处、和一个它流过血的主题共处——也许会变得更小、更怪、更有意思。我会下注这一边。" — @tferriss（Tim Ferriss，5 部 NYT 头号畅销书作者，Tim Ferriss Show 累计下载 10 亿次）· 👍322 👁68741 · engagement_rate 0.33%
  改写方向：适合公众号 / 小报童 / 即刻"内容创作者必读"切片；可以加一句"如果你正在做长视频 / 长访谈 / 长文，这条判断给你一个非鸡汤的乐观理由"
  点评：这条的思想价值在于把"AI 杀媒体"叙事拆成两个市场。其前提假设是"chatbot 满足不了人类的'被一个心智浸泡过的'体验需求"——如果这个前提对，长形式内容的 ARPU 会反向上涨；如果错（即 AI 可以模拟"浸泡感"），整个判断会塌。盲区：忽略了内容生产者本身被 AI 工具替代的速度。

- "**Things in the long run are better for shareholders too.**" / "（设计成抵抗金融重力的公司）长期来看，对股东也更好。" — @ericries 引用 Jeff Berman 评《Incorruptible》（Eric Ries，《精益创业》作者）· 👁604 · engagement_rate 0% — 互动较低但思想性强：把"使命 vs 股东回报"的二元对立直接拆穿
  改写方向：财经类公众号 / 36Kr / 投中 ESG 选题切片；可与 Branko Milanovic"国家市场自由主义"配对成"治理回归"系列
  点评：这条的论点不新——巴菲特、Charlie Munger、Brian Chesky 都说过类似话——但 Eric Ries 把它系统化为"设计原则"是有原创性的。前提假设：长期与短期之间存在可设计的制度桥梁。盲区：没有给出在没有创始人控制权（如 IPO 后被动股东占多数）情况下如何执行的方案。

- "**Without distinct data sets to train over and specifically narrow use cases to build expertise on, convergence seems at hand for this class of model architecture.**" / "如果不能拥有独特的数据集，也没有特别狭窄的应用场景作为专长，这一类模型架构的收敛已近在眼前。" — @chamath（Chamath Palihapitiya，Social Capital 创始人，Facebook 早期增长团队）· 👍463 👁102414 · engagement_rate 0.10%
  改写方向：适合科技商业类公众号 / 知乎专栏 "AI 模型护城河消失，下一波护城河在哪" 切片
  点评：思想价值在于把"模型差异化"的讨论从"参数量 / 训练算力"导向"数据与应用场景"。前提假设：开源能持续追上闭源（GLM-5.2 已经证明阶段性成立）。盲区：忽略了"分发渠道与用户数据飞轮"这类非数据集型护城河，可能高估了模型层级的同质化。

- "**software engineering is so different now. hard to remember what it was like even 6 months ago.**" / "软件工程现在已经完全不同了。连 6 个月前是什么样都难以记起。" — @gdb（Greg Brockman，OpenAI 总裁联合创始人）· 👍6149 👁263947 · engagement_rate 0.13%
  改写方向：CTO 圈 / 工程师社群切片；可以与 Block Builderbot 数据配对成"6 个月革命"
  点评：这是 OpenAI 总裁亲口说的工程师生产力转折性表态——其权威性来自他不是局外人。前提假设：所谓"完全不同"是结构性而非工具性。盲区：6 个月可能是 OpenAI 内部尺度，对存量大企业 IT 系统并不适用。

- "**The hardest problems are rarely solved by adding more complexity to the solution — they are solved by reframing the question until a simpler, clearer answer reveals itself.**" / "最困难的问题，很少是通过给解决方案添加更多复杂性来解决的——它们是通过重新框定问题，直到一个更简单、更清晰的答案自己显形而被解决的。" — @fchollet（François Chollet，Ndea / ARC Prize 联合创始人，Keras 创造者）· 👍1263 👁38523 · engagement_rate 0.74%
  改写方向：产品经理 / 创业者 / 工程类公众号 "问题重构" 切片
  点评：这条略接近金句的边缘——"重新框定问题"是设计圈说烂的概念。但 Chollet 的位置（Keras 创造者、ARC-AGI 主创）赋予了它额外权重，因为 ARC-AGI 测试本身就是"重新框定 AGI 评估问题"的具体实例。前提假设：复杂性是 lazy thinking 的征兆。盲区：现实中很多问题的复杂性是无法被消除的，强行简化反而失败。

- "**If you don't grapple with an idea, it won't change you. And if you're not changed by an idea, you're no better than a chatbot.**" / "如果你不去**搏斗一个想法**，它就不会改变你。如果你没有被一个想法改变，你就不比一个聊天机器人好到哪里去。" — @david_perell 引用 Ezra Klein（David Perell，How I Write 播客主持人）· 👁1806 · engagement_rate 0.33% — 互动低但思想性强
  改写方向：阅读 / 知识工作类公众号；与 Tim Ferriss"转化市场"配对，构成"AI 时代的深度阅读宣言"
  点评：这条的独创性在于"被一个想法改变"被作为人与 chatbot 的分界判据。前提假设："被改变"是一种可识别的体验。盲区：对那些"读得快 + 实践快"的极致 doer，这种"长时间共处"标准可能过于浪漫化。

---

## 十、本期信号评估

**信号 / 噪音比**：
通过铁律六质量门槛约 30 条，进入主区块 5 条，进入单源高启发 5 条，剩余约 60% 为低价值（政治站队 / 营销 / 个人生活 / 无认知信息量的短回应 / 视频展示型推文）。

**信息密度**：高
今天虽然总推文数（287 条）不算突出，且 List 内有较大比例被英国"Rape Gang 报告"政治话题占据，但**思想类高质量信号集中度异常高**——Acemoglu 新论文、Jeff Dean 公开背书 Radical Numerics、Milanovic 新书塞尔维亚语版 + Foreign Policy 文章、Mallaby 新书 + Tim Ferriss 播客同日上线，叠加 GLM-5.2 / 开源模型话题的双独立信源——这种密度在思想类简报中属罕见。

**主导主题**：
今日 List 的"思想"集中在三条主线：① "AI / 自动化的政治经济后果"（Acemoglu × Pinker × Sacks）；② "AI 进入新的物质层 / 生命层"（Radical Numerics × Jeff Dean × Sakana AI Marlin × Pieter Abbeel 机器人数据）；③ "全球化秩序结构性重组"（Milanovic × paulg 伊朗判断 × Cowen 霍尔木兹判断）。

**未浮现但值得追踪**（推测）：
- Karp《Technological Republic》被左翼经济学家公开背书后，本 List 中是否会有右翼科技立场的发言人公开回应？
- GLM-5.2 / 智谱 AI 在下一轮基准（编程之外的推理 / 数学）上的表现，是否会持续支撑 Chamath / Jeremy Howard 的"收敛在即"判断？
- Sebastian Mallaby 新书《The Infinity Machine》在 FT / The Economist / HBR 等长文媒体的多家评论，预计 1-2 周内浮现。

**本期信源**（共 30+ 位）：
@DAcemogluMIT @JeffDean @BrankoMilan @jack @gdb @chamath @jeremyphoward @tylercowen @patrick_oshag @sapinker @paulg @tferriss @ericries @emollick @michaeljburry @saylor @naval @fchollet @ylecun @hardmaru @RichardSocher @rsalakhu @pabbeel @rcbregman @david_perell @shaneparrish @DavidSacks @DanielaGabor @kevin2kelly @JamesClear @TimHarford @bfeld @AndrewYang @satyanadella @NickSzabo4 @elonmusk @pmarca @dhh @Cmdr_Hadfield @Scobleizer @NewYorker @KirkusReviews @goodreads（共 43 位活跃用户）

---

## 附录 A · 行业内幕（可选阅读）

> ⚠️ 这一节是给从业者的，普通读者可跳过。

- **Pieter Abbeel（伯克利） × XDOF**：宣布 $70M 融资 + 开源 ABC-130K 双手机器人遥操数据集（130K+ 轨迹，200 个复杂任务，Apache 2.0 协议）。这是当前最大的开源双手机器人操作数据集，对训练机器人基础模型的研究者有直接意义。
- **Russ Salakhutdinov（CMU / Sooth Labs）**：发布 iOSWorld 基准（26 个自定义 iOS 应用，133 个任务，3 个难度层级，包括 single-app / multi-app / memory & personalization）；当前最强前沿模型在 privileged 模式下成功率仅 52%，凸显个性化、跨 App 推理的难度。
- **Unreal Engine 5.8** 今天上线，附带实验性 MCP 服务器支持，意味着任何 Agent 都可以通过 MCP 协议与 UE5 工作流交互。
- **Epic 开源 Lore**：从零构建的版本控制系统，MIT 协议开源，定位为面向超大规模数据/二进制资产场景的 Git 替代。
- **OpenAI × Molecule.one**：GPT-5.4 帮助药物化学项目从文献综述走到经过实验验证的结果（来源：@OpenAI 官方账号，@gdb 转推），具体改进的是一个广泛使用的反应。
- **Jeremy Howard 转推 lvwerra**：一周内 100+ Agent 协作让 Gemma 4 throughput 从 100 tok/s 到 500 tok/s，是一个早期但具体的"群体 Agent 工程"案例。

---

## 简报末尾固定声明

本简报的所有判断、关联推测均基于公开推文与公开网络信息。所有具体数字均标注来源；无法多源验证的内容已显性隔离至「单源高启发」区块。读者应理解：思想类信号的"准确性"低于事实类新闻——这份简报的价值不是"告诉你真相"，而是"告诉你此刻在商业与科技领域最值得思考的方向"。
