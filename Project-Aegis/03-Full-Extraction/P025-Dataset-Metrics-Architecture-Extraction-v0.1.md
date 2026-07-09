# P025 Dataset, Metrics, and Architecture Extraction v0.1

## Paper

**FinRpt: Dataset, Evaluation System and LLM-based Multi-agent Framework for Equity Research Report Generation**

arXiv:2511.07322

## Extraction status

This file performs the first source-level extraction for P025.

It upgrades P025 from a section-level scaffold to a partial source-level extraction covering:

1. task formulation;
2. dataset construction;
3. data sources;
4. train/validation/test split;
5. report output structure;
6. FinRpt-Gen architecture;
7. agent roles;
8. evaluation metrics;
9. baselines and experiments;
10. human evaluation;
11. source availability.

It is still not a complete table-by-table or appendix-level extraction.

---

# 1. Task formulation

## Source content

P025 formally defines the Equity Research Report (ERR) generation task.

Given:

- a company's stock ticker;
- a research / analysis date;

The system gathers and structures recently relevant information and generates an ERR.

## Structured extraction

| Field | Extracted value |
|---|---|
| Task name | Equity Research Report generation |
| Input key | company stock ticker + research date |
| Input source information | company information, financial indicators, company announcements, company-related news, historical stock prices, historical market indices |
| Output | equity research report |
| Claimed workflow analogy | mimics a real-world analyst drafting an ERR |

## Project Aegis interpretation

This is highly relevant because it shifts the unit of evaluation from a trading action to a research artifact.

P025 is therefore much closer to Project Aegis than most trading-agent papers.

## Claim supported

P025 supports:

> Equity research report generation can be formulated as a structured AI task.

## Claim not supported

This does not yet prove that generated ERRs are reliable, auditable, or institutionally usable.

---

# 2. Output report structure

## Source content

P025 defines an ideal ERR as containing at least six segments.

## Structured extraction

| Segment | Meaning for Project Aegis |
|---|---|
| Financial Analysis | Core financial statement and indicator analysis |
| News Analysis | Analysis of company-related news and its market impact |
| Management and Development Analysis | Analysis of company announcements, management, and development status |
| Risks Analysis | Identification of investment risks |
| Investment Potential Assessment | Forward-looking assessment of investment opportunity |
| Recommendation Rating | Buy or sell recommendation |

## Project Aegis interpretation

This is important because it gives a concrete structure for evaluating investment research artifacts.

A Project Aegis report evaluation rubric can map directly onto these sections, but should add:

- claim-level evidence grounding;
- valuation assumption transparency;
- contrary-evidence handling;
- human-review notes;
- source timestamping.

## Claim supported

P025 supports:

> Equity research report generation requires multi-section financial reasoning, not only generic summarization.

## Claim not supported

P025's six-section report format does not prove that the generated report is complete enough for all buy-side use cases.

---

# 3. Dataset construction

## Source content

P025 constructs an ERR dataset called FinRpt.

It uses 800 stocks from the CSI800 Index in the Chinese market. The date range is from 2024-09-03 to 2024-11-05, with one-week intervals between analysis dates. This yields 10 analysis dates for each company stock.

The final dataset contains 6,825 samples, each including input source information and a corresponding ERR.

## Structured extraction

| Dataset field | Extracted value |
|---|---|
| Dataset name | FinRpt |
| Market | Chinese market |
| Stock universe | CSI800 Index |
| Number of stocks | 800 |
| Date range | 2024-09-03 to 2024-11-05 |
| Analysis interval | weekly |
| Analysis dates | 10 dates per company stock |
| Total samples / reports | 6,825 |
| Dataset language | Chinese-English dataset / English-translated version reported |
| Primary task use | evaluation, supervised fine-tuning, reinforcement learning |

## Project Aegis interpretation

This is a meaningful dataset contribution because ERR generation needs paired input-output samples.

However, the dataset is still limited by:

- one market: China;
- one index universe: CSI800;
- short date range: about two months;
- automatically generated report construction process;
- possible dependence on GPT-4o refinement;
- uncertain external validity for buy-side research.

