# Retail Sales Dashboard — Power BI (In Progress)

A one-page Power BI sales dashboard built from a 300-row retail dataset (Jan–Jun 2026).

## Status
Dataset and full build guide are in this repo. The dashboard itself is being assembled in Power BI Desktop following the guide — this project is honestly marked **In Progress** until the `.pbix` is finished.

## Dashboard plan
- **KPI cards:** Total Sales, Total Profit, Total Orders, Avg Order Value
- **Bar chart:** Sales by City
- **Line chart:** Sales by Month
- **Donut chart:** Sales by Category
- **Table:** Product-wise Sales, Profit, Profit %
- **Slicers:** City, Channel

## DAX measures
- `Total Sales = SUM(retail_sales_powerbi[Sales])`
- `Total Profit = SUM(retail_sales_powerbi[Profit])`
- `Total Orders = COUNTROWS(retail_sales_powerbi)`
- `Avg Order Value = DIVIDE([Total Sales], [Total Orders])`
- `Profit % = DIVIDE([Total Profit], [Total Sales])`

## Files
- `retail_sales_powerbi.csv` — the dataset (Date, Product, Category, City, Qty, Sales, Profit, Channel)
- `BUILD_GUIDE.md` — step-by-step build instructions

## Skills used
Power BI, Power Query, basic DAX, dashboard design.
