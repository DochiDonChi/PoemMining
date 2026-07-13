# P001 Protocol and Reproducibility Extraction v0.1

## Paper

**P001 — Agentic Trading: When LLM Agents Meet Financial Markets**

arXiv:2605.19337

## Purpose

This file addresses the most important weakness identified in `Reviewer-Audit-v0.8.md`:

> P001's hardest evidence is not Figure 1, Figure 2, Table 1, or Table 3. The strongest evidence for Project Aegis comes from protocol reporting tables, reproducibility tier definitions, R0-R3 counts, and reporting checklist items.

This extraction file therefore focuses on the evidence needed to support the reproducibility-gap claim.

## Extraction discipline used in this file

Each item is separated into five layers:

1. **Source content** — what the paper reports or defines.
2. **Structured extraction** — the extracted item in review-friendly form.
3. **Project Aegis interpretation** — how Project Aegis may use it.
4. **Claim supported** — what this item supports.
5. **Claim not supported** — what this item should not be used to claim.

This structure is intentionally stricter than earlier extraction files.

---

# 1. Protocol reporting gap — source-level finding

## 1.1 Source content

P001 reports that in the 19-study primary empirical subset, protocol reporting is weak across several fields.

The already captured high-level counts are:

| Protocol / reproducibility field | Reported count in primary empirical subset |
|---|---:|
| Extractable time-consistent split protocols | 2 / 19 |
| Explicit transaction-cost model | 1 / 19 |
| Universe / survivorship handling | 1 / 19 |
| Execution timing or execution semantics | 11 / 19 |
| R0 reproducibility | 15 / 19 |
| R3 reproducibility | 0 / 19 |

## 1.2 Structured extraction

The main extraction is not simply that reporting is imperfect. The more precise extraction is:

> The primary empirical subset has enough reported trading-agent experiments to create an evidence map, but many studies lack the protocol details required for rigorous comparison and reproduction.

The most important missing or underreported protocol fields are:

1. data split / time-consistency;
2. transaction-cost model;
3. asset universe and survivorship handling;
4. execution timing semantics;
5. reproducibility artifacts.

## 1.3 Project Aegis interpretation

Project Aegis can use this to argue that financial-agent evaluation should not rely only on outcome metrics.

For investment research agents, the equivalent missing protocol fields may include:

| Trading-agent protocol field | Investment-research-agent equivalent |
|---|---|
| Time-consistent split protocol | Evidence timestamp and source-version control |
| Transaction-cost model | Query cost, data cost, latency, and analyst-review cost |
| Universe / survivorship handling | Company/document universe and missing-document handling |
| Execution timing semantics | Research artifact timestamp and evidence availability semantics |
| Reproducibility artifacts | Prompt/code/data/report reconstruction package |

## 1.4 Claim supported

This supports:

> LLM trading-agent studies have a serious protocol-reporting and comparability problem.

It also supports:

> Project Aegis should design investment research agent evaluation around reproducible evidence and source/version control.

## 1.5 Claim not supported

This does **not** prove:

- all LLM trading agents fail;
- all investment research agents are unreliable;
- all financial LLM research lacks reproducibility;
- Project Aegis has already solved the protocol problem.

---

# 2. Time-consistent split protocols

## 2.1 Source content

P001 reports that only **2 / 19** primary empirical studies have extractable time-consistent split protocols.

## 2.2 Structured extraction

A time-consistent split protocol is important because financial data is temporal. Training, validation, and testing must respect chronological order. If this is unclear, performance can be contaminated by look-ahead bias or future-data leakage.

## 2.3 Project Aegis interpretation

For investment research agents, the equivalent is evidence-time consistency.

A research agent should not generate a report using information that was not available at the report date.

Possible Project Aegis requirement:

> Every generated investment research artifact must record the source timestamp, retrieval timestamp, and report timestamp.

## 2.4 Claim supported

This supports:

> Temporal protocol reporting is weak in the current LLM trading-agent primary evidence set.

## 2.5 Claim not supported

This does not prove that every result in the 17 remaining papers is invalid. It only shows that the split protocol is not extractable or sufficiently reported in the evidence map.

---

# 3. Transaction-cost model

