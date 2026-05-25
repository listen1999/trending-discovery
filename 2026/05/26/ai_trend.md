# AI 行业情报简报 | 2026-05-26

> 数据窗口：2026-05-25 06:00 — 2026-05-26 06:00（北京时间，过去 `24 小时`）
> 深度分析：3 条 | 模板版本：v2.3

---

## 1. 重大新闻 & 突发事件

- xAI Grok 基础模型 V9-Medium（1.5T）完成预训练，2–3 周后开放

  来源：@elonmusk · 约 16 小时前
  关键数字：1.5T 参数（来源：@elonmusk，当事方口径，未经独立验证）；当前生产版 v8-small 为 0.5T；公开发布预计 2–3 周内，已开始 SFT，RL 在数天内启动
  行业影响：xAI 时隔半年再推前沿基础模型，规模直接 3 倍于在产模型，且 Musk 明确强调"难度高的编码任务上明显提升"。监督训练阶段加入大量 Cursor 用户行为数据（不是公开 GitHub 代码），意味着新模型在 IDE 内的 agentic 操作链路上有了真实分布的训练源——这是 OpenAI、Anthropic 与 xAI 这一轮编程能力角力的新变量。

- Google DeepMind AlphaProof Nexus 自主求解 9 个开放 Erdős 问题、44 条 OEIS 猜想

  来源：@GoogleDeepMind / @pushmeet · 约 5 小时前
  关键数字：9/353 个开放 Erdős 问题（来源：arXiv:2605.22763 + Google DeepMind 官方），其中 2 题已开放 56 年；另证明 1 个 15 年未解的代数几何问题、1 个 7 年未解 min-max 优化问题；单题推理成本"几百美元量级"（来源：the-decoder.com 报道 DeepMind 数据）
  行业影响：第一次出现公开可复现、可被 Lean 形式化校验的 agentic 数学突破，验证了"LLM 提议 + 形式化校验 + Elo 评分多 agent 协同"这一研究范式的可行性。对应用侧的直接读法：在结果可被独立验证的窄域（数学、形式化合同、定理求解、协议证明），Gemini 3.1 Pro 这一级别的模型 + 简单 agent loop 已经能产出研究级成果，门槛低到值得创业者重新评估垂类。

- 教皇利奥十四世首份通谕《Magnifica humanitas》专门讨论 AI，Anthropic 联合创始人 Chris Olah 现场宣读

  来源：@AnthropicAI · 约 3 小时前
  关键数字：83 页通谕（来源：religionnews.com）；这是历史上首份由教皇亲自向公众发布的通谕，也是首份系统讨论 AI 的天主教教廷文件
  行业影响：把"AI 必须服务全体人类、不得成为少数富国/资本的工具"写入了天主教廷的最高级别教导文件，与 5 月以来欧盟 AI Act 二阶段执行、英国 AI Bill 二读形成共振。对前沿实验室而言，这是第一份不来自监管机构、却面向全球 14 亿信众的"道德合规叙事"框架；Anthropic 主动站台，相当于公开把 alignment / interpretability 工作绑定到这套叙事上，与 xAI、OpenAI 路线形成明显公关分野。

---

## 深挖：xAI Grok 基础模型 V9-Medium 完成训练

背景补充：
V9-Medium 是 xAI 自 5 月以来主推的"中等档"前沿模型。在产的 v8-small 仅约 0.5T 参数，主要承担 Grok 产品流量；V9 直接跳到 1.5T 量级，并保留更大档（V9-Heavy）的命名空间。多家行业报道交叉确认该模型采用了"大量 Cursor 数据"做监督训练，目的明确指向编码能力（basenor、techloy、capitalbay）。

数字核实：
1.5T 参数 → 已验证（来源：@elonmusk 原贴 + KuCoin/Caliber/Odaily 同步报道），口径一致，无独立基准跑分。
2–3 周后发布 → Musk 当事方时间表，未经独立验证；过去 xAI 的发布节奏经常滑期，应保留怀疑。
"难度高的编码任务上明显提升" → Musk 表态，无第三方评测。

