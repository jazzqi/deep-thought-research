# Reference · HN 书摘 2026-09-06

## 数据来源

### HN 帖子（query_raw_items）

- Anthropic 形式化费马大定理: query_raw_items(source='hackernews', keyword='Anthropic OR Claude OR Opus', min_points=20)[id:292970] = ▲33 💬4, Formalizing Fermat's Last Theorem, 2026-09-04 19:06 UTC
- 美国两大校区 AI 禁令: query_raw_items(source='hackernews', keyword='AI agent', min_points=20)[id:295120] = ▲21 💬9, America's Two Largest School Districts Impose AI Moratoriums, 2026-09-05 23:06 UTC
- .gitignore 默认忽略一切: query_raw_items(source='hackernews', keyword='AI agent', min_points=20)[id:294835] = ▲34 💬28, .gitignore Everything by Default, 2026-09-05 15:32 UTC
- AI 事件响应失感: query_raw_items(source='hackernews', keyword='AI agent', min_points=20)[id:294472] = ▲21 💬5, AI handles incidents engineers lose touch, 2026-09-05 08:47 UTC
- Claude 新提示词歌词禁令: query_raw_items(source='hackernews', keyword='Anthropic OR Claude OR Opus', min_points=20)[id:294821] = ▲22 💬8, Claude's new system prompt doesn't want to reproduce song lyrics, 2026-09-05 15:17 UTC
- GPT-6 Astra 代码审查: query_raw_items(source='hackernews', keyword='AI agent', min_points=20)[id:294359] = ▲20 💬5, GPT-6 Astra in code review, 2026-09-05 07:32 UTC
- Intelligence Index v4.2: query_raw_items(source='hackernews', keyword='AI agent', min_points=20)[id:293858] = ▲21 💬4, Artificial Analysis Intelligence Index v4.2, 2026-09-05 01:02 UTC
- MikroTik 静默补丁: query_raw_items(source='hackernews', keyword='AI agent', min_points=20)[id:294015] = ▲20 💬9, Reversing MikroTik's Silent Patch, 2026-09-05 03:02 UTC
- Grep vs LSP: query_raw_items(source='hackernews', keyword='AI agent', min_points=20)[id:280746] = ▲31 💬10, Grep beats LSP, 2026-09-04 05:02 UTC
- Trusting-Trust 攻击: query_raw_items(source='hackernews', keyword='AI agent', min_points=20)[id:294784] = ▲26 💬0, Trusting-Trust Attack against an Entire Linux Distribution, 2026-09-05 14:36 UTC
- Kevin Kelly 诗集: query_raw_items(source='hackernews', keyword='Anthropic OR Claude OR Opus', min_points=20)[id:294848] = ▲20 💬7, Poetry book that Anthropic tried to censor, 2026-09-05 15:47 UTC
- OKF Agent Memory: query_raw_items(source='hackernews', keyword='AI agent', min_points=20)[id:295234] = ▲21 💬10, OKF Agent Memory, 2026-09-06 00:47 UTC
- OpenLake MLPerf: query_raw_items(source='hackernews', keyword='AI agent', min_points=20)[id:294967] = ▲29 💬1, OpenLake Leads MLPerf Storage v3.0, 2026-09-05 18:02 UTC
- Rust Vtables: query_raw_items(source='hackernews', keyword='AI agent', min_points=20)[id:294998] = ▲25 💬0, Visualizing Rust's Vtables, 2026-09-05 19:02 UTC
- AMD Threadripper Halo Station: query_raw_items(source='hackernews', keyword='AI agent', min_points=20)[id:294976] = ▲21 💬5, AMD Threadripper Halo Station, 2026-09-05 18:17 UTC
- 费马大定理 Lean 4 仓库: query_raw_items(source='hackernews', keyword='Anthropic OR Claude OR Opus', min_points=20)[id:293129] = ▲23 💬5, Fermat's Last Theorem in Lean 4, 2026-09-04 21:47 UTC

### 文章正文（fetch_url）

- 费马大定理形式化: fetch_url(https://www.anthropic.com/research/formalizing-fermats-last-theorem) = Claude 11天自主完成，1300万行 Lean，29500中间定理
- 美国校区 AI 禁令: fetch_url(https://www.techpolicy.press/americas-two-largest-school-districts-impose-ai-moratoriums/) = NYC K-8 禁止，LAUSD 一年暂停令
- .gitignore 反向策略: fetch_url(https://packagemain.tech/p/gitignore-everything-by-default) = 白名单策略，CLAUDE.md 等 AI 文件泛滥
- AI 事件响应失感: fetch_url(https://www.sylvainkalache.com/blog/ai-handles-incidents-engineers-lose-touch-with-their-systems/) = Bainbridge 1983悖论，航空模拟器对标
- Claude 提示词歌词禁令: fetch_url(https://simonwillison.net/2026/Sep/2/claudes-new-system-prompt/) = Fable 5.1 系统提示词变更，版权诉讼时间线
- GPT-6 Astra 代码审查: fetch_url(https://www.coderabbit.ai/blog/gpt-6-astra-code-review-evaluation) = 跨文件审查比 Opus 5 高33%
- Intelligence Index v4.2: fetch_url(https://artificialanalysis.ai/articles/artificial-analysis-intelligence-index-v4-2) = 私有测试集权重40%，Fable 5.1 领先
- MikroTik 静默补丁: fetch_url(https://npratley.net/reversing-mikrotiks-silent-patch-the-routeros-7-23-4-fix-they-wouldnt-explain/) = SSH 用户名 -2 全权限执行
- Grep vs LSP: fetch_url(https://www.agentconnect.md/blog/grep-beat-lsp-harness/) = 简单任务0-6%选LSP，引用任务45-57%
- Kevin Kelly 诗集: fetch_url(https://kk.org/cooltools/the-1930-poetry-book-that-anthropic-tried-to-censor/) = Kunitz 1930诗集，Claude 拒绝复现
- OKF Agent Memory: fetch_url(https://github.com/okf-memory/okf-agent-memory) = Git 原生 BM25 搜索 <300µs，token 膨胀降低80%
- OpenLake MLPerf: fetch_url(https://www.theopenlake.com/blog/openlake-leads-mlperf-storage-v3-0) = 6.72 GiB/s 写，11.55 GiB/s 读
- AMD Threadripper: fetch_url(https://www.tomshardware.com/...) = 96核 + 双液冷 MI350P，万亿参数模型

### 往期去重

- 基线: themes/hn-daily/index.md 往期列表（2026-08-15 ~ 2026-09-05），所有2026-09-05及更早日期的帖子已在往期报告中覆盖，本期（2026-09-06）仅收录2026-09-04 04:00 UTC 之后首次出现在 HN 首页的帖子。
