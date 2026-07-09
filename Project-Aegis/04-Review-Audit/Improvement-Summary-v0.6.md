# Improvement Summary v0.6

## Date

2026-07-09

## Purpose

This iteration implements the next actions from Reviewer Audit v0.6. The goal is to move Project Aegis closer to Milestone 2.0 by improving score justification, testing the investment research agent definition, and isolating unverified candidate records.

## Improvements completed

### 1. Core paper score justifications added

Added:

`02-Comparative-Matrix/Core-Paper-Score-Justifications-v0.1.md`

This file explains the provisional scores for the six first-core papers:

- P001 Agentic Trading
- P004 TradingAgents
- P006 FinMem
- P013 Finance Agent Benchmark
- P014 Evaluation and Benchmarking Suite
- P016 FinRobot Equity Research

It records:

- current score;
- justification;
- uncertainty;
- next action.

This makes the quality scoring more transparent and easier to challenge.

### 2. Taxonomy coding test added

Added:

`05-Definitions/Taxonomy-Coding-Test-v0.1.csv`

This applies the investment research agent definition to the current database sample. Early result:

- P016 clearly fits as an equity research / investment research agent.
- P013 is better coded as a benchmark for finance research tasks.
- P004 and P006 remain trading-agent papers.
- P017/P018 are financial LLM infrastructure, not agents.
- P021 is general agent theory.

This shows that the definition is useful but still needs testing on at least 20 papers.

### 3. Candidate-only records separated

Added:

`02-Paper-Database/Candidate-Only-Records-v0.1.csv`

This isolates P007-P011 because their metadata is unverified. These records should not be used as evidence until verified.

## What became stronger

### Stronger scoring discipline

Scores are no longer just numbers in a table. The six core papers now have written justification and uncertainty notes.

### Stronger taxonomy discipline

The investment research agent definition has been tested on the current sample. This revealed that only one current paper, P016, clearly fits the definition. That is useful because it prevents overclaiming.

### Stronger bibliography hygiene

Unverified records are now visibly separated as candidate-only. This reduces the risk that the living review accidentally cites uncertain metadata.

## What remains weak

1. Search-Round-02 still has not been executed.
2. PRISMA counts remain placeholders.
3. The definition has been tested on only 12 records, not 20+.
4. Core extractions remain abstract-level plus interpretation.
5. P007-P011 still require verification or replacement.
6. The living review draft has not yet been rewritten using the updated claim language.

## Current status after v0.6

Project Aegis remains:

**Level 2.0 candidate / 5**

It is stronger than before because the project now has:

- concept definition;
- search protocol;
- extraction depth tracker;
- core score justifications;
- taxonomy coding test;
- candidate-only metadata isolation.

But it still cannot be confirmed as Level 2 because the reproducible search round has not been executed.

## Recommended next step

Execute Search-Round-02 and populate PRISMA counts. This is now the main blocker.

Alternative if search execution is delayed:

Upgrade P001 extraction to section/table/figure-level extraction because P001 is the strongest current evidence anchor.
