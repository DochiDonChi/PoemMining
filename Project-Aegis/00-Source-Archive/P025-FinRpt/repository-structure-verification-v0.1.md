# P025 Repository Structure Verification v0.1

## Paper

**FinRpt: Dataset, Evaluation System and LLM-based Multi-agent Framework for Equity Research Report Generation**

## Purpose

This file verifies whether the public GitHub repository reported by P025 contains enough concrete project structure to support reproducibility assessment.

This is not a full execution test. No code has been run.

---

# 1. Repository-level status

## Verified repository

`jinsong8/FinRpt`

## Verified facts

| Field | Status |
|---|---|
| Public repository | verified |
| Default branch | main |
| README | verified |
| `requirements.txt` | verified |
| Dataset checking script | verified: `dataset/check.py` |
| Benchmark execution script | verified: `finrpt/benchmark/exec_exp.py` |
| Separate root `LICENSE` file | not found during prior check |
| README license statement | MIT License stated |

---

# 2. Environment and dependency verification

## Source content

The repository contains a `requirements.txt` with a detailed pinned Python dependency list.

Important packages include:

| Package / group | Why it matters |
|---|---|
| `akshare` | Chinese financial data access |
| `yfinance` | market data access |
| `openai` | closed-source API model access |
| `datasets`, `huggingface-hub` | dataset loading / hosting integration |
| `transformers`, `peft`, `trl`, `torch`, `deepspeed` | LLM fine-tuning and training stack |
| `bert-score`, `rouge`, `sentence-transformers` | evaluation metrics |
| `reportlab` | PDF report generation |
| `Flask` | possible web front-end/server support |
| `wandb` | experiment logging |

## Project Aegis interpretation

The dependency file strengthens reproducibility because it pins concrete package versions.

However, full environment reproducibility remains unverified because:

1. no code has been run;
2. GPU/CUDA requirements may be heavy;
3. API credentials may be needed for remote models;
4. model downloads and local Ollama setup are not verified;
5. external data APIs may change;
6. some hard-coded paths appear in scripts.

## Claim supported

P025 supports:

> The public repository includes a detailed dependency file for environment setup.

## Claim not supported

Do not yet claim:

> The project is fully reproducible from requirements alone.

---

# 3. Dataset checking script verification

## Source file

`dataset/check.py`

## Source-level observations

The script imports and uses:

- `sqlite3`;
- `pickle`;
- `yfinance`;
- `akshare`;
- `sklearn.metrics.accuracy_score`;
- local CSI300 / CSI500 stock lists;
- a local SQLite database path.

The script contains checks for:

| Function | Purpose |
|---|---|
| `check_news()` | checks number of news records by stock and date |
| `check_trend()` | checks trend labels against standard stock/date IDs |
| `check_financials()` | checks financial indicator coverage |
| `check_company_report()` | checks company report availability |
| `check_report()` | serializes generated reports and checks recommendation accuracy |
| `check_report_from_jsonl()` | checks generated report recommendations against stored trend labels |

## Important source details

The script uses CSI300 and CSI500 lists together as the stock universe, matching the CSI800 framing.

It includes date lists covering weekly analysis dates, including:

- 2024-09-03;
- 2024-09-10;
- 2024-09-17;
- 2024-09-24;
- 2024-10-01;
- 2024-10-08;
- 2024-10-15;
- 2024-10-22;
- 2024-10-29;
- 2024-11-05.

It also exposes the key serialized dataset/report fields:

```text
id
stock_code
date
news_anlyzer_prompt
news_anlyzer_response
income_prompt
income_response
balance_prompt
balance_response
cash_prompt
cash_response
finance_write_prompt
finance_write_response
news_write_prompt
news_write_response
report_write_prompt
report_write_response
risk_prompt
risk_response
trend_write_prompt
trend_write_response
```

## Project Aegis interpretation

This is important because it confirms that the dataset is not just final reports; it also contains prompt/response pairs for multiple pipeline stages.

That makes P025 more useful for Project Aegis because it may allow analysis of intermediate agent outputs.

However, the script contains hard-coded local paths, for example a database path under `/data/name/FinRpt_v1/...`. This suggests that full reproduction may require local database reconstruction not immediately available from the repo alone.

## Claim supported

P025 supports:

