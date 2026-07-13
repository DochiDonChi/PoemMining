# P013 Bilingual Ebook — Finance Agent Benchmark

## Paper

**Finance Agent Benchmark: Benchmarking LLMs on Real-world Financial Research Tasks**

## How to read

先读中文理解 benchmark 的作用，再读英文学习如何解释 financial research task evaluation。

Read the Chinese section first to understand the benchmark logic, then use the English section to practice explaining financial research task evaluation.

---

# Chapter 1 — Why this paper matters

## 中文理解

P013 重要，因为它不是问 AI 能不能直接交易，而是问 LLM agent 能不能完成真实金融研究任务。Project Aegis 关心的是 investment research agent，而 research task 是投资研究系统的基础。如果模型连专业金融研究问题都答不好，就很难直接相信它可以生成高质量投资研究报告。

## English version

P013 matters because it does not ask whether AI can directly trade. Instead, it asks whether LLM agents can solve real-world financial research tasks. Project Aegis focuses on investment research agents, and research-task capability is foundational to such systems. If a model cannot answer professional financial research questions well, it is difficult to trust it to generate high-quality investment research reports.

## Key vocabulary

| English | 中文 |
|---|---|
| benchmark | 基准测试 |
| financial research task | 金融研究任务 |
| real-world task | 真实世界任务 |
| professional question | 专业问题 |
| foundational | 基础性的 |

---

# Chapter 2 — What problem the authors solve

## 中文理解

作者想解决的问题是：我们需要一个更真实的 benchmark 来测试 LLM 在金融研究中的能力。普通金融问答太简单，不能代表真实分析师工作。真实任务可能需要读 SEC filing、理解财务数据、找到相关证据、做推理，并给出正确答案。

## English version

The authors address the need for a more realistic benchmark to evaluate LLM capability in financial research. Generic financial QA is often too simple to represent real analyst work. Real tasks may require reading SEC filings, understanding financial data, locating relevant evidence, reasoning over the information, and producing correct answers.

## Key vocabulary

| English | 中文 |
|---|---|
| SEC filing | SEC 申报文件 |
| analyst work | 分析师工作 |
| relevant evidence | 相关证据 |
| reasoning | 推理 |
| financial data | 财务数据 |

---

# Chapter 3 — Main idea

## 中文理解

P013 的核心思想是建立一个由专家设计的金融研究问题集，然后测试不同 LLM agents 能否完成这些问题。它的价值不在于生成交易策略，而在于衡量 AI 是否具备基本金融研究能力。

## English version

The main idea of P013 is to build a set of expert-designed financial research questions and test whether different LLM agents can solve them. Its value is not in generating trading strategies, but in measuring whether AI systems possess basic financial research capability.

## Key vocabulary

| English | 中文 |
|---|---|
| expert-designed | 专家设计的 |
| question set | 问题集 |
| capability | 能力 |
| measure | 衡量 |
| trading strategy | 交易策略 |

---

# Chapter 4 — Key concepts

## 中文理解

这里最重要的概念是 benchmark。Benchmark 就像考试，用统一问题测试不同模型。另一个重要概念是 agentic harness，也就是给模型工具，例如搜索和 EDGAR，让它像研究助理一样查资料。P013 不是只考记忆，而是考模型能不能用工具解决金融研究问题。

## English version

The key concept is the benchmark. A benchmark is like an exam that uses standardized questions to compare different models. Another key concept is the agentic harness, where the model is given tools such as search and EDGAR access, allowing it to act more like a research assistant. P013 does not only test memorization; it tests whether models can use tools to solve financial research problems.

## Key vocabulary

| English | 中文 |
|---|---|
| standardized question | 标准化问题 |
| agentic harness | 智能体工具框架 |
| EDGAR | 美国 SEC 公司文件数据库 |
| research assistant | 研究助理 |
| memorization | 记忆 |

---

# Chapter 5 — Method / system architecture

## 中文理解

P013 的结构可以理解为：专家设计问题 → agent 使用搜索和 EDGAR 等工具 → agent 查找资料和推理 → 输出答案 → benchmark 评分。这个结构很适合 Project Aegis，因为未来 investment research agent 也需要工具、证据和评估。

## English version

The structure of P013 can be understood as: experts design questions → the agent uses tools such as search and EDGAR → the agent retrieves information and reasons over it → the agent outputs an answer → the benchmark scores the result. This structure is highly relevant to Project Aegis because future investment research agents also need tools, evidence, and evaluation.

## Key vocabulary

| English | 中文 |
|---|---|
| retrieve information | 检索信息 |
| output an answer | 输出答案 |
| score the result | 给结果评分 |
| tool use | 工具使用 |
| evaluation | 评估 |

---

