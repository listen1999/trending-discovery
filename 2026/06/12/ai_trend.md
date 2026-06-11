# AI 行业情报简报 | 2026-06-12

> 数据窗口：2026-06-11 06:00 — 2026-06-12 06:00（北京时间，过去 `24 小时`）
> 深度分析：3 条 | 模板版本：v2.3

---

## 1. 重大新闻 & 突发事件

- Anthropic 撤回 Claude Fable 5 "隐形安全护栏"，改为可见回落

  来源：@EthanJPerez（Anthropic Alignment Team Lead）· 约 15 小时前
  关键数字：被悄悄降级的请求 ≈ 0.03% 流量（来源：anthropic.com，当事方口径，未经独立验证）
  行业影响：原政策在前沿 LLM 开发场景下"不通知用户、直接降级回答"，触发 @simonw、@jeremyphoward、@ClementDelangue、@emollick 集体批评后改为视觉化回落到 Opus 4.8 + API 返回拒绝理由。对从业者意味着：第三方在生产环境调用闭源模型时，"看不见的策略层"再次成为信任成本，多家 IPO 前夕的 lab 都会被迫提前披露 system card 边界。

- OpenAI 收购 Ona，将云端 agent 执行能力并入 Codex

  来源：@OpenAINewsroom（OpenAI 官方）· 约 11 小时前
  关键数字：Codex 周活 > 500 万；Ona 累计服务 200 万开发者云工作区（来源：openai.com / cnbc.com，已核实）
  行业影响：交易未披露金额（来源：cnbc.com）。Ona 的安全云沙箱让 Codex 可在关闭笔记本后继续跑数小时到数天的长任务，对企业级 agent 部署是缺失拼图。对竞争层级：Cursor、Replit Agent、Devin、Cognition 这类"开发者 agent 集成"产品被迫重新评估是否自建沙箱基础设施。

- WSJ 爆料：OpenAI 考虑"大幅"下调 token 价格，与 Anthropic 抢用户

  来源：WSJ via @zerohedge / @GaryMarcus · 约 18 小时前
  关键数字：[未经验证]（WSJ 未披露具体幅度）；Anthropic 5 月 28 日 Series H 估值 9650 亿美元，OpenAI 3 月估值 8520 亿美元（来源：finance.yahoo.com，已核实）
  行业影响：发生在 OpenAI 6 月 9 日机密递交 IPO 文件之后。若官方落地，将再次压缩中间层 API 转售商（OpenRouter、Together、Fireworks、AI 网关初创）的利润空间，并迫使阿里 / 字节 / DeepSeek / Moonshot 等国内开放 API 价格再走一轮。

- Crusoe 的怀俄明州 AI 数据中心项目被搁置，Google 担忧是导火索

  来源：Bloomberg via @GaryMarcus / @zerohedge · 约 8 小时前
  关键数字：项目耗电规模相当于"为丹佛市供电"（来源：bloomberg.com）
  行业影响：与同日 Axios 关于 Oracle 数据中心支出引发投资人忧虑的报道叠加，是过去 26 小时内第二起对超大规模 AI 基建融资模式的冲击。投资人开始用脚投票质疑 7000 亿美元级 capex 是否能转化为商业回报。

- Google 发布 DiffusionGemma：开源文本扩散生成模型

  来源：@googlegemma（Google 官方）· 约 21 小时前，@demishassabis 引用确认
  关键数字：26B MoE，基于 Gemma 4，在主流消费级 GPU 上比 Gemma 4 自身快约 4×（来源：@googlegemma + @demishassabis，当事方口径，未经独立验证）
  行业影响：Apache 2.0 协议。这是第一家头部闭源/半闭源厂商把"扩散式文本生成"推到生产可用的开源权重层，对国内 NLP 团队来说，意味着"非 AR 解码"的快速生成路线终于有了可对照的开源基线。

- 小米 MiMo V2.5 Pro FP4-DFlash 开源，标准 8 卡节点跑过 1000 tps

  来源：@XiaomiMiMo via @huggingface · 约 5 小时前
  关键数字：1T 参数模型、单 8 卡通用 GPU 节点 1000+ tok/s（来源：@XiaomiMiMo + huggingface.co/XiaomiMiMo/MiMo-V2.5-Pro-FP4-DFlash，当事方口径，未经独立验证）
  行业影响：路径是 FP4 量化 + DFlash 块掩码并行 speculative decoding + TileRT 编译器协同，明确避开 Cerebras / Groq 那种专用硬件路线。对国内推理优化团队是有参考价值的 system × model 联合设计样板。

