---
name: gap-investment
version: "0.1.0"
description: "Gap Investment Structure — a housing investment model using jeonse (전세) leverage. Jeonse-to-price ratio, reverse-gap risk, ROE, cash flow tracking, and an economic dissection of the Korean jeonse system."
---

# Gap Investment (갭투자) Structure

## One-Line Summary

**Sale price − Jeonse deposit = Gap (equity)**. The jeonse deposit is used as an *interest-free loan* to purchase a home. When sale prices rise, leverage is maximized; when they fall, reverse-gap (역전세) and "underwater jeonse" (깡통 전세) risks emerge.

## Theoretical Position

- A structure created by Korea's unique jeonse (전세) system. Different from Anglo buy-to-let (which is interest-bearing-loan-based).
- No formal academic theory. **From a financial engineering perspective, can be interpreted as a short put option + long housing position.**
- Jeonse deposit = interest-free, unsecured short-term debt. From the tenant's perspective, it serves as a *principal-guaranteed savings* substitute.

## Core Structure

### 1. Basic Formula

$$\text{Gap} = \text{Sale Price} - \text{Jeonse Deposit}$$
$$\text{Jeonse-to-Price Ratio} = \frac{\text{Jeonse Price}}{\text{Sale Price}} \times 100\%$$

- Jeonse-to-price ratio 0.7 → Gap 30%
- Jeonse-to-price ratio 0.9 → Gap 10% (extreme leverage)

### 2. Return (Simplified)

$$\text{ROE} = \frac{\text{Sale Price Appreciation} - \text{Costs}}{\text{Gap (Equity)}}$$

Example: Sale 1B KRW, jeonse 800M, gap 200M. If sale price rises 10% (to 1.1B):
$$\text{ROE} = \frac{100M - \text{Costs}}{200M} = 50\% \text{ (approx.)}$$

5x leverage effect.

### 3. Cost Structure

| Item | Approx. |
|---|---|
| Acquisition tax | 1~4% (8~12% for multi-home owners in regulated zones) |
| Brokerage commission | 0.4~0.6% (at sale) |
| Legal/stamp fees | Small amount |
| Property tax & comprehensive real estate tax (종부세) during holding | 0.1~2% annually (heavy surcharge for multi-home owners) |
| Rental income tax | Separate taxation possible if under 20M KRW |
| Repairs, wallpaper, flooring | At tenant turnover |
| Capital gains tax at sale | 6~45% depending on holding period and multi-home status |

### 4. Jeonse Renewal & Refund Cycle

