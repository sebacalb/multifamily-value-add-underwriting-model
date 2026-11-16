# Hypothetical Value-Add Multifamily Acquisition: Underwriting Model

A work sample: a fully linked Excel model that underwrites a **hypothetical** 120-unit value-add apartment acquisition in a Sun Belt market, from rent roll to levered returns, a JV waterfall and Base / Downside / Upside scenarios.

> **This is a hypothetical case.** It does not describe, analyze or reference any specific property, seller, broker or transaction, and it uses no confidential or non-public information. Every input is an illustrative assumption of the author and has not been verified. Not investment advice.

## The case

| | |
|---|---|
| Asset | 120 units (60 1BR / 60 2BR), 40 already renovated, 80 classic units to renovate |
| Business plan | Renovate 80 units over 3 years (30 / 30 / 20) at $7,500 per unit, earning a $90/month rent premium |
| Price | Derived: stabilized in-place NOI / 6.5% going-in cap = $10.68M ($89.0k per unit) |
| Debt | Floating interest-only loan at SOFR + 400 bps (7.95%), 1% origination fee, sized as the lesser of 65% LTV, 8% debt yield and 1.10x DSCR (65% LTV binds: $6.94M) |
| Reserve | $300k renovation reserve funded at closing; the rest of the $600k budget is paid from cash flow |
| Hold / exit | 5 years; sale at Year 6 NOI / 6.75% exit cap, less 2% selling costs |
| JV | 90% LP / 10% GP capital; 8% compounded preferred return; 20% promote to a 15% IRR hurdle, 30% above |

## Base-case results

| | |
|---|---|
| NOI, Year 1 to Year 5 | $580k to $864k |
| Yield on total cost (Year 5) | 7.6% (NOI / $11.44M total cost) vs 6.75% exit cap |
| Unlevered / levered IRR | 8.7% / 9.5% |
| Equity multiple | 1.56x |
| LP IRR / GP IRR | 9.2% / 11.9% (GP promote $86k) |
| Price for a 12% levered IRR | about $10.19M (4.6% below the implied price) |

| Scenario | Levered IRR | Equity multiple | Minimum DSCR |
|---|---|---|---|
| Base | 9.5% | 1.56x | 1.05x |
| Downside | -12.1% | 0.54x | 0.90x |
| Upside | 17.7% | 2.19x | 1.19x |

At the implied price the deal does not reach a 12% target, and with debt costing about 8.2% all-in (including the origination fee) against an 8.7% unlevered return, leverage adds less than one point of IRR. The Downside and Upside change all drivers at once (rent growth, occupancy, renovation cost and premium, opex growth, exit cap, interest rate and RUBS), so they show the range of outcomes, not which single assumption matters most.

## Workbook structure

| Sheet | Content |
|---|---|
| Summary | One-page output, integrity check and key judgments |
| Assumptions | All inputs with rationale; stabilized NOI, implied price, loan sizing and equity at close |
| Rent Roll / Opex Detail | In-place rents by unit type; opex by category |
| CF Base | 6-year operating projection, renovation program and reserve |
| Returns | Debt, exit, levered and unlevered cash flows, IRR, multiple, DSCR |
| Scenarios | Driver table and selector (`Scenarios!B4`: 1 Base, 2 Downside, 3 Upside; leave at 1) with a results table by scenario |
| Sensitivity | Levered IRR and multiple by purchase price and exit cap |
| Waterfall | LP / GP distributions with preferred return and promote tiers |

## Modeling notes

- **Price and debt are fixed at closing.** Scenarios change operations, exit and the interest rate paid, but never the purchase price, loan amount or equity at close.
- **Reserve and total cost.** Total cost counts the full $600k renovation budget once (financing costs excluded); the $300k reserve only determines when it is paid.
- **Waterfall.** The preferred return is cumulative and compounded annually; cash flows go first to return of capital plus the 8% preferred return, then to the next tier. The GP's promote is on top of its pro rata share as a co-investor.
- **Simplification.** One renovation cost ($7,500) and one rent premium ($90) are used for both 1BR and 2BR. The premium already observed on renovated units is the same $90 for both types, so splitting them would not change base-case results.
- **Timing.** Annual, end-of-year cash flows; Year 6 NOI is used only for the exit value.
- **Integrity.** `Summary` reports "OK" when the rent roll, opex, cash-flow, debt and waterfall reconciliation checks are all zero.

## Limitations

Illustrative inputs only; not calibrated to a real market or property. Annual periods, no refinancing, no taxes or fund-level costs. Results show how the structure behaves, not a forecast.
