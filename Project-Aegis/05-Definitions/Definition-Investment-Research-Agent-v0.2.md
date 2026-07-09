# Definition: Investment Research Agent v0.2

## Purpose

This file updates the Project Aegis working definition of an investment research agent after the P016/P025 comparison.

The purpose is to reduce ambiguity when comparing:

- financial QA systems;
- trading agents;
- report generators;
- equity research agents;
- valuation platforms;
- benchmark/evaluation systems;
- investment research agent systems.

## Why v0.2 is needed

The v0.1 definition was useful but broad. After source-level work on P016 and P025, the category can be made sharper.

Key evidence updates:

- P016 shows the importance of equity research workflow, valuation engines, deterministic computation, and report generation.
- P025 shows the importance of ERR datasets, multi-agent report generation, finance-specific evaluation metrics, and human analyst evaluation.

Together, P016 and P025 suggest that investment research agents should be defined around **research artifacts**, **financial evidence**, **valuation / risk reasoning**, and **auditability potential** rather than direct trading actions.

---

# 1. Updated working definition

An **investment research agent** is an AI agent system that produces or supports investment research artifacts by coordinating financial data collection, deterministic financial computation, qualitative analysis, valuation reasoning, risk assessment, thesis synthesis, and report generation, while preserving enough evidence, assumptions, intermediate outputs, and reviewer context to make the research artifact auditable.

The system does not need to execute trades. Its primary output is a research artifact or decision-support artifact.

Examples of research artifacts include:

- analyst-style equity research report;
- investment thesis;
- valuation memo;
- risk review;
- evidence memo;
- investment committee memo;
- decision-support note.

---

# 2. Minimum criteria v0.2

A system should satisfy at least five of the following eight criteria to be coded as an investment research agent.

## Criteria

1. **Financial evidence collection**
   - retrieves, ingests, or processes filings, earnings calls, financial statements, news, market data, macro data, research notes, or alternative data.

2. **Structured financial analysis**
   - analyzes fundamentals, valuation, macro drivers, sentiment, industry context, risk, or portfolio implications.

3. **Deterministic computation for financial numbers where appropriate**
   - uses code, formulas, or models for valuation, ratios, forecasts, peer comparison, WACC, DCF, DDM, LBO, Monte Carlo, or similar calculations rather than relying only on LLM-generated numbers.

4. **Research artifact generation**
   - produces a report, thesis, memo, valuation analysis, recommendation note, or risk review.

5. **Multi-step or role-specialized workflow**
   - uses structured stages, tools, planning, memory, debate, critic/reviewer roles, or specialized agents.

6. **Risk analysis or contrary-evidence handling**
   - identifies risks, downside cases, bear arguments, uncertainty, contradictory evidence, or sensitivity analysis.

7. **Evaluation of research quality or usefulness**
   - includes report-quality metrics, human analyst evaluation, factuality checks, valuation checks, usefulness scoring, or benchmark comparison.

8. **Traceability / auditability potential**
   - preserves or requires source provenance, evidence links, intermediate outputs, assumptions, prompt/model versions, reviewer comments, or reproducibility artifacts.

---

# 3. Strong versus weak investment research agents

## Strong investment research agent candidate

A strong candidate should have:

- research artifact output;
- multi-source evidence;
- financial reasoning;
- valuation / risk analysis;
- intermediate outputs;
- evidence or numeric provenance;
- evaluation;
- human-review or auditability pathway.

## Weak / partial investment research agent candidate

A weak candidate may generate research-like text but lacks:

- source grounding;
- valuation assumptions;
- risk review;
- evaluation;
- reproducibility;
- audit trail.

Such systems should be coded as:

`research_report_generator_partial`

or:

`equity_research_agent_candidate`

rather than fully mature investment research agents.

---

# 4. Boundary with related categories

## Financial QA agent

A financial QA agent answers finance questions. If it only returns answers without thesis-level reasoning or research artifact generation, it should not be coded as an investment research agent.

## Trading agent

A trading agent primarily outputs market actions, allocation changes, or position decisions.