## 3.1 Source content

P001 reports that only **1 / 19** primary empirical studies explicitly models transaction costs.

## 3.2 Structured extraction

Transaction-cost modeling matters because trading strategies can look profitable before costs and fail after costs.

Transaction costs may include:

- commission;
- bid-ask spread;
- slippage;
- market impact;
- financing costs;
- turnover-related frictions.

## 3.3 Project Aegis interpretation

Investment research agents do not have transaction costs in the same way, but they have research-production costs.

Possible equivalent costs:

- LLM query cost;
- premium data-source cost;
- retrieval latency;
- human review time;
- report revision cost;
- compliance review cost.

Project Aegis should avoid evaluating AI research systems only by report quality if the cost and latency of producing the report are hidden.

## 3.4 Claim supported

This supports:

> Trading-agent performance claims may be difficult to compare when transaction-cost assumptions are absent or underreported.

## 3.5 Claim not supported

This does not prove that transaction costs would eliminate all reported returns. It only shows that cost assumptions are usually not explicitly modeled in the primary subset.

---

# 4. Universe / survivorship handling

## 4.1 Source content

P001 reports that only **1 / 19** primary empirical studies reports universe / survivorship handling.

## 4.2 Structured extraction

Universe definition matters because the asset pool determines the difficulty and realism of the trading task.

Survivorship handling matters because excluding failed, delisted, or unavailable assets can make performance look artificially strong.

## 4.3 Project Aegis interpretation

For investment research agents, the equivalent is document and company universe control.

Questions Project Aegis should ask:

1. Which companies are included?
2. Which documents are included?
3. Are failed companies included?
4. Are negative reports included?
5. Are missing filings handled explicitly?
6. Are analyst revisions and incorrect theses included?

Without this, AI research benchmarks may overrepresent clean cases and underrepresent difficult cases.

## 4.4 Claim supported

This supports:

> Asset-universe and survivorship assumptions are underreported in LLM trading-agent studies.

## 4.5 Claim not supported

This does not prove that every study suffers from survivorship bias. It shows that survivorship handling is rarely extractable from the reported protocols.

---

# 5. Execution timing / semantics

## 5.1 Source content

P001 reports that **11 / 19** primary empirical studies report execution timing or execution semantics.

## 5.2 Structured extraction

Execution timing matters because a trading decision must be tied to what information is available at the decision time and when execution occurs.

Examples of timing questions:

- Does the agent trade at market open, close, or next day?
- Is news available before or after the decision?
- Are prices known before the trade decision?
- Does the backtest assume immediate execution?

## 5.3 Project Aegis interpretation

For investment research agents, the equivalent is research artifact timing.

A research report should specify:

- evidence cutoff date;
- report generation date;
- model run date;
- source retrieval date;
- human review date;
- final approval date.

This is necessary because financial facts change quickly.

## 5.4 Claim supported

This supports:

> Execution timing is reported more often than costs or survivorship, but still not universally reported.

## 5.5 Claim not supported

This does not show that the 11 reported protocols are all high quality. It only shows that execution timing or semantics are extractable in those cases.

---

# 6. Reproducibility tiers R0–R3

## 6.1 Source content

P001 reports that:

- **15 / 19** primary empirical studies reach R0 reproducibility;
- **0 / 19** primary empirical studies reach R3 reproducibility.

The exact R0-R3 definitions still require final table-level extraction and verification.

## 6.2 Structured extraction

The high-level meaning is clear: many studies provide enough information for basic identification or partial understanding, but none in the primary subset reaches the strongest reproducibility tier.

However, Project Aegis must not overstate this until the exact definitions of R0, R1, R2, and R3 are extracted.

## 6.3 Project Aegis interpretation

This is one of the most important evidence points for the project.

A future Project Aegis reproducibility ladder for investment research agents may include:

| Proposed tier | Investment research reproducibility meaning |
|---|---|
| IR-R0 | Paper describes task and high-level system only |
| IR-R1 | Prompts, model names, source types, and evaluation metrics are reported |
| IR-R2 | Code, prompts, sample data, generated reports, and scoring rules are partially available |
| IR-R3 | Full reproducibility package with source snapshots, prompts, code, generated artifacts, reviewer labels, and audit logs |

