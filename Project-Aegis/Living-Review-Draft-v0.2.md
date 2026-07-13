# Towards Trustworthy AI Investment Research: From Trading Agents to Auditable Research-Artifact Agents

## Living Review Draft v0.2

## Status

This is a revised living review draft based on the current Project Aegis evidence base.

It is **not yet a publishable systematic review** because full Search-Round-02, final PRISMA counts, and complete table/figure-level extraction remain incomplete.

Current maturity:

**Level 2.0 candidate / 5**

---

# Abstract

Large Language Models are moving financial AI from static prediction toward agentic systems that retrieve information, reason over heterogeneous data, coordinate specialized roles, generate financial research artifacts, and support investment decisions. Early work has focused heavily on trading agents that output market actions such as buy, sell, hold, or portfolio allocation decisions. However, the strongest emerging research opportunity is not simply building more autonomous trading agents. It is building trustworthy AI investment research agents whose primary outputs are auditable research artifacts: equity reports, valuation memos, investment theses, evidence notes, and risk reviews.

This living review argues that the field is splitting into at least two streams: **trading-action agents** and **research-artifact agents**. P001 Agentic Trading shows that LLM trading-agent research already faces reproducibility and protocol-reporting bottlenecks. P016 FinRobot shows how equity research agents may combine live data, valuation workflow, deterministic computation, LLM-assisted narrative generation, and report artifacts. P025 FinRpt shows how equity research report generation can be formalized as a dataset, benchmark, multi-agent framework, and evaluation problem. Together, these anchors motivate Project Aegis: a research agenda for reproducible, evidence-grounded, risk-aware, human-reviewable investment research agents.

The central gap is auditability. Current systems can generate professional-looking financial reports, but neither trading-agent nor research-agent literature has fully solved claim-level evidence grounding, source-version control, valuation-assumption transparency, reproducible artifact reconstruction, or human-reviewable audit trails. Project Aegis therefore proposes that future AI investment research should be evaluated not only by returns, accuracy, or report fluency, but by whether the research artifact can be traced, challenged, reproduced, and reviewed.

---

# 1. Introduction

The first wave of AI in finance was dominated by prediction: forecasting returns, classifying sentiment, identifying factors, or optimizing portfolios. The arrival of large language models changes the research problem. LLMs are not only predictive models. They can read filings and news, retrieve information, use tools, coordinate roles, generate explanations, summarize evidence, and produce research-like outputs.

This creates a new question:

> What kind of financial agents are being built, and what would make them trustworthy enough for investment research?

The answer is not the same for all systems. A trading agent that outputs a buy/sell decision should be evaluated differently from a research agent that generates an equity report or valuation memo. Trading agents require careful evaluation of execution timing, transaction costs, survivorship bias, benchmark realism, risk, and reproducibility. Research agents require all of those concerns plus another layer: factuality, evidence grounding, valuation-assumption transparency, report quality, human review, and auditability.

Project Aegis focuses on the second problem. It does not reject trading-agent research. Instead, it uses trading-agent literature as a methodological warning. If even trading-agent papers struggle with reproducibility and comparable protocols, then investment research agents should not repeat the same mistake at the level of generated reports.

---

# 2. Research question

This living review asks:

> How is the literature on LLM-based financial agents evolving from trading-action systems toward investment research artifact systems, and what evidence, evaluation, and auditability gaps must be solved before these systems can become trustworthy AI investment research agents?

The working thesis is:

> Existing financial-agent research is splitting into trading-action agents and research-artifact agents. P001 shows that trading-agent research already suffers from reproducibility and protocol-reporting gaps. P016 and P025 show that equity research agents and report-generation systems are emerging, but they do not yet fully solve auditability, evidence grounding, or reproducibility. Project Aegis therefore proposes a trustworthy investment research agent framework that combines deterministic financial computation, source-grounded research artifacts, multi-agent analyst roles, reproducible workflows, and human-reviewable audit trails.

---

# 3. Definitions: from trading agents to investment research agents

## 3.1 Trading-action agents

Trading-action agents primarily output market actions. Their outputs include:

- buy / sell / hold decisions;
- portfolio weights;
- allocation changes;
- position adjustments;
- trading signals;
- execution decisions.

