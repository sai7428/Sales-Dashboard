
# 🧭 Interactive Sales Dashboard — Power BI Edition

## 📘 Project Overview
This repository contains a **fully interactive sales dashboard** built using **Microsoft Power BI** to analyze the **SuperMarket Analysis** dataset.  
It was developed as the final project for the *Visualization and Storytelling* module.

The assignment brief allowed using **either Tableau or Power BI**, and this project **intentionally uses Power BI** due to its powerful data modeling capabilities, integration with DAX (Data Analysis Expressions), and dynamic visualization features.  

The dashboard simulates a real-world business environment where a Data Analyst must provide actionable insights to help a mid-sized retail company optimize sales performance.

---

## 📂 Repository Structure
```

Sales-Dashboard/
├── Sales Dashboard.pbix             ← Power BI Dashboard file
├── SuperMarket Analysis.csv         ← Dataset used in the dashboard
└── README.md                        ← Project documentation

````

---

## 🧩 Dashboard Overview

The Power BI dashboard is designed with **five interactive pages**, each addressing specific business questions and stakeholder needs:

### 1. 🏠 Main Dashboard
- Displays key KPIs including **Total Sales**, **Gross Income**, **Average Customer Rating**, and **Transaction Count**.  
- Provides a quick snapshot of overall business performance.

### 2. 🌍 Regional Insights
- Compares **sales**, **profitability**, and **customer satisfaction** across cities:  
  **Yangon**, **Mandalay**, and **Naypyitaw**.  
- Supports branch-level performance analysis and benchmarking.

### 3. 📦 Product Performance
- Evaluates **sales and profit contribution** by product line.  
- Identifies top-performing categories and underperforming segments for inventory optimization.

### 4. 👥 Customer & Payment Insights
- Analyzes customer demographics (**Gender**, **Customer Type**) and **Payment Preferences** (E-Wallet, Cash, Credit Card).  
- Helps the marketing team target promotions effectively.

### 5. ⏰ Time Analysis & Forecasting
- Visualizes **daily and monthly sales trends**.  
- Uses Power BI’s built-in **forecasting tools** to predict future sales performance.  

---

## 🧠 Technical Details

| Feature | Description |
|----------|--------------|
| **Tool Used** | Microsoft Power BI |
| **Dataset** | SuperMarket Analysis (CSV) |
| **Language** | Data Analysis Expressions (DAX) |
| **Data Source** | Static dataset downloaded from Kaggle |
| **Data Model** | Single-table model with additional Date Table for time intelligence |

### Key DAX Measures
```DAX
Profit Margin % = DIVIDE([Gross Income], [Total Sales], 0) * 100
````

```DAX
Sales Growth % = ( [Current Month Sales] - [Previous Month Sales] ) / [Previous Month Sales]
```

A **Date Table** was created using:

```DAX
Date = CALENDAR(MIN(Sales[Date]), MAX(Sales[Date]))
```

This enables **Year-to-Date (YTD)** calculations, rolling totals, and other time-based comparisons.

---

## 🧩 How to Use This Dashboard

### 🔹 Step 1: Download the Files

1. In this repository, click **Raw → Download** for both files:

   * `Sales Dashboard.pbix`
   * `SuperMarket Analysis.csv`
2. Save them in the same local folder (e.g., `Documents/PowerBI Projects/SalesDashboard/`).

---

### 🔹 Step 2: Open in Microsoft Power BI Desktop

1. Open **Microsoft Power BI Desktop**.
2. Click **File → Open → Sales Dashboard.pbix**.
3. If prompted about missing data source:

   * Go to **Transform Data → Edit Queries**.
   * In the **Source** step, update the file path to where your CSV is saved:

     ```
     Source = Csv.Document(File.Contents("C:\Users\<YourName>\Documents\PowerBI Projects\SuperMarket Analysis.csv"), [Delimiter=",", Columns=...])
     ```
   * Click **Close & Apply**.

---

### 🔹 Step 3: Explore the Interactive Dashboard

* Use **filters and slicers** to analyze sales by branch, product, city, customer type, and payment method.
* Navigate between pages for:

  * **KPI Overview**
  * **Regional & Product Insights**
  * **Customer Analysis**
  * **Time Forecasting**
* Hover or click visuals for interactive cross-filtering.

---

## 💡 Tool Selection Note

> The module permitted using either **Tableau** or **Power BI**.
> Power BI was selected for this project because it offers advanced data modeling, DAX calculations, and flexible interactivity—perfect for meeting the module’s visualization and storytelling learning outcomes.

---

## 📊 Insights & Findings

* **Branch C (Naypyitaw)** had the highest sales and profitability.
* **Member customers** generated higher transaction values, showing loyalty benefits.
* **E-Wallet** payments are rising, suggesting a digital payment shift.
* **Food & Beverages** emerged as the most profitable and stable product line.
* **Forecasts** indicate continued sales growth, demonstrating business sustainability.

---

## 🔍 Evaluation & Reflection

**Strengths:**

* Strong alignment with business KPIs.
* Clear, interactive visuals and storytelling elements.
* Accurate use of DAX and time intelligence functions.

**Limitations:**

* Dataset is static (no live connection).
* Limited demographic detail (no age/income segmentation).
* Real-time or predictive analytics could enhance future iterations.

---

## 🏁 Conclusion

This Power BI Sales Dashboard successfully translates static sales data into an actionable, story-driven business intelligence tool.
It allows stakeholders—from the VP of Sales to Branch Managers—to make data-informed decisions by exploring regional, product, customer, and time-based performance.

The project demonstrates how **Power BI** can transform raw data into a visual narrative that drives strategic insights and supports organizational growth.

---

## 🙏 Acknowledgements & References

* **Few, S.** (2012). *Show Me the Numbers: Designing Tables and Graphs to Enlighten*.
* **Knaflic, C. N.** (2015). *Storytelling with Data: A Data Visualization Guide for Business Professionals*.
* **Kirk, A.** (2019). *Data Visualisation: A Handbook for Data Driven Design*.
* **Faresashraf1001 (2023).** *Supermarket Sales Dataset*. Kaggle.

---

## 👤 Author Information

**Author:** Sai Harshith Thoutam
**Course:** MSc Data Analytics
**Module:** Visualization and Storytelling
**Institution:** BSBI (Berlin School of Business and Innovation)
**Year:** 2025

--
