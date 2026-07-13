# P025 Extraction v0.1

## Paper

**FinRpt: Dataset, Evaluation System and LLM-based Multi-agent Framework for Equity Research Report Generation**

## Metadata

- Paper ID: P025
- Year: 2025
- Source: arXiv
- arXiv ID: 2511.07322
- URL: https://arxiv.org/abs/2511.07322
- Authors: Song Jin; Shuqi Li; Shukun Zhang; Rui Yan
- Verification status: verified from Search-Round-02A arXiv metadata / abstract-level capture

## Research stream

Equity research report generation / investment research agent / benchmark and evaluation / multi-agent framework

## Why this paper is high priority

P025 is one of the most important new Search-Round-02A candidates because it directly targets equity research report generation. This is closer to Project Aegis than many trading-agent papers, because the primary output appears to be a research artifact rather than a direct trading action.

## Relationship to Project Aegis definition

Using `Definition-Investment-Research-Agent-v0.1.md`, P025 appears to satisfy several investment research agent criteria at abstract level:

1. **Evidence gathering** — likely uses company / market / financial information for report generation.
2. **Financial reasoning** — likely requires reasoning over equity research content.
3. **Research artifact generation** — directly targets equity research report generation.
4. **Multi-step workflow** — includes an LLM-based multi-agent framework.
5. **Decision support** — equity research reports are decision-support artifacts.
6. **Traceability potential** — dataset and evaluation design may support traceability, but this requires full-text verification.

Preliminary coding: `equity_research_agent` / `investment_research_agent` / `benchmark_evaluation_framework`.

## Main research question

How can LLM-based systems generate and evaluate equity research reports using a dataset, evaluation system, and multi-agent framework?

## Core contribution based on Search-Round-02A abstract-level capture

The paper appears to contribute three components:

1. a dataset for equity research report generation;
2. an evaluation system with multiple metrics;
3. an LLM-based multi-agent framework, referred to in the Search-Round-02A screening notes as FinRpt-Gen.

## Why it matters for Project Aegis

P025 may become a second strong anchor for the investment research agent category alongside P016 FinRobot Equity Research.

P016 is useful because it frames equity research and valuation using Data-CoT, Concept-CoT, and Thesis-CoT agents. P025 appears to strengthen this category because it focuses explicitly on equity research report generation and evaluation.

Together, P016 and P025 could support a more defensible claim:

> Equity research agents are emerging as a distinct subcategory of financial agents whose primary output is a research artifact rather than a trading action.

This claim remains preliminary until more papers are coded.

## Methodological value

P025 is especially valuable because it may help Project Aegis evaluate research artifacts rather than only market returns. This is important because investment research quality cannot be judged only by trading performance.

Potential evaluation dimensions to extract from the full text:

1. report factual accuracy;
2. evidence grounding;
3. financial reasoning quality;
4. valuation quality;
5. risk discussion quality;
6. structure and completeness;
7. consistency with source documents;
8. analyst usefulness;
9. hallucination or unsupported claim rate;
10. traceability from report claims to evidence.

## Main limitation at current extraction depth

This extraction is based on Search-Round-02A abstract-level capture. The following details are still unknown:

1. dataset construction procedure;
2. source documents used;
3. evaluation metrics and whether there are 11 metrics as captured in screening notes;
4. multi-agent architecture;
5. model backbones;
6. baseline systems;
7. human evaluation design;
8. whether generated reports are compared with professional analyst reports;
9. whether claims are traceable to source evidence;
10. whether code or data are available.

## Project Aegis gap revealed

P025 suggests that the field is moving toward research-artifact generation, not only trading decisions. The next gap is likely:

> How can AI-generated equity research reports be made reproducible, auditable, evidence-grounded, and useful for human investment decision-making?

## Initial quality score proposal

This is a proposed score only and should not replace the formal score table until full-text extraction is completed.

- Relevance: 4/4
- Evidence strength: 3/4
- Reproducibility: 2/4
- Auditability: 2/4
- Risk-awareness: 2/4
- Gap value: 4/4
- Proposed total: 17/24
- Proposed classification: Important literature / high-priority extraction candidate

## Reviewer questions

1. What exact dataset is introduced?
2. What are the evaluation metrics?
3. Does the evaluation measure evidence grounding or only text quality?
4. Does the paper compare generated reports with professional analyst reports?
5. Does the multi-agent framework include specialized analyst roles?
6. Does it include valuation and risk reasoning?
7. Does it record source citations or evidence trails?
8. Does it handle hallucination and unsupported claims?
9. Is the dataset public?
10. Can the results be reproduced?
11. Is the task sell-side report generation only, or can it support buy-side investment decisions?
12. How does P025 differ from P016 FinRobot Equity Research?

## How to use this paper in the living review

Use P025 as a high-priority candidate for the claim:

> Equity research report generation is becoming an important subproblem for investment research agents.

Do not yet use it as strong evidence for auditability, reproducibility, or institutional readiness until full-text extraction is completed.

## Extraction status

- Metadata: captured through Search-Round-02A arXiv-focused pilot
- Abstract-level extraction: completed
- Full-text section-level extraction: pending
- Dataset extraction: pending
- Evaluation-metric extraction: pending
- Architecture extraction: pending
- Report-quality / evidence-grounding extraction: pending
- Code/data availability check: pending
