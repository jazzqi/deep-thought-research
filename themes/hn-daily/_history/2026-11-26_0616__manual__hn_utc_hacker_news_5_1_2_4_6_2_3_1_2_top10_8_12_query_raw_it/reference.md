# 数据溯源 · HN 书摘 2026-11-26（11-25 UTC 窗口）

## 取数口径
- 候选池: query_raw_items(source=hackernews, min_points=20, published_after=2026-11-25T00:00:00Z, published_before=2026-11-26T00:00:00Z) = 54 条（≥20 points 阈值）
- 口径陷阱: 标题 ▲ 前缀（如 ▲878）与 metadata.hn_points（如 Points: 25）是两套量，机械过滤以 Points 字段为准；正文热度行 ▲ 值来自标题前缀快照

## 引用条目（query_raw_items，保留 id 供打分）
- Matrix Multiplication is O(n^2.25): query_raw_items(source=hackernews,min_points=20,11-25窗口)[id:818395] = ▲878/💬491，OpenAI 证明 ω=9/4 含匹配下界
- Google Releases Cogentic Papers on Integer Factorization: query_raw_items(source=hackernews,min_points=20,11-25窗口)[id:820921] = ▲404/💬314，11/25 新增 6 篇（整数分解/离散对数/1/5近似Nash/Log-Rank/边重构等）
- Holy Shit [Algorithmic Complexity Lower Bounds]: query_raw_items(source=hackernews,min_points=20,11-25窗口)[id:821687] = ▲173/💬101，Aaronson 确认 ω=9/4、傅里叶线性门下界、QIP(2)=PSPACE
- SpaceX wins FCC approval to deploy 1M orbital data center satellites: query_raw_items(source=hackernews,min_points=20,11-25窗口)[id:821686] = ▲43/💬64，CNBC 源
- US authorizes SpaceX to deploy 1M satellites: query_raw_items(source=hackernews,min_points=20,11-25窗口)[id:821705] = ▲22/💬14，Reuters 源（双源交叉）
- U.S. jury convicts Huawei of fraud, Iran sanctions violations: query_raw_items(source=hackernews,min_points=20,11-25窗口)[id:821094] = ▲151/💬182
- 1Password Security Incident: query_raw_items(source=hackernews,min_points=20,11-25窗口)[id:821485] = ▲133/💬58
- Taking over US Treasury subdomains for $3 each: query_raw_items(source=hackernews,min_points=20,11-25窗口)[id:819154] = ▲215/💬46
- Anthropic migrated Messages API to Rust with no Rust developers: query_raw_items(source=hackernews,min_points=20,11-25窗口)[id:821420] = ▲27/💬6
- I checked Clojure's core with Lean and found unreported bugs: query_raw_items(source=hackernews,min_points=20,11-25窗口)[id:821443] = ▲56/💬20
- Serving Qwen via AWS Lambdas for fun and 80x negative profit: query_raw_items(source=hackernews,min_points=20,11-25窗口)[id:818905] = ▲125/💬18
- Why aren't we working 2-days a week?: query_raw_items(source=hackernews,min_points=20,11-25窗口)[id:821573] = ▲47/💬56
- Rumors swirling that labs might have cracked Factoring in P: query_raw_items(source=hackernews,min_points=20,11-25窗口)[id:821301] = ▲67/💬32（用于对比社区质疑强度）
- Button Sounds: query_raw_items(source=hackernews,min_points=20,11-25窗口)[id:818728] = ▲751/💬119（用于 points/评论比价值错配论据）
- Wall Street Expects Anthropic's Committed $900B Debt to Be Junk: query_raw_items(source=hackernews,min_points=20,11-25窗口)[id:821669] = ▲20/💬4（用于共识5剪刀差论据）

