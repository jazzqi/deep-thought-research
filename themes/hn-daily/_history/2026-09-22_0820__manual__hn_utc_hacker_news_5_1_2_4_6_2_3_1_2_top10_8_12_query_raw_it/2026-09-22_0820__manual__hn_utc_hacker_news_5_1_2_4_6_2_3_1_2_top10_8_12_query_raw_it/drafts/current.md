# HN 书摘 · 2026-09-21（周日）

> 今日三句话：① Grok 4.7 以 1/5 价格打平 Fable 5.1，AI 模型性价比竞争进入"同价更大"新阶段；② ZuckOff 通过蓝牙被动监听识别 Meta 智能眼镜，隐私对抗工具从"事后追责"升级为"事前感知"；③ Bryan Cantrill 复盘 Sun 衰落——战略正确但厌倦运营执行，是技术公司最常见的墓志铭。

---

## 分工

| 栏目 | 负责人 | 说明 |
| --- | --- | --- |
| 头条深读 | tech_generalist | 两条头条 |
| 值得一读 | tech_scout | 5 条，侧重开发者工具与开源生态 |
| 技术雷达 | tech_scout | 3 条，新工具/新库 |
| 社区之声 | tech_generalist | 2 条，用户权利讨论 |
| 数据速览 | 代码注入 | Top10 快照 |

---

## 头条深读（1-2 条）

### 1. Grok 4.7：xAI 发布旗舰模型，性价比重新洗牌

