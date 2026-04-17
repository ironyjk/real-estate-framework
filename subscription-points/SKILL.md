---
name: subscription-points
version: "0.1.0"
description: "Subscription (청약) points system strategy — points calculation (non-homeownership, dependents, account), general vs. special supply selection, lottery combinations, special supply eligibility assessment. The game theory created by Korea's subscription system."
---

# Subscription (청약) Points Strategy

## One-Line Summary

Subscription (청약) is a game of **points + eligibility + timing**. The key is finding the pool that matches your points and eligibility, and selecting complexes with high winning probability.

## Regulatory Overview

- Legal basis: **Housing Act (주택법)**, Rules on Housing Supply.
- Administered by: **Korea Real Estate Board Subscription Home (한국부동산원 청약홈)** (applyhome.co.kr).
- Purpose: Priority housing supply for non-homeowners and actual-demand buyers.

## Points Calculation (Max 84 points)

### 1. Non-Homeownership Period (Max 32 points)
- Non-homeownership period recognized from age 30
- Upon marriage, recognized from marriage registration date (even if married before age 30)
- 2 points added per year (less than 1 year: 2 points, 15+ years: 32 points)
- If **prior home ownership** history exists, recalculated from date of sale

### 2. Number of Dependents (Max 35 points)
- Dependents excluding the applicant
- Spouse, lineal ascendants (same household registration for 3+ years), lineal descendants (unmarried, under age 30)
- 0 persons: 5 points, 1 person: 10 points, ..., 6+ persons: 35 points
- **Number of children is the biggest variable**

### 3. Subscription Account Holding Period (Max 17 points)
- Less than 6 months: 1 point, 6 months–1 year: 2 points, ..., 15+ years: 17 points
- **Points transfer upon name change** (between spouses, household head change)

## Supply Types

### General Supply

| Type | Points System Ratio | Lottery Ratio |
|---|---|---|
| Speculative Overheated District, 60㎡ or less | 40% | 60% (2023.4 reform) |
| Speculative Overheated District, 60–85㎡ | 70% | 30% |
| Speculative Overheated District, over 85㎡ | 80% | 20% (high-point holders dominant) |
| Adjustment Target Area, 60㎡ or less | 0% | 100% |
| Adjustment Target Area, 60–85㎡ | 30% | 70% |
| Adjustment Target Area, over 85㎡ | 50% | 50% |
| Non-regulated area, 85㎡ or less | 40% | 60% |
| Non-regulated area, over 85㎡ | Lottery 100% | — |

*Regulated area scope and ratios have changed since 2024 — must reconfirm based on subscription (청약) timing*

### Special Supply (특공, as of 2026.4)

| Type | Eligibility | Share |
|---|---|---|
| Newlyweds | Within 7 years of marriage, or prospective/single-parent. **From 2024~, weighted by presence/number of children** | 30% |
| Multi-child families | **2+ minor children (2024.3 eased, previously 3+)** | 10% |
| First-time homebuyers | Lifelong non-homeowner, married or single-person household | 20% |
| Elderly parent support | Supporting lineal ascendants aged 65+ for 3+ years | 3% |
| Institutional recommendation | National merit holders, disabled persons, SMEs, etc. | 10% |
| **Newborn Special Supply (신생아 특공, newly established 2024.3)** | Non-homeowner households with children aged 2 or younger, 70,000 units supplied annually | Priority in public sale |

Total special supply ≈ 73–83% (including newborn, varies by region)

### Points System vs. Lottery Ratio Reform (from 2023.4)

- **Speculative Overheated District, 60㎡ or less**: Points system 40% / **Lottery 60%** (previously 100% points → lottery share dramatically expanded)
- **Speculative Overheated District, 60–85㎡**: Points 70% / Lottery 30%
- **Over 85㎡**: Points 80% / Lottery 20% (high-point holders dominant, detailed rules need confirmation)
- Purpose: Expand winning opportunities for younger generations and single-person households (centered on small 60㎡ or less)
- *Designed to favor high-income households with low points* — paradoxically, criticism of "parental assistance" influx

## Winning Probability Function

$$P_\text{winning} = f(\text{applicant points}, \text{complex points cutoff}, \text{lottery competition rate}, \text{regional priority})$$

- **Regional priority**: Priority for regional residents and regionally allocated units → 1-year/2-year residency requirement in metropolitan overpopulated areas
- **Lottery system**: Luck-based even with low points. Especially for newlyweds, first-time homebuyers, and multi-child families, the lottery share is high.

## When to Use

- Subscription (청약) vs. purchase decision
- Special supply eligibility assessment (newlyweds, multi-child, first-time, elderly parent support)
- Lottery strategy when points are uncompetitive
- Account maintenance and deposit strategy
- Calculating actual gains from winning a price-capped unit

## Korean Market Application Points

### 1. Points Inflation

- 2020–2022 metropolitan area cutoff: 60–70 points
- Perfect score (84 points) = 15 years non-homeownership + 6 dependents + 15 years account = nearly impossible
- **Below 55 points is effectively impossible for popular metropolitan complexes**
- Regional and less-popular complexes possible with 40–50 points

### 2. Households with 3 Children on Special Track

- Multi-child special supply: 3 children + income and asset requirements
- Already advantaged in *general points system* due to dependents
- **Selection strategy**: Apply for multi-child special supply first; if rejected, reapply for general points

### 3. Regulatory Easing Trend (from 2023)

