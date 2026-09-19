# Reference — hn-daily 2026-09-19

## 数据来源追加（tech_scout 轮次）

### 头条深读
- Gemini 安全突破: query_raw_items(source=hackernews, keyword='Gemini hacked', published_after=2026-09-19)[id:427491] = Reuters 报道 Google Gemini 在安全测试中自主入侵三家公司
- Gemini 安全突破 HN 讨论: query_raw_items(source=hackernews, keyword='Gemini hacked')[id:427790] = BBC 同步报道，HN 讨论区 68 条评论

### 值得一读
- Laya 开源项目: query_raw_items(source=hackernews, keyword='Laya Jev', published_after=2026-09-19)[id:427861] = ConvAI Innovations 发布 Laya，846 分 208 评论
- 韩国数据泄露罚款: query_raw_items(source=hackernews, min_points=1, published_after=2026-09-19, keyword='Korea data breach')[id:428096] = 韩国修订数据保护法，罚款提至年收入 10%，321 分 107 评论
- GPT-6 Astra 密码破解: query_raw_items(source=hackernews, keyword='GPT-6 Astra', published_after=2026-09-19)[id:427676] = GPT-6 Astra 破解 ADFGVX 密码，343 分 157 评论
- OpenAI 芯片设计: query_raw_items(source=hackernews, keyword='OpenAI chip', published_after=2026-09-19) = IEEE Spectrum 报道 Jalapeño 芯片，190 分 128 评论
- 斯坦福大脑研究: query_raw_items(source=hackernews, keyword='brain separate organs', published_after=2026-09-19)[id:427634] = Nature Neuroscience 论文，573 分 208 评论

### 技术雷达
- 微软 AI 抓取: query_raw_items(source=hackernews, keyword='Microsoft AI scraping', published_after=2026-09-19)[id:428111] = NYT 诉讼文件披露微软内部表述，34 分 6 评论
- CUA-S1: query_raw_items(source=hackernews, keyword='CUA-S1', published_after=2026-09-19)[id:427977] = Cua 团队发布 Computer Use 小型专用模型，29 分 3 评论
- ZK-JPEG: query_raw_items(source=hackernews, keyword='ZK-JPEG', published_after=2026-09-19)[id:428122] = 零知识证明 JPEG 压缩验证，36 分 5 评论
- ZK-JPEG 论文正文: fetch_url(url=https://eprint.iacr.org/2026/2039) = Stealth Software Technologies 与佛蒙特大学联合论文，PicoZK 框架

### 社区之声
- AI 写作辩论: query_raw_items(source=hackernews, keyword='Almost Never Use AI Write', published_after=2026-09-19)[id:428021] = Erich Grunewald 文章，39 分 18 评论
- AI 写作正文: fetch_url(url=https://erichgrunewald.substack.com/p/why-you-should-almost-never-use-ai) = 三论点反对 AI 代写：写作即思考、AI 文本模糊错误、不标注即欺骗
- AI 帖子高分 meta 讨论: query_raw_items(source=hackernews, keyword='AI posts points HN', published_after=2026-09-19)[id:427860] = Ask HN 帖子，25 分 26 评论
- AI 帖子高分评论: fetch_url(url=https://news.ycombinator.com/item?id=49764057) = 三重机制解释：三类人群涌入、astroturfing 怀疑、新用户高兴趣
- 面试数据点: fetch_url(url=https://news.ycombinator.com/item?id=49768826) = Ask HN 面试讨论，status_quo69 评论：AI 生成提交物的候选人全部未通过后续测试
