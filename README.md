# Cloud-Based E-Commerce Data Pipeline

## Project Overview

An end-to-end cloud-based e-commerce data engineering pipeline built on Microsoft Azure to ingest, process, clean, validate, and transform e-commerce data into analytics-ready datasets.

The project uses Azure Data Factory for orchestration, ADLS Gen2 for cloud storage, Azure Databricks with PySpark and Delta Lake for data processing, and Power BI for business analytics.

## Business Problem

E-commerce systems generate large volumes of data from multiple sources. Raw data may contain missing values, duplicate records, invalid values, and inconsistent formats.

The objective of this project is to build a reliable data pipeline that:

- Ingests raw e-commerce data
- Stores data in a scalable cloud data lake
- Performs data cleaning and transformation
- Identifies and quarantines invalid records
- Creates analytics-ready datasets
- Supports incremental data processing
- Provides business insights through Power BI

## Architecture
```
E-Commerce CSV Files
        |
        v
Azure Data Factory
(Ingestion & Orchestration)
        |
        v
Azure Data Lake Storage Gen2
        |
        v
Azure Databricks
(PySpark + Delta Lake)
        |
   +----+----+
   |         |
   v         v
Bronze    Data Quality
   |       & Quarantine
   v
Silver
   |
   v
Gold
   |
   v
Power BI
(Analytics Dashboard)
```
## Technology Stack

- Azure Data Factory
- Azure Data Lake Storage Gen2
- Azure Databricks
- PySpark
- SQL
- Delta Lake
- Power BI
- Git & GitHub

## Key Features

- End-to-end Azure data pipeline
- Bronze-Silver-Gold Medallion Architecture
- Data quality validation
- Duplicate and null-value handling
- Invalid-record quarantine
- Incremental data processing
- Azure Data Factory orchestration
- Delta Lake processing
- Power BI analytics dashboard

## Data Sources

The pipeline processes:

- Customers
- Products
- Orders
- Order Items
- Payments

## Data Processing

### Bronze Layer

Stores ingested raw data in Delta format.

### Silver Layer

Cleans and validates the data using PySpark, including null checks, duplicate detection, invalid values, and business rules.

### Quarantine

Invalid records are separated into quarantine tables for further investigation.

### Gold Layer

Creates analytics-ready datasets such as:

- Daily Sales
- Customer Sales
- Product Sales
- Category Sales
- Sales Summary

## Incremental Processing

An incremental processing demonstration was implemented using a watermark/timestamp approach to identify and process newly arriving records without reprocessing the complete dataset.
```
Detect New Data
        ↓
Apply Watermark
        ↓
Process New Records
        ↓
Update Target Tables
```
## Pipeline Orchestration

Azure Data Factory orchestrates the Databricks processing workflow:
```
Bronze Ingestion
        ↓
Silver Transformation
        ↓
Gold Analytics
```
## Power BI Dashboard

The final Gold datasets are used to build a Power BI dashboard containing:

- Total Sales
- Total Orders
- Total Quantity
- Daily Sales Trend
- Sales by Category
- Top Products
- Top Customers
- Category Distribution

## Project Outcome

The project demonstrates an end-to-end Azure data engineering workflow from raw e-commerce data ingestion to cleaned, transformed, and analytics-ready data, with data-quality handling, incremental processing, orchestration, and business intelligence.

## Skills Demonstrated

Data Engineering: ETL/ELT, data pipelines, data quality, incremental processing

Big Data: PySpark, Apache Spark, Delta Lake

Azure: Azure Data Factory, ADLS Gen2, Azure Databricks

Analytics: SQL, Power BI

## Author

Om Kharwade

Aspiring Data Engineer

