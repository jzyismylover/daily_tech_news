> Karpathy 精选 RSS 日报 | 2026年5月14日 | 共 18 条更新

---

## 🔥 核心主题：AI、权力与独裁的范式

Cory Doctorow 在 Pluralistic 发表长文，探讨亿万富翁的唯我主义、独裁者的唯我主义与 AI 之间的深层联系。文章开篇引用 Granny Weatherwax 的名言——"罪就是把人当东西对待"——以此揭示权力如何将人异化为统计数据。Doctorow 论证了社交媒体平台如何将用户降格为"参与度最大化"的工具，而 AI 的出现进一步加剧了这种趋势。

文章的核心论点是：当权者越强大，其他人就越不真实——这与 AGI（通用人工智能）的愿景形成了危险的共振。Doctorow 认为，科技巨头们的"AGI 梦"本质上是一种极端的唯我主义表现，因为它假设人类智能可以被完全复制和控制，正如独裁者假设社会可以被完全掌控一样。

**关键要点：**
- **权力导致唯我主义**：拥有越多权力，他人就越不真实——这与社交媒体平台将用户视为"数据点"的逻辑一致
- **AI 加剧了这种趋势**：AGI 的叙事本质上是将人类智能"物化"，与独裁思维同构
- **平台经济的困境**：用户对朋友的真实情感 vs. 平台对"参与度"的追求，AI slop 正在取代真实内容

