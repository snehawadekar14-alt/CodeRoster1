# PlantNxt Data Scientist Assignment  
## Sales Revenue Forecasting & Decision Intelligence

**Author:** Atharv Borse  
**Date:** 21 May 2026  
**Dataset:** revenue_ledger.csv (Apr 2022 – Mar 2024)

---

### Key Findings

| Finding                | Detail                                                                 |
|------------------------|------------------------------------------------------------------------|
| **Date Range**         | Apr 2022 – Mar 2024 (2 full fiscal years)                              |
| **Missing Values**     | ~2% Tax, ~1% Others — imputed with 0 (tax-exempt or included)          |
| **Zero-revenue Days**  | Sundays and Indian holidays (~18% of days)                             |
| **Part-01675 dominance** | ~44% of Account A revenue — significant concentration risk           |
| **Weekly pattern**     | Tuesday/Wednesday peak; Saturday ~30%; Sunday nil                      |
| **Nov 2022 dip**       | Likely supply disruption — revenue fell ~65% for 20 days               |
| **Sep 2023 spike**     | Bulk order event — 2.8× baseline for ~7 days                           |
| **Trend**              | ~0.02% daily growth (≈7.3% annualised)                                 |

*MAPE is elevated because ~18% of days have zero revenue (weekends/holidays), making the denominator small. On trading-days only, MAPE improves significantly.*

---

### Business Recommendations

- **Diversify Product Portfolio:** Address concentration risk from Part-01675 (~44% of Account A revenue).
- **Mitigate Supply Chain Risks:** Investigate and address causes of the Nov 2022 revenue dip.
- **Leverage Bulk Order Insights:** Plan for and capitalize on bulk order events (e.g., Sep 2023 spike).
- **Enhance Forecasting:** Incorporate external signals (PO backlog, commodity prices, IIP index) and develop per-customer models, especially for high-value customers (e.g., Cust-00519).
- **Improve Data Coverage:** Extend historical data for better seasonality detection.
- **Refine Confidence Intervals:** Calibrate Prophet model intervals for production use.

---
