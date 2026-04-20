# Subscription (청약) Points Strategy -- Theoretical Foundation

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

