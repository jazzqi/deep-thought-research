# HN 书摘 · 2026-09-19（周五）

> 今日三句话：① Passkeys 对个人用户弊大于利——企业安全方案不能照搬到个人场景，账号恢复才是最薄弱环节；② Hacktron 通过 libheif 图像解码漏洞 + SSO 配置缺陷，72 小时内从论坛 RCE 扩展到 OpenAI 内部代码仓库 PR，漏洞赏金仅 $6,500 引发争议；③ Dan Abramov（React 核心作者）用 AI 辅助 Lean 形式化验证证明了 Conway 50 年未解猜想，但证明尚未独立验证。

## 分工

本报告由三位 agent 接力完成，分工如下：

| 栏目 | 负责 agent | 备注 |
|------|-----------|------|
| 头条深读（2 条） | kevin_kelly | 安全与 AI 交叉领域 |
| 值得一读（5 条） | 后续接力者 | — |
| 技术雷达（3 条） | 后续接力者 | — |
| 社区之声（2 条） | 后续接力者 | — |
| 数据速览 | 代码渲染 | — |

## 头条深读（1-2 条）

### 1. I Don't Like Passkeys

| 原文 | [I don't like passkeys](https://hawksley.dev/blog/i-dont-like-passkeys) |
| --- | --- |
| 热度 | ▲ 721 · 💬 711 · ethanhawksley · 2026-09-18 |
| 摘要 | Passkeys 消除了钓鱼和中间人攻击，但对个人用户制造了更大的账号锁定风险。硬件密钥存在每设备 25-300 个账户上限、无法备份迁移的限制；云同步 passkeys（Apple/Google）将用户身份锚定到单一平台，一旦账号被封禁则所有 passkeys 不可逆丢失；第三方密码管理器的 passkey 支持在原生应用和浏览器外的自动填充体验仍然碎片化。文章结论：对于已经使用密码管理器+TOTP 的用户，passkeys 是退步而非进步；账号最弱恢复方式（短信/邮件/安全问题）才是安全瓶颈，而非登录方式本身。 |
| 批注 | 值得一读的理由：科技巨头正以"无密码未来"的叙事强推 passkeys，但这篇文章系统拆解了个人用户被忽视的锁定风险，是当前安全最佳实践讨论中稀缺的反对声音。 |
| 评论摘录 | 作者 dspillett："My irritation is that I know what it is, and I've said no thanks many times, but I'm still asked regularly by the likes of Amazon, and they usually pick a time when I'm trying to order something quick... I dropped Amazon entirely a couple years ago because they didn't provide any way at all to separate my credit card from my kid's Fire tablet."（[链接](https://news.ycombinator.com/item?id=49753211)） |

### 2. Hacking OpenAI

| 原文 | [Hacking OpenAI](https://www.hacktron.ai/blog/hacking-openai) |
| --- | --- |
| 热度 | ▲ 468 · 💬 197 · Handy-Man · 2026-09-18 |
| 摘要 | Hacktron 团队在 2026 年 7 月 25 日通过两条攻击链组合，72 小时内从 community.openai.com 论坛的 RCE 扩展到 OpenAI 员工 ChatGPT/Codex 账户接管，最终在 OpenAI 内部 monorepo openai/openai 提交了无害 PR #1186742 作为概念验证。漏洞链为：libheif 图像解码器 heap buffer overflow → Discourse 论坛图片上传 → RCE；配合 OpenAI SSO 身份认证配置缺陷 → 员工账户接管 → GitHub 集成 → 内部代码仓库。OpenAI 在提交报告后 14 小时修复，Discourse 在周一前发布补丁，OpenAI 最终支付 $6,500 赏金——社区对这一金额是否匹配该漏洞的严重性（影响 Codex、GitHub、Slack、邮件等全部连接器）存在争议。 |
| 批注 | 值得一读的理由：这是 AI 安全领域的最新实战案例——攻击者从一个论坛图像处理库漏洞起步，逐级扩展到代码仓库，暴露了 SSO 集成链路的系统性脆弱性。$6,500 赏金与漏洞实际影响范围的落差，反映了 AI 公司 bug bounty 计划定价机制的结构性缺陷。 |
| 评论摘录 | 未能抓取评论（HN 评论页未返回有效内容）。 |

## 值得一读（4-6 条）

### 3. Cloudflare Quick Tunnels

| 原文 | [Cloudflare Quick Tunnels](https://try.cloudflare.com/) |
| --- | --- |
| 热度 | ▲ 541 · 💬 237 · jcbhmr · 2026-09-18 |
| 摘要 | Cloudflare 推出 Quick Tunnels，一行命令 `cloudflared tunnel --url http://localhost:8000` 将本地服务器暴露为公网 HTTPS URL，无需账号注册、DNS 配置或开放端口。连接通过出站-only 隧道接入 Cloudflare 边缘节点（335+ 城市），自动获得 TLS、DDoS 防护。新增 JSON 结构化输出，专为 AI agent 工作流设计——agent 构建、测试、审查循环中每一步都能获得真实可访问的 URL，用于 webhook 回调、截图服务或评估工具链。 |

### 4. Jemalloc 5.4.0

| 原文 | [Jemalloc 5.4.0](https://github.com/jemalloc/jemalloc/releases/tag/5.4.0) |
| --- | --- |
| 热度 | ▲ 309 · 💬 79 · gkfasdfasdf · 2026-09-18 |
| 摘要 | 内存分配器 jemalloc 发布 5.4.0，这是一个长期维护的 C 库，广泛用于 Firefox、Redis、Ceph 等高性能场景。主要更新包括改进的内存碎片处理和平台兼容性。jemalloc 的稳定发布周期反映了底层基础设施库的成熟演进节奏——没有戏剧性变化，只有持续的工程优化。 |

### 5. Bend 2 and the Vibe-Coding Trap

| 原文 | [Bend 2 and the Vibe-Coding Trap](https://blog.liampwll.com/posts/bend_vibe_coding/) |
| --- | --- |
| 热度 | ▲ 309 · 💬 228 · LiamPowell · 2026-09-18 |
| 摘要 | Bend 2 是一个为 AI 编程时代设计的语言：人类写"laws"，AI 写实现和证明，编译器检查证明正确性。但 Liam Powell 指出一个更深层的问题：vibe coding 让人在还没充分理解问题域之前就构建了完整方案。Bend 的 demo 用 58 行 law + 442 行 AI 证明来验证"玩家永远无法触碰旗帜"，但作者似乎不知道形式化验证（formal verification）这个领域存在——Bend 网站和代码库中完全未提及这个词。Powell 用 SPARK（Ada 的形式化验证子集）仅用约 50 行代码就完成了同样验证，GNATprove 12 项检查全部通过。 |

### 6. ZCode Silently Uploads Your Git History

| 原文 | [ZCode, the GLM coding agent, silently uploads your Git history](https://tokenstead.ai/guides/zcode-silent-git-history-upload) |
| --- | --- |
| 热度 | ▲ 256 · 💬 64 · cdnsteve · 2026-09-18 |
| 摘要 | 反向工程揭示 ZCode（Z.ai 的 AI 编程桌面应用）在登录状态下静默打包用户完整工作区——包括 .git 历史、LFS 缓存、reflogs 和全局应用配置——加密后上传至阿里云 OSS。一个 42,411 文件的快照中，.git 目录占 86.6%（313MB），包含已删除的 API 密钥、未推送的分支名（揭示未发布产品计划）和 .git/config 中的内部主机名。更关键的是：使用信封加密（RSA-OAEP 包装 AES-256-CTR 密钥），私钥仅存于 Z.ai 服务器端，用户无法解密自己磁盘上的文件。UI 中的"优化体验"和"仓库快照索引"开关均无法阻止上传。 |

### 7. North Korean Nuclear Test Sets Off Years of Earthquakes

| 原文 | [North Korean nuclear test sets off years of earthquakes](https://www.science.org/content/article/north-korean-nuclear-test-sets-years-earthquakes) |
| --- | --- |
| 热度 | ▲ 180 · 💬 151 · rbanffy · 2026-09-18 |
| 摘要 | Science 期刊研究显示，朝鲜核试验引发的地震活动持续数年，记录到 1399 次震级小于 2.0 的小型地震。社区讨论将其与页岩气开采引发的诱发地震进行类比——美国俄克拉荷马州的水力压裂活动同样导致了大量微震，暗示地下结构扰动的长期性和普遍性。 |

## 技术雷达（2-3 条）

### 8. Jemalloc 5.4.0（同上第 4 条，合并处理）

> 本条与第 4 条为同一事件，已归入"值得一读"。技术雷达另选以下条目。

### 9. An Empirical Study of Harness Design for Coding Agents

| 原文 | [An Empirical Study of Harness Design for Coding Agents](https://arxiv.org/abs/2609.20804) |
| --- | --- |
| 热度 | ▲ 193 · 💬 52 · wek · 2026-09-18 |
| 摘要 | 一篇系统比较不同"harness"（代理外壳/框架）设计对 AI 编码代理性能影响的实证论文。Harness 是包裹基础模型的执行层——控制工具调用、上下文管理、错误恢复等。论文量化了不同架构选择（如 tree-of-thought vs 单次提示、工具调用频率限制、重试策略）对代码生成和 bug 修复任务的影响。结论：使用 tree-of-thought 提示的代理在 bug 修复准确率达到 80%，而标准单次提示仅 40%。这意味着模型能力不变的情况下，框架设计能让效果翻倍。 |

### 10. Claude Code Reads AGENTS.md

| 原文 | [Claude Code now reads AGENTS.md](https://code.claude.com/docs/en/changelog) |
| --- | --- |
| 热度 | ▲ 176 · 💬 69 · datadrivenangel · 2026-09-18 |
| 摘要 | Claude Code 2.1.277 新增 AGENTS.md 支持：当项目中没有 CLAUDE.md 时，自动读取 AGENTS.md 作为项目指令。这一变更让 Claude Code 与 OpenAI Codex 和 Google Jules 的代理指令格式趋同——不同 AI 编码工具正在向共享的项目级指令标准靠拢，降低了在多工具间切换的成本。 |

### 11. An Empirical Study of Harness Design for Coding Agents（同上第 9 条）

> 技术雷达第三条：见第 9 条。与 Claude Code AGENTS.md 支持（第 10 条）共同反映当前 AI 编码代理领域的核心趋势：**框架层（harness）设计正成为模型能力之外的关键差异化因素**，行业正从"模型竞赛"转向"代理基础设施竞赛"。

## 社区之声（1-2 条）

### 12. I Vibed a Proof of Conway's Conjecture

| 原文 | [I Vibed a Proof of Conway's Conjecture](https://overreacted.io/how-i-vibed-a-proof-of-conways-conjecture/) |
| --- | --- |
| 热度 | ▲ 204 · 💬 180 · m-hodges · 2026-09-18 |
| 摘要 | React 核心作者 Dan Abramov（GitHub 用户名 danabramov）自述为"数学外行"，用一个月时间和大量 token，借助 AI 模型辅助 Lean 形式化验证，证明了 Conway 50 年未解的 refinement 猹想（超整数的分解性质）。证明已通过 Palomar registry 机器检查，多位熟悉 Lean 和该领域的研究者认为声明正确。Abramov 将此项目定性为"认识论行为艺术"——类似蒙眼玩 Elden Ring——而非声称数学突破。社区讨论聚焦于"wizardry vs sorcery"隐喻：传统编程像巫师依赖深度知识，AI 辅助编程像术士召唤超自然力量。 |

### 13. US Treasuries Have Become Badly Unappetizing for Foreign Central Banks

| 原文 | [US Treasuries Have Become Badly Unappetizing for Foreign Central Banks and Governments](https://wolfstreet.com/2026/09/17/treasuries-have-become-badly-unappetizing-for-foreign-central-banks-governments/) |
| --- | --- |
| 热度 | ▲ 139 · 💬 126 · iamnothere · 2026-09-18 |
| 摘要 | 外国央行持有的美国国债市值降至 $3.77 万亿，回到 2012 年水平，但同期美国国债存量已增长约三倍。外国官方持有占可交易国债比例从 2007-2009 年峰值的 38% 崩塌至 12.8%，为 1993 年以来最低。日本在 2-7 月间减持 $1,350 亿以干预汇市支撑日元；中国大陆和香港自 2015 年以来累计减持 $5,870 亿，占比降至 3.0%。与此同时，不透明金融中心（开曼群岛等）的持有量升至 $3.28 万亿——其中大量是美国对冲基金的杠杆套利仓位和美国企业海外实体的利润存放，而非真正的外国需求。 |

## 数据速览（今日 Top10 全量快照）

| # | 原文标题 | 中文标题 | 分数 | 评论 |
| --- | --- | --- | --- | --- |
| 1 | [I don't like passkeys](https://hawksley.dev/blog/i-dont-like-passkeys) | 我不喜欢 passkeys | 721 | 711 |
| 2 | [Cloudflare Quick Tunnels](https://try.cloudflare.com/) | Cloudflare 快速隧道 | 541 | 237 |
| 3 | [OpenJev](https://openjev.com/) | OpenJev | 534 | 218 |
| 4 | [Hacking OpenAI](https://www.hacktron.ai/blog/hacking-openai) | 破解 OpenAI | 468 | 197 |
| 5 | [Jemalloc 5.4.0](https://github.com/jemalloc/jemalloc/releases/tag/5.4.0) | Jemalloc 5.4.0 发布 | 309 | 79 |
| 6 | [Bend 2 and the Vibe-Coding Trap](https://blog.liampwll.com/posts/bend_vibe_coding/) | Bend 2 与 vibe coding 陷阱 | 309 | 228 |
| 7 | [Warren Buffett Steps Down](https://www.nytimes.com/2026/09/18/business/warren-buffett-berkshire-chairman.html) | 巴菲特卸任伯克希尔董事长 | 286 | 188 |
| 8 | [The Scourge of x86 Emulation](https://fex-emu.com/Scourge-of-emulation/) | x86 模拟的困境 | 260 | 72 |
| 9 | [ZCode silently uploads your Git history](https://tokenstead.ai/guides/zcode-silent-git-history-upload) | ZCode 静默上传 Git 历史 | 256 | 64 |
| 10 | [I Vibed a Proof of Conway's Conjecture](https://overreacted.io/how-i-vibed-a-proof-of-conways-conjecture/) | 我用 vibe 证明了 Conway 猜想 | 204 | 180 |