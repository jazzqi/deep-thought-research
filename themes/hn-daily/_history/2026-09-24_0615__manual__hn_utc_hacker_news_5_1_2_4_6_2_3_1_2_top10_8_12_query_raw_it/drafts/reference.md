# Reference — 2026-09-24 HN 书摘

## 头条深读
- GPT-6 Sol/Luna 发布（▲1665 · 💬799）: query_raw_items(source=hackernews, min_points=100, published_after=2026-09-22T00:00:00Z) = OpenAI 发布 GPT-6 系列旗舰模型，含 Sol（快速推理）和 Luna（深度思考）双变体，Luna 定价为 GPT-5.6 Luna 的一半
- GPT-6 Astra 破译 Enigma（▲715 · 💬428）: query_raw_items(source=hackernews, min_points=100, published_after=2026-09-22T00:00:00Z) = Astra 自主破解 2005 年以来未解的二战恩尼格玛密电 MVUEH
- 缓存读取成本差异 8-10 倍: query_raw_items(source=hackernews)[id:49805509] 作者 sieve 评论 — MiMo 2.6 花费 $0.019 vs GPT-5.6 Luna $0.072

## 值得一读
- Apple Intelligence 强制启用（▲852 · 💬690）: query_raw_items(source=hackernews, min_points=100, published_after=2026-09-22T00:00:00Z) = macOS 升级后 Apple Intelligence 被强制启用，关闭开关被移除
- Pentagon Palantir AI 误杀（▲832 · 💬446）: query_raw_items(source=hackernews, min_points=100, published_after=2026-09-22T00:00:00Z) = 五角大楼承认 Palantir AI 过度依赖致 123 名伊朗儿童死亡
- AI 无智慧（▲383 · 💬537）: query_raw_items(source=hackernews, min_points=100, published_after=2026-09-22T00:00:00Z) = NYT 深度反思文章质疑 AI 是否能产生智慧
- OpenAI 训练员工被解雇（▲76 · 💬55）: query_raw_items(source=hackernews, min_points=20, published_after=2026-09-22T00:00:00Z) = 404 Media 报道 OpenAI 承包商用 AI 辅助训练被解雇
- Grammarly 异常消息（▲332 · 💬93）: query_raw_items(source=hackernews, min_points=20, published_after=2026-09-23T00:00:00Z) = Reddit r/sysadmin 热帖，取消订阅后向所有用户发异常消息
- SAML 设计缺陷（▲314 · 💬163）: query_raw_items(source=hackernews, min_points=100, published_after=2026-09-22T00:00:00Z) = Trail of Bits 安全审计揭露 SAML 协议在每个抽象层级的缺陷

## 技术雷达
- Drop (droprun.sh)（▲184 💬61）: query_raw_items(source=hackernews, id:435461) = 无 root 权限 Linux 沙箱，集成 gVisor
- Nari Qwen3-TTS/ASR（▲90 💬31）: query_raw_items(source=hackernews) = Nari Labs 语音模型，Coval 基准领先
- Jev in 25 Lines（▲458 💬139）: query_raw_items(source=hackernews, id:437668) = 25 行 Python 实现 Jev 决策模型
- JetBrains Air（▲72 💬111）: query_raw_items(source=hackernews) = IDE 厂商发布 agentic 开发产品线
- Unreal Agent（▲224 💬118）: query_raw_items(source=hackernews) = Unreal Engine AI Agent 集成项目
- Skillsync（▲65 💬57）: query_raw_items(source=hackernews) = AI agent 会话可移植方案
- Nathan Lambert 国会证词（▲117 💬52）: query_raw_items(source=hackernews, id:436520) = 中美开放模型竞争分析
- Meta Muse 0-day（▲121 💬49）: query_raw_items(source=hackernews, id:435578) = AI 助手权限管理安全漏洞
- Google CC 家庭扩展（▲50 💬63）: query_raw_items(source=hackernews, id:436613) = AI agent 进入家庭场景

## 社区之声
- Waymo transit rewards（▲234 💬289）: query_raw_items(source=hackernews, id:436989) = Waymo 与公共交通联运奖励计划
- 测试覆盖率虚荣指标: query_raw_items(source=hackernews) = 2085 个测试无一覆盖核心功能

## 数据速览
- CPI 同比 3.4% (2026-08): query_indicators(category=macro, country=us) = akshare
- 核心 CPI 337.765 (2026-08): query_indicators(category=macro, country=us) = openbb
- PPI 287.928 (2026-08): query_indicators(category=macro, country=us) = openbb
- 联储资产负债表 6,746,548M (2026-09-16): query_indicators(category=macro, country=us) = openbb
- 消费者信心指数 55.2 (2026-07, ⚠️过时): query_indicators(category=macro, country=us) = openbb
- 首次申请失业金 19.6万 (2026-09-12): query_calendar_events(importance=high, country=US) actual=19.6, forecast=20.7
- 9月FOMC (9/15-16) 完成: query_fomc(lookback_days=60) — 含 SEP，声明已发布
- 9/24 失业金数据（预期 20.0万）: query_calendar_events(importance=high, country=US)
- 9/30 ADP 就业（预期 5.8万）+ GDP 终值（预期 1.5%）: query_calendar_events(importance=high, country=US)
