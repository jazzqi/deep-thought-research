# Reference — HN 书摘 2026-11-25（覆盖 11-24 UTC 窗口）

## query_raw_items 引用条目

- Anthropic IPO 破发至 $83 发行价以下: query_raw_items(source='hackernews', published_after=2026-11-24T00:00:00Z, published_before=2026-11-25T00:00:00Z, keyword='Anthropic')[id:816836] = Bloomberg 报道 Anthropic 盘前跌破 $83 IPO 价，HN ▲235/💬495
- Anthropic 破发二次报道: query_raw_items(同上)[id:817214] = MSN 报道 Anthropic 跌破 IPO 价，▲90/💬85
- Anthropic 破发 Reuters: query_raw_items(同上)[id:817285] = Reuters 报道首日涨势反转，▲21/💬1
- LLM agent 为母公司工作: query_raw_items(source='hackernews', min_points=100, 11-24 窗口)[id:816708] = michaelharley.net 帖 ▲797/💬337
- Polymarket 黄仁勋内幕交易调查: query_raw_items(同上)[id:816461] = 4,648 美元→71,518 美元，89 分钟前，Gnosis Safe Proxy，▲456/💬263
- 华盛顿议员交易英伟达股票: query_raw_items(同上)[id:816674] = Trump 28 买 15 卖，37 议员 192 笔，▲275/💬158
- Tegmark 称 Anthropic 员工谈"接管世界": query_raw_items(同上)[id:817527] = Novara Media 报道，▲152/💬79
- Ask HN 被 Anthropic 指控蒸馏: query_raw_items(keyword='Anthropic')[id:817654] = ▲116/💬61，24h 自证清白
- Tidal 封禁 AI 生成音乐: query_raw_items(同上)[id:817318] = Variety 报道，▲148/💬105
- 2035 Came Early（unkernel 浏览器跑 Linux）: query_raw_items(同上)[id:815421] = fzakaria.com，▲915/💬347
- OpenAI 抢先证明 VP≠VNP: query_raw_items(keyword='Anthropic')[id:817611] = GitHub openai/math，▲74/💬72
- Anthropic VP≠VNP over Every Field: query_raw_items(keyword='Anthropic')[id:815250] = GitHub anthropics/formal-math，▲24/💬9
- Check Point 服务器攻击活动: query_raw_items(同上)[id:817387] = GreyNoise 报道，▲131/💬44
- Anthropic 官方 Working with AI: query_raw_items(keyword='Anthropic')[id:817875] = anthropic.com/research，▲35/💬29

## fetch_url 正文/评论溯源

- Anthropic 破发评论: fetch_url(news.ycombinator.com/item?id=50627836) = 作者 futureshock 高赞评论"AI 可变革、可盈利、Anthropic 可领先，但股票仍可能是糟糕的投资"
- LLM agent 正文: fetch_url(michaelharley.net/posts/2026/11/01/llm-agents-work-for-their-parent-companies-not-for-you/) = Claude Code 建 Bandcamp 歌曲识别技能，Bandcamp 加验证码后 Claude 拒绝绕过却愿从 YouTube 下载无版税歌曲
- LLM agent 评论: fetch_url(news.ycombinator.com/item?id=50627340) = 作者 Lerc 主张 LLM 应像法律/医疗顾问按客户最大利益行事；反对者指 LLM 输出概率性、技术尚无法可靠走边界
- Polymarket 正文: fetch_url(deucalionn.vercel.app/polymarket-delit-initie-jensen-huang-nvidia/) = 账户 ljhggk 于 11-23 UTC 01:19–02:28 以 6.5 美分买入 71,518 份 YES，投入 4,648 美元，特朗普发文前 89 分钟停止，四笔 Polygon 交易哈希可查
- 华盛顿议员正文: fetch_url(kadoa.com/congress/insights/trump-nvidia) = Trump 2026 年 28 笔买入 $5.1M–$16.7M、15 笔卖出 $4.4M–$12M；37 议员 192 笔；NVDA 10 月高点到 11/20 跌 48%，11/23 涨 33%
- Tegmark 评论: fetch_url(news.ycombinator.com/item?id=50631210) = 作者 georgemcbay 澄清 Tegmark 说的是"alignment without control"，即创造连创造者都无法控制的超级智能
- 蒸馏指控正文: fetch_url(news.ycombinator.com/item?id=50630809) = 公司称不训练模型，仅改设置时跑回归基准，被要求 24h 举证；高赞建议对抗性 Claude 审查、迁 AWS Bedrock
- Tidal 正文: fetch_url(variety.com/2026/music/news/tidal-bans-ai-generated-music-1236956924/) = 12/9 起移除纯 AI 曲目，43% 新歌 AI 生成、96% 零播放，每日拒收 8–8.5 万首；Spotify 年内移除 7500 万首
- unkernel 正文: fetch_url(fzakaria.com/2026/11/23/2035-came-early) = unkernel 把 Linux 编译到 WebAssembly，比 qemu-wasm 快 2–32 倍，支持网络/Wayland/ALSA，可嵌套 Firefox
- unkernel 评论: fetch_url(news.ycombinator.com/item?id=50624497) = 作者 gbl08ma 称用 Claude 做两个月的项目被 unkernel 抢先发布
- OpenAI VP≠VNP 正文: fetch_url(github.com/openai/math/tree/main/preprints/VP-and-VNP-are-different-November-23-2026) = 下界 exp(Ω((log n)^{5/4}))，附 Lean 形式化，不解决 P vs NP
- Check Point 正文: fetch_url(greynoise.io/blog/check-point-security-management-servers-intrusion-campaign) = GT13，99 IP，22 组织横跨 17 国，CVE-2026-16232，窃取 24 台服务器数据，疑用 LLM/agentic 系统
- Working with AI 正文: fetch_url(anthropic.com/research/working-with-ai) = 66 次访谈 58 家企业，价值来自增量产出而非降本，多数企业减少招聘/削减离岸外包，瓶颈从编码转向代码审查/战略决策
- Working with AI 评论: fetch_url(news.ycombinator.com/item?id=50634734) = 作者 flowerlad 质疑模型无护城河、10 年内本地硬件可跑前沿模型
- Bloomberg/Reuters/MSN 正文: fetch_url 均失败（403/401/仅页头），具体跌幅未核验，稿中已诚实标注

