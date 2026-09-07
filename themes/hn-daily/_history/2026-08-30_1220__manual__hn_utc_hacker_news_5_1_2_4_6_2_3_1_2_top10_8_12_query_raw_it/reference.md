# 数据溯源 · hn-daily · 2026-08-30（窗口 2026-08-29 UTC）

## 数据管线状态
- query_raw_items 失效: query_raw_items(source='hackernews', min_points=20, limit=50) = 仅返回 9 条，最高 ▲3，混入 longbridge 泄漏条目(id:146460/145875/114342/114340)，完全漏检 2026-08-29 HN 高价值帖。source 过滤持续失效（2026-08-30 第 5+ 次确认）。本次榜单改用 Algolia HN API。
- HN 榜单(主取数): fetch_url(https://hn.algolia.com/api/v1/search?tags=story&numericFilters=created_at_i>1787961600,created_at_i<1788048000&hitsPerPage=50) = 2026-08-29 UTC 窗口 Top 故事：OpenAI/Cursor 805pts/493c、Debian AI 475/442、Internet cesspit 405/272、DHS 354/62、Iceland 326/428、Good Culture 293/70、GrapheneOS MTE 275/145、Samsung PIM 251/95、Hy4 229/137、StemDeck 210/59。

## 正文抓取
- OpenAI/Cursor 原文: fetch_url(https://openai.com/index/our-decision-on-cursor-following-its-acquisition-by-spacex/) = 403 Forbidden，未能抓取正文；摘要基于标题 + HN 评论区共识。
- Debian AI: fetch_url(https://lwn.net/Articles/1091231/) = GR 选项5胜出，两反AI选项低于 None of the Above。
- Internet cesspit: fetch_url(https://www.stephendiehl.com/posts/internet_predatory_cesspit/) = 正文抓取成功。
- DHS: fetch_url(https://www.theguardian.com/us-news/2026/aug/29/trump-dhs-1509-summons-records-journalists-nonprofits) = 19 USC 1509 行政传票，Fort 1万+通话记录。
- Iceland: fetch_url(https://www.bbc.com/news/articles/cn45vdxyvvlo) = 反对派民调 51.6%，渔业占出口近40%。
- Good Culture: fetch_url(https://newsletter.eng-leadership.com/p/good-culture-is-the-biggest-productivity) = 康威定律论证文化优先。
- GrapheneOS: fetch_url(https://bsky.app/profile/grapheneos.org/post/3mua32q4ds22e) = Pixel 11 移除 MTE，评估 Motorola。
- Samsung PIM: fetch_url(https://chipsandcheese.com/p/hot-chips-2026-samsungs-processing) = 614 GB/s 内部带宽，8芯片 9.6 INT8 TOPS。
- Hy4: fetch_url(https://www.tencent.com/tencent-releases-and-open-sources-tencent-hy4-preview/) = 770B/49B，盲评2.99，吞吐+31.8%。
- StemDeck: fetch_url(https://github.com/stemdeckapp/stemdeck) = 本地 htdemucs 封装，3.2k star。
- TurboKV: fetch_url(https://github.com/kingroryg/turbokv) = durable() 不 fsync，paranoid() 才真持久。
- Burning Man: fetch_url(https://sfstandard.com/2026/08/29/burning-man-lost-its-soul-founder/) = 创始人 John Law 批评商业化。
- Flock: fetch_url(https://www.texastribune.org/2026/08/28/texas-flock-cameras-auto-insurance-fee-mvcpa-grants/) = $1车险费→3200+摄像头。

## 评论抓取（HN item 页）
- Cursor 评论: fetch_url(https://news.ycombinator.com/item?id=49486172) = cornholio 评私有版权体系。
- Debian 评论: fetch_url(https://news.ycombinator.com/item?id=49489982) = bfgeek 评 AI PR 淹没维护者。
- 其余评论页(49492193/49492219/49488282/49494182/49489057/49494151/49490702/49492632/49487341/49486081/49486334) 均抓取成功。