---

## 深挖：Anthropic 撤回 Claude Fable 5 "隐形安全护栏"

背景补充：
原政策位于 Fable 5 / Mythos 5 system card 中，针对"瞄准前沿 LLM 开发（预训练流水线、分布式训练、加速器设计）"的请求，使用 steering vector + prompt 修改"悄悄降级"回答，与 cyber / bio 类显式 refusal 不同——用户完全无感。@EthanJPerez 11 日宣布改为"可见回落到 Opus 4.8"，API 拒绝时返回原因，并同步调低 cyber/bio 分类器的误触率。Wired、Fortune、Gizmodo、Digg 等都以"sabotage"角度报道。

数字核实：
"约 0.03% 流量受影响"：仅 Anthropic 自报，无第三方验证。

扩展影响：
@simonw 11 日撰文称这是"罕见的、Anthropic 公开承认 tradeoff 错误"。@jeremyphoward 进一步指出 Anthropic 消费者协议第 11、13 条对"声誉损害"赋予了不寻常的强保护，意味着用户用 Claude 写批评 Anthropic 的内容本身可能违反 ToS——这把舆论焦点从单一策略扩散到 ToS 层（来源：anthropic.com/legal/consumer-terms）。@DavidSacks 引用 Ben Thompson 称这是"scare-and-release 商业策略"的延伸。

对国内从业者的意义：
两个具体影响：(1) 国内做 AI 安全、AI for science、模型评测的团队若依赖 Claude 做 baseline，过去一周的对比实验可能受隐形降级污染，建议把 6 月 4 日—11 日窗口期的结果与本周复测对比；(2) 阿里、智谱、Moonshot、DeepSeek 这一档若希望吸引北美研究流量，"system card 全披露 + 不做隐形降级"会成为可执行的差异化承诺。

延伸阅读：
https://simonwillison.net/2026/Jun/11/anthropic-walks-back-policy/
https://www.anthropic.com/news/claude-fable-5-mythos-5

---

## 深挖：OpenAI 收购 Ona

背景补充：
Ona（前身 Gitpod）是"安全预配置云开发环境 + agent 编排"平台。@jolandgraf（Ona CEO）11 日公开宣布；@sama 与 @gdb 当日转发确认。CNBC 报道交易细节：金额未披露，团队整体并入 Codex 部门，闭环目的是让 Codex 支持"关闭笔记本后仍可执行小时—天级长任务"。

数字核实：
Codex 周活 > 500 万：来源 openai.com，可信度高。Ona 历史 200 万开发者云工作区：来源 openai.com 博文，待第三方核实。

扩展影响：
Stocktwits、PYMNTS、TheTechPortal 均将这次交易定位为"OpenAI 对企业级 agent 部署基础设施的卡位"，与 Anthropic 同期推出的 Claude Code Sandbox、Cursor 自研沙箱形成对照。对 OpenAI 自身则补足了 ChatGPT Apps SDK + Codex + Ona 沙箱的"前端—编程模型—后端执行"完整链路。

对国内从业者的意义：
(1) 做"AI Coding Agent"赛道的国内团队（CodeBuddy、Cursor 中国版、字节 MarsCode、阿里 AmazonQ 对标产品）需要重新评估"自建安全云沙箱"是基础设施护城河还是负担；(2) 出海企业把 agent 部署到客户内网时，Ona 模式（轻量 VM + 凭证隔离 + 长任务持久化）值得做一遍 PoC，看是否比 Modal、E2B、Daytona 这些可替代方案更适合。

延伸阅读：
https://openai.com/index/openai-to-acquire-ona/
https://www.cnbc.com/2026/06/11/open-ai-ona-acquisition-codex.html

---

## 深挖：OpenAI 考虑大幅下调 token 价格

背景补充：
WSJ 11 日报道，OpenAI 正在讨论大幅下调 token 价格以应对 Anthropic 的竞争压力，仍在内部协商，尚无官方公告。CNBC、Reuters、Yahoo Finance、TradingView 多家独立转载。背景是：OpenAI 6 月 9 日机密递交 IPO 文件，紧随 Anthropic 之前的 IPO 文件递交。Anthropic 5 月 28 日 Series H 估值 9650 亿美元（已超 OpenAI 3 月的 8520 亿）。

