# AI 一人公司日报 | 2026-07-28

数据窗口：2026-07-27 06:00 — 2026-07-28 06:00（北京时间，过去 24 小时）
深度挖掘：2 条

---

## 今日头条

Moonshot AI 正式放出 Kimi K3 的模型权重与技术报告——2.8 万亿参数 MoE、104B 激活参数、1M 上下文、原生视觉理解，是目前公开的最大开源权重模型。真正值得一人公司圈子注意的不是参数量，而是它的商业授权结构：推理服务商一旦规模做到 ARR 超过 2000 万美元，必须单独签商业协议，训练和推理被拆开授权，被 @dotey 称为大模型界的"fabless"模式（类似芯片设计与代工分离）。这意味着围绕开放权重会长出一整套生态位——微调服务商、prefill 适配商、区域托管商——而不是所有人都挤在同一个闭源 API 入口上。对国内独立开发者和工具集成者，Kimi K3 提供了一个不依赖美元支付、Frontend Code Arena 跑分上还反超 Claude Fable 5 的可选项。

---

## 今日金矿

### 金矿 1：Kimi K3 —— 中国最大开源权重模型，附带一套"芯片式"商业授权

来源：@lidangzzz（转推 @Kimi_Moonshot）· 2026-07-28 00:00 · 6h ago · 👍28995 👁4493753 🔖7934
engagement_rate：0.18%（同期中位数约 0.15%-0.20%，处于正常偏上区间；本条金矿价值主要来自绝对传播量和后续多账号的深度解读，而非单条 ER）

**核心数据（已验证）**
- 2.8T 总参数 / 104B 激活参数，896 个专家、每 token 选 16 个，93 层（69 KDA + 24 Gated MLA），MoonViT-V2 视觉编码器 401M 参数（据 GitHub 仓库 README，经 web_fetch 核实）
- API 定价：输入 $3/百万 token（缓存命中 $0.3/百万 token）、输出 $15/百万 token，内置联网搜索 $0.015/次（据 OpenRouter 及多家评测博客交叉验证，约合 ¥20.3 / ¥101.5 每百万 token，按 1 USD≈6.77 CNY，据 Investing.com 2026-07-28 查询）
- SWE-bench Verified 得分 93.4%，在 Arena.ai Frontend Code Arena 排名第一，超过 Claude Fable 5（据行业评测网站交叉核实；[未经第三方独立复现验证]，厂商自测跑分需谨慎看待）
- GitHub 仓库 star 数 1.1k（据 web_fetch 核实，仓库刚发布，属早期数字，会快速变化）
- 完整运行 2.8T 模型需约 1.4TB 显存、官方建议 64+ 张加速卡（据 @eyishazyer 转推 @heypearlai），个人硬件基本跑不动，"开源权重"目前主要面向企业级部署

**商业模式拆解**
Moonshot 没有把 K3 做成纯闭源 API 生意，也没有完全免费开源，而是分层：个人/中小规模调用走标准 API 计费；一旦推理服务商做到 ARR 超 2000 万美元的规模，必须单独签商业协议。这套结构把"训练一个好模型"和"围绕它做生意"拆成了两件事，允许微调服务商、区域托管商、垂直场景适配商在权重之上长出自己的生意，而不必都给 Moonshot 交 API 过路费——直到他们自己做大到需要谈判的规模。

**复制路径（只写真正适用的档位）**
- 档位 B（独立开发者）：本周用同一批测试用例，把 Kimi K3 和现在用的模型（Claude / GPT / GLM）跑一遍前端代码生成对比，通过 platform.moonshot.cn 或 OpenRouter 的低价额度测试；如果产品面向国内用户，用支付宝/微信结算 API 调用费，能省掉美元信用卡和 Stripe 在国内的可用性问题。
- 档位 C（工具集成者/vibe coder）：K3 的 1M 上下文和原生视觉理解适合做长文档/多模态类的轻量工作流（例如批量图片+文字审核、长报告摘要），值得在 Dify / n8n 里接一个 Kimi K3 节点做对比测试。

**竞争格局**
国内开源模型这一档已经很挤：DeepSeek V4、Qwen3.7 Max、GLM-5.2 都是当前活跃的开源梯队选手，GLM-5.2 定价更低（$1.10/$4.10 每百万 token），DeepSeek V4 Flash 更低至 $0.139/$0.278（据 Morph 等评测站点数据）。Kimi K3 的差异化在于原生视觉理解、1M 上下文和跑分优势，但不是价格最低的选项。

