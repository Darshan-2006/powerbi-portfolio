# Superstore Sales Dashboard

Power BI dashboard built on the classic **Sample Superstore** dataset.

## Overview

| Item | Detail |
|------|--------|
| File | `SampleSuperstore.pbix` |
| Source | `Sample - Superstore (1).xls` (~14 MB) |
| Model | Star schema — Fact Sales + Dim Customer, Dim Product, Dim Calendar |
| Pages | 1 (dashboard) |
| Visuals | KPI cards + 5 slicers |

## Data Model

```
Dim Customer ──┐
Dim Product  ──┼── Fact Sales
Dim Calendar ──┘
```

## KPI Measures
- Total Sales
- Total Profit
- Total Orders
- Total Customers
- Total Products

## Slicers
Region, Category, Year, Month, Ship Mode

## Skills Practised
- Star schema on a well-known public dataset
- Core business KPIs as DAX measures
- Interactive dashboard with multiple slicers
- Superstore domain (orders, customers, products, shipping)

## Supporting Doc
`Doc.docx` — project notes / documentation.

## How to Open
Open `SampleSuperstore.pbix` in Power BI Desktop.
