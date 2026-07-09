# Improvement Summary v2.0

## Date

2026-07-09

## Purpose

This iteration continues improving P025 by verifying the external resources reported by the paper: the GitHub code repository and the Hugging Face dataset page.

The goal is to move P025 from `reported public resources` toward `partially verified public resources` while preserving uncertainty around license chain, source rights, and full reproducibility.

## Improvements completed

### 1. P025 external resource verification added

Added:

`00-Source-Archive/P025-FinRpt/external-resource-verification-v0.1.md`

This file verifies:

- the reported GitHub repository is reachable and public;
- the README exists;
- the README contains the arXiv and Hugging Face links;
- the README states that all code and datasets are publicly available;
- the README lists project structure paths;
- the README states MIT License;
- a standalone root `LICENSE` file was not found via GitHub fetch;
- the Hugging Face dataset page is reachable;
- the Hugging Face page shows `cc-by-4.0`;
- the dataset viewer shows about 13.6k rows;
- visible fields include prompt/response columns for multiple agents.

### 2. P025 source record updated

Updated:

`00-Source-Archive/P025-FinRpt/source-record-v0.1.md`

The source record now includes:

- GitHub verification status;
- Hugging Face verification status;
- caution about README MIT statement versus missing standalone LICENSE file;
- caution about paper-level 6,825 ERR sample count versus about 13.6k Hugging Face viewer rows;
- source-copying policy.

### 3. P025 extraction tracker updated

Updated:

`03-Full-Extraction/P025-Extraction-Tracker-v0.1.csv`

The tracker now marks:

- metadata as `source_and_external_resources_partially_verified`;
- reproducibility as `public_code_dataset_partially_verified_license_chain_pending`.

## What became stronger

### Better reproducibility evidence for P025

P025 is now stronger because the reported public code and dataset resources are not just claims in the paper; they have been partially verified.

### Better source archive discipline

The repository now has a source archive record and external verification file for P025.

This is important because Project Aegis should not only summarize papers. It should track the availability and reuse limits of source materials.

### Better license caution

The project now distinguishes:

- README license statement;
- standalone license file;
- Hugging Face dataset license;
- upstream source-rights chain.

This is important because a dataset may show a license, but source news, announcements, reports, or generated outputs may still raise reuse questions.

## What remains weak

1. The standalone root LICENSE file for the GitHub repository was not found.
2. The Hugging Face row count differs from the paper-level sample count.
3. The dataset license chain and upstream source rights remain unverified.
4. The code has not been run.
5. The repo tree, requirements, scripts, prompts, and generated report examples need deeper inspection.
6. Claim-level evidence grounding remains unestablished.
7. P025 figures and appendix prompts remain pending.

## Current status after v2.0

Project Aegis remains:

**Level 2.0 candidate / 5**

But P025 is now stronger than before because it has:

- source-level extraction;
- source archive record;
- external resource verification;
- tracker updates.

## Recommended next step

Continue P025 verification by inspecting:

1. GitHub repository tree;
2. `requirements.txt`;
3. dataset card/files on Hugging Face;
4. prompt/output fields;
5. generated report case;
6. whether reports contain citations or evidence links;
7. figure assets: `assets/pipeline.png`, `assets/agent.png`, and `assets/report.png`.

The highest-value next file is:

`00-Source-Archive/P025-FinRpt/repository-structure-verification-v0.1.md`
