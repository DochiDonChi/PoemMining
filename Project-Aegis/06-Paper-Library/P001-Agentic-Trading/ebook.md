# P001 Ebook — Agentic Trading

## Paper

**Agentic Trading: When LLM Agents Meet Financial Markets**

---

# Chapter 1 — Why this paper matters

This is the first paper to read because it gives Project Aegis the big picture.

Most people enter this field by asking:

> Can AI trade stocks and make money?

This paper pushes the question deeper:

> Are current LLM trading-agent studies evaluated in a reliable and comparable way?

For Project Aegis, this is important because we are not trying to build another trading bot. We are trying to understand how trustworthy financial agents should be designed, evaluated, and audited.

---

# Chapter 2 — What problem the authors solve

The authors look at the growing literature on LLM trading agents and ask whether these studies are methodologically sound.

The problem is that many papers may report impressive performance, but they may use different:

- market universes;
- time periods;
- data splits;
- transaction-cost assumptions;
- execution timing assumptions;
- model versions;
- prompts;
- evaluation metrics.

If these assumptions are not clear, results cannot be compared properly.

---

# Chapter 3 — The main idea

The main idea is simple:

> LLM trading agents should not only be judged by return. They should be judged by reproducibility, protocol quality, transaction-cost awareness, and evaluation discipline.

This supports the Project Aegis view that the next serious research problem is not just performance, but trustworthiness.

---

# Chapter 4 — Key concepts

## LLM trading agent

An AI system that uses a large language model to process information and make trading-related decisions.

## Reproducibility

Whether another researcher can repeat the study and get comparable results.

## Transaction cost

The cost of trading, including fees, spread, slippage, and market impact. Ignoring transaction cost can make a strategy look better than it really is.

## Survivorship bias

A testing problem where failed or delisted assets are ignored, making historical performance look artificially strong.

## Execution timing

Whether the system uses information that would actually have been available at the time of the trade.

---

# Chapter 5 — Method / system architecture

P001 is not mainly a system-building paper. It is closer to a review / evidence-map paper.

Its value is that it surveys the field and identifies weaknesses in how trading-agent papers are designed and evaluated.

For Project Aegis, this means P001 is a foundation paper for methodology and skepticism.

---

# Chapter 6 — Data and experiment design

The paper reviews existing LLM trading-agent studies. In our current extraction, the most important reported evidence is:

- 77 included studies;
- 19 primary empirical studies;
- limited time-consistent split reporting;
- limited explicit transaction-cost modeling;
- limited universe / survivorship handling;
- no R3 reproducibility in the captured summary.

These numbers need full-text verification before final publication use.

---

# Chapter 7 — Main results

The main result is not that LLM trading agents are useless.

The main result is:

> The current field has serious evaluation and reproducibility weaknesses.

This is exactly why Project Aegis should focus on:

- reproducibility;
- auditability;
- evidence trails;
- risk-aware evaluation;
- human review.

---

# Chapter 8 — Limitations

P001 mainly studies trading agents.

It does not automatically prove that investment research agents have the same weaknesses. Project Aegis must be careful not to overclaim.

Correct use:

> P001 supports the reproducibility gap in LLM trading-agent literature.

Incorrect use:

> P001 proves all AI investment research agents are unreliable.

---

# Chapter 9 — Project Aegis relevance

P001 supports Project Aegis in three ways:

1. It gives the field-level reproducibility gap.
2. It shows why performance claims need skepticism.
3. It motivates a more trustworthy financial-agent research agenda.

P001 is the reason Project Aegis should not be framed as:

> Can AI make money?

but instead:

> Can AI financial agents produce decisions or research that are reproducible, auditable, and risk-aware?

---

# Chapter 10 — Supervisor questions

1. What exactly does P001 prove?
2. What does P001 not prove?
3. Why is transaction cost important?
4. Why does survivorship bias matter?
5. Why is reproducibility difficult in LLM-agent systems?
6. How does this paper support Project Aegis?
7. How could Project Aegis extend this paper from trading agents to investment research agents?

---

# Chapter 11 — What to read next

Read P016 next.

P001 gives the field-level problem. P016 shows a concrete move from trading agents toward equity research agents.

# Reading status

- Mobile ebook: draft complete
- Summary: complete
- Questions: complete
- Full-text section/table/figure extraction: pending
