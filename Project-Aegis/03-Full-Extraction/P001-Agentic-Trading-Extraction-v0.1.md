# P001 Full Extraction v0.1

## Paper

**Agentic Trading: When LLM Agents Meet Financial Markets**

## Metadata

- Paper ID: P001
- Year: 2026
- Source: arXiv
- arXiv ID: 2605.19337
- URL: https://arxiv.org/abs/2605.19337
- Authors: Yihan Xia; Panpan You; Taotao Wang; Fang Liu; Han Qi; Xiaoxiao Wu; Shengli Zhang
- Submitted: 2026-05-19
- Length: 59 pages, 15 figures, 27 tables
- Subject: Computer Science > Artificial Intelligence

## Research stream

Survey / evaluation / reproducibility / agentic trading

## Why this paper is included

This paper is currently one of the strongest anchor papers for Project Aegis because it does not simply propose another trading agent. It reviews the field and identifies major methodological weaknesses: protocol incomparability, weak transaction-cost reporting, limited survivorship/universe handling, unclear execution semantics, and poor reproducibility.

## Main research question

How should LLM-based trading agents be understood, evaluated, and audited as they move from isolated model experiments toward decision pipelines that perceive market information, retrieve context, reason, emit actions, and adapt under market feedback?

## Core contribution

The paper reframes LLM-based trading agents as expert-system decision pipelines rather than simple prediction models. It provides an audit-oriented evidence map of 77 included studies screened through 2026-03-09.

## Key empirical evidence from abstract

- Included studies: 77
- Primary empirical subset: 19 studies satisfying Action Output + Closed-Loop Evaluation
- Background/design-context studies: 58
- Only 2/19 primary empirical studies report extractable time-consistent split protocols
- Only 1/19 reports an explicit transaction-cost model
- Only 1/19 documents universe or survivorship handling
- 11/19 report execution timing or semantics
- 15/19 are coded as R0
- No study reaches R3 reproducibility

## Why it matters for Project Aegis

This paper directly supports the claim that the field's immediate bottleneck is not merely agent architecture but trustworthy evaluation. It provides evidence that current LLM trading-agent studies are difficult to compare and reproduce.

## Methodological value

The paper is valuable because it demonstrates how to make a literature review more defensible:

1. It defines a study inclusion boundary.
2. It separates primary empirical studies from background/design-context studies.
3. It codes reproducibility and reporting quality.
4. It introduces an evidence ledger and reporting checklist.
5. It avoids claiming that its taxonomy is final; it calls Architecture-Capability-Adaptation a working analytical lens.

## Main limitation

The paper itself is still a survey and evidence map. It does not build the trustworthy investment research system that Project Aegis aims to study. It also focuses on trading agents rather than the broader institutional investment research workflow.

## Project Aegis gap revealed

The paper reveals the need for:

1. a reproducibility checklist for financial agents;
2. a transaction-cost and execution-semantics reporting standard;
3. a survivorship and universe-handling checklist;
4. an audit trail for agent decisions;
5. a shift from trading-action evaluation to investment-research workflow evaluation.

## Relationship to Project Aegis thesis

Project Aegis extends this paper in three ways:

1. From **trading agents** to **investment research agents**.
2. From **performance comparison** to **trustworthy research workflow**.
3. From **survey evidence map** to **framework for reproducible, auditable, risk-aware multi-agent investment research**.

## Initial quality score

- Relevance: 4/4
- Evidence strength: 4/4
- Reproducibility: 3/4
- Auditability: 3/4
- Risk-awareness: 4/4
- Gap value: 4/4
- Total: 22/24
- Classification: Core literature

## Reviewer questions

1. Is the paper's primary empirical subset definition too narrow or too broad?
2. Does the Action Output + Closed-Loop Evaluation boundary exclude relevant investment research agents that do not trade directly?
3. Can the reproducibility coding scheme be reused for investment research agents?
4. Does the paper overemphasize trading performance and underemphasize research workflow quality?
5. What would be the equivalent of transaction-cost reporting for investment research agents?
6. What is the equivalent of execution semantics when an agent produces an investment thesis rather than a trade?

## How to use this paper in the living review

Use P001 as the main evidence source for the statement:

> Existing LLM trading-agent research suffers from protocol incomparability and weak reproducibility, making trustworthy evaluation an urgent research gap.

But avoid overclaiming. P001 supports the reproducibility gap for trading agents. It does not by itself prove the same gap for all investment research agents; that extension must be supported by additional papers such as P013, P014, and P016.

## Extraction status

- Metadata: verified from arXiv page
- Abstract-level evidence: verified from arXiv page
- Full-text section-level extraction: pending
- Tables/figures extraction: pending
- Citation chasing: pending
