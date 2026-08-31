# Hi, I'm Mohammad Abdullah 👋

Computer Science undergraduate at **Canadian University Dubai** (GPA: 3.97) with hands-on experience in **data engineering, full-stack development, machine learning, computer vision, and LLM-powered applications**.

I build end-to-end systems — from orchestrated cloud data pipelines and deployed multi-user web services to object detection models — and I'm comfortable across the whole workflow: infrastructure as code, ELT modelling, API design, controlled experimentation, and quantitative evaluation.

📫 [LinkedIn](https://www.linkedin.com/in/abdulla1x/) • [Email](mailto:m.abdulla992003@gmail.com)

---

## 🛠 Technical Stack

**Languages:** Python • TypeScript • JavaScript • Java • SQL • C++ • Prolog • Lisp

**Data Engineering:** Apache Airflow • dbt • BigQuery • Google Cloud Storage • Terraform • Docker Compose • Elementary • Looker Studio

**ML & Computer Vision:** YOLOv8 • PyTorch • scikit-learn • pandas • NumPy • Transfer Learning • Object Detection

**AI & Automation:** Gemini • Groq (Llama 3.3) • Ollama (DeepSeek-R1) • FAISS • Browser Automation

**Frameworks & Tools:** FastAPI • React • Tailwind CSS • Streamlit • Git • GitHub Actions • pytest • Playwright • Roboflow • Google Colab

**Databases:** PostgreSQL • SQLAlchemy • BigQuery • SQLite

**Cloud & Deployment:** Google Cloud Platform • Vercel • Render • Neon

---

## 🚀 Featured Projects

### 🌍 [OpenAQ Air-Quality Data Pipeline](https://github.com/Abdulla1x/openaq-pipeline) — [Live Dashboard](https://datastudio.google.com/reporting/7c88238c-c153-4c64-bf5b-c1974f859158/page/9Fj4F)
`Python` `Airflow` `dbt` `BigQuery` `Terraform` `Docker` `Looker Studio`

Batch data pipeline ingesting air-quality data from the OpenAQ v3 API, comparing the UAE and Pakistan on PM2.5 against WHO 2021 guidelines.
- Backfilled **1.8M measurements** in resumable 60-day chunks, each count-reconciled against the API before it is checkpointed
- An **Airflow** DAG fans out one dynamically-mapped task per sensor behind a rate-limit pool; a Dataset event then schedules a **dbt** transform DAG that astronomer-cosmos renders as one Airflow task per model
- staging → daily aggregates → WHO-exceedance marts across **121 dbt nodes and 83 data tests**, with every GCP resource provisioned by **Terraform** and five required CI checks on `main`
- The finding: Pakistan's PM2.5 exceeded the WHO 24-hour guideline on **100% of 455 shared days** (mean 75 µg/m³) against the UAE's **94%** (mean 37 µg/m³) — published alongside the coverage gap that qualifies it, ~180 reporting stations a day versus ~8

---

### 🥗 [Macros Calculator](https://github.com/Abdulla1x/Macros-Calculator) — [Live App](https://macros-calculator-mu.vercel.app)
`React 19` `TypeScript` `FastAPI` `PostgreSQL` `SQLAlchemy` `Gemini`

Multi-user nutrition tracking app, rebuilt from a single-user Streamlit prototype into a decoupled frontend/backend architecture — the original still lives in `legacy/`.
- **React 19 + TypeScript** SPA, installable as a PWA, over a **FastAPI + SQLAlchemy** REST API on **PostgreSQL** — 50 endpoints, every one scoped to the authenticated user
- Argon2id password hashing, JWT bearer tokens and per-IP rate limiting; cross-tenant isolation proved twice over, by 49 in-process tests and a 127-check smoke script fired at a *running* server
- **AI meal analysis** from a photo, a voice note or a typed description — estimates come back as calorie and macro *ranges* with per-ingredient confidence, and the accuracy report refuses to answer where the sample is too small to answer honestly
- **725 tests** behind a five-gate CI pipeline; 21 shipped phases; deployed on Vercel + Render + Neon

---

### 🎮 [Game Dashboard](https://github.com/Abdulla1x/game-dashboard)
`Python` `Standard Library` `HTTP` `Windows`

One place to see and launch every game on a Windows PC — Steam, Epic, Xbox, Riot, and the loose folders that belong to no launcher at all — with real cover art for all of them.
- **Pure Python 3 standard library**: no pip install, no npm, no build step, and nothing in the cloud
- Runs a small HTTP server on `127.0.0.1` and opens a browser window at it; launcher detection, executable heuristics and icon extraction are all hand-rolled

---

### 🎯 [AI Campus Safety Detection System](https://github.com/Abdulla1x/BCS407_Project)
`Python` `YOLOv8` `Roboflow` `PyTorch` `Google Colab`

Trained a YOLOv8s object detection model on a custom 2,069-image campus dataset to detect fire alarms, wet floor signs, emergency exits, and safety helmets in real time.
- Achieved **96.8% mAP@0.50** after diagnosing class imbalance and consolidating exit sub-classes (+15.8 pp improvement)
- Ran 3 controlled improvement experiments; hyperparameter tuning was the best strategy (**94.52% mAP** on test set)
- End-to-end pipeline: Roboflow annotation → COCO transfer learning → 10.4ms/frame inference

---

### 🚕 NYC Yellow Taxi Data Mining Pipeline
`Python` `Pandas` `scikit-learn`

End-to-end ETL pipeline covering ingestion, profiling, cleaning, feature engineering, and classification modeling on large-scale taxi trip data — achieving **97% prediction accuracy**.

---

### 🤖 [CUD Course Scraper](https://github.com/Abdulla1x/CourseScraping-BU)
`Python` `Streamlit` `Gemini LLM` `Ollama DeepSeek-R1` `Browser Automation`

AI-powered browser automation tool that logs into the CUD student portal, scrapes course offerings, and enables natural language queries via integrated LLMs.

---

### 🏙️ [Chicago City Data Analysis](https://github.com/Abdulla1x/sql-assessments)
`SQL`

Multi-dataset SQL analysis exploring correlations between community hardship, crime rates, and school performance — including views, stored procedures, and transaction management.

---

### 💊 [AI Medication Reminder](https://github.com/Abdulla1x/AI-Medication-Remainder)
`Python` `Streamlit` `Gemini LLM` `APScheduler` `SWI-Prolog`

Natural language medication scheduling app using Gemini LLM for input parsing, APScheduler for automated reminders, and Prolog logic rules for drug interaction safety checks.

---

## 🔨 Currently Building

### hybrid-rag-agent
`Python` `FAISS` `sentence-transformers` `Groq` `FastAPI`

A research assistant over a local corpus of AI/ML papers. An agent decides, per query, whether to answer from the papers (dense retrieval over a FAISS index) or from a live web search — the routing decision is the point of the project.

Deliberately **no RAG frameworks** — no LangChain, no LlamaIndex. The chunker, the embedding and indexing step, retrieval, the ReAct loop and tool dispatch are all written directly; libraries are used only for primitives. Every model call goes through one entry point, so swapping Llama 3.3 70B on Groq for a local Ollama server is a one-file change.

**Status:** the PDF ingestion and text-cleaning layer is built. Chunking, the FAISS index, retrieval, the agent loop, the evaluation harness and the API are still to come.

### LiteMP — Minecraft server & control panel

A PaperMC server and a custom web control panel running on a headless Ubuntu mini PC at home, for a handful of friends. PaperMC under **systemd**, a Python control panel served over HTTPS behind **nginx**, **Tailscale** for remote administration, and scripted backups with off-box copies.

*No public repo — the repository is a private server backup rather than a portfolio project.*

---

## 🎓 Algorithm Visualizations

Interactive browser-based tools built for BCS 309 – Algorithms I. No dependencies — pure HTML, CSS, and vanilla JavaScript, deployed on GitHub Pages.

### 📦 [Subset Sum — Interactive Teaching Tool](https://github.com/Abdulla1x/subset-sum) — [Live Demo](https://abdulla1x.github.io/subset-sum/)
`HTML` `CSS` `Vanilla JavaScript`

Six-section interactive lecture covering brute force O(n·2ⁿ), dynamic programming O(n·t), pseudo-polynomial complexity, and a formal NP-completeness proof via 3-SAT reduction. Three visualization modes: DP table animation, brute force bitmask walkthrough, and side-by-side comparison with live operation counters.

---

### 🌳 [Huffman Coding — Interactive Visualization](https://github.com/Abdulla1x/huffman-visualization) — [Live Demo](https://abdulla1x.github.io/huffman-visualization/)
`HTML` `CSS` `Vanilla JavaScript`

Step-by-step visualization of the Huffman coding algorithm — min-heap construction, greedy merges, tree building, and code generation. Includes encode/decode, complexity comparison charts (Huffman vs Shannon-Fano vs Arithmetic), and an exchange-argument proof of greedy optimality.

---

## 📜 Certifications
- **Introduction to Modern AI** — Cisco Networking Academy (Apr 2026)
- **Databases and SQL for Data Science with Python** — IBM, Coursera (Jul 2024)
- **C Essentials 1** — Cisco Networking Academy (Apr 2026)
- **What is Data Science?** — IBM, Coursera (Dec 2023)
