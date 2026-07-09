# P016 Source-Level Extraction v0.1 — FinRobot Equity Research

## Paper

**FinRobot: AI Agent for Equity Research and Valuation with Large Language Models**

arXiv:2411.08804

## Extraction purpose

This file upgrades P016 from abstract-level extraction to a first source-level extraction.

It uses the arXiv abstract record and the public FinRobot GitHub repository to extract source-level facts about the equity research module, multi-agent architecture, deterministic valuation design, report-generation workflow, and reproducibility implications.

No code has been executed. This is source inspection only.

---

# 1. Why P016 matters now

## Source content

P016 explicitly targets equity research and valuation with LLM agents.

The public FinRobot repository now describes FinRobot as an AI agent platform for financial applications, including investment research automation, algorithmic trading strategies, and risk assessment.

The repository also includes a dedicated `finrobot_equity/` module described as an AI-powered equity research report generator.

## Structured extraction

| Field | Extracted value |
|---|---|
| Research stream | equity research agent / valuation / investment thesis generation |
| Core repository | `AI4Finance-Foundation/FinRobot` |
| Core module | `finrobot_equity/` |
| Primary output | equity research reports / investment research outputs |
| Key distinction from trading agents | output is research artifact, not trade action |

## Project Aegis interpretation

P016 is central because it represents the investment research agent side more directly than trading-agent papers.

P025 provides a dataset/benchmark/report-generation anchor. P016 provides an equity research workflow / valuation / deterministic compute anchor.

Together, P016 and P025 are likely the strongest pair for defining the investment research agent category.

## Claim supported

P016 supports:

> Equity research agents are emerging as a distinct financial-agent category focused on research artifacts and valuation outputs rather than trading actions.

## Claim not supported

P016 does not yet prove:

- full institutional auditability;
- complete reproducibility;
- human analyst replacement;
- claim-level evidence grounding.

---

# 2. Repository-level verification

## Source content

The reported repository `AI4Finance-Foundation/FinRobot` is public and not archived.

The root README states that FinRobot is an AI agent platform tailored for financial applications and describes support for investment research automation, algorithmic trading strategies, and risk assessment.

The README links to the FinRobot whitepaper and contains a dedicated FinRobot Desktop / Pro section for equity research.

## Structured extraction

| Field | Verification |
|---|---|
| Repository reachable | yes |
| Visibility | public |
| Default branch | master |
| Archived | false |
| Root README | verified |
| Equity module README | verified |
| License indication | Apache 2.0 stated in equity module README; root license still needs direct verification |

## Project Aegis interpretation

P016 has stronger open-resource status than many finance-agent papers because the codebase is public and contains a substantial equity research module.

However, the repository appears to have evolved beyond the original paper. Some README statements may refer to later FinRobot Desktop / Pro capabilities rather than exactly the 2024 P016 paper.

This creates a version-control issue:

> P016 extraction must separate paper-era claims from current repository capabilities.

## Claim supported

P016 supports:

> A public FinRobot repository exists and contains an equity research module.

## Claim not supported

Do not claim:

> Every current repository feature belongs to the original P016 paper.

---

# 3. Current repository architecture

## Source content

The root README describes FinRobot Desktop / equity research as a multi-agent platform with:

- 1 Lead Agent for orchestration and task routing;
- 5 role-based sub-agents for data, analysis, modeling, synthesis, and report generation;
- 3 debate agents for bull case, bear case, and judge-style investment reasoning.

The README presents this flow:

```text
User Research Request
        ↓
Lead Agent / Orchestrator
        ↓
Data Agent → Analysis Agent → Modeling Agent → Synthesis Agent → Report Agent
        ↓
Bull Agent ↔ Bear Agent → Judge Agent
        ↓
Traceable Investment Research Output
```

## Structured extraction

| Agent type | Role |
|---|---|
| Lead Agent | orchestration and routing |
| Data Agent | data acquisition / source collection |
| Analysis Agent | financial / business analysis |
| Modeling Agent | valuation and modeling |
| Synthesis Agent | integrates research findings |
| Report Agent | generates report artifact |
| Bull Agent | positive investment case |
| Bear Agent | negative investment case |
| Judge Agent | investment reasoning / decision arbitration |

## Project Aegis interpretation

This architecture is highly relevant to Project Aegis because it mirrors a research team rather than a pure trading bot.

It also introduces a debate layer, which could be important for contrary-evidence handling.

