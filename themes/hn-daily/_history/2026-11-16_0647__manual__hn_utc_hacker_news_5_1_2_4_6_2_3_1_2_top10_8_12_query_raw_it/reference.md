# reference · HN 书摘 2026-11-15 期

- HN 候选池（2026-11-15 UTC 窗口，hn_points≥20）: query_raw_items(source=hackernews, min_points=20, published_after=2026-11-15T00:00:00Z, published_before=2026-11-16T00:00:00Z) = 42 条
- 正文入选帖 raw id: query_raw_items(同上窗口) = AI-code [id:781011]、DRAM [id:780575]、Lutnick [id:780882]、OLED [id:780918]、EFF ALPR [id:780496]、氯气 [id:781172]、Duffy [id:781062]、Raschka [id:780917]、Kiri [id:780653]、Hackable [id:781258]、Apollo [id:780784]；正文引用的另两帖 WSJ 路由器 [id:780537]、Reuters L3Harris 路由器 [id:780610]
- Top10 分数/评论（2026-11-16 06:47 UTC 快照）: fetch_url(hn.algolia.com/api/v1/search?tags=story&numericFilters=created_at_i>1794700800,created_at_i<1794787200&hitsPerPage=15) = AI-code 1016/565、DRAM 481/212、Lutnick 441/190、OLED 375/203、EFF 333/109、氯气 278/144、Apollo 213/141、NES 197/39、Raschka 185/23、Turbo Pascal 179/89、Emacs 162/82、Duffy 135/39
- Kiri 分数/评论: fetch_url(hn.algolia.com/api/v1/search?query=Kiri container runtime&tags=story&numericFilters=窗口) = 90 分/34 评论，作者 nikolay
- Hackable 帖分数/评论: fetch_url(hn.algolia.com/api/v1/search?query=Hackable Agent&tags=story&numericFilters=窗口) = 50 分/33 评论，作者 tensafefrogs
- DRAM 判决正文: fetch_url(litnews.ai/articles/garciaguirre-samsung-sk-hynix-micron-dram-conspiracy-suit-survives-dismissal) = Judge Noël Wise 2026-11-14 全盘驳回撤诉动议；17 名原告/5 州、2026-06-25 立案、三巨头 2025Q3 全球 DRAM 收入 91%+、常规 DRAM 一年 +171.8%/18 个月 +697%、HBM 每 GB 耗硅 3-4 倍、答状 2026-12-07、CMC 2027-01-12
- Lutnick 正文: fetch_url(nyt.com/2026/11/15/us/politics/lutnick-pushed-to-weaken-chip-rules...) = 马来西亚 A201 数据中心供中国科技巨头、运营方为 Cantor Fitzgerald 客户、政府内部争论约两年、考虑中更强版本含对国际数据中心销售更多监督
- OLED PWM 正文: fetch_url(macanorak.com/the-macbook-pros-oled-pwm-problem...) = 串联 OLED（PROLED XDR）、MacRumors/Reddit 成批报告、AppleInsider 11-10 汇总、Notebookcheck 实测 240Hz PWM（≤99% 亮度触发）
- EFF ALPR 正文: fetch_url(eff.org/deeplinks/2026/11/were-asking-appeals-court-require-warrant-alpr-searches) = 2026-11-09 与 ACLU 提交第六巡回 amicus、US v. Sturdivant、Flock/ELSAG、"虚拟时间机器"、上月联邦地区法院"大规模监控"裁定
- 氯气事件正文: fetch_url(wdr.de/nrw/rheinland/rhein-erft-kreis/technischer-defekt-chlor-phantasialand-100.html) = 2026-11-13 周五微软故障、Phantasialand 酒店 Ling Bao、告警邮件未达、计量系统故障、15 人受伤/4 人送医（1 人中度伤留观）
- AI-code 正文: fetch_url(jakub.jankiewicz.org/blog/ai-code-open-source/) = 许可证洗白、猴子自拍判例、版权局 AI 口径、CC0/公有领域、英国计算机生成作品版权
- Raschka 正文: fetch_url(magazine.sebastianraschka.com/p/understanding-positional-embeddings) = 绝对位置编码到 RoPE、最小 PyTorch 实现、2026 开源模型选型预览图、第 6 节现代架构选型
- Kiri 正文: fetch_url(runkiri.com) = docker run 22ms vs 178ms（Colima 152/OrbStack 279，2CPU/8GB）、单 daemon、k3s 约 20 秒、常驻约 15MB、免费公测
- Hackable 正文: fetch_url(geoffstearns.com/blog/your-agent-will-pick-the-hackable-one/) = M-VAVE FM-1 约 70 美元、9 月起机主 AI 写固件、Doom 移植、10 月厂商 GPLv3 开源+浏览器模拟器、agent 采购将偏好可改写设备
- Apollo 高票答案: fetch_url(api.stackexchange.com/2.3/questions/37775/answers?site=space&sort=votes) = Russell Borogove 得分 110：地震成像实验（地震仪+已知当量地表爆炸反推月球内部结构）
- Duffy/停航正文: fetch_url(commondreams.org/news/duffy-ground-stop-explanation) = 2026-11-13 FAA 第三次全美停航、约 150 万旅客、Duffy 归因交换机/路由器过载、记者 Anna Giaritelli 采访 60 名空管员"没一个买账"
- AI-code 评论: fetch_url(hn.algolia.com/api/v1/search?tags=comment,story_50507303) = 作者 CharlesW 引美国版权局《版权与人工智能·第三部分》反驳转换性前提（comment id 50511698）
- DRAM 评论: fetch_url(hn.algolia.com/api/v1/search?tags=comment,story_50502988) = 作者 sleight42：2017-2020 主板 1.1-2k 美元、老旧平台抢手（comment id 50510627）
- Apollo HN 评论: fetch_url(hn.algolia.com/api/v1/search?tags=comment,story_50505271) = 141 条，月球车机动性/影视梗发散（如 comment id 50511673）
- 跨天去重: query_raw_items(keyword=grenade launcher, published_before=2026-11-15, source=hackernews) = 7 条均非同题旧帖，Apollo 帖（2019 原题）未在此前入库
- 付费墙/反爬核验: fetch_url(WSJ 单台路由器文) = 401 失败；fetch_url(Reuters L3Harris 路由器文) = 401 失败；fetch_url(space.stackexchange.com/questions/37775) = 403 失败（改用 StackExchange API 取答案）


