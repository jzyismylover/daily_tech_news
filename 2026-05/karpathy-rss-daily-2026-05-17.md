> Karpathy 精选 RSS 日报 | 2026-05-17 | 共 17 条更新

---

## 🔥 核心主题：AI 不是产品，是技术——对生成式 AI 泡沫的集体反思

过去 48 小时，Karpathy 精选 RSS 源中出现了一个引人注目的主题汇聚：多位作者从不同角度对"AI 万能论"发起了冷静审视。

Gary Marcus 发表重磅文章《生成式 AI 的幻觉》（The Illusion of Generative AI），尖锐批评了行业对超大规模扩展（hyperscaling）的疯狂押注。他在文中引用了三场近期深度访谈，分别涉及与 Brian Greene 的科学对话、Web Summit 上关于超大规模扩展风险的主题演讲，以及在 Bug Bash 2026 大会上关于神经符号 AI 和世界模型必要性的炉边谈话。Marcus 的核心论点一如既往：LLM 的根本认知缺陷无法通过单纯扩大规模来解决，软件验证在 LLM 时代比以往任何时候都更重要。

与此同时，John Gruber 在 Daring Fireball 发表了《AI 是技术，不是产品》（AI Is Technology, Not a Product），直接回应 Steven Levy 在 Wired 上呼吁"Apple 下一任 CEO 需要推出杀手级 AI 产品"的言论。Gruber 认为，Levy 的观点陷入了 AI 炒作的陷阱——正如 iPod 不是为了卖 MP3 文件，而是为了卖音乐体验，Apple 从不"交付技术"，而是交付产品和体验。他尤其嘲讽了"AI 代理会自动叫好车等你走出餐厅"的愿景，称其为"纯粹的狂热幻想"。

Sean Goedecke 作为资深工程师的务实视角则为这场讨论增添了技术落地的维度。他在《2026 年我如何使用 LLM》中指出，AI 代理在过去一年确实取得了质的飞跃——从"偶尔试试"变成"每个变更都先让代理做"——但他也坦承自己仍然比 AI 更擅长调试复杂问题，上周一个棘手 bug 花了十四个 AI 会话才解决。

**关键要点：**
- **Gary Marcus**：超大规模扩展是"疯狂的赌注"，行业需要神经符号 AI 和世界模型
- **John Gruber**：Apple 不需要追赶每一波技术浪潮，AI 是基础设施而非独立产品
- **Sean Goedecke**：AI 代理已从"辅助工具"进化为"初级执行者"，但仍需大量人工审查

