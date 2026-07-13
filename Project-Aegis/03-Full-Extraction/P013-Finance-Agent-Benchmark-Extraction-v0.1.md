# P013 Full Extraction v0.1

## Paper

**Finance Agent Benchmark: Benchmarking LLMs on Real-world Financial Research Tasks**

## Metadata

- Paper ID: P013
- Year: 2025
- Source: arXiv
- arXiv ID: 2508.00828
- URL: https://arxiv.org/abs/2508.00828
- Authors: Antoine Bigeard; Langston Nashold; Rayan Krishnan; Shirley Wu
- Submitted: 2025-05-20
- Subject: Computer Science > Computational Engineering, Finance, and Science

## Research stream

Benchmark / investment research tasks / real-world finance reasoning

## Why this paper is included

This paper is highly relevant because it evaluates LLM agents on real-world finance research tasks rather than only trading signals or generic financial question answering. It directly supports Project Aegis's argument that reliable AI investment research requires more than price prediction.

## Main research question

How capable are LLM agents at solving realistic financial research problems that require analysis of recent SEC filings and finance-domain reasoning?

## Core contribution

The paper introduces the Finance Agent Benchmark, a benchmark of expert-authored financial research questions designed to test LLM agents in realistic finance workflows.

## Key evidence from abstract

- Dataset size: 537 expert-authored questions
- Task coverage: nine financial task categories
- Expert input: taxonomy developed in consultation with experts from banks, hedge funds, and private equity firms
- Data source emphasis: recent SEC filings
- Tool harness: Google Search and EDGAR database access
- Best reported model: OpenAI o3
- Best reported accuracy: 46.8 percent
- Average cost for best model: USD 3.79 per query

## Why it matters for Project Aegis

This paper is important because it shows that even strong current models struggle with expert-level finance research tasks. That supports the Project Aegis thesis that the field should not jump too quickly to autonomous trading or portfolio management without first solving trustworthy investment research.

## Methodological value

The benchmark has several strengths:

1. It focuses on real-world finance research tasks.
2. It uses recent SEC filings rather than only static textbook-style questions.
3. It uses expert-authored questions.
4. It includes an agentic tool harness with external search and EDGAR access.
5. It reports both accuracy and cost.

## Main limitation

The benchmark is still primarily a question-answering benchmark. It does not fully model the institutional buy-side research process, including thesis generation, evidence debate, valuation, risk review, portfolio implications, human challenge, and audit trail.

## Project Aegis gap revealed

This paper reveals the gap between:

- answering finance research questions;
- producing a defensible investment thesis;
- integrating that thesis into a portfolio decision;
- documenting evidence and contrary evidence;
- making the process auditable.

## Relationship to Project Aegis thesis

Project Aegis can build on this benchmark by asking:

1. How should finance research tasks be embedded inside a multi-agent investment research workflow?
2. How should accuracy be combined with evidence quality, reasoning traceability, risk awareness, and auditability?
3. Can a benchmark evaluate not only final answers but the research process itself?

## Initial quality score

- Relevance: 4/4
- Evidence strength: 4/4
- Reproducibility: 3/4
- Auditability: 2/4
- Risk-awareness: 2/4
- Gap value: 4/4
- Total: 19/24
- Classification: Important literature

## Reviewer questions

1. Are 537 questions enough to represent real finance research?
2. How are the nine task categories defined?
3. Are questions biased toward SEC filing retrieval rather than broader investment judgment?
4. Does accuracy capture the quality of financial reasoning?
5. How should cost per query be incorporated into evaluation?
6. Does the benchmark test ability to consider contrary evidence?
7. Does the benchmark test risk awareness?
8. Can this benchmark be adapted for buy-side investment thesis generation?

## How to use this paper in the living review

Use P013 as the main evidence source for the claim:

> Current LLM agents still face significant limitations on real-world expert-authored financial research tasks, even when equipped with search and EDGAR tools.

Do not use it as evidence that LLM agents cannot trade or cannot create alpha. Its evidence is specifically about finance research question performance.

## Extraction status

- Metadata: verified from arXiv page
- Abstract-level evidence: verified from arXiv page
- Full-text section-level extraction: pending
- Task taxonomy extraction: pending
- Benchmark design extraction: pending
