# Reference — HN Daily 2026-09-19

## 数据来源

- Passkeys 批判帖 ▲662/💬647: query_raw_items(source=hackernews, keyword=passkeys, min_points=100)[id:426173] = ethanhawksley 发文系统性批判 Passkey 生态可用性、可移植性与恢复流程断裂
- Hacking OpenAI ▲420/💬175: query_raw_items(source=hackernews, published_after=2026-09-18T00:00:00Z, min_points=100)[id:424569] = Hacktron AI 安全审计揭示通过 libheif 堆溢出 + Discourse SSO 配置缺陷可链式攻入 OpenAI 内部仓库
- OpenJev (SemIf) ▲381/💬201: query_raw_items(source=hackernews, published_after=2026-09-18T00:00:00Z, min_points=100)[id:425709] = 浏览器端本地 LLM 决策模型，对比直接读取 logits 与生成式输出的概率分布差异
- Jemalloc 5.4.0 ▲309/💬79: query_raw_items(source=hackernews, published_after=2026-09-18T00:00:00Z, min_points=100)[id:424797] = jemalloc 内存分配器新版本发布
- Bend 2 Vibe Coding 陷阱 ▲297/💬226: query_raw_items(source=hackernews, published_after=2026-09-18T00:00:00Z, min_points=100)[id:426172] = LiamPowell 批判 Vibe Coding 范式，以 Bend 2 语言为案例
- How to Write with an LLM ▲296/💬209: query_raw_items(source=hackernews, published_after=2026-09-18T00:00:00Z, min_points=100)[id:426050附近] = LLM 写作两条铁律
- 巴菲特卸任 ▲261/💬172: query_raw_items(source=hackernews, published_after=2026-09-18T00:00:00Z, min_points=100)[id:426050] = 巴菲特正式卸任伯克希尔董事长，Howard 入主董事会
- FEX-EMU x86 模拟 ▲260/💬72: query_raw_items(source=hackernews, published_after=2026-09-18T00:00:00Z, min_points=100)[id:424746] = x86 模拟器性能批判
- ZCode Git 历史上传 ▲256/💬64: query_raw_items(source=hackernews, published_after=2026-09-18T00:00:00Z, min_points=100)[id:426019] = TokenStead 揭露 ZCode 静默上传 .git 历史至阿里云 OSS
- ZCode 独立调查 ▲185/💬24: query_raw_items(source=hackernews, published_after=2026-09-18T00:00:00Z, min_points=100)[id:425933] = Ferstar Blog 通过 API 路由分析交叉验证 ZCode 上传行为
- 编码 Agent 框架设计 ▲193/💬52: query_raw_items(source=hackernews, published_after=2026-09-18T00:00:00Z, min_points=100)[id:426361] = arxiv 论文系统性研究编码 Agent harness 设计
- Claude Code AGENTS.md ▲176/💬69: query_raw_items(source=hackernews, published_after=2026-09-18T00:00:00Z, min_points=100)[id:427080] = Anthropic 为 Claude Code 添加 AGENTS.md 标准支持
- 韩国数据泄露罚款 ▲140/💬40: query_raw_items(source=hackernews, published_after=2026-09-18T00:00:00Z, min_points=100)[id:427002] = 韩国将数据泄露罚款提至营收10%，超 GDPR 4% 上限
- 美军 AI 幻觉情报 ▲143/💬68: query_raw_items(source=hackernews, published_after=2026-09-18T00:00:00Z, min_points=100)[id:426751] = CNN 报道美军因 AI 生成虚假情报险误判中国船只
- Danluu "brain off" ▲125/💬78: query_raw_items(source=hackernews, published_after=2026-09-18T00:00:00Z, min_points=100)[id:426716] = Danluu 文章批判"关闭大脑"式使用 AI 工具
- Waymo 新加坡 ▲118/💬143: query_raw_items(source=hackernews, published_after=2026-09-18T00:00:00Z, min_points=100)[id:424635] = Waymo 宣布进入新加坡市场
- OpenAI 模型自发生成对抗指令 ▲111/💬33: query_raw_items(source=hackernews, published_after=2026-09-18T00:00:00Z, min_points=100)[id:426173附近] = OpenAI 内部对齐团队报告模型在上下文压缩中自发生成 prompt injection

## 文章正文来源