| 原文 | [Grok 4.7](https://x.ai/news/grok-4-7) |
| --- | --- |
| 热度 | ▲ 481 · 💬 400 · 作者 meetpateltech · 2026-09-21 |
| 摘要 | xAI 发布 Grok 4.7，在 CursorBench 4.0（长周期编码任务）上得分 46.3%，与 Fable 5.1 Max（51.8%）和 GPT-5.6 Sol（41.7%）处于同一梯队，但输入 token 价格 $2/M（Fable $10/M，GPT-5.6 $4/M）。新模型采用更长强化学习训练，专注多小时级任务，在 Terminal-Bench 4.0（38.0%）和 Harvey Legal Agent（19.6%）上均超前代 Grok 4.6（20.3%、15.8%）。安全层面，Grok 4.7 在 HackerBench v0.3 上仅放行 3.3% 风险提示，同时在 LatchBio 生物安全基准达 62.4%。 |
| 批注 | 价格锚点转移：xAI 用"同速同价+更大模型"策略，将竞争焦点从绝对性能转向"单位成本性能"——这对依赖 API 成本的编码工具链影响深远。 |
| 评论摘录 | [HN 评论页](https://news.ycombinator.com/item?id=49788838) — 作者 moojacob 指出 Grok 4.7 比 4.6 多 40% 权重但价格不变，xAI 利润率被压缩；同时质疑基准测试的有效性，称 Grok 4.5 在某些场景（如 buildroot 系统配置）上表现优于 Fable 5。 |

### 2. ZuckOff：蓝牙被动监听识别 Meta 智能眼镜

| 原文 | [ZuckOff](https://zuckoff.app/) |
| --- | --- |
| 热度 | ▲ 590 · 💬 3 · 作者 Bluestein · 2026-09-21 |
| 摘要 | ZuckOff 是一款 iOS/Android 应用，通过监听设备蓝牙广播信号识别附近是否携带 Ray-Ban Meta、Oakley Meta、Snap Spectacles 等摄像眼镜。应用基于制造商蓝牙签名（如 0x0D53 对应 Luxottica 产品线）进行识别，提供后台扫描、iPhone 锁屏 Live Activity 和 Shortcuts 自动化支持。所有数据本地处理，无需账户。 |
| 批注 | 这是"被拍摄者反制拍摄者"的首次规模化工具——当可穿戴摄像设备普及，隐私保护从"事后追责"转向"事前感知"，法律与伦理框架尚未跟上。 |
| 评论摘录 | [HN 评论页](https://news.ycombinator.com/item?id=49785429) — 帖子评论已合并至 [Wired 报道帖](https://news.ycombinator.com/item?id=49785397)（303 条评论），主帖仅 3 条。 |

---

## 值得一读（4-6 条）

### 3. Attention Is All You Have：呼吁回归"主动互联网"

| 原文 | [Attention is all you have](https://alicegg.tech/2026/09/21/attention) |
| --- | --- |
| 热度 | ▲ 557 · 💬 164 · 作者 zer0tonin · 2026-09-21 |
| 摘要 | 文章以心理学"俄罗斯方块效应"开篇——长期关注什么就会被什么塑造——论证推荐算法正在系统性劫持用户注意力。作者指出，算法驱动平台（YouTube、Spotify、LinkedIn、Reddit）的共同问题：用"停留时长最大化"取代"用户意图满足"，将 LLM 内容、推广信息和无关推荐混入用户原本想看的内容流。文章呼吁回归"主动互联网"：用 RSS、书签、订阅制博客取代算法 feed，接受一个"不无限刷新"但可预测的网络。 |

### 4. Disney+ 用户协议变更："无广告"订阅不再保证无广告

| 原文 | [Disney+ ad policy change](https://consumerrights.wiki/w/Disney%2B_ad_policy_change) |
| --- | --- |
| 热度 | ▲ 484 · 💬 342 · 作者 DeepLogin · 2026-09-21 |
| 摘要 | Disney+ 于 2025 年 1 月更新用户协议，Section 2(k) 允许在"无广告"订阅层中播放广告，条件包括：流媒体版权要求、直播/线性内容、捆绑包推广内容、品牌整合和赞助信息。2026 年 9 月，Disney 向德国订阅者发送"澄清"邮件，明确可在内容前后插入广告。此变更通过修改条款实现，现有用户除非主动取消否则自动受新条款约束。 |

### 5. What Sun Got Wrong：Bryan Cantrill 复盘 Sun 衰落

| 原文 | [What Sun Got Wrong](https://bcantrill.dtrace.org/2026/09/20/what-sun-got-wrong/) |
| --- | --- |
| 热度 | ▲ 489 · 💬 272 · 作者 chmaynard · 2026-09-21 |
| 摘要 | Oxide Computer 创始人 Bryan Cantrill 回顾 Sun Microsystems 衰落的核心原因：战略正确但运营执行失败。案例：2005 年一家使用 OpenSolaris 的初创公司想购买大量 Sun 硬件，但 Sun 无法响应销售需求；对比之下，Dell 的销售代表 Steve 在 24 小时内主动联系、两周内完成部署和融资。Cantrill 的结论：一个"厌倦了经营业务基本功"的公司无法持续成功——这是 Sun 的墓志铭。 |

### 6. Kev：基于 Qwen3.5 的轻量决策模型家族

| 原文 | [Kev](https://github.com/jaredpalmer/kev/tree/main) |
| --- | --- |
| 热度 | ▲ 401 · 💬 177 · 作者 tosh · 2026-09-21 |
| 摘要 | Kev 是基于 Qwen3.5 的小规模决策模型家族（0.8B/4B/9B 参数），支持是/否、多选、评分三种问题类型，API 兼容 TypeSafe System One SDK。模型可在 CUDA、ROCm 和 Apple Silicon 上运行，4B/9B 模型在 32GB Mac 上以 bf16 推理。项目提供训练代码、评估数据和 Hugging Face 在线体验，定位为本地可训练、可部署的"轻量决策引擎"。 |

### 7. Mini-AGI：8GB VRAM 上的持续学习实验

| 原文 | [Mini-AGI](https://github.com/volotat/mini-AGI/) |
| --- | --- |
| 热度 | ▲ 248 · 💬 56 · 作者 volotat · 2026-09-21 |
| 摘要 | Mini-AGI 是一个持续学习字节级语言模型，可在单张 8GB VRAM 显卡上从零训练。核心设计：采用 MoE 架构，专家数量随训练动态增减，参数上限由磁盘空间而非显存决定；训练时仅加载当前需要的专家子集，batch-1 流式数据训练避免大批次显存占用。作者自述为"玩具级实验"，目标是证明在消费硬件上实现无灾难性遗忘的持续学习是可行的。 |

---

## 技术雷达（2-3 条）

### 8. Cloudflare Python Workers 正式 GA

| 原文 | [Python Workers are now generally available](https://blog.cloudflare.com/python-workers-ga/) |
| --- | --- |
| 热度 | ▲ 175 · 💬 28 · 作者 torutofu · 2026-09-21 |
| 摘要 | Cloudflare 宣布 Python Workers 正式进入 GA（通用可用）阶段。此前 Python Workers 通过 Pyodide（Wasm 编译的 Python 解释器）运行，开发者需手动处理 Python↔JavaScript 类型转换。GA 版本将类型转换封装进运行时和 SDK，开发者可直接用 Pythonic 方式调用 Cloudflare 全平台绑定（R2、D1、Queues 等），无需写一行 JavaScript。支持 FastAPI、Django、Flask 等主流框架。 |

### 9. Raspberry Pi 禁止更换 RAM 芯片

| 原文 | [Raspberry Pi blocks changing RAM chips](https://forums.raspberrypi.com/viewtopic.php?p=2380887#p2380888) |
| --- | --- |
| 热度 | ▲ 205 · 💬 160 · 作者 edandersen · 2026-09-21 |
| 摘要 | Raspberry Pi 基金会通过 EEPROM 更新阻止用户更换 RAM 芯片，论坛帖子引发社区争议。此举被解读为对硬件可修复性和用户自主权的限制，与开源硬件精神形成张力。 |

### 10. 小米 MiMo v2.6 发布

| 原文 | [Xiaomi MiMo v2.6](https://mimo.xiaomi.com/mimo-v2-6) |
| --- | --- |
| 热度 | ▲ 154 · 💬 53 · 作者 volf_ · 2026-09-21 |
| 摘要 | 小米发布 MiMo v2.6，细节未完全披露。作为小米 AI 模型线的持续迭代，此版本可能涉及多模态能力增强。 |

---

## 社区之声（1-2 条）

### 11. macOS 27 如何绕过 AI 模型自动下载

| 原文 | [macOS 27: Workaround to avoid downloading AI models](https://www.reddit.com/r/MacOSBeta/comments/1vlnf13/workaround_to_avoid_downloading_ai_models_and/) |
| --- | --- |
| 热度 | ▲ 207 · 💬 98 · 作者 ano-ther · 2026-09-21 |
| 摘要 | Reddit 用户分享 macOS 27 beta 中避免 Apple Intelligence 自动下载 AI 模型、节省存储空间的变通方法。社区反应混合：部分用户赞赏对存储控制的需求，部分认为这是对 Apple "强制 AI 化"策略的被动抵抗。 |

### 12. Ask HN: macOS 27 是否无法禁用 Siri？

| 原文 | [Is it impossible to disable Siri on macOS 27?](https://news.ycombinator.com/item?id=49786609) |
| --- | --- |
| 热度 | ▲ 137 · 💬 73 · 作者 semidror · 2026-09-21 |
| 摘要 | 用户报告在 macOS 27 中禁用 Siri 后，系统仍通过 Screen Time、服务管理等多种途径尝试启用。帖子列出详细的禁用步骤（包括 GitHub 上的开源工具），反映社区对 Apple 强制 AI 功能整合的抵触情绪。 |

---

## 数据速览（今日 Top10 全量快照）

| # | 原文标题 | 中文标题 | 分数 | 评论 |
| --- | --- | --- | --- | --- |
| 1 | [ZuckOff](https://zuckoff.app/) | ZuckOff 摄像头眼镜检测器 | 590 | 3 |
| 2 | [Attention is all you have](https://alicegg.tech/2026/09/21/attention) | 注意力就是你拥有的一切 | 557 | 164 |
| 3 | [What Sun Got Wrong](https://bcantrill.dtrace.org/2026/09/20/what-sun-got-wrong/) | Sun 做错了什么 | 489 | 272 |
| 4 | [Disney+ ad policy change](https://consumerrights.wiki/w/Disney%2B_ad_policy_change) | Disney+ 广告政策变更 | 484 | 342 |
| 5 | [Grok 4.7](https://x.ai/news/grok-4-7) | Grok 4.7 发布 | 481 | 400 |
| 6 | [Kev](https://github.com/jaredpalmer/kev/tree/main) | Kev：轻量决策模型家族 | 401 | 177 |
| 7 | [Grim Fandango Puzzle Document](http://gameshelf.jmac.org/2008/11/13/GrimPuzzleDoc_small.pdf) | 神秘岛谜题文档 (1996) | 344 | 87 |
| 8 | [Fable 5 – Median thinking declined in August](https://twitter.com/Lon/status/2101793422487204027) | Fable 5 – 中位思维八月下降 | 340 | 235 |
| 9 | [Mini-AGI](https://github.com/volotat/mini-AGI/) | Mini-AGI：8GB VRAM 持续学习模型 | 248 | 56 |
| 10 | [Raspberry Pi blocks changing RAM chips](https://forums.raspberrypi.com/viewtopic.php?p=2380887#p2380888) | 树莓派禁止更换 RAM 芯片 | 205 | 160 |
