# AI 行业情报简报 | 2026-07-13

> 数据窗口：2026-07-12 06:00 — 2026-07-13 06:00（北京时间，过去 `24 小时`）
> 深度分析：3 条 | 模板版本：v2.3

---

## 1. 重大新闻 & 突发事件

- **Satya Nadella 发表 X Article：企业必须掌控自身 AI 学习循环，否则价值将向基础模型厂商单向集中**

  来源：@satyanadella · 2026-07-12 23:09 BJT
  关键数字：Azure AI 年化收入 $37B，同比增长 123%（来源：Microsoft，当事方口径，未经独立验证）；原文因 X 平台 JavaScript 限制无法完整抓取，下述内容综合 @AravSrinivas 引文与权威媒体报道还原
  行业影响：Nadella 核心论点——若 AI 学习单向流动（企业使用产生的数据被基础模型厂商学习而非企业自留），经济价值将不可逆地向学习基础设施拥有者集中，每家企业必须掌控自己的学习循环。这篇文章由 OpenAI 最大投资方、同时经营 Azure AI 平台的 CEO 发出，直接指向 OpenAI 等厂商在蒸馏条款和客户数据使用上的不对等规则，战略信号清晰：Microsoft 的赌注在企业自建学习循环的 Azure 基础设施上。本期收藏量最高（8,240，engagement_rate: 0.36%）。

- **S&P 将 Oracle 信用评级降至 BBB-，明确点名 OpenAI 为关键信用风险**

  来源：S&P Global Ratings 官方公告（@GaryMarcus 于 2026-07-12 16:39 BJT 引用分析推送）
  关键数字：Oracle 长期信用评级降至 BBB-（来源：S&P Global 官方，已核实）；OpenAI 占 Oracle 剩余绩效义务约 50%（来源：@Ric_RTP 援引 Oracle 年报）；Oracle FY2027 自由现金流缺口预计约 -$420 亿（来源：S&P 报告，据权威媒体核实）
  行业影响：一家从未盈利的私营 AI 公司的财务健康，通过企业信用链条写入了养老金和债券基金的风险敞口，并同日进入英国银行监管视野。Oracle 数据中心租约 15-19 年、云合同约 5 年的错配意味着：若 OpenAI 无法按时付款，Oracle 面临无法提前退出的超长期债务。再降一级即为历史首次垃圾级债券。

- **Grok 4.5 第三方 Browser Use 基准接近 Claude Opus 4.8，定价约为 Opus 的 40%**

  来源：@Alezander907（Browser Use 团队，Physics & CS @ Stanford SLAC）；引用扩散：@elonmusk · 2026-07-13 05:01 BJT
  关键数字：Grok 4.5 定价 $2/$6 per million input/output tokens（来源：xAI，当事方口径），Claude Opus 4.8 为 $5/$25（来源：Anthropic 官网）；SWE-Bench Pro 输出 token 效率：Grok 4.5 约 15,954 vs Opus 4.8 约 67,020，约 4.2 倍差距（来源：xAI 官方，当事方口径，未经独立验证）
  行业影响：首份来自第三方 agent 框架的 Grok 4.5 vs Opus 评测：浏览器 agent 任务性能高于 GPT-5.6-Sol、接近 Opus 4.8，且 token 使用量约为 Opus 的 24%。如结果可独立复现，agent 工作流成本结构将有实质性下移空间。信源仅 854 粉丝，尚待独立验证。

- **Claude Fable 5 付费计划访问权延长至 7 月 19 日，Claude Code 速率上限保持 +50%**

  来源：@claudeai（Anthropic 官方）· 2026-07-13 约 02:00 BJT 前（50,419 likes，当事方口径）
  行业影响：7 天延长窗口直接影响正在评估 Fable 5 代码能力的开发者团队——无需升级计划即可继续在高速率下运行 agent 任务。

- **OpenAI Bio Bug Bounty 升级为常设私有项目，奖励翻倍至 $50,000**

  来源：@OpenAI（官方）；转发：@EthanJPerez（Anthropic 对齐团队负责人）· 2026-07-12 09:55 BJT
  关键数字：$50,000（来源：@OpenAI，当事方口径）
  行业影响：从一次性赏金升级为持续运营项目，意味着 OpenAI 判断生物安全越狱威胁尚未闭合；被 Anthropic 对齐团队负责人转发，是实验室间在 AI 生物安全方向存在信息互通的公开信号。

