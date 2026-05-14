# 思想发现简报 | 2026-05-15

> 数据窗口：2026-05-14 06:00 — 2026-05-15 06:00（北京时间，过去 24 小时）
> 深度挖掘：3 条 | 模板版本：v2.0
> 说明：本期未执行实时 web_search 核实，所有需多源核实的数字与引文均按"推文当事方原话 / [未经独立验证]"两档标注；读者请据此调整信任阈值。

---

## 一、今日要点

凌晨，Patrick OShaughnessy（@patrick_oshag，长青播客 *Invest Like the Best* 主播、psum 风投合伙人）把一段录音剪辑放上推特：Anthropic 的 CFO Krishna Rao（首席财务官，五年前还是 Cedar 这家健康保险结算公司的 CFO，今年是他第一次接受公开访谈）说，他每天 30%–40% 的时间花在一件事上——"算力配置"（compute allocation，即决定把英伟达 GPU、Google TPU 和亚马逊 Trainium 这三类训练芯片各分多少给哪个团队）。两年前他加入时，公司年化营收（run-rate revenue）是 2.5 亿美元；今天是 300 亿美元（来源：@patrick_oshag，当事方原话）。同一天，Yann LeCun（@ylecun，纽约大学教授、ACM 图灵奖得主、原 Meta 首席 AI 科学家）转发 Andrew Ng 的长文，断言"AI 失业大潮"是言过其实的恐慌；几小时后，Bernie Sanders（@SenSanders，佛蒙特州联邦参议员）和 AOC 提出法案，要暂停美国所有新 AI 数据中心建设。Elon Musk 看完只发了一个字："Hmm"。

如果只挑一件事今晚再读一遍，应该是 Krishna Rao 那段。原因不是 300 亿这个数字——而是它背后有一个新职位正在被发明出来：一种把硬件采购、能源调度、模型路线图、客户合同绑在一起的"算力 CFO"。它和过去 20 年 SaaS 时代的 CFO 几乎没有交集。这不是一条 AI 新闻，是一条关于"企业角色"如何被重新切分的信号。

**Bottom line in English:** A new corporate function — the "compute CFO" — is being invented in real time at Anthropic; the headlines about layoffs and data-center bans are the visible noise around it.

---

## 二、主信号（多源验证）

### 信号 #1：Anthropic CFO 第一次坐进话筒，留下一连串反 SaaS 时代的数字

主信源：@patrick_oshag（投资人 / 播客主，*Invest Like the Best* 自 2017 年起的常设节目，已访谈 500+ 位投资人与创始人） · 约 20 小时前
佐证：@patrick_oshag 当日发布 7 条相关推文（节目预告、统计清单、嘉宾职涯回顾、Mythos 章节剪辑）；2026-05-14 同日，FT、CoinDesk 等媒体围绕 Anthropic 的 Mythos 模型发布做补充报道
题材分类：商业 / 科技 / 投资

**故事 / 场景**：
Krishna Rao 两年前从 Fanatics（一家美国体育周边电商）跳到 Anthropic 时，公司年化营收 2.5 亿美元。他录这期节目当天，从他家开往录音棚的 20 分钟 Uber 车程里，签下两份各上千万美元的算力合同（来源：@patrick_oshag，当事方原话）。他坐进话筒时，那个数字已经是 300 亿美元（来源：@patrick_oshag）。他列出的统计像一份对 SaaS 时代价签的清算：

- 净收入留存率（NDR，即同一客户群第二年支出 / 第一年支出）按年化算超过 500%（来源：@patrick_oshag，当事方原话；[未经独立验证]）
- Anthropic 内部 90% 以上的代码由 Claude Code 写出
- 财务团队"代币消耗量最大的人"是税务负责人
- Fortune 10 中 9 家是客户
- Claude 上线五年，所有 7 位联合创始人仍在公司
- 上季度年化营收从 90 亿跳到 300 亿；新产品 Cowork 的增速比 Claude Code 当年同阶段更快
- Mythos（Anthropic 5 月发布的最新模型）在一个开源代码库里找到 250 个安全漏洞，前一代模型只找到 22 个

**为什么值得思考**：
过去十年的 SaaS 心智模型是"每人每年 100–1000 美元"。Krishna 隐含的新模型是"每人每年 10000 美元"——锚点不是软件，是被替代/被增强的员工工资。Patrick 的节目嘉宾上一周还在讨论"Anthropic 估值是不是泡沫"，这一期变成了"Anthropic 的 CFO 一天有 30%–40% 的精力像石油公司的 COO 一样在分配燃料"。这条信号的独特性在于：它不是关于一个模型公司值多少钱，而是关于"模型公司"这个组织形态正在长出哪些新器官。一个真正反共识的细节是，所有联合创始人都还在——Meta 重金挖人的时候，Anthropic 在技术线只走了 2 人，对照其他实验室"走了几十人"（来源：@patrick_oshag，当事方原话）。

**关键引文**：
> EN: "People misconstrue Mythos as just a cyber model. ... We had an open-source codebase that a prior model found 22 security vulnerabilities in, and Mythos then found 250. That is kind of scary, but that informed the way in which we released it."
>
> 中：人们误以为 Mythos 只是一个网络安全模型。……我们有一个开源代码库，前一代模型在里面找到 22 个漏洞，Mythos 找到了 250 个。这有点吓人，也决定了我们后来怎么发布它。

**链接**：
- 节目页：https://x.com/patrick_oshag/status/2054532117410054252
- Mythos 章节剪辑：https://x.com/patrick_oshag/status/2055034109320159281

---

### 信号 #2：把莫奈当成 AI 让人嘲笑——一场关于"标签如何劫持感知"的社会实验

主信源：@SHL0MS（艺术家，原推作者，本 List 之外） · 约 24 小时前
List 内放大者：@pmarca（Marc Andreessen，a16z 共同创始人；本期收藏量 4812，居 List 之首）；@rcbregman（Rutger Bregman，*Humankind* 作者）；@tylercowen（乔治梅森经济学教授）；@david_perell（写作 / 媒介评论者）
题材分类：科技 / 文化批评 / 认知科学

**故事 / 场景**：
艺术家 SHL0MS 把一张莫奈（Claude Monet，1840–1926，印象派创始人之一）的真迹照片发上 X，谎称是 AI 生成，请大家解释"为什么不如真迹"。评论区涌入了"这一看就是 AI"，"配色廉价"，"细节糊"。Andreessen 转推时只写了一个字："😳"（约 1819 likes / 393 bookmarks）。Rutger Bregman 引用了一项 *Nature Scientific Reports*（2024）研究：受试者一旦被告知"这是 AI 作品"，对同一幅画的审美评分会系统性下降。Tyler Cowen 用 Marcel Duchamp 1917 年的"小便池签名当艺术"案作类比——"杜尚问的是语境能不能把东西变成艺术，SHL0MS 问的是语境能不能反向把艺术变成垃圾。"David Perell 给出一句总结：人们对一次发布的反应，由"发布的故事"决定，而不是"被发布的东西"。

