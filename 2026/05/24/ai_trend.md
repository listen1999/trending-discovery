# AI 行业情报简报 | 2026-05-24

> 数据窗口：2026-05-23 06:00 — 2026-05-24 06:00（北京时间，过去 `24 小时`）
> 深度分析：3 条 | 模板版本：v2.3

---

## 1. 重大新闻 & 突发事件

- Anthropic Project Glasswing 一个月发现逾 1 万条高危/严重漏洞

  来源：@AnthropicAI（经 @EthanJPerez 转发）· 约 24 小时前
  关键数字：高危/严重漏洞 >10,000 条（来源：@AnthropicAI，当事方口径，未经独立验证）；项目启动至今满 1 月
  行业影响：定义了"未公开前沿模型 + 防御性合作伙伴"的封闭范式。Glasswing 把 Claude Mythos Preview 仅授权给 AWS、Apple、Google、Microsoft、NVIDIA、JPMorganChase、Cisco、CrowdStrike、Palo Alto Networks、Broadcom、Linux Foundation 等 12 家机构（来源：foreignpolicy.com、anthropic.com）。1 万 + 漏洞节奏意味着 AI 辅助漏洞挖掘已从 PoC 进入规模化产线，安全团队的修复节奏需要按小时而不是季度重置。

- Trump 行政令要求绿卡申请人离境申请，AI 产业人才链承压

  来源：@AndrewYNg、@JeffDean、@ylecun 同步转发；底层报道 WSJ、华盛顿邮报
  关键数字：政策 2026-05-22 公布（来源：washingtonpost.com、cbsnews.com）；H-1B 印度持有人占比约 71%（来源：Newsweek，2024 数据）；离境后领事处理周期 12–24 个月（来源：washingtonpost.com）
  行业影响：调整身份（adjustment of status）从默认通道改为"特殊情况"，多数 F-1/H-1B/L-1 想拿绿卡需先离境。Andrew Ng、Jeff Dean、Yann LeCun 三位行业级声音公开反对。USCIS 对 Semafor 表示高技能岗位"短期内可能不受影响"，但无书面例外，雇主侧出现"延后申请 vs 让员工带工作离境"的两难。

- Google Antigravity 2.0 紧急修复 IDE 体验，Demis Hassabis 亲自补偿配额

  来源：@demishassabis · 约 21 小时前
  关键数字：本周第二次重置全员 Gemini 配额（来源：@demishassabis，当事方口径）；Antigravity 2.0 主体于 2026-05-19 I/O 大会发布（来源：blog.google）
  行业影响：I/O 推出的 Antigravity 2.0 默认走 Agent-first 路径，引发 3 天内开发者回流。Google 在 7 天内上线 Antigravity 2.0 更新、补 IDE 接入说明、修复 Windows 启动 bug、并第二次重置配额，说明在与 Cursor、Anthropic Claude Code 的 IDE+Agent 控制权之争中态度变得激进。

---

## TOP 新闻深挖

#### 深挖：Anthropic Project Glasswing 一个月发现逾 1 万条高危/严重漏洞

背景补充：
Project Glasswing 于 2026 年 4 月正式启动，配套未公开的 Claude Mythos Preview 模型；Anthropic 出资 1 亿美元授信，分配给 11 家行业头部企业与 Linux Foundation，仅用于防御性安全研究（来源：foreignpolicy.com、anthropic.com）。完整漏洞清单预计 2026 年 7 月公开摘要报告，目前以加密哈希预承诺（来源：vulncheck.com、cloudsecurityalliance.org）。

数字核实：
"10,000+ 高危/严重漏洞" → 已有多家外部源印证 Mythos 在多个主流操作系统与浏览器中发现"成千上万"漏洞（来源：anthropic.com、justsecurity.org）。具体类别细分未披露，与推文一致，不构成矛盾。

