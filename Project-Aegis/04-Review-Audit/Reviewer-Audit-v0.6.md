# Reviewer Audit v0.6

## Date

2026-07-09

## Purpose

This audit reviews the Project Aegis workspace after the v0.5 improvements. The focus is to check whether the latest changes solved the concerns raised in Reviewer Audit v0.5 and to identify the next bottlenecks.

## Overall judgement

Project Aegis is now a **Level 2.0 candidate**, but not yet a confirmed Level 2 research foundation.

The project now has a much stronger scaffold, especially because it added:

- a working definition of investment research agent;
- a Search-Round-02 protocol;
- an extraction depth tracker;
- softened claim language;
- uncertainty-aware quality scores.

However, the project still cannot be called a defensible systematic review because the most important evidence-generating steps have not yet been executed.

## What improved since v0.5

### 1. The concept boundary is much clearer

`Definition-Investment-Research-Agent-v0.1.md` now defines investment research agents by output type and workflow properties. This directly addresses the previous concern that the term could be too vague.

The current definition is useful because it separates:

- financial QA agents;
- trading agents;
- portfolio optimization models;
- financial LLM infrastructure;
- equity / investment research agents.

This is a meaningful conceptual improvement.

### 2. The methodology is better prepared

`Search-Round-02-Protocol-v0.1.md` is a strong addition. It defines sources, queries, logging fields, inclusion criteria, exclusion criteria, exclusion codes, and PRISMA update requirements.

This is better than searching first and writing the method afterward.

### 3. Extraction depth is now transparent

`Extraction-Depth-Status-v0.1.csv` clearly states that current extractions are abstract-level plus interpretation. This prevents a common research mistake: overstating the depth of analysis.

### 4. The research language is more careful

The claim ledger now uses more cautious language. This improves academic credibility.

Examples:

- `dominant design pattern` was softened to `emerging design pattern in the currently reviewed sample`.
- `strongest PhD direction` was softened to `promising PhD direction`.
- auditability and risk-aware evaluation are treated as candidates needing further coding.

### 5. Quality scores are now easier to challenge and revise

Adding evidence level, uncertainty, and next-score action to the quality score table is a good improvement. It shows that scores are for research triage, not final evidence.

## Remaining concerns

### Concern 1: Search-Round-02 is still only a protocol

The protocol is good, but no new reproducible search has been executed. Until Search-Round-02 is run, the project remains a structured foundation rather than a reproducible review.

Reviewer question:

> Can another researcher reproduce your paper selection process today?

Current answer:

> Not yet. The protocol exists, but the reproducible search has not been executed.

### Concern 2: PRISMA remains unpopulated

The PRISMA flow draft still does not contain actual counts. This is the most obvious blocker for a systematic-review claim.

Required next fields:

- records identified;
- duplicates removed;
- records screened;
- records excluded;
- full texts assessed;
- full texts excluded;
- final included papers.

### Concern 3: The definition is useful but untested

The investment research agent definition is plausible, but it has not yet been tested against enough papers. At least 20 papers should be coded using the definition before treating it as stable.

Potential edge cases:

1. A system that answers detailed filing questions but does not generate a report.
2. A trading system with analyst agents and debate but final output is a trade.
3. A valuation model that produces a target price but no evidence trail.
4. A portfolio tool that explains allocation decisions but does not produce research artifacts.
5. A general financial LLM used inside a workflow but not itself agentic.

### Concern 4: Extraction depth remains limited

The extraction tracker is honest, but the underlying problem remains: the six core extraction files are not yet section/table/figure-level.

The next extraction upgrade should include:

- method details;
- architecture diagrams;
- dataset / market universe;
- evaluation period;
- cost / friction assumptions;
- model versions;
- limitations;
- future work;
- reproducibility artifacts.

### Concern 5: P007-P011 metadata debt remains

The project correctly marks these records as unverified, but they remain a debt. They should either be cleaned or moved into a separate candidate file.

Reviewer concern:

> Why are unverified records still in the main paper database?

Recommended answer:

> They are candidates, not evidence. But this distinction should be made more visible.

### Concern 6: Quality scores are still not score-by-score evidence backed

The new columns help, but each numerical score still lacks detailed explanation. For example, why P004 gets reproducibility 3 rather than 2 or 4 still needs exact evidence.

Recommendation:

Create a score justification file for the six core papers.

### Concern 7: The living review draft is now behind the audit layer

The audit layer has become more sophisticated than the living review draft. The draft should eventually be rewritten to reflect the more cautious claim language and new definitions.

## Critical questions to answer before next upgrade

### Methodology

1. Will Search-Round-02 be executed exactly as written?
2. Which source should be searched first: arXiv, SSRN, ACL, or Google Scholar?
3. What will count as a duplicate?
4. Will preprints and published versions be merged or treated separately?
5. How will citation chasing be logged?

### Definition and taxonomy

1. Does a benchmark qualify as an agent paper or only an evaluation paper?
2. Can one paper have both `trading_agent` and `investment_research_agent` labels?
3. What minimum evidence is required to label a paper as an investment research agent?
4. How should role-playing agents be treated if they do not use real tools or evidence retrieval?
5. Should `equity_research_agent` be a subtype of `investment_research_agent`?

### Evidence and scoring

1. Which of the six core papers has the strongest actual evidence?
2. Which claims rely only on abstracts?
3. Which claims require full-text extraction before use in the living review?
4. Are the current quality scores too generous?
5. Should unverified papers receive scores at all?

### Strategy

1. Is the next goal to impress a supervisor or to prepare a publishable review?
2. If supervisor-facing, what 3 files should be shown first?
3. If publication-facing, what methodology gaps must be closed first?
4. Should the repo be moved out of `PoemMining` before wider sharing?
5. Should a README warning be added: `Research scaffold, not final review`?

## Recommended next actions

### Highest priority

1. Execute Search-Round-02 using the protocol.
2. Populate PRISMA provisional counts.
3. Clean or separate P007-P011 metadata.

### Second priority

4. Create `Core-Paper-Score-Justifications-v0.1.md`.
5. Create `Taxonomy-Coding-Test-v0.1.csv` and apply the investment-research-agent definition to at least 20 papers.
6. Upgrade P001 from abstract-level extraction to section/table/figure-level extraction.

### Third priority

7. Rewrite the living review introduction using only supported claims.
8. Add a supervisor-facing summary document.
9. Prepare a migration plan for a dedicated repo.

## Suggested next milestone

**Milestone 2.0: Reproducible Review Foundation**

Completion criteria:

1. Search-Round-02 executed and logged.
2. PRISMA counts populated.
3. P007-P011 cleaned or moved to candidate-only status.
4. Six core papers have score justifications.
5. Investment research agent definition tested on at least 20 papers.

## Reviewer decision

**Decision: Keep as draft. Continue improving.**

This is a strong research scaffold and now close to Level 2, but the next improvement must produce new reproducible evidence rather than more structure alone.
