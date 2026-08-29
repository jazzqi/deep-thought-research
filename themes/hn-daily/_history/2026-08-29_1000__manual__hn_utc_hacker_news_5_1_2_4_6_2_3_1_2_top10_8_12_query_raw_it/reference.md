# reference.md — HN 书摘 2026-08-28（周六）数据溯源

## 取数窗口与方法
- 窗口：2026-08-28 00:00 → 2026-08-29 00:00 UTC（前一日 UTC 窗口）
- 主取数：query_raw_items(source=null) 全量返回后，消费端按 [hackernews] 标签 + 时间戳过滤（source='hackernews' 查询层过滤失效，已确认多次）
- 机械门槛 hn_points≥20 在本窗口无帖达成（最高 ▲2），故按"四维精筛"以 LLM 判断补位

## 数据点溯源
- OpenAI 在 ChatGPT 投放广告（Free/Go 计划，2026-08 月底起，初期非个性化，依据对话主题+大致位置+设备类型，不使用历史对话/记忆）: query_raw_items(source=null)[id:189870] = We're rolling out ads in ChatGPT（OpenAI 隐私政策更新通知）
- 广告细节（Plus/Pro/Enterprise/Business/Education 无广告；广告不影响回答；不与广告主共享对话）: fetch_url(https://news.ycombinator.com/item?id=49483929) = OpenAI 隐私政策更新全文 + 评论
- Moonshot Kimi K3（2.8 万亿参数）与微软/AWS/Google Cloud 谈判托管与收入分成（最高 30%）；阿里亦谈类似安排: query_raw_items(source=null)[id:189018] = Moonshot and Nvidia Talks Show Chinese AI Models Moving into the Enterprise
- 中国每日 AI token 调用量超 500 万亿（截至 2026-06）；模型迭代周期 3 个月→4-6 周；腾讯混元 3 首周 token 为混元 2 的 68 倍: query_raw_items(source=null)[id:188036] = China's daily AI token usage tops 500 trillion
- Promptless 重构代码库使单工程师产出 3-5 倍、bug 率不升；重构前 on-call 占 30-40%、59% 新代码短期被重写: query_raw_items(source=null)[id:189023] = Field rearchitecting our codebase 5x'ed our code output
- Irreplaceable 组织成立（气候运动老兵 Phil Aroneanu/350.org、Jeremy Ornstein/Sunrise）；民调 3/4 反对本地数据中心、3/4 认为 AI 损就业、近 70% 认为过快: query_raw_items(source=null)[id:190072] = The AI Backlash Gets Professional
- 跨境电力约 60 条国际 HVDC 链路（RTE International 2026-07 库存），欧洲主导: query_raw_items(source=null)[id:189953] = Energy Security Is Increasing the Value of Cross-Border Electricity
- Show HN: Claude Code Skills 解决上下文膨胀: query_raw_items(source=null)[id:190041] = Show HN: Claude Code Skills – Solving context bloat
- Show HN: Conduct 开源 LLM/MCP 护栏: query_raw_items(source=null)[id:189022] = Show HN: Conduct, open-source guardrails for LLM and MCP tool calls
- Show HN: Rundown 集成 Claude Code+Codex 的 HN 客户端: query_raw_items(source=null)[id:189755] = Show HN: Hacker News Client with Claude Code and Codex Integration
- Show HN: 拍卖 RTX 5090 贴纸位: query_raw_items(source=null)[id:189784] = Show HN: I'm auctioning 10 sticker spots on an RTX 5090
- Show HN: Sesame 本地优先开源密码管理器: query_raw_items(source=null)[id:189010] = Show HN: Sesame – a local-first, open-source password manager

## 数据质量备注
- 分数/评论数取自 query_raw_items 的 metadata.hn_points / hn_comments；抓取时部分帖 live HN 计数已略升（如 id:190072 元数据 ▲1·💬1，live 页显示 3 分·4 评论），以元数据为准。
- 本窗口 HN 互动异常低迷（约 44 条 hackernews 帖，最高 ▲2），属低活跃日，非数据缺失。


# 审查人 tech_scout 交叉核验追加（2026-08-29 02:16 UTC）

- 源过滤失效复验: query_raw_items(source='hackernews', limit=200) = 仍仅 9 条（id:173855/173305/146460/145875/122607/99390/45862/114342/114340），最新仅 2026-08-27、最旧 2026-06-30，且混入 longbridge 泄漏；与 reference.md 首段一致，确认 source 过滤在查询层失效，拿不到 2026-08-28/29 窗口帖。
- 2026-08-28/29 窗口真实 HN 帖（keyword 检索可得，source 过滤拿不到）— 早期技术信号视角 must-cover：
  - OpenAI 终止 Cursor 合作（SpaceX 600 亿美元收购后）: query_raw_items(keyword=Cursor)[id:190899] = ▲8 💬1 @meetpateltech, 2026-08-29 02:02, openai.com 官方声明
  - Show HN: ArchLex（AWS/GCP/K8s 图表 DSL）: query_raw_items(keyword=Show HN)[id:190866] = ▲1, 2026-08-29 01:32
  - Show HN: Claude Code Skills starter kit: query_raw_items(keyword=claude-skills)[id:190041] = ▲2, 2026-08-28 22:02
  - Anthropic 诉五角大楼胜诉（ibtimes 转述）: query_raw_items(keyword=Anthropic)[id:190642] = ▲4, 2026-08-28 23:36
  - OSS harness 将 Claude Opus 5 从 30% 拉到 99.95% ARC-AGI-3: query_raw_items(keyword=claude-skills)[id:184072] = ▲5, 2026-08-28 15:47
  - Ask HN: AI 写得比我还好，如何保住身份: query_raw_items(keyword=claude-skills)[id:186702] = ▲3 💬2, 2026-08-28 18:02
  - Show HN: Rafter（MCP server 共享团队记忆/技能/Agent）: query_raw_items(keyword=Cursor)[id:180739] = ▲1, 2026-08-28 09:06
  - Show HN: AgentCloud（MCP-first iOS 模拟器云）: query_raw_items(keyword=Cursor)[id:175517] = ▲1, 2026-08-27 19:32
  - Show HN: Concord（Claude Code/Codex/Cursor 互聊）: query_raw_items(keyword=Cursor)[id:168383] = ▲1, 2026-08-27 13:47
  - Show HN: Agentctl（Agent harness 的 Terraform）: query_raw_items(keyword=claude-skills)[id:187217] = ▲1, 2026-08-28 18:32
  - Show HN: Agentify Chat（Codex/Claude/Grok CLI 端到端加密远程）: query_raw_items(keyword=claude-skills)[id:187218] = ▲1, 2026-08-28 18:32
  - Show HN: HN Client with Claude Code/Codex: query_raw_items(keyword=claude-skills)[id:189755] = ▲2, 2026-08-28 20:06
  - data center backlash（BI/Engadget）: query_raw_items(keyword=data center)[id:190869] = ▲3 💬1, 2026-08-29 01:32; [id:190844] = ▲2, 2026-08-29 01:17
  - Anthropic self-improving AI: query_raw_items(keyword=Anthropic)[id:190074] = ▲1, 2026-08-28 22:17, techcrunch
  - Chardet v7 rewrite controversy: query_raw_items(keyword=claude-skills)[id:190055] = ▲2, 2026-08-28 22:06
- 数据质量复验: reference.md 记 id:177572（Anthropic 诉五角大楼）入库 hn_points=5，但 HN 实时页 533 分；同主题另一提交 id:190642 入库 ▲4。结论：raw hn_points 不可信，排名须以实时页或 LLM 判断为准，不能机械按分筛选。
