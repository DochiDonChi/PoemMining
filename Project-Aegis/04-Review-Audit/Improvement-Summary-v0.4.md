# Improvement Summary v0.4

## Date

2026-07-09

## Purpose

This iteration continued the evidence-deepening work after v0.3. The priority was to complete extraction for the remaining first-core papers before expanding the database too aggressively.

## Improvements completed

### 1. P004 TradingAgents extraction added

Added:

`03-Full-Extraction/P004-TradingAgents-Extraction-v0.1.md`

This strengthens the multi-agent trading baseline. P004 is now used as evidence for role-specialized trading agents and as a comparison point against investment research agents.

### 2. P006 FinMem extraction added

Added:

`03-Full-Extraction/P006-FinMem-Extraction-v0.1.md`

This strengthens the memory-agent pillar. P006 is now used to support the idea that memory is important but risky, because memory can help retain context but may also create stale beliefs or anchoring unless it is auditable.

### 3. Claim-evidence ledger updated

`Claim-Evidence-Ledger-v0.1.csv` was updated with:

- stronger evidence for C003 using P004 as trading-agent contrast;
- clearer support for C004 using P004 and P006 as examples requiring audit-trail verification;
- upgraded C005 from `plausible_but_under_evidenced` to `partially_supported`;
- stronger support for C006 as a strategic synthesis;
- new C009 on memory as necessary but risky;
- new C010 on multi-agent role specialization as a design pattern.

## What became stronger

### Stronger claim 1

**Multi-agent role specialization is becoming an important design pattern in financial agents.**

Supported by P004, P016, and candidate P015.

### Stronger claim 2

**Memory is a necessary but risky component for trustworthy investment research agents.**

Supported by P006, but more memory-agent papers are needed.

### Stronger claim 3

**Risk-first evaluation is now partially supported rather than only plausible.**

P001 shows weak cost/survivorship reporting; P004 includes risk-management roles; P014 supports lifecycle governance. This still requires deeper extraction and broader coding.

## Current status after v0.4

Project Aegis is now approximately:

**Level 1.9 / 5 — strong structured foundation, still not systematic review.**

It is close to Level 2, but not there yet.

## Why it is not yet Level 2

Level 2 requires:

1. complete search log;
2. populated PRISMA counts;
3. clean metadata;
4. extraction templates filled for core papers;
5. quality scores justified.

Current gaps:

- Search-Round-02 not yet done.
- PRISMA counts still placeholders.
- P007-P011 metadata still unverified.
- Full extractions are still abstract-level plus interpretation, not section/table/figure-level.
- Quality scores still need exact evidence references.

## Recommended next step

Choose one of two paths:

### Path A — Reach Level 2 methodology

Run a properly logged `Search-Round-02` and update PRISMA counts.

### Path B — Deepen the first-core paper set

Turn P001, P013, P014, P016, P004, and P006 from abstract-level extraction into section/table/figure-level extraction.

Recommended choice: **Path A** if the goal is to make the review methodology defensible; **Path B** if the goal is to strengthen understanding before searching more papers.
