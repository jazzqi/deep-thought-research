# 参考文献

## 原始条目引用

- Passkeys 文章热度与评论: query_raw_items(keyword='passkeys OR passkey', source='hackernews', min_points=50, published_after='2026-09-18T00:00:00Z')[id:426173] = ▲662 💬647 ethanhawksley, I don't like passkeys
- Hacktron 攻击 OpenAI: query_raw_items(keyword='hacktron OR openai hack', source='hackernews', min_points=50, published_after='2026-09-18T00:00:00Z')[id:424569] = ▲468 💬197 Handy-Man, Hacking OpenAI
- 巴菲特卸任: query_raw_items(keyword='buffett OR berkshire', source='hackernews', min_points=50, published_after='2026-09-18T00:00:00Z')[id:426050] = ▲261 💬172 saimiam, Warren Buffett Steps Down
- Conway 猜想证明: query_raw_items(keyword='conway OR abramov OR lean proof', source='hackernews', min_points=50, published_after='2026-09-18T00:00:00Z')[id:426525] = ▲198 💬174 m-hodges, I Vibed a Proof of Conway's Conjecture
- Cloudflare Quick Tunnels: query_raw_items(keyword='cloudflare tunnel', source='hackernews', min_points=50, published_after='2026-09-18T00:00:00Z')[id:426554] = ▲510 💬218 jcbhmr, Cloudflare Quick Tunnels
- ZCode 静默上传: query_raw_items(keyword='zcode OR git history upload OR silent upload', source='hackernews', min_points=50, published_after='2026-09-18T00:00:00Z')[id:426019] = ▲256 💬64 cdnsteve, ZCode silently uploads your Git history
- HarnessTax 论文: query_raw_items(keyword='zcode OR git history upload OR silent upload', source='hackernews', min_points=50, published_after='2026-09-18T00:00:00Z')[id:416942] = ▲225 💬93 matt_d, HarnessTax: How Much Does the Harness Matter for Coding Agents?

## 网页抓取来源

- Passkeys 文章正文: fetch_url('https://hawksley.dev/blog/i-dont-like-passkeys') = 完整技术分析，含硬件密钥容量限制、云同步锁定风险、第三方管理器 UX 问题
- Hacktron 文章正文: fetch_url('https://www.hacktron.ai/blog/hacking-openai') = 完整攻击链描述，72 小时时间线，$6,500 赏金细节
- Passkeys HN 评论: fetch_url('https://news.ycombinator.com/item?id=49753211') = dspillett 评论，Amazon passkey 体验批评
- Hacktron HN 评论: fetch_url('https://news.ycombinator.com/item?id=49749656') = btown 引用攻击描述，wood_spirit 关于 AI 安全军备竞赛的评论
- Conway 证明文章: fetch_url('https://overreacted.io/how-i-vibed-a-proof-of-conways-conjecture/') = Dan Abramov 自述，surreal numbers 背景，Lean 证明过程
- Bend 2 文章: fetch_url('https://blog.liampwll.com/posts/bend_vibe_coding/') = vibe coding 认知盲区分析，SPARK 对比验证
