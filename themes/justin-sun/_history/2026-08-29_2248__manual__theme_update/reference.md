# 数据来源溯源（2026-08-29 定版）

- BTCUSDT 现价: binance_get_price(symbol=BTCUSDT) = 78023.9 (2026-08-29 14:48 UTC)
- TRXUSDT 现价/24h: binance_get_ticker(symbol=TRXUSDT) = 0.33828, 24h -0.588%, 高0.34221/低0.33739, 量1.47亿
- WLFIUSDT 现价/24h: binance_get_ticker(symbol=WLFIUSDT) = 0.05821, 24h -0.479%
- TRX 20日K线区间: binance_get_klines(symbol=TRXUSDT, interval=1d, limit=20) = 0.32805-0.35355（收盘0.33828）
- 稳定币总市值/USD1增发: query_raw_items(keyword=稳定币总市值)[id:191853] = 3045.64亿美元,+0.48%; USD1 +3.71%, USDC +0.76%, USDT 市占60.21%
- 美联储资产负债表: query_indicators(category=macro, country=us)[fed_balance_sheet] = 6730912.0 (2026-08-26)
- 7月核心PCE: query_indicators / query_calendar_events = 3.34% yoy, PCE 3.7% yoy (2026-08-26 发布)
- 美国CPI同比: query_indicators(category=macro, country=us)[cpi_yoy_us] = 3.4% (2026-07-01, 59天前, 已陈旧)
- Binance-HTX隔离: query_raw_items(keyword=HTX)[id:112905] = Binance不再处理涉及HTX(Huobi Global SA)/EXMO等实体交易(2026-08-14)
- 孙宇晨回应HTX: query_raw_items(keyword=HTX)[id:122860] = 孙宇晨称HTX不在英欧展业、与英欧监管和解谈判进行中(2026-08-15)
- OCC批准WLFI信托银行: query_raw_items(keyword=WLFI)[id:176733] = OCC初步有条件批准WLFI设立全国性信托银行发行USD1；阿布扎比Tahnoon bin Zayed via WLTC Holdings持股49%，特朗普家族约38%(2026-08-28)
- WLFI任命CBO: query_raw_items(keyword=WLFI)[id:99245] = WLFI任命前Coinbase高管Ryan Ballantyne为首席商务官(2026-08-13)
- 孙宇晨景甜长文: query_raw_items(keyword=孙宇晨)[id:177553] = 孙宇晨发布《我的女友景甜》长文，称景甜索要5000万美元代孕费(2026-08-28)
- 微博AI造假通报: query_raw_items(keyword=孙宇晨)[id:178002] = 微博通报孙宇晨谷爱凌聊天记录系AI炮制、造谣账号已关闭(2026-08-28)
- 孙宇晨驻港表态: query_raw_items(keyword=孙宇晨)[id:179786] = 孙宇晨称近期一直在香港生活工作，关注香港数字货币政策(2026-08-28)
- 特朗普加密损失47亿: query_raw_items(keyword=WLFI)[id:177309] = 维权组织称特朗普相关加密项目致投资者损失约47亿美元(TRUMP~32亿+WLFI等)(2026-08-28)
- 孙宇晨起诉WLFI(基线): query_raw_items(keyword=孙宇晨)[id:47846] = 孙宇晨起诉WLFI非法阻止其出售代币(2026-07-02)
- 美联储Warsh鹰派: 历史记忆(2026-08-28 Jackson Hole) = 9月加息25bp概率升至59.7%(基线8/12为42.1%)；BTC 24h爆仓4.74亿美元、跌至~$77.5K

# reference.md — justin-sun 主题更新 2026-08-29

## 行情（Binance 实时，2026-08-29 14:55 UTC）
- BTCUSDT 现价 77,965.7 美元: binance_get_price(BTCUSDT) = 77965.7
- TRXUSDT 现价 0.33842 美元，24h -0.582%，高 0.34221/低 0.33739，量 146.7M TRX: binance_get_ticker(TRXUSDT)
- TRUMPUSDT 现价 2.731 美元，24h -3.634%，高 3.068/低 2.51，量 385.7M TRUMP，额 $1.07B: binance_get_ticker(TRUMPUSDT)
- TRUMP 24h 曾 +8% 至 2.936 美元、市值 20.37 亿美元（早盘，后回落）: query_raw_items(keyword='HTX')[id:191054]
- BTC 反弹至 78,007.56 美元、24h -0.28%（14:47 HTX 行情）: query_raw_items(keyword='HTX')[id:192086]

