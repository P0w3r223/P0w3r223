# Piotr Cząstkiewicz

I study telecommunications at Wrocław University of Science and Technology and I am looking for a
junior AI Engineer role. I am also open to Data Scientist and ML Engineer positions. This summer I
built an MCP server and agent for a team at BIAP during my internship.

📧 [p0w3r2243@gmail.com](mailto:p0w3r2243@gmail.com)

## Projects

Start with the first four rows. Each project has tests and CI, and all but one have a live page.

| Project | What it shows | Live |
|---|---|---|
| **[apply-scout](https://github.com/P0w3r223/apply-scout)** · LLM agent | Job-matching agent on a tool loop written from scratch. On 8 annotated postings every cover-letter citation resolves to real evidence (fidelity 1.00), and the evaluation replays offline in CI. Its retriever finds evidence for 8 of 27 provable requirements, and the page reports that defect. | [demo](https://p0w3r223.github.io/apply-scout/) |
| **[ab-lab](https://github.com/P0w3r223/ab-lab)** · statistics | A/B testing library checked by simulation. Peeking 20 times turns a 5% false-positive rate into 25.3%, and mSPRT brings it back to 1.2%. Clustered users (44.0%) and 20 metrics (65.7%) get the same treatment. | [demo](https://p0w3r223.github.io/ab-lab/) |
| **[mlops-car-price](https://github.com/P0w3r223/mlops-car-price)** · MLOps | MLflow registry, drift monitoring and a promotion gate. The gate refused a model 4.0% more accurate because it was 103× larger and 5× slower at p95. | [demo](https://p0w3r223.github.io/mlops-car-price/) |
| **[it-job-radar](https://github.com/P0w3r223/it-job-radar)** · data pipeline | Polish IT job market from a committed Parquet snapshot (2026-08-14): 97 of 368 junior vacancies are support or service-desk work, 72 are development. | [demo](https://p0w3r223.github.io/it-job-radar/) |
| [doc-extract](https://github.com/P0w3r223/doc-extract) *(in progress)* · LLM extraction | Reads Polish KSeF e-invoices with an LLM and uses the invoice's own arithmetic to flag reading errors without labels: precision 100%, recall 76.2% on a weaker model's errors. Synthetic corpus so far; a real held-out set is the open milestone. | [demo](https://p0w3r223.github.io/doc-extract/) |
| [car-price-ml](https://github.com/P0w3r223/car-price-ml) · ML service | LightGBM at 8 612 PLN MAE in 13.9 MB, against RandomForest at 8 798 PLN in 590 MB. The API returns HTTP 422 for cars outside the training domain, and the same model runs in the browser. | [demo](https://p0w3r223.github.io/car-price-ml/) · [app](https://p0w3r223.github.io/car-price-ml/app/) |
| [pl-review-sense](https://github.com/P0w3r223/pl-review-sense) · NLP | Polish review sentiment: fine-tuned HerBERT at 0.986 macro-F1 against a TF-IDF baseline at 0.944, McNemar p = 3.1e-06. | [demo](https://p0w3r223.github.io/pl-review-sense/) |
| [wroclaw-air-insights](https://github.com/P0w3r223/wroclaw-air-insights) · forecasting | Daily 24-hour PM2.5 forecast for Wrocław. MAE 6.97 against 8.61 µg/m³ for the naive rule, lower on 5 of 5 chronological folds. | [demo](https://p0w3r223.github.io/wroclaw-air-insights/) |
| [pl-jobs-lora](https://github.com/P0w3r223/pl-jobs-lora) *(in progress)* · LLM fine-tuning | Polish job ads to JSON. Few-shot claude-haiku-4-5 reaches field F1 0.51 and Bielik-1.5B 0.30; the QLoRA run is not measured yet. | [demo](https://p0w3r223.github.io/pl-jobs-lora/) |
| [auth-log-scan](https://github.com/P0w3r223/auth-log-scan) · security | OpenSSH log scanner, standard library only. On the demo log: 108 failed logins, 4 brute-force sources, 1 suspicious success. | [demo](https://p0w3r223.github.io/auth-log-scan/) |
| [mini-traceroute](https://github.com/P0w3r223/mini-traceroute) · C++ | Traceroute over raw sockets in C++17, with 25 unit tests on Linux and Windows CI that need no root. | [demo](https://p0w3r223.github.io/mini-traceroute/) |
| [token-budget](https://github.com/P0w3r223/token-budget) · tooling | Command-line tool that adds up Claude Code token spend per milestone and fails CI when a budget is exceeded. | none |

<p align="center">
  <img src="https://github.com/P0w3r223/apply-scout/raw/main/docs/demo.gif" width="640"
       alt="apply-scout run: the agent fetches the posting, reads the CV, probes GitHub for evidence, and prints a match report">
</p>

## Stack

- **Languages:** Python (main), SQL, C++, JavaScript, Bash
- **ML and statistics:** scikit-learn, LightGBM, SHAP, pandas, SciPy, PyTorch with transformers (HerBERT), time-series forecasting
- **LLM:** Anthropic API, agents without a framework, evaluation harnesses, QLoRA pipeline (fine-tune in progress)
- **Data:** DuckDB, Parquet, SQLite, data contracts
- **MLOps:** MLflow, Docker, FastAPI, GitHub Actions
- **Integrations:** MCP, Microsoft Graph, MSAL

## Work

**BIAP**, Intelligent Technologies division · Intern · July to September 2026

Built Sufler, an MCP server and agent that connects Claude Code, Teams, GitHub and Jira for one
team, and the kit that deploys it. Deployed as a pilot in one team; writes are off by default
behind per-capability gates. [Code](https://github.com/P0w3r223/sufler) ·
[one-page case study](sufler-case-study.md)

## How I work

I build these projects with Claude Code as a pair programmer. I choose the problem, the baseline and
the evaluation, and I read every change before it is merged; tests and CI decide what ships. My
decisions are recorded as ADRs in each repository. Ask me about any file.

---

[portfolio-index](https://github.com/P0w3r223/portfolio-index) is the maintenance record behind these
repositories: decision records, dated audits, and a checker that tests the published pages in CI.
