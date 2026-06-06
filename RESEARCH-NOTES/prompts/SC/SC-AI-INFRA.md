# SMALL-CAP AI INFRASTRUCTURE RESEARCH FRAMEWORK

To prevent output token exhaustion and avoid model compression during the execution of chokepoint research reports, this framework is decoupled into a modular two-turn pipeline.

> [!IMPORTANT]
> **DO NOT USE THIS mega-prompt in a single turn.** Instead, execute the research report across two sequential prompts:

### Turn 1 — Data Ingestion & JSON Extraction

Use the **Extractor template** to perform transcript sweeps, web integrity audits, and output the raw JSON data block:

- [SC-AI-EXTRACTOR.md](SC-AI-EXTRACTOR.md)

### Turn 2 — Deep Analytical Valuation & Scoring

Once you have reviewed the JSON buffer, copy it into the **Scorer template** to execute the 15 scoring sections and scorecard:

- [SC-AI-SCORER.md](SC-AI-SCORER.md)

### Turn 2 Data Validation Rule:
When executing the Scorer template (Turn 2), you must cross-examine the JSON data block metrics against your text conclusions before writing any narrative sections. If the buffer shows an inventory-to-binding backlog ratio near zero (e.g., 0.003) or a zero drawdown velocity, your analysis in Section 3, Section 4, and Section 6 must explicitly address this operational bottleneck (e.g., explaining that the company's immediate valuation is bound to facility qualification milestones rather than physical inventory accumulation). If data and narrative contradict, halt and recalibrate the timeline tracking parameters.
