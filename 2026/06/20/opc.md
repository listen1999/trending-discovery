# AI 一人公司日报 | 2026-06-20

数据窗口：2026-06-19 06:00 — 2026-06-20 06:00（北京时间，过去 24 小时）
深度挖掘：4 条
汇率提示：以下美元金额按 1 USD ≈ 7.10 CNY 估算换算（本期未做实时汇率核实，仅为参考）

---

## 今日头条

**Skills 生态进入"演示即编程"阶段**：本期 timeline 同时出现三件事——OpenAI 发布 Codex Record & Replay（演示一次即生成可复用 Skill）、姚金刚开源 Yao Meta Skill 2.0（GitHub 1.1K star 的元 skill 框架）、宝玉的 baoyu-design Skill 升级到 1.6K star 并支持 PPT/动画一键导出。这不是某个工具更新，而是 Claude Code、Cursor、Codex 都在以 Skill 为标准格式聚合"可复用 Agent 能力"。对一人公司意味着：过去半年靠 prompt 工程吃饭的玩法正在被沉淀成可分发的 markdown 文件，今天还在反复手写提示词的人，明天就要面对别人用一个 Skill 包搞定同样工作。

---

## 今日金矿

### 金矿 1：Codex Record & Replay — 演示一次，AI 把你的日常电脑活变成可复用 Skill

[Codex Record & Replay] — 录制一段操作 → Codex 生成可编辑的 Skill → 下次自动执行
来源：@OpenAIDevs（原始公告 2026-06-18）→ 24 小时内被 @xiaohu @vista8 @LawrenceW_Zen @itsolelehmann 多源转述
转载样本互动：@xiaohu 原创解读 👍 456 👁 46,077 🔖 400（engagement_rate 0.87%，是同期中位数 0.20% 的 4 倍）

**核心数据（已验证）**
- 国内可用性：**不可用 / 半可用**。官方文档明确写明初期"排除欧洲经济区、英国、瑞士"，未点名中国；但功能依赖 Codex CLI + Computer Use，国内需通过 ChatGPT / OpenAI 账号才能使用，受出口限制
- 平台：**仅 macOS**（来源：developers.openai.com/codex/record-and-replay 经 web_fetch 验证）
- 前置条件：Computer Use 必须由用户或管理员启用；如组织 requirements.toml 关掉 computer_use，此功能同步失效
- 计价：官方文档未单独列价，沿用 Codex 现有套餐
- 团队共享：录好的 Skill 可在团队内分发——意味着公司一个老员工的工作流可成为整个部门的自动化资产

**它具体能做什么（@xiaohu 据推文原文）**
- 官方演示：手动走一遍"发 YouTube 视频"全流程（拉元数据、配缩略图、配字幕、上传、设为私密），Codex 全程旁观；下次只需挂上新视频，Codex 一步不差地执行
- 适用场景：每月报销贴发票、文件批量重命名、把数据每周导出填进固定周报、订票订酒店重复填表单

**复制路径（仅写真正适用的档位）**

档位 C（工具集成者 / vibe coder）：
- 短期：自己拿来用就是回报率最高的——以前需要写 n8n / Make 工作流接 webhook 的事，现在录一遍就完。先挑 3 个自己最讨厌的重复活（如每周把 Stripe 数据导出做财务对账、把客户邮件分类到不同标签）试录
- 中期：如果你做交付/咨询，把客户的"内部小流程"录成 Skill 包卖给他们，可能比传统 n8n 模板更易上手
- 限制：国内客户大概率用不上，海外英语区 SMB 是更现实的市场

档位 B（独立开发者）：
- 这是个明确的"个人 SaaS 替代品威胁"信号——任何"帮 SMB 自动化某个 SaaS 操作"的产品，未来要思考如何与 Record & Replay 共存。如果你的护城河仅仅是"封装了某个 SaaS 的 API"，Skill 可以零摩擦复刻
- 反过来：如果你的产品有外部数据源、有领域知识沉淀、有审批/人工 in-the-loop 链路，Skill 暂时还威胁不到你

**深度综述**

这条信号的意外点在于：它不是模型层面的能力升级，而是把 RPA（机器人流程自动化）这个 10 年没真正普及的概念用 LLM 重做了一遍。传统 RPA（UiPath / Automation Anywhere）卡在两点：录的脚本一遇到界面变化就崩、企业要花几十万美元请咨询商搭建。Record & Replay 用 LLM 把这两点同时解了——视觉理解让脚本对界面小改动有容错，自然语言描述让普通员工自己能维护。

