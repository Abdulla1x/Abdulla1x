# Hi, I'm Mohammad Abdullah 👋

Fourth-year Computer Science student at **Canadian University Dubai** (GPA 3.97, graduating Dec 2027). I build **applied AI and LLM features, cloud data pipelines and machine-learning models**, and I don't stop at "it runs": I measure whether the numbers are right.

In practice that means scoring an AI model's estimates against what users actually saved, reconciling every backfilled chunk of a pipeline against its source, and publishing the coverage gap next to the finding it qualifies.

📫 [LinkedIn](https://www.linkedin.com/in/abdulla1x/) • [Email](mailto:m.abdulla992003@gmail.com) • [trackaholic.app](https://trackaholic.app)

---

## 🥗 [Trackaholic](https://github.com/Abdulla1x/Trackaholic)

**[Open the app](https://trackaholic.app)** · [The story](https://story.trackaholic.app/?ref=gh-profile) · [Docs](https://github.com/Abdulla1x/Trackaholic#read-more)

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Abdulla1x/Trackaholic/main/screenshots/hero-dark.png">
  <img src="https://raw.githubusercontent.com/Abdulla1x/Trackaholic/main/screenshots/hero-light.png" width="640" alt="Trackaholic on a phone: the Today screen, an AI estimate of a chicken and rice meal, and the Progress screen">
</picture>

A calorie and macro tracker, live for multiple users: a React PWA over a FastAPI + PostgreSQL API, with Gemini for the meal estimates.

- **Log a meal from a photo, a voice note or a sentence.** The AI returns a calorie range and every assumption it made, so a wrong guess gets fixed before it is saved.
- **The AI's accuracy is measured, not assumed.** Every estimate is compared with what the user actually saved (how often the truth fell inside the range, and which way it leans), and the app refuses to report where the evidence is too thin.
- **1,700+ tests · 210+ merged PRs · six CI gates**, including a cross-account suite that checks no user can read another's data.

<sub>Write-ups: [a three-day AI outage, traced to the server's region](https://github.com/Abdulla1x/Trackaholic/blob/main/docs/incident-2026-07-gemini-eea-region.md) · [picking a photo size with an A/B test](https://github.com/Abdulla1x/Trackaholic/blob/main/docs/photo-size-ab-2026-10.md) · [setting a calorie target from sources](https://github.com/Abdulla1x/Trackaholic/blob/main/docs/goal-setting-rules.md)</sub>

---

### 🌍 [OpenAQ air-quality pipeline](https://github.com/Abdulla1x/openaq-pipeline) · [Live dashboard](https://datastudio.google.com/reporting/7c88238c-c153-4c64-bf5b-c1974f859158/page/9Fj4F)
`Airflow` `dbt` `BigQuery` `Terraform` `Docker`

**Pakistan's PM2.5 exceeded the WHO 24-hour guideline on 100% of 455 shared days; the UAE's on 94%.** The UAE figure rests on ~8 reporting stations a day against Pakistan's ~180, and that gap is published with the finding. 1.8M measurements backfilled, every chunk count-reconciled against the API; 83 dbt data tests.

### 🎯 [Campus safety detection](https://github.com/Abdulla1x/BCS407_Project)
`YOLOv8` `PyTorch` `Roboflow`

**81.0% → 96.8% mAP@0.50 (+15.8 pp)** by diagnosing class imbalance and consolidating the exit sub-classes. Trained a YOLOv8s model on a 2,069-image campus dataset to detect fire alarms, wet floor signs, emergency exits and safety helmets.

---

**Stack:** Python · TypeScript · SQL · FastAPI · React · PostgreSQL · Airflow · dbt · BigQuery · Terraform · PyTorch · YOLOv8 · Google Cloud

<details>
<summary><b>More projects</b></summary>

- 🎮 **[Game Dashboard](https://github.com/Abdulla1x/game-dashboard)** — `Python` — one place to see and launch every game on a Windows PC (Steam, Epic, Xbox, Riot and loose folders) with real cover art, in pure standard-library Python
- 🧱 **LiteMP** — `Linux` `systemd` `nginx` `Tailscale` — a PaperMC Minecraft server and a Python web control panel on a headless home server, with scripted off-box backups (private repo)
- 🚕 **NYC Yellow Taxi Data Mining** — `pandas` `scikit-learn` — ETL over large-scale trip data feeding classification models at ~97% accuracy
- 🤖 **[CUD Course Scraper](https://github.com/Abdulla1x/CourseScraping-BU)** — `browser-use` `Gemini` `Ollama` `Streamlit` — LLM-driven browser automation that logs into the CUD student portal and scrapes course offerings into a searchable, filterable table
- 🏙️ **[Chicago City Data Analysis](https://github.com/Abdulla1x/sql-assessments)** — `SQL` — community hardship, crime and school performance, with views, stored procedures and transactions
- 💊 **[AI Medication Reminder](https://github.com/Abdulla1x/AI-Medication-Remainder)** — `Gemini` `APScheduler` `Prolog` — natural-language schedules, timed reminders and Prolog rules for drug interactions

</details>

<details>
<summary><b>Algorithm visualizations</b> (live demos)</summary>

Interactive teaching tools for BCS 309 – Algorithms I, in plain HTML, CSS and JavaScript.

- 📦 **[Subset Sum](https://github.com/Abdulla1x/subset-sum)** · [demo](https://abdulla1x.github.io/subset-sum/) — brute force vs dynamic programming with an animated DP table and live operation counters, through to an NP-completeness proof via 3-SAT
- 🌳 **[Huffman Coding](https://github.com/Abdulla1x/huffman-visualization)** · [demo](https://abdulla1x.github.io/huffman-visualization/) — min-heap, greedy merges and code generation step by step, with encode/decode and an exchange-argument proof of optimality

</details>

<details>
<summary><b>Full tech stack</b></summary>

- **Languages:** Python · TypeScript · JavaScript · Java · SQL · C++ · Prolog · Lisp
- **Data engineering:** Airflow · dbt · BigQuery · Cloud Storage · Terraform · Docker Compose · Elementary · Looker Studio
- **ML and computer vision:** YOLOv8 · PyTorch · scikit-learn · pandas · NumPy · Roboflow
- **AI and automation:** Gemini · Ollama (DeepSeek-R1) · browser-use
- **Web and APIs:** FastAPI · React · Tailwind CSS · Streamlit · SQLAlchemy · PostgreSQL · SQLite
- **Tooling and cloud:** Git · GitHub Actions · pytest · Playwright · Google Cloud · Vercel · Render · Neon

</details>

<details>
<summary><b>Certifications</b></summary>

- **Introduction to Modern AI** — Cisco Networking Academy (Apr 2026)
- **C Essentials 1** — Cisco Networking Academy (Apr 2026)
- **Databases and SQL for Data Science with Python** — IBM, Coursera (Jul 2024)
- **What is Data Science?** — IBM, Coursera (Dec 2023)

</details>
