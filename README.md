# Task 16 — Simple Profit Analysis

**Track:** Data Analytics (Veda Technology Internship — Level 1, Day 16)
**Tool:** Microsoft Excel (SUMIF / AVERAGEIF / COUNTIF)
**Dataset:** Superstore — `Sales_Facts` (10,194 order-line records)

## Objective
Compare total profit across product categories and understand basic profitability.

## Approach
1. Pulled `Category`, `Sub-Category`, `Sales`, `Quantity`, `Discount`, `Profit` from `Sales_Facts` into a `Sales_Data` sheet.
2. Built a **Profit Summary** table on the `Summary` sheet, grouped by category:
   - **Order Count** — `COUNTIF`
   - **Total Sales / Total Profit** — `SUMIF`
   - **Avg Profit / Order** — `AVERAGEIF`
   - **Profit Margin %** — Total Profit ÷ Total Sales
3. Added a clustered column **chart** comparing Total Sales vs. Total Profit by category.
4. Flagged the highest-profit and lowest-margin categories with `INDEX/MATCH` + `MAX`/`MIN`.

## Results

| Category        | Orders | Total Sales   | Total Profit | Avg Profit/Order | Margin % |
|------------------|--------|---------------|---------------|-------------------|----------|
| Furniture        | 2,201  | $754,747.76   | $19,730.00    | $8.96             | **2.6%** |
| Office Supplies  | 6,128  | $731,893.31   | $126,023.44   | $20.57            | 17.2%    |
| Technology       | 1,865  | $839,893.28   | **$146,543.38**| **$78.58**       | 17.4%    |
| **Grand Total**  | 10,194 | $2,326,534.35 | $292,296.81   | $28.67            | 12.6%    |

- **Highest total profit:** Technology ($146,543) — highest sales *and* highest average discount efficiency.
- **Lowest profit margin:** Furniture (2.6%) — despite the 2nd-highest sales, it earns almost no profit.

## Files
- `Profit_Analysis.xlsx` — workbook with `Sales_Data` and `Summary` sheets (live formulas + chart)
- `report.pdf` — one-page project report

## Interview Questions (from the task brief)
**Revenue vs profit?**
Revenue (Sales) is the total money brought in from selling products — it says nothing about cost. Profit is what's left after costs and discounts are subtracted from revenue. A category can have high revenue and still make little or no profit if its costs/discounts eat into that revenue.

**Why can sales be high but profit low?**
That's exactly what happens with Furniture here: it has the 2nd-highest total sales ($754.7K) but by far the lowest margin (2.6%). The main driver is **discounting** — Furniture carries the highest average discount rate (~17.3%, vs ~13–16% for the other categories) in this dataset. Heavy discounting, high shipping/handling costs, or low per-unit margins can all push profit down even while sales volume stays strong.

---
*Veda Technology Data Analytics Internship — Task 16/45*
