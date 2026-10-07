# Data Modeling — Star Schema (Chocolate Sales)

Introduction to **dimensional modelling** in Power BI using chocolate shipment sales data.

## Overview

| Item | Detail |
|------|--------|
| File | `DataModeling.pbix` |
| Source | `sample-chocolate-sales-data-all.xlsx` |
| Model | Star schema — 5 tables |
| Pages | 1 |
| Visuals | Column chart + slicer |

## Data Model

```
calendar ──┐
locations ─┼── shipments (fact)
people ────┤
products ──┘
```

| Table | Role | Key Fields |
|-------|------|------------|
| shipments | Fact | ShipmentID, Amount, Boxes, Shipdate, Order_Status |
| products | Dimension | Product, Category |
| people | Dimension | Sales person |
| locations | Dimension | Geo |
| calendar | Dimension | Date hierarchy |

## Source Data
- **Shipments:** 7,905 rows
- Dimensions and calendar included in the Excel workbook

## Skills Practised
- Building a star schema
- Creating relationships between fact and dimensions
- Calendar table for time-based analysis
- Basic visual on top of the model (Amount by Product / Geo)

## How to Open
Open `DataModeling.pbix` in Power BI Desktop and switch to **Model view** to inspect relationships.
