# Core Paper Score Justifications v0.1

## Purpose

This file explains the provisional quality scores assigned to the six first-core papers. The current scores are **research-triage scores**, not final publication-ready scores. They are intended to guide which papers should receive deeper extraction first.

## Scoring dimensions

Each paper is scored from 0 to 4 on:

1. Relevance to Project Aegis
2. Evidence strength
3. Reproducibility
4. Auditability
5. Risk-awareness
6. Gap value

## Important warning

Most current justifications are based on arXiv metadata, abstract-level extraction, and early interpretation. Final scores must be re-evaluated after section-level, table-level, and figure-level extraction.

---

## P001 — Agentic Trading

### Current score

- Relevance: 4
- Evidence strength: 4
- Reproducibility: 3
- Auditability: 3
- Risk-awareness: 4
- Gap value: 4
- Total: 22 / 24
- Classification: Core literature

### Justification

P001 is currently the strongest anchor paper because it is a survey and evidence map rather than a single system demo. It directly supports the reproducibility and evaluation-gap argument. The abstract-level evidence reports 77 included studies, 19 primary empirical studies, weak time-consistent split reporting, weak transaction-cost reporting, weak universe / survivorship reporting, and no R3 reproducibility.

### Uncertainty

Medium. The score is high because the paper directly targets evaluation and reproducibility, but final scoring requires extracting its tables, coding scheme, reproducibility levels, and inclusion criteria.

### Next action

Extract all tables and figures related to reproducibility, evaluation protocol, transaction costs, execution semantics, and evidence ledger.

---

## P004 — TradingAgents

### Current score

- Relevance: 4
- Evidence strength: 3
- Reproducibility: 3
- Auditability: 1
- Risk-awareness: 2
- Gap value: 4
- Total: 17 / 24
- Classification: Important literature

### Justification

P004 is highly relevant because it is a concrete multi-agent trading framework with role-specialized agents. It supports the idea that financial agents are moving toward workflow-like architectures. However, current scoring is cautious because transaction costs, slippage, execution timing, model versions, prompt details, and audit trails still need full-text verification.

### Uncertainty

High. The paper may deserve a lower or higher reproducibility score depending on code availability, experiment detail, and prompt / model disclosure.

### Next action

Extract architecture details, experiment setup, market universe, baseline comparison, cost assumptions, prompts, model versions, and repository reproducibility.

---

## P006 — FinMem

### Current score

- Relevance: 3
- Evidence strength: 3
- Reproducibility: 2
- Auditability: 1
- Risk-awareness: 1
- Gap value: 4
- Total: 14 / 24
- Classification: Supporting literature

### Justification

P006 is important for the memory pillar. It supports the idea that financial agents need more than one-shot prompts. However, it is primarily a trading-agent paper, not an investment research agent paper. Its strongest value for Project Aegis is gap generation: how should memory become auditable, editable, evidence-linked, and resistant to stale beliefs?

### Uncertainty

High. The current score depends heavily on abstract-level understanding. Full-text extraction may change reproducibility, risk-awareness, and auditability scores.

### Next action

Extract memory architecture, update rules, input data sources, evaluation setup, trading-cost treatment, and any discussion of stale or biased memory.

---

## P013 — Finance Agent Benchmark

### Current score

- Relevance: 4
- Evidence strength: 4
- Reproducibility: 3
- Auditability: 2
- Risk-awareness: 2
- Gap value: 4
- Total: 19 / 24
- Classification: Important literature

### Justification

P013 is highly relevant because it focuses on real-world financial research tasks rather than only market actions. The abstract reports 537 expert-authored questions, SEC filing use, an agentic tool harness, and low best-model accuracy relative to expert-level task demands. This strongly supports the claim that finance research tasks remain difficult for current agents.

### Uncertainty

Medium. The evidence strength is high at abstract level, but auditability and reproducibility scores need benchmark-design extraction.

### Next action

Extract task taxonomy, question construction process, scoring protocol, tool harness, model list, cost calculation, and error analysis.

---

## P014 — Evaluation and Benchmarking Suite

### Current score

- Relevance: 4
- Evidence strength: 3
- Reproducibility: 3
- Auditability: 2
- Risk-awareness: 3
- Gap value: 4
- Total: 19 / 24
- Classification: Important literature

### Justification

P014 is important because it frames financial LLM/agent evaluation as a lifecycle issue involving evaluation pipelines, governance, leaderboards, AgentOps, and documentation. This supports the Project Aegis argument that trustworthy financial AI requires infrastructure, not only model performance.

### Uncertainty

Medium-high. The paper appears highly relevant, but the exact relevance to investment research agents depends on the full benchmark tasks and governance framework.

### Next action

Extract evaluation components, benchmark categories, governance framework, leaderboard design, AgentOps details, and whether investment research tasks are explicitly covered.

---

## P016 — FinRobot Equity Research

### Current score

- Relevance: 4
- Evidence strength: 3
- Reproducibility: 3
- Auditability: 2
- Risk-awareness: 2
- Gap value: 4
- Total: 18 / 24
- Classification: Important literature

### Justification

P016 is the clearest current example of an equity research agent in the database. Its Data-CoT, Concept-CoT, and Thesis-CoT structure supports the concept of an agent that produces research artifacts rather than only trading actions. It is therefore central to defining the boundary between trading agents and investment research agents.

### Uncertainty

Medium-high. Current extraction is abstract-level. The final score depends on how the paper evaluates generated reports, handles evidence traceability, records valuation assumptions, and supports auditability.

### Next action

Extract architecture, agent roles, data pipeline, valuation process, report generation process, evaluation design, open-source reproducibility, and evidence-traceability mechanisms.

---

## Cross-paper reviewer concerns

1. P004 and P006 should not be overused as evidence for auditability or risk-first evaluation until their full text is coded.
2. P013 is strong evidence for finance research task difficulty, but not proof that full investment research systems are unsolved.
3. P016 is strong evidence for equity research agents, but not proof that investment research agents are institutionally ready.
4. P014 supports lifecycle evaluation, but does not automatically solve the narrower Project Aegis problem.
5. P001 supports reproducibility concerns for trading-agent studies; extension to broader investment research agents needs additional evidence.

## Status

Version: v0.1

Status: provisional score justification. Requires full-text extraction before final use in review paper.
