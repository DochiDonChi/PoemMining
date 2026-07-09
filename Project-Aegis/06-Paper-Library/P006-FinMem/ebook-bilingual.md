# P006 Bilingual Ebook — FinMem

## Paper

**FinMem: A Performance-Enhanced LLM Trading Agent with Layered Memory and Character Design**

## How to read

先读中文理解 financial agent 为什么需要 memory，再读英文学习如何解释 layered memory 和 research memory。

Read the Chinese section first to understand why financial agents need memory, then use the English section to practice explaining layered memory and research memory.

---

# Chapter 1 — Why this paper matters

## 中文理解

P006 重要，因为它研究金融智能体的 memory。投资研究不是一次性任务，一个可信的 research agent 需要记得过去的投资 thesis、公司事件、宏观环境、预测错误、风险暴露和之前被否定的想法。P006 虽然是 trading agent 论文，但它给 Project Aegis 提供了 memory 这条基础线。

## English version

P006 matters because it studies memory in financial agents. Investment research is not a one-shot task. A trustworthy research agent needs to remember past investment theses, company events, macro environments, forecast errors, risk exposures, and previously rejected ideas. Although P006 is a trading-agent paper, it provides an important memory foundation for Project Aegis.

## Key vocabulary

| English | 中文 |
|---|---|
| memory | 记忆 |
| investment thesis | 投资论点 |
| macro environment | 宏观环境 |
| forecast error | 预测错误 |
| risk exposure | 风险暴露 |

---

# Chapter 2 — What problem the authors solve

## 中文理解

作者想解决的问题是：LLM agent 如果只依赖当前 prompt，很难持续学习和调整。金融市场是连续变化的，agent 需要记住之前发生过什么、之前判断对错、哪些信息重要、哪些信息过时。P006 用 layered memory 和 character design 来增强金融决策。

## English version

The authors address the problem that an LLM agent relying only on the current prompt may struggle to learn and adapt over time. Financial markets evolve continuously. An agent needs to remember what happened before, whether previous judgments were correct, which information matters, and which information has become outdated. P006 uses layered memory and character design to improve financial decision-making.

## Key vocabulary

| English | 中文 |
|---|---|
| current prompt | 当前提示词 |
| adapt over time | 随时间适应 |
| outdated information | 过时信息 |
| layered memory | 分层记忆 |
| character design | 角色/性格设计 |

---

# Chapter 3 — Main idea

## 中文理解

P006 的核心思想是：给金融 agent 加上分层记忆，让它不是每次从零开始。不同层级的 memory 可以保存不同类型的信息，然后在新的决策中调用。这个思路对 Project Aegis 很重要，因为投资研究 agent 也需要长期研究记忆。

## English version

The main idea of P006 is to give financial agents layered memory so they do not start from zero each time. Different memory layers can store different types of information and be retrieved during new decisions. This idea is important for Project Aegis because investment research agents also need long-term research memory.

## Key vocabulary

| English | 中文 |
|---|---|
| start from zero | 从零开始 |
| memory layer | 记忆层 |
| retrieve | 调取 / 检索 |
| long-term memory | 长期记忆 |
| research memory | 研究记忆 |

---

# Chapter 4 — Key concepts

## 中文理解

几个概念很重要。Layered memory 是把记忆分层，而不是所有信息放在一起。Character design 是给 agent 设定某种交易风格或性格。Decision-making module 是把记忆和当前信息结合起来形成决策。Project Aegis 关心的是：这些 memory 能不能审计、能不能更新、能不能避免 stale belief。

## English version

Several concepts are important. Layered memory means organizing memory into different layers rather than storing all information together. Character design gives the agent a particular trading style or personality. The decision-making module combines memory with current information to form decisions. Project Aegis is especially interested in whether such memory can be audited, updated, and protected from stale beliefs.

## Key vocabulary

| English | 中文 |
|---|---|
| decision-making module | 决策模块 |
| trading style | 交易风格 |
| stale belief | 过时信念 |
| auditable memory | 可审计记忆 |
| update | 更新 |

---

# Chapter 5 — Method / system architecture

## 中文理解

P006 的结构可以理解为：市场信息和新闻进入 agent，agent 通过 memory module 存储和整理信息，再由 decision-making module 形成交易判断。对 Project Aegis 来说，可以把这个结构改造成：公司信息、宏观信息、历史 thesis、错误记录进入 research memory，再支持生成投资报告和风险复核。

## English version

The architecture of P006 can be understood as follows: market information and news enter the agent, the memory module stores and organizes the information, and the decision-making module produces trading judgments. For Project Aegis, this structure can be adapted so that company information, macro information, historical theses, and error records enter research memory and support investment reports and risk reviews.

## Key vocabulary

| English | 中文 |
|---|---|
| memory module | 记忆模块 |
| market information | 市场信息 |
| historical thesis | 历史论点 |
| error record | 错误记录 |
| risk review | 风险复核 |

