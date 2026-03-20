# Leveraged Buyout (LBO) Model

A leveraged buyout model built in Excel, structured around a private equity acquisition framework with a fully integrated sources & uses, debt schedule, and returns analysis.

---

## Overview

This model replicates the analytical framework used in private equity to evaluate leveraged acquisition opportunities. It sizes the transaction, structures the debt, projects operating performance, and calculates sponsor returns across multiple exit scenarios.

---

## Model Structure

### 1. Transaction Overview
- Sources & uses of funds
- Entry valuation (EV, EBITDA multiple, equity check)
- Capitalization table at close

### 2. Operating Model
- Revenue and EBITDA projections over the investment horizon
- Margin assumptions by year
- Working capital and capex schedule feeding into free cash flow

### 3. Debt Schedule
- Tranche-level debt structure (senior secured, subordinated)
- Cash sweep mechanics — free cash flow applied to debt repayment
- PIK toggle optionality (where applicable)
- Covenant tracking

### 4. Returns Analysis
- Exit at multiple investment horizons (Year 3, 4, 5)
- Sensitivity table: IRR and MoM across exit EBITDA multiples and operating scenarios
- Equity bridge — reconciles entry equity to exit equity value

---

## Key Outputs

| Metric | Description |
|---|---|
| **IRR** | Internal rate of return to equity sponsor |
| **MoM** | Cash-on-cash multiple on invested equity |
| **Exit EV** | Enterprise value at exit under each scenario |
| **Debt Paydown** | Leverage ratio progression over hold period |

---

## Scenario Analysis

Three operating scenarios tested across multiple exit multiples:

| Scenario | EBITDA Growth | Exit Multiple Range |
|---|---|---|
| Base | Moderate growth, stable margins | Entry multiple ± 1x |
| Bull | Accelerated revenue + margin expansion | Entry multiple + 1–2x |
| Bear | Flat/declining EBITDA, compressed exit | Discount to entry |

---

## Files

```
lbo-model/
├── LBO_Model.xlsx      # Full model (transaction, debt schedule, returns, scenarios)
└── README.md
```

---

## Tools Used

- Microsoft Excel (formula-driven; no VBA)

---

## Notes

- Model is structured to mirror the analytical framework used by PE associates at the deal evaluation stage
- Debt sizing follows typical LBO leverage conventions (senior debt as a multiple of EBITDA)
- Returns analysis intentionally built to be sponsor-agnostic — assumptions can be swapped for any target company
