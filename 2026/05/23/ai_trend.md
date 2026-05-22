# AI 行业情报简报 | 2026-05-23

> 数据窗口：2026-05-22 06:00 — 2026-05-23 06:00（北京时间，过去 `24 小时`）
> 深度分析：3 条 | 模板版本：v2.3

---

## 1. 重大新闻 & 突发事件

- Microsoft 取消内部 Claude Code 订阅，AI 订阅红利期正在结账

  来源：@HedgieMarkets（经 @ylecun 转推 10615 收藏）· 约 11 小时前
  关键数字：Microsoft 取消内部 Claude Code 订阅，近 10 万工程师改用 GitHub Copilot CLI（来源：windowscentral.com，已核实）；Uber 内部备忘录称 4 个月烧光全年 AI 预算（来源：@HedgieMarkets 转述，当事方未公开备忘录原文）；称美国 AI 软件价格 6 个月内 +20%~+37%（[未经验证]）;Microsoft 历史上对 OpenAI 投资 $13B（来源：The Information，已核实）
  行业影响：对 Anthropic 是直接出血——大客户「按席位」简单合同要重谈成 usage cap + overage，企业首次正面看到 token 单价。对 OpenAI/Google/xAI 同样适用：补贴期一旦结束，企业真实付费意愿才会显形。Microsoft 选择回流自家 GitHub Copilot CLI，等于把「成本可控」当采购第一指标，国内 DeepSeek、Qwen Coder、Doubao Coder 等低价 endpoint 的换装窗口被同步拉开。

- xAI Grok Build 进入开发者编码 CLI 战场

  来源：@elonmusk（24 小时内 6+ 条相关推/转推）· 24 小时贯穿
  关键数字：SuperGrok Heavy $299/月，前 6 个月可走 SuperHeavy $99/月（来源：mem0.ai、devops.com，已核实）；API $0.20/M input、$1.50/M output；SWE-Bench Verified 70.8%、256k 上下文；最多 8 个 sub-agent 并行 + plan mode 强制确认（来源：devops.com，已核实）；当日 0.1.214 Build 含 X 搜索、Windows 渲染修复、MCP token 过期处理（来源：@skcd42，当事方口径）
  行业影响：把 Claude Code、Codex 的入门档拉到 $99，Musk 个人转推十余条用户实测推文（kilocode 测 5 个网站、Boyuan Zheng「recursive self-improvement loop」、xAI 新官网）做免费分发。Anthropic 失 Microsoft 后，编码 agent 增量心智被 Cursor + xAI + Google Antigravity 三家以「便宜或不限量」横切瓜分。

- Cursor Composer 2.5 把 Opus 4.7 / GPT-5.5 价格打到 1/10–1/30

  来源：@ArtificialAnlys（经 @elonmusk 转推）· 约 5 小时前
  关键数字：每任务比 Claude Code 中 Opus 4.7（medium）便宜 3–18x，比 Codex 中 GPT-5.5（medium）便宜 5–32x；基准平均仅用 1.6M token vs 其他 5.7M；平均 ~9 分钟/任务，Fast 版 ~7 分钟（来源：@ArtificialAnlys，第三方独立 benchmark）；API $0.50/M input、$2.50/M output（来源：cursor.com，已核实）；SWE-Bench Multilingual 79.8%，反超 GPT-5.5 的 77.8%（来源：the-decoder.com，已核实）；底层为 Kimi K2.5 base + 25× 合成训练任务 + Sharded Muon optimizer（来源：cursor.com，已核实）
  行业影响：紧贴 Anthropic / OpenAI 涨价节奏出手，把「单任务费」当一级产品指标。Composer 2.5 用 Kimi K2.5 作 base，等于让 Cursor 自家分发渠道「绕过 Claude」也能拿到 Opus 4.7 同档体验；对国内 Moonshot 是免费推广。