扩展影响：
The Information / Eyerys 报道 SuperGrok 订阅用户已经在反馈生成额度被收紧，业内普遍解读为给 V9 让出推理算力。capitalbay.news 同时点出"使用 Cursor 数据"引发的数据合规疑问——Cursor 的服务条款是否允许其用户的代码上下文流向第三方训练管线尚未公开答复。

对国内从业者的意义：
两个具体读法。其一，国内编程类 SaaS（Cursor 平替、IDE-内 agent 产品）应当意识到自己产品中沉淀的"用户行为数据"已经成为前沿实验室的差异化训练源——是壁垒，也是潜在数据合规风险点，需要在 ToS 与数据流向上提前定调。其二，Grok 在中国不直接销售，但 Grok Build CLI 已对全球 X Premium+ 开放（见第 2 节），国内有海外账号的开发者将在 2–3 周内获得一个新的编码模型选择，Qwen3-Coder、DeepSeek-Coder、MiMo V2.5-Coder 等国产线需要在新基线下重新校准定位。

延伸阅读：
https://x.com/elonmusk/status/2058787384364265734
https://www.basenor.com/blogs/news/grok-v9-medium-1-5t-finishes-training-release-in-2-3-weeks

---

## 深挖：Google DeepMind AlphaProof Nexus 求解开放 Erdős 问题

背景补充：
AlphaProof Nexus 是一套"agentic 形式化证明搜索"框架：Gemini 3.1 Pro 生成证明草稿，由 Lean 形式化验证器逐步核验，Gemini 3.0 Flash 构建的评分 agent 用 Elo 体系排序候选解。完整 Agent (D) 配置被用于 Erdős 问题集（the-decoder、cryptobriefing、officechai 一致报道）。论文 arXiv:2605.22763 已于 5 月 21 日预印。

数字核实：
9 个开放 Erdős 问题（含 2 题开放 56 年）→ 已验证（来源：arXiv 论文 + DeepMind 官博）。
44 个 OEIS 开放猜想 → 已验证（来源：arXiv 论文）。
15 年未解代数几何问题、7 年未解 min-max 优化问题 → 已验证（来源：@pushmeet 推文 + arXiv 论文）。
单题成本"几百美元" → 来源：the-decoder 引用 DeepMind 数据，未见 DeepMind 公开成本分摊明细，可信但属二手转述。

扩展影响：
社区两极反应：DeepMind 自家 CEO Demis Hassabis 同期在采访中明确"今天的系统离 AGI 还很远，无论你解多少 Erdős 问题"（见第 4 节），主动给热度降温。学界一侧 @ValerioCapraro 等评论指出，Erdős 问题大多是组合学、有限空间问题——恰好是当前大模型 + 搜索最擅长的场景，距"发明新数学对象"的能力仍有明显鸿沟。Noah Smith 等评论者则质疑"专业数学家多年没解出来"是否被夸大。

对国内从业者的意义：
具体可执行。其一，国内做 Lean / Coq 形式化的小团队（中科院、清华、北大、Numina 等）此前主要做基础设施，AlphaProof Nexus 用 Gemini 通用模型 + 简单 agent loop 就拿到研究级成果，说明垂类 agent 已经不再需要专门微调出来的"数学模型"——给国内复刻路径降低了模型门槛。其二，"LLM 提议 + 形式化验证器校验"这一架构可以直接迁移到合同条款验证、智能合约审计、SLA 合规检查等中国出海与企业服务场景，验证器替换 Lean 即可，是国内做企业级 agent 的现成模板。

延伸阅读：
https://arxiv.org/abs/2605.22763
https://the-decoder.com/google-deepminds-alphaproof-nexus-solves-decades-old-math-problems-for-a-few-hundred-dollars/

---

## 深挖：教皇利奥十四世通谕《Magnifica humanitas》

