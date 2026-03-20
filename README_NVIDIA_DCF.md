# NVIDIA DCF Valuation Model

A fully integrated three-statement financial model and DCF valuation for NVIDIA Corporation, built in Excel with scenario analysis and an executive dashboard.

---

## Overview

This model builds a bottom-up intrinsic value estimate for NVIDIA using a discounted cash flow framework, anchored to segment-level revenue assumptions and driven by a fully linked income statement, balance sheet, and cash flow statement.

**Valuation Summary**

| Method | Implied Price |
|---|---|
| Gordon Growth Model | ~$169 |
| Exit Multiple (25x EBITDA) | ~$266 |
| Market Price (at model date) | ~$183 |

---

## Model Architecture

### Three-Statement Model
- Fully integrated P&L, balance sheet, and cash flow statement
- All statements linked — changes in assumptions flow through automatically

### Revenue Build
Segment-level forecasts with explicit growth rate assumptions:

| Segment | Year 1 | Year 2 | Year 3 | Year 4 |
|---|---|---|---|---|
| Data Center | 45% | 35% | 25% | 18% |
| Gaming / Other | Custom assumptions per segment |

### DCF Valuation
- **WACC:** 9.0%
- **Terminal Growth Rate:** 3.5%
- **Exit Multiple:** 25x EV/EBITDA
- Two terminal value methodologies run in parallel (Gordon Growth vs. Exit Multiple)

### Scenario & Sensitivity Analysis
- Base, bull, and bear cases with distinct macro and operational assumptions
- Two-variable sensitivity tables on WACC and TGR
- Bear case stress-test with compressed margins and Data Center growth deceleration

### Dashboard
- Executive summary tab consolidating key outputs, assumptions, and valuation range

---

## Key Assumptions & Decisions

All forecast assumptions were driven by bottom-up analysis, not template defaults:

- Data Center segment modeled as the primary value driver given hyperscaler capex tailwinds and AI infrastructure demand
- Margin expansion tapered in outer years to reflect competitive entry and pricing normalization
- WACC built from first principles (CAPM equity cost, market debt cost, market-value weights)
- Terminal growth capped conservatively relative to nominal GDP given NVIDIA's current elevated base

---

## Files

```
nvidia-dcf/
├── NVIDIA_DCF_Model.xlsx       # Main model (three statements + DCF + scenarios + dashboard)
└── README.md
```

---

## Tools Used

- Microsoft Excel (no VBA — formula-driven throughout)

---

## Limitations

- Model reflects a point-in-time snapshot; revenue and margin assumptions would require updating for current filings
- Does not incorporate real-time market data or live API feeds
- Qualitative factors (regulatory risk, export controls, competitive dynamics) are captured in scenario narratives but not formally probabilistically weighted
