# PRISMA Methodology v0.1

## Purpose

This document defines the systematic review methodology for Project Aegis. The goal is to make the review process transparent, reproducible, and defensible in front of a PhD supervisor, journal reviewer, or research committee.

## Review title

**Towards Trustworthy AI Investment Research: A Systematic Review and Research Gap Map of LLM-based Financial Agents**

## Review type

This is designed as a hybrid of:

1. **Systematic literature review** — structured search, screening, inclusion/exclusion criteria, and coding.
2. **Research gap map** — identifying underexplored areas and future research opportunities.
3. **Living review** — designed for periodic updates as new papers emerge.

## Main research question

How has the literature on LLM-based financial agents evolved, and what research gaps must be solved before such agents can become credible investment research systems?

## Search period

Initial review period:

- Primary focus: 2023-2026
- Historical baseline: selected pre-2023 papers only if they are necessary for understanding financial NLP, deep learning in quantitative finance, or agent architecture foundations.

## Target literature categories

The search will focus on seven categories:

1. LLM financial agents
2. LLM trading agents
3. Multi-agent financial systems
4. Financial agent memory / RAG / tool use
5. Financial agent benchmark and evaluation
6. Reproducibility, auditability, and explainability in financial AI
7. Governance and systemic risk of agentic AI in financial markets

## Databases and sources

The first version will search:

1. arXiv
2. SSRN
3. ACL Anthology
4. ACM Digital Library
5. IEEE Xplore
6. SpringerLink
7. ScienceDirect
8. Google Scholar
9. OpenReview
10. Regulatory / policy sources such as ESMA, FCA, BIS, IOSCO, IMF, and central bank reports when relevant

## Core search strings

Search strings should be adapted to each database syntax.

### String group A: financial agents

```text
("large language model" OR LLM OR "foundation model") AND (finance OR financial OR investment OR trading OR portfolio) AND (agent OR agents OR "multi-agent" OR "agentic")
```

### String group B: investment research agents

```text
("investment research" OR "equity research" OR "asset management" OR "portfolio management") AND (LLM OR "large language model" OR "AI agent" OR "multi-agent")
```

### String group C: trading agents

```text
("LLM trading" OR "trading agent" OR "financial trading agent" OR "agentic trading")
```

### String group D: benchmark and evaluation

```text
(finance OR trading OR investment) AND (LLM OR "AI agent" OR "multi-agent") AND (benchmark OR evaluation OR reproducibility OR "transaction cost" OR backtest)
```

### String group E: trust and governance

```text
(finance OR financial OR investment) AND (LLM OR "agentic AI" OR "AI agent") AND (trustworthy OR auditability OR explainability OR governance OR regulation OR "systemic risk")
```

## Inclusion criteria

A paper/report is included if it meets at least one of the following:

1. It studies LLM-based or AI-agent-based systems for finance, trading, investment, risk, or portfolio management.
2. It proposes an agent framework, benchmark, evaluation protocol, memory architecture, RAG pipeline, tool-use mechanism, or platform relevant to investment research.
3. It discusses reproducibility, auditability, explainability, governance, systemic risk, or regulatory issues for financial AI agents.
4. It is a high-quality survey that helps position the field of LLM/AI agents in finance.
5. It provides a benchmark, dataset, or evaluation method that can be adapted to trustworthy AI investment research.

## Exclusion criteria

A paper/report is excluded if:

1. It only performs generic stock-price prediction without agentic workflow, reasoning, tool use, memory, benchmark design, or governance relevance.
2. It is a low-quality blog post or commercial article without methodological details.
3. It is unrelated to finance, even if it discusses generic LLM agents, unless the architecture is directly useful for financial-agent design.
4. It has no accessible abstract, paper, report, or stable source.
5. It duplicates another version of the same paper; in this case, the latest or most complete version is retained.

## Screening stages

### Stage 1: Identification

Collect candidate papers from databases and search engines using the search strings above.

### Stage 2: De-duplication

Remove duplicate titles, preprint/journal duplicates, and repeated versions. Keep the latest full version unless the earlier version contains important methodological details.

### Stage 3: Title and abstract screening

Screen titles and abstracts against inclusion/exclusion criteria.

### Stage 4: Full-text eligibility screening

Read full paper or report to determine whether it should be included in the core review.

### Stage 5: Final inclusion

Assign final papers into:

- Core literature
- Supporting literature
- Background literature
- Excluded but relevant notes

## Planned PRISMA flow fields

The final review should report:

- Records identified from databases
- Records identified from citation chasing / manual search
- Duplicates removed
- Records screened by title/abstract
- Records excluded at title/abstract stage
- Full-text papers assessed
- Full-text papers excluded with reasons
- Final included papers

## Paper classification taxonomy

Each included paper will be classified by:

1. Research stream
2. Agent type
3. Financial task
4. Workflow stage
5. Evaluation method
6. Reproducibility level
7. Auditability level
8. Risk-awareness level
9. Governance relevance
10. Project Aegis relevance

## Reproducibility scoring

Each paper receives a reproducibility score:

- 0 = no reproducibility details
- 1 = partial methodological details, no code/data/prompt disclosure
- 2 = some code/data/prompt/model details disclosed
- 3 = sufficient details for attempted reproduction
- 4 = open code, data or data pipeline, prompts, model versions, seeds, costs, and execution rules

## Auditability scoring

Each paper receives an auditability score:

- 0 = no explanation or evidence trail
- 1 = outputs contain explanations but no structured evidence trail
- 2 = cites or retrieves evidence but weak traceability
- 3 = records evidence, reasoning, tool calls, and decision logic
- 4 = full audit trail with contrary evidence, risk flags, and human review mechanism

## Risk-awareness scoring

Each paper receives a risk-awareness score:

- 0 = only return/accuracy metrics
- 1 = includes basic risk metrics such as volatility or drawdown
- 2 = includes transaction costs, turnover, or stress periods
- 3 = includes regime robustness, slippage, liquidity, or failure-mode analysis
- 4 = risk-first framework with explicit unsafe trajectories, governance controls, and human oversight

## Reviewer defense requirement

Every included paper must answer:

1. Why is this paper included?
2. What does it contribute?
3. What does it fail to solve?
4. What gap does it reveal?
5. How does it support or challenge Project Aegis?

## Status

Version: v0.1  
Date: 2026-07-09  
Status: Initial methodology framework created. Needs actual search execution and screening log population.
