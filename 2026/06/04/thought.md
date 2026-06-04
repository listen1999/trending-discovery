# 思想发现简报 | 2026-06-04

> 数据窗口：2026-06-03 06:08 — 2026-06-04 06:08（北京时间，过去 24 小时）
> 深度挖掘：3 条 | 模板版本：v1.2

---

## 一、今日要点

今天值得花时间想的事，是一位 Ethereum 基金会研究员的"破坏式自首"。Justin Drake 是 Google 量子团队三月份那篇里程碑式 Shor 算法论文（针对 secp256k1 椭圆曲线——比特币和以太坊签名的数学基础）的共同作者，他平日不算高产。今天，他发布了一篇长贴，承认自己亲历了"用零知识证明（即一种能证明"我知道某个秘密"但不泄露秘密的密码学技术）来对一篇学术论文做内容审查"——这件事在科学史上没有先例。更扎心的，是他自己给出的预测："考虑到我所知道的一切，包括非公开的可怕信息，我现在把 Q 日（quantum day，即量子计算机第一次破解生产环境密码的那天）2032 年到来的概率定在 50%，2030 年定在 10%。"美国政府基于 NIST 的官方迁移截止日是 2035 年——他直接说："以事后视角看，这个日期是个笑话。"

Drake 不是危言耸听型的研究者，他平时谨慎、技术深、几乎不发情绪化推文。当这种人公开写"我所在的政府/学术机构正在压制信息，但我无法吹哨"时，值得放下手里的事去读完整篇。Paul Graham 罕见地直接转推（5169 收藏、298 万次浏览），意味着硅谷顶层圈子已经把它当作一个"政策窗口正在快速关闭"的信号。

**Bottom line in English:** A senior Ethereum researcher — and Google quantum paper co-author — has put 50% odds on Q-day arriving by 2032 while publicly disclosing that academic ZK-censorship is now a thing; if he's even directionally right, every long-lived secret protected by today's elliptic-curve cryptography is on a borrowed timeline.

---

## 二、主信号（多源验证）

### 信号 #1：Q 日时间表正在被压缩——一位 Google 共同作者从体制内部说出"还有 6 年"

主信源：@drakefjustin（被 @paulg 转推 5169 收藏 / 298 万次浏览） · 跨界发言人，Ethereum Foundation 研究员、Google 量子论文共同作者 · 约 22 小时前
佐证：@paulg · @JeremiahDJohns（独立转发）· theblock.co · cryptoadventure.com · cryptotimes.io · thequantuminsider.com
题材分类：科技 / 投资（与所有依赖椭圆曲线密码学的资产相关，包括比特币、以太坊、企业 PKI、HTTPS）

故事 / 场景：
6 月 3 日上午，Justin Drake 在 X 上贴出一篇近 2000 字的长帖。他从一个具体场景写起：三月 31 日，Google 量子 AI 团队发表了关于 Shor 算法的"重磅"论文——把破解 secp256k1（即比特币、以太坊签名所用的椭圆曲线）所需的算力门槛压缩了 10 倍。但论文最反常的部分不是技术：Google 用零知识证明（ZK proof）的方式把核心优化"加密公开"——既证明"我们做出来了"，又不泄露细节，并在博客中提到"与美国政府进行了沟通"。"用 ZK 做学术审查，这是历史上第一次。"两个月后，法国密码学者 André Schrottenloher 独立复现了那个被遮蔽的优化，今天上 arXiv；Google 内部专家 Craig Gidney 同步发文承认自己已经被压住了整整一年。一个匿名的"Shor-at-home"挑战（ecdsa.fail）几小时内就刷新了 Shor 世界纪录，连青少年都在贡献微优化。

为什么值得思考：
过去主流共识是 "量子破密码至少还有 15–20 年"，NIST 的迁移截止日是 2035。这条挑战的核心是：当一个研究者愿意公开承认"我所知的非公开信息让我把概率往前拉到 2030 年 10% / 2032 年 50%"时，决定不是"信不信他"，而是"如果他对的概率超过 20%，企业、银行、链上资产的迁移日历应不应该重排"。Drake 还指出 Google 已悄悄启动中性原子（neutral atom）量子实验室，这是它从超导路线唯一专注偏离的第一次。

关键引文（中英并存）：
> EN: "Given everything I know, including scary non-public information, I now put the odds of qday by 2032 at 50%. 10% by 2030."
>
> 中："综合我所知的一切，包括令人不安的非公开信息，我现在把 Q 日 2032 年到来的概率定在 50%，2030 年定在 10%。"

链接：
- 原推文：https://x.com/paulg/status/2061949326264599002 （Paul Graham 转 Justin Drake 全文）
- 一手挑战赛：ecdsa.fail
- 媒体报道：https://www.theblock.co/post/395944/no-longer-drill-googles-latest-quantum-breakthrough-debate-bitcoins-security

---

### 信号 #2：Uber 一个季度烧光了一整年的 AI 预算——并被迫开始为"token 成本"做产能规划

主信源：@patrick_oshag（投资人 / 主持人，Investlikebest 主持人、Positive Sum 创始人） · 约 10 小时前
佐证：@DKThomp（Derek Thompson 转评）· Fortune · CNBC · 多家二手报道援引 Uber COO 在 Rapid Response 播客上的同口径表述
题材分类：商业 / 科技（企业 AI 落地的经济学）

故事 / 场景：
Patrick O'Shaughnessy 在 Invest Like the Best 上播出与 Uber CEO Dara Khosrowshahi 的长访谈。Dara——一位接手时公司一年亏 45 亿美元、如今做出 100 亿美元自由现金流的运营者——把企业用 AI 的真实节奏摊开讲。一句话被反复传播：「我们一个季度就烧光了全年的 AI 预算，这迫使我们必须做调整。」（来源：@patrick_oshag 引用 Dara 原话）Dara 接下来说的更值得听：他们不会反过来削减 token 投入，因为"工程师吞吐量在涨"；而是开始"计量招聘"——人头扩张要为 token 预算腾位置。一个细节：他们用最贵的前沿模型"做探索"，一旦实验跑通就切到"更高效的 / 开源的"模型来规模化。

