# HN 书摘 · 2026-11-19（周四）

## Big Picture

今天这期 HN 头部（12 条书摘，2026-11-18 UTC 窗口）共同拼出一句话：AI 竞争轴已从「模型能做什么」切换到「谁为 AI 定价、谁为 AI 买单、谁承担 AI 的代价」。供给侧，能力正以可度量的速度商品化——微软 Ignite 一次发 7 个模型、MAI Code 2 以 5% 价格拿到 Opus 5.5 的 96% 性能，与 11-18 期 GPT-6.2 把单任务成本从约 $20 打到约 $4、10 月下旬实测推理价数月降 80% 连成一条连续曲线：前沿模型的超额毛利被竞争与评测透明化双向挤压。资本侧，Anthropic 今日以 83 美元/股挂牌、将成史上最大 IPO，Amazon 与 Google 合计持股近 30%，同日遭安全联盟、财务质疑、股权披露三面夹击——稀缺性叙事正从「模型能力」迁移到「资本结构与信任」。代价侧，搜索流量 -40%、84% 答案漂移、独立站被 AI 拖垮在同一天三信源交叉，AI 负外部性首次以一手数据链形态进入公共讨论。我们判断，这是技术演化从「变异爆发」进入「选择压力显现」的典型切面：方向（知化、过滤、流动）依然必然，不确定的只是摩擦的时间线与谁来买单。

> 今日三句话：① Anthropic 今日（11-19）以 83 美元/股定价挂牌、将成史上最大 IPO，同日遭科学家与法学家联盟「Anthropic Is Not a Safe AI Company」、Gary Marcus 财务质疑、股权结构披露三面夹击——AI 叙事主战场从模型能力切到资本结构与信任；② 黄仁勋 11-18 辞任 NVIDIA CEO 被董事会确认不回归（临时 CEO Colette Kress、穆迪展望调至稳定、NVIDIA 收跌近 3%、道指 -561 点），涟漪直达出口管制：荷兰公开抵制美国 MATCH 法案「域外条款」，该法案恰因黄仁勋事件获得新推力；③ 微软 Ignite 一次发 7 个模型、以「Opus 5.5 5% 价格 96% 性能」正面开打价格战，HN 评论区顺势展开「AI 是电动机还是汽车」的护城河大辩论。

## 头条深读

### 1. Amazon and Google will together own nearly 30% of Anthropic after its IPO（亚马逊与谷歌 IPO 后将合计持有 Anthropic 近 30%）