- OpenAI Codex 上线 Appshots + Remote Computer Use

  来源：@gdb / @AriX · 约 19 小时前
  关键数字：macOS Cmd+Cmd 把任意 app 的可见 + 不可见上下文塞入 Codex（来源：@AriX，当事方口径）；笔记本锁屏后仍可从手机远程驱动桌面 app；@gdb 同步声明「the model alone is no longer the product」（6094 likes、611k views）
  行业影响：把编码 agent 从「仓库内动作」扩展到「全 OS 动作」，对 IDE 外的实际办公链路是 frontier lab 里第一个落地的方案。@gdb 的判断 + Codex/Antigravity/Composer 同周齐发，等于头部 lab 承认 frontier 模型差异化已收窄，差异来自「产品形态 + 资源调度 + OS 集成」。

- Google Antigravity 周内 Gemini 配额二次 3x，Gemini 3.5 Flash 跑赢 3.1 Pro

  来源：@_mohansolo（经 @sundarpichai、@demishassabis 转推）· 约 15 小时前
  关键数字：Antigravity 周配额连续两次三倍（48 小时内累计 +9x）、所有付费档配额重置（来源：@_mohansolo，当事方口径）；Gemini 3.5 Flash 在 GDPval 上超过 Gemini 3.1 Pro（来源：@OfficialLoganK，当事方口径）；同期 Demis 展示用 Gemini Omni 把 Google Maps 截图 + 路线变成第一人称驾驶视频
  行业影响：Google 用「不限量补贴 + Flash 跑赢上一代 Pro」抢编码 agent 增量用户。Omni 系列同时拉模态宽度（图→视频）和 Flash 等级延迟，是把多模态从「概念秀」拉进「日常 IDE 工具」的最直接信号。

- DeepSeek-V4-Pro 折扣转永久

  来源：@deepseek_ai（经 @jeremyphoward 转推 2510 收藏）· 约 2 小时前
  关键数字：原阶段性折扣价改为永久（来源：@deepseek_ai，当事方口径，未单独披露绝对价格）；同窗口 @huggingface 转推开发者用 DeepSeek-V4-Flash + OpenRouter，1 美元以内完成 distilbert 任务级 fine-tune（来源：@Everlier，当事方口径）
  行业影响：与 Composer 2.5、Grok Build 同周出招，国内开源/出海一线把「价格底」按住，对北美 frontier lab 涨价形成正面对冲。开发者侧的「OpenRouter + DeepSeek」组合在本轮成本焦虑下回到首选。

---

## TOP 新闻深挖

#### 深挖：Microsoft 取消内部 Claude Code 订阅

背景补充：
Microsoft Claude Code 内部试点 2025 年 12 月在 Experiences & Devices 部门上线，因实际 token 账单远超 flat-seat 估算，定于 2026-06-30 全面取消，近 10 万工程师切回 GitHub Copilot CLI（来源：windowscentral.com、aiweekly.co、techbuzz.ai）。Uber CTO 4 个月烧光 2026 年 AI 预算的备忘录目前仅二手转述，绝对金额未公开。

数字核实：
- 「~10 万工程师切换」→ 已验证（来源：Windows Central）
- 「Microsoft $13B 投资 OpenAI」→ 已验证（来源：The Information / Reuters 历史报道）
- 「美国 AI 软件 6 个月内 +20%~+37%」→ 未在 IDC / Gartner 公开报告中复现，[未经验证]
- 「Uber 4 个月烧光全年 AI 预算」→ 仅 @HedgieMarkets 引内部备忘录转述，备忘录原文未公开，存疑

扩展影响：
直接冲击 Anthropic 的企业 ARR——大型客户的简单席位合同被迫重谈。同周 Cursor / xAI / Google 用「单任务费 1/10」「$99 入门」「不限量」三路反击，OpenAI 用 Appshots/Remote 把「OS 集成」当差异化。GitHub Copilot CLI 因「成本可控」反而拿到内部份额。

