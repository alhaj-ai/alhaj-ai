<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00F7FF,50:3B82F6,100:8B5CF6&height=220&section=header&text=Mohammed%20Al-Haj&fontSize=52&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Senior%20AI%20%26%20Machine%20Learning%20Systems%20Engineer&descFontSize=20&descAlignY=62&descColor=e0f2fe" width="100%" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=24&duration=2500&pause=800&color=00F7FF&center=true&vCenter=true&width=950&lines=Mohammed+Al-Haj+%7C+Senior+AI+Engineer;Autonomous+Multi-Agent+Systems+%7C+LangGraph+2.0+Cycles;Enterprise+Multi-Tenant+RAG+%7C+Qdrant+Vector+DB;Multimodal+Document+AI+%7C+LayoutLMv3+%26+Arabic+PII;Real-Time+Conversational+Voice+AI+%7C+Twilio+%26+Deepgram;Production+Computer+Vision+%7C+YOLOv8+Yemeni+ANPR;Building+Sovereign+%26+Production-Grade+AI+Infrastructure" />
</p>

<p align="center">
  <a href="mailto:ai.mohammed.alhaj@gmail.com"><img src="https://img.shields.io/badge/Email-ai.mohammed.alhaj%40gmail.com-00F7FF?style=for-the-badge&logo=gmail&logoColor=black" /></a>
  <a href="https://linkedin.com/in/mohammed-mohammed-al-haj-341ab7369"><img src="https://img.shields.io/badge/LinkedIn-Mohammed_Al--Haj-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="https://x.com/mod_alhaj"><img src="https://img.shields.io/badge/X-@mod__alhaj-121212?style=for-the-badge&logo=x&logoColor=white" /></a>
  <img src="https://komarev.com/ghpvc/?username=alhaj-ai&color=00F7FF&style=for-the-badge&label=PROFILE+VIEWS" />
</p>

<p align="center">
  📍 <strong>Sana'a, Yemen (صنعاء، اليمن)</strong> · 🌐 <strong>Open to Global Remote Roles & Relocation</strong>
</p>

---

## 📌 ملف المهندس التنفيذي | Executive Engineering Dossier

<div dir="rtl">

> **مهندس ذكاء اصطناعي ونظم تعلم آلي أول (Senior AI & ML Systems Engineer)** متخصص في تصميم وبناء البنى التحتية الذكية عالية الموثوقية للإنتاج. تتركز خبرتي الهندسية في بناء **أنظمة الوكلاء الذاتية متقدمة التنسيق (LangGraph Multi-Agent Orchestration)**، ومنظومات **الاسترجاع المعزز المؤسسية (Enterprise Multi-Tenant RAG)**، ونماذج **معالجة المستندات متعددة الوسائط (Multimodal Document AI)**، مع تعزيز السيادة الرقمية وحماية البيانات الشخصية للمنطقة العربية واليمن (Saudi PDPL & GDPR). ألتزم بأعلى معايير الهندسة البرمجية (TDD، التصميم المعياري، والاستدلال منخفض الكمون).

</div>

I am a **Senior AI & Machine Learning Systems Engineer** dedicated to engineering resilient, scalable intelligence platforms. Rather than building ephemeral proof-of-concepts, my work emphasizes **strict software engineering rigor (TDD, decoupled microservices, multi-tenancy, and deterministic guardrails)** to deploy artificial intelligence safely into production environments.

### 🎯 Key Engineering Pillars & Benchmarks:
1. **Multi-Agent StateGraph Architecture**: Cyclic state machines with **LangGraph**, decomposing queries into parallel retrieval vectors and executing self-correcting reflection loops (38+ passing automated tests across flagship systems).
2. **Enterprise RAG & Tenant Isolation**: High-throughput semantic retrieval using **Qdrant Vector DB**, hybrid indexing, exact page citations (`file.pdf (p.4)`), and multi-tenant collection isolation.
3. **Multimodal Document AI & Sovereign Privacy**: Visual-textual understanding via **LayoutLMv3** (87% accuracy, 0.55s on RTX 5070 Ti) combined with deterministic Yemeni & Arabic PII redaction engines.
4. **Computer Vision & Real-Time Telephony**: Edge-deployed **YOLOv8** (0.94 mAP50 on Yemeni vehicle license plates) and sub-second full-duplex conversational voice telephony via **Twilio** & **Deepgram** WebSockets.

---

## 🏛️ Flagship Engineering Systems

