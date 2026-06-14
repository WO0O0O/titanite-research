# CATALYST TRACKER

## Thesis Catalyst Prediction Accuracy Monitoring

This tracker quantifies the accuracy of time-sensitive catalyst predictions across the portfolio. Systematic catalyst timing errors (over-optimism or excessive conservatism) indicate framework calibration issues that must be corrected.

---

## PURPOSE

Many Tier 1 theses depend on **time-sensitive catalysts** where the expected date materially affects return math:
- Product qualification completions
- Manufacturing capacity ramps
- Customer contract announcements
- Regulatory approvals
- First commercial shipments
- M&A deal closures

If catalysts consistently arrive 6-12 months late, the thesis return profile degrades from 3-5x to 1.5-2x, and capital is dead-weighted. This tracker identifies **systematic timing bias** in research forecasts.

---

## ACTIVE CATALYST TRACKING TABLE

| Ticker | Catalyst Description | Expected Date | Confidence Level | Actual Date | Delta (Days) | Impact on Thesis | Status |
|--------|---------------------|---------------|------------------|-------------|--------------|------------------|--------|
| **IQE** | MACOM LTSA capacity ramp to £25M+ quarterly revenue | Q3 2026 (Sept) | High | _Pending_ | — | Revenue inflection drives re-rating | 🟡 Active |
| **ASPI** | Silicon-28 Pretoria facility first commercial shipments | Q3 2026 (July-Sept) | Medium | _Pending_ | — | Validates quantum materials revenue stream | 🟡 Active |
| **AL2SI** | Sacramento Blackwell cluster (Godì 1.8) Phase 1 deployment | H2 2026 (Aug-Dec) | High | _Pending_ | — | $610M master contract validation | 🟡 Active |
| **FOCI** | CPO FAU commercial shipments begin (TSMC COUPE platform) | Q3 2026 (July-Sept) | Medium-High | _Pending_ | — | Revenue inflection from <$10M to $30M+ run rate | 🟡 Active |
| **SHUNSIN** | Broadcom CPO switch platform trial production (Vietnam) | Mid-2026 (June-July) | Medium | _Pending_ | — | De-risks geopolitical supply chain | 🟡 Active |
| **OKLO** | NRC Combined License Application (COLA) submission | H2 2026 | Medium | _Pending_ | — | Regulatory de-risking milestone | 🟡 Active |
| **TLN** | Cornerstone 2.6 GW gas acquisition final close | 1 June 2026 | High | ✅ 1 June 2026 | 0 days | Adds dispatchable capacity for AWS PPA | ✅ Hit |
| **BE** | Oracle 1.2 GW contracted segment of 2.8 GW agreement signing | Q1 2026 | High | ✅ Confirmed Q1 2026 | ~0 days | De-risks backlog conversion | ✅ Hit |
| **AAOI** | 800G transceiver volume shipment ramp (post-Q1 2026 delay) | Q2-Q3 2026 | Medium | _Pending_ | — | Revenue recovery from $50M → $80M+ quarterly | 🟡 Active |
| **SEE** | Magna convertible note refinancing (due Oct 2026) | Q3 2026 (before Oct) | High | _Pending_ | — | Balance sheet risk mitigation | 🟡 Active |
| **KEEL** | Panther Creek 62 MW AI data centre lease-up (first tenant) | Q3-Q4 2026 | Medium | _Pending_ | — | Validates pivot from Bitcoin to AI colocation | 🟡 Active |

---

## HISTORICAL CATALYST PERFORMANCE (Completed)

| Ticker | Catalyst Description | Expected Date | Actual Date | Delta (Days) | Outcome | Lesson Learned |
|--------|---------------------|---------------|-------------|--------------|---------|----------------|
| **TLN** | AWS Susquehanna PPA restructure approval | Q1 2026 | March 2026 | ~0 days | ✅ On Time | Strong regulatory visibility on nuclear deals |
| **IQE** | £81M strategic fundraise close (MACOM anchor) | May 2026 | May 2026 | ~0 days | ✅ On Time | Management execution on capital raises reliable |
| **SOITEC** | Laurent Rémont CEO appointment | April 2026 | April 2026 | ~0 days | ✅ On Time | Board transitions tracked accurately |
| **AL2SI** | Yih-Shyan Liaw indictment (risk event) | _Not predicted_ | March 2026 | N/A | ⚠️ Miss | Need systematic tracking of departed executives' legal issues |

---

## CATALYST HIT RATE METRICS

### Overall Performance (Rolling 12 Months)
- **Total Catalysts Tracked:** 15
- **Catalysts Hit On Time (±30 days):** 4
- **Catalysts Delayed (>30 days late):** 0
- **Catalysts Accelerated (>30 days early):** 0
- **Catalysts Still Pending:** 11
- **Hit Rate (Completed Catalysts Only):** 100% (4/4)
  
_Note: Hit rate is artificially high due to small sample size. Requires 12+ months of tracking for statistical significance._

