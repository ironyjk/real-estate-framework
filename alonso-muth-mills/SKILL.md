---
name: alonso-muth-mills
version: "0.1.0"
description: "Alonso-Muth-Mills location theory — models the trade-off between downtown accessibility and housing cost via the bid-rent curve. Analyzes why downtown is expensive, commute time vs. home price trade-offs, and how GTX/subway openings affect prices."
---

# Alonso-Muth-Mills Monocentric City Model

## One-Line Summary

Households minimize the total cost combining **commuting cost** and **housing cost**. The result is a **bid-rent curve** in which land prices decline with distance from downtown.

## Theoretical Origins

- **Alonso, W. (1964)** — *Location and Land Use*. The original.
- **Muth, R. (1969)** — *Cities and Housing*. Application to the housing market.
- **Mills, E. (1967, 1972)** — Empirical extension to urban structure.
- The standard model in urban economics. Later extended by Wheaton, Anas, Glaeser, and others.

## Core Concepts

### 1. Bid-Rent Curve

Willingness to pay for land at distance $x$ from the CBD (downtown):
$$R(x) = R_0 - t \cdot x$$

- $R_0$: CBD land price
- $t$: commuting cost per unit distance (including time value)
- Slope = *steeper for those with higher time value*

### 2. Sorting by Income

- High income · high time value → concentrates downtown, steep bid-rent
- Low income · low time value → suburbs, gentle bid-rent
- **Market clearing**: at each distance, the highest bidder wins

### 3. Land → Housing Price

$P_\text{housing} \approx R \cdot \text{floor area ratio} + $ construction cost
→ If the floor area ratio is restricted, land scarcity ↑ → downtown housing prices rise further

## When to Use

- "If GTX opens, how much will this area rise?" — effect of a reduction in effective $x$
- "How does the spread of remote work affect location value?" — $t$ falls → bid-rent flattens → suburban premium
- "Why is Gangnam accessibility so expensive?" — $R_0$ of Gangnam in a polycentric structure
- "How to judge location when relocating to a provincial city" — mini-CBD structure of regional cities
- "Will new towns replace existing downtown?" — testing the polycentric hypothesis

## Application Points for the Korean Market

### 1. Korea Is Not Strictly Monocentric — Extend to a Polycentric Model

- **Seoul's multiple cores**: Gangnam (GBC · Teheran-ro), Yeouido (finance), Gwanghwamun (public sector · large conglomerates), Guro/Gasan (IT), Magok (bio), Pangyo (tech · ventures)
- **Anas-Arnott-Small (1998)** theory: In a polycentric city, each employment center $j$ generates its own bid-rent:
  $$R(x) = \max_j \left[ R_{0j} - t_j \cdot x_j \right]$$
  (at each location, bidding is based on the *nearest or most attractive* CBD)
- Bid-rent curves from each core *overlap* → intersection areas become super-premium
- **Glaeser & Kahn (2004)** — empirical study of employment dispersion: suburbanization is the modern phenomenon of bid-rent flattening
- Result: the Han River line with good access to all three Gangnam · Yeouido · Gwanghwamun axes is super-premium. After the Pangyo boom, the **Shinbundang · Bundang line axis** has become a new bid-rent peak.

### 1-1. Korean Specificity: "School District Cores" Act as a Second CBD

- School district cores such as Daechi, Mok-dong, and Junggye are not employment centers but generate an *effective $R_0$*
- For families with school-age children, the school district core has a higher bid-rent than the employment core
- Since 2024~, the ultra-low birth rate has triggered an ongoing debate between the **long-term weakening of the school district premium hypothesis** vs. **strengthening due to concentration among a smaller population**

### 2. Regional Metropolitan Cities Are Closer to Monocentric

- Busan: dual-core structure of Seomyeon and Haeundae
- Daegu: Suseong-gu centered + Dongseongno
- Ulsan: Nam-gu · Samsan · Okdong centered + Ulsan College of Science · Hyundai Heavy Industries employment zone
- **A move from Beomseo in Ulsan to Nam-gu is a textbook "outskirts → CBD" move**