## Claim supported

P025 supports:

> A structured ERR generation dataset can be built using market, company, announcement, news, price, and index data.

## Claim not supported

P025 does not yet prove:

- the dataset generalizes across countries;
- the dataset generalizes across market regimes;
- the generated reports match true institutional buy-side research quality;
- the dataset is free from licensing or source redistribution issues.

---

# 4. Data sources and filtering

## Source content

P025's data collection module integrates six valuable and complementary types of company-related data:

1. company information;
2. financial indicators;
3. company announcements;
4. company-related news;
5. historical stock prices;
6. historical market indices.

The dataset construction pipeline filters samples lacking financial indicators, samples with fewer than two news articles, and samples with summarized announcement lengths under 300 Chinese characters.

## Structured extraction

| Data type | Function in ERR generation |
|---|---|
| Company Information | foundation for company profile and context |
| Financial Indicators | financial statement / operational analysis |
| Company Announcements | management and development signals |
| Company-related News | event and sentiment information |
| Historical Stock Prices | investment assessment and recommendation context |
| Historical Market Indices | market condition and benchmark context |

## Quality filters

| Filter | Purpose |
|---|---|
| exclude samples lacking financial indicators | ensure financial analysis input exists |
| exclude samples with fewer than two news articles | ensure enough news context |
| exclude short announcement summaries under 300 Chinese characters | ensure sufficient announcement information |

## Project Aegis interpretation

The data-source design is stronger than generic financial QA because it integrates several finance-relevant sources.

However, Project Aegis should still ask:

- Are source timestamps preserved?
- Are source document URLs preserved?
- Can individual report claims be traced back to these sources?
- Are irrelevant or conflicting news items retained for audit?

## Claim supported

P025 supports:

> ERR generation requires multi-source financial evidence, not only a single prompt or annual report.

## Claim not supported

The source design does not yet prove claim-level evidence grounding.

---

# 5. Dataset enhancement process

## Source content

P025 uses a Dataset Enhancement Module with three steps:

1. Recommendation Rating Corrector;
2. Expert-written ERRs Corrector;
3. LLM Polisher.

The Recommendation Rating Corrector compares the generated recommendation rating against a ground-truth trend label. If inconsistent, the sample is re-inferred until the correct prediction is generated.

The Expert-written ERRs Corrector retrieves stock-related reports from Eastmoney during the week before the analysis date and uses GPT-4o to review and refine information accuracy, logical consistency, and writing style.

The LLM Polisher uses GPT-4o to improve readability, coherence, and logical flow.

## Structured extraction

| Enhancement step | Role | Project Aegis concern |
|---|---|---|
| Recommendation Rating Corrector | Aligns recommendation with trend label | May create label leakage or over-align outputs with trend label |
| Expert-written ERRs Corrector | Uses retrieved Eastmoney reports and GPT-4o refinement | Need verify licensing, source traceability, and whether expert reports are preserved |
| LLM Polisher | Improves readability/coherence | May improve style without improving factual grounding |

## Project Aegis interpretation

This is a key finding. P025's dataset is not simply human-authored ground truth. It appears to be generated and enhanced through a multi-step LLM-assisted process.

This is useful, but it creates methodological questions:

1. Does repeated inference until the recommendation matches a trend label bias the dataset?
2. Are reports optimized for prediction label consistency rather than independent research quality?
3. Does GPT-4o refinement make the dataset partly teacher-model dependent?
4. Can downstream models learn GPT-4o style rather than analyst reasoning?

## Claim supported

P025 supports:

> LLM-assisted pipelines can construct ERR training/evaluation data at scale.

## Claim not supported

P025 does not yet prove that the resulting ERRs are equivalent to independent professional analyst reports.

---

# 6. Dataset statistics and split

## Source content

P025 reports that FinRpt contains 6,825 reports from 2024-09-03 to 2024-11-05.

It partitions the dataset as follows:

- data before 2024-10-31 is randomly split into training and validation with a 9:1 ratio;
- samples after 2024-10-31 are used as the test set;
- training set: 5,556 samples;
- validation set: 617 samples;
- test set: 652 samples.

