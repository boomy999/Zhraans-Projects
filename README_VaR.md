# Value-at-Risk & Stress Testing — Natural Resources Equity Portfolio

A quantitative risk analysis framework applied to a natural resources equity portfolio (gold and silver mining stocks), implementing historical VaR, parametric VaR, and macro stress testing in Python.

---

## Overview

This project builds a risk measurement and stress-testing toolkit for a concentrated equity portfolio in the precious metals mining sector. It quantifies downside risk across multiple methodologies and subjects the portfolio to historical and hypothetical macro shock scenarios.

---

## Portfolio

| Constituent | Sector |
|---|---|
| Gold mining equities | Precious metals |
| Silver mining equities | Precious metals |

Portfolio is equal- or custom-weighted depending on the scenario being analyzed.

---

## Methodology

### Value-at-Risk
Three parallel VaR implementations:

| Method | Description |
|---|---|
| **Historical VaR** | Empirical return distribution — no distributional assumption |
| **Parametric VaR** | Gaussian assumption; mean and variance estimated from historical window |
| **Monte Carlo VaR** | Simulated return paths using calibrated parameters |

Confidence levels: **95%** and **99%**  
Holding period: **1-day and 10-day** horizons

### Stress Testing
Portfolio subjected to historical macro shock scenarios:
- 2008 Global Financial Crisis
- 2020 COVID crash
- Sharp USD rally scenarios (relevant for commodity pricing)
- Gold/silver-specific supply shocks

Each scenario maps historical factor moves to estimated portfolio P&L impact.

### Correlation & Diversification Analysis
- Rolling correlation between portfolio constituents
- Assessment of diversification benefit (or lack thereof) under stress — mining equities tend to correlation = 1 in tail events

---

## Key Findings

- Precious metals rally timing proved prescient — model captured upside participation while quantifying left-tail risk
- Historical VaR and parametric VaR diverge meaningfully at 99% confidence, reflecting fat tails in mining equity returns
- Correlation clustering under stress eliminates most within-sector diversification benefit

---

## Repository Structure

```
var-stress-testing/
├── data/
│   └── prices.csv                  # Historical price data
├── notebooks/
│   ├── 01_data_preparation.ipynb
│   ├── 02_var_calculations.ipynb
│   └── 03_stress_testing.ipynb
├── src/
│   ├── var_models.py               # VaR computation functions
│   ├── stress_scenarios.py         # Scenario definitions and shock mappings
│   └── portfolio.py                # Portfolio construction and weighting
├── outputs/
│   └── risk_report.xlsx            # Summary tables and charts
└── README.md
```

---

## Tech Stack

- **Python 3.x**
- `pandas`, `numpy` — data manipulation and return calculations
- `scipy` — statistical distributions for parametric VaR
- `matplotlib`, `seaborn` — visualization
- `openpyxl` — Excel output for risk report

---

## Usage

```bash
pip install -r requirements.txt
jupyter notebook notebooks/02_var_calculations.ipynb
```

---

## Limitations

- Analysis is backward-looking; VaR does not predict future tail events
- Parametric VaR understates risk for non-normally distributed mining equity returns
- Liquidity risk not explicitly modeled — bid-ask spread and market impact excluded
- Portfolio does not include commodity futures directly; risk is captured through equity proxies