## 6.4 Claim supported

This supports, cautiously:

> The strongest reproducibility tier appears absent from the 19-study LLM trading-agent primary empirical subset.

## 6.5 Claim not supported

Until exact definitions are extracted, this should not be used to claim:

- no study shares any code;
- no study shares any prompts;
- no study can be partially reproduced;
- R3 means a specific artifact package unless verified.

---

# 7. Reporting checklist implication

## 7.1 Source content

P001 implies or provides a reporting-checklist direction focused on protocol clarity, costs, universe definition, timing, reproducibility, and audit artifacts.

Exact checklist items still require final extraction.

## 7.2 Structured extraction

The minimum reporting checklist for trading-agent studies should include:

1. data sources;
2. time period;
3. train/validation/test split;
4. asset universe;
5. survivorship handling;
6. transaction-cost assumptions;
7. execution timing;
8. model identity and version;
9. prompt and tool setup;
10. code/data/prompt availability;
11. risk metrics;
12. baseline comparisons.

## 7.3 Project Aegis interpretation

A future Project Aegis reporting checklist for investment research agents should include:

1. source documents and versions;
2. evidence cutoff date;
3. retrieval method;
4. prompt and model version;
5. generated report artifact;
6. claim-level evidence references;
7. valuation assumptions;
8. risk-review notes;
9. human-review process;
10. scoring rubric;
11. cost and latency;
12. reproducibility package.

## 7.4 Claim supported

This supports:

> P001 can be translated into a reporting discipline for Project Aegis, but the translation must be explicitly marked as Project Aegis interpretation.

## 7.5 Claim not supported

The Project Aegis reporting checklist is not directly in P001. It is a derived framework inspired by P001.

---

# 8. Stronger wording for Project Aegis literature review

## Current weak wording to avoid

Avoid:

> P001 proves that financial agents are not reproducible.

Avoid:

> Existing AI investment research agents are unreliable.

Avoid:

> No financial LLM studies are reproducible.

## Stronger defensible wording

Use:

> P001 provides evidence that within a 19-study primary empirical subset of LLM trading-agent research, key protocol fields such as time-consistent splits, transaction-cost assumptions, universe/survivorship handling, and the strongest reproducibility tier are rarely reported or absent. Project Aegis uses this as a methodological warning for investment research agents, where analogous protocol fields include source-version control, evidence timestamps, claim-level grounding, human-review logs, and reproducibility packages.

---

# 9. Integration into Project Aegis claims

## Claim update recommendation

Update the Claim-Evidence Ledger as follows:

| Claim ID | Recommended status after this extraction |
|---|---|
| C001 | strengthened, but still pending exact table verification |
| C004 | strengthened conceptually through auditability interpretation, but direct auditability coding still pending |
| C005 | still cautious; risk-aware evaluation is adjacent but not fully proven by P001 alone |
| C006 | remains strategic hypothesis, not direct evidence |

## Why this matters

This prevents overclaiming. P001 is strong for trading-agent reproducibility and protocol reporting. It is indirect for investment research agent trustworthiness.

---

# 10. Remaining verification tasks

## Must verify in next pass

1. Exact R0-R3 definitions.
2. Exact table number for protocol reporting counts.
3. Exact table number for reproducibility-tier counts.
4. Whether reporting checklist is explicit or derived.
5. Whether code/data/prompt availability is separated by artifact type.
6. Whether execution timing includes semantic detail or only mention-level reporting.

## Current status after this file

| Extraction area | Status |
|---|---|
| Protocol gap high-level counts | extracted |
| Project Aegis translation | extracted with caution |
| R0-R3 exact definitions | pending |
| Protocol table numbers | pending |
| Reproducibility table numbers | pending |
| Reporting checklist exact source | pending |

---

# 11. Final reviewer note

This file strengthens P001's role as the reproducibility-gap anchor, but it deliberately avoids claiming complete extraction.

The project can now say:

> P001 has section-level extraction, partial core table/figure extraction, and a dedicated protocol/reproducibility extraction pass.

The project still cannot say:

> P001 is fully extracted table by table and figure by figure.
