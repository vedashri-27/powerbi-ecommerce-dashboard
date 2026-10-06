# E-Commerce Sales Dashboard (Power BI)

An interactive sales dashboard I built in Power BI to explore an online retail
store's orders — what sells, who buys, how they pay, and where the profit
actually comes from. It's one of my first Power BI projects.

![Dashboard](screenshots/dashboard.png)

## What it shows

The report pulls two tables (Orders + Details) into Power BI, connects them, and
summarises the business on a single page:

- **KPI cards** — total amount (118K), quantity sold (1K), profit (12K) and
  average order value (AOV).
- **Profit by month** — profit was strongest in November and actually went
  negative in December, which stood out and is worth digging into.
- **Payment mode** — Cash on Delivery dominates (44%), followed by UPI (22%).
- **Category & sub-category** — Clothing is ~66% of quantity sold, while on
  profit the top sub-categories are Printers, Sarees and Chairs.
- **Top customers and top states** — Maharashtra leads on sales amount.
- **Quarter slicer** — buttons to filter the whole page by Qtr 1–4.

## Files

- `Ecommerce_Dashboard.pbix` — the Power BI report (open with Power BI Desktop)
- `Orders.csv` — order-level data (customer, state, date, payment mode)
- `Details.csv` — line-item data (category, sub-category, amount, profit, quantity)
- `screenshots/dashboard.png` — preview image used above

## How I built it

1. Loaded `Orders.csv` and `Details.csv` into Power BI.
2. Cleaned the columns and set the relationship between the two tables (joined on Order ID).
3. Built the measures (sum of amount, profit, quantity, AOV).
4. Added the visuals — KPI cards, donut charts, bar charts, a monthly profit column chart — and a quarter slicer to filter everything at once.

## What I'd add next

- A proper date table so I can slice by month/quarter more cleanly.
- A profit-margin % measure, not just absolute profit.
- Look into why December profit turned negative (returns? discounts?).

*Data is a sample e-commerce dataset, used for practice.*
