# Infosys Stock Valuation Model

An Excel-based **Discounted Cash Flow (DCF) and Comparable Company Analysis** model for valuing Infosys Limited.

The model combines historical financial analysis, operating forecasts, FCFF-based DCF valuation, WACC calculation, sensitivity analysis, and relative valuation using peer-company multiples.

**Valuation Date:** 10-Sep-2026  
**Company:** Infosys Limited  
**Currency:** ₹ crore unless otherwise stated

---

## 📊 Valuation Snapshot

| Valuation Method | Implied Value / Share | Upside vs. Current Price |
|---|---:|---:|
| Current Share Price | ₹1,036.50 | — |
| DCF Valuation | ₹1,173.10 | +13.18% |
| P/E Relative Valuation | ₹1,269.85 | +22.51% |
| EV/EBITDA Relative Valuation | ₹1,234.75 | +19.13% |

### Base-Case View

The base-case DCF produces an intrinsic value of approximately **₹1,173 per share**, implying approximately **13.2% upside** to the valuation-date share price of ₹1,036.50.

Infosys also trades at a discount to the selected peer group on both P/E and EV/EBITDA, providing a supportive relative-valuation signal.

> **Note:** These outputs are model-based estimates and are sensitive to the assumptions described below.

---

## 📌 Project Overview

This project was built to develop and demonstrate practical skills in:

- Financial statement analysis
- Financial forecasting
- Discounted Cash Flow valuation
- WACC and CAPM
- Free Cash Flow to Firm (FCFF)
- Comparable Company Analysis
- Sensitivity analysis
- Excel-based financial modeling

The model uses **FY2022–FY2026 historical financials** and forecasts **FY2027–FY2031**.

---

## 🧮 DCF Methodology

The DCF valuation follows a standard **FCFF-based approach**:

1. Forecast revenue and operating performance for FY2027–FY2031.
2. Calculate EBITDA, D&A, EBIT and NOPAT.
3. Estimate capital expenditure and changes in net working capital.
4. Derive Free Cash Flow to Firm (FCFF).
5. Discount projected FCFF using WACC.
6. Calculate terminal value using the **Gordon Growth Method**.
7. Bridge Enterprise Value to Equity Value using cash and debt.
8. Divide Equity Value by shares outstanding to derive intrinsic value per share.

### FCFF

`FCFF = NOPAT + D&A − Capex − Change in NWC`

### Terminal Value

`TV = FCFFₙ × (1 + g) / (WACC − g)`

---

## ⚙️ Key DCF Assumptions

| Assumption | Base Case |
|---|---:|
| WACC | 10.89% |
| Terminal Growth | 4.00% |
| FY2027 Revenue Growth | 3.00% |
| FY2031 Revenue Growth | 6.00% |
| EBITDA Margin | 23.50% |
| Tax Rate | 25.00% |
| Capex / Revenue | 1.50% |
| Change in NWC / Revenue | 1.50% |

The FY2027 revenue-growth assumption uses the upper end of Infosys' revised guidance range. FY2028–FY2031 represent analyst assumptions used for the model.

The terminal growth rate is a normalized long-term assumption and is **not company guidance**.

---

## 📈 DCF Sensitivity

The DCF valuation is particularly sensitive to changes in WACC and terminal growth.

| Scenario | WACC | Terminal Growth | Implied Value / Share | Upside / (Downside) |
|---|---:|---:|---:|---:|
| Conservative | 11.89% | 3.00% | ₹957 | -7.62% |
| Base Case | 10.89% | 4.00% | ₹1,173 | +13.18% |
| Optimistic | 9.89% | 5.00% | ₹1,563 | +50.79% |

Across the tested sensitivity range, the implied valuation spans approximately **₹957–₹1,563 per share**.

This highlights the importance of WACC and terminal-growth assumptions in long-duration DCF valuations.

---

## 🏢 Comparable Company Analysis

The relative valuation uses the following listed Indian IT peers:

- Tata Consultancy Services (TCS)
- HCLTech
- Wipro
- Tech Mahindra

The analysis compares Infosys and its peers using:

- P/E
- EV/EBITDA

### Relative Valuation

| Metric | Infosys | Peer Median | Discount |
|---|---:|---:|---:|
| P/E | 13.9x | 17.0x | -18.38% |
| EV/EBITDA | 9.4x | 10.7x | -12.79% |

The peer median excludes Infosys itself.

The implied values are calculated by applying peer multiples to Infosys' LTM financial metrics.

---

## 📉 Model Visualizations

### Historical Financials

![Historical Financials](screenshots/historicals.png)

### Forecast Financials

![Forecast Financials](screenshots/forecast.png)

### DCF Valuation

![DCF Valuation](screenshots/dcf.png)

### Comparable Company Analysis

![Comparable Company Analysis](screenshots/comps.png)

---

## 📁 Repository Structure

```text
stock-valuation-model/
│
├── model/
│   └── DCF_Model_v1.xlsx
│
├── output/
│   └── valuation_summary.pdf
│
├── screenshots/
│   ├── inputs.png
│   ├── historicals.png
│   ├── forecast.png
│   ├── dcf.png
│   └── comps.png
│
└── README.md