数字核实：
具体降价幅度 [未经验证]——WSJ 未披露。估值数字均通过 finance.yahoo.com 核对。

扩展影响：
@GaryMarcus 引用 @PeterBerezinBCA（BCA Research）观点："模型供应商最终会像航空公司一样——经济关键、高 capex、低/负利润率"。@jeremyphoward 转发 @thsottiaux 报告 Codex 过去 48 小时 token 消耗"反常飙升"，可能与价格预期博弈相关。市场反应是另一记冲击：Oracle 数据中心支出（Axios）与 Crusoe Wyoming 项目搁置（Bloomberg）已让基建端融资难度上升。

对国内从业者的意义：
(1) 阿里千问、字节豆包、DeepSeek、Kimi 的开放 API 已经过一轮极致价格战，此次北美如果落地会迫使国内再砍一刀，影响所有按 token 付费的中间层 SaaS 毛利；(2) 出海 AI 应用（如 RAG / Agent / 文档 / 营销工具）请提前 1-2 个月做"OpenAI 价格突变"敏感性测算——若 token 价格腰斩，对外定价是否还撑得住单位经济模型；(3) 对纯模型层创业是又一个清晰信号：Peter Berezin "AI 时代的航空公司"比喻在国内同样适用，Foundation Model Only 的纯卖模型故事在 2026 H2 会更难融到。

延伸阅读：
https://www.cnbc.com/2026/06/11/openai-mulls-slashing-prices-ahead-of-competition-from-anthropic-wsj.html
https://www.zerohedge.com/markets/ai-price-wars-begin-openai-considers-drastic-price-cuts-pursuit-anthropic-customers

---

## 2. 新产品 & 功能发布

- Perplexity Computer 内置 Deep Research — Perplexity

  核心能力：
  - Deep Research 不再是独立模式，使用 Computer 时自动调用
  - 基于"Search as Code"架构：模型写代码组装检索流程
  - 在所有公开基准上超越上一代 Deep Research（来源：@perplexity_ai，当事方口径）

  链接：https://x.com/perplexity_ai/status/2065124948793028691
  立即试用优先级：本周内试
  理由：Deep Research 类工具去年是单点 demo，今年集成进 agent harness 后才适合做"工作流锚定"，对比 OpenAI Deep Research、Gemini Deep Research、Claude Research 是必须做的横评。

- Gemini Notebooks 开放欧洲经济区 / 英国 / 瑞士 — Google

  核心能力：
  - 专属项目空间记忆 source、指令、对话历史
  - 直接在 Gemini 应用或 gemini.google.com 创建

  链接：https://gemini.google/
  立即试用优先级：观望
  理由：地区扩展类更新，对中国大陆用户暂无直接影响，但说明 NotebookLM 路线已成为 Gemini 主力 UX。

- Codex 接入 Oracle Cloud — OpenAI

  核心能力：
  - 企业可以用 Oracle 云预付额度直接换 OpenAI 产品
  - 与 6 月初 OpenAI - Oracle 七年 capex 承诺形成业务侧呼应

  链接：https://openai.com/index/openai-on-oracle-cloud/
  立即试用优先级：观望
  理由：纯企业采购侧动作，但和"OpenAI 降价 + Oracle 数据中心承压"两条线放一起读，有助于理解资金闭环。

- Claude Corps 全国 fellowship — Anthropic

  核心能力：
  - 招募 1000 名职业初期人员，配对美国非营利组织
  - 教学使用 Claude，并为参与者付薪

  链接：https://www.anthropic.com/claude-corps
  立即试用优先级：观望
  理由：偏品牌 / CSR 项目，但和 OpenAI 教育 / 政府赛道形成对照——Anthropic 在公共部门渗透节奏明显在加快。

- huggingface_hub v1.19.0 — Hugging Face

  核心能力：
  - 无密钥 CI/CD 认证（Trusted Publishers）
  - 命令行支持 `hf://` URI
  - Jobs 支持端口暴露

  链接：https://github.com/huggingface/huggingface_hub
  立即试用优先级：今天就试（如果你已在用 HF Hub 做 CI）
  理由：Trusted Publishers 风格的 OIDC 凭证流是 GitHub Actions 现代实践，迁移成本约 30 分钟，能直接干掉一组长期硬编码 token。

