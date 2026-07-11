# AI 一人公司日报 | 2026-07-12

数据窗口：06:00 — 06:00（北京时间，2026-07-11 至 2026-07-12）
深度挖掘：3 条

---

## 今日头条

**AI Agent 成本战开打：同类任务从 $12 降到 $2.49，经济窗口正在打开**

Grok 4.5 于 7 月 8 日发布，专为多步骤 agentic 任务训练，API 价格 $2/M tokens（约 ¥13.6/M），@gregisenberg 估算某类工作流每任务成本约 $2.49，而同类任务在 Claude Fable 里约 $12（均据推文原文，为作者估算值 [未经独立验证]）。与此同时，OpenAI 推出 GPT 5.6 三档模型并发布官方优化指南，@itsolelehmann 将其中 7 条关键技巧整理成推文，engagement_rate 高达 1.65%——是当日数据中位数的 8-11 倍。两个信号方向一致：用 AI 跑 autonomous agent 的实际成本正在进入可负担区间，一人公司做 AI-driven 产品的起步门槛在加速下降。

---

## 今日金矿

### 金矿 1：GPT 5.6 实战优化手册 — 7 条立刻可用的技巧

来源：@itsolelehmann · 2026-07-11 22:37 · 👍169 👁19,047 🔖315
engagement_rate：1.65%（同期中位数约 0.15%-0.20%，约为中位数的 8-11 倍，属极高阈值）
内容类型：方法论框架 / 操作指南

**国内可用性**
- GPT 5.6 API：需要工具访问
- 原始推文和 OpenAI 帮助文档：**直接访问**（help.openai.com）

**完整步骤（逐条列出）**

1. **删除重复指令**：OpenAI 实验数据表明，每条指令只写一次，删除重复后平均提分 10-15%，token 消耗可减少高达 66%（经 OpenAI 帮助文档验证）。给旧模型写的大段规则列表在 GPT 5.6 上不仅没用，还会拖累表现、增加成本。

2. **匹配算力档位**：两个独立维度——①选模型规格：Sol（最复杂任务）/ Terra（日常业务，性能接近 GPT-5.5，价格低 50%）/ Luna（廉价快任务）；②调思维力度：6 个等级。OpenAI 官方建议从上一个模型的 level 开始，试着降一级测试。

3. **启用 Pro 模式**：reasoning="pro" 会让模型在输出答案前额外计算，适合质量优先于速度和成本的场景，可叠加任意思维力度。

4. **检查旧有简洁指令**：GPT 5.6 默认比 5.5 更简短，原来加的"要简洁"类指令现在可能截断有用信息。调整方向：改为具体说明保留哪些信息、删掉哪些细节，而非一刀切"keep it brief"。

5. **用行为描述替代抽象语气词**："友好"、"共情"太抽象。改成"开头点明客户问题、用编号步骤给解决方案、省略道歉段落"这类具体行为指令，每次输出的语气才能稳定一致。

6. **用代码调用工具（Programmatic Tool Calling）**：GPT 5.6 新特性。处理大量数据时不再把 900 行数据全喂给模型逐行读，而是让模型写一小段脚本来处理，再只读结果——速度更快，成本是原来的几分之一。（仅对已有工具调用接口的开发者适用）

7. **输出长度独立可调**：verbosity 设置（低/中/高）可全局设定一次，不用在每个 prompt 里重复加"请简短回答"。

**前置条件**：已有 GPT 5.6 API 访问权限（OpenAI 付费套餐）。

**原始链接**：https://x.com/itsolelehmann/status/2075952515762257969

---

**复制路径**

档位 B（独立开发者）
- 今天 30 分钟：打开最常用的 system prompt，逐行扫描有无重复指令，压缩后记录 token 数变化，预期节省 30-66%
- 本周：测试 Programmatic Tool Calling——如果有需要处理表格/数据的 Agent 工作流，这个特性单次 API 成本可能降幅 80%+
- 模型选型：用 Terra 替代目前跑 Sol 的日常任务，价格降 50%，能力差距在大多数业务场景可忽略（经 CodeRabbit benchmark 报告验证）

档位 C（工具集成者）
- 用 verbosity 全局设置取代工作流里每个节点上的"请简洁"提示词，减少冗余 token
- 重写 Agent 输出格式规范：把"友好""专业"改成具体行为描述，提升 Agent 输出一致性