背景补充：
来源已充分，背景核实跳过。Vatican News 与 National Catholic Reporter 已确认通谕 5 月 25 日发布，由教皇本人亲自向公众宣读（教廷历史首例），Anthropic 联合创始人 Chris Olah 在梵蒂冈观众席就坐并发表英文讲话。Anthropic 官网同步刊出讲话全文。

数字核实：
83 页通谕 → 已验证（来源：religionnews.com）。
"集中于少数富裕国家"、"AI 红利需全球共享" → Olah 讲话原文，已验证（来源：anthropic.com）。

扩展影响：
NCR 报道指出，教廷选择在通谕发布时同台 Anthropic，是天主教廷有意识地与"以安全为旗号的实验室"建立长期对话的信号，而非偶发邀请。Angelus News 引述教皇当场感谢 Olah 的研究工作。社交平台上的反应分裂：@DavidSacks 等代表的硅谷右翼公开反驳，警告"以安全为名给政府收编 AI 等于打开 1984 式监控大门"；@vkhosla 则指控通谕的"AI 该如何与世界互动是给人文、宗教、哲学的问题"是"精英主义"。@tegmark 则强调通谕中"人性不可被替代或超越"一句实质上是对 superintelligence 路线的否定。

对国内从业者的意义：
两点具体影响。其一，对出海做欧洲、拉美市场的中国 AI 产品（特别是教育、医疗、儿童陪伴类），通谕将在未来 12 个月内成为天主教国家公共采购、教育部门审批环节的隐性合规背景，建议产品白皮书提前对齐"人为本、不可替代论"叙事。其二，国内监管框架与天主教伦理框架走的是两条完全独立路径，本通谕对国内合规没有直接约束力，但 Anthropic 借此完成的"安全叙事 + 人文叙事"双轨绑定，是国内大模型公司值得借鉴的对外话术策略，特别是对 ESG/合规敏感型客户。

延伸阅读：
https://www.anthropic.com/news/chris-olah-pope-leo-encyclical
https://www.ncronline.org/vatican/vatican-news/pope-leo-anthropic-co-founder-call-church-tech-ethics-partnership-magnifica

---

## 2. 新产品 & 功能发布

- Grok Build Beta — xAI

  核心能力：
  - Plan Mode（计划-执行-验证三段式 agent loop，由 Musk 亲自示范典型 prompt）
  - Imagine 集成（CLI 内直接生成、编辑图像与视频素材）
  - 原生 sub-agent + worktree 编排，<1 秒级别 Web/X 搜索

  链接：https://x.ai/cli
  立即试用优先级：本周内试
  理由：对所有 SuperGrok 与 X Premium+ 订阅用户全面开放，安装命令一行（curl 脚本），可与 Claude Code、Codex 直接做编码任务对比。

- LongCat 开源 talking-avatar 模型 — Meituan LongCat（Hugging Face 上线）

  核心能力：
  - MIT 许可证，单图驱动可生成讲话头像视频
  - Hugging Face 官方 demo 免费可跑（@victormustar 已建好 Space）
  - 适配对口型、配音、NPC 对白等下游场景

  链接：huggingface.co 上 LongCat 模型卡（推文未给定 ID）
  立即试用优先级：今天就试
  理由：MIT 协议 + 免费 demo + 商业可用，是当前开源 talking-head 模型中最少法律摩擦的一条线。

- LeRobot 桌面人形机器人 — Hugging Face

  核心能力：
  - 约 2,500 美元 BOM 即可组装人形机器人
  - 全栈开源：硬件、仿真环境、训练管线、运行时与数据集
  - 适配 agentic 编程（推文中提到 8 岁儿童用 Codex 为其加功能）

  链接：推文中未给出官方仓库，需在 huggingface.co/lerobot 检索
  立即试用优先级：本周内试
  理由：是目前价格-能力比最低的开源人形机器人参考设计，对教育、机器人学习数据采集团队有直接价值。