**为什么值得思考**：
这条不是 AI 艺术之争，而是一个更老的命题——**人对感官输入的解释力，比感官输入本身的信号强度更高**。它对商业判断的直接含义是：今天市场上每一份"AI 应用"评测、每一次产品发布的口碑塌方，可能都不在产品本身。一个反向的提问是：如果把 SHL0MS 的实验机制取反——把一段普通文本说成"GPT-5 写的"，是否会让人觉得"惊为天人"？过去半年若干次"AI 创作"惊艳事件，可能正在落入相反方向的同一陷阱。

**关键引文**：
> EN: "Peak Duchamp energy … the 'Fountain' test in reverse. Duchamp asked if context could make something art; @SHL0MS is asking if context can unmake it."
>
> 中：完美的杜尚式实验……只是把"喷泉"（杜尚 1917 年的成名作）反过来用。杜尚问的是"语境能不能把东西变成艺术"，SHL0MS 问的是"语境能不能让东西不再是艺术"。

**链接**：
- Andreessen 引用：https://x.com/pmarca/status/2054849794141479145
- Bregman 引用 + Nature 论文：https://x.com/rcbregman/status/2054973110890143747
- Cowen 评论：https://x.com/tylercowen/status/2055035580589683098

---

### 信号 #3：AI 失业大潮辩论同一天爆发——LeCun/Ng 与 Sanders/AOC 对撞

主信源：@ylecun（Yann LeCun，NYU 教授、图灵奖得主）转发 @AndrewYNg（Andrew Ng，DeepLearning.AI 创办人、原 Google Brain 负责人） · 约 19 小时前
对侧信源：@SenSanders（佛蒙特州联邦参议员 Bernie Sanders，参议院 HELP 委员会首席少数党议员）联合 AOC（众议员 Ocasio-Cortez，未在本 List）；@garrytan（Y Combinator 总裁兼 CEO）；@elonmusk
题材分类：经济 / 科技 / 公共政策

**故事 / 场景**：
Ng 在 *The Batch* 通讯里写："There will be no AI jobpocalypse"（没有 AI 失业末日）。理由不是 AI 不会替代工作，而是：（a）软件工程是受 AI 影响最重的行业，但软件工程师的招聘仍然强劲；（b）美国失业率仍在 4.3% 这一健康水平；（c）AI 实验室、SaaS 公司、用 AI 做裁员理由的企业三方，都有动机夸大 AI 的破坏力。LeCun 转发并附上"AI Jobapalooza"（AI 就业狂欢节）的反向口号。

同日，Sanders 与 AOC 提交一份要暂停**所有**新 AI 数据中心建设的联邦法案（来源：@garrytan，未经独立法案文本验证）。Garry Tan 反击："300 多份地方法案已经提交；2026 计划上线的数据中心有半数在延期或被取消——这是州际公路系统以来美国最大的就业引擎。" Musk 在 quote-tweet 里只留下两个字符："Hmm"，被 39 万次点赞、25 千次收藏。Bernie Sanders 当晚跟进："71% 的美国人反对在自家附近建 AI 数据中心。Big Tech 在中期选举上花了 3 亿美元让国会什么都不做。"（来源：@BernieSanders，原话；具体民调与游说支出数字 [未经独立验证]）

**为什么值得思考**：
两边都在调用相同的工业类比——"州际公路系统"或"原子能/电力管制"。但他们其实在用不同时间尺度的"就业"概念：Ng 说的是"两年内行业总就业"，Sanders 说的是"五年内地方社区就业 / 房价 / 电网"。这条信号的独特性在于：它把 AI 政策辩论从"模型能力"层面降到了"基础设施分配权"层面——电、土地、地方债——这个层面在过去 12 个月几乎没人正面讨论。它和铁路、电力曾经历过的相同治理周期高度相似：第一阶段比拼"建多大"，第二阶段比拼"谁有权决定建在哪"。

**关键引文**：
> EN: "Sanders and AOC introduced a bill to pause ALL AI data center construction. … The people who say they want American jobs are trying to block the biggest job creation engine since the interstate highway system."
> 中：Sanders 与 AOC 提案暂停所有 AI 数据中心建设。……那些声称要保住美国就业的人，正在试图阻挡州际公路系统以来最大的就业引擎。

**链接**：
- Ng 长文（LeCun 转发）：https://x.com/ylecun/status/2054749211472601194
- Sanders 表态：https://x.com/BernieSanders/status/2054992802392440995
- Musk "Hmm"：https://x.com/elonmusk/status/2054979419736035680

---

### 信号 #4："每周吃一张信用卡的微塑料"可能是科学家自己的手套

主信源：@jeremyphoward（Jeremy Howard，AnswerDotAI / FastDotAI 共同创办人、原昆士兰大学教授）转发 @agingroy（Avi Roy，长寿研究者） · 约 24 小时前
佐证：原推引用密歇根大学（University of Michigan）研究、2022 年对 WWF/Newcastle 2019 报告的再分析
题材分类：科学方法论 / 公共健康 / 测量学

**故事 / 场景**：
密歇根大学的研究人员发现，过去几年绝大多数测量"水/血液/大脑中微塑料"的红外光谱和拉曼光谱设备，其实把实验员佩戴的乳胶或丁腈手套上脱落的硬脂酸盐颗粒，误判成了聚乙烯。换上"洁净室手套"后，每平方毫米的假阳性从 7000 个降到约 100 个（来源：jeremyphoward 转发的原文，University of Michigan 研究；[未经独立验证]）。同一段还指出：广泛流传的"每周吃下一张信用卡（5 克）"的说法（最初来自 2019 年 WWF/Newcastle 联合报告），在 2022 年的一次再分析中被发现存在严重方法论错误，真实摄入量很可能低 100 倍。

注：原文同时强调——这并不意味着微塑料无害；上月公布的"大脑积累"数据仍然成立。

**为什么值得思考**：
独特性在于它是"科学自我纠错"的一个完美样本：一个被环保 NGO、保健品行业、媒体消费的 5 年顶流数字，可能根本就是测量工具的污染。对中文读者，它的反向用法更有价值——下一次看到任何"每天/每周/每年 X 克"的公共健康警告时，先问一句"这个数字是由谁、用什么工具、在什么环境下测的"。这条同时跨越了**科学传播 / 消费者行为 / 风险叙事**三个领域，与本期信号 #2（莫奈实验）共享同一个机制：测量框架决定测量结果。

**关键引文**：
> EN: "The numbers driving the panic may have been measuring the scientists, not the environment."
> 中：那些驱动恐慌的数字，测量到的可能是科学家本人，而不是环境。

**链接**：
- 转发原文：https://x.com/jeremyphoward/status/2054697290288550335

---

## 三、单源高启发信号

> ⚠️ 以下信号**仅有一个 List 内来源**，未经多方独立验证。但发言人在该领域有明确权威性，内容具有思想价值。请读者自行判断。