为什么值得思考：
这条挑战了三个主流共识。第一，挑战"AI 用量会收敛"的预算派：实际是越用越多，且互相强化。第二，挑战"前沿实验室有强护城河"的派系：Uber 把前沿模型当 R&D 试管，规模化时切到便宜替代品。第三，挑战"AI 让所有人都失业"的派系：Dara 选择的是冻结增员，而不是裁员；token 把"人头扩张"挤走，而不是把现有人挤走。同时来自一位 Fortune 6 月 3 日的二次确认：Uber COO Andrew Macdonald 在 Rapid Response 上对同件事的表述是"4 个月烧光全年预算"。

关键引文（中英并存）：
> EN: "We blew through our AI budget in a quarter, for the whole year. … We're using the more expensive models to explore. Once we scale some of these experiences, we'll look to bring in more efficient models that are more efficient on a token basis or are open source."
>
> 中："我们一个季度就烧光了全年的 AI 预算。…… 我们用更贵的模型做探索；一旦把这些体验规模化，我们会切到 token 成本更优、或开源的模型。"

链接：
- 原推文：https://x.com/patrick_oshag/status/2062142259944927564
- 媒体二次确认：https://fortune.com/2026/05/26/uber-coo-ai-spending-tokens-claude-code/
- CNBC 报道（Uber 大裁 People 部门）：https://www.cnbc.com/2026/06/03/uber-layoffs-people-division-ai.html

---

### 信号 #3："AI 抢走了工程师饭碗" 是一个让所有人体面退场的谎言

主信源：@johnloeber（被 @pmarca 转推 1041 收藏 / 51 万次浏览）· 经营者 / 实操者，自己面试过 100+ 工程师的技术 CEO · 约 19 小时前
佐证：@pmarca 加按语「Interesting」并整段转发 · @TMTLongShort 同方向独立长贴（被 pmarca 同期转）· @binarybits（Timothy Lee）对 Anthropic "意外 5 亿美元账单" 的当面质疑（被 @emollick 同期附议）
题材分类：商业 / 科技（劳动力市场、AI 叙事的可信度）

故事 / 场景：
John Loeber 是一位面试过 100 多位工程师的技术型 CEO。他写了一段冷静、信息密度高的备忘录。开头第一段："存在严重的 ZIRP（零利率时期）工程师过剩，正在被甩出市场——他们 2020–2022 年被大规模超招，现在正一波波被裁、被管理出局。受影响最重的是 PayPal、Bill 这种二线大厂，但 FAANG 也跑不掉。" 然后是那一段值得收藏的判断："我高度怀疑'AI 是工程师裁员的原因'这种说法。我认为这是一个大规模的、礼貌的谎言——公司不愿意承认自己曾经超招，工程师不愿意承认自己干得不行。大家都把账记在 AI 头上，而真相只是市场在做自我修正。" 他还引用了 Marc Andreessen 的旧判断："基本上每家科技公司都被超配了 2–4 倍人头。"

为什么值得思考：
这是一条挑战"AI 抢饭碗"主流叙事的内部告白——不是反 AI 派的批评（他显然是 AI 多头），而是一位每天面对面看简历的 CEO 的观察。它跨越了三组似乎无关的对话：MIT/McKinsey/Bain 三份连续报告显示企业 AI 投资回报"令人失望"（被 @JohnCassidy 和 @pmarca 当日同步转）；@emollick 当日质疑某家公司"意外花了 5 亿美元 Claude"的故事"在数量级上不成立"；以及 Uber 的"我们要冻结增员"。把这些放在一起，浮现出一个更清晰的图像：AI 没有"杀死"那些工作；那些工作早就死了，AI 只是给了一个体面的告别仪式。

关键引文（中英并存）：
> EN: "Everyone's blaming AI when it's really just the market rectifying itself. … People will be mad at AI for taking away their lucrative sinecures."
>
> 中："所有人都在怪 AI，但实际只是市场在做自我修正。…… 人们会因为 AI 拿走了他们高薪的虚衔而愤怒。"

链接：
- 原推文：https://x.com/pmarca/status/2062008718049382748
- @binarybits 关于"5 亿美元 Claude 账单"质疑：https://x.com/binarybits/status/2062239559128080740（@emollick 当日附议）
- @JohnCassidy 关于 Bain 报告：https://x.com/JohnCassidy/status/2061986834775789713

---

## 三、单源高启发信号

> ⚠️ 重要说明：以下信号**仅有一个来源**，未经多方独立验证。但发言人在该领域有明确权威性，内容具有思想价值。请读者自行判断。

### 启发 #1：学术界刚出现第一例"AI 量产论文"被批量撤销，逼迫期刊回到"口试评审"

发言人：@BrankoMilan（Branko Milanovic，CUNY 研究教授、LSE 客座，《The Great Global Transformation》作者，全球不平等研究权威之一）
领域：高等教育治理 / 学术诚信
发布时间：约 12 小时前（多条连发推）

他/她说了什么：
Milanovic 转述一桩刚发生的事件——一位被发现批量在多家学术期刊上发表 AI 生成论文的研究者，正被该期刊及其所属出版集团永久禁稿。Milanovic 随后给出自己的两条解药："考试改回纸笔手写（我已经这样做了 4 年，没人抱怨，考试质量很好）；论文评审改成视频面谈，没有双盲，但也没法用 AI 代笔。我们必须回到口试。"

为什么值得记下：
这是 Milanovic 在其专业范围之外、关于学术评价体系本身的一次"反共识直觉"——不是技术派的"靠 AI 检测器"也不是放弃派的"和平共处"，而是从制度设计的角度回到工业时代之前的口试传统。如果这种思路被一所欧洲顶级研究机构采纳，是一个值得追踪的拐点。

目前的不确定性：
- 暂无主流期刊系统采纳口试评审的公开公告
- "几个月前那位被禁稿者"具体身份未在推文中点名 [未经多源验证]
- 该方案在中国高校的可行性（研究生招生规模数十倍于欧美）需另外讨论

链接：https://x.com/BrankoMilan/status/2062113418333626758

