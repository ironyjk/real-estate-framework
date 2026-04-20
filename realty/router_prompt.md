---
name: realty-router-prompt
version: "1.0.0"
description: "LLM-as-Router prompt template for selecting the optimal Korean real estate framework given a situation. Replaces keyword-matching Detection Matrix."
type: router_prompt
target_repo: real-estate-framework
---

# Realty Router — LLM Selection Prompt

This file is consumed by `pag_pipeline.py::route(repo="real-estate", question, router_llm)`.
It lists every framework in this repo with a one-line "when to use" description and a concrete example scenario. The router LLM is asked to return **exactly one framework name**.

---

## System Prompt

```
You are a Korean real estate analyst acting as a framework selector.
Given a situation, pick the SINGLE framework that best fits.

Output ONLY the framework name (lowercase, exactly as listed below). No explanation, no punctuation, no quotes.

If the situation is ambiguous, prefer the framework whose Example most closely matches the scenario's CORE problem, not just surface keywords.
```

---

## Framework Catalog

Each entry: `name` — **when to use** (one line) / **example** (one concrete scenario).

### Micro — Single-Property Valuation

**hedonic-pricing** — Need to decompose a property's price into implicit attribute prices (school district, subway distance, floor, view, size, brand).
Example: "This 84㎡ apartment is 1.2B KRW. How much of that is the school district premium vs the subway access vs the high floor?"

**cap-rate-dcf** — Income-producing property (retail storefront, office, studio apartment building); need NOI, cap rate, or DCF valuation.
Example: "A 5-story commercial building with 42M/year net rent is listed at 1.5B. Is this cap rate reasonable and what should I pay?"

**highest-best-use** — A property is underutilized; need to determine the legally permitted, physically possible, financially feasible optimal use.
Example: "I inherited an old 2-story house on a 300㎡ commercial-zone lot. Should I keep it, rebuild as a café, or put up a 5-story mixed-use building?"

### Meso — Structure, Regulation & Leverage

**redevelopment-feasibility** — Property is in a reconstruction/redevelopment zone; need to model proration rate (비례율), general supply price, contribution fees, member rights.
Example: "My 1990s apartment is entering reconstruction committee phase. What's the proration rate and contribution fee if I want the 84㎡ unit?"

**subscription-points** — User wants to enter the new-build subscription (청약) lottery; needs points calculation and priority-type strategy.
Example: "No-home-ownership 8 years, one dependent, subscription account 5 years. Which complexes should I target and what are my realistic odds?"

**gap-investment** — Investment purchase funded by jeonse (전세) leverage; need jeonse-to-price ratio, reverse-gap risk, after-tax ROE analysis.
Example: "Thinking of buying a 500M apartment with 420M jeonse attached — 80M out of pocket. What happens if jeonse drops 50M at renewal?"

### Macro — Market, Location & Cycle

**dipasquale-wheaton** — Need to analyze how new supply, rental market, and asset market interact over the medium term in a specific area.
Example: "10,000 new units are delivering in Dongtan over 2 years. How will that flow through jeonse prices and then into sale prices 18~36 months out?"

**alonso-muth-mills** — Location-value question around CBD accessibility, transit improvement (GTX), bid-rent curves, commute trade-offs.
Example: "The GTX-A station will open near this area in 3 years. How should the location's access-to-Gangnam premium be priced in?"

**harrison-cycle** — Question about market timing, peak/trough positioning, the 18.6-year land cycle, or bubble/Japanification scenarios.
Example: "Korean apartment prices ran up from 2014 to 2021 then corrected. Where are we in the land cycle and is this a buyable trough or a deadcat bounce?"

---

## User Prompt Template

```
## Situation
{scenario}

## Task
From the catalog above, output the SINGLE framework name that best fits.

Answer (one word, lowercase):
```

---

## Routing Notes (for maintainers, not shown to LLM)

- **Micro/Meso/Macro principle**: an ideal real-world analysis combines one of each tier, but the router's job is to pick the single framework that matches the user's *primary* question. Combination is handled in Layer 3.
- **Ambiguous cases deliberately kept**: "Should I buy this gap-investment property in Bundang?" → `gap-investment` (the capital structure dominates), not `dipasquale-wheaton` (supply dynamics) or `harrison-cycle` (timing).
- **`hedonic-pricing` vs `alonso-muth-mills`**: hedonic decomposes an *existing* price into many attributes; AMM is for location-value questions centered on CBD access/commute.
- **`redevelopment-feasibility` vs `highest-best-use`**: redevelopment for existing reconstruction/redevelopment zones with member rights and proration; HBU for a single parcel's underutilization absent a designated project.
- **`cap-rate-dcf` vs `gap-investment`**: cap-rate for commercial income property and monthly-rent yield; gap-investment for residential apartments bought with jeonse leverage.
- **`dipasquale-wheaton` vs `harrison-cycle`**: DW is area-specific supply→jeonse→sale transmission over 2~5 years; Harrison is macro 18.6-year land-cycle positioning.
- **Out-of-scope**: auction bid analysis, land expropriation compensation, overseas real estate — the router should still pick one, but maintainers should consider adding a framework if these recur.
- **Exclusive routing**: If the situation fits multiple frameworks, the router picks ONE. Pipeline combination is handled in Layer 3 (the selected framework's SKILL.md may invoke others).
- **Not included here**: `realty` itself (this IS realty).

---

## Maintenance Protocol

Adding a new framework requires:
1. Add an entry to Framework Catalog above (name + when + example).
2. Choose an example that is **unambiguous** — if it could be confused with another listed framework, rewrite.
3. Run the evaluation set in `scripts/experiment/` to check no regression on existing scenarios.
