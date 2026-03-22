# 📊 Superstore Sales Dashboard — Power BI

An interactive 2-page Power BI report built on 5 years of superstore sales data (2014–2018), designed to give leadership and category managers instant visibility into revenue, profit, and product performance — with no SQL or data team needed.

---

## 🖼️ Dashboard Preview

### Page 1 — Executive Sales Overview
![Superstore Sales Dashboard](images/dashboard_page1.png)

### Page 2 — Product Analysis
![Product Analysis](images/dashboard_page2.png)

---

## 🧩 Problem Statement

Sales data spanning 5 years, 4 regions, 3 product categories, and thousands of SKUs existed in raw tabular form with no unified view. Leadership had no fast way to:
- Track monthly revenue trends across the year
- Compare regional performance side by side
- Understand which categories and products were actually profitable

This dashboard solves all three — interactively, in a single `.pbix` file.

---

## 📋 Report Pages

### Page 1 — Superstore Sales Dashboard (Executive Overview)

| Visual | Description |
|---|---|
| **4 KPI Cards** | Total Sales ($2M), Total Orders (9,994), Total Profit ($286.40K), Profit Margin % (12.47%) |
| **Monthly Sales Trend** | Line chart showing sales across all 12 months — reveals strong Q4 seasonality |
| **Total Sales by Region** | Horizontal bar chart — West ($0.73M) leads, South ($0.39M) trails |
| **Total Sales by Category** | Donut chart — Technology (36.4%), Furniture (32.3%), Office Supplies (31.3%) |
| **Slicers** | Year filter (2014–2018) and Region filter (Central, East, South, West) — cross-filter all visuals |

### Page 2 — Product Analysis (Deep Dive)

| Visual | Description |
|---|---|
| **Top 10 Products by Sales** | Horizontal bar — Canon imageCLASS leads at ~$60K+, followed by Fellowes PB500 and Cisco TelePresence |
| **Sales by Sub-Category** | Horizontal bar — Phones and Chairs top the list (~$0.3M each); Bookcases at the bottom |
| **Total Profit by Category** | Clustered bar — Technology (~$145K) and Office Supplies (~$122K) dominate; Furniture (~$18K) lags far behind |
| **Profit Margin % by Category** | Bar chart — Technology (~17%) and Office Supplies (~16%) are healthy; Furniture (~2–3%) is nearly break-even |
| **Slicers** | Year (2014–2018) and Region (Central, East, South, West) — consistent with Page 1 |

---

## 💡 Key Insights

**1. Furniture is a margin crisis**
Furniture contributes 32.3% of total revenue — almost equal to Technology — but generates only ~$18K in profit vs Technology's ~$145K. Its profit margin of ~2–3% is unsustainable and likely driven by heavy discounting or high return/shipping costs.

**2. Technology is the real profit engine**
With 36.4% revenue share and ~17% profit margin, Technology is the strongest category on both dimensions. The Canon imageCLASS copier alone is the single highest-selling product in the entire dataset at ~$60K+.

**3. Strong Q4 seasonality**
The Monthly Sales Trend shows a clear dip from January through mid-year, then a sharp acceleration from September through December. The business is heavily back-loaded with Q4 driving disproportionate revenue.

**4. West and East carry the business**
West ($0.73M) and East ($0.68M) together account for ~60% of total sales. The South ($0.39M) underperforms significantly — nearly half the West's output — representing the clearest growth opportunity.

**5. Phones and Chairs dominate sub-categories**
In the product drill-down, Phones and Chairs both approach $0.3M in sales — far ahead of all other sub-categories. Tables appear in the top 5 by sales but carry poor margins within the Furniture category.

---

## 🛠️ Technical Details

**Built with:** Power BI Desktop
**Data source:** Superstore Sales dataset (Excel/CSV)
**Time period:** 2014–2018
**Records:** 9,994 orders

### DAX Measures Used

```dax
-- Total Sales
Total Sales = SUM(Orders[Sales])

-- Total Profit
Total Profit = SUM(Orders[Profit])

-- Profit Margin %
Profit Margin % = DIVIDE([Total Profit], [Total Sales])

-- Total Orders
Total Orders = COUNTROWS(Orders)
```

### Data Model
- Fact table: `Orders` (sales, profit, quantity, discount per line item)
- Dimension tables: `Date`, `Product`, `Customer`, `Geography`
- Relationships defined for accurate cross-filter behaviour across all visuals

---

## 🎯 Strategic Recommendations

| Priority | Action |
|---|---|
| 🔴 Urgent | Audit Furniture sub-categories — especially Tables — for discount rates and return costs |
| 🟠 High | Reduce Q4 dependency by running targeted mid-year promotions (May–July) |
| 🟡 Medium | Expand Technology range — highest margin and highest revenue simultaneously |
| 🟢 Growth | Invest in South region sales — biggest gap vs. market potential |

---

## 👩‍💻 Author

**Aditi Sharma** — B.Tech CSE (Data Science), Class of 2026
📧 aditias0101@gmail.com · [LinkedIn](https://linkedin.com/in/aditi-sharma-5a1a31289)
