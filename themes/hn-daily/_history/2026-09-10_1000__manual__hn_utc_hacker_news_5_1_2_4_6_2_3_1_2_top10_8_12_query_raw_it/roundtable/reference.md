# 数据溯源 — 2026-09-09 HN 书摘

## 帖子数据（query_raw_items source='hackernews'）
- iPhone Duo 202分/204评论: query_raw_items(source='hackernews', published_after='2026-09-09T00:00:00Z', published_before='2026-09-10T00:00:00Z')[id:339809]
- Anthropic 监控系统 92分/28评论: query_raw_items(source='hackernews')[id:337787]
- Anthropic 研究员辞职 79分/63评论: query_raw_items(source='hackernews')[id:325058]
- Apple Watch Series 12 71分/46评论: query_raw_items(source='hackernews')[id:339806]
- Automattic CEO 休假(404media) 50分/16评论: query_raw_items(source='hackernews')[id:340145]
- Automattic CEO 休假(TechCrunch) 21分/97评论: query_raw_items(source='hackernews')[id:341355]
- Muse/Meta 重名 47分/10评论: query_raw_items(source='hackernews')[id:340977]
- AirPods 5 45分/45评论: query_raw_items(source='hackernews')[id:339717]
- YC/Flock 44分/11评论: query_raw_items(source='hackernews')[id:336763]
- MacRumors iPhone Duo 41分/48评论: query_raw_items(source='hackernews')[id:339808]
- Claude Opus 5 demo 37分/4评论: query_raw_items(source='hackernews')[id:335023]
- Tailwind/Shopify 36分/8评论: query_raw_items(source='hackernews')[id:335177]
- DeepSeek V4.1 Flash 36分/3评论: query_raw_items(source='hackernews')[id:334798]
- Apple Watch Ultra 4 35分/70评论: query_raw_items(source='hackernews')[id:339971]
- RSA-260 factoring 22分/3评论: query_raw_items(source='hackernews')[id:341208]
- AI Psychosis Part 2 27分/7评论: query_raw_items(source='hackernews')[id:338458]
- AI Policy宣言 23分/12评论: query_raw_items(source='hackernews')[id:339881]
- Read the Docs DDoS 24分/10评论: query_raw_items(source='hackernews')[id:338802]

## 文章正文（fetch_url）
- Anthropic 监控系统正文: fetch_url(https://prospect.org/2026/09/09/anthropic-artificial-intelligence-surveillance-system-monitor-activists/) → 报道引述 Keon Ellison 播客访谈细节
- Automattic CEO 休假正文: fetch_url(https://www.404media.co/wordpress-automattic-ceo-matt-mullenweg-put-on-leave-of-absence/) → 付费墙限制，仅获取摘要
- Read the Docs DDoS 正文: fetch_url(https://about.readthedocs.com/blog/2026/09/2026-ddos-attack/) → 峰值 550 万请求/分钟，持续 10 天
- Google Ads 恶意软件误判正文: fetch_url(https://xlii.space/eng/malicious-software-on-google-ads/) → 开发者 Google Ads 账户被误判为恶意软件
- RSA-260 分解正文: fetch_url(https://cognition.com/blog/factoring-rsa-260) → Devin 自主构建 GPU 格基筛器，打破 RSA-250 记录
- Tailwind/Shopify 正文: fetch_url(https://tailwindcss.com/blog/tailwind-is-joining-shopify) → 周安装量 1.1 亿，MIT 协议保留
- Muse/Meta 正文: fetch_url(https://www.engadget.com/2254419/muse-the-band-lost-its-social-media-handles-to-muse-meta-s-new-ai-agent/) → 1999年注册商标，三次账号被夺
- AI Psychosis Part 2 正文: fetch_url(https://jeffs.blog/p/defining-ai-psychosis-part-2-prolific) → "高产AI精神病"概念定义
- GPT-6 Astra 分析正文: fetch_url(https://magazine.sebastianraschka.com/p/gpt-6-astra-looped-transformers-and) → looped transformers 架构分析

## 评论摘录（fetch_url HN comments pages）
- iPhone Duo 评论: fetch_url(https://news.ycombinator.com/item?id=49630931) → ksec 评论: "no crease at all"
- Anthropic 监控 评论: fetch_url(https://news.ycombinator.com/item?id=49628704) → cldellow 评论: 区分编辑渲染与事实
- Anthropic 辞职 评论: fetch_url(https://news.ycombinator.com/item?id=49619227) → huitzitziltzin 质疑"10%致灭论"
- Automattic 评论: fetch_url(https://news.ycombinator.com/item?id=49636283) → Shank 评论: "在全员频道发这种指控基本不会回来了"

## 数据说明
- 分数为采集时刻（ingestion time）数据，HN 分数随时间持续增长。iPhone Duo 在采集后 7 小时已增长至 898 分。