```
┌──────────────────────────────────────────────────────────────────────────────────────────────────┐
│                                   ENGINEERING PILLARS OVERVIEW                                   │
├───────────────────────────────┬───────────────────────────────┬──────────────────────────────────┤
│ 🔬 Multi-Agent Orchestration  │ 🧠 Enterprise RAG Systems    │ 🛡️ Multimodal & Sovereign AI     │
│ • LangGraph Cyclic Loops      │ • Multi-Tenant Qdrant DB      │ • LayoutLMv3 Visual Tokens       │
│ • Reflection & Critic Rubric  │ • Document Page Citations     │ • XLM-RoBERTa Clinical NER       │
│ • Parallel Search Synthesis   │ • Zero-Hallucination Guard    │ • Yemeni / Arabic PII Redaction  │
└───────────────────────────────┴───────────────────────────────┴──────────────────────────────────┘
```

---

### 🏛️ Pillar I: Autonomous Multi-Agent Orchestration & Self-Correction

#### 1. 🔬 [Agentic-DeepResearch](https://github.com/alhaj-ai/Agentic-DeepResearch)
> **Autonomous Multi-Agent Web Research & Report Synthesis Engine**  
> *LangGraph 2.0 • Google Gemini 2.5 Flash • Cyclic Reflection Loops • Bilingual (Arabic & English) • FastAPI • Docker*

- **The Problem**: Single-turn LLMs hallucinate, suffer from context drift, and cannot iteratively refine complex research topics against live web facts.
- **The Solution**: Engineered a directed cyclic state graph in **LangGraph 2.0** orchestrating 4 specialized agents:
  - `Planner Agent` 🧠: Decomposes broad inquiries into 2 focused, complementary sub-queries with native Arabic/English detection.
  - `Searcher Agent` 🔍: Parallel retrieval combining **Tavily API** with a zero-token **Wikipedia & Open Web** fallback engine.
  - `Writer Agent` ✍️: Synthesizes structured, evidence-grounded reports (150–350 words) with source links.
  - `Critic Agent` ⚖️: Enforces a strict 3-dimension rubric (relevance, brevity, citations) and loops back up to 3 revisions until verified.
- **Production Impact**: Complete offline fallback capability; 12/12 automated integration tests passing; interactive glassmorphism UI with real-time agent execution telemetry.

<p align="center">
  <a href="https://github.com/alhaj-ai/Agentic-DeepResearch">
    <img src="https://github-readme-stats-eight-theta.vercel.app/api/pin/?username=alhaj-ai&repo=Agentic-DeepResearch&theme=tokyonight&hide_border=true" />
  </a>
</p>

#### 2. 🧭 [mindRouter — Multi-Agent Intent Routing System](https://github.com/alhaj-ai/mindRouter-agent)
> **Stateful Agentic Graph Architecture for Intent-Driven Workflows**  
> *LangGraph • LangChain • OpenAI GPT-4 • Streamlit • Python Async*

- Architected a cyclical directed graph routing complex incoming user queries between specialized analytical and empathetic persona agents.
- Integrated checkpointed short- and long-term memory persistence across multi-turn user sessions.
- Developed an inspection dashboard in Streamlit displaying real-time agent node activations and confidence distributions.

---

### 🏢 Pillar II: Enterprise Retrieval-Augmented Generation (RAG) & Vector Intelligence

#### 3. 🧠 [DocuMind-RAG](https://github.com/alhaj-ai/DocuMind-RAG)
> **Enterprise Multi-Tenant RAG Platform with Qdrant Vector DB & Document Page Citations**  
> *FastAPI • Qdrant Vector DB • Google Gemini • PostgreSQL/SQLite • JWT Authentication • GDPR Compliance*

- **The Problem**: Standard RAG pipelines lack multi-tenant data boundaries, leak information between users, and cannot provide verifiable page-level audit trails.
- **The Solution**: Built an enterprise-grade RAG platform featuring:
  - **Zero-Trust Multi-Tenancy**: Isolated per-user Qdrant vector collections guaranteeing complete cryptographic and physical data isolation.
  - **Exact Page-Level Citations**: Sliding-window chunking (500 tokens / 100 overlap) maintaining exact document name and page number offsets (`audit_2026.pdf (p.4)`).
  - **Hybrid Routing**: Context-grounded answering for document queries with graceful fallback to general assistant mode using `<no_sources>` markers.
  - **Resilient Infrastructure**: Automatic exponential backoff for Gemini rate limits (429) and request tracing via `X-Request-ID`.
- **Production Impact**: 17/17 automated PyTest unit/integration tests passing in <8 seconds; full GDPR account/collection wipe endpoints.

<p align="center">
  <a href="https://github.com/alhaj-ai/DocuMind-RAG">
    <img src="https://github-readme-stats-eight-theta.vercel.app/api/pin/?username=alhaj-ai&repo=DocuMind-RAG&theme=tokyonight&hide_border=true" />
  </a>
