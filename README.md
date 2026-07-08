# Employee & Sales Analytics — Complete Data Analysis Project

A **full-stack data analyst portfolio project** built with SQL, Excel, Power BI, Pandas & NumPy.

## Project Overview
Two datasets — **Employees** (250 rows) and **Sales** (5,000 orders across 2022–2025) —
are analysed end-to-end to answer real business questions on attrition, compensation, revenue growth,
regional performance and customer segmentation.

## Folder Structure
```
EmployeeSalesAnalytics/
├── 01_datasets/           # CSV data (employees, sales, products, customers, departments)
├── 02_sql/                # Schema + 25+ analysis queries (MySQL / PostgreSQL / SQLite)
├── 03_excel/              # Ready-to-open .xlsx workbooks with pivot summaries & native charts
├── 04_python_notebooks/   # 4 Jupyter notebooks (Pandas + NumPy + Matplotlib)
├── 05_powerbi/            # Step-by-step Power BI build guide + all DAX formulas
├── 06_reports/            # Final PDF report
├── 07_html_dashboards/    # Interactive Plotly HTML dashboards (Power BI preview)
└── README.md
```

## How to Use

### 1. SQL
Open any MySQL / PostgreSQL / SQLite client. Run `02_sql/01_schema.sql`, then import CSVs, then explore `03_*` and `04_*` and `05_*` queries.

### 2. Excel
Just double-click `03_excel/Employee_Analysis.xlsx` and `Sales_Analysis.xlsx`. All charts render natively.

### 3. Python (Pandas / NumPy)
```bash
pip install pandas numpy matplotlib jupyter
jupyter notebook 04_python_notebooks/
```
Run notebooks 01 → 04 in order.

### 4. Power BI
Follow `05_powerbi/PowerBI_Setup_Guide.md`. Download **Power BI Desktop** (free), load the CSVs,
paste the DAX formulas from `DAX_Formulas.md`, and build the exact dashboard shown in the HTML preview.

### 5. Preview Dashboards without Power BI
Open `07_html_dashboards/employee_dashboard.html` and `sales_dashboard.html` in any browser —
this is exactly how your Power BI dashboard will look after following the guide.

### 6. Final Report
`06_reports/Final_Project_Report.pdf` — 5-page executive summary with all findings.

---
Built as a portfolio-ready project. Every file is production-quality and can be shown directly to recruiters.
