# Checkpoint Review v0.2

## Date

2026-07-09

## Review purpose

This checkpoint reviews the current Project Aegis working output after the first methodology, evidence, scoring, and extraction improvements. It is written as a critical internal audit, not as a promotional summary.

## Current repository state

- PR status: draft
- Branch: `project-aegis-v0.1`
- Changed files: 21
- Added lines: approximately 1602
- Main folder: `Project-Aegis/`
- Current maturity estimate: **Level 1.5 / 5**

## What has been established

### 1. Research direction

The project has a coherent research direction:

> Trustworthy AI Investment Research, with emphasis on reproducibility, auditability, risk-aware evaluation, and human governance.

This is stronger than a generic AI trading-bot topic because it can connect finance, AI agents, research workflow, risk management, and governance.

### 2. Research scaffold

The project now contains:

- research protocol;
- PRISMA-style methodology draft;
- search strategy;
- search log;
- screening log;
- paper database;
- comparative matrix;
- quality scoring rubric;
- provisional quality scores;
- question bank;
- research gap map;
- claim-evidence ledger;
- two early full extraction files.

This is enough to show that the project has moved beyond an idea.

### 3. Evidence discipline has started

The project now separates claims into different confidence levels:

- provisionally supported;
- partially supported;
- plausible but under-evidenced;
- strategic hypothesis.

This is a major improvement because it prevents broad statements from being treated as proven facts.

### 4. Two anchor papers have been extracted

The current anchor papers are:

- P001 — Agentic Trading
- P013 — Finance Agent Benchmark

These support two early claims:

1. LLM trading-agent research has weak reproducibility and protocol comparability.
2. Current LLM agents still struggle with expert-authored real-world finance research tasks.

## Main problems found

### Problem 1: The literature database is still small

The database currently contains 21 papers/reports. This is useful for a v0.1 foundation but too small for a serious systematic review.

Recommended target:

- 50 papers for a defensible early review;
- 100 papers for a strong review;
- 300+ papers for a living literature map.

### Problem 2: Search-Round-01 is not fully reproducible

The current search log honestly records that several searches were exploratory. This is good transparency, but not enough for final methodology.

Missing items:

- exact database result counts;
- sorting method;
- filters;
- exact date/time;
- number screened;
- number excluded;
- exclusion reasons by category.

### Problem 3: Metadata quality is uneven

Some records still have placeholder authors or incomplete source information. This is a credibility risk.

Highest-priority cleanup:

- P007
- P008
- P009
- P010
- P011

### Problem 4: Full extraction is still too shallow

P001 and P013 are extracted mainly at metadata / abstract / interpretation level. They still need:

- section-by-section extraction;
- table extraction;
- figure extraction;
- limitation extraction;
- future work extraction;
- citation-chasing notes.

### Problem 5: Comparative matrix is useful but subjective

The matrix uses values such as `Weak`, `Partial`, `Needs verification`, and `Conceptual`. These are useful early labels, but they need coding rules and evidence references.

Recommendation:

Every matrix value should eventually be backed by either:

- a paper section;
- a table/figure reference;
- a coded extraction field;
- or a clear `unknown / not reported` label.

### Problem 6: Quality scores are provisional

The scoring system is good, but the current numbers are not final. A reviewer would ask why one paper gets 3/4 on reproducibility and another gets 2/4.

Recommendation:

For each score, add:

- evidence note;
- extraction source;
- uncertainty level;
- reviewer challenge.

### Problem 7: The living review draft is still too narrative-heavy

The draft currently has a good argument, but it is ahead of the evidence base. It should later be rewritten using database counts.

Example:

Weak version:

> The field's main bottleneck is trustworthiness.

Stronger version:

> In our initial coded sample, X/Y studies do not report transaction-cost assumptions, X/Y do not provide reproducibility artifacts, and X/Y lack audit-trail mechanisms. This suggests that trustworthiness is a major bottleneck.

## Key questions to answer next

1. Can the category `investment research agent` be defined rigorously enough to survive reviewer criticism?
2. How exactly is an investment research agent different from a trading agent, a financial QA system, or a portfolio optimization model?
3. Is auditability truly underdeveloped, or have we simply not extracted the evidence yet?
4. What is the minimum evidence needed before claiming that risk-first evaluation is a major gap?
5. Which gap is most defensible: reproducibility, auditability, investment workflow modeling, or human governance?
6. Should the first paper be framed as a systematic review, a scoping review, or a research gap map?
7. Should Project Aegis prioritize academic rigor first or GitHub platform visibility first?

## Recommended next work package

### Work Package A — Metadata cleanup

Goal: Make P001-P021 bibliographically credible.

Tasks:

1. Replace all placeholder author fields.
2. Add venue/source details.
3. Add DOI/arXiv ID where available.
4. Add version date for arXiv papers.
5. Mark every uncertain item as `needs verification`.

### Work Package B — Full extraction

Goal: Make the first six core papers audit-ready.

Priority order:

1. P001 Agentic Trading
2. P013 Finance Agent Benchmark
3. P016 FinRobot Equity Research
4. P014 Evaluation and Benchmarking Suite
5. P004 TradingAgents
6. P006 FinMem

### Work Package C — Evidence-backed scoring

Goal: Turn provisional quality scores into defendable scores.

Tasks:

1. Add score justification for every dimension.
2. Add uncertainty flags.
3. Link each score to extraction notes.
4. Re-score after full extraction.

### Work Package D — Search-Round-02

Goal: Create the first actually reproducible search round.

Minimum requirement:

For each database/search string:

- exact search date/time;
- exact search string;
- database/source;
- filters;
- result count;
- screened count;
- retained count;
- excluded count;
- exclusion reasons.

### Work Package E — Rewrite claims

Goal: Make the living review evidence-first.

Tasks:

1. Use the claim-evidence ledger as the source of truth.
2. Replace broad claims with evidence-backed claims.
3. Explicitly label strategic hypotheses.
4. Avoid saying a gap is proven before it is coded.

## Suggested status label

Current label:

> v0.1 structured research foundation

Not yet:

> systematic review

Not yet:

> submission-ready paper

## Bottom line

Project Aegis now has a credible starting structure. Its biggest strength is that it has started to build an evidence-and-audit layer rather than only a narrative review. Its biggest weakness is that the evidence base is still too small and not yet reproducible enough. The next stage should focus less on adding more impressive claims and more on cleaning metadata, completing full extraction, and making each claim traceable to evidence.