However, the current extraction must verify whether these agents are implemented as current product architecture, paper architecture, or README-level documentation.

## Claim supported

P016 supports:

> FinRobot's public repository describes a role-based multi-agent equity research workflow.

## Claim not supported

It does not yet prove:

> The agents generate independently auditable claims or preserve full evidence trails.

---

# 4. Deterministic computation versus LLM narration

## Source content

The root README states a key design principle:

> Numbers are code-calculated. Narratives are LLM-assisted. Every output is provenance-tracked.

It states that financial numbers are generated by pure-Python compute operators, not by the language model. LLMs are used for reasoning, synthesis, explanation, and report writing.

The README lists deterministic valuation methods including:

- DCF;
- DDM;
- LBO;
- WACC;
- comparable-company analysis;
- Monte Carlo.

## Structured extraction

| Design principle | Meaning |
|---|---|
| Code-calculated numbers | financial computations should be deterministic |
| LLM-assisted narratives | language model writes explanations / synthesis |
| Provenance tracking | outputs should be traceable to compute/data path |
| Valuation engines | DCF, DDM, LBO, comps, WACC, Monte Carlo |

## Project Aegis interpretation

This is one of the strongest Project Aegis-relevant design ideas found so far.

For trustworthy investment research agents, valuation numbers should not be hallucinated by an LLM. They should be calculated by deterministic code, while the LLM explains assumptions and implications.

This can become a Project Aegis design principle:

> deterministic compute for numbers, LLM narration for explanation, evidence ledger for claims.

## Claim supported

P016 supports:

> A credible equity research agent architecture should separate deterministic financial computation from LLM narrative generation.

## Claim not supported

It does not yet prove:

> FinRobot's implementation fully enforces this separation in every report output.

---

# 5. Equity module structure

## Source content

`finrobot_equity/README.md` describes the equity research module as a report generator that fetches financial data, runs LLM-based analysis, and produces professional multi-page HTML/PDF reports.

The module architecture includes:

- `generate_financial_analysis.py` — data fetching and analysis;
- `create_equity_report.py` — HTML report generation;
- `generate_pdf_report.py` — optional PDF generation;
- modules for market data, financial processing, text generation agents, charts, templates, valuation, sensitivity, catalysts, news integration, retail sentiment, and report structure;
- `equity_agents/` for section-level report agents.

## Structured extraction

| Component | Function |
|---|---|
| Market data API | fetch financial and market data |
| Financial data processor | metrics extraction and forecasting |
| Valuation engine | valuation modeling |
| Text generation agents | LLM-based section writing |
| Chart generator | visual output |
| HTML renderer | report generation |
| PDF generator | optional PDF output |
| Equity agents | section-specific analysis and writing |
| Tests | unit tests for report generation and modules |

## Project Aegis interpretation

P016 is stronger than a paper-only system because it includes an actual module layout for equity research.

The presence of valuation and sensitivity modules is especially important because P025 is stronger on dataset/report benchmark, while P016 appears stronger on valuation workflow.

## Claim supported

P016 supports:

> The FinRobot repository contains a dedicated equity research module with data, valuation, charting, text-generation, and report-generation components.

## Claim not supported

It does not yet prove:

> The full equity research pipeline is reproducible without API keys, local setup, and execution testing.

---

# 6. Equity research pipeline

## Source content

The equity module README describes a two-step pipeline:

1. `generate_financial_analysis.py` fetches data, processes financial metrics, generates 3-year forecasts, runs peer comparison, and performs AI text generation.
2. `create_equity_report.py` loads analysis outputs, auto-fetches market data, generates charts, renders HTML report, and validates/regenerates sections.

The README also provides command-line examples for NVDA.

## Structured extraction

| Pipeline step | Output |
|---|---|
| Data fetching | raw financial and market data |
| Metrics processing | financial metrics and forecasts |
| Peer comparison | comparable-company context |
| AI text generation | thesis / sections / qualitative analysis |
| Chart generation | report visualizations |
| HTML report rendering | research report artifact |
| Optional PDF generation | formatted report artifact |

## Project Aegis interpretation

This gives a more realistic research workflow than a one-shot LLM prompt.

It also creates an opportunity for auditability because intermediate CSV, JSON, TXT, HTML, and PDF artifacts may exist.

However, auditability depends on whether these artifacts preserve data sources, formulas, model prompts, and section-level provenance.

## Claim supported

