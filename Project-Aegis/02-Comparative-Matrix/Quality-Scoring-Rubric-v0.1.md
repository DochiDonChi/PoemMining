# Quality Scoring Rubric v0.1

## Purpose

This rubric is used to evaluate papers in the Project Aegis literature database. The goal is to avoid treating all papers equally. A paper with impressive claims but weak reproducibility should not carry the same weight as a paper with transparent methodology and usable artifacts.

## Scoring dimensions

Each paper is scored from 0 to 4 on six dimensions.

## 1. Relevance to Project Aegis

- 0 = unrelated to financial agents or investment research
- 1 = general finance AI or general agent paper with weak relevance
- 2 = relevant to finance LLMs but not agentic workflow
- 3 = directly relevant to financial agents or investment research automation
- 4 = central to trustworthy, reproducible, auditable AI investment research systems

## 2. Evidence strength

- 0 = purely speculative or commercial claim
- 1 = conceptual with limited evidence
- 2 = experiment exists but narrow or weakly documented
- 3 = solid empirical or systematic evidence
- 4 = strong empirical evidence, systematic review, or expert-validated benchmark

## 3. Reproducibility

- 0 = no reproducibility details
- 1 = partial methodological details only
- 2 = some code/data/prompt/model details disclosed
- 3 = sufficient detail for attempted reproduction
- 4 = open code, data or data pipeline, prompts, model versions, seeds, cost assumptions, and execution rules

## 4. Auditability

- 0 = no explanation or evidence trail
- 1 = natural-language explanations only
- 2 = cites or retrieves evidence but weak traceability
- 3 = records evidence, reasoning, tool calls, and decision logic
- 4 = full audit trail including contrary evidence, risk flags, tool logs, and human review mechanism

## 5. Risk-awareness

- 0 = only return/accuracy metrics
- 1 = includes basic risk metrics such as volatility or drawdown
- 2 = includes transaction costs, turnover, or stress periods
- 3 = includes regime robustness, slippage, liquidity, or failure-mode analysis
- 4 = risk-first framework with explicit unsafe trajectories, governance controls, and human oversight

## 6. Gap value

- 0 = does not reveal a useful gap
- 1 = reveals a minor technical gap
- 2 = reveals a useful but narrow research gap
- 3 = reveals a major research gap relevant to future work
- 4 = strongly supports a PhD-level research direction

## Total score

Maximum score: 24

Suggested classification:

- 20-24 = Core literature
- 15-19 = Important literature
- 10-14 = Supporting literature
- 5-9 = Background literature
- 0-4 = Exclude or mention only briefly

## Current scoring priority

The first papers to be fully scored should be:

1. P001 Agentic Trading
2. P013 Finance Agent Benchmark
3. P016 FinRobot Equity Research
4. P014 Evaluation and Benchmarking Suite
5. P004 TradingAgents
6. P006 FinMem

These papers are central to the review's first argument: the field is moving from trading agents toward investment research agents, but evaluation, reproducibility, and auditability remain unresolved.