---

**深度综述**

这条信号的稀缺性在于来源可信度：不是猜测，而是 Ole Lehmann 直接从 OpenAI 官方发布的优化文档提炼，关键数据（重复指令扫描提分 10-15%、token 减少 66%）有 OpenAI Help Center 背书，不是营销说辞。

**商业模式意义**：对月均 100 万次 API 调用的产品，按 GPT 5.6 Terra 定价（$2.50/M tokens，约 ¥17/M），单靠删重复指令节省 30% token，月节省成本约 ¥5,000+。对一人公司而言，这类边际节约通常直接转化为净利润。

**趋势定位**：GPT 5.6 发布于 7 月 9 日，3 天前。绝大多数在用 GPT 5.5 的产品还没有针对 5.6 做任何迁移优化。这是一个时间窗口：率先完成提示词迁移的开发者，在未来 2-3 周有短暂的性能和成本优势。

**意外与反直觉**：最反直觉的是第 4 条——GPT 5.6 原生就更简洁，原来写的"要简洁"指令在新模型上反而可能截断有用信息。这说明提示词迁移不是复制粘贴，而是需要在新模型上逐条重测限制指令。如果机械迁移，可能在不知情的情况下让产品质量下降。

**风险与局限**：第 6 条 Programmatic Tool Calling 是最有价值但门槛最高的特性，需要工具调用接口支持让模型写脚本——简单 RAG 应用或单轮对话场景不适用。另外，GPT 5.6 API 在中国大陆需要代理，这是所有相关优化的前提条件。

---

### 金矿 2：Grok 4.5 + Hermes = 每任务 $2.49 的 AI 联合创始人方案

来源：@gregisenberg · 2026-07-11 06:29 · 👍1,353 👁145,383 🔖1,283
engagement_rate：0.88%（同期中位数约 0.15%-0.20%，属高区间）
内容类型：视频 + 工具组合框架（@startupideaspod 完整单集摘要）

**核心数据（来源标注）**
- Grok 4.5 发布日期：2026-07-08（据 MarkTechPost 报道验证）
- API 定价：$2/M input tokens（约 ¥13.6/M），$10/M output（约 ¥67.8/M）——据 MyClaw 定价页验证（$1≈¥6.78，据 2026-07-10 汇率数据）
- 每任务成本 $2.49 vs 约 $12（据推文原文，作者对特定工作流的估算）[未经独立验证]
- 比 Claude Opus 4.8 便宜 60% 以上（据推文原文）[未经独立验证]
- 跑速：80 tokens/秒（据 MarkTechPost 报道）

**工具卡片**

**Grok 4.5** | xAI 新一代 agentic 模型
- 发布：2026-07-08
- 国内可用：需要工具（xAI API 需代理访问）
- 特点：专为多步骤软件工程和技术 Agent 任务训练，SWE Bench Pro 上比 Opus 4.8 max 少用 4.2 倍 output tokens（据 MarkTechPost）
- 定价：$2/M input（约¥13.6/M）/ $10/M output（约¥67.8/M）

**Hermes Agent** | 开源 AI Agent 框架
- 国内可用：开源，可自托管
- 功能：给 Agent 配独立邮箱、电话、借记卡、工具访问，实现 autonomous 执行

**OpenClaw** | 开源 Agent 编排平台
- 国内可用：开源，可自托管，VPS 自托管成本 $5-20/月（约¥34-136/月）
- 平台本身免费，带自己的 LLM API key 使用

**国内可用性整体评估**：需要分层——xAI API 需要代理；Hermes/OpenClaw 开源项目可直接访问 GitHub 部署；支付问题（Stripe 国内限制）需要独立解决。

---

**复制路径**

档位 B（独立开发者）
- 今天：如果已有 xAI API 访问，跑同一批 Agent 任务对比 Grok 4.5 vs 现用模型的质量和成本
- 本周：参照 gregisenberg 的组合框架，在 Hermes Agent 或 OpenClaw 上搭建一个具体的 autonomous 工作流（如邮件处理、数据采集、竞品监控）
- 注意：先在小任务上验证质量达标再切换，不要直接用成本估算做决策

档位 C（工具集成者）
- 用 n8n/Make 调用 Grok 4.5 API，替换现有工作流里的高成本模型节点，降低 agent 工作流的整体 API 成本
- 如果做客户交付的自动化产品，成本节省可以转化为更高毛利率或更有竞争力的报价

