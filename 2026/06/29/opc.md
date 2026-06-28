# AI 一人公司日报 | 2026-06-29

数据窗口：06:00 — 06:00（北京时间，过去 24 小时）
深度挖掘：2 条

---

## 今日头条

@levelsio（月收入 $242K，据其自述）公开了他用 Claude Code 在生产 VPS 上直接开发近一年的完整工作流——不再需要本地环境，不用 git push，代码改动 3 秒内在生产环境生效，一年仅出了 2 次故障、每次宕机不超过 10 秒。他用的底层技术栈是 vanilla PHP + vanilla JS：没有构建步骤，没有重启，改完即生效。这不只是一个操作偏好，而是一个已被年收入约 $290 万的产品矩阵验证过的一人公司工作流范式——"本地→staging→生产"三段式正在被"VPS 上直接改"这条路压缩掉。

---

## 今日金矿

### 金矿 1：@levelsio 的生产 VPS + Claude Code 工作流

来源：@levelsio · 2026-06-28（经 @akokoi1 引用）· 原推 👍4,649  
engagement_rate：原推未收录于数据集，通过引用推文挖掘；引用推文（@akokoi1）engagement_rate 0.20%

**核心数据（据推文原文）**
- 月收入：$100K（PhotoAI）+ $44K（远程工作追踪）+ $39K（游戏）+ $35K（NomadList）+ $14K（泳装+X）+ $10K（地图工具）+ $0（新产品），合计约 $242K/月（约 ¥1,742K/月，参考汇率 1 USD ≈ 7.2 CNY [估算，未经今日实时验证]）
- 工作流演进：本地→git push→自动部署（~1 分钟）→ 直接推到 VPS 生产（~3 秒）→ Claude Code 在 VPS 直接实时编辑生产代码（即时）
- 故障率：近 12 个月仅 2 次问题，每次仅导致网站宕机约 10 秒
- 来源标注：据推文原文

**工作流详解**

levelsio 用 Claude Code 在生产 VPS 上直接编码的具体逻辑：
1. SSH 登入 VPS，在服务器上运行 Claude Code
2. Claude Code 直接修改生产服务器上的代码文件
3. 因为用 vanilla PHP + vanilla JS，没有构建步骤，改动立即生效
4. 用 `/goal` 命令让 Claude Code 整夜持续运行任务
5. 可在手机、平板任意切换继续工作，计算全在 VPS 上

他补充说：曾买新 MacBook Pro 后懒得搭本地 Nginx 环境，索性直接推生产，结果"一切正常"。这种"懒出来的最优解"是这条工作流诞生的真实背景。

**国内可访问性**：Claude Code 需要代理（claude.ai 需要工具访问）；VPS 国内外均可选

**复制路径（真正适用的档位）**

档位 B（独立开发者）：
- 立刻可做：在有完整备份的现有 VPS 上安装 Claude Code，选一个最简单的 PHP/Python 项目试跑，感受直接在生产环境编辑的手感
- 风险控制：3-2-1 备份（3 份副本、2 种介质、1 份异地）是前提，不是可选项
- 技术约束：如果项目依赖构建步骤（React/Next.js/Vite 等），这套工作流不能直接套用；需要专门搭 staging VPS 或改造为无构建架构

档位 C（工具集成者 / vibe coder）：
- 核心收益：用 Claude Code 的 `/goal` 指令让任务跑过夜，明早检查结果——不需要懂 PHP，但需要能 SSH 进 VPS 并安装 Claude Code
- 可用 Cursor 的"远程 SSH"模式部分替代 Claude Code VPS 方案

**深度综述**

这条信号最反直觉的地方是：**月入 $242K 的产品矩阵背后是零构建步骤的 vanilla PHP。** 大多数独立开发者在追着 Next.js、Vercel、Docker 这条技术链跑，而 levelsio 的答案是越简单越好——没有构建，就没有"构建失败"这个风险点。

