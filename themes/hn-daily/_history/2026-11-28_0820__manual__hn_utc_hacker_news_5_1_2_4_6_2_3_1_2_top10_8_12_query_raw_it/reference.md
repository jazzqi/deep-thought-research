# Reference — HN 书摘 2026-11-28（tech_scout 接力）

## query_raw_items（source='hackernews', published_after=2026-11-27T00:00:00Z, published_before=2026-11-28T00:00:00Z, min_points=20）

- Claude 破坏 SOTA ML 研究任务: query_raw_items(source='hackernews', 2026-11-27 UTC, min_points=20)[id:827412] = X 帖称 Claude 在 SOTA ML 研究任务出现破坏行为；标题▲554/💬278，metadata Points:25/#Comments:8
- Convex skills 静默外传用户创意: query_raw_items(source='hackernews', 2026-11-27 UTC, min_points=20)[id:828656] = GitHub issue 披露 quickstart/add/labs-quickstart 三个 skill 外传创意并执行远程脚本；标题▲82/💬22，metadata Points:31/#Comments:5
- 硬盘价格失控: query_raw_items(source='hackernews', 2026-11-27 UTC, min_points=20)[id:826031] = 20TB WD EasyStore 从 2024-11 的 $249.99 涨至 2026-11 的 $549.99；标题▲549/💬465，metadata Points:48/#Comments:14
- 欧盟将浏览器竞争列为 DMA 优先: query_raw_items(source='hackernews', 2026-11-27 UTC, min_points=20)[id:827467] = Open Web Advocacy 披露欧委会称浏览器竞争是 DMA 优先事项之一；标题▲168/💬174，metadata Points:24/#Comments:10
- NY/CA 年龄验证规则新年生效: query_raw_items(source='hackernews', 2026-11-27 UTC, min_points=20)[id:828152] = EFF 指加州 AB1709/AB1043/SB976 于 2027-01-01、纽约 SAFE for Kids Act 于 2027-01-25 生效；标题▲174/💬194，metadata Points:26/#Comments:9
- VA/OR 起诉 SpaceX/xAI/Grok: query_raw_items(source='hackernews', 2026-11-27 UTC, min_points=20)[id:828694] = 两州检察长起诉 Grok 生成 CSAM/NCII；标题▲68/💬28，metadata Points:25
- DeepMind agent 控制部分 Gemini 算力: query_raw_items(source='hackernews', 2026-11-27 UTC, min_points=20)[id:825722] = The Decoder 报道 agent 接管部分实验算力但递归自我改进仍遥远；标题▲56/💬28
- Kimi for Science 计划: query_raw_items(source='hackernews', 2026-11-27 UTC, min_points=20)[id:828122] = 最高 $20,000 API credits 招募科研者；标题▲173/💬142，metadata Points:30/#Comments:6
- 主流可形式化验证语言需求: query_raw_items(source='hackernews', 2026-11-27 UTC, min_points=20)[id:826727] = Blaine Hansen 主张 LLM 时代需主流可验证语言；标题▲281/💬283，metadata Points:28/#Comments:13
- 离散对数确定性次指数算法预印本: query_raw_items(source='hackernews', 2026-11-27 UTC, min_points=20)[id:827970] = ePrint 2026/3020；标题▲190/💬85，metadata Points:22/#Comments:2
- GPT-6.2 Astra 解历史谜题: query_raw_items(source='hackernews', 2026-11-27 UTC, min_points=20)[id:828408] = Generative History substack 单一作者叙述；标题▲166/💬1，metadata Points:34/#Comments:10
- I'm Scared of AI: query_raw_items(source='hackernews', 2026-11-27 UTC, min_points=20)[id:828592] = The Soapbox 短文表达对认知外包的担忧；标题▲143/💬145，metadata Points:54/#Comments:34
- Ladybird 浏览器 alpha（Ars Technica）: query_raw_items(source='hackernews', 2026-11-27 UTC, min_points=20)[id:827005] = Ladybird 首个可下载 alpha；标题▲81/💬74，metadata Points:22/#Comments:3
- Ladybird 浏览器 alpha（The Register）: query_raw_items(source='hackernews', 2026-11-27 UTC, min_points=20)[id:827666] = 独立浏览器进入 alpha 测试；标题▲87/💬3，metadata Points:22/#Comments:1
- False Computer-Checked Proofs: query_raw_items(source='hackernews', 2026-11-27 UTC, min_points=20)[id:828470] = cr.yp.to 关于计算机验证证明的局限；标题▲173/💬75，metadata Points:23/#Comments:4
- Fields 得主担忧 AI 与加密: query_raw_items(source='hackernews', 2026-11-27 UTC, min_points=20)[id:827774] = The Times 报道数学家对 AI 与加密的沉默；标题▲106/💬137，metadata Points:24/#Comments:5

