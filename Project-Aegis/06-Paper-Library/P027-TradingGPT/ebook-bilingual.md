# P027 Bilingual Ebook — TradingGPT

## Paper

**TradingGPT: Multi-Agent System with Layered Memory and Distinct Characters for Enhanced Financial Trading Performance**

## How to read

先读中文理解 layered memory 和 character design，再读英文学习如何解释 memory-agent lineage。

Read the Chinese section first to understand layered memory and character design, then use the English section to practice explaining the memory-agent lineage.

---

# Chapter 1 — Why this paper matters

## 中文理解

P027 重要，因为它是 memory-based multi-agent trading 这条线的一篇早期候选论文。它和 P006 FinMem 有关联，可以帮助 Project Aegis 理解金融 agent 里面的 memory 和 character design 是如何发展出来的。

## English version

P027 matters because it is an early candidate paper in the memory-based multi-agent trading line of research. It is related to P006 FinMem and helps Project Aegis understand how memory and character design developed within financial-agent systems.

## Key vocabulary

| English | 中文 |
|---|---|
| memory-based | 基于记忆的 |
| character design | 角色 / 性格设计 |
| lineage | 发展脉络 |
| financial-agent system | 金融智能体系统 |
| early candidate | 早期候选 |

---

# Chapter 2 — What problem the authors solve

## 中文理解

作者想解决的问题是：金融市场不是一次性决策环境。agent 如果没有记忆，就很难利用过去的信息、错误和市场经验。P027 尝试用 layered memory 和不同 character 的 agents 来增强交易表现。

## English version

The authors address the problem that financial markets are not one-shot decision environments. Without memory, agents may struggle to use past information, mistakes, and market experience. P027 attempts to use layered memory and agents with distinct characters to improve trading performance.

## Key vocabulary

| English | 中文 |
|---|---|
| one-shot decision | 一次性决策 |
| market experience | 市场经验 |
| past information | 过去信息 |
| trading performance | 交易表现 |
| distinct character | 不同角色 / 性格 |

---

# Chapter 3 — Main idea

## 中文理解

P027 的核心思想是：用多个 agent，加上 layered memory 和不同 character，让系统可以从过去经验中学习，并产生更丰富的交易判断。它的价值在于提示我们：未来 investment research agent 也可能需要不同分析师角色和长期 research memory。

## English version

The main idea of P027 is to use multiple agents, layered memory, and distinct characters so the system can learn from past experience and produce richer trading judgments. Its value is that it suggests future investment research agents may also need different analyst roles and long-term research memory.

## Key vocabulary

| English | 中文 |
|---|---|
| richer judgment | 更丰富的判断 |
| past experience | 过去经验 |
| analyst role | 分析师角色 |
| long-term research memory | 长期研究记忆 |
| multiple agents | 多个智能体 |

---

# Chapter 4 — Key concepts

## 中文理解

Layered memory 是分层记忆，不是把所有信息混在一起。Distinct characters 是让 agents 有不同风格或角色。Project Aegis 关心的是：这些设计是否真的提高推理质量，还是只是增加文本多样性？这些 memory 是否可追踪、可审计、可更新？

## English version

Layered memory means organizing memory into layers rather than mixing all information together. Distinct characters means giving agents different styles or roles. Project Aegis is interested in whether these designs truly improve reasoning quality or merely increase textual diversity. It also asks whether such memory is traceable, auditable, and updatable.

## Key vocabulary

| English | 中文 |
|---|---|
| textual diversity | 文本多样性 |
| reasoning quality | 推理质量 |
| traceable | 可追踪的 |
| auditable | 可审计的 |
| updatable | 可更新的 |

---

# Chapter 5 — Method / system architecture

## 中文理解

可以把 P027 理解为：市场信息进入多个有不同 character 的 agents，每个 agent 结合 layered memory 形成判断，系统再综合这些判断形成交易决策。Project Aegis 可以把这个架构改造成：不同 research agents 结合 thesis memory、evidence memory 和 risk memory 生成研究报告。

## English version

P027 can be understood as follows: market information enters multiple agents with different characters; each agent uses layered memory to form a judgment; the system combines these judgments into trading decisions. Project Aegis can adapt this architecture so different research agents use thesis memory, evidence memory, and risk memory to generate research reports.

## Key vocabulary

| English | 中文 |
|---|---|
| combine judgments | 综合判断 |
| thesis memory | 论点记忆 |
| evidence memory | 证据记忆 |
| risk memory | 风险记忆 |
| generate reports | 生成报告 |

