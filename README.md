# Mohammed Al-Haj

**AI Engineer** — Agentic Systems, Multi-Agent Workflows, Hybrid RAG, Document & Vision AI & Computer-Use Automation

[GitHub](https://github.com/alhaj-ai) · [LinkedIn](https://linkedin.com/in/mohammed-mohammed-al-haj-341ab7369) · [X](https://x.com/mod_alhaj) · [ai.mohammed.alhaj@gmail.com](mailto:ai.mohammed.alhaj@gmail.com)

> I build verifiable AI software backed by crash-recovery ledgers, deterministic browser replay, isolated multi-tenant retrieval, and automated `pytest` + GitHub Actions CI suites rather than unguarded prompt loops.

---

## Flagship Systems (6 Core Repositories)

### 1. [Haseen-AI](https://github.com/alhaj-ai/Haseen-AI) — Crash-Resilient Software Agent Runtime
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Haseen-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/Haseen-AI/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/Haseen-AI?style=flat-square&color=0F766E)](https://github.com/alhaj-ai/Haseen-AI/releases)

`Python 3.11` · `FastAPI` · `Pydantic` · `Next.js 14` · `Docker`

* **Design & Trade-offs**: Long-running coding agents lose context or leave partial file edits if killed mid-run. `backend/haseen/` writes every stage to an append-only ledger with `SHA-256` checkpoints, fences stale workers using lease expiration, executes changes inside isolated shadow workspaces, and only promotes patches that pass validation gates.
* **Verified Execution**: `PYTHONPATH=backend python -m haseen.cli demo crash` terminates the active worker with `SIGKILL` mid-run and resumes via a secondary worker without duplicate writes (`patch applied 1 time(s); repository fixed: True; duplicate side effects 0`). Passing CI job: *Crash Recovery & Runtime Verification*.

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

* **Design & Trade-offs**: Driving every browser interaction through a Vision LLM incurs high latency, token cost, and coordinate drift. `src/computer_use/compiler.py` and `replay.py` discover the workflow once, compile ARIA role/name locators into versioned YAML capability graphs with DOM pre/post guards and OTP operator handoff hooks, and replay deterministically via Playwright with **0 model calls**.
* **Verified Execution**: `python -m mutahakkim.cli replay --capability lookup_savings_balance --member-id 10002 --headless` completes with **`model_calls: 0`** (`813ms` observed locally on Windows; `716ms` baseline documented in the repo). Passing CI job: *Capability Graph & CLI Verification*.

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

* **Design & Trade-offs**: Enforces strict tenant isolation and answer provenance across uploaded PDFs. `rag/chunker.py` segments pages into `1,000`-character chunks with `200`-character overlap (`config.py`), `rag/vectorstore.py` isolates per-account **Qdrant** collections, `rag/citations.py` binds generated answers back to source page numbers, and `auth/security.py` guards endpoints with JWT + Bcrypt.
* **Verified Execution**: **`17 / 17` pytest unit & integration tests passing (`5.00s`)** in GitHub Actions (*Hybrid RAG & Security Test Suite*).

---

### 4. [Agentic-DeepResearch](https://github.com/alhaj-ai/Agentic-DeepResearch) — Self-Correcting Research Pipeline
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Agentic-DeepResearch/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/Agentic-DeepResearch/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/Agentic-DeepResearch?style=flat-square&color=0F766E)](https://github.com/alhaj-ai/Agentic-DeepResearch/releases)

`Python 3.11` · `LangGraph` · `FastAPI` · `Google Gemini` · `Tavily API` · `SSE` · `Docker`

* **Design & Trade-offs**: Replaces single-shot web synthesis with a bounded cyclic `StateGraph` (`graph/workflow.py`: `planner` ➔ `searcher` ➔ `writer` ➔ `critic`, up to `MAX_REVISIONS=3`) supporting bilingual Arabic/English query decomposition, concurrent web search, critic-gated revision loops, and SSE progress streaming.
* **Verified Execution**: **`12 / 12` pytest workflow, agent & API tests passing (`1.58s`)** in GitHub Actions (*Multi-Agent DeepResearch Tests*).

---

### 5. [DocuShield-AI](https://github.com/alhaj-ai/DocuShield-AI) — Local Arabic Document & PII Intelligence
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/DocuShield-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/DocuShield-AI/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/DocuShield-AI?style=flat-square&color=0F766E)](https://github.com/alhaj-ai/DocuShield-AI/releases)

`Python` · `PyTorch` · `LayoutLMv3` · `XLM-RoBERTa` · `FastAPI` · `Streamlit` · `Docker`

* **Design & Trade-offs**: Built for sensitive institutional documents that cannot leave private infrastructure. Pairs fine-tuned `LayoutLMv3` visual document extraction (`models/problem1_layoutlmv3`), `XLM-RoBERTa` multilingual NER (`models/problem2_xlmr_joint`), and deterministic Arabic PII redaction rules behind FastAPI and Streamlit.
* **Verified Execution**: **`9 / 9` pytest verification tests passing (`1.99s`)** in GitHub Actions (*Document Intelligence & Yemeni PII Redaction Tests*).

---

### 6. [Mustakshef-AI](https://github.com/alhaj-ai/Mustakshef-AI) — Interactive Arabic Vision & Phonics System
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Mustakshef-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/Mustakshef-AI/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/Mustakshef-AI?style=flat-square&color=0F766E)](https://github.com/alhaj-ai/Mustakshef-AI/releases)

`Python` · `YOLOv8-Seg` · `FastAPI` · `Edge TTS` · `Next.js 14` · `Docker`

* **Design & Trade-offs**: Pairs `YOLOv8` instance segmentation across 82 Arabic object classes (`backend/main.py`) with RTL visual pill annotation (`arabic_reshaper`, `python-bidi`, `NotoNaskhArabic-Regular.ttf`), diacritic-stripped Arabic phonics breakdown, concurrent per-letter neural speech synthesis (`ar-SA-HamedNeural` / `ar-SA-ZariyahNeural` with HTTP TTS fallback), explicit unrecognized empty states, and `Next.js 14` App Router UI.
* **Verified Execution**: **`7 / 7` pytest API & phonics tests passing (`0.91s`)** + `Next.js` TypeScript & production build passing in GitHub Actions (*Backend API, Phonics & Pipeline Tests* · *Frontend TypeScript & Next.js Build*), with `v1.0.0` model weights release published.

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

## Core Technical Stack

| Domain | Core Technologies & Protocols |
| :--- | :--- |
| **Agentic & LLM Systems** | `LangGraph` · `LangChain` · `Playwright` (Computer-Use) · `Google Gemini` · `Ollama` · `Tavily` · `Pydantic` |
| **RAG, Vectors & Data** | `Qdrant` · `FAISS` · `CrossEncoder` · `PostgreSQL` · `MongoDB` · `Apache Spark (PySpark)` · `SQLite` · `SQLAlchemy` |
| **Vision, Document & Speech AI** | `PyTorch` · `LayoutLMv3` · `XLM-RoBERTa` · `Ultralytics YOLOv8` · `WhisperX` · `Edge TTS` · `Twilio` · `Deepgram` |
| **Languages, APIs & Infra** | `Python 3.11+` · `TypeScript` · `FastAPI` · `Next.js 14` · `React 19` · `Flutter` · `Docker` · `Pytest` · `GitHub Actions` |
