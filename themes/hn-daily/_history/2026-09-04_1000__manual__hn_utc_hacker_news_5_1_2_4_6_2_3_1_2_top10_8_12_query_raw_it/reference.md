# Reference — HN Daily 2026-09-04

## 数据来源

### 原始新闻数据
- Firefox讨论: query_raw_items(source=hackernews, min_points=20)[id:245629] = "Hang on to Your Firefox" (968分, 528评论)
- 本地AI设置: query_raw_items(source=hackernews, min_points=20)[id:245635] = "My local model setup on an M4 Pro Mac Mini" (152分, 72评论)
- 真实失业率: query_raw_items(source=hackernews, min_points=20)[id:245646] = "True Rate of Unemployment" (157分, 99评论)
- FBI调查: query_raw_items(source=hackernews, min_points=20)[id:245640] = "FBI Probes Service Selling 153M+ Drivers Licenses" (147分, 55评论)
- Dyson牙刷: query_raw_items(source=hackernews, min_points=20)[id:245630] = "Dyson CameraJet electric toothbrush" (103分, 113评论)
- LLM推理前沿: query_raw_items(source=hackernews, min_points=20)[id:245642] = "The efficient frontier of LLM inference" (96分, 25评论)

### 文章正文抓取
- Firefox文章: fetch_url(url=https://www.newsonaut.com/articles/hang-on-to-your-firefox) = 描述Firefox作为最后独立浏览器引擎的战略价值
- 本地AI设置: fetch_url(url=https://lws.io/blog/my-local-model-setup/) = 详细说明M4 Pro Mac Mini本地LLM部署方案
- 失业率数据: fetch_url(url=https://www.lisep.org/tru) = LISEP真实失业率24.9% (2026-07)
- FBI调查: fetch_url(url=https://krebsonsecurity.com/2026/09/fbi-probes-service-selling-153m-drivers-licenses/) = 153M+驾照数据泄露事件
- Dyson产品: fetch_url(url=https://www.dyson.com/oral-care/electric-toothbrush/camerajet/ceramic-ultra-blue) = CameraJet相机牙刷技术规格
- LLM推理: fetch_url(url=https://www.baseten.co/blog/the-efficient-frontier-of-llm-inference/) = 推理工程效率前沿分析

### 评论数据
- Firefox评论: fetch_url(url=https://news.ycombinator.com/item?id=49527748) = 社区对Mozilla决策的批评讨论

## 关键数据点
- 真实失业率(TRU) 24.9% (2026-07) vs 标题失业率4.1%
- 153M+ 驾照数据泄露，FBI已介入调查
- Dyson CameraJet牙刷售价$499.99，集成Gap Optical Targeting™技术
- 本地AI部署：M4 Pro Mac Mini (48GB RAM)可运行Qwen3.6-35B模型