## 稳定币与生态
- 稳定币总市值 3045.64 亿美元、周 +0.48%，USDC +0.76%、USD1 +3.71%、USDT 占 60.21%: query_raw_items(keyword='稳定币')[id:191853]
- HTX USDD 活期 4.00%（主流 CEX 中低差异化）: query_raw_items(keyword='USDD')[id:180129]
- BIS 唱空稳定币、更看好代币化存款: query_raw_items(keyword='稳定币')[id:191351]
- JPMorgan 评估自推稳定币: query_raw_items(keyword='稳定币')[id:154851]
- HKDAP 港元稳定币授权分销商增至 5 家: query_raw_items(source='telegram:Financial_Express')[id:181154]
- Fireblocks 托管钱包近一周向 Binance 转入约 6600 万美元 USD1: query_raw_items(keyword='USD1')[id:156250]

## 孙宇晨个人事件
- 孙宇晨/景甜纠纷波及景田纯净水（同音品牌恶搞）: query_raw_items(keyword='Justin Sun')[id:191026]
- 微博官方证实孙-谷爱凌聊天记录系 AI 炮制、造谣账号已关闭: query_raw_items(keyword='孙宇晨')[id:178002]
- 孙宇晨称长期驻港、高度关注香港数字货币政策: query_raw_items(keyword='孙宇晨')[id:179786]
- 孙宇晨 8/28 发《我的女友景甜》长文，称景甜索要 5000 万美元代孕费: query_raw_items(keyword='孙宇晨')[id:178860]

## 政治关系与诉讼
- OCC 初步有条件批准 WLFI 设全国性信托银行，阿布扎比 Tahnoon 49%、特朗普家族约 38%: query_raw_items(keyword='WLFI')[id:176733]
- NYT 7/2 孙宇晨起诉 WLFI，指控其非法阻止出售代币: query_raw_items(keyword='WLFI')[id:47846]
- Binance 8/14 起停止处理 HTX（Huobi Global SA）/EXMO 相关交易: query_raw_items(keyword='HTX')[id:112905]
- 孙宇晨 8/15 称 HTX 不在英欧展业、与英欧监管和解谈判进行中: query_raw_items(keyword='Justin Sun')[id:122860]

## 监管与诈骗尾部
- GOLD 骗局团队获利约 101 万美元、抛售 82.45% 代币: query_raw_items(keyword='GOLD')[id:191348]
- GOLD 开发者资金可追溯至 KuCoin、并部署 PLATINUM: query_raw_items(keyword='GOLD')[id:191854]
- CFTC 罚前白宫提词员 17.2 万美元（利用特朗普演讲下注）: query_raw_items(keyword='CFTC')[id:191223]

## 情绪与宏观
- 加密恐慌贪婪指数 68（贪婪，前日 73）: query_raw_items(keyword='恐慌')[id:191225]
- Waller 鹰派、9 月加息概率升至近 60%: query_raw_items(keyword='美联储')[id:191916]
- 美联储资产负债表 6,730,912（2026-08-26）: query_indicators(country='us')[fed_balance_sheet]
- 美国 7 月 CPI 同比 3.4%、核心 CPI 2.5%；8 月消费者信心 89.4（8/25）；7 月核心 PCE 同比 3.3%: query_calendar_events(country='US', importance='high')
- 未来事件：9/11 美国 CPI、9/15 FOMC 会议: query_calendar_events(country='US')

