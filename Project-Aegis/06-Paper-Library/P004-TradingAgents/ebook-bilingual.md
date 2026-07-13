# P004 Bilingual Ebook — TradingAgents

## Paper

**TradingAgents: Multi-Agents LLM Financial Trading Framework**

## How to read

先读中文理解 multi-agent trading 的结构，再读英文学习如何解释 role-specialized financial agents。

Read the Chinese section first to understand the structure of multi-agent trading, then use the English section to practice explaining role-specialized financial agents.

---

# Chapter 1 — Why this paper matters

## 中文理解

P004 重要，因为它是一个很清楚的 multi-agent trading framework。它不像单一模型直接预测涨跌，而是把金融交易流程拆成多个角色，例如基本面分析、情绪分析、技术分析、牛方研究、熊方研究、风险管理和交易决策。这对 Project Aegis 有启发，因为未来 investment research agent 也需要多角色协作。

## English version

P004 matters because it is a clear multi-agent trading framework. Instead of using a single model to predict price movement directly, it decomposes the financial trading process into multiple roles, such as fundamental analysis, sentiment analysis, technical analysis, bull-side research, bear-side research, risk management, and trading decisions. This is useful for Project Aegis because future investment research agents may also require role-based collaboration.

## Key vocabulary

| English | 中文 |
|---|---|
| multi-agent framework | 多智能体框架 |
| role specialization | 角色专业化 |
| fundamental analysis | 基本面分析 |
| sentiment analysis | 情绪分析 |
| risk management | 风险管理 |

---

# Chapter 2 — What problem the authors solve

## 中文理解

作者想解决的问题是：单一 agent 很难同时处理所有金融信息，也很难模拟真实交易团队的协作。真实金融机构通常不是一个人做所有决定，而是不同角色分别分析数据、讨论观点、评估风险，最后形成决策。P004 尝试用多个 LLM agents 模拟这种协作。

## English version

The authors address the problem that a single agent may struggle to process all financial information and may not reflect the collaborative nature of real trading teams. In real financial institutions, decisions are usually not made by one person alone. Different roles analyze data, debate views, evaluate risk, and contribute to final decisions. P004 attempts to simulate this collaboration using multiple LLM agents.

## Key vocabulary

| English | 中文 |
|---|---|
| collaboration | 协作 |
| trading team | 交易团队 |
| debate | 辩论 |
| final decision | 最终决策 |
| simulate | 模拟 |

---

# Chapter 3 — Main idea

## 中文理解

P004 的核心思想是：把 trading decision 拆成多个 agent 任务。不同 agent 分析不同信息，然后通过讨论或综合，把结果交给 trader 或 risk manager 形成最终交易动作。这种设计让 agent 系统更像一个小型 trading firm。

## English version

The main idea of P004 is to decompose trading decisions into multiple agent tasks. Different agents analyze different types of information, then their outputs are discussed or synthesized and passed to traders or risk managers to form final trading actions. This design makes the agent system resemble a small trading firm.

## Key vocabulary

| English | 中文 |
|---|---|
| decompose | 拆解 |
| trading decision | 交易决策 |
| synthesize | 综合 |
| trading firm | 交易公司 / 交易团队 |
| final action | 最终动作 |

---

# Chapter 4 — Key concepts

## 中文理解

最重要的概念是 role-specialized agents。每个 agent 有不同任务：基本面 agent 看公司和财务，情绪 agent 看新闻和市场情绪，技术 agent 看价格和指标，牛方和熊方 agent 提出正反观点，风险管理 agent 评估风险。这种结构让系统更容易模拟真实金融讨论。

## English version

The key concept is role-specialized agents. Each agent has a different task: the fundamental agent examines company and financial information, the sentiment agent analyzes news and market sentiment, the technical agent studies prices and indicators, bull and bear agents provide opposing views, and risk-management agents evaluate risk. This structure helps the system simulate real financial discussion.

## Key vocabulary

| English | 中文 |
|---|---|
| bull case | 看多观点 |
| bear case | 看空观点 |
| opposing views | 对立观点 |
| technical indicator | 技术指标 |
| market sentiment | 市场情绪 |

---

# Chapter 5 — Method / system architecture

## 中文理解

可以把 P004 的架构理解为：市场和公司信息进入不同 analyst agents，然后进入 bull/bear debate，再经过 risk management，最后由 trader agent 形成买入、卖出或持有决策。这个流程对 Project Aegis 有参考价值，但 Project Aegis 的最终输出应更偏 research artifact，而不是直接 trade。

## English version

The architecture can be understood as follows: market and company information flows into different analyst agents, then into bull/bear debate, then through risk management, and finally to a trader agent that produces buy, sell, or hold decisions. This workflow is useful for Project Aegis, but the final output of Project Aegis should focus more on research artifacts than direct trades.

## Key vocabulary