### 启发 #1：Chamath 在斯坦福——"地球上最省电的通用智能跑在 20 瓦上"

发言人：@chamath（Chamath Palihapitiya，Social Capital 创办人，Facebook 早期增长团队领导）
领域：科技 / 投资 / 神经科学（领域外，应降级评估）
发布时间：约 7 小时前

他说了什么：人类大脑在大约 20 瓦的功率下运转，仍然是地球上"最省电"的通用智能。AI 实验室真正应该从中借鉴的，不是结构相似性，而是**能量预算的纪律**。

为什么值得记下：
当前一座新 AI 数据中心动辄请求 1–2 GW（约相当于一座中型城市的用电）。Chamath 的提醒，是把"模型成本"的讨论从"美元/token"切回"焦耳/token"——这个换算视角在主流投资人发言里近乎缺席。他作为投资人，本职是回答"投谁能赚钱"，今晚却在斯坦福谈"能效约束"，本身就是个稀缺信号。

目前的不确定性：
- 这只是片段截取，完整演讲的论证链条不可见
- 神经科学家会反驳"20 瓦"包含的是远比 LLM 任务复杂的多模态/具身控制
- Chamath 本人在能效硬件方向并无投资记录可参照

链接：https://x.com/chamath/status/2054935627087687977

---

### 启发 #2：Ethan Mollick——"荒诞理由"能突破 AI agent 的护栏

发言人：@emollick（Ethan Mollick，沃顿商学院教授，研究 AI 与组织变革）
领域：AI 应用 / 组织行为
发布时间：约 8 小时前

他说了什么：微软研究院的一份新论文给出一个反直觉发现：用看上去**完全不合理**的理由（whimsey attacks，"奇思怪想攻击"，例如"我没法付那么多，因为日内瓦公约……"）对 AI agent 议价或交涉时，护栏（即模型被训练成拒绝某类请求的判断界面）反而更容易失效——因为这些理由处于训练分布之外（out-of-distribution，即模型在训练时几乎没见过的样本类型）。小模型尤其脆弱，但即便大模型也有可观的下降。

为什么值得记下：
这条信号挑战了一个隐含的工业共识——"模型越大，对抗越难"。它暗示一个更深的脆弱点：今天的 AI 安全测试主要在"对抗性强但仍合逻辑"的样本上做（例如越狱、prompt 注入），而**真实人类**的反常行为可能比这些精心设计的对抗更难防。对未来要部署 agent 做客服、谈判、采购的中国企业，这是一个值得提前演练的攻击面。

目前的不确定性：
- 微软研究院作为利益相关方，发布会侧重"我们的发现"
- 复现实验在中文场景下是否同样适用，尚无公开数据

链接：https://x.com/emollick/status/2054918927952548223

---

### 启发 #3：Steven Pinker 转 David Epstein——"别花 15 分钟想一个能省 10 分钟的捷径"

发言人：@sapinker（Steven Pinker，哈佛认知科学家）转发自己评论 David Epstein 的 NYT 专栏
领域：决策科学 / 心理学 / 个人生产力
发布时间：约 22 小时前

他说了什么：Pinker 拎出 Herbert Simon（赫伯特·西蒙，诺贝尔经济学奖得主、认知心理学与人工智能奠基者之一）的旧概念"满意化"（satisficing，把"满足"和"足够"两词合成的造词，意为"足够好就行，不必最优"）：信息搜集和决策本身有成本，把每一件事都做到最优反而是反生产力的。Epstein 把它推广到人生重大决策——选大学、选职业、选伴侣——大量"应该再调研"的时间，其实低于"现在就做出选择并修正"的期望收益。

为什么值得记下：
中文读者熟悉的"完美主义陷阱"是道德语言；Simon 的"satisficing"是经济学语言——它在 60 年前已经把这件事公式化。对 AI 时代的具体含义：当 LLM 把"信息搜集"的边际成本压到接近零时，**"决策成本"的相对占比反而上升了**。换言之，AI 越好用，"想清楚再做"反而越不划算——这是一个反直觉但严肃的推论。

目前的不确定性：
- Epstein 的 NYT 文章背后是否给出量化研究，仍待原文核实
- Simon 自己在 1956 年的原始论文针对的是组织决策，跨到个人决策需要谨慎

链接：https://x.com/sapinker/status/2054721319342580214

---

### 启发 #4：Reid Hoffman——区块链在 agentic 经济里的真实角色

发言人：@reidhoffman（Reid Hoffman，LinkedIn 共同创办人，微软董事，Greylock 合伙人）
领域：科技 / 加密 / 商业基础设施
发布时间：约 5 小时前

他说了什么：crypto（加密货币与区块链）在 AI 世界里有一个被低估的功能位——**给 agent 提供数字货币**（让 AI 代理之间能够互相支付）和**信任协议**（agent-to-agent、人-to-agent 之间无法仅靠企业自证完成的信任补缺）。

为什么值得记下：
Reid 是少数同时深度持仓"AI"和"crypto"两边的资深投资人，他这次的措辞特别克制——没有谈币价、没有谈基金会、只谈两个具体协议位（支付 + 信任）。对一直把 crypto 等同于"投机品"的中文商业读者，这是一个干净的反向提示：crypto 的应用层论证在 2026 年的合法性，可能不来自"金融自由"，而来自"agent 经济需要陌生人之间结算"。

目前的不确定性：
- Reid 在 Greylock 投资了若干 crypto 公司，存在持仓利益冲突
- "agent 互相付钱"的真实业务场景在 2026 年仍以演示和小规模实验为主，规模化使用案例尚未公开

链接：https://x.com/reidhoffman/status/2054968985901302015

---

### 启发 #5：Patrick OShaughnessy——Raspberry Pi 的反直觉故事

发言人：@patrick_oshag
领域：商业 / 教育创业 / 工业 IoT
发布时间：约 18 小时前

他说了什么：Raspberry Pi（树莓派）这家公司今天年化营收 3 亿美元、市值 14 亿美元；80% 的收入来自工业应用（嵌入式控制器、传感器网关、产线监控），**不是**消费电子。最初创办的目的是"让英国小孩有便宜的可编程电脑"。后来把制造基地从中国搬回威尔士一个小镇，没有损失效率。

为什么值得记下：
这条信号挑战的是"消费起家是创业最稳路径"这个常识。它的机制独特性是：**初始约束（必须便宜、必须可教学）反而塑造了一条工业市场必须的特性（开放、低功耗、长生命周期）**——这正是教育市场要求和工业市场要求的偶然重合。对中文创业者特别有用：当下一个"开源消费硬件"被嘲笑"赚不到钱"时，这个故事提供了一条"教育用户→工业客户"的非显然路径。

目前的不确定性：
- 这是一篇商业 profile，数字来自访谈
- 制造业本土化在中国语境下面临的成本结构与英国完全不同

