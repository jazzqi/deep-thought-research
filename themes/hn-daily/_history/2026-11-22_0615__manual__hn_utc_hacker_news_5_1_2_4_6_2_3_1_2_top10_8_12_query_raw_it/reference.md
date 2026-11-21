## 数据溯源 · HN 书摘 2026-11-22（覆盖 2026-11-21 UTC 窗口）

### 主取数 query_raw_items（source=hackernews, min_points=20, published 2026-11-21T00:00→2026-11-22T00:00Z，返回 24 条）

- 黎曼猜想 Lean 形式化证明获社区联合认证（1700 万行代码、多独立校验器复核）: query_raw_items(source=hackernews, min_points=20, 2026-11-21 UTC)[id:807529] = Lean Verification of the Riemann Hypothesis - Joint statement，▲148/💬117
- SimpleBench 人类基线 83.7% 胜过全部前沿模型，OpenAI 新模型集体退步: query_raw_items(source=hackernews, min_points=20, 2026-11-21 UTC)[id:807493] = Astra 6.2 and Sol 6.2 flop at Simple Bench，▲155/💬151
- GPGME 严重漏洞 double-free 可致数据外泄与 RCE（CVE-2026-129975）: query_raw_items(source=hackernews, min_points=20, 2026-11-21 UTC)[id:807342] = RCE in Gnupg，▲173/💬53
- Studio Display 经 USB-C 适配器使下载速度降 75%: query_raw_items(source=hackernews, min_points=20, 2026-11-21 UTC)[id:807410] = My Monitor Was Cutting My Download Speed by 75%，▲359/💬187
- 8088 DOS 上运行的 AI 编程 agent，100% 由 Claude 编写: query_raw_items(source=hackernews, min_points=20, 2026-11-21 UTC)[id:807169] = ClawDOS – An AI coding agent for DOS，▲152/💬47
- FBI 国家犯罪信息中心 NCIC 数据库疑似被入侵: query_raw_items(source=hackernews, min_points=20, 2026-11-21 UTC)[id:807343] = FBI reportedly investigating apparent hack of its criminal database，▲137/💬70
- 用 TEE 中的开源权重模型实现零学习成本隐私推理: query_raw_items(source=hackernews, min_points=20, 2026-11-21 UTC)[id:807570] = Anyone can easily use private, open weight models，▲20/💬7
- Ghostscript Type 1 字体加载器 use-after-free 逃逸 -dSAFER 沙箱（CVE-2026-125396）: query_raw_items(source=hackernews, min_points=20, 2026-11-21 UTC)[id:807729] = Upload2Shell · CVE-2026-125396，▲36/💬9
- 量化编译器同体积下 KL 比 Q4_K_M 低 12 倍，Qwen3.5-4B 压到 1.23GB: query_raw_items(source=hackernews, min_points=20, 2026-11-21 UTC)[id:807682] = Inkling-2-Mini in 5.4 GB Memory，▲65/💬4
- 无 GC 无 .NET runtime 的 C#，编译到 386/DOS/WebAssembly: query_raw_items(source=hackernews, min_points=20, 2026-11-21 UTC)[id:807592] = Show HN: Zero C#, Power of C# without any GC，▲32/💬20
- 前 Rockstar 工程师爆料 GTA6 建立可交易行为画像（单一匿名信源，未核实）: query_raw_items(source=hackernews, min_points=20, 2026-11-21 UTC)[id:807730] = GTA VI is building behavioral profiles of those who play，▲22/💬8
- 发往 MiniMax 的 OpenRouter 提示词疑似被读取: query_raw_items(source=hackernews, min_points=20, 2026-11-21 UTC)[id:807275] = Tell HN: OpenRouter prompts to Minimax may have been read，▲29/💬3
- Top10 快照补充条目: query_raw_items(source=hackernews, min_points=20, 2026-11-21 UTC)[id:807459] = Detonating a Pile of Lead Azide，▲454/💬300（正文 403 未抓取）
- Top10 快照补充条目: query_raw_items(source=hackernews, min_points=20, 2026-11-21 UTC)[id:806914] = BlackBlaze now explicitly states selling your data for advertisement，▲221/💬78（抓取正文未见出售数据条款，标题主张未核实）
- Top10 快照补充条目: query_raw_items(source=hackernews, min_points=20, 2026-11-21 UTC)[id:806951] = Clojure will affect the way you think about programming (2017)，▲171/💬78（2017 旧文重发）
- Top10 快照补充条目: query_raw_items(source=hackernews, min_points=20, 2026-11-21 UTC)[id:807265] = Surprisingly Adorable Insect Portraits，▲141/💬30（正文 403 未抓取）

### 正文抓取 fetch_url（HTTPS 优先，抓不到如实标注）