**成本与时间预期**
API 调用按量付费，无起步门槛；自建部署门槛极高（64+ 加速卡），个人/小团队不具备可行性，需进一步调研云端按需租赁的实际成本。

**踩坑预警**
"开源权重"不等于可以无限制商用——规模做大后（ARR 超 2000 万美元）必须补签商业协议，靠转售/托管 K3 推理服务规模化之前要提前了解这个门槛。另外据 @lidangzzz 观察，Moonshot 当天连续发布了一堆产品线推文，信息分散、不成体系，普通用户很难串联起完整信息，建议直接看官方技术报告和博客（链接见延伸资源库），不要只看社交媒体碎片。

**深度综述**
这条信号的意外之处在于授权结构，而不是参数量本身——大部分人看到"开源权重"会默认等同于 Llama 那种近乎无限制的开源协议，但 Kimi K3 的"fabless"式分层授权说明中国大模型厂商正在探索一种介于全闭源和全开源之间的中间地带：用开放换生态覆盖和使用规模，同时给自己保留在下游巨头做大之后收租的权利。放在趋势坐标里看，这是国产大模型开源竞赛的最新一步，与 GLM-5.2、DeepSeek V4、Qwen 系列共同构成了一个价格战 + 生态战并行的格局，对独立开发者的直接利好是"可选项变多、议价能力变强"；但风险在于，今天免费或低价能用的权重，明天做大了可能要重新谈合同，这对计划长期靠转售模型服务盈利的团队是一个需要提前纳入商业计划的变量。竞争格局上，Kimi K3 的护城河目前主要是跑分和视觉理解能力，而不是生态或价格，一人公司量级的入场窗口期是开放的——只要不追求把它包装成大规模转售的推理服务生意。

---

### 金矿 2：Marketing Agents —— Greg Isenberg 拆解"从抓痛点到自动投放"的完整闭环

[产品名] Marketing Agents（方法论 + 工具栈组合，非单一产品）
来源：@gregisenberg · 2026-07-28 02:50 · 3h ago · 👍367 👁39513 🔖652
engagement_rate：1.65%（同期中位数约 0.15%-0.20%，属于 Top 5% 极高区间，说明读者在真实存档这条内容）
内容类型：Thread + 配套 YouTube 视频

**完整步骤（逐条列出）**
1. 用 Perplexity 抓取 Reddit 上的真实用户痛点，作为选题/需求来源
2. 用 Nano Banana（Google 的图像生成模型）生成符合品牌调性的静态素材
3. 用一个视觉模型反向检查生成素材是否符合品牌规范
4. 用 HeyGen 生成 AI UGC 风格的口播视频广告
5. 把以上环节接入一个循环：读取 Facebook 广告账户的实时数据 → 自动关停表现差的素材、放大表现好的素材，持续迭代
6. 商业化延伸建议：把 WordPress 生态里人们已经在付费的插件（Yoast SEO、WooCommerce、WP Forms）逐个做成"AI 原生版"——工具直接自动执行，而不是像 Yoast 那样只用红绿灯提示你该做什么。原文举例 Yoast 年收入量级在 $15M ARR（经 web_search 交叉核实，2019 年公开数据为 $12M ARR，近期第三方估算约 $16.4M/年，量级基本吻合）

**前置条件/适用人群**
已经有一定客户或内容基础、希望把"素材生成—投放—复盘"全链路自动化的独立开发者/营销从业者；对 Facebook Ads 投放逻辑和 Reddit 选题有基础认知者更容易上手。

**国内可用性：需要工具**
Perplexity、HeyGen、Nano Banana（Google 产品）、Facebook Ads 在国内均不可直接访问，需要科学上网 + 海外支付方式（信用卡/PayPal）。思路可以参考，工具栈需要替换为国产平替（例如秘塔AI搜索/文心一言替代 Perplexity，即梦/可灵替代 Nano Banana 做素材生成），但原文描述的执行细节无法直接照搬。

**预计耗时**
配套视频《Marketing Agents Are Too Good Now》（经 web_fetch 核实标题存在，具体时长未获取）；完整跑通一个闭环建议按"周"为单位规划，而非一天内完成。

**可直接使用的代码/配置**
无——为方法论框架，非代码教程。

**原始链接**
推文：https://x.com/gregisenberg/status/2081814601851900221
视频：https://youtube.com/watch?v=U2hogriGmEw

