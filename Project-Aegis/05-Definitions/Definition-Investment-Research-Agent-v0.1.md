# Definition: Investment Research Agent v0.1

## Purpose

This file defines what Project Aegis means by an investment research agent. The purpose is to reduce ambiguity when comparing financial QA systems, financial language models, research assistants, and agentic finance systems.

## Working definition

An investment research agent is an AI agent system that supports or produces investment research artifacts by collecting financial evidence, reasoning over company, macro, valuation, risk, or portfolio information, and generating a research output such as an analyst-style report, investment thesis, evidence memo, risk review, or decision-support note.

The system does not need to perform direct market execution. The primary output is a research artifact or decision-support artifact.

## Minimum criteria

A system should satisfy at least four of the following six criteria to be coded as an investment research agent:

1. Evidence gathering: it retrieves, ingests, or processes financial evidence such as filings, earnings calls, news, market data, macro data, or research notes.
2. Financial reasoning: it reasons over fundamentals, valuation, macro drivers, sentiment, risk, or portfolio context.
3. Research artifact generation: it produces a thesis, analyst-style report, memo, recommendation note, evidence summary, or valuation analysis.
4. Multi-step workflow: it goes beyond single-turn question answering by using a structured workflow, tools, planning, memory, debate, or role-specialized agents.
5. Decision support: it supports human or institutional investment decision-making rather than only producing a standalone factual answer.
6. Traceability potential: it contains, or clearly requires, a mechanism for tracing claims back to evidence, tools, data sources, or reasoning steps.

## Boundary with related categories

### Financial QA agent

A financial QA agent answers finance questions. If it only returns answers without a research artifact or thesis-level reasoning, it should be coded as a financial QA agent rather than an investment research agent.

### Trading agent

A trading agent primarily outputs market actions, allocation changes, or position decisions. It may contain research-like components, but if the main output is an action rather than a research artifact, it should be coded as a trading agent.

### Portfolio optimization model

A portfolio optimization model converts expected returns, risks, or constraints into allocations. If it lacks evidence retrieval, thesis generation, agentic workflow, or research artifacts, it should not be coded as an investment research agent.

### Financial LLM infrastructure

A financial LLM is infrastructure. It becomes part of an investment research agent only when embedded in an agentic workflow that produces research artifacts or decision-support outputs.

## Current database examples

### Likely investment research agent or equity research agent

- P016 FinRobot Equity Research: likely qualifies because it targets equity research, valuation, risk assessment, and thesis/report generation.

### Benchmark for research tasks

- P013 Finance Agent Benchmark: evaluates finance research tasks, but the benchmark itself is not necessarily an investment research agent.

### Trading-agent literature

- P004 TradingAgents: primarily a multi-agent trading framework, although it uses analyst-like roles.
- P006 FinMem: primarily a memory-based trading agent.
- P001 Agentic Trading: survey of trading-agent literature.

## Coding labels

Use these labels when coding papers:

- financial_llm_infrastructure
- financial_qa_agent
- trading_agent
- equity_research_agent
- investment_research_agent
- portfolio_risk_agent
- benchmark_evaluation_framework
- governance_policy_framework
- general_agent_theory

A paper may receive one primary label and one secondary label.

## Reviewer challenge

A reviewer may argue that investment research agent is an invented category. Project Aegis should respond by showing that the category is useful because it captures systems whose primary output is a research artifact used in investment decision-making, rather than a direct market action.

## Status

Version: v0.1

Status: working definition. Needs testing against at least 20 coded papers before being treated as stable.
