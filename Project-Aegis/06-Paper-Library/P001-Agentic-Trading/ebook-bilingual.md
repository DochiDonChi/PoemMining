# P001 Bilingual Ebook — Agentic Trading

## Paper

**Agentic Trading: When LLM Agents Meet Financial Markets**

## How to read

先读中文，再读英文。中文帮助理解，英文帮助你以后跟导师、面试官或研究伙伴解释。

Read the Chinese section first to build intuition, then read the English section to learn academic expression.

---

# Chapter 1 — Why this paper matters

## 中文理解

这篇论文应该第一篇读，因为它帮你看清楚整个 LLM trading agent 领域的问题。大部分人一进入这个领域会问：AI 能不能炒股赚钱？但这篇论文问的是更重要的问题：现在这些 LLM trading agent 论文的评估方法可靠吗？结果之间可以比较吗？这正好支持 Project Aegis 的核心方向：我们不是要做另一个 trading bot，而是要研究金融智能体如何做到可复现、可审计、风险可控。

## English version

This paper should be read first because it maps the broader LLM trading-agent field. Most people enter this topic by asking whether AI can trade profitably. This paper asks a deeper question: are current LLM trading-agent studies evaluated in a reliable and comparable way? This is central to Project Aegis because the goal is not to build another trading bot, but to understand how financial agents can become reproducible, auditable, and risk-aware.

## Key vocabulary

| English | 中文 |
|---|---|
| trading agent | 交易智能体 |
| reproducible | 可复现的 |
| auditable | 可审计的 |
| comparable | 可比较的 |
| risk-aware | 风险感知的 |

---

# Chapter 2 — What problem the authors solve

## 中文理解

作者关心的问题是：很多 LLM trading agent 论文报告了很好的收益，但这些收益是否可靠？不同论文可能使用不同市场、不同时间段、不同交易成本假设、不同模型版本、不同 prompt、不同执行时点。如果这些条件不清楚，所谓的高收益很可能没有可比性，也很难复现。

## English version

The authors focus on whether reported LLM trading-agent performance is methodologically reliable. Different studies may use different markets, time periods, transaction-cost assumptions, model versions, prompts, and execution-timing rules. If these assumptions are unclear, strong reported returns may not be comparable or reproducible.

## Key vocabulary

| English | 中文 |
|---|---|
| methodology | 方法论 |
| assumption | 假设 |
| transaction cost | 交易成本 |
| execution timing | 执行时点 |
| model version | 模型版本 |

---

# Chapter 3 — Main idea

## 中文理解

这篇论文的核心思想是：LLM trading agent 不能只看收益率，必须看它的研究设计是否严谨。真正重要的是有没有清楚说明数据、交易成本、执行逻辑、测试区间、复现条件。Project Aegis 可以从这里延伸：未来金融 AI 的重点不只是 performance，而是 trustworthiness。

## English version

The core idea is that LLM trading agents should not be judged only by return. They should also be judged by research design, including data setup, transaction costs, execution logic, testing periods, and reproducibility conditions. Project Aegis extends this idea by arguing that the future of financial AI should focus not only on performance, but also on trustworthiness.

## Key vocabulary

| English | 中文 |
|---|---|
| performance | 表现 / 绩效 |
| research design | 研究设计 |
| trustworthiness | 可信度 |
| testing period | 测试区间 |
| evaluation discipline | 评估纪律 |

---

# Chapter 4 — Key concepts

## 中文理解

几个概念很重要。第一，transaction cost，就是交易费用、买卖价差、滑点等成本。第二，survivorship bias，就是只看活下来的股票或资产，忽略已经失败或退市的资产。第三，execution timing，就是模型做决定的时候，是否用了当时还不可能知道的信息。第四，reproducibility，就是别人能不能用同样方法复现你的结果。

## English version

Several concepts are central. Transaction cost includes fees, bid-ask spread, slippage, and other trading frictions. Survivorship bias occurs when failed or delisted assets are ignored. Execution timing asks whether the model uses only information that would have been available at the decision time. Reproducibility asks whether other researchers can repeat the study and obtain comparable results.

## Key vocabulary

| English | 中文 |
|---|---|
| slippage | 滑点 |
| bid-ask spread | 买卖价差 |
| survivorship bias | 幸存者偏差 |
| delisted assets | 退市资产 |
| trading friction | 交易摩擦 |

---

# Chapter 5 — Method / system architecture

## 中文理解

P001 不是一个系统论文，它不是在建一个新的 trading agent。它更像是 review / evidence map，目的是审视已有研究。它的价值在于告诉我们：这个领域的问题不是没有 agent，而是很多 agent 的评估方式还不够严谨。

## English version

P001 is not mainly a system-building paper. It does not primarily propose a new trading agent. It is closer to a review or evidence map. Its value is to show that the field’s problem is not a lack of agents, but the weakness of evaluation practices around those agents.