# Chapter 6 — Data and experiment design

## 中文理解

目前我们记录到 P013 包含 537 个专家设计问题，使用 SEC filings，并让 agent 通过 Google Search 和 EDGAR 工具回答问题。最强模型表现仍然不到完美，说明真实金融研究任务对 LLM agent 来说仍然困难。后面需要看全文确认九类任务、评分规则和错误分析。

## English version

Our current extraction records that P013 contains 537 expert-authored questions, uses SEC filings, and gives agents access to tools such as Google Search and EDGAR. Even the strongest model performance is far from perfect, suggesting that real-world financial research tasks remain difficult for LLM agents. Full-text reading should verify the nine task categories, scoring rules, and error analysis.

## Key vocabulary

| English | 中文 |
|---|---|
| expert-authored | 专家撰写的 |
| task category | 任务类别 |
| scoring rule | 评分规则 |
| error analysis | 错误分析 |
| far from perfect | 远未完美 |

---

# Chapter 7 — Main results

## 中文理解

P013 的主要结果是：即使是强模型，在真实金融研究 benchmark 上也还有明显限制。这不是说模型没有价值，而是说明金融研究很难，需要更好的工具设计、证据追踪、任务分解和评估方法。

## English version

The main result of P013 is that even strong models still have clear limitations on real-world financial research benchmarks. This does not mean the models are useless. It means financial research is difficult and requires better tool design, evidence tracking, task decomposition, and evaluation methods.

## Key vocabulary

| English | 中文 |
|---|---|
| limitation | 限制 |
| evidence tracking | 证据追踪 |
| task decomposition | 任务分解 |
| tool design | 工具设计 |
| evaluation method | 评估方法 |

---

# Chapter 8 — Limitations

## 中文理解

P013 是 benchmark paper，不是完整 investment research agent system。它测试 agent 能不能回答金融研究问题，但不一定测试它能不能生成完整投资 thesis、估值报告、风险分析或 portfolio implication。所以不能把 P013 过度解释成完整投资研究系统的证明。

## English version

P013 is a benchmark paper, not a complete investment research agent system. It tests whether agents can answer financial research questions, but it does not necessarily test whether they can generate full investment theses, valuation reports, risk analyses, or portfolio implications. Therefore, P013 should not be overinterpreted as evidence for complete investment research systems.

## Key vocabulary

| English | 中文 |
|---|---|
| investment thesis | 投资论点 |
| valuation report | 估值报告 |
| portfolio implication | 组合影响 |
| overinterpret | 过度解释 |
| complete system | 完整系统 |

---

# Chapter 9 — Project Aegis relevance

## 中文理解

P013 支持 Project Aegis 的 evaluation 主线。它说明如果要建立可信 investment research agent，不能只看生成文本是否流畅，而要设计专业任务、标准答案、工具环境和评分规则。它也帮助我们连接 P016/P025：研究报告生成之前，先要有研究问题求解能力。

## English version

P013 supports the evaluation pillar of Project Aegis. It shows that trustworthy investment research agents should not be evaluated only by fluent text generation. We need professional tasks, reference answers, tool environments, and scoring rules. It also connects to P016 and P025: before generating research reports, agents need the ability to solve financial research questions.

## Key vocabulary

| English | 中文 |
|---|---|
| evaluation pillar | 评估支柱 |
| fluent text generation | 流畅文本生成 |
| reference answer | 标准答案 |
| tool environment | 工具环境 |
| scoring rule | 评分规则 |

---

# Chapter 10 — Supervisor questions

## 中文理解

导师可能会问：P013 是评估 finance QA，还是 investment research agent？它的任务是否真的代表分析师工作？为什么用 SEC filings？它和 P016/P025 有什么关系？Project Aegis 能不能把 P013 的 benchmark 思路扩展到 research report 和 investment thesis？

## English version

A supervisor may ask: Does P013 evaluate finance QA or investment research agents? Do its tasks truly represent analyst work? Why are SEC filings used? How is P013 related to P016 and P025? Can Project Aegis extend P013’s benchmark logic to research reports and investment theses?

## Key vocabulary

| English | 中文 |
|---|---|
| analyst work | 分析师工作 |
| benchmark logic | 基准测试逻辑 |
| extend | 扩展 |
| investment thesis | 投资论点 |
| evaluate | 评估 |

---

# Chapter 11 — What to read next

## 中文理解

读完 P013 后，下一篇读 P014。P013 讲 financial research task benchmark，P014 讲更大的 evaluation lifecycle 和 governance。

## English version

After P013, read P014. P013 focuses on financial research task benchmarking, while P014 focuses on the broader evaluation lifecycle and governance.

# Reading status

- Bilingual mobile ebook: draft complete
- Full-text extraction: pending
