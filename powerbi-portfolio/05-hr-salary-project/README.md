# HR Salary Analytics

Power BI project modelling **employee, department, and salary** data for HR / payroll analysis.

## Overview

| Item | Detail |
|------|--------|
| File | `PBI_Project2.pbix` |
| Source data | 3 CSV files |
| Model tables | dept_dataset, employee_dataset, fact_salary_dataset, Dim Calendar |

## Source Data

| File | Rows | Columns |
|------|------|---------|
| `dept_dataset.csv` | 5 | DeptID, DeptName, Location |
| `employee_dataset (1).csv` | 50 | EmpID, EmpName, Designation, Gender, DateOfJoining |
| `fact_salary_dataset.csv` | 504 | SalaryLogID, EmployeeID, DeptID, SalaryDate, BasicSalary, HRA, Allowances, Commission, Bonus, Deductions, NetSalary |

## Data Model

```
Dim Calendar ──┐
dept_dataset ──┼── fact_salary_dataset
employee_dataset ──┘
```

- **Fact:** Monthly salary logs (Basic, HRA, Allowances, Commission, Bonus, Deductions → NetSalary)
- **Dimensions:** Employee, Department, Calendar

## Skills Practised
- Multi-table relational model (HR domain)
- Fact table with multiple salary components
- Calendar dimension for salary trends over time
- Data cleaning (mixed-case names, date formats in source CSVs)

## Screenshot
See `IMG1.png` for a preview of the model / report.

## How to Open
Open `PBI_Project2.pbix` in Power BI Desktop. Use **Model view** to explore relationships.