- TRXUSDT 现价 $0.33845, 24h -0.587%, 高 0.34221/低 0.33739, 成交量 1.47亿 TRX: binance_get_ticker(symbol=TRXUSDT) = {price:0.33845, change:-0.587%, high:0.34221, low:0.33739, volume:146874800}
- TRXUSDT 14日K线区间 0.331–0.346, 近乎零涨幅: binance_get_klines(symbol=TRXUSDT, interval=1d, limit=14) = 收盘 0.33101(8/16)→0.33845(8/29)
- BTCUSDT 现价 $77,985.10: binance_get_price(symbol=BTCUSDT) = 77985.10 (2026-08-29 14:59 UTC)
- BTC 反弹至 78,007.56, 24h -0.28%: query_raw_items(keyword='HTX')[id:192086] = 比特币反弹，短时突破7.8万美元，现报价78007.56美元，24小时跌幅缩窄至0.28%
- 稳定币总市值 $3045.64B, 周增0.48%, USDT占60.21%, USD1周增3.71%: query_raw_items(keyword='WLFI OR USD1')[id:191853] = 稳定币总市值重拾升势，过去一周增长0.48%；USDC和USD1是增发主力，USD1增发3.71%；USDT市占率60.21%
- TRUMP 24h +8%, $2.936, 市值 $2.037B: query_raw_items(keyword='HTX')[id:191054] = TRUMP 24小时涨近8%，市值升至20.37亿美元
- 孙宇晨/景甜纠纷外溢景田纯净水: query_raw_items(keyword='Justin Sun OR 孙宇晨')[id:191026] = 孙宇晨、景甜纠纷波及景田纯净水，同音品牌遭恶搞，旗舰店客服：建议举报
- 微博通报孙宇晨-谷爱凌聊天记录系AI炮制: query_raw_items(keyword='孙宇晨')[id:178002] = 微博官方通报：孙宇晨谷爱凌聊天记录系 AI 炮制，造谣账号已被关闭
- 孙宇晨发布《我的女友景甜》长文: query_raw_items(keyword='孙宇晨')[id:177553] = 孙宇晨发布《我的女友景甜》小作文，提及景甜索要5000万美元代孕费
- Binance不再处理HTX/EXMO交易: query_raw_items(keyword='HTX')[id:112905] = Binance将不再处理涉及HTX、EXMO等平台的相关交易，用户需额外合规审核
- 美股盘前要闻确认Binance-HTX: query_raw_items()[id:113439] = 美股盘前要闻：Binance表示将不再处理涉及HTX、EXMO等平台的相关交易
- Justin Sun: 和解谈判进行中, HTX不在英欧展业: query_raw_items(keyword='Justin Sun')[id:122860] = Justin Sun称与英欧监管和解谈判进行中，HTX不在英国与欧盟展业
- 孙宇晨诉WLFI: query_raw_items(keyword='WLFI')[id:47846] = 孙宇晨起诉World Liberty Financial，指控其非法阻止出售代币
- HTX USDD活期4.00%, 仅HTX提供: query_raw_items(keyword='USDD')[id:180129] = 主流CEX稳定币活期：HTX USDD为4.00%；USDT小额档最高10%，Binance U产品8.59%
- 孙宇晨驻港表态: query_raw_items(keyword='孙宇晨')[id:179786] = 孙宇晨表示近期一直在香港生活工作，高度关注香港数字货币政策
- 张小泉被炒"指甲刀概念股"高开超11%: query_raw_items(keyword='孙宇晨')[id:177644] = 张小泉股价高开超11%，因孙宇晨景甜事件被列为"指甲刀概念股"
- 特朗普加密项目致投资者损失约$4.7B: query_raw_items(keyword='WLFI OR TRUMP')[id:177309] = 维权组织：特朗普相关加密项目致投资者损失约47亿美元，TRUMP约32亿
- WLFI获OCC有条件信托银行牌照: query_raw_items(keyword='WLFI')[id:122695] = World Liberty获美国OCC有条件信托银行牌照，USD1稳定币发行权将转移
- 阿布扎比王室持WLFI新银行49%: query_raw_items(keyword='WLFI')[id:176733] = 阿布扎比王室成员持有WLFI新银行控股公司49%股份
- CFTC罚没前白宫提词员17.2万美元: query_raw_items(keyword='CFTC')[id:190902] = CFTC已罚没前白宫提词员17.2万美元（利用特朗普演讲交易事件合约）
- 蹭叙事诈骗代币GOLD/PLATINUM出现: query_raw_items(keyword='TRUMP')[id:191854] = 蹭叙事诈骗代币GOLD/PLATINUM已出现
- 参院民主党就阿联酋$5亿投资WLFI要求听证: query_raw_items(keyword='WLFI')[id:38206] = 参院民主党就阿联酋5亿美元投资WLFI要求听证
- HKDAP授权分销商增至5家: query_raw_items(keyword='孙宇晨')[id:181154] = 港元稳定币HKDAP授权分销商已增至5家（kahneman引用）
- DJT.US Q2净亏$1.3B, DCF公允价值$1.37 vs现价$8.35, 同比跌超50%, 共识Sell: query_longbridge_by_route(news/company, symbol=DJT.US) = Trump Media Q2净亏13亿美元，DCF公允价值$1.37 vs $8.35，同比跌超50%，共识Sell
- FOMC下一会议2026-09-15/16(SEP), 目标区间3.50–3.75%(截至2026-07-28): query_fomc(lookback=120, lookahead=120) = next_meeting 2026-09-15/16, target_range 3.50–3.75% as of 2026-07-28