对国内从业者的意义：
1）API / Agent 类产品 BD 话术需从「能力对比」改成「单任务成本对比」，准备一份同 benchmark 下的「每 1k 任务花多少」表；2）DeepSeek-V4-Pro 永久折扣 + Qwen / Doubao 等低价 endpoint 在出海 SaaS 集成端口的替代窗口期落在 6 月这一波；3）做 enterprise AI SaaS 的国内团队应主动接 Anthropic 流失客户，尤其「内部代码 agent」这类高 token 场景。

延伸阅读：
https://www.windowscentral.com/microsoft/microsoft-cancels-claude-code-licenses-shifting-developers-to-github-copilot-cli-a-move-likely-driven-by-financial-motives

#### 深挖：xAI Grok Build 进入编码 CLI 战场

背景补充：
Grok Build 于 2026-05-14 以 agentic CLI 形态公开 beta，正面对标 Anthropic Claude Code 与 OpenAI Codex（来源：eweek.com、devops.com、engadget.com）。订阅层 SuperGrok Heavy $299/月，前 6 个月可走 SuperHeavy $99/月「拉新」档。底层模型 SWE-Bench Verified 70.8%、256k 上下文。

数字核实：
- 「最多 8 个 sub-agent 并行 + plan mode」→ 已验证（来源：devops.com）
- 「API $0.20/M input、$1.50/M output」→ 已验证（来源：mem0.ai 等多源）
- 24 小时内 @elonmusk 至少 6 条相关推/转推（含 @boyuan__zheng「recursive self-improvement loop」、@kilocode「测 5 个网站」、@benjitaylor xAI 新网站、@skcd42 Daily Build 0.1.214）→ 高密度、当事方多渠道分发

扩展影响：
入门档 $99 把 Claude Code Pro 的 $200/月段位拉到一半。Anthropic 失 Microsoft 后，开发者增量心智被 Cursor + xAI + Google Antigravity 三家以「便宜或不限量」瓜分。Boyuan Zheng 的「recursive self-improvement loop」是营销语，未公开技术细节，国内复刻团队暂不应当作差异化基础。

对国内从业者的意义：
1）Grok Build 在中国大陆不可直接订阅，但 API 经 OpenRouter / 第三方中转，开发体验团队可做 benchmark 对照；2）Musk 用「私号 megaphone + 24 小时连环更新 + 版本号 0.1.214」把迭代节奏推到「日更」，对国内 coding agent 团队冷启动期是直接示范——公开 release notes 频率本身就是产品。

延伸阅读：
https://www.eweek.com/news/xai-grok-build-coding-agent/

#### 深挖：Cursor Composer 2.5 单任务费降到 Opus 4.7 的 1/10

背景补充：
Cursor 于 2026-05-18 发布 Composer 2.5（来源：cursor.com/blog/composer-2-5）。技术栈披露：Kimi K2.5 base + 25× 合成训练任务 + targeted text-feedback RL + Sharded Muon 优化器；定价 $0.50/M input、$2.50/M output；Fast 版同等智能但延迟更低，$3.00/M input、$15.00/M output（来源：buildfastwithai.com，已核实）。

数字核实：
- 「每任务 3–18x / 5–32x cheaper」→ @ArtificialAnlys 独立 benchmark，与 Cursor 自报「1/10 token 成本」一致量级
- 「SWE-Bench Multilingual 79.8% > GPT-5.5 的 77.8%」→ 已验证（来源：the-decoder.com）
- 「CursorBench v3.1 63.2%」→ Cursor 自家 benchmark，需按当事方口径打折看

扩展影响：
对 Anthropic：Cursor 自家分发渠道用 Kimi K2.5 + 自研后训练就贴到 Opus 4.7 同档，单任务费用低一个数量级。对 OpenAI Codex：多语 SWE-Bench 已被反超，必须靠 Appshots / Remote 这种「OS 集成」拉差异化。对国内 Moonshot：等同免费做了一次国际化推广。

对国内从业者的意义：
1）验证「半开源 base + 一线后训练」链路在 2026 仍能贴近 Opus 4.7，是国内 coding 产品的可复刻参考；2）有 Kimi K2.5 调用权限的团队，可优先评估「自家后训练 + 25× 合成任务」复刻成本与上限；3）Composer 2.5 仅在 Cursor IDE 内运行（不开放 API 蒸馏），国内 IDE 类产品的窗口是「同价位、同 base、可本地化部署」。

