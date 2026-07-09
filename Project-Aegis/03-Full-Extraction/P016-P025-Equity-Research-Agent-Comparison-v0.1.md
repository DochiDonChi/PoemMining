# P016 / P025 Equity Research Agent Comparison v0.1

## Purpose

This file compares the two strongest current Project Aegis anchors for the emerging **equity research agent / investment research agent** category:

- **P016 — FinRobot: AI Agent for Equity Research and Valuation with Large Language Models**
- **P025 — FinRpt: Dataset, Evaluation System and LLM-based Multi-agent Framework for Equity Research Report Generation**

The goal is to clarify what each paper contributes, what each paper does not prove, and how they jointly support the Project Aegis thesis.

---

# 1. High-level comparison

| Dimension | P016 FinRobot | P025 FinRpt | Project Aegis interpretation |
|---|---|---|---|
| Main role | Equity research workflow / valuation platform | ERR dataset, benchmark, and report-generation framework | The two papers are complementary |
| Primary output | Equity research report / valuation output / investment thesis | Six-section equity research report | Both shift from trading actions to research artifacts |
| Main strength | Practical workflow, valuation engine, deterministic compute, report generation | Dataset construction, evaluation metrics, multi-agent ERR generation, human evaluation | P016 is stronger for workflow; P025 is stronger for benchmark/evaluation |
| Main weakness | Current repo may differ from original paper; source-level claim grounding unverified | Claim-level evidence grounding not established; code/dataset execution not tested | Neither proves full trustworthy investment research |
| Best use in Project Aegis | Workflow and valuation-system anchor | Dataset and report-evaluation anchor | Together define the core investment research agent category |

---

# 2. Task definition

## P016

P016 focuses on equity research and valuation. Its core task is to automate parts of an analyst workflow: data gathering, financial analysis, valuation, risk assessment, synthesis, and report generation.

## P025

P025 focuses on Equity Research Report generation. It defines the task using stock ticker and analysis date as inputs, then generates a multi-section ERR from financial, news, announcement, price, and market-index information.

## Comparison

| Question | P016 | P025 |
|---|---|---|
| Is the output a trade? | no | no |
| Is the output a report/research artifact? | yes | yes |
| Does it focus on valuation? | strongly | partially / less central |
| Does it formalize a dataset task? | less central | strongly |
| Does it support Project Aegis category definition? | yes | yes |

## Project Aegis conclusion

Both papers support the claim that a distinct research-artifact-oriented financial-agent category is emerging.

Suggested category term:

> Equity Research Agent

Suggested broader term:

> Investment Research Agent

---

# 3. Architecture comparison

## P016 architecture

P016 / FinRobot repository-level extraction identifies a multi-agent equity research workflow with:

- Lead Agent / Orchestrator;
- Data Agent;
- Analysis Agent;
- Modeling Agent;
- Synthesis Agent;
- Report Agent;
- Bull Agent;
- Bear Agent;
- Judge Agent.

It also emphasizes deterministic computation for financial numbers and LLM assistance for narrative generation.

## P025 architecture

P025 / FinRpt-Gen contains three modules and nine agents:

| Module | Agents |
|---|---|
| Information Extraction | News Extraction, Income Extraction, Balance Extraction, Cash Extraction |
| Information Analysis | Finance Analysis, News Analysis, Status Analysis, Risk Analysis |
| Prediction | Prediction Agent |

## Architecture comparison

| Dimension | P016 | P025 |
|---|---|---|
| Orchestration | Lead Agent / Orchestrator | Pipeline-style multi-agent framework |
| Role specialization | data, analysis, modeling, synthesis, report, bull/bear/judge | extraction, analysis, prediction |
| Debate / contrary view | bull, bear, judge agents described | not central in current extraction |
| Valuation modeling | DCF, DDM, LBO, WACC, comps, Monte Carlo claimed | not central in extracted architecture |
| Report generation | HTML/PDF research reports | six-section ERR generation |
| Deterministic computation | explicit design principle | less emphasized |

## Project Aegis conclusion

P016 is stronger for the **research workflow and valuation-system architecture**.

P025 is stronger for the **structured report-generation dataset and benchmark architecture**.

A future Project Aegis architecture should combine both:

