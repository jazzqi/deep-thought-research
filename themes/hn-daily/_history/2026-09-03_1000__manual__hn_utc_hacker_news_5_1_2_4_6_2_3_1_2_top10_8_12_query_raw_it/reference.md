- HN front page 2026-09-02 (UTC): fetch_url('https://news.ycombinator.com/front?day=42615') = Top 30 items with scores and comment counts
- Gemini 3.8 Flash: fetch_url failed 404 on blog.google, source from HN front page data = ▲831, 💬485
- Hang on to Your Firefox: fetch_url('https://www.newsonaut.com/articles/hang-on-to-your-firefox') = Mark Rogers 呼吁保护 Firefox 浏览器引擎多样性
- FBI Probes 153M+ Drivers Licenses: fetch_url('https://krebsonsecurity.com/2026/09/fbi-probes-service-selling-153m-drivers-licenses/') = Krebs 深度调查，数据泄露源头疑似路易斯安那州身份验证公司
- LWN subscription prices: fetch_url failed 404 on lwn.net, source from HN front page = ▲679, 💬133
- Mistral opt-out: fetch_url failed 404 on mistral.ai, source from HN front page = ▲372, 💬164
- AI-generated SEO farms: fetch_url('https://trellner.com/') = Trellner Research 报告，215,128 个 AI 推荐页面中 59.8% 来自非 Top 10 万网站
- LLM inference efficient frontier: fetch_url('https://www.baseten.co/blog/the-efficient-frontier-of-llm-inference/') = Philip Kiely, 详细分析推理优化的延迟-吞吐权衡
- WebLLM: fetch_url('https://github.com/mlc-ai/web-llm') = MLC AI 开源项目，18.8k star，浏览器端 WebGPU 加速 LLM 推理
- Commodore 64: fetch_url('https://dfarq.homeip.net/2026/09/commodore-64-released-september-1-1982/') = 1982年9月1日发布，64KB内存，史上销量最高计算机约1230万台
- True Rate of Unemployment: fetch_url failed 404 on lisep.org, source from HN front page = ▲300, 💬337
- Google avoids ad tech breakup: fetch_url failed 403 on nytimes.com, source from HN front page = ▲267, 💬185
- Quasar 438B: fetch_url failed 404, source from HN front page = ▲160, 💬102
- GrapheneOS Pixel 11 MTE: source from HN front page = ▲173, 💬139
- Dutch central bank gold: fetch_url failed 403 on nltimes.nl, source from HN front page = ▲221, 💬218

# 审查参考数据

## 数据来源追加

- Gemini 3.8 Flash 官方博客文章链接: query_raw_items(source=hackernews, keyword="Gemini 3.8 Flash")[id:254195] = https://blog.google/innovation-and-ai/models-and-research/gemini-models/3-8-flash-and-3-8-flash-cyber/
- Gemini 3.8 Flash 模型卡: query_raw_items(source=hackernews, keyword="Gemini 3.8 Flash")[id:253334] = https://deepmind.google/models/model-cards/gemini-3-8-flash/
- FBI Probes Service Selling 153M+ Drivers Licenses (Krebs): query_raw_items(source=hackernews, keyword="Nexus driver license")[id:245640] = https://krebsonsecurity.com/2026/09/fbi-probes-service-selling-153m-drivers-licenses/
- Hang on to Your Firefox: query_raw_items(source=hackernews, keyword="Firefox")[id:245629] = https://www.newsonaut.com/articles/hang-on-to-your-firefox (注: 原始数据中分数为776，文档中为938，可能存在数据源差异)
- A note on subscription prices from LWN: query_raw_items(source=hackernews, keyword="LWN")[id:未知] = https://lwn.net (链接不具体，需验证)
- Three sites made 215,128 "best software" pages for AI: query_raw_items(source=hackernews, keyword="Perplexity")[id:未知] = https://trellner.com (链接不具体)
- Can I opt out of my input or output data being used for training? (Mistral): query_raw_items(source=hackernews, keyword="Mistral opt-out")[id:未知] = https://mistral.ai (链接不具体)
- The efficient frontier of LLM inference: query_raw_items(source=hackernews, keyword="LLM inference")[id:未知] = https://www.baseten.co/blog/the-efficient-frontier-of-llm-inference/
- My local model setup on an M4 Pro Mac Mini: query_raw_items(source=hackernews, keyword="local LLM")[id:未知] = https://lws.io/blog/my-local-model-setup/
- Dyson CameraJet electric toothbrush: query_raw_items(source=hackernews, keyword="Dyson CameraJet")[id:未知] = https://www.dyson.com/oral-care/electric-toothbrush/camerajet/ceramic-ultra-blue
- True Rate of Unemployment: query_raw_items(source=hackernews, keyword="True Rate of Unemployment")[id:未知] = https://www.lisep.org/tru
- GrapheneOS says Pixel 11 has MTE support after all: query_raw_items(source=hackernews, keyword="GrapheneOS Pixel 11 MTE")[id:未知] = https://grapheneos.social