These systems may contain research-like components, but their final evaluation usually centers on market performance: return, Sharpe ratio, drawdown, win rate, turnover, or risk-adjusted return.

## 3.2 Research-artifact agents

Research-artifact agents primarily output investment research materials. Their outputs include:

- equity research reports;
- valuation memos;
- investment theses;
- evidence summaries;
- risk reviews;
- investment committee notes;
- decision-support reports.

These systems should be evaluated differently. A good research artifact is not just a profitable signal. It should be factually correct, evidence-grounded, complete, well-reasoned, risk-aware, reproducible, and reviewable.

## 3.3 Updated Project Aegis definition

Project Aegis currently defines an investment research agent as:

> An AI agent system that produces or supports investment research artifacts by coordinating financial data collection, deterministic financial computation, qualitative analysis, valuation reasoning, risk assessment, thesis synthesis, and report generation, while preserving enough evidence, assumptions, intermediate outputs, and reviewer context to make the research artifact auditable.

This definition is still provisional. It must be tested against a larger coded corpus after full Search-Round-02.

---

# 4. Anchor 1 — P001 Agentic Trading: reproducibility discipline from trading-agent research

P001 is currently the strongest Project Aegis evidence anchor for reproducibility and protocol-reporting gaps.

P001 reviews LLM trading-agent literature and separates a primary empirical subset from broader background papers. Its extraction is valuable because it uses denominator discipline. It does not simply mix every finance LLM paper into one pool. It distinguishes systems that produce tradable actions and evaluate those actions in closed-loop settings.

Current extracted P001 evidence includes:

| Evidence item | Extracted point |
|---|---|
| Candidate registry | 92 records after deduplication |
| Evidence map | 77 included records |
| Primary empirical subset | 19 studies |
| Time-consistent split reporting | 2 / 19 |
| Transaction-cost model | 1 / 19 |
| Universe / survivorship handling | 1 / 19 |
| Execution timing / semantics | 11 / 19 |
| R0 reproducibility | 15 / 19 |
| R3 reproducibility | 0 / 19 |

The central lesson is not that all trading agents fail. The central lesson is that performance claims are hard to compare when studies do not consistently report the protocols behind the results. Missing split protocols, transaction-cost assumptions, survivorship handling, execution semantics, and reproducibility artifacts make the literature harder to audit.

## Project Aegis implication

P001 is indirect evidence for investment research agents. It does not prove that equity research agents are unreliable. Instead, it provides a methodological warning:

> If trading-agent studies already suffer from protocol-reporting and reproducibility gaps, investment research agent studies should be designed from the beginning with source timestamps, evidence trails, model/prompt versions, reproducibility packages, and human-review logs.

For Project Aegis, P001 becomes the reproducibility discipline anchor.

---

# 5. Anchor 2 — P016 FinRobot: equity research workflow and deterministic computation

P016 is important because it targets equity research and valuation rather than direct trading action.

The current source-level extraction of the public FinRobot repository shows that FinRobot contains a dedicated equity research module. The repository describes an equity research workflow involving orchestration, data collection, analysis, modeling, synthesis, report generation, and debate agents. It also emphasizes a key design principle:

> Numbers are code-calculated. Narratives are LLM-assisted.

This principle is highly relevant. In trustworthy investment research, valuation numbers should not be hallucinated by an LLM. Financial ratios, DCF outputs, WACC, comparable-company metrics, and sensitivity analysis should be generated through deterministic code or explicit models. The LLM can explain, synthesize, and write, but the numeric chain should remain inspectable.

## Current P016 contribution

P016 currently contributes:

- equity research workflow architecture;
- valuation-system orientation;
- deterministic computation / LLM narration separation;
- multi-agent role structure;
- report generation capability;
- public repository evidence;
- practical live API workflow.

## Current P016 limitations

P016 does not yet prove:

- claim-level evidence grounding;
- full report auditability;
- execution reproducibility;
- stable paper/repository version matching;
- complete valuation assumption traceability.

P016 therefore acts as the **workflow and valuation anchor**, not yet a full auditability anchor.

---

# 6. Anchor 3 — P025 FinRpt: dataset, benchmark, and equity research report generation

P025 is currently the strongest Project Aegis anchor for equity research report generation as a structured task.

