# Hi, I'm Mohammad Abdullah 👋

Fourth-year Computer Science student at **Canadian University Dubai** (GPA 3.97, graduating Dec 2027). I build **applied AI and LLM features, cloud data pipelines and machine-learning models**, and I don't stop at "it runs": I measure whether the numbers are right.

In practice that means scoring an AI model's estimates against what users actually saved, reconciling every backfilled chunk of a pipeline against its source, and publishing the coverage gap next to the finding it qualifies.

📫 [LinkedIn](https://www.linkedin.com/in/abdulla1x/) • [Email](mailto:m.abdulla992003@gmail.com)

---

## 🛠 Technical Stack

**Languages:** Python • TypeScript • JavaScript • Java • SQL • C++ • Prolog • Lisp

**Data Engineering:** Apache Airflow • dbt • BigQuery • Google Cloud Storage • Terraform • Docker Compose • Elementary • Looker Studio

**ML & Computer Vision:** YOLOv8 • PyTorch • scikit-learn • pandas • NumPy • Transfer Learning • Object Detection

**AI & Automation:** Gemini • Ollama (DeepSeek-R1) • browser-use

**Frameworks & Tools:** FastAPI • React • Tailwind CSS • Streamlit • Git • GitHub Actions • pytest • Playwright • Roboflow • Google Colab

**Databases:** PostgreSQL • SQLAlchemy • BigQuery • SQLite

**Cloud & Deployment:** Google Cloud Platform • Vercel • Render • Neon • Resend

---

## 🚀 Featured Projects

### 🥗 [Trackaholic](https://github.com/Abdulla1x/Trackaholic) — [Live App](https://trackaholic.app) — [The Story](https://story.trackaholic.app/?ref=gh-profile)
`React 19` `TypeScript` `FastAPI` `PostgreSQL` `SQLAlchemy` `Gemini` `PWA`

A deployed **multi-user** calorie and macro tracker, formerly *Macros Calculator*. It started in 2024 as a single-user Streamlit prototype and was rebuilt as a React SPA over a FastAPI REST API. **200+ merged PRs · 1,600+ tests · 55 API paths · six-gate CI.**
- **Multimodal AI meal analysis** (Gemini) — describe a meal, record a voice note, or photograph it. A voice note becomes editable text *before* anything is estimated, so a misheard ingredient is a typo to fix, not a wrong number to catch. Results are calorie and macro **ranges** with per-ingredient confidence, never a false-precision single number
- **Your foods, the AI's eyes:** attach saved foods and their macros are sent as facts — **the AI estimates the portion, your library supplies the macros.** A photo with no note is asked about hidden oil and sauces first, because on 14 weighed meals every model tested read a photo alone low, by a median of 53–64% of the true calories
- **The model's accuracy is measured, not assumed.** Every estimate is logged and compared against what the user actually saved — interval coverage and directional bias per macro, with sample sizes — and it **refuses to report** where the evidence is too thin
- **Food search over 26,000 foods from five national tables** (USDA, UK, France, Australia, Canada) plus Open Food Facts, ranked by its own in-memory search: the plain food is in the top 3 for **92%** of a 25-food benchmark, and CI fails if a change drops that below 90%
- **Targets from sources, not round numbers:** a one-question-per-screen setup whose every limit cites a primary source (FAO/WHO/UNU activity data, sourced loss and gain caps), a **daily burn measured from energy balance** once there is enough data, calorie banking between days, and an eight-check **weekly review** where every figure carries its own window and sample size
- Argon2id + JWT auth, per-IP rate limiting, and password reset by email; **cross-tenant isolation proved twice** — 51 in-process tests and a smoke script of 100+ live checks fired at a *running* server
- Redesigned installable **PWA** — light and dark, nine palettes and a nutrition-label style — with **zero WCAG 2.2 A/AA violations** in an axe-core audit of all 37 routes at two widths; on Vercel + Render + Neon with Alembic migrations on every deploy

*Engineering write-ups: [a three-day AI outage, traced to the server's region](https://github.com/Abdulla1x/Trackaholic/blob/main/docs/incident-2026-07-gemini-eea-region.md) · [picking a photo size with an A/B instead of a hunch](https://github.com/Abdulla1x/Trackaholic/blob/main/docs/photo-size-ab-2026-10.md) · [setting a calorie target from sources](https://github.com/Abdulla1x/Trackaholic/blob/main/docs/goal-setting-rules.md). Full feature list, architecture and screenshots in the [project README](https://github.com/Abdulla1x/Trackaholic#readme).*

---

### 🌍 [OpenAQ Air-Quality Data Pipeline](https://github.com/Abdulla1x/openaq-pipeline) — [Live Dashboard](https://datastudio.google.com/reporting/7c88238c-c153-4c64-bf5b-c1974f859158/page/9Fj4F)
`Python` `Airflow` `dbt` `BigQuery` `Terraform` `Docker` `Looker Studio`

Batch data pipeline ingesting air-quality data from the OpenAQ v3 API, comparing the UAE and Pakistan on PM2.5 against WHO 2021 guidelines.
- Backfilled **1.8M measurements** in resumable 60-day chunks, each count-reconciled against the API before it is checkpointed
- An **Airflow** DAG fans out one dynamically-mapped task per sensor behind a rate-limit pool; a Dataset event then schedules a **dbt** transform DAG that astronomer-cosmos renders as one Airflow task per model
- staging → daily aggregates → WHO-exceedance marts across **121 dbt nodes and 83 data tests**, with every GCP resource provisioned by **Terraform** and five required CI checks on `main`
- The finding: Pakistan's PM2.5 exceeded the WHO 24-hour guideline on **100% of 455 shared days** (mean 75 µg/m³) against the UAE's **94%** (mean 37 µg/m³) — published alongside the coverage gap that qualifies it, ~180 reporting stations a day versus ~8

---

### 🎯 [AI Campus Safety Detection System](https://github.com/Abdulla1x/BCS407_Project)
`Python` `YOLOv8` `Roboflow` `PyTorch` `Google Colab`

Trained a YOLOv8s object detection model on a custom 2,069-image campus dataset to detect fire alarms, wet floor signs, emergency exits, and safety helmets in real time.
- Achieved **96.8% mAP@0.50** after diagnosing class imbalance and consolidating exit sub-classes (+15.8 pp improvement)
- Ran 3 controlled improvement experiments; hyperparameter tuning was the best strategy (**94.52% mAP** on test set)
- End-to-end pipeline: Roboflow annotation → COCO transfer learning → 10.4ms/frame inference

---

### 🎮 [Game Dashboard](https://github.com/Abdulla1x/game-dashboard)
`Python` `Standard Library` `HTTP` `Windows`

One place to see and launch every game on a Windows PC — Steam, Epic, Xbox, Riot, and the loose folders that belong to no launcher at all — with real cover art for all of them.
- **Pure Python 3 standard library**: no pip install, no npm, no build step, and nothing in the cloud
- Runs a small HTTP server on `127.0.0.1` and opens a browser window at it; launcher detection, executable heuristics and icon extraction are all hand-rolled

---

### 🧱 LiteMP — Minecraft Server & Control Panel
`Python` `Linux` `systemd` `nginx` `Tailscale`

A PaperMC Minecraft server and a custom web control panel running on a headless Ubuntu mini PC at home, for a handful of friends.
- PaperMC under **systemd**, with a Python control panel served over HTTPS behind **nginx** — start/stop, live console, player management, plugin installs and metrics from a browser
- **Tailscale** for remote administration, a tunnel for friends to connect through, and scripted backups with off-box copies

*No public repository — the repo is a private server backup rather than a portfolio project.*

---

## 🧩 Smaller Projects

- 🚕 **NYC Yellow Taxi Data Mining Pipeline** — `Python` `pandas` `scikit-learn` — ETL over large-scale trip data (profiling, cleaning, feature engineering) feeding classification models at **~97% accuracy**
- 🤖 **[CUD Course Scraper](https://github.com/Abdulla1x/CourseScraping-BU)** — `Python` `browser-use` `Gemini` `Ollama DeepSeek-R1` `Streamlit` — LLM-driven browser automation that logs into the CUD student portal and scrapes course offerings into a searchable, filterable Streamlit table
- 🏙️ **[Chicago City Data Analysis](https://github.com/Abdulla1x/sql-assessments)** — `SQL` — multi-dataset analysis of community hardship, crime rates and school performance, with views, stored procedures and transaction management
- 💊 **[AI Medication Reminder](https://github.com/Abdulla1x/AI-Medication-Remainder)** — `Python` `Streamlit` `Gemini` `APScheduler` `SWI-Prolog` — Gemini parses natural-language schedules, APScheduler fires the reminders, and Prolog rules check for drug interactions

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
