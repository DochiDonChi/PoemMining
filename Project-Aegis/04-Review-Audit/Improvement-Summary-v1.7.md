# Improvement Summary v1.7

## Date

2026-07-09

## Purpose

This iteration directly addresses the recommendations from `Reviewer-Audit-v0.8.md` by improving the P001 evidence layer. The goal is to make the reproducibility-gap evidence more explicit and less interpretive.

## Improvements completed

### 1. P001 protocol and reproducibility extraction added

Added:

`03-Full-Extraction/P001-Protocol-Reproducibility-Extraction-v0.1.md`

This file focuses on:

- time-consistent split reporting;
- transaction-cost modeling;
- universe / survivorship handling;
- execution timing semantics;
- R0-R3 reproducibility counts;
- reporting checklist implications;
- correct and incorrect claim use.

### 2. Extraction discipline improved

The new P001 extraction uses a stricter five-layer structure:

1. Source content
2. Structured extraction
3. Project Aegis interpretation
4. Claim supported
5. Claim not supported

This directly addresses the v0.8 concern that earlier extraction could mix source content with Project Aegis interpretation.

### 3. P001 table/figure tracker updated

Updated:

`03-Full-Extraction/P001-Table-Figure-Extraction-Tracker-v0.1.csv`

The tracker now marks:

- protocol reporting tables as `extracted_high_level_v0.1`;
- reproducibility tier tables as `extracted_high_level_counts_v0.1`;
- reporting checklist as `derived_checklist_v0.1_pending_source_verification`.

### 4. Extraction depth tracker updated

Updated:

`03-Full-Extraction/Extraction-Depth-Status-v0.1.csv`

P001 is now marked as:

`section_level_plus_partial_table_figure_and_protocol_extraction`

## What became stronger

### Stronger reproducibility-gap evidence

The project now has a dedicated extraction file for the exact evidence pillar that supports the reproducibility-gap claim.

### Better anti-overclaiming discipline

The extraction explicitly states what P001 supports and does not support.

This is important because P001 is strong evidence for trading-agent reproducibility gaps, but only indirect evidence for investment research agent trustworthiness.

### Better translation to Project Aegis

The file translates trading-agent protocol fields into investment-research-agent protocol fields:

- time-consistent split → evidence timestamp / source-version control;
- transaction cost → query, data, latency, and review cost;
- universe / survivorship → company and document universe control;
- execution timing → report timestamp / evidence availability semantics;
- reproducibility artifacts → prompt/code/data/report reconstruction package.

## What remains weak

1. Exact R0-R3 definitions still need extraction.
2. Exact protocol/reproducibility table numbers still need verification.
3. Per-study protocol entries still need extraction.
4. P025 remains shallow relative to its importance.
5. Full Search-Round-02 remains incomplete.

## Current status after v1.7

Project Aegis remains:

**Level 2.0 candidate / 5**

However, the P001 reproducibility-gap anchor is now significantly stronger than before because it has a dedicated protocol/reproducibility extraction pass.

## Recommended next step

Two possible next steps:

### Option A — Finish exact P001 evidence verification

Extract exact R0-R3 definitions, exact table numbers, and per-study protocol entries.

### Option B — Balance the thesis by upgrading P025

Start `P025-FinRpt-Full-Text-Extraction-v0.2.md` to strengthen the investment research agent side of the project.

Recommended choice: Option B if the goal is to balance the thesis; Option A if the goal is to make the P001 reproducibility claim maximally defensible.