---

### 启发 #2："Claude Mythos 已经达到了超预测者对 2026 年底的中位数预测"

发言人：@emollick（Ethan Mollick，Wharton 商学院教授、《Co-Intelligence》作者，长期独立追踪生产场景下 AI 的能力进展）
领域：AI 能力评测 / 预测可信度
发布时间：约 20 小时前

他/她说了什么：
Mollick 引用 Forecasting Research Institute 的数据：5 月初，最优秀的超预测者群体（superforecasters）对"年底 METR 80% 任务完成时长"的预测中位数是 3–4 小时；5 月下旬，Anthropic 的 Claude Mythos 已经把这个指标推到 3 小时 6 分钟，"已经落在专家与超预测者中位数预测的范围内"。也就是说，全年预期，半年就完成了。

为什么值得记下：
METR 这套基准（即"测试 AI 能独立完成多长时间任务"的基准）是过去一年用来对照 AI 增速最被认真对待的标尺之一。Mollick 这条信号的独特性在于：它不是模型公司自己说"我变强了"，而是来自独立预测机构的"被预测速率打脸了"——超预测者通常被认为是已知最准的人类预测者群体。

目前的不确定性：
- METR 基准本身在持续更新，"3 小时 6 分钟" 是某次单点测试，可能含选样偏差
- Mythos 与下一代竞品的可比性需要看后续基准刷新

链接：https://x.com/emollick/status/2062235461364445204

---

### 启发 #3：法学教授在双盲条件下，明显更偏好 Gemini 2.5 Pro 的回答而不是同行的

发言人：@chrmanning（Christopher Manning，Stanford NLP 创始人、HAI 高级研究员，自然语言处理领域的奠基者之一，被 @pmarca 当日独立转发同一篇研究）
领域：法律服务 / 知识工作者替代
发布时间：约 11 小时前

他/她说了什么：
Manning 转发 Stanford 法学教授 Julian Nyarko 团队的新论文。论文方法很简单：把法律技术问题分别交给法学教授和 Gemini 2.5 Pro 作答，把作答者身份隐藏后让其他法学教授盲评。结果是教授们"明显更喜欢"Gemini 2.5 Pro 的回答。Manning 自评："我也并非毫无理由地担心，Claude 或 ChatGPT 对技术问题的回答经常比我自己的更新、更全、更平衡。知识工作者和社会将如何面对人类专业能力的贬值？"

为什么值得记下：
这是一位 NLP 奠基者在自己领域外（法律实务）对自家技术结果的诚实读取。它把过去十年关于"专家知识何时被替代"的讨论从猜测拉到了同行评议层面——而且选了一个传统上极难被自动化的领域：法律。如果这个结论可复现，对法律服务、企业内部知识管理岗都是一次重定价。

目前的不确定性：
- 单一研究、单一律法领域 / 单一模型版本
- "教授偏好 Gemini" 不等于"Gemini 答案在法庭上能站住" [未经多源验证]
- 法律问题分布与生产场景差距：研究中的"技术问题"是否包含含混的事实判断不明

链接：https://x.com/chrmanning/status/2062216638624321653（指向 SSRN 论文 abstract_id=6849678）

---

### 启发 #4："沙堡是真的、易碎的；但滑坡会把大多数人逼疯，让他们最终在沙堡被冲走时根本没站在对的一边"

发言人：@michaeljburry（Michael Burry，《大空头》原型、Scion Asset Management 创始人，被 Warren Buffett 称作 "Cassandra"）
领域：投资心理 / 做空哲学
发布时间：约 10 小时前；同时附带其本人 Substack 长文《MEGA Trading Post / Short Thoughts Mash-Up June 2, 2026》

他/她说了什么：
Burry 的原文："Shorting is a world filled with slippery slopes and sand castles. The sand castles are real, and vulnerable, but the slippery slopes drive men insane and ultimately prevent most from being properly positioned when the castle is washed away."（做空是一个充满滑坡和沙堡的世界。沙堡是真实的、易碎的，但滑坡会把人逼疯，让大多数人在沙堡被冲走时根本没在正确的位置上。）

为什么值得记下：
Burry 极少高频发推（最近 7 天仅 2 条原创），这是一位"稀缺信号源"对"做空泡沫"心理学的浓缩判断。它的独特性不在结论（"做空很难"是共识），而在路径描述——把"事实正确"与"时机正确"分开，并指出失败模式不在前者。在 SpaceX 估值、AI 资本开支泡沫、Strategy/MSTR 等当下高估值话题环绕的语境里，这段话提供了一种心理免疫的语言。

目前的不确定性：
- Burry 自己 2023–2024 年的几个高调空头仓位（如 Big Tech）公开收益参差，他本人在该 Substack 帖中也部分承认
- 推文未指明针对哪类标的

链接：https://x.com/michaeljburry/status/2062231887343415373

---

## 四、跨领域关联

> 本区块尝试**主动建立**几条看似不相关但指向同一深层变化的信号关联。
> ⚠️ 这是 LLM 的关联推测，不是事实。每条都给反向思考。

### 关联线 A：企业 AI 不再是"零摩擦补贴"——token 经济学开始反向塑造组织

信号 1：Uber 一个季度烧光全年 AI 预算，CEO 决定"计量招聘"为 token 腾位置 — @patrick_oshag
信号 2：Bain 第三份连续 study 发现企业 AI 投资回报"令人失望"——继 MIT、McKinsey 之后 — @JohnCassidy（被 @pmarca 转）
信号 3：John Loeber「~每家科技公司都被超配 2–4 倍」+「AI 是 ZIRP 工程师裁员的体面替罪羊」— @johnloeber（被 @pmarca 转）

潜在共同根源：
这三条信号都指向同一件事——AI 在企业里不是按"软件许可证"那种边际成本接近零的方式扩散，而是按"重型生产资料"那种"每单位输出都有真实成本"的方式扩散。这件事的二阶后果是：HR 预算、IT 预算、研发预算之间的边界被彻底打乱，"人头"和"token"开始进入同一张电子表格。Uber 是第一个公开把这件事说出来的大公司。

