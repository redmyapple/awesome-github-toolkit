# 自动化 / 爬虫 / 浏览器自动化

## n8n — https://github.com/n8n-io/n8n
- 用途：无代码 / 低代码自动化工作流，数百集成，可自托管，支持 AI 节点。
- 安装：Docker `docker run -it --rm -p 5678:5678 -v ~/.n8n:/home/node/.n8n n8nio/n8n`；或 `npm i -g n8n && n8n`。
- 快速：开 `http://localhost:5678`，拖节点配触发（定时 / Webhook）→ 动作（HTTP / Gmail / DB / AI）。
- 何时用：定时任务、跨系统串接、把多个 API + LLM 编成流水线。
- 注意：凭据存本地卷；暴露公网需加鉴权 / 反向代理。

## firecrawl — https://github.com/mendableai/firecrawl
- 用途：把网站爬成"LLM 就绪"的干净 Markdown / 结构化数据，处理翻页 / 动态页。
- 安装 / 使用：`pip install firecrawl-py`→`from firecrawl import FirecrawlApp`→`FirecrawlApp(api_key=...).scrape_url("https://...")`；也可自托管 Docker。
- 何时用：抓网页喂 RAG / Agent，需要干净内容而非原始 HTML。
- 注意：托管需 API Key；自托管较重；遵守目标站 robots / 条款。

## stagehand — https://github.com/browserbase/stagehand
- 用途：Browserbase 出品：自然语言 + Playwright 结合的浏览器自动化库（TS）。
- 安装：`npm install @browserbasehq/stagehand`（配合 Playwright）。
- 快速：用 `act` / `extract` / `observe` 等 API 以自然语言驱动页面，如 `page.act("click login")`。
- 何时用：想用自然语言写稳定的浏览器流程；可结合 Browserbase 云浏览器。
- 注意：需配模型做理解；本地跑要装 Playwright 浏览器。

## browser-use — https://github.com/browser-use/browser-use
- 用途：让 AI Agent 自己操作浏览器（打开、点击、填表、读页）。
- 安装：`pip install browser-use` 并 `playwright install`（见其 quickstart）。
- 快速：指定 LLM + 任务，Agent 自动驱动浏览器完成（如"在 X 站搜 Y 并总结"）。
- 何时用：无 API 的网站、需要"AI 自主浏览"的场景。
- 注意：需 LLM Key；速度 / 成本受模型影响；仅用于授权与合规场景。
