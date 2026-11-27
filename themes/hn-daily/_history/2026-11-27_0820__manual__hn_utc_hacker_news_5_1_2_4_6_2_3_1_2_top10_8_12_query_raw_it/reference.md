# Reference — HN 书摘 2026-11-27（0820 轮，tech_scout 接力补充）

## tech_scout 接力补充（2026-11-27 00:23 UTC，信号校准与开发者生态）

- 裸机 Qwen（▲225/💬55，Points:21/1评论）: query_raw_items(source='hackernews', published_after=2026-11-26)[id:822073] = 24KB 纯汇编 x86-64 内核跑 Qwen3-0.6B，无 Linux/C/Rust/libc，QEMU KVM 134.9 tok/s
- 裸机 Qwen 正文: fetch_url(github.com/alesha-pro/llm.asm/tree/main/02-baremetal-os) = 24,252 bytes stripped kernel，74–94ms 冷启动，134.9 tok/s（EPYC 7642/16 vCPU）、55.4 tok/s（Xeon E5-2670 v3/12 核 Proxmox），token-exact 对齐 Phase 1
- 裸机 Qwen HN 评论: fetch_url(news.ycombinator.com/item?id=50648365) = 作者 sandworm101"无底层 OS 大幅缩小攻击面、可预测性更高"；作者 george_max"前沿模型下 OS 层开销可忽略"
- AI 重燃自托管（▲94/💬55，Points:34/21评论）: query_raw_items(source='hackernews', published_after=2026-11-26)[id:825273] = AI agent 降低 Docker Compose/NixOS/bootc 自托管配置摩擦
- AI 自托管正文: fetch_url(janlukas.blog/posts/ai-self-hosting) = NixOS 配置"半天 vs 无 AI 至少一周"，Renovate + GitHub Actions 自动化，bootc 镜像
- AMD llama.cpp HN 评论: fetch_url(news.ycombinator.com/item?id=50657265) = 作者 rao-v 指出 gfx906（32GB VRAM/1TB/s HBM2/约$200）优化生态，27B Q8 从 ~250pp/25tg→600pp/40tg；作者 boomskats 称 TheRock 重拾 gfx906 支持
- Tracking Diseases Cured by AI（▲299/💬177，Points:28/6评论）: query_raw_items(source='hackernews', published_after=2026-11-26)[id:825029] = 网站追踪"AI 治愈疾病"清单，当前 0 项过三期
- Diseases HN 评论: fetch_url(news.ycombinator.com/item?id=50657307) = 作者 theptip 用 ClinicalTrials.gov 检验"AI 加速新药"假设，未见 GPT 时代（约 2020）趋势断点，新药入组 2014–2022 翻倍后趋平；作者 jollymonATX 指一期到三期需 6–10 年



## ai_specialist 接力深化（2026-11-27 00:33 UTC，开源 vs 闭源动力学 / 能力地图分维度）

- Moat: Your OpenRouter Replacement（▲238/💬133，Points:26/16评论）: query_raw_items(source='hackernews', published_after=2026-11-26T00:00:00Z, published_before=2026-11-27T00:00:00Z)[id:823792] = 会员制模型批发商，自称"the costco of ai"
- Moat 正文: fetch_url(commandcode.ai/moat) = $5/月会员无 5小时/周/月限额、批发价；GLM-5.3 Flash 输入 $0.045/输出 $0.15 每百万 token（省70%）、DeepSeek V4.1 Flash $0.06/$0.24（省60%）、inclusionAI Ling 3.1 Flash $0.12/$0.36（省60%）、Moonshot Kimi K3 $1.80/$9.00（省40%）
- Moat HN 评论: fetch_url(news.ycombinator.com/item?id=50652184) = 作者 jedjonesuk 质疑"where these requests are being served? Is it them hosting? Is it the Chinese labs?"，称对数据治理严肃的机构是 non starter；作者 esskay 称"farming out to the cheapest provider, so yes China in many cases"；作者 gpfuchter 指 OpenRouter 会披露 provider 并允许按地区/隐私政策过滤
- Z.ai 澄清 GLM-5.5 未延迟（▲23/💬2，Points:22/2评论）: query_raw_items(source='hackernews', published_after=2026-11-26T00:00:00Z)[id:825359] = Z.ai 澄清 GLM-5.5 未延迟，计划 12 月发布
- GLM-5.5 HN 评论: fetch_url(news.ycombinator.com/item?id=50657724) = 作者 dgellow 猜测"China is around ~6 months behind?"（判断是 fable 5 而非 5.2）；作者 Sphax 抱怨 max coding plan 太贵
- DeepSeekMath（▲30/💬8，Points:20/5评论）: query_raw_items(source='hackernews', published_after=2026-11-26T00:00:00Z)[id:825101] = DeepSeekMath: Pushing the Limits of Mathematical Reasoning
- DeepSeekMath 正文: fetch_url(github.com/deepseek-ai/deepseek-math) = 以 DeepSeek-Coder-v1.5 7B 初始化，在数学相关 token 上继续预训练 500B token；7B 在竞赛级 MATH 基准达 51.7%（不依赖外部工具/投票），超越 Minerva 540B、接近 Gemini-Ultra 与 GPT-4；提出 GRPO（Group Relative Policy Optimization）；对比基线为 GPT-4/Gemini-Ultra 一代



