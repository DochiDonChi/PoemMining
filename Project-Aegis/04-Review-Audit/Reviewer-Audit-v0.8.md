# Reviewer Audit v0.8

## Date

2026-07-09

## Audit scope

This audit reviews the current Project Aegis workspace after:

1. completion of the bilingual mobile reading layer for twelve priority/candidate papers;
2. P001 section-level extraction scaffold;
3. first-pass P001 core table/figure extraction covering Figure 1, Figure 2, Table 1, and Table 3;
4. update of extraction depth tracker to mark P001 as section-level plus partial core table/figure extraction.

## Overall assessment

Project Aegis has improved meaningfully since the earlier audit rounds.

The project is no longer only a concept map or reading list. It now has:

- a clear research protocol;
- a paper database;
- candidate-only metadata isolation;
- a claim-evidence ledger;
- a quality-scoring rubric;
- a bilingual mobile learning layer;
- a working definition of investment research agent;
- taxonomy coding;
- extraction-depth tracking;
- first-pass full-text extraction upgrade for P001.

However, the project is still not a publishable systematic review. It remains a strong **Level 2.0 candidate**, not a confirmed Level 2 review.

The main reason is simple: the project has built strong scaffolding, but the hard evidence layer is still incomplete.

## What is strong now

### 1. Learning usability is now strong

The bilingual ebook layer is a genuine strength. It makes the literature usable for daily study and oral explanation.

This is useful for:

- PhD interview preparation;
- supervisor discussion;
- self-study;
- English academic vocabulary development;
- remembering paper-level contributions.

This is not a normal feature of early research repositories. It is a practical advantage.

### 2. The project now has honest uncertainty markers

The repository repeatedly marks current limitations:

- abstract-level extraction;
- table/figure pending;
- candidate-only metadata;
- provisional PRISMA counts;
- Search-Round-02 not completed.

This improves credibility because the project does not pretend to be more mature than it is.

### 3. P001 is now more than abstract-level

P001 has been upgraded from abstract-level extraction to section-level scaffold plus partial core table/figure extraction.

This is a meaningful improvement because P001 is the strongest current anchor for the reproducibility-gap argument.

The extraction now captures:

- agency boundary logic;
- reasoning-flow framing;
- selected related-work positioning;
- study selection denominator logic.

### 4. The trading-agent versus investment-research-agent boundary is becoming clearer

The project increasingly distinguishes:

- trading agents;
- financial QA agents;
- report generators;
- equity research agents;
- investment research agents;
- governance/evaluation frameworks.

This boundary is essential. Without it, the thesis would become too broad and academically weak.

## Major concerns

### Concern 1 — P001 table/figure extraction may still be too interpretive

The P001 core table/figure extraction is useful, but it is still written in a translated, Project-Aegis-oriented style.

A strict reviewer may ask:

> Are these extracted details directly from the paper, or are they the project's interpretation of the paper?

The current extraction should therefore separate more clearly:

1. literal source content;
2. paraphrased extraction;
3. Project Aegis interpretation;
4. claim supported;
5. claim not supported.

This is already partially done, but the distinction should be made even stricter in future extraction files.

### Concern 2 — The hardest P001 evidence is still pending

The strongest reproducibility-gap evidence does not mainly come from Figure 1 or Figure 2.

It comes from:

- protocol reporting tables;
- reproducibility tier tables;
- R0-R3 definitions;
- reporting checklist;
- study-level evidence ledger.

These are still pending.

Until these are extracted, Project Aegis can say that P001 has begun deeper extraction, but should not yet treat P001 as fully extracted.

### Concern 3 — P025 remains too shallow relative to its importance

P025 is currently one of the strongest anchors for the investment research agent category, but its extraction remains abstract-level.

This creates an imbalance:

- reproducibility-gap side: P001 is becoming stronger;
- investment-research-agent side: P016/P025 are still weaker than they should be.

If the project is meant to be about investment research agents rather than only trading-agent reproducibility, P025 needs full-text extraction soon.

### Concern 4 — Search-Round-02 is still not complete

The repository has a Search-Round-02 protocol and a Search-Round-02A pilot, but not a full reproducible Search-Round-02.

