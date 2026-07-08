# DAX Formulas — Copy/Paste into Power BI

```DAX
Total Employees = COUNTROWS(employees)

Active Employees = CALCULATE([Total Employees], employees[status] = "Active")

Exited Employees = CALCULATE([Total Employees], employees[status] = "Exited")

Attrition % =
DIVIDE([Exited Employees], [Total Employees], 0) * 100

Avg Salary = AVERAGE(employees[salary])

Avg Performance = AVERAGE(employees[performance_rating])

Total Revenue = SUM(sales[revenue])

Total Profit  = SUM(sales[profit])

Total Orders  = COUNTROWS(sales)

Avg Order Value = DIVIDE([Total Revenue], [Total Orders])

Profit Margin % = DIVIDE([Total Profit], [Total Revenue]) * 100

-- Year-over-Year Growth
Prev Year Revenue =
CALCULATE([Total Revenue],
    DATEADD(sales[order_date], -1, YEAR))

YoY Revenue Growth % =
DIVIDE([Total Revenue] - [Prev Year Revenue], [Prev Year Revenue]) * 100

-- Revenue by Sales Rep
Revenue per Rep =
CALCULATE([Total Revenue],
    FILTER(employees, employees[dept_id] = "D01"))

-- Revenue-to-Salary ratio
Rev to Salary =
DIVIDE([Total Revenue], SUM(employees[salary]))
```
