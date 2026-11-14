<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0B1120,50:1E293B,100:0369A1&height=210&section=header&text=Mohammed%20Al-Haj%20%7C%20%D9%85%D8%AD%D9%85%D8%AF%20%D8%A7%D9%84%D8%AD%D8%A7%D8%AC&fontSize=36&fontColor=F8FAFC&fontAlignY=38&desc=AI%20Systems%20%26%20Multi-Agent%20Runtime%20Engineer&descSize=18&descColor=38BDF8&descAlignY=60" width="100%" alt="Mohammed Al-Haj Header Banner" />

<a href="https://github.com/alhaj-ai">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=18&duration=3200&pause=900&color=38BDF8&center=true&vCenter=true&width=860&lines=Crash-Resilient+Agent+Runtimes+(SIGKILL+Recovery+%26+SHA-256+Ledgers);Discover-Once%2C+Zero-Token+Browser+Replay+(0+LLM+Calls+%E2%80%A2+%3C1s+Replay);Multi-Tenant+Hybrid+RAG+%E2%80%A2+Exact+Page+Citations+%E2%80%A2+Local+Inference;Arabic+Document+PII+Intelligence+%E2%80%A2+YOLOv8+Vision+%E2%80%A2+Distributed+ETL" alt="Engineering Focus" />
</a>

<br/>

