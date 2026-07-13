# P001 Full-Text Extraction v0.2 — Agentic Trading

## Paper

**Agentic Trading: When LLM Agents Meet Financial Markets**

Authors: Yihan Xia, Panpan You, Taotao Wang, Fang Liu, Han Qi, Xiaoxiao Wu, Shengli Zhang

Source: arXiv:2605.19337

## Extraction status

This file upgrades P001 from abstract-level extraction to **section-level extraction scaffold with verified source anchors**.

It is not yet a complete table-by-table or figure-by-figure extraction. The next pass should extract all 27 tables and 15 figures.

## Why P001 is the first full-text target

P001 is currently the strongest evidence anchor for Project Aegis's reproducibility-gap argument.

It directly supports the claim that the LLM trading-agent literature has serious problems with:

- protocol comparability;
- time-consistent split reporting;
- transaction-cost modeling;
- universe / survivorship handling;
- execution timing semantics;
- reproducibility artifacts.

This matters because Project Aegis is trying to move from performance-centered financial agents to trustworthy, auditable, risk-aware investment research systems.

---

# 1. Bibliographic and source metadata

## Extracted metadata

| Field | Value |
|---|---|
| Paper ID | P001 |
| Title | Agentic Trading: When LLM Agents Meet Financial Markets |
| Authors | Yihan Xia, Panpan You, Taotao Wang, Fang Liu, Han Qi, Xiaoxiao Wu, Shengli Zhang |
| arXiv ID | 2605.19337 |
| Submission date | 2026-05-19 |
| Length | 59 pages |
| Figures | 15 |
| Tables | 27 |
| Main method | Audit-oriented evidence map / survey |
| Evidence set | 77 included studies |
| Candidate records | 92 after deduplication |
| Primary empirical subset | 19 studies |
| Background/context tier | 58 studies |

## Verification status

Metadata has been checked against the arXiv record and HTML full-text view. Table and figure content still requires a dedicated pass.

---

# 2. Main research purpose

P001 reframes LLM-based trading agents as expert-system decision pipelines. Instead of only asking whether LLM trading agents produce high returns, it asks whether the field has enough protocol clarity and reproducible evidence for meaningful comparison.

The paper is explicitly audit-oriented. It separates primary empirical evidence from broader design/background context and emphasizes protocol reporting rather than headline trading performance.

## Project Aegis interpretation

This is exactly the methodological direction Project Aegis needs. It supports the argument that financial-agent research should not be evaluated only by output quality or apparent performance. The evaluation must also inspect whether the system's input data, decision loop, execution assumptions, logs, and reproducibility artifacts are available for audit.

---

# 3. Inclusion boundary and evidence scope

## What enters the primary empirical subset

P001 defines a narrow primary empirical subset. A paper must satisfy:

1. **Action Output** — the system emits tradable actions such as orders, position changes, or portfolio allocations.
2. **Closed-Loop Evaluation** — those actions are evaluated through backtesting, simulation, benchmark, or live trading.

Papers that are useful for architecture or context but do not meet both criteria remain in the background tier.

## Extracted counts

| Category | Count |
|---|---:|
| Candidate registry after deduplication | 92 |
| Included evidence-mapping ledger | 77 |
| Excluded at screening / eligibility | 15 |
| Primary empirical subset | 19 |
| Background/context tier | 58 |

## Project Aegis interpretation

The Action Output + Closed-Loop Evaluation boundary is important because it prevents the review from mixing weakly related finance LLM papers with genuine trading-agent evidence.

For Project Aegis, a similar boundary should eventually be created for **investment research agents**. A candidate definition could require:

1. evidence gathering;
2. investment reasoning;
3. research artifact generation;
4. traceable output;
5. evaluation against expert or ground-truth criteria.

---

# 4. Central empirical finding: protocol incomparability

## Core finding

P001's central empirical finding is that the current primary subset of LLM trading-agent studies is not protocol-comparable.

Within the 19-study primary empirical subset, P001 reports:

