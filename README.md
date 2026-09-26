<h1 align="center">Vishal Goyal</h1>

<p align="center">
  <b>Full-Stack AI · Backend · GenAI Engineer</b><br>
  <sub>Bangalore, India · open to relocation / remote</sub>
</p>

<p align="center">
  <a href="https://theknowledgeorbits.com"><img src="https://img.shields.io/badge/%F0%9F%8C%90_Live_Site-theknowledgeorbits.com-2ea44f?style=for-the-badge" alt="Live Site"></a>
  <a href="https://linkedin.com/in/vishalgoyal25"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:vishal25goyal25@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

<p align="center">
  <a href="https://buymeacoffee.com/vishalgoyal25"><img src="https://img.shields.io/badge/Buy%20Me%20a%20Coffee-FFDD00?style=flat-square&logo=buymeacoffee&logoColor=black" alt="Buy Me a Coffee"></a>
  <a href="https://ko-fi.com/vishalgoyal25"><img src="https://img.shields.io/badge/Ko--fi-FF5E5B?style=flat-square&logo=kofi&logoColor=white" alt="Ko-fi"></a>
</p>

---

Full-stack AI engineer who owns systems end to end — backend-first.

I have shipped **two live production AI systems solo**: a 16-engine AI platform with hybrid RAG, a LangGraph multi-agent research assistant and LLMOps instrumentation; and a conversational analytics platform built on a deterministic engine/AI separation. Python/Django foundation, backed by formal GenAI engineering training (IBM Professional Certificate). I design around engine isolation, async workers and vector retrieval.

I spent 2019–2024 preparing full-time for India's Civil Services Examination, then GATE through early 2025. I returned to software engineering in 2025 — and the first thing I built was the platform I wish I had while preparing.

---

## 🚀 What I've built

