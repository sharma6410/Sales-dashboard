# 📊 Superstore Sales Dashboard — Case Study Analysis

**Tool:** Power BI Desktop  
**Dataset:** Superstore Sales (2014–2018)  
**Pages:** 2 — Overview Dashboard + Product Analysis  
**Author:** Aditi Sharma

---

## 🧩 Business Problem

A retail superstore operating across 4 regions in the US needed a unified view of its sales performance. Data was spread across years, regions, product categories, and individual SKUs — with no fast way to answer critical questions like:

- Which region is driving the most revenue?
- What is our actual profit margin, and which categories are most profitable?
- Which months are consistently strong or weak?
- Which products are our top earners, and which sub-categories should we invest in?

The goal was to build a **self-serve analytics dashboard** that any stakeholder — from a regional manager to a C-suite executive — could use without touching a spreadsheet or writing SQL.

---

## 📐 Dashboard Design

The report is split into **two focused pages**, each answering a distinct layer of business questions.

### Page 1 — Executive Sales Overview

A high-level command centre for leadership to monitor the business at a glance.

### Page 2 — Product Analysis

A deeper drill-down for category managers and buyers to understand what's selling, what's profitable, and what to prioritise.

---

## 📈 Page 1: Executive Sales Overview — Key Findings

### KPI Summary

| Metric | Value |
|---|---|
| Total Sales | **$2M** |
| Total Orders | **9,994** |
| Total Profit | **$286.40K** |
| Profit Margin % | **12.47%** |

A 12.47% profit margin on $2M in revenue signals a healthy but optimisable business. With 9,994 orders, the average order value sits around **$200** — suggesting a mix of low-ticket office supplies and high-ticket technology products.

---

### 📅 Monthly Sales Trend

The line chart reveals a clear **seasonal pattern**:

- **January–March:** Sales dip to their lowest (~$0.1M–$0.15M) — a classic post-holiday slowdown
- **April–August:** Gradual recovery and moderate steady growth
- **September–December:** A sharp acceleration, peaking in **November–December** (~$0.35M+) — driven by year-end corporate procurement cycles and holiday demand

**Insight:** The business is heavily back-loaded. Nearly 40% of annual revenue is generated in Q4. This creates a risk — a bad Q4 can wipe out a full year's growth. A strategic recommendation would be to run mid-year promotions in May–July to flatten the revenue curve.

---

### 🗺️ Total Sales by Region

| Region | Total Sales | Share |
|---|---|---|
| **West** | $0.73M | ~31% |
| **East** | $0.68M | ~29% |
| **Central** | $0.50M | ~21% |
| **South** | $0.39M | ~17% |

**West and East together account for ~60% of total revenue.** The South is the weakest region, generating barely half of what the West produces despite presumably similar market sizes.

**Insight:** The South represents the biggest untapped growth opportunity. A regional sales push, targeted promotions, or additional sales headcount in the South could meaningfully move the overall revenue needle.

---

### 🍩 Total Sales by Category

| Category | Sales Share |
|---|---|
| Technology | **36.4%** |
| Furniture | **32.3%** |
| Office Supplies | **31.3%** |

Sales are remarkably balanced across all three categories — no single category dominates. However, revenue share alone doesn't tell the full story. The real question is **which category is most profitable** — answered on Page 2.

---

## 🔍 Page 2: Product Analysis — Key Findings

### 💰 Total Profit by Category

The bar chart reveals a striking divergence from the sales share data:

| Category | Profit | Observation |
|---|---|---|
| **Technology** | ~$145K | Highest profit despite similar sales share |
| **Office Supplies** | ~$122K | Strong profit relative to its sales volume |
| **Furniture** | ~$18K | Disproportionately low profit vs. sales |

**Furniture is the most alarming finding.** It contributes 32.3% of revenue but generates only ~6% of total profit. This suggests heavy discounting, high return rates, shipping costs, or low-margin product mix within the category.