---

#### 深挖：Satya Nadella X Article——企业必须掌控 AI 学习循环

背景补充：
Nadella 在这篇 X Article 中系统阐述了"学习循环"战略：AI 时代的竞争优势将不再取决于选择哪个模型，而取决于企业能否积累并复利自身机构知识。Microsoft 的定位是为企业提供构建私有学习循环的基础设施（Azure AI、Copilot Studio 等），而非仅靠托管最好的模型赚钱。发文时 Azure AI 年化收入已达 $37B，同比增长 123%（来源：Microsoft FY2026 财报，Forbes、TheStreet、CryptoBriefing 等权威媒体核实）。

数字核实：
$37B Azure AI 年化收入 → 已核实（来源：Microsoft FY2026 Q3 财报，多家权威媒体交叉引用）；文章正文引用内容来自 @AravSrinivas 转述，与多家媒体报道方向一致，无矛盾。

扩展影响：
此文直接影响 AI API 合同谈判格局——当 Microsoft CEO 公开为"企业自控学习循环"站台，大型企业客户在与 OpenAI/Anthropic 签约时拥有了主张自身数据不被用于上游训练的更强话语权。开发者层面，自建微调管道 + Azure 存储的方案获得更多 C 级背书；纯 API 调用模式的议价能力相对下降。（来源：TheStreet、edtechinnovationhub.com 报道）

对国内从业者的意义：
国内 AI 生态的私有化部署路径与此论点天然对齐，阿里云、百度智能云等推"企业自控数据"的销售叙事已久。此文可为出海 AI 厂商向欧美企业客户销售时提供额外论据：数据主权和学习循环控制权正在成为 C 级关注点，不再只是技术细节，有助于将私有化部署方案的销售对话从 IT 部门提升到 CEO 层面。

延伸阅读：
- https://www.thestreet.com/technology/microsoft-ceo-sends-a-blunt-warning-on-ai-and-the-tech-ecosystem
- https://cryptobriefing.com/nadella-ai-proprietary-learning-loops/

---

#### 深挖：S&P 将 Oracle 评级降至 BBB-，OpenAI 信用风险进入监管视野

背景补充：
S&P Global 于 2026 年 7 月初完成评级下调（官方公告可查）。Oracle FY2026 资本支出 $557 亿（同比增长 162%），超出自身 $500 亿目标，产生 -$237 亿自由现金流；FY2027 现金流缺口预计扩大至 -$420 亿，超出 S&P 此前预测近一倍。英国金融当局在同一时间节点将 Oracle 列为英国金融体系关键第三方，Bank of England 开始正式监管，为历史首次。（来源：S&P Global 官方，investing.com，Yahoo Finance 核实）

数字核实：
BBB- 评级 → 已核实（S&P Global 官方公告）；OpenAI 约占 50% Oracle 绩效义务 → 来自 @Ric_RTP 援引 Oracle 年报，权威媒体方向一致，具体比例未能独立核实；-$420 亿 FY2027 现金流缺口 → 来源 S&P 报告，多家媒体核实，与 -$237 亿 FY2026 实际值吻合。

扩展影响：
评级下调当日 Oracle 股价上涨 2.65%，但 Oracle 债券利差同步扩大——权益投资者和信用投资者对同一家公司判断分歧鲜明。信用投资者的职责是为潜在违约定价，此分歧值得追踪。AI 基础设施的金融风险已通过企业信用链条进入英国银行体系监管范畴，是系统性风险传导的里程碑信号。（来源：ainvest.com、optionstradingreport.com）

对国内从业者的意义：
国内 AI 基础设施买方与 Oracle 无深度绑定，短期无直接成本影响。但若 Oracle 进一步降至垃圾级，全球 AI 基础设施融资成本可能整体上行，间接影响国内大规模 GPU 集群融资的利率环境。国内 AI 创业公司与大客户签约时，可参考此案例在合同中加入数据中心服务商信用评级底线条款。

延伸阅读：
- https://www.spglobal.com/ratings/en/regulatory/article/-/view/type/HTML/id/3592348
- https://www.ainvest.com/news/oracle-notch-junk-ai-trade-credit-limit-2607/

---

#### 深挖：Grok 4.5 多维基准——Browser Use 评测之外的完整图谱