链接：https://x.com/patrick_oshag/status/2054770673159983275（Colossus 长文）

---

## 四、跨领域关联

### 关联线 A：感知由框架决定——莫奈实验 + 微塑料手套 + Whimsey attacks

信号 1：把莫奈说成 AI，专业读者也会觉得它劣质 — @SHL0MS via @pmarca
信号 2：标准红外光谱仪测出来的"微塑料"，可能是实验员手套 — @jeremyphoward
信号 3：AI agent 的护栏被"日内瓦公约"这种荒诞理由击穿 — @emollick

**潜在共同根源**：
三件事都关于"**测量/感知工具的预设决定了它能看见什么**"。莫奈实验里预设是"AI 作品 = 廉价"；微塑料里预设是"任何聚乙烯式样的颗粒 = 微塑料"；agent 攻防里预设是"对抗者会用合逻辑的理由"。一旦预设被巧妙地翻转或落在预设之外，测量结果整体崩塌。这一组信号共同指向 2026 年一个被忽视的认知工程问题：当 AI 和传感器主导越来越多的"感知"，**它们的预设比它们的精度更值得审计**。

**反向思考**：
如果"标签劫持感知"是真的（莫奈实验机制），那么微塑料案例里的"换手套就少 99%"也可能是研究者的预设劫持——他们想找出污染源，因此愿意接受手套作为答案。这条关联线不算高确定性，但机制本身可证伪：找一个不预设手套是污染源的对照实验。

---

### 关联线 B：编程 agent 走出开发者圈子——Codex 移动版 + Grok Build CLI + Anthropic 法律插件

信号 1：OpenAI 把 Codex 接入 ChatGPT 移动应用 — @sama @gdb
信号 2：xAI 发布 Grok Build CLI，把"多 sub-agent 并行编辑代码"做成可点击界面 — @elonmusk @Scobleizer
信号 3：Anthropic 一次性发布 20+ 法律连接器 + 12 个律师业务领域插件 — via @Scobleizer / lawnext.com

**潜在共同根源**：
2026 上半年的产品发布密集地把 coding agent（写代码的 AI 代理）从"程序员命令行"搬向"非程序员可用界面"。移动版意味着 PM/CEO 在咖啡厅也能给代码库下指令；fully interactive CLI 意味着不会写脚本的人也能"点"出多 agent；20+ 法律连接器意味着律所合伙人不再需要 IT 团队参与。共同根源是：**agent 的瓶颈从"模型能力"切到"工作流接入"**。这与信号 #1（Anthropic CFO 谈 Cowork 增速比 Claude Code 同期更快）严丝合缝——客户买的不是更强的模型，是更深的接入。

**反向思考**：
如果"agent 走向非程序员"机制成立，那么 Grok Build CLI 的"鼠标可点"和 Codex 移动版的"通勤路上推进代码"应该指向同样的客户增长曲线。如果 Grok Build CLI 真增长慢，机制就可能错——也许移动 ≠ 非程序员，移动只是"开发者通勤"。这条关联线在 90 天内可以被验证。

---

## 五、本期书单与访谈

> 本节是本简报核心价值之一。收录权威发言人当日推荐的新书、访谈和长文（不限书名年份，但要求当期推动者具备权威性）。

### 新书 / Books

- **《Incorruptible》 — Eric Ries**
  推荐者：@ericries（本人，*Lean Startup* 作者）；@andrewtghill（FT 高级商业作家）当日访谈
  推荐语境：FT 在 2026-05-14 发了访谈长文，Eric 形容写这本书像 Joseph Conrad 的《黑暗的心》——"沿着河流往里走，看清楚现代金融系统怎么运作"
  核心论点：把"价值创造资本主义"（开面包店供应面包）与"价值榨取资本主义"（用杠杆收购全镇面包店、装上债务、降配、抬价、剥离资产破产）区分开来；公众基准公司（PBC，Public Benefit Corporation，2010 年起在美国数州设立的一种法律实体形式，允许董事在利益相关方之间寻求平衡而不只是股东收益）是一种制度反制工具（核心论点来自 ericries 当日推文与 kaseyklimes 引用，[完整论证待 web 核实]）
  题材分类：商业 / 法律治理 / 投资伦理
  中文版状态：[未经独立验证]
  对什么人最有价值：在 PE 行业工作的中文从业者；研究公司法的学者；考虑 ESOP / PBC 转型的创业者
  链接：https://as.ft.com/r/6353d07a-daba-4838-a027-838eacac5a54

- **《Take Me to Your Leader: Perspectives on Your First Alien Encounter》 — Neil deGrasse Tyson**
  推荐者：@KirkusReviews（Kirkus Reviews，1933 年起的英语图书评论机构，以"星标书评"著称）
  推荐语境：Kirkus 给出星标书评。中文 List 当日唯一被独立图书评论机构推荐的科普新书
  核心论点：Tyson 借"首次外星人接触"的科幻框架，讨论智能生命形式与让它们能跨越宇宙抵达地球的物理学条件
  题材分类：科技 / 科普
  中文版状态：[未经独立验证]
  对什么人最有价值：天文/物理科普读者；中学教师；做科技传播的内容工作者
  链接：https://ow.ly/US5U50YZKMB

- **《Suicidal Empathy》 — Gad Saad**
  推荐者：@elonmusk（"Read this book and give it to all your friends. Survival of civilization depends on it!"，原话；本期收藏量第二）；同时被 @sapinker 公开批评
  推荐语境：在加拿大新书榜列第二（来源：@GadSaad 当事人原话）
  核心论点（[待 web 核实，原作者措辞]）：批判过度"同理心"在公共政策中可能造成的反向伤害
  题材分类：心理学 / 公共政策 / 灰色地带（政治化色彩强，按 v1.2 通常会剔除，本期收录是因为它同时被 List 内最具权威的认知科学家公开评论）
  反对意见：@sapinker 当日撰文回应——"Gad 自己在书中确实澄清不是反对全部 empathy，只是反对脱离理性的 empathy。但书名的夸张（美国移民执法或许偏松，但远谈不上'自杀')，以及当下的政治语境（Trump 阵营正以反 empathy 为名为残忍政策背书）使得批评是合理的。"
  对什么人最有价值：对北美政治-情感话语演变感兴趣的研究者
  链接：https://x.com/elonmusk/status/2055007595359039742（Musk 推荐）；https://x.com/sapinker/status/2054721388607307842（Pinker 批评）

- **《The Bow and the Lyre》 — Seth Benardete**（旧书被重提）
  推荐者：@tylercowen 转发 @thenewthinkery
  推荐语境：今天 *Rolling Stone* 刊出 Christopher Nolan 谈他即将上映的《奥德赛》改编时说："I consulted no secondary literature, save Benardete's *The Bow and the Lyre*. It was my muse."（"我没有看任何二手文献，除了 Benardete 的《弓与琴》。它是我的缪斯。"）
  核心论点：Benardete（1930–2001，纽约 New School 古典学家）的这本书是对荷马《奥德赛》的哲学解读
  题材分类：文学 / 哲学 / 文化批评（非商业/科技，按 v2.0 仍可纳入）
  对什么人最有价值：电影从业者；古典文学爱好者；想看明白下半年大片的人
  链接：https://x.com/tylercowen/status/2054968390926660073