延伸阅读：
https://cursor.com/blog/composer-2-5

---

## 2. 新产品 & 功能发布

- LeRobot Humanoid — Hugging Face / LeRobot 团队

  核心能力：
  - 完整开源人形机器人栈：硬件 CAD、运行时、标定、仿真环境、训练 zoo
  - 整机 BOM ~$2,500，主要为 3D 打印 + 现成件
  - sim-to-real 行走策略迁移视频已放出（红色双足）

  链接：https://huggingface.co/blog/VirgileBatto/lerobot-humanoid ｜ https://github.com/Virgileboat/lerobot-humanoid
  立即试用优先级：本周内试
  理由：首个把「整机 < $3k + 全栈开源」打到位的双足平台，可用同一份训练管线对标 Figure 类商业线。

- llama.cpp 内建模型路由 + WebGPU 后端 — llama.cpp / UC Santa Cruz（Hugging Face 转推）

  核心能力：
  - 单 server + 单 INI 在 disk 上的多模型间秒切，零重复缓存
  - WebGPU backend 已合入 llama.cpp/ggml，浏览器端即可跑全规格 LLM
  - 性能贴近 native llama.cpp，无抽象层

  链接：https://youtu.be/V2t_YRsyqeI
  立即试用优先级：本周内试
  理由：直接吃掉 Ollama + Open WebUI 的角色，本地 inference 栈回到 llama.cpp 单中心。

- Perplexity Bumblebee — Perplexity AI

  核心能力：
  - macOS / Linux 只读扫描器，检查 AI 工具、扩展、包的供应链风险
  - 与 Perplexity Computer 联动后可在新供应链风险出现时自动复扫
  - 仓库已公开开源

  链接：https://github.com/perplexityai/bumblebee
  立即试用优先级：本周内试
  理由：少见地把「agent 工作的安全外环」做成只读工具的实际产品，企业引入 AI agent 时直接可用。

- MiniMax Agent × Perplexity Search 集成 — MiniMax / Perplexity

  核心能力：
  - MiniMax Agent 默认搜索切换到 Perplexity Search
  - 700+ agent 任务基准：tool-call 数 -45%（17.8 vs 32.6）、token -42%（94.6M vs 162.3M）、pass rate +2%、总成本 -27%（来源：@MiniMaxAgent，当事方口径）

  链接：https://agent.minimax.io/
  立即试用优先级：观望
  理由：「单次搜索更好 → 整个 agent 链路成本下降」的实证案例；Perplexity 作为 agent 搜索中间件的占位速度值得追踪。

- Cohere Command A+ 上架 Microsoft Foundry — Cohere / Microsoft Azure

  核心能力：
  - 单一模型覆盖推理、多语、多模态、检索、编码、tool use
  - 以 Managed Compute offer 形态进入 Foundry，企业可直接拉起
  - 同期 @aidangomez 确认这次发布走 Apache 2.0（与 Cohere Transcribe 同协议）

  链接：链接未提供（推文未直接附 Foundry URL）
  立即试用优先级：本周内试
  理由：Cohere 把企业级 agent 工作负载做成 Apache 2 + 进入 Azure 主流分发，是开源 + 企业渠道两边吃的少见路径。

- Notion 移动应用焕新 + Agent Insights — Notion / @ivanhzhao + @NotionHQ

  核心能力：
  - 全新视觉语言先在 Notion AI App 落地，再覆盖 Notion / Calendar
  - 配套 Agent Insights：按 agent / 用户级别看「谁建了什么、跑了什么、花了多少、有没有用」
  - 配 credit limits、usage controls、agent-level access 共同构成「agent 治理」首套官方能力

  链接：链接未提供
  立即试用优先级：观望
  理由：是头部 SaaS 第一个把「企业里跑一千个 agent 怎么治理」做成产品级答案，正面响应当下 token 计费焦虑。

