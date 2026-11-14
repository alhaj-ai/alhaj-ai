# Mohammed Al-Haj

**AI Engineer** — LLMs · Agent Harnesses · Model Fine-Tuning · Hybrid RAG · Computer Vision · Backend Systems

[GitHub](https://github.com/alhaj-ai) · [LinkedIn](https://linkedin.com/in/mohammed-mohammed-al-haj-341ab7369) · [X](https://x.com/mod_alhaj) · [ai.mohammed.alhaj@gmail.com](mailto:ai.mohammed.alhaj@gmail.com)

---

## About

I design, fine-tune, and ship production AI systems, backed by hands-on experience in LLM engineering, agent harnesses, model adaptation, hybrid RAG, and computer vision.

When engineering language and multi-agent workflows, I work from the model and retrieval layers up: fine-tuning Transformer and deep learning architectures with PyTorch and Hugging Face, implementing hybrid vector search with tenant isolation and source grounding, and running both local open-weights models and cloud APIs. Around the LLM itself, I build the execution harness that makes autonomy reliable: stateful orchestration, strict schema boundaries, measurable evaluations, crash recovery, latency and cost controls, and automated test suites.

Because production AI depends on the infrastructure around the model, my experience also spans computer vision and OCR pipelines, real-time speech and voice applications, distributed PySpark and SQL/NoSQL data flows, and shipping complete services with FastAPI, Django, Next.js, Flutter, Docker, and GitHub Actions.

---

## Flagship Systems (6 Core Repositories)

### 1. [Haseen-AI](https://github.com/alhaj-ai/Haseen-AI) — Crash-Resilient Software Agent Runtime
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Haseen-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/Haseen-AI/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/Haseen-AI?style=flat-square&color=0F766E)](https://github.com/alhaj-ai/Haseen-AI/releases)

`Python 3.11` · `FastAPI` · `Pydantic` · `Next.js 14` · `Docker`

Long-running coding agents lose progress or leave broken partial edits when a worker dies mid-task. Inside `backend/haseen/`, each execution step is recorded in an append-only ledger with `SHA-256` checkpoints, stale workers are fenced out using lease expiry, and diffs run inside an isolated shadow workspace before any patch is promoted.

**Verification:** `PYTHONPATH=backend python -m haseen.cli demo crash` survives forced `SIGKILL` mid-run and completes via a second worker with `patch applied 1 time(s)` and `duplicate side effects 0`. Passing CI: *Crash Recovery & Runtime Verification*.

<details>
<summary>CLI Crash-Recovery Trace (verified live)</summary>

```text
$ PYTHONPATH=backend python -m haseen.cli demo crash
worker-1 holds the lease and is mid-run - killing it with SIGKILL
worker-1 (pid 8404) is gone; its last checkpoint is #6 after 'analysis' (6 saved)
worker-2: the lease expired 2.2s after the kill; run recovered as 'queued'
ledger: patch_applied          runtime    Patch applied to 1 files
result: completed/applied/passed; patch applied 1 time(s); repository fixed: True
evidence: planner model calls 1 (the plan was kept, not redone); duplicate side effects 0; finished by worker-2
```

</details>

---

### 2. [Mutahakkim-AI](https://github.com/alhaj-ai/Mutahakkim-AI) — Discover-Once, Zero-Token Browser Automation
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Mutahakkim-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/Mutahakkim-AI/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/Mutahakkim-AI?style=flat-square&color=0F766E)](https://github.com/alhaj-ai/Mutahakkim-AI/releases)

`Python 3.11` · `Playwright` · `FastAPI` · `Pydantic` · `PyYAML` · `Next.js 14`

Driving every browser click through a Vision LLM is slow, costly, and fragile when page coordinates shift. `src/computer_use/compiler.py` discovers the workflow once, compiles accessible ARIA role and name locators into versioned YAML capability graphs with pre/post DOM guards and OTP handoff hooks, and replays runs directly in Playwright without calling a model.

**Verification:** `python -m mutahakkim.cli replay --capability lookup_savings_balance --member-id 10002 --headless` finishes with `model_calls: 0` (`813ms` locally on Windows; `716ms` baseline documented in the repo). Passing CI: *Capability Graph & CLI Verification*.

<details>
<summary>Zero-Token Replay Output (verified live)</summary>

```json
{
  "kind": "success",
  "run_id": "14a1c83e1da1",
  "outputs": {
    "savings_balance": "$12040.00",
    "member_name": "Marcus Chen"
  },
  "model_calls": 0,
  "duration_ms": 813,
  "evidence_dir": "evidence\\replay-success"
}
```

</details>

---

### 3. [DocuMind-RAG](https://github.com/alhaj-ai/DocuMind-RAG) — Multi-Tenant PDF Q&A with Source-Page Citations
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/DocuMind-RAG/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/DocuMind-RAG/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/DocuMind-RAG?style=flat-square&color=0F766E)](https://github.com/alhaj-ai/DocuMind-RAG/releases)

`Python` · `FastAPI` · `Qdrant` · `PostgreSQL / SQLAlchemy` · `Google Gemini` · `Docker`

Shared vector indexes mix tenant data, and ungrounded Q&A answers make citation audits painful. `rag/chunker.py` splits PDFs into `1,000`-character chunks with `200`-character overlap (`config.py`), `rag/vectorstore.py` isolates each account in its own Qdrant collection, `rag/citations.py` links responses back to exact source pages, and `auth/security.py` protects routes with JWT and Bcrypt.

**Verification:** `17 / 17` pytest unit and integration tests passing (`5.00s`) in GitHub Actions (*Hybrid RAG & Security Test Suite*).

---

### 4. [Agentic-DeepResearch](https://github.com/alhaj-ai/Agentic-DeepResearch) — Self-Correcting Research Pipeline
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Agentic-DeepResearch/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/Agentic-DeepResearch/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/Agentic-DeepResearch?style=flat-square&color=0F766E)](https://github.com/alhaj-ai/Agentic-DeepResearch/releases)

`Python 3.11` · `LangGraph` · `FastAPI` · `Google Gemini` · `Tavily API` · `SSE` · `Docker`

Single-pass web search agents often summarize incomplete drafts without catching missing evidence. `graph/workflow.py` wires a cyclic LangGraph `StateGraph` (`planner` ➔ `searcher` ➔ `writer` ➔ `critic`, bounded by `MAX_REVISIONS=3`) for bilingual Arabic/English query planning, parallel retrieval, SSE streaming, and critic-gated revisions.

**Verification:** `12 / 12` pytest workflow, agent, and API tests passing (`1.58s`) in GitHub Actions (*Multi-Agent DeepResearch Tests*).

---

### 5. [DocuShield-AI](https://github.com/alhaj-ai/DocuShield-AI) — Local Arabic Document & PII Intelligence
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/DocuShield-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/DocuShield-AI/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/DocuShield-AI?style=flat-square&color=0F766E)](https://github.com/alhaj-ai/DocuShield-AI/releases)

`Python` · `PyTorch` · `LayoutLMv3` · `XLM-RoBERTa` · `FastAPI` · `Streamlit` · `Docker`

Sensitive institutional and clinical documents cannot safely be sent to external cloud APIs. The pipeline runs fine-tuned `LayoutLMv3` layout parsing (`models/problem1_layoutlmv3`), `XLM-RoBERTa` entity extraction (`models/problem2_xlmr_joint`), and deterministic Arabic PII redaction rules behind FastAPI and Streamlit.

**Verification:** `9 / 9` pytest verification tests passing (`1.99s`) in GitHub Actions (*Document Intelligence & Yemeni PII Redaction Tests*).

---

### 6. [Mustakshef-AI](https://github.com/alhaj-ai/Mustakshef-AI) — Interactive Arabic Vision & Phonics System
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Mustakshef-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/Mustakshef-AI/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/Mustakshef-AI?style=flat-square&color=0F766E)](https://github.com/alhaj-ai/Mustakshef-AI/releases)

`Python` · `YOLOv8-Seg` · `FastAPI` · `Edge TTS` · `Next.js 14` · `Docker`

An interactive Arabic vision and phonics system pairing `YOLOv8` instance segmentation across 82 Arabic object classes (`backend/main.py`) with RTL visual overlays (`NotoNaskhArabic-Regular.ttf`), diacritic-stripped letter breakdown, concurrent neural speech synthesis (`ar-SA-HamedNeural` / `ar-SA-ZariyahNeural` with HTTP TTS fallback), explicit unrecognized empty states, and a Next.js 14 interface.

**Verification:** `7 / 7` pytest API and phonics tests passing (`0.91s`) plus Next.js TypeScript check and production build passing in GitHub Actions, alongside published `v1.0.0` model weights.

---

## Selected Domain Systems

| Repository | Scope & Core Implementation | Verification |
| :--- | :--- | :--- |
| [**data-migration-pipeline**](https://github.com/alhaj-ai/data-migration-pipeline) | Hybrid CSV-to-MongoDB ETL router (`src/file_router.py`) selecting Python streaming vs distributed **PySpark**, normalizing Eastern Arabic numerals/currency strings, and quarantining invalid rows via 9 quality rules | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/data-migration-pipeline/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/data-migration-pipeline/actions) `15/15` pytest (`0.02s`) |
| [**TaskFlow**](https://github.com/alhaj-ai/taskflow) | Offline-first **Flutter** (`SQLite sqflite`) + **FastAPI / PostgreSQL** (`8` relational tables) task ecosystem with Gemini task breakdown and local fallback | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/taskflow/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/taskflow/actions) Backend + Flutter CI · `v1.0.0` APK |
| [**Majles-AI**](https://github.com/alhaj-ai/Majles-AI) | Arabic meeting assistant combining **WhisperX** diarization, **FAISS + CrossEncoder** retrieval, and local **Ollama** Q&A (`Next.js 14`, `FastAPI`) | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Majles-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/Majles-AI/actions) `4/4` pytest (`0.99s`) |
| [**Mohawir-AI**](https://github.com/alhaj-ai/Mohawir-AI) | Technical interview simulator coordinating 5 **LangGraph** `StateGraph` agents, FAISS RAG, isolated code evaluation, and `Next.js 14` UI | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Mohawir-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/Mohawir-AI/actions) `4/4` pytest (`0.59s`) |
| [**Azal-AI**](https://github.com/alhaj-ai/Azal-AI) | Multi-agent e-commerce operations assistant with supervisor routing, supplier PDF invoice auditing, and **React 19** + local/cloud LLM hub | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Azal-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/Azal-AI/actions) `2/2` pytest (`0.06s`) |
| [**voice-agent-Pharmacy-Assistant**](https://github.com/alhaj-ai/voice-agent-Pharmacy-Assistant) | Real-time bidirectional **Twilio Media Streams** & **Deepgram Voice Agent** WebSocket bridge with `Barge-in` interruption handling | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/voice-agent-Pharmacy-Assistant/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/voice-agent-Pharmacy-Assistant/actions) Function & bridge CI |
| [**ai-multi-search-agent**](https://github.com/alhaj-ai/ai-multi-search-agent) | 9-node parallel **LangGraph** workflow aggregating and synthesizing Google, Bing, and Reddit SERP results (`Streamlit`) | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/ai-multi-search-agent/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/ai-multi-search-agent/actions) Topology CI |
| [**mindRouter-agent**](https://github.com/alhaj-ai/mindRouter-agent) | Stateful **LangGraph** conditional intent router preserving conversation history across specialized assistant nodes | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/mindRouter-agent/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/mindRouter-agent/actions) Routing logic CI |

---

## Skills & Technical Stack

| Domain | Technologies & Capabilities |
| :--- | :--- |
| **LLMs, Fine-Tuning & AI** | `Large Language Models (LLMs)` · `Model Fine-Tuning` · `Transfer Learning` · `Agent Harnesses` · `Multi-Agent Orchestration` · `Hybrid RAG` · `Prompt Engineering` · `NLP` · `Computer Vision` · `Machine Learning` · `Deep Learning` |
| **AI Frameworks & Serving** | `PyTorch` · `TensorFlow` · `Hugging Face Transformers & Trainer` · `LangGraph` · `LangChain` · `Scikit-learn` · `XGBoost` · `Pydantic` · `Ollama` · `LM Studio` · `Google Gemini` · `Tavily` |
| **Vision, OCR & Speech** | `Ultralytics YOLOv8` · `LayoutLMv3` · `XLM-RoBERTa` · `OpenCV` · `EasyOCR` · `Tesseract OCR` · `spaCy` · `NLTK` · `WhisperX` · `Edge TTS` · `Twilio Media Streams` · `Deepgram` |
| **Data, Retrieval & Eval** | `Qdrant` · `FAISS` · `CrossEncoder` · `Apache Spark (PySpark)` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `SeqEval / F1 Evaluation` · `ETL Pipelines` |
| **Languages & Databases** | `Python` · `TypeScript` · `JavaScript (ES6+)` · `SQL` · `Dart` · `PostgreSQL` · `MongoDB` · `SQLite` · `SQLAlchemy` |
| **Web, Mobile & Automation** | `FastAPI` · `Django REST Framework` · `Next.js 14` · `React` · `Flutter` · `Streamlit` · `Playwright` · `REST APIs` · `WebSockets` · `SSE` · `JWT / Bcrypt` |
| **DevOps, Testing & Tooling** | `Docker` · `Git` · `GitHub` · `GitHub Actions CI/CD` · `Pytest` · `Linux` |
