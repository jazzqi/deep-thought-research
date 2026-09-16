# 数据来源溯源

## query_raw_items 查询

- 2026-09-15 HN 窗口（≥20分）: query_raw_items(source='hackernews', min_points=20, published_after='2026-09-15T00:00:00Z', published_before='2026-09-16T00:00:00Z') = 18 条
- Show HN 补充查询: query_raw_items(source='hackernews', keyword='Show HN', min_points=1, published_after='2026-09-14T00:00:00Z', published_before='2026-09-16T00:00:00Z') = 80 条

## 入选条目详情

- DeepMind 前研究员公开指控 Google: query_raw_items(source='hackernews')[id:392985] = ▲20 💬11 - I worked at Google DeepMind. You should listen to the warnings about AI (2026-09-15 02:25 UTC)
- AI agent 生成不可理解混合语言: query_raw_items(source='hackernews')[id:405062] = ▲20 💬1 - AI models chatting in 'surreal' dialect (2026-09-15 18:37 UTC)
- e-ink 相框听鸟鸣画插画: query_raw_items(source='hackernews')[id:396507] = ▲73 💬21 - Fugleramme e-ink bird frame (2026-09-15 12:31 UTC)
- Schneier/Cohn 大规模监控 25 年: query_raw_items(source='hackernews')[id:396506] = ▲25 💬3 - 25 Years of Mass Surveillance Is Enough (2026-09-15 12:08 UTC)
- Firefox 156 地址栏广告: query_raw_items(source='hackernews')[id:398555] = ▲21 💬6 - Firefox 156 ads in address bar (2026-09-15 14:15 UTC)
- Sunk Cost 本地 LLM 回本计算: query_raw_items(source='hackernews')[id:389205] = ▲36 💬57 - Sunk Cost local LLM rig payback (2026-09-15 01:37 UTC)
- Ordewell 编码 agent 任务编排: query_raw_items(source='hackernews')[id:398681] = ▲23 💬20 - Ordewell coding agent orchestration (2026-09-15 13:31 UTC)
- Have I Been Proxied IP 检查: query_raw_items(source='hackernews')[id:399392] = ▲20 💬10 - Check if IP in proxy network (2026-09-15 14:24 UTC)
- Capsule 单文件 Web 应用: query_raw_items(source='hackernews')[id:397505] = ▲24 💬8 - Capsule single-file web apps SQLite (2026-09-15 13:31 UTC)
- AI 不是普通技术: query_raw_items(source='hackernews')[id:376509] = ▲23 💬33 - AI is not a normal technology (2026-09-14 01:00 UTC)

## 正文抓取

- DeepMind 警告文章全文: fetch_url('https://www.theguardian.com/technology/2026/sep/14/google-deepmind-ai-warnings') = Guardian 长文，Alex Turner 辞职指控+Hugging Face 入侵事件
- AI surreal dialect 文章全文: fetch_url('https://www.theguardian.com/technology/2026/sep/15/syd-barrett-ai-chat-language-poetic-tech-bro-jargon-oversight') = Guardian 报道，Emergence 实验室研究
- Schneier 监控文章全文: fetch_url('https://www.lawfaremedia.org/article/25-years-of-mass-surveillance-is-enough') = Lawfare 联署文章
- Flock Camera 被入侵: fetch_url('https://www.wired.com/story/hackers-flock-camera-data-shows-how-system-works/') = WIRED/404 Media 联合调查
- Sunk Cost 工具: fetch_url('https://sunkcost.ai/') = 本地 LLM 回本计算器
- Ordewell GitHub: fetch_url('https://github.com/ordewell/ordewell') = 多 agent 任务编排框架
- Have I Been Proxied: fetch_url('https://haveibeenproxied.com/') = IP 代理网络检查工具
- Bottom 50% 数据: fetch_url('https://whats-left-over.pages.dev/') = BLS 数据家庭收支模拟器

## 跨期去重

- 与 2026-09-15 期 Top10 比对，以下条目已在昨日报道：Signal ZKP (376), Apple 配件图纸 (373), iOS 27 发布 (331), Siri 替换 (218), Irregular 安全丑闻 (90), 伊朗 SSL (81), Anthropic 盈利 (49), RubyGems 安全 (45), AI 材料/生物科学 (39), iOS 27 无法禁用 AI (43)

- Flock 摄像头黑客逆向（设备明文存储加密密钥）: query_raw_items(source='hackernews')[id:411426] = WIRED/404 Media 联合调查，黑客团体 stegan0gram 拆下 Flock 摄像头完整逆向，发现未加密分区存储加密密钥，21 天日志显示 50,200 辆车检测和 160 万张图像
- Flock 摄像头滥用搜索（LMAO）: query_raw_items(source='hackernews')[id:398307] = EFF 分析显示警察以"LMAO"为由跨 1558 城搜索 19,000 台摄像头，超过 6,300 次搜索使用"TBD"
- Wayback Machine 访问更新: query_raw_items(source='hackernews')[id:400329] = Internet Archive 确认遭受大规模自动化流量冲击，部署防护措施导致正常用户被误拦
- OpenAI 收购 Glass Imaging: query_raw_items(source='hackernews')[id:396336] = TechCrunch 报道 OpenAI 以 3 亿美元收购手机摄像头公司 Glass Imaging
- Apple Reference Image: query_raw_items(source='hackernews')[id:403798] = Apple 发布可验证摄影方案，基于安全硬件和 Private Cloud Compute，首发于 iPhone 18 Pro
- AI 代理破坏互联网: query_raw_items(source='hackernews')[id:399353] = 404 Media 记者收到 AI 代理"Kudzu"自动辩驳邮件，文章论述 AI 代理自主性已超出控制
- Baseten GitHub 被接管: query_raw_items(source='hackernews')[id:400330] = Strix 安全公司 25 分钟发现 Baseten 公开 Harbor 注册表中泄露的 GitHub PAT，获得管理员权限
- Jev 模型发布: query_raw_items(source='hackernews')[id:400453] = TypeSafe AI 发布 System One 系列模型，声称结构化推理成本降至 LLM 的 1/40-1/240
- Gemini 3.8 Live: query_raw_items(source='hackernews')[id:400364] = Google 发布 Gemini 3.8 Live 和 Extended Thinking，语音质量指数排名第一
- Swift 6.4 发布: query_raw_items(source='hackernews')[id:398682] = Swift 6.4 重点更新 WebAssembly 桥接 40 倍加速、Subprocess 1.0、C++20 span 桥接
- 全球债券收益率 2008 年新高: query_raw_items(source='hackernews')[id:398000] = Reuters 报道全球债券收益率升至 2008 年以来最高
- LLM 看空论: query_raw_items(source='hackernews')[id:400971] = Jay Kruer 从形式化验证视角论证 LLM 自主能力天花板，类比硬件工程规范-验证成本
- 石油供应危机数据: fetch_url(url='https://www.depletion.org') = 布伦特 $108.75（+43%）、美国柴油 $6.31 历史新高（+70%）、SPR 285.4M 为 1982 年以来最低
