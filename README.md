# Awesome Open Foundation Models & AI Platforms

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](http://creativecommons.org/publicdomain/zero/1.0/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://makeapullrequest.com)

A curated list of top **Open Foundation Models and AI Platforms** — covering hosted commercial API inference providers, enterprise neoclouds, and high-performance open-source engines for serving, fine-tuning, and running foundation models on your own infrastructure.

Whether deploying large language models (LLMs), multimodal vision-language models (VLMs), or embedding models in production or experimenting locally on workstations, this guide outlines ecosystem benchmarks, pricing tiers, free quotas, and self-hosted tools.

---

## 📋 Table of Contents

- [📈 Sector Overview & Market Dynamics](#-sector-overview--market-dynamics)
- [🟦 Hosted SaaS AI Inference & Foundation Model Platforms](#-hosted-saas-ai-inference--foundation-model-platforms)
- [🟩 Open-Source Inference & Foundation Model Engines](#-open-source-inference--foundation-model-engines)
- [📊 Comparison at a Glance](#-comparison-at-a-glance)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

---

## 📈 Sector Overview & Market Dynamics

The global foundation model and AI inference market is projected to expand from **~$25B–$110B in 2024–2025 to over $310B–$520B by the 2030s** at an estimated **CAGR of ~18%–31%**, as production enterprise budgets rotate rapidly from capital-intensive model pre-training to operational real-time token inference and agentic workflows.

The sector exhibits a distinct two-layer market structure:
- **Foundational Compute & Proprietary Model Layer (Moderately to Highly Concentrated):** Capital requirements create an oligopolistic tier dominated by hyperscalers, custom-silicon chipmakers, and leading labs (NVIDIA, OpenAI, Anthropic, Google).
- **Inference Serving & Application Orchestration Layer (Highly Fragmented):** Fierce competition thrives across open-weight model serving, serverless API providers, specialized routing gateways, and local runtime software where margins and latency optimizations drive developer choice.

---

## 🟦 Hosted SaaS AI Inference & Foundation Model Platforms

The table below covers prominent hosted platforms and API inference services for open foundation models (e.g., Llama 3, DeepSeek, Mistral, Qwen), sorted in descending order by company scale (valuation / market capitalization / revenue metrics).

| Platform | Company Scale (Valuation / Revenue) | Starting Paid Pricing | Free Tier Limits / Free Trial | Key Capabilities & Highlights |
|:---|:---|:---|:---|:---|
| **[Groq Cloud](https://groq.com/)** | **$20.0B** valuation deal *(~$6.9B Series E / $90M+ rev)* | **$0.075 / 1M input**, **$0.30 / 1M output** tokens (on-demand LPU) | **Free forever plan**: 30 RPM, 1,000 RPD, 8,000 TPM, 200,000 TPD (per organization, no credit card required) | Ultra-fast token throughput using custom Language Processing Unit (LPU) silicon architectures. |
| **[Fireworks AI](https://fireworks.ai/)** | **$17.5B** valuation *(Series D / $305M+ ARR)* | **$0.10 / 1M input**, **$0.20 / 1M output** tokens (serverless) | **$1.00 free starting trial credit** upon sign-up (no credit card required; pay-as-you-go top-up afterwards) | Enterprise serverless model inference optimized for low latency and custom LoRA adapter serving. |
| **[Mistral Platform](https://mistral.ai/)** | **$14.0B** valuation *(~€11.7B Series C / $310M+ ARR)* | **$14.99/month** (Pro plan) or **$0.15 / 1M input**, **$0.45 / 1M output** tokens | **Free Mode forever plan**: Capped at 1 RPS (Request Per Second) across shared organization limits | First-party managed platform, fine-tuning, and APIs for Mistral model families (Large, NeMo, Codestral, Pixtral). |
| **[Hugging Face Hub](https://huggingface.co/)** | **$4.5B** valuation *(Series D / $80M+ ARR)* | **$9.00/month** (PRO tier) or **$0.40/GPU-hour** (Spaces Nvidia T4) | **Free forever tier**: Unlimited public repos, 2 ZeroGPU Spaces (T4), and basic serverless inference credits (~$0.10/month) | Central hub for open-source AI weights, datasets, benchmarks, and interactive Spaces demos. |
| **[Together AI](https://together.ai/)** | **$3.3B** valuation *(Series B / $50M+ ARR)* | **$0.10 / 1M input**, **$0.10 / 1M output** tokens (minimum $15 initial deposit) | **No standing free tier**; $15 initial deposit required to activate console (Startups eligible for $15k–$50k grant credits) | Serverless, Dedicated Endpoints, and Provisioned Throughput with 99% uptime SLAs for open-weight models. |
| **[Anyscale](https://www.anyscale.com/)** | **$1.1B** valuation *(~$100M ARR; acquired by Nscale)* | **$1.00 per cluster-hour** platform fee + raw cloud compute usage | **$100 free trial usage credit** for new accounts (Startup program offers up to $20,000 in compute credits) | Distributed compute platform built on Ray for distributed model training, fine-tuning, and batch inference. |
| **[Replicate](https://replicate.com/)** | **$350M** valuation *(Series B; acquired by Cloudflare)* | **$0.0002 to $0.01 per second** (hardware-based pay-per-second billing) | **$25 free introductory trial credit** upon initial account registration | Simple HTTP API for thousands of open models (text, image, audio) with auto-scaling down to zero. |
| **[Lepton AI (NVIDIA DGX Cloud)](https://www.lepton.ai/)** | **~$200M+** exit *(acquired by NVIDIA for nine figures)* | **$0.80 / 1M input**, **$0.80 / 1M output** tokens (Llama 3.3 70B) | **Free basic developer tier**: Includes complimentary sandbox testing credits and access to serverless testing endpoints | Production AI cloud infrastructure and serverless inference powered by NVIDIA DGX hardware. |
| **[OctoAI](https://octoai.cloud/)** | **$165M** exit *(acquired by NVIDIA)* | **$0.10 / 1M tokens** starting tier (pay-as-you-go inference) | **$10 free usage credit** for new account sign-ups | Turnkey compute and inference platform focused on optimized model execution and latency tuning. |
| **[DeepInfra](https://deepinfra.com/)** | **$136M+** raised *(Series B / $100M+ ARR)* | **$0.05 / 1M input**, **$0.10 / 1M output** tokens or **$0.55/GPU-hour** | **Free tier forever**: Free weekly inference allowance on select Flash models (reset every Monday) with GitHub account | Cost-effective token-based serverless inference and dedicated GPU instances with zero-scale elasticity. |

---

## 🟩 Open-Source Inference & Foundation Model Engines

Self-hosted, community-driven runtimes, servers, and deployment frameworks for running open foundation models on personal machines, on-premise clusters, or private cloud infrastructure.

Sorted in descending order by GitHub stargazers count:

### 1. [Ollama](https://github.com/ollama/ollama) [![GitHub stars](https://img.shields.io/github/stars/ollama/ollama?style=social&color=white)](https://github.com/ollama/ollama/stargazers)
* **Repository:** [ollama/ollama](https://github.com/ollama/ollama)
* **Stack:** Go / C++ (llama.cpp) | **License:** MIT
* **Overview:** The most popular tool for getting started with local models. Offers single-command downloads, automatic GPU hardware acceleration (macOS Metal, CUDA, ROCm), and an OpenAI-compatible REST API.
* **Best for:** Developers and local workstations seeking quick setup and zero configuration for running models like Llama 3, Mistral, and DeepSeek locally.

### 2. [llama.cpp](https://github.com/ggml-org/llama.cpp) [![GitHub stars](https://img.shields.io/github/stars/ggml-org/llama.cpp?style=social&color=white)](https://github.com/ggml-org/llama.cpp/stargazers)
* **Repository:** [ggml-org/llama.cpp](https://github.com/ggml-org/llama.cpp)
* **Stack:** C / C++ | **License:** MIT
* **Overview:** The cornerstone C/C++ inference implementation for LLMs with zero dependencies. Defines the modern GGUF format and provides 2-bit through 8-bit integer quantization for CPU, Apple Silicon, and commodity GPUs.
* **Best for:** Resource-constrained devices, edge deployments, and cross-platform native execution.

### 3. [vLLM](https://github.com/vllm-project/vllm) [![GitHub stars](https://img.shields.io/github/stars/vllm-project/vllm?style=social&color=white)](https://github.com/vllm-project/vllm/stargazers)
* **Repository:** [vllm-project/vllm](https://github.com/vllm-project/vllm)
* **Stack:** Python / CUDA / C++ | **License:** Apache-2.0
* **Overview:** High-throughput, production-grade LLM inference and serving library. Introduced PagedAttention to eliminate memory fragmentation in KV-caches, continuous batching, and chunked prefill.
* **Best for:** High-concurrency enterprise serving on NVIDIA/AMD clusters and powering backend API services.

### 4. [LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory) [![GitHub stars](https://img.shields.io/github/stars/hiyouga/LLaMA-Factory?style=social&color=white)](https://github.com/hiyouga/LLaMA-Factory/stargazers)
* **Repository:** [hiyouga/LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory)
* **Stack:** Python / PyTorch | **License:** Apache-2.0
* **Overview:** Unified, web-UI-enabled fine-tuning and inference framework supporting 100+ foundation models with LoRA, QLoRA, DPO, ORPO, and PPO training pipelines.
* **Best for:** Rapid fine-tuning, alignment, and local serving of foundation models through an intuitive visual interface or CLI.

### 5. [LocalAI](https://github.com/mudler/LocalAI) [![GitHub stars](https://img.shields.io/github/stars/mudler/LocalAI?style=social&color=white)](https://github.com/mudler/LocalAI/stargazers)
* **Repository:** [mudler/LocalAI](https://github.com/mudler/LocalAI)
* **Stack:** Go / C++ / Multi-backend | **License:** MIT
* **Overview:** Drop-in, self-hosted replacement REST API compatible with OpenAI API specifications. Supports multi-modal capabilities including text generation, audio transcription, image generation, and embeddings.
* **Best for:** Self-hosted multi-modal AI infrastructure requiring a single unified endpoint without third-party vendor lock-in.

### 6. [SGLang](https://github.com/sgl-project/sglang) [![GitHub stars](https://img.shields.io/github/stars/sgl-project/sglang?style=social&color=white)](https://github.com/sgl-project/sglang/stargazers)
* **Repository:** [sgl-project/sglang](https://github.com/sgl-project/sglang)
* **Stack:** Python / CUDA / C++ | **License:** Apache-2.0
* **Overview:** Fast execution engine and domain-specific language for LLMs and vision-language models. Features RadixAttention for automatic KV cache reuse across complex multi-turn and constrained decoding flows.
* **Best for:** Structured JSON output, multi-call agent workflows, and ultra-high-performance server-side inference.

### 7. [TensorRT-LLM](https://github.com/NVIDIA/TensorRT-LLM) [![GitHub stars](https://img.shields.io/github/stars/NVIDIA/TensorRT-LLM?style=social&color=white)](https://github.com/NVIDIA/TensorRT-LLM/stargazers)
* **Repository:** [NVIDIA/TensorRT-LLM](https://github.com/NVIDIA/TensorRT-LLM)
* **Stack:** C++ / Python / CUDA | **License:** Apache-2.0
* **Overview:** NVIDIA’s premier library for compiling and maximizing inference performance on NVIDIA GPUs (Hopper, Blackwell, Ada Lovelace), using kernel fusion, in-flight batching, and FP8/FP4 acceleration.
* **Best for:** Maximum hardware saturation and lowest latency on dedicated NVIDIA datacenter infrastructure.

### 8. [Axolotl](https://github.com/axolotl-ai-cloud/axolotl) [![GitHub stars](https://img.shields.io/github/stars/axolotl-ai-cloud/axolotl?style=social&color=white)](https://github.com/axolotl-ai-cloud/axolotl/stargazers)
* **Repository:** [axolotl-ai-cloud/axolotl](https://github.com/axolotl-ai-cloud/axolotl)
* **Stack:** Python / PyTorch | **License:** Apache-2.0
* **Overview:** Streamlined tool for fine-tuning open foundation models (Llama, Mistral, Qwen, Gemma) across multi-GPU environments using FlashAttention, DeepSpeed, and FSDP.
* **Best for:** Post-training, alignment, and parameter-efficient fine-tuning on enterprise compute clusters.

### 9. [Text Generation Inference (TGI)](https://github.com/huggingface/text-generation-inference) [![GitHub stars](https://img.shields.io/github/stars/huggingface/text-generation-inference?style=social&color=white)](https://github.com/huggingface/text-generation-inference/stargazers)
* **Repository:** [huggingface/text-generation-inference](https://github.com/huggingface/text-generation-inference)
* **Stack:** Rust / Python / CUDA | **License:** Apache-2.0
* **Overview:** Hugging Face’s purpose-built toolkit for deploying and serving open LLMs in production. Features Tensor Parallelism, token streaming, watermarking, and optimized tokenizers.
* **Best for:** Turnkey production deployments tightly integrated with the Hugging Face Hub ecosystem.

### 10. [Xinference](https://github.com/xorbitsai/inference) [![GitHub stars](https://img.shields.io/github/stars/xorbitsai/inference?style=social&color=white)](https://github.com/xorbitsai/inference/stargazers)
* **Repository:** [xorbitsai/inference](https://github.com/xorbitsai/inference)
* **Stack:** Python / C++ | **License:** Apache-2.0
* **Overview:** Powerful distributed inference engine supporting LLMs, speech recognition, multimodal models, and rerankers with multi-engine backends (vLLM, llama.cpp, Transformers).
* **Best for:** Cluster orchestration of diverse AI workloads across heterogeneous hardware.

---

## 📊 Comparison at a Glance

| Solution | Deployment Model | Primary Focus | Best For |
|:---|:---|:---|:---|
| **Ollama** | Self-Hosted / Local | Local runtime & developer CLI | Rapid local prototyping on consumer hardware |
| **llama.cpp** | Self-Hosted / Embedded | Quantized CPU & edge inference | Resource-constrained systems and native integration |
| **vLLM** | Self-Hosted / Cloud | Production high-concurrency serving | Enterprise serving clusters requiring peak throughput |
| **SGLang** | Self-Hosted / Cloud | Structured generation & prompt caching | Complex agent workflows with branching prompts |
| **TensorRT-LLM** | Self-Hosted / Datacenter | NVIDIA-optimized kernel execution | Maximum utilization on dedicated NVIDIA GPUs |
| **Groq Cloud** | Hosted SaaS / API | Hardware-accelerated LPU inference | Ultra-low latency requirements and real-time voice/chat |
| **Together AI** | Hosted SaaS / Dedicated | Serverless & dedicated model endpoints | Production SLAs without infrastructure maintenance |
| **Fireworks AI** | Hosted SaaS / API | Low-latency serverless serving | High-speed production model execution |
| **Hugging Face Hub** | Hosted SaaS / Hub | Model repository & demo hosting | Discovery, community benchmarks, and sharing weights |

---

## 🤝 Contributing

Contributions are warmly welcome! If you know of an open-source foundation model platform, inference engine, or serving framework that belongs on this list:

1. Fork this repository.
2. Add your suggested project to the appropriate section with complete metadata.
3. Ensure the project is actively maintained and has open documentation.
4. Submit a descriptive pull request.

---

## 📄 License

This repository is distributed under the [CC0 1.0 Universal (Public Domain)](LICENSE) license. Listed individual platforms and open-source software libraries remain subject to their respective licenses.