---

**深度综述**

这条信号的价值有两层：一层是 Grok 4.5 本身的性价比（技术事实），另一层是 gregisenberg 给出的"AI 联合创始人"组合框架（操作范式）。

**商业模式拆解**：框架逻辑很清晰——低成本模型（Grok 4.5）+ 工具赋权（Hermes/OpenClaw）+ 独立身份（邮箱、电话、借记卡）= 一个能 autonomous 处理重复业务任务的 Agent。如果按推文估算数字，月跑 1000 次 Agent 任务的一人公司，在 Grok 4.5 上成本约 $2,490（约¥17,000），而在 Claude Fable 上约 $12,000（约¥81,400）[以上均为作者估算数字，实际成本取决于具体任务 token 消耗，未经独立验证]。

**创始人背景**：Greg Isenberg（@gregisenberg）是 Late Checkout 的 CEO，@startupideaspod 播客主持人，68 万粉丝，长期深度追踪 AI 工具。他对 Grok 的公开态度转变（"I slept on Grok. Not sleeping on it anymore."）来自独立实测而非 xAI 的营销，信号真实度较高。

**趋势定位**：这条信号处于 AI Agent 工具链"中期验证"阶段——开源框架（Hermes/OpenClaw）已存在，新模型（Grok 4.5）刚发布，但整合实践刚在浮现。过去 2 周类似的"低成本 agent"讨论持续增多，说明市场对 agent 成本的敏感度正在明显上升。现在进入这个方向，不是最早期，但窗口仍然开着。

**风险与局限**：最需要警惕的是"便宜 ≠ 够用"的陷阱。Grok 4.5 针对编码和技术任务强化训练，对于需要高精度创意输出或复杂推理的任务，切换前必须实测对比。中国独立开发者还需要额外解决：xAI API 代理访问、Stripe 支付限制（Hermes/OpenClaw 虽然开源免费，但 xAI API 本身是付费的）。Hermes Agent 的学习曲线和 Agent 任务的监控/回滚机制也需要时间投入。

**竞争格局**：这个赛道目前进入门槛主要是"会搭"，真正的护城河在于特定行业的任务熟悉度和 Agent 稳定性打磨，而不是工具选型本身。

---

### 金矿 3：Kill AI Slop — 识别和消灭 AI 产品通病的开源工具包

来源：@yetone（经 @oran_ge 转推）· 2026-07-11 06:03 · 👍460 👁105,968 🔖458
engagement_rate：0.43%（同期中位数约 0.15%-0.20%，属高区间）
内容类型：工具发布 + GitHub Repo

**工具卡片**

**Kill AI Slop** | AI 产品通病的识别与修复工具包
- 上线时间：2026-07 最新发布
- 国内可用：**直接访问**（killaislop.com / GitHub 均可直接访问）
- GitHub：github.com/yetone/kill-ai-slop（经 web_search 验证，repo 存在；精确 star 数未能从搜索结果获取）
- 定价：完全免费，开源

**核心功能（聚焦对一人公司的价值）**
1. **网站 killaislop.com**：23 条 AI slop 特征图鉴，支持中/英/日/韩四语言，每条有交互式 before/after 示例，可当成产品审计清单
2. **Agent Skill（kill-ai-slop skill）**：扫描 Web 项目代码，识别 AI slop 信号，解释为什么读起来像机器生成，提出或直接应用修复

**10 分钟上手**
1. 访问 killaislop.com，过一遍 23 条特征图鉴，建立"AI slop 感知力"
2. 克隆 repo：`git clone https://github.com/yetone/kill-ai-slop`
3. 参照 README 安装 skill 到 Claude Code 或其他支持 Agent Skill 的环境
4. 在项目目录运行 skill，获取扫描报告
5. 针对报告逐条修复，或让 skill 直接应用修复

**踩坑预警**
- yetone 在推文中坦言，最难的是让工具的文案本身不含 AI slop——视觉交互类通病识别比较准确，文案/营销类内容的判断更主观，可能有误报
- 开源工具没有 SaaS 式的维护保证，使用前建议查看 repo 最近 commit 活跃度

**原始链接**：https://x.com/oran_ge/status/2075702505082884103

---

**复制路径**

