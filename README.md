# Real Time ECommerce Data Processing & Analytics using Medallion Architecture on Azure Cloud

## Project Structure
ECommerce-Data-Processing-and-Analytics-using-Medallion-architecture-on-Azure-Cloud/
│
├── README.md                          # Project documentation
├── 1719345910378.gif                  # Medallion architecture animation
│
├── data/                              # Source data files
│   ├── customers.csv
│   ├── products.csv
│   ├── orders.csv
│   └── ...
│
├── adf-pipelines/                     # Azure Data Factory pipeline configs
│   ├── pipeline_ingest_http.json      # HTTP source ingestion pipeline
│   └── pipeline_ingest_sql.json       # SQL source ingestion pipeline
│
├── databricks-notebooks/              # Azure Databricks notebooks
│   ├── 01_bronze_ingestion.py         # Bronze layer — raw data landing
│   ├── 02_silver_transformation.py    # Silver layer — cleaning & curation
│   ├── 03_gold_aggregation.py         # Gold layer — business-ready datasets
│   └── 04_mongodb_enrichment.py       # MongoDB enrichment merge
│
├── synapse/                           # Azure Synapse SQL scripts
│   └── gold_layer_views.sql           # Serverless SQL views on Gold data
│
├── powerbi/                           # Power BI report files
│   └── ecommerce_dashboard.pbix       # Interactive dashboard
│
└── screenshots/                       # Architecture & dashboard screenshots
    └── ...

## Project overview
This project follows a modern **Medallion Architecture (Bronze → Silver → Gold)** built on Azure cloud to enable scalable, real-time e-commerce data processing and analytics.

🔹 **Data Ingestion (Bronze Layer)**
Multiple data sources (GitHub HTTP endpoints and SQL tables) are ingested using Azure Data Factory and stored as raw files in Azure Data Lake Storage Gen2.

🔹 **Data Transformation (Silver Layer)**
Raw data is cleaned, modeled, and enriched in Azure Databricks using PySpark.
Additional enrichment tables are fetched from MongoDB and merged with processed datasets.

🔹 **Data Storage & Serving (Gold Layer)**
The transformed and curated Gold datasets are stored back into ADLS Gen2, optimized in Parquet format for analytics workloads.

🔹 **Analytics & Visualization**
Azure Synapse Serverless SQL reads directly from ADLS to enable fast querying without needing provisioning. Finally, Power BI is used to build interactive dashboards for revenue analysis, customer insights, and operational KPIs.

<img width="1219" height="693" alt="image" src="https://github.com/user-attachments/assets/2b3540df-6098-42b0-8d68-65d9795aaf54" />

## Medallion Architecture
The Medallion Architecture is a multi-layered data design used in modern data engineering to organize data as it flows from raw ingestion to refined, business-ready datasets. It improves data quality, reliability, and scalability across analytics platforms such as Databricks and Azure.

🥉 **Bronze Layer – Raw Data (Landing Zone)**

- Stores raw, unprocessed data exactly as received from various sources (APIs, databases, streams).
- Schema is not enforced — data is stored in its original form.
- Purpose: Ingest quickly, keep full data fidelity, enable replay if needed.
👉 Think of it as a digital warehouse where all incoming items are dropped off without sorting.

🥈 **Silver Layer – Cleaned & Curated Data**

- Data is cleaned, filtered, deduplicated, and the schema is standardized.
- Ensures data is quality-checked and consistent.
- Combines data from multiple Bronze tables if needed.
👉 Like a processing center where items are inspected, cleaned, and organized into proper categories.

🥇 **Gold Layer – Business-Level, Analytics-Ready Data**

- Data is modeled for analytics, often aggregated by business needs.
- Used for dashboards, ML models, KPIs, and reporting.
- Optimized for fast queries and consumption by tools like Power BI.
👉 This is the final store display — polished, arranged, and ready for customers (business users).

🔍 **Why to use Medallion Architecture?**

- Ensures clean, reliable, and traceable data.
- Enables scalable ETL pipelines.
- Supports multiple consumers (BI, ML, reports).
- Simplifies debugging — each step is separated and transparent.

![Alt text](https://github.com/SIDDHARTH107/Real-Time-E-Commerce-Data-Processing-and-Analytics-using-Medallion-architecture-on-Azure-Cloud/blob/main/1719345910378.gif?raw=true)

<img width="1355" height="727" alt="image" src="https://github.com/user-attachments/assets/73f99e14-da68-4a71-8c3c-6c1d78c74c90" />

## 🚀 Tech Stack
- **Data Ingestion**: Azure Data Factory
- **Storage**: Azure Data Lake Storage Gen2
- **Transformation**: Azure Databricks (PySpark)
- **Analytics**: Azure Synapse Analytics
- **Visualization**: Microsoft Power BI
- **Databases**: PostgreSQL, MongoDB Atlas, MongoDB Compass
- **Languages**: Python, SQL
- **Spreadsheet**: Microsoft Excel, Google Sheets
- **IDE (Integrated Development Environment**: Windsurf

## 📊 Key Features
- Automated data ingestion from HTTP and SQL/NoSQL sources
- Medallion architecture implementation
- Real-time data processing with PySpark
- Interactive Power BI dashboard
- Serverless SQL querying
  
## POWER BI DASHBOARD
<img width="838" height="476" alt="image" src="https://github.com/user-attachments/assets/2f662506-ff05-4e9b-8c56-1c534773122c" />

## Business Insights from Gold Layer table
<img width="859" height="326" alt="image" src="https://github.com/user-attachments/assets/ff9e7819-252b-4e44-af79-c72199816df8" />

## 🔗 Connect
- 💼 [LinkedIn](https://www.linkedin.com/in/siddharthmohapatra-dataanalyst/)
- 🐦 [Twitter](https://x.com/SidDS2000)
- 📧 [Email](siddharth.m33@gmail.com)
