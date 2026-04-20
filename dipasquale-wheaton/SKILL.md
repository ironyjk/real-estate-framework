---
name: dipasquale-wheaton
version: "0.2.0"
description: "DiPasquale-Wheaton 4-Quadrant Model — visualizes how the rental market, asset market, construction market, and stock market interlock to create equilibrium/disequilibrium. Use for interpreting home-swapping, supply shocks, jeonse (전세) transmission, and sale-jeonse price divergence."
---

# DiPasquale-Wheaton 4-Quadrant Model

> Background and theory: Read references/foundation.md



## When to Use

- "How much will the move-in supply shock hit sale prices?" — Path 4→1→2
- "Why are sale prices holding up when jeonse (전세) is falling?" — Lag and divergence between 1 and 2
- "Timing for home-swapping" — compare local imbalances between the sell-side market (Quadrant 2) and buy-side market (Quadrant 2)
- "Which market gets hit first when rates rise?" — Quadrant 2 $i$ change → propagation
- "Impact of the price cap on new apartments" — distortion of the $P→C$ link in Quadrant 3

## Application Points for the Korean Market

### 1. Korea-Specific: The Jeonse System

Jeonse (전세) is both a substitute for monthly rent and an *interest-free loan*. In the 4Q model:

- Quadrant 1: Instead of a single rent, there is a **dual structure of jeonse deposit + monthly rent**
- Quadrant 2: Gap investment distorts the $P = R/i$ relationship. Jeonse leverage can push $P$ up *independently of $R$*
- Result: **A jeonse-to-sale ratio approaching 1.0 signals gap-investment overheating; below 0.4 signals a cooling market**

### 2. Impact of the Price Cap on New Apartments

Breaks the $C = f(P)$ link in Quadrant 3:
- Even as market prices rise, new subscription (청약) prices are regulated
- → Weakens construction incentives (reconstruction delays)
- → Stock supply shortage persists
- → Price appreciation becomes entrenched
- *The opposite of intent* is explained by this model

### 3. Supply Shock Analysis

Example: "30,000 units move into Dongtan in 2025–2026"
- Quadrant 4: $\Delta S$ surges
- Quadrant 1: Jeonse $R$ falls → reverse jeonse (역전세)
- Quadrant 2: Asset price $P = R/i$ comes under downward pressure
- Quadrant 3: New construction $C$ contracts
- **Due to the lag, jeonse moves first, sale prices follow 1–2 years later**

### 4. Interest Rate Shock

Quadrant 2 $i$ rises → $P$ falls
→ Quadrant 3 $C$ decreases
→ Quadrant 4 stock decreases (with lag)
→ Quadrant 1 $R$ rises (long run)
**Short run: prices↓ and jeonse↓ together | Long run: prices↓ but jeonse↑ reversal possible**

## Procedure for Use

```
1. Diagnose current position:
   - Jeonse-to-sale ratio (Quadrant 1 ↔ Quadrant 2)
   - PIR, PRR (price relative to income and rent)
   - Move-in supply (Quadrant 4 forecast)
   - Permits and groundbreaking (Quadrant 3 leading indicator)
   - Interest rates and loan conditions (Quadrant 2)

2. Identify the shock:
   - Which quadrant is currently being shocked?
   - How large?

3. Trace the propagation path:
   - Lagged impact over the next 12/24/36 months

4. Where does your position get hit:
   - Buyer: Quadrant 2
   - Seller: Quadrant 2
   - Tenant: Quadrant 1
   - Gap investor: Quadrants 1+2 combined
```

## Korean Context Example

**Question**: "I'm trying to move up from Beomseo in Ulsan to a higher-tier district. I hear 2025 brings a wave of new supply across metropolitan cities — when should I move?"

**4Q Analysis**:

- **Quadrant 4 (Stock)**: Ulsan move-in supply rises in 2025–2026 (exact figures need confirmation)
- **Quadrant 1 (Jeonse)**: Jeonse starts falling from the move-in date → about 6–12 months
- **Quadrant 2 (Sale price)**: Jeonse decline → gap investors exit → downward pressure on sale prices. Lag of about 12–18 months
- **Sell timing**: Sell the current home *before* jeonse declines (H2 2024 – H1 2025)
- **Buy timing**: Buy the upper-tier property *after* the sale-price correction (H2 2026 – 2027)
- **Intermediate gap**: Consider an "all-in" strategy of renting jeonse in between

*Caveat*: This is model-based reasoning, not a forecast. Interest rates, policy, and region-specific factors can cause deviations.

## Limitations

1. **Insufficient regional granularity** — The original model assumes a single market. Korea's metropolitan area, metropolitan cities, and regional markets follow independent cycles.
2. **Psychology and narrative missing** — The effect of expectations like "housing never loses" or "Japanification" on $P$ is not fully absorbed by $i$.
3. **Exogenous policy shocks** — Multi-home taxation and loan regulations shake the coefficients from outside the model.
4. **Jeonse deposit as capital flow** — In Korea, $R$ is also a capital flow, which the original model cannot fully capture.
5. **Data lags** — Statistical delays differ across Quadrant 1 jeonse, Quadrant 2 actual transaction prices, and Quadrant 3 permits.

## When This Framework Is *Wrong*

- Decomposing price by attribute → `hedonic-pricing`
- Judging the long-term position of the cycle → `harrison-cycle`
- Profitability of a single property → `cap-rate-dcf`
- Structure of locational competitiveness → `alonso-muth-mills`

## Additional Learning Resources

- DiPasquale, D. & Wheaton, W. (1996). *Urban Economics and Real Estate Markets.* Prentice Hall.
- Domestic application: KDI real estate reports, Korea Development Institute housing market analysis series
- Practical references: Move-in supply data (Budongsan114, Asil), jeonse-to-sale ratio (KB Statistics)