P016 supports:

> FinRobot's equity module has a staged pipeline for financial analysis and report generation.

## Claim not supported

It does not yet prove:

> The staged pipeline produces claim-level auditable investment reports.

---

# 7. Data and API dependencies

## Source content

The equity module README states API requirements:

| Service | Required | Purpose |
|---|---|---|
| Financial Modeling Prep | yes | financial data, market metrics, peer comparison |
| OpenAI | yes | AI-powered text generation for report sections |
| Adanos Finance API | optional | retail sentiment insights for Reddit, X.com, and Polymarket |

## Structured extraction

P016 depends on live external APIs.

This means reproducibility requires:

- API keys;
- API data availability;
- API version stability;
- model version stability;
- preserved output snapshots.

## Project Aegis interpretation

This is both a strength and a weakness.

Strength: it makes the system live and practically useful.

Weakness: reproducibility may suffer if API outputs change over time.

Project Aegis should require source snapshots or data-version logging for research-grade reproduction.

## Claim supported

P016 supports:

> FinRobot uses live external data and LLM APIs to generate equity research reports.

## Claim not supported

It does not yet support:

> Independent researchers can reproduce the same report without preserving API snapshots and model versions.

---

# 8. Example reports

## Source content

The root README links to example equity research reports for:

- NVDA;
- MSFT;
- COP;
- TSLA;
- META.

## Structured extraction

These examples are important because they can be inspected later for:

- report structure;
- evidence links;
- valuation tables;
- assumptions;
- charts;
- risk section;
- source provenance;
- citation behavior.

## Project Aegis interpretation

Example reports may become one of the best ways to assess whether FinRobot outputs are only polished narratives or truly traceable research artifacts.

## Claim supported

P016 supports:

> Public example reports are linked from the repository.

## Claim not supported

Until inspected, these examples do not prove claim-level evidence grounding.

---

# 9. Comparison with P025 after first P016 source extraction

| Dimension | P016 FinRobot | P025 FinRpt |
|---|---|---|
| Core role | equity research workflow / valuation platform | ERR dataset / benchmark / generation framework |
| Output | HTML/PDF equity research reports and investment research outputs | six-section ERRs |
| Data | live APIs including FMP, OpenAI, optional Adanos; repository lists data providers | CSI800 dataset with company info, financials, announcements, news, prices, indices |
| Architecture | lead orchestrator, pipeline agents, debate agents, deterministic compute | 9 agents across extraction, analysis, prediction modules |
| Valuation | explicit DCF, DDM, LBO, comps, WACC, Monte Carlo claims | less valuation-focused; stronger dataset/report-generation benchmark |
| Reproducibility | public repo, CLI commands, API-dependent, execution not tested | public repo and dataset partially verified, execution not tested |
| Auditability | provenance-tracking claimed, not yet verified at claim level | source provenance partial, claim-level grounding not established |
| Best Project Aegis use | valuation/research workflow anchor | dataset/benchmark/report artifact anchor |

## Project Aegis conclusion

P016 and P025 are complementary:

- P016 is stronger for practical equity research workflow and valuation-system architecture.
- P025 is stronger for benchmark/dataset/report-generation evaluation.

Together they support the emerging category of equity research agents, but neither alone proves trustworthy investment research.

---

# 10. Updated P016 status

## Current classification

P016 can now be classified as:

`source_level_repository_and_equity_module_extraction_started`

## Stronger evidence

P016 is now stronger as:

- an equity research workflow anchor;
- a valuation-system architecture anchor;
- a deterministic-compute / LLM-narration design anchor;
- an open-repository candidate;
- a P025 comparison anchor.

## Remaining weaknesses

1. Root LICENSE file still needs direct verification.
2. Core Python scripts need inspection.
3. Equity agents need inspection.
4. Valuation engine needs inspection.
5. Example reports need inspection.
6. Evidence links and numeric provenance need verification.
7. Code has not been run.
8. P016 paper text and current repo version may differ.

---

# 11. Recommended next step

Create:

`03-Full-Extraction/P016-P025-Equity-Research-Agent-Comparison-v0.1.md`

This should be the next synthesis file because P016 and P025 together define the investment research agent category more strongly than either paper alone.

After that, continue deeper source verification of P016 modules:

- `generate_financial_analysis.py`;
- `create_equity_report.py`;
- `valuation_engine.py`;
- `equity_agents/agent_manager.py`;
- example reports.