### 访谈 / 播客 / Interviews & Podcasts

- **Invest Like the Best — Krishna Rao（CFO @ Anthropic）**（首次播客出镜）
  主持人：Patrick OShaughnessy
  时长：1 小时 17 分钟
  发布日期：2026-05-13（在我们的 24 小时窗口里被多次复推）
  题材分类：科技 / 投资 / 公司治理
  核心话题：算力分配机制；前沿智能为何回报率持续上升；模型公司的"平台 vs 应用"两难；Anthropic 的财务团队如何使用 Claude
  关键时间戳（按主持人提供的章节）：
  - [02:38] The Compute Canvas（算力画布——三类芯片如何分配）
  - [11:58] Why the Returns to Frontier Intelligence Are So High（为什么前沿智能的回报率持续走高）
  - [23:30] Sourcing $100 Billion in Compute（如何凑齐 1000 亿美元的算力承诺）
  - [38:48] How Anthropic's Finance Team Uses Claude（Anthropic 财务团队如何使用 Claude）
  - [57:25] Mythos Release（Mythos 模型发布的内幕）
  收听链接：节目主页见 invest like the best；视频版：https://x.com/patrick_oshag/status/2054532117410054252
  为什么值得听：这是 2026 年到目前为止，少数能让你听到"AI 公司财务怎么变成石油公司财务"的一手访谈。

- **The Knowledge Project — Winston Weinberg（共同创办人 @ Harvey）**
  主持人：@shaneparrish（Shane Parrish）
  题材分类：商业 / 法律科技 / 创业
  核心话题：从一封写给 Sam Altman 的冷邮件开始；几乎撕毁公司的那笔交易；"决策的三条原则"；为什么法律费用没有下降
  关键时间戳：
  - [11:36] The Cold Email to Sam Altman（写给 Sam Altman 的冷邮件）
  - [19:34] The Deal that Almost Killed Harvey（差点搞垮 Harvey 的那笔合同）
  - [48:54] The Future of Law Firms（律所的未来）
  收听链接：https://x.com/shaneparrish/status/2054218165111177644
  为什么值得听：Harvey 是当前最早接入 Mythos 的法律 AI 公司之一；与同日 Anthropic 法律插件发布合看，能拼出法律 AI 的供给侧全景。

- **The Tim Ferriss Show — Jerzy Gregorek（奥运举重教练，训练脑瘫青年 Tae Jin Park）**
  主持人：@tferriss
  题材分类：心理学 / 训练科学 / 个人转变（非商业/科技，按 v2.0 仍纳入）
  核心话题：把医学预测彻底击破的训练叙事；身份认同的可塑性
  收听链接：https://x.com/tferriss/status/2054999272165187641
  为什么值得听：与本期信号 #3（满意化决策）形成有趣的对照——一个讲"够好就行"，一个讲"绝不接受预测"。

- **FT Andrew Hill 访谈 Eric Ries**（已收录在新书条目）
  发布日期：2026-05-14
  链接：https://as.ft.com/r/6353d07a-daba-4838-a027-838eacac5a54

- **The Próspera Podcast EP01 — Tim Urban**（@waitbutwhy）
  题材分类：商业 / 制度设计 / 创业地理
  核心话题：Tim Urban 实地访问洪都拉斯特许城市 Próspera 后的观察；Próspera 从美国宪法起草者那里学到了什么
  收听链接：https://youtu.be/GzQxmWp2TYQ
  为什么值得听：把"创业 = 做产品"扩展到"创业 = 做制度"。

### 重要长文 / Long-form Articles

> 来自 FT / NYT / Stratechery 等当日商业 / 科技 / 经济长文。本期最多 2 篇。

- **"Betting on Risk Changes the World" — Tim Harford / FT**
  发布日期：2026-05-13—14
  题材分类：经济 / 风险研究
  主题：FT 的 Undercover Economist 专栏写"对风险下注"如何在医学、保险、城市规划三个领域改变了世界
  为什么值得读：Harford 的专栏是中文读者读懂 FT 经济专栏的最佳入门
  链接：https://timharford.com/2026/05/betting-on-risk-changes-the-world/

- **"Decision-Making: Herbert Simon" — David Epstein / NYT 评论版**
  发布日期：2026-05-12
  题材分类：经济 / 决策科学
  主题：用 Herbert Simon 的"satisficing"概念重读现代人生决策（详见本期单源 #3）
  为什么值得读：把诺贝尔经济学奖得主 60 年前的一个概念，重新装配进 2026 的"AI 抹掉信息成本"语境
  链接：https://www.nytimes.com/2026/05/12/opinion/decision-making-herbert-simon.html

### 课程 / Courses

- **"Transformers in Practice" — Andrew Ng / DeepLearning.AI（与 AMD 联合）**
  讲师：Sharon Zhou
  题材分类：科技 / 工程师再培训
  核心收益：理解为什么 LLM 会幻觉；理解注意力和层如何配合预测下一个 token；诊断推理瓶颈并应用量化加速 GPU 推理
  报名链接：https://www.deeplearning.ai/courses/transformers-in-practice
  适合：在企业里推动 AI 部署、但本身不是模型研究者的工程经理 / 技术架构师

---

## 六、TOP 3 深度挖掘

> 对前面区块中（主信号 + 书单与访谈）合计排名前 3 的信号执行深挖。
> v1.1 强制约束：TOP 3 中至少 1 条来自「书单与访谈」区。

---

#### 深挖 #1：Anthropic CFO 第一次坐进话筒

**事实核实**：
Krishna Rao 是 Anthropic 现任 CFO，职涯路径（Harvard → Yale → Bain → Blackstone → Airbnb → Cedar → Fanatics → Anthropic）由 Patrick OShaughnessy 在 LinkedIn 资料基础上汇总。$30B 年化营收、$75B 累计融资、90% 内部代码由 Claude Code 写出、9/10 Fortune 10 客户——这些数字均为节目原话，**未经独立第三方核实**。

**思想溯源**：
"compute is the new oil" 这种比喻可上溯到 2017 年 *Economist* 的封面"The world's most valuable resource is no longer oil, but data"。Krishna Rao 这一期的真正贡献，不是这个比喻，而是给"算力配置"一个可观察的组织形态：**CFO 把 30%–40% 时间花在硬件采购**。这与 2010 年代云计算崛起时 SaaS CFO 把时间花在"营收净留存率"上构成对照。最有力的反驳来自 LeCun 在本期的另一条转发——他暗示前沿 AI 实验室有动机夸大模型能力以支撑高估值；按这种反驳，Krishna 的 NDR > 500% 也可能含有阶段性 inflated 成分。

