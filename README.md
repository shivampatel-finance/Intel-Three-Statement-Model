# Intel Three-Statement Financial Model

I wanted to learn how a full financial model is built, so I built one from scratch in Excel for Intel, pulling every input from the 10-K and 10-Q filings. I then used it to forecast FY2026E to FY2030E and value the company.

## Status

Complete. I built it in four stages: Lite, Core, Full and Pro. This is the Pro version.

## Key results (Base case)

| | FY2025 | FY2026E | FY2030E |
|---|---|---|---|
| Revenue | $52.9B | $62.8B | $88.8B |
| Net income attributable to Intel | -$0.3B | $2.1B | $12.7B |
| Debt / EBITDA | n/a | 3.0x | 1.4x |

- **Scenarios:** FY2030E net income ranges from $8.3B (Downside) to $16.8B (Upside).
- **Valuation:** DCF of $10.78 per share (Downside $7.08, Upside $16.76) at a 15.3% discount rate. Peer comps give $49.68 (EV / EBITDA) and $163.35 (EV / Revenue), against a share price of $91.69 on Oct 21, 2026.
- **Main risks:** gross margin and revenue growth drive earnings, and gross margin and capex drive cash.
- Full write-up: [Intel_Model_Memo.pdf](Intel_Model_Memo.pdf)

## What's in the model

- **Summary:** key outputs and scenario comparison
- **Assumptions:** all forecast drivers
- **Income Statement, Balance Sheet, Cash Flow Statement:** the three linked statements
- **Scenarios:** Base, Upside and Downside cases
- **Segments:** revenue built by segment (CCG, DCAI, Foundry, All Other)
- **Bonds, Debt Schedule:** 42 bonds from the 10-K and the debt and interest forecast
- **Quarterly:** reported Q1 and Q2 2026, estimated Q3 and Q4
- **PP&E Schedule, Working Capital, Share Count**
- **Credit Ratios, Payback, Sensitivity**
- **DCF, Comps, Valuation Summary**
- **Checks:** 15 checks, with a master flag on Summary B3 that should read ALL CHECKS PASS
- **Notes:** source and page reference for every input

## How to use it

Change the scenario in **Scenarios B1** (1 = Base, 2 = Upside, 3 = Downside). Blue cells are typed inputs and black cells are formulas. The sensitivity tables are Excel data tables, so use Excel rather than Google Sheets.

## Data sources

- [FY2025 Form 10-K](https://www.sec.gov/ix?doc=/Archives/edgar/data/0000050863/000005086326000011/intc-20251227.htm)
- [FY2024 Form 10-K](https://www.sec.gov/ix?doc=/Archives/edgar/data/0000050863/000005086325000009/intc-20241228.htm)
- Intel 10-Q filings for 2025 and 2026
- Market prices and peer multiples from Yahoo Finance, Oct 21, 2026

## Limitations

- Public filings only, with no internal company data.
- FY2027E to FY2030E are my own estimates, not company guidance.
- Q3 and Q4 2026 are estimates made before Intel reported Q3 on Oct 29, 2026.
- Simplifications: one company-wide gross margin, blended interest rates, and about $13.4B of non-cash first-half 2026 losses excluded from the annual cash model.
