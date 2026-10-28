# Seasonal Sales Trend Analysis

An Excel dashboard that finds seasonal sales patterns and uses them to plan promotions, inventory and staffing.



## Project Overview

Retail sales change across months and quarters, but the business does not clearly know when demand is high or low. This leads to poorly timed promotions, extra stock when demand is low, and idle staff in slow periods.

This project analyses 2,000 orders (Jan 2022 – Dec 2024) to measure seasonal demand with a **Seasonal Index** and to show how promotions, stock and staffing line up with it.

## Objectives

- Plan promotions during high-demand periods
- Prepare adequate inventory before peak seasons
- Adjust staffing levels according to expected demand
- Reduce unnecessary operational costs during slow periods

## Business Questions

- Do sales follow consistent monthly or quarterly patterns?
- Which months or quarters have higher demand?
- When do sales typically decline?
- How does seasonal demand affect different products or categories?

## Tools Used

- Microsoft Excel (add your version) – Tables, Pivot Tables, PivotCharts, Slicers, formulas (SUMIFS, AVERAGE, INDEX/MATCH)
- System: Windows 10, 16 GB RAM

## Dataset

A **simulated** retail dataset created for this project (not real company data), with 2,000 rows and 15 columns:

| Group | Columns |
|---|---|
| Order details | Order Id, Order Date, Category, Sub-Category, Quantity, Unit Price, Discount % |
| Calculated | Year, Month, Quarter, Promotion Flag, Sales, Seasonal Index |
| Assumed values | Closing Stock, Staff Count |

`Closing Stock` and `Staff Count` are **assumed monthly values**, because public sales datasets do not include them. Results show the method, not real business figures.

**Seasonal Index** = a month's total sales ÷ the average month's sales. Above 1.1 is high demand, below 0.9 is low demand.

## Workflow

1. **Data collection** – prepared the simulated dataset (2,000 orders, 2022–2024).
2. **Data understanding** – reviewed order, product, price, discount, stock and staff columns.
3. **Data cleaning** – checked blanks, duplicate Order Ids and date/number formats. None found.
4. **Data transformation** – added Year, Month, Quarter, Promotion Flag, Sales and Seasonal Index.
5. **Analysis** – built seven comparison analyses with pivot tables and charts.
6. **Dashboard** – combined the charts and KPI cards on one sheet, with slicers for Year, Quarter, Month, Category, Sub-Category and Promotion Flag.

## The Seven Analyses

| # | Analysis | Columns compared |
|---|---|---|
| 1 | Month wise Sales | Month vs Sales |
| 2 | Quarter wise Sales | Quarter vs Sales |
| 3 | Month wise Seasonal Index | Month vs Seasonal Index |
| 4 | Category wise Monthly Sales | Category vs Sales |
| 5 | Promotion wise Sales | Promotion Flag vs Sales |
| 6 | Month wise Stock vs Units Sold | Closing Stock vs Quantity |
| 7 | Month wise Staff vs Sales | Staff Count vs Sales |

## Key Findings

- **December (index 1.74) and November (1.46) are the high-demand months.** February (0.59) is the lowest.
- **Q4 is the strongest quarter in all three years** (about 100K, 132K and 158K in sales).
- **Each category peaks at a different time.** Technology and Furniture peak in Nov–Dec; Office Supplies peak in Aug and Jan.
- **About 40% of promotion orders ran in low-demand months**, with almost no lift (3.25 vs 3.17 units per order with and without a promotion).
- **Stock stays flat while demand changes.** April has 8.8 units of stock per unit sold, against 4.5 in December.
- **Staff levels do not follow demand.** Sales per employee are 796 in February and 2,004 in December.

## Recommendations

- Focus promotions on November and December, and review those in February, July and September.
- Build stock before November and December, and reduce stock cover in January to April.
- Add staff in November and December, and reduce idle hours in February.

## Project Files

```
seasonal-sales-trend-analysis/
├── README.md
├── Seasonal_Sales_Dataset.xlsx

```

- `data/Seasonal_Sales_Dataset.xlsx` – dataset, Seasonal Index sheet and dashboard workbook
- `images/dashboard_preview.png` – dashboard screenshot
- `reports/` – project report and presentation

## How to Use

1. Download `data/Seasonal_Sales_Dataset.xlsx` and open it in Microsoft Excel.
2. Open the `dashboard` sheet to see the KPI cards and charts.
3. Use the slicers on the right to filter by Year, Quarter, Month, Category, Sub-Category or Promotion Flag.
4. Open the `Sales Data` and `Seasonal Index` sheets to see the data and formulas.


## Future Enhancement

- Use real sales, stock and staff data in place of assumed values
- Add demand forecasting and a Power BI dashboard
- Include profit, region and customer analysis
