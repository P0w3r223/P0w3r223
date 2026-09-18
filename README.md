# Piotr Cząstkiewicz — AI Engineer / Data Scientist / Data Engineer

I build complete, defensible data and AI systems in Python — from data acquisition, through
models, to deployed and **evaluated** applications. Telecommunications student; open to
**AI Engineer**, **Data Scientist**, **Data Engineer**, and Junior Python / ML Engineer roles.

📧 **[p0w3r2243@gmail.com](mailto:p0w3r2243@gmail.com)** — the quickest way to reach me about
any of the above.

Every project below is defensible in a technical interview: each non-trivial decision is
documented (ADRs), results are **measured rather than asserted**, and models are always compared
against a baseline. The same standard applies to the portfolio itself — see
[portfolio-index](https://github.com/P0w3r223/portfolio-index) at the bottom of this page.

## Start here

One project per track. **Each quoted line is the claim that project's own published page opens
with** — not a summary written for this page — and the page carries the measurement behind it.

### AI Engineer → [apply-scout](https://github.com/P0w3r223/apply-scout)

> *This agent's retriever finds the evidence for 8 of the 27 requirements a repository can prove*

An LLM job-matching agent with a from-scratch tool loop — and an evaluation that scores its own
retriever and its own attack surface, offline from a committed recording.
· **[live demo](https://p0w3r223.github.io/apply-scout/)**

### Data Scientist → [ab-lab](https://github.com/P0w3r223/ab-lab)

> *A 5% test is only 5% if you look once, count each user once, and test one metric.*

Three ways an A/B experiment stops being the test it claims to be — peeking, clustered users,
many metrics — each turning a true null into a **25.3%, 44.0% or 65.7%** false positive rate on
simulated experiments where the truth is known, and each paired with the correction that puts it
back. · **[live demo](https://p0w3r223.github.io/ab-lab/)**

### Data Engineer → [it-job-radar](https://github.com/P0w3r223/it-job-radar)

> *Most junior IT offers in Poland are not development jobs*

**97 of 368** vacancies open to juniors are IT support and service-desk work — the largest single
category. Measured honestly: a census population frame, bounded attribute sampling, a data
contract, and a published Parquet artifact the page is built from.
· **[live demo](https://p0w3r223.github.io/it-job-radar/)**

## The rest of the index

Same standard, and the same rule where it applies: **where a project publishes a page, the
leading italic line is that page's own opening claim.** Two rows below are described instead and
say why — `wroclaw-air-insights` opens with a label rather than a claim, and `token-budget`
publishes no page at all.

| Project | What it is, in its page's own words where it has one | Live |
|---|---|---|
| **[doc-extract](https://github.com/P0w3r223/doc-extract)** | *Poland's national e-invoice schema checks nothing an accountant would* — the KSeF FA(3) schema carries zero assertions, so *net + VAT = gross* is unenforced by the national standard. Consistency rules fill that gap and become a label-free error detector. | [demo](https://p0w3r223.github.io/doc-extract/) |
| **[mlops-car-price](https://github.com/P0w3r223/mlops-car-price)** | *The most accurate model is the one this layer refuses to deploy* — MLflow tracking and registry, a drift detector that is itself measured, and champion/challenger promotion decided by a paired bootstrap. | [demo](https://p0w3r223.github.io/mlops-car-price/) |
| **[car-price-ml](https://github.com/P0w3r223/car-price-ml)** | *A 13.9 MB model prices this market better than a 590 MB one* — the full ML cycle end to end, a model that refuses the cars it cannot price, and a FastAPI + Docker service. It also [runs in your browser](https://p0w3r223.github.io/car-price-ml/app/). | [demo](https://p0w3r223.github.io/car-price-ml/) |
| **[wroclaw-air-insights](https://github.com/P0w3r223/wroclaw-air-insights)** | A live 24-hour PM2.5 forecast that writes down what it published *before* the outcome exists and grades itself once those hours are measured. | [demo](https://p0w3r223.github.io/wroclaw-air-insights/) |
| **[pl-review-sense](https://github.com/P0w3r223/pl-review-sense)** | *HerBERT reaches 0.986 against the baseline's 0.944* — Polish review sentiment on PolEmo 2.0, right on 38 reviews the baseline misses and wrong on 7 it gets, p < 0.0001. | [demo](https://p0w3r223.github.io/pl-review-sense/) |
| **[pl-jobs-lora](https://github.com/P0w3r223/pl-jobs-lora)** *(in progress)* | *A frontier API reaches 94% of a model-free 0.28 ceiling* — a QLoRA fine-tune turning Polish job-posting prose into structured JSON, against honest API baselines. | [demo](https://p0w3r223.github.io/pl-jobs-lora/) |
| **[auth-log-scan](https://github.com/P0w3r223/auth-log-scan)** | *108 failed logins in 7.1 hours — and only some of them are an attack* — brute force, user enumeration, and SSH logins that succeed from an address that had been failing. | [demo](https://p0w3r223.github.io/auth-log-scan/) |
| **[mini-traceroute](https://github.com/P0w3r223/mini-traceroute)** | *A traceroute, one TTL at a time* — written from scratch in C++ over raw sockets, with a page that runs the same checksum, header parser and reply-matching rule in front of you. | [demo](https://p0w3r223.github.io/mini-traceroute/) |
| **[token-budget](https://github.com/P0w3r223/token-budget)** | A standard-library CLI that tracks token spend against a milestone budget and enforces a hard ceiling. The one project here with no published page. | — |

## What I work with

- **Languages** — Python (primary), C++, SQL, JavaScript, Bash / Linux
- **ML / Data Science** — scikit-learn, LightGBM, pandas, SHAP, applied statistics, time-series forecasting
- **LLM / AI** — Anthropic API, from-scratch agents, QLoRA fine-tuning, evaluation harnesses
- **Data Engineering** — ETL pipelines, DuckDB / Parquet, SQLite, data contracts, GitHub Actions
- **MLOps** — MLflow, drift monitoring, model registries, Docker, FastAPI, GitHub Actions
- **NLP (Polish)** — TF-IDF baselines, HerBERT / Bielik fine-tuning, PolEmo

## How the portfolio is held together

- **[portfolio-index](https://github.com/P0w3r223/portfolio-index)** — the index behind the
  repositories above, and the record of how they are maintained: architecture decision records,
  audits of the portfolio's own presentation, and a standard-library checker that holds every
  published page to a written specification and **fails CI** when a gated clause does. Written
  for me rather than for a reader, and public because a claim about engineering discipline is
  worth what its record is worth.