- MiniCPM5-1B 全量开源 — OpenBMB（面壁智能）

  核心能力：
  - 1B 参数，Artificial Analysis 榜单 ≤2B 模型第 1（17.9 分），击败 Qwen3.5-2B（16.3）
  - INT4 量化后 0.5GB，可在手机、浏览器、边缘设备运行
  - 权重、训练数据、部署代码全部开源
  - 训练框架 ForgeTrain "完全由 AI 编写、零人类程序员"，自称比 NVIDIA Megatron 快 10%（来源：@huggingface 转 @ModelScope2022，当事方口径，未经独立验证）

  链接：https://modelscope.cn/models/OpenBMB/MiniCPM5-1B
  立即试用优先级：今天就试
  理由：国产端侧模型新基线，0.5GB 体量直接覆盖国内移动端、车机、IoT 场景，国内可直接访问 ModelScope。

- MiMo V2.5-Coder（Q2 量化）— Xiaomi（jedisct1 量化版 Hugging Face 上架）

  核心能力：
  - 128GB 内存机器可本地跑
  - 体感超越 Qwen 3.6 与 DeepSeek 4-Flash（来源：@jedisct1 主观测试，未经独立验证）
  - 适合本地代码助手日常使用

  链接：https://huggingface.co/jedisct1/MiMo-V2.5-coder-Q2
  立即试用优先级：本周内试
  理由：是 Xiaomi 加入开源编码模型竞赛的新一代产品，与 DeepSeek、Qwen、GLM 形成国产开源编码模型四强格局。

- Kimi K2.6 — Moonshot AI

  核心能力：
  - Design Arena 3D Design 榜单第 1（开源权重）
  - 击败 Claude Opus 4.7、Gemini 3.5 Flash、GPT 5.5（来源：@Designarena 榜单）
  - 较前代 K2.5 上升 18 位

  链接：推文未直接给链接，可在 designarena.ai 验证排名
  立即试用优先级：今天就试
  理由：3D 设计是少数开源权重模型整体占优的赛道，对独立游戏、3D 内容、CAD 自动化创业者是首选 baseline。

- llama.cpp 加入 MTP（Multi-Token Prediction）支持 — open-source

  核心能力：
  - Qwen3.6-27B 密集模型本地推理：A10G 上 25 tok/s → 45 tok/s（+78%，来源：@ClementDelangue 实测）
  - 让本地大模型作为日常驱动器变得现实

  链接：llama.cpp GitHub
  立即试用优先级：本周内试
  理由：直接提升所有 llama.cpp 部署的吞吐，是过去半年本地模型最大的性能跃迁之一。

---

## 3. 行业趋势 & 热议话题

- 开源小模型在专项榜单与端侧场景全面咬住闭源旗舰

  参与讨论的主要声音：@ClementDelangue、@huggingface、@ModelScope2022、@jedisct1、@Designarena
  主流观点：同一窗口内三条独立信号——Kimi K2.6（3D Design 第 1）、MiniCPM5-1B（≤2B 模型 SOTA）、MiMo V2.5-Coder（本地编码超 Qwen 3.6/DeepSeek 4-Flash）——共同指向"开源在专项窄域追平甚至反超闭源旗舰"已经是稳定现象。
  主要分歧：闭源阵营仍掌握 horizon-level capability（agent、长 context、多模态深度推理）。
  信号强度：强
  判断依据：三条信号分别来自 Moonshot、面壁、Xiaomi 三个独立组织，皆 24 小时内集中释放，且都附榜单/可复现数据，不是单一观点。