> The repository contains scripts that expose dataset quality checks and intermediate prompt/response fields.

## Claim not supported

Do not claim:

> The dataset construction pipeline is fully reproducible without additional local data or path configuration.

---

# 4. Benchmark execution script verification

## Source file

`finrpt/benchmark/exec_exp.py`

## Source-level observations

The script imports:

- `FinRpt`;
- `FinRptSingle`;
- `FinRpt_analyst_finance`;
- `FinRpt_analyst_news`;
- `FinRpt_no_write`.

This confirms that the repository contains or expects several framework variants:

| Class / variant | Likely role |
|---|---|
| `FinRpt` | main multi-agent framework |
| `FinRptSingle` | single-model baseline |
| `FinRpt_analyst_finance` | ablation / finance-analysis variant |
| `FinRpt_analyst_news` | ablation / news-analysis variant |
| `FinRpt_no_write` | ablation without writing/analysis agents |

The script defines model groups:

| Model group | Examples |
|---|---|
| Local models | Llama, Qwen, Mixtral, FinMA, DeepSeek, GLM, Gemma, fine-tuned models |
| Remote models | GPT-4o, GPT-4o-mini |

The script writes results to JSONL and serializes prompt/response fields similar to `dataset/check.py`.

## Project Aegis interpretation

This is strong evidence that the repository is not only documentation. It includes executable benchmark scaffolding for local and remote models.

However, reproduction still requires:

1. local model availability;
2. remote API credentials;
3. `results/standard.txt`;
4. source database/cache;
5. correct path setup;
6. model serving environment such as Ollama for local models.

## Claim supported

P025 supports:

> The repository contains benchmark execution code for multiple model configurations and ablation variants.

## Claim not supported

Do not claim:

> The reported benchmark results can be reproduced immediately without additional setup and data.

---

# 5. Reproducibility assessment after repository inspection

## Stronger evidence

P025 now has stronger reproducibility evidence than before because:

1. a public repo exists;
2. a dependency file exists;
3. README gives high-level setup and directory structure;
4. dataset checking code exists;
5. benchmark execution code exists;
6. intermediate prompt/response fields are visible in code;
7. multiple framework variants and model groups are represented.

## Remaining barriers

| Barrier | Why it matters |
|---|---|
| hard-coded local database paths | may prevent direct reproduction |
| missing standalone root LICENSE file | weakens license clarity |
| external data APIs | data availability may change |
| API credentials | remote model reproduction requires keys |
| local model serving | local models require installation and serving infrastructure |
| heavy GPU stack | SFT/RL reproduction may be costly |
| row-count discrepancy | paper 6,825 ERR samples versus Hugging Face about 13.6k viewer rows needs reconciliation |
| unclear upstream rights | news/report/source data may have redistribution restrictions |

## Suggested classification

Current P025 reproducibility status should be:

`public_code_dataset_partially_verified_but_execution_not_tested`

not:

`fully_reproducible`

---

# 6. Updated Project Aegis use

P025 is now stronger as:

- a task-definition anchor;
- a dataset/benchmark anchor;
- a multi-agent report-generation anchor;
- a partially verified open-resource anchor.

P025 is still weak as:

- an auditability anchor;
- a claim-level evidence-grounding anchor;
- a full reproducibility anchor.

## Correct wording

Use:

> P025 reports and partially verifies public code and dataset resources. Repository inspection confirms the presence of a pinned dependency file, dataset checking code, and benchmark execution code. However, full reproducibility remains untested because local databases, model serving, API credentials, source-rights chain, and execution scripts still require verification.

Avoid:

> P025 is fully reproducible.

---

# 7. Next verification tasks

1. Inspect `finrpt/module/FinRpt.py`.
2. Inspect `finrpt/module/FinRpt_single.py`.
3. Inspect ablation modules.
4. Inspect `results/standard.txt` availability.
5. Inspect generated report asset `assets/report.png` visually or via file metadata.
6. Inspect `assets/pipeline.png` and `assets/agent.png` visually or via file metadata.
7. Inspect Hugging Face dataset card and file list.
8. Reconcile 6,825 sample count with about 13.6k viewer rows.
9. Check whether output reports contain citations or source links.
10. Check whether the dataset includes enough source provenance to support claim-level grounding.