---

# Chapter 6 — Data and experiment design

## 中文理解

全文阅读时要重点看：memory 分几层？character 如何定义？不同 agent 如何互动？有没有和无 memory 或无 character 的 baseline 比较？有没有交易成本？结果是否可复现？这些决定 P027 是否只是概念演示，还是有严谨实证支持。

## English version

When reading the full text, focus on how many memory layers are defined, how characters are defined, how agents interact, whether there are baselines without memory or without character design, whether transaction costs are included, and whether the results are reproducible. These details determine whether P027 is only a conceptual demonstration or has rigorous empirical support.

## Key vocabulary

| English | 中文 |
|---|---|
| baseline | 基准对照 |
| conceptual demonstration | 概念演示 |
| empirical support | 实证支持 |
| reproducible | 可复现的 |
| agent interaction | 智能体互动 |

---

# Chapter 7 — Main results

## 中文理解

P027 的潜在价值是补充 P006：它说明 memory 和 character design 在金融 agent 早期研究中已经出现。它可以帮助 Project Aegis 建立 memory-agent 发展脉络，但还不能证明 memory-based agents 已经可信。

## English version

The potential value of P027 is that it complements P006 by showing that memory and character design already appeared in early financial-agent research. It helps Project Aegis build the lineage of memory-based agents, but it does not prove that memory-based agents are already trustworthy.

## Key vocabulary

| English | 中文 |
|---|---|
| complement | 补充 |
| appear | 出现 |
| trustworthy | 可信的 |
| memory-based agent | 基于记忆的智能体 |
| research lineage | 研究脉络 |

---

# Chapter 8 — Limitations

## 中文理解

P027 仍然是 trading-focused，不是 investment research-focused。它主要看交易表现，不是研究报告质量、证据链或审计能力。Project Aegis 不能直接把它当成 investment research memory 已经解决的证据。

## English version

P027 is still trading-focused, not investment-research-focused. It mainly examines trading performance rather than research report quality, evidence chains, or auditability. Project Aegis should not treat it as evidence that investment research memory has already been solved.

## Key vocabulary

| English | 中文 |
|---|---|
| trading-focused | 以交易为中心 |
| research report quality | 研究报告质量 |
| evidence chain | 证据链 |
| auditability | 可审计性 |
| solved | 已解决 |

---

# Chapter 9 — Project Aegis relevance

## 中文理解

P027 对 Project Aegis 的启发是：未来 research agent 可能需要多种 memory，例如 thesis memory、evidence memory、mistake memory、regime memory 和 reviewer feedback memory。关键不是有没有 memory，而是 memory 是否可信、可追踪、可更新、可删除。

## English version

P027 inspires Project Aegis to think about multiple forms of memory for research agents, such as thesis memory, evidence memory, mistake memory, regime memory, and reviewer-feedback memory. The key question is not whether memory exists, but whether memory is reliable, traceable, updatable, and deletable.

## Key vocabulary

| English | 中文 |
|---|---|
| mistake memory | 错误记忆 |
| regime memory | 市场状态记忆 |
| reviewer feedback memory | 复核者反馈记忆 |
| reliable | 可靠的 |
| deletable | 可删除的 |

---

# Chapter 10 — Supervisor questions

## 中文理解

导师可能会问：P027 和 P006 有什么区别？character design 是否有科学意义？memory 是否能追溯来源？结果是否可复现？这种 trading memory 如何转化成 investment research memory？

## English version

A supervisor may ask: How is P027 different from P006? Is character design scientifically meaningful? Can memory be traced to sources? Are the results reproducible? How can trading memory be transformed into investment research memory?

## Key vocabulary

| English | 中文 |
|---|---|
| scientifically meaningful | 有科学意义的 |
| source tracing | 来源追踪 |
| transform | 转化 |
| investment research memory | 投资研究记忆 |
| difference | 区别 |

---

# Chapter 11 — What to read next

## 中文理解

读完 P027 后，Search-Round-02A 的手机双语阅读层已经完整。下一步更重要的不是继续扩展阅读层，而是开始 P001 或 P025 的全文级精读。

## English version

After P027, the mobile bilingual reading layer for Search-Round-02A is complete. The next important step is not further expansion of the reading layer, but full-text guided reading of P001 or P025.

# Reading status

- Bilingual mobile ebook: draft complete
- Full-text extraction: pending