从工作流演进看，这不是一夜之间的决定。他先从"本地→git push→自动部署（1 分钟）"变成"直接推生产（3 秒）"，再从"推代码"变成"Claude Code 在 VPS 上直接改（即时）"。每一步都是"能不能去掉这个摩擦"的追问。最终结果是：开发环境消失了，代码和生产之间没有任何中间层。

**趋势定位**：这是"云端 AI 编码"方向的早期强验证，不是理论。@theo（Ping.gg）和 @karpathy（通过 Slack 在云端用 Claude）都在往这个方向走，但 levelsio 是目前公开说明"已在生产跑了一年"的少数高收入 solopreneur 之一。这条路径窗口期存在。

**意外之处**：12 个月仅 2 次故障、每次宕机 10 秒——这个稳定性超出大多数人预期。他的解释是 vanilla PHP 本身极稳定，Claude Code 修改时"非常谨慎"。但这是 N=1 个人经验，且他深度理解自己的代码库，Claude Code 并非对所有项目都这么稳定。

**风险与局限**：这个工作流成立的前提：1）项目足够简单，无复杂构建链；2）有完整备份；3）能接受"生产即开发环境"这个心理转变。在监管严格的行业（金融、医疗等），staging→生产的隔离是硬性要求，不能套用。此外，他的产品矩阵是他本人深度熟悉的代码库，对于新接手或复杂项目，直接编辑生产环境的风险会显著放大。

**竞争格局**：这不是"Claude Code vs Cursor"的 IDE 之争，而是"在哪里跑代码"的根本性转变。国内开发者可用 Cursor 的远程 SSH 模式+国内 VPS 部分实现类似效果，但 Claude Code 的 `/goal` 长任务能力目前没有直接替代。

---

### 金矿 2：RepoPrompt 社区版正式开源

RepoPrompt CE — 帮开发者从代码仓库精选文件、构建高质量 prompt 的上下文工程工具  
来源：@dotey · 2026-06-29 05:40 · 👍5 👁912 · engagement_rate 1.21%（极高，约为当期中位数的 6-8 倍）  
发布日期：2026-06-29  
国内可用：GitHub 直接访问；原始 RepoPrompt 平台需代理

**背景（据推文原文）**

RepoPrompt 原作者 Provencher 被 OpenAI 开发者体验负责人 Romain Huet 招募加入 OpenAI。加入前，他提出条件：先将产品免费开放，再彻底开源。社区版（CE）已上线 GitHub，同时保留老版本仓库。

社区版 GitHub：https://github.com/repoprompt/repoprompt-ce  
老版本 GitHub：https://github.com/repoprompt/repoprompt-classic  
安装：`brew install --cask repoprompt-ce`（macOS，跨平台版本开发中）

经 web_search：本期为非交互式自动生成，无法执行实时 web_search。以上信息均来自 @dotey 推文原文，标注为[据推文原文]。GitHub 仓库链接需实际访问验证最新状态。

**核心功能（聚焦对一人公司的价值）**

RepoPrompt 解决的是"上下文工程"问题——不是把整个代码库丢给 AI，而是精选真正需要的文件，避免超过 32K token 的 prompt 导致模型变笨。

社区版架构变化（据推文原文）：
- 原版：应用本身调度 agent
- 社区版：内置 MCP server 成为主控；Claude Code / Codex / OpenCode / Gemini CLI 等命令行工具变成可替换的执行层
- 实际效果：用一个推理模型做规划和任务分解，把子任务分发给不同 agent 并行执行，每个 agent 只看自己负责的那部分文件

**定价**
- 免费：社区版（CE）完全免费开源
- 旧版付费用户：如同意则自动成为认证贡献者（类似 libgdx 的贡献者白名单模式）

**10 分钟上手**
1. `brew install --cask repoprompt-ce`（macOS）
2. 打开 RepoPrompt，导入代码仓库
3. 精选相关文件子集（这是核心操作：不是全选，是精选）
4. 生成 prompt，复制到 Claude Code / Claude.ai / Codex 使用
5. 进阶：使用 MCP server 模式，让 Claude Code 直接连接 RepoPrompt 进行上下文管理