档位 B（独立开发者）
- 今天 30 分钟：用 killaislop.com 的 23 条清单自测自己的产品主页和核心 UI，看踩了多少条
- 本周：集成 kill-ai-slop skill 到 CI 流程或代码审查阶段，让每次提交自动检测

档位 C（工具集成者）
- 把 skill 集成进 vibe coding 项目模板，新建项目时自动扫描——尤其适合帮客户交付的项目，可以显著提升交付质量

档位 D（服务变现者）
- "AI 产品去 slop 化审计"是一个新兴需求。把 killaislop.com 的 23 条清单转化成审计 checklist，当成可交付物卖给已上线的 AI 产品
- 可以做的：UI/文案专业化改造，帮产品减少"机器感"、提升用户信任

---

**深度综述**

这个项目有一个耐人寻味的自我指涉：yetone 在推文里坦承，"这个产品本身极有可能成为 AI slop 的一部分"，但他选择用大量 human in the loop（亲自截图每个产品并详细描述）来对抗这个风险，结果这成了他所有产品里人工投入最多的一个。这个过程揭示了 AI slop 问题的本质——不是工具的问题，而是人工质量控制缺位的问题。工具生成 80%，剩下 20% 的判断力和审美决定了最终产品是否有辨识度。

**创始人背景**：yetone 是 @avante.nvim 的作者，avante.nvim 是 Neovim 的 AI 编程插件，在开源社区有相当规模的认可度。这不是一个做营销内容的人随手搭的网站，而是有技术深度的开发者在解决自己感受到的真实问题。信源可信度高。

**商业模式与商业化潜力**：工具本身免费开源，作者目前没有直接变现意图。但它开创了一个可以有人来填补的服务需求缺口：已有企业愿意付费让产品看起来更"人性化"，减少"AI 味"。killaislop.com 的 23 条标准可以直接包装成收费的"AI 产品品质评估报告"，适合档位 D 的服务变现者。

**趋势定位**：AI slop 话题在 2026 年已经从"小众抱怨"进入"有解决方案"阶段——不止是一篇文章，而是一个可以运行的工具。目前这个赛道基本空白，killaislop.com 是可见的最完整的解决方案之一，竞争窗口还开着。

**意外与反直觉**：这个工具最有价值的受众反而是大量产出 AI 内容的 vibe coder，因为他们最容易堆砌 AI 默认输出，却没有足够的审美判断力去识别和修复这些通病。工具把"识别 AI 通病"这个能力外包给了 AI 本身——是一种有趣的元层面对抗。

**风险与局限**：文案层面的 AI slop 识别比 UI/代码层面更主观，工具在这里的精准度值得存疑。另外，开源工具的长期维护需要关注——如果 repo 活跃度下降，skill 与最新 Agent 环境的兼容性可能会有问题。

---

## 快讯区

**收入信号**
- Marc Lou（@marclou）发布视频"my $1M/year startup office tour" — 据其 2025 年度复盘，全年收入 $1,032,000（经 newsletter.marclou.com 及多个报道交叉验证）；2026 年 1-2 月月收入分别为 $94,799 和 $81,683（据 IndieAI 2026年2月数据）。他一向无实体办公室，视频可能为反差标题。— @marclou · 2026-07-11 20:49

**产品发布**
- **Knockoff.shopping v0.5.0 上线**（@Shpigford / Josh Pigford）— 浏览器插件（Chrome + Firefox），过滤 Amazon 山寨/低质品牌，白名单 5,000+ 真实品牌，本地运行，无账号、无追踪、无分析。v0.5.0 新增按评分和评价数过滤。上线于 2026-07-07，已有 Digital Trends / Boing Boing / Fast Company 等媒体报道。Safari 版等待 Apple 审核中。国内可用：**直接访问** knockoff.shopping。— @Shpigford · 4 条推文 · 2026-07-11

**工具更新**
- **Orca ADE**（Agent Development Environment）— 开源，MIT 许可证，支持在隔离 worktree 中并行运行 25+ 款代码 Agent（Claude Code / Codex / Gemini / Cursor CLI 等）。16,300 GitHub stars（据 GitHub 直接验证），YC 背书，July 2026 最新版本 v1.4.135，活跃开发（805 个发布版本）。免费，桌面 + 移动端。国内可用：**直接访问** GitHub / onorca.dev。— @indie_maker_fox 推荐 · 2026-07-11
- **SuperX Chrome 插件改版即将发布**（@tibo_maker，Tweet Hunter/Taplio 创始人，已以 $8M 出售两款产品）— 支持在 X 内直接排帖、研究账号、获取病毒灵感、与 Ask SuperX 对话。国内可用：需要工具。— 2026-07-11

