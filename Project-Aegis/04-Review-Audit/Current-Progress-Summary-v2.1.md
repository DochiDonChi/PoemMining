# Current Progress Summary v2.1

## Date

2026-07-09

## Project

**Project Aegis: Trustworthy AI Investment Research**

Working direction:

> Towards reproducible, auditable, evidence-grounded, risk-aware AI investment research agents.

## Current PR status

| Field | Status |
|---|---|
| Repository | `DochiDonChi/PoemMining` |
| Branch | `project-aegis-v0.1` |
| PR | #1 |
| PR state | open |
| Draft | true |
| Mergeable | false |
| Commits | 149 |
| Changed files | 114 |
| Additions | 14,427 |
| Deletions | 0 |

## Current maturity rating

**Level 2.0 candidate / 5**

The project is now a structured research workspace, not just a reading list. It has methodology, paper database, extraction files, review audits, bilingual reading layer, source archive, and early source-level verification.

However, it is still not a publishable systematic review because:

1. full Search-Round-02 has not been executed;
2. exact source result counts are missing;
3. PRISMA counts are still provisional;
4. P007-P011 metadata debt remains;
5. full table/figure extraction is incomplete;
6. P001 exact R0-R3 definitions remain pending;
7. P025 reproducibility and evidence grounding remain only partially verified.

---

# 1. What has been completed

## 1.1 Research foundation

Completed:

- project README;
- research protocol;
- research questions;
- inclusion/exclusion criteria;
- paper database;
- research gap map;
- question bank;
- living review draft;
- PRISMA-style methodology;
- search strategy;
- screening log;
- extraction template;
- quality scoring rubric;
- claim-evidence ledger;
- reviewer audit chain.

This gives the project a real research-management structure.

## 1.2 Bilingual mobile reading layer

Completed bilingual mobile reading packages for 12 papers:

1. P001 Agentic Trading
2. P016 FinRobot Equity Research
3. P025 FinRpt
4. P013 Finance Agent Benchmark
5. P014 Evaluation and Benchmarking Suite
6. P004 TradingAgents
7. P006 FinMem
8. P022 StockAgent
9. P024 StockBench
10. P023 AFIB / SuperInvesting Benchmark
11. P026 TrustTrade
12. P027 TradingGPT

Each main reading package includes:

- `summary.md`;
- `questions.md`;
- `ebook-bilingual.md`.

This is useful for:

- mobile reading;
- bilingual learning;
- supervisor discussion;
- PhD interview preparation;
- English academic vocabulary building.

## 1.3 Working definition and taxonomy

Completed:

- `Definition-Investment-Research-Agent-v0.1.md`;
- `Taxonomy-Coding-Test-v0.1.csv`.

Current working distinction:

| Category | Primary output |
|---|---|
| Financial QA agent | answer |
| Trading agent | trading action / position / allocation |
| Report generator | research-style text artifact |
| Investment research agent | evidence-grounded investment research artifact with reasoning and traceability potential |
| Governance/evaluation framework | evaluation lifecycle, benchmark, audit, AgentOps |

This distinction is now one of the most important intellectual contributions of the project.

---

# 2. P001 progress — reproducibility-gap anchor

## Current role

P001 is the strongest current evidence anchor for:

> LLM trading-agent literature has protocol-reporting and reproducibility gaps.

## Completed P001 files

- `P001-Agentic-Trading-Extraction-v0.1.md`
- `P001-Agentic-Trading-Full-Text-Extraction-v0.2.md`
- `P001-Core-Tables-Figures-Extraction-v0.1.md`
- `P001-Protocol-Reproducibility-Extraction-v0.1.md`
- `P001-Table-Figure-Extraction-Tracker-v0.1.csv`

## What has been extracted

P001 now has:

- section-level extraction scaffold;
- Figure 1 agency spectrum extraction;
- Figure 2 reasoning flow extraction;
- Table 1 related surveys / benchmarks extraction;
- Table 3 study selection summary extraction;
- high-level protocol reporting gap extraction;
- high-level reproducibility tier counts extraction.

## Key extracted P001 evidence

| Evidence item | Current extracted point |
|---|---|
| Primary empirical subset | 19 studies |
| Evidence map | 77 included records |
| Candidate registry | 92 records after deduplication |
| Time-consistent split reporting | 2 / 19 |
| Transaction-cost model | 1 / 19 |
| Universe / survivorship handling | 1 / 19 |
| Execution timing / semantics | 11 / 19 |
| R0 reproducibility | 15 / 19 |
| R3 reproducibility | 0 / 19 |

