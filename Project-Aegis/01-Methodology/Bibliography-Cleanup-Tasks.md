# Bibliography Cleanup Tasks

## Purpose

This file records incomplete, uncertain, or placeholder bibliography metadata that must be cleaned before the review can be shown to supervisors or submitted anywhere.

## Why this matters

A systematic review is only as credible as its bibliographic discipline. Placeholder authors such as `Paper authors`, `Survey authors`, or `Article authors` make the project look amateur and will be challenged immediately by any serious reviewer.

## High-priority cleanup items

### P007 — Large Language Model Agents for Investment Management

- Current issue: authors are listed as `Paper authors`.
- Required action:
  - Verify official title.
  - Verify authors.
  - Verify source / venue.
  - Verify whether the source is SSRN, ACM, or another venue.
  - Verify publication year and version.
  - Verify whether the paper is a survey, empirical paper, or conceptual framework.
- Status: **metadata incomplete**.

### P008 — Large Language Model Agents in Finance: A Survey

- Current issue: authors are listed as `Survey authors`.
- Required action:
  - Verify ACL Anthology record.
  - Add full author list.
  - Add venue name and paper identifier.
  - Confirm whether this is Findings of ACL / EMNLP / other ACL venue.
- Status: **metadata incomplete**.

### P009 — Large Language Models in Equity Markets

- Current issue: authors are listed as `Article authors`.
- Required action:
  - Verify Frontiers page.
  - Add full author list.
  - Add DOI.
  - Confirm year and article number.
- Status: **metadata incomplete**.

### P010 — A Risk-First Evaluation Framework for Multi-Agent LLM Systems in Financial Markets

- Current issue: authors are listed as `Paper authors`.
- Required action:
  - Verify ACL Anthology record.
  - Add full author list.
  - Add venue and PDF URL.
  - Confirm title exactly.
- Status: **metadata incomplete**.

### P011 — Evaluating LLMs in Finance Requires Explicit Bias Assessment

- Current issue: authors are listed as `Paper authors`.
- Required action:
  - Verify arXiv record.
  - Add full author list.
  - Verify abstract claims and reviewed-paper count.
- Status: **metadata incomplete**.

## Medium-priority cleanup items

### P015 — HedgeAgents

- Current issue: metadata partly verified but performance claims need source-level confirmation.
- Required action:
  - Verify authors and arXiv version.
  - Extract exact experimental setup.
  - Check cost, slippage, turnover, and evaluation period.
- Status: **needs full extraction**.

### P017 — FinGPT

- Current issue: likely correct but should be verified from official arXiv page.
- Required action:
  - Verify title, authors, and abstract.
  - Distinguish FinGPT v1, FinGPT ecosystem, and later FinGPT-related papers.
- Status: **needs source verification**.

### P018 — BloombergGPT

- Current issue: likely correct but should be verified from official arXiv page.
- Required action:
  - Verify author list.
  - Add DOI / arXiv ID.
  - Confirm model size and dataset description.
- Status: **needs source verification**.

## Bibliography quality rule

No paper can be classified as `core literature` until its metadata has:

1. exact title;
2. full author list or verified author truncation rule;
3. year;
4. stable URL;
5. source / venue;
6. version date if arXiv;
7. one-paragraph verified contribution summary;
8. one-paragraph verified limitation summary.

## Next cleanup target

Clean P007-P011 first because they currently contain placeholder authors and would be the easiest points for a reviewer to attack.
