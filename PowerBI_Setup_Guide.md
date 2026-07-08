# Power BI Dashboard — Step-by-Step Build Guide

> This guide lets you rebuild the exact dashboard in **Power BI Desktop (free)** using the CSVs in `../01_datasets/`.

## 1. Download Power BI Desktop (Free)
- https://powerbi.microsoft.com/desktop/  (Windows) — free, no login needed to build reports.

## 2. Load Data
1. Open Power BI Desktop → **Home → Get Data → Text/CSV**.
2. Load all 5 files: `departments.csv`, `employees.csv`, `products.csv`, `customers.csv`, `sales.csv`.
3. Click **Transform Data** → set `hire_date`, `exit_date`, `order_date`, `signup_date` to type **Date**. Close & Apply.

## 3. Create Relationships (Model view)
| From table.column | To table.column | Cardinality |
|---|---|---|
| employees.dept_id | departments.dept_id | Many-to-One |
| sales.employee_id | employees.employee_id | Many-to-One |
| sales.product_id  | products.product_id  | Many-to-One |
| sales.customer_id | customers.customer_id | Many-to-One |

## 4. Build Measures (DAX)
See `DAX_Formulas.md`. Copy-paste each into **Modeling → New Measure**.

## 5. Report Pages

### Page 1 — Employee Analytics
- **Card:** Total Employees, Attrition %, Avg Salary, Avg Rating
- **Clustered bar:** Headcount by Department
- **Donut:** Active vs Exited
- **Line:** Yearly Hires
- **Table:** Top 10 Highest-paid employees

### Page 2 — Sales Analytics
- **Card:** Total Revenue, Total Profit, Orders, Avg Order Value
- **Line:** Monthly Revenue Trend
- **Clustered column:** Yearly Revenue vs Profit
- **Map/Filled map:** Revenue by Region
- **Bar:** Top 10 Products
- **Donut:** Customer Segment share

### Page 3 — Combined KPIs
- **Scatter:** Performance Rating (X) vs Revenue Generated (Y), size = Salary
- **Bar:** Revenue-to-Salary ratio (Top 15 reps)
- **Card:** Revenue Lost due to Attrition

## 6. Slicers to add on every page
- Year (from `order_date`)
- Region
- Department

## 7. Publish (optional)
File → Publish → sign in with a work/school Microsoft account → shows on app.powerbi.com.

---
**Note:** A ready-made HTML dashboard (`../07_html_dashboards/`) is also included as a preview of exactly how the Power BI dashboard should look.
