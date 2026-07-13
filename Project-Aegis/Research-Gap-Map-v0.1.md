# Research Gap Map v0.1

## Field

LLM-based financial agents and AI investment research systems.

## Central finding

The field is moving from prediction models toward agentic decision workflows. The most important unresolved gaps are not only model accuracy, but **trust, reproducibility, auditability, risk-first evaluation, and human governance**.

## Gap 1: Reproducibility

### Current state

Many studies report impressive trading or portfolio results, but they often use different data universes, time periods, prompts, model versions, split protocols, transaction-cost assumptions, and execution semantics.

### Evidence

The 2026 *Agentic Trading* survey reports severe protocol incomparability and weak reproducibility across the core empirical subset of LLM trading-agent studies.

### Research opportunity

Build a reproducibility checklist and benchmark protocol for LLM financial agents.

### Possible paper title

**A Reproducibility Checklist for LLM-based Financial Agents**

---

## Gap 2: Auditability

### Current state

Many agents output a recommendation without showing a complete chain of evidence: sources used, tool calls made, contrary evidence considered, assumptions made, and reasons for final decision.

### Research opportunity

Design an investment-agent audit trail that records evidence, reasoning steps, risk flags, and human review decisions.

### Possible paper title

**Auditable Investment Research Agents: Evidence Trails for LLM-based Financial Decision Support**

---

## Gap 3: Risk-first evaluation

### Current state

Many papers emphasize return, Sharpe ratio, or classification accuracy. Real investment systems require max drawdown, turnover, transaction cost, slippage, liquidity, stress periods, and regime robustness.

### Research opportunity

Create an evaluation framework where risk metrics are primary, not secondary.

### Possible paper title

**Beyond Sharpe: Risk-first Evaluation of Multi-Agent Financial LLM Systems**

---

## Gap 4: Long-term financial memory

### Current state

Existing memory papers such as FinMem show that memory matters, but memory is still often narrow and trading-decision focused.

### Research opportunity

Develop multi-layer investment memory: macro memory, company memory, thesis memory, mistake memory, regime memory, and portfolio memory.

### Possible paper title

**Thesis Memory for Autonomous Investment Research Agents**

---

## Gap 5: Investment workflow modeling

### Current state

Many agents jump from information directly to buy/sell/hold decisions. Real buy-side research is more structured: idea sourcing, hypothesis generation, evidence collection, valuation, risk review, portfolio implication, compliance review, and monitoring.

### Research opportunity

Model the full institutional investment research workflow as a multi-agent process.

### Possible paper title

**From Trading Signals to Investment Theses: Modeling the Buy-side Research Workflow with LLM Agents**

---

## Gap 6: Human-AI collaboration

### Current state

Much of the literature discusses automation, but institutional investment decisions still require human accountability.

### Research opportunity

Study how portfolio managers should review, challenge, override, and learn from agent-generated research.

### Possible paper title

**Human-in-the-loop Investment Research: How Portfolio Managers Should Supervise AI Agents**

---

## Gap 7: Governance and regulatory alignment

### Current state

Regulators and central banks are increasingly concerned about AI-related financial stability, model concentration, cyber risk, and accountability.

### Research opportunity

Translate governance concerns into system design requirements: approval workflow, kill switch, evidence log, model monitoring, role-based permission, and responsibility assignment.

### Possible paper title

**Governance-by-design for Agentic AI in Asset Management**

---

## Gap 8: Systemic effects of financial agents

### Current state

As more institutions deploy agents, the key question is no longer only whether one agent works, but how many agents interacting together may affect liquidity, herding, volatility, and market stability.

### Research opportunity

Simulate multi-institution agent markets and study emergent systemic behavior.

### Possible paper title

**When AI Agents Become Market Participants: Systemic Risk in Agentic Financial Markets**

---

## Best PhD-level direction

**Reproducible, auditable, risk-aware multi-agent investment research systems.**

This direction has the strongest combination of academic novelty, industry relevance, regulatory importance, and personal fit for a candidate with finance operations and investment-process experience.