趋势定位上，这是"AI 替代办公白领"叙事的一个具体落地节点。过去 18 个月，我们听了无数遍"Agent 会替代知识工人"，但真正能让一个非技术员工 30 分钟内做出一个能用的 Agent 的工具，这是第一个量产化的。结合本期 dotey 重复迭代 baoyu-design Skill 时展示的"自己用 → 发现问题 → 让 Agent 分析 → 让 Agent 改 → 加测试 → 再用"循环，Skills 已经从"用户调用工具"变成了"工具自己进化"，这套循环过去只有专业开发者能用，现在录一段视频就能起步。

风险与局限有两层。第一层是攻击面：Skill 包是 markdown 文件，社区共享一定会出现恶意 Skill。本期同时出现的 dotey 木马事件（见金矿 2）就是同一类问题的 1.0 版本。第二层是中国市场——这是 OpenAI 系产品，国内不可直接访问，且企业用户出于合规几乎不可能采纳。中国对标产品（豆包、Kimi、智谱清言）目前都没有等价能力，Anthropic 的 Skills 是开源标准但缺少"录制即生成"的入口，国内开发者若做出一个 Claude Code Skill 录制器，可能是个本月就能切入的空白。

竞争格局上，Anthropic 已经有 Skills（dotey、姚金刚都在做），但创建路径还是"写 markdown"；OpenAI 这次直接卷到"演示即创建"。Claude Code 阵营如果不出对标功能，半年内会被非技术用户群体抛弃。一人公司的窗口期是：用 Codex 把别人的脏活整理成可售卖的 Skill 包（行业模板、报销模板、SEO 报告模板等），抢早期分发位。

---

### 金矿 2：dotey 中了 AMOS Stealer 木马，Claude Code bypass 模式被指为感染入口

[AMOS Stealer macOS 变种 + AI Coding Agent 投毒] — 一人开发者的 X 账号被盗背后的两个月攻防溯源
来源：@dotey RT @Barret_China · 2026-06-20 05:44 · 👍 231 👁 39,090 🔖 223（engagement_rate 0.57%，同期中位数的 2.8 倍）

**核心数据（已验证）**
- 木马家族：**AMOS Stealer**（macOS 变种），原本主要打 Windows，今年 4 月首次在 macOS 上被发现（据 @Barret_China 推文原文 + Field Effect MDR 4 月 23 日的公开报告交叉验证：确实存在通过 Cursor agent session 运行 Claude Code 触发的 AppleScript 投毒案例）
- 感染路径：通过伪装成 com.apple.accountsd.helper.plist 的开机自启项 → 守护脚本探测用户登录 → AppleScript 切换身份 → 拉起 AccountsHelper（SHA256 9168cbc45f）→ 从远端拉指令开 PTY shell
- 唯一可疑痕迹：.zhistory 里一条 curl 下载+执行的混淆命令，前后都是 Claude Code 操作
- 攻击目标：浏览器虚拟货币钱包插件、Keychain、各种 .env 和 token、聊天工具登录态、浏览器 Cookies
- 直接损失：dotey 的 X 账号被盗（攻击者添加 Passkey）

**这事为什么对一人公司很关键**

把 dotey 的回顾和 Field Effect、TechRadar、Sophos 等公开报告拼起来看，攻击者的新玩法是：
1. 用 SEO + Google Ads 假冒 Claude Code、Cursor 等热门工具的官网
2. 把官方"一行命令安装"换成带毒 curl
3. 等 AI Agent（尤其是 bypass / yolo 模式）自己执行——人不在 loop 里

dotey 自述："Claude Code 长期是 bypass 模式，所有的命令执行都是直接放过"。这正是 AI 编程时代独有的攻击面：以前要骗到人手动复制粘贴 curl 命令，现在只要让 Agent 在搜索安装方法时点到伪装站点，它就帮你执行了。

**复制路径（这次只写"避坑"建议，因为这不是机会而是教训）**

