# Awesome-Open-Foundation-Models-AI-Platforms

# Awesome Open Foundation Models & AI Platforms

> A curated list of top Open Foundation Models and AI Platforms — both SaaS/Hosted commercial inference and model-hosting services and open-source alternatives for running, serving, and experimenting with foundation models on your own infrastructure.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Hugging Face Hub](#hugging-face-hub)
  - [Replicate](#replicate)
  - [Together AI](#together-ai)
  - [Fireworks AI](#fireworks-ai)
  - [Groq Cloud](#groq-cloud)
  - [DeepInfra](#deepinfra)
  - [Mistral Platform](#mistral-platform)
  - [Lepton AI (NVIDIA DGX Cloud)](#lepton-ai-nvidia-dgx-cloud)
  - [Anyscale](#anyscale)
  - [OctoAI](#octoai)
- [Open-Source Software](#-open-source-software)
  - [vLLM](#vllm)
  - [Ollama](#ollama)
  - [LocalAI](#localai)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted model hubs and inference platforms. These are not open-source but are included as reference points for feature comparison.

### Hugging Face Hub
**Type:** Central model, dataset, and demo hosting platform
Hugging Face Hub is the default destination for open foundation models, hosting models, datasets, and Spaces (demo apps) with Git-based collaboration and community discovery [citation:1]. Paid plans include PRO at **$9/month**, Team at **$20/user/month**, and Enterprise at **$50/user/month**, with storage priced per TB (public repos $12/TB/mo, private $18/TB/mo, with volume discounts). Spaces hardware ranges from a free CPU Basic tier to GPU instances starting at **$0.40/hour** for a small Nvidia T4 [citation:1].  
**Best for:** Teams wanting the largest catalog of open models and datasets with community tooling, accepting that compute for hosted demos is billed separately.

### Replicate
**Type:** Pay-per-second model inference API
Replicate runs thousands of open-source models (Llama, Stable Diffusion, Whisper, and custom models) via a simple API, handling GPU provisioning and scaling automatically [citation:2][citation:13]. Pricing is **pay-per-second** based on hardware requirements (roughly $0.0002–$0.01/sec), with no subscription and a **$25 free credit** for new accounts [citation:2]. **Trade-off:** No free tier for ongoing use, and costs can accumulate for sustained workloads [citation:13].  
**Best for:** Developers wanting on-demand access to a broad model catalog without managing any infrastructure.

### Together AI
**Type:** Serverless and dedicated inference platform
Together AI offers serverless inference (best-effort) alongside **Dedicated Endpoints** (reserved GPUs billed per-minute) and **Provisioned Throughput** (token-based reserved capacity with a 99% uptime SLA) [citation:3][citation:14]. Dedicated hardware includes H100 at **$5.40/hour**, H200 at **$6.60/hour**, and B200 at **$9.00/hour** [citation:3]. Provisioned Throughput is priced at **$0.05 per PTU per minute**, with full utilization yielding roughly $0.36/M input and $2.16/M output tokens on MiniMax M3 [citation:14].  
**Best for:** Teams needing predictable production capacity for open models with an SLA, accepting the complexity of choosing between serverless, dedicated, and provisioned form factors.

### Fireworks AI
**Type:** Serverless inference platform
Fireworks AI provides serverless inference for open models with a focus on speed and production reliability [citation:4]. It competes directly with Together AI and Replicate on throughput and latency for open-weight models.  
**Best for:** Teams wanting fast serverless inference for popular open models without reserved capacity commitments.

### Groq Cloud
**Type:** Ultra-low-latency inference on custom LPU hardware
Groq Cloud runs open models on its custom Language Processing Unit (LPU) hardware, with published speeds and per-token pricing. Production model pricing includes **$0.15 input / $0.60 output per 1M tokens** for one model and **$0.075 input / $0.30 output** for a smaller model, with rate limits on the Developer plan [citation:7].  
**Best for:** Latency-sensitive applications where token generation speed is the primary constraint.

### DeepInfra
**Type:** Token-based serverless and GPU-hour private inference
DeepInfra offers shared serverless inference (pay per token) and **Private Models** on dedicated GPUs with autoscaling from zero [citation:8]. GPU options span A100 through B300 (Blackwell Ultra). Private deployments bill **per GPU-hour** regardless of traffic, with a warning that an unattended 2-GPU deployment over a weekend costs roughly **$256** [citation:8].  
**Best for:** Teams needing custom weights or compliance isolation, accepting the cost discipline required for always-on GPU deployments.

### Mistral Platform
**Type:** First-party platform for Mistral models
Mistral's platform provides access to its own model family (Mistral Medium, Mistral Large, OCR, Voxtral) with a free tier and paid plans. **Pro is $14.99/month**, **Team is $24.99/user/month**, and **Company is custom** [citation:9]. API pricing is per million tokens (e.g., Mistral Large at **$2/M input, $6/M output**), with a **50% batch discount** [citation:9].  
**Best for:** Teams standardized on Mistral models wanting a first-party platform rather than a third-party aggregator.

### Lepton AI (NVIDIA DGX Cloud)
**Type:** Serverless inference on NVIDIA DGX Cloud
Lepton AI was acquired by NVIDIA and rebranded as **NVIDIA DGX Cloud Lepton** in 2026, running serverless inference on DGX infrastructure with an OpenAI-compatible API [citation:10]. The model catalog is currently small (one production model listed), with pricing at **$0.80/M input tokens** for Llama 3.3 70B [citation:10].  
**Best for:** Enterprises wanting NVIDIA-backed infrastructure and SLAs for serverless open-model inference, accepting a narrower model selection.

### Anyscale
**Type:** Managed Ray platform for distributed AI workloads
Anyscale is the company behind **Ray**, the open-source distributed computing framework used by OpenAI, Uber, and Spotify [citation:6]. Its platform provides managed Ray clusters for distributed training, batch inference, and model serving. It is described as **super complex and technical**, with pay-as-you-go pricing and no monthly fees [citation:6].  
**Best for:** Teams needing to scale AI workloads across many GPUs with Ray, accepting significant technical complexity.

### OctoAI
**Type:** Inference platform with free starting credit
OctoAI offers pay-for-what-you-use inference with **$10 of free credit** for new signups, positioning itself on low latency and cost savings from its optimization expertise [citation:5].  
**Best for:** Teams wanting to evaluate an inference provider with minimal upfront commitment.

---

## 🟩 Open-Source Software

Self-hosted, community-driven tools for running and serving foundation models on your own infrastructure.

### vLLM
**Stack:** Python / CUDA | **License:** Apache-2.0
vLLM is the leading open-source **high-throughput LLM inference and serving engine**, listed among the healthiest LLM API gateway and local inference projects with a Linux Foundation health score of **79/100** [citation:11]. It is the de facto standard for self-hosted production inference, powering many commercial inference platforms behind the scenes.  
**Best for:** Teams wanting maximum throughput and efficient GPU utilization for self-hosted LLM serving, accepting the operational overhead of managing GPU infrastructure.

### Ollama
**Stack:** Go / llama.cpp | **License:** MIT
Ollama provides the simplest path to running LLMs locally, with a single-binary installation, a model library, and an OpenAI-compatible API. It is listed with a Linux Foundation health score of **72/100** and **21,737** activity metric [citation:11]. It is the default choice for local development and experimentation with open models.  
**Best for:** Developers wanting to run models locally on laptops or workstations with minimal setup, accepting lower throughput than production serving engines.

### LocalAI
**Stack:** Go / llama.cpp / multiple backends | **License:** MIT
LocalAI is an open-source **OpenAI-compatible API** that runs models locally across multiple backends, supporting text generation, image generation, audio transcription, and embeddings. It is listed with a health score of **65/100** and **2,167** activity metric [citation:11].  
**Best for:** Teams wanting a unified local API surface across multiple model types (text, image, audio) without cloud dependencies.

---

## 📊 Comparison at a Glance

| Software | License | Type | Pricing Model | Self-Hosted | Best For |
|----------|---------|------|---------------|-------------|----------|
| **Hugging Face Hub** | Proprietary | Model hub + Spaces | Per-user + per-TB + GPU-hour | ❌ | Model discovery + demo hosting |
| **Replicate** | Proprietary | Inference API | Pay-per-second | ❌ | Broad catalog, no infra |
| **Together AI** | Proprietary | Inference platform | Serverless / dedicated / PTU | ❌ | Predictable production capacity |
| **Groq Cloud** | Proprietary | Inference (LPU) | Per-token | ❌ | Ultra-low latency |
| **DeepInfra** | Proprietary | Inference platform | Per-token / GPU-hour | ❌ | Custom weights + compliance |
| **Mistral Platform** | Proprietary | First-party models | Per-token + subscription | ❌ | Mistral model users |
| **vLLM** | Apache-2.0 | Inference engine | N/A (self-hosted) | ✅ | High-throughput self-hosting |
| **Ollama** | MIT | Local inference | N/A (self-hosted) | ✅ | Local development |
| **LocalAI** | MIT | Local OpenAI API | N/A (self-hosted) | ✅ | Multi-modal local API |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source foundation model platform or inference tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source.

**Note on the ecosystem:** The open-model inference landscape splits between **managed platforms** that abstract GPU management (Hugging Face Hub for discovery and hosting, Replicate for on-demand inference, Together AI for production SLAs, Groq for latency) and **self-hosted engines** that give full control (vLLM for high-throughput serving, Ollama for local development, LocalAI for multi-modal local APIs). **Hugging Face Hub** is the gravitational center for open models and datasets [citation:1]. **Together AI** offers the most complete range of production form factors (serverless, dedicated, provisioned throughput with SLA) [citation:3][citation:14]. **vLLM** is the strongest self-hosted option for teams with GPU infrastructure, while **Ollama** is the best starting point for local experimentation [citation:11].

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
