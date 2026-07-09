# Research Protocol v0.1

## Working title

**Towards Trustworthy AI Investment Research: A Systematic Review and Research Gap Map of LLM-based Financial Agents**

## Main research question

How has the literature on LLM-based financial agents evolved, and what research gaps must be solved before such agents can become credible investment research systems?

## Secondary research questions

1. What types of financial agents have been studied so far: single-agent, multi-agent, memory-based, platform-based, benchmark-based, or governance-focused?
2. Which parts of the investment workflow are covered: news analysis, fundamental research, macro research, sentiment analysis, technical analysis, risk management, portfolio construction, execution, compliance, or post-trade review?
3. What evaluation metrics are used: accuracy, return, Sharpe ratio, max drawdown, turnover, transaction cost, slippage, regime robustness, decision consistency, reproducibility, auditability?
4. What are the most common limitations reported by authors?
5. Which research gaps are under-explored but high-value for PhD research?

## Search scope

Initial scope: 2023-2026 papers and reports on:

- LLM agents in finance
- AI agents in financial markets
- LLM trading agents
- multi-agent investment systems
- financial agent benchmarks
- financial LLM reproducibility
- financial AI governance and auditability
- investment research automation

## Inclusion criteria

A paper/report should be included if it satisfies at least one of the following:

1. It studies LLM-based or AI-agent-based systems in finance, investment, trading, risk, or portfolio management.
2. It proposes an agent framework, benchmark, evaluation method, memory design, or platform relevant to investment research.
3. It discusses governance, systemic risk, auditability, reproducibility, or regulatory concerns for agentic AI in financial services.
4. It is a high-quality survey that maps AI/LLM applications in finance and helps position the field.

## Exclusion criteria

Exclude papers that only do generic stock-price prediction without agentic workflow, tool use, reasoning, memory, evaluation design, or governance relevance, unless they are necessary historical baselines.

Exclude low-quality articles that make performance claims without enough methodological detail, unless used as negative examples in the reproducibility discussion.

## Data extraction fields

For each paper, extract:

- Paper title
- Year
- Authors
- Venue / source
- URL / DOI
- Research stream
- Research question
- Agent type
- Workflow coverage
- Data sources
- Evaluation metrics
- Transaction cost treatment
- Reproducibility artifacts
- Key contribution
- Main limitation
- Claimed future work
- Relevance to Project Aegis

## Initial taxonomy

1. **Trading agents** — agents that directly output trading actions.
2. **Investment research agents** — agents that support research notes, evidence synthesis, thesis generation, or analyst workflows.
3. **Multi-agent finance systems** — systems using role-specialized agents.
4. **Memory-based agents** — systems emphasizing long-term memory, thesis memory, or market-regime memory.
5. **Benchmark and evaluation papers** — papers proposing evaluation protocols or benchmark environments.
6. **Open-source financial agent platforms** — tools and frameworks for building agents.
7. **Risk, governance, and auditability studies** — papers and reports focusing on safety, accountability, regulation, and systemic effects.

## Quality assessment standard

Each paper will be scored from 0 to 3 on four dimensions:

- **Relevance**: direct relevance to trustworthy investment research agents.
- **Evidence strength**: quality of data, experiment, and argument.
- **Reproducibility**: code, data, prompts, model versions, and execution details.
- **Gap value**: how useful the paper is for identifying future research opportunities.

## Research philosophy

Do not chase model performance claims. Chase evidence quality, reproducibility, auditability, and decision-process trust.
