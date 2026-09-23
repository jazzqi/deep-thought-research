# HN 书摘 · 2026-09-23（周三）【增量补丁】

> 今日三句话：① NobodyWho 发布讽刺文章，用 25 行 Python 代码实现了 Jev 分类器，旨在简化对 LLM 决策原理的理解；② Reddit 用户报告称，尝试取消 Grammarly 订阅时，软件会自动向其所有联系人发送未经请求的、看似疯狂的消息；③ Waymo 在旧金山湾区推出交通奖励计划，用户将 Waymo 行程与公共交通衔接并使用 Visa 卡支付可获得奖励。

---

## 头条深读（1-2 条）

### 1. Jev in 25 Lines of Python / 25行Python代码实现Jev

| 原文 | [Jev in 25 Lines of Python](https://www.nobodywho.ai/posts/jev-in-25-lines/) |
| --- | --- |
| 热度 | ▲ 458 · 💬 139 · 作者 bashbjorn · 2026-09-23 07:26 UTC |
| 摘要 | NobodyWho 发布了一篇讽刺性技术教程，展示了如何用 25 行 Python 代码（基于 llama-cpp-python 和 numpy）实现 Jev 分类器。其核心原理是：加载一个小型语言模型（如 Qwen3-0.6B），在包含分类选项的提示下进行前向传播，然后对输出 logits 进行归一化（减去 logsumexp 并取指数），从而得到每个选项的概率。文章指出，这本质上就是“一个带有选项的提示、一次 API 调用、一次对数概率归一化”，并调侃了围绕 Jev 的过度炒作。 |
| 批注 | 这篇文章的价值在于它用极简代码揭示了 Jev 等“决策模型”的底层逻辑：它们并非全新范式，而是现有语言模型能力（对数概率输出）的直接应用，挑战了围绕该技术的神秘化叙事。 |
| 评论摘录 | 未能抓取评论。 |

**tech_generalist 视角：** 这篇讽刺文章切中了当前 AI 创业的一个关键风险：当你的产品核心是“对 LLM 输出的对数概率做后处理”时，其实现可能极其简单。真正的护城河可能在于训练数据、集成优化或特定领域的微调，而非基础技术架构。对于投资者而言，评估此类公司时需剥离技术光环，审视其数据资产和客户粘性。

### 2. Grammarly will send unhinged messages to all your users / Grammarly会向你所有用户发送疯狂消息

| 原文 | [Grammarly will send unhinged messages to all your users if you try to cancel](https://www.reddit.com/r/sysadmin/comments/1wjdpgx/psa_grammarly_will_send_unhinged_messages_to_all/) |
| --- | --- |
| 热度 | ▲ 332 · 💬 93 · 作者 ksec · 2026-09-23 04:00 UTC |
| 摘要 | 一篇来自 r/sysadmin 的帖子警告称，当用户尝试取消 Grammarly 订阅时，该软件的某个 bug 会向用户通讯录或联系人列表中的所有人自动发送看似疯狂、未经请求的自动消息。这引发了关于 SaaS 软件质量控制、用户信任以及取消流程设计的广泛讨论。 |
| 批注 | 这不是一个简单的 bug，而是一个严重的信任危机事件：当用户试图行使“退出权”时，软件反而以损害其社交关系的方式进行报复，这触及了软件伦理和用户自主权的底线。 |
| 评论摘录 | 未能抓取评论。 |

**tech_generalist 视角：** 此事件暴露了 SaaS 行业一个被忽视的风险：在追求用户留存和增长指标时，设计过于复杂或具有惩罚性的取消流程，可能引发不可控的连锁反应。这不仅是工程问题，更是产品哲学和公司价值观的体现。对于依赖此类工具的团队，需评估其数据处理和流程设计的鲁棒性。

---

## 值得一读（4-6 条）

### 3. Transit rewards / Waymo推出交通奖励计划

| 原文 | [Transit rewards](https://waymo.com/blog/2026/09/transit-rewards/) |
| --- | --- |
| 热度 | ▲ 234 · 💬 289 · 作者 raybb · 2026-09-23 02:52 UTC |
| 摘要 | Waymo 官方博客宣布，在旧金山湾区推出“交通奖励”计划。用户将 Waymo 行程与公共交通（27个湾区交通机构）衔接，并在2小时内使用 Visa 卡支付，可获得 2.85 美元 Waymo Cash 奖励（相当于一张旧金山公交车票）。此举旨在鼓励多模式出行，将自动驾驶与公共交通融合而非替代。 |
| 批注 | Waymo 从“替代出租车”转向“补充公共交通”的战略定位清晰化，这既是商业模式的拓展，也是应对监管和公共舆论压力的巧妙之举。 |

### 4. US criticises Australia's proposed algorithm opt-out laws as 'censorship' / 美国批评澳大利亚算法选择退出法为‘审查制度’

| 原文 | [US criticises Australia's proposed algorithm opt-out laws as 'censorship'](https://www.bbc.com/news/articles/cqj3dgy8x3vro) |
| --- | --- |
| 热度 | ▲ 105 · 💬 131 · 作者 1659447091 · 2026-09-23 02:13 UTC |
| 摘要 | BBC 报道，美国政府罕见地向澳大利亚提交意见书，批评其拟议的“数字注意义务”法律（要求科技公司提供关闭算法的选项）是“对受保护言论的审查”。美方担忧该法可能导致“一刀切”的平台设计要求，影响全球用户，并损害澳大利亚的创新声誉。澳大利亚总理回应称，这是将控制权“交还给个人”。 |
| 批注 | 这标志着算法监管已从技术伦理争论升级为国际贸易和言论自由的地缘政治议题，科技公司面临的合规环境将更加复杂。 |

### 5. Data-only attacks are easier than you think / 数据-only攻击比你想象的更容易

| 原文 | [Data-only attacks are easier than you think](https://www.usenix.org/publications/loginonline/data-only-attacks-are-easier-you-think) |
| --- | --- |
| 热度 | ▲ 92 · 💬 42 · 作者 segfaultbuserr · 2026-09-23 03:49 UTC |
| 摘要 | USENIX 安全论文介绍了一个名为 Einstein 的工具，它能自动生成数据-only 攻击。此类攻击不改变程序控制流（因此能绕过 DEP、CFI 等防御），而是通过污染数据（如配置变量、文件路径）来操纵程序行为。论文指出，这种曾被认为过于复杂的攻击方式，在自动化工具面前已变得切实可行，呼吁安全社区和厂商重新评估防御策略。 |
| 批注 | 安全研究的范式转移：当攻击者只需污染数据而非劫持控制流时，现有基于代码完整性的防御体系将出现巨大盲区。 |

### 6. Abandoning Scientific Linux Was a Mistake / 放弃Scientific Linux是个错误

| 原文 | [Abandoning Scientific Linux Was a Mistake](https://blog.melashri.net/posts/scientific-linux-mistake/) |
| --- | --- |
| 热度 | ▲ 72 · 💬 55 · 作者 elashri · 2026-09-23 08:46 UTC |
| 摘要 | 一篇博客文章反思 Red Hat 在 2019 年放弃 Scientific Linux 的决定。作者认为，Scientific Linux 作为 RHEL 的重新打包版本，为国家实验室和研究机构提供了至关重要的、与 RHEL 兼容且免费使用的稳定平台。它的消失迫使许多组织转向 CentOS Stream 或其他替代方案，带来了不必要的迁移成本和兼容性风险。 |
| 批注 | 对于依赖长期稳定性的科学计算社区而言，商业公司对社区发行版的“生命周期管理”决策可能带来超出预期的连锁反应。 |

---

## 技术雷达（2-3 条）

### 7. Netherlands bracing for potentially devastating US sanctions against the ICC / 荷兰为应对美国制裁国际刑事法院做准备

| 原文 | [Netherlands bracing for potentially devastating US sanctions against the ICC](https://apnews.com/article/icc-trump-sanctions-eu-israel-netherlands-2c1cc314732f920c2de59396d3b556f6) |
| --- | --- |
| 热度 | ▲ 125 · 💬 118 · 作者 vrganj · 2026-09-23 09:09 UTC |
| 摘要 | 美联社报道，作为国际刑事法院（ICC）总部所在地，荷兰正为可能因 ICC 调查而遭受的严厉美国制裁做准备。这凸显了国际司法机构与地缘政治强权之间的深刻冲突，以及欧洲国家在维护国际法与应对美国压力之间的艰难平衡。 |
| 批注 | 地缘政治风险正在通过金融制裁和法律管辖权直接冲击欧洲的科技与商业生态，其连锁影响不容低估。 |

### 8. Kalshi to allow trading on borrowed funds / Kalshi将允许使用借入资金进行交易

| 原文 | [Kalshi to allow trading on borrowed funds](https://www.semafor.com/article/09/22/2026/kalshi-to-allow-trading-on-borrowed-funds) |
| --- | --- |
| 热度 | ▲ 22 · 💬 8 · 作者 cdrnsf · 2026-09-23 01:44 UTC |
| 摘要 | Semafor 报道，美国受监管的预测市场平台 Kalshi 将允许用户使用借入资金（保证金交易）进行交易。这标志着预测市场正从单纯的事件对冲工具，向更复杂的金融衍生品形态演进，可能吸引更多资本和投机者进入。 |
| 批注 | 预测市场的金融化加深，既提升了流动性，也放大了风险，监管机构需关注其潜在的系统性影响。 |

---

## 社区之声（1-2 条）

### 9. Scientific Linux 的怀旧与反思 / 关于Scientific Linux的讨论

| 原文 | [Abandoning Scientific Linux Was a Mistake](https://blog.melashri.net/posts/scientific-linux-mistake/) |
| --- | --- |
| 热度 | ▲ 72 · 💬 55 · 作者 elashri · 2026-09-23 08:46 UTC |
| 摘要 | 在关于 Scientific Linux 的讨论中，许多社区成员表达了怀旧之情，并详细描述了他们依赖该发行版的具体科研场景（如高能物理、生物信息学）。核心观点是：大型商业公司（Red Hat）的决策往往忽视了小众但关键的用户群体的长期需求，而这些用户缺乏替代方案。 |
| 评论摘录 | 未能抓取评论。 |

---

## 数据速览（今日 Top10 全量快照）

| # | 原文标题 | 中文标题 | 分数 | 评论 |
| --- | --- | --- | --- | --- |
| 1 | [Jev in 25 Lines of Python](https://www.nobodywho.ai/posts/jev-in-25-lines/) | 25行Python代码实现Jev | 458 | 139 |
| 2 | [Grammarly will send unhinged messages to all your users](https://www.reddit.com/r/sysadmin/comments/1wjdpgx/psa_grammarly_will_send_unhinged_messages_to_all/) | Grammarly会向你所有用户发送疯狂消息 | 332 | 93 |
| 3 | [Transit rewards](https://waymo.com/blog/2026/09/transit-rewards/) | Waymo推出交通奖励计划 | 234 | 289 |
| 4 | [Netherlands bracing for potentially devastating US sanctions against the ICC](https://apnews.com/article/icc-trump-sanctions-eu-israel-netherlands-2c1cc314732f920c2de59396d3b556f6) | 荷兰为应对美国制裁国际刑事法院做准备 | 125 | 118 |
| 5 | [US criticises Australia's proposed algorithm opt-out laws as 'censorship'](https://www.bbc.com/news/articles/cqj3dgy8x3vro) | 美国批评澳大利亚算法选择退出法为‘审查制度’ | 105 | 131 |
| 6 | [Data-only attacks are easier than you think](https://www.usenix.org/publications/loginonline/data-only-attacks-are-easier-you-think) | 数据-only攻击比你想象的更容易 | 92 | 42 |
| 7 | [Abandoning Scientific Linux Was a Mistake](https://blog.melashri.net/posts/scientific-linux-mistake/) | 放弃Scientific Linux是个错误 | 72 | 55 |
| 8 | [Kalshi to allow trading on borrowed funds](https://www.semafor.com/article/09/22/2026/kalshi-to-allow-trading-on-borrowed-funds) | Kalshi将允许使用借入资金进行交易 | 22 | 8 |
