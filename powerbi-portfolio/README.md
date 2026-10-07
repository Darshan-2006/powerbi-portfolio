# Power BI Portfolio

Complete collection of Power BI projects covering **Power Query → Data Modelling → DAX → Report Design**.

[![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-F2C811?logo=powerbi&logoColor=black)]()
[![Projects](https://img.shields.io/badge/Projects-7-blue)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## Portfolio Map

| # | Project | Focus | Tables | Pages | Visuals | Key Skills |
|---|---------|-------|--------|-------|---------|------------|
| 01 | [My First Project](01-my-first-project/) | First dashboard | 1 | 2 | 12 | Charts, cards, slicers |
| 02 | [Power Query](02-power-query/) | Data cleaning | — | — | — | Transform, web scrape |
| 03 | [Data Modeling](03-data-modeling/) | Star schema | 5 | 1 | 2 | Relationships, calendar |
| 04 | [DAX](04-dax/) | Measure writing | 5 | 6+6 | 7+8 | CALCULATE, targets, % |
| 05 | [HR Salary](05-hr-salary-project/) | Payroll model | 4 | 1 | — | Multi-table HR model |
| 06 | [Superstore](06-superstore-project/) | Sales KPIs | 4 | 1 | 7 | Star schema, slicers |
| 07 | [Retail Advanced](07-retail-sales-advanced/) | Full BI solution | 5 | 16 | 68 | 35+ DAX, time intel |

---

## Complete Analysis by Project

### 01 — My First Power BI Project
- **File:** `My_First_PowerBI_Project.pbix`
- **Model:** Single table `data`
- **Fields:** Amount, Boxes, Product, Sales Person, Country, Date (with Year/Quarter/Month hierarchy)
- **Page 1:** Column chart, clustered bar, KPI card, 2 slicers
- **Page 2:** Line chart, donut, table, clustered bar, card, slicer, text box
- **Skills:** First visuals, date hierarchy, interactive filters

### 02 — Power Query
| File | Rows | What it shows |
|------|------|---------------|
| `PowerQuery.xlsx` | 260 staff | Cleaned output — Emp ID, First/Last Name, Gender, Department, Salary, Salary Bucket, FTE, Work Type, Employee type, Work location, Age |
| `sample-staff-data (1).xlsx` | 276 staff | Raw source — messy department (`???`), combined Name, date as text |
| `WebScrapping.xlsx` | 93 countries | Olympic medals scraped from web — Rank, Gold, Silver, Bronze, Total, Division |
- **Skills:** Header promotion, data types, custom columns (Salary Bucket, Age), web data import, cleaning dirty values

### 03 — Data Modeling (Chocolate Sales)
- **File:** `DataModeling.pbix` + `sample-chocolate-sales-data-all.xlsx`
- **Model (star schema):**
  ```
  calendar ──┐
  locations ─┼── shipments (fact: 7,905 rows)
  people ────┤
  products ──┘
  ```
- **Fact columns:** ShipmentID, SPID, PID, GID, Shipdate, Amount, Boxes, Order_Status
- **Visuals:** Column chart (Amount by Product) + Geo slicer
- **Skills:** Creating relationships, calendar table, star schema layout

### 04 — DAX Practice
**DAX.pbix** (sales fact) and **DAX2.pbix** (shipments fact) — both star schema with calendar, locations, people, products.

| Measure Category | Examples |
|------------------|----------|
| Aggregations | Total Amount, Total Boxes, Shipment Count, Count of Products |
| Ratios | Amount Per Shipment (APS), Amount Per Boxes (APB), Boxes Per Shipment, Bar Shipment % |
| Filtered | Americas Shipments, Bar Shipments, Barr Amount, Low Box Shipment Count |
| Team / Target | Total Amount (My Team v1/v2), APS Target Achieved?, Target Comparison v1/v3, Sales Target |
- **Pages:** 6 each — mostly tables + slicers for measure testing
- **Skills:** CALCULATE, filter arguments, % of total, boolean status measures, iterative measure versions

### 05 — HR Salary Analytics
- **File:** `PBI_Project2.pbix`
- **Sources:**
  - `dept_dataset.csv` — 5 departments (DeptID, DeptName, Location)
  - `employee_dataset (1).csv` — 50 employees (EmpID, EmpName, Designation, Gender, DateOfJoining)
  - `fact_salary_dataset.csv` — 504 salary logs (BasicSalary, HRA, Allowances, Commission, Bonus, Deductions, NetSalary)
- **Model:** fact_salary_dataset ← employee, department, Dim Calendar
- **Skills:** HR domain modelling, multi-component salary fact, calendar for payroll trends, data cleaning (mixed-case names)

### 06 — Superstore Sales
- **File:** `SampleSuperstore.pbix` + `Sample - Superstore (1).xls`
- **Model:** Fact Sales + Dim Customer, Dim Product, Dim Calendar
- **KPI measures:** Total Sales, Total Profit, Total Orders, Total Customers, Total Products
- **Slicers:** Region, Category, Year, Month, Ship Mode
- **Skills:** Classic public dataset, KPI cards, multi-slicer dashboard

### 07 — Retail Sales Advanced (capstone)
- **File:** `PBI_P1.pbix`
- **Model:** Fact Sales + Dim Customer, Dim Product, Dim Store, Dim Calendar
- **16 pages / 68 visuals**
- **35+ DAX measures** across:
  - Core aggregations (Sales, Profit, Orders, Customers)
  - Min/Max/Avg statistics
  - City & channel filters (Chennai, Delhi, Kolkata, Bangalore, Online)
  - ALL / ALLEXCEPT / REMOVEFILTERS patterns
  - % of total (region, city, profit)
  - Time intelligence: YTD, MTD, QTD, Previous Year, Previous Month, DATESYTD/MTD/QTD
- **Flagship pages:** Overview (executive KPIs) + Time Series Analysis (YoY/MoM trends)
- **Skills:** Production-grade DAX, multi-page architecture, consistent slicer design

---

## How to Upload to GitHub

### Easiest — GitHub website
1. Go to [github.com/new](https://github.com/new)
2. Name: `powerbi-portfolio`
3. Public or Private → **Create repository**
4. Click **uploading an existing file**
5. Drag **all files and folders** from this zip into the browser
6. Commit: `Initial commit: Power BI portfolio`

### Command line
```bash
cd powerbi-portfolio
git init
git add .
git commit -m "Initial commit: Power BI portfolio"
git branch -M main
git remote add origin https://github.com/<YOUR-USERNAME>/powerbi-portfolio.git
git push -u origin main
```

> GitHub file limit is 100 MB per file. All files in this portfolio are under that limit.

---

## Skills Summary

| Skill Area | Where Demonstrated |
|------------|-------------------|
| Power Query / cleaning | 02 |
| Web data import | 02 |
| Star schema modelling | 03, 04, 05, 06, 07 |
| Calendar / date table | 03, 04, 05, 06, 07 |
| Basic DAX (SUM, COUNT) | 01, 03, 04, 06 |
| CALCULATE & filter context | 04, 07 |
| ALL / ALLEXCEPT / % of total | 04, 07 |
| Time intelligence (YTD/MTD/QTD/YoY) | 07 |
| KPI cards & slicers | 01, 06, 07 |
| Multi-page dashboards | 04, 07 |
| HR / payroll domain | 05 |
| Retail / sales domain | 03, 04, 06, 07 |

---

## License

MIT — see [LICENSE](LICENSE)
