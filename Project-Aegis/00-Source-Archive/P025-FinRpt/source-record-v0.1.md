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
| Hugging Face dataset URL reported by paper | https://huggingface.co/datasets/jinsong8/FinRpt |
| Repository storage decision | store metadata and extracted facts first; do not store full PDF until license checked |

## Source-level facts captured from arXiv HTML

| Fact | Source-level note |
|---|---|
| Task | Equity Research Report generation |
| Benchmark name | FinRpt |
| Dataset size | 6,825 ERRs / samples |
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
| Code availability claim | paper reports public code |
| Dataset availability claim | paper reports public dataset |

## Important caution

These facts are source-level extractions from the arXiv HTML view, but the next step should still verify:

1. exact tables and figure numbers;
2. appendix prompt details;
3. code repository availability and license;
4. Hugging Face dataset card, license, and file availability;
5. whether source reports have copyright or redistribution restrictions;
6. whether generated reports can be redistributed.

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
- dataset files with unclear redistribution license.

## Next source-level verification tasks

1. Verify GitHub repository availability and license.
2. Verify Hugging Face dataset availability and license.
3. Extract table and figure numbers from the PDF/HTML.
4. Check whether generated ERR examples are included and reusable.
5. Check whether prompts can be stored or only referenced.