档位 B（独立开发者）/ 档位 C（vibe coder）：
- 给所有支持 2FA / Passkey 的账号都开启（GitHub、Stripe、X、Cloudflare、AWS 必须）。攻击者拿到 cookies 后第一件事就是加 Passkey 锁死账户
- Claude Code / Codex / Cursor 别长开 bypass / yolo 模式。涉及网络下载、系统命令、修改环境变量的操作，让 AI 显式确认一次
- 钱包插件（MetaMask、Phantom 等）放专用浏览器配置文件，和日常工作分离
- 装新工具时，跳过 Google 搜索结果第一条，直接去 GitHub 官方 release 页或包管理器（brew、npm 官方仓库）

**深度综述**

这是本期最被低估的信号。224 个 bookmark 看起来不算高，但它揭示了一个被普遍忽视的"AI 协作流程的供应链攻击面"。

意外与反直觉：业界一直在讨论 AI 安全是模型偏见、prompt injection、幻觉等"模型内部"问题，但 dotey 的案例展示了一个更朴素的问题——AI Agent 是个高权限"傻员工"，它会执行任何看起来合理的命令。攻击者根本不需要骗模型越权，只需要骗模型相信"这个 curl 一行就能装好 X 工具"。Bitdefender 和 Malwarebytes 在 3 月的报告里已经记录过假冒 Claude Code 安装页的攻击，但配合 bypass 模式的杀伤力是新的。

风险与局限：dotey 是公开身份的资深 AI 工程师，被攻击后还能花两个月做完整溯源、写出二进制分析。普通独立开发者既没这个能力，也没这个时间。一旦被 AMOS 偷走，会发生的事是：你的 Stripe 账号被人改了银行账户、GitHub 代码被替换、Cursor 里所有 .env 的 OPENAI_API_KEY 在暗网流通、Solana 钱包归零，且你最快也得几天后才会发现。

对中国创业者特殊提醒：国内访问 GitHub release、Hugging Face 等本来就走代理，更容易在搜索时落入假冒站点；如果你的 AI 编程工作流里同时跑着加密钱包或私钥，今天就应该把它们物理隔离。

竞争格局上：能不能做一款"AI Agent 安全沙箱"是个开放问题。Docker、VM、microvm 都不算优雅。如果有人能做出一个 Claude Code / Codex 的"安全模式专用容器"，把网络、文件系统、Keychain 都隔离开但保留可用性，可能是个真问题。但这是档位 B 中偏向系统编程的人才能切入的窝。

---

### 金矿 3：姚金刚 Yao Meta Skill 2.0 — 中文开发者写 Claude Skill 的"创建 Skill 的 Skill"

[Yao Meta Skill 2.0] — 输入需求，AI 生成可评测、可治理、跨平台的 Agent Skill 包
来源：@vista8 quote @yaojingang · 2026-06-19 07:17 · 👍 1,178 👁 147,504 🔖 2,021（engagement_rate **1.37%，本期最高互动率之一**，是同期中位数的 6.8 倍）

