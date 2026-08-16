# Roundtable Scratchpad — podcast-digest

- Session: 2026-08-16_1809__manual__podcast_youtube_1_themes_podcast_digest_index_md_query_raw_i
- Lead: tech_generalist
- 议题: 播客/访谈学习文档（单集）：把最新一期已抓取的 podcast/YouTube 访谈转录稿 蒸馏为中文学习文档。只处理 1 集——取最近入库、尚未整理过的集 （与 themes/podcast-digest/index.md 的「往期」列表比对去重）。
【数据 · 全部工具查询，不注入数值】用工具主动取数（禁止凭空写数字）： - 主取数：query_raw_items 工具，source 前缀 'youtube:@ILTB_Podcast'
  或 'happyscribe:'，content_type='podcast'；优先 transcript 非空、
  最新 published_at 且未整理的集。
- 转录稿获取：query_raw_items 返回的 transcript 字段（单集 25-99KB，
  超长可分次读取/分段注入，禁止截断后凭猜补充）。

【规范 · 必读】用 ReadThemeDocsTool 读取两份规范后动笔： 1. themes/podcast-digest/template.md —— 学习文档结构 seed（总览 / TL;DR /
   核心论点 / 关键细节 / Key Takeaways；禁止编号顶层节——透传 publish 精确匹配）
2. themes/WRITING_GUIDE.md —— 写作硬规则（集体署名/金字塔原理/数字溯源）
【写作铁律】（写入产出文档）： - 金字塔原理（硬约束）：每节/每段结论先行，第一句就是答案或判断。
  禁止「本集讨论了…」「他分享了对…的看法」「在对话中我们了解到…」
  式开场白。摘要=讲内容本身，不是讲"这集讲了什么"。
- 避免转述式刻意口吻：禁止「主持人问道…嘉宾回答说…」「他谈到…」这类
  转述腔与访谈流程复述。直接以内容本身叙事；仅在署名观点时用「{嘉宾} 认为」。
- 中文为主 + 关键英文保留：只有确实无法简洁翻译的常见术语才保留英文
  （SaaS/LLM/ARR/CSP 等）；不保留金句原文+翻译（读者目标=获取认知，
  非学习句法）；不为了双语而双语。
- 信达，禁止生造词：使用常见同义中文表达（"新兴云厂商"而非"新云"、
  "云计算发展史"而非"云史"）。
- 演绎解释：必要时适当，不冗余——仅当该点反直觉/因果链不直观/术语难懂
  且是关键判断时才加，1-2 句直接给深层含义，禁止复述论据已说内容。
- 长度：推荐 转录稿每 10KB ≈ 350-400 字中文（82KB ≈ 2900-3300 字），
  仅为推荐值非硬限制——按内容丰富度增减，超多内容可同步增加行文长度。
- 溯源：所有数字/事实必须来自转录稿实际内容，禁止虚构；数字说话人不明时
  写"嘉宾认为"或直接陈述。
- 禁止 session 目录名/manual/internal 等内部元数据出现在正文。
【立场】服务作者与团队成员的二次学习，非投资建议。
【记忆 · 分析中自主沉淀】分析中如产生客观事实/带出处数据的关键结论， 可调用 remember 工具存储（个人记忆层）；无需存储已 publish 进主题文档的 完整内容（避免重复）。

- 参与 Agent: tech_generalist, ai_specialist, kevin_kelly, soros, karpathy, geopolitics_agent, buffett, kahneman
- 轮次: 1 / 1
- 状态: ok

## Lead 最终综合

{"action":"finalize","questions":["最新未整理集应为《Sam Altman on AGI, Compute, and Human Agency》（query_raw_items，id:123328），但当前工具返回的仅是转录稿片段，未提供可完整读取的 transcript 字段；因此无法按要求蒸馏完整学习文档，也无法可靠提取其全部论点、关键细节和数字。"],"confirmed_missing_indicators":[],"confirmed_event_mappings":[]}

## 第 1 轮（finalize）

- 问题: 最新未整理集应为《Sam Altman on AGI, Compute, and Human Agency》（query_raw_items，id:123328），但当前工具返回的仅是转录稿片段，未提供可完整读取的 transcript 字段；因此无法按要求蒸馏完整学习文档，也无法可靠提取其全部论点、关键细节和数字。
