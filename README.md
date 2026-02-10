

# Online Retail SQL Analytics

Welcome to the **Online Retail SQL Analytics Project**! 🚀  
This project demonstrates how raw sales data can be transformed and analyzed to generate actionable business insights using SQL. It is designed as a portfolio project to showcase skills in SQL, data analysis, data cleaning, and reporting.

---

## Project Objective

**Business Analytics & Reporting:**  
- Transform raw sales data into a structured format suitable for analysis.  
- Clean, validate, and deduplicate data to ensure accuracy.  
- Generate actionable insights on **customer behavior**, **product performance**, and **sales trends** using SQL queries and aggregations.  
- Present findings using KPIs, segments, and aggregated metrics to support business decision-making.  

---

## Data Flow & Architecture

Diagrams are included in the `/docs` folder:  

- **[Data Flow Diagram](docs/DataFlow.drawio.png)** – Shows how data moves from raw CSVs into structured tables and views.  
- **[Data Architect Diagram](docs/DataArchitect.drawio.png)** – Illustrates objects (tables, views), transformations, and business-level aggregates.  

---

## Layers Overview

### Bronze Layer
- **Object Type:** Table (`bronze.online_retail`)  
- **Purpose:** Raw data ingestion from CSV.  
- **Loading Method:** Full load via truncate and insert.  
- **Transformations:** None (raw data preserved).  

### Silver Layer
- **Object Type:** Table (`silver.online_retail_clean`)  
- **Purpose:** Cleaned and typed data ready for analysis.  
- **Transformations:** Data type conversion, trimming spaces, deduplication, null handling, and basic validation.  

### Gold Layer
- **Object Type:** Views (8 views for customer, product, and sales reporting)  
- **Purpose:** Business-level aggregates, KPIs, and segmentation for decision-making.  
- **Transformations:** Aggregation, revenue calculation, customer/product segmentation, and trend analysis.  

**Views Included:**  
1. `customer_sales_report` – Aggregates revenue, quantity, orders, and segments customers by value.  
2. `customer_segment_report` – Summarizes customer counts and percentages by segment.  
3. `product_sales_report` – Aggregates revenue, quantity sold, and segments products by performance.  
4. `product_segment_report` – Summarizes product counts and revenue percentages by segment.  
5. `sales_by_country` – Shows total revenue, orders, and quantity per country.  
6. `sales_by_customer` – Displays total revenue, orders, and quantity per customer.  
7. `sales_trend_by_month` – Shows monthly sales trends for revenue, quantity, and orders.  
8. `top_selling_products` – Lists products by total revenue and quantity sold.  

---

## Dataset

The dataset (`online_retail.csv`) is included in the `/dataset` folder.  

---

## How to Run / Reproduce

1. Clone this repository to your local machine.  
2. Place the raw CSV (`online_retail.csv`) in the `/dataset` folder (already included).  
3. Execute the SQL scripts in the following order:  
   - **Bronze Layer:** `bronze.proc_load_bronze_online_retail`  
   - **Silver Layer:** `silver.proc_load_silver_online_retail`  
   - **Gold Layer:** Views for analytics and reporting.  
4. Refer to the diagrams in `/docs` to understand the data flow and architecture.  

---

## Tests

Quality checks are provided in the `/tests` folder for both Bronze and Silver layers to ensure data cleanliness, consistency, and validity. These tests help identify issues like null values, duplicates, negative numbers, or incorrectly formatted data before analysis.

---

## Example Analytics Queries

**1. Top 5 Customers by Revenue**
```sql
SELECT TOP 5 CustomerID, NetRevenue
FROM gold.customer_sales_report
ORDER BY NetRevenue DESC;

**2. Monthly Sales Trend**
```sql
SELECT SalesYear, SalesMonth, TotalRevenue
FROM gold.sales_trend_by_month
ORDER BY SalesYear DESC, SalesMonth DESC;

---

## License

This project is licensed under the MIT License. You are free to use, modify, and share it with proper attribution.

---

## About Me

Hi! I’m Meenakshi Singh, an aspiring Data Analyst with a strong foundation in SQL and Excel. I enjoy transforming raw data into meaningful insights, understanding relationships in data, and creating KPIs that help businesses make better decisions. This project reflects my hands-on approach to data analysis and reporting.
