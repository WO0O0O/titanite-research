# Small-Cap AI Infrastructure Prompt Architecture Notes

This document details the structure of the decoupled research framework and the engineering rationale behind these design choices.

### The Decoupled Turn Structure

- **Issue:** Running the entire data ingestion, transcript sweep, and 15-section scoring narrative in a single prompt consistently triggers output token exhaustion limits. Under single-turn execution, the presence of the scoring instructions acts as an attractor vector. The model subconsciously compresses the narrative sections to avoid truncation, sacrificing data density and analytical rigour.
- **Fix:** We split the process into two distinct turns:
  - **Turn 1 (Data Extractor):** Ingests transcripts and filings, performing raw keyword sweeps and integrity audits. It outputs _only_ the structured raw JSON extraction buffer.
  - **Turn 2 (Analytical Scorer):** Ingests the JSON buffer as an immutable data layer and executes the narrative report, scoring sections, scorecard, and synthesis pitch.

### Currency Normalisation

- **Issue:** European hardware and photonics players routinely report in native currencies (SEK, EUR), whilst the scoring TAM equations are anchored to USD. Processing raw metrics in different currencies causes multi-magnitude mathematical errors in the calculated valuation and return ratios.
- **Fix:** We added explicit currency normalisation fields directly inside the Turn 1 Extractor. All financials are converted to USD prior to running the Turn 2 valuation mathematics.

### Backlog Velocity and Duration

- **Issue:** Infrastructure plays frequently sign multi-year frame agreements that do not translate into immediate quarterly revenue. Evaluating backlog as a flat, single metric causes the model to assume rapid short-term revenue inflection and mismodel inventory drawdowns.
- **Fix:** We introduced temporal velocity and duration fields (projected 12-month drawdown and average contract duration) into the extraction buffer to separate long-horizon contract horizons from near-term shipment schedules.

### Logical OR Gates for Regional Coverage

- **Issue:** Strict US-style consensus beats and guidance raises are unsuitable for European micro-caps or pre-consensus equities. The model previously faced a logical contradiction, checking for Nasdaq First North analyst consensus averages, encountering a null set, and failing the section's scoring criteria.
- **Fix:** We refactored Section 12 into mutually exclusive branches:
  - _Branch Alpha:_ For US/Consensus covered companies.
  - _Branch Beta:_ For European, pre-consensus, or qualification-cycle equities, evaluating verified operational milestones (e.g., tape-outs, PDK reference designs) instead of consensus beats.

### Forensic Conflation Checks

- **Issue:** Short sellers targeting deep-tech companies often conflate legacy components with next-generation architectural shifts (e.g., comparing old GaAs components to new Indium Phosphide tunable arrays) to fabricate competitive displacement narratives.
- **Fix:** Section 13 now enforces a forensic conflation check. The model is instructed to audit short reports for generational or substrate boundary errors by referencing verified foundry PDKs, MSA standards, or Tier 1 ecosystem documentation.

### Baseline Networking Anchor & TAM Scaling

- **Issue:** The non-linear scaling multiplier formula in Section 5 previously relied on a "Baseline Cluster Size" variable that was not defined anywhere in the Scorer script. Left unanchored, the model would arbitrarily select its own baseline denominator, creating massive mathematical swings in Layer TAM calculation. Furthermore, multiplying linear power demand with the scaling multiplier created an incorrect $O(\text{Cluster Size}^{2.2})$ hyper-growth term, inflating Layer N TAM to trillions of dollars at hyperscale.
- **Fix:** We anchored the baseline denominator directly to the 2024 baseline cluster footprint of 100,000 GPUs, and isolated Layer N's super-linear scaling directly from a baseline dollar spend ($C_{\text{base}}$), bypassing the linear power term entirely.

### Structured Moat Override Ingestion

- **Issue:** The Section 0 Architectural Moat Override gate checks for foundry reference designs, sole-source integrations, and custom ASIC wins. However, the Turn 1 Extractor schema lacked explicit JSON keys for these parameters, forcing them into loose text snippets in arrays where the Scorer could easily miss them.
- **Fix:** We added explicit, structured keys (`confirmed_foundry_reference_design_status`, `confirmed_tier1_cm_sole_source_integration`, `direct_hyperscaler_custom_asic_design_win`) inside the `operational_flags` block of the Extractor JSON schema, and updated Section 0 to reference them directly.

### Non-Binding Backlog & Margin Waiver Discipline

- **Issue:** Pre-volume companies often announce non-binding LOIs or MOUs to support sentiment. Evaluating forward revenue inflection without distinguishing these from binding contracts could cause the model to overestimate near-term revenue growth. Additionally, requiring strict gross margin improvements during initial volume inflections penalises qualification-cycle players experiencing early under-absorption or transitional cross-listing adjustments.
- **Fix:** We embedded a rule in Section 4 that automatically reduces the Evidence Quality rating to "Weak" if the inflection argument relies on non-binding backlog, and injected an explicit waiver for gross margin compression driven by pre-production overhead under-absorption or cross-listing compliance adjustments.

### Capital Structure & Final Scorecard Sync

- **Issue:** Section 9's final gate had a strict requirement for a literal "raise", which failed strategic JV funding or parent loan facilities. Additionally, the scorecard's summary logic at the very bottom failed to refer back to Section 12's branch sub-logic, triggering positional bias where the model scored European companies a 0 at the final scorecard pass.
- **Fix:** We broadened Section 9's gate to explicitly accept continuous capital access pathways, and added a scorecard sync summary block at the bottom pointing directly back to Section 12's sub-branch architecture.

### Expanded Keyword Sweeps & Moat Ingestion Fields

- **Issue:** The Scorer evaluates specific balance sheet and operational metrics (e.g. capitalized software to hardware asset ratio, crypto validation exposure under Section 3, and default waivers/bridge debt OID under Section 9). However, the Extractor previously did not scan for these terms in transcripts or expose dedicated JSON variables for them, resulting in missing ingestion data during Turn 1.
- **Fix:** We added keywords like "crypto", "ASC 842", "capitalised software", and "bridge debt" to the transcript passes, and introduced structured JSON fields (`capitalised_software_balance_sheet_usd`, `physical_hardware_assets_usd`, `operating_lease_liabilities_asc842_usd`, and `crypto_validation_revenue_pct`) into the Extractor.

### Section 5 Exponent Scratchpad & Blueprint Table

- **Issue:** LLMs frequently approximate or hallucinate calculations when executing non-linear scaling rules (such as computing the fractional exponent in the Clos networking multiplier) or introduce format variance when calculating arithmetic variables.
- **Fix:** We inserted a mandatory execution instruction requiring the model to write out the step-by-step arithmetic in a raw Markdown table matrix before stating the final return multiple, and provided an explicit empty Markdown table blueprint to guarantee format uniformity.

### Section 12 State Anchor

- **Issue:** If the `working_capital_divergence_detected` flag is deeply buried inside the pasted JSON block, the model can suffer from context drift and score the execution section anyway.
- **Fix:** We hardcoded a strict logic constraint at the start of Section 12, forcing the model to print the boolean state of the flag as its first line of output, anchoring the probability space.