扩展影响：
Foreign Policy 把 Glasswing 定位为"网络攻防节奏被压缩到分钟级"的转折点；VulnCheck 与 Cloud Security Alliance 已开始整理与 Anthropic 研究人员/Glasswing 相关 CVE 的归属表，安全社区已把 Glasswing 当作新的 CVE 源对待（来源：vulncheck.com）。

对国内从业者的意义：
1）出海产品的依赖库今后大概率被 Mythos 类模型扫出未知 0-day，国内开源/SaaS 团队需要把"AI 辅助漏洞披露"纳入安全响应 SOP；2）防御能力侧出现 US-only 准入壁垒——Anthropic 已拒绝中国智库对 Mythos 的访问请求（来源：gigazine.net、scmp.com），国内厂商只能押注开源底座（DeepSeek、Qwen）做对等攻防训练；3）SCMP 报道国内安全产业已被这波公开数据激活，DeepSeek V4 路径中亦在规划对位响应。

延伸阅读：
https://www.anthropic.com/project/glasswing
https://foreignpolicy.com/2026/04/20/claude-mythos-preview-anthropic-project-glasswing-cybersecurity-ai-hacking-danger/

#### 深挖：Trump 行政令要求绿卡申请人离境申请，AI 产业人才链承压

背景补充：
USCIS 于 2026-05-22 公告，将"in-country adjustment of status"重新定义为非常规通道，多数非移民签证持有人需到本国美国领事馆完成永居申请（来源：washingtonpost.com、cbsnews.com）。USCIS 同日对 Semafor 表示 H-1B 高技能岗位"短期内可能不受影响"，但未出具书面例外（来源：semafor.com）。

数字核实：
推文未给具体数字。补充：印度籍 2024 年占 H-1B 发放比例约 71%（来源：newsweek.com）；离境后领事处理通常 12–24 个月，并可能触发 3–10 年再入境禁令（来源：washingtonpost.com、businesstoday.in）。

扩展影响：
TechCrunch、CBS、Semafor 报道硅谷雇主已开始评估"延后绿卡申请 vs 让员工带工作离境"的预案。行业内 Jeff Dean、Andrew Ng、Yann LeCun 三位顶级声音同窗口期公开反对。

对国内从业者的意义：
1）美中 AI 顶级人才回流窗口短期变大，国内大厂与新势力（Moonshot、智谱、阶跃、DeepSeek 等）有 6–12 个月的窗口期挖人；2）想"赴美创办 AI 公司"的中国创业者拿 EB-1/EB-2 难度上升，STEM-OPT 路径成本也跟着抬高；3）Sakana AI 同窗口期在日本开放 5 个软件工程师岗位（来源：sakana.ai/careers），日本/新加坡/英国可能承接部分被美国推开的人才。

延伸阅读：
https://www.cbsnews.com/news/trump-green-cards-leave-us/
https://www.semafor.com/article/05/22/2026/trump-orders-green-card-seekers-to-go-overseas-to-apply

#### 深挖：Google Antigravity 2.0 紧急修复 IDE 体验，Demis Hassabis 亲自补偿配额

背景补充：
Antigravity 2.0 在 2026-05-19 I/O 大会发布，原 IDE 入口被 Agent-first 工作流默认覆盖，引发开发者反弹（来源：techcrunch.com、blog.google）。本周内 Google 已上线 Antigravity 2.0 后续版本、补充 IDE 恢复说明、修复 Windows 启动 bug，并在一周内第二次重置全员 Gemini 配额（来源：@demishassabis、techcrunch.com）。

数字核实：
推文未列具体数字。补充：Gemini 3.5 Flash 同期发布，号称在多数 benchmark 上超过 Gemini 3.1 Pro，且速度为同档前沿模型 4×（来源：webdeveloper.com，未经独立验证）。

扩展影响：
9to5Google、MarkTechPost 报道 Antigravity 2.0 已扩展为五形态平台（桌面、CLI、SDK、Managed Agents API、Enterprise Agent Platform），与 Cursor / Anthropic Claude Code 形成正面 IDE+Agent 竞争。Demis 7 日内两次重置配额，把开发者留存优先级抬到了 marketing 预算之上。