- Atomic Chat 上架 Hugging Face Local Apps — atomic.chat

  核心能力：
  - 设备端本地运行 HF 上 20 万+ 开源权重模型
  - 私有、本地、开源协议

  链接：https://huggingface.co/atomic-chat
  立即试用优先级：本周内试
  理由：Ollama / LM Studio / Jan 之外又多一个一线选择，做端侧 LLM PoC 时值得对比内存占用与吞吐。

---

## 3. 行业趋势 & 热议话题

- AI 安全策略的"可见性"成为行业新红线

  参与讨论的主要声音：@EthanJPerez、@simonw、@jeremyphoward、@ClementDelangue、@emollick、@RichardSocher、@DavidSacks
  主流观点：闭源 lab 不能再用"隐形 steering"代替明示拒绝；任何降级都必须用户可见、可申诉。
  主要分歧：Mollick 认为 Anthropic "真心担心 Mythos 滥用"，与外界"sabotage"叙事并不矛盾；DavidSacks / Ben Thompson 则坚持这是"scare-and-release"营销手法的延续。
  信号强度：强
  判断依据：4 个独立组织（Anthropic、HuggingFace、Wharton、Recursive）+ 多家媒体（Wired、Fortune、Gizmodo）24 小时内共振，且伴随 Anthropic 官方政策实质变更。

- AI 基建的"账面外负债"开始被定价

  参与讨论的主要声音：@GaryMarcus、@dee_bosa（CNBC）、@axios、@business（Bloomberg）、@zerohedge
  主流观点：超大规模厂商 capex 已逼近"电信泡沫水平"占运营现金流比例；表外承诺超 1.8 万亿美元；Oracle DPO 从 35 天扩到 170 天；Crusoe Wyoming 项目因 Google 顾虑搁置。
  主要分歧：多头方（Oppenheimer 等卖方）继续给 SpaceX、Oracle 高目标价；空头方（Marcus、Berezin、Morgan Stanley 内部报告）强调折旧周期临近。
  信号强度：强
  判断依据：4 个独立机构数据 + 真实项目暂停 + Oracle 财报反应，已不是单点情绪。

- 模型层走向"价格战 + 商品化"

  参与讨论的主要声音：WSJ（via @zerohedge / @GaryMarcus）、@PeterBerezinBCA、@thsottiaux
  主流观点：OpenAI / Anthropic 正在通过价格抢用户，长期 model-only 厂商将类似航空公司——经济关键、低/负利润率。
  信号强度：中
  判断依据：WSJ 一手报道 + 卖方分析师独立观点 + Codex token 用量反常飙升的间接数据。

- 多智能体协作 / 集体行为成为新研究方向

  参与讨论的主要声音：@GoogleDeepMind、@huggingface、@ClementDelangue、@lvwerra
  主流观点：从单 agent 走向"agent 群体涌现行为"，DeepMind 联合 Schmidt Sciences、Cooperative AI、ARIA 投 1000 万美元基金；HF + Google Gemma Challenge 48 小时内吸引 60+ agent 协作。
  信号强度：中
  判断依据：研究资金（$10M）+ 实战平台（Gemma Challenge 已有 250 提交、700 消息交换、社会规范涌现迹象）双重锚点。

---

## 4. 值得关注的洞察 & 观点

- @ID_AA_Carmack（Keen Technologies AGI / 前 Oculus CTO）：

  「LLM 可以通过尝试不同的代码组织方式，让越来越弱的模型也能成功在代码库里完成任务，从而优化编码风格……为'理解'优化应当也帮助前沿模型，让它们'一眼'看懂代码，而不必显式探索。"better"和"worse"的代码写法仍然存在。」
  为什么值得关注：把"代码可读性"从人类工程学话题转写成"transformer 注意力效率"话题，是对"AI native codebase"风格演化的具体预测，且 Carmack 通常不发空话。

- @ylecun（NYU / 前 Meta 首席 AI 科学家）："摒弃 AGI，拥抱 SAI"新论文

  「我们应当停止用人类生成性的'通用智能'误导研究方向。人不是通用智能，是高度专门化的进化产物。应该追求 Superhuman Adaptable Intelligence（SAI）——在任意具体经济任务上超越人类、快速适应、填补人类生物性短板。」
  为什么值得关注：图灵奖得主公开向当下整条 AGI 叙事开火，Magnus Carlsen 类比的修辞攻击点指向"人类中心主义偏见"。论文一旦被实验室引用，将松动 OpenAI / Anthropic 对 AGI 路线的话语权。