- Expanded lottery ratio → more opportunities for younger generations
- First-time homebuyer single-person households allowed
- Weighting for newlywed couples based on children
- *However, policy changes are frequent, so regulations must be reconfirmed right before subscription (청약)*

### 4. Value of Winning a Price-Capped Unit (as of 2026.4)

- Upon winning, immediate 20–50% premium over market price (varies by region)
- **Resale restrictions**:
  - Metropolitan public land price-capped: 3–10 years
  - Private land price-capped: 1–3 years (significantly eased 2023.4)
  - Speculative overheated district private: 1 year (re-winning restrictions separate)
- **Actual residency obligation**:
  - Government announced abolition plan in 2023.4 but pending in National Assembly → **Housing Act amendment in 2024.2 granted 3-year grace period** (not abolition; actual residency must begin within 3 years of initial move-in date)
  - Regulatory uncertainty persists. Upon winning, check original contract and announcement text.
- Short-term sale not possible → long-term holding strategy
- Need funding plan for sale price and intermediate payments

### 4-1. Unranked (줍줍)

- 2023.2 easing → *all citizens can apply* (non-homeownership and regional requirements abolished)
- Regulations fluctuate with 2024 residency obligation revival debates
- Overheating as "lottery 줍줍" → must reconfirm eligibility per supply complex
- Contract-forfeiting households return to market via unranked → opportunities at 20–40% discount to market price

### 5. Subscription Home Practical Tips

- Use subscription (청약) points calculator (on your own)
- Accumulate public data on competition rates and cutoffs
- Compare complexes with similar location and price ranges
- Must verify actual residency requirement and mandatory residency period conditions

### 6. Pitfalls

- **Timing of existing home sale**: If not disposed of by move-in, winning is canceled or deemed illegal
- **Household head requirement**: Certain supply types require household head status
- **Past winning history**: Re-winning restriction period
- **Miscalculation of dependents**: Disqualified if household registration actual residency requirements unmet

## Usage Procedure

```
1. Calculate points
   - Non-homeownership + dependents + account = X points
2. Identify applicable pool
   - Competitive in general points system? (cutoff vs. your points)
   - Special supply eligible? (newlywed/multi-child/first-time/elderly parent support)
3. Select target region and complex
   - Your residence and living area
   - Cutoffs of similar past complexes
   - Upcoming supply calendar (builder, local government websites)
4. Funding plan
   - Intermediate payment 60% / final payment 30% schedule
   - DSR and final payment loan feasibility
5. Winning scenarios
   - Fulfill actual residency obligation
   - Resale restriction period
   - Timing of existing home disposal
6. Rejection alternatives
   - Monitor 줍줍 (unranked)
   - Switch to purchase
   - Maintain account
```

## Korean Context Examples

**Question**: "Resident of Ulsan, 3 children, non-homeowner for 10 years, account for 15 years — possibility of metropolitan subscription (청약)?"

**Points Calculation**:
- Non-homeownership 10 years: 22 points
- 4 dependents (spouse + 3 children): 25 points
- Account 15 years: 17 points
- **Total: 64 points**

**Strategic Analysis**:
- Metropolitan general points system cutoff: 55–70 points (varies by complex)
- 64 points possible for mid-tier metropolitan complexes, impossible for popular complexes (Gangnam area)
- **Regional priority** unmet (metropolitan residents prioritized) → outranked by metropolitan 1st-tier residents
- Alternative 1: Multi-child special supply (if income/asset requirements met) — lottery
- Alternative 2: Regional (Ulsan, Gwangju, Daegu) complex points system → virtually certain
- Alternative 3: Switch to purchase in Ulsan premium area (trading up)

**Recommendation**: Explore metropolitan only as opportunity; main focus on *Ulsan premium area purchase* + *parallel multi-child special supply*.

**Question**: "Non-homeowner for 2 years, no children, account for 3 years — should I apply?"

**Analysis**:
- Points: 4 + 5 + 5 = **14 points** → points system meaningless
- **Lottery-focused** strategy needed
- Non-regulated area lottery 60–75%, speculative overheated 60% → good lottery pool
- Utilize first-time homebuyer special supply (20%) and newlywed special supply (30%)
- **Long-term strategy based on account maintenance + family expansion plans**

## Limitations

1. **Frequent policy changes** — Points and lottery ratios, special supply scope, and regional priority regulations change often.
2. **Short-term luck factor** — Lottery is probabilistic. Difficult to make plans.
3. **Financial capacity not reflected** — Even with high points, must forfeit if unable to pay intermediate and final payments.
4. **Sale price risk** — With high sale prices, winning premium is thin and actual residency burden heavy.
5. **Large competitive environment variance** — Seoul vs. regional areas are entirely different games.
6. **Information game** — Builder and supply schedules are determined by information accessibility.

## When This Framework *Is Wrong*

- Comparing purchase timing → `harrison-cycle`, `dipasquale-wheaton`
- Comparing subscription rights vs. existing purchase value → `hedonic-pricing`
- Redevelopment/reconstruction association member eligibility → `redevelopment-feasibility`

## Additional Learning Resources

- Korea Real Estate Board Subscription Home (applyhome.co.kr) — Official materials and points calculator.
- Rules on Housing Supply — Check original text.
- Ministry of Land, Infrastructure and Transport housing/urban policy materials.
- **Warning**: Many "subscription (청약) tips" on YouTube and blogs are based on old regulations. Amendments after 2024 must be verified against original text on Subscription Home.
