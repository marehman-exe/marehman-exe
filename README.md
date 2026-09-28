<h1 align="center">Hi, I'm Muhammad Abdur Rehman 👋</h1>
<h3 align="center">AI Engineer | Data & ML Practitioner | Building at the intersection of data, AI & backend engineering</h3>

<p align="center">
  <a href="https://www.linkedin.com/in/marehmandev"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:abdurrehmanm778@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white" /></a>
  <img src="https://img.shields.io/badge/Location-Faisalabad%2C%20Pakistan-2563EB?style=flat" />
</p>

---

### 🎯 About Me

I'm interested in what happens when **data meets AI**. My journey started in data analysis and e-commerce — learning how data drives real business decisions — and gradually led me toward AI and software engineering.

Currently working as an **AI Engineer**, building predictive ML models, automated data pipelines, and hardware-software integrations, while finishing my Computer Science degree.

I'm focused on:
- 🤖 **AI & Machine Learning**
- 🐍 **Python, SQL & Backend Engineering**
- 🔗 **RAG & LLM Applications**
- 📊 **Data Analysis & Automation**

Still learning, building, and experimenting — one practical project at a time.

---

### 🛠️ Tech Stack

**Languages & Data**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)

**Machine Learning & AI**
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-018080?style=flat)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white)
![Claude API](https://img.shields.io/badge/Claude%20API-D97757?style=flat)
![Groq](https://img.shields.io/badge/Groq-000000?style=flat)

**Backend & Infrastructure**
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-4169E1?style=flat)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Alembic](https://img.shields.io/badge/Alembic-333333?style=flat)

**Frontend**
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat&logo=vite&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat&logo=tailwindcss&logoColor=white)
![TanStack Query](https://img.shields.io/badge/TanStack_Query-FF4154?style=flat)

**Tools & Platforms**
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-A22846?style=flat&logo=raspberrypi&logoColor=white)

---

### 🚀 Featured Projects

