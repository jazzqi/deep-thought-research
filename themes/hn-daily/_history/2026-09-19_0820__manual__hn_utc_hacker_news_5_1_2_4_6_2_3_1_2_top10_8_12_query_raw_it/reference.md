# 参考来源 · HN 书摘 2026-09-19

## 原始条目 (query_raw_items)
- Passkeys 反对文: query_raw_items(source=hackernews, keyword=passkeys, min_points=100)[id:426173] = ▲662 💬647, Hawksley 系统拆解 passkeys 对个人用户的锁定风险
- Hacking OpenAI: query_raw_items(source=hackernews, keyword=Hacktron OpenAI hacking)[id:424569] = ▲468 💬197, Hacktron 72h 从论坛 RCE 到 OpenAI 内部代码仓库
- Conway 猜想证明: query_raw_items(source=hackernews, keyword=Conway proof Abramov)[id:426525] = ▲198 💬174, Dan Abramov 用 AI+Lean 证明 Conway refinement 猜想
- ZCode 静默上传: query_raw_items(source=hackernews, keyword=ZCode git upload)[id:426019] = ▲256 💬64, ZCode 打包 .git 历史加密上传阿里云 OSS
- HarnessTax 论文: query_raw_items(source=hackernews, keyword=ZCode git upload)[id:416942] = ▲225 💬93, harness 设计对编码代理性能影响的实证研究

## 评论页抓取 (fetch_url)
- Passkeys HN 评论: fetch_url(https://news.ycombinator.com/item?id=49753211) = dspillett 评论关于 Amazon 强推 passkeys 的体验
- Conway 猜想 HN 评论: fetch_url(https://news.ycombinator.com/item?id=49755024) = gbjcantab "wizardry vs sorcery" 隐喻讨论
- ZCode HN 评论: fetch_url(https://news.ycombinator.com/item?id=49752422) = 帖子已被 flagged，评论转至 id:49750694
- HarnessTax HN 评论: fetch_url(https://news.ycombinator.com/item?id=49733726) = 社区讨论 harness 对小模型的重要性大于大模型

## 正文抓取 (fetch_url)
- Passkeys 正文: fetch_url(https://hawksley.dev/blog/i-dont-like-passkeys) = 硬件密钥 25-300 账户上限、云同步锁定风险、恢复方式是瓶颈
- ZCode 正文: fetch_url(https://tokenstead.ai/guides/zcode-silent-git-history-upload) = 42,411 文件快照 .git 占 86.6%, 信封加密 RSA-OAEP+AES-256-CTR
- Conway 正文: fetch_url(https://overreacted.io/how-i-vibed-a-proof-of-conways-conjecture/) = Palomar registry 机器检查通过, Abramov 自述"数学外行"