- Phantasialand 氯气事件 HN 评论页（作者 amluto 闭环加氯工程要求、作者 N19PEDL2 归责酒店）: fetch_url(https://news.ycombinator.com/item?id=50509411) = 实时 315 分/157 评论 [id:781172]
- Raschka 位置嵌入文 HN 评论页（作者 programjames 群表示理论、作者 nlitened 事后合理化反驳）: fetch_url(https://news.ycombinator.com/item?id=50506376) = 实时 190 分/26 评论 [id:780917]
- Phantasialand 条目定位: query_raw_items(keyword='Phantasialand', source=hackernews, published 2026-11-15~11-16) [id:781172] = Comments URL id=50509411
- Raschka 条目定位: query_raw_items(keyword='Positional Embeddings', source=hackernews, published 2026-11-15~11-16) [id:780917] = Comments URL id=50506376


## 第 3 棒 tech_generalist 统稿新增（2026-11-15/16）

- NVDA/MSFT 最新收盘（2026-11-13 收盘口径，15 分钟延迟）: market_quote(symbols=['NVDA.US','MSFT.US']) = NVDA 162.85 美元（-2.01%，量 3.66 亿股）、MSFT 523.88 美元（+0.17%）
- Anthropic 拟 62.5 亿美元 IPO + 26 亿美元私募: query_raw_items(keyword='Anthropic IPO OR 算力 OR 基金', published_after='2026-11-15T22:00:00Z', limit=15)[id:780990] = longbridge 快讯
- 中信证券提示 Anthropic 巨型 IPO 对美股流动性短期扰动: query_raw_items(same)[id:780775] = longbridge 快讯
- 美股基金连续第二周净流入 66 亿美元（前周 149.7 亿美元，-56%），大盘股基金 116.4 亿美元创四周新高: query_raw_items(same)[id:781362][id:781361] = telegram:Financial_Express（金十）
- AI 硬件板块调仓迹象（重仓光模块/PCB 的主动权益基金净值与持仓偏离）: query_raw_items(same)[id:781357] = telegram:Financial_Express（中国证券报）
- 基金研判英伟达风波冲击的是"确定性溢价"而非长期需求、产业链"一枝独秀→百花齐放": query_raw_items(same)[id:781270] = telegram:Financial_Express（证券时报）
- 黄仁勋回归两线并行最新状态（硅谷盟友施压董事会 vs Bessent 要求管理层大改组）: query_raw_items(keyword='Nvidia OR Jensen OR Anthropic', published_after='2026-11-15T18:00:00Z', limit=30)[id:781352][id:781283] = longbridge 快讯
- 本周美股焦点=英伟达财报+Anthropic IPO、三大股指上周涨超 2%: query_raw_items(same)[id:781281][id:780989] = longbridge 快讯
