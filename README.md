# Mohammed Al-Haj

**AI Engineer** | LLMs · Hybrid RAG · Model Fine-Tuning · Agent Systems · Computer Vision · FastAPI

[Portfolio](https://alhaj-ai.github.io) · [GitHub](https://github.com/alhaj-ai) · [LinkedIn](https://linkedin.com/in/mohammed-mohammed-al-haj-341ab7369) · [X](https://x.com/mod_alhaj) · [ai.mohammed.alhaj@gmail.com](mailto:ai.mohammed.alhaj@gmail.com)

Open to remote AI and LLM Engineering roles.

---

## About

I build applied LLM systems, retrieval pipelines, and fine-tuned models backed by clean APIs and automated tests.

For private workloads that cannot leave local hardware, I train Transformer and vision models with PyTorch and Hugging Face Trainer, and isolate document embeddings per account in Qdrant and FAISS with source page citations.

On the application side, I connect models to LangGraph workflows, FastAPI and Django backends, Next.js interfaces, Flutter mobile apps, and real-time voice streams, with Docker builds and pytest checks on GitHub Actions.

---

## Flagship projects (6 core repositories)

### 1. [Haseen-AI](https://github.com/alhaj-ai/Haseen-AI): Crash-resilient coding agent runtime
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Haseen-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/Haseen-AI/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/Haseen-AI?style=flat-square&color=0F766E)](https://github.com/alhaj-ai/Haseen-AI/releases)

`Python 3.11` · `FastAPI` · `Pydantic` · `Next.js 14` · `Docker`

Long-running coding agents lose progress or leave broken partial edits when a worker exits mid-task. Inside `backend/haseen/`, the runtime logs each step to an append-only `SHA-256` ledger, lets another worker take over after lease expiry, and tests patches inside a shadow workspace before touching the repo.

Running `PYTHONPATH=backend python -m haseen.cli demo crash` simulates a mid-run exit and finishes via a second worker with `patch applied 1 time(s)` and `duplicate side effects 0`. Passing CI: *Crash Recovery & Runtime Verification*.

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

### 2. [Mutahakkim-AI](https://github.com/alhaj-ai/Mutahakkim-AI): Discover-once browser automation
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Mutahakkim-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/Mutahakkim-AI/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/Mutahakkim-AI?style=flat-square&color=0F766E)](https://github.com/alhaj-ai/Mutahakkim-AI/releases)

`Python 3.11` · `Playwright` · `FastAPI` · `Pydantic` · `PyYAML` · `Next.js 14`

Calling a Vision LLM for every click is slow and breaks whenever layout coordinates shift. After one exploration pass, `src/computer_use/compiler.py` writes a versioned YAML graph anchored to ARIA roles and element names with pre/post DOM guards and OTP hooks, then replays runs in Playwright without calling a model.

Running `python -m mutahakkim.cli replay --capability lookup_savings_balance --member-id 10002 --headless` finishes with `model_calls: 0` (`813ms` locally on Windows; `716ms` baseline recorded in the repo). Passing CI: *Capability Graph & CLI Verification*.

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

### 3. [DocuMind-RAG](https://github.com/alhaj-ai/DocuMind-RAG): Multi-tenant PDF Q&A with page citations
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/DocuMind-RAG/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/DocuMind-RAG/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/DocuMind-RAG?style=flat-square&color=0F766E)](https://github.com/alhaj-ai/DocuMind-RAG/releases)

`Python` · `FastAPI` · `Qdrant` · `PostgreSQL / SQLAlchemy` · `Google Gemini` · `Docker`

Shared vector indexes risk mixing data across accounts, and uncited answers make audits hard. `rag/chunker.py` splits PDFs into `1,000`-character chunks with `200`-character overlap (`config.py`), `rag/vectorstore.py` puts each user in a separate Qdrant collection behind JWT and Bcrypt routes (`auth/security.py`), and `rag/citations.py` attaches source page numbers to every response.

All `17 / 17` pytest unit and integration tests pass in `5.00s` on GitHub Actions (*Hybrid RAG & Security Test Suite*).

---

### 4. [Agentic-DeepResearch](https://github.com/alhaj-ai/Agentic-DeepResearch): Self-correcting research pipeline
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Agentic-DeepResearch/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/Agentic-DeepResearch/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/Agentic-DeepResearch?style=flat-square&color=0F766E)](https://github.com/alhaj-ai/Agentic-DeepResearch/releases)

`Python 3.11` · `LangGraph` · `FastAPI` · `Google Gemini` · `Tavily API` · `SSE` · `Docker`

Single-pass search agents often return thin drafts with missing sources. `graph/workflow.py` runs a bounded LangGraph `StateGraph` (`planner` -> `searcher` -> `writer` -> `critic`, capped at `MAX_REVISIONS=3`) for bilingual Arabic and English queries, parallel searches, draft checks, and SSE streams.

All `12 / 12` pytest workflow, agent, and API tests pass in `1.58s` on GitHub Actions (*Multi-Agent DeepResearch Tests*).

---

### 5. [DocuShield-AI](https://github.com/alhaj-ai/DocuShield-AI): Local document extraction and Arabic PII redaction
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/DocuShield-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/DocuShield-AI/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/DocuShield-AI?style=flat-square&color=0F766E)](https://github.com/alhaj-ai/DocuShield-AI/releases)

`Python` · `PyTorch` · `Hugging Face Trainer` · `LayoutLMv3` · `XLM-RoBERTa` · `FastAPI` · `Streamlit` · `Docker`

Clinical and legal files cannot always go to external cloud APIs. Using Hugging Face `Trainer`, `src/problem1_document_understanding/train_layout_model.py` trains `LayoutLMv3` locally (`0.9856` eval F1, `0.9871` accuracy) and `src/problem2_ner_classification/train_ner.py` trains `XLM-RoBERTa` with `seqeval` (`0.1292` baseline up to `0.5606` eval F1), paired with rule-based Arabic PII redaction behind FastAPI and Streamlit.

All `9 / 9` pytest verification tests pass in `1.99s` on GitHub Actions (*Document Intelligence & Yemeni PII Redaction Tests*).

---

### 6. [Mustakshef-AI](https://github.com/alhaj-ai/Mustakshef-AI): Arabic vision and phonics web app
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Mustakshef-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/Mustakshef-AI/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/Mustakshef-AI?style=flat-square&color=0F766E)](https://github.com/alhaj-ai/Mustakshef-AI/releases)

`Python` · `YOLOv8-Seg` · `FastAPI` · `Edge TTS` · `Next.js 14` · `Docker`

Paired with a Next.js 14 interface, the backend runs `YOLOv8` segmentation across 82 Arabic object classes (`backend/main.py`), draws RTL Pillow overlays (`NotoNaskhArabic-Regular.ttf`), splits detected words into unvocalized letters, and plays concurrent Edge TTS speech (`ar-SA-HamedNeural` / `ar-SA-ZariyahNeural` with HTTP fallback) while returning explicit empty states when nothing matches.

All `7 / 7` pytest API and phonics checks pass in `0.91s` alongside Next.js TypeScript and production build checks in GitHub Actions, with `v1.0.0` model weights published.

---

## Domain repositories

| Repository | Scope and implementation | Verification |
| :--- | :--- | :--- |
| [**data-migration-pipeline**](https://github.com/alhaj-ai/data-migration-pipeline) | Routes CSV-to-MongoDB imports in `src/file_router.py` between Python streaming and **PySpark**, normalizes Eastern Arabic numerals and currency strings, and isolates rows failing 9 validation rules | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/data-migration-pipeline/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/data-migration-pipeline/actions) `15/15` pytest (`0.02s`) |
| [**TaskFlow**](https://github.com/alhaj-ai/taskflow) | Offline-first **Flutter** client (`SQLite sqflite`) paired with a **FastAPI / PostgreSQL** (`8` relational tables) backend, Gemini task breakdown, and local fallback | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/taskflow/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/taskflow/actions) Backend + Flutter CI · `v1.0.0` APK |
| [**Majles-AI**](https://github.com/alhaj-ai/Majles-AI) | Local Arabic meeting assistant with **WhisperX** diarization, **FAISS + CrossEncoder** search, and **Ollama** Q&A (`Next.js 14`, `FastAPI`) | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Majles-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/Majles-AI/actions) `4/4` pytest (`0.99s`) |
| [**Mohawir-AI**](https://github.com/alhaj-ai/Mohawir-AI) | Technical interview simulator running 5 **LangGraph** `StateGraph` agents, FAISS search, sandboxed code checks, and a `Next.js 14` UI | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Mohawir-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/Mohawir-AI/actions) `4/4` pytest (`0.59s`) |
| [**Azal-AI**](https://github.com/alhaj-ai/Azal-AI) | Multi-agent e-commerce tool with supervisor routing, supplier PDF invoice checks, and a **React 19** UI supporting **LM Studio** local weights and cloud APIs | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Azal-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/Azal-AI/actions) `2/2` pytest (`0.06s`) |
| [**voice-agent-Pharmacy-Assistant**](https://github.com/alhaj-ai/voice-agent-Pharmacy-Assistant) | Two-way **Twilio Media Streams** and **Deepgram Voice Agent** WebSocket bridge that handles caller `Barge-in` interruptions live | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/voice-agent-Pharmacy-Assistant/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/voice-agent-Pharmacy-Assistant/actions) Function & bridge CI |
| [**ai-multi-search-agent**](https://github.com/alhaj-ai/ai-multi-search-agent) | 9-node parallel **LangGraph** workflow collecting search results from Google, Bing, and Reddit in `Streamlit` | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/ai-multi-search-agent/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/ai-multi-search-agent/actions) Topology CI |
| [**mindRouter-agent**](https://github.com/alhaj-ai/mindRouter-agent) | Stateful **LangGraph** intent router carrying conversation history across specialized assistant roles | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/mindRouter-agent/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/mindRouter-agent/actions) Routing logic CI |

---

## Skills and technical stack

| Domain | Technologies |
| :--- | :--- |
| **LLMs, Fine-Tuning & AI** | `Large Language Models (LLMs)` · `Model Fine-Tuning` · `Transfer Learning` · `Agent Harnesses` · `Multi-Agent Workflows` · `Hybrid RAG` · `Prompt Engineering` · `NLP` · `Computer Vision` · `Machine Learning` · `Deep Learning` |
| **AI Frameworks & Serving** | `PyTorch` · `TensorFlow` · `Hugging Face Transformers & Trainer` · `LangGraph` · `LangChain` · `Scikit-learn` · `XGBoost` · `Pydantic` · `Ollama` · `LM Studio` · `Google Gemini` · `Tavily` |
| **Vision, OCR & Speech** | `Ultralytics YOLOv8` · `LayoutLMv3` · `XLM-RoBERTa` · `OpenCV` · `EasyOCR` · `Tesseract OCR` · `spaCy` · `NLTK` · `WhisperX` · `Edge TTS` · `Twilio Media Streams` · `Deepgram` |
| **Data, Search & Eval** | `Qdrant` · `FAISS` · `CrossEncoder` · `Apache Spark (PySpark)` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `SeqEval / F1 Evaluation` · `ETL Pipelines` |
| **Languages & Databases** | `Python` · `TypeScript` · `JavaScript (ES6+)` · `SQL` · `Dart` · `PostgreSQL` · `MongoDB` · `SQLite` · `SQLAlchemy` |
| **Web, Mobile & Automation** | `FastAPI` · `Django REST Framework` · `Next.js 14` · `React` · `Flutter` · `Streamlit` · `Playwright` · `REST APIs` · `WebSockets` · `SSE` · `JWT / Bcrypt` |
| **DevOps, Testing & Tooling** | `Docker` · `Git` · `GitHub` · `GitHub Actions CI/CD` · `Pytest` · `Linux` |

Additional TensorFlow, XGBoost, data-mining, and Django REST projects are in the public repository archive.
