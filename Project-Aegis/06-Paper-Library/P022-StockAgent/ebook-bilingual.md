# P022 Bilingual Ebook — StockAgent

## Paper

**When AI Meets Finance (StockAgent): Large Language Model-based Stock Trading in Simulated Real-world Environments**

## How to read

先读中文理解 trading simulation，再读英文学习如何解释 simulated real-world financial environments。

Read the Chinese section first to understand trading simulation, then use the English section to practice explaining simulated real-world financial environments.

---

# Chapter 1 — Why this paper matters

## 中文理解

P022 重要，因为它研究如何在更接近真实市场的模拟环境中测试 LLM trading agents。很多 trading-agent 论文最大的问题是测试环境太干净，可能没有真实市场的复杂性。StockAgent 这类论文帮助我们理解：如果要评估金融 agent，就必须认真设计 market environment。

## English version

P022 matters because it studies how to test LLM trading agents in simulated environments that are closer to real-world markets. A major weakness of many trading-agent papers is that their evaluation environments may be too clean and may not capture real market complexity. Papers like StockAgent help us understand that financial-agent evaluation requires careful market-environment design.

## Key vocabulary

| English | 中文 |
|---|---|
| simulated environment | 模拟环境 |
| real-world market | 真实市场 |
| market complexity | 市场复杂性 |
| evaluation environment | 评估环境 |
| trading agent | 交易智能体 |

---

# Chapter 2 — What problem the authors solve

## 中文理解

作者想解决的问题是：LLM trading agent 在普通 benchmark 里表现好，不代表它在更真实的市场环境中也可靠。金融市场有噪音、延迟、信息不完整、交易摩擦和行为反馈。P022 试图用模拟真实环境的方法，让 agent evaluation 更接近现实。

## English version

The authors address the problem that strong performance in a simple benchmark does not mean an LLM trading agent is reliable in a more realistic market environment. Financial markets contain noise, delay, incomplete information, trading frictions, and behavioral feedback. P022 attempts to make agent evaluation more realistic through simulated real-world environments.

## Key vocabulary

| English | 中文 |
|---|---|
| noise | 噪音 |
| delay | 延迟 |
| incomplete information | 不完整信息 |
| trading friction | 交易摩擦 |
| behavioral feedback | 行为反馈 |

---

# Chapter 3 — Main idea

## 中文理解

P022 的核心思想是建立 StockAgent，用模拟真实市场的方式观察 LLM agents 的交易行为。它的价值不是直接证明 agent 可以赚钱，而是帮助我们思考：什么样的测试环境更适合评估 trading agents？

## English version

The main idea of P022 is to build StockAgent and observe LLM agents’ trading behavior in simulated real-world market environments. Its value is not simply to prove that agents can make money, but to help us think about what type of testing environment is appropriate for evaluating trading agents.

## Key vocabulary

| English | 中文 |
|---|---|
| observe behavior | 观察行为 |
| testing environment | 测试环境 |
| appropriate | 合适的 |
| evaluate | 评估 |
| make money | 盈利 |

---

# Chapter 4 — Key concepts

## 中文理解

几个概念很重要。第一是 market simulation，即模拟市场环境。第二是 agent behavior，即观察 agent 在不同信息和价格变化下如何行动。第三是 test-set leakage，也就是模型可能已经在训练中见过测试数据，导致结果虚高。第四是 realism，即测试环境和真实市场的接近程度。

## English version

Several concepts are important. The first is market simulation, which means creating a simulated market environment. The second is agent behavior, meaning how agents act under changing information and prices. The third is test-set leakage, where a model may have already seen test data during training, making results look artificially strong. The fourth is realism, or how close the evaluation environment is to real markets.

## Key vocabulary

| English | 中文 |
|---|---|
| market simulation | 市场模拟 |
| agent behavior | 智能体行为 |
| test-set leakage | 测试集泄漏 |
| realism | 真实程度 |
| artificially strong | 虚高的 |

---

# Chapter 5 — Method / system architecture

## 中文理解

可以把 P022 理解成：市场数据和模拟环境输入系统，LLM agents 在环境中观察信息、做判断、执行交易动作，然后系统记录表现和行为。这个框架和 Project Aegis 有关系，但 Project Aegis 关注的不只是交易动作，而是研究报告、证据链、风险分析和人类复核。

## English version

P022 can be understood as follows: market data and a simulated environment are provided to the system; LLM agents observe information, make judgments, and take trading actions; the system then records performance and behavior. This framework is related to Project Aegis, but Project Aegis focuses not only on trading actions, but also on research reports, evidence chains, risk analysis, and human review.

## Key vocabulary

