> Karpathy 精选 RSS 日报 | 2026-05-18 | 共 47 条更新

---

## 🔥 核心主题：软件工程师的身份危机——AI 时代谁在重新定义我们的职业？

Ibrahim Diallo 发表了一篇引发广泛讨论的文章《别再叫自己软件工程师了，你是 AI 赋能工程师》。文章以 LinkedIn 上人人争相改头衔的现象为切入点，犀利地指出：当整个公司的市场部都换上了"AI 优先"的标签，真正用 Claude、Cursor、Codex 写代码的工程师们反而成了"旧时代"的残余。Diallo 回顾了 Patrick McKenzie 当年说服大家从"程序员"升级为"软件工程师"的历史，认为当下的核心问题不是换一个新头衔，而是回到那个根本——**工作的成果比名号更重要**。

与此呼应的是 Sean Goedecke 的《"Just Say No"工程师是零利率时代的产物》（ZIRP = Zero Interest Rate Phenomenon）。文章探讨了在宽松融资环境下养成的"拒绝型工程师"文化——那些以说"不"为荣、以抵抗需求为专业精神的工程师，在 AI 浪潮和资本收紧的双重压力下正在失去立足之地。

**关键要点：**
- **LinkedIn 上的"AI 头衔通胀"正在模糊真正的技术能力边界**——人人都是"AI 工程师"，但真正理解底层原理的人并没有变多
- **工程师的核心价值仍在于解决问题的能力，而非工具标签**——Diallo 引用 McKenzie 的经典建议：沟通、人脉、理解业务比精通框架更有长期价值
- **"拒绝型工程文化"是特定经济周期的产物**——零利率时代已过，务实协作比"说不"更有竞争力