---

# Chapter 6 — Data and experiment design

## 中文理解

全文阅读时要看：P006 用了什么市场数据？memory 具体分几层？每层存什么？memory 如何更新？有没有交易成本？有没有和无 memory 的 baseline 比较？如果只看收益提升，不看 memory 是否可审计，就还不够支持 Project Aegis。

## English version

When reading the full text, focus on what market data is used, how many memory layers are defined, what each layer stores, how memory is updated, whether transaction costs are included, and whether the system is compared with a no-memory baseline. If the paper only shows better returns without showing whether memory is auditable, it is not enough for Project Aegis.

## Key vocabulary

| English | 中文 |
|---|---|
| no-memory baseline | 无记忆基准 |
| memory update | 记忆更新 |
| transaction cost | 交易成本 |
| market data | 市场数据 |
| compare | 比较 |

---

# Chapter 7 — Main results

## 中文理解

P006 的主要价值不是证明 memory agent 已经可信，而是证明 memory 是金融 agent 的重要设计方向。它让我们看到，如果 agent 要连续处理金融市场，它需要记忆。但 Project Aegis 还要继续追问：这个记忆是否可追踪、可修改、可删除、可审计？

## English version

The main value of P006 is not to prove that memory-based agents are already trustworthy. Its value is to show that memory is an important design direction for financial agents. It suggests that if an agent continuously interacts with financial markets, it needs memory. Project Aegis must then ask whether that memory is traceable, editable, deletable, and auditable.

## Key vocabulary

| English | 中文 |
|---|---|
| design direction | 设计方向 |
| traceable | 可追踪的 |
| editable | 可修改的 |
| deletable | 可删除的 |
| auditable | 可审计的 |

---

# Chapter 8 — Limitations

## 中文理解

P006 的限制是它主要面向 trading decision，不是 investment research artifact。它可能说明 memory 有助于交易表现，但还不能说明 memory 能支持可信投资研究。另外，memory 也有风险：它可能强化旧观点、产生 anchoring bias、保存错误信息、无法忘记过时信息。

## English version

The limitation of P006 is that it mainly targets trading decisions, not investment research artifacts. It may show that memory helps trading performance, but it does not prove that memory supports trustworthy investment research. Memory also creates risks: it may reinforce old views, create anchoring bias, preserve incorrect information, or fail to forget outdated information.

## Key vocabulary

| English | 中文 |
|---|---|
| trading decision | 交易决策 |
| research artifact | 研究产物 |
| anchoring bias | 锚定偏差 |
| incorrect information | 错误信息 |
| forget outdated information | 忘记过时信息 |

---

# Chapter 9 — Project Aegis relevance

## 中文理解

P006 对 Project Aegis 的启发是：未来 investment research agent 应该有 research memory。这个 memory 不只是保存聊天记录，而是保存 thesis、证据、反方观点、预测错误、风险变化和人类 reviewer 的反馈。真正的研究问题是：如何设计可信的 investment research memory？

## English version

P006 inspires Project Aegis to develop the idea of research memory for investment research agents. This memory should not merely store chat history. It should store theses, evidence, opposing views, forecast errors, risk changes, and feedback from human reviewers. The real research question is: how should trustworthy investment research memory be designed?

## Key vocabulary

| English | 中文 |
|---|---|
| research memory | 研究记忆 |
| opposing view | 反方观点 |
| human reviewer | 人类复核者 |
| feedback | 反馈 |
| trustworthy design | 可信设计 |

---

# Chapter 10 — Supervisor questions

## 中文理解

导师可能会问：P006 的 memory 是怎么存的？怎么更新？怎么删除？有没有来源追踪？memory 是否真的提升决策质量，还是只是提升 backtest？memory 会不会造成 anchoring bias？Project Aegis 如何把 trading memory 扩展成 thesis memory？

## English version

A supervisor may ask: How is memory stored in P006? How is it updated? How is it deleted? Does it have source tracing? Does memory truly improve decision quality, or only backtest performance? Could memory create anchoring bias? How can Project Aegis extend trading memory into thesis memory?

## Key vocabulary

| English | 中文 |
|---|---|
| source tracing | 来源追踪 |
| backtest performance | 回测表现 |
| decision quality | 决策质量 |
| thesis memory | 论点记忆 |
| extend | 扩展 |

---

# Chapter 11 — What to read next

## 中文理解

读完 P006 后，你已经完成第一阶段的核心阅读路径：P001、P016、P025、P013、P014、P004、P006。下一步可以开始做 P001 或 P025 的全文级精读。

## English version

After P006, you will have completed the first-stage core reading path: P001, P016, P025, P013, P014, P004, and P006. The next step is to begin full-text guided reading for P001 or P025.

# Reading status

- Bilingual mobile ebook: draft complete
- Full-text extraction: pending
