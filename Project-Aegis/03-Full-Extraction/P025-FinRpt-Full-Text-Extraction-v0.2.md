# P025 Full-Text Extraction v0.2 — FinRpt

## Paper

**FinRpt: Dataset, Evaluation System and LLM-based Multi-agent Framework for Equity Research Report Generation**

Authors: Song Jin; Shuqi Li; Shukun Zhang; Rui Yan

Source: arXiv:2511.07322

## Extraction status

This file upgrades P025 from abstract-level extraction to a **section-level extraction scaffold**.

Important caution: this is not yet a complete table-by-table, figure-by-figure, or metric-by-metric extraction. The next pass must verify exact dataset construction, evaluation metrics, architecture details, and evidence-grounding claims from the full text.

## Why P025 is the next full-text target

P001 strengthens the reproducibility-gap side of Project Aegis, but Project Aegis is not meant to be only a trading-agent reproducibility review.

P025 is important because it directly targets **equity research report generation**, which is much closer to the core Project Aegis concept of an investment research agent.

P025 may become one of the strongest anchors for the claim:

> Equity research agents are emerging as a distinct subcategory of financial agents whose primary output is a research artifact rather than a trading action.

This claim remains preliminary until P025 is fully extracted and compared with P016.

---

# 1. Bibliographic and source metadata

## Source content

| Field | Value |
|---|---|
| Paper ID | P025 |
| Title | FinRpt: Dataset, Evaluation System and LLM-based Multi-agent Framework for Equity Research Report Generation |
| Authors | Song Jin; Shuqi Li; Shukun Zhang; Rui Yan |
| Year | 2025 |
| Source | arXiv |
| arXiv ID | 2511.07322 |
| Current verification status | Search-Round-02A arXiv metadata / abstract-level capture |

## Structured extraction

P025 is categorized as:

- equity research report generation;
- investment research agent candidate;
- benchmark/evaluation framework candidate;
- multi-agent financial research system candidate.

## Project Aegis interpretation

P025 is likely more central to Project Aegis than many trading-agent papers because its primary output is a research artifact.

## Claim supported

P025 supports, at candidate level:

> Equity research report generation is a relevant subproblem for investment research agents.

## Claim not supported

At current extraction depth, P025 does not yet prove:

- generated reports are factually reliable;
- generated reports are evidence-grounded;
- generated reports are auditable;
- the framework is institutionally deployable;
- the dataset and code are reproducible.

---

# 2. Research problem

## Source content

P025 appears to address the problem of generating and evaluating equity research reports using LLM-based systems.

## Structured extraction

The research problem can be expressed as:

> How can LLM-based systems generate equity research reports and how should the quality of those reports be evaluated?

This is different from general financial QA and trading-agent evaluation.

| System type | Primary output | Evaluation focus |
|---|---|---|
| Financial QA system | Answer | Correctness / relevance |
| Trading agent | Trade / allocation / position | Return / risk / execution performance |
| Equity research report generator | Research report | Factuality / completeness / reasoning / usefulness |
| Investment research agent | Evidence-grounded investment research artifact | Traceability / auditability / thesis quality / risk review |

## Project Aegis interpretation

P025 helps Project Aegis shift the evaluation target from trading performance to research artifact quality.

## Claim supported

This supports:

> Financial-agent evaluation should include research-artifact evaluation, not only market-return evaluation.

## Claim not supported

This does not prove that research-artifact evaluation is already solved.

---

# 3. Claimed components to verify

## Source content

The abstract-level capture identifies three major components:

1. a dataset for equity research report generation;
2. an evaluation system with multiple metrics;
3. an LLM-based multi-agent framework, referred to in screening notes as FinRpt-Gen.

## Structured extraction

These components should be verified in full text using this checklist:

| Component | Verification questions | Status |
|---|---|---|
| Dataset | What is the source? How many reports? Which companies? Which market? What date range? | pending |
| Evaluation system | What metrics? Automatic or human? Does it evaluate factuality and grounding? | pending |
| Multi-agent framework | What agents? What roles? What workflow? What model backbones? | pending |
| Baselines | What systems are compared? Are strong LLM baselines included? | pending |
| Human evaluation | Are human analysts or annotators involved? | pending |
| Reproducibility | Is code/data/prompt/report output available? | pending |

## Project Aegis interpretation

If verified, these three components would make P025 highly relevant because Project Aegis also needs:

- dataset definition;
- evaluation rubric;
- agent workflow;
- artifact-level output;
- reproducibility package.

## Claim supported

At current stage, P025 supports:

