# P025 Module and Asset Verification v0.1

## Paper

**FinRpt: Dataset, Evaluation System and LLM-based Multi-agent Framework for Equity Research Report Generation**

## Purpose

This file responds to the recommendation in `Reviewer-Audit-v1.0.md`:

> Verify P025 modules/assets, then start P016 source-level extraction.

This verification inspects the public FinRpt codebase at module level to assess whether P025 has evidence-grounding and auditability potential, or whether it is mainly a report-generation pipeline.

No code was executed. This is source inspection only.

---

# 1. Files inspected

## Source files

| File | Purpose |
|---|---|
| `finrpt/module/FinRpt.py` | main multi-agent FinRpt pipeline |
| `finrpt/module/FinRpt_single.py` | single-model baseline pipeline with explicit prompts |
| `finrpt/utils/ReportBuild.py` | PDF report builder |
| `finrpt/source/Dataer.py` | data retrieval and caching layer |

## Asset files

Assets are referenced in README and report builder, but were not visually inspected in this pass.

Priority assets still requiring visual inspection:

- `assets/pipeline.png`;
- `assets/agent.png`;
- `assets/report.png`.

---

# 2. Main FinRpt pipeline verification

## Source content

`FinRpt.py` imports the following major modules:

- `Advisor`;
- `FinancialsAnalyzer`;
- `NewsAnalyzer`;
- `Predictor`;
- `RiskAssessor`;
- `Dataer`;
- `build_report`.

The `FinRpt` class initializes five major analysis / generation components:

| Component | Source role |
|---|---|
| Advisor | advisory / management-development analysis role |
| FinancialsAnalyzer | financial statement analysis role |
| NewsAnalyzer | news analysis role |
| Predictor | investment potential / recommendation role |
| RiskAssessor | risk analysis role |
| Dataer | data retrieval and caching role |

The main `run()` function collects:

- company information;
- financials;
- news;
- company report;
- stored trend label;
- news analysis;
- financial analysis;
- advisor analysis;
- risk analysis;
- prediction analysis;
- generated PDF report.

It saves intermediate data into `data['save']` and writes `result.pkl`.

## Project Aegis interpretation

This supports the claim that P025 has a concrete multi-component report generation pipeline.

It is stronger than a simple prompt-only report generator because the code separates data retrieval, financial analysis, news analysis, risk assessment, and prediction.

However, it still does not establish claim-level auditability. The pipeline saves intermediate objects, but source-to-claim traceability is not yet explicit.

## Claim supported

P025 supports:

> FinRpt-Gen has an implementable multi-component pipeline for generating equity research reports.

## Claim not supported

P025 does not yet support:

> Every generated report claim can be traced back to source evidence.

---

# 3. Hard-coded local path issue

## Source content

`FinRpt.py` initializes with a default local database path:

`/data/name/FinRpt_v1/finrpt/source/cache.db`

`FinRpt_single.py` uses the same default database path.

`Dataer.py` also defaults to the same path.

## Project Aegis interpretation

This is a reproducibility concern.

A public repository can still be difficult to reproduce if the database path assumes a local private environment.

The code may be runnable after path configuration, but the current default suggests that reproduction requires:

- local SQLite cache reconstruction;
- downloaded / scraped source data;
- correct local path setup;
- possible API/model credentials.

## Claim supported

P025 supports:

> The codebase contains executable pipeline code.

## Claim not supported

P025 does not yet support:

> The code can be run out-of-the-box by an independent researcher.

---

# 4. Data retrieval and source provenance

## Source content

`Dataer.py` retrieves and caches data from several public web / finance sources.

Observed sources include:

| Source | Evidence from code |
|---|---|
| Eastmoney datacenter | company information and reports |
| Eastmoney notice APIs | company annual / semiannual reports |
| Sina finance | company reports, announcements, news |
| yfinance | market data |
| akshare | financial indicators / Chinese market data |
| SQLite cache | local persistence of retrieved source data |

The code stores some source-related fields such as:

- report IDs;
- report dates;
- report titles;
- announcement URLs;
- news URLs;
- news titles;
- news authors;
- news times;
- stock code;
- source content.

## Project Aegis interpretation

This is a positive sign for source provenance at data-collection level.

The code does preserve URLs and timestamps for some source objects. That means source-level traceability may be possible at the raw data / intermediate object level.

However, this is not the same as final-report claim-level grounding.

The missing step is showing whether final report sentences or claims are linked back to specific URLs, reports, or financial data rows.

## Claim supported

P025 supports:

> The codebase collects and caches source-level financial, news, announcement, and report data with some provenance fields.

## Claim not supported

P025 does not yet prove:

