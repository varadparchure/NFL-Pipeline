# NFL Data Pipeline with Azure and Databricks
## Project Overview<br>
This project involves creating an ELT (Extract, Load, Transform) pipeline using NFL data sourced from Kaggle. The pipeline processes data from raw CSV files to transformed datasets ready for further analysis or reporting. The focus of this project is solely on pipeline creation, leveraging Azure and Databricks for data management and transformation.

## Goal for this project
The goal of this project was to build a robust data pipeline that ingests raw data from CSV files, stores it as raw data in Azure Data Lake Gen2, and then utilizes Azure Databricks for transformations. While the transformations in this project were limited in scope, they were implemented using PySpark to demonstrate scalable data processing capabilities. The transformed data was then stored back into Azure Data Lake Gen2 and subsequently ingested into Azure Synapse Analytics, making it readily available for further analysis or reporting. The primary focus of this project was on the pipeline creation process rather than performing an in-depth analysis of the data. However, extending this project to include detailed analysis and visualization will be the next step and will be added in a new repo.

## Data Source
Dataset: NFL Data from Kaggle<br>
Files Provided: 19 CSV files containing various data categories such as basic stats, passing stats, defensive stats, and more.

<img width="894" alt="Screenshot 2025-01-13 at 12 54 52 PM" src="https://github.com/user-attachments/assets/cba2ccb7-5612-4c38-aa56-9b516f1dff27" />

kaggle Dataset link: https://www.kaggle.com/datasets/kendallgillies/nflstatistics?resource=download
<br>Data Scraped from NFL website: https://github.com/kendallgillies/NFL-Statistics-Scrape


## Pipeline Workflow<br>
1. Data Injection<br>
The raw data (CSV files) is ingested into the pipeline using Azure Data Factory.<br>
2. Data Storage<br>
The ingested data is stored as raw data in Azure Data Lake Gen2.<br>

<img width="920" alt="Screenshot 2025-01-13 at 12 41 02 PM" src="https://github.com/user-attachments/assets/c4ddc9dd-93b0-4a9c-9659-ab279d316616" />

</br>
4. Data Transformation<br>
Data is pulled into Azure Databricks for processing.
Using Apache Spark, basic transformations are applied to clean and standardize the data.<br><br>
5. Transformed Data Storage<br>
The transformed data is stored back into Azure Data Lake Gen2.<br><br>
6. Data Integration<br>
The processed data is ingested into Azure Synapse Analytics, creating structured tables that can be queried for analysis or used in BI tools.<br><br>
7. Optional Visualization (Out of Scope for This Project)<br>
Although visualization (e.g., using Tableau, Power BI, or Looker) is not within the scope of this project, the structured tables in Azure Synapse can be integrated with these tools for reporting in future projects.<br><br>

## Tech:<br>
Azure Data Factory: For data ingestion and pipeline orchestration.<br>
Azure Data Lake Gen2: To store raw and transformed data.<br>
Azure Databricks: For scalable data transformations using Apache Spark.<br>
Azure Synapse Analytics: For structured data storage and integration.<br>
PySpark: For scripting and transformations within Databricks.