反向思考：
机制相似性测试——如果 Uber 那条机制错了（实际上是"AI 没有创造增量价值，企业只是被迫续费"），那么 Bain 报告也不"错"，而是"印证"；但 Loeber 的"AI 没杀工作"叙事就会反向——如果 AI 真的没有增量价值，那么裁员就只能从市场修正解释，不需要"polite fiction"。这三条还能不能站在一起？只有当"AI 提升生产力" 与 "AI 投资回报令人失望" 同时成立时——即生产力提升被压在头部少数公司、未渗透到大盘均值——这条关联线才成立。

---

### 关联线 B：关键基础设施的"迁移截止日"正在被外部压力同步前移

信号 1：Justin Drake 把 Q 日概率拉到 2032 年 50%；Ethereum 把后量子迁移目标定在 2029 — @paulg 转 @drakefjustin
信号 2：欧盟决定加入美国主导的 Pax Silica 芯片同盟以"对冲中国 AI" — @DanielaGabor 转 @BertuzLuca
信号 3：OpenAI 公布 Frontier Safety Blueprint，明确呼吁建立"持久的前沿 AI 安全治理机构" — @gdb 转 OpenAINewsroom

潜在共同根源：
三条信号本来分属密码学、地缘产业、AI 治理三个领域，但都在描述同一种企业 / 政府 / 协议在 2027–2029 年间被外部冲击压成的"硬截止日"——基础设施层（密码、芯片、模型权重）正在从"可以慢慢演进"变成"必须在窗口内完成切换"。这种转换在历史上罕见（最近一次或许是 1999 年的 Y2K）。

反向思考：
机制相似性测试——如果 Justin Drake 的概率估算被证伪（量子工程在 2029 年遇到新瓶颈），那么 Pax Silica 的进度并不会被影响（地缘逻辑独立），但 OpenAI 的安全蓝图反而会失去"急迫性"——因为 frontier safety 的政治窗口在很大程度上靠"AI 进展速度"维持。所以这三条信号能否并立的条件是：**至少其中两个领域的进度同时维持当下节奏**。如果只剩 AI 继续快、而量子和地缘都放缓，这条关联线就要降级为"AI 一枝独秀"。

---

## 五、本期书单与访谈

### 新书 / Books

- **《Incorruptible: Why Good Companies Go Bad… and How Great Companies Stay Great》** — Eric Ries
  推荐者：@ericries（本人，《Lean Startup》作者；今天 List 上 Garry Tan、Anil Dash、Kim Scott、Wade Foster、Mark Pincus 等多人同期独立引用）
  推荐语境：今天是该书发布周，作者本人和 YC 现任合伙人 Garry Tan 都在 List 中高密度发声；Tim Ferriss 的旁支访谈正与之共振。
  核心论点（经 web 检索 simonandschuster.com / longnow.org 验证）：企业偏离创始使命，不是道德失败，而是治理结构失败——"金融引力"会把组织拉向短期攫取。Ries 提出"精神控股公司"（spiritual holding company）这一治理架构作为解药，并引用 Patagonia、Costco、IKEA、Novo Nordisk、Cloudflare 为案例。数据：使命可控的公司活到 50 岁的概率是非使命可控公司的 6 倍。
  题材分类：商业（公司治理）
  中文版状态：暂未见中译本公告 [未经多源验证]
  Amazon 评分：详情见 amazon.com/Incorruptible 当前评论
  对什么人最有价值：在融资压力下纠结于是否接受 PE 收购的创始人；正在思考"为什么 Twilio 创始人 Jeff Lawson 的双层股权失效后 199 天就被驱逐"这类问题的董事会成员。
  链接：https://incorruptible.co · https://www.simonandschuster.com/books/Incorruptible/Eric-Ries/9798893311860

### 访谈 / 播客 / Interviews & Podcasts

- **Invest Like the Best — 嘉宾 Dara Khosrowshahi（Uber CEO）**
  主持人：Patrick O'Shaughnessy
  时长：约 60 分钟
  发布日期：2026-06-03
  题材分类：商业 / 科技 / 投资
  核心话题：Uber 如何在 7 年内从年亏 45 亿美元做到 100 亿美元自由现金流；为什么 Uber 把自己定位在"物理 AI 与 AV"中心；Uber 平台上 AV 的车辆利用率比其他平台高 30%。
  关键时间戳：
  - 14:28 — 为什么 Uber 处在 AI 与物理世界的交叉点
  - 22:39 — 如何在自动驾驶赛道赢
  - 32:25 — "万亿级 AV 机会"的拆解
  - 47:00 — Uber 应用的未来形态
  收听链接：见 https://x.com/patrick_oshag/status/2062142259944927564 描述中的链接
  为什么值得听：今天主信号 #2 的全部背景；也是本期唯一对"前沿模型 vs 开源模型"商用切换路径有具体描述的一手访谈。

- **The Tim Ferriss Show #868 — 嘉宾 Jake Becraft（Strand Therapeutics CEO）**
  主持人：Tim Ferriss
  发布日期：2026-06-02（24 小时窗口内由 @tferriss 与 @DrSynbio 多次回流）
  题材分类：科技 / 生物技术
  核心话题：mRNA 治疗药物的临床转化；中国生物科技对美国的"超车压力"；为什么"治愈小鼠的癌症没有意义"。
  关键时间戳：Ferriss 试验性新格式"Founder Kitchen"——半访谈半头脑风暴。
  收听链接：https://tim.blog/2026/06/02/jake-becraft-strand-therapeutics/
  为什么值得听：罕见地把"生物技术商业化的具体痛点"讲清楚——区别于多数 mRNA 访谈停留在科学层面。

- **The Generalist — 嘉宾 Bryon Hargis（Castelion CEO，由 @pmarca 转推）**
  主持人：Mario Gabriele
  题材分类：商业 / 科技 / 国防
  核心话题：用 SpaceX 的迭代式制造方法做超音速导弹；"美国不缺武器，缺的是制造能力和学习速率"。
  关键时间戳：
  - 25:05 — 防御性 vs 进攻性武器的经济学
  - 1:01:06 — 为什么"更便宜更快"才是关键
  收听链接：见 https://x.com/pmarca/status/2062029787615375569
  为什么值得听：少数把"防务初创"与"硬科技创业 ergonomics"放在同一个语言体系里讨论的访谈。

