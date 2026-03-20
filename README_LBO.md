# Leveraged Buyout (LBO) Model — Stanley Black & Decker (SWK)

A leveraged buyout model built in Excel analyzing a hypothetical PE acquisition of Stanley Black & Decker (NYSE: SWK), a mature industrial conglomerate trading at depressed margins. The thesis centers on operational turnaround — aggressive SG&A rationalization driving EBITDA margin expansion from ~10.6% to 17%+ — with multiple expansion on exit as the market re-rates higher-quality cash flow.

---

## Investment Thesis

Stanley Black & Decker entered a period of margin compression following supply chain disruptions and cost creep. At ~10.6% LTM EBITDA margin, the company trades well below industrial peers:

| Peer | EBITDA Margin |
|---|---|
| Snap-on (SNA) | ~25% |
| Illinois Tool Works (ITW) | ~29% |
| **SWK (entry)** | **~10.6%** |

A PE sponsor acquires at a distressed/underperforming multiple, executes on SG&A cuts + gross margin improvement (management targeting 35%+ gross margin), and exits a meaningfully higher-quality business at a re-rated multiple.

---

## Key Assumptions

### Transaction
| Parameter | Assumption |
|---|---|
| Entry premium | 15% |
| Entry leverage | 5.5x EV/EBITDA |

*15% premium — pay the minimum to get the deal done.*

### Operating Model
| Parameter | Assumption |
|---|---|
| Revenue CAGR | 3.0% (in line with nominal GDP) |
| LTM EBITDA margin | ~10.6% |
| Year 5 EBITDA margin (base) | 17% |
| Margin expansion driver | SG&A rationalization + gross margin recovery to 35%+ |

### Exit
| Parameter | Assumption |
|---|---|
| Exit multiple (base) | 13.0x EV/EBITDA |
| Exit multiple range | 12.5x — 13.5x |
| Rationale | Buy at 10–11x distressed; exit at 13x as market rewards improved cash flow quality. Capped at 14x — mature industrials don't trade at tech multiples. |

---

## Scenario Matrix

| Scenario | Revenue CAGR | Year 5 Margin | Exit Multiple |
|---|---|---|---|
| Bear | 2.5% | 16% | 12.5x |
| **Base** | **3.0%** | **17%** | **13.0x** |
| Bull | 3.0% | 18% | 13.5x |

---

## Model Structure

1. **Sources & Uses** — transaction sizing, equity check, debt stack
2. **Operating Model** — revenue build, EBITDA bridge, FCF projection
3. **Debt Schedule** — tranche-level amortization and cash sweep mechanics
4. **Returns Analysis** — IRR and MoM at Years 3, 4, 5; sensitivity tables on margin and exit multiple
5. **Equity Bridge** — entry to exit equity value reconciliation

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