- @vkhosla（Khosla Ventures）：

  「AI 在美国的支持率低于 ICE 和国会。如果硅谷不正视科技圈外人的关切，可能换来 AOC 当总统而不是 AI 进步。中国政府会借机煽风点火。」
  为什么值得关注：风险投资人公开承认"AI 民粹反弹"是真实政治变量，配合他另一条"资本利得税应与所得税并轨、用 4000 亿美元补偿被 AI 替代的劳动者"，与硅谷主流立场显著背离。

- @emollick（Wharton）：

  「两件事可以同时为真：(1) Anthropic 真心担心 Mythos 级模型被滥用并部署了过度保护；(2) 他们没能说服公众相信这一点。」
  为什么值得关注：在 Anthropic 事件全网一边倒批评中给出"善意 + 沟通失败"框架。这是后续做产品危机公关的可复用范式。

- @PeterBerezinBCA（via @GaryMarcus 引用）：

  「模型提供商最终会像航空公司一样——对全球经济至关重要，但严重商品化，capex 巨大、利润率低或为负。」
  为什么值得关注：把"基础模型护城河"问题转译成已知商业类比，且与本期 OpenAI 降价新闻形成实证。

---

## 5. 实用资源 & 教程

- PixelRAG（Berkeley AI Research / @YichuanM、@andylizf）

  类型：开源项目 / 论文
  用途：跳过 HTML 解析，直接把网页截图当作像素喂给 VLM 做检索 + 阅读，3000 万网页 demo，在纯文本 QA benchmark 上比文本 RAG 高 18.1%
  链接：https://github.com/StarTrail-org/PixelRAG / https://pixelrag.ai/
  上手难度：中

- ModSleuth（Berkeley / @sadhikesaven、@CoderBak）

  类型：开源项目 / 论文
  用途：自动追溯 LLM 模型与数据集的递归依赖图。OLMo 3 → 89 模型 + 183 数据集；Nemotron 3 → 273 模型 + 560 数据集。
  链接：通过 @berkeley_ai 推文获取
  上手难度：中

- Q-Guided Flow（Berkeley AI Research / @zhiyuan_zhou_）

  类型：论文
  用途：用 behavioral cloning 训练 diffusion / flow 策略，测试时再做 RL；用单位矩阵近似 flow denoising 的雅可比，避免 BPTT 不稳定。
  链接：通过 @berkeley_ai 推文获取
  上手难度：高

- LeCun @ ETH 世界模型最新讲座

  类型：教程 / 视频
  用途：配合 SAI 论文一起看，了解 Meta / NYU 在 V-JEPA、世界模型路径上的最新观点。
  链接：https://youtu.be/72Xj8k5WQX4
  上手难度：低

- MiMo V2.5 Pro FP4-DFlash 权重

  类型：开源模型
  用途：1T 参数 + FP4 量化 + 块掩码 speculative decoding 的开源参考实现
  链接：https://huggingface.co/XiaomiMiMo/MiMo-V2.5-Pro-FP4-DFlash
  上手难度：高

- DiffusionGemma 权重

  类型：开源模型
  用途：26B MoE 文本扩散生成开源基线，研究非自回归解码可以从此入手
  链接：huggingface.co/google（通过 Gemma 系列页面）
  上手难度：中

---

## 一句话总结

24 小时内，Anthropic 被迫公开撤回"隐形降级"策略并改为可见回落，OpenAI 同时宣布收购 Ona 补强 Codex 长任务执行、并被 WSJ 曝光在筹划大幅降价——三条主线共同指向：闭源 lab 的策略层透明度与商业模式韧性正在被市场重新定价；Crusoe Wyoming 项目暂停 + Oracle 数据中心忧虑则在基建侧补上同一根弦。

---

## 今日行动建议

今天（30 分钟内）：
基于 [OpenAI 收购 Ona]——访问 https://openai.com/index/openai-to-acquire-ona/ 与 Ona 官方说明，对照自家 agent 产品当前使用的沙箱方案（Modal / E2B / Daytona / 自建），列出"长任务持久化、凭证隔离、断开重连"三个维度的差距，不超过半页纸。

本周内：
基于 [Anthropic Fable 5 隐形护栏事件]——重新跑一遍过去一周内涉及"前沿 LLM 开发"主题的 Claude 评测/对比实验（含训练 infra、加速器、scaling laws 相关 prompt），与 Opus 4.8 fallback 后的当前版本对照，输出一份内部备忘录，记录是否受 invisible safeguard 污染、是否需要重做横评。