**深度综述**
这条信号的价值在于类比的精准和商业敏感度，而不是工具本身的新颖性——Perplexity、Nano Banana、HeyGen 都不是新工具，新的是把它们串成一个"感知-生成-投放-复盘"的闭环，并且举了一个具体到"WordPress 插件已经证明用户愿意为自动化 SEO/表单/电商功能付费"的商业机会，这比空喊"用 AI 做营销"要落地得多。放在趋势坐标里，这是"coding agents 改变了谁能做软件"叙事的下一步延伸——"marketing agents 改变了谁能做增长"，与近期大量关于 AI-native SaaS 替代传统 WordPress 插件的讨论相互印证，处于早中期验证阶段（有具体玩法但还没有跑出规模化收入案例佐证）。最大的局限对中国读者来说是工具链断层：Perplexity/Nano Banana/HeyGen/Facebook Ads 全部处于"需要工具"或事实上不可用的状态，直接复制执行链路不现实；能复制的是背后的结构性思路——找到用户已经在为某类自动化功能付费的存量市场（WordPress 插件生态在国内对应的可能是企业微信/飞书生态里的付费插件、或者独立站的付费 App 生态），用 AI 把"提示你做"变成"帮你做"。竞争格局上，这类营销自动化 Agent 目前门槛主要在工具组合和工程化能力，而不是某个单一环节的技术壁垒，先跑通闭环、先积累投放数据的人有先发优势，但窗口期不会太长——一旦有团队把这套流程封装成 SaaS 产品，单独复刻流程的价值会迅速下降。

---

## 快讯区

**收入信号**
- @marclou 用 TrustMRR 平台的 Stripe 验证数据追踪了 991 家初创公司：中位数月环比收入增速从年初 +9.0% 一路降到 6 月 -1.4%，整体中位数增长 1.6% 但趋势向下；分类目看，娱乐媒体 +72%（n=17，样本量小）、教育 +15%（n=69）、健康健身 +10%（n=36）逆势增长，而 AI 工具类目 -6%（n=230）、创作者经济 -13%（n=51）、游戏 -16%（n=15）在下滑 — @marclou · 2026-07-28 02:10 · 4h ago [数据据其自述来自 TrustMRR 平台真实 Stripe/RevenueCat/Creem 数据；TrustMRR 平台自身 MRR 规模经历史推文交叉核实约在 2.2万-3.3万美元/月量级，不同信源数字不一致，标注未统一核实]
- @marclou 发文称收到一个"上线 20 天新产品"的收购邀约，公开征询"接受还是再等等"，未透露具体金额 — @marclou · 2026-07-27 13:11 · 17h ago [未经验证，无 $ 数字]

**产品发布**
- @indie_maker_fox（独立开发者，出海 2 年破 10 万美元收入）当日连续开源多个小项目：MkDocs 文档站模板（基于 FumaPress，一键部署 Cloudflare Workers，支持多语言/暗黑模式/自动 sitemap）、"猫咪数独""超级积木"两款纯 AI 生成的小游戏（体积均低于 200KB，未做深度 review） — @indie_maker_fox · 2026-07-27 [GitHub: open-fox/mkdocs, open-fox/game-sudoku, open-fox/game-blocks，国内可直接访问]
- @packyM（Not Boring）开放"Solo Founders Program"申请：3 个月旧金山驻场 + 1 对 1 支持 + 10 万美元资金，押注"一人创业将成为伟大公司诞生的默认方式" — @packyM · 2026-07-28 05:46 [面向在美居留身份申请者，国内创业者基本不适用]

**工具更新**
- @xiaohu 转发 Claude Design 作者 Nate Parrott 亲述工具诞生始末，并分享 10 个实操技巧 — @xiaohu · 2026-07-27 20:33 · 9h ago
- @xiaohu 分享 Anthropic 官方 Opus 5 提示指南，核心建议是"做减法"而非堆砌提示词 — @xiaohu · 2026-07-27 13:50 · 16h ago
- @awilkinson（Tiny 联合创始人）分享 ChatGPT Voice 工作流：用语音模式配合多设备 Connections 功能，在徒步/开车/咖啡馆等场景用语音指挥主力电脑处理实际工作（写 newsletter 草稿、跟进 side project） — @awilkinson · 2026-07-27 21:12 · 9h ago · 👍8005 👁4438470 🔖9047（本期收藏数最高单条）[国内不可用，需魔法上网 + 海外 ChatGPT 账号]
- @bentossell：Kimi K3 已上线第三方推理平台 Droid，前两周限时 5 折优惠至 8 月 10 日 — @bentossell · 2026-07-27 23:49 · 6h ago
- @op7418：HuggingFace 专门为 Kimi K3 做了开源倒计时预告页 — @op7418 · 2026-07-27 16:58 · 13h ago

