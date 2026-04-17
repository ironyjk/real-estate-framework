---
name: cap-rate-dcf
version: "0.1.0"
description: "Cap Rate / DCF — Valuation of income-producing real estate (retail, office, studio apartments, small buildings) using NOI and discount rates. Handles Korean monthly-rent/jeonse hybrid structures, deposit conversion, acquisition tax, comprehensive real estate tax, and rental income tax."
---

# Cap Rate / DCF Valuation

## One-Line Summary

The value of income-producing real estate = **the present value of current and future Net Operating Income (NOI)**. Use Cap Rate for short-term judgment, DCF for mid- to long-term judgment.

## Theoretical Origins

- Traditional commercial real estate appraisal method. Appraisal Institute standard.
- Among the three approaches (sales comparison, cost, income), this is the *income approach*.
- Korpacz, PwC Real Estate Investor Survey, etc. serve as Cap Rate data standards.

## Core Concepts

### 1. NOI (Net Operating Income)

$$\text{NOI} = \text{GPR} \times (1 - \text{vacancy rate}) - \text{operating expenses}$$

- **GPR (Gross Potential Rent)**: Total potential rental income (assuming zero vacancy)
- **Operating expenses**: Property tax, management fees, repairs and maintenance, insurance. *Loan interest and depreciation are excluded.*

### 2. Cap Rate

$$\text{Cap Rate} = \frac{\text{NOI}}{\text{property price}}$$

$$\text{Price} = \frac{\text{NOI}}{\text{Cap Rate}}$$

- Approximate Korean commercial Cap Rates (April 2026): Seoul prime office 4.0~4.8% (risen due to interest rate hikes), Gangnam small buildings (꼬마빌딩) 2.8~3.8%, regional retail 5~8%
- The lower it is, the more expensive the asset has become (low yield relative to asset price).

### 2-1. Gordon Growth (Theoretical Dissection of Cap Rate)

$$\text{Cap Rate} = r - g$$

- $r$: Required rate of return (opportunity cost + risk premium)
- $g$: Long-term NOI growth rate (rent increases − depreciation − operating expense increases)
- Implications:
  - Rent growth rate↑ → Cap Rate↓ → Price↑ ("growth premium")
  - If interest rates rise causing $r$↑ but $g$ stays the same → Cap Rate↑ → Price↓
  - Why Korean small buildings (꼬마빌딩) have low Cap Rates: Capital gains expectations (high estimated $g$) push Cap Rate down → **a signal that buyers are betting on capital gain rather than cash flow**

### 3. DCF (Discounted Cash Flow)

$$V = \sum_{t=1}^{n} \frac{\text{CF}_t}{(1+r)^t} + \frac{\text{Terminal Value}}{(1+r)^n}$$

- $r$: Discount rate (opportunity cost + risk premium)
- Terminal Value: Final year NOI / exit cap rate
- 5~10 year projections are typical

### 4. Levered Return

When including debt:
$$\text{Cash-on-Cash} = \frac{\text{NOI} - \text{interest}}{\text{equity}}$$

- If loan rate < Cap Rate, leverage is favorable (positive leverage)
- If the opposite, leverage erodes returns

## When to Use

- Purchase decisions for retail, office, small buildings (꼬마빌딩), studio apartments, and goshiwon (고시원)
- Verification of commercial appraisals
- Renovation vs. sale decisions (simulating value changes)
- Comparing rental vs. sale-based profits
- As a sub-tool for reconstruction feasibility analysis (post-development NOI → price)

## Korean Market Application Points

### 1. Deposit → Monthly Rent Conversion (Jeonse-Wolse Conversion Rate)

Korea uses a hybrid structure like "deposit 50M / monthly rent 1M". Standardization:

$$\text{converted monthly rent} = \text{monthly rent} + \text{deposit} \times \frac{\text{conversion rate}}{12}$$

- Conversion rate: 4~7% by region (Korea Real Estate Board public disclosure)
- Alternatively, calculate internally using opportunity cost (deposit rate + 2~3%)

### 2. Residential vs. Commercial Application Differences

| Category | Cap Rate Applicability | Reason |
|---|---|---|
| Apartment (owner-occupied) | ❌ Rarely used | Capital gains focused, thin monthly rental market |
| Apartment (monthly rent) | △ Reference only | Cap Rate 1~2.5% → very low |
| Officetel | ○ Applicable | Standardized rental market |
| Retail | ◎ Core tool | Income focused |
| Small building (꼬마빌딩) | ◎ Core tool | Rental + capital gains hybrid |
| Studio/goshiwon | ◎ | Pure income-producing |

