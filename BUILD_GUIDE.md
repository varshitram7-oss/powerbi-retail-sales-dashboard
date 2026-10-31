# Project 3 — Power BI Sales Dashboard (build guide)

Dataset: `retail_sales_powerbi.csv` — 300 rows: Date, Product, Category, City, Qty, Sales, Profit, Channel (Jan–Jun 2026).

Note, honestly: a .pbix file cannot be authored outside Power BI Desktop, so for this project YOU assemble the dashboard in Power BI Desktop (free) following these steps — the assembly is the learning, and it takes about an hour once Excel/SQL thinking is in place.

## Steps
1. Power BI Desktop → Get Data → Text/CSV → load `retail_sales_powerbi.csv`.
2. In Power Query, check types: Date = date, Qty/Sales/Profit = whole numbers, the rest = text. Close & Apply.
3. Create these measures (Home → New measure) — type each one yourself:
   - `Total Sales = SUM(retail_sales_powerbi[Sales])`
   - `Total Profit = SUM(retail_sales_powerbi[Profit])`
   - `Total Orders = COUNTROWS(retail_sales_powerbi)`
   - `Avg Order Value = DIVIDE([Total Sales], [Total Orders])`
   - `Profit % = DIVIDE([Total Profit], [Total Sales])`
4. Page layout (one page, one story):
   - Top row: 4 cards — Total Sales, Total Profit, Total Orders, Avg Order Value
   - Left: bar chart — Sales by City
   - Middle: line chart — Sales by Month (Date hierarchy → Month)
   - Right: donut chart — Sales by Category
   - Bottom: table — Product, Sales, Profit, Profit %
   - Slicers: City and Channel
5. Format: title "Retail Sales Dashboard — Jan to Jun 2026", one accent colour, no clutter.
6. Write a 3-line insight summary: top city, top category, and one thing the trend shows.
7. Save as `Retail_Sales_Dashboard.pbix` in this folder and export a PDF/PNG of the page for your portfolio.

## Interview lines you can honestly say after building it
- "I built a one-page Power BI dashboard from a 300-row sales dataset — KPI cards, city and category breakdowns, month trend, with slicers for city and channel."
- "I wrote basic DAX measures: total sales, average order value, and profit percentage."
