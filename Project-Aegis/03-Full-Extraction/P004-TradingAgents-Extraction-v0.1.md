# P004 Full Extraction v0.1

## Paper

**TradingAgents: Multi-Agents LLM Financial Trading Framework**

## Metadata

- Paper ID: P004
- Year: 2024
- Source: arXiv
- arXiv ID: 2412.20138
- URL: https://arxiv.org/abs/2412.20138
- Authors: Yijia Xiao; Edward Sun; Di Luo; Wei Wang
- Submitted: 2024-12-28
- Verification status: verified from arXiv metadata and abstract-level source

## Research stream

Multi-agent trading / trading-firm simulation / LLM financial decision pipeline

## Why this paper is included

TradingAgents is one of the central baseline papers for the LLM financial trading-agent literature. It directly models a collaborative multi-agent trading firm, making it highly relevant to Project Aegis's question of how financial agents move from single-task prediction toward role-based investment workflows.

## Main research question

Can a multi-agent LLM framework, inspired by the collaborative dynamics of real-world trading firms, improve stock trading decisions by assigning specialized roles to agents such as analysts, researchers, risk managers, and traders?

## Core contribution

The paper proposes a stock trading framework with specialized LLM-powered agents. According to the arXiv abstract, these include:

1. fundamental analysts;
2. sentiment analysts;
3. technical analysts;
4. traders with varied risk profiles;
5. Bull and Bear researcher agents;
6. a risk management team;
7. traders who synthesize debates and historical data into final decisions.

## Key evidence from abstract

- The paper frames prior finance-agent work as often focused on single-agent systems or independent multi-agent data gathering.
- It argues that the collaborative dynamics of trading firms remain underexplored.
- It simulates a dynamic collaborative trading environment.
- It reports improvements over baseline models in cumulative returns, Sharpe ratio, and maximum drawdown.
- It provides a project page: https://TradingAgents-AI.github.io

## Why it matters for Project Aegis

P004 is important because it is a clear example of a multi-agent trading framework that tries to map financial work roles into agent roles. It gives Project Aegis a concrete baseline for comparing **trading-agent workflows** with **investment-research-agent workflows**.

## Methodological value

The paper contributes to Project Aegis's taxonomy in several ways:

- It is not merely a price-prediction model.
- It is not only a QA agent.
- It uses role specialization.
- It includes debate-style Bull/Bear reasoning.
- It includes an explicit risk-management team.
- It converts multi-agent analysis into trading decisions.

This makes it a strong example of the `multi-agent trading system` category.

## Main limitation

Based on abstract-level extraction, the paper still requires verification on:

1. transaction-cost assumptions;
2. slippage treatment;
3. universe and survivorship handling;
4. execution timing;
5. prompt and model-version reproducibility;
6. whether risk management is a formal quantitative module or a role-play layer;
7. whether the system records an auditable evidence trail;
8. whether results survive different market regimes.

## Project Aegis gap revealed

TradingAgents reveals that financial multi-agent systems can imitate trading-firm roles, but Project Aegis still needs to ask:

> Can such multi-agent workflows be made reproducible, auditable, risk-aware, and suitable for institutional investment research rather than only trading action generation?

## Relationship to Project Aegis thesis

P004 supports the thesis that multi-agent architectures are becoming central in financial AI. However, it also motivates Project Aegis's critique: multi-agent trading performance is not enough. The research field needs auditability, reproducibility, transaction-cost discipline, and human-governed investment research workflows.

## Initial quality score

- Relevance: 4/4
- Evidence strength: 3/4
- Reproducibility: 3/4
- Auditability: 1/4
- Risk-awareness: 2/4
- Gap value: 4/4
- Total: 17/24
- Classification: Important literature

## Reviewer questions

1. Does TradingAgents provide enough code, prompts, data, and model-version details for reproduction?
2. How exactly are transaction costs and slippage handled?
3. Does the risk-management team perform quantitative risk control or mainly narrative moderation?
4. Does Bull/Bear debate improve decision quality or only create plausible reasoning?
5. Are improvements robust across market regimes?
6. Does the system evaluate turnover and trading frequency?
7. Are the agents using information that would have been available at the decision time?
8. Does the system have an audit trail from evidence to final trade?
9. How does it compare with simpler non-agent baselines?
10. How can the framework be adapted from trading actions to investment thesis generation?

## How to use this paper in the living review

Use P004 as a baseline example of multi-agent trading systems. It should not be treated as proof that multi-agent financial systems are ready for institutional deployment. It is better used as evidence that financial-agent architecture is becoming more workflow-like, while reproducibility and auditability remain unresolved.

## Extraction status

- Metadata: verified from arXiv page
- Abstract-level extraction: completed
- Full-text section-level extraction: pending
- Architecture diagram extraction: pending
- Experiment and cost-assumption extraction: pending
- Reproducibility artifact check: pending