**来源：** [Ibrahim Diallo](https://idiallo.com/blog/you-are-an-ai-enabled-engineer-now?src=feed) | [seangoedecke.com](https://seangoedecke.com/the-just-say-no-engineer-was-a-zirp-phenomenon/)

---

## 🧠 AI 技术深度：LLM 引导向量（Steering Vectors）的现实与幻灭

Sean Goedecke 的另一篇重磅文章探讨了 DeepSeek-V4-Flash 发布后重新引起关注的 LLM 引导技术。引导向量的核心思路是直接操纵模型内部的激活值来控制行为，听起来比写 prompt 更"底层"、更强大。但 Goedecke 的结论相当冷静：

- **大部分引导效果可以被更简单的 prompt 替代**——"让模型话多一点"不如直接说"请详细回答"
- **真正有用的引导场景（比如提升"智能"）可能根本不可行**——因为"智能"这个概念太复杂，引导向量可能需要覆盖整个模型权重
- **开放权重模型的兴起让实验成为可能**——之前只有大厂内部能做，现在社区可以开始探索
- **值得注意的是**：antirez（Redis 作者）指出引导技术已经在被用于移除模型的安全限制（即"去审查化"），而且可能比 LoRA 微调对模型能力的损伤更小

此外，Sean Goedecke 还有一篇《2026 年我作为 Staff Engineer 如何使用 LLMs》，从一线资深工程师的视角分享了 LLM 在日常工作中的实际用法，是了解 AI 工具真实落地情况的重要参考。

**来源：** [seangoedecke.com - Steering Vectors](https://seangoedecke.com/steering-vectors/) | [seangoedecke.com - LLMs in 2026](https://seangoedecke.com/how-i-use-llms-in-2026/)

---

## 🏛️ AI 不是产品——Gruber 与 Gary Marcus 的双重冷水

John Gruber 以标志性的犀利风格发表《AI 是技术，不是产品》，回应 Steven Levy 在 Wired 上"苹果下一任 CEO 必须推出杀手级 AI 产品"的论调。Gruber 引用了新任 CEO John Ternus 的回应："我们从不想交付一项技术，我们想交付令人惊叹的产品、功能和体验。"他的核心论点是：

- iPod 的核心不是 MP3 文件，是音乐；iPhone 的核心不是触屏，是移动体验
- AI 威胁颠覆整个 iPhone 生态系统？更可能的是改变，而非替代
- "云"概念的炒作前车之鉴——说得越宏大，实际意义越模糊

Gary Marcus 则继续他的 AI 怀疑论路线，《生成式 AI 的幻觉、超大规模投资的疯狂、以及世界模型和神经符号 AI 的案例》一文收录了三篇精彩访谈，从学术角度论证当前 LLM 范式的局限性。

**来源：** [Daring Fireball](https://daringfireball.net/2026/05/ai_is_technology_not_a_product) | [Gary Marcus on Substack](https://garymarcus.substack.com/p/the-illusion-of-generative-ai-the)

---

## 📋 开源与治理：英国政府数字服务局公开批评 NHS 关闭开源仓库

Simon Willison 和 Terence Eden 持续追踪 NHS 因 Project Glasswing 安全漏洞报告而关闭其开源代码仓库的争议。本周迎来重大升级：英国政府数字服务局（GDS）发布了《公共部门中的 AI、开放代码和漏洞风险》报告，核心立场是：

> **"保持默认开放。将一切设为私有会增加额外的交付和政策成本，并可能减少复用和审查。开放应继续作为默认姿态，关闭应谨慎且有意识地使用。"**

GDS 没有点名 NHS，但 Terence Eden 解读这是"一次重大升级"——在英国公务员体系中，这相当于被叫去"开会但不提供茶点"（frosty discussion）。NHS 的决定被视为违背了政府的开放原则。

**来源：** [Simon Willison's Weblog](https://simonwillison.net/2026/May/17/gds-weighs-in/) | [Terence Eden's Blog](https://shkspr.mobi/blog/2026/05/gds-weighs-in-on-the-nhss-decision-to-retreat-from-open-source/)

---

## 📚 学术界：ArXiv 严打 AI 灌水论文，违者禁投一年

404 Media 报道，ArXiv 计算机科学板块主席 Thomas Dietterich 宣布了新的处罚政策：如果论文提交包含"确凿证据"表明作者没有检查 LLM 生成的内容，将被禁止投稿一年，之后的投稿必须先被同行评审期刊接受才能再投。

确凿证据包括：幻觉引用、LLM 元评论残留（如"这是一个200字的摘要；您需要我修改吗？"），以及表格中标注"此数据为示例，请填入真实实验数据"等明显未处理的痕迹。这是学术界对 AI 灌水的最强硬回应之一。

**来源：** [404 Media](https://www.404media.co/new-arxiv-rules-ai-generated-papers-ban/) via [Daring Fireball](https://daringfireball.net/2026/05/arxiv_to_ban_researchers_for_a_year_if_they_submit_ai_slop)

---

## 🏢 OpenAI 组织变动：Greg Brockman 正式接管产品

Wired 报道，OpenAI 宣布联合创始人 Greg Brockman 正式接管产品战略（此前为临时任命，因 AGI 部署 CEO Fidji Simo 休病假而代理）。Gruber 引用了自己上个月的评论："OpenAI 的工作环境似乎不仅是压倒性的，简直是折磨人的。"这再次引发了对 OpenAI 组织稳定性的讨论。

**来源：** [Wired](https://www.wired.com/story/openai-reorg-greg-brockman-product/) via [Daring Fireball](https://daringfireball.net/2026/05/greg_brockman_officially_takes_control)

---

## 📊 今日数据

- **47** 条 RSS 更新（最近 3 天）
- **8** 篇精选深度阅读
- **6** 个核心主题

## 💡 编者观察

今天的 Karpathy 精选呈现出一个有趣的张力：AI 正在深刻地改变软件行业的每一个角落——从 LinkedIn 上的职业标签到学术出版的质量标准，从 LLM 底层技术的探索到对 AI 泡沫的冷静反思。但最引人注目的不是 AI 本身的能力，而是**人类在面对这波技术浪潮时的身份焦虑**：工程师该叫什么？CEO 该做什么？学术论文该由谁写？

Gruber 的那句话可能是今天的最佳注脚："AI 是技术，不是产品。"技术从来不需要被"发布"——它需要被**融入**。正如 iPod 不是关于 MP3 文件，iPhone 不是关于触屏，AI 的真正价值不在于它本身，而在于它如何让我们更好地做我们已经在做的事情。

---

*本日报由 AI 自动生成 | 数据源：[Andrej Karpathy curated RSS](https://youmind.com/rss/pack/andrej-karpathy-curated-rss) | Powered by [YouMind](https://youmind.com)*