| English | 中文 |
|---|---|
| buy/sell/hold | 买入 / 卖出 / 持有 |
| research artifact | 研究产物 |
| workflow | 工作流程 |
| analyst agent | 分析师智能体 |
| trader agent | 交易员智能体 |

---

# Chapter 6 — Data and experiment design

## 中文理解

全文阅读时要重点检查：用了哪些市场和股票？测试时间段是什么？有没有交易成本？有没有滑点？有没有明确 execution timing？有没有跟简单 baseline 比较？如果这些不清楚，交易表现就不能直接被信任。

## English version

When reading the full text, focus on which markets and stocks are used, what testing period is selected, whether transaction costs are included, whether slippage is considered, whether execution timing is clearly defined, and whether the system is compared with simple baselines. If these details are unclear, the trading performance should not be trusted too strongly.

## Key vocabulary

| English | 中文 |
|---|---|
| testing period | 测试区间 |
| transaction cost | 交易成本 |
| slippage | 滑点 |
| execution timing | 执行时点 |
| baseline | 基准模型 / 对照组 |

---

# Chapter 7 — Main results

## 中文理解

P004 的重要结果不是简单证明 multi-agent 一定能赚钱，而是展示了 multi-agent role specialization 在金融场景中的一种可行设计。它让我们看到：金融 agent 不一定是一个模型，而可以是一组有角色分工的 agents。

## English version

The important result of P004 is not simply that multi-agent systems can make money. Its value is that it demonstrates a possible design for role-specialized multi-agent systems in finance. It shows that a financial agent system does not have to be a single model; it can be a group of agents with different roles.

## Key vocabulary

| English | 中文 |
|---|---|
| role-specialized | 角色专业化的 |
| possible design | 可能设计 |
| demonstrate | 展示 |
| financial setting | 金融场景 |
| group of agents | 一组智能体 |

---

# Chapter 8 — Limitations

## 中文理解

P004 的限制在于它主要是 trading agent，不是 investment research agent。它的最终目标是交易表现，而不是生成可审计的研究报告或 investment thesis。另外，role-playing agents 看起来像分析师，但不一定真的有严谨的证据链。

## English version

The limitation of P004 is that it is mainly a trading-agent paper, not an investment research agent paper. Its final goal is trading performance rather than auditable research reports or investment theses. In addition, role-playing agents may look like analysts, but they do not necessarily provide rigorous evidence chains.

## Key vocabulary

| English | 中文 |
|---|---|
| trading performance | 交易表现 |
| investment thesis | 投资论点 |
| evidence chain | 证据链 |
| role-playing agent | 角色扮演智能体 |
| rigorous | 严谨的 |

---

# Chapter 9 — Project Aegis relevance

## 中文理解

P004 对 Project Aegis 的价值是架构启发，而不是最终答案。它告诉我们，多角色 agent 在金融中是有意义的。但 Project Aegis 要把这种结构从 trading decision 延伸到 investment research workflow，例如 company analyst、macro analyst、valuation analyst、risk reviewer、compliance reviewer。

## English version

The value of P004 for Project Aegis is architectural inspiration, not a final answer. It shows that multi-role agents are meaningful in finance. Project Aegis should extend this structure from trading decisions to investment research workflows, such as company analysts, macro analysts, valuation analysts, risk reviewers, and compliance reviewers.

## Key vocabulary

| English | 中文 |
|---|---|
| architectural inspiration | 架构启发 |
| company analyst | 公司分析师 |
| macro analyst | 宏观分析师 |
| valuation analyst | 估值分析师 |
| compliance reviewer | 合规复核者 |

---

# Chapter 10 — Supervisor questions

## 中文理解

导师可能会问：P004 的 agent 是真的在推理，还是只是在生成看起来合理的文本？bull/bear debate 是否真的提高决策质量？risk management 是定量风控，还是只是角色描述？有没有交易成本？有没有复现材料？它和 Project Aegis 的 investment research agent 有什么关系？

## English version

A supervisor may ask: Are P004’s agents actually reasoning, or merely generating plausible text? Does bull/bear debate truly improve decision quality? Is risk management quantitative, or only a role description? Are transaction costs included? Are reproducibility materials available? How is P004 related to Project Aegis’s investment research agent direction?

## Key vocabulary

| English | 中文 |
|---|---|
| plausible text | 看似合理的文本 |
| decision quality | 决策质量 |
| quantitative risk control | 定量风控 |
| reproducibility material | 复现材料 |
| role description | 角色描述 |

---

# Chapter 11 — What to read next

## 中文理解

下一篇读 P006。P004 讲多智能体角色分工，P006 讲 memory-based financial agent。两篇结合起来，可以帮你理解未来 investment research agent 为什么需要多角色和长期记忆。

## English version

Read P006 next. P004 explains multi-agent role specialization, while P006 explains memory-based financial agents. Together, they help you understand why future investment research agents may need both multiple roles and long-term memory.

# Reading status

- Bilingual mobile ebook: draft complete
- Full-text extraction: pending
