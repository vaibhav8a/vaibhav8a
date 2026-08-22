<div align="center">

# Vaibhav Srivastava

**Final-year Computer Science undergrad · PES University, Bengaluru '27**<br />
Machine Learning Intern @ MindKonnected

<a href="mailto:vaibhavsri1712@gmail.com"><img src="https://img.shields.io/badge/Email-2E3440?style=flat-square&logo=gmail&logoColor=88C0D0" /></a>
<a href="https://vaibhavsrivastava.me"><img src="https://img.shields.io/badge/Portfolio-2E3440?style=flat-square&logo=aboutdotme&logoColor=88C0D0" /></a>
<a href="https://github.com/vaibhav8a?tab=repositories"><img src="https://img.shields.io/badge/Repositories-2E3440?style=flat-square&logo=github&logoColor=88C0D0" /></a>

</div>

---

## Hey there 👋

I'm a final-year CS student at PES University, and I'm in this field for the reason
most people who stay in it are: you can have an idea in the morning and be using the
thing by evening. Nothing else lets you build that fast.

I've deliberately kept my interests wide. Over the past few years I've written a
retrieval system over Indian criminal statute, a civic platform for a Gram Panchayat,
an e-commerce backend with hand-tuned SQL, a robot that follows a line and dodges
obstacles, and a study predicting sediment grain size from water-chemistry data. Those
have almost nothing in common on the surface — which is the point. Every one of them
taught me something the others couldn't, and I'd rather understand five layers of the
stack badly at first than one layer comfortably forever.

The thing I enjoy most is the moment a system stops being a diagram and starts
behaving — the first correct query, the first clean deploy, the first PR a stranger
merges. That last one got addictive: **31 patches merged into projects I didn't
start**, in codebases I had to read before I could touch.

Right now I'm deep in backend engineering, applied ML and system design, and I'm
looking for a role where I get to keep building things that people actually run.

---

## Currently

```
studying      final year — system design, distributed systems, applied ML
working on    LawLine AI, a grounded QA system over Indian criminal statute
contributing  Pyleoclim_util · revive · watchdog · flagd · pymc-marketing · eslint-plugin-vue
curious about retrieval evaluation, Go, developer tooling, anything with a REPL
open to       backend / applied-AI internships and new-grad roles
```

---

## What I've built

### 🤖 AI & Retrieval

