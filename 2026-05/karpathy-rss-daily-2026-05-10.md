> Karpathy 精选 RSS 日报 | 2026-05-10 | 共 144 条更新

---

## 🔥 核心主题：AI 经济学危机与开源健康评分的系统性谬误

两条来自本周的重磅报道，从截然不同的角度揭示了 AI 行业当前的深层矛盾：**表面繁荣下的经济不可持续性**，以及**技术圈对"什么是健康开源项目"的衡量标准正在严重误导产业政策**。

**关键要点：**
- **xAI 将整个 Colossus 1 数据中心（300MW）转租给 Anthropic**，xAI 本身几乎不需要自用算力——这意味着除 OpenAI 和 Anthropic 之外，真正的大规模 AI 算力需求买家几乎不存在
- **Anthropic 在 8 个月内融资 108 亿美元**，但仍需额外承担每年 25–35 亿美元的 Colossus 1 租金；其商业模式本质上是**算力套利 + 风险资本补贴的循环**
- Ed Zitron 指出，整个 AI 经济的 **7480 亿美元收入 backlog** 依赖 Anthropic 和 OpenAI 两家公司——而这两家公司都无法靠自身营收存活
- 与此同时，Andrew Nesbitt 揭示：现有所有衡量"关键开源项目健康度"的模型，都存在**系统性盲点**——把"缺失数据"当"零值"处理（curl 实际年安装量约 200 亿次，但 GitHub API 只记录了约 1 万次），导致大量关键基础设施工具被排除在评估体系之外
- Mozilla 在 Code w/ Claude 活动上宣布：通过 Claude Mythos（AI 辅助漏洞发现），Firefox **月度修复安全漏洞数从 20–30 个跃升至 423 个**（2025 年 4 月数据），但批评者指出 LLM 生成的安全报告大部分是看似正确但实则错误的"slop"