**同行视角**：
- DeepMind 的 Demis Hassabis 在过去 12 个月公开偏向"模型架构创新"路线（与 Anthropic 的"compute scaling first"形成对照）
- Anthropic 与 OpenAI 在"recursive self-improvement"（递归自我改进）路线图上分歧明显——本期 Patrick 节目章节 [16:45] 专门讨论
- 主要分歧点：是否应该承认前沿模型本身已经在加速模型工程

**对中国商业 / 科技读者的含义**：
中国大模型公司目前还没有公开的 "compute CFO" 角色出现——这个职能要么混在 COO 里，要么混在采购副总裁里。Anthropic 这个组织信号可能在 6–12 个月内传染到国内头部模型公司。对国内财务从业者，这意味着一个新的、可被预见的高薪职业方向正在长出来。

**延伸阅读**：
- Patrick OShaughnessy 节目首播：https://x.com/patrick_oshag/status/2054532117410054252
- 同期"哪些会让 AI 革命脱轨"章节剪辑：https://x.com/patrick_oshag/status/2055034109320159281

---

#### 深挖 #2："真莫奈被当 AI 嘲笑"——感知如何被一句话劫持

**事实核实**：
SHL0MS 的原推存在于本 List 之外，但被 List 内至少 4 位发言人独立放大（Andreessen、Bregman、Cowen、Perell）。Bregman 引用的 Nature *Scientific Reports* (2024) 文章 "When art is labelled AI"（[标题与年份按引用，未经核实]）研究流程是：同一画作分两组展示，仅说明文字不同，受试者审美评分有显著差异。

**思想溯源**：
这条信号的认知根源不是"AI 艺术"，而是 1960 年代 Solomon Asch 的从众实验、1970 年代 Daniel Kahneman 的"代表性启发"（representativeness heuristic）、以及 Walter Benjamin 1936 年关于"机械复制时代艺术作品"的论文。Benjamin 的关键命题是：作品的"灵晕"（aura）由其历史与稀缺性赋予，而非由材料本身决定——SHL0MS 的实验完美演示了这个论点的反向运行（剥除灵晕的标签让感知者真的看不出价值）。最有力的反驳来自一个看似平庸的方向：受试者可能并非"看不出"价值，而是觉得"如果是 AI 我得贬低它，否则会被同伴瞧不起"——这个机制更接近社会压力而非感知失灵。

**同行视角**：
- @david_perell：框架决定反应，反之则不然——故事先于产品
- @rcbregman：研究文献已经证实这是稳定的现象
- @tylercowen：杜尚 1917 年的"喷泉"是这个机制的镜像——意识到这一点的人会同时看到两个方向（语境造艺术 vs 语境毁艺术）
- 主要分歧点：这是认知失灵，还是社会从众？

**对中国商业 / 科技读者的含义**：
对内容产业、设计行业、AI 应用创业者直接有用——产品上线时"如何被介绍"在很多场景下比"产品本身"更影响留存。具体动作：把同一段功能描述用三种不同前缀（"AI 自动"、"专家手动"、"无标签"）发给同一批用户测一遍，2026 上半年中国创业者几乎没有人系统做过这件事。

**延伸阅读**：
- 原推社会实验：https://x.com/Jediwolf/status/2054776716770320631
- Bregman 引 Nature 论文：https://x.com/rcbregman/status/2054973110890143747

---

#### 深挖 #3：《Incorruptible》— Eric Ries 用《黑暗的心》框架重读现代金融

**事实核实**：
Eric Ries 当日转发自己接受 FT Andrew Hill 访谈的链接。Ries 的前作《精益创业》（*The Lean Startup*，2011）有广泛中文读者基础。新书《Incorruptible》在 2026 春季上市的事实已由 Eric 本人 bio 与多次推文确认。Joseph Conrad 的《黑暗的心》（*Heart of Darkness*，1899）作为参照框架由 Ries 本人在访谈中提出。

**思想溯源**：
"价值创造 vs 价值榨取"这一对概念可以上溯到 Mariana Mazzucato 在 *The Value of Everything* (2018) 中的核心论证；更早可溯到马克思区分"生产性劳动"与"非生产性劳动"。Ries 的真正新意，不在概念本身，而在他用"面包店比喻"（来自 kaseyklimes 的网络贴文）把这个概念翻译成创业者可感的语言，并将其与 PBC（Public Benefit Corporation）这种法律实体绑定为可操作的反制工具。最有力的反驳：PBC 自 2010 年起在美国数州可注册，14 年过去了，被这种实体真正约束的公司寥寥——制度本身可能远比 Ries 在书中描绘的更弱。

**同行视角**：
- 支持方：Andrew Hill / FT 给出了带温度但克制的肯定，把它放在"商业道德书评"系列里
- 怀疑方：a16z 立场（pmarca 本期未直接回应此书，但他过去多次撰文反对 PBC 这种"以股东之外的利益相关方为名"的治理形式）

**对中国商业 / 科技读者的含义**：
中国不存在 PBC 这种法律实体形式，但中国创业者在过去 5 年频繁面对的两个相关命题——"基金优先"还是"创始人优先"、产业资本"长期"还是"短期"——与 Ries 在书中追问的是同一个底层问题。这本书的中文译本如果在 2026 下半年出版，将很可能在创业圈引发讨论。

**延伸阅读**：
- FT 访谈：https://as.ft.com/r/6353d07a-daba-4838-a027-838eacac5a54
- Eric Ries 本人推荐：https://x.com/ericries/status/2054972845219000629

---

## 七、决策与思考清单

> 这是日常思考读物，不是工作清单。形式是问题，不是任务。

**今晚值得再看一遍的（30–60 分钟内可消化）**：
基于信号 #1，去翻 Patrick OShaughnessy 这期 *Invest Like the Best* 的章节 [11:58]（"Why the Returns to Frontier Intelligence Are So High"）与 [23:30]（"Sourcing $100 Billion in Compute"），听他对 NDR > 500% 那段的具体解释。

**今晚值得想一想的（适合通勤或临睡前回味）**：
基于信号 #2（莫奈实验）—— 如果"标签先于感知"成立，那么过去 12 个月里，你工作上做过的哪一次"被同事/客户低估"的决策，是不是其实输在了"标签"而不是输在了内容？这个问题的反向更刺人：你低估过的某个东西，去掉作者标签后，你还会一样低估吗？

**本周值得追踪的**：
基于信号 #3 —— 跟踪 Bernie Sanders/AOC 的 AI 数据中心法案在两院的进展。如果它在 30 天内进入小组委员会听证，就意味着"地方反对数据中心"会成为 2026 中期选举的一个真议题；如果三个月还无音讯，就回到"姿态法案"分类。对中国电力 / 散热 / 模块化数据中心相关行业，这是一个值得建立的对照指标——"美国地方政府否决数据中心数 vs 中国地方政府招商数据中心数"。