### 重要长文 / Long-form Articles

- **"A pond of interesting problems"** — DHH (David Heinemeier Hansson, Ruby on Rails 创始人 / 37signals CTO)
  发布日期：2026-06-03
  题材分类：科技 / 商业（个人工作哲学，AI 时代的工作设计）
  主题：DHH 论"使用 AI 工具后，工作变得更像是坐在一个'有趣问题的池塘边'，挑那些既'抓住眼睛'又'勾住动机'的来钓——而不是被分配的杂活。"
  为什么值得读：一位 25 年高产工程师 / 作者对"AI 时代什么样的工作仍值得做"的具体回答，避开了"AI 替代谁"的空话。
  阅读时长：约 8 分钟
  链接：https://world.hey.com/dhh/a-pond-of-interesting-problems-5f697567

- **"The Ideological Implications of China's Economic Success / Sinified Marxism and Its Future"** — Branko Milanovic
  发布日期：2026-06-04
  题材分类：经济
  主题：Milanovic 在其 Substack 论中国经济成功对全球意识形态的影响——"中国化马克思主义"作为一种独立思想传统的未来走向。
  为什么值得读：Milanovic 是当代研究全球不平等最重要的经济学家之一；他从"思想史"而不是"GDP"层面分析中国，对中文读者尤其有"被外部权威评价"的价值。
  链接：https://branko2f7.substack.com/p/the-ideological-implications-of-chinas

---

## 六、TOP 3 深度挖掘

#### 深挖：Q 日时间表正在被压缩——Justin Drake 50% / 2032 的概率宣告

事实核实：
经 web_search 三家媒体（theblock.co、cryptotimes.io、thequantuminsider.com 6 月初）独立报道核实：Drake 的 50% / 2032 与 10% / 2030 概率表述属实；Google 量子团队 3 月 31 日论文、André Schrottenloher 的 arXiv 复现、ecdsa.fail 挑战赛真实存在。"ZK 审查"细节仅在 Drake 本人和少量加密技术媒体中提及，主流学术媒体尚未确认。

思想溯源：
"量子破密码"的学术先驱可以追溯到 Peter Shor 1994 年的算法。Drake 的判断属于"Shor 算法工程化加速 + 中性原子物理路线突破"双重叠加的复合预测，跨越了密码学、量子物理、信息治理三个领域。该观点的可识别学术先驱包括 Scott Aaronson（量子复杂度理论权威，4 月 29 日博文给出过更保守的概率）。最有力的反驳来自"量子误差校正实际门槛远高于纸面估计"派，代表是 IBM 量子团队，但本期 24 小时窗口内未见 IBM 量子的公开回应。

同行视角：
- Scott Aaronson（4 月 29 日博文）持"概率明显但比 Drake 更保守"立场
- Craig Gidney（Google 内部 Shor 算法世界级权威，今天发文证实"压了一年的优化"）支持 Drake 的事实陈述但未给出概率
- 主要分歧点：从"Shor 算力门槛下降"到"实际可用量子机存在"之间，工程化误差校正成本到底是 2 个数量级还是 5 个数量级。

对中国商业 / 科技读者的含义：
中国在量子通信（QKD，量子密钥分发）上长期领先，但在"破解他人密码"的可扩展通用量子计算上未公开领先。如果 Drake 的概率被市场逐步接受，潜在影响有：1）所有依赖椭圆曲线签名的链上资产（包括 USDT、USDC 这类与中文区高度相关的稳定币）会进入"后量子迁移焦虑"窗口；2）国密 SM2 算法同样基于椭圆曲线，迁移到 SM9（基于配对密码）或后量子格密码的窗口正在收窄；3）国内 PKI / CA 产业链将出现一波"重发证书"的实际工程压力，时间点可能比 NIST 官方 2035 截止日早 3–5 年。

延伸阅读：
- ecdsa.fail（挑战赛入口）
- Schrottenloher "Optimized Point Addition Circuits for Elliptic Curve Discrete Logarithms"（今日 arXiv）
- Scott Aaronson 4 月 29 日博文（搜 "Aaronson quantum cryptanalysis April 29 2026"）

---

#### 深挖：Uber 一个季度烧光全年 AI 预算

事实核实：
经 web_search 三家独立媒体（Fortune 5 月 26 日、CNBC 6 月 3 日、Outlook Business 6 月初）核实：Uber COO Andrew Macdonald 在 Rapid Response 播客上的口径是"4 个月烧光全年 AI 预算"，与 CEO Dara 在 Patrick O'Shaughnessy 访谈中"一个季度"的口径在数量级上一致（季度 ≈ 3–4 个月）。Uber 同日（6 月 3 日）宣布 People 部门大裁员近 1/4。

思想溯源：
"企业 AI 投资回报令人失望"这个判断的认知根源是 MIT 4 月一篇研究、McKinsey 5 月一篇报告、Bain 5 月底一篇报告——三家连续给出同方向结论。但 Dara 的版本提供了一个少见的反例叙述：投资回报"令人失望"不等于"投入会下降"——反而因为竞争压力，企业被迫追加。最有力的反驳来自 @TMTLongShort（被 pmarca 同日转）："胜任的员工 × token = 加速；不胜任的员工 × token = slop。" 暗示均值令人失望但分布严重双峰。

同行视角：
- Marc Andreessen（@pmarca）持"每家科技公司超配 2–4 倍"立场，与 Dara 的"冻结增员"互证
- Bain（被 @JohnCassidy 引用）持"返报令人失望"立场
- Ivanka Trump 当日转推 Charlton J. Boyd "每家企业 AI token 预算都超支"——交叉印证 Uber 不是孤例
- 主要分歧点：是"token 预算超支"代表"AI 价值确认"还是代表"沉没成本陷阱"。