**来源：**
- [Simon Willison — xAI/Anthropic deal 分析](https://simonwillison.net/2026/May/7/xai-anthropic/)
- [Ed Zitron — AI's Circular Psychosis](https://www.wheresyoured.at/premium-ais-circular-psychosis/)
- [Andrew Nesbitt — The Mismeasure of Open Source](https://nesbitt.io/2026/05/09/the-mismeasure-of-open-source.html)
- [Simon Willison — Behind the Scenes Hardening Firefox with Claude Mythos Preview](https://simonwillison.net/2026/May/7/firefox-claude-mythos/)

---

## 🤖 AI 工具实践：HTML 正在挑战 Markdown 作为 LLM 输出格式的地位

Simon Willison 撰文指出，他多年来默认要求 LLM 输出 Markdown（因为 GPT-4 时代的 8192 token 限制使 Markdown 更加 token 高效），但 Thariq Shihipar（Anthropic Claude Code 团队成员）的一篇深度文章促使他重新思考这一选择。

HTML 作为 LLM 输出格式的优势包括：**可嵌入 SVG 图表、交互式小部件、页面内导航**，以及借助 CSS/JS 实现更丰富的信息呈现方式。Simon 用 GPT-5.5 生成了一个解释 Linux 安全漏洞 copy.fail 的交互式 HTML 页面，效果远超纯文本。他正计划在更多场景中尝试要求 LLM 输出结构化 HTML 而非 Markdown。

与此同时，Simon Willison 的 llm-gemini 插件发布 0.31 版，Gemini 3.1 Flash-Lite 正式脱离预览阶段。

**来源：**
- [Simon Willison — The Unreasonable Effectiveness of HTML](https://simonwillison.net/2026/May/8/unreasonable-effectiveness-of-html/)
- [Simon Willison — llm-gemini 0.31](https://simonwillison.net/2026/May/7/llm-gemini/)
- [Simon Willison — GitHub Repo Stats 工具](https://simonwillison.net/2026/May/7/github-repo-stats/)

---

## 🏛️ 政策与批评：左翼阵营内部对 AI 的分歧加剧

Gary Marcus 持续追踪"AI 反弹"现象：QuitGPT 运动正在集结力量，他预测 AI 反对情绪将成为 **2028 年美国总统大选的关键议题**——而这一预测似乎正在应验。

与此同时，seangoedecke.com 发表了**明确的左翼亲 AI 立场文章**，从disability（残障）、慢性病医疗倡导、阶级与"代码切换"（code-switching）三个角度，提出 AI 实际上有助于减少不平等：
- **残障权益**：LLM 驱动的自动字幕、语音控制、邮件语气转换，正实质性改变残障人士的数字生活
- **慢性病群体**：面临医疗体制惯性的患者借助 LLM 做文献研究、撰写有力陈述，弥补医生知识盲点
- **阶级与专业语言**：LLM 帮助非精英背景人群写出符合"专业权威"语域的文档（ Patrick McKenzie 描述的那种"危险的专业人士"沟通模式），降低被体制机器忽视的概率

Westenberg. 则从监管角度指出：欧盟用四年制定 AI Act，而 OpenAI 在两个月内将 GPT-4 推向一亿用户——**监管速度永远赶不上技术迭代**，规则最终只能约束早已迭代多轮的旧系统。

**来源：**
- [Gary Marcus — The Growing AI Backlash](https://garymarcus.substack.com/p/the-growing-ai-backlash)
- [seangoedecke.com — The Left-Wing Case for AI](https://seangoedecke.com/the-left-wing-case-for-ai/)
- [Westenberg. — The War Between Fast and Legitimate Is Here](https://www.joanwestenberg.com/the-war-between-fast-and-legitimate-is-here/)

---

## 🔧 开发者实践：AI 代码生成的质量困局与包管理安全

Andrew Nesbitt 的"Semver 塔罗牌"系列续作《Madame Semver Will See You Now》以寓言形式描述了一个开源维护者的典型困境：某天"安全扫描报告"出现——12 项发现中 11 项其实是维护者自身记录在案的行为，被重新包装为漏洞，第 12 项才是真实问题，但同样问题会在十一月再次出现。讽刺的是，**行业正在用 LLM 生成此类"安全扫描"**——Nesbitt 另一篇文章详细剖析了当前所有开源健康评分模型的根本性错误：把"无法收集"当成"零"。

John Gruber 报道了 Y Combinator 持有 OpenAI 约 0.6% 股份的披露——在 Paul Graham 公开质疑 Sam Altman 可信度时，这一关联值得注意。

**来源：**
- [Andrew Nesbitt — Madame Semver Will See You Now](https://nesbitt.io/2026/05/10/madame-semver-will-see-you-now.html)
- [Andrew Nesbitt — The Mismeasure of Open Source](https://nesbitt.io/2026/05/09/the-mismeasure-of-open-source.html)
- [John Gruber — Y Combinator's Stake in OpenAI](https://daringfireball.net/2026/05/y_combinators_stake_in_openai)

---

## 📰 其他值得注意

- **Construction Physics** 刊出阅读列表（5月9日），涵盖"室内数据中心"、纸板军用无人机、Brightline 可能破产等话题；另一篇"How Long Do We Wait for New Inventions?"探讨发明的时间尺度
- **Cory Doctorow** 的 Pluralistic 继续每日追踪科技政策：Trump 寻找"goreable ox"（可宰杀的牛，比喻白宫寻找替罪羊）、Enron 式审计丑闻等
- **Ibrahim Diallo** 反思 AI 辅助写作带来的问题：引用自己用 AI 写的文章时发现内容已面目全非
- **Terence Eden** 发表书评《The Names》（Florence Knapp），叙事结构精妙但充斥家庭暴力内容，阅读体验"不享受"
- **The Old New Thing** 继续 Windows 内部机制科普；The Silicon Underground 回溯 Dell 收购 Alienware（2006年5月8日）、Intel Pentium II 发布（1997年5月7日）等历史节点

---

## 📊 今日数据

- **144** 条 RSS 更新（过去 48 小时）
- **10+** 篇精选深度阅读
- **5** 个核心主题

## 💡 编者观察

本周最值得深思的对比来自两篇文章：**Ed Zitron 用最简单的逻辑（"Anthropic 没有钱付账单，因为 Anthropic 花了太多钱"）** 拆解了价值 7480 亿美元的 AI 经济循环；而 **Andrew Nesbitt 则揭示了更深层的认知问题——我们甚至不知道如何正确衡量开源生态系统的健康度**。

这两条线索都指向同一个结论：AI 行业当前的增长模式建立在多层未验证的假设之上——假设有真实的市场需求，假设开源生态可被量化，假设监管会滞后但最终有效。在 Simon Willison 等人持续产出高质量一手分析的同时，大量信息源（Cory Doctorow 的每日链接、Ed Zitron 的商业拆解、Gary Marcus 的批评追踪）正在构建一套反主流叙事的知识体系。

---

*本日报由 AI 自动生成 | 数据源：[Andrej Karpathy curated RSS](https://youmind.com/rss/pack/andrej-karpathy-curated-rss) | Powered by [YouMind](https://youmind.com)*