## Structured extraction

| Split | Count |
|---|---:|
| Training | 5,556 |
| Validation | 617 |
| Test | 652 |
| Total | 6,825 |

## Project Aegis interpretation

This split is partly time-aware because the test set is after 2024-10-31.

However, training and validation before 2024-10-31 are randomly split, so the exact temporal discipline should be checked more carefully.

Project Aegis should ask:

- Are companies overlapping across train/validation/test?
- Are future trend labels used in construction?
- Are Eastmoney reports retrieved before or after the analysis date?
- Does re-inference until correct rating introduce target leakage?

## Claim supported

P025 supports:

> The dataset includes a defined train/validation/test split with a held-out later test period.

## Claim not supported

P025 does not yet prove the benchmark is leakage-free.

---

# 7. FinRpt-Gen architecture

## Source content

P025 proposes FinRpt-Gen, described as a multi-agent framework specifically designed for ERR generation.

FinRpt-Gen has three modules:

1. Information Extraction Module;
2. Information Analysis Module;
3. Prediction Module.

It involves nine agents.

## Structured extraction

| Module | Agents / functions |
|---|---|
| Information Extraction Module | News Extraction Agent; Income Extraction Agent; Balance Extraction Agent; Cash Extraction Agent |
| Information Analysis Module | Finance Analysis Agent; News Analysis Agent; Status Analysis Agent; Risk Analysis Agent |
| Prediction Module | Prediction Agent |

## Agent roles

| Agent | Role |
|---|---|
| News Extraction Agent | ranks news by likely impact and outputs top 10 news articles |
| Income Extraction Agent | extracts revenue, net income, EPS and other income statement metrics |
| Balance Extraction Agent | extracts assets, liabilities, equity and other balance sheet indicators |
| Cash Extraction Agent | extracts operating, investing and financing cash flow information |
| Finance Analysis Agent | summarizes financial health, profitability and cash flow position |
| News Analysis Agent | explains how selected news may affect future stock performance |
| Status Analysis Agent | derives management and development analysis from announcements |
| Risk Analysis Agent | integrates analysis outputs and identifies key investment risks |
| Prediction Agent | forecasts investment potential assessment and buy/sell recommendation |

## Project Aegis interpretation

This is strong evidence that P025 is more than a generic report generator. It uses role-specialized agents mapped to report sections.

However, Project Aegis should still ask:

- Are agents only prompt roles or trained specialized modules?
- Are intermediate outputs logged?
- Are agent decisions traceable?
- Does the system cite source documents?
- Can a human reviewer inspect each agent's contribution?

## Claim supported

P025 supports:

> Multi-agent role specialization is being applied to equity research report generation.

## Claim not supported

P025 does not yet prove that this architecture is auditable or institutionally realistic.

---

# 8. Training strategy

## Source content

P025 applies Supervised Fine-Tuning to four critical agents:

- Finance Analysis Agent;
- News Analysis Agent;
- Status Analysis Agent;
- Prediction Agent.

It then applies Reinforcement Learning to the Prediction Agent using DAPO, optimizing a reward that combines recommendation rating accuracy and analytical-content quality measured by ROUGE.

## Structured extraction

| Training stage | Target agents | Purpose |
|---|---|---|
| SFT | Finance Analysis, News Analysis, Status Analysis, Prediction | learn section-specific generation from FinRpt demonstrations |
| RL / DAPO | Prediction Agent | optimize recommendation accuracy and rationale quality |

## Project Aegis interpretation

This is important because it shows P025 is not only a prompted agent system. It also trains agents.

But the RL reward design raises questions:

- Does ROUGE measure financial reasoning quality adequately?
- Does optimizing recommendation accuracy over trend labels encourage short-horizon prediction behavior?
- Does the reward capture risk completeness or evidence grounding?

## Claim supported

P025 supports:

> ERR-generation agents can be trained using a dataset plus SFT/RL pipeline.

## Claim not supported

This does not prove that the training objective optimizes for trustworthy research quality.

---

