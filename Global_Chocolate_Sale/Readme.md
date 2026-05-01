# 🍫 Chocolate Sales Dashboard

> Power BI dashboard analysing 2021 sales performance for **Awesome Chocolate Co.** across 6 countries, 22 products, and 25+ salespeople.

![dashboard-preview.png](https://github.com/Kaushal-2371/BI_Dashboards/blob/main/Global_Chocolate_Sale/Dash_Pic.png?raw=true)

---

## 📊 Overview

This dashboard was built in **Microsoft Power BI Desktop** using a star schema data model. It enables data-driven decisions on regional performance, product strategy, and sales team effectiveness.

| Field | Details |
|-------|---------|
| **Tool** | Microsoft Power BI Desktop |
| **Data Period** | January 2021 – December 2021 |
| **Total Records** | 3,300 sales transactions |
| **Countries** | India, New Zealand, UK, Canada, USA, Australia |
| **Categories** | Bars, Bites, Other |
| **Salespeople** | 25+ across Yummies, Delish, Jucies teams |

---

## 🗂️ Data Model

Star schema — all relationships flow from dimension tables → fact table (single direction).

| Table | Type | Key Fields |
|-------|------|------------|
| `Sales` | Fact | Salesperson, Geography, Product, Date, Amount, Customers, Boxes |
| `People` | Dimension | Salesperson, Team, Picture |
| `Products` | Dimension | Product, Category, Size |
| `Locations` | Dimension | Geo, Region |
| `DateTable` | Dimension | Date, Year, Month, Quarter *(created via DAX)* |

---

## 📈 KPIs

| Metric | Value |
|--------|-------|
| Total Sales | $18.63M |
| Total Boxes | 1.09M |
| Total Customers | 535K |
| Shipments | 3,300 |
| Sales per Box | $17.02 |

---

## 🧮 DAX Measures

```dax
Total Sales    = SUM(Sales[Amount])
Total Boxes    = SUM(Sales[Boxes])
Total Customers = SUM(Sales[Customers])
Shipments      = COUNTROWS(Sales)
Sales per Box  = DIVIDE([Total Sales], [Total Boxes])
```

---

## 💡 Key Insights

- 🥇 **India** leads all countries at **$3.25M** in sales
- 📦 **Bars** is the top category — **$9.19M** (49% of total revenue)
- 📅 **December** was the strongest month ($1.83M); **September** was the weakest ($1.27M)
- 🏆 **Rafaelita Blaksland** is the top salesperson at **$814K**
- 🌍 All 6 countries are within ~6% of each other — very balanced geographic spread

---

## 📁 File Structure
```
├── chocolate-dashboard.pbix   # Power BI file<br>
├── dashboard-preview.png      # Dashboard screenshot<br>
└── README.md                  # This file
```
---

## 🚀 How to Use

1. Open `chocolate-dashboard.pbix` in Power BI Desktop
2. Verify all 5 relationships in Model view (dimension → Sales)
3. Use the date range picker to filter by period
4. Use the Region / Category / Salesperson dropdowns to slice data
5. Click any chart element — all visuals cross-filter automatically
