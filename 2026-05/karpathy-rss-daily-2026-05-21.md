>> Karpathy 精选 RSS 日报 | 2026-05-21 | 共 330 条更新（近3天）

---

## 🔥 核心主题：Google I/O 2026 — AI 全线出击

Google I/O 2026 于5月19日举行，本次发布会几乎完全围绕 AI 展开，Gemini 家族迎来重大更新。最大亮点是全新的 **Gemini Omni** 模型系列——与 Veo 仅支持文生视频不同，Gemini Omni 能从文本、照片、视频、音频等多种输入生成视频内容，Google 宣称其最终目标是"万物输入，万物输出"。与此同时，**Gemini Spark** 作为 Google 版"OpenClaw"正式亮相，这是一个全天候运行的个人 AI Agent，运行在 Google Cloud 隔离虚拟机中，可连接 Gmail、Docs、Sheets、Slides 等 Google Workspace 应用，以及 Canva、Instacart 等第三方服务，并计划支持 macOS 本地文件访问。

值得特别关注的是 **Gemini CLI 向 Antigravity CLI 的切换**：Google 宣布 Apache 2.0 开源的 Gemini CLI 工具将于6月18日停止与其 AI 订阅计划兼容，被新的闭源 Antigravity CLI 取代——开源社区对此反应强烈。

**关键要点：**
- **Gemini 3.5 Flash** 今日起成为 Gemini App 和 Search AI Mode 的默认模型，速度显著提升，Agent 能力增强
- **Gemini Omni** 支持任意组合输入（文本/图片/音频/视频）生成视频，开创多模态新范式
- **Gemini Spark** 是 Google 的首个个人 AI Agent 产品，主打隐私隔离（每任务独立 ephemeral VM）+ 企业级 DLP 保护，但 prompt injection 风险仍存疑
- **Android vibe-coding**：用户现在可以用自然语言提示在 AI Studio 中" vibe code "完整 Android 应用，并直接安装到手机或发布到 Play Store
- **Project Aura** 智能眼镜是与 Xreal 合作的新版本，显示 Google 在 AR 硬件上的持续投入
- Simon Willison 评价：大量功能仍为"即将推出"状态，他更倾向于等正式上线后再评

