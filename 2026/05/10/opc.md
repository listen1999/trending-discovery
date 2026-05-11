# AI 一人公司日报 | 2026-05-10

数据窗口：2026-05-09 11:01 — 2026-05-10 11:01（北京时间，过去 24 小时）
处理推文：245 条 | 活跃用户：70 位 | 深度挖掘：3 条

---

## 今日头条

**Codex 长会话上下文管理实战四招——把"模型越用越笨"问题量化拆开**

@lxfater（铁锤人，公众号同名，GitHub 维护 30k star 项目，自述 12M 浏览长文经历）翻译并扩写 @cjzafir 的 Codex 上下文优化方法，给出 4 段可直接粘贴的 prompt（关闭 Process_narration、做 orchestrator 而非 worker、强制 task list、强制清理工作目录），自述"每轮节省 40% 上下文"。该推文 24 小时内 57,220 阅读、809 收藏，收藏率约 1.4%，明显高于本期其他同类内容——意味着工具集成者（C 档）和独立开发者（B 档）真的在收藏后用，而不是看完就忘。Codex / Claude Code 长会话掉性能是当下日常痛点，"分模式 + 卸活给 sub-agent + 强制规划 + 强制干净目录"四件套今天就可以嵌进现有工作流。

---

## 今日金矿

### 金矿 1：Codex 长会话上下文优化的 4 条可粘贴 Prompt

来源：@lxfater · 2026-05-10 00:17 BJT · 👍531 👁57,220 🔖809
内容类型：Quote Tweet（引用并中文扩写 @cjzafir 英文原版，原版 1,398 likes，发布于约 24 小时窗口边缘）

完整步骤（逐条列出，不压缩）

1. **关闭进度叙事，省输出 token**
   - 设置 `Process_narration=false`
   - 默认 Codex 把所有规划步骤打印给你看，但你不会真的逐条审，关掉就直接砍掉每轮的"自我解说"输出 token

2. **让 Codex 当协调者，不当苦力**
   - 中文 prompt（@lxfater 版）：
     > 充当协调者，用并行 agents 做研究和执行，给每个 agent 写详细任务，强制它们行动、迭代、完成，带回深入报告，你的工作是分析、反馈、给持续任务
   - 英文原版（@cjzafir）：
     > Act as an orchestrator. Use parallel agents to do the research and execution work. Write detailed tasks for each parallel agent and force them to act, iterate, get their tasks done, and bring back an in-depth report. Your job is to deeply analyze the agents' work, provide feedback, and provide them with continuous tasks.
   - 核心：吃上下文的脏活全卸给 sub-agent，主上下文只留干净的协调任务。同时开 5 个 agent，相当于 5 个独立上下文窗口在跑

3. **强制先列 task list 再动手**
   - Hard rule（cjzafir 原文）："Measure twice, cut once policy."
   - 不开 plan mode（"那玩意太重"），但要求每个任务先输出 task list、再执行，进度可追、可迭代
   - 防止在调试 / 修补这种本来就乱的工作里，Codex 一边乱试一边污染上下文

4. **强制保持代码库干净**
   - 粘贴 prompt：
     > 保持代码库干净，没有临时文件，没有死代码，没有死文件，始终保持组织化，没有不必要的文件夹、子文件夹、文件
   - Claude 把脏东西藏在缓存里所以代码库整洁；Codex 输出贼重，几轮会话后工作目录会一团乱
   - 目录乱 → 上下文跟着脏 → 性能下降，闭环

附加技巧：规划阶段用 Codex 5.5（超高），方案定了切到 Codex 5.5（高）+ 快速模式执行——脑力和速度分开使。

前置条件 / 适用人群

- 长期开 Codex 长会话的开发者；用 Cursor / Claude Code 做 vibe coding 的人也基本通用（核心是"卸活给 sub-agent + 工作目录干净"两条 universal）
- 国内可访问性：Codex（OpenAI）需要工具，Claude Code 直接访问，Cursor 直接访问
- 预计耗时：5 分钟把 prompt 写进 `CLAUDE.md` / `AGENTS.md` / Codex settings

可直接使用的代码 / 配置

把以下内容加入项目根目录 `CLAUDE.md` 或 `AGENTS.md`：

