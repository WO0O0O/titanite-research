# TITANITE Research

## The Thesis: Mapping the Decade of the OOMs

The scaling laws of AGI are no longer confined to the digital realm. As model training and deployment scale by orders of magnitude (OOMs), the primary constraints have shifted from algorithmic design to the physical world: power generation, transmission infrastructure, advanced metrology, and semiconductor supply-chain security.

Titanite Research is my personal research project to identify, analyse, and track the critical nodes, materials, and equipment manufacturers that underpin this transition. Inspired by the macro-industrial and national security outlook of Leopold Aschenbrenner's _Situational Awareness_ thesis, this repository focuses on the companies that will capture the economics of this capital spend before they are priced in by the consensus.

My research is organised around four interlocking structural pillars:

1. **Compute & Semiconductor Scaling**: Hardware chokepoints in the advanced packaging, optical interconnect, and substrate layers (e.g. Glass Substrates, high-frequency Metrology, and micro-materials).
2. **Energy & Power Infrastructure**: The physical bottlenecks of the gigawatt-scale data centre. This encompasses power transmission, high-voltage transformers, grid connection hardware, and next-generation liquid cooling systems.
3. **Geopolitical Realignment & Sovereignty**: The decoupling of Western supply chains from Chinese manufacturing, the impact of export controls, and the national security mandates driving domestic capacity expansion.
4. **Orbital Infrastructure & Space Tech**: The physical and regulatory constraints of the emerging space economy—specifically launch capacity, spectrum allocations, and sovereign military constellations.

## Methodology: The Human-Machine Loop

I run a dual-phase research methodology, using automated model sweeps to process vast financial datasets and filing databases, followed by my own human-led research to verify the findings and build a complete investment thesis.

### Phase 1: Modular Agentic Sweeps

I build and deploy specialised, prompt-engineered AI agents to run initial company and sector assessments. Currently, this repository utilises three framework modules:

- **Small-Cap AI Infrastructure Chokepoints** (defined in `RESEARCH-NOTES/SMALLCAP-AI-INFRA/SC-AI-INFRA.md`). This module targets micro-to-small cap companies (<$5B market cap) in the hardware supply chain, auditing earnings transcripts and regulatory filings for capacity constraints, lead time extensions, and backlog changes.
- **Trillion-Dollar Scale-Up Beneficiaries** (defined in `RESEARCH-NOTES/SITUATIONAL-AWARENESS/leopold.md`). This module targets mid-to-large-cap companies that are primary enablers or operators of the AI infrastructure buildout, focusing on power and scale.
- **Space-Infrastructure & Orbital Chokepoint Framework** (defined in `RESEARCH-NOTES/SPACE/SPACE-INFRA.md`). This module targets Space Tech companies, focusing on launch capacity bottlenecks, spectrum/regulatory moats, and constellation capital runways.

### Phase 2: Human Reconciliation

The agentic output is a starting filter, not the final investment decision. I manually stress-test and rebuild the analysis where automated tools fall short:

- **Forensic Accounting**: Checking auditor credibility, internal controls, related-party transactions, and capital allocation discipline (e.g. share buybacks vs. dilutive raises).
- **Competitive Roadmap Verification**: Scrutinising emerging technology threats, Chinese competitor progress, and customer qualification cycle times.
- **Upside Arithmetic**: Auditing valuation models and peer-group multiple comparisons to ensure candidate companies present genuine asymmetric risk-reward profiles.

## Repository Structure

My research is categorised by thematic bottlenecks:

- **`RESEARCH-NOTES/SMALLCAP-AI-INFRA/`**: Small-cap chokepoints.
  - `3D-metrology/`: Yield inspection systems for high-bandwidth memory (HBM).
  - `MLCC/`: High-capacitance capacitors for GPU power delivery.
  - `TGV/`: Glass substrates and laser-induced deep etching (LIDE).
  - `photonics/`: Silicon photonics and optical interconnects.
  - `advanced-packaging-equip/`: 2.5D/3D chip stacking.
  - `Semis/`: Specialty foundry and component fabrication.
  - `broadband/`: Optical transport and cable infrastructure.
- **`RESEARCH-NOTES/SITUATIONAL-AWARENESS/`**: Mid-to-large cap scale-up plays.
  - `ENERGY/`: Fuel cells, SMRs, power generation, and grid equipment.
  - `AI-CLOUD-INFRA/`: GPU cloud operators and sovereign hyperscalers.
  - `photonics/`: Transceivers and optical networking.
- **`RESEARCH-NOTES/SPACE/`**: Launch services, satellite manufacturers, and orbital connectivity operators.

---

_Disclaimer: Research use only. Not financial advice. Perform your own due diligence._