**值得关注的观点**（仅收录有可验证背景的实践者判断）
- @dagorenouf（15 年编程 / 7 年 UX / 7 年营销 / 5 年 Copywriting 积累）："I have zero interest in building software anymore. AI makes it too easy to copy your ideas. The next thing I build will be hardware." — 485 likes，164 replies（大量反驳和讨论），engagement_rate 0.19%。这是当日关于"AI时代软件护城河"讨论密度最高的推文之一，值得持续追踪。— 2026-07-11 22:35
- @SimonHoiberg（多款 Bootstrap SaaS 组合创始人）："Never again: freemium、powered by 链接、等影响力飞轮。付费用户，从第 1 天起。其他都是噪音。" — 来自多产品组合实践者的总结，适合正在考虑定价策略的阶段。— 2026-07-11 22:30

**教训与反思**
- @marclou 分享了他和妻子盲目跟随 @bryan_johnson 低卡路里饮食方案导致妻子荷尔蒙水平严重下降的经历，历时近 2 年才找到根本原因。核心教训：不要把为特定年龄/性别设计的方案直接套用到不同情况的人身上。和产品开发的逻辑是一样的——MVP 数据不能不加筛选地直接指导不同用户群的产品决策。— @marclou · 2026-07-12 02:50

**传播力素材**（适合自媒体改写的高互动观点）

- "Underrated life advice: Make yourself easy to root for. Be kind. Be reliable. Celebrate other people's wins. Work hard without complaining. Carry good energy into rooms. You'll be shocked by how many doors open for you by making life better for others." — @blakeaburge · 👍12,708 👁222,196 · engagement_rate 1.15%
  改写方向：适合小红书图文——把"让自己值得被支持"这个概念落地，列出 6-8 个具体可执行行为（比如主动帮圈子里的人转发作品、在别人成功时第一批出现、言出必行），配上"这样做 90 天之后"的场景对比，比空泛励志更有操作性。
  点评："make yourself easy to root for"这个表达有一定新鲜感，击中了想建立个人品牌的人的心理需求——不是"你要多优秀"而是"你要让别人乐于支持你"，角度更实用。局限在于缺乏如何判断"自己是否已经值得被支持"的反馈机制，改写时可以补上这一维度。

- "I have zero interest in building software anymore. AI makes it too easy to copy your ideas. The next thing I build will be hardware." — @dagorenouf · 👍485 👁37,194 · engagement_rate 0.19%
  改写方向：适合公众号/视频号——"当 AI 让一切软件都可以被 24 小时内复制，一人公司的护城河在哪里？"切入软件 vs 硬件 vs 服务化的路径选择讨论，配上真实案例。
  点评：价值不在于结论正确与否（评论区大量反驳，很多人认为硬件门槛更高对一人公司不现实），而在于触发了"AI 时代软件护城河消失"的真实焦虑。这个焦虑是真实的，但"转向硬件"作为解决方案对大多数独立开发者并不可复制。改写时最好呈现这个张力，而不是把他的判断直接包装成建议。

- "C students run companies. A students work for them. Dropouts run the rest of the world." — @Codie_Sanchez · 👍1,580 👁71,757 · engagement_rate 0.30%
  改写方向：适合视频号——做对比内容，把这个观点拆成具体数据（实际上有研究表明顶尖创业者学业成绩分布非常分散），注意配平衡视角，避免纯鸡汤。
  点评：典型的"半真实"金句，大体方向有支持性数据，但表述夸张，容易被用来为"不学习"辩护。改写时加一个"但这不意味着知识不重要，而是说明执行力和销售力比成绩更关键"的转折，内容质量会高很多。

---

## 延伸资源库

### 播客 / 视频 / 访谈