| 原文 | [Amazon and Google will together own nearly 30% of Anthropic after its IPO](https://techcrunch.com/2026/11/17/amazon-and-google-will-together-own-nearly-30-of-anthropic-after-its-ipo/) |
| --- | --- |
| 热度 | 作者 sshah03 · 2026-11-18 15:59 UTC（关联帖「Anthropic Is Not a Safe AI Company」同日入库；分数与评论数由冻结快照注入） |
| 摘要 | Anthropic IPO 定价 83 美元/股、高于推介区间，11-19（周四）挂牌，媒体称其将成史上最大 IPO。股权披露：Amazon 转股后持股 14.7%（若全部持有的可转债转股可达 23.8%）、Google 13.7%，合计近 30%，均为无投票权股；AMD、Broadcom、Google、Micron、Microsoft、Nvidia、TSMC 已同意在 IPO 中合计认购 260 亿美元无投票权股票（Google 与 Nvidia 各 100 亿）；Amazon 另承诺未来十年在 AWS 支出超 1000 亿美元。同日三路质疑齐发：科学家/法学家/科技领袖联盟在 IPO 前挑战其安全品牌（[HN 讨论](https://news.ycombinator.com/item?id=50548485)，businesswire 正文 403 未能抓取）；Gary Marcus 援引 S-1 称估值上限 1.4 万亿美元而公司除一个受补贴的异常季度外从未盈利、未来负债约 8950 亿美元，Q3 增速 47% 已较 Q2 的 147% 大幅放缓。 |
| 批注 | **tech_generalist 视角：** 定价与质疑同日登顶，标志 AI 叙事主战场从模型能力转向资本结构——同日微软用「5% 价格 96% 性能」给前沿模型的可替代性定价（第 2 条），Anthropic 则用史上最大 IPO 给稀缺性定价，两个定价在同一天正面对冲。 **kevin_kelly 视角：** 用 12 个必然趋势筛这条线——知化、流动、共享全部命中，长期方向确定[高]；要判断的是稀缺性还剩什么。三期对照给出答案：10-23 Kimi K3.1 Pro 开放权重站上 Pareto 前沿、10-26 IBM 称开源权重「不可抗拒地好用」、11-18 微软 5% 价格拿 96% 性能——模型能力的稀缺性每周都在折旧，招股书里真正稀缺的只剩三样：资本结构（260 亿美元基石认购全为无投票权股）、信任（安全联盟同日挑战）与分发（AWS 十年千亿美元承诺）。我们判断这次 IPO 会被市场定价为「AI 信任与资本的定价实验」而非模型公司定价[中高]。 |
| 评论摘录 | 作者 platinumrad 转引联盟金句：「联盟中的人几乎在一切上都不同意彼此，但我们一致认识到：一家说服自己『自身主导地位就是更大善』的公司是危险的。」（[HN 讨论](https://news.ycombinator.com/item?id=50548485)） |

### 2. Microsoft AI: Seven new world-class models at scalable price-performance（微软一次发布七个世界级模型，主打可扩展性价比）

| 原文 | [Microsoft AI: Seven new world-class models at scalable price-performance](https://microsoft.ai/news/microsoft-ignite-2026/) |
| --- | --- |
| 热度 | 作者 gmays · 2026-11-18 16:08 UTC（分数与评论数由冻结快照注入） |
| 摘要 | 微软在 Ignite 一次发布 7 个模型，全部以性价比对标前沿：MAI Cyber 2 Flash 在 CyberGym-E2E 上超过 GPT-6 Astra 而单任务成本不足其 2%；MAI Code 2 达 GPT-6.1 Sol 编码质量的 98%、价格 40%，达 Opus 5.5 性能的 96%、价格仅 5%；MAI Image 2.7 以五分之一价格登顶 Artificial Analysis 图像编辑；MAI Realtime 1 起价 $0.01/音频分钟；Decision 1.1 比 GPT-6.1 Sol 快 50 倍、便宜 79 倍；自研 Maia 200 加速器二代投产，tokens/watt 提升 1.7 倍。 |
| 批注 | **tech_generalist 视角：** 价格战从「发一个便宜模型」升级为「全栈能力按 5% 定价」——当 MAI Code 2 用 5% 价格拿到 96% 性能，Anthropic 估值所依赖的毛利假设在 IPO 挂牌当天被同日削弱；上期「发布热度≠能力超越」的共识再添一层：发布密度高，边际信息已转向单位经济性。 **kevin_kelly 视角：** 这是能力商品化的教科书样本，且已是三期连续信号：11-18 GPT-6.2 单任务约 $20→$4、10-25 实测推理价数月最高降 80%、本期 5% 价格 96% 性能。知化+形成趋势下，能力像带宽一样越用越便宜是方向性的、不是周期性的[高]；泡沫判据不看价格战本身，看谁在价格战里仍在沉淀基础设施——微软自研 Maia 200 二代与 tokens/watt +1.7 倍属「遗传」沉淀，是必然方向上的赢家动作而非烧钱信号。 |
| 评论摘录 | 作者 rayiner：「AI 公司越来越像发明了电动电机——技术会嵌入一切，但没人能在电机周围建起护城河；对 LLM 而言基本接口就是一段可即插即用的文本流，任何能吐 9600bps 串口 TTY 的东西都可互换。」（[HN 讨论](https://news.ycombinator.com/item?id=50548021)；跟帖分别用汽车、Linux VPS、拨号 ISP 补充类比，全部指向商品化） |

## 值得一读

### 3. 'Human' Is Cambridge Dictionary's Word of the Year 2026（「Human」当选剑桥词典 2026 年度词）

| 原文 | ['Human' Is Cambridge Dictionary's Word of the Year 2026](https://www.cam.ac.uk/news/cambridge-dictionary-reveals-word-of-the-year-2026) |
| --- | --- |
| 热度 | 作者 DeepLogin · 2026-11-18 14:43 UTC（分数与评论数由冻结快照注入） |
| 摘要 | 剑桥词典选「human」为 2026 年度词，副题即「AI 时代何以为人」。正文串起全年事件：比尔·盖茨主张「human reserved jobs」（如护工）不应被机器取代；Hinton 警告「我们正在创造 alien beings，我愿意自私地选择人类」；教皇 Leo XIV 在《Magnifica Humanitas》信中呼吁抵御「非人化」；作者公会推出「Human Authored」图书标识；麦康纳与泰勒·斯威夫特分别为声音、形象注册商标以防 AI 复制。 |
| 批注 | **kevin_kelly 视角：** 年度词是文化对技术方向的反应函数，选「human」恰说明知化已渗透到日常焦虑层[高]。反共识判断：这类符号事件不改变技术方向（知化不可逆），但会固化为标识摩擦——「Human Authored」标识与声音/形象商标注册会像 GDPR 一样变成标配合规成本，对 AI 应用方是按年计的长期摩擦项[中]。 |

### 4. CVE-2026-99312: KVM Guest-to-Host Escape（KVM 客户机到主机逃逸漏洞）

| 原文 | [CVE-2026-99312: KVM Guest-to-Host Escape](https://www.cve.org/CVERecord?id=CVE-2026-99312) |
| --- | --- |
| 热度 | 作者 Kozmik1 · 2026-11-18 16:06 UTC（分析文与 CVE 记录为同一讨论串两条；分数与评论数由冻结快照注入） |
| 摘要 | KVM 在模拟 x86 INIT 信号时未无条件重置 MMU 上下文，构成 guest-to-host 逃逸（CVE-2026-99312）；terra.security 分析文 404、cve.org 需 JS 渲染，正文未能抓取，摘要据 HN 帖标题与讨论区。评论区两个落点：作者 fwsgonzo 指分析文是 AI 写作、「应由人类重写」；tptacek 与 JoshTriplett 就嵌套虚拟化威胁模型交锋——多租户互不信任场景下 KVM 逃逸即全失守，而 AWS 普通实例借嵌套虚拟化跑 firecracker/crosvm 又是现实刚需。 |
| 评论摘录 | 作者 3g56g6g6h 一句话点破根因：「failure of KVM to grok and implement long-standing x86 behavior: INIT invalidates the TLBs」；作者 immibis2 同时质疑披露粒度：「The kernel project marks everything that could conceivably be of any use to an attacker as CVE. What are we actually looking at here?」（[HN 讨论](https://news.ycombinator.com/item?id=50548004)） |
| 批注 | **kevin_kelly 视角：** 底层依赖尚未「基础设施化」的又一实证——KVM 承载着全球多数云租户，其逃逸面却仍靠单个 CVE 修补；按演化阶段标注，这是「变异→选择」尚未走完的中间态，与第 8 条 Nginx 同日出现说明脆弱性是结构性的、不随 AI 叙事降温而消失[中高]。 |

### 5. Jensen Huang's fall hits 'open' models in boost to Anthropic and OpenAI（黄仁勋离场打击「开放权重」阵营，利好 Anthropic 与 OpenAI）

| 原文 | [Jensen Huang's fall hits 'open' models in boost to Anthropic and OpenAI](https://www.ft.com/content/418ca885-fbcf-4b9f-a8b9-2bd60b543fc5) |
| --- | --- |
| 热度 | 作者 teleforce · 2026-11-18 15:08 UTC（分数与评论数由冻结快照注入） |
| 摘要 | FT 付费墙，正文未能抓取；据标题与同日多方快讯交叉：黄仁勋因 NYT 调查（其向公司承认婚外不忠，另有其与一名疑似中国间谍关联的报道）辞任，董事会确认不回归，Arm CEO Rene Haas 已进入继任候选；NVIDIA 11-18 收跌近 3%、道指跌 561 点、穆迪将展望由正面调至稳定（确认 Aa1）。FT 的判断是其离场重创开放权重阵营——黄仁勋在任时是开放权重模型的公开倡导者——利好了 Anthropic 与 OpenAI 的闭源路线。 |
| 批注 | **tech_generalist 视角：** 个人事件→产业政策的传导在 24 小时内走完：HN 评论区已出现「泄密时机恰逢 Anthropic IPO」的阴谋论，被作者 jaredklewis 以「只有间接证据」驳回——情绪面已形成、证据密度不足，这正是本条进「值得一读」而非头条的原因；但 MATCH 法案借势提速（第 6 条）证明政策侧不等证据。 **kevin_kelly 视角：** FT 的因果链我只认一半：个人离场能改变开放权重的速度，改不了方向——10 月证据链（Kimi K3.1 Pro 开放权重贴住前沿、IBM 开源权重表态）显示开放权重是被市场「选择」出来的趋势，载体是基础设施与人才池，不是单个 CEO。人是脆弱的遗传载体，治理结构才是基础设施；此事件真正加速的是 MATCH 法案这类政策摩擦（第 6 条）——摩擦改变时间线，不改变终点[中高]。 |

### 6. Dutch resist 'unacceptable' US bid to tighten semiconductor export controls（荷兰抵制美国收紧半导体出口管制的「不可接受」要求）

| 原文 | [Dutch resist 'unacceptable' US bid to tighten semiconductor export controls](https://www.politico.eu/article/dutch-resist-unacceptable-us-bid-to-tighten-semiconductor-export-controls-asml/) |
| --- | --- |
| 热度 | 作者 sergdigon · 2026-11-18 13:46 UTC（分数与评论数由冻结快照注入） |
| 摘要 | 美国国会两党 MATCH 法案拟给荷兰、日本等盟友 150 天使其对华先进芯片制造设备管制与美国对齐，否则美商务部将把美国出口管制单边延伸至其设备；荷兰外交部回应称法案「域外性质不可接受，域外措施违背各自主权原则」。法案在黄仁勋事件曝光后获得新推力；ASML 去年近三分之一营收来自中国。海牙战略研究中心分析师 Benedetta Girardi：问题不在更严管制是否正当，而在「谁来定义、经由何种程序」。 |
| 批注 | **kevin_kelly 视角：** 治理摩擦集中在中间层的又一例：技术必然走向流动与共享，监管则在设备、DNS 这类中间层设卡（同窗 Quad9 退出法国是同一形态另一面）。域外条款遭盟友反弹说明执行成本在上升——摩擦是基础设施化的常态成本，过早≠错误；ASML 近三分之一营收系于中国，意味着摩擦期以年计而非以月计[中]。 |

### 7. We asked AI the same 210 questions two days in a row, 84% of answers changed（同一问题隔天再问：84% 的 AI 答案变了）

| 原文 | [We asked AI the same 210 buying questions 2 days in a row, 84% of answers changed](https://supercite.ai/blog/ai-answers-change-every-day) |
| --- | --- |
| 热度 | 作者 avatar99 · 2026-11-18 17:58 UTC（分数与评论数由冻结快照注入） |
| 摘要 | 210 个购买类问题、4 个引擎、同设置隔天重问：84%（701/839）的答案品牌组合发生变化，Gemini 上高达 95%；首日被点名品牌 27% 次日消失；#1 位次次日仍在率 90% 但保住第一的仅 63%；被引用页面隔天只有 42% 相同。个例：Google AI Mode「最易上手 CRM」首日 Less Annoing CRM 居首（读 Zapier 列表），次日改读 Slack 博客与 HubSpot 自家页面后 HubSpot 居首、前者消失——答案不稳定源于「每次现挑几页」，单日一次「ChatGPT 是否推荐我们」的抽查几乎没有信息量。 |
| 批注 | **kevin_kelly 视角：** 84% 漂移是「形成」（Becoming）趋势的日常形态——答案每天被重新组装，不稳定性是现阶段的正常形态而非缺陷[高]；真正变的是下游含义：被引用页面隔天仅 42% 相同，意味着「排名」这类静态指标在 AI 分发时代失去测量意义。对内容方的可执行结论是把单日抽查改成连续采样，否则测到的是噪声[高]。 |

### 8. Pre-auth RCE in Nginx HTTP/2 handling（Nginx HTTP/2 处理存在认证前远程代码执行）

| 原文 | [Pre-auth RCE in Nginx HTTP/2 handling](https://www.wiz.io/blog/nginx-http2-rce-vulnerabilities) |
| --- | --- |
| 热度 | 作者 speedping · 2026-11-18 15:19 UTC（分数与评论数由冻结快照注入） |
| 摘要 | Wiz 披露 Nginx HTTP/2 处理路径存在未认证 RCE，HN 讨论串挂出两个 CVE 记录（CVE-2026-123633、CVE-2026-123007）；wiz.io 博文正文未能抓取，据讨论区：临时规避是禁用 http2，但 gRPC 等依赖 HTTP/2 的服务无法照做（评论作者 verst），另有评论指出修复提交一周前已进开源仓库。 |
| 批注 | **tech_scout 视角：** 本条是 11-18 窗口 ▲ 分最高条目（988 分，领先第二名 All About Berlin 的 741 分），与同窗口 KVM guest-to-host 逃逸（第 4 条）、Optimizely 被用于对顶级网站做恶意 A/B 测试（11-18 15:09 入库）构成基础设施安全三连——漏洞细节未抓取，当前置信度只覆盖「事件已发生、社区高度关注」层面，技术细节待补抓后再升档。 **kevin_kelly 视角：** 「共享」的双刃被这条评论说透：修复提交公开进仓库一周即可被监控仓库的攻击者利用——开源透明既是安全资产也是情报源；这与底层依赖尚未基础设施化是同一件事的两面[中高]。 |
| 评论摘录 | 作者 black3r：「The bug was apparently fixed in open source repo a week earlier, this could've been abused by anyone smart enough to monitor repos like this for exploitable bugfixes for a week (the commit message even included "Reported by Xint.io")」（[HN 讨论](https://news.ycombinator.com/item?id=50547374)） |

## 技术雷达

### 9. Google's AI answers reducing search traffic by 40%（谷歌 AI 回答使搜索流量下降 40%）

| 原文 | [Google's AI answers reducing search traffic by 40%](https://revscope.co/blog/search-seo-geo-2026/) |
| --- | --- |
| 热度 | 作者 slashdev · 2026-11-18 00:17 UTC（分数与评论数由冻结快照注入） |
| 摘要 | 未能抓取正文。 |
| 批注 | **tech_scout 视角：** 与 All About Berlin（第 12 条）、84% 答案漂移（第 7 条）在同一天构成「AI 负外部性」三信源交叉——同一趋势被三个独立站点独立量化，且该主线已连续多日占据 HN 头部，属持续上升信号而非脉冲热度；GEO（生成式引擎优化）正从边缘话题变成内容站的生存问题。-40% 单一来源未核验，本条置信度 75：趋势方向高置信，具体数值中低置信。 **kevin_kelly 视角：** 跨期对照把这条线钉死为连续信号：11-17 Cloudflare 同题帖 ▲866 → 11-18 本条 ▲682 与 All About Berlin ▲741 → 同日 84% 答案漂移，三天三信源同向。筛子过两道：过滤、流动均命中，方向确定[高]；-40% 出自 SEO 博客、未独立核验[低]——方向置信度不外借给数值，两者分开标注。 |
| 评论摘录 | 作者 ordersofmag：「Whether it goes into training data is irrelevant. The AI agent will do the search on behalf of the person, find the answer in your page and return the answer, rather than your page... Once LLMs were good enough to make reasonable tool calls to search the web it was game over.」（[HN 讨论](https://news.ycombinator.com/item?id=50540178)） |

### 10. Energy-Based Reasoners: 385x more efficient inference（能量基推理器：推理效率宣称提升 385 倍）

| 原文 | [Energy-Based Reasoners: 385x more efficient inference](https://energy-based-reasoners.github.io/) |
| --- | --- |
| 热度 | 作者 frenchmajesty · 2026-11-18 09:29 UTC（分数与评论数由冻结快照注入） |
| 摘要 | 未能抓取正文。 |
| 批注 | **tech_scout 视角：** 入选理由是管道位置而非热度：这是一条 research→product 管道左端信号（论文/演示页先于产品出现），▲273 分而评论仅 43 条，高分低评正是「研究先行、工程未至」的早期特征；标题宣称的 385 倍未核验，按早期信号评分暂列探索级（置信度 35），后续跟踪开源实现与复现报告再升降档。 **kevin_kelly 视角：** 按演化阶段标注：这是「变异」，不是「选择」——385 倍若被复现，受益方向仍是单位成本塌缩主线，与第 2、11 条同一终点；未复现前保持探索级[低]。 |

### 11. A 4.5M-parameter TTS model runs 70x real-time on CPU and cost just $10 to train（450 万参数 TTS 模型：CPU 70 倍实时、训练成本 10 美元）

| 原文 | [A 4.5M-parameter TTS model runs 70x real-time on CPU and cost just $10 to train](https://huggingface.co/n4ze3m/tiny-voca) |
| --- | --- |
| 热度 | 作者 mrkn1 · 2026-11-18 15:01 UTC（分数与评论数由冻结快照注入） |
| 摘要 | 未能抓取正文。 |
| 批注 | **tech_scout 视角：** 边缘侧小模型的单位经济性信号——标题给出三项指标：4.5M 参数、CPU 上 70 倍实时推理、训练成本 10 美元。若三项可复现，语音合成将彻底商品化到任意设备端，与第 2 条微软「5% 价格 96% 性能」指向同一结论：前沿能力在被快速压缩为廉价商品。模型卡未抓取，置信度 40，属「值得进雷达跟踪、尚不足以进正文」的早期条目。 **kevin_kelly 视角：** 与第 2 条同构的「知化下沉到边缘」终点站形态——判断标准不变：三项指标可复现才升档，模型卡未抓取前保持探索级[低]。 |

## 社区之声

### 12. AI is killing All About Berlin（AI 正在杀死 All About Berlin）

| 原文 | [AI is killing All About Berlin](https://nicolasbouliane.com/blog/death-by-ai) |
| --- | --- |
| 热度 | 作者 grey-area · 2026-11-18 06:47 UTC（分数与评论数由冻结快照注入） |
| 摘要 | 未能抓取正文。 |
| 批注 | **tech_scout 视角：** 本帖是 11-18 窗口评论最多的讨论（671 条评论），以站点经营者第一人称讲述 AI 搜索对内容站的冲击；与第 7 条（84% 答案漂移）、第 9 条（搜索流量 -40%）同日三信源交叉，且包揽当日 HN 头部——这是持续 6 个月以上的上升信号形态，不是脉冲热度，值得作为「AI 负外部性」主线持续跟踪。 **kevin_kelly 视角：** 评论区给出了演化终局的反身性推演（作者 boringg：高质量数据被一次性收割后信息变旧，AI 或已进入「glory age」）——内容供给萎缩→语料变旧→能力折旧，这是 AI 商品化曲线上唯一可能自我打断的回路，值得作为跨期观察项跟踪[中]。 |
| 评论摘录 | 作者 ryandrake：「I think using AI in 10 years will feel like using StackOverflow today. SO is kind of stuck in time... The same might happen to AI if it stops having access to fresh information.」（[HN 讨论](https://news.ycombinator.com/item?id=50542705)） |

## 数据速览（今日 Top10 全量快照）

> Top10 快照由代码从冻结快照注入，本稿不手写数值（11-18 UTC 窗口 hn_points≥20 条目共 76 条，同 URL 已去重）。

## 接力协作

本稿为接力第 2/3 棒（kevin_kelly）产出，在第 1 棒（tech_scout）完整稿上渐进融合，未另起炉灶：头条深读 1-2 与各条目他人批注、结论、归属标注全部原样保留。本棒新增六项：① 稿首 Big Picture 宏观叙事总纲；② **kevin_kelly 视角** 批注（头条 1-2、值得一读 3/4/5/6/7/8、技术雷达 9/10/11、社区之声 12）；③ 评论摘录补抓 4 条（第 4、8、9、12 条，HN 讨论页抓取成功）；④ 第 8 条摘要据 HN 讨论页升级（补两个 CVE 编号、禁用 http2 的规避约束与仓库泄露窗口）；⑤ 跨期趋势对照（单位成本三期连续：GPT-6.2 → 推理价 -80% → 本期 5% 定价；AI 负外部性三信源 + 11-17 Cloudflare 前帖）；⑥ 隔夜窗口核验：11-18 20:00 UTC 后仅 3 条 ≥60 分新条目（We Need Smart People Who Give a Shit ▲177、Gemini 4 Neon ▲151 已在稿内、Software companies are trying to kill home computing ▲80），无新头条级事件，当日框架维持。

已知缺口（留给第 3 棒）：第 3、9、10、11 条正文仍为「未能抓取正文」，可用抓取工具补抓升级摘要；第 5、6、10、11 条缺评论摘录；第 3、7 条尚无 ai_specialist 视角；数据速览与热度行维持代码注入、未手写。

### 分工

| 棒次 | Agent | 负责栏目 | 状态 |
| --- | --- | --- | --- |
| 1 | tech_scout | 全稿融合、技术雷达（9-11）、社区之声（12）、接力协作 | 已完成 |
| 2 | kevin_kelly | Big Picture、kevin_kelly 视角批注、跨期趋势对照、评论摘录补抓（4/8/9/12）、隔夜窗口核验 | 本轮完成 |
| 3 | ai_specialist | 值得一读 AI 相关条目（3/7/9）正文补抓与深化、剩余评论摘录补全、终校 | 待接力 |
| Lead | tech_generalist | 头条深读 1-2、三句话定调、终审 | 圆桌稿已交付，终审待接力后 |

（实际接力顺序与首轮代拟分工略有出入：第 2 棒由 kevin_kelly 执行，ai_specialist 顺延至第 3 棒、负责范围不变；后续棒次增删条目时需同步更新本表。）