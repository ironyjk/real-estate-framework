---
name: hedonic-pricing
version: "0.2.0"
description: "Hedonic Pricing Model — decompose real estate prices into implicit prices by attribute (school district / proximity to subway / floor / size / view / brand / age, etc.). Rosen 1974. Use this when quantifying how much the school district premium is, or what percentage premium the subway-proximity adds."
---

# Hedonic Pricing Model

> Background and theory: Read references/foundation.md



## When to Use

- "How much premium does the school district add?" — price difference between Building A vs Building B in the same complex when only the school district differs
- "Is the subway-proximity premium justified?" — how much a 500m distance change affects price
- "What's the value of remodeling or improving the view?" — expected price increase when an attribute changes
- "Judging whether a listing is cheap or expensive" — predicted price vs asking price comparison
- "Validating an appraisal" — understanding the structure of the public assessed price and appraised value

## Application Points for the Korean Market

### 1. Attributes with the Strongest Effects in Korea (Empirical Coefficient Guide, Based on Comparison of Similar Complexes)

| Attribute | Estimated Premium | Source/Caveat |
|---|---|---|
| Top-tier school district (Daechi / Mok-dong / Junggye) | **+10~25%** | Range from KDI Seoul school district papers and government research. When in-complex zoning differs, gaps can reach tens of millions to 100M KRW per unit |
| Hyper-subway access (within 200m) | **+5~15%** | Step changes at 500m and 1km thresholds; transfer stations add more |
| Direct Han River view | **+15~30%** | Comparison of view vs no-view units within the same complex (based on actual transaction prices) |
| Brand (top-tier vs second-tier) | **+5~15%** | Raemian / Prugio / Xi / Hillstate vs mid-tier developers |
| Large complex (1,000+ units) | **+3~8%** | Lower management fees, liquidity premium |
| Royal floor (50~80% of total floors) | **+3~10%** vs low floors | Within the same size |
| Pansang (slab) vs Tower type | Pansang **+3~7%** (family units in metropolitan area) | Floor plan preference |
| South-facing vs N/E-facing | South-facing **+2~5%** | Sunlight, dryness, heating costs |
| Cho-poom-a (elementary school inside complex) | **+5~10%** | Family-unit demand |

**Warning**: The above ranges are *empirical intervals* and vary completely by complex. Not a substitute for regression analysis.

### 2. Korea-Specific Attributes
- **Reconstruction expectations** — A reversal where prices *rise as the building gets older* (older complexes in Gangnam, Seoul)
- **Price ceiling on new sales (분양가상한제)** — winning a new-construction subscription (청약) = immediate premium of hundreds of millions of KRW (decoupled from market price)
- **School zoning change risk** — recent zoning adjustments in Gangnam / Mok-dong
- **Floor area ratio headroom** — implicitly reflects reconstruction potential

### 3. Caveats When Estimating
- **Sample bias**: reported transaction price vs asking price vs actual transaction. Use both KB market price and Ministry of Land actual transaction data in parallel.
- **Time-series shifts**: There's a hypothesis that the school district premium is in long-term decline due to low birth rates.
- **Policy shocks**: changes in acquisition tax / capital gains tax shake the coefficients.

### 4. Interfaces with Korean Appraisal Practice

- **Public land price / public assessed price (공시지가·공시가격)**: Calculated by the Korea Real Estate Board and certified appraisers. The *comparable sales method* is the practical variant of hedonic analysis.
- **Comparable sales method** (the dominant method for residential properties): select benchmark comparables → adjust by attribute → derive final appraised value. A condensed version of hedonic Stage 1.
- **Individual factor adjustment rates**: Korean appraisal practice standards present adjustment rate tables by floor / orientation / location / size (±3~15%). A subjective version of hedonic implicit prices.
- **Public-assessed-price reflection ratio of actual transactions**: As of 2026.4, the **target is 65~70%** (after the revision of the government's realization rate roadmap). Slightly increased year-over-year.
- Implication: Appraised values for collateral, taxation, and compensation purposes are *conservative* relative to actual transactions → hedonic analysis based on actual transaction prices takes precedence for purchase feasibility analysis

## Procedure for Use

```
1. Set comparison targets (5~20 similar complexes)
2. List attributes: area, floor, orientation, distance to subway, school district, age, brand, number of units, floor area ratio
3. Collect actual transaction prices (Ministry of Land public API, KB, Hogangnono, Asil)
4. Calculate price differences by attribute:
   - Assuming identical conditions, the price difference between two complexes that differ only in attribute A = the premium of A
5. Map the target listing's attribute vector → derive a predicted price
6. Compare predicted price vs asking price → use as an aid for buy/sell judgment
```

## Korean-Context Example

**Question**: "Raemian A 85㎡ at 1.3B KRW vs Xi B 85㎡ at 1.25B KRW — same neighborhood; which should I buy?"

**Hedonic Decomposition Attempt**:

| Attribute | Raemian A | Xi B | Gap Impact |
|---|---|---|---|
| Age | 5 years | 12 years | +100~150M (new-build premium) |
| Number of units | 2,000 units | 800 units | +30~50M (large complex) |
| Distance to subway | 350m | 800m | +50~100M (hyper-subway access) |
| School district | Identical | Identical | 0 |
| Brand | Raemian | Xi | No difference (both top-tier) |
| Royal floor status | Royal floor | Low floor | +50~100M |

→ Expected justified gap: 150~250M KRW. Actual gap: 50M KRW. **Xi B is potentially relatively undervalued** (or Raemian A hasn't risen as much as it should have).

Additional checks: whether Xi B has any future reconstruction / remodeling issues, management condition, reason for sale.

## Limitations

1. **Omitted variable bias** — unobservable attributes (inter-floor noise, community atmosphere, specific generational influx) get bundled into the coefficients
2. **Endogeneity** — Is it expensive because the school district is good, or does a good school district cluster because it's expensive? (bidirectional)
3. **Market segmentation** — Gangnam / Gangbuk and metropolitan area / regional are different markets. Combining them into one model causes errors.
4. **Vulnerable to short-term shocks** — coefficients shift drastically with policy / interest rate / sentiment changes
5. **Low-transaction items**: For complexes with few transactions, even the implicit price estimation itself is unstable

## When This Framework Is *Wrong*

- Leverage structure (gap investment) issues → `gap-investment`
- Supply-volume issues → `dipasquale-wheaton`
- Income-property valuation → `cap-rate-dcf`
- Cycle-position questions → `harrison-cycle`

## Further Reading

- Rosen, S. (1974). "Hedonic Prices and Implicit Markets." *Journal of Political Economy*.
- Malpezzi, S. (2003). "Hedonic Pricing Models: A Selective and Applied Review."
- Korean empirical work: housing-related reports from the Korea Housing Industry Research Institute and KDI