对国内从业者的意义：
1）做 AI 编码工具的国内团队（Trae、CodeBuddy、各 Cursor 国内代理）需评估 Antigravity 2.0 的 Agent 模式对自身差异化的压力；2）"Managed Agents API"提供托管执行 + 计费，意味着出海做 Agent 应用的中国团队可以直接基于 Google 这层托管，不必自建 sandbox；3）国内自研模型团队需观察 Gemini 3.5 Flash 的 4× 加速来源——是 MoE 还是 sparse attention/蒸馏；若是后者，价格战节奏将比预期更快。

延伸阅读：
https://techcrunch.com/2026/05/19/google-launches-antigravity-2-0-with-an-updated-desktop-app-and-cli-tool-at-io-2026/

---

## 2. 新产品 & 功能发布

- ZeroEntropy — 任务特化重排/嵌入模型平台

  核心能力：
  - 6 人团队，单任务速度比 OpenAI/Anthropic 通用模型快 4–8×（来源：@garrytan，二手口径，未经验证）
  - HuggingFace 累计下载 50 万次（来源：@garrytan，二手口径，未经验证）
  - 主打 reranker / embeddings / 客制小模型，可直接替换通用模型层

  链接：https://zeroentropy.dev
  立即试用优先级：本周内试
  理由：被 Garry Tan（YC President）和 Clem Delangue（HF CEO）同窗口期同时背书；如果当前 RAG 栈用的是 OpenAI/Anthropic 通用 embedding，可在本周做一次延迟与成本对照

- RWKV-7 "G1g" — 纯 RNN 架构 7B 模型，单卡 5090 解码 >15,000 tps

  核心能力：
  - 作者口径"目前最强的纯 RNN LLM"（来源：@BlinkDL_AI，当事方口径，未经独立验证）
  - HuggingFace Spaces 提供 7B 推理 demo
  - 6 月将放出 G1h 版本

  链接：https://huggingface.co/spaces/BlinkDL/RWKV-Gradio-2、https://github.com/BlinkDL/Albatross
  立即试用优先级：本周内试
  理由：纯 RNN 内存占用与序列长度解耦，长上下文/端侧场景下与 Transformer 互补，适合做边缘/嵌入式 LLM PoC

- Stable Audio 3 — 一键启动器，无 GPU 也能跑

  核心能力：
  - 跨平台（Mac/Linux/Windows）开箱即用
  - CPU 即可生成 2 分钟片段（来源：@cocktailpeanut，二手口径，未经验证）
  - 与 DAW 插件 gary4juce v4 预先集成

  链接：链接未提供
  立即试用优先级：观望
  理由：CPU 生成时间未经独立基准核实，建议等第三方测评再决定是否纳入工作流

- Codex 计算机使用模式 — 端到端驱动 iPhone Simulator 自检

  核心能力：
  - Codex 自主调用 iPhone Simulator 跑通"构建—调试—回归"闭环
  - 演示者 @JustinBleuel（OpenAI Codex），Greg Brockman 二次背书
  - 当前为 demo，尚未给出普通用户启用细节

  链接：https://x.com/JustinBleuel/status/2058228412158758950
  立即试用优先级：观望
  理由：computer-use × 移动端模拟器场景样例稀少，需要等是否进入 Codex 正式产品线

- DeepSeek Sparse Attention（DSA）from-scratch 参考实现

  核心能力：
  - GPT 风格小模型上的可运行 DSA 实现，含动机、整体结构与单文件代码
  - 社区贡献者编写，Sebastian Raschka 审校
  - 适合理解 DSA 如何嵌入预训练栈

  链接：https://github.com/rasbt/LLMs-from-scratch/tree/main/ch04/09_dsa
  立即试用优先级：今天就试
  理由：3 小时内可跑通；若团队在评估稀疏注意力对 KV cache 的影响，这是门槛最低的入口

---

## 3. 行业趋势 & 热议话题

