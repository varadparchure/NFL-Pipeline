# NFL-Pipeline


# NFL Data Pipeline with Azure and Databricks
Project Overview
This project involves creating an ELT (Extract, Load, Transform) pipeline using NFL data sourced from Kaggle. The pipeline processes data from raw CSV files to transformed datasets ready for further analysis or reporting. The focus of this project is solely on pipeline creation, leveraging Azure and Databricks for data management and transformation.

## Data Source
Dataset: NFL Data from Kaggle
Files Provided: 19 CSV files containing various data categories such as basic stats, passing stats, defensive stats, and more.

kaggle Dataset link: https://www.kaggle.com/datasets/kendallgillies/nflstatistics?resource=download
Data Scraped from NFL website: https://github.com/kendallgillies/NFL-Statistics-Scrape

## Pipeline Workflow
1. Data Injection
The raw data (CSV files) is ingested into the pipeline using Azure Data Factory.
2. Data Storage
The ingested data is stored as raw data in Azure Data Lake Gen2.

<img width="1469" alt="Screenshot 2025-01-12 at 11 06 15 PM" src="https://github.com/user-attachments/assets/427f7f6f-fd2f-470d-8a7f-690ee8734528" />

4. Data Transformation
Data is pulled into Azure Databricks for processing.
Using Apache Spark, basic transformations are applied to clean and standardize the data.
5. Transformed Data Storage
The transformed data is stored back into Azure Data Lake Gen2.
6. Data Integration
The processed data is ingested into Azure Synapse Analytics, creating structured tables that can be queried for analysis or used in BI tools.
7. Optional Visualization (Out of Scope for This Project)
Although visualization (e.g., using Tableau, Power BI, or Looker) is not within the scope of this project, the structured tables in Azure Synapse can be integrated with these tools for reporting in future projects.

## Key Technologies Used
Azure Data Factory: For data ingestion and pipeline orchestration.
Azure Data Lake Gen2: To store raw and transformed data.
Azure Databricks: For scalable data transformations using Apache Spark.
Azure Synapse Analytics: For structured data storage and integration.
Python: For scripting and transformations within Databricks.