```
## Orchestration
Act as an orchestrator. Use parallel agents to do the research and execution work.
Write detailed tasks for each parallel agent and force them to act, iterate, get their
tasks done, and bring back an in-depth report. Your job is to deeply analyze the agents'
work, provide feedback, and provide them with continuous tasks.

## Codebase hygiene
Keep the codebase clean: no tmp files, no dead code, no dead files. Stay organized at
all times. No unnecessary folders, subfolders, or files. Follow the existing file structure.

## Planning
Measure twice, cut once. Output a task list before any non-trivial change; track progress
through it.
```

复制路径

档位 B（独立开发者）：今天就把上面三段贴进 `CLAUDE.md` / `.codex/AGENTS.md`，下一次开 4 小时以上的长会话之后回来对比性能感觉。
档位 C（工具集成者）：把 "orchestrator + parallel sub-agent" 这套思路搬到 n8n / Make / 自研 agent pipeline——主流程不写脏活，所有抓数据 / RAG / 文件操作放进子流程，主流程只做调度和反馈。

原始链接

- 中文展开版：https://x.com/lxfater/status/2053147480938971585
- 英文原版（cjzafir）：https://x.com/cjzafir/status/2052801300627435996

---

### 金矿 2：iOS AI App $200/mo 在 Trust MRR 以 $1,250 完成交易

[产品名] 未公开（@marclou 推文中只标 "iOS AI app"）— 一句话定位：iOS 端 AI 工具产品，月 MRR $200，已易主

来源：@marclou · 2026-05-09 20:46 BJT · 👍154 👁17,572 🔖30

核心数据（已验证，据推文原文 + marclou 个人 bio）

- 月收入：$200/月（约 ¥1,420，按 1 USD ≈ 7.1 CNY [汇率参考，需以当日中间价为准]）
- 成交价：$1,250（约 ¥8,875）
- 成交倍数：~6.25× MRR
- 平台：Trust MRR（@trust_mrr，专做小型 SaaS / iOS 项目交易的市场，定位 < $5K 收购额这一段）
- 卖家身份 / 买家身份：未在推文披露 [未经验证]
- 参考锚点：@marclou 自身 bio 公开 7 个产品组合，分别为 $36K/$21K/$9K/$8K/$2K/$0/$0/m，合计约 $76K/m（据其推特个人主页）

商业模式拆解

- 这是一个"小型 SaaS / iOS App 退出"信号，而不是稳定盈利产品本身
- 6.25× 倍数在 < $5K 总价的 micro-acquisition 段属于市场常态——买家逻辑通常是"低成本拿资产 + 用 AI 重做"，不是真要靠它现金流回本
- 真正值钱的不是产品代码，而是已有付费用户、已上架且通过审核的 App Store 资产、关联的开发者账号

复制路径

档位 B（独立开发者）：把 "$200/m 也能脱手" 理解为试错的最低退出阈值——独立开发者做 iOS AI 小工具，做到稳定 $200/m 就有市场（Trust MRR、Acquire.com、IndieMaker），不必非追 $1K MRR；反过来这意味着"做出 $200/m"才是真正第一个里程碑，之前的 PoC 没退出价值。
档位 C（工具集成者）：参考意义在于估值锚点——把交付给客户的 GPTs / Claude Skill / 自动化工作流当资产报价时，"× MRR" 倍数可参考 micro-app 的 2-10× 区间，但服务流量和 SaaS 留存不可直接套用。

竞争格局

- 国内同类二级市场仍然薄弱（独立开发者社群有零星接洽，但没有像 Trust MRR / Acquire.com 这样规模化、标准化的成交平台）
- 国内独立开发者要走这条退出路径，目前主要选项还是出海挂在 Trust MRR / Acquire.com / Flippa；国内更多是项目 / 团队 / 收益权直接转让，缺标准化估值

成本与时间预期

- 不在公开数据基线内，需进一步调研

[关键约束]

- 不要把 "$200/m → $1,250" 解读成"做个类似产品就能复刻"——成交价大头其实在"已有付费用户 + App Store 资产 + 已通过审核的开发者账号"，这三件资产对国内开发者尤其值钱（开发者账号 + 已审核通过的 AI App，自己冷启会卡很久）

原始链接

- 推文：https://x.com/marclou/status/2053094145884086562
- 平台：Trust MRR（推文 @trust_mrr）

---

### 金矿 3：$1.5M ARR / 93% 利润率数字营销代理上架 Acquire.com

[产品名] 数字营销代理（具体公司名未在推文披露）— 一句话定位：100% 合同制循环收入、93%+ 利润率的数字营销代理，挂牌出售