# 9. Evaluation metrics

## Source content

P025 uses two groups of metrics:

1. Basic Metrics;
2. LLM Evaluation Metrics.

Basic Metrics:

- CompletionRate;
- Accuracy;
- BERTScore;
- ROUGE-L;
- NumberRate.

LLM Evaluation Metrics:

- Financial Numeric;
- News;
- Company & Market & Industry;
- Invest;
- Risk;
- Writing.

## Structured extraction

| Metric | Type | What it evaluates |
|---|---|---|
| CompletionRate | basic | whether report is generated in required format |
| Accuracy | basic | buy/sell recommendation accuracy |
| BERTScore | basic NLP | semantic similarity |
| ROUGE-L | basic NLP | text overlap / generation quality |
| NumberRate | financial-text proxy | richness of numerical content |
| Financial Numeric | LLM evaluation | precision and depth of financial numeric analysis |
| News | LLM evaluation | relevance and comprehensiveness of news analysis |
| Company & Market & Industry | LLM evaluation | insight into company, market and industry context |
| Invest | LLM evaluation | whether investment recommendation is logical and well-reasoned |
| Risk | LLM evaluation | thoroughness of risk analysis |
| Writing | LLM evaluation | coherence, readability and logical consistency |

## Project Aegis interpretation

This is a meaningful evaluation system because it goes beyond ROUGE/BERTScore.

However, important Project Aegis metrics are still missing or not yet verified:

- claim-level source grounding;
- citation correctness;
- unsupported-claim detection;
- valuation assumption transparency;
- contrary-evidence handling;
- audit-trail completeness.

## Claim supported

P025 supports:

> ERR generation evaluation is moving beyond generic NLP similarity metrics toward finance-specific report-quality dimensions.

## Claim not supported

P025 does not yet prove that evidence grounding or auditability are evaluated.

---

# 10. Baselines and experimental setup

## Source content

P025 evaluates four baseline categories:

1. standalone state-of-the-art LLMs;
2. FinRpt-Gen with closed-source LLMs;
3. FinRpt-Gen with open-source LLMs;
4. FinRpt-Gen with fine-tuned open-source LLMs.

It uses 100 randomly selected samples from the FinRpt test set for evaluation.

Implementation details include:

- open-source models accessed locally via the Ollama Python Library;
- closed-source models accessed via official APIs;
- SFT conducted on 8 NVIDIA 3090 GPUs;
- RL conducted on 8 NVIDIA A100 GPUs.

## Structured extraction

| Area | Extracted value |
|---|---|
| Evaluation sample | 100 random samples from test set |
| Baseline categories | standalone LLMs; FinRpt-Gen with closed-source LLMs; FinRpt-Gen with open-source LLMs; fine-tuned FinRpt-Gen open-source LLMs |
| Local model access | Ollama Python Library |
| Closed model access | official APIs |
| SFT compute | 8 NVIDIA 3090 GPUs |
| RL compute | 8 NVIDIA A100 GPUs |

## Project Aegis interpretation

The inclusion of multiple baselines is a strength.

However, 100 test samples may be too small for broad claims, and the compute requirements are non-trivial.

Project Aegis should ask whether evaluation results are stable across:

- different sectors;
- market regimes;
- company sizes;
- languages;
- report dates;
- model families.

## Claim supported

P025 supports:

> FinRpt-Gen is evaluated against multiple model and framework baseline categories.

## Claim not supported

P025 does not yet prove broad robustness across markets, time periods, or institutional use cases.

---

# 11. Reported basic metric results

## Source content

P025 reports that the best model in Table 1 is the authors' FinRpt-Gen using Qwen2.5-7B-Instruct-SFT-RL.

Reported values:

| Method | CompletionRate | Accuracy | ROUGE-L | BERTScore | NumberRate |
|---|---:|---:|---:|---:|---:|
| Our FinRpt-Gen (Qwen2.5-7B-Instruct-SFT-RL) | 100% | 55% | 49.06 | 82.43 | 95.15% |

The table also reports strong GPT-4o and Gemini baselines around 50-51% accuracy in the FinRpt-Gen setting.

