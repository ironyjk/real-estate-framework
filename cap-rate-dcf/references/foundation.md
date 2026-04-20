# Cap Rate / DCF Valuation -- Theoretical Foundation

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

