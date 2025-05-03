# 📊 Sales Performance and Customer Insights Dashboard

## 📚 Table of Contents

- [Introduction](#-introduction)
- [Problem Statement](#-problem-statement)
- [Data Sourcing](#-data-sourcing)
- [Data Modelling](#-data-modelling)
- [Data Cleaning and Transformation](#-data-cleaning-and-transformation)
- [Dashboard Specifications](#-dashboard-specifications)
  - [Sales Dashboard](#-sales-dashboard)
  - [Customer Dashboard](#-customer-dashboard)
- [Design & Interactivity](#-design--interactivity)
- [Key Features](#-key-features)
- [Live Demo)](#-live-demo)
- [Conclusion](#-conclusion)
- [Recommendations](#-recommendations)


## 🧾 Introduction
This project outlines the development of two interactive Tableau dashboards designed to help stakeholders—such as sales managers, executives, and marketing teams—analyze sales performance and customer behavior. The dashboards are built to support data-driven decisions through dynamic visualizations and year-over-year comparisons.

---

## ❗ Problem Statement
In many organizations, sales and customer data are often siloed and difficult to analyze efficiently. Business stakeholders require accessible, real-time insights to monitor performance, identify trends, and make strategic decisions. This project addresses the need for a comprehensive, user-friendly tool that aggregates and visualizes key sales and customer metrics in one place.

---
## 🔍 Data Sourcing

The dataset used in this project was obtained from a public learning resource shared by **@DataWithBaraa** on YouTube. The dataset was provided as part of a Tableau dashboard tutorial and includes sample data on Orders, products, customers, and Locations.

📌 **Data Source**: [Sales Dashboard Tutorial by DataWithBaraa (YouTube)](https://www.youtube.com/@DataWithBaraa)

> Note: This dataset is intended for educational purposes and may not represent real-world business data.

The data used in this project simulates a retail sales environment and includes the following key information:
- Order details (sales, quantity, profit, order date)
- Product attributes (category, sub-category)
- Customer data (customer ID, name, segment)
- Locaton data (region, state, city)
- 
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
Sales KPI calculations
1. Current year sales
```sql
IF YEAR([Order Date]) = [Select Year]
THEN [Sales]
END
```
2. Previous year sales
```sql
IF YEAR([Order Date]) = [Select Year]-1
THEN [Sales]
END
```

3. Current year Profit
```sql
IF YEAR([Order Date])=[Select Year]
THEN [Profit]
END
```

4. Previous year Profit
```sql
IF YEAR([Order Date])=[Select Year] -1
THEN [Profit]
END
```

5. Current year Quantity
```sql
IF YEAR([Order Date]) = [Select Year]
THEN [Quantity]
END
```

6. Previous year Quantity
```sql
IF YEAR([Order Date]) = [Select Year] - 1
THEN [Quantity]
END
```

## 🎯 Dashboard Specifications

### 📌 Sales Dashboard
![](https://github.com/evansory/Tableau-Project/blob/main/Sales%20Dash%20Tableau.png)
#### 🎯 Purpose
To provide a high-level and detailed view of sales performance, allowing stakeholders to analyze trends, compare metrics, and monitor year-over-year progress.

#### 🧾 Key Requirements
- **KPI Overview**:
- Display total sales, profit, and quantity for the current and previous year.
- **Sales Trends**: Show monthly data for each KPI over the two years and highlight months with peak and low performance.
- **Product Subcategory Comparison**: Compare performance by subcategory and evaluate sales versus profit.
- **Weekly Trends**: Display weekly sales and profit with average lines, and visually emphasize weeks above and below average.
---

Customers KPI calculations
1. Current year Customers
```sql
IF YEAR([Order Date])= [Select Year]
THEN [Customer ID] 
END
```

2. Previous year Customers
```sql
IF YEAR([Order Date])= [Select Year] -1
THEN [Customer ID] 
END
```

3. Current year Orders
```sql
IF YEAR([Order Date]) = [Select Year]
THEN [Order ID]
END
```

4. Previous year Orders
```sql
IF YEAR([Order Date]) = [Select Year] -1
THEN [Order ID]
END
```

5. Current year Sales per Customer
```sql
SUM([CY sales]) / COUNTD([CY Customers])
```

6. Previous year SAles per Customer
```sql
SUM([PY sales]) / COUNTD([PY Customers])
```

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

- ## 🚀 Key Features
- Fully interactive dashboards built in Tableau
- Year-over-year comparisons across multiple metrics
- KPI highlights and trend visualizations
- Clean, professional UI with clear labeling and layout
- Filterable by date, product category, and geography

---

## 🔗 Live Demo 
click on the link below to view the project on Tableau
> [https://github.com/evansory/Tableau-Project/blob/main/Dynamic%20Sales%20and%20Customers%20Dashboard.twbx]



## ✅ Conclusion

This project successfully delivered two interactive Tableau dashboards that empower business stakeholders to monitor key sales and customer metrics in real time. Through effective data modeling, transformation, and visualization, the dashboards provide both high-level overviews and granular insights into performance trends, customer behavior, and product-level dynamics. The visual design ensures clarity and usability, while interactive elements enable users to explore the data from multiple perspectives.

The structured workflow—starting from requirement gathering to final dashboard development—demonstrates a solid foundation in both technical skills and analytical thinking. The dashboards are scalable and adaptable, ready to be enhanced further as business needs evolve.

---

## 💡 Recommendations

- **Automate Data Updates**: Integrate live or scheduled data refreshes to keep dashboards current without manual intervention.
- **Enhance User Roles**: Implement user-specific views (e.g., by region or team) to tailor insights to different stakeholder groups.
- **Expand Scope**: Add dashboards for other business domains such as inventory, shipping performance, or customer support to provide a more holistic business overview.
- **Incorporate Predictive Analytics**: Leverage tools like Tableau Prep, R, or Python to introduce forecasting models and deeper trend analysis.
- **User Training & Feedback Loop**: Provide brief training to stakeholders to maximize dashboard utility and collect feedback for continuous improvement.

---
## ✍️ Author

**Asamu Augustine**  
[LinkedIn](https://www.linkedin.com/in/augustineasamu/) | [Portfolio](#) | [Email](evansory9561@gmail.com)