- "Coding Agent 半年前的最佳实践已经过时"成跨厂共识

  参与讨论的主要声音：@simonlast（Notion）、@ivanhzhao（Notion CEO）、@NotionHQ、@dhh（37signals）、@gdb（OpenAI）、@badlogicgames（独立开发者，经 @jeremyphoward 转发）
  主流观点：六个月前关于在大型代码库跑 Coding Agent 的方法多数已被新模型/新 harness 推翻；新一轮拐点出现在 GPT-5.5 vs Claude Opus 4.7 / Mythos 之间，互有胜负且强依赖具体任务
  主要分歧：badlogicgames、dhh 认为模型 RL 数据耗尽后已接近 S 曲线顶部，benchmark 进步与真实工作流脱节；OpenAI 阵营（gdb）强调 GPT-5.5 在复杂 Agent 任务上"大幅赶上"
  信号强度：强
  判断依据：Simon Last 的线程被 Notion 官号、Notion CEO、Garry Tan 同时转发（bookmarks 累计 1 万 +），DHH/Greg Brockman 各自独立确认；不是单点观点，而是来自多个独立机构的共振

- World Models 重新进入主流议程

  参与讨论的主要声音：@demishassabis（DeepMind）、@GaryMarcus、@ylecun、@SuryaGanguli、@rohanpaul_ai
  主流观点：纯语言模型对物理与因果的覆盖见顶，下一阶段共识在"通过经验/交互学习世界模型"，而不是用更多 token 喂同一个语言先验
  主要分歧：DeepMind 路径偏 sensorimotor + simulation；Gary Marcus 强调"神经-符号 + 显式表征"；LeCun 把 World Models 放进"物理-神经科学-AI 大一统"框架（Daedalus 新文）
  信号强度：中
  判断依据：Demis 在 DeepMind 官方播客明确将 World Models 称作"最长情怀"，Gary Marcus、LeCun 同窗口期两份独立长文/转发跟进，不再是任一方单独喊话

---

## 4. 值得关注的洞察 & 观点

- @scaling01（独立基准测评作者，LisanBench 维护者）：

  「SWE-bench Pro：Mythos 77.8% / GPT-5.5 58.6%；ExploitBench：Mythos 18 ACE / GPT-5.5 0 ACE；UK AISI 'The Last Ones' cyber range：Mythos 6/10 / GPT-5.5 3/10。」
  为什么值得关注：是窗口内对外公开的最系统化 Mythos vs GPT-5.5 横评；ExploitBench 18-vs-0 的差距，解释了为何 Anthropic 不全量开放 Mythos——它既是性能差，也是攻防对称性差

- @dhh（37signals CTO，Ruby on Rails 作者）：

  「对复杂 Agent 任务，GPT-5.5 相比 5.2 进步惊人；从 Opus 4.7 后退到 5.5 已不再是大幅倒退；OpenAI 出现强势回归。」
  为什么值得关注：DHH 是少数同时高强度使用 Claude Code 与 Codex 的高知名度独立判断者；Greg Brockman 直接引用其原文，是看本周 OpenAI/Anthropic 编码模型差距重新拉近的最有力第三方证词

- @ylecun（图灵奖得主，前 Meta 首席 AI 科学家）：

  「AI 是否需要'非常规'政府干预？基于尚未发生的伤害施加责任、绕过常规立法、对非直接责任方加压——这些都偏离了正常技术治理。Resilience 优于 Nonproliferation，因为后者只能买几个月时间。」
  为什么值得关注：与 Arvind Narayanan/Sayash Kapoor 合著的《AI as Normal Technology》系列新文，是当前监管立法最重要的反主流学术声音之一；时点正卡在美方收紧人才政策、Anthropic 用 Glasswing 提"准入门槛"的关口

