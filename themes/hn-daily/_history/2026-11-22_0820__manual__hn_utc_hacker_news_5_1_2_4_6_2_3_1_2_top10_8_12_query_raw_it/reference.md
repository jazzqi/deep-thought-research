# 数据溯源 · HN 书摘 2026-11-22（tech_scout 第 1/3 棒改写增补）

## fetch_url 正文抓取
- 黎曼社区认证正文: fetch_url(https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) = 2026-11-20 Levent Alpöge 发布 1700 万行 Lean 证明；社区认证陈述与证明均正确、四条标准全满足；comparator/con-leche 独立工具确认所证即 Mathlib RiemannHypothesis；Lean 官方内核 + con-leche/con-ron + 第三方多语言 checker 交叉复核；con-leche/con-ron 带相对集合论形式化可靠性证明
- SimpleBench 正文: fetch_url(https://simple-bench.com/) = 200+ 道时空推理/社交智能/语言对抗鲁棒性题；非专业人类基线 83.7%（9 人样本）胜过全部模型；顶级 Claude Fable 81.9%
- SimpleBench 评论: fetch_url(https://news.ycombinator.com/item?id=50588916) = 作者 0xbadc0de5 称重度使用 Sol-6.2/Astra-6.2 后认为是明显改进、可比 Opus-5.5/Fable-5.2，"不再相信 influencer-benchmaxxers"（基准合成、不跑真实工作流）
- 黎曼评论: fetch_url(https://news.ycombinator.com/item?id=50589618) = 作者 rcr-anti 称 RH 为假需所有内核同时存在既影响一致性证明又影响 RH 证明的 bug；作者 jychang 解释 comparator 可识别"重定义 2 为 4 去证明 1+2=5"这类数学作弊
- LookAtMyQuant 正文: fetch_url(https://github.com/ShinMegamiBoson/lookatmyquant) = Gemma 4 E2B 同尺寸 KL 比 Q4_K_M 低 12×；Qwen3.5-4B→1.23GB/2.3bit（330/540）；Qwen3.8-27B 53.7GB→7.2GB/2.1bit（401/540，HumanEval 73.8% vs Unsloth GGUF 67.1%）；$34 GPU 时间；39 commits；MIT 许可
- OpenComputer 正文: fetch_url(https://github.com/diggerhq/opencomputer) = 开源可自托管 Devin 替代；单 VM + rootless Podman 隔离 + git-backed 持久化；Cloudflare Workers/Durable Objects；1.2k stars/138 forks/2755 commits/Apache 2.0；开 PR 比 Devin 快 3.3×（56s vs 185s）
- Aaronson 博客: fetch_url(https://scottaaronson.blog/?p=10344) = 17.4M 行 Lean 证明 GRH；"迄今所有带 Lean 证书的 AI 结果无一被撤回"（无证书的已有多起撤回）；数学家需数年才能消化

## query_raw_items 条目（跨期信号衰减曲线 + 本轮引用）
- 黎曼跨期共振: query_raw_items(keyword='Riemann Lean')[id:784168] = 11-12 "proof is checked in Lean"
- 黎曼跨期共振: query_raw_items(keyword='Riemann Lean')[id:780105] = 11-14 税码形式化
- 黎曼跨期共振: query_raw_items(keyword='Riemann Lean')[id:756608] = 11-16 Lean Grimoire
- 黎曼跨期共振: query_raw_items(keyword='Riemann Lean')[id:494143] = 11-19 quasi-RH
- 黎曼跨期共振: query_raw_items(keyword='Riemann Lean')[id:805305] = 11-20 员工声称 ▲2816
- 黎曼社区认证: query_raw_items(keyword='Riemann Lean')[id:807529] = 11-21 Lean/Mathlib 联合认证
- MIT 验证文件: query_raw_items(keyword='Riemann Lean')[id:807681] = 11-21 MIT 验证文件
- Aaronson 佐证: query_raw_items(keyword='Riemann Lean')[id:806307] = 11-20 "stochastic parrots proved RH"
- SimpleBench: query_raw_items(source='hackernews')[id:807493] = Astra 6.2/Sol 6.2 翻车
- Inkling 5.4GB: query_raw_items(source='hackernews')[id:807682] = Inkling-2-Mini 压进 5.4GB
- OpenComputer: query_raw_items(source='hackernews')[id:806458] = 开源 Devin 替代


## tech_generalist 终审增补（第 3/3 棒，监管节点 + 平台锁定视角）
- 联合国自主武器管控谈判破裂: query_raw_items(source='hackernews', keyword='autonomous weapons', 2026-11-21 UTC)[id:807812] = International UN talks on controlling use of autonomous weapons collapse, ▲22/💬0
- GrapheneOS 绕开 Google Messages 实现 RCS: query_raw_items(source='hackernews', keyword='GrapheneOS RCS', 2026-11-21 UTC)[id:807760] = GrapheneOS made a proof of concept RCS messaging app without Google Messages, ▲26/💬3
- Anthropic IPO 银行平仓稳价: query_raw_items(source='hackernews')[id:807591] = Anthropic's IPO bank closed position meant to stabilize stock, ▲31/💬1
- OpenRouter 提示词疑被读取: query_raw_items(source='hackernews')[id:807275] = Tell HN: OpenRouter prompts to Minimax may have been read, ▲41/💬5
- Backblaze 明示出售用户数据: query_raw_items(source='hackernews')[id:806914] = BlackBlaze now explicitly states selling your data for advertisement, ▲221/💬78
