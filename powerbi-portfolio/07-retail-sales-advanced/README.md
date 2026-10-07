# Retail Sales — Advanced Power BI Dashboard

Full-featured retail analytics solution demonstrating advanced **DAX**, **time intelligence**, and **multi-page report design**.

## Overview

| Item | Detail |
|------|--------|
| File | `PBI_P1.pbix` |
| Model | Star schema — 5 tables |
| Pages | 16 |
| Visuals | 68 |
| DAX measures | 35+ |
| Theme | CY25SU10 |
| Power BI version | 1.28 |

## Data Model

```
Dim Customer ──┐
Dim Product  ──┼── Fact Sales
Dim Store    ──┤
Dim Calendar ──┘
```

| Table | Key Columns |
|-------|-------------|
| Fact Sales | Sales, Profit, Quantity, CostPrice, UnitPrice, Discount |
| Dim Customer | CustomerID, CustomerName, Region, City |
| Dim Product | ProductID, ProductName, Category, Brand |
| Dim Store | StoreID, StoreName, Channel, SalespersonID |
| Dim Calendar | Date, Year, Quarter, Month |

## DAX Measure Categories

**Core:** Total Sales, Total Profit, Total Orders, Total Customers, Total Product  
**Statistical:** Max/Min/Avg Profit, CostPrice, Discount, Gross Sales  
**Filtered:** Online Sales, Brand A Sales, City-level (Chennai, Delhi, Kolkata, Bangalore)  
**Filter context:** ALL, ALLEXCEPT, REMOVEFILTERS, % of total patterns  
**Time intelligence:** YTD, MTD, QTD, Previous Year, Previous Month, DATESYTD/MTD/QTD  

## Report Pages (highlights)

| Page | Purpose |
|------|---------|
| Overview | Executive KPI dashboard with region charts & slicers |
| Time Series Analysis | YoY / MoM trends, online sales by quarter |
| Pages 1–5 | Dimension exploration (Customer, Product, Store) |
| Pages 6–12 | Measure testing — ALL, ALLEXCEPT, % contribution |
| Pages 13–14 | Time intelligence line charts |

## Skills Demonstrated
- Advanced DAX (filter context, time intelligence, % of total)
- Multi-page report architecture
- Consistent slicer design across dashboards
- KPI card layouts
- Star schema best practices

## How to Open
Open `PBI_P1.pbix` in Power BI Desktop. Start with the **Overview** and **Time Series Analysis** pages.
