# End-to-End Data Engineering Project | Databricks Medallion Architecture
# 
This repository contains an end-to-end data engineering project built using Databricks Free Edition and Apache Spark, implementing the Medallion Architecture (Bronze → Silver → Gold).

The pipeline transforms raw transactional sales data into analytics-ready datasets for business reporting and insights

## 🏗️ Architecture (Medallion Pattern)


## 🏗️ Data Warehouse Layers

🟤 Bronze Layer
Stores raw sales, customer, and product data as-is from source CSV files in Databricks.

⚪ Silver Layer
Cleansed, deduplicated, and standardized data using PySpark, including handling historical changes in dimensions with SCD Type 2 for Customer and Product tables.

🟡 Gold Layer
Business-ready data modeled into a star schema with dimension and fact tables optimized for analytical queries.

### 📖 Project Overview
This project involves:

Data Architecture: Modern data warehouse in Databricks using the Medallion Architecture — Bronze, Silver, Gold.

ETL Pipelines: Idempotent, incremental pipelines built with PySpark and Databricks Jobs to load, transform, and historize data.

Data Modeling: Implemented fact and dimension tables with SCD Type 2 for Customer & Product dimensions, plus Date dimension.

Analytics & Reporting: SQL and PySpark-based reporting for insights on customer behavior, product performance, and sales trends.

### Project Requirements

Building the Data Warehouse (Data Engineering)

Objective: Consolidate sales data from CSVs into a Delta Lake warehouse, tracking historical changes in dimensions.

Data Sources: Sales Data in csv format.

Data Quality: Deduplication, cleansing, and historization using PySpark.

Integration: Join Customer, Product, and Date dimensions to the fact table for accurate historical reporting.

Scope: Full and incremental loads with idempotent pipelines.

Documentation: Clear documentation of tables, keys, and SCD2 logic for stakeholders.

### BI: Analytics & Reporting (Data Analysis)

Objective: Deliver insights into:

Customer Behavior — track historical changes in customer attributes.

Product Performance — analyze sales over time.

Sales Trends — aggregate using the Date dimension.

Impact: Supports data-driven decision-making using both current and historical data.