- @GaryMarcus（NYU 名誉教授，长期 GenAI 怀疑论者）：

  「OpenAI 总融资 1900 亿美元 / 已承诺支出 6000 亿美元 / 累计利润 0 美元——bezzle 已经长到国会能看见。」
  为什么值得关注：上述数字均来自其自整理口径（[未经验证]），但在 Michael Burry 公开警告 Nvidia 需求集中度后，"AI 资本回报缺口"开始成为可重复传播的叙事锚，不再是 Gary 一人题目

- @AnthropicAI alignment lead @EthanJPerez：

  「Glasswing 启动至今，我们和合作方在关键软件中发现了 >10,000 条高危/严重漏洞。」
  为什么值得关注：来自 Anthropic alignment 负责人的当事方口径，配合 Anthropic 7 月将公布完整摘要的预承诺，是窗口内最具确定性的"前沿模型实际产能"数据点

---

## 5. 实用资源 & 教程

- DeepSeek Sparse Attention from-scratch 实现

  类型：开源项目 / 教程
  用途：在 GPT 风格小模型上跑通 DSA，理解稀疏注意力对 KV cache 的影响
  链接：https://github.com/rasbt/LLMs-from-scratch/tree/main/ch04/09_dsa
  上手难度：中

- Simon Last：在大型代码库运行 Coding Agent 的最新经验线程

  类型：教程 / 经验文
  用途：复盘半年内 Notion 在生产仓库跑 Coding Agent 的方法变化
  链接：https://x.com/ivanhzhao/status/2058202867706585578
  上手难度：低

- "Do AI Risks Require Extraordinary Government Intervention?"（Narayanan & Kapoor）

  类型：长文 / 政策论文
  用途：理解 nonproliferation vs resilience 这条治理路径之争
  链接：https://knightcolumbia.org/blog/do-ai-risks-require-extraordinary-government-intervention
  上手难度：中

- "Toward a science of intelligence: unifying physics, neuroscience and AI"（Yann LeCun）

  类型：论文（Daedalus 期刊 AI+Science 特刊）
  用途：把 World Models 话题嵌入物理/神经科学统一框架
  链接：https://www.amacad.org/publication/daedalus/toward-science-of-intelligence-unifying-physics-neuroscience-ai
  上手难度：高

- Google AI Agents "构建操作系统 $900" 事实核查（Arvind Narayanan / normaltech.ai）

  类型：长文分析
  用途：核查 Google 关于 Agent 自主构建 OS 的宣传与实际 prompt/token 成本
  链接：https://www.normaltech.ai/p/did-googles-ai-agents-really-build
  上手难度：低

---

## 一句话总结

今天最值得关注的不是哪个模型又涨了几分，而是 Anthropic 用 Glasswing 把"前沿模型仅授权给十余家国家关键基础设施企业"的封闭防御范式正式跑出 1 万 + 漏洞产能；同时美国一纸绿卡新规把 AI 人才链上的"现签现转"路径堵死，开源、出海、国内挖人的窗口同步打开。

## 今日行动建议

今天（30 分钟内）：
基于 Anthropic Project Glasswing 一个月发现逾 1 万条高危/严重漏洞——把团队过去 6 个月使用过的开源依赖列出 Top 20，对照 https://www.vulncheck.com/blog/anthropic-glasswing-cves 检查是否已涉及 Glasswing 归属 CVE，并标注修复状态

本周内：
基于 Trump 行政令要求绿卡申请人离境申请——做一页两栏备忘录：左栏列出公司当前持 F-1/H-1B/L-1 的 AI 关键岗位，右栏给出（a）转岗加拿大/英国/新加坡/日本子公司、（b）冻结境内 AOS、（c）按新规走境外面签三档应对预案，交付给法务与高管

月内验证：
基于 Google Antigravity 2.0 紧急修复 IDE 体验——跟踪 Antigravity vs Cursor vs Claude Code 三家在 r/cursor、Hacker News、GitHub trending 上的开发者讨论占比与 weekly active install 变化；若 Antigravity 占比在 4 周内涨过 15%，须纳入团队 IDE 评估短名单

---

## 传播力素材

