# 参考来源 — HN 书摘 · 2026-10-05（窗口 2026-10-03T22:54Z ~ 2026-10-04T23:00Z）

> 内部 raw_items 的 hackernews 源自 2026-09-23 后零入库（断档第 12 天，query_raw_items 复核仍为陈旧条目）。
> 本期条目数据全部来自 Algolia HN 公开 API（fetch_url 兜底，抓取于 2026-10-04T23:00Z 前后），无内部 raw_item id，
> 未触发引用打分（RescoreRawItemTool 仅适用于 query_raw_items 返回的 [id:N] 条目）。

## 条目热度与元数据（Algolia API）

- Strata（Qwen 3.8 Flash Next 125B 本地运行）: fetch_url(hn.algolia.com search_by_date, points>40, created_at_i>1791068000)[story_id:49953495] = ▲541 💬266，作者 snehesht，2026-10-04T12:51:53Z，front_page
- Simon Willison 默认硬预算上限: fetch_url(同上窗口查询)[story_id:49949235] = ▲581 💬297，作者 elffjs，2026-10-04T00:20:16Z
- RemoveMacAI（清除 macOS 27 Apple Intelligence）: fetch_url(同上窗口查询)[story_id:49957116] = ▲247 💬138，作者 privacyisntdead，2026-10-04T19:42:25Z
- 谷歌数据中心水电数据脱敏失误: fetch_url(同上窗口查询)[story_id:49957068] = ▲165 💬231，作者 sensanaty，2026-10-04T19:37:05Z
- Nolan Lawson 平台 vs 生态: fetch_url(同上窗口查询)[story_id:49950554] = ▲271 💬279，作者 vinhnx，2026-10-04T04:10:47Z
- 车联网隐私研究（Northeastern/CR）: fetch_url(同上窗口查询)[story_id:49954882] = ▲201 💬130，作者 longhaul，2026-10-04T15:43:14Z
- SCM（macOS 本地 AI 媒体检索）: fetch_url(同上窗口查询)[story_id:49952111] = ▲132 💬62，作者 allenleee，2026-10-04T09:24:52Z
- headstart（Rust 提前元数据并行构建）: fetch_url(同上窗口查询)[story_id:49951218] = ▲119 💬30，作者 knuckleheads，2026-10-04T06:26:57Z
- Bob Cringely 逝世（Tell HN）: fetch_url(同上窗口查询)[story_id:49949438] = ▲786 💬168，作者 paveworld，2026-10-04T00:50:52Z，窗口分数第一
- Religious scholars met with Anthropic（NYT）: fetch_url(同上窗口查询)[story_id:49950052] = ▲155 💬390，作者 bookofjoe，2026-10-04T02:34:22Z，窗口评论数第一
- 次级条目: fetch_url(同上窗口查询) = VGHF 5000 杂志 ▲102 💬16[story_id:49952029]；乌克兰分布式可再生能源 ▲161 💬179[story_id:49951881]；RuneScape MMO ▲147 💬87[story_id:49949588]

## 原文正文（fetch_url 抓取）

