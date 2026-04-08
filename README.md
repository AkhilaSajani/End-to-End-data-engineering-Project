End-to-End Data Engineering Pipeline on Azure

This project demonstrates the implementation of a complete data engineering workflow using Azure services. 
The pipeline ingests, processes, and prepares data for analytics and reporting using the AdventureWorks dataset sourced from GitHub.

🔹 Environment Setup

The solution is built using the following Azure services:

Azure Data Factory for orchestrating data movement
Azure Storage Account as a centralized data lake (bronze, silver, gold layers)
Databricks for data processing and transformation

All resources were configured with appropriate access controls to enable secure and seamless integration.

🔹 Data Ingestion (ADF Pipeline)

Azure Data Factory is used to manage and automate data ingestion workflows.

Data is extracted from GitHub using an HTTP connector
Ingestion pipelines are designed to support dynamic inputs through parameterization
Raw data is stored in the bronze layer within Azure Storage

This setup enables scalable and reusable ingestion across multiple datasets.

🔹 Data Transformation (Databricks)

Data processing is handled using Databricks notebooks.

A compute cluster is configured for distributed processing
Raw data from the bronze layer is accessed directly from the data lake

Transformations performed include:

Standardizing date formats
Filtering invalid or incomplete records
Aggregating and reshaping datasets for analysis

Processed data is written to the silver layer in Parquet format to improve performance and storage efficiency.

🔹 Data Serving Layer

The transformed data is organized into a gold layer within Azure Storage.

Curated datasets are prepared for downstream consumption
Data is structured to support reporting and analytics use cases
Optimized storage formats are used for efficient querying
🔹 Reporting and Visualization

The curated datasets are integrated with Power BI for reporting.

Power BI connects directly to the processed data
Dashboards are created to visualize trends and key metrics
Reports are designed to support data-driven decision making