- AI 资本周期与"泡沫破裂"风险被主流声音公开背书

  参与讨论的主要声音：@sundarpichai（BBC 采访）、@GaryMarcus、Andrew Ross Sorkin（60 Minutes）、Larry Fink（BlackRock CEO，被 @ShadowofEzra 引述）、@geohotz（博客 The Eternal Sloptember）
  主流观点：AI 投资规模与短期回报严重失衡，编码这一"主力支柱"用例的产出质量正在被一线开发者质疑（GeoHot：代码 slop 化），叠加养老金、储蓄账户被引导进入 AI 基础设施融资，系统性风险被多方公开指出。
  主要分歧：David Sacks / Clem Delangue 等以"GitHub commits 同比 14×"为依据反驳"AI 抢工作"叙事，认为生产力红利尚未真正释放。
  信号强度：强
  判断依据：Pichai 是 Google CEO（当事方），Sorkin 是 60 Minutes 财经口主笔，Fink 是 BlackRock CEO，GeoHot 是工程师端代表——四个不同身份、不同立场的主流声音同窗口齐发声，明显超出单一账号噪音。

- AGI 时间表降温：JEPA / 世界模型派与 LLM 派的争论再次升温

  参与讨论的主要声音：@demishassabis（"我们离 AGI 还非常远"）、@ylecun（JEPA-WM v2 论文 TMLR 接收）、@SchmidhuberAI（指控 JEPA 等同其 1992 PMAX）、@GaryMarcus、@ns123abc、@ValerioCapraro
  主流观点：在 AlphaProof 等 narrow 突破的同时，世界模型、形式化推理、神经符号等"非 LLM 主路径"的话语权显著增强；最有公信力的实验室负责人主动给 AGI 叙事降温。
  主要分歧：Schmidhuber 与 LeCun 的归属权之争（学术伦理），与 LLM-as-AGI vs 世界模型这两个层级的争论被有意无意混在一起。
  信号强度：中
  判断依据：3 个独立来源（DeepMind / Meta-NYU LeCun / IDSIA Schmidhuber）+ 多位学界评论者同窗口共振，且伴随真实学术动作（TMLR 接收、IDSIA-3-22 报告发布），不是单一观点。

---

## 4. 值得关注的洞察 & 观点

- @demishassabis（DeepMind CEO、诺贝尔奖得主）：

  「Today's systems are nowhere near [AGI]. Doesn't matter how many Erdős problems you solve… I think it's far, far from what a true invention, or someone like Ramanujan, would have been able to do.」
  为什么值得关注：这是 AlphaProof Nexus 自家发布方 CEO 的主动降温——把"narrow benchmark 攻克"与"AGI 真正缺失能力"严格切开，是当前过热估值环境下罕见的负向校准信号。

- @fchollet（Keras 作者、ARC-AGI 共创）：

  「Thinking of AI as a productivity booster for prior workflows is the wrong framing. Like all of the previous waves of computerization/softwarization, AI is a tool that lets you do new things in new ways.」
  为什么值得关注：把"用 AI 提速旧 SOP"和"用 AI 重新设计新工作流"两类创业者明确切开——前者天花板就是单点效率改进，后者才有重塑公司形态的可能。给产品经理选题提供了明确判别框架。

- @sundarpichai（Google CEO，BBC 采访）：

  「There is some irrationality in the current AI boom… asked what happens if the AI bubble pops: I think no company is going to be immune, including us.」
  为什么值得关注：第一次有头部超级应用厂商 CEO 公开承认资本周期非理性、且明示"自家也躲不掉"。与 Larry Fink、Andrew Sorkin 的预警形成同期共振（见第 3 节），是当前主流叙事的明显裂缝。

- @vkhosla（KhoslaVentures 创始人）：

  「Founders should work on things AI is not good at... Agree focusing on AI's weakness will accelerate it and create opportunities.」并加注 autoformalization 是 ASI 的关键拼图，6 月 10 日与 PramaanaLabs 联办验证峰会。
  为什么值得关注：来自顶级 AI 投资人的反向选题指引——明确把"AI 当前最弱的地方"作为创业方向，而不是追前沿模型能力。配合 6 月 10 日 verification summit 的具体动作，是可被跟踪的资金信号。

