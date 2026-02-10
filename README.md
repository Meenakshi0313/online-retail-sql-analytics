Retail Analytics – Medallion Architecture Project

Welcome to the Retail Analytics Data Warehouse Project repository! 🚀
This project demonstrates a complete analytics workflow using SQL Server and the Medallion Architecture (Bronze, Silver, Gold) to transform raw retail data into business-ready insights.
It is designed as a portfolio project showcasing practical data analytics and data modeling skills.

🚀 Project Objective
Data Engineering

Build a structured analytics pipeline that ingests raw retail transaction data, cleans and standardizes it, and produces business-level analytical outputs.

Analytics & Reporting

Develop SQL-based analytical views to provide insights into:

Customer behavior

Product performance

Sales and revenue trends

🏗️ Architecture Overview

This project follows the Medallion Architecture pattern:

Bronze Layer: Raw data ingestion from CSV files (no transformations)

Silver Layer: Data cleansing, validation, type conversions, and deduplication

Gold Layer: Business-level aggregates, KPIs, and analytical views

The architecture ensures data quality improves at each stage while keeping transformations transparent and traceable.

🧩 Data Layers Summary
🥉 Bronze Layer

Object Type: Tables

Load Strategy: Full load (Truncate & Bulk Insert)

Purpose: Store raw source data exactly as received, preserving source fidelity

🥈 Silver Layer

Object Type: Tables

Transformations:

Data type conversions

NULL and invalid value handling

Text trimming and standardization

Deduplication

Purpose: Provide clean, analytics-ready data

🥇 Gold Layer

Object Type: Views

Purpose: Business-level aggregations and KPIs

Focus Areas:

Customer analytics

Product analytics

Sales and trend analysis

📊 Analytics Use Cases

The Gold layer supports:

BI dashboards (Power BI / Tableau)

Ad-hoc SQL analysis

Business reporting for stakeholders

🛠️ Tech Stack

SQL Server

SQL (T-SQL)

Medallion Architecture

CSV-based batch ingestion

 📂 Dataset
The dataset used in this project is a public online retail transactions dataset.
It is stored in the `data/` folder and serves as the source for building the Bronze, Silver, and Gold layers of the analytics pipeline.


🛡️ License

This project is licensed under the MIT License. You are free to use, modify, and share it with proper attribution.

🌟 About Me

Hi! I’m Meenakshi Singh, an aspiring Data Analyst with a strong foundation in SQL and Excel and a growing interest in data analytics.
I enjoy working with structured data, applying data quality rules, and transforming raw transactional data into meaningful business insights.
This project reflects my hands-on learning approach and my understanding of real-world analytics workflows.


