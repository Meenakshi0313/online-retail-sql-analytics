# Data Warehouse & Analytics Project

Welcome to my Data Warehouse and Analytics Project! 🚀  
This project demonstrates a full end-to-end workflow for building a data warehouse, performing data cleansing and transformation, and generating analytical insights using SQL Server. It’s designed to showcase real-world data engineering and analytical skills for portfolio purposes.

## Project Objective
The main goal of this project is to consolidate raw sales data into a structured data warehouse and generate meaningful insights for business stakeholders. The project focuses on understanding:

- Customer behavior and segmentation  
- Product performance and sales trends  
- Aggregated business metrics (KPIs) for decision-making

## Dataset
The raw sales dataset is included in the [dataset](dataset) folder:  

- `online_retail.csv` – transactional sales data containing invoices, products, customers, quantities, prices, and countries.  

This dataset serves as the source for the Bronze layer of the data warehouse.

## Project Architecture

### Data Flow
The project follows a standard **Bronze → Silver → Gold** data pipeline:  

[![Data Flow](docs/DataFlow.drawio.png)](docs/DataFlow.drawio.png)

### Data Architecture
The high-level architecture shows tables, views, and the transformations applied at each layer:  

[![Data Architecture](docs/DataArchitect.drawio.png)](docs/DataArchitect.drawio.png)

## Layers Overview

### Bronze Layer
- **Object Type:** Table  
- **Purpose:** Raw data ingestion from source CSV files  
- **Process:** Full load with truncate & insert. No transformations are applied to preserve raw data fidelity.

### Silver Layer
- **Object Type:** Table  
- **Purpose:** Cleaned and structured data for analytics  
- **Process:** Data cleansing, type conversion, null handling, trimming of whitespace, and deduplication. Ensures data is accurate and ready for reporting.

### Gold Layer
- **Object Type:** Views  
- **Purpose:** Business-level reporting and analytical insights  
- **Process:** Aggregate data for customers, products, and sales trends. Calculates key performance indicators (KPIs), segments customers and products, and provides actionable insights for business decisions.

## How to Reproduce / Run
1. Clone this repository to your local machine.  
2. Place the raw CSV (`online_retail.csv`) in the `/dataset` folder (already included).  
3. Run the SQL scripts in order:  
   - Bronze Layer: `bronze.proc_load_bronze_online_retail`  
   - Silver Layer: `silver.proc_load_silver_online_retail`  
   - Gold Layer: Views for analytics and reporting  
4. Use the diagrams in `/docs` to understand data flow and architecture.

## License
This project is licensed under the MIT License — free to use, modify, and share with proper attribution.

## About Me
Hi! I’m Meena