**踩坑预警**
- 目前仅 macOS，Windows/Linux 需等待
- 旧版部分"手工拼 prompt"功能已在开源版中被砍掉
- 从手工拼 prompt 迁移到 MCP server 模式有一定学习曲线

**复制路径（真正适用的档位）**

档位 B（独立开发者）：
- 立刻可做：`brew install --cask repoprompt-ce`，导入正在维护的项目，体验"精选文件→高质量 prompt"与"全塞进去"的实际差异
- 进阶：用 MCP server 模式接入 Claude Code，实现更精细的上下文控制

档位 C（工具集成者 / vibe coder）：
- 核心价值：把 RepoPrompt 的 MCP server 作为 agent workflow 的上下文层——规划模型负责理解整体，执行模型只看自己的片段，多 agent 并行跑

**深度综述**

这条信号的关键不在工具本身，而在它揭示的趋势：**"上下文工程"正在从 prompting 技巧变成独立工具类别。**

Provencher 的判断（"把整个代码库丢给 AI 效果差，需要精选"）两年前是少数人的认知，现在已经开始工具化。RepoPrompt 的产品历程——从付费小工具到作者被 OpenAI 招募、再到彻底开源——其实是 OpenAI 在做一件事：把上下文工程的最佳实践内化到自己的开发者生态里。

**趋势定位**：这是上下文工程工具从"技巧"到"产品"的早期信号，且处于早期中期之间——OpenAI 已经在收编这个方向，说明它的价值已经被验证，但工具生态还没成熟，独立工具的机会窗口仍在。

**意外之处**：RepoPrompt 完全开源这个决定是被动的（作者加入 OpenAI 的条件），但结果对社区的影响实际上是主动的——有了 MCP server 主控这个架构升级，社区版比旧版更有框架价值。OpenAI 的招募既是对 Provencher 的认可，也间接帮社区做了一次"有赞助商的开源升级"。

**竞争格局**：类似工具有 Cursor 的 composer（部分功能重叠）、Claude Code 的 /compact 命令（手动压缩上下文）。RepoPrompt 的差异化是以"文件选择"为核心交互，而非对话框。国内目前无直接对应的同类工具，GitHub 可直接访问，使用门槛低。

---

## 快讯区

**收入信号**
- @marclou 分享收购案例 #113：$19/月 SaaS 卖出 $1,400（约 74 倍月收入，约 6.1 倍年收入）。marclou 自评："两年以上产品，3-5x ARR 倍数更常见"——提示小 SaaS 退出估值应该现实 — @marclou · 2026-06-28 20:43

**工具更新**
- Elon Musk 宣布 Grok 4.5（基于 1.5T V9 基础模型）在训练中加入了 Cursor 代码数据，已在 SpaceX & Tesla 私测，早期评估"性能接近甚至可能超过 Opus"[据推文原文，未独立验证]。SpaceX 计划每月从头训练并发布新模型。@aaditsh 指出：7 百万 Cursor 开发者写的代码正在训练 Grok，这才是这条新闻最值得关注的细节 — 2026-06-28 21:39

**产品发布**
- @indie_maker_fox 介绍腾讯推出的 Agent Mail：微信扫码注册，对话式发邮件，每人最多 2 个邮箱地址，每天可发 50 封，1G 存储上限。国内可用。暂无明确应用场景（据其自述） — 2026-06-28 17:00
- @shl（Sahil Lavingia，Gumroad 创始人）发布手机 App，允许用手机浏览桌面版网页。内容为视频，无法从文本分析具体功能和商业模式 — 2026-06-28 10:57

