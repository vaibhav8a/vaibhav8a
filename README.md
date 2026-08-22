<div align="center">

# Vaibhav Srivastava

**Computer Science undergrad · PES University, Bengaluru '27**<br />
Machine Learning Intern @ MindKonnected

<a href="mailto:vaibhavsri1712@gmail.com"><img src="https://img.shields.io/badge/Email-2E3440?style=flat-square&logo=gmail&logoColor=88C0D0" /></a>
<a href="https://github.com/vaibhav8a?tab=repositories"><img src="https://img.shields.io/badge/Repositories-2E3440?style=flat-square&logo=github&logoColor=88C0D0" /></a>
<a href="https://github.com/vaibhav8a/Capstone_AI_Lawline"><img src="https://img.shields.io/badge/Capstone-LawLine_AI-2E3440?style=flat-square&logo=bookstack&logoColor=88C0D0" /></a>

</div>

---

I build retrieval systems that are willing to say **"I don't know."**

A language model will answer anything you ask it, fluently and immediately, whether
or not it has grounds to. In the domains I care about — statute, policy, internal
documentation — that confidence is the failure mode, not the feature. So the systems
I build retrieve first, cite what they retrieved, and abstain when the corpus doesn't
support an answer. I pick the pipeline by measuring it, and I keep the experiments
that went badly in the repo alongside the ones that went well.

---

## Currently

```
building     LawLine AI — grounded QA over Indian criminal statute (capstone)
learning     retrieval evaluation, IR metrics, agent orchestration
contributing Pyleoclim_util · revive · watchdog · flagd · pymc-marketing · eslint-plugin-vue
open to      backend / applied-AI internships and new-grad roles
```

---

## Selected work

### LawLine AI — grounded retrieval over Indian criminal statute

