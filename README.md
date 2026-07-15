# NHA-4-82
# SalesPulse360: Real-Time Sales Data Engineering Pipeline

## Project Overview
**SalesPulse360** is a sophisticated hybrid data engineering pipeline designed to bridge the gap between traditional batch ETL and real-time streaming analytics. By utilizing a Medallion Architecture, this project provides a scalable, reliable, and business-ready data environment that ensures Business Intelligence (BI) dashboards are always fed with timely data.

The project processes the Olist e-commerce dataset (historical batch) alongside simulated real-time payment transactions.

## Architecture & Data Flow
The project leverages the **Medallion Architecture** to structure the Data Lakehouse:

1. **Bronze Layer (Raw):** Stores raw Olist CSV datasets and incoming real-time payment streams from Azure Event Hub as Delta tables without transformation[cite: 6, 7].
2. **Silver Layer (Cleaned):** Performs data cleansing (null handling, deduplication), standardization, and joins historical sales data with streaming payment updates[cite: 5, 7].
3. **Gold Layer (Business-Ready):** A curated Data Warehouse (Galaxy Schema) optimized for fast analytics, serving 9 business-ready tables to Power BI[cite: 4, 7].

## Technology Stack
* **Cloud & Processing:** Azure Databricks, PySpark, Spark Structured Streaming.
* **Data Streaming:** Azure Event Hub[cite: 2, 7].
* **Storage:** Delta Lake[cite: 7].
* **Data Modeling:** Galaxy Schema (Fact/Dimension Tables)[cite: 1, 7].
* **Visualization:** Power BI[cite: 7].

## Repository Structure
* `/etl_pipeline`: Contains the PySpark notebooks for Bronze, Silver, and Gold layers[cite: 7].
* `/streaming`: Includes the Python producer/consumer scripts for real-time Event Hub ingestion[cite: 2, 3, 7].
* `/docs`: Project documentation and the Galaxy Schema Entity-Relationship Diagram (ERD)[cite: 1, 7].
* `/dashboard`: The Power BI report file used for business insights[cite: 7].

## Key Insights
The project addresses critical business questions, including:
- **Revenue & Order Behavior:** Tracking daily trends and performance[cite: 7].
- **Product Performance:** Identifying high-revenue categories and volume metrics[cite: 7].
- **Logistics Efficiency:** Measuring on-time vs. late delivery rates and average delays[cite: 7].
- **Customer Behavior:** Insights into payment methods and regional buying patterns[cite: 7].

## Team
- **Project Team:** Nada Ashraf, Hana Samy, Khaled Korayem[cite: 7].
- **Supervisor:** Eng. Mohamed Hammed[cite: 7].

