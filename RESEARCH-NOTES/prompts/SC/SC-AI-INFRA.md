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

---

_Framework based on Serenity (@aleabitoreddit) Chokepoint Theory._