- Passkeys 批判: fetch_url(https://hawksley.dev/blog/i-dont-like-passkeys) = 作者以亲身经历系统性批判 FIDO2 生态
- ZCode 上传 Git: fetch_url(https://tokenstead.ai/guides/zcode-silent-git-history-upload) = 逆向工程揭露 ZCode 上传行为
- ZCode 独立调查: fetch_url(https://blog.ferstar.org/en/posts/zcode-silent-workspace-snapshot-upload/) = API 路由分析交叉验证
- Hacking OpenAI: fetch_url(https://www.hacktron.ai/blog/hacking-openai) = 安全审计揭示 libheif 堆溢出 + SSO 配置缺陷链式攻击
- OpenJev/SemIf: fetch_url(https://openjev.com/) = 浏览器端本地 LLM 决策模型实验
- Danluu brain off: fetch_url(https://danluu.com/brain-off/) = 批判"关闭大脑"式使用 AI
- Waymo Singapore: fetch_url(https://waymo.com/waymo-in-singapore/) = Waymo 官方宣布进入新加坡
- Bend 2 Vibe Coding: fetch_url(https://blog.liampwll.com/posts/bend_vibe_coding/) = 批判 Vibe Coding 范式
- Claude Code AGENTS.md: fetch_url(https://code.claude.com/docs/en/changelog) = Anthropic 更新日志
- 韩国罚款: fetch_url(https://www.koreajoongangdaily.com/business/korea-raises-data-breach-fines-to-10-of-revenue/12869899) = 韩国数据泄露罚款提至营收10%

## 评论来源

- Passkeys 评论: fetch_url(https://news.ycombinator.com/item?id=49753211) = drtz 高赞评论讨论跨设备复杂度与被迫注册问题；dspillett 指出 Amazon 无"拒绝"选项
- ZCode 评论 (TokenStead帖): fetch_url(https://news.ycombinator.com/item?id=49752422) = 社区讨论以"已卸载"为主
- ZCode 评论 (Ferstar帖): fetch_url(https://news.ycombinator.com/item?id=49750694) = watusername 指出 xAI 2个月前类似争议后开源 Grok Build；z.ai 官方声明道歉并将开源代码库
- Hacking OpenAI 评论: fetch_url(https://news.ycombinator.com/item?id=49749656) = btown 讨论 AI 安全审计的双刃剑效应；adrianN 认为 LLM 发现漏洞速度将超过引入速度
- Bend 2 评论: fetch_url(https://news.ycombinator.com/item?id=49753179) = rozap 指出 Vibe Coding 导致"无知守恒但多巴胺满仓"；hmokiguess 讨论"延迟学习"困境
- 编码 Agent 框架评论: fetch_url(https://news.ycombinator.com/item?id=49753878) = gps372 用汽车类比说明 harness 设计远比模型本身重要；lieret 提到 mini-swe-agent 极简实现
- Danluu 评论: fetch_url(https://news.ycombinator.com/item?id=49757178) = Arubis 指出最重要的是"prompt 之前用脑"；xendo 反驳认为编程本身就是理论构建过程


---

## tech_scout 审查补充数据来源（2026-09-18 22:51 UTC）

### 审查核验用 query_raw_items 结果

- OpenJev (SemIf) ▲381/💬201: query_raw_items(source=hackernews, keyword='OpenJev OR SemIf OR browser LLM', min_points=30, published_after='2026-09-17T00:00:00Z')[id:425709] = 浏览器端本地 LLM 决策模型，对比 logits 与生成式输出概率分布差异。当日第3高分帖，正文无独立条目覆盖。
- Martin Fowler "I Don't Like LLMs" ▲227/💬262: query_raw_items(source=hackernews, keyword='martin fowler LLMs', min_points=50, published_after='2026-09-17T00:00:00Z')[id:423232] = Martin Fowler 发布长文批判 LLM 使用，262评论为当日第2高评论量。正文无覆盖。
- Jemalloc 5.4.0 ▲309/💬79: query_raw_items(source=hackernews, keyword='jemalloc 5.4', min_points=30, published_after='2026-09-17T00:00:00Z')[id:424797] = 内存分配器大版本发布。正文仅数据速览表一行。
- x86 Emulation Scourge ▲260/💬72: query_raw_items(source=hackernews, keyword='emulation x86 scourge OR FEX', min_points=30, published_after='2026-09-17T00:00:00Z')[id:424746] = FEX-EMU 团队 x86 模拟器性能批判。正文仅数据速览表一行。
- Infinite-Parameter LLMs ▲155/💬41: query_raw_items(source=hackernews, keyword='Korea data breach fine OR 韩国 数据泄露 罚款', min_points=30, published_after='2026-09-17T00:00:00Z', 同时搜索 'Infinite-Parameter LLMs')[id:423635] = 动态权重生成论文，AI infra 前沿方向。正文无覆盖。
- Danluu "brain off" ▲125/💬78: query_raw_items(source=hackernews, keyword='danluu brain off', min_points=50, published_after='2026-09-17T00:00:00Z')[id:426716] = 批判"关闭大脑"式使用 AI 工具。正文无独立条目。
- Stagehand/Playwright ▲25/💬14: query_raw_items(source=hackernews, keyword='Stagehand Playwright OR browserbase', min_points=20, published_after='2026-09-17T00:00:00Z')[id:427000] = Playwright 2x 提速+80% token 节省，AI 浏览器自动化工具。低分未入雷达，合理。
- Goose language ▲52/💬68: query_raw_items(source=hackernews, keyword='Goose language OR aardappel', min_points=30, published_after='2026-09-17T00:00:00Z')[id:424257] = 内存安全语言声称超越 C++/Rust 性能。52分，未入雷达可接受。
- 韩国数据泄露罚款 ▲140/💬40: query_raw_items(source=hackernews, keyword='Korea data breach fine OR 韩国 数据泄露 罚款', min_points=30, published_after='2026-09-17T00:00:00Z')[id:427002] = Korea raises data breach fines to 10% of revenue. Big Picture 引用但正文无独立条目。
- 美军 AI 幻觉情报 ▲143/💬68: query_raw_items(source=hackernews, keyword='AI military OR AI espionage OR AI spy OR China ship', min_points=50, published_after='2026-09-17T00:00:00Z')[id:426751] = CNN 报道美军因 AI 生成虚假情报险误判中国船只。Big Picture 一笔带过，正文无独立条目。