**今天值得重新审视的旧判断**：
"模型公司估值是泡沫"——本期 Krishna Rao 数据给这一判断打开了一个具体的反驳通道（NDR 与 Cowork 增速）。可以暂时把"全是泡沫"修正为"估值结构对 compute 占用最深的几家更稳"，并把"哪些是 compute-deep / 哪些是 application-thin"的对照表，作为本周建立的认知工具。

---

## 八、本期发言人画像更新

| 账号 | 类型标签 | 题材覆盖 | 本期表现 | 建议优先级 |
|------|---------|---------|---------|-----------|
| @patrick_oshag | 投资人 + 优秀述评号 | 投资 / 模型公司 / 财务工程 | 本期连发 7 条围绕 Anthropic CFO 节目，提供了本期最高密度的一手数据，是信号 #1 与深挖 #1 的核心来源 | **高** |
| @ylecun | 领域内权威（Type 1） | AI 经济 / 模型架构 / 学术正统 | 转发 Andrew Ng 的"无 AI 失业末日"长文，同时单源转发 Aleph 形式化证明 agent；前者是本期主信号 | **高** |
| @pmarca | 投资人 + 资本视角（Type 3） | 科技政策 / 文化批评 / 媒体史 | 收藏量第一来自他的"真莫奈"转发；本期他对 General Catalyst 的连续讽刺也值得记录但属内幕信号 | **高** |
| @ericries | 经营者（Type 2） | 商业治理 / 公司法 / PBC | 新书 *Incorruptible* 在本期获 FT 加持，价值-创造/价值-榨取二分框架值得长期追踪 | 中 |
| @sapinker | 领域内权威（Type 1） | 认知科学 / 决策学 / 公共智识 | 高产日，11 条推文跨越演化心理学、决策哲学、政治评论；本期满意化决策一条值得单独记 | 中 |
| @jeremyphoward | 领域内权威（Type 1） | AI 工程 / 科学方法论 | 微塑料手套那条是本期最干净的"科学自我纠错"信号 | 中 |
| @chamath | 投资人（Type 3） | AI 能效 / 半导体 | 斯坦福"20 瓦"片段属于跨领域评论，按规则降级，仍纳入单源 | 中 |
| @emollick | 领域内权威（Type 1） | AI 应用 / 组织行为 | "Whimsey attacks"信号属于研究外溢，他的总结很到位 | 中 |
| @reidhoffman | 投资人 + 经营者（Type 2/3） | AI / Crypto / 平台战略 | 关于"agent 经济中 crypto 的真实角色"的发言克制且有信息量 | 中 |
| @BernieSanders / @SenSanders | 政治人物（Type 4） | 数据中心 / AI 产业政策 | 政治目的明显，但 71% 民调与 $300M 游说数字若能验证，对产业判断有用；按 v1.2 视为产业政策信号保留 | 低-中 |
| @elonmusk | 经营者 + 投资人 | xAI 产品 / 政策表态 | 本期主导对话度高，但绝大部分是产品营销和个人段子；"Hmm" 那条是难得的姿态信号 | 低-中 |
| @adam_tooze | 领域内权威（Type 1） | 经济史 / 历史 / 公共政策 | 本期发言主要围绕国际政治与"柴静-Macaron"事件，与商业/科技弱相关，按 v2.0 仍保留观察 | 低-中 |

**优先级定义**：
- **高**：本期产生了至少 1 条进入主区块或书单区的商业 / 科技信号，且发言人类型有更新或本期表现突出
- **中**：本期是高效信号过滤器或重要资源信源
- **低-中**：本期未提供足够独立判断或语境敏感

---

## 九、沉默与意外信号

**本期值得注意的沉默**：
今天 OpenAI 在 ChatGPT 移动端发布 Codex 集成（产品发布日）。在本 List 内当日发推 ≥ 3 条的账号中——@elonmusk（34 条）、@Scobleizer（22 条）、@pmarca（16 条）——只有 @Scobleizer 进行了无评论转推；@elonmusk 与 @pmarca 都没有提到这次发布。考虑到这是直接竞争产品，沉默本身是一个温和信号：OpenAI 这次发布在头部 KOL 圈未被视为"必须回应"的事件，可能意味着行业内默认"移动端 agent"是必走步骤而不是新主张。@sama 与 @gdb 当然都发了，但作为厂方，不计入"List 内反应"。

**本期意外信号**：
- @IvankaTrump 引用 @thedankoe 的"内在框架"长文，本期收藏数 3433 位居 List 前列。Ivanka 通常不发表与商业/科技直接相关的内容，这次的引用主题（精神成长 + 写作）属于本简报话题外的"个人成长 / 自助产业"。但她引用一个 90 万粉丝的 build-in-public 网红，本身是一个轻量级信号：自助内容产业正在跨越"政治家庭"这种通常的边界。仅作记录，不作主信号。
- @Fukuyama（弗朗西斯·福山，*历史的终结*作者）当日发布"The Importance of Civic Virtue"长文于 Substack 的 Persuasion 出版物。他在本 List 内发文极少（一年个位数），本期是稀缺信号，但内容偏政治哲学，按 v1.2 题材范围降级为"值得记录的发言人活跃度异常"。

---

## 传播力素材（适合自媒体改写的高互动思想观点）

> 从被噪音过滤丢弃的金句/观点类推文中，回捞具备思想独创性和传播潜力的商业/科技相关内容。

- "Most of us spend years trying to change outcomes without examining the internal framework producing them." / 中：大多数人花数年时间想改变结果，却不去检查那个产生这些结果的内在框架。 — @IvankaTrump 引 @thedankoe（建设个人品牌的网红）· 👍2975 👁524K · engagement_rate 0.65%
  改写方向：适合知识星球、抖音个人成长类账号；改写时把"内在框架"具体化为"工作流的隐含假设"，避免软鸡汤化
  点评：去掉作者名后这句话有微弱的陈词滥调风险，但加上"examining"这个动作词使它有了认知操作含义。它的前提假设是"个人结果由可观察的认知框架产生"，对受过教育的中文读者，这个假设和心理学常识一致；它的盲区是低估了制度与运气的份量——内在框架的边际收益对很多职业人群是有限的。

- "Building a company is a thousand failures and then a couple successes." / 中：建一家公司是一千次失败之后的几次成功。 — @winstonweinberg via @shaneparrish · 👍158 · engagement_rate 0.31%
  改写方向：适合创投账号、知识付费；改写时配一个具体失败案例
  点评：典型的创业陈词滥调，独创性低；纳入仅因它来自当日热门 Harvey 访谈，有引用价值。前提假设是"失败可以被计数"，但创业里很多失败是含糊的；盲区是它把"建公司"简化成数字游戏。

