# Towards Trustworthy AI Investment Research: A Systematic Review and Research Gap Map of LLM-based Financial Agents

## Abstract

Large Language Models (LLMs) are rapidly moving from passive financial text analysis toward autonomous financial agents capable of information retrieval, reasoning, tool use, portfolio decision support, and trading action generation. Recent studies such as TradingAgents, FinRobot, FinMem, Agent Market Arena, and Agentic Trading show that the field is shifting from single-task prediction to agent-based investment workflows. However, the literature remains fragmented. Existing studies often differ in data sources, market universes, trading assumptions, transaction-cost treatment, evaluation metrics, prompt design, model versions, and reproducibility standards. This review argues that the next major research opportunity is not simply building another trading agent, but developing reproducible, auditable, risk-aware multi-agent investment research systems. We map the current literature into seven research streams: trading agents, investment-management agents, memory-based agents, open-source financial agent platforms, benchmark and evaluation frameworks, systemic-risk studies, and governance-oriented research. We identify major research gaps in reproducibility, auditability, long-term financial memory, investment workflow modeling, risk-first evaluation, human-AI collaboration, and regulatory alignment.

## 1. Introduction

The first wave of AI in finance focused on prediction: using machine learning or deep learning models to forecast returns, classify sentiment, or optimize portfolios. The recent emergence of LLMs has changed the research problem. LLMs are not merely predictive models; they can read documents, retrieve context, reason over heterogeneous information, use tools, generate explanations, and participate in multi-step workflows. This enables a new class of financial agents that may act less like statistical predictors and more like digital analysts, traders, risk managers, or portfolio assistants.

Recent work shows this transition clearly. TradingAgents proposes a multi-agent trading framework inspired by real trading firms, with specialized fundamental, sentiment, technical, risk, and trader agents working together. FinRobot introduces an open-source financial agent platform with specialized financial AI agents, LLM algorithms, DataOps, and LLMOps layers. FinMem proposes a layered memory architecture for LLM-based trading agents, highlighting the importance of memory and character design in financial decision-making. Agent Market Arena introduces a live multi-market benchmark for LLM agents, pushing the field closer to continuous and realistic evaluation.

Despite this progress, the field faces a serious credibility problem. The recent Agentic Trading survey reviews 77 studies and finds that comparable evaluation protocols, execution semantics, and reproducible artifacts remain immediate bottlenecks. This suggests that the field's main bottleneck is no longer simply agent architecture, but trustworthiness.

## 2. Research Question

This review addresses the following question:

**How has the literature on LLM-based financial agents evolved, and what research gaps must be solved before such agents can become credible investment research systems?**

The central argument is that the next high-value research direction is:

**A reproducible, auditable, risk-aware multi-agent framework for autonomous investment research.**

This differs from "AI stock prediction" or "LLM trading." The goal is not only to generate buy/sell signals, but to model the full investment research workflow: hypothesis generation, evidence retrieval, financial reasoning, risk assessment, portfolio implication, human review, and audit trail.

## 3. Literature Landscape

### 3.1 Trading agents

Trading-agent papers focus on systems that directly output trading actions. They often combine news, market data, technical indicators, sentiment signals, and LLM reasoning to produce buy, sell, hold, or portfolio allocation decisions. The main contribution of this stream is to move from static prediction to closed-loop action generation.

### 3.2 Multi-agent financial systems

Multi-agent systems divide financial reasoning into specialized roles: macro analyst, fundamental analyst, sentiment analyst, technical analyst, trader, risk manager, and portfolio manager. This mirrors real financial institutions more closely than single-agent systems. However, multi-agent systems create new risks: coordination failure, inconsistent reasoning, duplicated evidence, groupthink, and hard-to-audit decision paths.

### 3.3 Memory-based agents

Memory-based agents attempt to overcome the short-term nature of prompt-only LLM reasoning. Financial research requires long-term context: previous theses, management credibility, macro regimes, past mistakes, and evolving risk narratives. Existing memory work is promising, but remains narrow compared with the complexity of institutional investment research.

### 3.4 Benchmarks and evaluation

Benchmark papers recognize that static financial QA tests are insufficient. Investment and trading are sequential, uncertain, path-dependent, and sensitive to costs and execution timing. The key research opportunity is to design benchmark protocols that combine returns with risk, robustness, transaction costs, reproducibility, and auditability.

### 3.5 Governance and systemic implications

As AI agents become more capable, the research question expands from "Can one agent trade?" to "What happens when many institutions deploy agents?" The systemic implications include herding, liquidity fragility, market concentration, cyber risk, correlated model behavior, and overreliance on a few AI providers.

## 4. Research Gap Map

### Gap 1: Reproducibility

Many studies do not provide enough information to reproduce results. Missing details include model version, prompt templates, seed control, data split protocol, survivorship bias handling, transaction-cost assumptions, execution timing, and code availability.

### Gap 2: Auditability

Investment agents often produce recommendations without a full audit trail. A credible investment research agent should record what information it used, what evidence supported the thesis, what contrary evidence was considered, which tools were called, and why the final recommendation was made.

### Gap 3: Risk-first evaluation

Many papers still emphasize return, accuracy, or Sharpe ratio. But investment systems should be evaluated on drawdown, turnover, transaction costs, stress periods, regime shifts, liquidity risk, decision consistency, and failure modes.

### Gap 4: Long-term financial memory

Current memory systems remain narrow. A serious investment research agent needs memory across multiple levels: company memory, macro memory, thesis memory, error memory, regime memory, and portfolio memory.

### Gap 5: Investment workflow modeling

Many agents jump from information to trading decision. Real buy-side research is more structured: idea sourcing, hypothesis generation, evidence gathering, valuation, risk review, portfolio construction, compliance review, and post-trade monitoring.

### Gap 6: Human-AI collaboration

Most literature discusses automation, but institutional investment decisions usually require human accountability. The important question is not whether AI replaces the portfolio manager, but how human PMs should review, challenge, override, or learn from agent-generated research.

### Gap 7: Regulatory alignment

Regulators are increasingly concerned about AI-driven financial advice, systemic risk, model concentration, and accountability. Academic research has not yet fully translated these concerns into technical design requirements such as kill switches, approval workflows, evidence logs, model governance, and responsibility assignment.

## 5. Proposed Future Direction

Based on the literature, the most promising research direction is:

**Reproducible and Auditable Multi-Agent Investment Research Systems.**

Such a system should include:

1. specialized agents for macro, company, sentiment, valuation, risk, portfolio, and compliance analysis;
2. structured memory for historical context and prior investment theses;
3. retrieval and citation mechanisms for evidence grounding;
4. standardized benchmark protocols;
5. transaction-cost-aware backtesting;
6. risk-first evaluation;
7. human-in-the-loop review;
8. full audit logs for every recommendation.

This direction is valuable because it addresses the field's most urgent weakness: trust. Without reproducibility and auditability, financial agents may remain impressive demos rather than credible institutional tools.

## 6. Conclusion

The literature on LLM-based financial agents is moving quickly from stock prediction toward agentic investment workflows. TradingAgents, FinRobot, FinMem, Agent Market Arena, and recent surveys show that the field has entered a new phase. However, the strongest research opportunity is not simply building more agents. The real gap is building systems that are reproducible, auditable, risk-aware, and aligned with real investment research practice. This review therefore proposes a research agenda centered on autonomous investment research agents rather than autonomous trading alone. Such a direction has academic value, practical value, and strong relevance for future PhD research in AI, finance, and risk management.

## References to expand

See `paper-database-v0.1.csv` for the initial structured paper list.
