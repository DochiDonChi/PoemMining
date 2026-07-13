# Improvement Summary v1.9

## Date

2026-07-09

## Purpose

This iteration performs the first real source-level extraction for P025 FinRpt and creates a source record for the paper.

The goal is to move P025 beyond scaffold-level planning and make it a stronger investment-research-agent / equity research report generation anchor.

## Improvements completed

### 1. P025 source record added

Added:

`00-Source-Archive/P025-FinRpt/source-record-v0.1.md`

This file records:

- arXiv metadata;
- arXiv abstract URL;
- arXiv HTML URL;
- reported GitHub code URL;
- reported Hugging Face dataset URL;
- source-level facts;
- repository policy for storing source material;
- next verification tasks.

Important decision:

The repository stores source metadata and extracted facts first. It does not store the full PDF until redistribution rights and licensing terms are checked.

### 2. P025 source-level extraction added

Added:

`03-Full-Extraction/P025-Dataset-Metrics-Architecture-Extraction-v0.1.md`

This file extracts:

- ERR generation task formulation;
- output report structure;
- dataset construction;
- data sources and filtering;
- dataset enhancement process;
- dataset statistics and split;
- FinRpt-Gen architecture;
- agent roles;
- training strategy;
- evaluation metrics;
- baselines and experimental setup;
- basic metric results;
- ablation study;
- human evaluation;
- code and dataset availability claims;
- auditability assessment;
- updated P016/P025 comparison;
- updated claim status.

### 3. P025 extraction tracker updated

Updated:

`03-Full-Extraction/P025-Extraction-Tracker-v0.1.csv`

Several items are now marked as extracted:

- dataset name and construction;
- source documents and company universe;
- input-output format;
- exact evaluation metrics;
- human evaluation design;
- multi-agent framework overview;
- agent roles;
- baselines;
- comparison with P016.

Several items remain pending or partially established:

- claim-level evidence grounding;
- hallucination / unsupported-claim error analysis;
- GitHub and Hugging Face license verification;
- appendix prompt extraction;
- figure extraction.

### 4. Extraction depth tracker updated

Updated:

`03-Full-Extraction/Extraction-Depth-Status-v0.1.csv`

P025 is now marked as:

`section_level_plus_source_level_dataset_metrics_architecture_extraction`

## What became stronger

### P025 is no longer only a scaffold

P025 now has concrete source-level evidence extracted from the arXiv HTML source.

### Investment research agent side is stronger

The project now has much better evidence that ERR generation is an emerging task with:

- a defined task formulation;
- a dataset;
- a multi-agent framework;
- finance-specific metrics;
- human evaluation;
- public code/dataset claims.

### P025 is now a stronger anchor for research-artifact generation

The paper now supports a stronger but still cautious claim:

> Equity research report generation is becoming a structured benchmark and multi-agent system problem within financial-agent research.

## What remains weak

1. P025 does not yet establish claim-level evidence grounding.
2. P025 code and dataset availability are reported but not independently verified.
3. P025 license and redistribution status are not verified.
4. P025 appendix prompts are not yet extracted.
5. P025 figures and appendix tables are not yet extracted.
6. P025 generated report examples are not yet inspected for citations or evidence references.
7. P001 exact R0-R3 definitions remain pending.
8. Full Search-Round-02 remains incomplete.

## Current status after v1.9

Project Aegis remains:

**Level 2.0 candidate / 5**

But the project is significantly stronger than before because it now has:

- P001 as a strengthened reproducibility-gap anchor;
- P025 as a strengthened research-artifact generation anchor;
- explicit uncertainty around auditability and evidence grounding.

## Recommended next step

The next best step is external source verification for P025:

1. verify GitHub repository availability and license;
2. verify Hugging Face dataset availability and license;
3. extract Appendix prompts;
4. inspect final report case for citations / evidence grounding;
5. extract Figure 1 dataset pipeline and Figure 3 FinRpt-Gen architecture.

These steps determine whether P025 can become a strong reproducibility and auditability anchor, or only a strong task/dataset/architecture anchor.