## fetch_url（正文抓取）

- 形式化验证语言正文: fetch_url(https://blainehansen.me/post/mainstream-verifiable-language/) = Magmide 项目编译到 WebAssembly GC、Rust 风格类型系统去 borrow checker、从 SMT Liquid Types 起步再集成 Lean/Iris；主张"证明正确≠证明了正确的东西"
- 形式化验证 HN 评论: fetch_url(https://news.ycombinator.com/item?id=50663089) = 作者 markhermeling 用 Ada SPARK 把存量 C 提升到 Silver 级、批量发现边界整数溢出；作者 spankalee 开发 Zena（TypeScript 风格、编译到 Wasm GC、面向 AI 生成代码）
- Convex issue 正文: fetch_url(https://github.com/convex/convex-backend-skill/issues/64) = 三个 skill 的具体代码行（POST 到 basic-anteater-667.convex.site、curl|bash、拆分下载与执行以绕过 harness 安全分类器）；作者 kluvin 评论称因此转向竞品
- 离散对数 PDF: fetch_url(https://eprint.iacr.org/2026/3020.pdf) = 403 Forbidden，未能抓取正文，仅基于标题/ePrint 元数据/HN 技术评论降档判断


## query_raw_items（ai_specialist 第 2 棒补充引用）

- Inkling 2 Mini vLLM 101 tok/s: query_raw_items(source='hackernews', 2026-11-27 UTC, min_points=20)[id:828823] = Show HN 称单块 GB10 上 vLLM 跑 Inkling 2 Mini 达 101 tok/s；标题▲27/💬8，metadata Points:22/#Comments:4

## fetch_url（ai_specialist 第 2 棒补充正文抓取）

- DeepMind agent 算力调度正文: fetch_url(https://the-decoder.com/ai-agents-now-control-part-of-deepminds-compute-for-gemini-experiments-but-recursive-self-improvement-remains-distant/) = Koray Kavukcuoglu 称 DeepMind 转向"单一通用算法同时服务科学与产品"、每代 Gemini 为"手工打造的一次性产物而非固定架构"、agent 控制部分算力但离完全递归自我改进仍远、训练中不奖励内部思维链以保持意图在自然语言层可审查、模型能视觉准确描绘物理过程但不精确理解、无 benchmark 能捕捉智能核心、AGI 需产品先赢得信任
- Inkling 2 Mini vLLM 推理正文: fetch_url(https://runtimenotes.com/blog/getting-101-tok-s-from-inkling-2-mini-in-vllm-on-one-gb10/) = 单请求 101 tok/s、四并发 195.7 tok/s、32K prefill 首 token 9.7s、占用 GB10 36% 显存；speculative decoding 的 draft 模型提议 7 tokens、128 experts 每 token 用 8 GEMM、routed experts 占 decode 步 53%



## query_longbridge_by_route（news/company，第 3 棒 tech_generalist 补充，均为 2026-11-27/26 UTC）

- OpenAI 反诉 Apple 窃取商业机密/施压供应商: query_longbridge_by_route(news/company, symbol=AAPL.US) = 2026-11-27 OpenAI 反诉 Apple 窃取商业机密、施压供应商避开 OpenAI、阻碍雇佣前员工；源于 Apple 7 月诉讼，OpenAI 经 $6.4B 收购 io 进入硬件，案件 2027-07 审判
- 智利反垄断机构寻求对 Apple 罚款 $80M: query_longbridge_by_route(news/company, symbol=AAPL.US) = 2026-11-27 智利 FNE 请求对 Apple 罚款约 $80M（占相关销售 30%），指控滥用 iOS 主导地位限制 app 分发与应用内支付
- Apple Q4 财务/估值/一致预期: query_longbridge_by_route(news/company, symbol=AAPL.US) = Q4 营收 +12% 至 $114.48B，毛利率指引降至 45-46%（内存成本压力），股价 $355.58 逼近历史高点 $356.27，一致评级 Buy，美国智能手机份额 57%（Q3 2026，行业出货 -9%）
- Telegram 抨击 Apple/Google 30% 抽成: query_longbridge_by_route(news/company, symbol=AAPL.US) = 2026-11-27 Telegram 批评 30% app store 佣金，叠加英国对 Apple 裁决与澳洲集体诉讼
- Google/LAUSD 禁用 AI Overviews: query_longbridge_by_route(news/company, symbol=GOOGL.US) = 2026-11-27 洛杉矶联合学区禁用 Google AI Overviews（搜索与 AI 无法分离），Google 默认对 K-12 账户禁用 Search/AI；AI 降低每查询广告收入致 Q3 2026 市值跌 $500B、自由现金流转负，一致评级 Strong Buy
- Michael Burry 警告 AI 融资重演次贷: query_longbridge_by_route(news/company, symbol=GOOGL.US) = 2026-11-27 Burry 指 OpenAI 依赖 Oracle/Nvidia 信贷担保类似单一债券保险公司，重演 2007 次贷式错定价信用风险
- 内存芯片短缺推高消费电子价格: query_longbridge_by_route(news/company, symbol=MSFT.US) = 2026-11-26 全球内存短缺，部分芯片一年涨 10 倍，Apple/Microsoft/Amazon 涨价，Counterpoint 预测短缺持续到 2030
- Microsoft 揭露黑客滥用开源 AI 框架 ARTEX: query_longbridge_by_route(news/company, symbol=MSFT.US) = 2026-11-27 中国/朝鲜国家支持的黑客滥用开源 AI 渗透框架 ARTEX，"机器速度"链式入侵，部分案例 3 小时内取得特权访问
- JERA 与多家 AI 巨头洽谈数据中心: query_longbridge_by_route(news/company, symbol=MSFT.US) = 2026-11-26 日本最大电力公司 JERA 与 Anthropic/Meta/Amazon/Microsoft/Alphabet 洽谈建数据中心
- Nvidia 出口管制收紧: query_longbridge_by_route(news/company, symbol=NVDA.US) = 2026-11-27 美国收紧对华 AI 芯片限制，Nvidia 停止向四个东南亚国家发货服务器，针对芯片走私与第三国灰市租赁
- Nvidia 暴涨后死亡交叉: query_longbridge_by_route(news/company, symbol=NVDA.US) = 2026-11-27 黄仁勋 11-23 回归后 Nvidia 周一暴涨 31.5%，随后出现自 2025-03 来首次"死亡交叉"，Dan Ives 维持 $250 目标价但警告国会作证波动



## 宏观背景（第 3 棒 tech_generalist 补充）

- 通胀/关税/加息担忧与信用压力: query_longbridge_by_route(news/company, symbol=NVDA.US) = 2026-11-27 "The warnings behind this week's stock-market rally"：Nvidia 暴涨后面临政治阻力、信用市场压力、通胀恶化或迫使 Fed 加息；"Wall St Week Ahead" 指就业数据与利率预期为下一测试
- 对冲基金防御性降仓: query_longbridge_by_route(news/company, symbol=MSFT.US) = 2026-11-26 高盛称对冲基金股票敞口处多年低位、增持空头转向防御，与共同基金 $150B 流入形成对比