[`Capstone_AI_Lawline`](https://github.com/vaibhav8a/Capstone_AI_Lawline) · Python 3.13 · FastAPI · React · ChromaDB · BGE-M3

Question answering over the **Indian Penal Code, 1860** (523 sections) and the
**Bharatiya Nyaya Sanhita, 2023** (355 sections).

The IPC was repealed on 1 July 2024, but offences committed before that date are
still tried under it. Both statutes are therefore live law at once, and a system
that flattens them into one corpus will answer confidently with law that does not
apply to the asker. LawLine keeps them strictly separate and labels every result
with its status.

**What the measurements said.** I ran a grid over two embedding models and three
chunking strategies, scored over 38 queries against 57 gold labels:

| Configuration | Hit@5 | Recall@5 | MRR | p50 latency |
| --- | ---: | ---: | ---: | ---: |
| Baseline — dense, fixed-window chunks | 0.474 | 0.364 | 0.309 | 65 ms |
| **One chunk per statutory section** | **0.868** | **0.763** | **0.633** | **64 ms** |
| Hybrid BM25 + dense (RRF) | 0.816 | 0.702 | 0.666 | 65 ms |
| Hybrid + cross-encoder rerank | 0.842 | 0.697 | 0.669 | 627 ms |

Respecting the document's own structure nearly doubled retrieval quality for free.
The elaborate option did not earn its keep: **cross-encoder reranking cost 10× the
latency and still retrieved less** — it edged ahead on MRR but lost on both Hit@5 and
Recall@5, which is what actually determines whether the right section reaches the answer. Every number above is generated
from the run artifacts in [`evaluation/results/`](https://github.com/vaibhav8a/Capstone_AI_Lawline/tree/main/evaluation/results) — none is hand-entered, and the
abstention results ship with an explicit warning that their thresholds were fit to
the test set.

---

### AI Enterprise Knowledge Manager — multi-agent RAG with a real stop button

[`ai-enterprise-knowledge-manager`](https://github.com/vaibhav8a/ai-enterprise-knowledge-manager) · Python · OpenAI Agents SDK · ChromaDB · Streamlit

An orchestrator routes plain-English questions to one of six specialists — Knowledge
Search, Policy Expert, Meeting Memory, Document Reader, Recommendation, Knowledge
Curator — using the SDK's real `handoffs`, not a prompt that pretends to route.

* **RAG** over PDF / DOCX / TXT / MD with **page-level citations** on every answer
* Every specialist declares a Pydantic `output_type`, so there is no JSON parsing or retry logic anywhere
* `commit_recommendation` is `needs_approval=True` — the run genuinely **halts** and the write happens only after a human clicks Approve
* Each agent re-checks its own sentences against a retrieved passage before returning, and downgrades confidence or says "not found" when it can't
* **142 tests, runnable with no API key**

---

### AI Nutrition Tracker

[`AI-Nutrition-tracker`](https://github.com/vaibhav8a/AI-Nutrition-tracker) · Flask · Firebase

Daily calorie and macro tracking with personalised goals, real-time remaining-intake
maths, an intelligent food suggestion system, and progress dashboards.

---

<details>
<summary><b>More projects</b></summary>

<br>

| Project | Stack | What it is |
| --- | --- | --- |
| [E-GRAM-CONNECT](https://github.com/vaibhav8a/E-GRAM-CONNECT) | TypeScript | Civic platform linking a Gram Panchayat to residents — grievance filing and tracking, notices, admin dashboards |
| [Cash & Carry Mart](https://github.com/vaibhav8a/Cash-and-Carry-Mart) | React · Express · MySQL | Full-stack commerce app — JWT auth, bcrypt hashing, advanced MySQL programming |
| [Real-Time Market Data](https://github.com/vaibhav8a/Real-Time-Market-Data-Aggregation-and-Analysis) | JavaScript | Live market data aggregation and analysis |
| [Sediment Grain-Size ML](https://github.com/vaibhav8a/Machine-Learning-Applications-in-Modeling-Sediment-Grain-Size-Using-Hydrodynamic-and-Biogeochemical-) | Jupyter · scikit-learn | Predicting sediment particle-size distributions from hydrodynamic, water-chemistry and biological variables (Random Forest, SVR) |
| [BookPulse](https://github.com/vaibhav8a/BookPulse) | JavaScript | Trend analysis and visualisation over Amazon bestseller data |
| [Spotify Album Finder](https://github.com/vaibhav8a/Spotify-Album-Finder) | React · Spotify API | Music discovery across albums, artists and tracks |
| [Delivery Visibility Dashboard](https://github.com/vaibhav8a/Delivery-Visibility-Dashboard) | JavaScript | Shipment tracking and status dashboard |
| [Line Tracking Robot](https://github.com/vaibhav8a/Line-tracking-with-obstacles-detection-and-avoidance) | Python | Line following with obstacle detection and avoidance |

</details>

---

## Open source

**31 merged pull requests** into projects I didn't start — reading unfamiliar
codebases, matching their conventions, and shipping something the maintainer
wanted to merge.

| Project | What it is | Merged |
| --- | --- | :---: |
| [sipyourdrink-ltd/bernstein](https://github.com/sipyourdrink-ltd/bernstein) | Deterministic orchestrator for CLI coding agents | **20** |
| [reticlehq/reticle](https://github.com/reticlehq/reticle) | Runtime perception for agents that build web apps | 3 |
| [bootstrap-vue-next](https://github.com/bootstrap-vue-next/bootstrap-vue-next) | Vue 3 + Bootstrap 5 + TypeScript UI library | 2 |
| [CodeWithCJ/SparkyFitness](https://github.com/CodeWithCJ/SparkyFitness) | Self-hosted family fitness and nutrition tracker | 2 |
| [lingdojo/kana-dojo](https://github.com/lingdojo/kana-dojo) | Next.js platform for learning Japanese | 2 |
| [felixmosh/bull-board](https://github.com/felixmosh/bull-board) | Background-job queue inspector | 1 |
| [stabldev/torrra](https://github.com/stabldev/torrra) | Torrent search and download from the CLI | 1 |

Open right now in [LinkedEarth/Pyleoclim_util](https://github.com/LinkedEarth/Pyleoclim_util),
[mgechev/revive](https://github.com/mgechev/revive),
[gorakhargosh/watchdog](https://github.com/gorakhargosh/watchdog),
[open-feature/flagd](https://github.com/open-feature/flagd),
[pymc-labs/pymc-marketing](https://github.com/pymc-labs/pymc-marketing),
[vuejs/eslint-plugin-vue](https://github.com/vuejs/eslint-plugin-vue),
[gravity-ui/aikit](https://github.com/gravity-ui/aikit) and
[marketcalls/openalgo](https://github.com/marketcalls/openalgo).

---

## Toolkit

| | |
| --- | --- |
| **Languages** | Python · TypeScript · JavaScript · C++ · C · SQL |
| **Backend** | FastAPI · Flask · Node.js · Express · Streamlit |
| **Frontend** | React · Vite · Tailwind · Bootstrap |
| **AI / ML** | ChromaDB · sentence-transformers · BGE-M3 · OpenAI Agents SDK · scikit-learn · pandas |
| **Data** | MySQL · PostgreSQL · Firebase · SQLite |
| **Practice** | pytest · Docker · Git · Linux · retrieval evaluation (P@K, Recall@K, MRR, nDCG) |

---

<div align="center">

<img height="180" src="https://streak-stats.demolab.com?user=vaibhav8a&theme=nord&hide_border=true&date_format=j%20M%5B%20Y%5D" />
<img height="180" src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=vaibhav8a&theme=nord_dark" />

<img width="100%" src="https://github-readme-activity-graph.vercel.app/graph?username=vaibhav8a&bg_color=2e3440&color=eceff4&line=88c0d0&point=eceff4&area=true&area_color=88c0d0&hide_border=true" />

</div>

---

<div align="center">
<sub>Grounded answers, measured choices, and the failed experiments left in the repo.</sub>
</div>
