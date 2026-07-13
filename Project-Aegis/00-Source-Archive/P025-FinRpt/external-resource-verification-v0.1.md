# P025 External Resource Verification v0.1

## Paper

**FinRpt: Dataset, Evaluation System and LLM-based Multi-agent Framework for Equity Research Report Generation**

## Purpose

This file verifies the external code and dataset resources reported by P025.

This is a source-verification file, not a full reproducibility test.

---

# 1. Reported GitHub repository

## Repository

`jinsong8/FinRpt`

## Verification result

| Field | Result |
|---|---|
| Repository reachable | yes |
| Visibility | public |
| Default branch | main |
| Archived | false |
| README exists | yes |
| README paper link | arXiv link present |
| README dataset link | Hugging Face dataset link present |
| README claims all code and datasets public | yes |
| Root LICENSE file | not found in root via GitHub fetch |
| README license statement | MIT License stated in README |

## README structure verified

The README lists the following project components:

| Component | README path |
|---|---|
| Dataset Construction Pipeline | `FinRpt/dataset` |
| Data Collection Module | `FinRpt/finrpt/source` |
| FinRpt Framework | `FinRpt/finrpt/module` |
| Benchmark Evaluation | `FinRpt/finrpt/benchmark` |
| Fine-tuning LLMs | `FinRpt/finetune/LLaMA-Factory` |
| Website front-end code | `FinRpt/front` |

The README also references:

- LLaMA-Factory for model fine-tuning;
- verl for reinforcement learning;
- ReportLab for PDF report generation.

## Project Aegis interpretation

The code repository appears to be real and public. This strengthens P025's reproducibility status relative to papers that only report methods without code.

However, the absence of a standalone root `LICENSE` file means license verification should remain cautious. The README states MIT License, but a proper repository license file is not currently verified.

## Claim supported

P025 supports:

> The authors report and provide a public GitHub code repository.

## Claim not supported

Do not yet claim:

> P025 is fully reproducible.

because full reproduction would require verifying dependencies, dataset access, prompts, model weights, API assumptions, execution scripts, and whether all reported results can be regenerated.

---

# 2. Reported Hugging Face dataset

## Dataset

`jinsong8/FinRpt`

## Verification result

| Field | Result |
|---|---|
| Dataset page reachable | yes |
| Hugging Face task tags | Text Generation; Summarization |
| Modalities | Text |
| Format | json |
| Languages | Chinese; English |
| Size label | 10K - 100K |
| arXiv link | arxiv:2511.07322 |
| License shown on page | cc-by-4.0 |
| Dataset viewer subset | default |
| Dataset viewer rows | about 13.6k rows |
| Split shown | train |
| Example fields visible | stock_code, date, news_anlyzer_prompt, news_anlyzer_response, income_prompt, income_response, balance_prompt, balance_response, cash_prompt, cash_response, finance_write_prompt, finance_write_response, news_write_prompt, news_write_response, report_write_prompt, report_write_response, risk_prompt, risk_response, trend_write_prompt, trend_write_response |

## Important observation

The Hugging Face dataset viewer reports about 13.6k rows, whereas the paper-level extraction reports 6,825 ERR samples.

This discrepancy is not necessarily an error. Possible explanations include:

1. the dataset viewer counts prompt/response rows differently;
2. Chinese and English versions may both be included;
3. processed records may differ from paper sample count;
4. Hugging Face auto-converted parquet view may expose a different unit than the paper's ERR sample definition.

This discrepancy requires follow-up verification.

## Project Aegis interpretation

The Hugging Face dataset page strengthens P025 because it shows an accessible dataset with visible prompt and response fields.

However, the 13.6k row count versus 6,825 paper sample count must be reconciled before using exact dataset size claims in a publication-style review.

## Claim supported

P025 supports:

> The authors report and provide a public Hugging Face dataset page with a CC-BY-4.0 license shown.

## Claim not supported

Do not yet claim:

> The dataset is fully clean, fully reproducible, or free of source-rights concerns.

The dataset license shown on Hugging Face does not automatically resolve upstream rights questions for source reports, company announcements, news content, or generated reports.

---

# 3. Verification impact on Project Aegis

## What became stronger

P025 is now stronger as a reproducible-resource candidate because:

1. the reported GitHub repository is public;
2. the README provides project structure;
3. the Hugging Face dataset page is public;
4. the dataset page shows CC-BY-4.0;
5. prompt/response fields are visible in the dataset viewer.

## What remains uncertain

1. Whether all code needed for reproduction is complete.
2. Whether there is a root LICENSE file or only a README license statement.
3. Whether dataset row count should be interpreted as 6,825 ERR samples or about 13.6k viewer rows.
4. Whether source data used to construct ERRs is redistributable.
5. Whether generated reports contain claim-level citations.
6. Whether prompts in the dataset are complete enough to reconstruct reported outputs.
7. Whether model/API versions and random seeds are fully specified.

---

# 4. Updated reproducibility interpretation

## Current status

P025 can now be classified as:

`public_code_and_dataset_reported_and_partially_verified`

but not yet:

`fully_reproducible`

## Suggested reproducibility note

Use this wording:

> P025 reports public code and dataset resources, and preliminary verification confirms that both a public GitHub repository and a public Hugging Face dataset page exist. The Hugging Face page shows a CC-BY-4.0 license and visible prompt/response fields. However, full reproducibility remains unverified because the standalone repository license file, exact dataset-row interpretation, dependency execution, source-rights chain, and output reconstruction have not yet been checked.

---

# 5. Next verification tasks

1. Inspect repository directory tree.
2. Check whether `requirements.txt` is complete.
3. Check whether example scripts can run from README instructions.
4. Check whether prompts are sufficient for reproduction.
5. Inspect Hugging Face dataset card more deeply.
6. Reconcile 6,825 paper samples with 13.6k dataset viewer rows.
7. Verify whether CC-BY-4.0 applies to all dataset fields.
8. Check whether source news/report data carries upstream copyright restrictions.
9. Extract Figure 1 and Figure 3 from paper/source assets.
10. Inspect generated report case for source citations or claim-level evidence links.
