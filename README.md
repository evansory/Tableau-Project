# 📊 Sales Performance and Customer Insights Dashboard

## 🧾 Introduction
This project outlines the development of two interactive Tableau dashboards designed to help stakeholders—such as sales managers, executives, and marketing teams—analyze sales performance and customer behavior. The dashboards are built to support data-driven decisions through dynamic visualizations and year-over-year comparisons.

---

## ❗ Problem Statement
In many organizations, sales and customer data are often siloed and difficult to analyze efficiently. Business stakeholders require accessible, real-time insights to monitor performance, identify trends, and make strategic decisions. This project addresses the need for a comprehensive, user-friendly tool that aggregates and visualizes key sales and customer metrics in one place.

---

## 🔍 Data Sourcing
The data used in this project simulates a retail sales environment and includes the following key information:
- Order details (sales, quantity, profit, order date)
- Product attributes (category, sub-category)
- Customer data (customer ID, name, segment)
- Regional data (region, state, city)
- [Sales-Dashboard-Materials](https://github.com/evansory/Tableau-Project/tree/main/Sales-Dashboard-Materials)

---

## 🧱 Data Modelling
To prepare the dataset for analysis in Tableau:
- Established relationships between fact and dimension tables
- Created a unified data model for seamless filtering and drill-down
- Ensured compatibility between fields for accurate aggregation and comparison
- ![](https://github.com/evansory/Tableau-Project/blob/main/Data%20Model.png)

---

## 🧹 Data Cleaning and Transformation
- Renamed fields and tables for clarity and consistency
- Verified and corrected data types (e.g., dates, numerics)
- Created calculated fields to support metrics such as YoY growth and weekly averages
- Filtered null or invalid records to ensure accuracy in visuals

---

## 🎯 Dashboard Specifications

### 📌 Sales Dashboard
![](https://github.com/evansory/Tableau-Project/blob/main/Sales%20Dash%20Tableau.png)
#### 🎯 Purpose
To provide a high-level and detailed view of sales performance, allowing stakeholders to analyze trends, compare metrics, and monitor year-over-year progress.

#### 🧾 Key Requirements
- **KPI Overview**: Display total sales, profit, and quantity for the current and previous year.
- **Sales Trends**: Show monthly data for each KPI over the two years and highlight months with peak and low performance.
- **Product Subcategory Comparison**: Compare performance by subcategory and evaluate sales versus profit.
- **Weekly Trends**: Display weekly sales and profit with average lines, and visually emphasize weeks above and below average.
---

### 👥 Customer Dashboard
![](https://github.com/evansory/Tableau-Project/blob/main/Customers%20Dashboard%20Tableau.png)
#### 🎯 Purpose
To help marketing teams and decision-makers understand customer engagement, behavior, and high-value relationships.

#### 🧾 Key Requirements
- **KPI Overview**: Present total customers, average sales per customer, and total orders for both years.
- **Customer Trends**: Monthly breakdowns of customer activity, highlighting the best and worst-performing months.
- **Customer Distribution**: Show order distribution to identify patterns in loyalty and engagement.
- **Top 10 Customers by Profit**: Highlight top customers along with their rank, order count, sales, profit, and last order date.

---

## 🎨 Design & Interactivity

- **Year Selection**: Dashboards are dynamic, allowing users to select and explore data for different years.
- **Navigation**: Easy switching between the Sales and Customer dashboards.
- **Interactive Charts**: Users can click charts to filter and explore related data.
- **Filter Options**: Users can filter by product category, sub-category, region, state, and city to narrow their analysis.

