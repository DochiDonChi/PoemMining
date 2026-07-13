# Improvement Summary v1.8

## Date

2026-07-09

## Purpose

This iteration follows the recommendation from the previous review step: after strengthening P001 as the reproducibility-gap anchor, the project now begins strengthening P025 as the investment-research-agent / equity research report generation anchor.

The goal is to balance the thesis:

- P001 supports the reproducibility and protocol-reporting problem in trading-agent literature.
- P025 supports the emerging research-artifact generation direction for investment research agents.

## Improvements completed

### 1. P025 full-text extraction scaffold added

Added:

`03-Full-Extraction/P025-FinRpt-Full-Text-Extraction-v0.2.md`

This file upgrades P025 from abstract-level extraction to a section-level extraction scaffold.

It covers:

- bibliographic metadata;
- research problem;
- claimed components to verify;
- dataset extraction plan;
- evaluation metric extraction plan;
- multi-agent framework extraction plan;
- evidence grounding and auditability extraction plan;
- comparison with P016;
- correct and incorrect use in the living review;
- supervisor-style defense answer;
- remaining extraction tasks.

### 2. P025 extraction tracker added

Added:

`03-Full-Extraction/P025-Extraction-Tracker-v0.1.csv`

This tracker lists high-priority extraction targets:

- dataset name and construction;
- source documents and company universe;
- input-output format;
- exact evaluation metrics;
- factuality and evidence-grounding metrics;
- human evaluation design;
- multi-agent framework overview;
- agent roles;
- retrieval and grounding mechanism;
- baseline systems;
- error analysis;
- code/data/prompt/report availability;
- limitations;
- comparison with P016.

### 3. Extraction depth tracker updated

Updated:

`03-Full-Extraction/Extraction-Depth-Status-v0.1.csv`

P025 is now marked as:

`section_level_scaffold_dataset_metrics_architecture_pending`

This indicates that P025 is no longer only abstract-level, but the most important full-text details are still pending.

## What became stronger

### Better thesis balance

Before this step, Project Aegis was becoming stronger on the trading-agent reproducibility side but still weak on the investment research agent side.

This update begins to fix that imbalance.

### Clearer P025 extraction agenda

The project now has a concrete checklist for extracting the evidence that matters most:

1. dataset construction;
2. evaluation metrics;
3. multi-agent architecture;
4. evidence grounding;
5. reproducibility.

### Better anti-overclaiming discipline

The new P025 extraction explicitly separates what P025 may support from what it does not yet prove.

## What remains weak

1. P025 dataset details remain pending.
2. P025 exact evaluation metrics remain pending.
3. P025 multi-agent architecture remains pending.
4. P025 evidence-grounding and auditability remain pending.
5. P025 code/data availability remains pending.
6. P001 exact R0-R3 definitions remain pending.
7. Full Search-Round-02 remains incomplete.

## Current status after v1.8

Project Aegis remains:

**Level 2.0 candidate / 5**

However, the project is now better balanced:

- P001 is the leading reproducibility-gap anchor.
- P025 is becoming the leading equity research report generation anchor.

## Recommended next step

Continue P025 extraction with the highest-value items:

1. dataset construction;
2. exact evaluation metrics;
3. multi-agent architecture;
4. evidence-grounding mechanism.

These items determine whether P025 can be used as strong evidence for the investment research agent category or only as a promising candidate.