| Protocol field | Reported count |
|---|---:|
| Extractable time-consistent split protocols | 2 / 19 |
| Explicit transaction-cost model | 1 / 19 |
| Universe / survivorship handling | 1 / 19 |
| Execution timing or semantics | 11 / 19 |
| R0 reproducibility | 15 / 19 |
| R3 reproducibility | 0 / 19 |

## Interpretation

The most important finding is not that LLM trading agents fail. The important finding is that many studies cannot be compared rigorously because the evaluation protocols are underreported or inconsistent.

For Project Aegis, this is a direct warning: if investment research agents are evaluated only by whether generated reports look professional, the field may repeat the same mistake. Project Aegis should design evaluation protocols that require source traceability, artifact logs, input snapshots, benchmark tasks, and reviewer notes.

---

# 5. Architecture-Capability-Adaptation lens

## What P001 proposes

P001 uses **Architecture-Capability-Adaptation (A-C-A)** as a working analytical lens.

Important caution: P001 does **not** present A-C-A as a fully externally validated taxonomy. It is a working lens to organize evidence.

## What A-C-A does

A-C-A separates:

1. **Architecture** — how the system is organized, including perception, memory, reasoning, action/execution, and coordination.
2. **Capability** — what the system can do, such as alpha discovery, portfolio management, or risk management.
3. **Adaptation** — how the system learns, updates, or changes behavior over time.

## Project Aegis interpretation

A-C-A is useful, but Project Aegis should not copy it mechanically. For investment research agents, the equivalent lens might be:

1. **Evidence Architecture** — data sources, filings, market data, search, retrieval, and document snapshots.
2. **Research Capability** — company analysis, valuation, thesis formation, risk analysis, and report generation.
3. **Governance / Auditability** — claim tracing, reviewer workflow, reproducibility package, human sign-off, and risk controls.
4. **Memory / Adaptation** — thesis memory, evidence memory, mistake memory, and regime memory.

---

# 6. Expert-system decision pipeline framing

P001 frames trading agents as financial decision-support pipelines.

The pipeline can be understood as:

```text
Market observations
        ↓
Perception / retrieval
        ↓
Memory / knowledge base
        ↓
Reasoning / inference engine
        ↓
Action / execution interface
        ↓
Feedback / adaptation
        ↓
Logs / human oversight / audit artifacts
```

## Why this matters

This framing shifts attention away from isolated model outputs and toward the full decision loop.

For trading agents, the loop ends in tradable action. For Project Aegis, the comparable loop should end in a research artifact:

```text
Financial evidence
        ↓
Retrieval and source logging
        ↓
Research memory
        ↓
Reasoning and valuation
        ↓
Investment thesis / research report
        ↓
Risk review and human audit
        ↓
Revision and evidence ledger
```

---

# 7. Auditability insight

P001 makes an important distinction: LLM agents can produce human-readable rationales, but readable rationales are not automatically faithful explanations.

Meaningful auditability requires independently verifiable artifacts, such as:

- grounded tool calls;
- timestamps;
- data snapshots;
- execution logs;
- reproducible prompts or code;
- decision records.

## Project Aegis interpretation

This is one of the strongest links between P001 and Project Aegis.

For investment research agents, a generated report is not auditable merely because it sounds logical. It must provide:

- claim-level source references;
- valuation assumption logs;
- source document versions;
- risk reviewer comments;
- human override records;
- final approval trail.

This becomes a core design principle for Project Aegis.

---

# 8. Table and figure extraction plan

P001 reports 15 figures and 27 tables. The next pass must extract them systematically.

## Priority figures to extract

| Priority | Figure | Why it matters |
|---|---|---|
| 1 | Figure 1 — Agency Spectrum of Trading Systems | Defines boundary from prediction models to trading agents |
| 2 | Figure 2 — Reasoning flow diagram | Shows agent reasoning loop and feedback cycle |
| 3 | Any A-C-A architecture figures | Helps translate framework into Project Aegis architecture |
| 4 | Any challenge/future direction figures | Helps identify research gaps |

## Priority tables to extract

