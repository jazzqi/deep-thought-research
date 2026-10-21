# 数据来源溯源（HN 书摘 · 2026-10-21，覆盖 10-17~10-21 周度复盘）

> 采集窗口：2026-10-17T00:00Z → 2026-10-21T22:28Z。本期主取数管道失效，全部结论均基于回退查询的实际返回，逐条标注。

## 取数尝试记录（全部为实际工具返回）

- 窗口 10-17~10-22，min_points=20: query_raw_items(source='hackernews', published_after=2026-10-17, published_before=2026-10-22, min_points=20, limit=100) = 仅 5 条，且全部窗口外（最新 id:488150 时间戳 2026-10-16 16:57Z）
- 窗口 10-16~10-22，min_points=1（回退 1）: query_raw_items(published_after=2026-10-16, min_points=1) = 同上 5 条，无新增
- 窗口 10-19~10-22，无过滤: query_raw_items(published_after=2026-10-19) = 同上 5 条，无新增
- keyword='Show HN'，窗口 10-17~10-22（回退 2）: query_raw_items(keyword='Show HN') = 工具参数校验报错，未能取数
- keyword 全源兜底（回退 3），窗口 10-19~10-22: query_raw_items(keyword='AI'/'LLM'/'OpenAI'/'Anthropic') = 4 次均返回 NO_DATA

## 唯一在库条目（窗口外，仅作管道健康证据，未入选本期正文）

- dev-null.sh /dev/null 开发者社交网络: query_raw_items(source='hackernews', min_points=20)[id:488150] = ▲180/💬171，元数据 Points: 33 # Comments: 23，发布 2026-10-16 16:57Z（落在 10-16 已出刊期）
- Launch HN: Mireye (YC S26) 物理世界 AI agent 基础设施: query_raw_items(source='hackernews', min_points=20)[id:274845] = ▲20/💬0，发布 2026-09-03
- Earth.nullschool.net: query_raw_items(source='hackernews', min_points=20)[id:122607] = ▲60/💬21，发布 2026-08-14
- Time to Move On: Querying Without Nulls and Bags: query_raw_items(source='hackernews', min_points=20)[id:99390] = ▲2/💬0，arxiv 2608.10863，发布 2026-08-13
- Show HN: fenic（LLM 作为 dataframe 算子）: query_raw_items(source='hackernews', min_points=20)[id:45862] = 发布 2026-06-30

## 结论

本期（覆盖 10-17~10-21 共 5 个 UTC 日）**未能抓取到任何窗口内 HN 条目**，5 栏目正文与 Top10 快照均无法产出，已按规范诚实标注，未编造任何条目、分数或评论。管道故障模式与 2026-08-29/08-30 已连续确认的取数结构性失效一致（当时表现为 min_points 过滤失效 + longbridge 条目泄漏 + 漏检整日），本次为该故障的第 6+ 次确认，且程度更重（整窗口零产出）。


## 本期（2026-10-22 重跑）取数与正文抓取溯源

