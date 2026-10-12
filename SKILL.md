---
name: awesome-github-toolkit
description: "Curated knowledge base of 50 practical open-source GitHub repos for AI/LLM, agents, RAG, automation, web scraping, security, and dev learning. TRIGGER when the user mentions or wants to install/set up/port/build with: ollama, llama.cpp, vLLM, transformers, nanoGPT, DeepSeek, langchain, LlamaIndex, RAGFlow, dify, langflow, open-webui, Lobe Chat, ComfyUI, openclaw, iFixAi, crewAI, MetaGPT, AutoGen, aider, markitdown, mem0, supermemory, browser-use, stagehand, firecrawl, n8n, maigret, bumblebee, TradingAgents, public-apis, awesome-selfhosted, awesome-claude-skills, developer-roadmap, free-programming-books, coding-interview-university, tech-interview-handbook, system-design-primer, the-art-of-command-line, build-your-own-x, you-dont-know-js, javascript-algorithms, 30-seconds-of-code, gitignore, freeCodeCamp, the-book-of-secret-knowledge. Also trigger on: 本地跑大模型/LLM推理加速, 搭AI Agent/多Agent, 做RAG/知识库, 爬虫/网页自动化/浏览器自动化, 自托管, 免费API, 系统设计/编程面试准备, 零基础学编程, 帮我选XX工具/快速搭一个XX/移植XX. Gives repo URL + install + quickstart + when-to-use. SKIP: unrelated UI/CSS or generic coding with no tool-selection intent."
license: Personal knowledge base; each repo keeps its own upstream license.
---

# Awesome GitHub Toolkit（50 个超实用开源仓库知识库）

这是一个**可检索的工具选型 + 快速实施**知识库，收录 50 个经过实战检验的 GitHub 仓库。
用户提到任何相关工具、或想"搭一个 XX / 移植 XX / 快速上手 XX"时，本 Skill 提供：**仓库地址 → 一键安装 → 最小可运行示例 → 选型建议**。

## 使用方式（被触发时怎么做）

1. 从下方**总索引表**或**决策图**定位目标仓库。
2. 给出：仓库链接 + 适用场景 + 安装命令 + 最小 quickstart。
3. 若用户要深入（架构、API、部署细节），打开对应的 `reference/` 子文件再展开。
4. **不要照抄本文件里的命令当作最新版本** —— 部署前用 `fetch_web_content` 或提示用户核对仓库当前 README（版本与命令会变）。

> 说明：原始清单 50 条中有 3 组重复（#7=#48 coding-interview-university、#18=#49 langchain、#19=#50 n8n）。下表已合并去重，共 **47 个唯一仓库**，均保留原链接。

## 总索引表

### A. 学习成长 / 求职面试（详见 `reference/1-learning-career.md`）
| 仓库 | 用途 | 链接 |
|---|---|---|
| developer-roadmap | 任意技术的学习路线图 | github.com/kamranahmedse/developer-roadmap |
| free-programming-books | 数千本免费编程书 | github.com/EbookFoundation/free-programming-books |
| freeCodeCamp | 免费全栈编程学习平台 | github.com/freeCodeCamp/freeCodeCamp |
| project-based-learning | 从做项目中学编程 | github.com/practical-tutorials/project-based-learning |
| coding-interview-university | 转码 / 面试完整备考 | github.com/jwasham/coding-interview-university |
| tech-interview-handbook | 技术面试速查手册 | github.com/yangshun/tech-interview-handbook |
| system-design-primer | 系统设计入门 | github.com/donnemartin/system-design-primer |
| the-art-of-command-line | 命令行技巧 | github.com/jlevy/the-art-of-command-line |

### B. 编程基础 / 开发资源（详见 `reference/2-dev-fundamentals.md`）
| 仓库 | 用途 | 链接 |
|---|---|---|
| build-your-own-x | 从零造轮子边做边学 | github.com/codecrafters-io/build-your-own-x |
| you-dont-know-js | JS 深入原理 | github.com/getify/You-Dont-Know-JS |
| javascript-algorithms | JS 算法与数据结构 | github.com/trekhleb/javascript-algorithms |
| 30-seconds-of-code | 30 秒代码片段 | github.com/Chalarangelo/30-seconds-of-code |
| github/gitignore | 官方 .gitignore 模板 | github.com/github/gitignore |

### C. 资源合集 / 目录（详见 `reference/3-resources-catalog.md`）
| 仓库 | 用途 | 链接 |
|---|---|---|
| public-apis | 免费 API 合集 | github.com/public-apis/public-apis |
| awesome-selfhosted | 可自托管应用清单 | github.com/awesome-selfhosted/awesome-selfhosted |
| the-book-of-secret-knowledge | 运维/安全工具宝典 | github.com/trimstray/the-book-of-secret-knowledge |
| awesome-claude-skills | Claude Skills 合集 | github.com/ComposioHQ/awesome-claude-skills |

### D. LLM 推理 / 本地大模型（详见 `reference/4-llm-inference.md`）
| 仓库 | 用途 | 链接 |
|---|---|---|
| ollama | 一行命令本地跑大模型 | github.com/ollama/ollama |
| llama.cpp | C/C++ 推理引擎，CPU 也能跑 | github.com/ggerganov/llama.cpp |
| vLLM | 高吞吐推理与服务 | github.com/vllm-project/vllm |
| transformers | HuggingFace 模型库 | github.com/huggingface/transformers |
| nanoGPT | Karpathy 的极简 GPT 训练 | github.com/karpathy/nanoGPT |
| deepseek-ai | DeepSeek 官方（权重+内核） | github.com/deepseek-ai |