- 「A 6-person team is building task-specific AI models that are 4-8x faster than anything from OpenAI or Anthropic. 500K downloads on HuggingFace. No hype. Just better engineering winning on the merits. This is what 'make something people want' looks like in the model layer.」 — @ClementDelangue · 👍1411 👁93718 · engagement_rate 1.72%
  改写方向：适合公众号 / 小红书的"6 人小团队跑赢千亿美金巨头"叙事；改成中文标题可锚"4–8 倍速度、50 万次下载"两个具体数字
  点评：Clem 用 ZeroEntropy 印证 HuggingFace 一贯的"专用小模型胜过通用大模型"叙事，正契合当下大厂资本回报承压的情绪。盲区是没说 ZeroEntropy 的 reranker 在哪类任务上显著弱于通用模型；只看这句话容易得出"通用模型已不重要"的错误结论

- 「1/ Some things I've learned recently running coding agents on large-scale projects. Most of this contradicts advice from 6 months ago!」 — @simonlast（经 @ivanhzhao、@NotionHQ 转发）· 👍2405 👁418477 · engagement_rate 1.25%
  改写方向：适合开发者社区（V2EX/掘金/Twitter 中文圈）"半年前的 Agent 经验已过期"系列拆解
  点评：标题钩子精准命中开发者焦虑——"我刚学会的东西又不能用了"。盲区是该结论高度依赖 Notion 这种大型 TypeScript 单仓的工作流，搬到 Java、Go、嵌入式或科研代码场景需重新校准

- 「i need someone at @OpenAI and @AnthropicAI to teach the models that while prototyping, backwards compatibility is just a bad idea.」 — @leostera（经 @jeremyphoward 转发）· 👍1046 👁45438 · engagement_rate 0.15%（注：likes 已显著超过 300 阈值）
  改写方向：适合给资深工程师写的"Coding Agent 的隐性偏见"短文
  点评：观点点出了 RLHF 训练数据偏向生产代码风格、导致原型阶段过度保守这一具体技术副作用，是只有真做过 prompt-to-prod 完整链路的人才说得出的判断。盲区是把"原型 vs 生产"的边界完全留给开发者，未给可执行的提示词模板

- 「the OpenAI crowd is suddenly coming after me relentlessly, but too chicken to actual face me in a moderated debate ... OpenAI is running out of money fast, and they know it. if the IPO were to fall flat, they could well be toast.」 — @GaryMarcus · 👍478 👁32870 · engagement_rate 0.14%（注：likes 超阈值）
  改写方向：适合作为"AI 资本叙事是否见顶"系列的对照声音引入，配合 Michael Burry Nvidia 警告做组合叙事
  点评：Gary 的财务断言基于公开二手数据，存疑；但他抓住了"IPO 临门一脚 + 行业怀疑论同时抬头"的叙事节拍。盲区是把所有反对声音归因于"OpenAI 派系打压"，掩盖了独立批评的差异——只看这条容易把行业辩论简化成对立站队

---

## 信号 / 噪音比

进入第 1 节的有效新闻 3 条，进入第 2-5 节的有效信号 16 条，剩余约 65% 为低价值或噪音（SpaceX Starship V3 首飞占据 by_views 与 by_bookmarks 主体；Gary Marcus 单日 40 条推文里有近 30 条为 OpenAI 系列贴身骂战或转发支持评论）。今日整体信号密度：正常

**本期信源**：@AnthropicAI @EthanJPerez @demishassabis @GoogleDeepMind @ylecun @JeffDean @AndrewYNg @ClementDelangue @garrytan @ivanhzhao @NotionHQ @simonlast @gdb @JustinBleuel @GaryMarcus @scaling01 @jeremyphoward @leostera @badlogicgames @BlinkDL_AI @StabilityAI @rasbt @MIT_CSAIL @hardmaru @SakanaAILabs @arthurmensch @huggingface @fchollet @hugo_larochelle @aidangomez @nvidia @tobi @pwang @mntruell @unixpickle @kchonyc（共 36 位）