**工具观点**
- @SimonHoiberg（bootstrapped SaaS 产品矩阵）：已超过 1 个月没打开 GitHub 和 VSCode，自称 agent 负责全部编码工作，自己只做高层讨论和代码 review。补充：自建 Forgejo 替代 GitHub，让 agent 开 PR 并自动合并 — 2026-06-28 16:06 / 19:49
- @runes_leo：把 Claude / Codex / Grok / Cursor 四个订阅账号接入本地 relay，变成本机 127.0.0.1 可调用的 OpenAI 兼容 API（Opus 4.8 / GPT 5.4 / Grok 4.3 / Composer 2.5）。强调这是"自己的订阅给自己用"，不对外服务。把订阅比作"月票"，relay 是"工程接口" — 2026-06-28 10:42

**工具实践**
- @indie_maker_fox：出门前用 `/goal` 让 Codex 帮迁移网站到 TanStack 模板，到商场回来已完成并上线。利用模板内置一键部署脚本实现 — 2026-06-28 17:06

**教训与反思**
- @marclou 评论语言学习 SaaS 创始人的产品页，给出具体建议：同一款产品按"学日语""学韩语""学西班牙语"拆分成 3 个独立 SaaS，各用不同域名、logo、主题、文案。"启动一个，全力打，做到 1 万访客，再复制到下一个语言。" 这是一个把同一技术栈卖给不同市场的实操框架 — @marclou · 2026-06-28 12:52 · engagement_rate 0.45%

**值得关注的观点**
- @runes_leo：投了 DeepSeek Agent Harness PM 职位。认为这类岗位"不是从传统岗位树上长出来的，而是从真实的 builder、高强度用户、研究者中长出来的"。他的 JD 分析：核心要求是高强度用过 Claude Code / Codex / Cursor，能理解 agent 在真实任务里为什么会断，而不是写传统 PRD — 2026-06-28 16:08

**传播力素材**（适合自媒体改写的高互动观点）

- "As boring as it sounds, I'm slowly realizing that 90% of success is doing the obvious thing for a painfully long amount of time without convincing yourself you're smarter than you are." — @Jayyanginspires · 👍20,506 👁557,452 · engagement_rate 0.69%  
  改写方向：适合小红书长图文或视频号——以"最无聊的成功公式"为标题，拆解"做显而易见的事"和"长期主义"的具体案例，强调"不要说服自己比实际更聪明"这半句，反差感强  
  点评：击中频繁切换方向的焦虑群体。这句话的价值在于它对"找捷径"心理的直接点名。局限：对于真的需要调整方向的人，可能成为继续错误执行的借口，改写时要加前提条件

- "What would the person you want to become do with the time you're spending right now? Do that." — @AlexHormozi · 👍2,913 👁69,050 · engagement_rate 1.05%  
  改写方向：适合公众号或视频号——以"问自己这一个问题"为入口，结合具体场景（刷手机时/摸鱼时/选项目时）写成可操作的决策框架  
  点评：1.05% 的极高 engagement_rate 说明读者在存档使用——这类"触发即可行动"的内容比纯励志金句高一档。盲区：没有回答"想成为的人是对的吗"这个前提问题，对于目标本身不清晰的人价值有限

- "It's better to be focused than intelligent." — @AlexHormozi · 👍6,595 👁135,294 · engagement_rate 0.52%  
  改写方向：适合小红书图文——用 3-5 个具体案例对比"高智商跳来跳去"和"专注一件事的普通人"，结果反直觉  
  点评：在商业结果上有强验证（Hormozi 本人专注 Acquisition.com 生态做到 $2.3B 估值）。改写时注意受众：创业者和内容创作者接受度高，学生群体会有争议，需加前提条件

---

## 延伸资源库

### 播客 / 视频 / 访谈
- Lenny's Podcast × Andrew Ambrosino（@ajambrosino，OpenAI Codex 桌面 App 负责人）  
  话题：Codex 已有 500 万周活跃用户，OpenAI 员工 100% 使用；AI 时代"品味"才是核心竞争力；同产品 2 月发布 vs 11 月发布效果为何天壤之别（关键变量是模型，不是产品本身）；PM 的"区域防守"模式；Codex + ChatGPT 的整合愿景  
  YouTube：https://www.youtube.com/watch?v=P3KDebPTUrw  
  来源：@lennysan 转推，@nikunj 原发 · 2026-06-28 09:47