- **World's Greatest Business Thinkers Podcast EP.53** — "The Unsexy Path to Building Wealth"
  - 嘉宾：Nick Huber（@sweatystartup）— 实体存储、房地产、成本分离等多个服务型公司创始人
  - 核心话题：被忽视的本地服务型生意机会、销售作为创业核心技能、被动收入神话、地理优势作为护城河
  - 收听链接：Apple Podcasts / Spotify / YouTube（均在推文原文中）
  - 核心价值：适合考虑服务型一人公司或实体资产布局方向的创业者

- **@startupideaspod** — Greg Isenberg + Nick Vasiles 关于 Grok 4.5 + Hermes 完整单集（上文金矿 2 来源），具体单集链接未在推文中单独提供

### 图书 / 课程
本期无图书/课程深度信号。

### 链接汇总（已验证）

**工具类**
- Orca ADE：https://www.onorca.dev | GitHub：https://github.com/stablyai/orca（16.3K stars，MIT 开源）
- Kill AI Slop：https://killaislop.com | GitHub：https://github.com/yetone/kill-ai-slop（开源免费）
- Knockoff.shopping：http://knockoff.shopping（浏览器插件）

**参考文档**
- GPT 5.6 官方说明（OpenAI Help Center）：help.openai.com/en/articles/20001325-a-preview-of-gpt-56-sol-terra-and-luna
- GPT 5.6 发布公告：openai.com/index/previewing-gpt-5-6-sol/
- Grok 4.5 发布报道（MarkTechPost，2026-07-08）：marktechpost.com

---

## 行动建议（按档位分组，不超过 4 条）

档位 A（内容创作者）
- 今天：把 killaislop.com 的 23 条清单过一遍，检查自己公众号/小红书的内容是否也踩了"AI 味"的坑（段落堆砌、格式模板化、无个人观点等）

档位 B（独立开发者）
- 今天 30 分钟：检查现有 system prompt，删除重复指令，估算 token 节省空间
- 本周：跑 Grok 4.5 vs 现用模型的对比测试，实测你自己的任务场景，不要靠别人的成本估算做决策

档位 C（工具集成者）
- 本周：在一个实际项目上集成 kill-ai-slop skill，用来做输出质量的自动检测

档位 D（服务变现者）
- 今天：把 killaislop.com 的 23 条清单整理成一份可交付的"AI 产品品质审计 Checklist"，这是一个新兴但真实的服务需求

---

## 避坑指南

- **Grok 4.5 成本数字不要直接用**：gregisenberg 的"$2.49/任务 vs $12/任务"是基于他特定工作流的估算，实际成本高度依赖任务 token 消耗量。在切换前必须在自己的实际工作流上跑对比测试，不能把他的数字当成普遍基准。

- **GPT 5.6 提示词迁移需要逐条重测**：旧 system prompt 不能机械迁移到 GPT 5.6。特别注意：原来的"要简洁"类限制指令可能在 5.6 上产生反效果——新模型默认更短，加了这类指令反而会截断有用信息。每条限制指令都需要在新模型上独立验证。

---

## 本期情报评估

**信息密度**：正常
今日 timeline 被欧洲杯（英格兰 vs 挪威，当日深夜比赛）和 EU Chat Control 政治事件分流了相当比例的注意力，OPC 相关信号处于正常水平，有 3 条值得深挖的 B 级信号。

**趋势信号**：
AI agent 的经济模型正在重构。模型价格战（Grok 4.5 vs Claude 系列 vs GPT 5.6 Terra）和工具链成熟（Orca ADE、Hermes/OpenClaw）同步推进，一人公司跑 autonomous agent 的实际成本正在向可负担区间移动。本期两条金矿从"怎么用"和"用哪个更便宜"两个角度切入同一趋势，可以同时执行。

**横向对比**：
金矿 1（GPT 5.6 优化指南）和金矿 2（Grok 4.5 方案）不互斥——前者是"让已有模型更高效"，后者是"换更便宜的模型"。两者都在降低 AI 工具的实际成本，路径不同，可以根据当前使用的模型生态各取所需。

**当日强信号数 vs 噪音比**：
3 条 B 级强信号 / 约 200 条噪音（体育娱乐约占 30%、通用励志约 20%、政治/社会事件约 15%、其他 OPC 弱相关约 35%）

**本期信源**：@itsolelehmann @gregisenberg @yetone @oran_ge @indie_maker_fox @Shpigford @marclou @dagorenouf @SimonHoiberg @tibo_maker @sweatystartup @blakeaburge @Codie_Sanchez（共 13 位）