## Key vocabulary

| English | 中文 |
|---|---|
| review paper | 综述论文 |
| evidence map | 证据地图 |
| evaluation practice | 评估实践 |
| system-building paper | 系统构建论文 |
| field-level | 领域层面 |

---

# Chapter 6 — Data and experiment design

## 中文理解

当前我们记录到的重点是：这篇论文覆盖了大量 LLM trading agent 研究，并特别指出很多研究在交易成本、时间切分、资产池定义、可复现性方面不够清楚。这些数字以后要通过全文表格再核实，不能只靠摘要级记录。

## English version

Our current extraction records that the paper covers a broad set of LLM trading-agent studies and highlights weaknesses in transaction-cost modeling, time-consistent data splits, asset-universe definition, and reproducibility. These numbers must later be verified through full-text table-level extraction, not only abstract-level notes.

## Key vocabulary

| English | 中文 |
|---|---|
| asset universe | 资产池 |
| data split | 数据切分 |
| table-level extraction | 表格级抽取 |
| full-text verification | 全文核实 |
| empirical subset | 实证子集 |

---

# Chapter 7 — Main results

## 中文理解

这篇论文最重要的结论不是「LLM trading agent 没用」，而是「这个领域的评估和复现标准还不够成熟」。这正好支持 Project Aegis：我们应该研究如何让金融 agent 变得可信，而不是只追求更高收益。

## English version

The most important result is not that LLM trading agents are useless. The key finding is that evaluation and reproducibility standards in this field are still immature. This supports Project Aegis: the research focus should be on making financial agents trustworthy, not merely more profitable.

## Key vocabulary

| English | 中文 |
|---|---|
| immature | 不成熟的 |
| standard | 标准 |
| key finding | 关键发现 |
| profitable | 有盈利能力的 |
| trustworthy | 可信的 |

---

# Chapter 8 — Limitations

## 中文理解

P001 主要讨论 trading agent，所以不能直接拿它证明 investment research agent 一定也有同样问题。正确用法是：P001 支持 trading-agent 文献存在复现和评估问题。然后 Project Aegis 再进一步研究这些问题是否也存在于 investment research agent。

## English version

P001 focuses mainly on trading agents, so it should not be used to prove that investment research agents have exactly the same problems. The correct use is to cite P001 as evidence that trading-agent literature has reproducibility and evaluation weaknesses, then investigate whether similar weaknesses appear in investment research agents.

## Key vocabulary

| English | 中文 |
|---|---|
| limitation | 局限性 |
| overclaim | 过度声称 |
| correct use | 正确用法 |
| evidence | 证据 |
| investigate | 研究 / 调查 |

---

# Chapter 9 — Project Aegis relevance

## 中文理解

P001 是 Project Aegis 的方法论支柱之一。它告诉我们，金融 AI 研究不能只看结果，还要看这个结果是怎么来的。Project Aegis 可以把这个逻辑从 trading 扩展到 investment research：AI 生成的研究报告、投资 thesis、风险分析，也必须可追踪、可审计、可复现。

## English version

P001 is one of the methodological pillars of Project Aegis. It shows that financial AI research should not focus only on outcomes, but also on how those outcomes are produced. Project Aegis extends this logic from trading to investment research: AI-generated research reports, investment theses, and risk analyses should also be traceable, auditable, and reproducible.

## Key vocabulary

| English | 中文 |
|---|---|
| methodological pillar | 方法论支柱 |
| traceable | 可追踪的 |
| investment thesis | 投资论点 |
| risk analysis | 风险分析 |
| outcome | 结果 |

---

# Chapter 10 — Supervisor questions

## 中文理解

你读完后要能回答：P001 到底证明了什么？它没有证明什么？为什么交易成本重要？为什么幸存者偏差重要？为什么 LLM agent 的结果很难复现？Project Aegis 如何从 P001 延伸出自己的研究问题？

## English version

After reading this paper, you should be able to answer: What exactly does P001 prove? What does it not prove? Why do transaction costs matter? Why does survivorship bias matter? Why is reproducibility difficult in LLM-agent systems? How does Project Aegis extend P001 into a new research agenda?

## Key vocabulary

| English | 中文 |
|---|---|
| prove | 证明 |
| research agenda | 研究议程 |
| extend | 延伸 |
| supervisor question | 导师问题 |
| defend an argument | 为论点辩护 |

---

# Chapter 11 — What to read next

## 中文理解

下一篇读 P016。P001 让你理解整个 trading-agent 领域的问题，P016 让你看到 agent 如何从 trading 走向 equity research。

## English version

Read P016 next. P001 helps you understand the field-level problems in trading-agent research, while P016 shows how financial agents may move from trading toward equity research.

# Reading status

- Bilingual mobile ebook: draft complete
- Full-text extraction: pending