Source-level extraction shows that P025 defines an Equity Research Report generation task using stock ticker and analysis date as key inputs. It constructs the FinRpt dataset from CSI800 Chinese market stocks, covering 2024-09-03 to 2024-11-05. The paper-level extraction reports 6,825 ERR samples, with training, validation, and test splits of 5,556, 617, and 652 samples respectively.

P025 uses multiple input information sources:

- company information;
- financial indicators;
- company announcements;
- company-related news;
- historical stock prices;
- historical market indices.

Its output report structure includes:

- financial analysis;
- news analysis;
- management and development analysis;
- risks analysis;
- investment potential assessment;
- recommendation rating.

## FinRpt-Gen architecture

P025 introduces FinRpt-Gen, a nine-agent framework across extraction, analysis, and prediction modules. Extracted agents include:

- News Extraction Agent;
- Income Extraction Agent;
- Balance Extraction Agent;
- Cash Extraction Agent;
- Finance Analysis Agent;
- News Analysis Agent;
- Status Analysis Agent;
- Risk Analysis Agent;
- Prediction Agent.

## Evaluation contribution

P025 is currently stronger than P016 on evaluation design. Extracted metrics include:

- CompletionRate;
- Accuracy;
- BERTScore;
- ROUGE-L;
- NumberRate;
- Financial Numeric;
- News;
- Company & Market & Industry;
- Invest;
- Risk;
- Writing.

P025 also includes human evaluation: 30 FinRpt ERRs and 30 expert-written ERRs rated by three senior financial analysts.

## Source verification contribution

Project Aegis has verified that P025 reports public code and dataset resources. The GitHub repository is public; the Hugging Face dataset page is reachable; the repository contains requirements, dataset-checking code, benchmark execution code, module code, data retrieval code, and report-building code.

This makes P025 a stronger source-verified anchor than before.

## Current P025 limitations

P025 still does not prove:

- claim-level evidence grounding;
- final report citation links;
- full reproducible execution;
- upstream source-rights clarity;
- row-count reconciliation between paper sample count and Hugging Face viewer rows;
- audit-ready report generation.

P025 therefore acts as the **dataset, benchmark, and report-generation anchor**, not yet a full auditability anchor.

---

# 7. P016 and P025 together: the emerging equity research agent category

P016 and P025 are complementary.

| Dimension | P016 FinRobot | P025 FinRpt |
|---|---|---|
| Main role | workflow / valuation platform | dataset / benchmark / report-generation framework |
| Output | equity research reports and valuation outputs | six-section ERRs |
| Strength | deterministic computation, valuation workflow, report generation | dataset, evaluation metrics, human evaluation, multi-agent ERR generation |
| Data mode | live APIs and workflow system | constructed benchmark dataset |
| Evaluation | still pending deeper extraction | stronger extracted metric system |
| Reproducibility | public repo, API-dependent, not tested | public repo/dataset partially verified, not tested |
| Auditability | provenance claimed, not verified | source provenance partial, claim-level grounding not established |

Together, they support the claim that equity research agents are emerging as a distinct subcategory of financial agents. They are not merely trading bots. Their output is a research artifact.

However, they do not prove that trustworthy investment research has been solved. The gap is precisely what Project Aegis should address.

---

# 8. Benchmark and governance layer: P013 and P014

P013 and P014 support the evaluation/governance layer of Project Aegis.

P013 Finance Agent Benchmark highlights the need to test LLM agents on realistic financial research tasks, not just generic QA or text generation. Its relevance is that financial research ability must be evaluated through domain-specific tasks and scoring protocols.

P014 Evaluation and Benchmarking Suite emphasizes broader evaluation lifecycle, governance, benchmarking, leaderboard design, documentation, and AgentOps. Its relevance is that trustworthy financial agents require not only task metrics but also governance infrastructure.

Together, P013 and P014 reinforce the idea that Project Aegis should not evaluate investment research agents only by report fluency. It should evaluate:

- factual accuracy;
- completeness;
- evidence grounding;
- reasoning quality;
- risk coverage;
- reproducibility;
- human review;
- operational governance.

---

# 9. Main research gaps

## Gap 1 — Reproducibility

P001 shows that trading-agent literature already has reproducibility and protocol-reporting gaps. P016 and P025 show that public code and data may exist, but full reproduction remains difficult because of API dependencies, local paths, live data sources, version drift, dataset rights, and untested execution.

