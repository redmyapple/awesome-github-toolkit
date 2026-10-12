# AI Agent / LLM 应用框架 + 文档 / 编程助手

## langchain — https://github.com/langchain-ai/langchain
- 用途：最主流的 LLM 应用框架（链 / 工具 / Agent / RAG / 记忆），生态庞大。
- 安装：Python `pip install langchain`（+ provider 包如 `langchain-openai`）；JS `npm i langchain @langchain/core`。
- 快速：用 LCEL 组合链，或用预构建 Agent；接 `ChatOpenAI` / 本地模型。
- 何时用：构建可定制 LLM 应用 / Agent / RAG，需要大量现成集成。
- 注意：抽象多、版本演进快，建议锁版本并照官方文档写。

## llama_index — https://github.com/run-llama/llama_index
- 用途：专注 RAG / 数据接入（解析、索引、检索、查询引擎）。
- 安装：`pip install llama-index`。
- 快速：读文档 → 建向量索引 → `query_engine.query("问题")`。
- 何时用：以"自有数据问答"为核心；可与 LangChain 组合。
- 注意：与 LangChain 有重叠，通常二选一或按职责分工。

## crewAI — https://github.com/crewAIInc/crewAI
- 用途：角色化多 Agent 协作框架（给每个 Agent 定 role/goal/tool，组队完成任务）。
- 安装：`pip install crewai crewai-tools`。
- 快速：定义 Agent / Task / Crew，`crew.kickoff()`。
- 何时用：快速搭"分工协作"的多 Agent 流水线（研究、内容、调研）。
- 注意：需 LLM Key；复杂编排建议配合其 Flows。

## MetaGPT — https://github.com/geekan/MetaGPT
- 用途：多 Agent "软件公司"：输入一句需求，产出 PRD / 设计 / 代码等。
- 安装：`pip install metagpt`（按其 quickstart 配 config）。
- 快速：`metagpt "做一个xxx"`；内置 Data Interpreter 等。
- 何时用：想体验"多角色 Agent 协作产出完整产物"。
- 注意：较重、耗 token 多；先按官方 quickstart 配好模型。

## autogen — https://github.com/microsoft/autogen
- 用途：微软多 Agent 对话 / 协作框架（原 AutoGen，后有 ag2 分支，此为微软官方仓库）。
- 安装：`pip install autogen-agentchat autogen-ext[openai]`。
- 快速：定义多个 AssistantAgent + 群聊 / 编排，跑对话完成任务。
- 何时用：需要可控的多 Agent 对话、代码执行、人机协同。
- 注意：生态有 AutoGen↔AG2 分叉，注意包名 / 文档对应。

## aider — https://github.com/Aider-AI/aider
- 用途：终端里的 AI 结对编程：直接改你 Git 仓库里的代码并自动提交。
- 安装：`python -m pip install aider-chat`（或按其 `aider-install`）。
- 快速：进入 git 仓库，`aider --model gpt-4o`（或本地模型），对话式让它改文件。
- 何时用：想让 AI 在真实代码库上做多文件编辑并与 Git 集成。
- 注意：会真实改动并提交代码，先在小仓库 / 分支试。

## markitdown — https://github.com/microsoft/markitdown
- 用途：微软官方：把 PDF / Word / PPT / Excel / HTML / 图片 / 音频（转写）等转成 Markdown，喂 LLM。
- 安装：`pip install 'markitdown[all]'`（按需选 extra）。
- 快速：CLI `markitdown report.pdf > report.md`；或 Python `from markitdown import MarkItDown`→`MarkItDown().convert("x.pdf").text_content`。
- 何时用：RAG / 喂模型前把各种文档统一转 Markdown。
- 注意：可选依赖多（`[all]` 装全部转写能力）；复杂排版 PDF 效果有限，需核对。