## Remaining P001 weaknesses

Still pending:

1. exact R0-R3 definitions;
2. exact table numbers for protocol/reproducibility counts;
3. per-study protocol entries;
4. full table extraction;
5. full figure extraction;
6. final verification against original paper tables and figures.

## Current P001 status

`section_level_plus_partial_table_figure_and_protocol_extraction`

---

# 3. P025 progress — investment research artifact anchor

## Current role

P025 is the strongest current candidate anchor for:

> equity research report generation as an emerging investment research agent / research-artifact generation task.

## Completed P025 files

- `P025-FinRpt-Extraction-v0.1.md`
- `P025-FinRpt-Full-Text-Extraction-v0.2.md`
- `P025-Dataset-Metrics-Architecture-Extraction-v0.1.md`
- `P025-Extraction-Tracker-v0.1.csv`
- `00-Source-Archive/P025-FinRpt/source-record-v0.1.md`
- `00-Source-Archive/P025-FinRpt/external-resource-verification-v0.1.md`
- `00-Source-Archive/P025-FinRpt/repository-structure-verification-v0.1.md`

## What has been extracted

P025 now has source-level extraction for:

- task formulation;
- dataset construction;
- output report structure;
- data sources and filtering;
- dataset enhancement process;
- train/validation/test split;
- FinRpt-Gen architecture;
- nine-agent structure;
- SFT/RL training strategy;
- evaluation metrics;
- baseline categories;
- ablation study;
- human evaluation;
- code and dataset availability claims.

## Key extracted P025 evidence

| Evidence item | Current extracted point |
|---|---|
| Dataset | FinRpt |
| Samples | 6,825 ERR samples in paper-level extraction |
| Market | Chinese market |
| Universe | CSI800 |
| Date range | 2024-09-03 to 2024-11-05 |
| Split | train 5,556; validation 617; test 652 |
| Output sections | financial analysis, news analysis, management/development analysis, risks analysis, investment potential assessment, recommendation rating |
| Framework | FinRpt-Gen |
| Agents | 9 agents across extraction, analysis, and prediction modules |
| Metrics | CompletionRate, Accuracy, BERTScore, ROUGE-L, NumberRate; plus 6 LLM evaluation dimensions |
| Human evaluation | 30 FinRpt ERRs and 30 expert-written ERRs rated by 3 senior financial analysts |
| Code | public GitHub repo verified |
| Dataset | Hugging Face dataset page verified |

## External verification completed

Verified:

- GitHub repository `jinsong8/FinRpt` is public;
- README exists;
- README links to arXiv and Hugging Face;
- README lists project structure;
- README states MIT License;
- no standalone root `LICENSE` file found;
- Hugging Face dataset page is reachable;
- Hugging Face page shows `cc-by-4.0`;
- Hugging Face viewer shows about 13.6k rows;
- `requirements.txt` exists and is detailed;
- `dataset/check.py` exists;
- `finrpt/benchmark/exec_exp.py` exists;
- benchmark script imports concrete framework variants;
- intermediate prompt/response fields are visible in code.

## Remaining P025 weaknesses

Still pending:

1. reconcile paper 6,825 ERR samples with Hugging Face about 13.6k viewer rows;
2. verify dataset license chain and upstream source rights;
3. inspect Hugging Face dataset card and files more deeply;
4. inspect `finrpt/module/FinRpt.py` and related modules;
5. inspect generated report asset;
6. verify whether reports include citations or claim-level evidence links;
7. inspect appendix prompts;
8. verify whether code can run;
9. verify exact reproduction steps;
10. check whether hard-coded local database paths block reproduction.

## Current P025 status

`section_level_plus_source_level_dataset_metrics_architecture_extraction`

P025 is now a strong task/dataset/architecture anchor, but not yet a full auditability or reproducibility anchor.

---

# 4. Source archive progress

A new source archive layer has started.

Current source archive:

`00-Source-Archive/P025-FinRpt/`

Files:

- `source-record-v0.1.md`
- `external-resource-verification-v0.1.md`
- `repository-structure-verification-v0.1.md`

Purpose:

- track source URLs;
- record extracted source facts;
- verify external resources;
- track licensing and redistribution uncertainty;
- avoid copying full PDFs or datasets without checking rights.

