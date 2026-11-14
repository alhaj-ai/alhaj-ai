<div align="center">

# Mohammed Al-Haj | محمد الحاج
### AI & Multi-Agent Systems Engineer
**Sana'a, Yemen (صنعاء، اليمن)**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Mohammed_Al--Haj-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/mohammed-mohammed-al-haj-341ab7369)
[![Email](https://img.shields.io/badge/Email-ai.mohammed.alhaj%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:ai.mohammed.alhaj@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-@alhaj--ai-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/alhaj-ai)
[![X (Twitter)](https://img.shields.io/badge/X-@mod__alhaj-000000?style=flat-square&logo=x&logoColor=white)](https://x.com/mod_alhaj)

<br/>

**Durable Agent Runtimes · Hybrid RAG · Multimodal Document AI · Full-Stack AI Systems**

</div>

---

### Engineering Focus

I am an **AI & Multi-Agent Systems Engineer** based in **Sana'a, Yemen**, focused on building verifiable AI software with deterministic fallbacks, strict automated test suites (`pytest`), GitHub Actions CI, and container-ready deployments:

1. **Durable Agentic Runtimes & Deterministic Automation**: Crash-resilient execution ledgers (`SIGKILL` recovery), discover-once-replay-many browser graphs, and cyclic LangGraph reasoning pipelines.
2. **Multi-Tenant RAG & Local Inference**: Per-user isolated Qdrant vector collections, page-level citation grounding, FAISS + CrossEncoder reranking, and local Ollama/Qwen execution.
3. **Arabic & Yemeni Document Intelligence**: LayoutLMv3 & XLM-RoBERTa models combined with Yemeni National ID (11-digit), telecom prefix, and clinical PII redaction.
4. **Offline-First & Voice Applications**: Real-time WebSocket telephony bridges and SQLite-to-PostgreSQL mobile sync architectures.

---

## 📌 Flagship Repositories (6 Core Systems)

### 1. [Haseen-AI](https://github.com/alhaj-ai/Haseen-AI) — Durable Software Agent Runtime
* **What it does**: Runs multi-step coding agents against an append-only state ledger and SHA-256 checkpoints inside isolated shadow workspaces, with verification gates before patch promotion and idempotency guards preventing duplicate writes on crash resume.
* **Tech Stack**: Python 3.11, FastAPI, Pydantic, Next.js 14 App Router, Docker
* **Verified Demo & CI**: `python -m haseen.cli demo crash` passes cross-platform recovery after forced process termination (`patch applied 1 time(s); duplicate side effects 0`). Verified in GitHub Actions CI.

### 2. [Mutahakkim-AI](https://github.com/alhaj-ai/Mutahakkim-AI) — Discover-Once, Zero-Token Browser Replay
* **What it does**: Discovers browser workflows once using a vision-language agent, compiles them into declarative YAML capability graphs with pre/post DOM verification guards, and replays them deterministically via Playwright with **0 LLM calls**.
* **Tech Stack**: Python 3.11, Playwright, FastAPI, Pydantic, PyYAML, Next.js 14
* **Verified Benchmark & CI**: `python -m mutahakkim.cli replay --capability lookup_savings_balance --headless` completes in **968ms** with **`model_calls: 0`**. Verified in GitHub Actions CI.

### 3. [DocuMind-RAG](https://github.com/alhaj-ai/DocuMind-RAG) — Multi-Tenant RAG & Page-Cited Q&A Engine
* **What it does**: Extracts PDF text into 1,000-character overlapping chunks (`rag/chunker.py`), indexes vectors in per-user isolated Qdrant collections (`rag/vectorstore.py`), enforces exact page-level citations (`rag/citations.py`), and isolates accounts with JWT + Bcrypt (`auth/security.py`).
* **Tech Stack**: FastAPI, Qdrant Vector DB, PostgreSQL/SQLAlchemy, Google Gemini API, Docker
* **Verified Tests & CI**: **`17 / 17` pytest unit & integration tests passing** in GitHub Actions CI.

### 4. [Agentic-DeepResearch](https://github.com/alhaj-ai/Agentic-DeepResearch) — Self-Correcting Research Pipeline
* **What it does**: Orchestrates a cyclic **LangGraph** state machine (`Planner` ➔ `Parallel Searcher` ➔ `Writer` ➔ `Critic`) that decomposes Arabic/English queries, retrieves live web/encyclopedia evidence concurrently, and loops until quality checks pass (up to 3 revisions).
* **Tech Stack**: Python 3.11, LangGraph, FastAPI, Google Gemini, Tavily API, SSE, Docker
* **Verified Tests & CI**: **`12 / 12` pytest tests passing** in GitHub Actions CI.

### 5. [DocuShield-AI](https://github.com/alhaj-ai/DocuShield-AI) — Arabic & Yemeni Document PII Intelligence
* **What it does**: Combines **`LayoutLMv3`** visual document understanding, **`XLM-RoBERTa`** clinical NER, and deterministic Arabic/Yemeni PII anonymization (11-digit National IDs, local telecom prefixes, MRNs) exposed through FastAPI and Streamlit.
* **Tech Stack**: Python, FastAPI, PyTorch, LayoutLMv3, XLM-RoBERTa, Streamlit, Docker
* **Verified Tests & CI**: **`9 / 9` pytest verification tests passing** in GitHub Actions CI.

### 6. [TaskFlow](https://github.com/alhaj-ai/taskflow) — Offline-First Task Ecosystem (Flutter + FastAPI)
* **What it does**: Provides local-first mobile persistence in SQLite (`sqflite`) synchronized to a 24-endpoint FastAPI + PostgreSQL backend with JWT/Bcrypt security and dual-engine task decomposition (Google Gemini API + local rule-based offline fallback).
* **Tech Stack**: Flutter 3.x (Dart), FastAPI, PostgreSQL 15, SQLAlchemy 2.0, SQLite, Docker
* **Verified Tests & CI**: Backend integration, cascade integrity, and cross-user isolation tests + `flutter analyze` passing in GitHub Actions CI, with Android APK releases published (`v1.0.0`).

---

## 🗂️ Additional Verified Engineering Projects

| Repository | Domain & Core Implementation | Verification |
| :--- | :--- | :--- |
| [**Mohawir-AI**](https://github.com/alhaj-ai/Mohawir-AI) | Technical interview simulator orchestrating 5 agents via a real `LangGraph StateGraph`, FAISS RAG & Next.js 14 UI | `4/4` pytest + CI ✅ |
| [**Majles-AI**](https://github.com/alhaj-ai/Majles-AI) | Arabic meeting intelligence with WhisperX diarization, FAISS + CrossEncoder RAG, & local Ollama Q&A | `4/4` pytest + CI ✅ |
| [**Azal-AI**](https://github.com/alhaj-ai/Azal-AI) | Yemeni YER ERP multi-agent assistant with Gemini Vision OCR, anomaly detection & React UI | `2/2` pytest + CI ✅ |
| [**voice-agent-Pharmacy-Assistant**](https://github.com/alhaj-ai/voice-agent-Pharmacy-Assistant) | Bidirectional Twilio Media Streams & Deepgram Voice Agent WebSocket bridge with `Barge-in` | Schema & function CI ✅ |
| [**ai-multi-search-agent**](https://github.com/alhaj-ai/ai-multi-search-agent) | 9-node parallel LangGraph workflow aggregating Google, Bing & Reddit via BrightData SERP APIs | Topology CI ✅ |
| [**mindRouter-agent**](https://github.com/alhaj-ai/mindRouter-agent) | LangGraph structured intent classifier routing full history across therapist & analyst nodes | Routing logic CI ✅ |

---

## 📬 Contact

* **Email**: [ai.mohammed.alhaj@gmail.com](mailto:ai.mohammed.alhaj@gmail.com)
* **LinkedIn**: [linkedin.com/in/mohammed-mohammed-al-haj-341ab7369](https://linkedin.com/in/mohammed-mohammed-al-haj-341ab7369)
* **GitHub**: [@alhaj-ai](https://github.com/alhaj-ai)
* **Location**: Sana'a, Yemen (صنعاء، اليمن)