**来源：** [Marcus on AI](https://garymarcus.substack.com/p/the-illusion-of-generative-ai-the) | [Daring Fireball](https://daringfireball.net/2026/05/ai_is_technology_not_a_product) | [seangoedecke.com](https://seangoedecke.com/how-i-use-llms-in-2026/)

---

## 🧬 DeepSeek-V4-Flash 与 LLM 引导技术的复兴

Sean Goedecke 的另一篇文章《DeepSeek-V4-Flash 意味着 LLM 引导再次变得有趣》深入探讨了一个技术前沿话题。文章以 antirez 最新项目 DwarfStar 4 为引子——这是一个精简版 llama.cpp，专门为运行 DeepSeek-V4-Flash 而生。

Goedecke 解释了"引导"（steering）的核心思想：通过直接操控模型推理过程中的激活值来引导输出，而非修改提示词。他介绍了两种方法：朴素的"对比法"（给同一组 prompt 加上不同后缀，测量激活差异作为引导向量）和 Anthropic 的稀疏自编码器方法（训练辅助模型提取特征）。

文章指出了引导技术的尴尬处境：大厂觉得它"不够高端"（直接训练模型更直接），普通用户又无法接触（需要模型权重），使得它成为了一个"中产阶级"研究方向。但 DeepSeek-V4-Flash 作为一个足够强的本地模型，可能改变这一局面——antirez 已经在 DwarfStar 4 中将引导作为一等公民内置。

**来源：** [seangoedecke.com](https://seangoedecke.com/steering-vectors/)

---

## 📰 学术界 AI 乱象：ArXiv 对 AI 灌水论文亮红灯

404 Media 报道，学术预印本平台 ArXiv 将对提交明显 AI 生成内容的作者实施一年禁令。ArXiv 计算机科学分部主席 Thomas Dietterich 在 X 上公布了新规，列举了"不可辩驳的证据"，包括：

- 幻觉引用（hallucinated references）
- LLM 的自言自语（如"以下是 200 字摘要；您需要修改吗？"）
- 占位数据未替换（如"表中数据为示例，请填入真实实验数据"）

禁令期为一年，之后的投稿必须先获得同行评审期刊的认可才能提交至 ArXiv。这一政策变化反映了学术界对 AI 生成内容泛滥的日益增长的焦虑。

**来源：** [404 Media](https://www.404media.co/new-arxiv-rules-ai-generated-papers-ban/)

---

## 🏛️ 英国政府请走 Palantir：主权技术的胜利

Terence Eden 在博客中详细分析了英国住房、社区和地方政府部（MHCLG）如何退出与 Palantir 的合同，并自行重建了"乌克兰之家"（Homes for Ukraine）数据系统。英国政府在博客中轻描淡写地写道"退出了与供应商的合同"，并强调新系统每年为 MHCLG 节省数百万英镑运行成本。

国家审计署 2023 年的报告曾指出，Palantir 的原始系统因绕过了常规采购审查流程而存在诸多问题，包括重复数据显示混乱、地方政府不知如何使用主数据系统等。MHCLG 最终用开源、自主控制的内部系统取而代之。

Eden 将此视为"主权技术"的胜利：虽然不是对抗 Palantir 的第一场战役，但他希望 MHCLG 的做法能带动更多部门跟进。

**来源：** [Terence Eden's Blog](https://shkspr.mobi/blog/2026/05/uk-government-kicks-out-palantir/)

---

## 🔧 OpenAI 重大重组：Brockman 正式掌舵产品线

WIRED 报道，OpenAI 周五告知员工将进行组织重组，核心变化包括：

- **Greg Brockman** 正式接管产品战略（此前为代理）
- **ChatGPT 和 Codex 将合并**为统一产品体验
- **Thibault Sottiaux**（Codex 负责人）将领导核心产品和平台团队
- **Nick Turley**（ChatGPT 负责人）转为企业产品方向
- **Ashley Alexander**（前 Instagram VP）接管消费者产品部门

Brockman 在内部备忘录中表示，公司正在"整合产品力量，以最大专注度迈向代理化未来"。OpenAI 还在开发一个"超级应用"，旨在将 ChatGPT、Codex 和 Atlas 浏览器融合为统一桌面应用。此次重组被解读为 OpenAI 为 IPO 做准备、应对 Anthropic（编程领域）和 Google（消费者聊天机器人）竞争压力的举措。

**来源：** [WIRED](https://www.wired.com/story/openai-reorg-greg-brockman-product/)

---

## 🦞 Simon Willison 的 OpenClaw 改名史：从 Warelay 到龙虾

Simon Willison 在 PyCon US 闪电演讲前分享了 OpenClaw 的命名演变史。这个 WhatsApp AI 网关项目在 Git 历史中经历了 6 个名字：

> Warelay → CLAWDIS → CLAWDBOT → Clawdbot → Moltbot → 🦞 OpenClaw

从 2025 年 11 月的"WhatsApp Relay CLI (Twilio)"到如今的"Personal AI Assistant"，项目定位也从简单的 WhatsApp 中继演变为完整的个人 AI 助手。Willison 用自己编写的 first_line_history.py 工具从 README 的 Git 历史中提取了完整的改名时间线。

**来源：** [Simon Willison's Weblog](https://simonwillison.net/2026/May/16/openclaw-names/)

---

## 📊 今日数据

- **17** 条 RSS 更新（2026-05-16 至 2026-05-17）
- **9** 篇深度文章已阅读
- **6** 个核心主题：AI 反思、LLM 引导、学术 AI 乱象、英国主权技术、OpenAI 重组、开源工具

## 💡 编者观察

本期日报呈现出一个有趣的格局：**AI 领域的"成人声音"正在回归**。Gary Marcus 的技术批评、Gruber 的产品哲学、Sean Goedecke 的工程师务实——三者从不同维度构成了对 AI 炒作的温和纠偏。与此同时，ArXiv 对 AI 灌水的铁腕政策和英国政府请走 Palantir 的案例，说明"负责任的 AI 使用"正在从口号变为行动。

值得关注的是，DeepSeek-V4-Flash 和 antirez 的 DwarfStar 4 项目可能重新激活"本地模型+引导"的技术路线——在 API 调用费用和隐私问题日益突出的背景下，这或许是一条被低估的发展路径。

OpenAI 的组织重组则暗示着行业正在从"谁的模型更大"的竞争转向"谁能更好地整合产品"的竞争。Brockman 将 ChatGPT 和 Codex 合并的决策，本质上是承认了"对话"和"编程代理"的边界正在消融。

---

*本日报由 AI 自动生成 | 数据源：[Andrej Karpathy curated RSS](https://youmind.com/rss/pack/andrej-karpathy-curated-rss) | Powered by [YouMind](https://youmind.com)*
