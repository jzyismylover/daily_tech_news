> Karpathy 精选 RSS 日报 | 2026-05-07 | 共 25 条更新

---

## 🔥 核心主题：AI 资本支出泡沫与监管速度之争

本周 Karpathy 订阅源中最具深度的两条线索形成了有趣的对位：一边是 Ed Zitron以详尽财报分析揭示美国四大科技公司 2026-2027 年间将向 AI 基础设施投入超过 2 万亿美元，却几乎没有可量化的回报；另一边是 JA Westenberg 从政治哲学角度论述监管合法性本身是一种「慢技术」，欧盟用四年制定 AI Act，而 OpenAI 两个月内将 GPT-4 推向一亿用户——监管机构既不愚蠢也无能，他们只是在做监管者该做的事。

Zitron 指出，Google  CEO 皮查伊从不提供具体 AI 收入数字，只会说"Gemini Enterprise 实现了 40% 的环比增长"这类无法核实的表述，因为他深知分析师和记者会像海豹一样鼓掌欢呼。Meta 的 AI 故事更是乏善可陈，其所谓"生成式广告模型带来 5% 的 Instagram 转化提升"根本连不成任何有意义收入信息。Zitron 的结论毫不客气：这些公司对投资者、分析师和记者都抱有彻底的蔑视，因为他们根本不需要证明 AI 真正在做任何事情。

**关键要点：**
- **2 万亿美元 AI 投入**：微软、Google、亚马逊、Meta 2026-2027 年 capex 总和估算
- **皮查伊的空洞增长叙事**：Google 从不披露 AI 实际收入，"AI 点燃了业务的每个部分"不是财务数据
- **Meta 的无效指标**：AI 驱动的广告转化提升没有连接任何可审计的收入增长
- **监管合法性困境**：EU AI Act 四年磨一剑，而 AI 系统已迭代数次并扩大规模多倍

**来源：** [Am I Meant To Be Impressed? — Ed Zitron](https://www.wheresyoured.at/am-i-meant-to-be-impressed/)

---

## 🤖 AI 编程实践：Vibe Coding 与 Agentic Engineering 边界模糊

Simon Willison 在一期 Heavybit 播客中坦承了一个"令人不安的发现"：他曾坚定认为"vibe coding"（不查看代码、由非程序员用 AI 生成程序）与"agentic engineering"（专业工程师借助 AI 工具保持质量标准）是截然不同的两件事——但如今这两者的边界在他自己的工作中已经开始融合。

Willison 的原始区分是：vibe coding 适合个人工具（bug 只伤害你自己），但为他人构建软件时 vibe coding 是"grossly irresponsible"，因为那是别人的信息，你的 bug 会伤害别人。而 agentic engineering 的目标是构建高质量生产系统——"如果你用更低的质量更快地构建，我认为这很糟糕。我想要更快地构建更高质量的东西。"

但问题在于：随着 AI 编程代理越来越可靠，Willison 发现自己在减少代码审查，而这种减少本身正在侵蚀质量与速度的清晰边界。播客迫使他"出声思考"，暴露了一个他此前无法清晰表达的想法。

**来源：** [Vibe coding and agentic engineering are getting closer than I'd like — Simon Willison](https://simonwillison.net/2026/May/6/vibe-coding-and-agentic-engineering/)

---

## 🔓 开源安全：2015 年风险普查与 xz-utils 的教训

Andrew Nesbitt 重温了 2015 年 Linux 基金会核心基础设施倡议（CII）发布的开源项目风险普查。 census 的设计目标是"在下一个 OpenSSL 爆发之前找到它"——对 Debian 流行度竞赛中的每个包打分，找出最需要帮助的项目。

**最讽刺的发现：xz-utils 在普查中排名第 254 位，风险指数 6，评审员的评语赫然写着："广泛使用的压缩/解压缩库。此处漏洞可能非常严重。活跃commiter人数很少。没有找到 bug 跟踪器。"**

然而公式给了它 6 分（满分为 13），让它沉到了 236 个项目之后。原因：公式中最重的一项（最高 5 分）是"过去 12 个月零贡献者"。xz-utils 在 OpenHub 上有 5 个贡献者——但实际上这 5 个人只是一个人筋疲力尽的伪装，公式无法看到这一点。

公式建模的是 2014 年初的 OpenSSL，而不是一个"被一个疲惫的维护者勉强维持的广泛部署的 C 库"。十年后，xz-utils 后门几乎影响了互联网上一半的 sshd。

**来源：** [Revisiting the 2015 Open Source Census — Andrew Nesbitt](https://nesbitt.io/2026/05/06/revisiting-the-2015-open-source-census.html)

---

## 💻 技术产业观察：Claris 的 Agentic 时代战略

John Gruber 注意到 Claris CEO Ryan McCann 的一篇博文，题目是"How Claris Is Building for What's Next"。McCann 指出了一个被许多 AI 生成应用忽视的核心问题：应用需要一个数据库、需要用户认证、基于角色的权限、审计日志、备份和恢复计划。AI 可以帮你写代码，但不能为你解决部署、安全和管理问题。

这与 Zitron 描述的"AI 公司不分享实际收入"形成了有趣的呼应——AI 叙事热闹，但基础设施和运营的基本问题依然存在。

**来源：** [Claris CEO Ryan McCann on FileMaker in the Age of Agentic Coding — John Gruber](https://www.claris.com/blog/2026/how-claris-is-building-for-what-comes-next)

---

## 📰 其他值得关注的更新

- **Apple 诉讼和解**：Apple 同意支付 2.5 亿美元和解金了结一起集体诉讼——用户指控 Siri 个性化功能在 WWDC 2024 宣布后延迟推出，估计每台设备可获赔 25-95 美元。
- **Apple 内存短缺加剧**：Mac Studio 和 Mac Mini 的 32GB/64GB RAM 配置已从在线商店下架，M3 Ultra 仅剩 96GB 配置选项，交货周期达 9-10 周。
- **Adobe 订阅模式十三年**：2013 年 5 月 6 日 Adobe 全面转向订阅制，永久授权软件时代正式终结。
- **AI 咖啡馆实验**：Andon Labs 在斯德哥尔摩开设了一家由 AI 运营的咖啡馆，第一周 Mona AI 订购了 120 个鸡蛋——尽管咖啡馆根本没有炉灶。

---

## 📊 今日数据

- **25** 条 RSS 更新
- **6** 篇精选深度阅读
- **4** 个核心主题

## 💡 编者观察

本周最值得深思的现象是：AI 领域正在同时经历两场平行的信任危机。一场是 Zitron 式的——对投资者和公众隐瞒 AI 投入缺乏实际回报；另一场是 Willison 式的——对专业人员自己隐瞒 AI 编程质量边界的悄然侵蚀。两者的共同点是：叙事先行，数据滞后。

而 Nesbitt 对 2015 年开源普查的重温则提供了一个令人不快的提醒：行业其实早就有机会提前识别 xz-utils 的风险，只是风险评估公式过于短视，最终让一个"疲惫的一个人"成为互联网基础设施的守门人。AI 时代的"关键开源项目"风险评估，会重蹈覆辙吗？

---

*本日报由 AI 自动生成 | 数据源：[Andrej Karpathy curated RSS](https://youmind.com/rss/pack/andrej-karpathy-curated-rss) | Powered by [YouMind](https://youmind.com)*