对中国商业 / 科技读者的含义：
对中文区高相关的两点：1）国内"AI 平台"创业者一直在用"token 边际成本可降至零"做 pitch，而 Uber 案例提示这是头部企业短期内不会发生的真相——头部企业的"探索阶段成本"必须为下一代模型买单。2）中国云厂商（阿里云、火山、腾讯云）目前在内部模型 + 开源（Qwen、DeepSeek、Hunyuan）替换前沿模型的路径上，可能比美国头部企业的"探索-规模化"切换路径更早完成第二阶段。

延伸阅读：
- Fortune 6 月报道：https://fortune.com/2026/05/26/uber-coo-ai-spending-tokens-claude-code/
- CNBC Uber 裁员报道：https://www.cnbc.com/2026/06/03/uber-layoffs-people-division-ai.html
- 完整 Invest Like the Best 访谈（YouTube/Spotify）

---

#### 深挖：《Incorruptible》——Eric Ries 关于"公司为什么会变坏"的新框架

事实核实：
经 web_search Simon & Schuster 官方页 / Penguin UK / Amazon / Long Now 演讲页等核实：《Incorruptible: Why Good Companies Go Bad... and How Great Companies Stay Great》由 Simon & Schuster 2026 年 5 月出版（ISBN 9798893311860），副标题与全 24 小时窗口内 @ericries 多次自引一致。"Spiritual holding company"概念、Patagonia / Costco / IKEA / Novo Nordisk / Cloudflare 五个案例研究、"使命可控公司 50 年存活率高 6 倍"的论点均在官方页 / Porchlight / Charterworks 多次出现。

思想溯源：
这本书的认知根源可以追溯到三条线：1）Patagonia Yvon Chouinard 2022 年"地球是唯一股东"的 PBC（Public Benefit Corporation）转型，与 Ries 此前推动 LTSE（Long-Term Stock Exchange）的工作直接续接；2）Lynn Stout 的《The Shareholder Value Myth》（2012）对"股东至上主义"的法理批判；3）Ronald Coase 与 Oliver Williamson 的交易成本 / 治理结构经济学。最有力的反驳来自标准代理理论（Jensen & Meckling, 1976），认为分散的所有权 + 短期市场惩罚机制反而是治理效率的来源。

同行视角：
- Garry Tan（YC 总裁，当日多次为该书背书）持"长期任务驱动 > 短期股价驱动"立场
- Anil Dash（CEO Glitch，当日推荐）从初创企业实操者视角支持
- Kim Scott（《Radical Candor》作者）："十年里最重要的书之一"
- 主要分歧点：Ries 的"spiritual holding company"实际操作上需要双层股权 / 信托结构等法律安排，这与活跃股东主义（activist shareholders）的判例 / 监管走向冲突——Twilio 创始人 Jeff Lawson 在双层股权 sunset 后 199 天被驱逐，正是 Ries 自己引用的案例。

对中国商业 / 科技读者的含义：
中国《公司法》目前不直接对应美国的 PBC 结构，但 2023 年新《公司法》允许双层股权（A 股、港股两条路径），近年蚂蚁、字节、Shein 等都在不同程度尝试治理架构创新。Ries 这本书对中文区读者最直接的价值不在"复制结构"，而在提供一个分析"为什么使命型公司在二代接班 / 上市后会失控"的工具箱——这对正在做家族企业接班、并购整合、PE 退出决策的读者尤其相关。

延伸阅读：
- 官方页：https://incorruptible.co
- Long Now 演讲："Incorruptible by Design" https://longnow.org/talks/02026-ries/
- Charter Works 书评：https://www.charterworks.com/book-briefing-incorruptible-by-eric-ries/

---

## 七、决策与思考清单