### By Confidence Level
| Confidence | Total Tracked | Hit On Time | Delayed | Early | Pending | Hit Rate |
|------------|---------------|-------------|---------|-------|---------|----------|
| **High**   | 7 | 4 | 0 | 0 | 3 | 100% (4/4) |
| **Medium-High** | 2 | 0 | 0 | 0 | 2 | _Pending_ |
| **Medium** | 6 | 0 | 0 | 0 | 6 | _Pending_ |
| **Low**    | 0 | 0 | 0 | 0 | 0 | N/A |

### By Catalyst Type
| Catalyst Type | Total Tracked | Hit On Time | Delayed | Average Delta (Days) |
|---------------|---------------|-------------|---------|---------------------|
| **Regulatory Approval** | 3 | 1 | 0 | 0 |
| **Manufacturing Ramp** | 4 | 0 | 0 | _Pending_ |
| **Financial Close** | 3 | 2 | 0 | 0 |
| **Product Shipment** | 4 | 0 | 0 | _Pending_ |
| **Management Change** | 1 | 1 | 0 | 0 |

---

## CATALYST CONFIDENCE LEVEL DEFINITIONS

**High Confidence (80%+ probability of hitting within ±30 days):**
- Management has publicly guided specific date/quarter
- Catalyst is contractually binding (e.g., M&A closing date)
- External validation exists (regulatory filings, customer confirmations)
- No material dependencies on third parties

**Medium-High Confidence (60-80% probability):**
- Management has guided date but with "expected" or "targeted" language
- Single external dependency (e.g., customer acceptance testing)
- Historical precedent suggests timing is realistic

**Medium Confidence (40-60% probability):**
- Management has guided quarter but not specific month
- Multiple external dependencies (supply chain, regulatory, customer)
- Industry-standard timelines suggest feasibility but no company-specific confirmation

**Low Confidence (<40% probability):**
- Analyst estimate based on industry norms, not management guidance
- Highly dependent on exogenous factors (macro, regulatory, geopolitical)
- Company has history of missing guided timelines

---

## SYSTEMATIC BIAS DETECTION

### Over-Optimism Indicators (Framework needs recalibration if ANY are true):
- [ ] >50% of completed catalysts arrived >60 days late
- [ ] Average delay across all completed catalysts >45 days
- [ ] 3+ consecutive "High Confidence" catalysts missed by >30 days

**Current Status:** No over-optimism detected (sample size too small)

### Excessive Conservatism Indicators:
- [ ] >50% of completed catalysts arrived >60 days early
- [ ] Average acceleration across all completed catalysts >45 days

**Current Status:** No excessive conservatism detected

---

## CATALYST MONITORING PROTOCOL

### Weekly Check (Mondays)
- Review all "Active" catalysts with expected dates within next 60 days
- Check company press releases, SEC filings, and industry news for updates
- Update "Status" column if new information emerges

### Monthly Review (First of Month)
- Update all "Actual Date" fields for catalysts that occurred in prior month
- Calculate "Delta (Days)" for completed catalysts
- Assess "Impact on Thesis" — did the catalyst arriving early/late/on-time materially change the investment case?
- Update hit rate metrics

### Quarterly Deep Dive (After Each Quarter Close)
- Analyze patterns: Are manufacturing catalysts systematically delayed? Are regulatory catalysts consistently on-time?
- Identify any companies with 2+ missed catalysts — triggers post-mortem analysis
- Update CHANGELOG.md if systematic timing bias detected requiring framework modification

---

## IMPACT CLASSIFICATION

When a catalyst is hit or missed, classify its impact on the thesis:

**Critical Impact:**
- Catalyst arriving >90 days late causes thesis to fail (stock likely declines >30%)
- Example: Product qualification delayed from Q2 to Q4, missing customer budget cycle

**Moderate Impact:**
- Catalyst arriving 30-90 days late reduces expected return from 3x to 2x
- Example: Manufacturing ramp delayed one quarter, pushing revenue inflection

**Low Impact:**
- Catalyst arriving ±30 days has negligible effect on 24-36 month thesis
- Example: CFO appointment delayed by 3 weeks

**Positive Surprise:**
- Catalyst arriving >60 days early accelerates thesis timeline
- Example: Regulatory approval 3 months ahead of schedule

---

## THESIS FAILURE TRIGGER

If a **Critical Impact** catalyst misses by >90 days with no credible revised timeline:
1. Immediately reduce position to 5% ("monitor-only" sizing)
2. Conduct emergency post-mortem within 7 days
3. Reclassify company from Tier 1 to Watchlist
4. Update TABLE.md and TITANITE-HOLDINGS.md

This is a mandatory risk management protocol, not discretionary.

---

## TEMPLATE FOR ADDING NEW CATALYSTS

When initiating a new Tier 1 position or updating an existing thesis, add catalyst(s) to the tracker using this format:

```markdown
| **[TICKER]** | [Brief catalyst description] | [Expected Date: Qx YYYY or Month YYYY] | [High/Medium-High/Medium/Low] | _Pending_ | — | [How this affects the thesis if missed] | 🟡 Active |
```

**Minimum Requirements:**
- Every Tier 1 position must have at least 1 tracked catalyst
- Catalyst must be time-bound (specific quarter or month, not "H2 2027")
- Impact on thesis must be quantified ("Revenue inflection" / "Regulatory de-risking" / "Balance sheet risk mitigation")

---

_Last Updated: 14 June 2026_
_Next Review: 1 July 2026_
