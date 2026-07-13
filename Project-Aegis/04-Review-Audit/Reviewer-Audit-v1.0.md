# Reviewer Audit v1.0

## Date

2026-07-09

## Audit scope

This audit reviews the current Project Aegis workspace after `Current-Progress-Summary-v2.1.md`.

The purpose is not to repeat the progress summary. The purpose is to challenge the current work as a supervisor, reviewer, or PhD committee member would.

## Overall verdict

Project Aegis has become a serious research workspace. It now has enough structure, files, and early evidence extraction to be useful for PhD preparation, research planning, and supervisor discussion.

However, the project is still not ready to be presented as a completed systematic review or publishable survey.

The strongest current assessment is:

> Project Aegis is a Level 2.0 candidate research workspace with strong scaffolding, a useful bilingual learning layer, and two emerging evidence anchors: P001 for reproducibility gaps and P025 for equity research report generation. It still lacks complete systematic search evidence, complete source-level extraction, and a rewritten narrative that converts the workspace into an argument.

---

# 1. What is genuinely strong

## 1.1 The project has moved beyond reading notes

The repository now contains:

- methodology;
- paper database;
- extraction files;
- claim-evidence ledger;
- reviewer audits;
- source archive;
- bilingual reading packages;
- extraction trackers;
- current progress summary.

This is no longer just a collection of papers.

## 1.2 The two-anchor logic is intellectually strong

The current thesis has become clearer:

| Anchor | What it contributes |
|---|---|
| P001 Agentic Trading | Shows protocol-reporting and reproducibility problems in LLM trading-agent literature |
| P025 FinRpt | Shows equity research report generation as a structured research-artifact task |

The bridge idea is strong:

> Take reproducibility discipline from trading-agent evaluation and apply it to investment research agents, where the output is a research artifact rather than a trade.

This is a credible research direction.

## 1.3 P025 source verification is a major improvement

Earlier P025 was mostly a candidate/scaffold. Now it has actual source-level extraction and external-resource verification.

The repository has verified:

- public GitHub repo;
- public Hugging Face dataset page;
- detailed requirements file;
- dataset checking script;
- benchmark execution script;
- intermediate prompt/response fields;
- multiple framework variants.

This makes P025 much stronger as a dataset / benchmark / report-generation anchor.

## 1.4 The project is honest about limitations

The progress summary explicitly states that Project Aegis is still not a publishable systematic review because Search-Round-02 is incomplete, PRISMA counts are provisional, P001 exact R0-R3 definitions are pending, and P025 evidence grounding remains partially verified.

This honesty is academically important.

---

# 2. Major doubts and reviewer questions

## Doubt 1 — Is Project Aegis a literature review, a framework, or a prototype?

The repository currently contains elements of all three:

1. literature review;
2. research gap map;
3. evaluation framework idea;
4. potential system design direction;
5. learning library.

A reviewer may ask:

> What exactly is the final deliverable?

Possible answers:

- a systematic review;
- a living review;
- a research proposal;
- an evaluation framework;
- a prototype design;
- a PhD research portfolio.

The project needs to decide the primary deliverable.

## Doubt 2 — The current evidence base is still seed-driven

Even though the project has many files, the paper set still comes from seed papers and Search-Round-02A pilot discovery.

A reviewer may ask:

> How do you know this is not cherry-picked?

Current answer:

> We do not know yet. This is a structured seed corpus, not a completed systematic corpus.

This is acceptable for a workspace but not for a formal review.

## Doubt 3 — P001 is indirect evidence for Project Aegis

P001 studies trading agents, not investment research agents.

P001 can support methodology warnings about reproducibility, but it cannot directly prove investment research agents are immature or unauditable.

The project must keep saying:

> P001 is a methodological warning, not direct evidence about investment research agents.

## Doubt 4 — P025 is stronger now, but auditability is still not proven

P025 now supports:

- ERR task formulation;
- dataset construction;
- multi-agent architecture;
- finance-specific metrics;
- human analyst evaluation;
- public resource availability.

But it does not yet establish:

- claim-level citation grounding;
- source-level traceability of each report claim;
- reproducible report reconstruction;
- upstream data rights clarity;
- institutional auditability.

A reviewer may ask:

> Can the generated report be audited claim by claim?

Current answer:

> Not established yet.

## Doubt 5 — P016 is underdeveloped relative to its importance

P016 is supposed to be one of the central equity research agent papers, but it is still not source-level extracted.

This creates an imbalance:

- P001 is relatively deep;
- P025 is becoming deep;
- P016 is still shallow.

If the final thesis is about investment research agents, P016 cannot remain shallow.

## Doubt 6 — The living review draft is now outdated

The repository has changed dramatically since the original living review draft.

A reviewer may ask:

> Where is the actual argument?

The current project has many files, but the narrative synthesis has not caught up.

The next stage must rewrite the living review draft or create a research brief.

---

# 3. Specific questions to ask next

## 3.1 Project identity questions

1. Is Project Aegis primarily a systematic review or a research proposal?
2. Is the final output a paper, a PhD proposal, a GitHub research portfolio, or a prototype design?
3. What is the minimum standard for calling something an investment research agent?
4. Are trading-agent papers core evidence or background methodology?
5. Is the unique contribution the definition, the evaluation framework, or the source-verification process?

## 3.2 P001 questions