| Priority | Table | Why it matters |
|---|---|---|
| 1 | Table 1 — Related surveys / benchmarks comparison | Positions P001 against prior work |
| 2 | Table 3 — Study selection summary | Provides PRISMA-style counts |
| 3 | Protocol-reporting tables | Direct support for reproducibility-gap claim |
| 4 | Reproducibility-tier tables | Direct support for R0–R3 claim |
| 5 | Evidence ledger / primary subset tables | Needed for full audit trail |

---

# 9. Claims supported for Project Aegis

## Strongly supported

### Claim A — Trading-agent literature has a reproducibility and protocol-comparability problem

P001 strongly supports this for LLM trading-agent studies, especially through the reported 19-study primary empirical subset.

### Claim B — Financial agent evaluation should inspect the full decision loop

P001 supports this through its expert-system decision-pipeline framing.

### Claim C — Readable rationales are not enough for auditability

P001 supports this by distinguishing human-readable text from independently verifiable audit artifacts.

## Moderately supported

### Claim D — Similar problems may exist in investment research agents

P001 does not directly prove this, because it studies trading agents. Project Aegis can use P001 as an analogy and methodological warning, but must verify investment research agent papers separately.

## Not supported directly

P001 does not directly prove:

- investment research agents are unreliable;
- equity research report generators are immature;
- all financial LLM systems lack auditability;
- Project Aegis's proposed architecture works.

---

# 10. Research gap extraction

P001 reveals several gaps that Project Aegis can reuse carefully:

| Gap | P001 context | Project Aegis translation |
|---|---|---|
| Protocol incomparability | Trading-agent studies use inconsistent / underreported protocols | Investment research agents need standardized report-evaluation protocols |
| Cost / friction underreporting | Trading studies rarely report cost models | Research agents need cost-of-query, latency, data-source, and revision-cost reporting |
| Execution semantics gap | Trading actions not always clearly timed or defined | Research artifacts need clear evidence timestamp and source-version semantics |
| Reproducibility artifact gap | No R3 reproducibility in primary subset | Research agents need prompt/code/data/report reconstruction packages |
| Auditability gap | Text rationales are not enough | Research reports need claim-level evidence trails and reviewer logs |

---

# 11. How P001 should be cited in Project Aegis

## Correct citation use

Use P001 to say:

> In LLM trading-agent literature, protocol comparability and reproducibility remain major bottlenecks.

Use P001 to motivate:

> Project Aegis applies a similar audit-oriented concern to investment research agents.

## Incorrect citation use

Do not use P001 to say:

> All investment research agents are unreliable.

Do not use P001 to say:

> Equity research agents have already been proven to lack auditability.

Do not use P001 to say:

> P001 validates the Project Aegis framework.

---

# 12. Supervisor-style defense answer

If a supervisor asks why P001 matters, the answer should be:

> P001 matters because it shows that LLM trading-agent research is already facing a reproducibility and protocol-comparability bottleneck. Its primary subset analysis shows that only a small number of studies report time-consistent splits, transaction costs, universe/survivorship handling, or high reproducibility artifacts. For Project Aegis, P001 is not proof about investment research agents directly. Instead, it is a methodological warning: if we want trustworthy AI investment research, we must design evaluation around audit trails, evidence grounding, source timestamps, and reproducible research artifacts rather than relying on polished text or headline performance.

---

# 13. Remaining extraction tasks

## Required next pass

1. Extract all 15 figures.
2. Extract all 27 tables.
3. Create a table-level evidence ledger for P001.
4. Verify the reproducibility-tier definition R0–R3.
5. Extract reporting checklist items.
6. Extract challenge / future direction section.
7. Update `Claim-Evidence-Ledger-v0.1.csv` with P001 full-text extraction status.
8. Update `Extraction-Depth-Status-v0.1.csv` from abstract-level to section-level for P001.

## Current status after this file

- Abstract-level extraction: complete.
- Section-level extraction scaffold: complete.
- Table-level extraction: pending.
- Figure-level extraction: pending.
- Claim translation to Project Aegis: complete but still requires cautious use.
