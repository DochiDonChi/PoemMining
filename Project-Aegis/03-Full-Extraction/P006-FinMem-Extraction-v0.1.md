# P006 Full Extraction v0.1

## Paper

**FinMem: A Performance-Enhanced LLM Trading Agent with Layered Memory and Character Design**

## Metadata

- Paper ID: P006
- Year: 2023
- Source: arXiv
- arXiv ID: 2311.13743
- URL: https://arxiv.org/abs/2311.13743
- Authors: Yangyang Yu; Haohang Li; Zhi Chen; Yuechen Jiang; Yang Li; Denghui Zhang; Rong Liu; Jordan W. Suchow; Khaldoun Khashanah
- Submitted: 2023-11-23
- Verification status: verified from arXiv metadata and abstract-level source

## Research stream

Memory-based financial agent / LLM trading agent / layered memory / character design

## Why this paper is included

FinMem is a central memory-focused paper in the financial LLM-agent literature. It is important for Project Aegis because a trustworthy investment research system cannot rely only on one-shot prompts. It needs structured memory for prior theses, macro context, company history, past mistakes, and regime shifts.

## Main research question

Can an LLM-based trading agent improve financial decision-making by using profiling, layered memory, and character design to process multi-source information and retain critical financial context?

## Core contribution

According to the arXiv abstract, FinMem introduces an LLM-based agent framework for financial decision-making with three core modules:

1. **Profiling** — customizes agent characteristics.
2. **Memory** — uses layered message processing to help the agent assimilate hierarchical financial data.
3. **Decision-making** — converts insights from memory into investment decisions.

The paper argues that the memory module aligns with the cognitive structure of human traders and enables interpretability, real-time tuning, adjustable cognitive span, and continuous refinement of trading decisions.

## Key evidence from abstract

- The paper targets financial decision-making and automated trading.
- It emphasizes multi-source information processing and reasoning chains.
- It uses layered memory to retain critical information beyond human perceptual limits.
- It reports comparison with algorithmic agents on a scalable real-world financial dataset.
- It claims enhanced trading outcomes after tuning perceptual span and character setting.

## Why it matters for Project Aegis

P006 supports the long-term memory dimension of Project Aegis. Investment research is not a one-shot task. A credible system needs memory of:

- past investment theses;
- company events;
- management credibility;
- macro regimes;
- previous forecast errors;
- portfolio exposure;
- rejected ideas and reasons.

FinMem is therefore useful even though it is primarily framed as a trading agent.

## Methodological value

The paper helps Project Aegis separate different memory concepts:

- short-term context window;
- episodic memory;
- hierarchical memory;
- trader-character profile;
- real-time tuning;
- memory-to-decision conversion.

This provides a foundation for designing `investment thesis memory` later.

## Main limitation

Based on abstract-level extraction, the main limitation is that FinMem appears focused on trading outcomes rather than institutional investment research quality. Project Aegis still needs to verify:

1. what exact memory layers are used;
2. what information enters memory;
3. how memory is updated;
4. whether memory can be audited;
5. whether memory causes anchoring or stale-thesis risk;
6. whether memory improves risk-adjusted returns after costs;
7. whether the framework generalizes beyond the evaluated assets or time period.

## Project Aegis gap revealed

FinMem reveals the need for memory mechanisms, but also exposes a deeper research gap:

> Financial-agent memory should not only improve trading returns; it should be auditable, editable, evidence-linked, and able to distinguish useful long-term context from stale or biased beliefs.

## Relationship to Project Aegis thesis

P006 supports the memory pillar of a trustworthy investment research system. Project Aegis can extend it from `trading memory` toward `research memory`, including thesis memory, error memory, regime memory, and portfolio memory.

## Initial quality score

- Relevance: 3/4
- Evidence strength: 3/4
- Reproducibility: 2/4
- Auditability: 1/4
- Risk-awareness: 1/4
- Gap value: 4/4
- Total: 14/24
- Classification: Supporting literature

## Reviewer questions

1. What are the exact memory layers and update rules?
2. Does the memory module have an audit trail?
3. Can memory entries be traced back to source evidence?
4. Does memory improve decisions after transaction costs?
5. Does memory create anchoring or confirmation bias?
6. Is character design robust or prompt-sensitive?
7. Can memory be transferred from trading to investment research?
8. How does the model handle contradictory memories?
9. Does the system forget outdated information?
10. What would thesis memory look like in a buy-side research process?

## How to use this paper in the living review

Use P006 as evidence that memory is an important architectural direction for financial agents. Do not use it as proof that memory-based agents are trustworthy. Its best use is to motivate a more rigorous research question: how should financial-agent memory be designed so that it is useful, auditable, and resistant to stale or biased reasoning?

## Extraction status

- Metadata: verified from arXiv page
- Abstract-level extraction: completed
- Full-text section-level extraction: pending
- Memory architecture extraction: pending
- Experiment and cost-assumption extraction: pending
- Bias / stale-memory risk extraction: pending