---

## 3. 行业趋势 & 热议话题

- 编码 Agent 进入价格 / 资源战的总爆发周

  参与讨论的主要声音：@elonmusk（Grok Build $99）、@cursor_ai 经 @ArtificialAnlys（Composer 2.5 单任务 1/10 成本）、@gdb / @AriX（Codex Appshots + Remote Computer Use）、@sundarpichai / @demishassabis / @_mohansolo（Antigravity 配额二次 3x）、@deepseek_ai 经 @jeremyphoward（V4-Pro 折扣永久）
  主流观点：5 家在同一周用不同武器抢同一个用户——xAI 走 megaphone + 低价、Cursor 走「单任务费 1/10」、OpenAI 走「OS 全屏覆盖 + 远程 agent」、Google 走「不限量」、DeepSeek 走「永久低价」。
  主要分歧：差异化路线分裂——Cursor / DeepSeek 押单位经济，Google / xAI 押补贴 + 流量，OpenAI 押 OS 集成。
  信号强度：强
  判断依据：5 个独立组织 24 小时窗内同向出招，每一家都有可验证产品动作或价格变化（详见 Section 1 第 2–6 条）。

- 开源人形机器人平台同周齐发

  参与讨论的主要声音：@huggingface / @ClementDelangue（LeRobot Humanoid ~$2.5k 全栈开源）、@adcock_brett（Figure 四年技术回顾，认为深度学习 + 全身 RL 把人形 timeline 至少压缩 10 年；F.03 完成 200 小时连续无故障 logistic 用例）、IEEE Spectrum（open-source-robot-ai-platforms 综述）
  主流观点：硬件层已基本去风险化，竞争重心移到 AI 控制 + 数据；开源平台首次把整机 BOM 压到 $3k 以下。
  主要分歧：开源派（HF）与垂直整合派（Figure / Hark）对未来 5 年人形机器人价值分布的判断截然不同。
  信号强度：中
  判断依据：HF 全栈开源 + Figure 公开技术回顾 + IEEE Spectrum 综述，3 个独立来源 + 配套硬件 / 文章发布。

---

## 4. 值得关注的洞察 & 观点

- @gdb（OpenAI President）：

  「the model alone is no longer the product」（@giffmana 续：「The model and the limit reset button are now the product」）
  为什么值得关注：是头部 lab 自上而下承认 frontier 模型差异化已收窄，未来差异来自「产品形态 + 资源调度（limit reset / 配额）+ OS 集成」。与同期 Codex Appshots、Antigravity 3x 配额、Composer 2.5 单任务费降一个数量级相互印证。

- @adcock_brett（Figure / Hark Labs CEO）：

  「过去四年有 4 个突破把人形机器人 timeline 至少压缩了 10 年：低成本电动整机 / 端到端深度学习（pixel→torque）/ 全身 RL 控制 / 在人类速度做有用工作。」配合 F.03 在 logistic 用例下连续 200 小时无故障。
  为什么值得关注：与 LeRobot Humanoid 同日发布的「行业自评」，少有的把硬件 + 算法两侧门槛同时下调的当事方陈述。可作为 12 个月内人形商业落地的领先指标。

- @AndrewYNg（DeepLearning.AI 创始人）：

  「新的白宫政策要求绿卡申请人从美国境外申请，是对合法移民的任性打击，会让美国失去医生、教师、科学家，并伤害美国在 AI 上的竞争力。」（同期他另一条批评 Harvard 限制 A 等级比例 ≤ 20%）
  为什么值得关注：连续两条对美国 AI 人才路径的同向表态。在 frontier 模型成本压力 + 移民收紧叠加下，AI 人才向中国 / 欧洲 / 中东重新分配的窗口期更具体。