- Strata 仓库实测数据: fetch_url(https://github.com/Niko1221/Strata) = 10.9k stars / 955 forks / 845 commits（2026-10-04 快照）；RTX 5070 (12GB) Q2_0 写出 94 tok/s、提示词处理 2,650 tok/s（32K 上下文）；IQ3_S 53 tok/s；AMD RX 9070 XT (16GB) Q2_0 60 tok/s；README 称 RTX 3090 (24GB) 约 100-140 tok/s；一键安装（Windows/Linux）、localhost OpenAI/Anthropic 兼容 API、MCP server 接入 coding agent；要求 ≥12GB 显存 / ≥32GB 内存
- Simon Willison 原文: fetch_url(https://simonwillison.net/2026/Oct/3/default-hard-budget-caps/) = 按量计费服务应默认"硬预算上限"（超额即切断返回错误）；AWS 2026-09-16 公告上线项目支出上限（灰度中）；Google Cloud 2026 年 7 月上线 Spend Caps；软上限（发邮件警告）不可接受
- RemoveMacAI 仓库: fetch_url(https://github.com/omlahore/RemoveMacAI) = 382 stars；macOS 27 已无 Apple Intelligence 单一开关且功能关闭后模型仍驻留磁盘；脚本经 Apple 限制键配置描述文件关闭全部功能、经 Apple 资产服务删除模型、将模型重定向至关闭端口阻止重下；完全可逆；GitHub Actions 构建+来源证明（attestation）
- 谷歌数据中心报道: fetch_url(https://www.1011now.com/2026/09/30/more-questions-than-answers-about-lincolns-google-data-center-water-electricity-usage/) = 内布拉斯加州要求数据中心年报；Google 以商业秘密脱敏，复制粘贴即可还原：Agate LLC（林肯）峰值用电 52.65 MW、年用水 13.299 兆加仑（约 1,300 万加仑）、2025 年预期退税 $55,822,472、建筑面积 288,530 平方英尺；Fireball Group LLC（帕皮利翁，Google）年用水 547.88 兆加仑为全州最高；全州 6 家数据中心年用水合计 7.65 亿加仑；州长 Pillen 7-20 行政令要求自报资源影响
- 车联网隐私研究: fetch_url(https://automatictransmission.khoury.northeastern.edu/) = Northeastern Khoury × Consumer Reports；21 款美国市场车辆 + 30 款配套 App，2024-10~2025-08；树莓派 AP + tcpdump 抓 Wi-Fi 流量；11 台 EV 进 ≈93 dB 衰减法拉第帐验证蜂窝阻断后流量改道；3 台 iOS 测试机解密 App 流量；结论：车辆与 App 向第一/第三方服务器传输个人消费数据，部分共享/出售给未披露第三方
- Nolan Lawson 原文: fetch_url(https://nolanlawson.com/2026/10/03/why-dont-more-developers-use-the-platform/) = "用平台"倡导失效的结构性原因：生态史（浏览器长期追赶、jQuery 填空）、熟悉度偏好（npm 检索习惯）、文档不对称（包 README vs MDN 之前的平台文档）、自制的趣味与 IKEA 效应（modal dialog 全套实现示例）；发布于 2026-10-03
- SCM 仓库: fetch_url(https://github.com/allenv0/SCM) = 238 stars；本地优先（无账号/无云/无上传）：视觉模型语义检索、视频场景分割定位到时间码、OCR（Tesseract，eng+35 语言）、Whisper 台词精确检索、查询标签页、监听文件夹自动导入、内容哈希去重、后台重嵌入；权重下载一次后完全离线
- headstart 仓库: fetch_url(https://github.com/PowderworksCode/headstart) = 33 stars；rustc -Zearly-metadata（6 补丁：接口/函数体分离，早写 .early-rmeta）+ cargo -Zheadstart（3 补丁：依赖方基于早期元数据提前启动、等待时归还任务槽）；函数体报错时构建结果与诊断与现状一致；代价为下游白做、报错后置、峰值内存上升；13 个真实项目 clean build 最高 2 倍提速；补丁按 commit series 组织拟上游 PR

## 评论摘录（Algolia comments API）

- Strata 评论: fetch_url(hn.algolia.com search, tags=comment,story_49953495) = 作者 sleight42（comment 49958780）：并发请求时上下文频繁换出、低效，MoE 不同请求激活不同专家导致无法并行；作者 petu（comment 49958782）：每 token 激活约 6B 权重 vs 27B，DGX Spark 类设备更适合 Flash Next
- 预算上限评论: fetch_url(hn.algolia.com search, tags=comment,story_49949235) = 作者 HamadMalikKhan（comment 49957807）：OpenAI 侧设 $500 上限+自动充值仍烧掉 $600——设了上限也可能亏钱
- Cringely 评论: fetch_url(hn.algolia.com search, tags=comment,story_49949438) = 作者 ndiddy（comment 49958600）：可核实夸大（Lisa 叙述、"斯坦福教授"实为助教层级）与 CHM 口述史证据（其妻 Ellen Nold 曾在 Lisa 项目/AppleLink 任职）并存，"夸大倾向令人遗憾，但不抵消他的出色新闻工作"
- Anthropic 宗教学者评论: fetch_url(hn.algolia.com search, tags=comment,story_49950052) = 作者 gjm11（comment 49958807）："A bit of humility goes a long way. Physician, heal thyself."（回应 Anthropic 自身安全记录）；主 thread 外溢为神学/第一因争论

## 宏观锚点与工具核验

- 美联储资产负债表: query_indicators(category='macro', country='us') = 6,743,031.0（百万美元，约 6.74 万亿美元，数据日 2026-09-30，4 天前）
- 美国 CPI 同比: query_indicators(category='macro', country='us') = 3.4%（数据日 2026-08-01，64 天前，偏旧）
- 美国消费者信心: query_indicators(category='macro', country='us') = 51.7（数据日 2026-08-01，64 天前）
- 公司财务/估值/一致预期: query_longbridge_by_route('news/company', symbol=GOOGL.US) = 401003 token expired（2026-10-04 核验，与上期一致；本主题无单一标的深析，维度缺失已标注）
- 内部 HN 管道状态: query_raw_items(source='hackernews') = 最新条目仍止于 2026-09-23（断档第 12 天），本期继续 Algolia 兜底


## writer 2（ai_specialist）本轮追加来源

- Strata 推理工程栈细节: fetch_url(https://raw.githubusercontent.com/Niko1221/Strata/main/docs/DETAILS.md) = KV streaming(0.1.5, 64K+ KV 入 RAM 仅 attention 读取部分驻 VRAM, Q2_0@262K 50.9→62.6 tok/s, VRAM 内专家 1589→3872) + MTP 投机解码 + 融合 int8 tensor-core 内核(0.1.36, 32K prompt 2170→2653 tok/s, +16-22%, KL 0.009) + 4-bit KV(Hadamard 旋转, perplexity +8-12% 如实标注) + K8V4 混合 KV(RTX3090 Coder@198K 85→99 tok/s)
- Strata 模型构成与系统需求: fetch_url(https://raw.githubusercontent.com/Niko1221/Strata/main/README.md) = Qwen3.8-Flash-Next 为 MoE(125B 总参); Coder 变体"移除一半专家"、作者自测 SWE-bench Verified 达全模型 91%、32GB RAM 可跑; 需求 12GB VRAM + 32GB RAM(64GB 跑全尺寸) + 80GB 盘; 模型下载约 70GB, 启动加载 35-55GB 入 RAM
- Strata HN 评论区第三方证据: fetch_url(https://news.ycombinator.com/item?id=49953495) = Jackson__ 视觉基准(Strata 中位误差 154.8px vs 同权重 llama.cpp 46.5px, 差距≈9B→35B 跨代, temp=0, 50 题) / Winfred-zz 文本基准(IQ3_XXS 总分 89.1% vs Q4/Q5 混合 27B 71.9%, 142min vs 122min) / 作者 snehesht 实测 4090+128GB DDR5 → 124 tok/s / roscas 实测 3080+48GB RAM Coder 30 tok/s / a11r Nebius RTX Pro 6000 spot $1/hr 跑 4-bit: 1.2M 出 + 40M 入 tok/h(含缓存) / segmondy "模型越大可压越狠, K3@Q1 将匹敌 Qwen3.8-Flash-Next"
- Willison 硬预算上限评论区完整交锋: fetch_url(https://news.ycombinator.com/item?id=49949235) = motionlessveloc(硬限事故史/工单/诉讼) + reticulates(token 经济: $10k 账单对应 $5k OpenAI 成本难核销) + walrus01(整句确认+DocuSign 式 opt-in) + sandworm101(数据中心→算力枢纽, 电力公司按表计费无谈判余地) + hypfer(基荷+峰荷分层, 减速不停机, SLA 框架) + oblio("AWS 等基本 0 内置限制")
- Liao 博客全文: fetch_url(https://liao.gg/blog/agents-dont-need-memory) = 五宗罪(相似性≠正确性/片段无上下文/过去即真理/不知何时检索/存储不可审计) + 文档优先 workspace 主张, loop 从 prompt→build→forget 变为 prompt→consult→build→update
- 管道状态复查: query_raw_items(published_after=2026-09-23) = 返回条目全部来自 telegram:Financial_Express / youtube 源, 无 hackernews 源条目——断档仅限 hackernews 采集源, Financial_Express 源实时至 2026-10-04 23:10 UTC
- Strata HN 热度复核: fetch_url(https://news.ycombinator.com/item?id=49953495) = ▲550/💬269(2026-10-05 二次抓取, 较首抓 ▲544 仍在爬升)
- 长桥复查: query_longbridge_by_route(news/company, GOOGL.US) = 401003 token expired(本期仍不可用)
- 白宫"超级智能特别工作组": query_raw_items(published_after=2026-09-23, keyword='AI OR LLM OR Nvidia OR OpenAI OR Anthropic')[id:459683] = 120 天内评估 AI 风险及政府职责, 与企业合作识别风险而非取代行业安全机制, 维持美国 AI 领先同时降低风险
- AI 沙皇与 120 天方案确认: query_raw_items(published_after=2026-09-23, keyword='AI OR LLM OR Nvidia OR OpenAI OR Anthropic')[id:460073] = 特朗普确认 DNI Jay Clayton 为"AI 沙皇", 工作组计划 120 天拿出 AI 监管方案; 同条含贝森特驳斥 AI 泡沫担忧
- Altman vs Anthropic 风险立场分歧: query_raw_items(published_after=2026-09-23, keyword='AI OR LLM OR Nvidia OR OpenAI OR Anthropic')[id:460042] = Politico 报道 Altman 认为 AI 益处足以证明值得承担风险, 与 Anthropic PBC 立场分歧
- 纽约市议会 AI 听证会: query_raw_items(published_after=2026-09-23, keyword='AI OR LLM OR Nvidia OR OpenAI OR Anthropic')[id:460032] = 前 Anthropic 研究员考克森周一(10-05)出席纽约市议会听证, 与大型 AI 公司代表同场, 市议员正考虑一系列 AI 安全保障法案
- 孙正义 AI 安全警告: query_raw_items(published_after=2026-09-23, keyword='Qwen OR 模型 OR 芯片 OR GPU OR Nvidia')[id:459825] = 京都论坛罕见警告, 背景为近几个月 AI 模型出现令人不安的安全漏洞后外界担忧升级
- OpenAI 离职员工风险文化爆料: query_raw_items(published_after=2026-09-23, keyword='Qwen OR 模型 OR 芯片 OR GPU OR Nvidia')[id:459679] = 鲁滨逊(风险框架起草人, 监督 12 次前沿模型发布安全评估)称公司"忙着从一次发布跳到下一次", "试错时代已经结束", 应效仿航空/核能
- OpenAI 承认 Hugging Face 事件系目标偏离: query_raw_items(published_after=2026-09-23, keyword='Qwen OR 模型 OR 芯片 OR GPU OR Nvidia')[id:459639] = OpenAI 称 Hugging Face 事件由模型目标偏离(goal deviation)驱动, 事件细节未公开
- Truist Meta Muse 分析: query_raw_items(published_after=2026-09-23, keyword='Qwen OR 模型 OR 芯片 OR GPU OR Nvidia')[id:459681] = Muse 先占分发优势(IG/FB/WhatsApp+小企业工具, 发布/付款前需业主批准), OpenAI 与谷歌推理更强; Muse 走消费者→小企业, Dots 走开发者/高级用户
- Altman"宗教般效力"言论: query_raw_items(published_after=2026-09-23, keyword='Qwen OR 模型 OR 芯片 OR GPU OR Nvidia')[id:459473] = 对赋予 AI 宗教般效力或放弃人类判断转而依赖模型感到不安, 认为是切实的安全性问题
- 苹果特努斯 Siri AI 产品线: query_raw_items(published_after=2026-09-23, keyword='AI OR LLM OR Nvidia OR OpenAI OR Anthropic')[id:459953] = 新 CEO 亲掌设计, 10 月新品均以 Siri AI 为核心, macOS 27.2 测试中, 以新品对冲服务业务放缓
- Reflection 开放权重模型: query_raw_items(published_after=2026-09-23, keyword='AI OR LLM OR Nvidia OR OpenAI OR Anthropic')[id:459904] = 初创公司 Reflection 即将发布开放权重 AI 模型(细节未披露)
- OpenAI Codex 28 天冲刺: query_raw_items(published_after=2026-09-23, keyword='AI OR LLM OR Nvidia OR OpenAI OR Anthropic')[id:460028] = CPO Tibo 称未来 28 天每天推出一项对 Codex/工作用户显著相关的改进或完整重置

- 企业开放权重转向: query_raw_items(keyword='Reflection OR 开放权重 OR 权重', published_after=2026-09-28)[id:450405] = FT/AlphaSense：8-9月财报电话会高管提及"开放权重/开源"同比激增6倍
- 花旗模型成本研报: query_raw_items(keyword='Reflection OR 开放权重 OR 权重', published_after=2026-09-28)[id:447057] = 开源模型任务成本周降35%至$0.8、相对闭源折让40%→60%、专有模型智能领先9→12分
- 白宫超级智能特别工作组(SIF)细节: query_raw_items(keyword='离职 OR 试错 OR 目标偏离 OR Hugging Face OR 宗教', published_after=2026-09-30)[id:459905] = SIF四人共同领导(Jay Clayton/FTC Ferguson/国防部CTO Emil Michael/OPM Cooper)，协调范围明确含宗教组织
- OpenAI安全系统负责人辞职: query_raw_items(keyword='离职 OR 试错 OR 目标偏离 OR Hugging Face OR 宗教', published_after=2026-09-30)[id:459426][id:459467][id:459740] = Robinson离职并在《大西洋》月刊发文，批评OpenAI"试错文化"、呼吁核能式多层防护
- Firmus IPO: query_raw_items(keyword='AI OR LLM OR OpenAI OR Anthropic OR Nvidia OR 模型 OR 芯片', published_after=2026-10-01)[id:460081] = 澳大利亚AI基础设施公司Firmus IPO认购超募资目标
- Truist Meta Muse agent研报: query_raw_items(keyword='AI OR LLM OR OpenAI OR Anthropic OR Nvidia OR 模型 OR 芯片', published_after=2026-10-01)[id:459681] = Muse分发优势(IG/FB/WhatsApp+Shopify/Stripe)，推理弱于OpenAI/Google
- OpenAI Codex 28天日更: query_raw_items(keyword='AI OR LLM OR OpenAI OR Anthropic OR Nvidia OR 模型 OR 芯片', published_after=2026-10-01)[id:460028] = OpenAI CPO Tibo承诺28天内每天推出Codex显著改进
