# Piotr Cząstkiewicz — AI Engineer / Data Scientist

I build complete, defensible data and AI systems in Python — from data acquisition, through
models, to deployed and **evaluated** applications. Telecommunications student; open to
**AI Engineer**, **Data Scientist**, and Junior Python / ML Engineer roles.

📧 **[p0w3r2243@gmail.com](mailto:p0w3r2243@gmail.com)** — the quickest way to reach me about
any of the above.

Every project below is defensible in a technical interview: each non-trivial decision is
documented (ADRs), results are **measured rather than asserted**, and models are always compared
against a baseline.

## Start here

- **AI Engineer →** [doc-extract](https://github.com/P0w3r223/doc-extract) — invoice extraction that knows when it is wrong
- **Data Scientist →** [ab-lab](https://github.com/P0w3r223/ab-lab) — a 5% test is only 5% if you look once

| Project | What it is | Live |
|---|---|---|
| **[doc-extract](https://github.com/P0w3r223/doc-extract)** | Structured extraction from Polish invoices where the point is not the extraction but the **error detection**: the Ministry's KSeF FA(3) schema carries 328 enumerations and **zero assertions**, so *net + VAT = gross* is unenforced by the national standard. Fifteen consistency rules fill that gap and become a label-free error detector. | [demo](https://p0w3r223.github.io/doc-extract/) |
| **[ab-lab](https://github.com/P0w3r223/ab-lab)** | A 5% test is only 5% if you look once, count each user once, and test one metric. Peeking, clustered users and many metrics each turn a true null into a 25–66% false positive rate — measured on experiments with no effect to find, each paired with the correction that puts it back. | [demo](https://p0w3r223.github.io/ab-lab/) |
| **[apply-scout](https://github.com/P0w3r223/apply-scout)** | An LLM agent — a from-scratch tool loop with safety budgets and guardrails — that matches a job posting against a CV and GitHub evidence, with a trajectory-evaluation harness measuring success rate, citation fidelity, and cost per task. | [demo](https://p0w3r223.github.io/apply-scout/) |
| **[mlops-car-price](https://github.com/P0w3r223/mlops-car-price)** | An MLOps layer around a price model: MLflow tracking and registry, a drift detector that is itself measured, and champion/challenger promotion decided by a paired bootstrap. | [demo](https://p0w3r223.github.io/mlops-car-price/) |
| **[car-price-ml](https://github.com/P0w3r223/car-price-ml)** | The full ML cycle end-to-end: EDA, feature engineering, model comparison, SHAP, and a FastAPI + Docker prediction service. | [demo](https://p0w3r223.github.io/car-price-ml/) |

## What I work with

- **Languages** — Python (primary), C++, SQL, JavaScript
- **ML / Data Science** — scikit-learn, LightGBM, pandas, SHAP, applied statistics, time-series forecasting
- **LLM / AI** — Anthropic API, from-scratch agents, QLoRA fine-tuning, evaluation harnesses
- **MLOps** — MLflow, drift monitoring, model registries, Docker, FastAPI, GitHub Actions
- **NLP (Polish)** — TF-IDF baselines, HerBERT / Bielik fine-tuning, PolEmo

## Live demos

| Project | Focus | Demo |
|---|---|---|
| doc-extract | Invoice extraction + error detection | https://p0w3r223.github.io/doc-extract/ |
| ab-lab | Applied statistics — when 5% is not 5% | https://p0w3r223.github.io/ab-lab/ |
| apply-scout | LLM agent + evaluation | https://p0w3r223.github.io/apply-scout/ |
| mlops-car-price | MLOps / drift / promotion | https://p0w3r223.github.io/mlops-car-price/ |
| car-price-ml | Full ML cycle + API | https://p0w3r223.github.io/car-price-ml/ |
| wroclaw-air-insights | Data + 24h forecast | https://p0w3r223.github.io/wroclaw-air-insights/ |
| it-job-radar | Data engineering | https://p0w3r223.github.io/it-job-radar/ |
| pl-review-sense | Polish NLP sentiment | https://p0w3r223.github.io/pl-review-sense/ |
| pl-jobs-lora | QLoRA fine-tune *(in progress)* | https://p0w3r223.github.io/pl-jobs-lora/ |
| auth-log-scan | Linux — SSH brute-force detection | https://p0w3r223.github.io/auth-log-scan/ |
| mini-traceroute | C++ — traceroute on raw sockets | https://p0w3r223.github.io/mini-traceroute/ |

## Also on the profile

- **[token-budget](https://github.com/P0w3r223/token-budget)** — a standard-library CLI that tracks token spend against a milestone budget.