## geopolitics_agent 刷新（2026-08-29 15:03 UTC）
- TRXUSDT 现价 0.33819 美元，24h -0.614%，高 0.34221/低 0.33739，量 146.4M TRX: binance_get_ticker(symbol=TRXUSDT) = 0.33819 (2026-08-29 15:03 UTC, geopolitics_agent 刷新)
- FOMC 下一会议 2026-09-15/16 确认（sep_meeting=True，当前目标区间 3.50–3.75% 截至 2026-07-28）: query_fomc(lookahead=45, lookback=30) = next_meeting 2026-09-15/16
- 孙宇晨驻港表态（香港锚定战略）: query_raw_items(keyword='孙宇晨')[id:179786] = 孙宇晨表示近期一直在香港生活工作，高度关注香港数字货币政策（geopolitics_agent 引用）
- 孙宇晨诉WLFI（美系政治前线敞口）: query_raw_items(keyword='WLFI')[id:47846] = 孙宇晨起诉World Liberty Financial，指控其非法阻止出售代币（geopolitics_agent 引用）
- 孙宇晨/景甜纠纷外溢景田纯净水（治理脆弱性领先信号）: query_raw_items(keyword='Justin Sun')[id:191026] = 孙宇晨、景甜纠纷波及景田纯净水，同音品牌遭恶搞（geopolitics_agent 引用）

# justin-sun 审查人 soros 独立核验来源（2026-08-29 15:04 UTC）

> 以下为审查人独立用 query_raw_items / query_longbridge_by_route / query_fomc 核验草稿论据的来源追加。
> 注意：草稿中 id:161414（JPMorgan 自推稳定币）、id:181154（HKDAP 授权分销商增至 5 家）经独立检索未能证实，未列入已确认来源。

