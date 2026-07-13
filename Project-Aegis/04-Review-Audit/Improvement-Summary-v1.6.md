# Improvement Summary v1.6

## Date

2026-07-09

## Purpose

This iteration continues the P001 full-text extraction upgrade by extracting the first high-priority figures and tables.

## Improvements completed

### 1. P001 core table/figure extraction added

Added:

`03-Full-Extraction/P001-Core-Tables-Figures-Extraction-v0.1.md`

This file extracts:

1. Figure 1 — Agency Spectrum of Trading Systems
2. Figure 2 — Reasoning Flow Diagram
3. Table 1 — Related surveys / benchmarks comparison
4. Table 3 — Study selection summary

### 2. P001 table/figure tracker updated

Updated:

`03-Full-Extraction/P001-Table-Figure-Extraction-Tracker-v0.1.csv`

The following items are now marked as extracted:

- P001-FIG-01 — Figure 1 Agency Spectrum of Trading Systems
- P001-FIG-02 — Figure 2 Reasoning Flow Diagram
- P001-TAB-01 — Table 1 Related surveys and benchmarks
- P001-TAB-03 — Table 3 Study selection summary

### 3. Extraction depth tracker updated

Updated:

`03-Full-Extraction/Extraction-Depth-Status-v0.1.csv`

P001 is now marked as:

`section_level_plus_partial_table_figure_extraction`

with:

- `table_extraction = partial_core_tables`
- `figure_extraction = partial_core_figures`

## What became stronger

### Stronger boundary discipline

Figure 1 helps Project Aegis think more rigorously about what counts as a trading agent and how to create an analogous boundary for investment research agents.

### Stronger workflow framing

Figure 2 helps translate trading-agent reasoning loops into Project Aegis's investment research workflow:

source evidence → research memory → reasoning/valuation → candidate thesis → evidence/risk review → research artifact → human feedback.

### Stronger denominator discipline

Table 3 clarifies how P001 separates:

- 92 candidate records;
- 77 included evidence-mapping records;
- 19 primary empirical studies;
- 58 background/context studies.

This is a useful model for Project Aegis's future primary/background/candidate paper split.

## What remains weak

1. Protocol reporting tables are still pending.
2. Reproducibility tier tables are still pending.
3. R0-R3 definitions still require extraction.
4. Reporting checklist tables are still pending.
5. Most of P001's 27 tables and 15 figures remain unextracted.

## Current status after v1.6

Project Aegis remains:

**Level 2.0 candidate / 5**

However, P001 is now meaningfully beyond abstract-level extraction. It has section-level extraction plus first-pass core table/figure extraction.

## Recommended next step

Continue P001 extraction with the most important remaining evidence items:

1. Protocol reporting tables;
2. Reproducibility tier tables;
3. R0-R3 reproducibility definitions;
4. Reporting checklist items.

These items are more important than extracting every remaining figure because they directly support the reproducibility-gap claim.
