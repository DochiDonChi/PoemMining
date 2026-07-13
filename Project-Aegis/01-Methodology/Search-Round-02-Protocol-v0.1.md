# Search-Round-02 Protocol v0.1

## Purpose

Search-Round-02 is designed to become the first reproducible search round for Project Aegis. Search-Round-01 was useful for discovery, but it mixed exploratory web search with direct-source verification. Search-Round-02 must be strict enough to support PRISMA-style reporting.

## Search objective

Expand the literature database from 21 candidate records toward 50+ screened records while recording exact search counts, screening decisions, and exclusion reasons.

## Sources to search

Search-Round-02 should search the following sources separately:

1. arXiv
2. SSRN
3. ACL Anthology
4. ACM Digital Library
5. IEEE Xplore
6. Google Scholar
7. OpenReview
8. ESMA / FCA / BIS / IOSCO / IMF / central bank policy sources

## Mandatory logging fields

Every query must be recorded with:

- search_id
- date_utc
- time_utc
- source
- exact_search_string
- filters
- sort_order
- result_count_reported
- results_screened
- results_retained
- results_excluded
- exclusion_reason_summary
- retained_paper_ids
- notes

## Search strings

### Query A: Core financial agents

```text
("large language model" OR LLM OR "foundation model") AND (finance OR financial OR investment OR trading OR portfolio) AND (agent OR agents OR "multi-agent" OR agentic)
```

### Query B: Investment research agents

```text
("investment research" OR "equity research" OR "asset management" OR "portfolio management") AND (LLM OR "large language model" OR "AI agent" OR "multi-agent")
```

### Query C: Agentic trading

```text
("LLM trading" OR "trading agent" OR "financial trading agent" OR "agentic trading" OR "multi-agent trading")
```

### Query D: Evaluation and benchmark

```text
(finance OR trading OR investment OR portfolio) AND (LLM OR "AI agent" OR "multi-agent") AND (benchmark OR evaluation OR reproducibility OR backtest OR "transaction cost")
```

### Query E: Trust and governance

```text
(finance OR financial OR investment OR trading) AND (LLM OR "AI agent" OR "agentic AI") AND (trustworthy OR auditability OR explainability OR governance OR regulation OR accountability OR "systemic risk")
```

### Query F: Memory and RAG

```text
(finance OR trading OR investment) AND (LLM OR "AI agent") AND (memory OR RAG OR retrieval OR "tool use" OR planning OR reflection)
```

## Inclusion criteria

Include a paper/report if it satisfies at least one of the following:

1. It studies LLM-based or AI-agent-based systems for finance, investment research, risk, trading, portfolio management, or financial analysis.
2. It proposes an agent framework, benchmark, memory system, RAG system, tool-use mechanism, or evaluation protocol relevant to financial agents.
3. It discusses reproducibility, auditability, explainability, governance, regulation, or systemic risk for agentic AI in finance.
4. It is a high-quality survey that helps position financial LLMs, financial agents, or general LLM-agent methodology.

## Exclusion criteria

Exclude a record if:

1. It is generic stock prediction without agentic workflow, tool use, memory, benchmark, or governance relevance.
2. It is not finance-related.
3. It is a blog, advertisement, or commercial page without methodological detail.
4. It is a duplicate or earlier version of a later complete record.
5. It has no accessible abstract, paper, or stable record.

## Exclusion reason codes

Use these codes in the screening log:

- E01 generic_prediction_only
- E02 not_agentic
- E03 not_finance_related
- E04 no_accessible_record
- E05 duplicate_or_superseded
- E06 commercial_or_low_method_detail
- E07 insufficient_relevance_to_project_aegis
- E08 already_in_database

## Screening output

Each retained record should be added to:

1. `Paper-Database-v0.1.csv` or next version;
2. `Screening-Log-v0.1.csv` or next version;
3. `Search-Log-v0.1.csv` or next version.

## Minimum target

Search-Round-02 should aim to produce:

- at least 100 records identified;
- at least 50 title/abstract screened;
- at least 20 retained new candidate records;
- at least 10 records marked as high-priority for extraction.

## PRISMA update requirement

After Search-Round-02, update:

- records identified;
- duplicates removed;
- records screened;
- records excluded;
- full texts assessed;
- full texts excluded with reasons;
- final included papers.

## Status

Version: v0.1

Status: protocol ready; Search-Round-02 not yet executed.