**来源：** [The Verge — The 13 biggest announcements at Google I/O 2026](https://www.theverge.com/tech/933415/google-io-2026-biggest-announcements-ai-gemini)

---

## 🤖 AI 研究与批评：o3 GeoGuessr 提示工程神话破灭

AI 圈曾广泛流传一个说法： Kelsey Piper 发现 o3 在 GeoGuessr（根据照片猜测地理位置）任务上表现惊人，而她的"秘诀"在于一条精心设计的提示词——通过不断让模型反思错误并改进提示而积累的工程技巧。这一说法催生了"提示词工程可以解锁全新能力"的流行观念。

但 Sean Goedecke 决定用数据验证这一假设。他从 Wikimedia Commons、Geograph Britain and Ireland 和 iNaturalist 抓取200张图片构建基准测试，分别用默认提示和 Kelsey 的 GeoGuessr 提示运行 o3，结果令人意外：

| 提示方式 | 中位误差 (km) | 均值误差 (km) | ≤25km 准确率 |
|----------|--------------|--------------|-------------|
| 默认提示 | 83.2 | 440.7 | 58/200 |
| GeoGuessr 提示 | 102.3 | 481.9 | 59/200 |

**默认提示反而表现更好**，精妙的提示词工程并未带来统计学意义上的提升。这说明：1）o3 的能力很可能是在预训练中就已经具备的，而非提示词解锁的；2）我们对当前模型有哪些未被发现的隐藏能力仍然知之甚少。

**来源：** [seangoedecke.com — The famous o3 "GeoGuessr" prompt did not work](https://seangoedecke.com/the-o3-geoguessr-prompt-did-not-work/)

---

## ⚠️ AI 反思与政策：Gary Marcus — AI 会成为科技行业的"越战"吗？

Gary Marcus 在 Substack 发表重磅文章，将生成式 AI 与越战进行类比，引发广泛讨论。他指出：AI 行业目前正以"史无前例的速度烧钱"，投资已达数万亿美元，却仍在与幻觉、不可靠性和对齐问题作斗争。Jason Calacanis 已将 AI 称为"Z 世代的越战"——年轻人普遍不想与之产生任何关系，三位毕业典礼演讲嘉宾仅因提及 AI 就遭到嘘声。

然而 Marcus 看到了更深层的类比：越战失败的根源之一是"指标问题"——美国用尸体数量和占领领土来衡量进展，而非真正的目标达成。AI 行业同样面临 ROI（投资回报率）困境，大多数试点研究都缺乏实际回报。

更值得注意的政治动向：Marcus 在1月曾预测"到2026年底特朗普将开始远离他2025年激进的亲 AI 行业政策"，如今这一预测正在加速兑现——特朗普已开始认真考虑由 Michelle Rempel Garner 和 Marcus 本人在三年前提出的"类 FDA 的 AI 预审机制"。如果公众压力足够大，AI 监管格局可能迎来根本性转变。

**来源：** [Gary Marcus — Could generative AI turn out to be the tech industry's Vietnam?](https://garymarcus.substack.com/p/could-generative-ai-could-turn-out)

---

## 💡 Simon Willison — Tokens/Second 真实体验工具 & Gemini CLI 末日

Simon Willison 推荐了一款由 Mike Veerman 制作的 HTML 应用，用于模拟 LLM token 输出速度（从5/秒到800/秒），帮助用户直观理解"30 tokens/秒"究竟意味着什么——是流畅对话还是令人抓狂的卡顿。

此外，Willison 记录了 Google I/O 的另一个重要细节：**Gemini CLI 开源工具将在6月18日被关闭**，被新的闭源 Antigravity CLI 取代。这对依赖开源 Gemini CLI 的开发者社区是一个打击。

在 AI 价格方面，Google 宣布 Gemini 3.5 Flash 虽然更贵，但 Google 计划将其用于所有场景——这意味着成本上升的压力将持续传导给用户。

**来源：** [Simon Willison — How fast is 10 tokens per second really?](https://simonwillison.net/2026/May/20/tokens-per-second/) | [Google I/O, Gemini Spark, Antigravity](https://simonwillison.net/2026/May/20/google-io/)

---

## 🌟 人生与工程：没有人注定伟大

Westenberg 发表评论文章，以德摩斯梯尼（Demosthenes）的故事开篇——这位古希腊最伟大的演说家早年登台失败，被观众轰下台，但他没有放弃，而是挖了一个地下书房，嘴里含满鹅卵石对着大海练习发音，最终成为激励雅典对抗马其顿腓力二世的精神领袖。

文章的核心观点：所谓"天才注定伟大"的故事是一种自我安慰的幻觉。Mozart 的父亲在其5岁作曲之前已对其进行十几年每天不间断的训练；Anders Ericsson 的研究表明，无论先天禀赋如何，杰出人物的共同特征是"起步早、投入时间多"；Ted Williams 挥棒直到手掌皮肤脱落，Eliud Kipchoge 40多岁时仍每天高强度训练。没有人被赋予伟大，伟大来自反复失败后的持续投入。

这与 AI 行业的某种"速成文化"形成了有趣的对照——人们期待用一条精妙的提示词瞬间解锁模型潜能，却不愿承认真正的能力来自持久的、默默无闻的深耕。

**来源：** [Westenberg — Nobody is destined for greatness.](https://www.joanwestenberg.com/nobody-is-destined-for-greatness/)

---

## 📊 今日数据

- **330** 条 RSS 更新（近3天）
- **5** 篇精选深度阅读
- **4** 个核心主题（Google I/O、o3 提示工程、AI 政策反思、个人成长哲学）

## 💡 编者观察

本周 Karpathy 精选 RSS 的最显著主题是 **Google 的全面 AI 化**——从模型（Gemini 3.5/Omni/Spark）到工具链（Android Studio → AI Studio vibe-coding）再到硬件（Project Aura），Google 正在将 AI 嵌入其整个产品矩阵。然而，Gary Marcus 的文章和 o3 GeoGuessr 实验共同揭示了一个深层矛盾：行业在营销上过度承诺，却在核心可靠性（幻觉、ROI）上尚未兑现。

值得关注的是，Marcus 预测的"特朗普 AI 政策转向"比预期来得更快——如果 AI 公众反对声浪持续上升，监管压力可能重塑行业轨迹，而非技术本身。与此同时，Simon Willison 持续追踪 AI 工具的实际可用性，是少数保持批判距离的技术观察者。

---

*本日报由 AI 自动生成 | 数据源：[Andrej Karpathy curated RSS](https://youmind.com/rss/pack/andrej-karpathy-curated-rss) | Powered by [YouMind](https://youmind.com)*
