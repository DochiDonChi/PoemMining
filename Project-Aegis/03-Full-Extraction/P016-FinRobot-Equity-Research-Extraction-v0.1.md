# P016 Full Extraction v0.1

## Paper

**FinRobot: AI Agent for Equity Research and Valuation with Large Language Models**

## Metadata

- Paper ID: P016
- Year: 2024
- Source: arXiv
- arXiv ID: 2411.08804
- URL: https://arxiv.org/abs/2411.08804
- Authors: Tianyu Zhou; Pinqiao Wang; Yilin Wu; Hongyang Yang
- Submitted: 2024-11-13
- Verification status: verified from arXiv metadata and abstract-level source

## Research stream

Investment research agent / equity research / valuation / multi-agent reasoning

## Why this paper is included

This paper is one of the most directly relevant papers for Project Aegis because it explicitly targets equity research and valuation rather than only trading actions. It helps support the distinction between **trading agents** and **investment research agents**.

## Main research question

Can a multi-agent LLM framework emulate parts of a human equity analyst's workflow, including data integration, conceptual reasoning, valuation, risk assessment, thesis synthesis, and report generation?

## Core contribution

The paper presents FinRobot as an AI agent framework designed for equity research. According to the abstract, the system uses a multi-agent Chain-of-Thought structure with three specialized agents:

1. **Data-CoT Agent** — aggregates diverse data sources for financial integration.
2. **Concept-CoT Agent** — imitates analyst reasoning to generate insights.
3. **Thesis-CoT Agent** — synthesizes insights into an investment thesis and report.

## Key evidence from abstract

- Focuses on equity research, particularly sell-side research.
- Argues that existing AI tools often focus too narrowly on technical factors.
- Claims to combine quantitative and qualitative analysis.
- Includes company analysis, valuation metrics, risk assessment, and report generation.
- Claims a dynamically updatable data pipeline.
- Open-source release is mentioned in the abstract.

## Why it matters for Project Aegis

P016 is useful because it moves closer to the Project Aegis target than pure trading-agent papers. It focuses on generating an investment thesis and research report, which are central to real analyst workflows.

## Methodological value

The paper helps Project Aegis develop a more precise taxonomy:

- Trading agent: outputs trading actions.
- Finance QA agent: answers financial questions.
- Equity research agent: produces company analysis, valuation, risk assessment, and investment thesis.
- Investment research system: coordinates evidence, thesis, risk, portfolio implication, audit trail, and human review.

P016 likely belongs to the third category and can be used as a bridge toward the fourth.

## Main limitation

Based on abstract-level extraction, the main limitation is that the paper appears to focus on generating analyst-like outputs, but Project Aegis still needs to verify:

1. whether the evaluation compares outputs against professional analysts;
2. whether it records evidence trails and contrary evidence;
3. whether valuation assumptions are auditable;
4. whether risk assessment is systematic or narrative;
5. whether human review is built into the workflow;
6. whether reproducibility details are sufficient.

## Project Aegis gap revealed

P016 reveals a key gap:

> Equity research agents can generate reports and investment theses, but the field still needs stronger standards for auditability, evidence traceability, professional evaluation, and human-in-the-loop governance.

## Relationship to Project Aegis thesis

P016 supports the Project Aegis argument that the field is moving beyond trading agents toward investment research agents. However, it also reinforces the need for trustworthy research-system design, because report generation alone does not guarantee institutional usability.

## Initial quality score

- Relevance: 4/4
- Evidence strength: 3/4
- Reproducibility: 3/4
- Auditability: 2/4
- Risk-awareness: 2/4
- Gap value: 4/4
- Total: 18/24
- Classification: Important literature

## Reviewer questions

1. How exactly is FinRobot evaluated?
2. Are the generated reports compared with human analyst reports?
3. Are valuation assumptions explicitly listed and auditable?
4. Does the system record source evidence for each claim?
5. Does it include contrary evidence or only supporting evidence?
6. Does risk assessment include quantitative downside analysis or only narrative discussion?
7. Does the open-source repository reproduce the paper's claimed workflow?
8. How would this system behave in market regime shifts?
9. Is this framework sell-side research only, or can it support buy-side investment decisions?
10. What is missing before it can be used in a real asset-management workflow?

## How to use this paper in the living review

Use P016 as evidence for the emergence of **equity research agents**. Do not overclaim that it solves trustworthy investment research. Its most important value is showing that the field is beginning to model analyst-like workflows, while still leaving auditability and institutional evaluation as research gaps.

## Extraction status

- Metadata: verified from arXiv page
- Abstract-level extraction: completed
- Full-text section-level extraction: pending
- Evaluation details extraction: pending
- Architecture diagram extraction: pending
- Open-source reproducibility check: pending
