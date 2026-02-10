# Data Warehouse & Analytics Project

Welcome to my Data Warehouse and Analytics Project! 🚀  
This repository demonstrates a complete end-to-end workflow for building a data warehouse, performing data cleansing and transformation, and generating actionable analytical insights using SQL Server. It is designed as a portfolio project to showcase practical data engineering and analytical skills.

---

## Project Objective
The goal of this project is to consolidate raw sales data into a structured data warehouse and generate business insights. The project focuses on:

- Understanding **customer behavior** and segmentation  
- Analyzing **product performance** and sales trends  
- Computing key **business metrics (KPIs)** for decision-making  

This workflow highlights best practices in data ingestion, cleaning, transformation, and reporting.

---

## Dataset
The raw sales dataset is included in the [dataset](dataset) folder:  

- `online_retail.csv` – transactional sales data containing invoices, products, customers, quantities, prices, and countries.  

This dataset is used as the source for the Bronze layer of the data warehouse.  

> ✅ *Note:* The dataset is part of this repository and can be used to run the project end-to-end.

---

## Project Architecture

### Data Flow
The project follows a **Bronze → Silver → Gold** layered data pipeline:

[![Data Flow](docs/DataFlow.drawio.png)](docs/DataFlow.drawio.png)

### Data Architecture
The high-level architecture displays all tables, views, and transformations applied at each layer:

[![Data Architecture](docs/DataArchitect.drawio.png)](docs/DataArchitect.drawio.png)

---

## Layers Overview

### Bronze Layer
- **Object Type:** Table  
- **Purpose:** Raw data ingestion from source CSV files  
- **Process:** Full load using truncate & insert. No transformations are applied to preserve source data fidelity.  

### Silver Layer
- **Object Type:** Table  
- **Purpose:** Cleaned and structured data for analytics  
- **Process:**  
  - Data type conversion  
  - Null handling and trimming of whitespace  
  - Deduplication and validation  
  - Ensures data is analytics-ready for reporting  

### Gold Layer
- **Object Type:** Views  
- **Purpose:** Business-level reporting and analytical insights  
- **Process:**  
  - Aggregate data for customers, products, and sales trends  
  - Calculate KPIs  
  - Segment customers and products  
  - Provide actionable insights for business decision-making  

---

## How to Reproduce / Run
1. Clone this repository to your local machine.  
2. Place the raw CSV (`online_retail.csv`) in the `/dataset` folder (already included).  
3. Execute the SQL scripts in the following order:  
   - Bronze Layer: `bronze.proc_load_bronze_online_retail`  
   - Silver Layer: `silver.proc_load_silver_online_retail`  
   - Gold Layer: Views for analytics and reporting  
4. Refer to the diagrams in `/docs` to understand the data flow and architecture.  

---

## License
This project is licensed under the MIT License — free to use, modify, and share with proper attribution.

---

## About Me
Hi! I’m Meenakshi Singh, an aspiring Data Analyst with a strong foundation in SQL and Excel. I enjoy transforming raw data into meaningful business insights. This project reflects my hands-on approach to learning, applying data engineering and analytical concepts to real-world sales data.