</p>

#### 4. 🏢 [Local RAG Workstation](https://github.com/alhaj-ai/local-rag-workstation)
> **Zero-Cloud-Egress Private RAG & Semantic Retrieval Platform**  
> *Next.js 15 • FastAPI • Qdrant Vector DB • PostgreSQL • Local LLMs (LM Studio / Ollama) • Docker*

- Engineered an on-premise, air-gapped document intelligence platform ensuring zero confidential data leaves the enterprise perimeter.
- Implemented hybrid dense-sparse vector indexing with Qdrant, supporting local offline inference backends.

---

### 🛡️ Pillar III: Multimodal Document AI & Sovereign Privacy Compliance

#### 5. 🛡️ [DocuShield-AI](https://github.com/alhaj-ai/DocuShield-AI)
> **Multilingual, Yemeni & Arabic Privacy-Preserving Document Intelligence Platform**  
> *LayoutLMv3 • XLM-RoBERTa • PyTorch (CUDA 13.4) • FastAPI • Streamlit • Yemeni & Arabic PII Engine • Saudi PDPL & GDPR*

- **The Problem**: Visual document analysis in healthcare and government domains exposes sensitive personal records (PII) to unauthorized models while failing on non-Latin scripts.
- **The Solution**: Engineered an end-to-end multimodal intelligence platform:
  - **Visual-Textual Layout Modeling**: Fine-tuned `microsoft/layoutlmv3-base` on scanned clinical documents (13 semantic token classes, **87.0% field accuracy**, 0.55s per document on RTX 5070 Ti).
  - **Cross-Lingual Clinical NER**: Multilingual disease and entity extraction across English and French using `xlm-roberta-base` (F1 0.77 EN / 0.52 FR).
  - **Sovereign Arabic PII Engine**: Deterministic regex & contextual heuristics for Yemeni National IDs (11-digit unified national ID: الرقم الوطني الموحد), Yemeni telecom networks (Yemen Mobile 77/78, YOU 73, Sabafon 71, Y 70), Saudi National IDs (`1X/2X`), GCC phones, and Arabic patient names.
  - **Tri-Mode Redaction**: Strict (`[محجوب]`), Typed (`[رقم_وطني_يمني]`), and Synthetic Surrogate replacement via an asynchronous **FastAPI** REST microservice and **Streamlit** dashboard.
- **Production Impact**: 9/9 automated tests passing; verified compliance with Saudi PDPL and international GDPR standards.

<p align="center">
  <a href="https://github.com/alhaj-ai/DocuShield-AI">
    <img src="https://github-readme-stats-eight-theta.vercel.app/api/pin/?username=alhaj-ai&repo=DocuShield-AI&theme=tokyonight&hide_border=true" />
  </a>
</p>

---

### 🚗 Pillar IV: Computer Vision, Edge AI & Real-Time Telephony

#### 6. 🚗 [Yemen License Plate Recognition System](https://github.com/alhaj-ai/yemen-licenser-plate-recognition-system)
> **Production Deep Learning & OCR Pipeline for Yemeni Vehicle Plate Identification**  
> *YOLOv8 • EasyOCR • Django REST Framework • React • OpenCV • PyTorch (CUDA)*

- Fine-tuned **YOLOv8** on customized high-variance regional datasets, achieving **0.94 mAP50** on Yemeni private, commercial, and governmental vehicle plates.
- Engineered specialized OCR post-processing heuristics resolving ambiguous Arabic typography, provincial badges, and degradation artifacts.
- Packaged as a containerized **Django REST** microservice with an interactive React visualization dashboard for real-time video stream inspection.

<p align="center">
  <a href="https://github.com/alhaj-ai/yemen-licenser-plate-recognition-system">
    <img src="https://github-readme-stats-eight-theta.vercel.app/api/pin/?username=alhaj-ai&repo=yemen-licenser-plate-recognition-system&theme=tokyonight&hide_border=true" />
  </a>
</p>

#### 7. 🎙️ [Voice Agent — Pharmacy Assistant](https://github.com/alhaj-ai/voice-agent-Pharmacy-Assistant)
> **Real-Time Telephony Conversational AI Assistant**  
> *Twilio Media Streams • Deepgram Voice Agent API • Full-Duplex WebSockets • Python AsyncIO • Function Calling*

- Architected a bidirectional full-duplex conversational voice pipeline bridging raw **Twilio Media Streams** with **Deepgram Voice Agent API** over WebSockets.
- Achieved sub-second voice-to-voice response latency for medical triage, medicine availability lookups, and automated order placements.
- Implemented deterministic tool calling handlers with real-time payload synchronization and conversation state management.

