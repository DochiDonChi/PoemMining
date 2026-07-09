# Improvement Summary v2.1

## Date

2026-07-09

## Purpose

This iteration continues P025 external verification by inspecting the public FinRpt GitHub repository structure, requirements file, dataset checking script, and benchmark execution script.

The purpose is to determine whether P025 is moving from merely `public resources reported` to a more credible `repository structure partially verified` status.

## Improvements completed

### 1. P025 repository structure verification added

Added:

`00-Source-Archive/P025-FinRpt/repository-structure-verification-v0.1.md`

This file verifies:

- public repository status;
- `README.md` presence;
- `requirements.txt` presence;
- dataset checking script presence;
- benchmark execution script presence;
- high-level code structure reported in README;
- dependency stack;
- dataset-checking functions;
- benchmark execution functions;
- local and remote model configuration;
- intermediate prompt/response serialization fields.

### 2. Requirements file inspected

The repository contains a detailed pinned `requirements.txt`.

Important dependency groups include:

- financial data access: `akshare`, `yfinance`;
- dataset and Hugging Face tooling: `datasets`, `huggingface-hub`;
- LLM training stack: `torch`, `transformers`, `peft`, `trl`, `deepspeed`;
- evaluation metrics: `bert-score`, `rouge`, `sentence-transformers`;
- API / application support: `openai`, `Flask`, `reportlab`, `wandb`.

This improves environment transparency, but execution remains untested.

### 3. Dataset checking script inspected

The file `dataset/check.py` was inspected.

It includes functions for checking:

- news availability;
- trend labels;
- financial indicator coverage;
- company report availability;
- generated report serialization;
- recommendation accuracy against stored trend labels.

It also exposes key dataset/report fields such as:

- `stock_code`;
- `date`;
- prompt and response fields for news, income, balance, cash, finance writing, news writing, report writing, risk, and trend writing.

This strengthens the view that FinRpt contains intermediate prompt/response artifacts, not just final reports.

### 4. Benchmark execution script inspected

The file `finrpt/benchmark/exec_exp.py` was inspected.

It imports several framework variants:

- `FinRpt`;
- `FinRptSingle`;
- `FinRpt_analyst_finance`;
- `FinRpt_analyst_news`;
- `FinRpt_no_write`.

It defines:

- local model group;
- remote model group;
- local run function;
- remote run function;
- output serialization to JSONL;
- ablation variant routing.

This strengthens the claim that the repository contains executable benchmark scaffolding, not only paper documentation.

## What became stronger

### P025 reproducibility evidence improved

P025 now has evidence of:

- public code repository;
- pinned dependencies;
- dataset-checking scripts;
- benchmark execution scripts;
- intermediate prompt/response serialization;
- ablation/framework variants.

### P025 is now stronger as an open-resource candidate

The repository inspection supports the classification:

`public_code_dataset_partially_verified_but_execution_not_tested`

## What remains weak

1. Code has not been run.
2. Some scripts contain hard-coded local paths.
3. Local SQLite/cache reconstruction is not verified.
4. Remote model reproduction requires API credentials.
5. Local model reproduction requires model-serving infrastructure.
6. SFT/RL reproduction likely requires heavy GPU resources.
7. Hugging Face dataset row count still needs reconciliation with the paper-level 6,825 ERR sample count.
8. Standalone root LICENSE file remains not found.
9. Claim-level evidence grounding remains unverified.
10. Generated report assets and source citations remain uninspected.

## Current status after v2.1

Project Aegis remains:

**Level 2.0 candidate / 5**

P025 is now significantly stronger as a source-verified research artifact generation anchor, but not yet a full reproducibility or auditability anchor.

## Recommended next step

Continue with:

`00-Source-Archive/P025-FinRpt/module-and-asset-verification-v0.1.md`

This should inspect:

1. `finrpt/module/FinRpt.py`;
2. `FinRptSingle` and ablation modules;
3. `assets/pipeline.png`;
4. `assets/agent.png`;
5. `assets/report.png`;
6. whether final report output contains citations or source links;
7. whether agent outputs are traceable to source evidence.
