# Sales Analysis: Profit, Logistics and Seasonality (Python)

## Goal
Analyze company sales data to find what drives profit (products, sales channels, countries), how long shipments take, and how sales change over time.

## Data
Three CSV tables:
- `events.csv`: orders (dates, units sold, price, cost, country code, sales channel)
- `products.csv`: product categories
- `countries.csv`: country names and regions

## What I did
1. Loaded and inspected the data (shape, types, missing values).
2. Cleaned it: removed 2 rows with missing `Units Sold`, replaced 82 missing country codes with `Unknown`, converted dates to datetime, converted units to integers.
3. Merged the three tables and calculated Revenue, Cost and Profit.
4. Calculated KPIs and built visualizations: profit by product category, sales channel, region and country; shipment time (order date to ship date); profit over time; sales by weekday; product seasonality heatmap.

**Tools:** Python, pandas, NumPy, matplotlib, seaborn, Google Colab.

## Key findings
- Revenue is over $1.7B and profit is $501.4M (margin about 29.4%).
- Average order value is about $1.28M, which points to a B2B (wholesale) business.
- Cosmetics is the most profitable category, followed by Office Supplies and Household. Fruits and Vegetables bring the least profit.
- Profit is split about 50/50 between Online and Offline channels.
- Top 3 countries by profit: Andorra, Ukraine, Malta.
- Average shipment time is about 25 days (maximum 50). Correlation between shipment time and profit is weak (0.06).
- Profit peaks every January. Friday and Monday are the strongest days, Thursday is the weakest.
- Products show clear seasonality, for example Meat peaks in December and June, Fruits in March and October.

## Recommendations
- Speed up shipping for Office Supplies and for key markets (Andorra, Ukraine).
- Run promotions on Wednesday evening and Thursday to balance weekly demand.
- Keep investing in high-margin categories (Cosmetics, Office Supplies).

## Files
- `sales_analysis.ipynb`: full analysis with code and charts