- @ClementDelangue（Hugging Face CEO，转 @DavidSacks）：

  「14× YoY increase in GitHub commits… AI has dramatically lowered the cost of writing code, so it's now being used across far more businesses, applications, and use cases.」
  为什么值得关注：用 GitHub commits 同比 14× 的量化数据，正面反驳"AI 抢走开发者岗位"的主流叙事，给"软件需求弹性大于自动化"假说提供了第一组公开数据点。数字来源为 GitHub 平台数据（来源：@DavidSacks，二手转述，未经独立验证）。

---

## 5. 实用资源 & 教程

- AlphaProof Nexus 论文（Advancing Mathematics Research with AI-Driven Formal Proof Search）

  类型：论文
  用途：研读 LLM + Lean + 多 agent Elo 评分的 agentic 证明范式，可直接迁移到形式化合同、智能合约审计、协议证明
  链接：https://arxiv.org/abs/2605.22763
  上手难度：高

- PhysX-Omni Physical AI 框架

  类型：开源项目
  用途：刚体、可变形体、关节物体统一的 sim-ready 生成框架，配套 PhysXVerse 数据集与新 benchmark
  链接：https://physx-omni.github.io、https://github.com/physx-omni/PhysX-Omni、https://huggingface.co/datasets/PhysX-Omni/PhysXVerse
  上手难度：中

- NayanaOCR Corpus

  类型：数据集
  用途：1M+ 文档图像、22 种语言的开源合成多模态多任务文档语料，可用于多语言 OCR、文档理解、RAG 预处理训练
  链接：推文未直给（@cognitivelab_ai 发布，在 Hugging Face 检索"NayanaOCR Corpus"）
  上手难度：中

- "Cognitive offloading and the speedup illusion in human-AI interaction" 论文

  类型：论文
  用途：斯坦福、剑桥等团队对"人 + AI 协作中的认知外包与速度幻觉"的实验研究，给设计 AI 副驾驶类产品提供反向警示
  链接：https://arxiv.org/abs/2605.23177
  上手难度：低

---

## 今日行动建议

今天（30 分钟内）：
基于 AlphaProof Nexus 自主求解 9 个开放 Erdős 问题——花 20 分钟读完 arXiv:2605.22763 的方法章节（重点看 Agent A/B/C/D 的拆解与 Elo 评分实现），并在笔记里写下 3 条可迁移到自家垂类（合同/合规/审计/协议）的验证器替换方案。

本周内：
基于 xAI Grok 基础模型 V9-Medium 完成训练——在 V9 公开发布前的 2–3 周窗口期内，跑一份内部 PoC：以现有主力编码模型（Claude Sonnet 4.6 / GPT-5.5 / DeepSeek-Coder / Qwen3-Coder）为基线，准备一组 20–30 题的真实业务编码评测集，明确"难任务"分布，等 V9 一上线即可直接出对比结论而不是临时设计评测。

月内验证：
基于开源小模型在专项榜单全面咬住闭源旗舰这一趋势——在接下来 30 天里持续跟踪 Design Arena、Artificial Analysis、LMArena 三个第三方榜单上 Kimi K2.6、MiniCPM5-1B、MiMo V2.5-Coder、GLM 5.1 的排名与权重下载量（Hugging Face 月下载、ModelScope 月下载），若 30 天内仍能保持各自专项榜单前三且累计下载破百万，则将"窄域选型默认开源"写进团队的模型采购 SOP。

---

## 传播力素材

- 「I'm now in the LeCun/Marcus camp on LLMs. Real programming agents will need world models, not some RLVR shit. It's over.」— @ns123abc（被 @GaryMarcus 转推）· 👍1460 👁241192 · engagement_rate 0.28%
  改写方向：适合知乎/即刻技术圈短帖，配 GeoHot 博客《The Eternal Sloptember》做"硬核 AI 工程师集体转向"叙事
  点评：这条话之所以传播，是因为它把过去两年最重要的两个反对派（LeCun 的世界模型派、Marcus 的神经符号派）在一个 AI-philic 工程师的口中合流。盲区是它把"LLM 不够"等同于"LLM 路线已终结"，事实上 AlphaProof 这种 LLM + verifier 的混合方案恰恰证明现有范式还在快速产出研究级成果——这条话当口号有力，当判断会误导。

