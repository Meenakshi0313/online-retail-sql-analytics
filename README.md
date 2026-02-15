# 🛒 Online Retail SQL Analytics

## 🚀 Project Overview

This project presents an end-to-end SQL analytics solution for an online retail dataset using SQL Server. It demonstrates how raw transactional data can be transformed into analytics-ready datasets using a structured **Medallion (Bronze → Silver → Gold) architecture**.

The solution implements a **Star Schema data model** in the Gold layer to support scalable analytics, business reporting, and BI tools such as Power BI.

The project focuses on building business-focused datasets that enable:

* Customer behavior analysis
* Product performance evaluation
* Revenue tracking
* Sales trend analysis
* KPI reporting

---

## 🎯 Business Objectives

The primary objective is to derive actionable business insights from online retail sales data by answering questions such as:

* Who are the highest-value and most loyal customers?
* How is revenue distributed across customers and products?
* What impact do product returns have on net revenue?
* Which products and countries contribute the most to sales?
* How do sales trends change over time?

---

## 📂 Dataset

The dataset used in this project is provided in the `/dataset` folder:

* **online_retail.csv** — transactional sales data from an online retail store

The data includes:

* Invoices
* Products
* Customers
* Quantities
* Pricing
* Dates
* Countries

---

## 🏗️ Data Architecture

This project follows the **Medallion Architecture** pattern:

### 🥉 Bronze Layer — Raw Data

* Raw ingestion from CSV files
* No transformations applied
* Preserves original source structure

### 🥈 Silver Layer — Cleaned Data

Data cleaning and standardization:

* Data type corrections
* Null handling
* Removal of invalid records
* Handling of sales and returns
* Standardized schema for analytics

### 🥇 Gold Layer — Star Schema (Analytics Ready)

The Gold layer contains a **Star Schema** optimized for reporting and BI tools.

#### Dimension Tables (Views)

* **gold.dim_customers**
  Customer attributes, lifecycle metrics, revenue, and segmentation.

* **gold.dim_products**
  Product attributes, revenue performance, and segmentation.

#### Fact Table (View)

* **gold.fact_sales**
  Transaction-level sales metrics including quantity, pricing, gross revenue, returns, and net revenue.

This structure enables scalable analytics and efficient reporting.

---

## 📊 Architecture & Data Flow Diagrams

Project diagrams are available in the `/docs` folder:

* **Data Architecture Diagram**
* **Data Flow Diagram**

These diagrams illustrate the movement of data across Bronze, Silver, and Gold layers.

---

## 📈 Key KPIs Defined

* Total Revenue
* Net Revenue (after returns)
* Average Order Value (AOV)
* Customer Lifetime Revenue
* Customer Active Days
* Product Net Revenue
* Monthly Revenue Trends

All KPIs are calculated using cleaned Silver-layer data to ensure accuracy and consistency.

---

## 🔍 Example Business Insights

* A small percentage of customers contribute a large share of total revenue.
* High-value loyal customers generate significantly higher lifetime value.
* Certain products show high return rates impacting profitability.
* Sales exhibit monthly seasonality patterns.
* Revenue contribution varies significantly across countries.

---

## ⚙️ How to Run / Reproduce

1. Clone this repository
2. Place `online_retail.csv` inside the `/dataset` folder
3. Execute SQL scripts in the following order:

```
1️⃣ Bronze Layer
2️⃣ Silver Layer
3️⃣ Gold Layer
```

4. Validate data using scripts in the `/tests` folder
5. Query Gold views directly or connect to a BI tool (e.g., Power BI)

---

## 🛠️ Technologies & Skills Used

* SQL Server (T-SQL)
* Data Cleaning & Transformation
* CTEs and Aggregations
* Star Schema Modeling
* Fact & Dimension Design
* Business KPI Modeling
* Customer & Product Segmentation
* Medallion Architecture
* BI-ready Semantic Layer Design

---

## 📜 License

This project is licensed under the MIT License.

---

## 👩‍💻 About Me

Hi, I’m **Meenakshi Singh**, a Data Analyst with hands-on experience in SQL-based data analysis, KPI modeling, and analytical reporting.

I enjoy transforming raw transactional data into structured, meaningful insights that support business decision-making. This project reflects my practical approach to building scalable and analytics-ready SQL solutions.

