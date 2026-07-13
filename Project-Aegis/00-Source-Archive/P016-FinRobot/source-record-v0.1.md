# P016 Source Record v0.1 — FinRobot Equity Research

## Paper

**FinRobot: AI Agent for Equity Research and Valuation with Large Language Models**

## Source metadata

| Field | Value |
|---|---|
| Paper ID | P016 |
| Title | FinRobot: AI Agent for Equity Research and Valuation with Large Language Models |
| Authors | Tianyu Zhou; Pinqiao Wang; Yilin Wu; Hongyang Yang |
| arXiv ID | 2411.08804 |
| arXiv abstract URL | https://arxiv.org/abs/2411.08804 |
| Submitted | 2024-11-13 |
| Reported code repository | https://github.com/AI4Finance-Foundation/FinRobot |
| Repository visibility | public verified |
| Default branch | master |
| Repository archived | false |
| Repository license | README badge / equity module README indicate Apache 2.0; full root LICENSE verification still pending |
| Source archive status | metadata and repository-level facts stored; full PDF not copied |

## Source-level facts captured

| Fact | Source-level note |
|---|---|
| Main domain | equity research and valuation |
| Platform | FinRobot / FinRobot Pro / FinRobot Desktop ecosystem |
| Core equity module | `finrobot_equity/` |
| Claimed output | professional equity research reports, investment thesis, valuation overview, risk assessment |
| Architecture | multi-agent equity research platform |
| Orchestrator | Lead Agent / Orchestrator |
| Pipeline agents | Data Agent, Analysis Agent, Modeling Agent, Synthesis Agent, Report Agent |
| Debate agents | Bull Agent, Bear Agent, Judge Agent |
| Deterministic computation principle | numbers are code-calculated, narratives are LLM-assisted |
| Valuation methods | DCF, DDM, LBO, comparable-company analysis, WACC, Monte Carlo |
| Data providers | FMP, Finnhub, yfinance, SEC EDGAR, Adanos, NewsAggregator, FX reported in README |
| Equity module API requirements | FMP API required; OpenAI required; Adanos optional |
| Equity module report pipeline | generate financial analysis, then create equity report, optional PDF generation |
| Report examples | NVDA, MSFT, COP, TSLA, META example reports linked in README |

## Repository storage policy

For now, store:

- source metadata;
- source URLs;
- extracted facts;
- verification notes;
- source-level extraction files.

Do not store:

- full paper PDF;
- copied example reports;
- generated outputs from external repo;
- API-derived data;
- any file whose redistribution terms are unclear.

## Next verification tasks

1. Verify root `LICENSE` file.
2. Inspect `finrobot_equity/core/src/generate_financial_analysis.py`.
3. Inspect `finrobot_equity/core/src/create_equity_report.py`.
4. Inspect `equity_agents/agent_manager.py` and agent files.
5. Inspect valuation engine and deterministic compute modules.
6. Inspect example reports for evidence links / numeric provenance.
7. Determine whether reports are claim-level auditable or mainly section-level traceable.