```text
Evidence / data retrieval
        ↓
Deterministic financial computation
        ↓
Research analysis agents
        ↓
Bull / bear / risk challenge agents
        ↓
Report generation
        ↓
Claim-level evidence audit
        ↓
Human review
```

---

# 4. Data and source comparison

## P016

P016 current repository extraction identifies live data and API dependencies:

- Financial Modeling Prep;
- OpenAI;
- optional Adanos;
- repository README also lists providers such as FMP, Finnhub, yfinance, SEC EDGAR, Adanos, NewsAggregator, FX.

## P025

P025 source-level extraction identifies a benchmark dataset built from:

- company information;
- financial indicators;
- company announcements;
- company-related news;
- historical stock prices;
- historical market indices;
- CSI800 Chinese market universe;
- 6,825 ERR samples in paper-level extraction.

## Comparison

| Dimension | P016 | P025 |
|---|---|---|
| Data mode | live API / workflow system | constructed dataset / benchmark |
| Market | mostly US examples in repo README | Chinese CSI800 |
| Source stability | depends on live APIs and keys | dataset page exists but row-count/license questions remain |
| Provenance potential | repository claims provenance tracking | source data and prompt/response fields visible, claim-level grounding not established |
| Reproducibility challenge | API snapshots and model versions | dataset count, source rights, execution scripts |

## Project Aegis conclusion

P016 is closer to a live analyst workflow. P025 is closer to a benchmark corpus.

Project Aegis needs both:

- live workflow realism from P016;
- benchmark/evaluation discipline from P025.

---

# 5. Evaluation comparison

## P016

Current extraction has not yet deeply verified P016's evaluation design. The repository shows example reports and workflow modules, but source-level evaluation details remain pending.

Key pending items:

- report quality evaluation;
- human analyst comparison;
- valuation accuracy;
- evidence traceability;
- reproducibility test.

## P025

P025 has stronger extracted evaluation details:

- CompletionRate;
- Accuracy;
- BERTScore;
- ROUGE-L;
- NumberRate;
- Financial Numeric;
- News;
- Company & Market & Industry;
- Invest;
- Risk;
- Writing;
- human evaluation by three senior financial analysts on 30 FinRpt ERRs and 30 expert-written ERRs.

## Comparison

| Evaluation dimension | P016 | P025 |
|---|---|---|
| Generic text metrics | not yet central in extraction | yes |
| Finance-specific report metrics | pending | yes |
| Human evaluation | pending | yes, limited sample |
| Valuation evaluation | pending | less central |
| Auditability evaluation | not established | not established |
| Claim-level grounding | not established | not established |

## Project Aegis conclusion

P025 is currently stronger for evaluation-method evidence.

P016 needs deeper source-level evaluation extraction before it can match P025's evaluation contribution.

---

# 6. Reproducibility comparison

## P016

P016 has:

- public repository verified;
- equity module README verified;
- CLI workflow described;
- API dependencies disclosed;
- example reports linked;
- source-level extraction started.

But still pending:

- root license verification;
- execution test;
- core scripts inspection;
- module-level reproducibility;
- exact paper/repo version matching.

## P025

P025 has:

- public GitHub repository verified;
- Hugging Face dataset page verified;
- requirements file inspected;
- dataset-checking script inspected;
- benchmark execution script inspected;
- module-level verification performed;
- public code/dataset status partially verified.

But still pending:

- execution test;
- dataset row-count reconciliation;
- upstream source-rights chain;
- claim-level grounding;
- final report citation behavior;
- hard-coded path issues.

## Comparison

| Reproducibility feature | P016 | P025 |
|---|---|---|
| Public code | yes | yes |
| Public dataset | not central / live APIs | yes, HF page verified |
| Requirements | likely, pending deeper check | verified |
| CLI commands | yes | benchmark script verified |
| Data dependency | live APIs | dataset + local cache / scripts |
| Execution tested | no | no |
| License verified | partial | partial |
| Source rights clear | not fully | not fully |

## Project Aegis conclusion

P025 currently has stronger reproducibility evidence because code and dataset are both partially verified.

P016 is more practically workflow-oriented but still needs deeper repository verification.

---

# 7. Auditability comparison

## P016

P016 repository README claims traceable reports, evidence links, numeric provenance, and deterministic compute. These are very important claims, but current extraction has not yet verified them in code or example reports.

## P025

