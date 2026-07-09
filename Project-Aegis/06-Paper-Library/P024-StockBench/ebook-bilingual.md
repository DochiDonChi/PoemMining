# P024 Bilingual Ebook — StockBench

## Paper

**StockBench: Can LLM Agents Trade Stocks Profitably In Real-world Markets?**

## How to read

先读中文理解 trading benchmark，再读英文学习如何解释 contamination-free evaluation 和 trading metrics。

Read the Chinese section first to understand trading benchmarks, then use the English section to practice explaining contamination-free evaluation and trading metrics.

---

# Chapter 1 — Why this paper matters

## 中文理解

P024 重要，因为它关注一个很直接的问题：LLM agents 到底能不能在更真实的股票市场环境中交易盈利？但对 Project Aegis 来说，重点不是它能不能赚钱，而是它如何设计 benchmark、如何避免数据污染、如何使用更完整的交易指标。

## English version

P024 matters because it focuses on a direct question: can LLM agents trade stocks profitably in more realistic market environments? For Project Aegis, however, the key issue is not only whether the agents make money, but how the benchmark is designed, how data contamination is avoided, and how trading performance is measured.

## Key vocabulary

| English | 中文 |
|---|---|
| trading benchmark | 交易基准测试 |
| profitable | 有盈利能力的 |
| data contamination | 数据污染 |
| trading metric | 交易指标 |
| market environment | 市场环境 |

---

# Chapter 2 — What problem the authors solve

## 中文理解

作者想解决的问题是：很多 trading-agent 测试可能不够真实，甚至可能被训练数据污染。如果模型已经看过测试期间的数据，结果就会虚高。P024 试图建立一个更真实、更少污染的 benchmark，让我们更严肃地评估 LLM trading agents。

## English version

The authors address the problem that many trading-agent evaluations may not be realistic enough and may suffer from training-data contamination. If a model has already seen data from the test period, its performance may look artificially strong. P024 attempts to build a more realistic and contamination-aware benchmark for evaluating LLM trading agents.

## Key vocabulary

| English | 中文 |
|---|---|
| training-data contamination | 训练数据污染 |
| test period | 测试期间 |
| artificially strong | 虚高的 |
| contamination-aware | 数据污染感知的 |
| evaluation | 评估 |

---

# Chapter 3 — Main idea

## 中文理解

P024 的核心思想是建立 StockBench，用更动态、更接近真实市场的方式测试 LLM agents 的交易能力。它不是只做静态问答，而是让 agent 在多个月的市场环境中连续做交易决策。

## English version

The main idea of P024 is to build StockBench, a benchmark that tests LLM agents’ trading ability in a more dynamic and realistic market setting. Instead of using static question answering, it evaluates agents through multi-month trading decisions.

## Key vocabulary

| English | 中文 |
|---|---|
| dynamic | 动态的 |
| static question answering | 静态问答 |
| multi-month | 多个月的 |
| trading decision | 交易决策 |
| ability | 能力 |

---

# Chapter 4 — Key concepts

## 中文理解

几个概念很重要。Return 是收益率，但不能单独看。Maximum drawdown 是最大回撤，表示最痛苦的亏损区间。Sortino ratio 更关注下行风险。Contamination-free 指测试尽量避免模型提前见过答案或数据。Project Aegis 需要学习这种 evaluation discipline。

## English version

Several concepts are important. Return measures profit, but it is not enough by itself. Maximum drawdown captures the worst peak-to-trough loss. The Sortino ratio focuses more on downside risk. Contamination-free evaluation means trying to prevent the model from having seen the answers or test data in advance. Project Aegis should learn from this evaluation discipline.

## Key vocabulary

| English | 中文 |
|---|---|
| return | 收益率 |
| maximum drawdown | 最大回撤 |
| Sortino ratio | 索提诺比率 |
| downside risk | 下行风险 |
| evaluation discipline | 评估纪律 |

---

# Chapter 5 — Method / system architecture

## 中文理解

P024 可以理解为：构建一个股票交易 benchmark，给 LLM agents 市场信息，让它们在时间推进中做交易决策，然后用收益、回撤、风险调整指标等评估表现。这个框架帮助我们理解 trading-agent evaluation，但它和 research report evaluation 仍然不同。

## English version

P024 can be understood as follows: build a stock-trading benchmark, provide LLM agents with market information, let them make trading decisions over time, and evaluate performance using return, drawdown, and risk-adjusted metrics. This framework helps us understand trading-agent evaluation, but it is still different from research report evaluation.

## Key vocabulary

| English | 中文 |
|---|---|
| risk-adjusted metric | 风险调整指标 |
| over time | 随时间推进 |
| market information | 市场信息 |
| research report evaluation | 研究报告评估 |
| benchmark framework | 基准测试框架 |