**今晚值得再看一遍的（30-60 分钟内可消化）**：
基于 [信号 #1 Q 日] —— 读 Justin Drake 的完整长贴 + ecdsa.fail 的现状页（合计约 30 分钟）。基于 [信号 #2 Uber] —— 听 Patrick O'Shaughnessy 与 Dara 的访谈 32:25–47:00 段（关于 AV 与 Uber App 未来形态）。

**今晚值得想一想的（适合通勤或临睡前回味）**：
基于 [信号 #1 Q 日] —— 如果"2030 年 10%、2032 年 50%"成立，我所在的行业 / 我自己存的、依赖现行密码学签名的资产（包括加密资产、企业 PKI 证书、个人邮件加密 / 数字签名），需要在哪些时间点开始迁移？这件事会改变我什么投资决策？
基于 [信号 #3 ZIRP 工程师过剩] —— 如果"AI 没杀掉那些工作，那些工作早就死了"这个判断是对的，那么我所在的组织里有哪些"高薪虚衔"实际上已经是僵尸岗位？我自己的岗位呢？我能给出的"我每天的具体产出"清单经得起这套测试吗？

**本周值得追踪的**：
基于 [信号 #2 Uber + 关联线 A] —— 建立一张"企业 AI ROI 实际口径表"，跟踪每周新增的"AI 投资令人失望" vs "AI 投资被迫追加"两类报告，看头部企业（Uber、Microsoft、Meta、Google）的口径差异是否在收敛。
基于 [信号 #1 Q 日] —— 观察 NIST 是否在 6–7 月发布把后量子迁移时间表提前的公告。

**今天值得重新审视的旧判断**：
[本期无累积输入，暂略]

---

## 八、本期发言人画像更新

| 账号 | 类型标签 | 题材覆盖 | 本期表现 | 建议优先级 |
|------|---------|---------|---------|-----------|
| @drakefjustin（被 paulg 高权重转推） | 跨界 (Polymath：密码学 + 协议工程 + 治理评论) | 量子密码学 / 协议安全 | 主信号 #1 的源头；24h 内单条长贴成为全 List 最高 bookmark 推文 | 高 |
| @patrick_oshag | 述评号 / 投资人 | 商业访谈 / 公司治理 / AI 经济 | 主信号 #2；本期持续把 Dara 访谈拆成 5+ 条高价值剪辑 | 高 |
| @ericries | 经营者 / 作家 | 创业治理 / 公司结构 | 书单核心；24h 内 32 条相关推 | 高 |
| @pmarca | 投资人 + 跨界评论 | AI 投资 / 工程市场 / 文化批评 | 主信号 #3 的放大器；当日 44 条，含约 8 条业务密度高的转推 | 中 |
| @paulg | 跨界（创业 / 政治评论 / 文化） | 创业 / 量子 / 媒体批评 | 当日 5 条；其中 Justin Drake 转推是本期最高价值动作 | 中 |
| @BrankoMilan | 领域内权威（经济学） | 经济史 / 全球不平等 / 学术治理 | 12 条；启发 #1 + Substack 双发 | 中 |
| @emollick | 领域内权威（管理学 / AI 评估） | AI 能力评测 / 知识工作未来 | 5 条；启发 #2 + Anthropic $500M 质疑 | 中 |
| @chrmanning | 领域内权威（NLP） | AI 替代专业知识 | 启发 #3 单条 | 中 |
| @michaeljburry | 投资人 | 做空哲学 | 启发 #4 + Substack 长文 | 中 |
| @demishassabis | 领域内权威 + 经营者 | AI 模型 | Gemma 4 12B 发布；附录材料 | 中 |
| @tferriss | 述评号 / 经营者 | 生物科技访谈 | 8 条推 + Strand 访谈 | 中 |
| @david_perell | 述评号 | 写作 / 创作 | 7 条都是 Noah Hawley 剪辑 | 低-中 |
| @Scobleizer | 述评号 | AI 产品 / 硬件 | 25 条多以产品发布为主，价值密度低 | 低-中 |
| @elonmusk | 政治人物 + 经营者 | 当日 28 条以英国政治 / 文化战为主，商业 / 科技内容仅 Robotaxi / Starship 高亮 | 仅 Robotaxi 进入附录；其余按规则剔除 | 低-中 |

**优先级定义**：
- **高**：本期产生了至少 1 条进入主区块或书单区的商业 / 科技信号，且发言人类型在画像上有更新（上限 3 个）。
- **中**：本期是高效信号过滤器、重要资源信源、或本期表现稳定的常规信号源。
- **低-中**：本期未提供足够独立判断或语境敏感。

---

## 九、沉默与意外信号

**本期值得注意的沉默**：
今天 OpenAI 一连推出了三件大事：GPT-Rosalind（生物科学定向模型）升级、Codex Sites（应用化部署）、Frontier Safety Blueprint（治理蓝图）。但本 List 里通常对 AI 安全治理高度关注的 @sama、@gdb 内部声音之外，@drfeifei、@chrmanning、@JeffDean 当日发推 ≥3 条但均未对 Frontier Safety Blueprint 做表态。这是一个值得记下的"学术-工业治理共识真空"：当 OpenAI 公开呼吁"建立持久的前沿 AI 安全治理机构"时，学术界顶级 AI 研究者的当日沉默是政策窗口尚未对齐的信号。

**本期意外信号**：
@paulg（Paul Graham）作为以创业 / YC 见长的发言人，今天罕见地转推了一条**密码学 + 量子物理 + 治理批评**的复合长贴（Justin Drake / Q 日）——这在他的题材覆盖上是 7 天内首次。同样意外的是 @BrankoMilan（经济学家）今天连发 4 条关于"学术 AI 抄袭治理"的推文——这是经济学家少见地深入到高等教育评审制度的具体改革建议。

---

## 传播力素材（适合自媒体改写的高互动思想观点）

> 从被噪音过滤丢弃的金句/观点类推文中，回捞具备思想独创性和传播潜力的商业/科技相关内容。

- **"Everyone's blaming AI when it's really just the market rectifying itself. People will be mad at AI for taking away their lucrative sinecures."** — @johnloeber（被 @pmarca 转推）· 👍1667 👁510275 · engagement_rate 0.2%
  改写方向：适合改写为 LinkedIn / 36 氪短评，标题方向 "AI 替我们隐藏了一个更难堪的真相"
  点评：这条观点的思想价值在于把"技术现象"还原为"组织现象"，提出"AI 是劳动力市场修正的体面替罪羊"——独创性高。前提假设是"过去三年大规模裁员主要发生在过度扩招的岗位"，这个前提在 FAANG 与二线大厂可能成立，在小型初创 / 中端服务业未必成立。盲区：未讨论"AI 同时也在创造新职位"的对冲效应。

- **"I think we're doing our kids a disservice by giving them too much, being around too much. … A happy life is not necessarily an easy life."** — Dara Khosrowshahi（Uber CEO，被 @patrick_oshag 引用）· 👍71 👁18202 · engagement_rate 0.25%
  改写方向：适合改写为公众号"育儿与商业领导力"主题，对比"巨头 CEO 的反内卷育儿观"
  点评：这条观点表面是育儿，但实际在讨论"过度托管 / 过度扶持"作为系统性失败模式——这正是 Eric Ries《Incorruptible》中"金融引力"的人际版本。前提假设是"挑战是性格形成的必要条件"。盲区：未区分"健康挑战"与"代际剥夺"。

- **"A clean deduction from a false premise looks exactly like a clean deduction, so the cases I'm most confident about are the ones that most need checking."** — @bfeld（Brad Feld，VC，Foundry Group）· 👁1148 · engagement_rate 0.17%
  改写方向：适合"决策科学"主题的小红书 / 即刻短文，"越确信的判断越要复查"
  点评：经典命题（Bayesian 反思）的新表述，但放在 AI 代理时代具有新意——AI 给出的"自信回答"恰恰是最危险的部分。前提假设是"前提错误难以自检"。盲区：未讨论复查的成本边界。

- **"There is no second best math protocol. There is no second best language. … Learn Arabic math. Learn to read English. Learn Bitcoin."** — @saylor（被引用的口径）· 👍692 👁163732 · engagement_rate 0.07%
  改写方向：适合改写为加密圈财经短视频脚本，"协议的网络效应是赢家通吃"
  点评：这条观点的思想价值在于把"语言学 / 数学协议史"与"加密资产投资"放在同一个网络效应框架下——独创性中等（"协议网络效应"是熟悉论点，但用阿拉伯数字 / 英文做类比新颖）。前提假设是"价值存储协议遵循语言协议的演化规律"。盲区：忽略了语言 / 数字协议的演化时间尺度（千年）与货币协议（百年）的巨大差距；也忽略了同期 Justin Drake 的 Q 日警告——比特币的"协议"本身正面临密码学层面的换轨。

- **"Many people, including really accomplished people, don't have an accurate mental model of how LLMs operate. … You see this in wide beliefs that AI is just copying from known sources, or that it only produces average answers."** — @emollick · 👍534 👁51668 · engagement_rate 0.3%
  改写方向：适合改写为"为什么聪明人也用错 AI"的中文长文
  点评：观点本身不新，但"成就高的人也常常错"是好钩子。前提假设是"对 LLM 的常见误读会显著影响使用质量"。盲区：未给出"准确 mental model"的具体内容。

- **"The best way to test people in conversation is to ask them a question you're deeply thinking about too."** — @reidhoffman · 👍224 👁52099 · engagement_rate 0.09%
  改写方向：适合公众号"招聘 / 面试技巧"短文
  点评：把"测试"与"互惠"合并——你提出的问题如果对自己也是真问题，对方的诚实度会被自然激发。前提假设是"被问者能分辨真问题与考试题"。盲区：在权力不对等场景（面试官 vs 求职者）可能效力下降。

---

## 十、本期信号评估

**信号 / 噪音比**：
通过铁律六质量门槛 约 32 条，进入主区块 3 条，进入单源高启发 4 条，剩余约 60% 为低价值（其中政治站队 / 英国 Henry Nowak 案讨论占了 elonmusk 28 条的近 80%）。

**信息密度**：高
本期含一条罕见的高质量复合信号（Justin Drake Q 日），一份大公司 AI 经济学的一手访谈（Uber Dara），一份针对 AI 叙事的内部反驳（Loeber），以及一本同期发布的商业治理新书（Incorruptible）。

**主导主题**：企业 AI 落地的经济现实 + 后量子密码学的迁移截止日 + 公司治理结构的"长期主义"再思考——三个主题交汇在"基础设施层正被外部冲击压成硬截止日"这一深层判断上。

**未浮现但值得追踪**：
（推测）下一期可能浮现的话题：1）NIST 对量子迁移截止日的回应；2）OpenAI Frontier Safety Blueprint 引发的学术界 / 国会反应；3）Bain / McKinsey 后续 AI ROI 研究的进一步细化。

**本期信源**：@pmarca @ericries @NewYorker @elonmusk @Scobleizer @BrankoMilan @tferriss @patrick_oshag @david_perell @gdb @emollick @KirkusReviews @paulg @saylor @NandoDF @BernieSanders @satyanadella @rsalakhu @chamath @goodreads @IvankaTrump @shaneparrish @drfeifei @AndrewYang @SenSanders @michaeljburry @chrmanning @HillaryClinton @DanielaGabor @naval @drakefjustin @sama @demishassabis @sundarpichai @jeremyphoward @nntaleb @TimHarford @reidhoffman @tylercowen @JeffDean @neiltyson @rcbregman @RichardDawkins @mjmauboussin @michaelmauboussin @kevin2kelly @dhh @patrickc @jack @bfeld @hugo_larochelle（共 49 位活跃账号）

---

## 附录 A · 行业内幕（可选阅读）

> ⚠️ 这一节是给从业者的，普通读者可跳过。

- **Anthropic "5 亿美元意外账单"故事的可信度** — @emollick / @binarybits 当日双双质疑：传出的"某公司一个月意外花了 5 亿美元 Claude"故事数量级上不成立，最可能是云厂商内部用自家算力做的会计占位符；即便如此也"非常勉强"。这对评估 Anthropic / OpenAI 等 API 收入数据有直接意义。
- **OpenAI Codex 上线"Sites"** — @gdb 转推 OpenAI：Codex 现支持把"工作 / 想法 / 计划"直接编译成可分享 URL 的交互应用；Business / Enterprise plan 先开放。同时 Codex 周活 500 万，主要使用场景已从"写代码"扩展到"研究 / 分析 / 内容 / 运营"。
- **Microsoft MAI-Image-2.5 在 Image Edit Arena 单图编辑赛道排名第二（1401 分），超过 Nano Banana 2、Grok Imagine 与 ChatGPT-Image-Latest-High Fidelity** — @NandoDF 转推。MAI-Transcribe-1.5 在 FLEURS（43 语种）取第一、Accuracy×Speed 帕累托前沿第一、WER 第三（2.4%）。说明 MS AI 在"模型层第二梯队"加速追赶。
- **Google Gemma 4 12B 上线，16GB VRAM 笔记本可本地跑 + Apache 2.0** — @demishassabis 发布、@sundarpichai 强调"agentic 工作流"。Gemma 4 累计下载量 1.5 亿。
- **Russ Salakhutdinov（CMU）发布 MACU（Multi-Agent Computer Use）框架** — 用 manager agent 把任务拆成动态 DAG，OSWorld 等基准上成功率提升 4.7–25.5%，长任务速度提升 1.5×。多 agent CUA（computer-use agent）开始从论文走向标准范式。
- **Fei-Fei Li / Stanford World Labs 发布 StereoPolicy** — 用立体 RGB 直接给 2D 编码器加几何先验，避开 RGB-D / 点云在反光 / 透明物体上的脆弱性。这是物理智能（physical AI）领域的小但关键进展。
- **Patrick Collison 转 Deel 推出 stablecoin wallet (DLUSD)** — 拉美承包商支付链路从今天起在 Deel App 内闭环；阿根廷先开放，APAC / MENA / 非洲跟进。这是稳定币真正进入跨境工资场景的一次结构性切换。

---

## 简报末尾固定声明

本简报的所有判断、关联推测均基于公开推文与公开网络信息。所有具体数字均标注来源；无法多源验证的内容已显性隔离至「单源高启发」区块。读者应理解：思想类信号的"准确性"低于事实类新闻——这份简报的价值不是"告诉你真相"，而是"告诉你此刻在商业与科技领域最值得思考的方向"。