**[LawLine AI](https://github.com/vaibhav8a/Capstone_AI_Lawline)** — `Python` `FastAPI` `React` `ChromaDB`

Question answering over the Indian Penal Code (523 sections) and the Bharatiya Nyaya
Sanhita (355 sections). The IPC was repealed in 2024 but still governs older offences,
so the two are live law at once and can't be flattened into one corpus. I picked the
retrieval pipeline by benchmarking it — chunking per statutory section nearly doubled
Hit@5 over a fixed-window baseline, and the fancier reranker I expected to win didn't.
All the runs, including the ones that went badly, are [in the repo](https://github.com/vaibhav8a/Capstone_AI_Lawline/tree/main/evaluation/results).

**[AI Enterprise Knowledge Manager](https://github.com/vaibhav8a/ai-enterprise-knowledge-manager)** — `Python` `OpenAI Agents SDK` `Streamlit`

Seven agents with real handoffs, RAG with page-level citations, Pydantic-typed outputs,
and a human approval gate that genuinely halts the run before any write. 142 tests that
run without an API key.

<br>

### 🌐 Full-stack

**[E-GRAM-CONNECT](https://github.com/vaibhav8a/E-GRAM-CONNECT)** — `TypeScript`

A civic platform connecting a Gram Panchayat to its residents: grievance filing and
tracking, public notices, admin dashboards.

**[Cash & Carry Mart](https://github.com/vaibhav8a/Cash-and-Carry-Mart)** — `React` `Express` `MySQL`

Production-style e-commerce app — JWT auth, bcrypt hashing, React Router and Context
API on the front, and the advanced MySQL programming I actually enjoyed writing.

**[AI Nutrition Tracker](https://github.com/vaibhav8a/AI-Nutrition-tracker)** — `Flask` `Firebase`

Calorie and macro tracking with personalised goals, real-time remaining-intake maths
and a food suggestion system.

<br>

### 📊 Data & Machine Learning

**[Modelling Sediment Grain Size](https://github.com/vaibhav8a/Machine-Learning-Applications-in-Modeling-Sediment-Grain-Size-Using-Hydrodynamic-and-Biogeochemical-)** — `Jupyter` `scikit-learn`

Predicting sediment particle-size distributions from hydrodynamic, water-chemistry and
biological variables using Random Forest and SVR. My first taste of ML on real
environmental data rather than a tidy teaching dataset.

**[Real-Time Market Data](https://github.com/vaibhav8a/Real-Time-Market-Data-Aggregation-and-Analysis)** · **[BookPulse](https://github.com/vaibhav8a/BookPulse)** · **[Delivery Visibility Dashboard](https://github.com/vaibhav8a/Delivery-Visibility-Dashboard)**

Live market data aggregation, Amazon bestseller trend analysis, and shipment tracking —
three takes on the same problem of turning a messy feed into something a person can read.

<br>

### ⚙️ Systems & Odds and Ends

**[Line Tracking Robot](https://github.com/vaibhav8a/Line-tracking-with-obstacles-detection-and-avoidance)** — `Python`

Line following with obstacle detection and avoidance. Physical hardware is a good
teacher: the code is wrong until the robot stops hitting things.

**[Spotify Album Finder](https://github.com/vaibhav8a/Spotify-Album-Finder)** — `React` `Spotify API`

Music discovery across albums, artists and tracks. Built because I wanted it.

---

## Open source

Reading someone else's codebase, matching conventions I didn't choose, and getting a
change past a maintainer taught me more about engineering than any assignment has.
**31 merged pull requests** so far:

| Project | What it is | Merged |
| --- | --- | :---: |
| [sipyourdrink-ltd/bernstein](https://github.com/sipyourdrink-ltd/bernstein) | Deterministic orchestrator for CLI coding agents | **20** |
| [reticlehq/reticle](https://github.com/reticlehq/reticle) | Runtime perception for agents that build web apps | 3 |
| [bootstrap-vue-next](https://github.com/bootstrap-vue-next/bootstrap-vue-next) | Vue 3 + Bootstrap 5 + TypeScript UI library | 2 |
| [CodeWithCJ/SparkyFitness](https://github.com/CodeWithCJ/SparkyFitness) | Self-hosted family fitness and nutrition tracker | 2 |
| [lingdojo/kana-dojo](https://github.com/lingdojo/kana-dojo) | Next.js platform for learning Japanese | 2 |
| [felixmosh/bull-board](https://github.com/felixmosh/bull-board) | Background-job queue inspector | 1 |
| [stabldev/torrra](https://github.com/stabldev/torrra) | Torrent search and download from the CLI | 1 |

Currently open in [Pyleoclim_util](https://github.com/LinkedEarth/Pyleoclim_util),
[revive](https://github.com/mgechev/revive),
[watchdog](https://github.com/gorakhargosh/watchdog),
[flagd](https://github.com/open-feature/flagd),
[pymc-marketing](https://github.com/pymc-labs/pymc-marketing),
[eslint-plugin-vue](https://github.com/vuejs/eslint-plugin-vue),
[aikit](https://github.com/gravity-ui/aikit) and
[openalgo](https://github.com/marketcalls/openalgo).

---

## Toolkit

| | |
| --- | --- |
| **Languages** | Python · TypeScript · JavaScript · C++ · C · SQL |
| **Backend** | FastAPI · Flask · Node.js · Express · Streamlit |
| **Frontend** | React · Vite · Tailwind · Bootstrap |
| **Data** | MySQL · PostgreSQL · Firebase · SQLite · ChromaDB |
| **ML** | scikit-learn · pandas · NumPy · sentence-transformers · Jupyter |
| **Tooling** | Git · Docker · Linux · pytest |
| **Foundations** | DSA · OOP · DBMS · operating systems · computer networks |

---

<div align="center">

<img height="180" src="https://streak-stats.demolab.com?user=vaibhav8a&theme=nord&hide_border=true&date_format=j%20M%5B%20Y%5D" />
<img height="180" src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=vaibhav8a&theme=nord_dark" />

<img width="100%" src="https://github-readme-activity-graph.vercel.app/graph?username=vaibhav8a&bg_color=2e3440&color=eceff4&line=88c0d0&point=eceff4&area=true&area_color=88c0d0&hide_border=true" />

</div>

---

<div align="center">
<sub>Still building, still breaking things, still reading other people's code.</sub>
</div>