---

# Chapter 6 — Data and experiment design

## 中文理解

全文阅读时要重点看：StockBench 如何避免污染？用了哪些股票？测试多长时间？agent 能看到什么信息？有没有交易成本和滑点？有没有和简单策略比较？这些决定它对 Project Aegis 的参考价值。

## English version

When reading the full paper, focus on how StockBench avoids contamination, which stocks are included, how long the evaluation period is, what information agents can observe, whether transaction costs and slippage are included, and whether simple strategy baselines are used. These details determine its value for Project Aegis.

## Key vocabulary

| English | 中文 |
|---|---|
| evaluation period | 评估期间 |
| simple strategy baseline | 简单策略基准 |
| transaction cost | 交易成本 |
| slippage | 滑点 |
| reference value | 参考价值 |

---

# Chapter 7 — Main results

## 中文理解

P024 的主要价值是推动 trading-agent benchmark 更接近真实市场。它提醒我们：AI 金融系统不能只在简单、静态、可能污染的数据上测试。Project Aegis 也应该用类似思路，要求 investment research agent 在真实研究任务和工作流中被评估。

## English version

The main value of P024 is that it pushes trading-agent benchmarks closer to real market conditions. It reminds us that AI financial systems should not be evaluated only on simple, static, or potentially contaminated data. Project Aegis should adopt a similar mindset by evaluating investment research agents in realistic research tasks and workflows.

## Key vocabulary

| English | 中文 |
|---|---|
| real market condition | 真实市场条件 |
| contaminated data | 被污染的数据 |
| realistic research task | 真实研究任务 |
| workflow | 工作流 |
| adopt a mindset | 采用一种思路 |

---

# Chapter 8 — Limitations

## 中文理解

P024 仍然主要是 trading benchmark。它评估的是交易结果，不是研究报告、证据链、估值假设或人类复核。因此，P024 对 Project Aegis 的作用是提供 evaluation discipline，而不是直接回答 investment research agent 是否可信。

## English version

P024 is still mainly a trading benchmark. It evaluates trading results, not research reports, evidence chains, valuation assumptions, or human review. Therefore, its role in Project Aegis is to provide evaluation discipline, not to directly answer whether investment research agents are trustworthy.

## Key vocabulary

| English | 中文 |
|---|---|
| evidence chain | 证据链 |
| valuation assumption | 估值假设 |
| human review | 人类复核 |
| trustworthy | 可信的 |
| trading result | 交易结果 |

---

# Chapter 9 — Project Aegis relevance

## 中文理解

P024 对 Project Aegis 的启发是：benchmark 必须防止污染，必须接近真实任务，必须使用多维度指标。未来我们可以把这个逻辑转移到 research agent：不能只看报告写得好不好，还要看事实是否正确、证据是否充分、风险是否完整、结论是否可审查。

## English version

P024 inspires Project Aegis by showing that benchmarks should avoid contamination, approximate realistic tasks, and use multidimensional metrics. In future research-agent evaluation, we should not only judge whether a report sounds good. We should also test whether facts are correct, evidence is sufficient, risk discussion is complete, and conclusions are reviewable.

## Key vocabulary

| English | 中文 |
|---|---|
| multidimensional metric | 多维度指标 |
| sufficient evidence | 充分证据 |
| risk discussion | 风险讨论 |
| reviewable conclusion | 可审查结论 |
| approximate | 接近 / 模拟 |

---

# Chapter 10 — Supervisor questions

## 中文理解

导师可能会问：StockBench 是否真的 contamination-free？是否包括交易成本？是否测试多个市场阶段？是否和简单 baseline 比较？这个 benchmark 的设计如何启发 investment research agent benchmark？它和 P022 有什么区别？

## English version

A supervisor may ask: Is StockBench truly contamination-free? Does it include transaction costs? Does it test multiple market regimes? Does it compare with simple baselines? How can this benchmark design inspire investment research agent benchmarks? How is it different from P022?

## Key vocabulary

| English | 中文 |
|---|---|
| market regime | 市场环境 / 市场状态 |
| truly | 真正地 |
| inspire | 启发 |
| compare with | 与……比较 |
| benchmark design | 基准测试设计 |

---

# Chapter 11 — What to read next

## 中文理解

读完 P024 后，可以读 P026 TrustTrade。P024 讲 benchmark，P026 更强调 trust、consensus、misinformation 和 risk-aware behavior。

## English version

After P024, read P026 TrustTrade. P024 focuses on benchmarks, while P026 focuses more on trust, consensus, misinformation, and risk-aware behavior.

# Reading status

- Bilingual mobile ebook: draft complete
- Full-text extraction: pending
