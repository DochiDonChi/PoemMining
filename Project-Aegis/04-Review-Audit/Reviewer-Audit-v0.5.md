# Reviewer Audit v0.5

## Date

2026-07-09

## Purpose

This file audits the current Project Aegis v0.1 research output from the perspective of a skeptical PhD supervisor or journal reviewer. It focuses on whether the current evidence, structure, and claims can survive questioning.

## Overall judgement

Project Aegis has become a strong **structured research foundation**, but it is still not a defensible systematic review.

Current maturity estimate remains approximately:

**Level 1.9 / 5**

The project is close to Level 2, but should not be upgraded until Search-Round-02 is done, PRISMA counts are populated, and metadata is cleaned.

## What is genuinely strong

### 1. The research direction is coherent

The project is not merely about predicting stock prices or building a trading bot. It is centered on trustworthy AI investment research, especially:

- reproducibility;
- auditability;
- risk-aware evaluation;
- multi-agent workflows;
- memory;
- human governance.

This framing is stronger and more defensible than a generic LLM trading topic.

### 2. The evidence architecture is emerging

The project now has:

- paper database;
- verification status flags;
- search log;
- claim-evidence ledger;
- quality scores;
- comparative matrix;
- full extraction files;
- maturity assessment;
- checkpoint summaries.

This is a serious improvement because it gives future work an audit trail.

### 3. The six-paper core is useful

The current first-core paper set is coherent:

- P001 — Agentic Trading: survey / reproducibility gap
- P004 — TradingAgents: multi-agent trading baseline
- P006 — FinMem: memory-based trading agent
- P013 — Finance Agent Benchmark: real-world finance research tasks
- P014 — Evaluation and Benchmarking Suite: lifecycle evaluation and governance
- P016 — FinRobot Equity Research: equity research agent / thesis generation

This set supports the transition from trading agents toward investment research agents, but only at an early level.

### 4. The project now admits uncertainty

The database now marks P007-P011 as metadata-unverified or TO_VERIFY. This is a good research habit. It is better to label uncertainty than to fake completeness.

## Main concerns

### Concern 1: Many extractions are still abstract-level

The current extraction files are useful, but they are not yet full extractions in the strict sense. They mostly use abstract-level evidence plus project interpretation.

A true full extraction should include:

1. research question from the paper;
2. method / architecture details;
3. dataset / market universe;
4. evaluation period;
5. transaction-cost assumptions;
6. model versions;
7. prompt / tool setup;
8. main tables;
9. main figures;
10. stated limitations;
11. author-proposed future work;
12. Project Aegis interpretation.

Recommendation: rename current files internally as `abstract-level extraction` or add a status field clearly saying full-text extraction remains pending.

### Concern 2: Claim statuses may be slightly too optimistic

Some claims are appropriately cautious, but others may be upgraded too early.

Examples:

- C005 says risk-first evaluation is `partially_supported`, but P004 only has a risk-management role; this does not prove risk-first evaluation.
- C006 is a strategic synthesis and should remain a hypothesis, not move toward a proven conclusion.
- C010 says multi-agent role specialization is becoming a dominant design pattern, but this is currently based on a small sample. `Dominant` may be too strong.

Recommendation: use weaker language until at least 20 papers are coded.

### Concern 3: The category `investment research agent` is not defined rigorously enough

This is the most important conceptual risk.

Right now, the distinction is intuitive:

- trading agents output trades;
- research agents generate analysis / thesis / answers.

But a reviewer will ask:

> What exactly makes something an investment research agent?

Need a formal definition with necessary and sufficient criteria.

Possible criteria:

1. It produces or supports an investment thesis rather than only a trading signal.
2. It uses evidence from financial documents, market data, or external sources.
3. It performs reasoning over company, macro, valuation, risk, or portfolio context.
4. It outputs a research artifact: report, thesis, recommendation memo, evidence summary, or analyst-style answer.
5. It is not required to execute trades directly.

### Concern 4: Search methodology is still the bottleneck

The project cannot claim to be systematic until Search-Round-02 records:

- source;
- exact query;
- date/time;
- filters;
- result count;
- screened count;
- included count;
- excluded count;
- exclusion reasons.

The current search log is honest but still insufficient.

### Concern 5: PRISMA file is still a placeholder

PRISMA-Flow-Draft-v0.1 is structurally useful, but it still contains TBD values. That is acceptable for v0.1 but should not be shown as a completed methodology.

### Concern 6: Metadata debt remains

P007-P011 should not be used in any argument until metadata is verified. They should remain in the database as candidates only.

### Concern 7: Quality scores need score-by-score justification

The scoring rubric is good. The current quality scores are useful for triage, but not yet reviewer-proof.

Each score needs:

- source evidence;
- rationale;
- uncertainty flag;
- whether the score is abstract-level or full-text-level.

## Critical questions for the next iteration

### Conceptual questions

1. What is the formal definition of an `investment research agent`?
2. What is the boundary between a financial QA agent and an investment research agent?
3. What is the boundary between an investment research agent and a trading agent?
4. Is Project Aegis studying agents, workflows, evaluation frameworks, or all three?
5. What is the first original contribution: taxonomy, gap map, scoring rubric, or framework?

### Methodology questions

1. Is this a systematic review, scoping review, or research gap map?
2. If systematic review, where are the PRISMA numbers?
3. If scoping review, what is the mapping framework?
4. If research gap map, what is the evidence threshold for a gap?
5. How will citation chasing be recorded?

### Evidence questions

1. Which claims are truly supported by evidence rather than project interpretation?
2. Which claims depend only on abstracts?
3. Which claims require full-text extraction before being used?
4. Are P004 and P006 being overused as support for auditability/risk claims?
5. How many papers are needed before claiming a design pattern is dominant?

### Strategic questions

1. Should the next step prioritize Search-Round-02 or full-text extraction?
2. Should unverified papers be temporarily removed from the core database?
3. Should the review title use `systematic review` before PRISMA is complete?
4. Should the repository be moved to a dedicated repo before public sharing?
5. What would impress a Hong Kong PhD supervisor most: methodology rigor, taxonomy, or working prototype?

## Recommended changes

### Immediate changes

1. Add `Definition-Investment-Research-Agent-v0.1.md`.
2. Add `Search-Round-02-Protocol-v0.1.md` before running Search-Round-02.
3. Add `Extraction-Depth-Status.csv` to label each paper as abstract-level, partial full-text, or complete full-text.
4. Downgrade or soften wording around `dominant design pattern` until more papers are coded.
5. Add score-level evidence notes to `Quality-Scores-v0.1.csv`.

### Next research tasks

1. Run Search-Round-02 with exact result counts.
2. Clean P007-P011 metadata.
3. Create formal taxonomy of financial agents.
4. Convert claim-evidence ledger into a visual gap map.
5. Rewrite the living review intro using only supported claims.

## Reviewer decision

**Decision: Keep as draft. Do not merge as final research output.**

This PR is valuable as a research scaffold and should be preserved. But it should not be presented as a completed review. The next milestone should be:

> Level 2: reproducible review foundation.

To reach Level 2, the project needs a reproducible Search-Round-02, clean metadata, populated PRISMA counts, and evidence-backed quality scores.