A reviewer will ask:

> How do you know this literature set is not cherry-picked?

The answer is currently:

> We do not fully know yet. The current set is a seed/pilot set, and the full search remains pending.

This is acceptable for a working repository, but not for a systematic review claim.

### Concern 5 — P007-P011 metadata debt remains unresolved

The candidate-only isolation is good, but unresolved candidate records still create cleanup debt.

A reviewer may ask:

> Are these papers real, duplicated, renamed, or incorrectly captured?

This should be resolved before the repository is presented as a formal literature review.

## Key questions the project must answer next

### Methodology questions

1. What exactly counts as an investment research agent?
2. Is report generation enough, or must the system include evidence retrieval and evaluation?
3. Should trading-agent papers be background only or part of the core review?
4. What is the final inclusion boundary for primary evidence?
5. What databases will be searched in the full Search-Round-02?

### Evidence questions

1. Which P001 tables directly support the reproducibility-gap claim?
2. What exactly are the R0-R3 reproducibility definitions?
3. Does P001's 0/19 R3 claim mean no code/data/prompt package, or something more specific?
4. Does P025 actually evaluate report factuality, evidence grounding, and usefulness?
5. Does P016 provide auditable valuation assumptions or only generated research outputs?

### Contribution questions

1. Is Project Aegis a literature review, a framework proposal, or both?
2. What does Project Aegis add beyond P001, P013, P014, P016, and P025?
3. Is the unique contribution the investment-research-agent boundary?
4. Is the unique contribution an auditability framework for research artifacts?
5. Is the unique contribution a reproducible evaluation protocol for AI-generated investment research?

## Recommended next actions

### Highest priority: finish the hard P001 evidence

Create:

`03-Full-Extraction/P001-Protocol-Reproducibility-Extraction-v0.1.md`

This file should extract:

1. protocol reporting tables;
2. reproducibility tier tables;
3. R0-R3 definitions;
4. reporting checklist;
5. study-level protocol gaps.

This is the most important next step because it directly supports the reproducibility-gap claim.

### Second priority: start P025 full-text extraction

Create:

`03-Full-Extraction/P025-FinRpt-Full-Text-Extraction-v0.2.md`

This should extract:

1. dataset construction;
2. report-generation framework;
3. agent roles;
4. evaluation metrics;
5. human evaluation if any;
6. evidence grounding if any;
7. limitations.

This is needed because P025 is central to the investment research agent category.

### Third priority: rewrite the literature review draft

The current repository has many new components, but the living review draft has not yet absorbed them.

A future draft should be structured around:

1. Why trading-agent evaluation is not enough;
2. Why investment research agents need their own definition;
3. What current equity research/report-generation agents show;
4. Why benchmark/evaluation/governance papers matter;
5. What gaps remain: reproducibility, auditability, evidence grounding, risk review, human governance.

### Fourth priority: execute full Search-Round-02

The full Search-Round-02 should produce:

- exact search strings;
- database/source names;
- search dates;
- raw result counts;
- deduplication counts;
- screening decisions;
- exclusion reasons;
- updated PRISMA flow.

Without this, the project should avoid calling itself a systematic review.

## Suggested revised maturity rating

Current rating should remain:

**Level 2.0 candidate / 5**

But the wording can be improved:

> Project Aegis is now a Level 2.0 candidate with strong infrastructure and the beginning of core evidence extraction. It is not yet a confirmed Level 2 review because full Search-Round-02 and full table/figure-level extraction are incomplete.

## Go / no-go recommendation

### Go for continued development

The project is worth continuing. The direction is coherent and the repository now has enough structure to support a credible PhD-preparation research portfolio.

### No-go for public academic claims yet

Do not present it yet as a completed systematic review or a publishable survey.

### Best immediate move

Complete P001 protocol/reproducibility extraction, then start P025 full-text extraction.

## Final reviewer verdict

Project Aegis has moved from a promising idea into a structured research workspace. The mobile bilingual layer is strong, the audit discipline is improving, and P001 has begun real depth extraction. The remaining weakness is not lack of structure; it is lack of completed evidence extraction and reproducible search counts.

The next phase should stop expanding breadth and focus on evidence depth.