- Re-contract every 2 years (tenant's contract renewal request right grants 1x extension of 2 more years = up to 4 years total)
- 5% cap on jeonse increase at renewal (Three Tenancy Acts (임대차 3법); deregulation under discussion)
- Obligation to refund jeonse deposit when tenant moves out → either find new tenant or use own funds

## Major Risks

### 1. Reverse Gap (역전세, Reverse Gap)

$$\text{Reverse Gap Burden} = \text{Existing Jeonse} - \text{New Jeonse}$$

- Occurs when jeonse market price drops
- When tenant requests to move out, *the difference must be paid by the owner*
- Reverse-gap crisis materialized in Seoul Metro and provincial metropolitan areas in 2022~2024
- **HUG Jeonse Deposit Refund Guarantee 126% Rule (effective May 2023)**:
  - Eligible for guarantee only if within 126% of officially appraised price (was 150% until 2022)
  - If exceeded, tenant cannot obtain guarantee → tenants avoid → jeonse price falls → owner takes hit
  - *Older or high-priced jeonse listings face pressure to reset jeonse to non-guaranteed levels* (capped at 126% of official price)
- As of April 2026, accumulated HUG guarantee accidents → trending toward higher premiums and stricter requirements. Periodic verification essential.

### 2. Underwater Jeonse (깡통 전세)

- State where sale price ≤ jeonse deposit
- Even after selling, insufficient to repay jeonse
- Priority issues at auction (jeonse rights/fixed-date confirmation)

### 3. Interest Rate Risk

- Rising jeonse loan rates → increased tenant burden ↑ → preference for monthly rent · jeonse demand ↓ → jeonse price falls
- Double burden if owner also has loans

### 4. Tax Risk

- Comprehensive real estate tax (종부세) and capital gains tax surcharges for multi-home owners
- Especially high under corporate ownership
- Vulnerable to policy changes (2020~2022 surcharge intensification → 2023 deregulation discussions)

### 5. Liquidity Risk

- Market cooling when wishing to sell → difficult disposal
- Distressed sale discount of 10~20%
- Larger price discount when selling with jeonse attached

## When to Use (As an Analytical Tool)

- Personal or peer's gap investment decision-making
- Reverse-gap scenario response
- Interpreting what jeonse-to-price ratio means market-wide
- Risk assessment of multi-home owner positions
- Sell vs. continue-holding judgment

## Korean Market Application Points

### 1. Jeonse-to-Price Ratio Interpretation Guide

| Jeonse-to-Price Ratio | Interpretation | Implication |
|---|---|---|
| 80%+ | Sale price stagnation/decline signal, gap investment overheating | Possibility of imminent correction |
| 65~80% | Normal range | Neutral |
| 50~65% | Expectations of sale price increase priced in | Early-mid bull market |
| Below 50% | Bubble or special jeonse market situation | Suspect sale price overvaluation |

### 2. Pitfalls of Gap Investment ROE

- **Favorable only in bull markets**. In bear markets, the loss is leveraged at the same multiple.
- *Reverse-gap funding cost* often omitted from calculations.
- Costs (acquisition tax, holding tax, capital gains tax) can deduct 30~60% of returns — calculate after-tax ROE.

### 3. Structural Changes in the Jeonse Market Since 2023

- *Jeonse avoidance* phenomenon due to jeonse fraud aftermath
- Increased share of monthly rent (deposit + monthly rent hybrid)
- **Pure gap investment environment deteriorated**
- Jeonse increase limits via contract renewal request right and jeonse/monthly rent cap
- Some regions require "gap + monthly rent" hybrid structure

### 4. Multi-Home Owner Surcharge System (as of April 2026, subject to change)

- **Acquisition tax**:
  - Current statutory rate: 8% for 2 homes in regulated zone, 12% for 3+ homes (effective Aug 2020)
  - Government deregulation proposal announced Dec 21, 2022: general rate (1~3%) for 2 homes, 4% for 3 homes, 6% for 4+ homes/corporations — *Local Tax Act amendment pending in National Assembly; legislative status as of April 2026 requires re-verification*
  - First-time-acquisition acquisition tax exemption capped at 2M KRW (2022~)
- **Capital gains tax**:
  - +20%p surcharge for 2 homes, +30%p surcharge for 3+ homes
  - Temporarily exempted May 2022 ~ May 2026 (multi-home surcharge moratorium — extension is a political issue)
  - Long-term holding special deduction up to 30% over 15 years (excluded for multi-home owners)
- **Comprehensive real estate tax (종부세)**: Progressive on aggregated official prices, 1.2B KRW deduction for single-household single-home, 900M for multi-home. High rates for corporations.
- **DSR (Debt Service Ratio)**:
  - Stress DSR: Phase 1 Feb 2024 (bank mortgage loans), **Phase 2 Sep 2024** (expanded to secondary financial sector and credit loans), **Phase 3 Jul 2025** (full application across all sectors, 1.5%p rate add-on)
  - DSR cap of 40% (banks) / 50% (secondary) relative to annual income
  - *Gap investment has small direct constraints due to low personal borrowing, but at sale, buyer's loan constraints → impact on sale price and liquidity*
- **First-time-acquisition LTV 80%** (2022~): All regions including speculation zones, no price limit. Loan cap 600M KRW. Favorable environment for gap investment competitors.
- *Current regulations must be confirmed with tax accountant and loan consultant*

### 5. Reverse-Gap Response Options

- Funding: credit loans · jeonse deposit refund loans · existing home mortgage loans
- Find new tenant: convert jeonse → semi-jeonse (반전세, deposit + monthly rent)
- Sell: sell with jeonse attached (discount) or vacate then sell
- Convert to owner-occupied

## Pre-Purchase Due Diligence Checklist

### Registry Verification (As Tenant + As Buyer)
- [ ] **Section 1 (갑구)**: Ownership change history, presence of provisional attachment/disposition/auction commencement
- [ ] **Section 2 (을구)**: Mortgage·jeonse rights·tenancy registration — *senior claim total + my jeonse deposit ≤ 70% of market price* is the safety standard
- [ ] Trust registration status — trust properties require trustee consent; jeonse contracts without it cause guarantee denial
- [ ] **Building register** vs registry consistency — verify unauthorized extensions and illegal buildings
- [ ] Official price × 126% vs jeonse price (HUG guarantee eligibility)

### Sale Simulation
- [ ] Expected price difference: sell with jeonse attached vs sell after vacating (typically 5~15% discount)
- [ ] Time required to sell (Seoul metro avg. 3~6 months, provinces 6~12 months, bear market 12+ months)
- [ ] **Number of transactions in the same complex over the past 6 months** (liquidity indicator) — 0~1 transactions means high difficulty selling
- [ ] Asking-actual price gap (asking price illusion vs true market price)

### Tenant Risk
- [ ] Existing tenant's **jeonse refund schedule** (contract expiration, whether renewal request right has been used)
- [ ] Allocation of moving schedule, moving cost, repair cost burden
- [ ] Tenant's occupation/income stability (disputes if jeonse loan goes delinquent)

## Procedure for Use (At Decision-Making Time)

```
1. Calculate gap size and leverage
   - Sale price - jeonse price = gap
   - Gap ratio relative to own available funds

2. Scenario analysis (3 cases)
   - Up 10%, flat 0%, down 10%
   - ROE, loss amount, cash flow per scenario

3. Reverse-gap stress test
   - Refund burden when jeonse falls -10%, -20%, -30%
   - Own cash and loan capacity vs burden
   - Endurance period (what if reverse-gap happens within 2 years?)

4. After-tax return
   - Deduct all of: acquisition tax, holding tax, capital gains tax
   - Scenarios by holding period

5. Liquidity check
   - Time required to sell (by market condition)
   - Distressed sale discount rate

6. Personal position fit
   - Can cash flow be sustained?
   - Risk of needing funds within 2~3 years?
   - Family/career change risks
```

## Korean Context Examples

**Question**: "Seoul metro apartment 800M KRW, jeonse 600M. Should I enter with a 200M gap?"

**Analysis**:
- Jeonse-to-price ratio 75% → upper end of normal range
- Acquisition tax (assuming 2 homes, regulated zone) 8% = additional 64M needed → **effective equity 264M**
- Scenarios:
  - Up 10% (940M - 800M) = 140M - capital gains tax → after-tax approx 90M → ROE 34%
  - Flat 0%: holding tax/repairs accumulating 1~2M annually, -5~10M over 5 years → loss
  - Down 10% (720M): 80M loss, **40% loss** relative to own equity of 200M (per calculation)
- Reverse-gap stress: if jeonse drops 600M → 500M, additional 100M funding needed. *Possible?*

**Decision Checklist**:
- [ ] Can you absorb 100M reverse-gap in 2 years?
- [ ] Can you absorb several million KRW in annual multi-home comprehensive real estate tax (종부세)?
- [ ] Willingness to hold 5+ years?
- [ ] Basis for market upturn outlook?
- [ ] Comparison of opportunity cost (other investments)?

If not all Yes, **reconsider**.

**Question**: "Already holding a gap investment, 50M reverse-gap occurred — what now?"

**Response Order**:
1. Verify immediately available cash
2. Search for new tenant candidates (semi-jeonse conversion possible?)
3. Jeonse deposit refund loan eligibility (varies by bank product)
4. Existing home mortgage loan capacity (LTV·DSR)
5. Sale possibility (cost comparison: sale with jeonse attached vs sale after vacating)
6. **Negotiate with tenant**: contract extension + maintain existing jeonse price as a condition

→ Most to be avoided: delay in jeonse deposit refund → legal disputes, credit damage, reputation harm.

## Limitations (of This Framework)

1. **Bull market bias** — A model created by the 2014~2021 Seoul metro bull market. Limited applicability in an era of demographic and structural change.
2. **Psychological and political factors** — Discussions of jeonse system reform itself can shake the model's premise.
3. **Extreme regional disparity** — Seoul metro vs provinces, regulated vs non-regulated zones are completely different games.
4. **Tax complexity** — After-tax returns shift dramatically depending on combinations of individual/corporate, number of homes, holding period, and regulated zone.
5. **Jeonse fraud externalities** — Some cases damage trust in the entire market.
6. **Regulatory direction uncertainty** — Policy variables include contract renewal, cap system, mandatory guarantees, refund guarantee mandates, etc.

## When This Framework Is *Wrong*

- Precise valuation of a single property → `hedonic-pricing`, `cap-rate-dcf`
- Structure of sale and jeonse market interaction → `dipasquale-wheaton`
- Cycle timing → `harrison-cycle`
- Owner-occupied/school district decisions → `hedonic-pricing`, `alonso-muth-mills`

## Additional Learning Materials

- Original text of the Housing Lease Protection Act, Three Tenancy Acts (임대차 3법).
- Korea Real Estate Board's monthly rent and jeonse price index, jeonse-to-price ratio statistics.
- HUG Jeonse Deposit Refund Guarantee system.
- **Caution**: "Gap investment success stories" on YouTube and blogs are bull-market samples. Bear-market failure cases (jeonse fraud, reverse-gap bankruptcy) are systematically less exposed in media. May distort the actual risk distribution.

## Ethical & Legal Cautions

Gap investment itself is legal, but:
- Civil/criminal liability for failure to fulfill jeonse refund obligation
- Criminal punishment for jeonse fraud (deception, intent)
- Duty to respect tenant rights and disclose information
- This framework is an analytical tool *for managing one's own assets*, not for inciting speculation targeting tenants.