## Structured extraction

The main result is not that ERR generation is solved. The main result is that the tailored multi-agent + SFT + RL system improves reported metrics relative to single-LLM and non-fine-tuned variants.

## Project Aegis interpretation

Accuracy remains modest at 55% for buy/sell recommendation, so the result should be treated cautiously.

The stronger evidence may be in report quality dimensions rather than recommendation accuracy alone.

## Claim supported

P025 supports:

> A tailored multi-agent and trained FinRpt-Gen setup can improve benchmark metrics over several baselines.

## Claim not supported

P025 does not prove that the generated recommendations are investment-grade or commercially actionable.

---

# 12. Ablation study

## Source content

P025 reports an ablation study comparing FinRpt-Gen with variants removing components.

Reported variants include:

1. without Finance Extraction;
2. without News Extraction;
3. without three Analysis Agents;
4. full FinRpt-Gen.

The full FinRpt-Gen reports the strongest results in the shown ablation table.

## Structured extraction

| Variant | Accuracy | ROUGE-L | BERTScore |
|---|---:|---:|---:|
| w/o Finance Extraction | 47 | 38.93 | 76.50 |
| w/o News Extraction | 49 | 46.02 | 81.20 |
| w/o 3 Analysis Agents | 51 | 45.92 | 81.38 |
| FinRpt-Gen | 55 | 49.06 | 82.43 |

## Project Aegis interpretation

This is useful because it provides evidence that role-specialized components matter.

The drop without finance extraction is especially relevant to Project Aegis: financial statement extraction appears necessary for strong report generation.

## Claim supported

P025 supports:

> Specialized financial extraction and analysis agents improve ERR-generation benchmark performance compared with simplified variants.

## Claim not supported

The ablation does not prove that the agents are auditable or that their intermediate reasoning is faithful.

---

# 13. Human evaluation

## Source content

P025 conducts human evaluation for dataset quality.

It randomly samples:

- 30 ERRs from the FinRpt dataset;
- 30 expert-written ERRs.

Three senior financial analysts rate each ERR from four aspects using a 0-5 scale.

Reported comparison:

| ERR type | FN | News | Invest | Writing | Average |
|---|---:|---:|---:|---:|---:|
| Expert-written | 4.57 | 4.00 | 4.13 | 4.33 | 4.30 |
| FinRpt | 4.33 | 4.20 | 4.10 | 4.17 | 4.20 |
| Kappa Score | 0.85 | 0.86 | 0.89 | 0.84 | 0.86 |

## Structured extraction

The human evaluation suggests FinRpt dataset reports are close to expert-written reports on the sampled dimensions.

However, the sample size is small and the evaluated dimensions do not fully cover source grounding or auditability.

## Project Aegis interpretation

This is one of P025's strongest pieces of evidence for report quality, but it is not enough for trustworthiness.

Project Aegis should ask:

- What were the analysts asked to evaluate exactly?
- Did they verify facts against sources?
- Were they blinded to report origin?
- Did they assess evidence grounding?
- Did they assess valuation assumptions?

## Claim supported

P025 supports:

> Human analysts rated sampled FinRpt reports close to expert-written ERRs on selected report-quality dimensions.

## Claim not supported

P025 does not yet prove the reports are factually correct or audit-ready.

---

# 14. Code and dataset availability

## Source content

P025 reports:

- code is public at https://github.com/jinsong8/FinRpt;
- datasets are public at https://huggingface.co/datasets/jinsong8/FinRpt.

## Structured extraction

| Artifact | Reported availability |
|---|---|
| Code | public GitHub repository reported |
| Dataset | public Hugging Face dataset reported |
| Prompts | appendix contains prompt examples / prompt table references |
| Generated report case | appendix contains report case |

## Project Aegis interpretation

This is a potential strength for reproducibility.

However, Project Aegis must still verify:

- repository exists;
- license is clear;
- dataset files are downloadable;
- prompts are complete;
- generated reports can be reproduced;
- external source data can be reconstructed.

## Claim supported

P025 supports, pending external verification:

