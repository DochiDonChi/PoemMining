# Reviewer Audit v0.9

## Date

2026-07-09

## Audit scope

This audit reviews Project Aegis after the addition of:

1. `P025-FinRpt-Full-Text-Extraction-v0.2.md`;
2. `P025-Extraction-Tracker-v0.1.csv`;
3. updated `Extraction-Depth-Status-v0.1.csv` marking P025 as a section-level scaffold;
4. `Improvement-Summary-v1.8.md`.

The purpose is to check whether the project has improved after balancing the P001 reproducibility anchor with the P025 investment-research-agent anchor.

## Overall assessment

The project has improved in the right direction.

Before this step, Project Aegis was becoming strong on the trading-agent reproducibility side because P001 had already been upgraded to section-level plus partial table/figure/protocol extraction. However, the investment research agent side was weaker. P025 was still abstract-level despite being central to equity research report generation.

The new P025 scaffold does not yet solve that weakness, but it correctly identifies the exact evidence that must be extracted next:

- dataset construction;
- evaluation metrics;
- multi-agent architecture;
- evidence grounding;
- human evaluation;
- reproducibility and code/data availability.

This is a good structural improvement, but not yet a hard evidence improvement.

## What is strong now

### 1. Thesis balance is better

The project now has a clearer two-anchor structure:

| Anchor | Role in Project Aegis | Current strength |
|---|---|---|
| P001 Agentic Trading | Reproducibility and protocol-reporting gap in trading-agent literature | Medium-strong |
| P025 FinRpt | Equity research report generation / investment research artifact direction | Medium but still scaffold-level |

This is important because the project should not become only a trading-agent reproducibility review. The P025 scaffold helps move the project back toward its intended center: trustworthy AI investment research.

### 2. P025 scaffold asks the right questions

The P025 scaffold correctly identifies the most important unknowns:

- What is the dataset?
- What are the exact evaluation metrics?
- Does evaluation include factuality or evidence grounding?
- What are the agent roles?
- Is there a retrieval/citation/grounding mechanism?
- Are generated reports shared?
- Are code, prompts, and data available?

These are the right questions for a serious investment research agent review.

### 3. Anti-overclaiming discipline remains strong

The P025 scaffold repeatedly states what P025 can and cannot yet support.

This is important because the project must not claim that P025 proves auditability, factual reliability, or institutional readiness before those details are extracted.

### 4. P016/P025 distinction is useful

The scaffold correctly distinguishes P016 and P025:

- P016 may be stronger for equity research workflow and valuation reasoning;
- P025 may be stronger for report-generation dataset and evaluation.

This distinction should become central to the literature review.

## Major concerns

### Concern 1 — P025 is still mostly a plan, not an extraction

The P025 v0.2 file is called a full-text extraction scaffold, but most of the important fields are still marked pending.

A strict reviewer may say:

> This is not yet full-text extraction. It is a well-designed extraction plan.

This is acceptable as long as the repository continues to label it correctly, but the project should not treat P025 as evidence-strengthened until actual dataset, metric, and architecture details are extracted.

### Concern 2 — P025 needs source-level verification urgently

P025 is central to the investment research agent claim, but its current status is still `verified_arxiv_abstract` rather than a deeply verified full-text record.

The next pass must verify:

1. exact dataset name;
2. exact sample count;
3. source document types;
4. evaluation metric names;
5. whether evidence grounding is measured;
6. architecture diagram or agent list;
7. code/data availability.

Without this, P025 remains a promising candidate rather than a strong anchor.

### Concern 3 — P001 is still stronger than P025

Even after the P025 scaffold, P001 remains much stronger as an evidence anchor.

Current imbalance:

- P001 has section-level scaffold plus partial core table/figure/protocol extraction.
- P025 has section-level scaffold only.

This means the project still risks being pulled toward trading-agent methodology instead of investment research agent evidence.

### Concern 4 — The living review draft is now outdated

The repository has changed significantly, but the living review draft has not yet been rewritten to reflect:

- the bilingual reading layer;
- P001 protocol/reproducibility extraction;
- P025 scaffold;
- P016/P025 distinction;
- the stronger trading-agent vs investment-research-agent boundary.

The project is accumulating evidence and scaffolds faster than it updates the narrative.