### 3. Korea-Specific Factors That Shake $R_0$

- **School districts** — generate a local $R_0$ independent of the CBD (Mok-dong · Daechi · Junggye)
- **Transit hub effects** — bridge premiums at transfer stations such as Gangnam Station and Hongik University Station
- **Brand towns** — even at identical locations, well-regarded complexes form a mini-$R_0$

### 4. Factors That Change $t$

- **GTX (A/B/C)**: sharp decline in effective distance for the outer metropolitan area → expected surge in bid-rent for Dongtan · Unjeong · Namyangju
- **Remote work**: $t$ falls → suburban preference → clear in the US/Europe, weaker in Korea
- **Oil prices · public transit fares**: minor changes in $t$

### 5. Floor Area Ratio Regulation = Vertical Expansion Constraint

*Artificially* sustains downtown land scarcity → locks in price premium

## Usage Procedure

```
1. Identify relevant CBDs
   - Monocentric? Polycentric? Estimate $R_0$ for each core
2. Measure commute time and cost
   - Time from home → each CBD (public transit/private car)
   - Value of time × time = $t \cdot x$
3. Compare alternative locations
   - Price distribution across neighborhoods within the same commute time band
   - Outliers (why undervalued/overvalued?)
4. Shock scenarios
   - Change in effective $x$ after GTX opens
   - Change in $t$ if remote work becomes entrenched
5. Apply to your situation
   - No commute needed (retirement, remote work) → bid-rent curve loses meaning
   - School-age children → school district core matters more than CBD
```

## Korean Context Example

**Question**: "Upgrading location in Ulsan — Nam-gu Samsan vs. Nam-gu Okdong vs. Jung-gu old downtown?"

**AMM Analysis**:

| Area | CBD Accessibility (Nam-gu employment zone) | School District Core | Estimated Proximity to $R_0$ |
|---|---|---|---|
| Samsan | ◎ Nearest | ○ Average | Highest |
| Okdong | ○ Middle | ◎ (Ulsan school district #1) | Highest once school district premium is included |
| Jung-gu old downtown | △ Far | △ | Middle (reflects old downtown decline) |

*Additional consideration*: Ulsan's employment structure is dispersed across Hyundai Heavy Industries (Dong-gu) and petrochemicals (Nam-gu · Ulju) → not strictly monocentric. $x$ must be recalculated based on the family's commuting destination.

**Question**: "Near Dongtan Station on GTX-A — is buying now the right call?"

**AMM Analysis**:
- Current $x$ (about 90 min to Gangnam by car, 100 min by bus)
- $x$ after opening (20 min via GTX) → effective $x$ reduced by ~70%
- Savings on $t \cdot x$ → bid-rent rises → check whether the price premium has already been priced in
- Caveat: opening delays, headway intervals, and transfer burdens create a gap between "theoretical $x$" and "perceived $x$"

## Limitations

1. **Gap with polycentric reality** — the circular model assumes a single CBD. Does not fit Korean reality.
2. **Commute-centric assumption** — weak explanatory power for retirees, remote workers, and households without children.
3. **Exogenous school district · environment** — the school district premium often outweighs CBD accessibility.
4. **Policy · transit infrastructure shocks** — major changes such as GTX are hard for the model to handle (price reflection across announcement · delay · opening stages).
5. **Psychological distance ≠ physical distance** — brand effects such as "Gangnam lifestyle area" are not captured in $x$.

## When This Framework Is *Wrong*

- Analysis of school district · structural attributes → `hedonic-pricing`
- Short-term supply · demand dynamics → `dipasquale-wheaton`
- Cycle perspective → `harrison-cycle`
- Re-creating location value via redevelopment → `redevelopment-feasibility` + `highest-best-use`

## Further Reading

- Alonso, W. (1964). *Location and Land Use.* Harvard University Press.
- Muth, R. (1969). *Cities and Housing.* University of Chicago Press.
- Glaeser, E. (2011). *Triumph of the City.* — Modern extension.
- Domestic: Korea Research Institute for Human Settlements urban spatial structure reports, metropolitan wide-area transportation network impact analyses.