1. What exactly are R0, R1, R2, and R3?
2. Which table reports the 2/19, 1/19, 11/19, and 0/19 numbers?
3. Which studies are the 19 primary empirical studies?
4. Are the protocol gaps uniformly severe, or concentrated in certain types of papers?
5. Can P001's reporting checklist be translated into an investment research agent checklist without overclaiming?

## 3.3 P025 questions

1. Why does the paper report 6,825 ERR samples while Hugging Face shows about 13.6k rows?
2. Are Chinese and English samples both counted on Hugging Face?
3. Does each row represent a full ERR or an intermediate prompt/response stage?
4. Are source documents retained or only processed summaries?
5. Do final reports contain citations or source links?
6. Is there claim-level evidence grounding?
7. Is the human evaluation blind?
8. Are analysts evaluating factual correctness or only perceived quality?
9. Does the MIT README statement apply to all code?
10. Does CC-BY-4.0 on Hugging Face apply to all dataset content and upstream source materials?

## 3.4 P016 questions

1. What exactly is FinRobot's equity research workflow?
2. Does P016 generate valuation assumptions or just narrative reports?
3. Does P016 use evidence retrieval?
4. Does it cite sources?
5. Does it provide human evaluation?
6. Does it provide code, prompts, and generated artifacts?
7. How is P016 different from P025?

---

# 4. Key risks

## Risk 1 — Overbuilding infrastructure before synthesis

The repository is becoming large. This is useful, but there is a risk of building too many support files without producing a coherent narrative.

Recommendation:

After one more P025/P016 verification step, rewrite the living review draft.

## Risk 2 — Treating public code as reproducibility

P025 has public code and dataset resources, but public availability is not the same as reproducibility.

The repository correctly notes this, but all future writing must preserve the distinction.

Use:

> public code/dataset partially verified

Do not use:

> fully reproducible

## Risk 3 — Dataset rights ambiguity

Even if Hugging Face shows CC-BY-4.0, upstream sources may include news, company announcements, or expert reports with separate rights.

Do not copy the full dataset into this repository until rights are clear.

## Risk 4 — P001/P025 bridge may become too ambitious

The bridge thesis is promising, but it is still partly conceptual.

P001 proves trading-agent protocol gaps. P025 shows ERR generation task structure. The claim that Project Aegis can combine these into a trustworthy investment research framework is a research proposal, not a proven fact.

## Risk 5 — PR body is now stale

The PR body does not fully reflect v1.9, v2.0, v2.1, and the current progress summary, likely because long PR body updates were blocked earlier.

This is not fatal because the files are committed, but it affects GitHub readability.

Recommendation:

Replace the PR body later with a shorter summary instead of a long file list.

---

# 5. Recommended next actions

## Priority 1 — Verify P025 modules and assets

Create:

`00-Source-Archive/P025-FinRpt/module-and-asset-verification-v0.1.md`

Inspect:

- `finrpt/module/FinRpt.py`;
- `FinRptSingle`;
- ablation modules;
- `assets/pipeline.png`;
- `assets/agent.png`;
- `assets/report.png`;
- whether reports contain citations or source evidence links.

Reason:

This directly tests whether P025 is only a report-generation benchmark or whether it has evidence-grounding potential.

## Priority 2 — Start P016 source-level extraction

Create:

`03-Full-Extraction/P016-FinRobot-Source-Level-Extraction-v0.1.md`

Reason:

P016 must be strengthened if the final thesis is about investment research agents.

## Priority 3 — Create P016/P025 comparison

Create:

`03-Full-Extraction/P016-P025-Equity-Research-Agent-Comparison-v0.1.md`

Reason:

This comparison may become the most important file for defining the investment research agent category.

## Priority 4 — Rewrite the living review

Create:

`Living-Review-Draft-v0.2.md`

Structure:

1. Trading-agent reproducibility gap;
2. Equity research agent/report-generation emergence;
3. Benchmark and governance layer;
4. Missing bridge: auditable investment research agents;
5. Project Aegis proposed research agenda.

## Priority 5 — Execute full Search-Round-02

Reason:

This is required to move from Level 2.0 candidate toward confirmed Level 2.

---

# 6. Recommended revised PR strategy

The current PR body is too long and stale.

Instead of repeatedly appending every file, replace the PR body with a short structure:

1. project purpose;
2. current maturity;
3. major modules;
4. current evidence anchors;
5. limitations;
6. next steps.

Do not list every file in the PR body anymore. Use the repo files as the detailed record.

Suggested PR-body status statement:

> Project Aegis is currently a Level 2.0 candidate research workspace. It contains a bilingual literature learning layer, PRISMA-style methodology scaffolding, a working investment research agent definition, extraction trackers, P001 reproducibility-gap extraction, P025 source-level extraction and external-resource verification, and a reviewer-audit chain. It is not yet a publishable systematic review because full Search-Round-02, final PRISMA counts, complete full-text extraction, and claim-level evidence-grounding verification remain incomplete.

---

# 7. Final reviewer verdict

The work is useful and directionally strong.

The best parts are:

- clear two-anchor logic;
- strong learning layer;
- honest limitation tracking;
- P001 reproducibility extraction;
- P025 source-level extraction and external verification.

The weakest parts are:

- no full Search-Round-02;
- P016 still shallow;
- P025 evidence grounding not established;
- P001 exact R0-R3 definitions pending;
- living review narrative outdated.

The project should now shift from building more scaffolds to producing synthesis and verification outputs.

Best immediate next action:

> Verify P025 modules/assets, then start P016 source-level extraction, then write the P016/P025 comparison.