## tech_generalist 最终收口（2026-11-27 00:37 UTC，平台竞争格局 / 监管地缘）

- NVIDIA CoWoS 份额下滑: query_longbridge_by_route(news/company, NVDA.US, 2026-11-27) = TSMC CoWoS 先进封装份额 2026 年 53.4% → 2027 年 45.6%（-8pct），需求仍增 57%，增量被云厂商自研 ASIC 分流（Anthropic 经 Broadcom 用 Google TPU、AWS/Meta 推进自研）
- 远程访问封锁与 GPU 抛售: query_longbridge_by_route(news/company, NVDA.US, 2026-11-26/27) = 11-19 生效远程访问禁令，数千张 B300 抛售，NVIDIA 要求 neocloud 排除中国租户、暂停对东南亚四国出货
- Huang 复职与股票/信用分歧: query_longbridge_by_route(news/company, NVDA.US, 2026-11-25) = Huang 复职 CEO 后股价反弹，但五年期 CDS 仍创纪录、S&P 列入负面观察
- 五巨头行情复核: market_quote(NVDA/GOOGL/MSFT/META/AMD.US, 2026-11-26 收盘) = NVDA 149.30(-3.91%)、GOOGL 273.10(-2.13%)、MSFT 489.93(-1.25%)、META 609.89(+3.40%)、AMD 406.03(-1.75%)
- Alphabet 监管/竞争摩擦: query_longbridge_by_route(news/company, GOOGL.US, 2026-11-26) = 马来西亚 MCMC 起诉 Google $146M（YouTube 有害内容）；Gemini 在 40.5% 假日购物提示提及 Amazon 但从不链接（Semrush）



## tech_scout 交叉审查独立核验（2026-11-27 00:39 UTC）

- NVDA FY2027 Q3 营收/EPS: fundamental/consensus(NVDA.US) = 营收 1158.44 亿（超预期 6.56%）、EPS 2.70（超预期 0.24）✓ 与稿件一致
- NVDA PE: fundamental/valuation/pe(NVDA.US) = current 28.55 / low 28.55 / high 44.68 / median 33.92 ✓ 与稿件一致
- 五巨头行情: market_quote(NVDA/GOOGL/MSFT/META/AMD.US, 11-26 收盘) = NVDA 149.30(-3.91%)、GOOGL 273.10(-2.13%)、MSFT 489.93(-1.25%)、META 609.89(+3.40%)、AMD 406.03(-1.75%) ✓ 与稿件一致
- S&P 董事会渗透帖真实元数据: query_raw_items(source='hackernews', keyword='compromised')[id:822237] = @narmiouh, 2026-11-25 23:03:16 UTC, ▲32/💬6（稿件热度行误标为 chirau / 11-26 06:43，该作者与时间实为 id:824416「Nvidia halts chip shipments to south-East Asia」）
- 遗漏的高价值 AI infra 帖: query_raw_items(source='hackernews', published_after=2026-11-26)[id:824855] = 45°C inlets just killed the chiller（▲238/💬121，数据中心冷却范式转变，当日第 12 高分帖）
- 遗漏的芯片架构帖: query_raw_items(source='hackernews', published_after=2026-11-26)[id:823249] = Qualcomm's Oryon 3 Reaches the Top（▲73/💬36，chipsandcheese）
- 遗漏的 agent 信任/马甲帖: query_raw_items(source='hackernews', published_after=2026-11-26)[id:824260] = Claude tries to sabotage research work（▲28/💬7）；[id:825476] = Novita/StreamLake are ByteDance Ark wrappers（▲20/💬3）
- CoWoS/远程禁令/AMD 转售/监管核验: query_longbridge_by_route(news/company, NVDA.US/GOOGL.US/AMD.US) = 稿件覆盖完整，无重大近期事件遗漏
