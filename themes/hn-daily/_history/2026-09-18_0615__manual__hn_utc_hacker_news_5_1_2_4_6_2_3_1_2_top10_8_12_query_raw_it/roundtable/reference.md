# tech_scout 审查数据来源

## query_raw_items 数据源

- 9月16日HN全量帖子（≥30分）: query_raw_items(source='hackernews', published_after='2026-09-16T00:00:00Z', published_before='2026-09-17T00:00:00Z', min_points=30) = 59条
- Small Programming Tricks确认存在: query_raw_items(source='hackernews', keyword='Small Programming Tricks')[id:413137] = "▲633 💬274, 作者 signa11, will-keleher.com"
- Cloudflare Security-Audit-Skill日期确认: query_raw_items(source='hackernews', keyword='Cloudflare Security Audit Skill')[id:421885] = "▲180 💬36, published 2026-09-17 04:36 UTC"
- OpenAI NYT披露确认: query_raw_items(source='hackernews', keyword='OpenAI Astra prompt injection compaction')[id:417043] = "▲91 💬88, published 2026-09-17 01:02 UTC"
- OpenAI Astra prompt injection确认: query_raw_items(source='hackernews', keyword='Astra prompt injection compaction')[id:422589] = "▲85 💬22, published 2026-09-17 05:13 UTC"
- Breaking 1.58-bit Ternary LLMs确认: query_raw_items(source='hackernews', keyword='ternary LLM 1.58 bit quantization')[id:415993] = "▲234 💬37, arxiv.org"
- HarnessTax确认: query_raw_items(source='hackernews', keyword='HarnessTax coding agents harness')[id:416942] = "▲212 💬87, harnesstax.github.io"
- Dream-RSI确认: query_raw_items(source='hackernews')[id:411990] = "▲207 💬50, arxiv.org"
- DeepMind Institute确认: query_raw_items(source='hackernews', keyword='DeepMind Institute launch')[id:414775] = "▲179 💬69, institute.deepmind.com"
- OpenSpec确认: query_raw_items(source='hackernews')[id:416632] = "▲186 💬92, openspec.dev"
- DeepSeek v4.1 Flash确认: query_raw_items(source='hackernews')[id:411987] = "▲171 💬66, enclave.ai"
- Backups Aren't Simple确认: query_raw_items(source='hackernews', keyword='Backups aren't simple')[id:416597] = "▲338 💬201"
- Cloudflare AI爬虫确认: query_raw_items(source='hackernews')[id:403331] = "▲86 💬49, blog.cloudflare.com"
- OpenAI广告评论数校正: query_raw_items(source='hackernews')[id:411891] = "▲156 💬176（文档写178，差2）"
- 微软/Anthropic评分校正: query_raw_items(source='hackernews')[id:412560] = "▲40 💬3, Points: 23（文档用23分，与全文▲惯例不一致）"
- Australia跟进Canada确认: query_raw_items(source='hackernews')[id:416612] = "▲236 💬208"
- How Stale Is Your AI?确认: query_raw_items(source='hackernews')[id:411988] = "▲78 💬45"
- ImpactGate确认: query_raw_items(source='hackernews')[id:411889] = "▲36 💬48"
