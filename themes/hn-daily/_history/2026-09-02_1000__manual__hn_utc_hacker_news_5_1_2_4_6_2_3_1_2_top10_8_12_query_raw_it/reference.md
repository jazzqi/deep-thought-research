# reference.md — 交叉审查数据来源

- query_raw_items(source='hackernews') 数据管道第 8+ 次确认结构性失效：仅返回低分陈旧条目（▲1-4），无法获取 2026-09-01 窗口高分帖子（947/836/807 等）: query_raw_items(source='hackernews', limit=50) = 28 条，最新条目 id:235155（2026-09-01 20:17），全部 ▲1-2
- Anthropic Fable 5.1 主公告（HN 前页帖）: query_raw_items(keyword='Anthropic OR Claude OR Fable OR Mythos')[id:234821] = "Claude Fable 5.1 and Claude Mythos 5.1" (▲15, 2026-09-01 18:17) — 注意: raw_items 分数 15 与文档声称的 947 分存在差异，可能因入库时间不同步
- AnkiDroid Google Play 捐赠链接被禁: query_raw_items(keyword='AuroraStore OR AnkiDroid OR Fastpotify OR LibreOffice')[id:228430] = "AnkiDroid: Google Play no longer allowing Open Collective donation link" (▲2, 2026-09-01 10:32)
- AuroraStore 被封: query_raw_items(keyword='AuroraStore OR AnkiDroid OR Fastpotify OR LibreOffice')[id:232058] = "Play Store blocks AuroraStore, hurting GrapheneOS users" (▲2, 2026-09-01 16:02)
- Fastpotify: query_raw_items(keyword='AuroraStore OR AnkiDroid OR Fastpotify OR LibreOffice')[id:217799] = "Fastpotify" (▲2, 2026-09-01 03:03)
- Jujutsu/ERSC: query_raw_items(keyword='ARC-AGI OR transformer OR Qwen OR Jujutsu')[id:234754] = "The creator of Jujutsu has joined ERSC" (▲4, 2026-09-01 18:02)
- Qwen3.8-Flash-Next 本地运行: query_raw_items(keyword='ARC-AGI OR transformer OR Qwen OR Jujutsu')[id:210827] = "Show HN: Slotstream, run Qwen3.8-Flash-Next 4-bit on a low-memory Mac" (▲1, 2026-08-31 15:02)
- Ambient CSS v3: query_raw_items(keyword='Semantic Overlays OR prompt injection OR Ambient CSS')[id:232006] = "Ambient CSS v3 – Blender meets CSS" (▲2, 2026-09-01 15:47)
- OpenAI Astra 模型延迟: query_raw_items(keyword='OpenAI OR Mac Mini OR Mac Studio OR FTC OR Amazon')[id:235842] = "OpenAI delayed its new model's development after the Hugging Face hack" (▲2, 2026-09-01 23:17) — 文档未覆盖
- FTC 指控 Amazon 广告竞价操控: query_raw_items(keyword='OpenAI OR Mac Mini OR Mac Studio OR FTC OR Amazon')[id:235900] = "FTC alleges Amazon illegally made $20B by rigging billions of ad auctions" (▲2, 2026-09-01 23:36) — 文档未覆盖
- Google Gemini 3.8 Flash 编码能力: query_raw_items(keyword='OpenAI OR Mac Mini OR Mac Studio OR FTC OR Amazon')[id:235901] = "New Google AI Model Said to Narrow Gap on Coding Ability (Gemini 3.8 Flash)" (▲1, 2026-09-01 23:36) — 文档未覆盖
- Semantic Overlays (LLM prompt injection 防御): query_raw_items(keyword='ARC-AGI OR transformer OR Qwen OR Jujutsu')[id:234747] = "Show HN: Semantic Overlays – an NX bit for LLM prompt injection (live demo)" (▲3, 2026-09-01 18:02) — 文档未覆盖
- Agent 安全: coding agent AWS 密钥暴露 query_raw_items(keyword='OpenAI OR Mac Mini OR Mac Studio OR FTC OR Amazon')[id:235322] = "Your coding agent has your AWS keys and an open internet connection" (▲2, 2026-09-01 21:02) — 文档未覆盖
- Perplexity Mac 隐私混合计算: query_raw_items(keyword='OpenAI OR Mac Mini OR Mac Studio OR FTC OR Amazon')[id:235892] = "Perplexity launches privacy-minded 'hybrid compute' AI feature for Mac" (▲2, 2026-09-01 23:32) — 文档未覆盖
- ⚠️ 注意: 文档声称的 HN 前页分数（947/836/807 等）来自 fetch_url 抓取 HN 前端页面，与 query_raw_items 数据库中对应条目的分数（15/2/2 等）存在显著差异，可能因 raw_items 入库时间点不同步所致，无法通过当前数据库完全验证
