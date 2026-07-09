# Reviewer Audit v0.7

## Date

2026-07-09

## Purpose

This audit reviews Project Aegis after the v0.6 improvements. The goal is to test whether the project has meaningfully advanced toward Milestone 2.0: Reproducible Review Foundation.

## Overall judgement

Project Aegis is now a strong **Level 2.0 candidate**, but it is still not a confirmed Level 2 foundation.

The project has improved its structure, definitions, scoring discipline, and metadata hygiene. However, the central blocker remains unchanged:

> The project still needs a properly executed Search-Round-02 and populated PRISMA counts.

Without that, it remains a sophisticated research scaffold rather than a reproducible systematic or scoping review.

## What improved since Reviewer Audit v0.6

### 1. Score justifications were added

`Core-Paper-Score-Justifications-v0.1.md` improves transparency. The six first-core papers now have written score rationale, uncertainty notes, and next extraction actions.

This helps answer the reviewer question:

> Why did this paper receive this score?

But it is still provisional because the scores remain mostly abstract-level.

### 2. The taxonomy definition was tested on the current sample

`Taxonomy-Coding-Test-v0.1.csv` is a useful first test of the investment research agent definition.

The most important finding is that only P016 clearly fits the current definition. This is actually a strength, because it prevents overclaiming that the literature is already full of investment research agents.

### 3. Candidate-only records were separated

`Candidate-Only-Records-v0.1.csv` improves bibliography hygiene. P007-P011 are no longer silently mixed into evidence use.

This helps answer the reviewer question:

> Why are unverified records still present?

Answer:

> They are candidate-only records and should not be used as evidence until verified.

## What remains problematic

### Problem 1: The project is accumulating structure faster than evidence

The repository now has many useful files: protocols, definitions, score justifications, audit notes, candidate lists, and extraction trackers.

However, the main evidence-generating task has not happened yet.

Reviewer concern:

> Are you building a research review, or are you building a management system around a review that has not yet been performed?

This is the most important critique at this stage.

### Problem 2: Search-Round-02 remains the main bottleneck

The protocol exists, but the search has not been executed. Until it is executed, the project cannot claim reproducibility.

Required next output:

- `Search-Round-02-Log-v0.1.csv`
- updated screening log;
- updated paper database;
- updated PRISMA counts.

### Problem 3: PRISMA is still only a skeleton

PRISMA requires counts, not only a flow structure. Current PRISMA draft remains useful but incomplete.

A supervisor or reviewer will ask:

- How many records were identified?
- How many were screened?
- How many were excluded?
- Why were they excluded?
- How many were included?

Current answer:

> Not yet available.

### Problem 4: Taxonomy test is still too small

The investment research agent definition has been tested on the current sample, but only around 12 coded records were used. This is useful but insufficient.

The definition should be stress-tested against at least 20-30 papers, including edge cases:

1. finance QA systems;
2. trading systems with analyst-like agents;
3. equity research report generators;
4. valuation tools;
5. portfolio/risk systems;
6. general financial LLMs;
7. benchmark-only papers.

### Problem 5: Score justifications are useful but still not evidence-complete

The score justifications are a good improvement, but most still say that full-text extraction is required. This means they are not final evidence-backed scores.

The next version should include paper-section references, table references, or quote-level evidence summaries.

### Problem 6: The living review draft is increasingly outdated

The audit layer has become much more mature than the living review draft. This is acceptable for now, but the gap is growing.

The living review should eventually be rewritten using:

- the investment research agent definition;
- softened claim-evidence ledger;
- taxonomy coding results;
- candidate-only record policy;
- PRISMA counts from Search-Round-02.

### Problem 7: Dedicated repository issue remains

The project is still inside `PoemMining`, which is unrelated to the research topic. This is acceptable for internal drafting but not ideal for sharing with supervisors or collaborators.

## Key questions to answer next

### Methodology questions

1. When Search-Round-02 is executed, which source will be searched first?
2. Will Google Scholar be used for discovery only, or included in PRISMA counts?
3. How will duplicate preprint and published versions be handled?
4. How will records from citation chasing be separated from database searches?
5. How many records are needed before the review can call itself a scoping review?

### Taxonomy questions

1. Is P016 enough to justify an `investment research agent` category, or should it remain a proposed category until more papers are found?
2. Should `equity research agent` be a subtype of `investment research agent`?
3. Should `benchmark_evaluation_framework` be outside the agent taxonomy entirely?
4. Can a paper have both `trading_agent` and `investment_research_agent` labels?
5. What happens when an agent performs research but outputs a trade?

### Evidence questions

1. Which claims can be used today without full-text extraction?
2. Which claims require P001 full-text extraction?
3. Which claims depend on P014 or P016 beyond abstract-level evidence?
4. Should P004 and P006 support architecture claims only, not auditability/risk claims?
5. Should P015 be removed from claim support until verified?

### Strategic questions

1. Should the next work be Search-Round-02 or P001 full-text extraction?
2. Is the short-term goal supervisor-facing material or publication-facing material?
3. What is the minimum package to show a Hong Kong PhD supervisor?
4. Should a new dedicated repository be created before further work?
5. Should the current PR be merged as a scaffold or kept draft until Level 2 is achieved?

## Recommended next actions

### Immediate priority: execute Search-Round-02

Create:

1. `Search-Round-02-Log-v0.1.csv`
2. `Search-Round-02-Screening-Results-v0.1.csv`
3. updated `PRISMA-Flow-Draft-v0.2.md`
4. updated `Paper-Database-v0.2.csv`

Minimum viable Search-Round-02:

- arXiv only, if time is limited;
- exact queries recorded;
- result counts recorded;
- at least 50 records screened;
- at least 10 retained or explicitly rejected with reasons.

### Second priority: P001 full-text upgrade

If search execution is delayed, upgrade P001 because it is the strongest evidence anchor.

Required additions:

- inclusion criteria;
- reproducibility coding scheme;
- tables;
- figures;
- transaction-cost findings;
- execution-semantics findings;
- limitation and future work extraction.

### Third priority: living review rewrite plan

Do not rewrite the full review yet. First create:

`Living-Review-Rewrite-Plan-v0.1.md`

It should map each section of the draft to supported claims and required evidence.

## Reviewer decision

**Decision: Keep as draft. Continue improving.**

The v0.6 improvements are useful and real, but the next iteration must produce new evidence through Search-Round-02 or full-text extraction. More structure alone will not move the project to confirmed Level 2.

## One-sentence assessment

Project Aegis now has enough structure; the next bottleneck is evidence generation.