### Concern 5 — Search-Round-02 remains the biggest systematic-review weakness

Even with better extraction files, the project still cannot claim systematic review maturity because full Search-Round-02 has not been executed.

A reviewer will still ask:

> How were these papers selected, and how do you know the set is complete enough?

The current answer remains:

> This is a structured seed / pilot corpus, not a complete systematic review corpus.

That answer is honest, but it limits the maturity level.

## Key questions to ask next

### P025-specific questions

1. What exact dataset does P025 introduce?
2. Is the dataset built from public filings, broker reports, company disclosures, or generated content?
3. Are there licensing or copyright risks if analyst reports are used?
4. What is the input-output structure of the task?
5. Does the benchmark require full reports or section-level report generation?
6. What exact metrics are used?
7. Are metrics finance-specific or generic NLP metrics?
8. Does evaluation include factual accuracy?
9. Does evaluation include evidence grounding?
10. Does evaluation include hallucination or unsupported claim detection?
11. Does the multi-agent framework include specialized research roles?
12. Is there a reviewer or critic agent?
13. Are human analysts involved in evaluation?
14. Are code, data, prompts, or generated reports available?
15. Is P025 closer to a dataset paper, a benchmark paper, or an agent-system paper?

### Project-level questions

1. Is Project Aegis mainly a literature review, an evaluation framework, or a prototype design?
2. What is the final unit of evaluation: report, thesis, claim, evidence trail, or workflow?
3. Should trading-agent papers be treated as core evidence or background methodology?
4. Should P016 and P025 become the central core evidence for investment research agents?
5. What minimum evidence is needed before claiming that investment research agents are an emerging subcategory?

## Recommended next actions

### Highest priority: perform actual P025 evidence extraction

Create:

`03-Full-Extraction/P025-Dataset-Metrics-Architecture-Extraction-v0.1.md`

This file should extract:

1. dataset construction;
2. exact dataset size and source documents;
3. input-output task format;
4. exact metric names and definitions;
5. automatic versus human evaluation;
6. architecture diagram or agent workflow;
7. source-grounding or citation mechanism;
8. code/data/prompt/report availability.

This is more urgent than expanding more reading materials.

### Second priority: update Claim-Evidence Ledger

After P025 details are extracted, update the claim ledger:

- strengthen or weaken C003 depending on whether P025 truly qualifies as an investment research agent;
- update C008 about equity research agents bridging financial QA and investment research systems;
- keep C004 auditability cautious unless evidence grounding is explicitly evaluated.

### Third priority: create a P016/P025 comparison file

Create:

`03-Full-Extraction/P016-P025-Equity-Research-Agent-Comparison-v0.1.md`

This should compare:

- task definition;
- output artifact;
- architecture;
- evidence source;
- valuation reasoning;
- report generation;
- evaluation method;
- auditability;
- reproducibility.

This comparison could become one of the most important files in the repository.

### Fourth priority: rewrite the living review draft

The narrative should be updated to reflect the current structure:

1. Trading-agent literature reveals reproducibility/protocol gaps.
2. Equity research/report-generation papers reveal an emerging research-artifact generation category.
3. Benchmarks and governance papers show evaluation is moving beyond accuracy/returns.
4. Project Aegis proposes the missing bridge: reproducible, auditable, evidence-grounded investment research agents.

## Suggested maturity rating

The maturity rating remains:

**Level 2.0 candidate / 5**

But the reason is now more nuanced:

> Project Aegis has strong infrastructure, a complete bilingual learning layer, a strengthened P001 reproducibility anchor, and a P025 extraction scaffold that begins to balance the investment research agent side. It remains a candidate rather than confirmed Level 2 because P025 is not yet evidence-extracted, P001 still lacks exact R0-R3/table-level verification, and full Search-Round-02 is incomplete.

## Final reviewer verdict

The latest work improves the project in the right direction. P025 was the correct next target because it balances the thesis and brings the project back toward investment research artifacts. However, the current P025 file is still a scaffold. The next step must extract actual source-level details from P025.

The project should now stop adding scaffolds and move to source-level verification.

Best immediate next file:

`P025-Dataset-Metrics-Architecture-Extraction-v0.1.md`