**值得关注的观点**
- @marclou："Codex 一次提示搭建完整 iOS App 并自动提交上架，我甚至没打开过 App Store。过去 10 年积累的执行技能正在贬值，剩下有价值的是判断力——想清楚做什么、以及决定不做什么。" — @marclou · 2026-07-28 05:50 · <1h ago
- @gregisenberg："AI 创业公司并购正在疯狂发生，周一早上就有两个人主动联系我要买公司；2021 年增长权重是盈利的 2.5 倍，现在 25% 增长 + 盈利 胜过 50% 增长 + 烧钱。" — @gregisenberg · 2026-07-27 23:18 · 7h ago [具体百分比数据来源未标注具体报告，标注未经验证]
- @SimonHoiberg（自举 SaaS 组合创始人）：自建 Grafana 做产品分析看板，替代 Amplitude/PostHog — @SimonHoiberg · 2026-07-27 16:04 · 14h ago

**教训与反思**
- @eyishazyer：Claude 分享链接隐私问题重演——本周末又曝出可被搜索引擎收录的分享对话泄露简历、API 密钥、疑似身份证号等敏感信息；Anthropic 已从 Google 索引下架，但泄露内容早被爬取并上传至 GitHub（含 Claude 和 Grok 对话），提醒"分享过的对话务必立即检查并撤销权限，下架不等于删除" — @eyishazyer · 2026-07-27 20:20/20:36 · 10h ago [据其推文自述及关联 GitHub 仓库链接，Claude 曾在 2025 年出现过同类问题]
- @dickiebush 转发一条旧文《7 个建立每日写作习惯的步骤》，本期收藏数高达 7431（但浏览量记录为 0，疑似数据异常），经 web_search 核实，同类"5/7/9 个步骤"内容至少可追溯至 2022-2023 年多个版本，本期未见新数据 [可能为旧素材回炉，不构成新信号]

**传播力素材**
- "Codex built me a new iOS app and submitted it. One prompt. I never even opened the App Store... The skills I acquired in the last 10 years have become useless. But strangely, I feel good about it." — @marclou · 👍1305 👁164186 · engagement_rate 0.3%
  改写方向：适合公众号/小红书——用"AI 让我引以为傲的技能贬值了，但我不慌"的反差角度切入，配上"一句话 prompt 生成 App 并自动上架"的具体细节做钩子。
  点评：击中了技术从业者面对 AI 替代的普遍焦虑，但用"从执行到判断"的框架化解焦虑而非制造对立，是反直觉但有说服力的视角；局限在于 marclou 本身有多年产品和渠道积累，"只要有判断力就够了"对完全没有基础的新手不成立，容易被断章取义成"不用学技术了"。

- "Marketing agents are the NEW coding agents... Coding agents changed who gets to build software. Marketing agents change who gets to grow a company." — @gregisenberg · 👍367 👁39513 · engagement_rate 1.65%
  改写方向：适合公众号技术/创业类选题——把"coding agents→marketing agents"的类比拆开讲透，配合具体工具链示意图。
  点评：类比精准且带着具体商业机会（WordPress 插件生态可复制到国内的付费工具场景），不是空喊口号；局限是背后工具栈国内几乎全部不可用，中国读者只能理解思路结构，无法直接复制执行细节。

- "You don't 'build an audience.' You build a valuable library of content in a category... that builds an audience." — @Nicolascole77 · 👍127 👁7747 · engagement_rate 2.84%（本期第一高 ER）
  改写方向：适合公众号内容运营类选题，拆成"内容资产 vs 粉丝数"对比图去讲。
  点评：点出了内容创作者常见的因果倒置——很多人先追粉丝数而不是先积累内容资产，这句话把顺序讲对了，属于内容运营圈的共识但表达精炼；局限是过于抽象，缺具体操作步骤，读者仍需自己摸索"如何构建内容资产库"。原推为 X Article 引用，经 web_fetch 尝试提取全文未成功（X Article 需登录访问），仅摘录可见部分。

---

## 延伸资源库

### 播客 / 视频 / 访谈
《Marketing Agents Are Too Good Now》—— The Startup Ideas Podcast（Greg Isenberg × Cody Schneider），YouTube：https://youtube.com/watch?v=U2hogriGmEw（国内需工具访问）

### 图书 / 课程
本期无