- 稳定币总市值 3045.64亿美元(=$304.564B)、周增0.48%、USDT市占60.21%、USD1周增3.71%: query_raw_items(keyword='稳定币 总市值')(id:191853) = 稳定币总市值重拾升势，过去一周增长0.48%，现报3045.64亿美元，USDC和USD1是增发主力，USD1增发3.71%，USDT市占60.21%
- Binance切断HTX/EXMO交易: query_raw_items(keyword='HTX')(id:112905) = Binance将不再处理涉及HTX、EXMO等平台的相关交易
- Binance隔离HTX(盘前要闻确认): query_raw_items(keyword='HTX')(id:113439) = Binance根据监管要求变化将不再处理涉及HTX、EXMO等平台的相关交易
- 孙宇晨诉WLFI: query_raw_items(keyword='孙宇晨')(id:47846) = 孙宇晨起诉世界自由金融，声称其为托价非法阻止他出售代币（2026-07-02）
- WLFI获OCC初步有条件批准设立全国性信托银行发行USD1; Tahnoon持49%、特朗普家族约38%: query_raw_items(keyword='WLFI')(id:176733) = 阿布扎比王室Tahnoon持WLTC Holdings 49%，特朗普家族约38%，OCC本月初步有条件批准World Liberty设立全国性信托银行发行USD1
- 特朗普相关加密项目致投资者损失约47亿美元(TRUMP约32亿): query_raw_items(keyword='WLFI')(id:177309) = 维权组织估算特朗普相关加密项目致投资者损失约47亿美元
- TRUMP 24h+8%至$2.936、市值20.37亿: query_raw_items(keyword='HTX')(id:191054) = TRUMP 24小时涨近8%，现报2.936美元，市值20.37亿美元
- BTC反弹至78007.56、24h-0.28%: query_raw_items(keyword='HTX')(id:192086) = 比特币反弹短时突破7.8万，现报78007.56美元，24h跌幅缩窄至0.28%
- BTC 8/28跌破7.7万至77119: query_raw_items(keyword='HTX')(id:184728) = 比特币短时跌破7.7万美元，现报77119美元，24h跌幅4.22%
- 主流CEX稳定币活期: USDT小额档10%、Binance U 8.59%: query_raw_items(keyword='HTX')(id:180129) = 主流CEX稳定币活期收益盘点USDT小额档最高10%，Binance U产品达8.59%
- Justin Sun确认英欧监管和解谈判进行中: query_raw_items(keyword='WLFI OCC')(id:122860) = Justin Sun称与英国欧盟监管机构和解谈判进行中，HTX不在英国与欧盟展业
- BIS唱空稳定币: query_raw_items(keyword='孙宇晨 监管')(id:191351) = BIS称稳定币难以成为大规模支付工具，代币化存款更具优势
- CFTC罚没前白宫提词员17.2万美元: query_raw_items(keyword='WLFI OCC')(id:190902) = CFTC罚没前白宫提词员17.2万美元，利用特朗普演讲信息非法交易
- GOLD/PLATINUM蹭叙事诈骗代币: query_raw_items(keyword='GOLD PLATINUM')(id:191854) = GoPlus监测GOLD开发者资金追溯至KuCoin，并部署PLATINUM
- 景甜长文: query_raw_items(keyword='孙宇晨')(id:177553) = 孙宇晨发布《我的女友景甜》小作文，称景甜索要5000万美元代孕费
- AI炮制聊天记录: query_raw_items(keyword='孙宇晨')(id:178002) = 微博官方通报孙宇晨谷爱凌聊天记录系AI炮制，造谣账号已关闭
- 景田纯净水外溢: query_raw_items(keyword='孙宇晨')(id:191026) = 孙宇晨景甜纠纷波及景田纯净水，同音品牌遭恶搞
- 张小泉指甲刀概念股: query_raw_items(keyword='孙宇晨')(id:177644) = 张小泉股价高开超11%，被炒为指甲刀概念股
- 孙宇晨驻港表态: query_raw_items(keyword='孙宇晨')(id:179786) = 孙宇晨称近期一直在香港生活工作，支持香港数字货币政策
- 参院民主党就阿联酋5亿投资WLFI要求听证: query_raw_items(keyword='WLFI OCC')(id:38206) = 美参议院民主党人要求就阿联酋5亿美元投资特朗普加密项目举行听证
- HTX 8/27上线TAO: query_raw_items(keyword='HTX')(id:167301) = 火币HTX将于8月27日21:00上线TAO
- HTX DeepThink谈Warsh长端收益率约束: query_raw_items(keyword='TRX OR TRON OR USDD')(id:90455) = HTX DeepThink分析政策利率之外长端收益率正成为Crypto估值关键约束，提及Warsh框架
- DJT Q2净亏13亿、DCF公允$1.37 vs现价$8.35、共识Sell: query_longbridge_by_route(news/company, DJT.US) = Trump Media Q2净亏$1.3B，DCF公允$1.37 vs现价$8.35，同比跌超50%，共识Sell
- 下一FOMC 2026-09-15/16(SEP)、目标区间3.50-3.75%(截至2026-07-28): query_fomc(lookback=120,lookahead=60) = 下一会议2026-09-15/16，sep_meeting=True，目标区间3.50-3.75% as of 2026-07-28
- Sanders/Warren抨击特朗普家族加密(8/27，草稿未覆盖): query_raw_items(keyword='WLFI OCC')(id:171540) = Bernie Sanders称特朗普家族靠总统职位赚40亿，Warren抨击加密监管不值一提
