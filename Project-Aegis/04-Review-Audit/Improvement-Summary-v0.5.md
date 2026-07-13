# Improvement Summary v0.5

## Date

2026-07-09

## Purpose

This iteration implements the recommendations from Reviewer Audit v0.5. The goal is to reduce conceptual ambiguity, improve methodological discipline, and prevent overclaiming.

## Improvements completed

### 1. Investment research agent definition added

Added:

`05-Definitions/Definition-Investment-Research-Agent-v0.1.md`

This file provides a working definition and minimum criteria for coding a system as an investment research agent. It also distinguishes investment research agents from financial QA agents, trading agents, portfolio optimization models, and financial LLM infrastructure.

### 2. Search-Round-02 protocol added

Added:

`01-Methodology/Search-Round-02-Protocol-v0.1.md`

This file defines the first strict reproducible search round. It includes target sources, mandatory logging fields, search strings, inclusion/exclusion criteria, exclusion reason codes, and PRISMA update requirements.

### 3. Extraction depth status added

Added:

`03-Full-Extraction/Extraction-Depth-Status-v0.1.csv`

This file makes clear that the six extraction files are currently abstract-level plus interpretation, not complete full-text extractions. This prevents overclaiming.

### 4. Claim language softened

Updated:

`04-Review-Audit/Claim-Evidence-Ledger-v0.1.csv`

Key changes:

- `The strongest PhD direction` became `A promising PhD direction`.
- `Dominant design pattern` became `Emerging design pattern in the currently reviewed sample`.
- `Risk-first evaluation is a necessary next direction` became `Risk-aware evaluation is an important candidate gap but not yet proven as risk-first field direction`.
- `Auditability is underdeveloped` became `Auditability appears underdeveloped but needs direct coding`.

This makes the project more defensible.

### 5. Quality scores made more transparent

Updated:

`02-Comparative-Matrix/Quality-Scores-v0.1.csv`

Added:

- `evidence_level`
- `uncertainty`
- `next_score_action`

This clarifies that the current scores are research-triage scores, not final publication-ready scores.

## What became stronger

### Stronger conceptual foundation

The project now has a working definition for investment research agents, reducing the risk that reviewers reject the category as vague.

### Stronger methodology foundation

Search-Round-02 now has a protocol before execution. This is better than searching first and justifying the method afterward.

### Stronger auditability of our own process

Extraction depth is now tracked explicitly. The project can no longer accidentally imply that abstract-level extraction is full-text extraction.

### Stronger research tone

The claim-evidence ledger now uses more cautious language. This is important for academic credibility.

## What remains weak

1. Search-Round-02 has not been executed.
2. PRISMA counts remain placeholders.
3. P007-P011 metadata remains unresolved.
4. Full-text section/table/figure extraction remains pending.
5. The investment research agent definition has not yet been tested on 20+ papers.
6. Quality scores still need full-text evidence notes.

## Current status after v0.5

Project Aegis is now approximately:

**Level 2.0 candidate / 5 — methodology scaffold is now close to reproducible foundation, but Search-Round-02 execution is still required.**

It should not be formally marked Level 2 until:

- Search-Round-02 is executed;
- PRISMA counts are populated;
- metadata for P007-P011 is cleaned or removed from core use;
- quality scores are linked to full-text evidence.

## Recommended next step

Execute `Search-Round-02` using the protocol, or clean P007-P011 metadata if the goal is to remove bibliography debt before expanding the database.