## 正文抓取（fetch_url）
- Google Cogentic 论文目录: fetch_url(github.com/google-research/google-research/tree/master/cogentic_research_papers) = 11/25 新增 6 篇（无条件整数分解 L_N[1/3,O(1)]、固定特征离散对数次拟多项式、1/5近似Nash精确多项式、确定性次指数分解与二次非剩余、Log-Rank 破平方根壁垒、线性密度边重构），标注"非 Google 官方产品"
- Aaronson HOLY SHIT 正文: fetch_url(scottaaronson.blog/?p=10379) = 确认 ω=9/4 匹配下界、傅里叶线性门 N(log N)^(1/2+o(1))、QIP(2)=PSPACE、Alpöge/Anthropic 黎曼猜想证明、"新大陆/显微镜/望远镜"类比
- Anthropic Rust 迁移正文: fetch_url(anthropic.com/research/migrating-api-to-rust) = 流量 2024初→2026秋增长约1800倍、Claude 约一周写出核心请求路径首版、把生产 API 当 verifier、CPU -70%、TTFT -20%、未下线服务
- Clojure Lean 验证正文: fetch_url(s.conao3.com/blog/2026/e4f733) = Clojure 1.12.7+JDK21、17 个未报告 bug、bv_decide 反例搜索、HAMT 300万次差分测试无异常
- iOS Safari 60fps 正文: fetch_url(rida.dev/blog/bypassing-ios-safari-60-fps-limit) = WebKit 把 rAF 限制在 60Hz（120Hz 屏）、用 compositor 滚动绕过（未入选正文，仅备查）
- 每周两天工作正文: fetch_url(anihil.com/why-arent-we-working-2-days-a-week) = AI 生产力红利未转化为休闲、反表现为裁员与不稳定
- 矩阵乘法 HN 评论: fetch_url(news.ycombinator.com/item?id=50637220) = zone411 高赞评论（4篇论文解决 Top500 中8个、源自同一底层框架）、idontneedcoffee 质疑（护城河是训练基础设施而非架构）
- Anthropic Rust HN 评论: fetch_url(news.ycombinator.com/item?id=50644162) = 标题党质疑（"无 Rust 开发者"原文无据）、"验证是新瓶颈"（作者 dadadad100）
- Reuters SpaceX: fetch_url(reuters.com/...spacex...) = 401 Forbidden，正文未抓取，仅用标题事实
- LessWrong 模型通信: fetch_url(lesswrong.com/...) = 429 Too Many Requests，未抓取（未入选正文）

