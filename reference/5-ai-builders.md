# AI 应用构建器 / 可视化 / 本地助手

## dify — https://github.com/langgenius/dify
- 用途：开源 LLM 应用平台，可视化编排 Agent / 工作流 / RAG，自带后端。
- 安装（自托管）：`git clone https://github.com/langgenius/dify.git && cd dify/docker && cp .env.example .env && docker compose up -d`。
- 快速：浏览器打开初始化，接模型 API，拖拽搭应用，发布为 API / WebApp。
- 何时用：想低代码快速做出带 RAG / 工具 / Agent 的 AI 应用。
- 注意：容器建议给足内存（≥4GB）；需自备 LLM API Key 或本地模型。

## langflow — https://github.com/langflow-ai/langflow
- 用途：拖拽式 LLM 流程 / Agent 可视化构建，偏数据流。
- 安装：`pip install langflow`（或 `uv pip install langflow`）；`python -m langflow run`。
- 快速：启动后打开本地 UI，拖组件连线，导出 JSON / 调 API。
- 何时用：快速原型、可视化调试 LangChain 生态组件。
- 注意：底层常用 LangChain 组件；生产可把流程当 API 调用。

## open-webui — https://github.com/open-webui/open-webui
- 用途：自托管、可扩展的 ChatGPT 风格前端，原生支持 Ollama，也接 OpenAI 兼容 API。
- 安装：`pip install open-webui && open-webui serve`；或 Docker `docker run -d -p 3000:8080 -v open-webui:/app/backend/data ghcr.io/open-webui/open-webui:main`。
- 快速：开 `http://localhost:3000`，接本地 Ollama 即可聊天 / 建知识库（RAG）。
- 何时用：给本地模型一个好用界面，团队共享。
- 注意：与 Ollama 组合最常见；用数据卷持久化用户 / 会话。

## lobe-chat — https://github.com/lobehub/lobe-chat
- 用途：现代开源聊天框架，插件 / 多模型 / 知识库 / TTS / 视觉，一键部署。
- 安装：`docker run -d -p 3210:3210 lobehub/lobe-chat`；或 Vercel 一键部署。
- 何时用：想要更现代 / 好看 / 插件化的聊天前端（相较 open-webui）。
- 注意：功能多，按需在设置里接模型 Provider。

## ComfyUI — https://github.com/comfyanonymous/ComfyUI
- 用途：节点式 Stable Diffusion / 扩散模型工作流，图像 / 视频生成。
- 安装：`git clone` → `pip install -r requirements.txt` → `python main.py`；也有便携版 / Manager。
- 何时用：精确控制生图流程、复用他人 workflow JSON。
- 注意：建议 NVIDIA GPU；权重另放 `models/checkpoints`（SD / SDXL / Flux 等）。License 为 GPL-3.0，商用需注意。

## openclaw — https://github.com/openclaw/openclaw
- 用途：本地个人 AI 助手（"The AI that really does things"），经 "Gateway" 控制平面接入 WhatsApp / Telegram / Slack / Discord / Signal / iMessage 等，可加工具 / 技能 / 插件。
- 安装：`git clone https://github.com/openclaw/openclaw.git && cd openclaw && pnpm install && pnpm build && pnpm ui:build`（需 Node + pnpm）。
- 快速：按 getting-started 初始化，`openclaw` CLI 配模型 Provider 与渠道，Control UI 里试聊。
- 何时用：要一个常驻、能收发消息、带工具调用（可 sandbox）的个人助理。
- 注意：把入站消息当不可信输入；对外暴露 Gateway 前读安全指南。MIT，OpenClaw 基金会。

## iFixAi — https://github.com/ifixai-ai/iFixAi （清单写作 iFixAI）
- 用途：**AI Agent 对齐 / 独立审计** CLI：检测幻觉、提示注入，评估对齐 / 合规（OWASP LLM、EU AI Act、ISO 42001、NIST AI RMF），约 120 秒出分。
- 安装：Python，`pip install ifixai`（或用 uv/pipx，见 README）；另提供 `.claude-plugin` / `.agents/plugins`。
- 快速：`ifixai run`；`ifixai run --print-telemetry` 看遥测内容；`--no-telemetry` 关闭。
- 何时用：评估自家 Agent 是否"做该做的事"、是否易被注入 / 出幻觉、合规体检。
- 注意：默认上传假名遥测，敏感环境用 `--no-telemetry` 或 `IFIXAI_TELEMETRY=0` / `DO_NOT_TRACK=1`。Apache-2.0。
