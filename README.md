# Superstore Sales Dashboard (Excel)

An interactive Excel dashboard built on the **Sample Superstore** dataset (Orders, Jan 2014 to Dec 2017). Choose filters from dropdowns and every KPI card and chart updates instantly.

![Dashboard preview](dashboard.png)

## Overview
This project turns 9,994 order lines into a one-page dashboard that answers questions such as:
- How much did we sell and earn, and at what margin?
- Which sub-categories bring the most sales and the most profit (or loss)?
- Which region and customer segment perform best?
- How do sales and profit change over the years and months?

## Key Figures (all data, no filters)
| Metric | Value |
|---|---|
| Total Sales | $2,297,201 |
| Total Profit | $286,397 |
| Profit Margin | 12.5% |
| Quantity Sold | 37,873 |
| Average Discount | 15.6% |
| Order Lines | 9,994 |

## Dashboard Features
- **4 dropdown filters:** Year, Region, Category, Segment ("All" means no filter)
- **6 KPI cards:** Total Sales, Total Profit, Profit Margin, Quantity Sold, Avg Discount, Order Lines
- **6 charts:**
  - Sales by Sub-Category (sorted bar)
  - Profit by Sub-Category (sorted bar)
  - Profit by Month (area)
  - Sales by Region (pie)
  - Sales by Year (line)
  - Sales by Segment (doughnut)

## Workbook Structure
| Sheet | Purpose |
|---|---|
| **Dashboard** | The final one-page dashboard with filters, cards and charts |
| **Calc** | Helper tables that read the filters and feed the charts (no manual edits) |
| **Data** | Cleaned source data: 12 columns, 9,994 rows |

## How It Works
1. The dropdowns on **Dashboard** pass their values to **Calc**.
2. **Calc** calculates totals with `SUMIFS`, `COUNTIFS` and `AVERAGEIFS` on the **Data** sheet.
3. Sub-categories are ranked using `LARGE`, `INDEX` and `MATCH`.
4. Cards and charts read from **Calc**, so they refresh when a filter changes.

## Excel Skills Used
`SUMIFS` | `COUNTIFS` | `AVERAGEIFS` | `INDEX-MATCH` | `LARGE` | `IF` / `IFERROR` | `YEAR` / `MONTH` | Data Validation (dropdowns) | Charts | Cell styling and layout

## How to Use
1. Download `Superstore_Dashboard.xlsx`.
2. Open it in Microsoft Excel and go to the **Dashboard** sheet.
3. Click a yellow box and choose a value from the list.
4. Set all four boxes back to "All" to see the full picture.

## Folder Structure
```
Superstore-Sales-Dashboard/
├── Superstore_Dashboard.xlsx
├── dashboard.png
└── README.md
```

## Notes
- The dropdown filters work like slicers, built with data validation and formulas.
- Dataset: Sample Superstore (a commonly used practice dataset).

