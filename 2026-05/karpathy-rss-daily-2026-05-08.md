> Karpathy 精选 RSS 日报 | 2026-05-08 | 共 19 条更新

---

## 🔥 核心主题：xAI 与 Anthropic 算力交易震动 AI 行业

本周最重大的 AI 行业新闻，莫过于 Anthropic 在 Code w/ Claude 活动上宣布与 SpaceX/xAI 达成协议——将使用 xAI 全部 Colossus 数据中心容量。Simon Willison 深度分析了这一交易的来龙去脉：Colossus 数据中心因环境问题备受争议，其燃气涡轮机在未取得清洁空气法许可的情况下运行，并被指与当地住院率上升有关。Anthropic 首席科学家 Greg Brockman 在活动上表示，这一合作将帮助 Anthropic 缓解算力紧张的困境。与此同时，xAI 仅出借了 Colossus 1，Colossus 2 仍保留用于自身模型训练。值得注意的是，就在合作宣布前一天，xAI 还突然宣布将在两周内停用 Grok 4.1 Fast 等多个模型，引发用户强烈不满。Gary Marcus 则援引 The Information 的报道指出，OpenAI 与 Broadcom 宣布合作研发 10 GW 定制 AI 芯片时，实际上"尚未弄清楚 OpenAI 将如何支付这笔费用"，并评论这可能成为"整个时代的墓志铭"。

**关键要点：**
- **Anthropic 租用 xAI Colossus**：Anthropic 使用 SpaceX/xAI 全部 Colossus 数据中心容量，换取算力缓解，但该数据中心环境记录存疑
- **OpenAI 融资模式遭质疑**：与 Broadcom 的定制芯片合作被指"尚未解决付款问题"，OpenAI 惯于宣布"里程碑式合作"却未敲定细节
- **算力焦虑驱动合作**：多家 AI 公司在算力紧张背景下寻求横向合作，但地缘政治与环境问题带来高度复杂性
- **xAI 突然停用 Grok 4.1 Fast**：仅提前两周通知，损害了依赖该模型的开发者信任