> The final ERR contains explicit citations or claim-level evidence links.

---

# 5. Single-model baseline prompts

## Source content

`FinRpt_single.py` exposes explicit prompts for:

- finance paragraph generation;
- news paragraph generation;
- report / management-development paragraph generation;
- trend / recommendation paragraph generation;
- risk list generation.

The trend prompt asks the model to provide an investment recommendation and predict the stock's future three-week trend. It assigns buy/sell depending on whether expected stock gains exceed CSI300 gains.

The risk prompt asks for at least three risks, each under ten Chinese characters.

## Project Aegis interpretation

This is useful because prompts are visible, making the baseline more inspectable.

However, the prompts are section-level generation prompts rather than evidence-citation prompts. They do not appear to require claim-level source references.

## Claim supported

P025 supports:

> The repository exposes explicit prompts for a single-model baseline generation pipeline.

## Claim not supported

P025 does not yet support:

> The prompts enforce source citation, evidence grounding, or audit logs.

---

# 6. Report builder verification

## Source content

`ReportBuild.py` uses ReportLab to generate a PDF report.

The report builder includes sections such as:

- core views;
- risk assessment;
- financial data;
- author information;
- basic company situation;
- stock and market trend comparison;
- PE & EPS;
- quarterly revenue and growth.

It calls chart functions to generate:

- share performance chart;
- PE / EPS chart;
- revenue performance chart.

The generated report includes a synthetic analyst field:

`分析师: FinRpt`

and placeholder fields such as:

`版权: ****`

`地址: ****`

## Project Aegis interpretation

This confirms that P025 can build a formatted PDF-like research report artifact.

However, from the inspected report builder code, explicit citations or source links are not yet visible in the generated PDF structure.

The report appears to be presentation-oriented, not audit-trail-oriented.

## Claim supported

P025 supports:

> FinRpt can generate formatted research report artifacts with charts and sections.

## Claim not supported

P025 does not yet support:

> The generated PDF is audit-ready or citation-grounded.

---

# 7. Evidence grounding assessment after module inspection

## Positive findings

| Layer | Positive evidence |
|---|---|
| Data collection | URLs, dates, source content, and cached database records are used |
| Intermediate pipeline | `data['save']` and `result.pkl` preserve intermediate outputs |
| Prompt visibility | single-model baseline prompts are visible |
| Report artifact | PDF report builder exists |
| Charts | report includes market / financial charts |

## Negative / unresolved findings

| Layer | Concern |
|---|---|
| Final report | no explicit citation layer verified |
| Claim-level evidence | not established |
| Report reconstruction | depends on local database/cache and path setup |
| Licensing | upstream source-rights chain remains unclear |
| Audit logs | logger exists, but not equivalent to review/audit trail |
| Human review | not part of executable code path inspected here |

## Current evidence-grounding status

`source_provenance_partial_but_claim_level_grounding_not_established`

This is a meaningful improvement over `not checked`, but it still falls short of Project Aegis's auditability requirement.

---

# 8. Updated reproducibility assessment

## Stronger than before

P025 is now stronger because the codebase includes:

- main pipeline code;
- single-model baseline code;
- explicit prompts;
- data retrieval layer;
- source URLs / dates in retrieval objects;
- SQLite caching;
- PDF report builder;
- intermediate result serialization.

## Still weak

P025 remains weak because:

- code has not been run;
- default paths are local and hard-coded;
- external web sources may change;
- API/model keys may be required;
- local model serving is not verified;
- full dataset and source cache reconstruction is not verified;
- final report citation/evidence links are not verified.

## Suggested classification

P025 reproducibility status should be:

`module_structure_verified_execution_not_tested_claim_grounding_not_established`

---

# 9. Project Aegis implications

P025 should now be used as strong evidence for:

1. ERR generation task formulation;
2. dataset/benchmark construction;
3. multi-component agent architecture;
4. source-level data collection and caching;
5. public code/data availability in partial sense;
6. formatted research artifact generation.

P025 should not yet be used as strong evidence for:

1. claim-level auditability;
2. citation-grounded reports;
3. fully reproducible execution;
4. institutional deployment readiness;
5. robust source-rights clearance.

---

# 10. Recommended next step

The next best improvement is no longer another P025 scaffold.

The next best step is to start P016 source-level extraction, because P016 is still shallow relative to P001 and P025.

Recommended file:

`03-Full-Extraction/P016-FinRobot-Source-Level-Extraction-v0.1.md`

After that, create:

`03-Full-Extraction/P016-P025-Equity-Research-Agent-Comparison-v0.1.md`

This will help decide whether P016 and P025 together support an emerging investment research agent category.
