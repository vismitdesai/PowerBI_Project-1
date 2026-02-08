# 📊 Power BI Sales & Profit Analysis Dashboard

## 📌 Project Overview
This project is a **Power BI dashboard** designed to analyze sales performance, production costs, and profitability for the *Apocolypse Store*.  
The report provides clear insights into revenue, costs, units sold, and overall profit using interactive visuals and DAX measures.

The goal is to transform raw transactional data into **actionable business intelligence**.

---

## 🛠 Tools & Technologies
- **Power BI Desktop**
- **DAX (Data Analysis Expressions)**
- **Power Query (ETL)**
- **Excel / CSV (Data Source)**

---

## 📂 Data Model
The data model follows a **star schema** design:

- **Fact Table**
  - Sales (Units Sold, Revenue calculations)

- **Dimension Tables**
  - Products
  - Store / Pricing
  - Date (if applicable)

Relationships are configured to ensure accurate filtering and aggregation across visuals.

---

## 📐 Key DAX Measures
Example profit calculation used in the report:

```DAX
Profit :=
SUMX(
    'Apocolypse Sales',
    ('Apocolypse Store'[Price] - 'Apocolypse Store'[Production Cost])
        * 'Apocolypse Sales'[Units Sold]
)