<p align="center">
  <a href="https://github.com/alhaj-ai/voice-agent-Pharmacy-Assistant">
    <img src="https://github-readme-stats-eight-theta.vercel.app/api/pin/?username=alhaj-ai&repo=voice-agent-Pharmacy-Assistant&theme=tokyonight&hide_border=true" />
  </a>
</p>

#### 8. 📱 [Taskflow — Intelligent Offline-First Mobile Platform](https://github.com/alhaj-ai/taskflow)
> **Full-Stack Intelligent Productivity & Task Automation System**  
> *Flutter • FastAPI • Google Gemini AI • PostgreSQL • Redis • Docker • Arabic RTL Support*

- Engineered a cross-platform mobile workspace operating under strict **Offline-First** constraints with conflict-free background data synchronization.
- Embedded Gemini AI to provide autonomous task scheduling, effort estimation, and intelligent priority clustering with full Arabic RTL support.

---

## 🛠️ Senior Technical Competencies & Toolchain

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,pytorch,tensorflow,opencv,fastapi,django,flutter,react,nextjs,postgres,mongodb,redis,docker,git,linux&perRow=15" />
</p>

| Engineering Discipline | Technologies, Frameworks & Tooling |
| :--- | :--- |
| **LLMs, Multi-Agent & RAG** | **LangGraph 2.0**, **LangChain**, **Qdrant Vector DB**, **ChromaDB**, Google Gemini (2.5 Flash, 1.5 Pro), OpenAI GPT-4o, Local LLMs (Ollama / vLLM / LM Studio), Prompt Engineering, DeepEval |
| **Multimodal & Computer Vision** | **LayoutLMv3**, **XLM-RoBERTa**, **YOLOv8**, OpenCV, EasyOCR, Tesseract, HuggingFace Transformers, PyTorch 2.x, CUDA Acceleration |
| **Real-Time & Telephony Voice AI** | **Twilio Media Streams**, **Deepgram Voice Agent API**, Full-Duplex WebSockets, Python AsyncIO, Function Calling Handlers |
| **Backend & Microservices** | **FastAPI**, **Django REST Framework**, Uvicorn, RESTful API Architecture, Pydantic V2, JWT, OAuth2, Rate Limiting |
| **Data Engineering & Storage** | **PostgreSQL**, **Qdrant**, **MongoDB**, **Redis**, Apache PySpark, SQLite (WAL Mode), Schema Validation, Distributed ETL |
| **DevOps & Verification (TDD)** | **Docker**, **Docker Compose**, Linux / Bash, **PyTest (TDD - 100% Passing)**, CI/CD, Git / GitHub |

---

## 💻 Local AI Infrastructure & Engineering Profile

- **Compute Hardware**:
  - **GPU**: NVIDIA GeForce RTX 5070 Ti Laptop GPU (12 GB GDDR7 VRAM, CUDA 13.4, PyTorch `cuda:0` acceleration).
  - **CPU**: AMD Ryzen 9 8940HX (16 Cores, 32 Threads).
  - **RAM**: 16 GB High-Speed System RAM.
- **Execution Standards**: Local accelerated inference, offline test suites, zero-hallucination pipelines, and verifiable physical exit codes.

---

## 📊 Live GitHub Engineering Metrics

<p align="center">
  <img src="https://github-readme-stats-eight-theta.vercel.app/api?username=alhaj-ai&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true" height="175" />
  <img src="https://github-readme-stats-eight-theta.vercel.app/api/top-langs/?username=alhaj-ai&layout=compact&theme=tokyonight&hide_border=true" height="175" />
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com/?user=alhaj-ai&theme=tokyonight&hide_border=true" height="175" />
</p>

---

## 💼 Open to High-Impact Opportunities

I am actively evaluating **Senior AI Engineer**, **LLM / Multi-Agent Systems Architect**, and **Production RAG Specialist** roles (Worldwide Remote / Relocation).

| Direct Channel | Details |
| :--- | :--- |
| **📧 Direct Email** | [ai.mohammed.alhaj@gmail.com](mailto:ai.mohammed.alhaj@gmail.com) |
| **💼 LinkedIn** | [linkedin.com/in/mohammed-mohammed-al-haj-341ab7369](https://linkedin.com/in/mohammed-mohammed-al-haj-341ab7369) |
| **🐙 GitHub** | [@alhaj-ai](https://github.com/alhaj-ai) |
| **🐦 X (Twitter)** | [@mod_alhaj](https://x.com/mod_alhaj) |
| **📍 Location** | Sana'a, Yemen (صنعاء، اليمن) · Available for Worldwide Remote & Relocation |

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:8B5CF6,50:3B82F6,100:00F7FF&height=100&section=footer" />
</p>