- AI for Math 集群（OpenAI ω=9/4, Google cogentic, Aaronson 确认, Hirsch 反例）: query_raw_items(source='hackernews', published_after='2026-11-25T00:00:00Z', published_before='2026-11-26T12:00:00Z')[id:818395,id:820921,id:821687,id:821720] = ▲878/💬491, ▲404/💬314, ▲173/💬101, ▲29/💬1（入库快照）
- Aaronson 博文细节（ω=9/4 匹配下界、FFT N(logN)^(1/2+o(1))、QIP(2)=PSPACE、RH 提及）: fetch_url(https://scottaaronson.blog/?p=10379) = 正文确认
- Anthropic Messages API Rust 迁移（1800x 流量、~1周首版、CPU -70%、TTFT -20%、无下线）: fetch_url(https://www.anthropic.com/research/migrating-api-to-rust) + query_raw_items[id:821420] = ▲27/💬6
- 1Password 安全事件（11/19 调查、员工 GitHub 账户、恶意代码、姓名/邮箱/邀请令牌泄露、vault/密钥未受影响）: fetch_url(https://1password.com/blog/update-on-nov-2026-security-incident) + query_raw_items[id:821485] = ▲133/💬58
- SpaceX FCC 轨道数据中心批准（100万颗上限）: query_raw_items[id:821686,id:821705] = ▲43/💬64, ▲22/💬14；CNBC/Reuters 正文抓取失败，标题确认
- 华为欺诈/伊朗制裁裁决: query_raw_items[id:821094] = ▲151/💬182；UPI 正文抓取失败，标题确认
- Factoring in P 传闻帖: query_raw_items[id:821301] = ▲67/💬32（未证实传闻）
- 自动证明死胡同论文: query_raw_items[id:820086] = ▲37/💬60
- Anthropic 9000B 债务被判垃圾级: query_raw_items[id:821669] = ▲20/💬4
- Lean 检查 Clojure 核心发现 17 bugs: query_raw_items[id:821443] = ▲56/💬20
- 5600 Lambda 跑 Qwen 80x 负利润: query_raw_items[id:818905] = ▲125/💬18
- 每周工作两天讨论: query_raw_items[id:821573] = ▲47/💬56
- 美国财政部子域接管: query_raw_items[id:819154] = ▲215/💬46

# Reference

- OpenAI 矩阵乘法 ω=9/4 预印本（HN ▲878/💬491, hn_points=25）: query_raw_items(source='hackernews', published_after='2026-11-25T00:00:00Z', published_before='2026-11-26T00:00:00Z', min_points=20)[id:818395] = Matrix Multiplication is O(n^2.25) [pdf]
- Google cogentic 论文集群（HN ▲404/💬314, hn_points=30）: query_raw_items(...)[id:820921] = Google Releases Cogentic Papers on Integer Factorization, Discrete Logs and More
- Aaronson 算法复杂度下界长文（HN ▲173/💬101, hn_points=27）: query_raw_items(...)[id:821687] = Holy Shit Holy Shit Holy Shit Holy Shit [Algorithmic Complexity Lower Bounds]; fetch_url(https://scottaaronson.blog/?p=10379) = 确认 ω=9/4 匹配下界、FFT N(log N)^(1/2+o(1))、QIP(2)=PSPACE、提及 Alpöge/Anthropic 黎曼猜想证明
- OpenAI Hirsch 猜想反例（HN ▲29/💬1, hn_points=22）: query_raw_items(...)[id:821720] = The polynomial Hirsch conjecture is false [pdf]
- SpaceX FCC 轨道数据中心批准（CNBC, HN ▲43/💬64, hn_points=24）: query_raw_items(...)[id:821686] = SpaceX wins FCC approval to deploy 1M orbital data center satellites
- SpaceX FCC 批准（Reuters 双源, HN ▲22/💬14, hn_points=20）: query_raw_items(...)[id:821705] = US authorizes SpaceX to deploy 1M satellites for data centers in space
- 华为欺诈/伊朗制裁裁决（HN ▲151/💬182, hn_points=27）: query_raw_items(...)[id:821094] = U.S. jury convicts Huawei of fraud, Iran sanctions violations
- 1Password 安全事件（HN ▲133/💬58, hn_points=41）: query_raw_items(...)[id:821485] = 1Password Security Incident; fetch_url(https://1password.com/blog/update-on-nov-2026-security-incident) = 11/19 起调查，攻击者经员工 GitHub 账户推送恶意代码，窃取部分客户姓名/邮箱/邀请令牌等非密钥元数据，vault 与密钥未受影响，已轮换凭证
- Anthropic Messages API Rust 迁移（HN ▲27/💬6, hn_points=21）: query_raw_items(...)[id:821420] = Anthropic migrated Messages API to Rust with no Rust developers; fetch_url(https://www.anthropic.com/research/migrating-api-to-rust) = 2024初至2026秋流量约1800倍增长，Claude约一周写出核心请求路径首版，生产API作verifier，每请求CPU降约70%、首token延迟降约20%，未下线/未冻结开发
- Lean 验证 Clojure 核心发现 17 个 bug（HN ▲56/💬20, hn_points=20）: query_raw_items(...)[id:821443] = I checked Clojure's core with Lean and found unreported bugs
- 5600 个 AWS Lambda 跑 Qwen 80 倍负利润（HN ▲125/💬18, hn_points=25）: query_raw_items(...)[id:818905] = Serving Qwen via AWS Lambdas for fun and 80x negative profit
- 每周工作两天讨论（HN ▲47/💬56, hn_points=33）: query_raw_items(...)[id:821573] = Why aren't we working 2-days a week?
- 因式分解传闻帖（HN ▲67/💬32, hn_points=44）: query_raw_items(...)[id:821301] = Rumors swirling that labs might have cracked Factoring in P
- 自动化证明死胡同论文（HN ▲37/💬60, hn_points=21）: query_raw_items(...)[id:820086] = Why Automated Proof-Solving Is the Same Old Dead End
- Anthropic 9000B 债务被预期为垃圾级（HN ▲20/💬4, hn_points=20）: query_raw_items(...)[id:821669] = Wall Street Expects Anthropic's Committed $900B Debt to Be Junk
- Button Sounds 高分娱乐帖（HN ▲751/💬119, hn_points=22）: query_raw_items(...)[id:818728] = Button Sounds – collection of professionally-recorded button clicks and presses
- 模型经推理服务器沙箱通信（HN ▲395/💬169, hn_points=22）: query_raw_items(...)[id:818633] = Models Can Communicate via Inference Servers Despite Being Sandboxed