### E. AI 应用构建器 / 可视化 / 本地助手（详见 `reference/5-ai-builders.md`）
| 仓库 | 用途 | 链接 |
|---|---|---|
| dify | 可视化 AI 应用/Agent 平台 | github.com/langgenius/dify |
| langflow | 拖拽式 LLM 工作流 | github.com/langflow-ai/langflow |
| open-webui | 自托管 ChatGPT 风格 UI | github.com/open-webui/open-webui |
| lobe-chat | 开源现代聊天框架 | github.com/lobehub/lobe-chat |
| ComfyUI | AI 绘画节点编辑器 | github.com/comfyanonymous/ComfyUI |
| openclaw | 本地个人 AI 助手(Gateway) | github.com/openclaw/openclaw |
| iFixAi | AI Agent 对齐/安全审计 CLI | github.com/ifixai-ai/iFixAI |

### F. AI Agent / LLM 应用框架 + 文档/编程助手（详见 `reference/6-ai-agents.md`）
| 仓库 | 用途 | 链接 |
|---|---|---|
| langchain | LLM 应用开发框架 | github.com/langchain-ai/langchain |
| llama_index | RAG / 数据框架 | github.com/run-llama/llama_index |
| crewAI | 角色化多 Agent 框架 | github.com/crewAIInc/crewAI |
| MetaGPT | 多 Agent "软件公司" | github.com/geekan/MetaGPT |
| autogen | 微软多 Agent 框架 | github.com/microsoft/autogen |
| aider | 终端 AI 结对编程 | github.com/Aider-AI/aider |
| markitdown | 文档转 Markdown | github.com/microsoft/markitdown |

### G. RAG / 记忆层（详见 `reference/7-rag-memory.md`）
| 仓库 | 用途 | 链接 |
|---|---|---|
| RAGFlow | 深度文档理解 RAG 引擎 | github.com/infiniflow/ragflow |
| mem0 | AI 记忆层 | github.com/mem0ai/mem0 |
| supermemory | 通用记忆工具/API | github.com/supermemoryai/supermemory |

### H. 自动化 / 爬虫 / 浏览器（详见 `reference/8-automation-scraping.md`）
| 仓库 | 用途 | 链接 |
|---|---|---|
| n8n | 无代码自动化工作流 | github.com/n8n-io/n8n |
| firecrawl | 网站爬取→LLM 就绪数据 | github.com/mendableai/firecrawl |
| stagehand | 自然语言浏览器自动化 | github.com/browserbase/stagehand |
| browser-use | AI 驱动浏览器操作 | github.com/browser-use/browser-use |

### I. OSINT / 安全 / 量化（详见 `reference/9-osint-security-trading.md`）
| 仓库 | 用途 | 链接 |
|---|---|---|
| maigret | 用户名 OSINT 情报 | github.com/soxoj/maigret |
| bumblebee | 供应链依赖暴露扫描 | github.com/perplexityai/bumblebee |
| TradingAgents | 多 Agent 交易模拟 | github.com/TauricResearch/TradingAgents |

## 决策图：我想做 X → 用哪个

- **本地/离线跑大模型，最省事** → `ollama`；**CPU/树莓派/边缘** → `llama.cpp`；**GPU 高并发对外服务** → `vLLM`
- **训练/微调、读论文跑模型** → `transformers` / `nanoGPT`；**用 DeepSeek 系模型/内核** → `deepseek-ai`
- **快速做一个 AI 应用，不想写代码** → `dify` / `langflow`
- **自托管一个"ChatGPT"界面** → `open-webui`（常配 `ollama`）；更现代/可扩展 → `lobe-chat`
- **搭对话机器人 / 多 Agent 系统** → `langchain` / `crewAI` / `MetaGPT` / `autogen`
- **给自己的产品加"长期记忆"** → `mem0` / `supermemory`
- **基于自有文档做问答(RAG)** → `llama_index`（灵活）；复杂文档/开箱即用 → `RAGFlow`
- **抓取网站喂给 LLM** → `firecrawl`；**让 AI 自己点网页** → `browser-use` / `stagehand`
- **定时/条件自动跑任务、串接 API** → `n8n`
- **AI 帮我改代码（终端里）** → `aider`
- **PDF/Office 转 Markdown 喂模型** → `markitdown`
- **AI 生图/工作流** → `ComfyUI`
- **要一个能登微信/Telegram/Slack 的本地助手** → `openclaw`
- **审查 AI Agent 是否合规/被注入/幻觉** → `iFixAi`
- **查一个用户名在各平台的踪迹(授权范围内)** → `maigret`；**查本机依赖是否命中已披露的投毒/漏洞** → `bumblebee`
- **找免费 API / 自托管服务清单 / 学编程 / 备面试 / 学系统设计** → 见 A/B/C 类

## 通用注意事项

- **版本会变**：安装/启动命令以仓库当前 README 为准；动手前建议 `fetch_web_content` 核对。
- **硬件门槛**：`vLLM`/`RAGFlow`/`ComfyUI`/`transformers` 微调倾向需要 NVIDIA GPU；`ollama`/`llama.cpp` CPU 可跑。
- **合规与伦理**：`maigret`、`bumblebee`、`TradingAgents` 等仅用于**授权范围内**的测试/研究/自身资产；不要在未授权目标上使用。
- **许可**：多为 MIT/Apache-2.0，少数（如 `ComfyUI` 为 GPL-3.0）需按其上游许可商用，二次分发前核对 LICENSE。
