# OSINT / 安全 / 量化

## maigret — https://github.com/soxoj/maigret
- 用途：用户名 OSINT：在数千平台查同一用户名的账号，生成情报报告。
- 安装：`pip install maigret`。
- 快速：`maigret someusername`（可加参数导出 HTML / PDF 报告）。
- 何时用：授权范围内的调查 / 研究，摸清某账号的公开足迹。
- 注意：仅用于合规、授权、公开信息；不得用于跟踪 / 骚扰他人。

## bumblebee — https://github.com/perplexityai/bumblebee
- 用途：Perplexity 的只读供应链安全扫描器：扫描本机（macOS / Linux）依赖包 / 扩展 / 开发工具元数据，比对已知投毒 / 漏洞清单，定位"哪些机器命中"。
- 安装：Go 项目，下载 Releases 二进制（或 `go install`），无需常驻。
- 快速：`bumblebee scan --exposure-catalog <catalog.json>`（用其 `threat_intel/` 目录公开清单）。
- 何时用：出现供应链投毒 / 漏洞公告时，快速清点本机依赖暴露面。
- 注意：只读、不做处置；输出 JSON 记录；只扫自己有权管理的机器。Apache-2.0。

## TradingAgents — https://github.com/TauricResearch/TradingAgents
- 用途：多 Agent 金融交易模拟（研究 / 风控 / 交易等角色协作）框架。
- 安装：clone 后 `pip install -r requirements.txt`（按其 README 配 LLM Key 与数据源）。
- 何时用：研究"多 Agent 做交易决策"的学术 / 原型实验。
- 注意：仅研究 / 模拟，非投资建议；需 LLM API，成本较高；数据源需自行合规获取。
