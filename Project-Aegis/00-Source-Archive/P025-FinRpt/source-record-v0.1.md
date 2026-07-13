# P025 Source Record v0.1 — FinRpt

## Paper

**FinRpt: Dataset, Evaluation System and LLM-based Multi-agent Framework for Equity Research Report Generation**

## Source status

This file records source-level access information for P025.

It is not a full copied PDF. The full paper should not be copied into this repository until redistribution rights and licensing terms are checked.

## Source metadata

| Field | Value |
|---|---|
| Paper ID | P025 |
| Title | FinRpt: Dataset, Evaluation System and LLM-based Multi-agent Framework for Equity Research Report Generation |
| Authors | Song Jin; Shuqi Li; Shukun Zhang; Rui Yan |
| arXiv ID | 2511.07322 |
| arXiv abstract URL | https://arxiv.org/abs/2511.07322 |
| arXiv HTML URL | https://arxiv.org/html/2511.07322 |
| arXiv source status | public web source available |
| GitHub code URL reported by paper | https://github.com/jinsong8/FinRpt |
| GitHub verification status | public repository verified; README states MIT License; standalone root LICENSE file not found |
| Hugging Face dataset URL reported by paper | https://huggingface.co/datasets/jinsong8/FinRpt |
| Hugging Face verification status | dataset page verified; page shows cc-by-4.0 license; dataset viewer shows about 13.6k rows |
| Repository storage decision | store metadata and extracted facts first; do not store full PDF or dataset copy until license/source-rights chain is checked |

## Source-level facts captured from arXiv HTML

| Fact | Source-level note |
|---|---|
| Task | Equity Research Report generation |
| Benchmark name | FinRpt |
| Dataset size in paper extraction | 6,825 ERRs / samples |
| Hugging Face viewer rows | about 13.6k rows; requires reconciliation with paper sample count |
| Market universe | CSI800 Index, Chinese market |
| Company count | 800 stocks |
| Date range | 2024-09-03 to 2024-11-05 |
| Analysis-date interval | one week |
| Number of analysis dates | 10 dates per company stock |
| Train / validation / test split | train 5,556; validation 617; test 652 |
| Input information sources | company information, financial indicators, company announcements, company-related news, historical stock prices, historical market indices |
| Output report sections | financial analysis, news analysis, management and development analysis, risks analysis, investment potential assessment, recommendation rating |
| Framework name | FinRpt-Gen |
| Framework modules | information extraction module, analysis module, prediction module |
| Number of agents | nine agents |
| Basic metrics | CompletionRate, Accuracy, BERTScore, ROUGE-L, NumberRate |
| LLM evaluation metrics | Financial Numeric, News, Company & Market & Industry, Invest, Risk, Writing |
| Human evaluation | 30 FinRpt ERRs and 30 expert-written ERRs rated by three senior financial analysts |
| Code availability claim | paper reports public code; public GitHub repository verified |
| Dataset availability claim | paper reports public dataset; public Hugging Face dataset page verified |

## Important caution

These facts are source-level extractions from the arXiv HTML view and preliminary external-resource verification, but the next step should still verify:

1. exact tables and figure numbers;
2. appendix prompt details;
3. whether the README MIT statement is sufficient without a standalone LICENSE file;
4. Hugging Face dataset card, license, and file availability in detail;
5. whether source reports/news/announcements have upstream copyright or redistribution restrictions;
6. whether generated reports can be redistributed;
7. why the paper-level 6,825 ERR sample count differs from the Hugging Face viewer's about 13.6k rows.

## Repository policy for source copying

For now, this repository should store:

- source metadata;
- source URLs;
- extracted facts;
- citation notes;
- extraction tables;
- verification status.

Do not store:

- full PDF;
- full article text;
- copyrighted broker reports;
- dataset files with unclear redistribution chain;
- generated reports if redistribution rights are unclear.

## Next source-level verification tasks

1. Inspect repository directory tree.
2. Verify `requirements.txt` and execution instructions.
3. Verify Hugging Face dataset card and files.
4. Reconcile paper sample count with Hugging Face row count.
5. Extract table and figure numbers from the PDF/HTML.
6. Check whether generated ERR examples are included and reusable.
7. Check whether prompts can be stored or only referenced.
8. Inspect generated report case for source citations or claim-level evidence links.