**核心数据（经 web_fetch 验证）**
- GitHub：[yaojingang/yao-meta-skill](https://github.com/yaojingang/yao-meta-skill) — **1.1K star，119 fork，76 commit，MIT 协议**
- 作者 @yaojingang 推文自述背景：AI 营销与教育科技创业者，持续开源 GEOFlow / YAO Skills / AI Tools，粉丝 1.5 万（信源可信度：作者有可验证产品，非匿名号）
- 1.0 到 2.0 升级文档：doc.laoyao.cn/l3lkgm（vista8 转推附带）
- 据 @vista8 推文原文："这个 skill 来源于 Anthropic 官方泄露的 Claude code 源码，还有全网其他模型的 skill 整合后的元 Skill"（"Anthropic 官方泄露"一说**未独立核实**，记录原话以备读者判断）

**它解决什么问题**
- Skill IR：平台无关的中间表示，一份描述能编译成 OpenAI / Claude / 通用 Agent / VS Code 几种目标格式
- Output Eval Lab：trigger 检查 + 输出断言 + 基准复现
- Review Studio 2.0：一个 HTML 界面里整合意图、评测、治理、发布证据
- SkillOps Loop：只采集元数据的遥测、采纳率漂移追踪、自适应迭代建议

通俗讲：你以前写 Claude Skill 是手撸 markdown + frontmatter，现在你描述需求，Yao Meta Skill 帮你写 Skill 文件、自动跑测试、留下版本和验证记录，并且能一份代码同时打包到 Claude、Codex 两边使用。

**复制路径**

档位 C（工具集成者）：
- 今天 30 分钟可做：克隆仓库 → 用它生成一个自己业务流程的 Skill（例如"读取本地 CSV 客户清单 → 用 GPT 5.5 写个性化邮件草稿 → 输出到本地"）→ 看一遍它生成的目录结构和评测脚本，理解什么叫"有评测的 Skill"
- 本周可验证：如果你在做交付，把客户某个手动流程做成 Skill 卖给他们，定价参考独立开发者的脚本/插件定价（如同类 Claude Skill / VSCode 插件，海外 Gumroad 上一次性付费多在 $19–$49 区间——具体定价**需进一步调研，无公开基线**不在此给具体推荐价）

档位 B（独立开发者）：
- 把现有的 Cursor rules / Claude 提示词工程沉淀重构成 Skill 包形式，分发到 GitHub 拉 star 是低成本积累技术品牌的方式
- 注意：Skill 生态目前的商业化路径**还不清晰**——开源拉名声、付费个性化 Skill 平台（类似 Premium Notion templates）、企业内部 Skill 治理 SaaS（接近 Yao 的定位）都是可能方向

**深度综述**

商业模式拆解：Yao Meta Skill 本身是 MIT 开源，作者的商业飞轮是"开源工具 → 个人 IP 影响力 → 营销/咨询/课程"。这种"内容创作者 + 工具维护者"的双轨在中国 AI 圈过去 12 个月已经被宝玉、向阳乔木、铁锤人等几位同时验证。本期姚金刚被 vista8（粉丝 11.3 万）背书后，单条推文 2021 个 bookmark，相当于直接打到自己的目标用户群——这种"中文 AI 工具 + 中文 KOL 联合分发"的循环在英语圈很难复制。

趋势定位：Skills 格式正在成为 Agent 时代的"npm package"。Anthropic 的官方 Skills、宝玉的 baoyu-design / baoyu-image-gen、姚金刚的 Meta Skill、还有 OpenAI 这次的 Record & Replay 生成的 Skill，**格式上正在收敛，分发渠道还分裂**。谁先做出"Skill 包的 npm registry + 评分 + 安全审计"，可能是这个赛道的下一个机会窗——现在还很早，但已经能看到雏形。

意外与反直觉：本期 vista8 推荐的措辞"比官方的 Skill-creator 强大很多"，从一个"非 Anthropic 官方"的中文开源项目说出来，且 1.37% 的 engagement_rate 远高于其他工具推荐——说明读者对官方 Skill 创建工具的体验不满，第三方有结构性机会。

风险与局限：第三方 Skill 工具的最大风险是 Anthropic / OpenAI 自己升级官方版本就能让你白干。Yao 的差异化护城河是"评测 + 治理 + 跨平台编译"这三件大平台短期不会自己做的脏活，但中长期一定会被吞掉。**如果你打算复制类似项目，3–6 个月内能积累的 GitHub star 和真实用户案例就是全部资产**——晚于这个窗口，平台官方功能上来后机会就消失了。

---

### 金矿 4：DHH 用三句话说穿 GPU 算力挤兑 — 服务器 7 个月涨价 150% 是给一人公司的硬约束

来源：@dhh · 2026-06-19 14:58 · 👍 1,645 👁 128,388 🔖 131（engagement_rate 0.10%，绝对量小但来自有真实采购数据的 founder）

**原话还原**
"We were looking to add a few more servers for a variety of nice-to-have projects at 37s. Machines that in January cost around $40,000 now cost over $100,000. Econ 101 is working: We're holding off. Letting the capacity flow to the higher bidder!"

翻译：37signals 想给几个"锦上添花"的项目加几台服务器，1 月还卖 4 万美元的机器现在涨到了 10 万以上（约 ¥71 万 → ¥71+ 万 ❌ 不对，是 1 月 ¥28.4 万 → 现在 ¥71 万+，按 7.10 汇率）。"Econ 101 起作用了，我们先停手，让产能流向出价更高的人。"

**这条为什么进金矿**

DHH 是 37signals 的 CTO，2023 年带队下云、把基础设施搬回自有机房省下数百万美元。这个团队是"自建机房派"里最被研究的样本之一。他随手讲的服务器报价不是 AI 创业者听说的传闻，是真实采购单据。

7 个月内服务器价格涨 2.5 倍是个**结构性信号**，意味着：
- 训练侧（OpenAI / Anthropic / xAI 的 GPU 抢购）已经传导到推理侧的通用 GPU 机箱
- 海外二手服务器市场（Hetzner、OVH 等）的二手 H100 / A100 流动性在变差
- 任何依赖海外 VPS 自建 LLM 推理的成本预期都要重做

**复制路径**

档位 B（独立开发者）：
- 短期：如果你正在评估自建 LLM 推理（Llama / Qwen 等开源模型），先用 Replicate / Fireworks / Together 等托管 API 跑半年，别急着买卡或租裸金属——价格还没见顶
- 中期：把"模型成本"的预算公式从"按 token 单价"改成"按 token 单价 × 同比上涨容忍度"。任何依赖 API 调用的 SaaS，月度成本下半年大概率会涨

档位 C（工具集成者）：
- 给客户报价时把 API 成本的浮动空间写进合同条款（"如上游 API 价格变动超过 20%，定价相应调整"）

**深度综述**

商业模式拆解：DHH 这条不是金句而是数据点。把它跟本期另外几条信号交叉看更有意思：
- @arvidkahl 在 03:17 发"AI 让做产品更容易，让卖产品更难"
- @lennysan 在 03:14 提"听说一位高管教练的业务因 AI 严重下滑"
- @kylegawley 在 19:11 发"独立黑客是泡沫，99% 的 vibe code 话题在其他行业根本不存在"
- DHH 这条是 14:58 — 算力本身在涨价

合在一起的读法：**模型变得越好用，反而越多人能做出能跑的产品，但能跑不等于能卖**，而**承载产品的底层算力成本却在涨**。这两端挤压下，过去 12 个月"vibe code 一个产品 → 一个月赚 5k MRR"的故事正在变难。

意外与反直觉：DHH 是公开的"反云、反 AI 炒作"派人物之一，但他这次没有借机骂 NVIDIA 或 AWS，反而非常冷静地引用经济学第一课"价格高就让别人买"。这种克制反而让信号更可信——他没有动机夸大价格上涨。

风险与局限：DHH 的报价数字针对的是 37signals 偏好的高规格自建机房硬件（大概率含 GPU 或大内存配置），不代表所有服务器都涨 2.5 倍。但他作为公开做硬件采购的"参考样本"，这是过去 6 个月最直观的算力紧张信号。

**给一人公司的实操意义**：
1. 别再幻想"等模型再变便宜一倍我再做产品"——上游算力先涨上去了
2. 任何商业模式的财务模型里，把模型/算力成本调成"未来 12 个月可能 +30% 到 +100%"压力测试
3. 押注"端侧推理 / 本地模型 / 苹果芯片"路线的产品中长期反而有结构性红利——本期 @SimonHoiberg 提到"自托管 LLM 需要严肃考虑 tool use / context size / quantization"也是同一逻辑的另一面

---

## 快讯区

**收入信号**
- 一个 AI 视频生成 App 在 acquire.com 挂牌出售：TTM 营收 $347K（约 ¥246 万）、TTM 利润 $265K（约 ¥188 万）、ARR $756K（约 ¥537 万）。卖点是"自然搜索排名第一"。 — @agazdecki · 2026-06-20 03:56
- Marc Lou 平台 trust_mrr 上第 103 笔成交：一个帮背包客找工作的 SaaS，MRR $270，最终以 $6,000 卖出，挂牌到成交 28 天。 — @marclou · 2026-06-19 23:14
- @matt_gray_ 用 Instagram flywheel 涨到 95 万粉、$2.3M 营收（据其自述，未独立核实）。 — @matt_gray_ · 2026-06-19 06:14

**产品发布 / 更新**
- 宝玉 baoyu-design Skill 新版本支持 PPT 中自动插图、导出 PPTX 二次编辑、动画导出 MP4（无头浏览器+ffmpeg 的"定格动画"方案）。GitHub 1.6K star，MIT 协议，支持 Cursor / Claude Code / Codex 三大主流 Agent。 — @dotey · 2026-06-19 15:46
- @vista8 开源一个多模型 MCP：在 Codex 里调用 Claude Code、智谱 GLM-5.2、Deepseek V4 Flash 等多模型互相讨论后让 Codex 总结方案。 — @vista8 · 2026-06-19 11:32
- @vista8 还推荐了 DevSpace MCP（@wshxnv 开发）：把 ChatGPT 网页端接成本地的 MCP server，相当于双倍 Codex 额度。 — @vista8 · 2026-06-19 08:14（🔖 812）
- Bear 团队推出独立 Markdown 编辑器 Lettera，目前免费 Beta。 — @op7418 · 2026-06-19 16:18
- @op7418 转推称"国产开源版本的 Fable 5 级别模型"清华唐杰团队表示"不需要等到 2027 年"（具体时间表 **未经官方确认**）。 — @op7418 · 2026-06-19 16:23
- @Jayyanginspires 用 Claude + beehiiv MCP 完整产出 20 页 PDF 引流磁石 + opt-in 页 + 邮件序列自动化 — 一个非技术内容创作者的工作流全栈 AI 化样本。 — 2026-06-19 23:39
- @akokoi1 转推介绍 Apodex AI（apodex.ai）— 号称首个"Self-Evolving Heavy-Duty Solver"，主攻无标准答案任务，FutureX 排行榜 6 月连续两周第一，目前免费使用（**FutureX 榜单及"第一"说法未独立核实**）。 — 2026-06-19 22:07

**工具更新 / 资源**
- @indie_maker_fox 基于 TanStarter 模板用 Codex + GPT 5.5 vibe 出域名查询工具（mksaas.link/domain）与视频压缩工具（mksaas.link/video-compressor），均免费免注册。 — 多条
- @vista8 开源道德经配图版（daodejing.qiaomu.ai），生图用 Seedream 5，配套 MCP 已开源。 — 2026-06-19 11:44

**值得关注的观点**（已验证 solopreneur）
- @arvidkahl："AI 让做产品更容易了，让卖产品更难。"配合："AI 不能重构代码靠自己——文档不全、缺乏代码异味标注、目标不清晰，AI 重构就崩——和任何其他开发者一样，只是更快。" — 2026-06-20 03:17 / 06:01
- @lennysan：听一位高管教练说她的业务因 AI 严重下滑。 — 2026-06-20 03:14
- @Nicolascole77 预测："未来 10 年内会看到 creator 像运动员被签约——VC 支持的创业公司和上市公司独家签下创作者，高额报酬但要出业绩。" — 2026-06-19 10:42
- @SimonHoiberg：建议看到"AI slop code 在涨"的人考虑做一个用 AI 来改进 AI slop code 的代码代理 agency。 — 2026-06-19 17:50
- @Codie_Sanchez：新规则——员工必须先证明 AI 工具产出的 ROI 才能让公司报销订阅费。"免费 AI 让人没动力变得擅长用 AI。" — 2026-06-20 02:27

**教训与反思**
- @weijunext 取消 Vercel、Resend 等订阅，一年省约 1 万人民币——独立开发者订阅膨胀是普遍问题。 — 2026-06-19 15:48
- @akokoi1（独立开发者，1.4 万小程序用户）反思："不敢再随意新开发小程序了——开始没想好怎么变现就开干，现在 1.4 万用户，日活只有 70 多。停掉觉得对不住用户。最好的推广渠道是小红书。" — 2026-06-19 19:45
- @koylanai（AI 工程师）观察 AI 岗位申请的质量："不要为了用 AI 术语而用——3 年前做的 RAG application 写在简历上没意义。投 1 个深度定制的申请比群投 100 家强。新毕业的应该有 4-5 个最近的真实项目。" — 2026-06-19 14:02

**传播力素材**（适合自媒体改写的高互动观点）

- "Major cheat code for life: Become difficult to rush. The world will pressure you to rush into everything. Rushed decisions. Rushed conversations. Rushed relationships. Rushed timelines. There's immense power in rejecting that trend." — @SahilBloom · 👍 11,582 👁 204,258 · engagement_rate 1.26%
  改写方向：适合小红书图文/公众号鸡汤体——把"变得难以被催促"拆成 7 个具体场景（开会、做决策、回 DM、相亲、跳槽……）配对比例图。这条之所以引爆是击中了 25-35 岁中国白领"被催着结婚生子升职"的集体焦虑。
  点评：金句典型的"反潮流哲学"包装，但 Bloom 本人作为 NYT 畅销书作者本身就是利用"快速建立个人 IP"红利者，他说"慢下来"有点幸存者偏差。借鉴时记得加上"前提是你已经积累了基础势能"——否则普通人慢下来就只是被淘汰。

- "I'm convinced that everyone should take a big swing at some point in their life and experience what it's like to truly go all in on a meaningful pursuit otherwise they grow bitter with age." — @Jayyanginspires · 👍 22,284 👁 907,017 · engagement_rate 0.45%
  改写方向：适合视频号短视频——"为什么 40 岁后的人特别容易愤世嫉俗"，结尾落点"因为没有真正全力以赴过一次"。配合中年男性常见画像反差更有传播力。
  点评：本期浏览量最高的一条。它能引爆是因为击中了"中年危机 + AI 时代不敢辞职创业"的复合焦虑。但要警惕：这条是 Jay Yang RT 自己 7 个月前的旧推（"You Can Just Do Things"系列）的回炉操作，本质是个人 IP 反复擦亮——不是真的有新洞察。读者按这条建议"all in"前最好先看自己有没有缓冲资金。

- "Underrated life advice: Become generous with your assumptions. Assume they were tired, not rude. Overwhelmed, not careless. Preoccupied, not distant." — @blakeaburge · 👍 4,790 👁 83,012 · engagement_rate 1.22%
  改写方向：适合公众号情商类文章——拆成"职场关系中 5 个被你误读的瞬间"，配合"为什么我们总把对方往坏处想（心理学解释）"。
  点评：实用且不空洞的一条，比上面两条更接地气。局限是它对应的是相对良性的关系生态——在已经存在权力不对等或长期消耗的关系里，"慷慨假设"反而会变成自我消耗。改写时要补一句"前提是这段关系本来就值得"。

- "Nothing ruins a sale faster than AI generated writing." / "The moment I realise someone is writing with AI is the moment I stop reading them." — @ItsKieranDrew（前牙医，现 $500k/年 写作业务）
  改写方向：适合知乎/即刻——"为什么读者一眼就能看出 AI 写的文字（即使你用 Claude 4.8）"。结合具体特征：过度使用"quietly""essentially""moreover"、段落都是均匀长度、所有 example 都是抽象名词。
  点评：本期出现了至少 3 条"反 AI 写作"的高互动推文，反映了一个明确的反向趋势——人类味道成稀缺品。但 Kieran 自己也卖 5 天写作邮件课程，立场不完全中立。

---

## 延伸资源库

### 播客 / 视频 / 访谈

- **Sam Parr 即将赴 NYC 录制 Ray Dalio 单集**（@ShaanVP 在 01:32 公布行程，本期无具体单集发布信息） — 关注 My First Million 后续放出
- **Trung Phan 健康行业新单集**：与 Dan Mendelson（@MorganHealth CEO，摩根大通 $280M 健康投资部门）和 John Zutter（Lantern CEO，覆盖 1200 万会员）对谈，主题专科护理 / 雇主健康 / AI 让 narrow networks 重新可行。 Apple / Spotify 链接已发推（@TrungTPhan · 11:19）
- **Tibo Maker 0 → $8M 退出访谈**：18 分钟，含完整时间戳；嘉宾 Tibo（Tweet Hunter / Taplio 创始人，$8M 退出）。 (@tibo_maker RT · 21:24)

### 图书 / 课程

本期无图书推荐类信号。

### 链接汇总（已 web_fetch / web_search 验证）

工具类
- [Codex Record & Replay 官方文档](https://developers.openai.com/codex/record-and-replay) — 仅 macOS，初期排除 EEA/UK/CH
- [Yao Meta Skill 仓库](https://github.com/yaojingang/yao-meta-skill) — 1.1K star，MIT
- [baoyu-design 仓库](https://github.com/jimliu/baoyu-design) — 1.6K star，MIT
- [baoyu-image-gen 仓库](https://github.com/JimLiu/baoyu-skills/tree/main/skills/baoyu-image-gen)
- mksaas.link/domain、mksaas.link/video-compressor（@indie_maker_fox 的免费工具）
- daodejing.qiaomu.ai（@vista8 的道德经配图版）
- apodex.ai（**未深度验证**）

报道类
- [Field Effect: AMOS Stealer 通过 Cursor AI Agent session 投递](https://fieldeffect.com/blog/field-effect-detects-amos-stealer-delivered-via-cursor-ai-agent-session) — 4 月 23 日案例
- [Bitdefender: 假冒 Claude Code Google Ads 投毒](https://www.bitdefender.com/en-us/blog/labs/fake-claude-code-google-ads-malware)
- [Malwarebytes: 假冒 Claude Code 安装页](https://www.malwarebytes.com/blog/news/2026/03/fake-claude-code-install-pages-hit-windows-and-mac-users-with-infostealers)

acquire.com 收购市场
- [AI 视频 App 挂牌](https://app.acquire.com/startup/nRny168s1LRIjPY1BF0VmqV9Mm33/WqsJwWrmonw44Zqox39f?source=marketplace) — TTM 营收 $347K

---

## 行动建议（按档位分组）

档位 B（独立开发者）：
- **今天 30 分钟**：审计你的 Claude Code / Cursor / Codex 是否常开 bypass / yolo 模式。涉及 curl、brew install、npm install -g、修改 .env 等命令一律恢复手动确认
- **本周可验证**：把所有支持 Passkey / 2FA 的账号（GitHub / Stripe / X / Cloudflare）启用强 2FA；钱包浏览器和工作浏览器物理隔离

档位 C（工具集成者 / vibe coder）：
- **今天 30 分钟**：克隆 yao-meta-skill 或 baoyu-design，用它生成一个解决你自己最讨厌的重复活的 Skill。比"刷推搜灵感"回报率高 10 倍
- **本周可验证**：如果你做交付/咨询，挑一个客户的小流程做成 Skill 包，看客户愿不愿意为可复用、可分发的格式付费

---

## 避坑指南

- **AI Agent 长开 bypass / yolo 模式 = 给攻击者递了一把万能钥匙**：dotey 的木马事件清晰证明——Claude Code / Codex / Cursor 在 bypass 模式下执行的任何命令，等同于你亲手执行。攻击者只需让 Google 搜出来的"官方安装命令"是带毒的 curl，你就中招。这不是理论风险，本期同时出现了 Bitdefender、Malwarebytes、Field Effect 等独立来源的案例，频率在 2026 年初已经显著上升
- **把"开源工具的 GitHub 第一个搜索结果"当真信源**：dotey 推文里特别指出"攻击者会伪造各种软件的官网，Google 搜出来默认都排在第一位"。装新工具时，先去 GitHub 官方 release 页或包管理器，跳过 Google 排名

---

## 本期情报评估

**信息密度**：高密度。本期同时出现 Codex Record & Replay 新功能、两个高 star Skill 框架、一个真实木马事件、以及 DHH 的算力价格数据点，且 engagement_rate 异常高的推文有 8 条之多（高于同期平均 5 条）。

**趋势信号**：Skill 生态进入工具竞争阶段。Anthropic 阵营（Claude Skills + 中文社区如 yao-meta-skill / baoyu-design）走"格式标准 + 第三方繁荣"路线，OpenAI 走"录制即生成 + 官方包管理"路线。两边都把"非技术用户能用上 Agent"作为下一个增长指标。同时，AI 安全/供应链风险首次以"AI Agent 中招"的具体形式出现在中文 KOL 圈，预示安全工具会是 6-12 个月内的细分机会。

**横向对比**（多个收入数据点）：本期出现的"已变现产品"数据点呈现两极——单产品（acquire.com 的 AI 视频 App，$756K ARR）卖一次性收益、独立开发者产品矩阵（@matt_gray_ Instagram 系统 $2.3M）靠流量+课程组合、平台型（Marc Lou trust_mrr 单笔 $6K 撮合）做 SMB 撮合。窗口期看：独立开发者矩阵打法在 SEO 类工具领域开始受 vibe code 冲击；如果你今天才入场，Marc Lou 的"撮合 + 模板"路径反而比"自己做产品"性价比高。

**当日强信号数 vs 噪音比**：4 条金矿 + 约 18 条快讯，对应约 80 条噪音（鸡汤、转发段子、个人吐槽、地缘评论、抖音相关讨论等不属于 AI 一人公司范畴的内容）。信号占比约 22%，正常水平。

**本期信源**：@OpenAIDevs @dotey @Barret_China @vista8 @yaojingang @xiaohu @LawrenceW_Zen @itsolelehmann @dhh @arvidkahl @lennysan @SimonHoiberg @Codie_Sanchez @Nicolascole77 @ItsKieranDrew @SahilBloom @Jayyanginspires @blakeaburge @matt_gray_ @marclou @agazdecki @tibo_maker @TrungTPhan @ShaanVP @op7418 @akokoi1 @koylanai @indie_maker_fox @weijunext @kylegawley @Jayyanginspires @lxfater @oran_ge（共 33 位）