背景补充：
Grok 4.5 于 2026-07-09 发布（原文发于 2026-07-09，今日被 @elonmusk 引用扩散）。xAI 官方定位为"Opus 级别、更快、更省 token、更低成本"。跨多个评测框架的表现不一：Browser Use 基准高于 GPT-5.6-Sol、接近 Opus 4.8；Snorkel GDPVal+（约 2,000 个专业任务）Grok 4.5 达 29%，超过 Opus 4.8（21%）和 GPT 5.5（22%）；DeepSWE 1.0 和 Terminal-Bench 2.1 胜 Opus 4.8；但 DeepSWE 1.1 和 SWE-Bench Pro 败于 Opus 4.8。（来源：TechCrunch、Snorkel AI、kingy.ai、explainx.ai）

数字核实：
$2/$6 per million tokens → 来源 xAI 官方，TechCrunch 核实；29% vs 21% Snorkel GDPVal+ → 来源 Snorkel AI 独立测评，已核实；4.2x token 效率差距（SWE-Bench Pro） → 来源 xAI 官方，当事方口径，未经独立验证；Browser Use 评测数据 → 来源 @Alezander907，当事方口径，尚待独立复现。

扩展影响：
价格锚定是此次最确定的竞争信号：$2/$6 vs Opus 4.8 的 $5/$25，在输出 token 密集型 agent 任务上总成本差距可达 3-4 倍。加上 4.2x token 效率差异（若独立验证），实际每任务成本可能更低。Browser Use 评测尤其值得关注：这是真实 agent 场景数据，而非学术基准。（来源：Snorkel AI、TechCrunch、MindStudio）

对国内从业者的意义：
Grok/xAI API 在国内无直接合规访问路径。但价格信号对竞争格局有参照压力：若 Opus 级别性能可在 $2/$6 获得，国内替代模型（DeepSeek、Kimi、GLM 等）在定价策略上面临参照系下移。有出海业务的 AI 应用开发者可通过合规中间层（如 AWS Bedrock 等）评估 Grok 4.5 的实际可用性。

延伸阅读：
- https://snorkel.ai/blog/grok-4-5-testing-results-how-spacexais-new-model-performs-on-real-professional-work/
- https://techcrunch.com/2026/07/08/spacexai-releases-grok-4-5-which-elon-describes-as-an-opus-class-model/

---

## 2. 新产品 & 功能发布

- **NVIDIA Nemotron Audex 30B-A3B** — NVIDIA

  核心能力：
  - 单一 MoE 模型覆盖音频理解、自动语音识别（ASR）、翻译、文字转语音（TTS）四项能力
  - Open weights，已上架 Hugging Face，支持 vLLM、SGLang、Transformers 推理框架
  - 针对不同任务提供推荐推理配置

  链接：https://huggingface.co/nvidia/Nemotron-Labs-Audex-30B-A3B
  立即试用优先级：本周内试
  理由：当前最完整的开源统一音频大模型，30B 规模在合理部署成本内；engagement_rate 1.83%（极高），工程师群体已在大量存档备查。

- **COLIBRI** — 开源社区（Apache-2.0）

  核心能力：
  - 在 25GB RAM、无 GPU 消费级机器上运行 GLM-5.2（744B 参数）
  - 核心参数驻留 RAM，其余参数从磁盘按需流式加载，无需完整 VRAM
  - Apache-2.0 授权，GitHub 2.1k Stars

  链接：链接未提供（推文中未附 GitHub URL，可搜索 COLIBRI GLM-5.2）
  立即试用优先级：本周内试
  理由：744B 模型在消费级机器运行是本地部署领域的工程突破，对私有化/离网部署场景有直接参考价值；engagement_rate 1.40%。

- **MuScriptor** — @kyutai_labs / @MireloAI

  核心能力：
  - 将任意音频（含 Suno 等 AI 生成音乐）自动转录为乐谱
  - 可导入主流 DAW（数字音频工作站），提供精细编辑控制
  - 由 Kyutai Labs 与 MireloAI 联合开发

  链接：链接未提供
  立即试用优先级：观望
  理由：填补了 AI 音乐领域的乐谱转录空白，但目前 API 可用性和定价信息待确认。

