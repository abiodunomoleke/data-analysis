# Data Analyst Portfolio — Abiodun Omoleke

Three end-to-end data analytics case studies, each covering the same full workflow — SQL analysis, a formula-driven Excel model, and a BI-style dashboard — applied to three different domains: retail sales, healthcare operations, and management consulting.

| Project | Domain | Headline finding |
|---|---|---|
| [`01-sales-analytics`](01-sales-analytics/) | Retail Sales | Revenue grew 13.9% YoY *with* margin improving — but Wholesale (20% of orders) drives 66.6% of revenue |
| [`02-healthcare-analytics`](02-healthcare-analytics/) | Healthcare Operations | 7.1% 30-day readmission rate; age group barely predicts risk — diagnosis and department do |
| [`03-management-consulting`](03-management-consulting/) | Management Consulting | One business unit is at breakeven, one is declining — and the profitability gap is a business-unit story, not a regional one |

|  |  |  |
|---|---|---|
| ![Sales dashboard](01-sales-analytics/dashboard/sales_dashboard_preview.png) | ![Healthcare dashboard](02-healthcare-analytics/dashboard/healthcare_dashboard_preview.png) | ![Consulting dashboard](03-management-consulting/dashboard/consulting_dashboard_preview.png) |

## About

I'm a data analyst with a background spanning procurement & logistics, marketing management, and hospitality, now focused on data analysis. I hold Microsoft and LinkedIn certifications in Data Analysis and Business Analysis, and I'm currently looking for remote data analyst roles.

- LinkedIn: [linkedin.com/in/abiodunomoleke](https://www.linkedin.com/in/abiodunomoleke/)

## What this portfolio demonstrates

- **SQL**: schema design, aggregation logic (`GROUP BY`, `SUMIF`-equivalents), time-window comparisons (YoY, quarterly trend), cohort/statistical-reliability filtering (`HAVING count >= n`)
- **Excel**: fully formula-driven workbooks — every summary tab recalculates from raw data using `SUMIFS`/`COUNTIFS`/`AVERAGEIFS`, nothing is hardcoded — plus native Excel charts
- **Dashboard design**: BI-style dashboards (KPI cards, trend lines, comparative bar charts) that actually work — each has a left-hand slicer panel, and every number on the page recomputes live in the browser from the underlying row-level data as filters are applied, with a written build guide in each project's README for recreating it as a live Power BI or Tableau report
- **Business framing**: every project starts from a stated business problem and ends with specific, numbers-backed recommendations — not just charts for their own sake

## Repository structure

```
data-analyst-portfolio/
├── README.md                      -- this file
├── PUBLISHING.md                  -- how to push this to your own GitHub account
├── 01-sales-analytics/
│   ├── README.md
│   ├── data/                      -- source CSV
│   ├── sql/                       -- schema + analysis queries
│   ├── excel/                     -- formula-driven workbook
│   └── dashboard/                 -- interactive HTML dashboard preview
├── 02-healthcare-analytics/
│   └── (same structure)
└── 03-management-consulting/
    └── (same structure)
```

## A note on the data

All three datasets are **synthetic** — generated programmatically rather than sourced from a real company, hospital, or client — because real proprietary data can't be published in a public portfolio. That said, each dataset was built with realistic structure (seasonality, department-specific clinical patterns, business-unit-specific margin profiles) and every number quoted in each project's README was computed directly from the raw data and independently validated in both SQL and Excel, so the analysis technique on display is exactly what would be applied to real data.

## Quick start

Each project folder is self-contained. To explore a project:
1. Open its `README.md` for the business problem, methodology, and key insights.
2. Open the `.xlsx` file in the `excel/` folder to see the formula-driven model.
3. Open the `.html` file in the `dashboard/` folder in any browser to see the interactive dashboard (works offline — no setup required).
4. Load the `.csv` from `data/` into the SQL engine of your choice using the matching `sql/schema.sql`, then run `sql/analysis_queries.sql`.