| English | 中文 |
|---|---|
| trading action | 交易动作 |
| record performance | 记录表现 |
| evidence chain | 证据链 |
| human review | 人类复核 |
| risk analysis | 风险分析 |

---

# Chapter 6 — Data and experiment design

## 中文理解

全文阅读时要重点看：模拟市场如何构建？用了哪些股票和时间段？agent 可以看到什么信息？有没有交易成本？有没有滑点？有没有避免未来数据泄露？有没有和简单策略比较？这些决定 P022 的可信度。

## English version

When reading the full paper, focus on how the simulated market is built, which stocks and time periods are used, what information the agent can observe, whether transaction costs are included, whether slippage is modeled, whether future-data leakage is avoided, and whether simple strategy baselines are included. These details determine the credibility of P022.

## Key vocabulary

| English | 中文 |
|---|---|
| future-data leakage | 未来数据泄漏 |
| simple strategy baseline | 简单策略基准 |
| credibility | 可信度 |
| time period | 时间区间 |
| slippage | 滑点 |

---

# Chapter 7 — Main results

## 中文理解

P022 的主要价值是把 trading-agent evaluation 推向更真实的模拟环境。它提醒我们：如果一个 agent 只在简单 benchmark 上表现好，不足以证明它可以在真实市场中工作。Project Aegis 可以借鉴这种思想，要求 investment research agent 也必须在更真实的研究工作流中被评估。

## English version

The main value of P022 is that it pushes trading-agent evaluation toward more realistic simulation environments. It reminds us that good performance in a simple benchmark is not enough to prove that an agent can work in real markets. Project Aegis can borrow this idea by requiring investment research agents to be evaluated in more realistic research workflows.

## Key vocabulary

| English | 中文 |
|---|---|
| realistic simulation | 真实感模拟 |
| work in real markets | 在真实市场中运作 |
| borrow this idea | 借鉴这个思想 |
| research workflow | 研究工作流 |
| benchmark | 基准测试 |

---

# Chapter 8 — Limitations

## 中文理解

P022 仍然是 trading-agent paper，不是 investment research agent paper。它主要评估交易行为，不是研究报告质量。模拟环境也不等于真实市场，所以不能过度声称它证明了 agent 的真实可用性。

## English version

P022 is still a trading-agent paper, not an investment research agent paper. It mainly evaluates trading behavior rather than research report quality. A simulated environment is also not the same as a real market, so we should not overclaim that it proves real-world agent usefulness.

## Key vocabulary

| English | 中文 |
|---|---|
| research report quality | 研究报告质量 |
| overclaim | 过度声称 |
| real-world usefulness | 真实世界可用性 |
| simulation | 模拟 |
| limitation | 局限 |

---

# Chapter 9 — Project Aegis relevance

## 中文理解

P022 对 Project Aegis 的启发是：评估环境很重要。未来我们不能只让 investment research agent 回答几个问题，而应该让它在完整 workflow 中工作，例如读文件、提取证据、生成 thesis、接受风险复核、修改报告。这才更接近真实投资研究。

## English version

P022 inspires Project Aegis by showing that the evaluation environment matters. In the future, we should not evaluate investment research agents only by asking a few questions. We should test them in complete workflows: reading documents, extracting evidence, generating theses, undergoing risk review, and revising reports. This is closer to real investment research.

## Key vocabulary

| English | 中文 |
|---|---|
| complete workflow | 完整工作流 |
| extract evidence | 提取证据 |
| generate thesis | 生成论点 |
| risk review | 风险复核 |
| revise report | 修改报告 |

---

# Chapter 10 — Supervisor questions

## 中文理解

导师可能会问：P022 的模拟环境是否足够真实？是否控制测试集泄漏？有没有交易成本？有没有和简单策略比较？模拟结果能不能代表真实市场？它和 Project Aegis 的 investment research workflow 有什么关系？

## English version

A supervisor may ask: Is P022’s simulated environment realistic enough? Does it control for test-set leakage? Are transaction costs included? Is it compared with simple strategies? Can simulation results represent real markets? How is it related to Project Aegis’s investment research workflow?

## Key vocabulary

| English | 中文 |
|---|---|
| realistic enough | 足够真实 |
| control for | 控制 / 排除 |
| represent | 代表 |
| simple strategy | 简单策略 |
| related to | 与……相关 |

---

# Chapter 11 — What to read next

## 中文理解

下一篇读 P024 StockBench。P022 讲模拟环境，P024 更偏 trading benchmark，可以帮助你继续理解 trading-agent evaluation 的设计问题。

## English version

Read P024 StockBench next. P022 focuses on simulated environments, while P024 focuses more on trading benchmarks. Together, they help you understand the design problems in trading-agent evaluation.

# Reading status

- Bilingual mobile ebook: draft complete
- Full-text extraction: pending