来源：@agazdecki · 2026-05-10 05:25 BJT · 👍11 👁810 🔖1
（发布人 Andrew Gazdecki 是 Acquire.com 创始人，bio 自述平台累计撮合 $500M+ 交易）

核心数据（已验证，据推文原文）

- ARR：$1.5M（约 ¥10.65M，按 1 USD ≈ 7.1 [汇率参考]）
- TTM 营收：$1.6M（约 ¥11.36M）
- TTM 利润：$1.5M（约 ¥10.65M）
- 利润率：93%+
- 营收性质：100% 合同制循环收入

商业模式拆解

- 利润率 93%+ 在代理行业属于极端，意味着核心成本是"老板自己的时间 + 极少数关键员工 + 工具订阅"，几乎没有外包 / 项目交付成本
- 100% 合同制 = 没有项目制冲单、没有渠道返点的代理形态，更像"小型 retainer 咨询"而不是传统乙方
- 这种业务很难规模化，但单老板拿走百万美金以上是完全可行的——这正是它适合一人公司的核心

复制路径

档位 D（服务变现者）：核心启示是"合同制 + 极简交付 + 极少数客户"。把咨询 / 培训 / 私教打包成 retainer（按月固定金额，包含具体可量化的交付物如 "每月 2 次会议 + 1 份月报 + Slack 答疑 SLA"），客户数量压到个位数，比常见的"按项目报价 / 按效果分成"更适合一人公司。本期推文未披露具体客户行业 / 客单价，因此不写具体定价区间——需打开 Acquire.com listing 自看再判断。
档位 C（工具集成者）：把"AI 工作流"打包成同样的 retainer 形态：固定月费、固定交付物（每月 X 个新工作流 + 维护既有 + Slack SLA），一次配置长期收钱，比按项目交付的现金流稳健很多。

竞争格局

- 国内同类形态：财务咨询 / 投顾 / 法律 retainer / 私董会，都是相同结构；AI 工作流 retainer 在国内是空白市场，门槛在客户教育（让客户认"我每月付 X 元买你的 SLA"而不是"我付 X 元买这个项目"）

成本与时间预期

- 不在公开数据基线内，需进一步调研

原始链接

- 推文：https://x.com/agazdecki/status/2053224767080268149
- Listing：https://app.acquire.com/startup/vBBHg0v9vzMnLvUZgGj1SKtzO4u1/pbKPkKhq2roeKAIQRvfO/（需注册 Acquire.com 账号查看完整资料）

---

## 快讯区

**收入信号**

- @starter_story 引用 Marc Lou 的"$77K/月、上午不看手机、4-6 小时深度工作、做过 35 个 startup"叙事被 @thepatwalls 转推，24 小时内 182,135 阅读、2,106 收藏 — 内容上没有新数据点，与 marclou 自身 bio 公开的 ~$76K/m 组合数据吻合，反映"早晨深度工作 + 多产品组合"叙事仍在持续吸量。@thepatwalls · 2026-05-09 21:15 BJT
- @indie_maker_fox（独立开发，bio 自述"产品出海，2 年收入破 10 万美刀"）公开 MkSaaS 模板 3-4 月联盟佣金已支付完毕；展示出"模板 + 联盟分销"的商业闭环跑通，但本条无具体金额披露。@indie_maker_fox · 2026-05-09 21:43 BJT

**产品发布**

- @dhh 发布 Omarchy 3.8（基于 Hyprland 的 Linux 发行版），新增提醒、天气、统一配置默认浏览器 / 终端 / 编辑器、可选无加密安装、内置 transcoding flow。@dhh · 2026-05-09 22:55 BJT · 👍944 👁50,680 · github.com/basecamp/omarchy/releases/tag/v3.8.0
- @op7418（歸藏）发布 PPT Skill 新主题预告（替代千篇一律衬线字体方案，配合 Claude Code Skill 调用）。@op7418 · 2026-05-09 23:35 BJT · 🔖180

**工具更新**

