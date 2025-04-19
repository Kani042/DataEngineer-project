# Azure End-to-End Data Engineering Pipeline - Adventure Works Sales Project

This project demonstrates a complete end-to-end data engineering pipeline built using Microsoft Azure. 
The solution ingests raw CSV data from GitHub, transforms it using Databricks, models it in Synapse, and visualizes it through Power BI.

- Azure Data Factory
- Azure Data Lake Storage Gen2
- Azure Databricks (PySpark)
- Azure Synapse Analytics
- Power BI
- GitHub
### 1. Data Ingestion
- CSV files are stored in GitHub.
- A JSON configuration file lists all the CSV file names.
- Azure Data Factory (ADF) is used to:
  - Use **Lookup** to read the JSON file.
  - **ForEach** activity to iterate over file names.
  - **Copy Activity** to load each file dynamically from GitHub to Data Lake Gen2.

### 2. Data Transformation
- Azure Databricks notebooks are used for transformation (e.g., cleaning, joining, formatting).
- Transformed data is written back to a curated zone in Data Lake Gen2.

### 3. Data Modeling
- Views are created in Azure Synapse Analytics from the curated data in Data Lake.
- External tables are defined on top of the views using Synapse SQL Serverless.

### 4. Data Visualization
- Power BI is connected to Synapse SQL for reporting and dashboard creation.

