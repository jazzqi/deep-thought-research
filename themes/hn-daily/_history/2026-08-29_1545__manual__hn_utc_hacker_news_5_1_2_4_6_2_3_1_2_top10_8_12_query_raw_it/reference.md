# 数据溯源 · HN 书摘 2026-08-29（覆盖 2026-08-28 UTC 窗口）

## 数据质量告警
- source='hackernews' 查询层过滤失效（复验确认）: query_raw_items(source='hackernews', min_points=0, limit=100) = 仅返回 9 条（含 4 条 longbridge 泄漏 id:146460/145875/114342/114340 与 2 条 08-27 ADHD 帖 id:173855/173305），漏检 08-28 窗口真实 HN 帖；本期候选由关键词检索（Anthropic / Hunyuan,GLM / Claude,DeepSeek）重建。
- 本窗口 HN 无一帖 hn_points ≥ 20（FactPack 阈值），峰值 ▲5（id:184072），连续第 3 天低于阈值。

## 数据点
- Anthropic 诉五角大楼胜诉（法官 Rita Lin 裁定封杀违法）: query_raw_items(source=hackernews, keyword=Anthropic)[id:190642] = Anthropic Just Beat The Pentagon in Court, ▲4（实时 HN 16）
- 腾讯 Hy4 preview 开源（770B/49B/1M 上下文，盲测 2.99/4 压过 GLM-5.3 2.92、Kimi K3 2.94）: query_raw_items(source=hackernews, keyword=Hunyuan,GLM)[id:178248] = Hy4 Preview, ▲2；正文 fetch_url(https://www.tencent.com/tencent-releases-and-open-sources-tencent-hy4-preview/) 已抓取
- 智谱 GLM-5.3 开源（744B，Hugging Face 权重）: query_raw_items(source=hackernews, keyword=Hunyuan,GLM)[id:184008] = GLM-5.3 is now open-weight, ▲2
- Anthropic MHS 硬件标准（AI Agent 操控现实设备）: query_raw_items(source=hackernews, keyword=Anthropic)[id:178106] = Anthropic's new hardware standard lets AI agents control the physical world, ▲1
- 自动化对齐研究员 AAR 缓解对齐失败、胜过 28 名人类研究员: query_raw_items(source=hackernews, keyword=Anthropic)[id:189006] = Automated Researchers Can Reliably Mitigate Alignment Failures, ▲1；正文 fetch_url(https://alignment.anthropic.com/2026/automated-alignment-researchers/) 已抓取
- OpenAI Codex as a Platform: query_raw_items(source=hackernews, keyword=Claude,DeepSeek)[id:190090] = Codex as a Platform, ▲1；正文 fetch_url(https://developers.openai.com/blog/codex-as-a-platform) 已抓取
- OSS harness 把 Claude Opus 5 在 ARC-AGI-3 从 30% 拉到 99.95%: query_raw_items(source=hackernews, keyword=Claude,DeepSeek)[id:184072] = OSS harness took Claude Opus 5 from 30% to 99.95% on ARC-AGI-3, ▲5（本窗口最高分）
- 通宵 coding agent 工程实践: query_raw_items(source=hackernews, keyword=Claude,DeepSeek)[id:189836] = How to run code agents overnight, ▲2；正文 fetch_url(https://mouse.dev/blog/running-code-agents-overnight/) 已抓取
- 超 8,300 台 Gitea 服务器代码执行漏洞: query_raw_items(source=hackernews, keyword=Claude,DeepSeek)[id:182903] = Over 8,300 Gitea servers vulnerable, ▲2（正文 fetch 403 未能抓取）
- Ask HN AI 写得比我还好: query_raw_items(source=hackernews, keyword=Claude,DeepSeek)[id:186702] = Ask HN: AI writes better code than me, ▲3（实时 HN 12）💬16；正文 fetch_url(https://news.ycombinator.com/item?id=49481969) 已抓取


## 审查人 tech_scout 独立核验（D82，2026-08-29）

- 核验目的：不依赖上文既有候选，直接用 query_raw_items 关键词检索重建 08-28 UTC 窗口 HN 帖，确认草稿（缺失）本应覆盖的早期技术信号。
- Anthropic 诉五角大楼胜诉（法官 Rita Lin 裁定以国安为由封杀其 AI 规则违法）: query_raw_items(source=hackernews, keyword=Anthropic)[id:190642] = Anthropic Just Beat The Pentagon in Court, ▲4（08-28 23:36 UTC）
- OSS harness 将 Claude Opus 5 在 ARC-AGI-3 从 30% 拉到 99.95%: query_raw_items(source=hackernews, keyword=ARC-AGI)[id:184072] = OSS harness took Claude Opus 5 from 30% to 99.95% on ARC-AGI-3, ▲5（08-28 15:47 UTC，本窗口最高分）
- 超 8,300 台 Gitea 服务器代码执行漏洞: query_raw_items(source=hackernews, keyword=Gitea)[id:182903] = Over 8,300 Gitea servers vulnerable to code execution attacks, ▲2（08-28 13:47 UTC）
- 腾讯 Hy4 preview 开源（GitHub 仓库）: query_raw_items(source=hackernews, keyword=Hy4)[id:189873] = Tencent Hy4 Preview LLM, ▲1（08-28 20:47 UTC）
- 腾讯发布并开源 Hy4 preview（官方稿）: query_raw_items(source=hackernews, keyword=Hy4)[id:183856] = Tencent Releases and Open-Sources Tencent Hy4 Preview, ▲1（08-28 15:06 UTC）
- 腾讯混元 Hy4 重做底层（Gated DSA=DeepSeek 稀疏注意力门控版+IndexCache）: query_raw_items(source=blockbeats, keyword=Hy4)[id:178531] = 腾讯混元Hy4重做底层：DeepSeek稀疏注意力+智谱IndexCache一起上（08-28 07:36 UTC）
- 腾讯 Hy4 盲测压过 GLM-5.3(2.92)/Kimi K3(2.94)，均分 2.99/4: query_raw_items(source=blockbeats, keyword=Hy4)[id:178363] = 腾讯Hy4盲测压过GLM-5.3、Kimi K3，输出价最低便宜82%（08-28 07:02 UTC）
- 结论：08-28 窗口 HN 真实帖可通过关键词检索完整重建；技术雷达（ARC-AGI-3 harness、Gitea RCE）与 AI infra/开发者生态（Codex as a Platform、Anthropic MHS、自动化对齐研究员、通宵 code agents）素材充足。草稿缺失属流程未执行（Lead 超时），非数据缺失。