### 3. Korea-Specific Costs

- **Acquisition tax 4.6~12%** — Reflect in year 1 of DCF. Multi-home owners, corporations, and regulated regions face heavier rates.
- **Comprehensive real estate tax (종부세)** — Progressive based on published price. High rate for corporations.
- **Property tax (재산세)** — Annual 0.1~0.4%
- **Rental income tax (임대소득세)** — For housing, separate taxation below 20M KRW, comprehensive taxation above. For commercial, includes VAT and income tax.
- **Health insurance premium (건보료)** — For regional subscribers, may surge based on assets and income
- **Loan regulations** — DSR, LTV, RTI (RTI is the binding constraint for commercial property loans)

### 4. Setting Discount Rate $r$ (Korea 2026 Guide)

- Risk-free (3-year government bond): ~3~3.5%
- Risk premium: Prime office +1.5~2%, regional retail +3~5%, small buildings (꼬마빌딩) +2~3%
- Total: **Start in the 5~8% range**, adjust by risk

### 5. Cautions When Estimating Terminal Value

- Setting the Exit Cap Rate *higher than the current Cap Rate* is conservative (assuming future rate and risk increases)
- The Korean commercial market has low liquidity → consider adding an exit discount

## Procedure

```
1. Calculate NOI
   - GPR (rent × 12)
   - Vacancy rate (prime 5%, regional retail 10~20%)
   - Operating expenses (roughly 10~25% of GPR)
   - Include deposits as converted monthly rent
2. Compare Cap Rate to market
   - Cap Rate of recently transacted comparable properties
   - My property's Cap Rate = NOI / asking price
3. Cross-verify value
   - Price = NOI / market Cap Rate
   - Compare asking price vs. calculated price
4. DCF (5~10 years)
   - Rent increase rate (annual 2~5%)
   - Vacancy and maintenance scenarios
   - Exit Cap Rate
5. Apply leverage
   - Loan rate, terms, RTI
   - Calculate Cash-on-Cash
6. After-tax return
   - Reflect acquisition tax, comprehensive real estate tax, rental income tax
   - Effective return (IRR)
```

## Korean Context Example

**Question**: "A small building (꼬마빌딩) in Seoul's outskirts costs 3B KRW, with 9M monthly rent + 500M deposit. Should I buy?"

**Cap Rate Calculation**:
- GPR: 9M × 12 = 108M
- Deposit conversion: 500M × 5% / 12 × 12 = 25M
- Effective rental income: 133M
- Vacancy 5%, operating expenses 15% → NOI ≈ 106M
- Cap Rate = 106M / 3B = **3.5%**

**Judgment**:
- Seoul outskirts small building (꼬마빌딩) market Cap Rate is 3.5~4.5% — at the lower bound
- Assuming 4.5% loan rate → negative leverage (equity return deteriorates)
- Without capital gains expectations, appeal is weak
- In 5-year DCF, need to calculate IRR assuming 3% annual rent increases and 4.0% Exit Cap

**Turn the question back**: "Why this property? Capital gains expectation? Renovation potential? Commercial district change forecast?" — Pure yield alone is insufficient.

## Limitations

1. **Capital gains omission** — In Korea, capital gains comprise a large portion of returns. NOI alone underestimates value.
2. **Rent rigidity** — Increase limits upon contract renewal (e.g., 5% rule for residential).
3. **Vacancy and defaulting tenant risk** — Calculating only with averages underestimates risk.
4. **Arbitrariness of discount rate** — Even a 0.5% change in $r$ causes significant value swings. Sensitivity analysis is essential.
5. **Thin Korean commercial data** — Small sample size for Cap Rate comparisons yields wide confidence intervals.
6. **Inappropriate for residential** — Apartment Cap Rate interpretation risks misunderstanding.

## When This Framework is *Wrong*

- Apartment price decomposition → `hedonic-pricing`
- Use conversion value through reconstruction → `highest-best-use` + `redevelopment-feasibility`
- Market cycle positioning → `harrison-cycle`
- Supply/inventory transitions → `dipasquale-wheaton`

## Further Learning Resources

- Brueggeman, W. & Fisher, J. *Real Estate Finance and Investments.* — Standard textbook.
- PwC/Korpacz Real Estate Investor Survey — Cap Rate benchmarks.
- Domestic: Korea Real Estate Board commercial real estate rental market trends, Genstar Mate Cap Rate reports.
