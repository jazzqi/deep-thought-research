# reference.md — HN 书摘 2026-08-29（周六）数据溯源

> ⚠️ 数据管道告警：query_raw_items(source='hackernews') 查询层 source 过滤持续结构性失效（tech_generalist 第 6+ 次确认，2026-08-29→08-30 复验一致）。直接按 source 查询仅返回 9 条（最高 ▲3，含 4 条 longbridge 财经泄漏 id:146460/145875/114342/114340 与 2 条 08-27 ADHD 帖 id:173855/173305），完全漏检 2026-08-29 真实 HN 头条（Cursor ▲808 等）。本期所有 HN 分数/评论/作者/时间均来自 Algolia HN API 交叉核验，非 query_raw_items。

- HN 2026-08-29 窗口 Top 故事（按分降序，created_at_i∈[1787961600,1788048000)）: Algolia HN Search API(tags=story, numericFilters=created_at_i>=1787961600,created_at_i<1788048000, hitsPerPage=50) = Cursor 808/497, Debian 477/445, Internet cesspit 408/282, DHS 375/69, Culture 328/76, Iceland 326/429, GrapheneOS 281/148, Samsung PIM 255/97, Hy4 229/137, StemDeck 210/59
- Cursor/SpaceX/OpenAI 断供公告正文核验: fetch_url(https://openai.com/index/our-decision-on-cursor-following-its-acquisition-by-spacex/) = 403 Forbidden（官网拦截），摘要依据 Algolia 元数据 + HN 评论 rgbrenner(id:49486172)
- DHS 19 USC 1509 秘密监控记者: fetch_url(https://www.theguardian.com/us-news/2026/aug/29/trump-dhs-1509-summons-records-journalists-nonprofits) = 正文已抓取（Georgia Fort 6 个月电话记录、Don Lemon YouTube 频道；法官两次驳回搜查令后 DHS 改用海关稽查条款行政传票绕开司法；前 DHS 监察长 John Roth 称"outrageous"）
- Debian 通用决议投票: Algolia HN Search API(story_49489982) = ▲477 💬445 @pluc，LWN 原文链接 lwn.net/Articles/1091231/
- query_raw_items 失效证据: query_raw_items(source='hackernews', min_points=20, status=processed, limit=50) = 仅 9 条，最高 ▲3，混入 longbridge id:146460/145875/114342/114340，漏检真实 HN
- 往期交叉比对: themes/hn-daily/index.md 往期列表（2026-08-15 至 2026-08-30）已读，确认本期为 2026-08-29 UTC 窗口
- 晚窗口信号（窗口内但分低，未入 Top10）: Algolia = "The Rise and Fall of Agent Civilizations"(dwarkesh.com) ▲21 front_page @consumer451 23:43Z；"New Chinese surveillance leaves foreigners nowhere to hide"(dw.com) ▲6 @pir8life4me 23:30Z

# reference.md — 数据溯源（hn-daily 2026-08-30 增量补丁）

- HN 2026-08-30 UTC 窗口(00:00–05:48) 真实 hackernews 帖 Top5: fetch_url(Algolia HN Search API, created_at_i∈[1788048000,1788134400], attributesToRetrieve=title,url,points,num_comments,objectID,created_at,author) = Bug Blindness ▲159💬65 / FreeCORE ▲64💬42 / Algorithmic Rent-Pricing ▲57💬23 / Benjamin Franklin ▲32💬9 / California Linux exemption ▲32💬1
- query_raw_items(source='hackernews') 过滤失效(第6+次确认): query_raw_items(source='hackernews', min_points=20, status='processed') = 返回 9 条且混入 longbridge 泄漏(id:146460/145875/114342/114340)，完全漏检 2026-08-30 真实 HN 帖
- Bug Blindness 正文: fetch_url(https://danluu.com/bug-blind/) = 作者主张"bug blindness"普遍存在，LLM 可模拟普通用户跨场景复现问题
- Bug Blindness 评论: fetch_url(Algolia HN items API, id=49494520) = sidewndr46 等讨论"用户用想不到的方式使用软件、绕开 bug 工作流"
- Algorithmic Rent-Pricing 正文: fetch_url(https://www.morganlewis.com/pubs/2026/08/algorithmic-rent-pricing-litigation-expands-under-new-state-and-local-laws) = 地方条例 SF §37.10C/SD §98.1103/Seattle ch.7.34/Philly §9-813 授权私诉+公罚，SF/SD 每单元每月违规最高 $1000、Seattle 最高 $7500
- FreeCORE 正文: fetch_url(https://freecore.org/) = 从 TrueNAS CORE 13.3 独立延续，15.0-U1 stable，FreeBSD+OpenZFS
- California Linux exemption 正文: fetch_url(https://www.tomshardware.com/software/linux/california-lawmakers-unanimously-pass-linux-exemption-from-age-verification-law-software-distributed-under-the-gpl-mit-bsd-and-apache-licenses-are-exempt) = 页面返回 CSS 框架，仅标题/导语可见（GPL/MIT/BSD/Apache 软件豁免年龄验证法）
- Benjamin Franklin 正文: fetch_url(https://www.smithsonianmag.com/history/among-all-great-things-benjamin-franklin-invented-discovered-alter-egos-gave-him-most-freedom-180988824/) = Franklin 用 Silence Dogood/Polly Baker/Richard Saunders 等笔名规避出版审查
- 基线 Aug 29 窗口 Top10 分数: fetch_url(Algolia HN Search API, created_at_i∈[1787961600,1788048000]) = OpenAI×Cursor ▲808💬497 / Debian AI ▲477💬445 / internet cesspit ▲408💬282 / DHS ▲375💬69 / Iceland ▲326💬429 / culture ▲328💬76 / Pixel MTE ▲281💬148 / Samsung PIM ▲255💬97 / Hy4 ▲251💬145 / StemDeck ▲215💬60（定版 2026-08-30.md 采用快照值 805/493 等）