- 「We will have a crash, I just can't tell you when, and I can't tell you how deep. But I can assure you, unfortunately, I wish I wasn't saying this, we will have a crash.」— Andrew Ross Sorkin（被 @GaryMarcus / @60Minutes 转推）· 👍6232 👁1878753 · engagement_rate 0.13%
  改写方向：适合 36Kr / Substack 财经向短评开头，引出"养老金被引导买 AI 基础设施"的链条
  点评：Sorkin 是《1929》作者，预言"会崩"几乎是他的人设输出——这一类预言不可证伪，但放在 Pichai 自己承认非理性、Larry Fink 表态把储蓄账户引导进 AI 基础设施的同一周内，叙事密度是真实的。读者要警惕的是：单独一句"will crash"在过去 24 个月每个季度都有名人说过一次。

- 「There is some irrationality in the current AI boom. No company is going to be immune, including us.」— @sundarpichai（BBC 采访，被 @Vivek4real_ 引述、@GaryMarcus 转推）· 👍1032 👁178866 · engagement_rate 0.12%
  改写方向：适合 LinkedIn / 公众号"领导力 + AI 战略"题材，做"超级应用 CEO 第一次承认自家也躲不掉"的反共识引子
  点评：这句话强在角色——超级应用厂商 CEO 主动给自家叙事降温，过去三年极罕见。盲区是 Pichai 同期 Google 的 CapEx 仍在加码，"承认非理性"并不等于"会降速"，把这句话理解成战略收缩信号会跑偏。

- 「Today's systems are nowhere near [AGI]. Doesn't matter how many Erdős problems you solve…」— Demis Hassabis（被 @ValerioCapraro 总结）· 👍1409 👁221022 · engagement_rate 0.24%
  改写方向：适合公众号 / 即刻 AI 产品圈做"AGI 时间表降温"专题首条
  点评：Hassabis 在自家 AlphaProof 发布同期给热度降温，是一次刻意的预期管理。需要补充的语境是：他没说"LLM 路线错了"，只说"现在的系统离 AGI 还远"——这与坊间流传的"DeepMind 转向世界模型派"是两件不同的事，单看这句容易误读。

- 「Thinking of AI as a productivity booster for prior workflows is the wrong framing... AI is a tool that lets you do new things in new ways.」— @fchollet · 👍233 👁21062 · engagement_rate 0.38%
  改写方向：适合产品经理/创业者向社群（即刻、生财有术、Indie Hackers）做"AI 创业选题判别"短帖
  点评：这是过去半年最能切创业者痛点的一条判断——它直接把"用 AI 提速 Excel/PPT"和"用 AI 重新设计公司"分成两条不同 ceiling 的路径。盲区是它隐含"前者没价值"的偏见，事实上 95% 的企业级 AI 落地仍然在前者，Chollet 的语境是"创业机会"而非"AI 整体价值"。

---

## 信号 / 噪音比

进入第 1 节的有效新闻 3 条，进入第 2–5 节的有效信号 21 条，剩余约 70% 为低价值或噪音（主要是 @elonmusk 当日大量政治、移民、城市治安转推与短回复，与 AI 行业无关，已剔除）。今日整体信号密度：正常。

**本期信源**：@elonmusk @GaryMarcus @ClementDelangue @huggingface @AnthropicAI @GoogleDeepMind @demishassabis @ylecun @AndrewYNg @AmandaAskell @tegmark @NotionHQ @fchollet @cohere @aidangomez @MIT_CSAIL @nvidia @hardmaru @NandoDF @gdb @tobi @vkhosla @emollick @victormustar @ModelScope2022 @jedisct1 @cognitivelab_ai @ziqi_huang_ @pushmeet @milichab @skcd42 @SchmidhuberAI @ValerioCapraro @DavidSacks @ns123abc（共 35 位）
