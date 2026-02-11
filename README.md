## Online Retail SQL Analytics 🚀


## Project Overview

This project presents an end-to-end SQL analytics solution for an online retail dataset using SQL Server. It demonstrates how raw transactional data can be transformed into analytics-ready datasets using a structured Medallion (Bronze–Silver–Gold) architecture.

The project focuses on building business-focused analytical views that support customer analysis, product performance evaluation, revenue tracking, and sales trend analysis. These views are designed to act as a semantic layer for downstream reporting and BI tools such as Power BI.


## Business Objectives

The primary objective of this project is to derive actionable business insights from online retail sales data by answering questions such as:

Who are the highest-value and most loyal customers?

How is revenue distributed across customers and products?

What impact do product returns have on net revenue?

Which products and countries contribute the most to sales?

How do sales trends change over time?


## Dataset

The dataset used in this project is provided in the /dataset folder as a CSV file:

- **online_retail.csv** — transactional sales data from an online retail store

The data includes invoices, products, customers, quantities, pricing, dates, and country-level information.


## Data Architecture

This project follows the Medallion Architecture pattern:

**Bronze Layer**
Raw data ingestion from CSV files without transformations.

**Silver Layer**
Cleaned and standardized transactional data with:

- Data type corrections
- Null handling
- Removal of invalid records
- Explicit handling of sales and returns

**Gold Layer**
Curated, analytics-ready views optimized for reporting, KPI tracking, and BI consumption.

Architecture and data flow diagrams are available in the /docs folder.


## Gold Layer – Analytical Views

The Gold layer serves as a semantic layer and contains the following views:


## Customer Analytics

- **customer_sales_report**  
  Provides customer-level KPIs including total orders, gross revenue, return revenue, net revenue, average order value (AOV), purchase lifecycle metrics, and customer segmentation.

- **customer_segment_report**  
  Summarizes the number and percentage of customers across defined customer segments.

- **sales_by_customer**  
  Breaks down total orders, quantity, and revenue by customer to analyze revenue concentration.

## Product Analytics

- **product_sales_report**  
  Aggregates product-level metrics including quantity sold and returned, gross and net revenue, average revenue per order, and product performance segmentation.

- **product_segment_report**  
  Analyzes product distribution and revenue contribution across performance segments.

- **top_selling_products**  
  Identifies top-performing products by quantity sold and revenue.


## Sales & Trend Analytics

- **sales_by_country**  
  Evaluates sales performance across different countries.

- **sales_trend_by_month**  
  Aggregates sales by year and month to identify seasonality and revenue trends.



## Key Business Insights (Example)

- A small percentage of customers contribute a significant share of total revenue.
- High-value loyal customers generate higher lifetime revenue than new customers.
- Certain products show high return rates, impacting net profitability.
- Sales exhibit clear monthly patterns.
- Revenue contribution varies significantly across countries.


## Key KPIs Defined

- Total Revenue
- Net Revenue (after returns)
- Average Order Value (AOV)
- Customer Lifetime Revenue
- Customer Active Days
- Product Net Revenue
- Monthly Revenue Trends

All KPIs are calculated using cleaned Silver-layer data to ensure accuracy and consistency.


## How to Run / Reproduce

- Clone this repository to your local machine
- Place online_retail.csv in the /dataset folder
- Execute SQL scripts in the following order:
- Bronze layer stored procedures
- Silver layer data cleaning procedures
- Gold layer view creation scripts
- Validate the data using the quality checks in the /tests folder
- Query the Gold views directly or connect them to a BI tool for visualization

## Technologies & Skills Used

- SQL Server (T-SQL)
- Data Cleaning & Transformation
- CTEs and Aggregations
- Business KPI Modeling
- Customer & Product Segmentation
- Medallion (Bronze–Silver–Gold) Architecture
- Analytics View Design
- BI-ready Semantic Layer Design


## License

This project is licensed under the MIT License. You are free to use, modify, and distribute this project with proper attribution.

## About Me

Hi, I’m Meenakshi Singh, a Data Analyst with hands-on experience in SQL-based data analysis, KPI modeling, and analytical reporting. I enjoy transforming raw transactional data into structured, meaningful insights that support business decision-making. This project reflects my practical approach to building scalable and analytics-ready SQL solutions.
