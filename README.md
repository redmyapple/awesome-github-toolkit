# awesome-github-toolkit

一个可被 **Claude Code 自动调用**的开源工具选型知识库 Skill，收录 **47 个**高价值 GitHub 仓库，覆盖 LLM 推理 / 本地大模型、AI Agent、RAG、自动化爬虫、安全、以及学习成长。

当你提到某个工具名，或说"帮我搭一个 X / 移植 X / 快速上手 X"时，它会自动给出：**仓库地址 → 一键安装 → 最小可运行示例 → 选型建议**。

**English:** A searchable, auto-triggerable Claude Code skill: 47 curated open-source repos (LLM inference, agents, RAG, automation/scraping, security, dev learning) with install + quickstart + when-to-use guidance.

---

## 📁 目录结构

```
awesome-github-toolkit/
├── SKILL.md            # 主文件：frontmatter(触发词) + 仓库总索引 + 选型决策图 + 注意事项
├── reference/          # 渐进式披露：细节按主题拆分
│   ├── 1-learning-career.md        # 学习成长 / 求职面试
│   ├── 2-dev-fundamentals.md       # 编程基础 / 开发资源
│   ├── 3-resources-catalog.md      # 资源合集 / 目录
│   ├── 4-llm-inference.md          # LLM 推理 / 本地大模型
│   ├── 5-ai-builders.md            # AI 应用构建器 / 可视化 / 本地助手
│   ├── 6-ai-agents.md              # AI Agent / LLM 框架 + 编程助手
│   ├── 7-rag-memory.md             # RAG / 记忆层
│   ├── 8-automation-scraping.md    # 自动化 / 爬虫 / 浏览器自动化
│   └── 9-osint-security-trading.md # OSINT / 安全 / 量化
└── README.md
```

主文件只放**总览 + 路由**，每个仓库的用途/安装/quickstart/注意事项下沉到 `reference/`，需要时再展开，避免主文件过载。

---

## 🚀 作为 Claude Skill 使用

```bash
# macOS / Linux
cp -r awesome-github-toolkit ~/.claude/skills/
```
```powershell
# Windows PowerShell
Copy-Item -Recurse awesome-github-toolkit "$env:USERPROFILE\.claude\skills\"
```

重启或重开会话后自动加载，用自然语言即可触发，例如：

- "本地离线跑大模型，怎么最快搭起来？" → 命中 `ollama` / `llama.cpp` / `vLLM`
- "帮我用 dify 或 langflow 做一个知识库问答应用"
- "推荐一个 AI 浏览器自动化 / 爬虫工具" → 命中 `browser-use` / `stagehand` / `firecrawl`
- "备战编程面试 / 学系统设计，有什么资料？" → 命中 A/B/C 类

当然也可以**直接当参考清单阅读**，不安装也不影响。

---

## 🧭 收录类别（47 个唯一仓库）

| 类别 | 代表仓库 | 详见 |
|---|---|---|
| LLM 推理 / 本地大模型 | ollama、llama.cpp、vLLM、transformers、nanoGPT、DeepSeek | `reference/4-llm-inference.md` |
| AI 构建器 / 本地助手 | dify、langflow、open-webui、Lobe Chat、ComfyUI、openclaw、iFixAi | `reference/5-ai-builders.md` |
| AI Agent / LLM 框架 | langchain、LlamaIndex、crewAI、MetaGPT、AutoGen、aider、markitdown | `reference/6-ai-agents.md` |
| RAG / 记忆层 | RAGFlow、mem0、supermemory | `reference/7-rag-memory.md` |
| 自动化 / 爬虫 | n8n、firecrawl、stagehand、browser-use | `reference/8-automation-scraping.md` |
| OSINT / 安全 / 量化 | maigret、bumblebee、TradingAgents | `reference/9-osint-security-trading.md` |
| 学习成长 / 求职 | developer-roadmap、free-programming-books、freeCodeCamp、coding-interview-university、tech-interview-handbook、system-design-primer… | `reference/1-learning-career.md` |
| 编程基础 | build-your-own-x、You-Dont-Know-JS、javascript-algorithms、30-seconds-of-code、gitignore | `reference/2-dev-fundamentals.md` |
| 资源合集 | public-apis、awesome-selfhosted、the-book-of-secret-knowledge、awesome-claude-skills | `reference/3-resources-catalog.md` |

---

## ⚠️ 注意事项

- **版本会变**：安装 / 启动命令以各仓库当前 README 为准，部署前建议核对。
- **硬件门槛**：`vLLM` / `RAGFlow` / `ComfyUI` / 大模型微调倾向需要 NVIDIA GPU；`ollama` / `llama.cpp` 在 CPU 上也能跑。
- **合规与伦理**：`maigret` / `bumblebee` / `TradingAgents` 等仅用于**授权范围内**的测试 / 研究 / 自身资产，请勿在未授权目标上使用。
- **许可证**：本仓库内容采用 MIT；所收录的每个第三方仓库保留其各自上游许可证，商用二次分发前请自行核对。

## 📄 License

MIT © redmyapple
