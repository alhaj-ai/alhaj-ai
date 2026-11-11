<div align="center">

# Mohammed Al-Haj | محمد الحاج
### AI & Machine Learning Systems Engineer
**Sana'a, Yemen (صنعاء، اليمن)**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Mohammed_Al--Haj-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/mohammed-mohammed-al-haj-341ab7369)
[![Email](https://img.shields.io/badge/Email-ai.mohammed.alhaj%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:ai.mohammed.alhaj@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-@alhaj--ai-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/alhaj-ai)
[![X](https://img.shields.io/badge/X-@mod__alhaj-000000?style=flat-square&logo=x&logoColor=white)](https://x.com/mod_alhaj)

</div>

---

### مرحبا بك! أنا محمد 👋

أنا مهندس ذكاء اصطناعي (AI Engineer) من اليمن - صنعاء. شغفي الأساسي هو بناء أنظمة ذكاء اصطناعي عملية وإنتاجية تعمل بكفاءة على أرض الواقع، بعيداً عن مجرد النماذج التجريبية البسيطة. 

أركز في عملي اليومي على تصميم **أنظمة الوكلاء الذاتية (Multi-Agent Systems)** باستخدام LangGraph، وهندسة **منظومات الاسترجاع المعزز المؤسسية (Enterprise RAG)** مع عزل تام للبيانات، وبناء **نماذج معالجة المستندات متعددة الوسائط (Document AI)** مع حماية سيادية للبيانات والخصوصية اليمنية والعربية.

---

### Hi there! I'm Mohammed 👋

I am an AI Engineer based in **Sana'a, Yemen**, passionate about building reliable, production-grade AI software. I focus on bridging modern research into dependable systems that solve concrete problems:

- **Multi-Agent Orchestration**: Designing stateful agent workflows with **LangGraph** where specialized agents plan, retrieve, write, and critically review their own output before delivering answers.
- **Enterprise RAG & Semantic Retrieval**: Architecting multi-tenant document systems using **Qdrant Vector DB** and **FastAPI**, with strict data isolation, zero-hallucination guardrails, and page-level source citations.
- **Multimodal Document AI & Sovereign Privacy**: Visual document parsing with **LayoutLMv3**, cross-lingual clinical NER with **XLM-RoBERTa**, and building deterministic PII redaction engines tailored for Yemeni and Arabic identity formats.
- **Computer Vision & Real-Time Audio**: Deploying custom **YOLOv8** models for localized detection challenges (like Yemeni vehicle plates) and building sub-second voice telephony pipelines over WebSockets.

---

## 🛠️ Flagship Projects

Here is a curated look at the core open-source systems I have engineered:

### 1. 🛡️ [DocuShield-AI](https://github.com/alhaj-ai/DocuShield-AI)
**Multimodal, Yemeni & Arabic Privacy-Preserving Document Intelligence**  
*LayoutLMv3 • XLM-RoBERTa • PyTorch (CUDA) • FastAPI • Streamlit • Yemeni PII Engine*

- **The Problem**: Medical and administrative visual documents contain sensitive patient data that cannot be sent to public third-party APIs, and standard OCR struggles with complex Arabic layouts.
- **What I Built**: An on-premise multimodal platform combining fine-tuned **LayoutLMv3** (87% layout accuracy on RTX 5070 Ti) and **XLM-RoBERTa** for clinical entity extraction.
- **Yemeni Privacy Engine**: Built deterministic detection for the Yemeni National ID (11 digits: الرقم الوطني الموحد), Yemeni mobile networks (Yemen Mobile 77/78, YOU 73, Sabafon 71, Y 70), and Sana'a clinical MRNs with instant redaction before data leaves the system.
- **Verification**: 9/9 automated unit tests passing, served via FastAPI and a real-time Streamlit dashboard.

---

### 2. 🔬 [Agentic-DeepResearch](https://github.com/alhaj-ai/Agentic-DeepResearch)
**Autonomous Multi-Agent Web Research & Report Engine with Self-Correction**  
*LangGraph 2.0 • Google Gemini • Cyclic Critic Feedback • Bilingual (Arabic & English) • FastAPI*

- **The Problem**: Single-prompt LLMs easily drift off-topic, lack factual verification, and hallucinate when researching broad subjects.
- **What I Built**: A directed cyclic graph orchestrating 4 focused agents:
  1. **Planner Agent**: Breaks inquiries into focused sub-questions (with native Arabic/English detection).
  2. **Searcher Agent**: Parallel web search with Tavily and a built-in zero-key open encyclopedic fallback.
  3. **Writer Agent**: Synthesizes structured, evidence-backed reports (150–350 words).
  4. **Critic Agent**: Evaluates relevance, conciseness, and citations, looping back up to 3 revisions if quality is insufficient.
- **Verification**: 12/12 automated integration tests passing, with a dark-mode web dashboard showing live agent execution.

---

### 3. 🧠 [DocuMind-RAG](https://github.com/alhaj-ai/DocuMind-RAG)
**Enterprise Multi-Tenant RAG Engine with Qdrant & Page-Level Citations**  
*FastAPI • Qdrant Vector DB • Google Gemini • SQLite / PostgreSQL • JWT Auth • GDPR*

- **The Problem**: Most tutorial RAG implementations mix all user documents together, lack authentication, and give answers without auditable page citations.
- **What I Built**: A full-stack, multi-tenant RAG platform where each user has an isolated Qdrant vector collection. Features sliding-window chunking that preserves document and page numbers (`report.pdf (p.4)`), hybrid query routing, and full user data deletion endpoints.
- **Verification**: 17/17 automated tests running offline in <8 seconds with Docker Compose orchestration.

---

### 4. 🚗 [Yemen License Plate Recognition System](https://github.com/alhaj-ai/yemen-licenser-plate-recognition-system)
**End-to-End YOLOv8 & OCR Pipeline for Yemeni Vehicle Plates**  
*YOLOv8 • EasyOCR • Django REST Framework • React • OpenCV • PyTorch*

- Trained a custom **YOLOv8** detector on Yemeni private, commercial, and taxi license plates, reaching **0.94 mAP50**.
- Built specialized OCR post-processing heuristics to handle non-standard Arabic fonts, provincial badges, and severe environmental noise.
- Deployed as a Django REST microservice with an interactive React interface for real-time video stream testing.

---

### 5. 🎙️ [Voice Agent — Pharmacy Assistant](https://github.com/alhaj-ai/voice-agent-Pharmacy-Assistant)
**Real-Time Telephony Conversational Voice Agent**  
*Twilio Media Streams • Deepgram Voice Agent API • WebSockets • Python AsyncIO*

- Engineered a full-duplex conversational audio pipeline connecting raw Twilio telephone streams to Deepgram Voice API over WebSockets.
- Delivers sub-second voice-to-voice response times for prescription inquiries and pharmacy triage, with real-time tool calling handlers.

---

### 6. 🧭 [mindRouter — Multi-Agent Intent Routing System](https://github.com/alhaj-ai/mindRouter-agent)
**Stateful Agentic Graph Architecture for Intent-Driven Workflows**  
*LangGraph • LangChain • OpenAI GPT-4 • Streamlit • Python Async*

- Built a cyclical graph in LangGraph that analyzes incoming user intent and routes queries to dedicated analytical or empathetic persona agents.
- Maintained conversational context across multi-turn interactions using checkpointed short/long-term memory.

---

## 💻 Tech Stack & Tools

- **Agentic AI & RAG**: LangGraph, LangChain, Qdrant Vector DB, ChromaDB, Google Gemini, OpenAI, Ollama, DeepEval.
- **Deep Learning & Vision**: PyTorch, HuggingFace Transformers, LayoutLMv3, XLM-RoBERTa, YOLOv8, OpenCV, Tesseract OCR.
- **Backend & APIs**: Python, FastAPI, Uvicorn, Django REST Framework, Pydantic V2, WebSockets, JWT.
- **Databases & Data**: PostgreSQL, SQLite (WAL mode), Qdrant, MongoDB, Redis, Apache PySpark.
- **DevOps & Verification**: Docker, Docker Compose, Linux, Git, GitHub, PyTest (TDD).

---

## ⚡ Local AI Infrastructure

I develop and test local inference workflows on a dedicated workstation:
- **GPU**: NVIDIA GeForce RTX 5070 Ti Laptop GPU (12 GB GDDR7 VRAM, CUDA 13.4, PyTorch `cuda:0`).
- **CPU**: AMD Ryzen 9 8940HX (16 Cores, 32 Threads).
- **RAM**: 16 GB High-Performance System RAM.

---

## 📬 Let's Connect

I am open to **AI Engineer**, **Multi-Agent Systems**, and **Production RAG** opportunities (Remote Worldwide / Relocation).

- **Email**: [ai.mohammed.alhaj@gmail.com](mailto:ai.mohammed.alhaj@gmail.com)
- **LinkedIn**: [linkedin.com/in/mohammed-mohammed-al-haj-341ab7369](https://linkedin.com/in/mohammed-mohammed-al-haj-341ab7369)
- **GitHub**: [@alhaj-ai](https://github.com/alhaj-ai)
- **Location**: Sana'a, Yemen (صنعاء، اليمن)