P025 module inspection shows partial source provenance through data retrieval, URLs, timestamps, source content, SQLite cache, and intermediate outputs. However, final report claim-level grounding is not established.

## Comparison

| Auditability feature | P016 | P025 |
|---|---|---|
| Source provenance | claimed | partially visible in data layer |
| Numeric provenance | claimed | limited / not central |
| Claim-level citations | pending | not established |
| Intermediate outputs | likely, pending | visible in dataset/code fields |
| Human review logs | not established | human evaluation scores, not audit logs |
| Final report evidence links | pending | not established |

## Project Aegis conclusion

Neither paper currently proves full auditability.

This is the most important gap.

Project Aegis should define the missing standard:

> A trustworthy investment research agent must not only generate reports. It must preserve source evidence, valuation assumptions, prompt/model versions, intermediate outputs, reviewer notes, and claim-level evidence links.

---

# 8. What P016 and P025 jointly support

Together, P016 and P025 support the following cautious claims:

## Claim 1 — Equity research agents are emerging

Supported because both papers move beyond trading action and toward research artifacts.

## Claim 2 — Multi-agent design is relevant to equity research

Supported because both use role-specialized agents.

## Claim 3 — Research artifact generation needs dedicated evaluation

Supported more strongly by P025.

## Claim 4 — Valuation and deterministic computation are important

Supported more strongly by P016.

## Claim 5 — Auditability remains underdeveloped

Supported by what is missing from both papers.

---

# 9. What P016 and P025 do not yet support

Do not claim:

1. investment research agents are mature;
2. AI-generated research reports are institutionally reliable;
3. claim-level evidence grounding is solved;
4. generated reports can replace human analysts;
5. public code equals full reproducibility;
6. live API workflows are reproducible without snapshots;
7. benchmark accuracy equals investment usefulness.

---

# 10. Proposed Project Aegis definition update

Based on P016 and P025, Project Aegis can refine the definition of an investment research agent.

## Updated working definition

An **investment research agent** is an AI agent system that produces or supports investment research artifacts by coordinating financial data collection, deterministic financial computation, qualitative analysis, valuation reasoning, risk assessment, thesis synthesis, and report generation, while preserving enough evidence, assumptions, intermediate outputs, and reviewer context to make the research artifact auditable.

## Minimum criteria

A system should meet at least five of the following eight criteria:

1. Collects or retrieves financial evidence.
2. Performs structured financial analysis.
3. Uses deterministic computation for financial numbers where appropriate.
4. Generates a research artifact such as an equity report, investment thesis, valuation memo, or risk review.
5. Includes risk analysis or contrary-evidence handling.
6. Provides evaluation of report quality or investment-research usefulness.
7. Preserves intermediate outputs or source provenance.
8. Supports human review, audit, or reproducibility.

## Boundary cases

| System type | Classification |
|---|---|
| Financial QA system | not sufficient unless it generates research artifacts |
| Trading agent | background unless it produces auditable research artifacts |
| Report generator | partial investment research agent if evidence/analysis is weak |
| Equity research workflow system | strong candidate |
| Benchmark-only dataset | supporting evidence, not an agent by itself |

---

# 11. Implications for Project Aegis thesis

The thesis can now be stated more clearly:

> Existing financial-agent research is splitting into at least two streams: trading-action agents and research-artifact agents. P001 shows that trading-agent research already suffers from reproducibility and protocol-reporting gaps. P016 and P025 show that equity research agents and report-generation systems are emerging, but they do not yet fully solve auditability, evidence grounding, or reproducibility. Project Aegis therefore proposes a trustworthy investment research agent framework that combines deterministic financial computation, source-grounded research artifacts, multi-agent analyst roles, reproducible workflows, and human-reviewable audit trails.

---

# 12. Next research actions

## Immediate next action

Update:

`05-Definitions/Definition-Investment-Research-Agent-v0.1.md`

with the refined definition and criteria from this comparison.

## Then inspect P016 deeper

Create:

`00-Source-Archive/P016-FinRobot/core-module-verification-v0.1.md`

Inspect:

- `generate_financial_analysis.py`;
- `create_equity_report.py`;
- `valuation_engine.py`;
- `equity_agents/agent_manager.py`;
- one example report.

## Then rewrite review draft

Create:

`Living-Review-Draft-v0.2.md`

Use P001 + P016 + P025 as the backbone.