---

### 📊 Profit Margin % by Category

| Category | Profit Margin |
|---|---|
| **Technology** | ~17–18% |
| **Office Supplies** | ~15–16% |
| **Furniture** | ~2–3% |

Technology is the star of the portfolio — highest revenue share AND highest margin. Office Supplies punches above its weight with solid margins on relatively low-cost products. Furniture is a serious margin problem — nearly break-even when factoring in operational costs.

**Recommendation:** Audit the Furniture category for loss-making SKUs. Tables in particular (visible in the sub-category chart) are a known margin drain in superstore datasets. Consider restructuring pricing or reducing discounts on Furniture.

---

### 🏆 Top 10 Products by Sales

The top revenue-generating products are dominated by **high-ticket technology items**:

| Rank | Product |
|---|---|
| 1 | Canon imageCLASS (Copier) |
| 2 | Fellowes PB500 Electric Binding Machine |
| 3 | Cisco TelePresence System |
| 4 | HON 5400 Series Task Chair |
| 5 | GBC DocuBind TL300 |
| 6 | GBC Ibimaster 500 |
| 7 | Hewlett Packard LaserJet |
| 8 | HP Designjet T520 |
| 9 | GBC DocuBind P400 |

8 of the top 9 products are technology or binding/printing machines — confirming that **big-ticket B2B equipment** drives the revenue peaks. The lone exception is a HON office chair, which reflects the high ASP of premium furniture.

**Insight:** These products likely have long sales cycles and are driven by corporate procurement decisions — reinforcing the Q4 spike seen in the trend chart, when businesses spend down annual budgets.

---

### 📦 Sales by Sub-Category

The top sub-categories by total sales:

| Sub-Category | Observation |
|---|---|
| **Phones** | #1 sub-category — consistent corporate demand |
| **Chairs** | #2 — high ASP, but check margins |
| **Storage** | Steady volume |
| **Tables** | High sales but known margin problem |
| **Binders** | High volume, likely low margin |
| **Machines** | Low volume, very high ASP |
| **Copiers** | Anchors the top 10 products list |

**Phones and Chairs are the volume leaders.** Copiers appear lower in volume but dominate the top products list by individual sale value — meaning a single copier sale is worth many phone sales.

---

## 🎯 Strategic Recommendations

Based on the full dashboard analysis:

| Priority | Recommendation |
|---|---|
| 🔴 **Urgent** | Investigate Furniture margin — ~2–3% is unsustainable. Audit Tables sub-category for discounting patterns |
| 🟠 **High** | Run mid-year (May–July) promotions to reduce Q4 revenue concentration risk |
| 🟡 **Medium** | Double down on Technology — highest margin + highest revenue. Expand Phones and Copiers range |
| 🟢 **Growth** | Invest in the South region — it underperforms by ~47% vs. the West with likely similar market potential |
| 🔵 **Retention** | Identify the corporate buyers behind the top 10 products — these accounts drive outsized revenue and need dedicated account management |

---

## 🛠️ Technical Implementation

- **Data modelling** — fact table (orders) linked to dimension tables (date, product, geography) for accurate cross-filter behaviour
- **DAX measures** — custom calculations for Profit Margin %, Total Profit, and aggregated KPIs
- **Interactive slicers** — Year (2014–2018) and Region filters applied across all visuals simultaneously
- **Visual choices** — KPI cards for instant executive summary; line chart for trend; bar chart for regional comparison; donut for category share; clustered bar for sub-category ranking

---

## 📌 Conclusion

The Superstore Sales Dashboard transforms 5 years of raw transactional data into a clear, actionable picture of business health. The headline finding is a **tale of two categories**: Technology is the growth engine with strong margins, while Furniture is quietly eroding profitability despite solid revenue. Combined with a South region opportunity and a heavy Q4 dependence, this dashboard gives leadership exactly what they need to make faster, smarter decisions.