It may contain analyst-like components, but if its main output is a trade or allocation rather than a research artifact, it should be coded as a trading agent.

Trading-agent papers can still be used as background methodology, especially for reproducibility, protocol reporting, memory, risk, and multi-agent architecture.

## Report generator

A report generator produces research-like text. It becomes an investment research agent only if it also includes structured evidence, financial reasoning, workflow, evaluation, and traceability potential.

## Benchmark-only dataset

A benchmark or dataset may support the investment research agent category, but it is not itself an investment research agent unless it includes an agentic workflow.

## Portfolio optimization model

A portfolio optimization model converts expected returns, risks, or constraints into allocations. If it lacks evidence retrieval, thesis generation, research artifacts, or traceability, it should not be coded as an investment research agent.

## Financial LLM infrastructure

A financial LLM is infrastructure. It becomes part of an investment research agent only when embedded in an agentic workflow that produces research artifacts or decision-support outputs.

---

# 5. Current database examples after P016/P025 comparison

## Strong equity research agent candidates

### P016 — FinRobot Equity Research

Current status:

`source_level_repository_and_equity_module_extraction_started`

Why it matters:

- equity research workflow;
- valuation platform;
- deterministic compute / LLM narration distinction;
- multi-agent role architecture;
- report generation;
- example reports;
- live API workflow.

Current limitation:

- claim-level evidence grounding not yet verified;
- code execution not tested;
- paper/repo version separation required.

### P025 — FinRpt

Current status:

`section_level_plus_source_level_dataset_metrics_architecture_extraction`

Why it matters:

- ERR generation task;
- 6,825-sample paper-level dataset extraction;
- CSI800 Chinese market dataset;
- nine-agent report-generation framework;
- finance-specific evaluation metrics;
- human analyst evaluation;
- public code/dataset partially verified.

Current limitation:

- claim-level grounding not established;
- external license/source-rights chain not fully verified;
- execution not tested.

---

# 6. Project Aegis thesis implication

Project Aegis should frame the field as splitting into at least two streams:

## Stream 1 — Trading-action agents

These systems output trades, allocations, or positions.

P001 shows that this stream already faces reproducibility and protocol-reporting gaps.

## Stream 2 — Research-artifact agents

These systems output reports, theses, memos, valuation outputs, or decision-support research artifacts.

P016 and P025 show that this stream is emerging, but auditability and evidence grounding remain underdeveloped.

## Bridge thesis

Project Aegis should bridge the two streams:

> Apply the reproducibility and protocol discipline learned from trading-agent research to emerging investment research agents, where the key output is an auditable research artifact rather than a market action.

---

# 7. Updated coding labels

Use these labels when coding papers:

- financial_llm_infrastructure
- financial_qa_agent
- trading_agent
- trading_agent_benchmark
- equity_research_agent_candidate
- investment_research_agent
- research_report_generator_partial
- portfolio_risk_agent
- benchmark_evaluation_framework
- governance_policy_framework
- general_agent_theory

A paper may receive:

- one primary label;
- one secondary label;
- one evidence-role label.

Suggested evidence-role labels:

- core_evidence
- methodological_background
- benchmark_support
- governance_support
- candidate_only

---

# 8. Reviewer challenge and response

## Challenge

A reviewer may argue:

> Investment research agent is an invented category.

## Response

Project Aegis should answer:

> The category is useful because some financial-agent systems now produce research artifacts such as equity research reports, valuation memos, and investment theses rather than direct trades. These systems require different evaluation standards from trading agents. Returns and Sharpe ratios are not enough. Research artifacts require factuality, evidence grounding, valuation assumption transparency, risk completeness, reproducibility, and human-reviewable audit trails.

## Challenge

A reviewer may argue:

> P016 and P025 still do not prove trustworthy investment research.

## Response

Project Aegis should answer:

> Correct. P016 and P025 support the emergence of the category, not its maturity. The gap is precisely that auditability, claim-level grounding, reproducibility, and governance remain incomplete.

---

# 9. Status

Version: v0.2

Status: refined working definition based on P016/P025 comparison.

Still needs testing against at least 20 coded papers and full Search-Round-02 before becoming stable.
