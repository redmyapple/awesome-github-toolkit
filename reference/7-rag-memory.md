# RAG / 记忆层

## RAGFlow — https://github.com/infiniflow/ragflow
- 用途：深度文档理解的 RAG 引擎，擅长复杂 PDF / 表格，开箱即用。
- 安装（自托管）：clone 后按其 docker 目录 `docker compose up -d`（组件多，建议 ≥16GB 内存，有 GPU 更佳）。
- 何时用：大量非结构化文档、复杂版式要高质量问答，不想自己拼 RAG。
- 注意：资源占用高；先看官方部署文档（CPU 版与 GPU 版有差异）。

## mem0 — https://github.com/mem0ai/mem0
- 用途：AI 记忆层：给 Agent 跨会话记住用户偏好 / 事实。
- 安装：`pip install mem0ai`（托管版用云 API；OSS 版自建向量库）。
- 快速：`from mem0 import Memory`→`m=Memory()`→`m.add("用户喜欢简洁回答", user_id="u1")`→`m.search("回答风格", user_id="u1")`。
- 何时用：给聊天 / Agent 产品加"长期记忆 / 个性化"。
- 注意：OSS 版需配向量库与 LLM；注意隐私与记忆内容管理。

## supermemory — https://github.com/supermemoryai/supermemory
- 用途：通用"超级记忆"工具 / API，把任意内容存成可检索记忆，供 AI / 应用调用。
- 安装 / 使用：JS/TS `npm install supermemory`（也有 API / 托管，具体见 README）。
- 何时用：想快速给应用接一层记忆 / 检索，不想自建向量库。
- 注意：具体 API 以仓库 README 为准；敏感数据先评估其托管与隐私策略。