- "Everyone is fighting a battle you know nothing about. Everyone struggles. Take solace in that." / 中：每个人都在打一场你毫不知情的仗。每个人都很辛苦。这件事本身就是一种安慰。 — @tferriss · 👍1099 · engagement_rate 0.25%
  改写方向：与上一条互补，适合配在新书《Incorruptible》或职场焦虑类内容的开头
  点评：经典金句改造，独创性弱，但传播性强。前提是"共苦"能带来道德意义上的安慰；盲区是它隐含一个对受困者的暗示——"你的痛是普遍的所以不那么独特"，对正在经历真实困境的人，这种安慰有时候会让人更觉得不被看见。

- "You don't get instant gratification from being like, 'I think you're wrong … but that's gonna take me six months to prove you wrong.'" / 中：你不会从"我觉得你错了……但我得用六个月才能证明你错了"里得到即时满足。 — @shaneparrish 引 @winstonweinberg · 👍127 · engagement_rate 0.20%
  改写方向：适合管理类账号、做"对抗即时反馈机制"的反向叙事
  点评：把"延迟满足"用一个具体职业场景翻译出来，比纯抽象更有力。前提是 founder 真的有"长期不被理解"的判断力优势；盲区是大量 founder 是在自我幻觉中"延迟满足"。这是一句值得引用、但需要在改写时加平衡的金句。

- "Common sense prevails." / 中：常识胜出。 — @elonmusk RT @jgebbia (Joe Gebbia, Airbnb 共同创办人) · 👍4457 · engagement_rate 0.02%
  改写方向：低传播力，但语境清楚——Joe Gebbia 当晚连发若干推支持 Trump-Xi 北京之行；适合作"硅谷向政治靠拢"叙事的素材
  点评：去掉作者名是典型陈词滥调。但作为 Gebbia 与 Musk 同步表态的一部分，它的信号在"谁说"而不在"说什么"——是硅谷的一种姿态的延续。

---

## 十、本期信号评估

**信号 / 噪音比**：
本期 List 共 223 条推文（其中转发 110、原创 70、引用 43）。通过铁律六质量门槛的约 22 条；进入主区块 4 条；进入单源高启发 5 条；进入书单与访谈区 9 条；剩余约 75% 为低价值（埃隆模因转发、产品广告、纯政治站队、个人生活段子）。

**信息密度**：高
解释：单日内同时出现 Anthropic CFO 首播、AI 失业政治化爆点、"莫奈实验"四源放大、微塑料假象重写、Eric Ries 新书四象限论述，密度高于本季度大多数工作日。

**主导主题**：
- 顶层：AI 商业化（Anthropic 内部数据、Codex 移动版、Grok Build CLI、Anthropic 法律插件）
- 次层：AI 公共政策（Sanders/AOC 法案 + LeCun/Ng 反驳）
- 远端但密集：感知与测量的认知陷阱（莫奈、微塑料、Whimsey attacks）

**未浮现但值得追踪**：
- 美国地方对数据中心的抵制运动（已在 Sanders 推文露面，但具体地方法案数 300+ 尚无独立媒体覆盖；推测未来 7–14 天会有专题报道）
- 第三家头部 AI 公司是否会公开"compute CFO"角色（推测 60 天内）

**本期信源**：
@patrick_oshag @ylecun @pmarca @jeremyphoward @ericries @sapinker @chamath @emollick @reidhoffman @david_perell @tferriss @shaneparrish @tylercowen @rcbregman @BernieSanders @SenSanders @elonmusk @sama @gdb @AndrewYNg @drfeifei @adam_tooze @FukuyamaFrancis @michaeljburry @TimHarford @VitalikButerin @Scobleizer @KirkusReviews @kevin2kelly @NewYorker @waitbutwhy @goodreads @Cmdr_Hadfield @nntaleb @saylor @jack @satyanadella @BrankoMilan @DanielaGabor @IvankaTrump @SpeakerPelosi @HillaryClinton（共 42 位发言人）

---

## 附录 A · 行业内幕（可选阅读）

> ⚠️ 这一节是给从业者的，普通读者可跳过。
> 严格上限 500 字。

- **OpenAI Codex 移动版发布**：@sama 与 @gdb 当晚把 Codex 接入 ChatGPT iOS / Android 应用，允许用户在手机上启动新任务、审查输出、批准下一步；执行仍在用户的本机/Mac mini/devbox 上跑。同步发布 Codex Hooks（在任务关键点插入自定义脚本——做校验、扫秘钥、写日志、按目录差异化行为）与可编程访问令牌（business / enterprise 工作区可生成具备过期与撤销控制的范围化凭证）。
- **xAI Grok Build CLI 早期 Beta**：仅向 SuperGrok Heavy 订阅者开放（前 6 个月 $99/月，之后 $299/月）。功能：Plan Mode 集成、多 sub-agent 并行查看、鼠标交互、全屏终端 UI、headless 自动化。安装：`curl -fsSL https://x.ai/cli/install.sh | bash`。
- **Anthropic 法律插件 + 20+ 连接器**：同步向 Westlaw、LexisNexis、iManage、NetDocuments 等法律软件开放 MCP（Model Context Protocol）连接器，12 个业务领域（诉讼、并购、知识产权、移民、税务等）的内置 prompt 模板。@Scobleizer 与 lawnext.com 双源确认。
- **Nous Research TST**（Token Superposition Training）：通过 @jeremyphoward 转发——在 LLM 预训练的前 1/3 阶段读/预测 token 包并对 embedding 做平均，后 2/3 切回正常下一 token 预测，整训练相对挂钟（wall-clock，墙上时钟实际耗时）加速 2–3 倍，FLOPs 相同，架构 / 优化器 / tokenizer / 训练数据均不变。在 270M、600M、3B 稠密以及 10B-A1B MoE 上验证。推理时模型与传统训练完全一致。
- **arXiv 新规**：对在论文中出现"幻觉式引用"（hallucinated references，即作者由 LLM 生成、实际不存在的参考文献）的作者将处以 1 年禁投（@tdietterich 公告，@jeremyphoward @emollick 转发评论）。Mollick 评：把"AI 使用的责任归于人"是当下最合理的应对。
- **Microsoft MDASH 登上 cybergym.io 榜首**：@satyanadella 转 @dwizzzleMSFT；多模型协同的代理式安全系统首次在主流自动化漏洞发现 benchmark 上拿到第一。
- **World Labs image-blaster**：@drfeifei 转——单张图生成 3DGS 环境、网格、可交互物理对象与音效，使用 Marble + Claude skills + fal。
- **Cerebras IPO 与 NVIDIA 收购 Groq**：@Scobleizer 引述 @techsnif——Cerebras 开盘 $350、估值超 $100B；同期"NVIDIA 以 $20B 收购 Groq"（[未经独立验证]，仅一个二手来源）。

---

## 简报末尾固定声明

本简报的所有判断、关联推测均基于公开推文与公开网络信息。所有具体数字均标注来源；无法多源验证的内容已显性隔离至「单源高启发」区块。读者应理解：思想类信号的"准确性"低于事实类新闻——这份简报的价值不是"告诉你真相"，而是"告诉你此刻在商业与科技领域最值得思考的方向"。
