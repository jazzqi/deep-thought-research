# Roundtable Scratchpad — hn-daily

- Session: 2026-09-03_1000__manual__hn_utc_hacker_news_5_1_2_4_6_2_3_1_2_top10_8_12_query_raw_it
- Lead: tech_generalist
- 议题: HN 书摘每日扫描：昨日（前一日 UTC 窗口）Hacker News 高价值帖子书摘。 产出 5 栏目：头条深读（1-2 条）/ 值得一读（4-6 条）/ 技术雷达（2-3 条）/ 社区之声（1-2 条）/ 数据速览（Top10 快照），共 8-12 条。
【数据 · 全部工具查询，不注入数值】用工具主动取数（禁止凭空写数字）： - 主取数：query_raw_items 工具，source='hackernews'，按前一日 UTC 窗口
  （created/ingested 前一日 00:00 → 当日 00:00）筛选。
  机械过滤：metadata 的 hn_points ≥ 20（采集端已带分）；同 URL 去重；
  跨天去重（用 ReadThemeDocsTool 读 themes/hn-daily/index.md 的「往期」列表比对标题）。
- 每条入选帖的正文/摘要：query_raw_items 返回的 full_text 优先；
  缺失则用 web 搜索/直接抓取原文补充（抓不到就标注"未能抓取"，不虚构）。
- 评论摘录：用 Algolia HN items API 或评论区抓取（可选，有则摘 1 条高质量评论）。
【规范 · 必读】用 ReadThemeDocsTool 读取两份规范后动笔： 1. themes/hn-daily/template.md —— 5 栏目结构 seed（## 头条深读 / ## 值得一读 /
   ## 技术雷达 / ## 社区之声 / ## 数据速览；禁止编号顶层节——透传 publish 精确匹配）
2. themes/WRITING_GUIDE.md —— 写作硬规则（集体署名/金字塔原理/数字溯源）
【方法 · 四维精筛】机械过滤只是保底线（去重/类型/分数≥20），**价值判断由 LLM 完成**： 对候选独立打分（1-5）：信息密度（新事实/数据/决策 vs 观点水贴）、 一手性（作者亲历 vs 二手转述）、讨论深度（评论区是否已产生高质量延伸）、 行业相关性（对科技从业者的 relevance）。≥4 入选；3 分按名额递补；<3 淘汰。 分数只是参考信号，**不要纯按分数排序选帖**——低分但有洞察的帖子（技术雷达/社区之声 栏目）应入选，高分但信息量低的（标题党/重复/宣传稿）应淘汰。 辅助信号：hn_points/hn_comments 比（高分低评论 ≈ 标题党嫌疑）。
【质量铁律】① 摘要必须基于实际抓到的正文——raw_items.full_text 只有元数据时， 用 fetch_url 工具按 URL 抓取文章正文（HTTPS 优先），抓不到才标注"未能抓取"—— 宁可失败得明显，不成功得虚假；② 每条带原文链接可追溯（原文 + 评论）； ③ 中文为主，标题保留英文原文 + 中文翻译副标题（无域名后缀）； ④ 摘要/批注/评论摘录直接讲内容，禁止"标题宣布""该文介绍"类开场白， 金字塔原则结论先行，篇幅从短信息密度优先。 禁止 session 目录名/manual/miss 等内部元数据出现在正文。
【立场】服务科技行业从业者的每日信息扫描，不输出投资建议。
【记忆 · 分析中自主沉淀】分析中如产生以下内容，调用 remember 工具存储（个人记忆层）： - 客观事实 / 带出处与数据的关键结论（如"非农 -2.3万，美元走低黄金上涨"） - 短期有效的观察（如"9月加息25bp隐含概率 56.5%"） 无需存储：过程性描述、已 publish 进主题文档的完整内容（避免重复）。

- 参与 Agent: tech_generalist, tech_scout, ai_specialist, kevin_kelly
- 轮次: 0 / 1
- 状态: degraded

## 讨论概况

（无轮次记录——讨论在首轮前即终止/超时）

# 审查结论 - tech_scout

## 审查结果（按严重度分级）

🚫 **blocker** — 多处原文链接指向主页而非具体文章，导致信息无法溯源。例如：
- Gemini 3.8 Flash 链接为 `https://blog.google`（应为具体博客文章URL）
- LWN 订阅价格调整链接为 `https://lwn.net`（应为具体文章URL）
- Mistral opt-out 链接为 `https://mistral.ai`（应为具体文档URL）
- Perplexity SEO 研究链接为 `https://trellner.com`（应为具体研究页面URL）
**必须返工**：为每条补充具体、可访问的原文链接。

⚠️ **concern** — 技术雷达栏目内容偏移：当前3条内容（LLM推理优化、Mac mini本地部署、Dyson牙刷）均非新工具/新库/新论文/Show HN。技术雷达应聚焦新兴技术工具，建议补充如 Show HN: Woxi（开源Mathematica重实现）、Launch HN: machine0（CLI管理GPU VM）等当日高分技术项目。

⚠️ **concern** — AI infra/开发者生态方向可能被低估：文档覆盖了LLM推理优化和本地部署，但遗漏了当日其他重要技术帖子，例如：
- Zed: Delta（672分）— 开发者工具更新
- Codex in ChatGPT desktop app for Linux（463分）— AI开发工具
- llama.cpp 更新（362分）— 本地LLM基础设施
建议评估是否将部分"社区之声"或"值得一读"名额分配给这些帖子。

⚠️ **concern** — 分数数据不一致：文档中部分帖子分数与query_raw_items查询结果差异较大（如Gemini 3.8 Flash文档写837分，raw_items显示27-33分；Firefox文档写938分，raw_items显示776分）。可能是数据源不同（如Hacker News API vs 爬虫），但需核实确保准确性。

✅ **pass** — 中文表达自然流畅，emoji/格式使用克制，符合HN书摘风格。无堆砌问题。

✅ **pass** — 每条均有真实摘要，内容准确，与标题对应。

## 审查依据
- 使用query_raw_items独立核查了Krebs驾照泄露、Gemini 3.8 Flash发布等关键事件，确认事件真实存在。
- 对比了文档覆盖的11条帖子与raw_items高分帖子列表，识别出技术雷达栏目覆盖不足。
- 验证了所有原文链接的可访问性（部分指向主页无法溯源）。

## 建议修改优先级
1. **立即修复**：补充所有不具体原文链接（blocker）
2. **建议调整**：重新平衡技术雷达栏目内容，增加新工具/Show HN覆盖
3. **可选优化**：核实分数数据来源，确保一致性