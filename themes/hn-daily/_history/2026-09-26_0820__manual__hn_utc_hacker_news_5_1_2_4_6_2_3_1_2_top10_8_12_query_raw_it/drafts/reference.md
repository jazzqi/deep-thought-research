# 数据来源参考

## 帖子数据来源

- Claude Opus 5.5发布: query_raw_items(source=hackernews, published_after=2026-09-22T00:00:00Z, published_before=2026-09-26T00:25:00Z, min_points=20)[id:435736] = Anthropic发布Claude Opus 5.5，1793分，1118评论
- GPT-6 Sol and Luna发布: query_raw_items(source=hackernews, published_after=2026-09-22T00:00:00Z, published_before=2026-09-26T00:25:00Z, min_points=20)[id:435956] = OpenAI推出GPT-6 Sol和Luna，1769分，847评论
- Palantir AI过度依赖事件: query_raw_items(source=hackernews, published_after=2026-09-22T00:00:00Z, published_before=2026-09-26T00:25:00Z, min_points=20)[id:436148] = 五角大楼报告承认Palantir AI过度依赖导致打击造成123名伊朗儿童死亡，955分，541评论
- Jev模型发布: query_raw_items(source=hackernews, published_after=2026-09-15T00:00:00Z, published_before=2026-09-26T00:25:00Z, min_points=20)[id:400453] = TypeSafe AI发布Jev模型，声称成本降低40-400倍，速度提升20-200倍，1885分，494评论
- Xiaomi MiMo v2.6: query_raw_items(source=hackernews, published_after=2026-09-21T00:00:00Z, published_before=2026-09-26T00:25:00Z, min_points=20)[id:432439] = 小米发布MiMo v2.6，1123分，477评论
- Grok 4.7: query_raw_items(source=hackernews, published_after=2026-09-21T00:00:00Z, published_before=2026-09-26T00:25:00Z, min_points=20)[id:432099] = x.ai发布Grok 4.7，607分，529评论
- Qwen-Image-2.1: query_raw_items(source=hackernews, published_after=2026-09-20T00:00:00Z, published_before=2026-09-26T00:25:00Z, min_points=20)[id:428886] = Qwen发布Image-2.1，735分，198评论
- Claude Code更新: query_raw_items(source=hackernews, published_after=2026-09-18T00:00:00Z, published_before=2026-09-26T00:25:00Z, min_points=20)[id:427080] = Claude Code现在读取AGENTS.md，734分，275评论

## 文章正文来源

- Claude Opus 5.5评论页: fetch_url(url='https://news.ycombinator.com/item?id=49803892', max_chars=8000)
- GPT-6 Sol and Luna评论页: fetch_url(url='https://news.ycombinator.com/item?id=49805509', max_chars=8000)
- Palantir AI事件评论页: fetch_url(url='https://news.ycombinator.com/item?id=49806430', max_chars=8000)
- Jev模型文章: fetch_url(url='https://typesafe.ai/blog/introducing-system-one-models-and-jev', max_chars=8000)