- @indie_maker_fox 把 TanStarter（Cloudflare Workers 上的 TanStack Start SaaS 模板）文档接入 Context 7 平台，意味着 LLM 可直接调用最新文档辅助 vibe coding。文档站：tanstarter.dev / context7.com/websites/tanstarter_dev。@indie_maker_fox · 2026-05-09 21:24 BJT
- @lxfater 引用 @easychen 的开源项目《一人企业方法论》第二版（github.com/easychen/opc-methodology），将其包装成 Claude Skill 调用。@lxfater · 2026-05-09 14:39 BJT · 🔖299
- @indie_maker_fox 转推 9Router（GitHub 趋势榜开源项目，统一管理 Codex / CC 订阅 + minimax / glm plan + opencode / openrouter 免费模型作为编程工具的代理）— 24h 内的二次扩散，原推非本期窗口。@indie_maker_fox · 2026-05-10 10:30 BJT

**值得关注的观点**（仅收录已验证 solopreneur）

- @tibo_maker（Tweet Hunter / Taplio 联合创始人，Taplio 据其 bio 自述以 $8M 出售）："$1M+/月不是线性增长——失败 startup × 2、死掉的产品 20+ 才换来 1 个跑通的"，提醒"产品 #3 在挣扎"≠ 失败，是常态。@tibo_maker · 2026-05-09 21:14 BJT · 👍169
- @marclou：理想晨间流程 = 头晚关机 / 老婆共进早餐 / 1-2 小时健身 / 上午只开 Cursor + localhost:3000。该叙事与 starter_story 那条 $77K/m 重合，可视为同一作者本人版本。@marclou · 2026-05-09 21:34 BJT · 👍1,108
- @vista8（向阳乔木）："Codex 口碑近期超过 Claude；下一波该 Gemini 发力" + "vibe coding 时骂模型频率明显下降（模型实际进步证据）"。@vista8 · 2026-05-10 00:57 BJT · 👍43

**教训与反思**

- @runes_leo 的"减法系统"：每条新规则跑 14 天，0 次产出动作就砍。一年砍掉约 20 条，本周砍 3 条。判定标准——留下的全有"产出闭环（跑完 → 推动具体动作 → 复盘）"，砍掉的全是"行为合规（扫了 N 条 / 检查了 X 项）"——给独立开发者 / 创作者的"个人系统该不该加新规则"提供了简单判据。@runes_leo · 2026-05-10 09:38 BJT
- @starter_story："几乎所有上节目的赚钱独立开发者都做了同一件事——抄已被验证过的应用"，原创 idea + 没融资 + 非 YC 背景的组合风险更高。@thepatwalls 转推 · 2026-05-10 08:50 BJT · 👍477 🔖445

---

## 延伸资源库

### 播客 / 视频 / 访谈

- @nathanbarry 提到 Nathan Barry Show 邀请 @wguidara、@bcanlis 谈 hospitality；本期推文未披露具体单集编号 [时间戳未获取]，可在 YouTube 搜 "Nathan Barry Show" 找完整集
- @indie_maker_fox 1 小时 TanStarter 模板部署视频教程：https://youtu.be/5tfid3SIq00（带字幕）

### 图书 / 课程

- 本期无新书推荐。@lxfater 引用 @easychen 的中文开源电子书《一人企业方法论》第二版（github.com/easychen/opc-methodology），适合非技术副业（自媒体、电商、数字商品）人群

### 链接汇总（按类别分组，已经过推文原文核对）

工具类
- TanStarter 模板（Cloudflare Workers + TanStack）：https://tanstarter.dev / 文档：https://context7.com/websites/tanstarter_dev
- Omarchy 3.8 release：https://github.com/basecamp/omarchy/releases/tag/v3.8.0
- bearlyai/openade：https://github.com/bearlyai/openade

报道类
- Apple Intelligence 集体诉讼 $250M 和解：https://www.nytimes.com/2026/05/05/technology/apple-intelligence-lawsuit-settlement.html（NYT 报道，本期被 @TrungTPhan 引用）

GitHub 类
- 一人企业方法论 v2：https://github.com/easychen/opc-methodology
- bearlyai/openade：https://github.com/bearlyai/openade
- lidangzzz/goal-driven：https://github.com/lidangzzz/goal-driven/

播客 / 视频类
- TanStarter 部署教程：https://youtu.be/5tfid3SIq00

二级市场类
- $1.5M ARR 数字营销代理 listing：https://app.acquire.com/startup/vBBHg0v9vzMnLvUZgGj1SKtzO4u1/pbKPkKhq2roeKAIQRvfO/

---

## 行动建议（按档位分组）