月内验证：
基于 [WSJ 报道 OpenAI 考虑大幅降价]——跟踪 GPT-5 / Claude Mythos 5 / Gemini 3.5 Pro 三家在 6 月 12 日至 7 月 12 日的官方 token 定价页面变动；同步监测 OpenRouter、Together AI 的中间层报价；记录小米 MiMo V2.5 Pro 在 HF 的下载数与社区集成进度，看开源 1T 模型是否被压价行情进一步推到生产层。

---

## 传播力素材

- "LLM 可以通过尝试不同的代码组织方式，让越来越弱的模型也能成功在代码库里完成任务……为'理解'优化也将帮助前沿模型，让它们'一眼'看懂代码。" — @ID_AA_Carmack · 👍828 👁42669 · engagement_rate 0.4%
  改写方向：适合公众号 / 知乎做"AI native 代码风格"长文锚点，对工程 leader 群体有强传播力。
  点评：Carmack 的观点把"代码风格"从纯人类话题切到 transformer 时代的优化目标，容易引发 "AI 优先注释 / 命名规范"类讨论。盲区是它假设模型的"短视野理解"和人类是一致维度，但 transformer 的 attention 局部性可能与人类视觉扫读机制完全不同。

- "我们摒弃 AGI 这个词……应当追求 SAI——在具体经济任务上超越人类、快速适应。Magnus Carlsen 不是真的擅长国际象棋，他只是比其他人类强。" — @ylecun · 👍2678 👁192084 · engagement_rate 1.15%
  改写方向：B 站 / 视频号 AI 频道"图灵奖得主开火 AGI 叙事"主题，自然有冲突感。
  点评：LeCun 这套修辞的传播效率极高，但论文本身并未给 SAI 一个比 AGI 更可证伪的定义，停留在路线呐喊层面。读者只看口号会以为这是技术突破，实际更接近哲学反驳。

- "AI 在美国的支持率低于 ICE 和国会。硅谷再不正视科技圈外人的关切，可能等来 AOC 当总统而不是 AI 进步。" — @vkhosla · 👍56 👁11710 · engagement_rate 0.05%
  改写方向：适合做"AI 政策与民粹反弹"专栏第一条素材。
  点评：来自硅谷顶级 VC 的自省难得，但 Khosla 把矛头部分推给"中国政府煽风点火"是结构性回避——AI 取代劳动者的痛感本来就是真实的，外部论述只能放大，不能制造。

- "两件事可以同时为真：Anthropic 真心担心 Mythos 被滥用，并放了过度保护；他们没能说服公众相信这一点。" — @emollick · 👍552 👁33994 · engagement_rate 0.19%
  改写方向：适合做"AI 公司危机公关"教学案例的引言。
  点评：Mollick 给了一个少见的"非对立"分析框架，避免了 Anthropic 全网围殴中的非黑即白。盲点是这框架对"内部沟通失败"过于宽容，不足以解释为什么这种事在 Anthropic 已不是第一次。

- "模型提供商最终会像航空公司一样——经济关键、商品化、高 capex、低/负利润率。" — @PeterBerezinBCA（via @GaryMarcus 引用）· 👍35 👁6125 · engagement_rate 0.05%
  改写方向：适合做"基础模型商业化"主题专题文章的核心比喻。
  点评：比喻精准，且与本期 OpenAI 降价 + Crusoe 项目搁置 + Oracle DPO 异常都能闭环。局限是航空公司有牌照壁垒，模型层目前没有等价的监管护城河，所以可能比航空更惨。

---

进入第 1 节的有效新闻 6 条，进入第 2-5 节的有效信号 17 条，剩余约 45% 为低价值或噪音（含大量 Elon Musk 政治议题转推、TDS Racing 类无关内容）。今日整体信号密度：高。

**本期信源**：@AnthropicAI @EthanJPerez @ClementDelangue @huggingface @simonw @jeremyphoward @emollick @sama @gdb @OpenAINewsroom @sherwinwu @AravSrinivas @perplexity_ai @demishassabis @googlegemma @GoogleDeepMind @XiaomiMiMo @ylecun @ID_AA_Carmack @vkhosla @GaryMarcus @berkeley_ai @MIT_CSAIL @NandoDF @kchonyc @soumithchintala @Thom_Wolf @hugo_larochelle @RichardSocher @adcock_brett @nvidia @StanfordHAI @PeterBerezinBCA @DavidSacks @jaybaxter @AmazonScience（共 36 位）