- @ylecun 转推 @Dan_Jeffries1：

  「封闭、网监型 SaaS 的 LLM 体系 + 它的 everything-app harness，都会被两层开源替换：开源模型 + 开源 agent harness。」
  为什么值得关注：在 Microsoft 砍 Claude Code 当天，LeCun 选择转推「开源接管」的强观点；与 Hugging Face 当天连发 LeRobot Humanoid、CommonCrawl-on-HF Buckets、WebGPU llama.cpp 形成互证。

- @GaryMarcus：

  「OpenAI Erdos 结果背后我们不知道：尝试了多少题、是否在已发现的反例上训练过、新模型与旧模型差异在哪、训练数据是什么、用了多少算力。」同步援引 The Information 数据：OpenAI Q1 营业利润率 -122%（已核实）。
  为什么值得关注：在 OpenAI IPO 季 + Erdos 数学营销期，把「frontier lab 论文/营销可信度」的核查清单一次写齐，可作为评估同类宣传的复用模板。

---

## 5. 实用资源 & 教程

- Mosaic 概率天气模型

  类型：论文 + 项目（@maxxxzdn 团队，经 @Thom_Wolf 转推）
  用途：单 H100 < 12s 生成 24 成员、10 天全球概率预报；推 ML 天气预报 Pareto 前沿
  链接：链接未提供（推文原 thread）
  上手难度：高

- Gated DeltaNet-2

  类型：论文 + 代码（NVIDIA Research / NVlabs）
  用途：1.3B 规模把 erase / write 两个门解耦的线性注意力新架构；长上下文检索 S-NIAH-3 从 63 升到 90，multi-key needle 28→38
  链接：https://github.com/NVlabs/GatedDeltaNet-2
  上手难度：高

- SimpleTES

  类型：论文 + 框架（Stanford AI Lab）
  用途：把 evaluation-driven loop 作为科学发现的 scaling axis；21 个科学问题取得 SOTA，含 2.17x lasso 求解器、IBM Q20 量子布线开销 -24.5%
  链接：链接未提供
  上手难度：中

- RecCuriosity

  类型：论文 + 代码（Berkeley AI Research）
  用途：以「记忆」为核心的 3D 探索 agent + world model，配合 episodic context 与 persistent worlds
  链接：https://recuriosity.github.io/ ｜ https://github.com/recuriosity/recuriosity ｜ https://arxiv.org/abs/2605.22814
  上手难度：中

- CommonCrawl April 2026 on Hugging Face Buckets

  类型：数据集 + 工具
  用途：在不下载的前提下用 DuckDB 直接 SQL 查询 2.19B 网页索引（hf:// 上 35 秒可全量计数）
  链接：https://huggingface.co/spaces/davanstrien/common-crawl-april-2026
  上手难度：中

- ArtifactLinker

  类型：工具（Ai2，HF 转推）
  用途：预测哪些模型在哪些 HF 上托管的 benchmark 上可创 SOTA，并自动跑评测验证；把 HF Hub 当「可执行、可验证的发现引擎」用
  链接：链接未提供（thread 起点）
  上手难度：中

---

## 传播力素材

- 「the model alone is no longer the product」 — @gdb · likes 6094 / views 611841 · engagement_rate 1.0%
  改写方向：适合公众号 / Newsletter 长文头标题「模型不再是产品」+ 给非技术读者解释三层产品壳（模型 / 配额 / IDE-OS 集成）。
  点评：OpenAI 总裁的自承，含金量高，但单看一句容易被误读成「模型已无差异」。真实信息是「模型 + 配额 + 调度 + IDE 集成 = 产品」，对应同期 Codex/Antigravity/Composer 的协同打法。

- 「The model and the limit reset button are now the product」 — @giffmana · likes 247 / views 21208 · engagement_rate 1.2%
  改写方向：开发者社区吐槽贴，配 Antigravity 3x 配额截图做对比。
  点评：是对 @gdb 那条的精炼，比之多了「limit reset」的讽刺，反向揭示 token 计费时代「重置按钮的稀缺性 = 商品」。盲区：没指出真正稀缺的是 inference 算力本身。

