# Sales & Customer Dashboards | Tableau

Two interactive Tableau dashboards that show how the business performed in **2023 compared to 2022**. The Sales Dashboard tracks revenue, profit and product performance. The Customer Dashboard shows who is buying, how often, and who is most valuable.

I built both from scratch, starting from a client user story and a raw dataset.

🔗 **Live dashboard:** [Tableau Public Link](https://public.tableau.com/app/profile/mohammed.adnan2171/viz/sales-customer-dashboard/SalesDashboard)

---

## Dashboards

### Sales Dashboard
![Sales Dashboard](Dashboard%20images/sales-db.png)

### Customer Dashboard
![Customer Dashboard](Dashboard%20images/customer-db.png)

---

## Business Problem

Sales managers, executives and the marketing team needed one place to answer simple questions:

- Are we growing compared to last year?
- Which products make money, and which ones lose money?
- Which months and weeks are strongest or weakest?
- How loyal are our customers, and who are our best ones?

The full list of client requirements is in [`docs/Business_Requirements.docx`](docs/Business_Requirements.docx).

---

## Key Results (2023)

| Metric | 2023 | vs 2022 |
|---|---|---|
| Total Sales | €733K | ▲ 20.4% |
| Total Profit | €93K | ▲ 14.2% |
| Total Quantity | 12K units | ▲ 26.8% |
| Total Customers | 693 | ▲ 8.6% |
| Sales per Customer | €1.1K | ▲ 10.8% |
| Total Orders | 1,687 | ▲ 28.3% |

Sales grew faster than profit, so the profit margin dropped slightly. The full story is in [`docs/Insights.docx`](docs/Insights.docx).

---

## Documentation

| Document | What it covers |
|---|---|
| [Business Requirements](docs/Business_Requirements.docx) | What the client asked for in the Sales and Customer dashboards, plus a checklist showing how each requirement was delivered |
| [Insights Report](docs/Insights.docx) | A short data story: what happened in 2023, why it matters, and what to do next, with charts and clear recommendations |

---

## What's Inside

**Sales Dashboard**
- KPI cards for Sales, Profit and Quantity with year-over-year change
- Monthly trend lines, 2023 vs 2022, with the highest and lowest month marked
- Sales and profit by sub-category, with loss-making products flagged
- Weekly sales and profit trends against the weekly average

**Customer Dashboard**
- KPI cards for Customers, Sales per Customer and Orders with year-over-year change
- Monthly trend lines, 2023 vs 2022, with the highest and lowest month marked
- Customer distribution by number of orders
- Top 10 customers by profit, with last order date, sales and order count

**Navigation:** buttons at the top switch between the two dashboards, and a filter panel is available on both.

---

## Data

Source: Kaggle (Superstore-style sales dataset). The data is split into four tables.

| File | What it holds | Rows |
|---|---|---|
| `Orders.csv` | One row per order line: dates, ship mode, segment, sales, quantity, discount, profit | 9,994 |
| `Customers.csv` | Customer ID and name | 793 |
| `Products.csv` | Product ID, category, sub-category, product name | 1,894 |
| `Location.csv` | Postal code, city, state, region, country | 632 |

**How the tables connect**

- `Orders` → `Customers` on **Customer ID**
- `Orders` → `Products` on **Product ID**
- `Orders` → `Location` on **Postal Code**

**Coverage:** orders from 2020 to 2023. The dashboards focus on 2023 and compare it with 2022.

**Data notes**
- Files use `;` as the separator and a comma as the decimal mark (for example `261,96`).
- Dates are in `dd/mm/yyyy` format.
- `Products.csv` has 32 repeated Product IDs and `Location.csv` has 2 repeated Postal Codes. Handle duplicates before joining, or the numbers will be inflated.

---

## Tools

- **Tableau** (Desktop / Public) for the dashboards
- **Kaggle** for the dataset


---

## How to View

1. Open the **live dashboard** link above, or
2. Download the `.twbx` file and open it in Tableau Desktop or Tableau Public.

---

## Author

**Mohammed Adnan** | [LinkedIn](www.linkedin.com/in/a-dnan)