## Gap 2 — Claim-level evidence grounding

P025 preserves source-level data and intermediate objects, and P016 claims provenance tracking. But neither has yet been verified to produce final reports where each material claim links back to a specific source, financial row, document, or calculation.

## Gap 3 — Valuation assumption transparency

P016 emphasizes deterministic valuation engines, but the exact traceability of valuation assumptions remains pending. A trustworthy investment research agent should expose assumptions, formulas, sensitivity analysis, and data sources.

## Gap 4 — Human-reviewable audit trails

Human evaluation in P025 is useful, but it is not the same as a human-reviewable audit trail. Future systems need reviewer comments, approval logs, override records, and traceable revision history.

## Gap 5 — Dataset and source-rights governance

P025 provides a public dataset page, but upstream source-rights questions remain. Research systems that use news, analyst reports, company disclosures, or third-party financial data must manage licensing and redistribution constraints.

## Gap 6 — Systematic-review completeness

Project Aegis itself remains incomplete as a systematic review because full Search-Round-02 has not been executed. The current corpus is structured and increasingly source-verified, but still seed/pilot-based.

---

# 10. Project Aegis proposed research agenda

Project Aegis proposes that future AI investment research agents should combine:

1. **Financial evidence collection** — filings, financial statements, news, market data, macro data, and alternative data.
2. **Deterministic financial computation** — ratios, valuation models, WACC, DCF, DDM, comparable-company analysis, scenario analysis.
3. **Multi-agent analyst roles** — data, financials, valuation, news, risk, bull, bear, judge, report, and audit agents.
4. **Research artifact generation** — equity reports, investment theses, risk reviews, valuation memos.
5. **Claim-level evidence grounding** — every material claim linked to source evidence or computation.
6. **Risk and contrary-evidence review** — downside cases, uncertainty, opposing evidence, sensitivity analysis.
7. **Human-reviewable audit trail** — reviewer notes, source versions, prompts, model versions, intermediate outputs, approval logs.
8. **Reproducibility package** — code, prompts, model versions, data snapshots, generated artifacts, evaluation rubrics.

This shifts the field from impressive financial-agent demos toward research systems that can be audited.

---

# 11. Current evidence status

## Strongly supported

- Trading-agent literature has protocol-reporting and reproducibility issues, based on current P001 extraction.
- Equity research report generation is emerging as a structured task, based on P025 extraction.
- Equity research workflow and valuation-oriented agents are emerging, based on P016 extraction.
- Multi-agent role specialization is relevant to financial research artifact generation.

## Moderately supported

- Investment research agents are a useful emerging category.
- Deterministic computation plus LLM narrative is an important design pattern.
- Finance-specific report evaluation is beginning to develop.

## Not yet supported

- Claim-level auditability is solved.
- Investment research agents are institutionally ready.
- P016 or P025 can be fully reproduced by an independent researcher.
- The literature corpus is systematic and complete.

---

# 12. Conclusion

The financial-agent literature is moving beyond stock prediction and trading signals. The field now contains trading-action agents, multi-agent trading frameworks, memory-based agents, financial research benchmarks, governance-oriented evaluation frameworks, and emerging equity research/report-generation systems.

Project Aegis argues that the next important research frontier is not simply autonomous trading. It is trustworthy AI investment research: systems that generate research artifacts that can be traced, challenged, reproduced, and reviewed.

P001 provides the reproducibility warning. P016 provides the equity research workflow and valuation-system anchor. P025 provides the dataset, benchmark, and report-generation anchor. Together, they show both the promise and the missing bridge.

The missing bridge is auditability.

A trustworthy investment research agent should not only sound like an analyst. It should preserve the evidence, assumptions, calculations, intermediate outputs, reviewer context, and source versions required to make its research artifact credible.

---

# 13. Next steps

To move Project Aegis from Level 2.0 candidate toward confirmed Level 2, the next steps are:

1. Execute full Search-Round-02.
2. Verify P001 exact R0-R3 definitions and table numbers.
3. Continue P016 module-level verification.
4. Continue P025 evidence-grounding and report-output inspection.
5. Update Claim-Evidence Ledger using P001/P016/P025.
6. Convert this living review draft into a formal review structure with citations, PRISMA counts, and final evidence tables.