- SimpleBench 人类基线 83.7%（9 人样本）、Claude Fable 81.9%、200+ 题: fetch_url(https://simple-bench.com/) = 官方首页正文
- 黎曼猜想证明 1700 万行 Lean 代码、11-20 发布、四条认证标准、con-leche/con-ron 校验器: fetch_url(https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) = Lean 社区联合声明全文
- GPGME CVE-2026-129975、2.3.1 修复、影响 Gpg4win/邮件客户端/Samba/Flatpak、因 Ruby2Shell 提前披露: fetch_url(https://lists.gnupg.org/pipermail/gnupg-announce/2026q4/000517.html) = GnuPG 官方公告全文
- 显示器 USB-C 适配器 Realtek RTL8156B、换驱动 1.1Gbps、开 flow control 恢复约 2Gbps: fetch_url(https://blog.tymscar.com/posts/studiodisplayethernet/) = 作者原文
- ClawDOS 运行于 IBM PC 5160（8088@4.77MHz/640K）、HARNESS.EXE 176KB、100% Claude 编写: fetch_url(http://ricapar.net/ClawDOS/) = 项目主页
- FBI NCIC 数据库被黑、特朗普福克斯采访回应: fetch_url(https://www.bbc.com/news/articles/cvze7de86pk3o) = BBC 正文
- Upload2Shell 披露时间线（7-27 发现→9-08 Ghostscript 10.08.0→9-17 Debian CUPS RCE）: fetch_url(https://pwn.ai/upload2shell) = pwn.ai 研究页
- LookAtMyQuant Gemma 4 E2B 12× lower KL、Qwen3.5-4B 1.23GB/2.3bit、解出 330/540: fetch_url(https://github.com/ShinMegamiBoson/lookatmyquant) = GitHub README
- Zero C# 无 GC/无 runtime、hello world 11KB(Win)/40KB(Linux)、支持 DOS 386/WebAssembly: fetch_url(https://onurgumus.github.io/zero-csharp/index.html) = 项目主页
- GTA6 Lens/Vantage Analytics 行为画像爆料全文（中文）: fetch_url(https://twitter.com/make_claude/status/2123908856145232060) = X 帖文
- 开源权重模型/Maple TEE 教程: fetch_url(https://micahflee.com/heres-how-anyone-can-easily-use-private-open-weight-models/) = 作者原文
- 抓取失败如实标注: fetch_url(https://www.science.org/...lead-azide-really) = 403 Forbidden；fetch_url(https://www.economist.com/...jensen-huangs-fall...) = 403；fetch_url(https://www.bloomberg.com/...toy-sales...) = 403；fetch_url(https://www.reuters.com/...anthropics-ipo...) = 401；fetch_url(https://amateurphotographer.com/...insect-portraits...) = 403

### 评论抓取 fetch_url（Algolia HN items API）

- 黎曼猜想评论（AI 参与争议、校验进度质疑）: fetch_url(https://hn.algolia.com/api/v1/items/50589618) = 评论树
- SimpleBench 评论（榜单更新细节、OpenAI 退步）: fetch_url(https://hn.algolia.com/api/v1/items/50588916) = 评论树


### 评论抓取补充（Algolia HN items API，tech_scout 第 1/3 棒）

- Inkling-2-Mini 评论（发布文件仅 MLX/Apple Silicon、ht2/ht3 码需定制 Metal 内核、drafter MLX-only、llama.cpp 尚不能运行、QAT vs 原生 NVFP4 之争）: fetch_url(https://hn.algolia.com/api/v1/items/50591853) = 评论树
- GnuPG RCE 评论（Johan Carlsson 发现、GitLab 2026-11-12 通知、原定 11-25 协调披露因 Ruby2Shell 提前至 11-20、GitLab 签名提交路径风险）: fetch_url(https://hn.algolia.com/api/v1/items/50587208) = 评论树
- 黎曼猜想评论（"verified to a much higher standard than peer reviewed mathematics"、AI 参与争议、校验进度质疑）: fetch_url(https://hn.algolia.com/api/v1/items/50589618) = 评论树
- SimpleBench 评论（榜单更新：6.2 Sol 第10→第30、Astra 6 第9→第15、Fable 5.2 升至第1、脑筋急转弯式题目设计）: fetch_url(https://hn.algolia.com/api/v1/items/50588916) = 评论树


### 正文复核（ai_specialist 第 2/3 棒）

- SimpleBench 官方首页复核：非专业人类基线 83.7%（9 人样本）、Claude Fable 81.9%、200+ 题覆盖 spatio-temporal reasoning/social intelligence/linguistic adversarial robustness（trick questions）: fetch_url(https://simple-bench.com/) = 与首棒记录一致，新增题型分类佐证"鲁棒性维度"判断
- LookAtMyQuant README 复核：Gemma 4 E2B 同体积 KL 比 Q4_K_M 低 12×、Qwen3.5-4B 1.23GB/2.3bit 解 330/540、Qwen3.8-27B 压到 7.2GB/2.1bit 解 401/540（与原模型持平）、MIT 许可、38 commits、$34 GPU 成本: fetch_url(https://github.com/ShinMegamiBoson/lookatmyquant) = 与首棒记录一致


### 终审补充溯源（tech_generalist 第 3/3 棒）

- Anthropic IPO 银行平仓稳价操作（资本侧背离依据）: query_raw_items(source=hackernews, min_points=20, 2026-11-21 UTC)[id:807591] = Anthropic's IPO bank closed position meant to stabilize stock，▲21/💬0（Reuters 正文 401 未抓取）
- OpenRouter 发往 MiniMax 的提示词疑似被读取（数据主权反噬依据）: query_raw_items(source=hackernews, min_points=20, 2026-11-21 UTC)[id:807275] = Tell HN: OpenRouter prompts to Minimax may have been read，▲29/💬3（无公开页面，未获官方证实）
- 黄仁勋跌落与加速主义叙事转向（情绪面参考）: query_raw_items(source=hackernews, min_points=20, 2026-11-21 UTC)[id:807660] = Jensen Huang's fall is bad news for Silicon Valley's accelerationists，▲87/💬118（Economist 正文 403 未抓取）
- 主取数窗口复核（终审）：query_raw_items(source=hackernews, min_points=20, published_after=2026-11-21T00:00:00Z, published_before=2026-11-22T00:00:00Z) = 返回 24 条，与前两棒记录一致，无数据缺口