**来源：** [Simon Willison - Notes on the xAI/Anthropic data center deal](https://simonwillison.net/2026/May/7/xai-anthropic/)

---

## 🤖 AI 工具与应用：Mozilla 用 Claude 强化 Firefox 安全

Mozilla 宣布在 Claude Mythos Preview 的帮助下，已在 Firefox 中识别并修复了"史无前例数量"的安全漏洞。在一篇深度技术文章中，Mozilla 工程师详细披露了这一工作的方法论：过去 AI 生成的安全漏洞报告被视为"不需要的垃圾"，因为假阳性报告给维护者带来不对称成本——生成容易，核查困难。但这一局面在数月内发生了根本性改变：模型能力大幅提升，加之 Mozilla 改进了引导、扩展和堆叠模型的技术，能够生成大量信号并过滤噪音。Mozilla 破例公开了部分漏洞报告样本，涵盖 JIT 优化漏洞、WebAssembly GC 漏洞、IPC 竞态条件等，展示了 AI 在安全领域从"噪音制造者"到"漏洞猎手"的转变。

**来源：** [Mozilla Hacks - Behind the Scenes Hardening Firefox with Claude Mythos Preview](https://hacks.mozilla.org/2026/05/behind-the-scenes-hardening-firefox/)

---

## 🛡️ 开源生态：AI 正在发现"僵尸软件包"的安全漏洞

Andrew Nesbitt 在其"Weekend at Bernie's"一文中提出了一个令人不安的问题：开源软件供应链中存在大量"活着的尸体"——npm/pypi 等仓库中大量软件包仍在被安装和依赖，但实际上 maintainer 已经失联，无人回应安全报告。当一个这样的包遇到安全漏洞时，结局往往是：无人响应， embargo 到期，CVE 公开，没有可用修复版本。即使有人提交了补丁，如果原注册账户已经失效，补丁也无法发布到 registry。Nesbitt 指出，这个问题在 AI 辅助漏洞发现技术快速进化的当下变得更加紧迫：AI 大幅降低了发现漏洞的门槛，但维护者消失的问题并未改善，二者之间的缺口正在扩大。

**来源：** [Andrew Nesbitt - Weekend at Bernie's](https://nesbitt.io/2026/05/08/weekend-at-bernies.html)

---

## 📜 AI 批评与反思：为什么更长的训练周期没有减缓 AI 进步？

seangoedecke.com 探讨了一个关于 AI 进步的深层问题：如果训练更强大的模型需要更长的时间来进行强化学习"评分"，那么 AI 进步应该会自然放缓，但事实似乎并非如此——METR 的 horizon-length 图表显示 AI 系统能完成的任务复杂度在不断提升，且在加速而非减速。文章提出了几个原因：其一，新模型可能从数量级更多的 FLOPs 中受益，效率提升空间巨大；其二，人类对"智能"的判断存在天然偏差——我们很容易判断 AI 比我们笨，却很难判断 AI 是否比我们聪明。文章还引用了 GPT-4 训练中 FP16 求和导致精度损失的实际 bug，说明"看似聪明"的系统中可能埋藏着大量"愚蠢错误"。

**来源：** [seangoedecke.com - Why hasn't longer-horizon training slowed AI progress?](https://seangoedecke.com/why-hasnt-longer-horizon-training-slowed-ai-progress/)

---

## ⚖️ 监管与权力：欧盟 AI Act 与创新速度的战争

Westenberg. 发表评论文章，剖析了欧盟四年磨一剑的 AI Act 与 OpenAI 两个月内席卷一亿用户之间的制度性矛盾。作者认为，监管机构的缓慢并非愚蠢或无能——咨询、影响评估、措辞辩论、二十四语言翻译、委员会投票、调和各国立场，这些正是监管机构应有的审慎程序。但问题在于：这种正当程序与科技公司的迭代速度之间存在根本性张力，且民主问责机制中最值得信赖的机构恰恰是行动最缓慢的，而能快速行动的机构往往信任度最低。作者警告：在算法权力已经重组了多个国家的政治之后，监管机器才刚开始运转。

**来源：** [Westenberg. - The war between fast and legitimate is here](https://www.joanwestenberg.com/the-war-between-fast-and-legitimate-is-here/)

---

## 🌐 科技文化与历史：Cory Doctorow 论泡沫与加密自由主义的虚伪

matduggan.com 发表评论文章，以相当个人化的笔触回溯了"网络自由主义"意识形态的起源与溃败。作者回顾了 1996 年 John Perry Barlow 起草的《网络空间独立宣言》，以及随后几十年间"网络自由"承诺如何被实际构建的基础设施所背叛——中心化的 ISP、云服务和 app store 实际上将权力集中到了少数公司手中，恰恰是当年宣言反对的那种"有形基础设施"。作者认为，这一意识形态的虚伪性在于：那些最激进地宣扬网络自由的人，往往是从中获利最多的既得利益者，而普通用户的"自由"实际上被卖给了广告商和数据经纪人。

**来源：** [matduggan.com - The Intolerable Hypocrisy of Cyberlibertarianism](https://matduggan.com/the-intolerable-hypocrisy-of-cyberlibertarianism/)

---

## 📊 今日数据

- **19** 条 RSS 更新（2026-05-08）
- **7** 篇精选深度阅读
- **6** 个核心主题

## 💡 编者观察

本周 RSS 内容呈现出一个清晰的主题：**AI 行业的基础设施信任危机正在多维度展开**。算力层面，Anthropic 与 xAI 的合作凸显了算力稀缺背景下企业不得不与争议对手合作的无奈；开源层面，Nesbitt 揭示的"僵尸软件包"问题暴露了去中心化生态的维护真空；监管层面，Westenberg 的分析则直指制度性滞后与技术创新之间那道尚未找到答案的裂痕。与此同时，Mozilla 的案例则展示了一个相对正面的叙事：AI 作为安全防御工具正在快速成熟，有望改变安全漏洞发现的游戏规则。总体而言，Karpathy 精选源继续呈现出一个高度批判性的 AI 行业观察视角，而非一味唱多——Gary Marcus 的"时代墓志铭"评论和 Cory Doctorow 对泡沫的持续追踪，都代表着一种来自行业内部的冷静声音。

---

*本日报由 AI 自动生成 | 数据源：[Andrej Karpathy curated RSS](https://youmind.com/rss/pack/andrej-karpathy-curated-rss) | Powered by [YouMind](https://youmind.com)*