### 🌍 [TheKnowledgeOrbits](https://github.com/vishalgoyal25/TheKnowledgeOrbits) — AI-Native UPSC Prep Platform
**Live:** [theknowledgeorbits.com](https://theknowledgeorbits.com) · Built solo, end to end

<p>
  <img src="https://img.shields.io/badge/Django-092E20?logo=django&logoColor=white" alt="Django">
  <img src="https://img.shields.io/badge/Next.js-000000?logo=nextdotjs&logoColor=white" alt="Next.js">
  <img src="https://img.shields.io/badge/LangGraph-1C3C3C?logo=langchain&logoColor=white" alt="LangGraph">
  <img src="https://img.shields.io/badge/pgvector-4169E1" alt="pgvector">
  <img src="https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white" alt="Redis">
  <img src="https://img.shields.io/badge/Langfuse-0A0A0A" alt="Langfuse">
  <img src="https://img.shields.io/badge/DeepEval-8B5CF6" alt="DeepEval">
</p>

- Architected a **modular monolith of 16 isolated Django domain engines** — each owns its models and communicates only via internal APIs, giving independent domain ownership without the operational overhead of microservices.
- Built a **hybrid RAG pipeline** — semantic (pgvector cosine) and lexical (BM25) retrieval fused via **Reciprocal Rank Fusion**, with a relevance gate and TopicRelation graph expansion.
- Built the **research_agent** — a 7-node LangGraph multi-agent workflow running in a django-background-tasks worker to bypass Render's 30s HTTP timeout, streaming live progress to the frontend over SSE.
- Integrated **LLMOps and AgentOps**: Langfuse tracing, DeepEval evaluations, a Redis-backed rate limiter, structlog logging, Sentry tracking, and LLM pooling across multiple providers.

### 📊 [DashBoards](https://github.com/vishalgoyal25/DashBoards) — Conversational Analytics Platform
**Built solo, end to end**

<p>
  <img src="https://img.shields.io/badge/Django-092E20?logo=django&logoColor=white" alt="Django">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/GCP_Cloud_Run-4285F4?logo=googlecloud&logoColor=white" alt="Cloud Run">
  <img src="https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white" alt="Docker">
</p>

- Designed the system so a **deterministic Pandas/SQL engine handles all computation**, with the LLM used only to interpret intent and narrate results — keeping analytical output reproducible.
- Built a **multi-key LLM pool** (round-robin with per-key cooldown) and a **5-layer input-validation guard** behind an SSE streaming chat interface.
- Solved real production failures: DB connection exhaustion on serverless, OOM on 51k-row datasets, and a WIF auth failure caused by repo-name case sensitivity.
- Deployed on **GCP Cloud Run** with **keyless CI/CD** via GitHub Actions and Workload Identity Federation.

### 🧠 [Multi-Agent RAG Research Platform](https://github.com/vishalgoyal25/Multi_Agent_RAG)
**Built solo, end to end**

<p>
  <img src="https://img.shields.io/badge/LangGraph-1C3C3C?logo=langchain&logoColor=white" alt="LangGraph">
  <img src="https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white" alt="FastAPI">
  <img src="https://img.shields.io/badge/ChromaDB-FF6B6B" alt="ChromaDB">
  <img src="https://img.shields.io/badge/RAGAS-22C55E" alt="RAGAS">
</p>

- A **Planner** routes each question to a cheap single-search path or fans out parallel **Researchers**; a **Synthesizer** merges cited findings or abstains; a **Critic** verifies every claim against retrieved evidence before a human approves the answer.
- **Dynamic parallel fan-out** via LangGraph's Send API with bounded retry and escalation cycles — every loop hard-capped in code — plus **human-in-the-loop approval with durable on-disk checkpointing** that resumes exactly where it paused.
- **Citations validated in code** against the chunks actually retrieved; fabricated or out-of-context citations are rejected, forcing an honest abstain. Quality scored with RAGAS.

---

## 🛠 Tech

**Languages & Core** &nbsp;
`Python` `TypeScript` `SQL`

**Backend** &nbsp;
`Django` `DRF` `FastAPI` `Flask` `REST APIs` `RBAC` `Async workers`

**Frontend** &nbsp;
`Next.js` `React` `Tailwind CSS` `shadcn/ui` `React Flow`

**AI / GenAI** &nbsp;
`LangGraph` `Hybrid RAG` `Embeddings` `Prompt Engineering` `Langfuse` `DeepEval` `RAGAS` `Tool Calling`

**Data** &nbsp;
`PostgreSQL` `pgvector` `FAISS` `Redis` `Pandas` `NumPy` `Scikit-learn`

**Infra & DevOps** &nbsp;
`Docker` `GCP` `GitHub Actions` `Render` `Vercel` `Supabase` `Sentry` `structlog` `Linux`

---

## 📈 Activity

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=vishalgoyal25&show_icons=true&hide_border=true&theme=tokyonight&count_private=true" alt="GitHub stats">
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=vishalgoyal25&layout=compact&hide_border=true&theme=tokyonight&langs_count=8" alt="Top languages">
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com/?user=vishalgoyal25&hide_border=true&theme=tokyonight" alt="Contribution streak">
</p>

---

## 🎓 Training & Achievements

- **IBM Generative AI Engineering Professional Certificate** — Coursera, 16 courses
- **IBM RAG and Agentic AI Professional Certificate** — Coursera, 10 courses *(in progress)*
- **MLOps Bootcamp** (10 end-to-end projects) · **GenAI with LangChain & HuggingFace** · **Data Science / ML / DL / NLP Bootcamp** — Udemy
- **Python for Everybody Specialization** — University of Michigan · **Python & Statistics for Financial Analysis** — HKUST
- 🏅 Qualified **GATE 2025** — Computer Science & Engineering
- 🏅 Qualified **GATE 2025** — Data Science & Artificial Intelligence
- 🏅 **AIR 4048** — GATE 2017, Computer Science & Engineering

**B.Tech, Computer Science & Engineering** — Jaipur Engineering College and Research Centre

---

## ❤️ Support the Code

Everything above is built and maintained solo, in the open. If any of it helped you, you can buy me a coffee — entirely voluntary.

<p>
  <a href="https://buymeacoffee.com/vishalgoyal25"><img src="https://img.shields.io/badge/Buy%20Me%20a%20Coffee-FFDD00?style=for-the-badge&logo=buymeacoffee&logoColor=black" alt="Buy Me a Coffee"></a>
  <a href="https://ko-fi.com/vishalgoyal25"><img src="https://img.shields.io/badge/Ko--fi-FF5E5B?style=for-the-badge&logo=kofi&logoColor=white" alt="Ko-fi"></a>
</p>

---

<p align="center"><sub>Backend-first. Production from day one.</sub></p>