**来源：** [Pluralistic](https://pluralistic.net/2026/05/13/vibe-governance/)

---

## 🤖 AI 工具与开发实践

Simon Willison 今天发布了三条更新。最重要的是他宣布 Datasette 项目开通了官方博客——他使用 OpenAI Codex 桌面版来构建这个博客，并称赞该工具的 Markdown 会话转录导出功能是他"一直想要的"。这展示了 AI 辅助编程工具在实际项目中的成熟应用。

同时，Willison 发布了一个 CSP（内容安全策略）白名单实验工具，使用 GPT-5.5 xhigh 在 Codex 桌面版中构建。该工具允许在 CSP 保护的沙盒 iframe 中运行应用，并通过自定义 `fetch()` 拦截 CSP 错误，提示用户将域名添加到白名单。

Boris Mann 的一句话引用也引发了思考："'11 个 AI 代理'作为短语毫无意义。如果我说'我有 11 个电子表格'或'我有 11 个浏览器标签'来做我的工作，意思基本一样。"这反映了当前 AI 代理概念的模糊性。

**来源：** [Simon Willison's Weblog](https://simonwillison.net/2026/May/13/welcome-to-the-datasette-blog/)

---

## 🔐 网络安全：AI 幻觉与数据泄露

两个有趣的网络安全故事今天同时出现。Troy Hunt 宣布巴哈马政府成为第 44 个加入 Have I Been Pwned 免费政府服务的国家——巴哈马国家计算机事件响应团队（CIRT-BS）现在可以监控政府域名的数据泄露情况。这展示了全球网络安全基础设施的持续扩展。

另一个故事更发人深省：Ibrahim Diallo 报道了传奇人物 Cliff Stoll（《杜鹃蛋》作者、克莱因瓶商人）的经历——Facebook 上一篇帖子声称他已于 2024 年去世，而 AI 大模型从网上抓取了这个虚假信息并将其当作事实输出，甚至维基百科也引用了这个 Facebook 帖子作为他去世的来源。Stoll 本人不得不在 Hacker News 上发帖澄清："我还没死呢。"这是 AI 幻觉如何通过互联网信息污染产生现实后果的绝佳案例。

**来源：** [Troy Hunt](https://www.troyhunt.com/welcoming-the-bahamian-government-to-have-i-been-pwned/) / [Ibrahim Diallo](https://idiallo.com/byte-size/its-funny-because-its-true?src=feed)

---

## 🖥️ 软件工程与开发者文化

John Gruber 详细评测了 Nextpad++——一个将开源 Notepad++ 移植到 Mac 的新项目。开发者 Andrey Letov 在短短几周内完成了这个移植，使用了"多智能体 AI 开发工作流"。Gruber 对此评价颇为辛辣："Nextpad++ 给人的感觉就像一个狂热的梦——像是纳粹赢得二战后 Mac 应用会变成的样子。"但他也承认，这种"一个人 + AI"的开发模式确实令人印象深刻。

Raymond Chen（The Old New Thing）则分享了一个经典的 Windows 内部调试故事：当用户通过 Win+Space 切换键盘布局时，程序挂起。原因是后台线程创建了窗口但没有泵送消息，导致输入语言更改请求无法完成。这个故事再次证明了"如果你创建了窗口，就必须泵送消息"这条黄金法则。

Terence Eden 发布了一个简洁的 SVG 迷你图（sparkline）教程，展示了如何用几行 PHP 代码生成轻量级数据可视化图表。

**来源：** [Daring Fireball](https://daringfireball.net/2026/05/nextpad) / [The Old New Thing](https://devblogs.microsoft.com/oldnewthing/20260513-00/?p=112318) / [Terence Eden's Blog](https://shkspr.mobi/blog/2026/05/stupidly-simple-svg-sparklines/)

---

## 📊 开源生态与太空数据中心

Andrew Nesbitt 分享了一项来自慕尼黑工业大学的 arXiv 预印本研究，该研究构建了 Python 依赖图中维护变更传播的模型，覆盖了 718,750 个 PyPI 包和 200 万条依赖边。研究对比了三种支持机制——Tidelift、GitHub Sponsors 和 ecosyste.ms Python 基金——发现 ecosyste.ms 的包选择效率最高：仅 97 个包就覆盖了 25.9% 的总模型改进影响和 38.0% 的总模型回归影响。Nesbitt 谦虚地指出，这是独立第三方的外部验证，他并未参与测试设计。

Sean Goedecke 则对"太空 AI 数据中心"的热门话题进行了深入分析。虽然太空真空环境使得热传导（原子碰撞和流体对流）无法工作，但辐射散热在太空中实际上更容易——一个遮光散热器可以排放大量热量。真正的挑战在于需要部署前所未有的大规模散热板，以及发射成本和维护问题。文章指出，Musk 提出这个想法更多是为了提升个人品牌和公司估值，而非真正可行的工程方案。

**来源：** [Andrew Nesbitt](https://nesbitt.io/2026/05/13/showing-our-work.html) / [Sean Goedecke](https://seangoedecke.com/space-ai-datacenters-do-not-have-a-cooling-problem/)

---

## 💼 媒体行业：BuzzFeed 的 Byron Allen 时代

Ernie Smith（Tedium）详细分析了 Byron Allen 收购 BuzzFeed 的交易。Allen 是一位传奇的电视商业模式"套利者"，擅长最大化困境资产的价值——从 Stephen Colbert 即将空出的时段到现在的 BuzzFeed。Jonah Peretti 将留任 BuzzFeed AI 总裁，Smith 对此评论道："希望'AI'在这里只是'发挥创造力'的简写。"文章指出 BuzzFeed 作为"病毒式传播实验"是巨大的成功，但作为公司已经日薄西山——而 Allen 的介入恰恰证明了 BuzzFeed 衰落的程度。

**来源：** [Tedium](https://feed.tedium.co/link/15204/17340934/buzzfeed-byron-allen-analysis)

---

## 📊 今日数据

- **18** 条 RSS 更新
- **11** 篇精选深度阅读
- **6** 个核心主题

## 💡 编者观察

今天的 Karpathy 精选呈现出一个有趣的张力：一方面，AI 工具正在以惊人的速度改变软件开发实践（Simon Willison 用 Codex 构建博客，Andrey Letov 用多智能体系统几周内完成 Notepad++ 移植）；另一方面，AI 的"唯我主义"本质正在被越来越多的人质疑（Doctorow 的长文、Boris Mann 的讽刺、Cliff Stoll 的 AI 幻觉事件）。

值得注意的是，今天有三篇来自 Simon Willison 的更新，他持续展示了如何将 AI 工具（GPT-5.5、Codex）融入日常工作流，而不是将其视为替代品。这与 Ibrahim Diallo 的文章形成了有趣的对比——当"vibe coders"声称软件工程师已经过时时，真正的工作仍然需要深厚的技术理解和判断力。

---

*本日报由 AI 自动生成 | 数据源：[Andrej Karpathy curated RSS](https://youmind.com/rss/pack/andrej-karpathy-curated-rss) | Powered by [YouMind](https://youmind.com)*