### 链接汇总（已 web_fetch / web_search 验证）
**工具类**
- Kimi K3 模型权重：https://huggingface.co/moonshotai/Kimi-K3（国内访问不稳定，需镜像如 hf-mirror.com）
- Kimi K3 技术报告：https://github.com/MoonshotAI/Kimi-K3/blob/master/k3_tech_report.pdf
- Kimi K3 官方博客：https://kimi.com/blog/kimi-k3（国内直接可用）
- Kimi K3 API 定价参考：https://openrouter.ai/moonshotai/kimi-k3
- Claude Design 诞生始末：https://best.xiaohu.ai/article/claude-design-nate-parrott/
- Opus 5 提示指南：https://best.xiaohu.ai/article/opus5-prompting-guide/

**GitHub**
- https://github.com/open-fox/mkdocs
- https://github.com/open-fox/game-sudoku
- https://github.com/open-fox/game-blocks

**报道类（用于交叉核实 Kimi K3 数据）**
- https://www.marktechpost.com/2026/07/16/moonshot-ai-releases-kimi-k3-a-2-8-trillion-parameter-open-moe-model-with-kimi-delta-attention-and-1m-context/
- https://www.morphllm.com/best-open-source-coding-model-2026

---

## 行动建议（按档位分组）

档位 B（独立开发者）
- 本周用同一批测试用例，把 Kimi K3 和现在用的模型跑一遍前端代码生成/长文档处理对比，通过 platform.moonshot.cn 或 OpenRouter 的低价额度先测试可用性，再评估是否值得替换部分国内支付场景的高成本调用。

档位 C（工具集成者/vibe coder）
- 本周挑一个"用户已经在为传统工具付费"的场景（参考 Yoast SEO 案例），用国产平替工具（秘塔AI搜索/文心一言替代 Perplexity，即梦/可灵替代 Nano Banana）先跑通"抓痛点→生成素材→发布"这两步小闭环，验证 Greg Isenberg 描述的结构在国内工具链下是否走得通。

---

## 避坑指南

- Kimi K3 的"开源权重"不等于可无限制商用：据 @dotey 核实，推理服务商规模做到 ARR 超过 2000 万美元后必须单独签商业协议。如果计划靠转售/托管 K3 推理服务规模化，需提前了解这个门槛，避免规模做大后才发现合规问题。
- Marketing Agents 方法论里的工具栈（Perplexity/Nano Banana/HeyGen/Facebook Ads）在国内全部处于"需要工具"或不可用状态，直接照搬执行链路走不通；能抄的是结构性思路，不是具体工具组合。
- Claude 分享链接的隐私问题是老问题重演（2025 年出现过一次），如果日常用分享链接做协作或内容素材，记得定期检查分享设置——从搜索引擎下架不等于内容已被彻底清除，此前已被爬取的内容可能仍在流传。

---

## 本期情报评估

**信息密度**：正常。时间线被 Kimi K3 开源发布（单一话题引发大量转发和二次解读）和大量个人生活分享（健身记录、旅行见闻、地缘政治评论、韦东奕相关争论）占据，真正与"AI 一人公司"强相关的信号集中在开源模型生态和一条营销自动化方法论上，其余多为中低优先级的工具更新和创作者内容。

**趋势信号**：中国大模型厂商延续"开源权重 + 分层商业授权"的打法，用生态覆盖而非纯闭源盈利参与国际竞争，同时国内大厂内部也出现资源赛马信号（腾讯微信 WeLM 对阵混元，据 @foxshuo 长文分析，属于行业背景信息，未纳入金矿）；海外独立开发者圈子里"营销自动化 Agent"叙事正在成型，对标此前的"编程 Agent"叙事，但配套工具栈仍以美国 SaaS 为主，国内复制存在明显的工具链断层。

**横向对比**：本期无多个可直接横向对比的收入数据点，跳过。

**当日强信号数 vs 噪音比**：2 条 B 级信号进入金矿，约 15 条中低优先级信号进入快讯；非 AI/非一人公司相关内容（生活方式金句、地缘政治评论、健身训练记录、韦东奕相关争论、明星八卦）在本期时间线中占比很高，粗略估计噪音与信号比例接近 4:1，读者刷到的时间线里真正可执行的情报密度中等偏低。

**本期信源**：@lidangzzz @gregisenberg @marclou @xiaohu @dotey @bentossell @op7418 @indie_maker_fox @SimonHoiberg @eyishazyer @Nicolascole77 @awilkinson @packyM @dickiebush（共 14 位）