[![GitHub](https://img.shields.io/badge/GitHub-@alhaj--ai-0F172A?style=for-the-badge&logo=github&logoColor=white)](https://github.com/alhaj-ai)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Mohammed_Al--Haj-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/mohammed-mohammed-al-haj-341ab7369)
[![Email](https://img.shields.io/badge/Email-ai.mohammed.alhaj%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ai.mohammed.alhaj@gmail.com)
[![X](https://img.shields.io/badge/X-@mod__alhaj-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/mod_alhaj)
[![Location](https://img.shields.io/badge/Sana'a%2C_Yemen-%D8%B5%D9%86%D8%B9%D8%A7%D8%A1%D8%8C_%D8%A7%D9%84%D9%8A%D9%85%D9%86-0D9488?style=for-the-badge)](https://github.com/alhaj-ai)

</div>

---

## Engineering Philosophy

I build verifiable AI software from **Sana'a, Yemen** where autonomous workflows meet deterministic systems engineering — favoring reproducible tests, strict state guarantees, and clean failure recovery over fragile prompt wrappers:

| Engineering Pillar | How It Shows Up in Code | Proven In |
| :--- | :--- | :--- |
| **Crash & State Determinism** | Append-only SHA-256 checkpoints, lease epoch fencing, shadow workspace isolation, and idempotent patch promotion across worker kills. | [`Haseen-AI`](https://github.com/alhaj-ai/Haseen-AI) |
| **Zero-Token Determinism** | Discover browser paths once via VLM, compile semantic YAML capability graphs, and replay via Playwright at `0` LLM cost. | [`Mutahakkim-AI`](https://github.com/alhaj-ai/Mutahakkim-AI) |
| **Grounded Retrieval & Privacy** | Per-tenant Qdrant collections, exact source-page citations, local `LayoutLMv3`/`XLM-RoBERTa` PII redaction, and offline `Ollama` inference. | [`DocuMind-RAG`](https://github.com/alhaj-ai/DocuMind-RAG) · [`DocuShield-AI`](https://github.com/alhaj-ai/DocuShield-AI) |
| **Verified Pipelines & CI** | Automated `pytest` suites, schema/cascade checks, distributed PySpark/MongoDB routing, and green GitHub Actions across all core repos. | [`Agentic-DeepResearch`](https://github.com/alhaj-ai/Agentic-DeepResearch) · [`data-migration-pipeline`](https://github.com/alhaj-ai/data-migration-pipeline) |

---

## Ecosystem Architecture Map

```mermaid
flowchart LR
    subgraph Runtimes["1. Agent Runtimes & Orchestration"]
        H["Haseen-AI\nSIGKILL Crash Recovery"]
        M["Mutahakkim-AI\n0-Token Browser Replay"]
        DR["Agentic-DeepResearch\nCyclic LangGraph + Critic"]
        MO["Mohawir-AI & Routers\nMulti-Agent StateGraphs"]
    end

    subgraph Knowledge["2. RAG & Document Intelligence"]
        DM["DocuMind-RAG\nQdrant Multi-Tenant + Citations"]
        DS["DocuShield-AI\nLayoutLMv3 + XLM-RoBERTa PII"]
        AZ["Azal-AI\nInvoice Audit & Local LLMs"]
    end

    subgraph Multimodal["3. Vision, Speech & Arabic AI"]
        MK["Mustakshef-AI\nYOLOv8-Seg + Saudi Neural TTS"]
        MJ["Majles-AI\nWhisperX + CrossEncoder RAG"]
        VA["voice-agent-Pharmacy\nTwilio + Deepgram Barge-In"]
    end

    subgraph Delivery["4. Data ETL & Offline Mobile"]
        DMP["data-migration-pipeline\nPySpark / Python + MongoDB"]
        TF["TaskFlow\nFlutter SQLite + FastAPI Postgres"]
    end

    Runtimes --> Knowledge
    Knowledge --> Multimodal
    Multimodal --> Delivery
```

---

## Technical Stack

<div align="center">

**Agents & AI Orchestration**  
![Python](https://img.shields.io/badge/Python_3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Google_Gemini-4285F4?style=for-the-badge&logo=googlegemini&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama_Local-000000?style=for-the-badge&logo=ollama&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logo=playwright&logoColor=white)

**Retrieval, Databases & Distributed ETL**  
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=for-the-badge)
![FAISS](https://img.shields.io/badge/FAISS-0467DF?style=for-the-badge&logo=meta&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Apache Spark](https://img.shields.io/badge/Apache_Spark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)

**Document AI, Vision & Speech**  
![YOLOv8](https://img.shields.io/badge/Ultralytics_YOLOv8-111F68?style=for-the-badge)
![LayoutLMv3](https://img.shields.io/badge/LayoutLMv3-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![XLM-RoBERTa](https://img.shields.io/badge/XLM--RoBERTa-FF9D00?style=for-the-badge&logo=huggingface&logoColor=black)
![WhisperX](https://img.shields.io/badge/WhisperX_ASR-10A37F?style=for-the-badge)
![Twilio](https://img.shields.io/badge/Twilio_Media_Streams-F22F46?style=for-the-badge&logo=twilio&logoColor=white)
![Deepgram](https://img.shields.io/badge/Deepgram_Voice-13EF93?style=for-the-badge&logoColor=black)

**Backend, Frontend, Mobile & DevOps**  
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js_14-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter_3.x-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)

</div>

---

## Flagship Systems (6 Core Projects)

### 1. [Haseen-AI](https://github.com/alhaj-ai/Haseen-AI) — Crash-Resilient Software Agent Runtime
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Haseen-AI/ci.yml?branch=main&style=flat-square&logo=githubactions&logoColor=white&label=CI)](https://github.com/alhaj-ai/Haseen-AI/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/Haseen-AI?style=flat-square&color=0D9488)](https://github.com/alhaj-ai/Haseen-AI/releases)

* **Architecture**: Executes multi-step coding agents (`backend/haseen/`) against an append-only state ledger with SHA-256 checkpoints, lease epoch fencing, and isolated shadow workspaces — promoting patches only after validation gates succeed and preventing duplicate file mutations after worker crashes.
* **Stack**: `Python 3.11` · `FastAPI` · `Pydantic` · `Next.js 14` · `Docker`
* **Verified Evidence**: `PYTHONPATH=backend python -m haseen.cli demo crash` survives forced `SIGKILL` termination cleanly (`patch applied 1 time(s); repository fixed: True; duplicate side effects 0`). Passing CI job: *Crash Recovery & Runtime Verification*.

<details>
<summary>Inspect verified live CLI crash-recovery trace</summary>

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

### 2. [Mutahakkim-AI](https://github.com/alhaj-ai/Mutahakkim-AI) — Discover-Once, Zero-Token Browser Replay
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Mutahakkim-AI/ci.yml?branch=main&style=flat-square&logo=githubactions&logoColor=white&label=CI)](https://github.com/alhaj-ai/Mutahakkim-AI/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/Mutahakkim-AI?style=flat-square&color=0D9488)](https://github.com/alhaj-ai/Mutahakkim-AI/releases)

* **Architecture**: Discovers UI workflows once via a Vision-Language Agent, compiles semantic ARIA/role capability graphs into declarative YAML (`src/computer_use/compiler.py`, `replay.py`) with DOM pre/post verification guards + human OTP handoff, and replays flows via Playwright with **0 LLM calls**.
* **Stack**: `Python 3.11` · `Playwright` · `FastAPI` · `Pydantic` · `PyYAML` · `Next.js 14`
* **Verified Evidence**: `python -m mutahakkim.cli replay --capability lookup_savings_balance --member-id 10002 --headless` completes deterministically with **`model_calls: 0`** (`813ms` observed live on Windows; `716ms` baseline documented in repo). Passing CI job: *Capability Graph & CLI Verification*.

<details>
<summary>Inspect verified zero-token replay output</summary>

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

### 3. [DocuMind-RAG](https://github.com/alhaj-ai/DocuMind-RAG) — Multi-Tenant PDF RAG & Page-Cited Q&A
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/DocuMind-RAG/ci.yml?branch=main&style=flat-square&logo=githubactions&logoColor=white&label=CI)](https://github.com/alhaj-ai/DocuMind-RAG/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/DocuMind-RAG?style=flat-square&color=0D9488)](https://github.com/alhaj-ai/DocuMind-RAG/releases)

* **Architecture**: Splits PDFs into `1,000`-character chunks with `200`-character overlap (`rag/chunker.py`), isolates vectors per authenticated account inside **Qdrant** (`rag/vectorstore.py`), grounds every generated claim to explicit document page citations (`rag/citations.py`), and protects routes with JWT + Bcrypt (`auth/security.py`).
* **Stack**: `Python` · `FastAPI` · `Qdrant` · `PostgreSQL / SQLAlchemy` · `Google Gemini` · `Docker`
* **Verified Evidence**: **`17 / 17` pytest unit & integration tests passing (`5.00s`)** in GitHub Actions (*Hybrid RAG & Security Test Suite*).

---

### 4. [Agentic-DeepResearch](https://github.com/alhaj-ai/Agentic-DeepResearch) — Cyclic Multi-Agent Research Pipeline
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Agentic-DeepResearch/ci.yml?branch=main&style=flat-square&logo=githubactions&logoColor=white&label=CI)](https://github.com/alhaj-ai/Agentic-DeepResearch/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/Agentic-DeepResearch?style=flat-square&color=0D9488)](https://github.com/alhaj-ai/Agentic-DeepResearch/releases)

* **Architecture**: Compiles a cyclic **LangGraph** state machine (`graph/workflow.py`: `planner` ➔ `searcher` ➔ `writer` ➔ `critic` loop up to `MAX_REVISIONS=3`) that decomposes Arabic/English research queries, gathers concurrent web evidence, streams progress over SSE, and rejects incomplete drafts through an automated evaluator gate.
* **Stack**: `Python 3.11` · `LangGraph` · `FastAPI` · `Google Gemini` · `Tavily API` · `Docker`
* **Verified Evidence**: **`12 / 12` pytest workflow & agent tests passing (`1.58s`)** in GitHub Actions (*Multi-Agent DeepResearch Tests*).

---

### 5. [DocuShield-AI](https://github.com/alhaj-ai/DocuShield-AI) — Arabic & Yemeni Document PII Intelligence
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/DocuShield-AI/ci.yml?branch=main&style=flat-square&logo=githubactions&logoColor=white&label=CI)](https://github.com/alhaj-ai/DocuShield-AI/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/DocuShield-AI?style=flat-square&color=0D9488)](https://github.com/alhaj-ai/DocuShield-AI/releases)

* **Architecture**: Combines trained **`LayoutLMv3`** visual document extraction (`models/problem1_layoutlmv3`), **`XLM-RoBERTa`** multilingual NER (`models/problem2_xlmr_joint`), and deterministic regex/entity redaction tailored for Arabic & Yemeni sensitive records, exposed via FastAPI and Streamlit.
* **Stack**: `Python` · `PyTorch` · `LayoutLMv3` · `XLM-RoBERTa` · `FastAPI` · `Streamlit` · `Docker`
* **Verified Evidence**: **`9 / 9` pytest verification tests passing (`1.99s`)** in GitHub Actions (*Document Intelligence & Yemeni PII Redaction Tests*).

---

### 6. [TaskFlow](https://github.com/alhaj-ai/taskflow) — Offline-First Task Ecosystem (Flutter + FastAPI)
[![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/taskflow/ci.yml?branch=main&style=flat-square&logo=githubactions&logoColor=white&label=CI)](https://github.com/alhaj-ai/taskflow/actions)
[![Release](https://img.shields.io/github/v/release/alhaj-ai/taskflow?style=flat-square&color=0D9488)](https://github.com/alhaj-ai/taskflow/releases)

* **Architecture**: Combines an offline-first **Flutter** mobile app persisted in `SQLite` (`sqflite`) with a containerized **FastAPI + PostgreSQL** backend (`8` relational tables: `users`, `user_settings`, `categories`, `tasks`, `subtasks`, `recurrence_rules`, `reminders`, `calendar_events`) and dual-mode task decomposition (Gemini API + deterministic offline fallback).
* **Stack**: `Flutter 3.x` · `Dart` · `FastAPI` · `PostgreSQL 15` · `SQLAlchemy` · `SQLite` · `Docker`
* **Verified Evidence**: Backend schema, CRUD & delete-cascade integration checks + `flutter analyze` passing in GitHub Actions CI, with Android APK release published (`v1.0.0`).

---

## Selected Domain Systems (8 Additional Public Repositories)

| Track | Repository | Implemented Capabilities & Stack | Verified Status |
| :--- | :--- | :--- | :--- |
| **Data & ETL** | [**data-migration-pipeline**](https://github.com/alhaj-ai/data-migration-pipeline) | Hybrid CSV-to-MongoDB router (`src/file_router.py`) selecting Python streaming vs distributed **PySpark**, normalizing Eastern Arabic digits/currency, and quarantining invalid rows via 9 quality rules | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/data-migration-pipeline/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/data-migration-pipeline/actions) **`15/15` pytest (`0.02s`)** |
| **Vision & Arabic Speech** | [**Mustakshef-AI**](https://github.com/alhaj-ai/Mustakshef-AI) | **YOLOv8** instance segmentation across 82 Arabic classes (`backend/main.py`), Arabic letter phonics breakdown, **Edge TTS** Saudi neural voices (`ar-SA-ZariyahNeural` / `HamedNeural`), and **Next.js 14** UI | [![Release](https://img.shields.io/github/v/release/alhaj-ai/Mustakshef-AI?style=flat-square&color=0D9488)](https://github.com/alhaj-ai/Mustakshef-AI/releases) **`v1.0.0` Release** |
| **Speech & Local RAG** | [**Majles-AI**](https://github.com/alhaj-ai/Majles-AI) | Arabic meeting intelligence with **WhisperX** diarization, **FAISS + CrossEncoder** retrieval, and local **Ollama** Q&A (`Next.js 14`, `FastAPI`) | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Majles-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/Majles-AI/actions) **`4/4` pytest (`0.99s`)** |
| **Real-Time Voice** | [**voice-agent-Pharmacy-Assistant**](https://github.com/alhaj-ai/voice-agent-Pharmacy-Assistant) | Real-time bidirectional **Twilio Media Streams** & **Deepgram Voice Agent** WebSocket bridge with `Barge-in` interruption handling and pharmacy order tools | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/voice-agent-Pharmacy-Assistant/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/voice-agent-Pharmacy-Assistant/actions) **Function & bridge CI** |
| **Multi-Agent Interview** | [**Mohawir-AI**](https://github.com/alhaj-ai/Mohawir-AI) | Technical interview simulator coordinating 5 **LangGraph** `StateGraph` agents, FAISS RAG, sandboxed assessment, and `Next.js 14` frontend | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Mohawir-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/Mohawir-AI/actions) **`4/4` pytest (`0.59s`)** |
| **Commerce Agents** | [**Azal-AI**](https://github.com/alhaj-ai/Azal-AI) | Multi-agent e-commerce operations hub with supervisor intent routing, invoice extraction/validation, and **React 19** + local GPU/cloud provider switching | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/Azal-AI/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/Azal-AI/actions) **`2/2` pytest (`0.06s`)** |
| **Parallel Search Graph** | [**ai-multi-search-agent**](https://github.com/alhaj-ai/ai-multi-search-agent) | **9-node** parallel **LangGraph** retrieval & synthesis workflow aggregating Google, Bing, and Reddit SERP endpoints (`Streamlit`) | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/ai-multi-search-agent/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/ai-multi-search-agent/actions) **9-node topology CI** |
| **Intent Routing Graph** | [**mindRouter-agent**](https://github.com/alhaj-ai/mindRouter-agent) | Stateful **LangGraph** structured intent router dispatching full conversation state across specialized logical & therapist nodes | [![CI](https://img.shields.io/github/actions/workflow/status/alhaj-ai/mindRouter-agent/ci.yml?branch=main&style=flat-square&label=CI)](https://github.com/alhaj-ai/mindRouter-agent/actions) **Routing logic CI** |

---

## Connect & Collaborate

* **Email**: [ai.mohammed.alhaj@gmail.com](mailto:ai.mohammed.alhaj@gmail.com)
* **LinkedIn**: [linkedin.com/in/mohammed-mohammed-al-haj-341ab7369](https://linkedin.com/in/mohammed-mohammed-al-haj-341ab7369)
* **GitHub**: [@alhaj-ai](https://github.com/alhaj-ai)
* **X (Twitter)**: [@mod_alhaj](https://x.com/mod_alhaj)
* **Location**: Sana'a, Yemen (صنعاء، اليمن)

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0B1120,50:1E293B,100:0369A1&height=100&section=footer" width="100%" alt="Footer Wave" />
</div>