### 图书 / 课程
本期无图书/课程内容

### 链接汇总（从推文数据提取）

工具类：
- RepoPrompt 社区版（CE）GitHub：https://github.com/repoprompt/repoprompt-ce
- RepoPrompt 旧版 GitHub：https://github.com/repoprompt/repoprompt-classic

播客/视频类：
- Lenny × Andrew Ambrosino（Codex PM）：https://www.youtube.com/watch?v=P3KDebPTUrw

---

## 行动建议（按档位分组，不超过 4 条）

> 仅给出与本期金矿直接对应的档位建议

档位 B（独立开发者）
- 今天 30 分钟内：在有完整备份的测试 VPS 上安装 Claude Code，选一个最简单的 PHP/Python 项目，做一次"SSH 进 VPS → Claude Code 直接修改生产文件"的完整循环。哪怕只改一行 CSS，亲身感受这个工作流的手感
- 本周：在 macOS 上安装 RepoPrompt CE（`brew install --cask repoprompt-ce`），对一个正在维护的项目体验"精选文件→高质量 prompt"与"全部塞进去"的实际差异

档位 C（工具集成者 / vibe coder）
- 今天 30 分钟内：参考 @runes_leo 的方案，把至少一个订阅账号（Claude 或 Codex）接入本地 relay，变成本机可调用的 API 接口，打通现有自动化工作流
- 本周：用 `/goal` 指令让 Claude Code 在 VPS 上跑一个完整的晚间任务（批量数据处理或自动测试），明早检查结果

---

## 避坑指南

- **VPS 直接改生产环境的前提是备份，不是胆子大**：levelsio 明确提到 3-2-1 备份策略（3 份副本、2 种介质、1 份异地）。他能做到"直接改生产"是因为最坏情况下代价可控（宕机 10 秒，有完整备份）。没有完整备份就尝试这个工作流，是在赌运气，不是在学 levelsio。

- **小 SaaS 退出估值要现实**：marclou 分享的案例（$19/月 SaaS 卖 $1,400 ≈ 6.1x ARR）和他自己的评论（2 年以上产品 3-5x ARR 更常见）共同说明，小 SaaS 的退出价格远低于很多创始人的心理预期。如果创业目标是"做出来卖掉套现"，要提前了解这个市场现实。

---

## 本期情报评估

**信息密度**：低密度  
本期处于周末（2026-06-28~29，周日），实质性强信号偏少。大量推文是励志金句（AlexHormozi、Jay Yang）、高考志愿填报建议（lidangzzz 贡献了 15 条，大量与主题无关）、世界杯话题。与 AI 一人公司直接相关的可操作信号仅 2 条，其余为辅助信号。

**趋势信号**：  
"AI 编码的执行环境正在从本地迁移到云端"——levelsio 的 VPS 实践、SimonHoiberg 放弃 VSCode/GitHub、RepoPrompt 的 MCP server 架构转变，以及 @karpathy 通过 Slack 在云端用 Claude，这些信号在本期同时出现，方向一致，但都处于个人实践阶段，尚未形成主流工具链共识。

**横向对比**（本期有两条开发工作流相关信号）：  
levelsio VPS 工作流解决的是"在哪里运行代码"，RepoPrompt 解决的是"给 AI 看哪些代码"——两者互补，分别处于 AI 编程效率链条的不同环节，不存在竞争关系。

**当日强信号数 vs 噪音比**：  
2 条强信号 / 约 196 条噪音（约 1%）；周末+高考志愿季导致 lidangzzz 等账号大量发非主题内容，噪音占比高于平均水平

**本期信源**：@levelsio @dotey @marclou @runes_leo @akokoi1 @indie_maker_fox @SimonHoiberg @aaditsh @lennysan @AlexHormozi @Jayyanginspires（共 11 位）
