# Real Estate Framework

[한국어](README.ko.md) | **English**

---

A meta-router + framework collection for Korean real estate decision-making.

Bundles academic theory (Hedonic pricing, DiPasquale-Wheaton, Alonso-Muth-Mills), investment analysis (Cap Rate/DCF, Harrison 18.6-year cycle, Highest & Best Use), and Korean institutional frameworks (redevelopment feasibility, subscription-point strategy, gap investment structure) under a single routing layer.

## Design Principles

1. **Translate English-language theory into the Korean market context** — No copy-paste theory. Must reflect Korea-specific factors: jeonse (전세) system, subscription regulations (청약 규제), redevelopment procedures (재건축 절차), etc.
2. **Bridge between retail investor intuition and academic empirics** — Decisions by data and institutions, not narratives like "real estate always wins" vs. "Japan-style stagnation."
3. **Decision support, not answer machine** — Provides thinking frames, not verdicts.

## Structure

```
real-estate-framework/
├── SKILL.md               # Meta-router — situation → framework selection
├── hedonic-pricing/       # Price decomposition by attribute
├── dipasquale-wheaton/    # 4-quadrant model (rental · asset · construction · stock)
├── alonso-muth-mills/     # Urban accessibility vs. price
├── cap-rate-dcf/          # Income-property valuation
├── harrison-cycle/        # 18.6-year real estate cycle
├── highest-best-use/      # Highest & best use principle
├── redevelopment-feasibility/  # Redevelopment feasibility (비례율·분담금)
├── subscription-points/   # Korean subscription scoring strategy (청약 가점제)
└── gap-investment/        # Jeonse leverage structure (갭투자)
```

## Usage

```
/realty <situation description>
```

The meta-router classifies the problem and calls relevant framework(s) to synthesize the analysis.

> 💡 **Short name**: after [wrapper setup](https://github.com/ironyjk/claude-frameworks-marketplace#short-command-setup-optional), callable as `/realty`

## Out of Scope

- Individual property recommendations or appraisals
- Short-term trading signals or price predictions
- Stock/bond portfolio management (→ [`money`](https://github.com/ironyjk/investment-framework))
- Business strategy (→ `think`)
- Psychological / emotional counseling (→ `counsel`)

## Sister Repo

For situations requiring evaluation of real estate + financial assets together from an asset-allocation perspective (e.g., "Should I put the 200M KRW freed from jeonse into ETFs?"), pair with [`investment-framework`](https://github.com/ironyjk/investment-framework) (`/money`).

## Meta

- `last_verified: 2026-04-17`
- `valid_until: 2026-10-17` — Korean tax rules (acquisition tax, capital gains, comprehensive real estate tax), HUG guarantee rates, and redevelopment regulations require re-verification within 6 months.

## Disclaimer

**This repo is a decision-support tool, not real estate or investment advice.**

- No specific complexes, regions, or properties are recommended; all buy/sell decisions are entirely the user's responsibility.
- Korean tax (acquisition tax · capital gains tax · comprehensive real estate tax), HUG guarantee rates, and redevelopment regulations are current as of 2026-04-17 and change frequently. Always verify with a tax accountant, licensed real estate agent, or legal professional before any transaction.
- This repo does not engage in activities classified as "유사투자자문업" under Korean capital markets law — no specific tickers, weightings, or timing recommendations. Only thinking structures and frameworks are provided.
- Past cycles and prices do not guarantee future results. All frameworks here are *models that can be wrong*.

## License

CC-BY-NC-4.0 — see [LICENSE](LICENSE) for details. Commercial licensing: ironyjk@gmail.com
