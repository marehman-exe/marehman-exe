<h1 align="center">Hi, I'm Muhammad Abdur Rehman 👋</h1>

<h3 align="center">AI Engineer | Data & ML Practitioner | Building at the intersection of data, AI & backend engineering</h3>

<p align="center">
  <a href="https://www.linkedin.com/in/marehmandev">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white" />
  </a>
  <a href="mailto:abdurrehmanm778@gmail.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white" />
  </a>
  <img src="https://img.shields.io/badge/Location-Faisalabad%2C%20Pakistan-2563EB?style=flat" />
</p>

---

### 🎯 About Me

I'm interested in what happens when **data meets AI**. My journey started in data analysis and e-commerce, learning how data drives real business decisions, and gradually led me toward AI and software engineering.

Currently working as an **AI Engineer**, building predictive ML models, automated data pipelines, and hardware-software integrations, while finishing my Computer Science degree.

I'm focused on:

- 🤖 **AI & Machine Learning**
- 🐍 **Python, SQL & Backend Engineering**
- 🔗 **RAG & LLM Applications**
- 📊 **Data Analysis & Automation**

Still learning, building, and experimenting, one practical project at a time.

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

**[LexBase](https://github.com/marehman-exe/Lexbase)**  
A production-grade, multi-tenant RAG system built for law firms. Hybrid semantic + keyword search over private PDF libraries, grounded AI summaries with numbered citations, and full role-based access control. Built across 11 milestones over ~2 weeks of intensive engineering.

**[SightShield](https://github.com/marehman-exe/SightShield)**  
An AI-empowered wearable smart belt for visually impaired individuals, built on Raspberry Pi with real-time object detection and hardware sensor integration. My Final Year Project, combining embedded systems with assistive AI.

---

### 🧠 LexBase — What I Learned

Building LexBase across 11 milestones gave me hands-on experience with the full stack of a production RAG system. Key areas covered:

- **RAG & Vector Search** — local embeddings (`BAAI/bge-small-en-v1.5`), pgvector HNSW index, hybrid Reciprocal Rank Fusion (vector cosine + BM25 keyword), relevance floor tuning

- **Backend Engineering** — FastAPI route design, SQLAlchemy 2.0 typed ORM, Alembic migrations, multi-tenant SQL isolation (`firm_id` scoping at every query)

- **Auth & Security** — JWT HS256 with refresh token rotation, hashed token storage, timing-oracle prevention, IDOR prevention, rate limiting, CORS hardening, upload security (magic bytes + UUID filenames)

- **LLM Integration** — pluggable provider abstraction (Groq / OpenRouter / Ollama), citation validation, prompt injection defense, hallucination suppression via grounded-only answers

- **Frontend** — React 19 + TypeScript + TanStack Query, silent 401 token refresh with request queue, role-based navigation guards, persistent research history

- **Production Thinking** — trade-off analysis between MVP choices (BackgroundTasks, local disk, single DB) and production equivalents (Celery, S3, read replicas, OpenTelemetry)

---

### 📊 Machine Learning & NLP Portfolio

A set of applied ML/NLP case studies, each following the same workflow:

**business question → data inspection → feature engineering & leakage review → model tuning & evaluation → responsible-use analysis**

| Project | Focus | Techniques |
|---|---|---|
| [Waze User Churn Prediction](https://github.com/marehman-exe/Wase---User-Churn-Prediction) | Predicting user churn from behavioral data (~15K records) | Random Forest, XGBoost, recall-focused evaluation |
| [TikTok Claim vs. Opinion Classification](https://github.com/marehman-exe/Tiktok---Claim-and-Opinion-Classification) | Content review prioritization (~19.4K records) | Metadata-based classification, train/val/test design |
| [Generous Tip Prediction](https://github.com/marehman-exe/Automatidata---Generous-Tip-Prediction) | NYC taxi tipping behavior (~22.7K records) | Leakage-aware feature engineering, GridSearchCV |
| [Arabic Small Language Model](https://github.com/marehman-exe/Google-DeepMind---Train-A-Small-Language-Model) | Character-level Arabic NLP | Tokenization, n-gram modeling, sequence prep |

*Built as capstone projects for **The Nuts and Bolts of Machine Learning** certification, evaluated and documented with that scope in mind, including responsible-use limitations for each.*

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