> The literature is beginning to address equity research report generation as a structured task.

## Claim not supported

Until full text is extracted, P025 should not be used to claim:

> The literature has already solved equity research report evaluation.

---

# 4. Dataset extraction plan

## Source content to verify

The dataset is one of the most important parts of P025, but details remain pending.

## Structured extraction template

| Dataset field | Extraction question | Status |
|---|---|---|
| Dataset name | What is the dataset called? | pending |
| Source documents | Are reports from broker research, company filings, public reports, or generated labels? | pending |
| Company universe | Which companies / sectors / markets are covered? | pending |
| Time period | What dates are covered? | pending |
| Dataset size | How many reports / samples / companies? | pending |
| Input-output format | What input is given and what report output is expected? | pending |
| Labels / references | Are there reference reports or expert labels? | pending |
| Public availability | Is the dataset public? | pending |
| Licensing / copyright risk | Are source reports legally usable? | pending |

## Project Aegis interpretation

Dataset construction is crucial because report-generation benchmarks can be misleading if the dataset is too clean or too narrow.

Potential risks:

- reports may be templated and easy to imitate;
- companies may be large-cap only;
- negative or failed cases may be underrepresented;
- reports may not include true buy-side decision context;
- copyrighted analyst reports may limit reproducibility.

## Claim supported

Once verified, dataset details may support:

> Equity research report generation can be formalized as a benchmark task.

## Claim not supported

Without dataset verification, Project Aegis cannot claim that P025 provides a robust or generalizable benchmark.

---

# 5. Evaluation metric extraction plan

## Source content to verify

The earlier extraction notes mention possible multiple metrics, but exact metrics remain pending.

## Structured extraction template

| Metric category | Key question | Status |
|---|---|---|
| Factual accuracy | Does the report state correct financial facts? | pending |
| Evidence grounding | Are claims linked to source evidence? | pending |
| Completeness | Does the report cover required sections? | pending |
| Reasoning quality | Does the report make coherent financial arguments? | pending |
| Valuation quality | Are valuation assumptions and outputs assessed? | pending |
| Risk discussion | Are risks identified and evaluated? | pending |
| Consistency | Is the report internally consistent? | pending |
| Hallucination / unsupported claims | Are unsupported claims measured? | pending |
| Analyst usefulness | Do humans judge usefulness for research? | pending |
| Readability / structure | Is report organization evaluated? | pending |
| Reproducibility / traceability | Can outputs be reconstructed and audited? | pending |

## Project Aegis interpretation

This is central to Project Aegis. A good investment research agent evaluation should not only reward fluent writing.

A Project Aegis evaluation rubric should include:

1. claim-level factuality;
2. evidence-source grounding;
3. thesis coherence;
4. valuation assumption transparency;
5. risk completeness;
6. contrary-evidence handling;
7. human-review usefulness;
8. reproducibility of generated artifact;
9. cost and latency;
10. audit trail completeness.

## Claim supported

If P025 includes metrics beyond style/readability, it can support:

> Research-artifact evaluation is becoming a distinct evaluation problem in financial-agent research.

## Claim not supported

If P025 mainly evaluates text similarity or generic generation quality, it should not be used as strong evidence for trustworthy investment research evaluation.

---

# 6. Multi-agent framework extraction plan

## Source content to verify

P025 reportedly includes an LLM-based multi-agent framework.

## Structured extraction template

| Architecture field | Extraction question | Status |
|---|---|---|
| Agent names | What agents are defined? | pending |
| Agent roles | Do agents map to analyst roles? | pending |
| Input pipeline | What information enters the system? | pending |
| Retrieval | Does the system retrieve external evidence? | pending |
| Reasoning | How does the system reason over financial information? | pending |
| Report generation | Which module writes the report? | pending |
| Review / critique | Is there a critic, evaluator, or reviewer agent? | pending |
| Revision loop | Does the report get revised? | pending |
| Citation / grounding | Does the output cite sources? | pending |
| Human involvement | Are humans in the loop? | pending |

## Project Aegis interpretation

P025 could help Project Aegis design a role-based investment research workflow.

Possible Project Aegis role mapping:

| Project Aegis role | Purpose |
|---|---|
| Evidence retrieval agent | Collect source documents and market data |
| Financial statement agent | Extract and analyze financials |
| Business analysis agent | Analyze company strategy and industry context |
| Valuation agent | Build and check valuation assumptions |
| Risk reviewer agent | Identify risks and contrary evidence |
| Report writer agent | Generate research artifact |
| Audit agent | Trace claims to evidence and logs |
| Human reviewer | Approve or reject final output |