# Reference — hn-daily 2026-11-25

- Anthropic 盘前跌破 $83 IPO 发行价: query_raw_items(source=hackernews, keyword=Anthropic)[id:816836] = ▲235 💬495，Bloomberg 报道盘前跌破发行价
- Anthropic 跌破 IPO 价后续报道: query_raw_items(source=hackernews, keyword=Anthropic)[id:817214] = ▲90 💬85，MSN/Reuters 跟进破发
- Anthropic IPO 破发第三条: query_raw_items(source=hackernews, keyword=Anthropic)[id:817285] = ▲21 💬1，Reuters 报道迅速反转
- Tegmark 称 Anthropic 员工谈“接管世界”: query_raw_items(source=hackernews, keyword=Anthropic)[id:817527] = ▲152 💬79，Novara Media 报道，HN 评论澄清标题失真
- Ask HN 被 Anthropic 指控蒸馏: query_raw_items(source=hackernews, keyword=Anthropic)[id:817654] = ▲116 💬61，公司称仅做回归基准被要求24小时举证
- Anthropic 企业调研 Working with AI: query_raw_items(source=hackernews, keyword=Anthropic)[id:817875] = ▲35 💬29，58家企业66次访谈
- OpenAI 宣称先于 Anthropic 解决 VP≠VNP: query_raw_items(source=hackernews, keyword=VP VNP)[id:817611] = ▲74 💬72，GitHub preprint + Lean 形式化
- Anthropic formal-math VP≠VNP: query_raw_items(source=hackernews, keyword=VP VNP)[id:815250] = ▲24 💬9，VP≠VNP over Every Field [pdf]
- unkernel/trynix 性能与能力描述: fetch_url(https://fzakaria.com/2026/11/23/2035-came-early) = unkernel 将 Linux 编译到 WASM，比 qemu-wasm 快 2–32 倍，支持网络/Wayland/WebGL2/ALSA
- HN 窗口高分条目概览: query_raw_items(source=hackernews, min_points=20, limit=80) = 返回80条，用于核对当日高分池与口径差异
- 讨论日志与接力上下文: ReadThemeDocsTool(themes/hn-daily/_history/2026-11-25_0616__manual__hn_utc_hacker_news_5_1_2_4_6_2_3_1_2_top10_8_12_query_raw_it/roundtable/discussion_log.md) = 记录 tech_generalist/tech_scout/ai_specialist/kevin_kelly 初始观点
- 当前稿接力基线: ReadThemeDocsTool(themes/hn-daily/_history/2026-11-25_0616__manual__hn_utc_hacker_news_5_1_2_4_6_2_3_1_2_top10_8_12_query_raw_it/drafts/current.md) = Lead 初稿全文

- Anthropic 盘前跌破 $83 IPO 发行价: query_raw_items(source=hackernews, published_after=2026-11-24T00:00:00Z, published_before=2026-11-25T00:00:00Z, min_points=20)[id:816836] = ▲235 💬495，Bloomberg 报道盘前跌破发行价
- Anthropic 跌破 IPO 价二次报道: query_raw_items(...)[id:817214] = ▲90 💬85，MSN 报道跌破 IPO 价
- LLM agent 忠诚归属: query_raw_items(...)[id:816708] = ▲797 💬337，作者称 Claude 拒绝绕过 Bandcamp 验证码但愿从 YouTube 下载
- Polymarket 黄仁勋复职内幕交易调查: query_raw_items(...)[id:816461] = ▲456 💬263，链上取证称 4648 美元变 71518 美元
- 华盛顿 NVDA 持仓与交易: query_raw_items(...)[id:816674] = ▲275 💬158，Kadoa 统计特朗普 43 笔、37 名议员 192 笔
- Tidal 封禁 AI 生成音乐: query_raw_items(...)[id:817318] = ▲148 💬105，Variety 报道 43% 新歌被判定 AI、96% 零播放
- Tegmark/Anthropic 接管世界报道: query_raw_items(...)[id:817527] = ▲152 💬79，Novara Media 报道，HN 评论澄清为 alignment without control
- Anthropic 蒸馏指控 Ask HN: query_raw_items(...)[id:817654] = ▲116 💬61，公司称被要求 24 小时举证
- unkernel/Linux 编译进 WASM: query_raw_items(...)[id:815421] = ▲915 💬347，fzakaria 报道比 qemu-wasm 快 2-32 倍
- OpenAI VP≠VNP 证明: query_raw_items(...)[id:817611] = ▲74 💬72，GitHub 预印本含 Lean 形式化
- GreyNoise Check Point 入侵活动: query_raw_items(...)[id:817387] = ▲131 💬44，99 IP 攻陷 22 机构，推断 LLM 驱动
- Jevons Paradox in AI: query_raw_items(...)[id:816379] = ▲77 💬37，更便宜 token 未必覆盖 capex
- Ternary Bonsai 2.5 27B: query_raw_items(...)[id:817761] = ▲65 💬12，三值 27B 权重发布
- Anthropic Working with AI: query_raw_items(...)[id:817875] = ▲35 💬29（draft 引用；本轮 query_raw_items 未返回该 id，数字沿用稿内标注）