- 窗口内 HN 高分条目: query_raw_items(source='hackernews', published_after=2026-10-17T00:00:00Z, published_before=2026-10-21T23:59:59Z, min_points=20, status='processed', limit=80) = 80 条，本次管道正常，无 longbridge 泄漏
- DeepInfer 特性清单: fetch_url(https://github.com/deepseek-ai/DeepInfer) = 支持 V4.1-Flash、FlashMLA/DeepGEMM/DeepEP、NVIDIA SM100 + 昇腾 950、KV cache/PD 分离不在开源范围
- PHP 紧急发版预告: fetch_url(https://news-web.php.net/php.announce/509) = 两枚 CVSS 4.0 9.2 级漏洞，原定 2026-10-21 14:00 UTC 发版
- PHP2Shell 漏洞详情: fetch_url(https://www.wiz.io/blog/php2shell-php-rce) = OOM 损坏 + 陈旧全局状态两组 RCE，影响约 70% 网站，回溯至 PHP 5.4，2026-10-21 提前发版
- eMudhra 单字节私钥: fetch_url(https://scotthelme.co.uk/eight-bits-of-trust-emudhras-ca-keys-cracked-in-milliseconds/) = 8 个私钥标量 4/56/66/115/155/156/230/237，2025-04 创建，经 Sectigo AAA 交叉签名
- DHS DeepSeek 禁令: fetch_url(federalregister.gov API, term=DeepSeek, date>=2026-10-17) = DHS 命令排除杭州深度求索及关联实体于 FCEB 采购，并移除用 DeepSeek 实现的第三方产品，发布日 2026-10-20
- WhatsApp 隐藏 LLM 指令: fetch_url(https://redact.dev/blog/whatsapp-help-pages-hidden-ai-instructions) = 545 页中 80 页含 102 个隐藏块，10-18 移除，WIRED 10-19 报道
- tsrs 性能: fetch_url(https://blog.cloudflare.com/typescript-rust-port/) = 比 TS 7.0 快至 8x、内存省约 70%，Oxc 孵化，非 fork
- Voxtral 3: fetch_url(https://mistral.ai/news/voxtral-3/) = 50+ 语言语音 Agent SDK + STT/TTS 模型，EU 托管或自部署
- Timestral: fetch_url(https://mistral.ai/news/timestral/) = 209M 参数登顶 GIFT-Eval/TIME/fev-bench，5M-209M 四档，CPU 可跑
- DuckDB 2.0: fetch_url(https://duckdb.org/2026/10/21/announcing-duckdb-200) = LTS 至 2027-10，Quack 协议/VARIANT/agent mode/触发器，约 2 万提交
- Peec AI 假统计实验: fetch_url(https://peec.ai/blog/publish-stats-get-cited-the-tactic-that-put-my-data-all-over-the-web) = 5 万编造统计、7 个月 1 万+ AI 会话、330+ 引荐域名、流入学术论文与银行研报
- Ruby 维护者归档声明: fetch_url(https://po-ru.com/2026/10/18/why-im-no-longer-updating-this-repository) = 归档全部 gems，抗议公共代码被 LLM 采集 strip-mining
- PHP 发版帖评论: fetch_url(https://news.ycombinator.com/item?id=50172041) = 1502 points/651 评论，作者 ljm/elyobo 评论摘录
- eMudhra 评论: fetch_url(https://news.ycombinator.com/item?id=50166579) = 1192 points/470 评论，作者 eqvinox 评论摘录
- 未能抓取: fetch_url(neowin Google Cloud 故障文 / techdirt No Kings 文 / meidasnews) = HTTP 403，仅用条目元数据列快照
- 条目引用 id（正文实际使用）: query_raw_items 窗口查询[id:495985/498032/497005/501116/501080/500902/493755/494357/497003/497282/492766/501233/496931/493523/497094/489580/501234/496273/489343/488988/497627/489228]

- DuckDB 2.0 HN 热度: query_raw_items(source=hackernews, published_after=2026-10-21T00:00:00Z, published_before=2026-10-22T00:00:00Z)[id:501233] = DuckDB 2.0.0 LTS "Cinnamon Teal" ▲332 💬38
- Meta 250 亿美元判决 HN 帖: query_raw_items(source=hackernews, published_after=2026-10-21T00:00:00Z)[id:501928] = 新墨西哥州 DOJ 宣布陪审团认定 Facebook 违规、判罚 $25B，▲111 💬19
- Claude Duet HN 帖: query_raw_items(source=hackernews, published_after=2026-10-21T00:00:00Z)[id:501713] = Anthropic 主动式 agent Claude Duet 产品帖 ▲95 💬109
- Hirundo Qwen3-Coder HN 帖: query_raw_items(source=hackernews, published_after=2026-10-21T00:00:00Z)[id:500929] = Qwen3-Coder 对 US persona 输出更低安全性代码 ▲236 💬117
- Solo founding HN 帖: query_raw_items(source=hackernews, published_after=2026-10-21T00:00:00Z)[id:501929] = After automation: Solo founding will be the default ▲27 💬25
- Meta 判决正文（43,899,725 次违规、$250 亿罚款、2026-10-21）: fetch_url(nmdoj.gov/press-release/...historic-25-billion-penalty-against-facebook/) = 陪审团认定违反《不公平贸易实践法》43,899,725 次，法院判 250 亿美元民事罚款
- DuckDB 2.0 评论（并行上限与 Splink 实测）: fetch_url(news.ycombinator.com/item?id=50181136) = 作者 RobinL 称 2.0 并行上限从约 64 vCPU 升至 128–192 vCPU，Splink 10 亿记录/100 亿比对 10 分钟完成
- Meta 判决评论（判决书点名高层参与）: fetch_url(news.ycombinator.com/item?id=50184820) = 作者 layer8 引判决书原文，"the involvement of senior Facebook leadership" 为最高档罚款依据之一
- Claude Duet 评论（agent 重度使用实证）: fetch_url(news.ycombinator.com/item?id=50186037) = 作者 intenex 称过去一月用 agent 完成购车、正在跨国协调京都购房全流程
- Hirundo 评论（方法论质疑）: fetch_url(news.ycombinator.com/item?id=50179706) = 作者 lukewarm707 指被测模型为 2025-07 旧模型（AA 分 10、幻觉率 80%），同厂更小模型分 34
- Solo founding 评论（指标因果质疑）: fetch_url(news.ycombinator.com/item?id=50186518) = 作者 onion2k 指单人创始人占比上升不等于成功率上升，可能只是失败基数变大


## 第 3 棒 tech_generalist 增补来源（技术雷达深化）
- LiteLLM 1.107.0 投毒帖（▲395/123 评论，作者 abhisek）: query_raw_items(source='hackernews', keyword='litellm')[id:501374] = SafeDep 披露 LiteLLM 1.107.0 被植入凭据窃取器与远程后门
- LiteLLM 评论摘录（rsanheim 指年内第二次利用、atmosx 永久锁 1.104.2、isityettime vs drdaeman 沙箱辩论）: fetch_url(https://news.ycombinator.com/item?id=50181114) = HN 评论页抓取（抓取时 401 分/125 评论，快照值以冻结数据为准）
- LayerFS 帖（▲69/40 评论，作者 l2dy）: query_raw_items(source='hackernews', keyword='LayerFS')[id:501042] = agent 文件系统项目发布
- LayerFS 评论摘录（compsciphd 指 Apiary/USENIX ATC 2010 与专利 US8589947B2 先例；fnordpiglet 称 vibe coded v1 但去重基准扎实）: fetch_url(https://news.ycombinator.com/item?id=50179857) = HN 评论页抓取
- GitHub agent-scale Git 帖（▲30/3 评论，作者 Klaster_1）: query_raw_items(source='hackernews', keyword='agent-scale Git')[id:501624] = GitHub 官方博客披露 agent 流量驱动 Git 存储架构迁移
- GitHub agent-scale Git 评论摘录（MobileVet 关联 Anthropic 公开抱怨 GitHub 无法承受 merge 量；laura2013 证实系三部曲系列）: fetch_url(https://news.ycombinator.com/item?id=50183344) = HN 评论页抓取
- 管道状态核验: query_raw_items(source='hackernews', keyword='litellm'/'LayerFS'/'agent-scale Git') = 三次查询均返回 2026-10-21 当日新鲜条目，确认 HN 取数管道已恢复

- 10-21 HN 当日条目核验（Railway 安全披露 147 分未覆盖）: query_raw_items(source=hackernews, published_after=2026-10-21T00:00:00Z)[id:502064] = Railway Security(Compromise) Disclosure
- 10-21 HN 当日条目核验（PHP 补丁主帖 912 分，草稿未引用）: query_raw_items(source=hackernews, published_after=2026-10-21T00:00:00Z)[id:50180873] = Updated PHP version released to GitHub (php-8.2.35)
- 10-21 HN 当日条目核验（OpenAI 协同披露帖 210 分未引用）: query_raw_items(source=hackernews, published_after=2026-10-21T00:00:00Z)[id:501153] = OpenAI: Patch the Planet. Global response coordination
- 10-21 HN 当日条目核验（Trail of Bits agent 审计帖未收录）: query_raw_items(source=hackernews, published_after=2026-10-21T00:00:00Z)[id:501538] = AI agent fixed the bug, but what else did it change?
- 10-21 HN No Kings 帖评论数快照 461（草稿写 469）: query_raw_items(source=hackernews, published_after=2026-10-21T00:00:00Z)[id:501234] = The No Kings Takedown Is Why You Shouldn't Rent Your Megaphone from Zuck
