# Search Strategy v0.1

## Objective

The search strategy is designed to collect literature for a systematic review on **LLM-based financial agents** and **trustworthy AI investment research systems**.

## Search design principle

The search should not only find papers that say "LLM trading agent". It should also capture adjacent work in:

- AI agents in finance
- multi-agent trading systems
- investment research automation
- benchmark and evaluation
- reproducibility
- auditability
- governance and systemic risk

## Search query groups

### Group A: Core LLM financial agents

```text
("large language model" OR LLM OR "foundation model") AND (finance OR financial OR investment OR trading OR portfolio) AND (agent OR agents OR "multi-agent" OR agentic)
```

Expected result type:

- broad set of LLM finance agent papers
- surveys
- trading frameworks
- agent platforms

### Group B: Trading agents

```text
("LLM trading" OR "trading agent" OR "financial trading agent" OR "agentic trading" OR "AI trading agent")
```

Expected result type:

- papers focused on trading actions
- benchmark papers
- simulation papers

### Group C: Investment research workflow

```text
("investment research" OR "equity research" OR "asset management" OR "portfolio management") AND (LLM OR "large language model" OR "AI agent" OR "multi-agent")
```

Expected result type:

- investment management agent papers
- portfolio research systems
- AI analyst / AI research assistant papers

### Group D: Memory / RAG / tool use

```text
(finance OR financial OR trading OR investment) AND (LLM OR "AI agent") AND (memory OR RAG OR retrieval OR "tool use" OR planning OR reflection)
```

Expected result type:

- memory-based financial agents
- RAG-based financial analysis systems
- tool-using financial LLM systems

### Group E: Benchmark and evaluation

```text
(finance OR trading OR investment OR portfolio) AND (LLM OR "AI agent" OR "multi-agent") AND (benchmark OR evaluation OR reproducibility OR backtest OR "transaction cost")
```

Expected result type:

- benchmark environments
- evaluation protocols
- reproducibility studies
- backtesting methodology papers

### Group F: Trust, auditability, and governance

```text
(finance OR financial OR investment OR trading) AND (LLM OR "AI agent" OR "agentic AI") AND (trustworthy OR auditability OR explainability OR governance OR regulation OR "systemic risk" OR accountability)
```

Expected result type:

- governance reports
- regulatory papers
- systemic-risk studies
- explainable financial AI papers

## Source-specific search notes

### arXiv

Use broad keyword search and sort by relevance and date. Prioritize 2023-2026 papers. Check all versions if a paper has updated methodology.

### SSRN

Search for finance-oriented preprints and working papers. SSRN may contain investment-management papers not indexed quickly elsewhere.

### ACL Anthology

Search for NLP/LLM papers in finance, especially surveys, benchmarks, and evaluation studies.

### ACM Digital Library

Search for agent systems, financial applications, and reproducibility/evaluation conference papers.

### IEEE Xplore

Search for AI finance systems, multi-agent frameworks, and trustworthy AI engineering.

### Google Scholar

Use for citation chasing and discovering related versions. Do not rely on Google Scholar alone because results are less reproducible.

### Regulatory / policy sources

Search ESMA, FCA, BIS, IOSCO, IMF, Bank of England, Federal Reserve, and central bank reports for governance and systemic-risk discussion.

## Search log requirements

For each search session, record:

- Date
- Source / database
- Search string
- Filters used
- Number of results returned
- Number screened
- Number retained
- Notes

## Manual search / snowballing

For every core included paper:

1. Check references for earlier related work.
2. Check citing papers for newer related work.
3. Check the authors' GitHub or project page when relevant.
4. Check whether a benchmark or dataset has a separate paper.

## Version control

Each search round should be logged as:

- Search-Round-01
- Search-Round-02
- Search-Round-03

The living review should report which search round generated the current paper list.