Current policy:

Do not store full PDFs, dataset files, broker reports, or generated reports unless redistribution rights are clear.

---

# 5. Reviewer audit progress

Current audit chain includes:

- `Reviewer-Audit-v0.5.md`
- `Reviewer-Audit-v0.6.md`
- `Reviewer-Audit-v0.7.md`
- `Reviewer-Audit-v0.8.md`
- `Reviewer-Audit-v0.9.md`

Main audit conclusions:

1. The project has strong structure.
2. The mobile bilingual layer is useful.
3. P001 is becoming a strong reproducibility-gap anchor.
4. P025 is becoming a strong research-artifact generation anchor.
5. The project is still not a publishable systematic review.
6. Full Search-Round-02 remains the biggest systematic-review weakness.
7. Claim-level evidence grounding remains the biggest auditability weakness.

---

# 6. Current main thesis structure

The project now has a clearer two-anchor logic:

## Anchor 1 — P001

Trading-agent literature shows reproducibility and protocol-reporting gaps.

This motivates Project Aegis to require:

- source timestamps;
- protocol transparency;
- reproducibility packages;
- audit logs;
- table/figure-level evidence extraction.

## Anchor 2 — P025

Equity research report generation is emerging as a structured AI task.

This motivates Project Aegis to focus on:

- research artifacts;
- report sections;
- multi-agent analyst roles;
- finance-specific metrics;
- human analyst evaluation;
- dataset and code verification.

## Bridge thesis

Project Aegis should bridge these two sides:

> Take the reproducibility discipline from trading-agent review and apply it to equity research / investment research agent systems, where outputs are research artifacts rather than trades.

---

# 7. Biggest current gaps

## Gap 1 — Search-Round-02 incomplete

The project still relies on seed and pilot literature discovery.

Need:

- exact databases;
- search dates;
- search strings;
- raw result counts;
- deduplication counts;
- screening decisions;
- exclusion reasons;
- final PRISMA flow.

## Gap 2 — P001 exact evidence not fully verified

Need:

- exact R0-R3 definitions;
- exact table numbers;
- per-study protocol entries.

## Gap 3 — P025 evidence grounding not established

Need:

- check whether final reports cite sources;
- check whether individual claims can be traced;
- inspect generated report examples;
- inspect prompt/output fields;
- verify whether dataset preserves source provenance.

## Gap 4 — P016 remains shallow

P016 is still a core equity research agent anchor, but it has not yet received the same depth as P001 or P025.

Need:

- P016 source-level extraction;
- P016/P025 comparison;
- valuation reasoning and auditability extraction.

## Gap 5 — living review draft is outdated

The project has accumulated much more evidence than the original living review draft reflects.

Need rewrite.

---

# 8. Recommended next steps

## Highest priority

Create:

`00-Source-Archive/P025-FinRpt/module-and-asset-verification-v0.1.md`

Purpose:

- inspect `finrpt/module/FinRpt.py`;
- inspect `FinRptSingle` and ablation modules;
- inspect `assets/pipeline.png`;
- inspect `assets/agent.png`;
- inspect `assets/report.png`;
- check whether reports contain citations or evidence links.

## Second priority

Create:

`03-Full-Extraction/P016-FinRobot-Source-Level-Extraction-v0.1.md`

Purpose:

- balance P025 with P016;
- extract architecture;
- extract valuation reasoning;
- extract evaluation and evidence-traceability details.

## Third priority

Create:

`03-Full-Extraction/P016-P025-Equity-Research-Agent-Comparison-v0.1.md`

Purpose:

- define equity research agent category more rigorously;
- compare task, output, evidence, architecture, evaluation, auditability.

## Fourth priority

Rewrite:

`Living-Review-Draft-v0.2.md`

Purpose:

- turn the current evidence into a coherent literature-review narrative.

## Fifth priority

Execute full Search-Round-02.

Purpose:

- move from Level 2.0 candidate toward confirmed Level 2.

---

# 9. Current concise status

Project Aegis is now a structured research workspace with:

- strong bilingual reading layer;
- strong methodology scaffold;
- partial source-level evidence extraction;
- stronger P001 reproducibility anchor;
- stronger P025 equity research report generation anchor;
- source archive and external verification process.

But it is still not a publishable systematic review.

The next phase should focus on:

1. source-level verification;
2. P016/P025 comparison;
3. living review rewrite;
4. full Search-Round-02.