- 「post-training makes models LESS human-like」 — @GaryMarcus 转推 @ValerioCapraro · likes 105 / views 12088 · engagement_rate 0.87%
  改写方向：AI 安全 / 对齐自媒体改写，搭配「窄域 fine-tune 触发跨域 misalignment」案例做长文。
  点评：少见的有大样本支撑（>20 万被试、~2600 万人类响应）的反共识结论。盲区：是否「human-like」应当是优化目标本身仍存争议。

- 「i don't think i need cloud models anymore」 — @ClementDelangue 转推 @danyurkin · likes 50 / views 10451 · engagement_rate 0.22%
  改写方向：本地推理 / 边缘 AI 类账号引用，配 llama.cpp WebGPU、内建路由当佐证。
  点评：HF CEO 转推等于背书。盲区：「不再需要云模型」对个人开发者成立，对企业级 RAG / agent 还偏激进，需要在受控负载下验证。

- 「We just wrapped what began as an 8-hour challenge — and it ran for 200 hours without a failure」 — @adcock_brett · likes 9256 / views 4097030 · engagement_rate 0.03%
  改写方向：人形机器人垂类自媒体可直接引用为「商业落地里程碑」。
  点评：少数可量化的人形机器人 reliability 数字。盲区：未披露任务复杂度、SKU 范围、抓取 / 放置失败的判定标准。

---

## 一句话总结

24 小时内是编码 agent 价格 / 资源战的总爆发：Cursor Composer 2.5、xAI Grok Build、OpenAI Codex Appshots + Remote、Google Antigravity 3x 配额、DeepSeek-V4-Pro 永久折扣同周出招，背景是 Microsoft 砍掉内部 Claude Code、Uber 4 个月烧光全年 AI 预算——AI 订阅红利期正在以「单位经济」为单位结账。同日 Hugging Face 把整机开源人形（LeRobot Humanoid）的 BOM 压到 ~$2,500，开源栈从 LLM 蔓延到机器人本体。

## 今日行动建议

今天（30 分钟内）：
基于「Cursor Composer 2.5」——用 Cursor 首周双倍额度跑一遍你手头最常拒绝交给 Opus 4.7 / GPT-5.5 的高 token 任务，记下完成时间和 token 用量，立即建立单位成本基线（https://cursor.com/blog/composer-2-5）。

本周内：
基于「Microsoft 取消 Claude Code」——做一份 1 页内部备忘录，把当前所有付费 AI 工具按「每月席位费 → 真实月 token 消耗 → 推算 usage-based 等效费」三栏排序，标出哪 1–2 个工具会在 GitHub / Anthropic 切 usage-based 时单月成本翻倍，准备换约或自建。

月内验证：
基于「Grok Build / Composer 2.5 / DeepSeek-V4-Pro」——以 ArtificialAnlys Coding Agent Index 或自家任务集为锚，30 天内跟踪三家的 SWE-Bench Verified + Multilingual 分数、API 单价、$/任务，月底输出一张「四家 coding agent 性价比变动表」，作为采购或自研决策依据。

---

## 信号 / 噪音比

进入第 1 节的有效新闻 6 条，进入第 2–5 节的有效信号 22 条，剩余约 60% 为低价值或噪音（@elonmusk 个人 / 政治 / SpaceX / 足球 / 名人 RT 等非 AI 内容、ylecun 政治转推等）。今日整体信号密度：正常。

**本期信源**：@ylecun @elonmusk @gdb @demishassabis @sundarpichai @sama @AndrewYNg @GaryMarcus @ClementDelangue @huggingface @jeremyphoward @adcock_brett @giffmana @AravSrinivas @cohere @aidangomez @Thom_Wolf @NotionHQ @ivanhzhao @StanfordAILab @berkeley_ai @NandoDF @GoogleDeepMind @GoogleAI @MIT_CSAIL @StanfordHAI @rowancheung @hugo_larochelle @fchollet @nvidia @deepseek_ai @cursor_ai @ArtificialAnlys @MiniMaxAgent @perplexity_ai（共约 35 位，含被转推的官方账号）
