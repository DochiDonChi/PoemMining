# Improvement Summary v0.8

## Date

2026-07-09

## Purpose

This iteration follows the Search-Round-02A pilot by extracting the highest-priority new candidate, P025 FinRpt, and updating the taxonomy and claim-evidence layer accordingly.

## Improvements completed

### 1. P025 FinRpt extraction added

Added:

`03-Full-Extraction/P025-FinRpt-Extraction-v0.1.md`

This is an abstract-level extraction plus Project Aegis interpretation. It does not yet replace full-text section/table/figure extraction.

P025 is high priority because it directly targets:

- equity research report generation;
- dataset construction;
- evaluation system;
- LLM-based multi-agent framework.

This makes it highly relevant to the investment research agent definition.

### 2. Extraction depth tracker updated

Updated:

`03-Full-Extraction/Extraction-Depth-Status-v0.1.csv`

P025 is now tracked as abstract-level plus interpretation. Full-text extraction remains pending.

### 3. Taxonomy coding test updated

Updated:

`05-Definitions/Taxonomy-Coding-Test-v0.1.csv`

The taxonomy coding test now includes 18 records after Search-Round-02A.

Key result:

- P016 and P025 are currently the strongest investment/equity research agent candidates.
- Most other papers remain better classified as trading agents, benchmarks, financial LLM infrastructure, or general agent theory.

### 4. Claim-evidence ledger updated

Updated:

`04-Review-Audit/Claim-Evidence-Ledger-v0.1.csv`

P025 now strengthens:

- C003: investment research agents appear distinguishable from trading agents;
- C006: promising PhD direction in reproducible, auditable, risk-aware multi-agent investment research systems;
- C008: equity research agents may bridge financial QA agents and full investment research systems;
- C010: multi-agent role specialization appears in the reviewed sample.

## Most important conceptual update

Before Search-Round-02A, P016 was the only clear investment/equity research agent candidate.

After adding P025, Project Aegis now has **two stronger anchors** for the investment research agent category:

1. P016 FinRobot Equity Research
2. P025 FinRpt Equity Research Report Generation

This makes the category more defensible, but still not stable. The taxonomy needs at least 20+ coded papers and full-text verification.

## What remains weak

1. P025 extraction is abstract-level only.
2. Full Search-Round-02 has not been executed.
3. Exact database result counts remain unavailable.
4. PRISMA v0.2 is pilot-only.
5. The taxonomy test has 18 records, still short of the 20+ target.
6. Living review draft has not been rewritten to reflect P025 and the updated claims.

## Current status after v0.8

Project Aegis remains:

**Level 2.0 candidate / 5**

It is stronger than before because the investment research agent category now has a second strong candidate anchor. However, it still cannot be confirmed as Level 2 until full Search-Round-02 is executed and PRISMA counts are populated with reproducible result counts.

## Recommended next step

Two good next options:

### Option A — Continue evidence expansion

Run another Search-Round-02B pass to reach 20+ taxonomy-coded records.

### Option B — Deepen evidence quality

Upgrade P025 or P001 from abstract-level extraction to full-text section/table/figure-level extraction.

Recommended choice: **Option A** if the goal is to reach taxonomy stability; **Option B** if the goal is to strengthen the evidence anchor for supervisor-facing discussion.