- **Character.AI FM** — Character.AI

  核心能力：
  - AI 生成原创音频剧，分集制，涵盖 romance/thriller/horror 等类型
  - 在 Character.AI 应用库和 c.ai/fm 网页端提供流媒体播放

  链接：http://c.ai/fm
  立即试用优先级：观望
  理由：AI 音频内容产品化的早期探索，对内容赛道从业者有参考价值，但发布互动数据有限（10 likes），早期关注度尚低。

---

## 3. 行业趋势 & 热议话题

- **"Opus 级别"多模型格局形成，单一最强模型叙事终结**

  参与讨论的主要声音：@Alezander907（Browser Use）、@Designarena / @sherwinwu（OpenAI）、@s_batzoglou（ICML 2026 Spotlight 论文作者）、@alexandr_wang（Meta Chief AI Officer）
  主流观点：在 4 个独立评测框架/机构中，至少 4 个模型（Grok 4.5、GPT-5.6 Sol、Claude Fable 5、Meta Muse Spark 1.1）在各自擅长的维度上达到或超过 Opus 4.8 水准，"最强模型"不再是单一答案，不同任务类型对应不同最优选项。
  主要分歧：基准之间结论不兼容——同一模型在 A 基准领先、B 基准落后，benchmark 代表性和操控风险成为核心争议。
  信号强度：强
  判断依据：4 个来自不同独立机构（第三方 agent 框架、设计评测平台、ICML 学术论文、Meta 内部评测）的来源在 24 小时内指向同一现象，且定价差异（Grok 4.5 $2/$6 vs Opus $5/$25）提供了明确的市场数据支撑。

- **企业 AI 学习循环所有权成为 C 级议题**

  参与讨论的主要声音：@satyanadella（Microsoft CEO）、@AravSrinivas（Perplexity CEO）
  主流观点：AI 生成价值的分配取决于谁拥有学习循环；基础模型厂商当前的蒸馏条款和客户数据使用权正在形成对企业不利的不对等格局，企业应主动争取控制权。
  信号强度：中
  判断依据：2 个独立来源，其中 1 个为当事方官方（Microsoft CEO），符合趋势成立门槛；目前仅限两位企业 CEO 公开表态，尚未出现监管层或独立研究机构的跟进验证。

---

## 4. 值得关注的洞察 & 观点

- @fchollet（Keras 创始人、ARC-AGI 联合创始人）：

  「The weak AI code gen we had until late last year was most useful to low-skill programmers -- it was raising the floor. [...] the strong AI code gen we have now is *most* useful to high-skill programmers, while low-skill programmers are vastly underutilizing it or sometimes drowning in it. It went from a crutch to a power tool.」
  为什么值得关注：直接指出 AI 代码工具在技能层分布上完成了"翻转"——不再是低技能程序员的护盾，而是高技能程序员的放大器。Chollet 有 ARC-AGI 基准构建经验，此判断有测量基础而非直觉推测，且与当前大量开发者的实操感受吻合。engagement_rate: 0.31%。

- @yunta_tsai（AI 研究员，被 @elonmusk 转发）：

  「I would like to offer a counterargument that LLMs (or maybe AIs) cannot jump. [...] Currently we have not run an agent for years of compute. The sessions are often fragmented and disoriented, so every new session is almost a fragmented memory of the past, but it may not be for long.」
  为什么值得关注：用 AlphaGo 的 Monte Carlo Tree Search 类比反驳"LLM 无法产生科学突破"，核心前提是：当前 AI 会话碎片化，没有进行连续数年的长程推理，突破可能在 agent 连续运行时间足够长时才出现。这是一个可以被实验证伪的具体假设，而非纯粹哲学猜测。bookmarks: 401，engagement_rate: 0.05%。

- @AravSrinivas（Perplexity CEO）：

  「Humans are pretty good at tool use. Especially using tools like frontier models that are far more power hungry and intelligent than humans in specific dimensions. This suggests that local models will be able to control and use frontier models effectively and will become the default entry point to operate most tasks by running at minimal power and costs.」
  为什么值得关注：从成本和能耗逻辑推导出具体的架构预测：本地轻量模型作为 orchestrator、前沿大模型作为 tool，将成为默认 agent 架构。Perplexity 同时部署本地推理和前沿模型 API，这是有实操基础的结构性判断，而非单纯技术路线主张。likes: 622，engagement_rate: 0.17%。

