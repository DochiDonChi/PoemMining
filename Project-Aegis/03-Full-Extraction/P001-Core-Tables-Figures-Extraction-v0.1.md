# P001 Core Tables and Figures Extraction v0.1

## Paper

**P001 — Agentic Trading: When LLM Agents Meet Financial Markets**

arXiv:2605.19337

## Extraction purpose

This file extracts the first high-priority figures and tables from P001:

1. Figure 1 — Agency Spectrum of Trading Systems
2. Figure 2 — Reasoning Flow Diagram
3. Table 1 — Selected related surveys / benchmarks and auditability-oriented review emphasis
4. Table 3 — Study selection summary

This is still a **partial table/figure extraction**, not the complete 27-table / 15-figure extraction.

---

# 1. Figure 1 — Agency Spectrum of Trading Systems

## Source description

Figure 1 defines an agency spectrum from less agentic systems to more agentic systems.

The spectrum moves from:

```text
Prediction Models
        ↓
Signal Generators
        ↓
Partial Agents
        ↓
Trading Agents
        ↓
Full Ecosystems
```

## Extracted structure

| Spectrum position | Description | Example types | Agentic status |
|---|---|---|---|
| Prediction Models | Perceive market information but do not make decisions | FinBERT, StockBERT-style models | Not primary trading agents |
| Signal Generators | Add decision layers but do not execute trades | Alpha-generation / factor-mining systems | Below primary inclusion boundary |
| Partial Agents | May include memory or reasoning but lack action modules | Systems such as FinVis-GPT without execution | Background/design context |
| Trading Agents | Close perception–memory–reasoning–action loop | FinAgent, TradingAgents-style systems | Candidate primary empirical subset if closed-loop evaluated |
| Full Ecosystems | Add adaptation and coordination across agents or markets | Multi-agent market/ecosystem systems | Broader agentic ecosystem |

## Inclusion boundary

P001's primary empirical subset requires:

1. **Action Output** — the system emits tradable actions such as orders, position changes, or portfolio allocations.
2. **Closed-Loop Evaluation** — those actions are evaluated in backtesting, simulation, live trading, or benchmark settings.

Works to the left of this boundary may inform background discussion, but they do not enter primary empirical, protocol-reporting, or reproducibility statistics.

## Project Aegis interpretation

Figure 1 is extremely important because it shows that not every financial LLM system should be treated as a trading agent.

For Project Aegis, the equivalent boundary problem is:

```text
Financial QA systems
        ↓
Financial report generators
        ↓
Partial research agents
        ↓
Investment research agents
        ↓
Research-governance ecosystems
```

A future Project Aegis figure should define a similar spectrum for **investment research agency**, where the primary inclusion boundary should require research artifact generation plus evidence-grounded evaluation.

## Claim supported

Figure 1 supports the claim that P001 uses a clear inclusion boundary instead of mixing all finance LLM systems together.

## Claim not supported

Figure 1 does not prove that trading agents are effective or trustworthy. It only defines the boundary for review inclusion.

---

# 2. Figure 2 — Reasoning Flow Diagram

## Source description

Figure 2 is a schematic reasoning-flow diagram.

It describes how an agent receives information from perception and memory, reasons over that information, generates candidate actions, evaluates candidate actions, selects an action, executes it, and then receives feedback for learning or adaptation.

## Extracted flow

```text
Perception input
        ↓
Memory input
        ↓
Reasoning mechanism
        ↓
Candidate action generation
        ↓
Forward planning / reflection / evaluation
        ↓
Best action selection
        ↓
Action module / execution
        ↓
Feedback loop
        ↓
Learning and adaptation
```

## Important note from P001

The figure is schematic. It is not used as evidence-mapping statistics or protocol comparison evidence.

## Project Aegis translation

For Project Aegis, this reasoning flow can be translated from trading action to research artifact generation:

```text
Source documents / filings / market data
        ↓
Research memory and prior thesis context
        ↓
Reasoning and valuation mechanism
        ↓
Candidate thesis / claim generation
        ↓
Evidence check / risk review / contradiction search
        ↓
Best-supported thesis selection
        ↓
Research report / investment memo generation
        ↓
Human reviewer feedback
        ↓
Research memory update
```

## Claim supported

Figure 2 supports the idea that financial agents should be evaluated as decision loops, not isolated text outputs.

## Claim not supported

Figure 2 does not prove that the reasoning loop is faithful, optimal, or auditable. It is a conceptual diagram.

---

# 3. Table 1 — Selected related surveys / benchmarks and auditability-oriented review emphasis

## Source description

Table 1 positions P001 against related surveys and benchmarks.

It compares whether prior works make the following criteria central:

- architecture-centric organization;
- execution semantics and transaction-cost modeling;
- structured evidence mapping table;
- reproducibility tier assessment.

## Extracted columns

| Column | Meaning |
|---|---|
| Work | Survey or benchmark being compared |
| Type | Survey, benchmark, model/tool, etc. |
| Scope | Field or task area |
| Arch | Whether architecture is a central organizing concern |
| Exec/Cost | Whether execution semantics and cost modeling are central |
| Map | Whether structured evidence mapping is central |
| R | Whether reproducibility tier assessment is central |

## Extracted comparison

