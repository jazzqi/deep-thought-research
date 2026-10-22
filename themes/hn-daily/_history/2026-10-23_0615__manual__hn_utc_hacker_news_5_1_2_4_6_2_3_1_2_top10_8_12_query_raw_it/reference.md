# 数据来源溯源（增量补丁 10-22 UTC 窗口）

- Amazon MadPot 披露 PHP2Shell 披露前在野利用: query_raw_items(source=hackernews, published_after=2026-10-22T00:00Z)[id:505051] = AWS 威胁情报 MadPot 于 10-17 公开披露前已观测到 PHP2Shell 利用（fetch_url 抓 AWS 博客失败，仅标题/摘要）
- eMudhra 退出全球 SSL/TLS 证书业务（14h 内吊销、约占全球收入 1%、舆论放大不成比例）: fetch_url(https://emudhra.com/en/press-release/emudhra-to-exit-global-ssl-tls-certificate-business) = 董事会 2026-10-22 官方公告全文（BSE: 543533）；条目热度: query_raw_items(source=hackernews)[id:505378] = ▲861 💬594（快照）
- 澳 Epic v Apple 判决（侧载/替代商店/第三方支付，2026FCA1552）: query_raw_items(source=hackernews)[id:502669] = ▲173 💬129，判决书原文链接（未逐页抓取）
- Quad9 退出法国（罚款 58 万欧→1000 欧/日，2026-11-24 生效，beIN 版权域名阻塞）: fetch_url(https://quad9.net/news/blog/au-revoir-france/) = 官方博客全文；条目热度: query_raw_items(source=hackernews)[id:505606] = ▲153 💬43（快照）
- Xbox 串流按小时收费 24-40 美分: query_raw_items(source=hackernews)[id:505050] = ▲88 💬128，Ars Technica 报道（正文未逐段抓取）
- OpenAI CLI 开源: query_raw_items(source=hackernews)[id:503216] = ▲224 💬108，github.com/openai/openai-cli（README 定位转述）
- WorldTUI 360M 终端世界模型（Qwen2.5-Coder-0.5B 微调、Docker 会话训练、行并行解码）: fetch_url(https://simedw.com/2026/10/21/world-model-terminal/) = 作者博客全文；条目热度: query_raw_items(source=hackernews)[id:503030] = ▲457 💬148（快照）
- Switch 2 越狱 ns2jb（固件 23.0.1、tethered、Codex harness、WebKit n-day、约两周）: fetch_url(https://pepsipu.com/blog/2026-10-switch2-jailbreak-ns2jb/) = 作者博客全文；条目热度: query_raw_items(source=hackernews)[id:504838] = ▲572 💬206（快照）
- pwn.watch 看板（40 起在追踪/21 已修/12 个月 239 起）: fetch_url(https://pwn.watch/) = 页面实时数据（2026-10-22 23:58 UTC 更新）；条目热度: query_raw_items(source=hackernews)[id:505541] = ▲311 💬147（快照）
- Tell HN PHP 禁运道歉帖（265 分/109 评论为 HN 页面抓取时点值）: fetch_url(https://news.ycombinator.com/item?id=50193416) = HN 帖文及评论全文；条目: query_raw_items(source=hackernews)[id:504820] = 快照 ▲91 💬16
- Cash App 女子案: query_raw_items(source=hackernews)[id:505259] = ▲260 💬261，Techspot 报道（正文未逐段抓取）
- 基线对照（10-22 版定版内容）: ReadThemeDocsTool(themes/hn-daily/2026-10-22.md) = 快照 2026-10-22T01:15 UTC，头条/共识/少数派跟踪条件


- eMudhra 退出全球 SSL/TLS 证书业务（2026-10-22 公告，SSL/TLS 占全球收入约1%，14小时内吊销受影响CA）: query_raw_items(source=hackernews, published_after=2026-10-22T00:00:00Z, published_before=2026-10-23T00:00:00Z)[id:505378] = eMudhra to Exit Global SSL/TLS Certificate Business（正文经 fetch_url 抓取 emudhra.com 新闻稿）
- eMudhra 弱钥根因（2025-04-30 密钥仪式 wrap/unwrap 脚本缺陷产生弱密钥集、员工误用，"多个人为错误"）: query_raw_items(source=hackernews)[id:505378] + fetch_url(https://news.ycombinator.com/item?id=50195110) = HN 高赞评论 overtomanu 引 Mozilla 追踪器
- CVE-2026-111943 被入侵中间 CA: query_raw_items(source=hackernews, 10-22窗口)[id:504147] = NVD 条目，HN 讨论串
- WorldTUI 360M 终端世界模型（基于 Qwen2.5-Coder-0.5B 微调、333 token 词表、语法约束解码、208MB WebGPU 浏览器 demo、自纠错训练为最有效改动）: query_raw_items(source=hackernews, 10-22窗口)[id:503030] = 正文经 fetch_url 抓取 simedw.com + HN 评论页
- OpenAI 官方 CLI（Go 实现，与 Codex CLI 分工：openai 管低层 API/codex 管 agent）: query_raw_items(source=hackernews, 10-22窗口)[id:503216] = fetch_url 抓取 github.com/openai/openai-cli README 及 HN 评论页
- O(n log n) 整数乘法论文（UNSW David Harvey 等）及 Lean 形式化（platypii/jdb1729，Mathlib TM2，指数至 1-2^-14.38）: query_raw_items(source=hackernews, 10-22窗口)[id:502716] = fetch_url 抓取 HN 评论页（PDF 抓取返回二进制未解析）
- Switch 2 越狱 ns2jb（固件 23.0.1、WebKit n-day 经强制门户、Codex 参与、越狱约两周、Mario Kart World 改版一天完成）: query_raw_items(source=hackernews, 10-22窗口)[id:504838] = fetch_url 抓取 pepsipu.com 正文
- AI 与科学公地圈地论文（arXiv:2610.27251，哈佛-史密松 P. K. G. Williams，14页，2026-10-19 提交）: query_raw_items(source=hackernews, 10-22窗口)[id:506081] = fetch_url 抓取 arXiv 摘要页
- NVIDIA OpenShell（agent 沙箱：内核级强制文件/系统调用/网络策略，策略变更前形式化验证，agent 不接触真实凭证）: query_raw_items(source=hackernews, 10-22窗口)[id:505978] = fetch_url 抓取 GitHub README 及 HN 评论页
- Minotaur 无 LLM 推理宣称与社区拆台（无可试 demo、论文未落地 507 报错、帖子被 flag）: query_raw_items(source=hackernews, 10-22窗口)[id:504379] = fetch_url 抓取 fleetingswallow.com 正文及 HN 评论页
- 12 模型"对人类最反直觉看法"趋同（10 家实验室 3 国，全部至少一次给出"忠于归属而非真理"，7/12 三次全中）: query_raw_items(source=hackernews, 10-22窗口)[id:505874] = fetch_url 抓取 modelcompare.ai 正文
- Ask HN 前沿实验室为何不自开 100 家公司（回复要点：token 抽成是唯一验证过的增长收入、借贷利率上升致 runway 收紧、Jevons 赌注）: query_raw_items(source=hackernews, 10-22窗口)[id:506244] = fetch_url 抓取 HN 讨论页

# HN 书摘 · 2026-10-23 取数来源

- eMudhra 退出全球 SSL/TLS 业务声明（受影响 CA 14 小时内吊销、未签发终端实体证书、SSL/TLS 约占全球收入 1%、G1 RSA 根过渡期安排）: fetch_url('https://emudhra.com/en/press-release/emudhra-to-exit-global-ssl-tls-certificate-business') = eMudhra Limited 新闻稿 2026-10-22
- eMudhra 退出帖热度: query_raw_items(source=hackernews, published_after=2026-10-21T20:00:00Z, published_before=2026-10-22T22:40:00Z, min_points=60)[id:505378] = ▲861/💬594, 作者 bo0tzz, 2026-10-22 13:33 UTC
- eMudhra 事件根因（2025-04-30 HSM 密钥仪式、wrap 脚本生成第二套更弱密钥、命名相似导致误用、"多个人为错误"）: fetch_url('https://news.ycombinator.com/item?id=50195110') = HN 评论 overtomanu 引 theprint.in, 及 wolvoleo/silisili 跟帖
- PHP RCE 反证文（数千个 LLM 生成 PoC 均不中原生 PHP、多依赖 LFI 前置、LLM 自证式作弊）: fetch_url('https://eliastaylor.com/noexploit/') = eliastaylor 博文全文
- PHP 帖评论区交锋（tptacek 称研究团队已有可用 RCE PoC 但拒绝给证据、承认无人公开分享）: fetch_url('https://news.ycombinator.com/item?id=50188948') = HN 评论页
- PHP 反证文热度演化（昨日 ▲31/0 评论 → 今日 ▲604/💬420）: query_raw_items(...同上窗口)[id:502221] = ▲604/💬420, 作者 zkldi, 2026-10-21 23:13 UTC；昨日基线见 themes/hn-daily/2026-10-22.md 头条 1 kevin_kelly 视角
- Switch 2 越狱 ns2jb（WebKit 三重缓解、Switch 1 游戏切入、JetKVM+蓝牙开关 Codex harness、2 周人工攻坚、马力欧卡丁车世界改模 vibe-coded）: fetch_url('https://pepsipu.com/blog/2026-10-switch2-jailbreak-ns2jb/') = 博文全文
- Railway 环境变量泄露与"针对 AI 推理服务商的系列攻击"定性、部署全停: fetch_url('https://blog.railway.com/p/security-disclosure-wednesday-october-21st') = Railway 安全披露 2026-10-21
- Railway 事件热度: query_raw_items(...同上窗口)[id:502064] = ▲571/💬329, 作者 passenger, 2026-10-21 21:58 UTC
- pwn.watch 指标（40 起活跃/19 critical、近 12 个月 239 起、距上次无事件日 0 天、Copy brief for your AI/llms.txt）: fetch_url('https://pwn.watch/') = 站点抓取 2026-10-22
- o(n log n) 整数乘法论文条目热度: query_raw_items(...同上窗口)[id:502716] = ▲285/💬240, 作者 craigcitro, 2026-10-22 02:30 UTC
- 该论文 Lean 形式化进展（platypii 与 jdb1729 在 Mathlib TM2 机器完成形式化、登录墙与"已完成"任务争议）: fetch_url('https://news.ycombinator.com/item?id=50190455') = HN 评论页；PDF 正文 fetch_url 返回二进制流，未能核验论文内容
- OpenAI CLI 定位与功能（官方 REST API CLI、Go、与 Codex CLI 分工、gpt-6-astra 文档示例）: fetch_url('https://github.com/openai/openai-cli') = README
- OpenAI CLI 评论之争（curl 等长命令、API key 泄漏进进程树 vs 可发现性/OAuth、AX 缺位）: fetch_url('https://news.ycombinator.com/item?id=50191507') = HN 评论页
- OpenAI CLI 热度: query_raw_items(...同上窗口)[id:503216] = ▲224/💬108, 作者 armcat, 2026-10-22 05:23 UTC
- WorldTUI 技术方案（360M、Qwen2.5-Coder-0.5B 微调、行级改写/COPY/WAIT/并行列解码、自修复训练、WebGPU 208MB）: fetch_url('https://simedw.com/2026/10/21/world-model-terminal/') = 博文全文
- WorldTUI 热度: query_raw_items(...同上窗口)[id:503030] = ▲457/💬148, 作者 alphax314, 2026-10-22 02:18 UTC
- NVIDIA OpenShell 架构（内核级强制、策略形式化验证、凭证不落地、Rust、0.1.x）: fetch_url('https://github.com/NVIDIA/OpenShell') = README
- OpenShell 热度: query_raw_items(...同上窗口)[id:505978] = ▲73/💬35, 作者 niemandhier, 2026-10-22 17:44 UTC
- Claude for Google Workspace 公测（侧边栏、就地编辑、Ask before edits/Accept all edits、Docs/Sheets/Slides 连接器、CMEK/Compliance API/OpenTelemetry）: fetch_url('https://claude.com/resources/articles/claude-now-works-in-google-docs-sheets-and-slides') = Anthropic 官方文
- Claude Workspace 热度: query_raw_items(...同上窗口)[id:503471] = ▲83/💬10, 作者 gmays, 2026-10-22 02:17 UTC
- Tell HN 禁运致歉正文与评论（john_strinlai/cperciva/user43928）: fetch_url('https://news.ycombinator.com/item?id=50193416') = 正文+评论页
- Tell HN 热度: query_raw_items(...同上窗口)[id:504820] = ▲91/💬16, 作者 petecooper, 2026-10-22 10:11 UTC
- Ask HN"为什么不开 100 家公司"正文与高赞回答（CoolestBeans 五点、nl 纠正债务口径、dofm 引 Alex Karp）: fetch_url('https://news.ycombinator.com/item?id=50200997') = 正文+评论页
- Ask HN 热度: query_raw_items(...同上窗口)[id:506244] = ▲25/💬18, 作者 ex-aws-dude, 2026-10-22 21:03 UTC
- mitmproxy --emudhra 选项（certifi 移除 eMudhra CA + 用泄露密钥签名的测试开关）: fetch_url('https://github.com/mitmproxy/mitmproxy/commit/169234499088fc2c414644a67efaed3d64ae2e3b') = commit diff
- mitmproxy 帖热度: query_raw_items(...同上窗口)[id:502257] = ▲585/💬139, 作者 ahlCVA, 2026-10-21 23:51 UTC
- CVE-2026-111943 条目热度（Compromised Intermediate Certificate Authority）: query_raw_items(...同上窗口)[id:504147] = ▲327/💬114, 作者 keks24, 2026-10-22 08:51 UTC；NVD 页面 fetch_url 仅返回站头，正文未核验
- Cash App 条目（Top10 快照用）: query_raw_items(...同上窗口)[id:505259] = ▲260/💬261, 作者 oidar, 2026-10-22 13:11 UTC
- eMudhra 上市主体（BSE:543533 | NSE:EMUDHRA）行情/财务: 数据缺失——长桥接口仅覆盖港股/美股/A股/新加坡，印度股票未覆盖，本文未引用任何该标的行情数据
- 取数窗口与管道: query_raw_items(source=hackernews, status=processed, published_after=2026-10-21T20:00:00Z, published_before=2026-10-22T22:40:00Z, min_points=60) = 33 条；另以 keyword='AI OR LLM OR model OR GPT OR Claude' 窗口查询复核 30 条

- Cash App 冒名账户案 HN 帖热度（▲260/💬261 快照值）: query_raw_items(keyword='prison', source='hackernews', 2026-10-21→10-23)[id:505259] = Woman faces six years in prison over Cash App account she never opened
- Cash App 案评论摘录（认罪交易陷阱，作者 benjiro29）: fetch_url(https://news.ycombinator.com/item?id=50194833) = 检方已向 Smith 提供认罪协议（$1,000 罚款 + $1,000 赔偿 + 3 年缓刑），评论指出大量无辜者因诉讼成本接受认罪协议
- Ask HN「模型这么好 OpenAI 为何不开 100 家公司」（▲25/💬18）: query_raw_items(keyword='Cash App', 2026-10-21→10-23)[id:506244] = 社区质疑 frontier lab 卖 token 模式，主张应用层价值更大
- eMudhra 退出 SSL/TLS 业务（▲861/💬594）: 由第 2 棒核验（emudhra.com 新闻稿 + HN 评论页），沿用未重复查询
- PHP RCE 证据战争（AWS 蜜罐 10-17 探测 + tptacek 对线）: 由第 2 棒核验（eliastaylor.com + AWS 帖 + HN 评论页），沿用未重复查询
- Quad9 退出法国、o(n log n) 论文、WorldTUI、ns2jb、pwn.watch、OpenAI CLI、NVIDIA OpenShell、Google 芬兰、Xbox 串流计费: 由第 2 棒 fetch_url 核验，沿用未重复查询