- Chamath Palihapitiya（via @dnapway，今日被 @GaryMarcus 引用；原文发布时间早于本期窗口）：

  「Our token costs are doubling every 45 days. [...] downstream productivity? [...] maybe 5% max. [...] We're going to take a step back and try to figure out what to do.」
  为什么值得关注：极少数公开量化 AI ROI 失衡的高知名度企业家——"成本每 45 天翻倍、收益仅涨 5%"是一个可追踪的反向数据点，与众多 AI 应用公司 CFO 私下判断方向一致，但公开量化的案例极少。需注意：数字为口述，来源单一，不可直接推广到其他公司。@dnapway 原推 likes: 2,878。

- @geohotarchive（George Hotz，今日被 @AravSrinivas、@GaryMarcus 引用；原文发于 2026-07-11）：

  「No matter how high quality your tokens are, they cannot turn lead into gold.」（出自博文 "AI 2040 and the Cult of Intelligence"）
  为什么值得关注：直接针对 AI 安全主义者关于 AI 控制和算力限制的政策倡议，核心论点是：物理现实的约束（hardware、物流、真实工程复杂度）不会被智能消解，AI 预测框架过度依赖纯粹的信息论推导而忽视现实摩擦。@AravSrinivas 转发（engagement_rate: 0.46%，bookmarks: 976），是本期收藏量最高的洞察类内容。

---

## 5. 实用资源 & 教程

- **The Well — 物理模拟开源数据集**

  类型：数据集
  用途：16 个物理领域的 15TB 高保真模拟数据（湍流、超新星爆炸、磁流体宇宙流、声学散射、活性生物物质等），专为训练 PDE 代理模型（偏微分方程神经网络代理）设计，支持 PyTorch 直接加载
  链接：https://polymathic-ai.org/the_well/
  上手难度：高（需偏微分方程或物理模拟背景才能有效使用）

  出品方：Polymathic AI，联合 Flatiron Institute、Princeton、Cambridge、NYU、Berkeley、Los Alamos 等机构。engagement_rate: 1.53%（极高信号）。

- **MIT CSAIL 强化学习免费指南**

  类型：教程
  用途：系统回答 RL 关键问题的免费参考手册，涵盖主要 RL 算法比较与使用场景
  链接：https://shorturl.at/zcciv
  上手难度：中

  engagement_rate: 2.16%（本期最高），1,538 bookmarks，从业者存档比例极高。作者：@arjunkocher & @sheriyuo，MIT CSAIL 出品。

- **MuScriptor — 音乐乐谱自动转录工具**

  类型：工具
  用途：将任意音频（含 AI 生成音乐）转换为可导入 DAW 的乐谱，填补音乐领域的"Whisper 空白"
  链接：链接未提供
  上手难度：低（面向有 DAW 经验的音乐制作人）

  来源：@honualx（Alexandre Défossez）与 @kyutai_labs、@MireloAI 合作开发，@ylecun 转发。

- **Picbreeder VLM 实验 — Sakana AI**

  类型：研究演示
  用途：在 Picbreeder 开放式创意环境中对比 VLM 与人类的探索行为；提供了罕见的"真实开放式场景下人类 vs AI"比较基准，可直接体验原版 Picbreeder 网站
  链接：https://pub.sakana.ai/picbreeder-vlm/breed/
  上手难度：低（直接在网站体验，无需配置）

  来源：@hardmaru（Sakana AI 联合创始人兼 CEO），分析：@kenneth0stanley。

---

## 一句话总结

今日三个信号同频：模型能力格局从"一强多弱"向"多 Opus 级别、按任务选型"演变，定价差异（Grok 4.5 约为 Opus 的 40%）成为新的竞争维度；Microsoft CEO 公开挑战基础模型厂商对企业学习数据的单向占有，为企业在 AI 合同谈判中提供了 C 级背书；S&P 对 Oracle 的降级把 OpenAI 的盈利能力从私下议题变为对冲基金和中央银行都无法回避的公开风险。

---

## 今日行动建议

今天（30 分钟内）：
基于"Grok 4.5 Browser Use 基准"——在 xAI API 控制台注册账户，提取一个目前在 Claude Opus 上运行的 browser agent 任务，发起同等 prompt 对比测试，记录 token 消耗量和响应质量，5 分钟内可得初步数据点。

本周内：
基于"Satya Nadella 学习循环文章"——梳理团队与 AI 厂商签订的合同条款，检查是否存在厂商对客户使用数据的训练授权条款；若存在，评估是否值得重新谈判，产出一页内部备忘（以微软"学习循环自控"框架作为谈判依据）。

