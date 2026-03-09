# 📊 Contoso Sales Performance Dashboard — Power BI

## 🗂️ Project Overview

An end-to-end **Business Intelligence solution** built in Power BI for Contoso, a multinational retail company. The project covers full data modeling, DAX measure development, feature engineering, and multi-audience dashboard design — targeting both **C-Level executives** and **Sales Operations teams**.

---

## 🎯 Business Objectives

- Provide **executive leadership** with a high-level view of overall business performance (revenue, profitability, growth).
- Equip **sales operations teams** with granular insights to monitor store, channel, and product-level performance.
- Enable **data-driven decisions** through interactive slicers, drill-throughs, and dynamic KPI tracking.

---

## 🛠️ Work Done

### 1. Data Modeling (Star Schema)
- Designed a clean **Star Schema** connecting 2 Fact tables to 7 Dimension tables.
- **Fact Tables:** `Fact_Sales`, `Fact_Marketing`
- **Dimension Tables:** `Dim_Product`, `Dim_Category`, `Dim_Subcategory`, `Dim_Stores`, `Dim_Geography`, `Dim_Promotion`, `Dim_Channel`
- Enforced correct **cardinality** and **relationship directions** across all tables.

### 2. Date Table (Custom Built)
- Built a custom `DATE NEW` table using DAX with full time intelligence support:
  - `Date`, `Month`, `Month Name`, `Quarter`, `Year`
- Marked as the **official date table** to enable time intelligence functions.

### 3. DAX Measures (15+ Measures)
All measures are organized in a dedicated `DAX_measures` table:

| Measure | Description |
|---|---|
| `Total_Sales` | Total revenue across all channels |
| `Net_Profit` | Revenue minus total cost |
| `Total Cost` | Aggregated cost of goods sold |
| `Margin %` | Net profit as a percentage of sales |
| `GROWTH` | Year-over-Year sales growth % |
| `Sales LY` | Sales for the previous year (time intelligence) |
| `Sales 2011` | Baseline year sales for benchmarking |
| `Ordered Amount` | Total value of orders placed |
| `Delivered Amount` | Total value of delivered orders |
| `Delivered %` | Delivery fulfillment rate |
| `AvgDiscount` | Average discount applied |
| `AVG ORDER` | Average order value |
| `Total Clicks` | Marketing engagement metric |
| `total qty` | Total units sold |
| `total return amount` | Total value of returned items |

### 4. Feature Engineering (Calculated Columns)
- Created calculated columns in `Fact_Sales` to enrich the dataset:
  - `TOTAL SALES` — row-level sales value
  - `Net Profit` — row-level profit
  - `TotalCost`, `UnitCost`, `UnitPrice` — cost breakdown per transaction

---

## 📊 Dashboard Pages

### 🔵 Page 1 — C-Level Executive Dashboard
**Audience:** CEO, CFO, Board of Directors

**KPIs:**
- Total Sales: **$8.24bn**
- Units Sold: **37M**
- Net Profit: **$4.69bn**
- Total Cost: **$3.55bn**
- Profit Margin: **56.9%**

**Visuals:**
- 📈 Sales Trend by Year (2011–2013)
- 📊 Sales by Product Category (Computers, Cameras, TV & Video, Cell Phones…)
- 📊 Profit & Sales by Sales Channel (Store, Online, Reseller, Catalog)
- 🍩 Sales Distribution by Continent (North America 59%, Asia 21%, Europe 19%)

---

### 🔴 Page 2 — Sales Team Operational Dashboard (Sales Team 1)
**Audience:** Sales Managers, Regional Directors

**KPIs:**
- Total Sales: **$2.61bn**
- Sales LY: **$3.11bn**
- YoY Growth: **-15.91%**
- Delivery Rate: **99.1%**
- Avg Discount: **12.29%**

**Visuals:**
- 📈 Sales Trend by Year
- 📊 Sales by Store (Top performing stores)
- 📊 Sales & Profit by Channel

---

### 🔴 Page 3 — Product Performance Dashboard (Sales Team 2)
**Audience:** Product Managers, Category Teams

**KPIs:**
- Total Sales: **$8.24bn**
- YoY Growth tracking
- Avg Discount: **12.25%**
- Net Profit: **$4.69bn**
- Total Qty: **37M**

**Visuals:**
- 📊 Sales & Profit by Category
- 📊 Sales by Subcategory (Camcorders, Projectors, Laptops, DSLR…)
- 📊 Top Products by Sales & Net Profit

---

## 🧩 Data Model Diagram

> Star Schema with 2 Fact tables + 7 Dimension tables

```
Dim_Category ──┐
Dim_Subcategory┤
Dim_Product ───┼──► Fact_Sales ◄──── Dim_Promotion
Dim_Stores ────┤         │
Dim_Geography ─┘         └──► DATE NEW
                               Dim_Channel
                          Fact_Marketing ◄── DATE NEW
```

---

## 💡 Key Insights

- **North America** drives **59%** of global revenue ($4.9bn).
- **Computers** is the top-selling category with **$3.17bn** in sales.
- **Store channel** leads all channels with **$4.8bn** in sales vs $2.7bn profit.
- Sales declined **~15.9% YoY** from 2011 to 2012/2013 — signaling a need for strategic intervention.
- **Delivery fulfillment rate** is exceptionally high at **99.1%**.

---

## 🚀 Tools & Technologies

| Tool | Usage |
|---|---|
| **Power BI Desktop** | Data modeling, DAX, Report design |
| **DAX** | KPIs, time intelligence, calculated columns |
| **Power Query (M)** | Data transformation & cleaning |
| **Star Schema** | Data warehouse design pattern |

---

## 📁 Project Structure

```
📦 contoso-sales-performance-powerbi/
 ┣ 📸 screenshots/
 ┃ ┣ home.png
 ┃ ┣ c_level_dashboard.png
 ┃ ┣ sales_team_1.png
 ┃ ┣ sales_team_2.png
 ┃ ┗ data_model.png
 ┗ 📄 README.md
```

---

## 👤 Author

**[Abdullah Ahmed]**
Data Analyst | Power BI Developer
[LinkedIn]([https://linkedin.com/in/yourprofile](https://www.linkedin.com/in/abdullah-ahmed-taha/))
