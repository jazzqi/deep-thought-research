# HN 书摘 2026-10-15 参考来源

- AdFection 零点击间谍软件报告（Citizen Lab，40亿竞拍记录/近20万站点/Al Jazeera 中招）: query_raw_items(source=hackernews, min_points=20, published_after=2026-10-15)[id:484092] = Citizen Lab 报告：Discover-Tech/Controlium 将定向广告变为零点击雇佣间谍软件投递管道
- AdFection 正文细节（Controlium 平台、DARK CARTOGRAPHER、Google/IAB 切断接入）: fetch_url(https://citizenlab.ca/research/how-discover-tech-turned-targeted-ads-into-a-pipeline-for-spyware/) = 报告全文
- AdFection HN 评论（作者 munk-a 广告取缔论）: fetch_url(https://news.ycombinator.com/item?id=50101813) = HN 评论页
- Goodfire"神经网络本来就干净"长文（InceptionV1 末层99-100%可解释、Qwen3-32B ~90%单主业、300×规模可读）: query_raw_items(source=hackernews, min_points=20, published_after=2026-10-15)[id:484505] = Nick Cammarata 长文：超级叠加假说被判定为误读
- Goodfire 正文与 HN 评论（作者 bluejay2387 质疑）: fetch_url(https://already-clean.goodfire.com/) + fetch_url(https://news.ycombinator.com/item?id=50105647) = 正文+评论页
- 数学界哀悼 OpenAI 数学成果（Duminil-Copin/Strogatz 语录）: query_raw_items(source=hackernews, min_points=20, published_after=2026-10-15)[id:484074] = Derek Thompson 长文；正文 fetch_url(https://www.derekthompson.org/p/i-know-why-the-mathematicians-weep)
- Simons/Anthropic/OpenAI 1500万美元数学界AI过渡计划: query_raw_items(source=hackernews, min_points=20, published_after=2026-10-15)[id:484298] = Simons Foundation 新闻稿；正文 fetch_url(simonsfoundation.org 对应页)
- Meta Muse Spark Open（816B总参/42B激活/1M上下文/双M5 Ultra Mac Studio 本地运行/Helion 内核1.03-3.95×）: query_raw_items(source=hackernews, min_points=20, published_after=2026-10-15)[id:484588] = Meta AI Research 开源公告；正文 fetch_url(https://research.meta.ai/blog/muse-spark-open)
- Steam vs Epic vibe-coded 启动器速度（0.5s/5s vs 2s/10-15s，正文403，据HN评论转述）: query_raw_items(source=hackernews, min_points=20, published_after=2026-10-15)[id:484393] = respawnfirst 报道；正文 fetch_url 失败(403)，评论页 fetch_url(https://news.ycombinator.com/item?id=50105635)
- ChatGPT 广告按手机号/邮箱/prompt 话题定向（10亿MAU，2026年2月美国上线）: query_raw_items(source=hackernews, min_points=20, published_after=2026-10-15)[id:484294] = 404 Media 实测；正文 fetch_url(https://www.404media.co/how-chatgpt-targets-ads-to-you-based-on-your-prompts-phone-number-and-email/)
- Withings 新账号 Apple Health 同步需 $99.99/年（2026-10-13 起，196赞/148评论）: query_raw_items(source=hackernews, min_points=20, published_after=2026-10-15)[id:484871] = Withings 论坛帖；正文 fetch_url(support.withings.com 对应帖)
- HTTP 响应头 prompt 注入扫描（217,097,223 响应/7,959 站发AI头/30站注入/139站标记AI bot/Claude 7/9 遵从测试）: query_raw_items(source=hackernews, min_points=20, published_after=2026-10-15)[id:484296] = Signals Corps 扫描报告；正文 fetch_url(https://www.signalscorps.com/blog/prompt-injection-in-http-headers/)
- AI 逆向硬件驱动（Plustek8200i SANE 驱动数小时复活/MIPI相机补丁/hw-harness）: query_raw_items(source=hackernews, min_points=20, published_after=2026-10-15)[id:484295] = GNOME 博客 Christian Schaller；正文 fetch_url(https://blogs.gnome.org/uraeus/2026/10/15/aiandreverseengineerhardware/)
- 微软 MAI-Base-2（2.8T总参/80B激活 MoE/FLOPs效率4-12× DeepSeek-V4-Pro-Base）: query_raw_items(source=hackernews, min_points=20, published_after=2026-10-15)[id:484745] = microsoft.ai Lab Notes；正文 fetch_url(https://microsoft.ai/news/frontier-pre-training-at-microsoft-ai/)
- Siri 用户体验退化吐槽（115分/102评论，LLM中间层归因）: query_raw_items(source=hackernews, min_points=20, published_after=2026-10-15)[id:484297] = Reddit r/apple 帖；评论页 fetch_url(https://news.ycombinator.com/item?id=50104465)
- 牛津物理硕士自述 AI 掏空作业文化: query_raw_items(source=hackernews, min_points=20, published_after=2026-10-15)[id:483180] = Substack 文章；正文 fetch_url(https://thetheorygirlie.substack.com/p/ai-was-great-until-it-was-not)
- 待补：Krea 3（正文两次抓取失败 ConnectError，交第2位接力）: query_raw_items(source=hackernews, min_points=20, published_after=2026-10-15)[id:484506] = Krea 3 图像模型发布

- Krea 3 公测（原生局部编辑/像素级精确编辑/内部评测替代 NBP 与 GPT Image/速度帕累托/LoRA 与开放权重"正在考虑"；krea.ai 官方页两次 ConnectError）: query_raw_items(source=hackernews, keyword='Krea', published_after=2026-10-14)[id:484506] = Krea 3 frontier image model 4× faster than Nano Banana Pro；一手内容 fetch_url(https://news.ycombinator.com/item?id=50105648)（作者 dvrp Hello HN 帖+78 条评论问答）
- Anthropic 独立评估方更新（METR 6 人"类员工访问"/无否决权发布/三级准入框架/SecureBio、Accenture、Faculty、Hugging Face/白宫超级智能协议）: query_raw_items(source=hackernews, keyword='Anthropic evaluator', published_after=2026-10-14)[id:484719] = anthropic.com 公告；正文 fetch_url(https://www.anthropic.com/news/an-update-on-independent-evaluators) + 评论页 fetch_url(https://news.ycombinator.com/item?id=50107114)（stratos123 质疑"employee-like"措辞、lukaswthoms"新模型发布前治理公示"解读）


## tech_scout 审查核验来源（2026-10-16）

- 2026-10-15 HN 全量窗口覆盖核验（60 条）: query_raw_items(source=hackernews, published_after=2026-10-15T00:00:00Z, published_before=2026-10-16T12:00:00Z, limit=60) = 已覆盖 15 条入选帖分数可对上（Citizen Lab ▲308/459 [id:484092]、Guardian ▲491 [id:483860]、Goodfire ▲444/163 [id:484505]、Krea 3 ▲226 [id:484506]、Reuters ▲51 [id:484529]）；未覆盖高分帖见下 6 行
- 未覆盖#1 DEsk（Wayland 拟物桌面，▲423/173，当日第 3 高分）: query_raw_items(source=hackernews, published_after=2026-10-15)[id:484121] = github.com/fyzugx/DEsk
- 未覆盖#2 Libreboot 26.10（▲227/128，UEFI+Chromebook 支持）: query_raw_items(source=hackernews, published_after=2026-10-15)[id:483857] = libreboot.org
- 未覆盖#3 Show HN: Flipflop（iroh 持久隧道文件传输，▲93/49）: query_raw_items(source=hackernews, published_after=2026-10-15)[id:482490] = github.com/andunieee/flipflop
- 未覆盖#4 C++26 Contracts（▲110/106）: query_raw_items(source=hackernews, published_after=2026-10-15)[id:484072] = cppstories.com
- 未覆盖#5 Jev Meets the Trolley Problem（Jev 生态应用帖，▲65/21）: query_raw_items(source=hackernews, published_after=2026-10-15)[id:484658] = zachlandes.com/trolley-problem
- 未覆盖#6 Anthropic Scion 抄袭 Mononoke 争议续（▲72/12）: query_raw_items(source=hackernews, published_after=2026-10-15)[id:484602] = sunshowers.io/posts/anthropic-mononoke-2
- 星期核验: 2026-10-15 为周四（index.md 往期标注"2026-10-15（周四）"），草稿标题写"周三"有误
- 外部交叉核验（非 HN 口径，仅备注）: query_raw_items(source=telegram:Financial_Express, published_after=2026-10-14)[id:485203] = 小米开源 MiDashengLM-Spatial 空间音频理解大模型；[id:485188] = 快手可灵 4.0 全量上线（4K/10bit HDR/30s）

（备注：上一条同内容追加因 session 目录名笔误写入了嵌套错误路径 _history/…/_history/…mn_utc…/reference.md，以本条为准，请 Lead publish 时忽略/清理该误写文件。）