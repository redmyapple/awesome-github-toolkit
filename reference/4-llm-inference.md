# LLM 推理 / 本地大模型

## ollama — https://github.com/ollama/ollama
- 用途：一行命令在本地拉取并运行开源大模型，内置 OpenAI 兼容 API。
- 安装：Linux/macOS `curl -fsSL https://ollama.com/install.sh | sh`；Windows 用官方安装包；或 `brew install ollama`。
- 快速：`ollama run llama3.2`；服务默认 `http://localhost:11434`，OpenAI 兼容端点 `/v1/chat/completions`。
- 何时用：想最简单地在本地 / 内网跑模型、做原型。
- 注意：模型默认存 `~/.ollama/models`，可用环境变量 `OLLAMA_MODELS` 改到 D 盘省 C 盘空间。

## llama.cpp — https://github.com/ggerganov/llama.cpp
- 用途：C/C++ 推理引擎 + GGUF 格式，CPU / 低显存可跑，量化友好。
- 安装：`git clone https://github.com/ggerganov/llama.cpp && cd llama.cpp && make`（或 CMake）；`brew install llama.cpp`。
- 快速：拿 GGUF 模型后 `./llama-cli -m model.gguf -p "你好"`；另提供 `llama-server`（OpenAI 兼容）。
- 何时用：无 GPU / 边缘设备 / 需要极致量化控制；也是很多本地 GUI 的底座。
- 注意：需 GGUF 格式模型（HuggingFace 下载，或用 ollama 模型转换）。

## vLLM — https://github.com/vllm-project/vllm
- 用途：高吞吐推理服务引擎（连续批处理 + PagedAttention）。
- 安装：`pip install vllm`（需 NVIDIA GPU + 合适 CUDA）。
- 快速：OpenAI 兼容服务 `python -m vllm.entrypoints.openai.api_server --model <hf-model>`；新版可 `vllm serve <model>`。
- 何时用：生产环境给多人 / 高并发提供模型 API。
- 注意：显存是硬门槛；版本对 CUDA / 驱动有要求，长上下文更吃显存。

## transformers — https://github.com/huggingface/transformers
- 用途：HuggingFace 模型 / 训练 / pipeline 标准库。
- 安装：`pip install transformers`（按需 `torch` / `accelerate` / `datasets`）。
- 快速：`from transformers import pipeline`→`pipeline("text-generation", model="gpt2")("hello")`。
- 何时用：微调、跑论文模型、自定义训练。
- 注意：大模型微调建议配合 `accelerate` / `peft`(LoRA) / `bitsandbytes`。

## nanoGPT — https://github.com/karpathy/nanoGPT
- 用途：Karpathy 的极简 GPT 训练代码（约千行），教学向。
- 安装：`git clone` 后 `pip install torch numpy datasets transformers tiktoken wandb`。
- 快速：`python data/shakespeare_char/prepare.py`→`python train.py`→`python sample.py`。
- 何时用：学习 Transformer / GPT 训练细节、从零理解预训练。
- 注意：单机教学规模；要训大模型需改造成多卡 / 分布式。

## deepseek-ai — https://github.com/deepseek-ai
- 用途：DeepSeek 官方组织：模型权重 + 高性能内核（FlashMLA、DeepGEMM、DeepEP、DeepJIT 等）+ DeepSeek Harness（TS 插件平台）。
- 使用：权重去 HuggingFace / ModelScope 下载；内核库按各仓库 README 编译；推理可复用 vLLM / SGLang。
- 何时用：用 DeepSeek-V/R 系列模型，或需要其高性能注意力 / GEMM 内核。
- 注意：这是"组织页"不是单一可运行仓库，按需进具体仓库；遵守各模型 License。