> The authors report public code and dataset availability.

## Claim not supported

Do not claim full reproducibility until the GitHub and Hugging Face resources are independently checked.

---

# 15. Evidence grounding and auditability assessment

## Source content

P025 evaluates financial numeric quality, news relevance, company/market/industry insight, investment logic, risk analysis, and writing quality.

However, from the current source-level extraction, explicit claim-level citation grounding is not yet established.

## Structured extraction

| Auditability field | Current evidence status |
|---|---|
| Source references in final report | not yet verified |
| Claim-level grounding | not established in current extraction |
| Data/source timestamps | partly implied through analysis date and data range, but not enough |
| Prompt availability | appendix prompt references reported |
| Generated artifacts | appendix report case reported |
| Human-review logs | human scores reported, logs not yet verified |
| Error analysis for hallucination | not yet established |
| Reproducibility package | code/dataset reported, not independently verified |

## Project Aegis interpretation

P025 is a strong anchor for research-artifact generation and report-quality evaluation, but not yet a strong anchor for auditability.

The key missing bridge is claim-level evidence grounding.

## Claim supported

P025 supports:

> Finance-specific report-quality evaluation is being developed for ERR generation.

## Claim not supported

P025 does not yet support:

> ERR generation is fully auditable or evidence-grounded at claim level.

---

# 16. Updated P016/P025 comparison

| Dimension | P016 FinRobot | P025 FinRpt |
|---|---|---|
| Main focus | Equity research and valuation workflow | ERR generation benchmark and multi-agent generation framework |
| Output | Investment thesis / valuation-style output | Six-section equity research report |
| Data source approach | Needs deeper extraction | Six data types across company, financial, announcement, news, price, and index data |
| Agent design | Data-CoT / Concept-CoT / Thesis-CoT | nine agents across extraction, analysis, and prediction modules |
| Evaluation | needs deeper extraction | basic metrics + LLM evaluation + human dataset-quality evaluation |
| Dataset contribution | not primary from current extraction | central contribution: 6,825-sample FinRpt dataset |
| Auditability | pending | source grounding not yet established |
| Project Aegis role | equity research workflow anchor | report-generation benchmark / artifact evaluation anchor |

## Project Aegis conclusion

P016 and P025 together provide a stronger basis for defining an investment research agent subcategory.

However:

- P016 needs deeper extraction;
- P025 needs evidence-grounding verification;
- neither yet proves institutional readiness.

---

# 17. Updated claim status

| Claim | Status after P025 source-level extraction |
|---|---|
| Equity research report generation is an emerging task | strengthened |
| P025 is relevant to investment research agents | strengthened |
| P025 provides a useful benchmark and dataset | strengthened but requires license/resource verification |
| P025 evaluates finance-specific report quality | strengthened |
| P025 solves auditability | not supported |
| P025 provides claim-level evidence grounding | not established |
| P025 is institutionally ready | not supported |

---

# 18. Remaining verification tasks

## Highest priority

1. Verify GitHub repository and license.
2. Verify Hugging Face dataset and license.
3. Extract appendix prompts.
4. Extract Figure 1 dataset pipeline.
5. Extract Figure 3 FinRpt-Gen architecture.
6. Extract Figure 4 LLM evaluation radar chart.
7. Extract Appendix Table 5 LLM evaluation quantitative results.
8. Extract Table 16 prompt for expert-written ERR corrector.
9. Check whether final report cases include citations or evidence references.
10. Check whether the human evaluation was blinded and how analysts were instructed.

## Current status after this file

| Extraction area | Status |
|---|---|
| Task formulation | extracted |
| Dataset construction | extracted |
| Data sources | extracted |
| Dataset split | extracted |
| Output structure | extracted |
| Architecture and agents | extracted |
| Training strategy | extracted |
| Metrics | extracted |
| Baselines / experiment setting | extracted |
| Ablation | extracted |
| Human evaluation | extracted |
| Code/dataset availability claim | extracted, not independently verified |
| Evidence grounding | not established |
| Appendix prompts | pending |
| External repository/dataset verification | pending |
