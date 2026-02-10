# Online Retail SQL Analytics 🚀

Welcome to the **Online Retail SQL Analytics** project!  
This project demonstrates a complete end-to-end analytics solution for an online retail dataset, from raw data ingestion to actionable business insights. It highlights hands-on skills in SQL, data cleaning, transformation, and reporting, designed for a **Junior Data Analyst portfolio**.

---

## Project Objective

The goal of this project is to consolidate and analyze sales data to generate meaningful insights into **customer behavior, product performance, and overall sales trends**. Using SQL Server, the project applies **data warehousing concepts** and **data quality best practices** to prepare clean, analytics-ready data.

---

## Dataset

The dataset used in this project is included in the `/dataset` folder.  
It contains **raw sales data (online_retail.csv)** from an online retail store.

---

## Documentation & Diagrams

Project diagrams are available in the `/docs` folder:

- **Data Flow Diagram**: [DataFlow.drawio.png](docs/DataFlow.drawio.png)  
- **Data Architecture Diagram**: [DataArchitect.drawio.png](docs/DataArchitect.drawio.png)  

These diagrams illustrate the flow of data from the **Bronze layer** to **Silver** and **Gold layers**, including transformations, tables, and views.

---

## How to Run / Reproduce

1. Clone this repository to your local machine.  
2. Place the raw CSV (`online_retail.csv`) in the `/dataset` folder.  
3. Execute the SQL scripts in the following order:  
   - **Bronze Layer**: `bronze.proc_load_bronze_online_retail`  
   - **Silver Layer**: `silver.proc_load_silver_online_retail`  
   - **Gold Layer**: All views for analytics and reporting  
4. Refer to the diagrams in `/docs` to understand the data flow and architecture.  
5. Run the quality checks in `/tests` to validate the data before analysis.

---

## Example Queries

**1. Top 5 Customers by Net Revenue**
```sql
SELECT TOP 5 CustomerID, NetRevenue
FROM gold.customer_sales_report
ORDER BY NetRevenue DESC;
```

**2. Monthly Sales Trend**
```sq
SELECT SalesYear, SalesMonth, TotalRevenue
FROM gold.sales_trend_by_month
ORDER BY SalesYear DESC, SalesMonth DESC;
```

---

## License

This project is licensed under the MIT License.
You are free to use, modify, and share it with proper attribution.

---

## About Me

Hi! I’m Meenakshi Singh, an aspiring Data Analyst with a strong foundation in SQL and Excel.
I enjoy transforming raw data into meaningful insights, understanding relationships in data, and creating KPIs that help businesses make better decisions.
This project reflects my hands-on approach to data analysis and reporting.