**[LexBase](https://github.com/marehman-exe/Lexbase)** — A production-grade, multi-tenant RAG system built for law firms. Hybrid semantic + keyword search over private PDF libraries, grounded AI summaries with numbered citations, and full role-based access control. Built across 11 milestones over ~2 weeks of intensive engineering.

**[SightShield](https://github.com/marehman-exe/SightShield)** — An AI-empowered wearable smart belt for visually impaired individuals, built on Raspberry Pi with real-time object detection and hardware sensor integration. My Final Year Project, combining embedded systems with assistive AI.

---

### 🧠 LexBase — Skills Learned

LexBase was a deliberate engineering training programme. Each milestone introduced one layer of a production RAG system and forced me to understand it from first principles. Below is a summary of what I built and what I learned at each layer.

---

#### M0 — Environment & Tooling
- How Docker named volumes persist data independently of containers — changing credentials in `docker-compose.yml` has no effect until the volume is deleted
- Why `normalize_embeddings=True` produces unit vectors, making dot product equivalent to cosine similarity with no extra division

#### M1 — Data Model & Migrations
- The difference between a Python enum `.name` (uppercase identifier) and `.value` (stored string) — and why SQLAlchemy sends the name by default, breaking PostgreSQL case-sensitive enums (fixed with `values_callable`)
- How Windows PowerShell's `Out-File` writes a UTF-8 BOM that silently corrupts `.env` key names (`DATABASE_URL` becomes `﻿DATABASE_URL`)
- Why database migrations must include the `CREATE EXTENSION vector` step — anything done manually outside Alembic cannot be reproduced on a fresh machine

#### M2 — Authentication & RBAC
- The JWT payload is Base64-encoded JSON readable by anyone, but tamper-proof via HMAC-SHA256 signature — confidentiality is not required, integrity is
- Why refresh tokens are stored hashed: a plain-text token in a leaked database lets an attacker immediately issue new access tokens; the hash is useless without the original
- How token rotation works as a theft-detection mechanism: whichever party (legitimate user or attacker) rotates first invalidates the other's token on the next request
- Why timing oracles matter: returning early for unknown emails makes the login endpoint measurably faster, allowing enumeration — always run bcrypt even against a dummy hash

#### M3 — Frontend Shell
- Vite reads `.env` once at startup — changes require a dev server restart, not just a page reload
- Why `CORSMiddleware` must be added before routers: a preflight OPTIONS request must reach the CORS handler before hitting a router that has no OPTIONS handler and returns 405
- `localStorage` persists across tab closes, browser restarts, and F5 — only "Clear site data" removes it

#### M4 — Account & Team Management
- Why `firm_id` must come from the JWT signature rather than the request body — the JWT signature is the only server-controlled mechanism that prevents IDOR (Insecure Direct Object Reference) attacks
- Why a cross-firm deactivation attempt should return 404, not 403 — 403 confirms the resource exists, which is cross-tenant information leakage

#### M5 — Document Ingestion Pipeline
- Why chunking uses token count, not character count: embedding models (BGE-small: 384 tokens) silently truncate the tail of oversized inputs — the stored vector would not represent the full chunk
- Why chunk overlap exists: semantic boundaries rarely align with document structure; a sentence spanning two chunks without overlap would be split, making neither chunk fully answerable
- Why files are stored under UUID names: the client-supplied filename is untrusted (`../../../etc/passwd` is a path traversal attack); a UUID is unguessable and safe on disk
- Why background ingestion needs its own `SessionLocal()`: the request handler's session is closed before the background task runs

#### M6 — Embeddings & Vector Search
- The BGE query prefix asymmetry: passages are indexed without a prefix; queries use `"Represent this sentence for searching relevant passages:"` — the model was trained on asymmetric pairs, and using the prefix on passage embeddings reduces quality
- pgvector's `<=>` operator returns *distance* (0 = identical), not similarity; HNSW approximates nearest neighbours and the planner defaults to a sequential scan on small tables

#### M7 — Hybrid Search (RRF)
- How Reciprocal Rank Fusion (`score = Σ 1/(k+rank)`, k=60) fuses vector and keyword results: a chunk in the top-5 of both legs scores higher than a chunk at rank 1 in only one leg; k=60 was chosen by the original authors to reduce sensitivity to outlier ranks
- How GIN (Generalized Inverted Index) stores pre-processed tsvector tokens for fast full-text matching — the same inverted index structure used in search engines
- Where hybrid improves over vector-only: exact identifiers like section numbers, clause numbers, and verbatim legal terms that vector similarity ranks too low (evaluation: 6 Good → 8 Good on 10 legal questions)

#### M8 — LLM Generation & Guardrails
- Why temperature 0.1 is the right choice for a legal tool: determinism is a feature — the same query should return the same citations
- Why retrieved passages go in the *user message*, not the *system prompt*: a document containing "IGNORE ALL PREVIOUS INSTRUCTIONS" is treated as data in the user message; the same text in the system prompt could interfere with the model's operating rules
- Why citation validation is the only automated hallucination check available: if the model cannot produce a `[N]` citation pointing to a real retrieved passage, the answer is suppressed and raw passages are shown instead
- Qwen thinking models emit `<think>...</think>` blocks in their response — disabled via `reasoning_effort: none` and stripped defensively by `_strip_thinking()` as a second pass
- Red-team result: all 4 completed attack vectors (off-corpus question, prompt injection in query, prompt injection inside a passage, role bypass) were blocked

#### M9 — Research Interface
- The 401 token refresh race condition in SPAs: without a request queue, 3 concurrent API calls on token expiry each attempt their own refresh — only the first succeeds; the other two burn the already-rotated token. Fix: a pending flag and a request queue — all callers wait for the single refresh to complete, then retry
- JavaScript regex with the `g` flag maintains internal `lastIndex` state — calling `.test()` on the same regex object inside `.map()` causes alternating calls to fail; fix: create a new regex without `g` for type guards

#### M10 — Hardening & Handover
- Why circular imports occur in Python: module A imports from B, B imports from A — Python's lazy import system uses the partially-initialised module, missing the symbol being imported. Fix: extract the shared object (`limiter`) into a third module
- Why correlation IDs (`X-Request-ID`) are essential: without one, finding a specific failed request in server logs requires timestamp-based guessing; with one, a single grep surfaces every log line for that exact request
- TF-IDF scores terms higher when they appear frequently in a specific document but rarely across all documents — making it a "what is this document about" signal without any LLM cost
- Why a committed API key is still compromised after replacing it in the file: git history preserves the old value; the key must be revoked in the provider dashboard

#### M11 — Persistent Chat History
- Research sessions (query + passages + optional AI answer) are persisted in a `chat_history` PostgreSQL table, scoped per user and firm
- The Research Page drawer loads the last 7 days of sessions on mount — history survives page refreshes, browser restarts, and device switches

---

#### Architecture Decisions & Scale Considerations

| Decision | MVP Choice | Production Fix |
|---|---|---|
| Document ingestion | FastAPI `BackgroundTasks` (in-process) | Celery + Redis (durable, retryable, scalable workers) |
| File storage | Local disk (`uploads/`) | S3 / MinIO (two touch-points: `save_file` + `delete_file`) |
| Database | Single PostgreSQL instance | Read replica for search queries (CPU-intensive HNSW) |
| HNSW index | Incremental inserts | Nightly `REINDEX INDEX CONCURRENTLY` at millions of chunks |
| Logging | uvicorn stdout + `X-Request-ID` | structlog + OpenTelemetry SDK → Jaeger / Grafana Tempo |

---

### 📊 Machine Learning & NLP Portfolio

A set of applied ML/NLP case studies, each following the same workflow — business question → data inspection → feature engineering & leakage review → model tuning & evaluation → responsible-use analysis:

| Project | Focus | Techniques |
|---|---|---|
| [Waze User Churn Prediction](https://github.com/marehman-exe/Wase---User-Churn-Prediction) | Predicting user churn from behavioral data (~15K records) | Random Forest, XGBoost, recall-focused evaluation |
| [TikTok Claim vs. Opinion Classification](https://github.com/marehman-exe/Tiktok---Claim-and-Opinion-Classification) | Content review prioritization (~19.4K records) | Metadata-based classification, train/val/test design |
| [Generous Tip Prediction](https://github.com/marehman-exe/Automatidata---Generous-Tip-Prediction) | NYC taxi tipping behavior (~22.7K records) | Leakage-aware feature engineering, GridSearchCV |
| [Arabic Small Language Model](https://github.com/marehman-exe/Google-DeepMind---Train-A-Small-Language-Model) | Character-level Arabic NLP | Tokenization, n-gram modeling, sequence prep |

*Built as capstone projects for **The Nuts and Bolts of Machine Learning** certification — evaluated and documented with that scope in mind, including responsible-use limitations for each.*

---

### 🎓 Certifications

- The Nuts and Bolts of Machine Learning
- Data Science & Analytics
- Python Data Analytics
- Building with the Claude API
- Critical Thinking in the AI Era

---

### 📈 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=marehman-exe&show_icons=true&theme=default&hide_border=true" width="48%" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=marehman-exe&layout=compact&hide_border=true" width="42%" />
</p>

---

### 📫 Let's Connect

<p align="center">
  <a href="https://www.linkedin.com/in/marehmandev">LinkedIn</a> ·
  <a href="mailto:abdurrehmanm778@gmail.com">Email</a> ·
  <a href="https://github.com/marehman-exe">GitHub</a>
</p>