| Work | Type | Scope | Arch | Exec/Cost | Map | R |
|---|---|---|---|---|---|---|
| This survey | Survey | Trading Agents | Primary | Primary | Primary | Primary |
| LLM-Agent Survey | Survey | General AI Agents | Primary | Partial | Not primary | Not primary |
| Giglio-Kelly-Xiu | Survey | Asset Pricing ML | Background | Partial | Not primary | Not primary |
| FinBen | Benchmark | Financial Tasks | Not primary | Not primary | Not primary | Not primary |
| FinGPT | Model/Tool | Financial NLP | Not primary | Not primary | Not primary | Not primary |
| InvestorBench | Benchmark | Trading Tasks | Not primary | Partial | Not primary | Not primary |
| LLM-Trading Survey | Survey | Trading Agents | Partial | Partial | Not primary | Not primary |
| LLM-Finance Survey | Survey | Finance Agents | Partial | Partial | Not primary | Not primary |

## Key interpretation

Table 1 shows that P001 claims a distinctive review position: it is not simply another finance LLM survey. Its emphasis is auditability-oriented and protocol-aware.

## Important caution

P001 itself notes that the comparison reflects its auditability-focused perspective and that other surveys may prioritize different goals. This means Table 1 should not be used to dismiss other surveys as low quality.

## Project Aegis use

Project Aegis can use Table 1 as a model for its own positioning table.

A future Project Aegis positioning table should compare:

- trading-agent surveys;
- finance LLM benchmarks;
- equity research agent papers;
- financial report generation papers;
- governance/evaluation frameworks;
- Project Aegis's own contribution.

## Claim supported

Table 1 supports the claim that P001's novelty is its auditability-oriented, protocol-aware review emphasis.

## Claim not supported

Table 1 does not prove that P001 is more comprehensive than every prior survey. It compares selected works through P001's chosen auditability lens.

---

# 4. Table 3 — Study selection summary

## Source description

Table 3 gives the canonical study-selection summary for P001.

The denominator is the 92-record deduplicated registry.

## Extracted counts

| Stage | Count |
|---|---:|
| Registry candidate records | 92 |
| Included in evidence mapping set | 77 |
| Excluded at screening / eligibility | 15 |
| Final exclusion reason: outside finance/trading/portfolio/risk-management scope | 15 |
| Included evidence-map partition: primary empirical subset | 19 |
| Included evidence-map partition: background/context tier | 58 |

## Inclusion logic

P001 uses a narrow inclusion boundary.

To enter the primary empirical subset, a study must satisfy:

1. **Action Output** — the system emits tradable actions such as orders, position changes, or portfolio allocations.
2. **Closed-Loop Evaluation** — those actions are evaluated in backtesting, simulation, live trading, or benchmark settings.

Finance-relevant papers that lack Action Output or Closed-Loop Evaluation remain in the background tier instead of being discarded entirely.

## Why this matters

Table 3 provides the denominator logic for all later protocol and reproducibility statistics.

When P001 says only 2/19 studies report extractable split protocols or 0/19 reach R3 reproducibility, the denominator is the 19-study primary empirical subset, not all 77 included papers.

## Project Aegis use

Project Aegis should copy this denominator discipline.

For investment research agents, future denominators may need to separate:

| Evidence role | Possible definition |
|---|---|
| Primary investment research agent subset | Systems that generate investment research artifacts and evaluate them against expert/ground-truth/reviewer criteria |
| Background finance LLM context | Finance LLM, QA, benchmark, or trading papers that inform design but do not generate research artifacts |
| Governance/evaluation context | Papers about evaluation lifecycle, auditability, or risk controls |
| Candidate-only records | Papers with unverified metadata or insufficient extraction |

## Claim supported

Table 3 strongly supports P001's evidence scope and denominator discipline.

## Claim not supported

Table 3 does not itself prove protocol incomparability. It only defines the evidence set and denominators used by later protocol/reproducibility analyses.

---

# 5. Combined Project Aegis insight from these four items

These four extracted items create a coherent foundation:

| Extracted item | What it contributes | Project Aegis translation |
|---|---|---|
| Figure 1 | Defines agent inclusion boundary | Define investment research agent boundary |
| Figure 2 | Shows decision-loop framing | Design research artifact generation loop |
| Table 1 | Positions auditability-oriented review novelty | Position Project Aegis against finance LLM / agent literature |
| Table 3 | Defines evidence denominators | Create rigorous primary/background/candidate denominator logic |

## Practical conclusion

P001 is valuable not mainly because it lists many trading-agent papers. It is valuable because it models **evidence discipline**:

1. define the agent boundary;
2. separate primary evidence from background context;
3. keep denominators fixed;
4. avoid mixing performance claims with incomplete protocols;
5. translate reporting gaps into future methodology requirements.

This is exactly the discipline Project Aegis needs for investment research agents.

---

# 6. Remaining P001 extraction tasks after this file

## Still pending

1. Protocol reporting tables.
2. Reproducibility tier tables.
3. R0–R3 reproducibility definitions.
4. Reporting checklist tables.
5. Challenge/future direction figures or tables.
6. All remaining tables and figures not yet extracted.

## Status after this file

| Extraction layer | Status |
|---|---|
| Abstract-level extraction | complete |
| Section-level scaffold | complete |
| Core figure extraction | partial: Figure 1 and Figure 2 extracted |
| Core table extraction | partial: Table 1 and Table 3 extracted |
| Full 27-table extraction | pending |
| Full 15-figure extraction | pending |
