# Research Maturity Assessment v0.1

## Purpose

This file evaluates the maturity of Project Aegis after the first improvement cycle. It is deliberately critical. The goal is to prevent the project from looking more mature than it actually is.

## Current maturity level

**Level 1.5 / 5 — structured research foundation, not yet systematic review.**

## Maturity scale

### Level 0 — Idea only

- Topic exists but no structured evidence.

### Level 1 — Research scaffold

- Research question, draft protocol, first paper list, and rough gap map exist.

### Level 2 — Reproducible review foundation

- Search log is complete.
- PRISMA counts are populated.
- Metadata is clean.
- Paper extraction templates are filled for core papers.
- Quality scores are justified.

### Level 3 — Defensible systematic review draft

- 50+ core papers included.
- Full comparative matrix complete.
- Taxonomy is stable.
- Gap map is evidence-backed by counts and coded limitations.
- Draft contains citations and avoids unsupported broad claims.

### Level 4 — Submission-ready review

- Review has introduction, methodology, results, taxonomy, discussion, limitations, and conclusion.
- All claims are supported by database counts or citations.
- Figures and tables are publication-quality.
- Search strategy is reproducible.

### Level 5 — Living research platform

- Public database, update protocol, citation graph, gap atlas, question bank, and reproducible code/tools exist.
- External researchers can reuse the platform.

## What has improved

1. The project now has a stronger methodological layer.
2. Search-Round-01 is documented instead of hidden.
3. The project now admits that Search-Round-01 is not fully reproducible.
4. A bibliography cleanup file exists to prevent placeholder metadata from being forgotten.
5. A numerical quality-scoring framework has been applied to the first 10 papers.
6. Two full extraction files have been created for P001 and P013.

## Remaining weaknesses

### 1. Search reproducibility remains incomplete

Search-Round-01 mixed exploratory web search and direct source verification. This is useful for discovery but insufficient for a publishable systematic review.

### 2. Metadata is still incomplete

P007-P011 still require author and source verification.

### 3. Full extraction is still shallow

P001 and P013 are extracted at abstract-level plus interpretation level. Full-text section-by-section extraction is still pending.

### 4. Quality scores are provisional

Quality scores are useful for triage but not yet publication-ready. Each score needs exact evidence notes.

### 5. Living review draft is still narrative-heavy

The current draft makes plausible claims but lacks enough quantified support from the database.

## Next milestone

**Milestone 1.2: Make the first 10 core papers audit-ready.**

Requirements:

1. Clean metadata for P001-P010.
2. Complete full extraction for P001, P013, P016, P014, P004, P006.
3. Create a `Claim-Evidence-Ledger-v0.1.csv`.
4. Convert the gap map from narrative gaps into evidence-backed gaps.
5. Update PRISMA flow with Search-Round-01 provisional counts.

## Decision

Do not merge this PR as final research output. Keep it as a draft foundation. Merge only if the goal is to preserve the research scaffold in the main branch. If the goal is academic quality, continue iterating before merge.