月内验证：
基于"S&P Oracle/OpenAI 信用风险"——设置三个跟踪指标：① Oracle 信用评级是否再降一级（进入垃圾级阈值）；② OpenAI 下一轮融资估值或盈利里程碑是否披露；③ 主流 AI 推理 API 定价是否出现异动。任何一个触发，意味着 AI 基础设施的金融风险已进入下一阶段。

---

## 传播力素材

- 「The weak AI code gen we had until late last year was most useful to low-skill programmers... It went from a crutch to a power tool.」— @fchollet · 👍1,086 👁78,385 · engagement_rate 0.31%
  改写方向：适合技术博客或 LinkedIn，角度："当 AI 成为'高手放大器'而非'低手护盾'，代码基础的价值被重新定价"
  点评：Chollet 指出的翻转是反直觉的——大众叙事是"AI 让初学者也能编程"，但此观察精确指出强 AI 工具在使用门槛和收益分配上的不对称。局限：来自单一框架，低代码平台和非技术用户的 AI 产品化赛道可能有相反结论。只看这句话容易误解为"AI 歧视初学者"——实际意思是工具的使用难度门槛提高了，初学者需要先提升基础技能才能充分发挥 AI 的杠杆效果。

- 「Our token costs are doubling every 45 days. [...] downstream productivity? [...] maybe 5% max.」— Chamath Palihapitiya（via @dnapway）· 👍2,878（@dnapway 原推）· engagement_rate [未知]
  改写方向：适合企业 CFO 受众，角度："AI 支出翻番时代，怎样建立自己的 ROI 底线"
  点评：极少数公开量化 AI ROI 失衡的商业案例，能引发共鸣是因为说出了许多 AI 团队私下计算后不敢公开的数字。局限：数字为口述，来源单一，没有详细方法论披露。只看这句话易误解为"AI 无效"——Chamath 的实际结论是"当前使用方式需要调整"，而非放弃 AI。

- 「Currently we have not run an agent for years of compute. The sessions are often fragmented and disoriented... but it may not be for long.」— @yunta_tsai（被 @elonmusk 转发）· 👍2,064 👁778,710 · bookmarks 401
  改写方向：适合 AI 研究者受众，角度："AlphaGo 时刻尚未到来——为什么 AI 的真正突破需要连续运行数年"
  点评：力量在于提出了可证伪的具体前提：能力涌现的条件是"连续长程计算"，而非仅仅更多参数。局限：即便 agent 持续运行数年，是否能产生 Einstein 式突破仍是未解命题，此论点更接近猜测而非工程预测。过度解读会产生"只要 agent 跑够久就能产生科学发现"的误解，而这忽略了记忆架构、目标设定等工程难题。

- 「Humans are pretty good at tool use... local models will be able to control and use frontier models effectively and will become the default entry point to operate most tasks.」— @AravSrinivas（Perplexity CEO）· 👍622 👁56,889 · engagement_rate 0.17%
  改写方向：适合 AI 产品架构师，角度："你的下一个 AI 应用，默认入口可能不是大模型"
  点评：从成本和能耗推导出的架构预测，Perplexity 的实际部署经验给这个判断提供了实操基础。局限：前提是本地模型的 orchestration 能力要足够强，而当前多数本地模型在复杂任务分解上仍有明显短板。过度解读会认为"本地模型将替代前沿模型"——Aravind 的意思是分工协作而非替代。

---

## 信号 / 噪音比

进入第 1 节的有效新闻 5 条，进入第 2-5 节的有效信号 14 条，剩余约 73% 为低价值或噪音（主要来源：@ylecun 共 13 条发文中约 10 条为美国政治评论；@elonmusk 共 12 条中约 7 条为 Grok 4.5 政治中立性宣传或非 AI 话题；另有体育赛事、Shopify 非 AI 内容各 1-2 条）。今日整体信号密度：正常。

**本期信源**：@satyanadella @AravSrinivas @elonmusk @Alezander907 @GaryMarcus @claudeai @OpenAI @EthanJPerez @ClementDelangue @pwang @ylecun @fchollet @emollick @MIT_CSAIL @hardmaru @sama @tegmark @alexandr_wang @JeffDean @character_ai @geohotarchive（共 21 位）
