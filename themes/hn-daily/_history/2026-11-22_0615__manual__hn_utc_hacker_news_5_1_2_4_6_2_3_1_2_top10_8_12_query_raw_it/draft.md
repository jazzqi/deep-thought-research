# HN 书摘 · 2026-11-22（周日）

> 今日三句话：① 黎曼猜想的 Lean 形式化证明获社区正式认证（1700 万行代码、多独立校验器复核），与昨日"零验证声称"形成对照——可机器验证性首次为 AI 时代的数学突破提供信用背书；② SimpleBench 显示非专业人类（83.7%）仍胜过全部前沿模型（Claude Fable 81.9%），OpenAI 新模型集体退步——"榜单即能力"再次被证伪；③ 开源基础设施安全与数据隐私双线告急：GPGME double-free RCE、Ghostscript 沙箱逃逸波及 Google/WordPress/Dropbox，叠加 GTA6 行为画像与 OpenRouter 提示词泄露——"可验证性 + 数据主权"贯穿本期。

> ⛔ 强制规则：正文禁止出现 `@用户名`。提及作者/评论者一律写「作者 用户名」。

## 头条深读（2 条）

### 1. 黎曼猜想的 Lean 证明获社区正式认证：1700 万行代码、多独立校验器复核

| 原文 | [Lean Verification of the Riemann Hypothesis - Joint statement by the Lean and Mathlib communities](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) |
| --- | --- |
| 热度 | ▲148 · 💬117 · 作者 g-b-r · 2026-11-21 14:36 UTC |
| 摘要 | Lean 与 Mathlib 社区发布联合声明，认证 Levent Alpöge 于 11-20 发布的黎曼猜想证明——一份 1700 万行代码的 Lean 库。认证依据四条标准：命题本身是 Mathlib 已审核的 RiemannHypothesis；代码库仅依赖 Mathlib 且数十人复现编译成功；用 comparator 与 con-leche --compare 两个独立工具确认所证命题与 Mathlib 命题完全一致；导出的原始证明经 Lean 官方 kernel、con-leche、con-ron 及第三方多语言校验器检验，其中 con-leche/con-ron 附带形式化证明保证"不可能接受假证明"。 |
| 批注 | **tech_generalist 视角：** 本期最重要的验证链闭合事件——昨日（11-21 稿）记录的"Anthropic 员工声称证明黎曼猜想（▲2145/💬1464）高热度零复核"，今天被一份可机器检验、多独立校验器交叉认证的证明取代。形式化验证把"数学突破"从依赖权威背书转为依赖可复现计算，这是 AI 时代建立技术叙事信用的范式样本。confidence 78（社区联合声明 + 多校验器，但数学界同行评议尚需时间）。 |
| 评论摘录 | 作者 adamtaylor_13："Last I heard Alpöge was quite a mathematician in his own right, so saying his using AI is 'controversial' is like saying programmers using AI is controversial."（[链接](https://news.ycombinator.com/item?id=50590275)）；另有作者质疑校验进度"not everything at math.mit.edu/~drew/grh had finished running"（[链接](https://news.ycombinator.com/item?id=50590100)）。 |

### 2. SimpleBench：人类常识推理仍胜过全部前沿模型，OpenAI 新模型集体退步

| 原文 | [Astra 6.2 and Sol 6.2 flop at Simple Bench](https://simple-bench.com/) |
| --- | --- |
| 热度 | ▲155 · 💬151 · 作者 algoth1 · 2026-11-21 13:16 UTC |
| 摘要 | SimpleBench 是一个 200+ 题的选择题基准，覆盖时空推理、社交智能与"语言对抗鲁棒性"（trick questions）。非专业人类基线 83.7%（9 人小样本）超过全部受测模型，包括榜首 Claude Fable 的 81.9%。榜单更新后新模型普遍进步，唯独 OpenAI 系列退步：Sol 6.2 从第 10 跌至第 30、Astra 6.2 从第 9 跌至第 15，仅 Astra 6 pro 略高于人类基线（第 8）。 |
| 批注 | **tech_generalist 视角：** 与头条 #1 构成同一主题的两面——#1 是"可验证的突破"，#2 是"不可验证的能力宣称被戳破"。SimpleBench 用高中知识水平的人类基线划出 LLM 能力边界：记忆知识 + 近似推理检索在基础常识题上仍不够用。OpenAI 新版本在更新后反而退步，直接证伪"版本号即能力"的叙事。confidence 72（benchmark 官方一手数据，但人类基线仅 9 人样本）。 |
| 评论摘录 | 作者 algoth1："every new model release got substantially better, except for the OpenAi models. 6.2 Sol is 30th whereas 6.1 Sol is the 10th."（[链接](https://news.ycombinator.com/item?id=50588917)） |

## 值得一读（5 条）

### 3. GPGME 严重漏洞：double-free 可致数据外泄与 RCE，波及主流邮件客户端

| 原文 | [GnuPG Security Advisory for GPGME (T8557, CVE-2026-129975)](https://lists.gnupg.org/pipermail/gnupg-announce/2026q4/000517.html) |
| --- | --- |
| 热度 | ▲173 · 💬53 · 作者 gdgghhhhh · 2026-11-21 08:32 UTC |
| 摘要 | GPGME 2.3.1 修复一个影响所有旧版本的严重漏洞：含超长 user id 的 OpenPGP 密钥可触发 double-free，被用于从应用中外泄数据（如签名数据），RCE 无法排除。根因是读取 status line 的缓冲区 realloc 后未及时回写 context，提前返回时留下悬空指针。影响 Gpg4win、GnuPG Desktop、多数邮件客户端、XMPP 客户端、Samba、Flatpak。因 Ruby2Shell 事件提前至 11-20 披露。 |

### 4. 显示器把下载速度砍掉 75%：一次 USB 流控调试

| 原文 | [My Monitor Was Cutting My Download Speed by 75%](https://blog.tymscar.com/posts/studiodisplayethernet/) |
| --- | --- |
| 热度 | ▲359 · 💬187 · 作者 soheilpro · 2026-11-21 10:36 UTC |
| 摘要 | 作者 2.5G 对称宽带经 Studio Display XDR 上的 UGREEN USB-C 转 2.5G 适配器只有 600Mbps 下行、上行正常。排查发现 Realtek RTL8156B 在 macOS 通用驱动下丢帧，换厂商驱动升至 1.1Gbps，最终在 UniFi 控制台开启 flow control（暂停帧让发送端缓冲）后恢复到约 2Gbps。 |

### 5. ClawDOS：在 8088 DOS 机器上跑的 AI 编程 agent，100% 由 Claude 编写

| 原文 | [ClawDOS – An AI coding agent for DOS](http://ricapar.net/ClawDOS/) |
| --- | --- |
| 热度 | ▲152 · 💬47 · 作者 Ricapar · 2026-11-21 05:38 UTC |
| 摘要 | 作者在真实 IBM PC 5160（8088 @ 4.77MHz、640K RAM、CGA）上实现 AI 编程 agent：176KB 的 HARNESS.EXE 直接说 Claude Messages API，能读写磁盘文件、用 Turbo C 编译、查看屏幕输出、跨对话保留笔记。仓库除作者手写说明外 100% 由 Claude 编写，TLS 由一台桥接 PC 处理。 |

### 6. FBI 犯罪数据库 NCIC 遭入侵，正在调查

| 原文 | [FBI reportedly investigating apparent hack of its criminal database](https://www.bbc.com/news/articles/cvze7de86pk3o) |
| --- | --- |
| 热度 | ▲137 · 💬70 · 作者 theanonymousone · 2026-11-21 10:33 UTC |
| 摘要 | FBI 正调查国家犯罪信息中心（NCIC）数据库疑似被入侵，该库供联邦与地方执法机构共享通缉令与背景调查信息。特朗普在福克斯采访中称"刚听说"，"这不好，我不喜欢"。FBI 未立即回应置评请求。 |

### 7. 任何人都能轻松使用私有开源权重模型

| 原文 | [Here's how anyone can easily use private, open weight models](https://micahflee.com/heres-how-anyone-can-easily-use-private-open-weight-models/) |
| --- | --- |
| 热度 | ▲20 · 💬7 · 作者 DeepLogin · 2026-11-21 12:11 UTC |
| 摘要 | 作者给出零学习成本的隐私推理路径：用 Maple AI 在 TEE 中运行开源权重模型，对话不被服务商窥探，无需昂贵 GPU 或专家知识。文章强调最强开源权重模型多来自中国公司，并推荐 OpenCode、Pi 等同类工具。 |

## 技术雷达（3 条）

### 8. Upload2Shell：Ghostscript 沙箱逃逸，波及 Google、WordPress、Dropbox、Debian

| 原文 | [Upload2Shell · CVE-2026-125396](https://pwn.ai/upload2shell) |
| --- | --- |
| 热度 | ▲36 · 💬9 · 作者 f311a · 2026-11-21 18:29 UTC |
| 摘要 | Ghostscript Type 1 字体加载器的 use-after-free 可越过 -dSAFER 沙箱、改写原生路径控制并以渲染进程权限执行任意命令。pwn.ai 记录完整披露链：7-27 发现，7-30 向 Google 提交生产环境证明，8-12 WordPress 修复，9-08 Artifex 发布 Ghostscript 10.08.0，9-17 Debian CUPS 未认证 RCE，9-18 Roundcube 附件缩略图触发 RCE。 |

### 9. LookAtMyQuant：同体积下 KL 比 Q4_K_M 低 12 倍的量化编译器

| 原文 | [Inkling-2-Mini in 5.4 GB Memory](https://github.com/ShinMegamiBoson/lookatmyquant) |
| --- | --- |
| 热度 | ▲65 · 💬4 · 作者 k__ · 2026-11-21 18:02 UTC |
| 摘要 | 开源量化编译器逐块测量压缩对输出的损害并分配编码，在 Gemma 4 E2B 上同文件体积下 GGUF 的 KL 比 Q4_K_M 低 12 倍；LookAtMyQuant 2 把 Qwen3.5-4B 压到 1.23GB（2.3 bit/权重），在 540 道精确答案数学题中解出 330 道。MIT 许可。 |

### 10. Zero C#：无 GC、无 .NET runtime，编译到 386 与 WebAssembly

| 原文 | [Zero C#, Power of C# without any GC](https://onurgumus.github.io/zero-csharp/index.html) |
| --- | --- |
| 热度 | ▲32 · 💬20 · 作者 reverseblade2 · 2026-11-21 15:39 UTC |
| 摘要 | bflat 的分支把 C# 直接编译为原生程序：保留语法、类型检查、泛型与 C# 15 特性，去掉 GC 与 .NET runtime，内存来自可整体释放的 arena。Hello world 在 Windows 仅 11KB、Linux 40KB，同一源码可跑在 Linux/macOS/Windows、WebAssembly 与 386 的 DOS 上。 |

## 社区之声（2 条）

### 11. 前 Rockstar 工程师爆料：GTA6 为玩家建立可交易的行为画像

| 原文 | [GTA VI is building behavioral profiles of those who play](https://twitter.com/make_claude/status/2123908856145232060) |
| --- | --- |
| 热度 | ▲22 · 💬8 · 作者 iloveyoutwo · 2026-11-21 18:59 UTC |
| 摘要 | 一名自称被解雇的 Rockstar North 高级引擎工程师称，GTA6 遥测经 Take-Two 内部系统 Lens 为每位玩家生成毫秒级"行为签名"（冲动控制、风险承受、攻击性反应等心理类别），再经子公司 Vantage Analytics 授权给保险、信用风控、HR 筛选与广告经纪客户。该爆料为单一匿名信源，未获独立核实。 |

### 12. Tell HN：发往 MiniMax 的 OpenRouter 提示词可能被读取

| 原文 | [Tell HN: OpenRouter prompts to Minimax may have been read](https://news.ycombinator.com/item?id=50585962) |
| --- | --- |
| 热度 | ▲29 · 💬3 · 作者 dannyw · 2026-11-21 04:31 UTC |
| 摘要 | 作者收到一封疑似真实的 OpenRouter 邮件，称安全研究员放置的唯一标识测试提示词显示，发往 MiniMax 模型的请求可能已被读取。无公开页面或博客说明，作者据邮件内容转述。 |

## 数据速览（今日 Top10 全量快照）

| # | 原文标题 | 中文标题 | 分数 | 评论 |
| --- | --- | --- | --- | --- |
| 1 | [Detonating a Pile of Lead Azide](https://www.science.org/content/blog-post/detonating-huge-pile-lead-azide-really) | 引爆一大堆叠氮化铅 | 454 | 300 |
| 2 | [My Monitor Was Cutting My Download Speed by 75%](https://blog.tymscar.com/posts/studiodisplayethernet/) | 显示器让下载速度掉了 75% | 359 | 187 |
| 3 | [BlackBlaze now explicitly states selling your data for advertisement](https://www.backblaze.com/company/policy/privacy) | Backblaze 明确声明出售用户数据用于广告 | 221 | 78 |
| 4 | [RCE in Gnupg](https://lists.gnupg.org/pipermail/gnupg-announce/2026q4/000517.html) | GnuPG 远程代码执行漏洞 | 173 | 53 |
| 5 | [Clojure will affect the way you think about programming (2017)](https://eli.thegreenplace.net/2017/clojure-the-perfect-language-to-expand-your-brain/) | Clojure 会改变你的编程思维方式（2017） | 171 | 78 |
| 6 | [Astra 6.2 and Sol 6.2 flop at Simple Bench](https://simple-bench.com/) | Astra 6.2 与 Sol 6.2 在 SimpleBench 翻车 | 155 | 151 |
| 7 | [ClawDOS – An AI coding agent for DOS](http://ricapar.net/ClawDOS/) | ClawDOS：DOS 上的 AI 编程 agent | 152 | 47 |
| 8 | [Lean Verification of the Riemann Hypothesis](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) | 黎曼猜想的 Lean 形式化验证 | 148 | 117 |
| 9 | [Surprisingly Adorable Insect Portraits](https://amateurphotographer.com/latest/these-astonishing-insect-portraits-reveal-a-hidden-world-you-never-knew-existed/) | 出人意料可爱的昆虫肖像 | 141 | 30 |
| 10 | [FBI reportedly investigating apparent hack of its criminal database](https://www.bbc.com/news/articles/cvze7de86pk3o) | FBI 据报调查犯罪数据库遭黑事件 | 137 | 70 |
