# Reference — 2026-10-12 UTC HN 书摘

- QGIS QEP428 全面禁止 AI 辅助贡献（维护者审查压力理由/贡献者自述/86赞24踩）: query_raw_items(source='hackernews')[id:472002] + fetch_url(https://github.com/qgis/QGIS-Enhancement-Proposals/pull/387) = PR 线程全文
- QGIS HN 讨论页（361分/391评论；评论 mootothemax 地理空间 LLM 失效细节）: fetch_url(https://news.ycombinator.com/item?id=50054751) = 评论页正文
- 欧洲超市冷柜网络攻击（多源）: query_raw_items(source='hackernews')[id:472155][id:472669][id:472604][id:472911][id:472712][id:472572] = Tom's Hardware/BBC/Yahoo/RNZ/Reuters/France24 报道
- 冷柜攻击细节（Danfoss 软件、约400/15000 法国门店、50°C×6h、阿尔萨斯损失€270k、检方立案）: fetch_url(https://www.bbc.com/news/articles/crq5nzxv9q4yo) = BBC 正文
- Rich Hickey《'AI' Is Not a Tool》全文（wield vs abdicating/自动化非工具论证）: query_raw_items(source='hackernews')[id:472940][id:473050] + fetch_url(https://gist.github.com/svieira/619d60dea942a8d4498cba3bb6b11c02) = gist 全文
- Zod 4.6.6 投毒机制（preinstall 钩子、eth_call C2 合约 0xe236…e523、base64 payload 动态执行）: query_raw_items(source='hackernews')[id:471671] + fetch_url(https://github.com/colinhacks/zod/commit/d821685ea6732436fcdf786a81d076958471e467) = 恶意 diff 全文
- Fable Took My Job 全文（岗位经济学替代判断/Shopify 机器编码重写/Opus 5.5 复刻 bug）: query_raw_items(source='hackernews')[id:471675] + fetch_url(https://cendyne.dev/posts/2026-10-11-fable-took-my-jorb.html) = 正文
- Meta Muse Wonder（Active Memory/Active Focus/Harvey LAB/FocusBench/SWE-Marathon/吉瓦级 Prometheus 数据中心）: query_raw_items(source='hackernews')[id:472713] + fetch_url(https://research.meta.ai/blog/muse-wonder) = 正文
- GLM-Legal（仅元数据；正文抓取两次失败）: query_raw_items(source='hackernews')[id:472607] = 标题"GLM-Legal: Advancing Agentic Legal Intelligence"；fetch_url(https://z.ai/blog/glm-legal) = no extractable text ×2
- AI 公司入侵事件与刑法意图要件框架（Anthropic 3 系统/OpenAI 澳政府健康网站+Hugging Face/Google 3 家）: query_raw_items(source='hackernews')[id:472454] + fetch_url(https://mortoray.com/why-arent-ai-companies-being-charged-for-hacking/) = 正文
- 现代 Web 应用 C+CGI（BCHS 栈/3 依赖/零停机发版/marketyour.games）: query_raw_items(source='hackernews')[id:472671] + fetch_url(https://prophitt.me/writing/a-modern-web-app-in-c) = 正文
- w1700k-sdr（MT7996 14-bit IQ 320Msps/10GbE 零拷贝/262144 点 FFT 100 帧/s/自研固件）: query_raw_items(source='hackernews')[id:472668] + fetch_url(https://github.com/h0m3us3r/w1700k-sdr) = README
- Postgres 存储瓶颈基准（33 亿行、gp3 3000 IOPS vs 本地 NVMe、m6id.4xlarge 16vCPU/64GiB）: query_raw_items(source='hackernews')[id:471663] + fetch_url(https://clickhouse.com/blog/posette-talk-recap-postgres-isnt-slow-your-storage-is) = 正文
- Codex CLI 0.157.0 默认自更新 daemon（374MB 包复制/每小时自更新/强杀活跃 turn/代理环境变量继承）: query_raw_items(source='hackernews')[id:472853] + fetch_url(https://github.com/openai/codex/issues/48195) = issue 正文
- vibe-coded Photoshop 克隆（165 开发者/日数百 PR/两周>$5万 token/8K 画布笔刷崩溃）: query_raw_items(source='hackernews')[id:471662] + fetch_url(https://www.shokunin.studio/blog/2026/10/9/attack-of-the-vibe-coded-photoshop-clones) = 正文
- Agent37 (YC F26) 沙箱均价 $0.37/月: query_raw_items(source='hackernews')[id:472757] = Launch HN 元数据摘要
- Opus 5.5 8 prompts/3 小时生成 Figma 克隆: query_raw_items(source='hackernews')[id:472822] = Show HN 元数据摘要
- Ars Technica"更多代码≠更多软件"（正文抓取 405 失败，仅元数据）: query_raw_items(source='hackernews')[id:472759] = 元数据；fetch_url(arstechnica URL) = HTTP 405
- HN 评论页抓取失败记录（后续棒次重试）: fetch_url(50060269/50057551/50053216) = ConnectError

- Anthropic 自我复制研究主帖: query_raw_items(keyword='self-replicating', source='hackernews') [id:472941] = HN 主帖（news.ycombinator.com/item?id=50061603），快照时 45 分/42 评
- 欧洲超市冷柜遭袭主帖: query_raw_items(keyword='defrosting OR Danfoss OR fridges') [id:472155] = tom's hardware 主帖 ▲154/💬306（id:50055304）；同日 BBC [id:472669]、Reuters [id:472712] 交叉证实
- Zod 4.6.6 投毒: query_raw_items(keyword='Zod compromised', source='hackernews') [id:471671] = ▲173/💬50（id:50052814）
- QGIS 禁止 AI 贡献: query_raw_items(keyword='QGIS', source='hackernews') [id:472002] = ▲335/💬364（id:50054751）
- GLM-Legal: query_raw_items(keyword='GLM-Legal', source='hackernews') [id:472607] = ▲381/💬218（id:50058507）
- Vibe-coded Photoshop 克隆: query_raw_items(keyword='Photoshop clones', source='hackernews') [id:471662] = ▲124/💬179（id:50052156）
- Fable Took My Job: query_raw_items(keyword='Fable Took My Job', source='hackernews') [id:471675] = ▲214/💬329（id:50053216）
- Doory 开源 Canva: query_raw_items(keyword='Doory', source='hackernews') [id:471629] = ▲187/💬68（id:50049872）
- Meta 发布 Muse Wonder 前沿模型: query_raw_items(keyword='OpenAI OR Anthropic OR Nvidia', published_after='2026-10-05') [id:472697][id:472681] = Financial Express 快讯，称基准超 Claude Opus 5.5/Fable 5.1/GPT-6 Astra，主攻企业市场
- 微软数吉瓦级 Maia 300 部署: query_raw_items(keyword='OpenAI OR Anthropic OR Nvidia', published_after='2026-10-05') [id:472318] = Financial Express 快讯，Maia 300 明年起部署，专为 AI 推理设计
- 英伟达-思科 USFP 光模块开放规范: query_raw_items(keyword='OpenAI OR Anthropic OR Nvidia', published_after='2026-10-05') [id:472464][id:472468] = OCP 峰会快讯
- AMD Helion Agentic AI 机架: query_raw_items(keyword='OpenAI OR Anthropic OR Nvidia', published_after='2026-10-05') [id:472252] = Bloomberg via Financial Express
- IREN 与 Anthropic 多年期云协议: query_raw_items(keyword='OpenAI OR Anthropic OR Nvidia', published_after='2026-10-05') [id:472280] = IREN 股价 +2.1%
- 美股 10-12 开盘: query_raw_items(keyword='OpenAI OR Anthropic OR Nvidia', published_after='2026-10-05') [id:472272] = 道指 +0.17%/标普 +0.04%/纳指 -0.05%；Meta +2.54%、NVDA -0.38%
- Agent37（YC F26 低价 agent 沙箱）: query_raw_items(keyword='Yandex bot', source='hackernews') [id:472757] = Launch HN ▲26/💬13（id:50059096）
- Airtable 大裁员: query_raw_items(keyword='Yandex bot', source='hackernews') [id:473025] = ▲31/💬7（id:50062076）
- Epic Games 要求员工用 AI 完成迪士尼游戏: query_raw_items(keyword='Yandex bot', source='hackernews') [id:473003] = ▲28/💬3（id:50062237）
- OpenAI Codex CLI 默认安装自更新常驻守护进程: query_raw_items(keyword='OpenAI OR Anthropic OR Nvidia', published_after='2026-10-05') [id:472853] = GitHub issue ▲76/💬29（id:50060694）
- NVDA/MSFT 行情: market_quote(['NVDA.US','MSFT.US']) = 失败（OpenApi 401003 token expired），本轮行情/估值数据缺失，市场锚改用当日 Financial Express 快讯
- NVDA 公司新闻: query_longbridge_by_route('news/company', symbol=NVDA.US) = 失败（OpenApi 401003 token expired）


## tech_scout 交叉审查独立核验（2026-10-13，D82 独立通道）

- 独立漏项审查基线（10-11~10-13 hackernews 全量 79 条）: query_raw_items(source='hackernews', published_after='2026-10-11', published_before='2026-10-13', limit=80) = 当日 HN 全清单，用于比对稿件 12 条覆盖度
- mortoray《Why aren't AI companies being charged for hacking?》: query_raw_items(source='hackernews')[id:472454] = ▲301/💬318（当日 AI 治理最高热度帖，reference 已收录但稿件未写入）
- Rich Hickey《'AI' Is Not a Tool》: query_raw_items(source='hackernews')[id:473050] = LinkedIn 镜像 ▲114/💬51；[id:472940] = gist ▲79/💬35（reference 已收录全文但稿件未写入）
- Anthropic IPO 争议: query_raw_items(source='hackernews')[id:471654] = CNBC"Unprecedented Test of Investor Gullibility"▲230/💬197（稿件与 reference 均未覆盖）
- Linux 手机替代 duopoly: query_raw_items(source='hackernews')[id:471649] = ▲245/💬295（未覆盖）
- GitHub Actions/PR/Issues 故障: query_raw_items(source='hackernews')[id:472419] = githubstatus incident ▲150/💬136（未覆盖）
- Postgres 存储瓶颈基准: query_raw_items(source='hackernews')[id:471663] = ▲161/💬175（reference 已收录，稿件未写入）
- Codex CLI 自更新 daemon: query_raw_items(source='hackernews')[id:472853] = ▲76/💬29（稿件仅内联一句、无独立条目与链接）
- Local Indexing 降 token: query_raw_items(source='hackernews')[id:471624] = ▲114/💬44（未覆盖）
- OpenFatigue: query_raw_items(source='hackernews')[id:472891] = ▲70/💬12（技术雷达未覆盖）
- HashiCorp 归档 Boundary: query_raw_items(source='hackernews')[id:471623] = ▲83/💬15（未覆盖）
- Micah Lee《Just say no to OpenAI and Anthropic》: query_raw_items(source='hackernews')[id:472823] = ▲91/💬48（未覆盖）
- 微软总裁"AI 监管少于牛奶": query_raw_items(source='hackernews')[id:472555] = ▲65/💬73（未覆盖）
- Yandex 袭击事实核验（稿件"三大主要数据中心"表述）: query_raw_items(keyword='Yandex OR Danfoss', published_after='2026-10-05')[id:471600] = BBC"third attack on Russian tech giant"（第三次袭击，非三大数据中心）；[id:467909] = FE 梁赞州萨索沃市单一数据中心遭无人机袭击起火
- Yandex 袭击时间线: query_raw_items(keyword='Yandex OR Danfoss')[id:467778] = FE 10-08 梁赞数据中心运营全面停止；[id:470977] = 泽连斯基称袭击后在线机器人减少
- 冷链主帖当前快照（核对稿件 371分/596评）: query_raw_items(keyword='Danfoss OR defrosting')[id:472155] = ▲154/💬306（id:50055304），稿件 371/596 无 reference 抓取记录支撑
- 微软 Maia 300 时间点: query_raw_items(keyword='Maia OR USFP', published_after='2026-10-05')[id:472207] = FE"Maia 300 将于 2027 年开始量产部署"（佐证稿件"明年起"表述）；[id:472756] = HN Azure Maia 300 架构深潜帖 ▲22（稿件未引用该 HN 帖）
- Meta Muse Wonder 发布确认: query_raw_items(keyword='Muse Wonder')[id:472661][id:472663] = FE 扎克伯格官宣"规模更大、能力更先进的模型系列"
- USFP 光模块规格: query_raw_items(keyword='USFP')[id:472474] = FE 每通道 400Gb/s、单模块最高 12.8Tb/s、带宽密度 4 倍
- IREN-Anthropic 云协议: query_raw_items(keyword='IREN')[id:472280] = FE IREN 股价 +2.1%
- Show HN Opus 5.5 Figma 克隆: query_raw_items(source='hackernews')[id:472822] = ▲26/💬23（"克隆潮做不出引擎"论点的反例素材，稿件未纳入）