档位 A（内容创作者）
- 今天 30 分钟：把 @op7418 / @dotey 提到的 GPT Image 2 + 水墨风格 PPT prompt 模板，套上自己专题领域的关键词，做一个公众号 / 小红书图文专属模板，本周观察是否减少出图时间 30% 以上

档位 B（独立开发者）
- 今天 30 分钟：把金矿 1 的三段 prompt 贴进 `CLAUDE.md` / `AGENTS.md`，下次开长会话观察"模型变笨"是否更晚出现
- 本周：盘点自己 #3、#4、#5 个产品是否任意一个稳定 $200/m，是 → 列入 Trust MRR / Acquire.com 候选清单；不是 → 参考 @tibo_maker、@marclou 的失败 / 死亡产品节奏作参照，不要在第 3 个产品就停止

档位 C（工具集成者）
- 今天 30 分钟：把当前 n8n / Make / 自研 agent pipeline 中"主流程承担抓数据 + RAG + 文件操作"那部分剥离到 sub-flow，主流程只做调度——直接对应金矿 1 的 orchestrator 思路
- 本周：把至少一个客户交付从"按项目报价"改成"按月 retainer + 固定可交付物"试报价（参考金矿 3 的 93% 利润率代理结构）

档位 D（服务变现者）
- 本周：参照金矿 3 的 retainer 形态，把现有咨询 / 培训打包成"月固定金额 + 明确可量化交付物"试卖给 1-2 个老客户做 pilot，重点是把客户认知从"项目"切到"SLA"

---

## 避坑指南

- **把 starter_story 那条 "$77K/月 不看手机" 直接当方法论照抄**：内容主角是 @marclou，他的 $76K/m 来自 7 个产品组合 + 长期 Build in Public 的流量沉淀（marclou bio 公开），"上午不看手机"是结果不是因。从同样行为出发不会有同样结果
- **把 marclou 的 "$200/m → $1,250" 当作"做个 AI 小工具就能卖钱"**：micro-acquisition 6.25× MRR 倍数的大头是已有付费用户 + App Store 通过审核的开发者账号 + 已上架资产，不是产品本身有多贵
- **把 lxfater 的 4 条 prompt 贴上就以为完事**：这套办法的前提是"主上下文只做调度"，如果你贴完 prompt 还把抓数据 / 大段读文件 / 多文件搜索全堆给主对话，效果会打折——主上下文必须保持瘦身

---

## 本期情报评估

**信息密度**：正常偏低
24 小时 245 条推文中，实质收入 / 退出 / 工具发布信号集中在 3-4 条，timeline 大量被励志生活方式、政治、健康养生话题占据。

**趋势信号**：
"Codex / Claude Code 长会话上下文管理"成为本周持续高密度话题（@lxfater Codex 4-tip、@xiaohu HyperFrames vs Markdown、@vista8 Codex vs Claude 口碑、@LawrenceW_Zen 提到 Boris 的 /loop until 笑话），说明 vibe coder 群体已经从"模型选哪家"过渡到"长会话怎么不掉性能"——这是可商业化的细分痛点。

**横向对比**（本期两个收入数据点）：
- 路径 A — @marclou 多产品组合：7 个产品 ~$76K/m，最小那个 $200/m 直接挂出场退出。优点：每条产品线有独立退出选项；缺点：精力分散、单产品天花板低
- 路径 B — Acquire.com 上的 $1.5M ARR / 93% 利润率代理：业务集中度高、不依赖产品矩阵，单老板年入百万美金。优点：现金流极稳；缺点：天花板低且严重依赖创始人时间，无法离场
对一人公司来说，路径 B 更适合"找到适合自己长期做的小生态"，路径 A 更适合"产品折腾型"——本期数据本身没法判断哪条更优，但提示一个变量：是否需要随时离场。

**当日强信号数 vs 噪音比**：
3 条强信号 / 8-10 条励志金句类噪音（@SahilBloom、@blakeaburge、@thedankoe、@Codie_Sanchez、@thejustinwelsh、@AlexHormozi 当日多条均属此列）。噪音明显大于信号，但金矿质量足以覆盖，今日不属于信号枯竭日。

---

原始推文来源：@lxfater @marclou @agazdecki @indie_maker_fox @tibo_maker @dhh @op7418 @dotey @xiaohu @vista8 @runes_leo @starter_story @thepatwalls @cjzafir @nathanbarry @lidangzzz @LawrenceW_Zen @Shpigford @easychen @TrungTPhan