## Claim supported

If full text verifies specialized roles, P025 may support:

> Multi-agent role specialization is emerging in equity research report generation.

## Claim not supported

Without architecture extraction, Project Aegis should not claim that P025 has a fully auditable or institutionally realistic multi-agent workflow.

---

# 7. Evidence grounding and auditability extraction plan

## Source content to verify

The most important question for Project Aegis is whether P025 evaluates or enforces evidence grounding.

## Structured extraction template

| Auditability field | Extraction question | Status |
|---|---|---|
| Source references | Does the generated report cite source documents? | pending |
| Claim-level grounding | Are individual claims linked to evidence? | pending |
| Data snapshot | Are source versions or dates recorded? | pending |
| Prompt availability | Are prompts or system instructions provided? | pending |
| Generated artifacts | Are generated reports shared? | pending |
| Human-review logs | Are reviewer comments or scores available? | pending |
| Error analysis | Are factual errors or hallucinations analyzed? | pending |
| Reproducibility package | Can another researcher reproduce outputs? | pending |

## Project Aegis interpretation

This is the make-or-break area for P025.

If P025 only generates plausible reports without claim-level grounding, it is still useful but not enough for trustworthy investment research.

If P025 evaluates factuality, evidence grounding, and human usefulness, it becomes a much stronger anchor.

## Claim supported

Pending verification.

## Claim not supported

At current stage, do not claim P025 solves auditability.

---

# 8. Comparison with P016 FinRobot Equity Research

## Source content to verify

P016 and P025 appear to be related but distinct.

## Structured comparison

| Dimension | P016 FinRobot Equity Research | P025 FinRpt |
|---|---|---|
| Main focus | Equity research and valuation agent | Equity research report generation |
| Output | Research / valuation output | Research report artifact |
| Architecture | Data-CoT / Concept-CoT / Thesis-CoT | Multi-agent framework to verify |
| Evaluation | Pending deeper extraction | Pending deeper extraction |
| Project Aegis role | First equity research agent anchor | Second report-generation anchor |

## Project Aegis interpretation

P016 and P025 together may support the emergence of equity research agents, but they should not be merged too quickly.

Important distinction:

- P016 may be stronger for analyst workflow and valuation reasoning.
- P025 may be stronger for report-generation benchmark and evaluation.

## Claim supported

Together, P016 and P025 may support:

> Equity research agents and equity research report generators are emerging as a distinct area within financial-agent research.

## Claim not supported

They do not yet prove institutional readiness or full trustworthiness.

---

# 9. Correct and incorrect use in the living review

## Correct use

Use P025 to say:

> Equity research report generation is a relevant and emerging task for LLM-based financial agents.

Use P025 to motivate:

> Project Aegis should evaluate research artifacts, not only trading returns or question-answer accuracy.

## Incorrect use

Do not use P025 to say:

> AI-generated equity research reports are already reliable.

Do not use P025 to say:

> Evidence grounding and auditability have already been solved.

Do not use P025 to say:

> Investment research agents are mature enough for institutional deployment.

---

# 10. Supervisor-style defense answer

If a supervisor asks why P025 matters, answer:

> P025 matters because it moves the literature closer to Project Aegis's core target: investment research artifacts. While many financial-agent papers evaluate trading performance, P025 appears to focus on equity research report generation, a dataset, an evaluation system, and a multi-agent generation framework. This makes it a candidate anchor for the investment research agent category. However, I would not overclaim it yet. The key verification questions are whether the dataset is robust, whether evaluation includes factuality and evidence grounding, whether the multi-agent architecture is clearly specified, and whether outputs are reproducible and auditable.

---

# 11. Remaining extraction tasks

## Required next pass

1. Extract dataset construction details.
2. Extract exact evaluation metrics.
3. Extract multi-agent architecture and roles.
4. Extract baselines and model backbones.
5. Extract human evaluation design.
6. Extract evidence-grounding or citation mechanism.
7. Extract error analysis and hallucination handling.
8. Extract code/data availability.
9. Create P025 table/figure tracker.
10. Update Claim-Evidence Ledger after verification.

## Current status after this file

| Extraction layer | Status |
|---|---|
| Abstract-level extraction | complete |
| Section-level extraction scaffold | complete |
| Dataset extraction | pending |
| Evaluation metric extraction | pending |
| Architecture extraction | pending |
| Evidence-grounding extraction | pending |
| Table/figure extraction | pending |
| Code/data availability | pending |
