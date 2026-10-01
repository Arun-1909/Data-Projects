# Retail Data Engineering Project – Microsoft Fabric

## Overview

This project implements an end-to-end retail data engineering pipeline using Microsoft Fabric.

The project demonstrates data ingestion, transformation, data cleaning, Gold-layer modeling, semantic modeling, and Power BI dashboard development.

## Architecture

The project follows a Medallion Architecture:

Bronze → Silver → Gold → Semantic Model → Power BI Dashboard

### Bronze Layer

Raw retail datasets are ingested into the Bronze layer.

Datasets include:

- Orders
- Inventory
- Returns

### Silver Layer

The Silver layer contains cleaned and standardized datasets.

Transformations include:

- Data type conversion
- Handling missing values
- Standardizing text values
- Cleaning product names
- Standardizing payment modes
- Standardizing delivery status
- Cleaning inventory values
- Creating derived columns

### Gold Layer

Business-ready Gold tables were created for analytics.

Main Gold tables include:

- gold_customer_kpis
- gold_daily_sales
- gold_inventory_kpis
- gold_product_kpis
- gold_retail_joined
- gold_retail_master

## Technologies Used

- Microsoft Fabric
- Fabric Lakehouse
- PySpark
- Python
- Delta Lake
- Power BI
- Semantic Models
- SQL
- GitHub

## Data Pipeline

The pipeline ingests the retail datasets and processes them through the Medallion Architecture.

Orders, inventory, and returns are processed and transformed into analytical datasets.

## Data Transformation

PySpark was used for:

- Data cleaning
- Data standardization
- Data transformation
- Joining datasets
- KPI calculation
- Gold-layer creation

## Power BI Dashboard

The final dashboard contains:

### KPI Cards

- Total Revenue
- Total Orders
- Unique Customers
- Total Returns
- Total Gross Margin
- Inventory Value

### Charts

- Monthly Revenue Trend
- Revenue by Product
- Gross Margin by Product
- Stock by Product
- Inventory Stock Status
- Returns by Refund Status
- Delivery Status

## Project Files

| File | Description |
|---|---|
| `Retail_Project_Notebook.ipynb` | PySpark notebook containing data processing and transformation code |
| `Retail_Dashboard.pbix` | Power BI dashboard |
| `Retail_Dashboard_Screenshots.pdf` | Screenshots documenting the Fabric pipeline, transformations and dashboard |

## Project Outcome

The project demonstrates an end-to-end retail analytics solution using Microsoft Fabric, from raw data ingestion to business intelligence visualization.

The solution enables analysis of:

- Sales performance
- Product performance
- Customer activity
- Inventory status
- Returns
- Refunds
- Delivery status
- Gross margin