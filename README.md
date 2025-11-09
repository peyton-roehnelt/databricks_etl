%md
# Sample Data Pipeline: API to Azure Storage

## Overview

This notebook demonstrates a serverless data pipeline that pulls data from a sample API, organizes it into three layers (bronze, silver, gold), and stores the data in various file formats (CSV, XML, Delta, Parquet) within an Azure Blob Storage container. Additionally, it showcases loading cleaned (silver layer) data into Azure Table Storage.

## Layers

- **Bronze**: Raw data ingested from the API.
- **Silver**: Cleaned and transformed data.
- **Gold**: Aggregated data for analytics.

## Storage

- Data is stored in Azure Blob Storage using a SAS token for authentication.
- Silver layer data is also loaded into Azure Table Storage.

## Technologies Used

- Python (Databricks notebook)
- Azure Blob Storage (via `azure.storage.blob`)
- Azure Table Storage (via `azure.data.tables`)
- Pandas for data manipulation
- Requests for API calls

## Steps

1. Retrieve SAS token from Databricks secrets.
2. Connect to Azure Blob Storage.
3. Fetch sample data from a mock API.
4. Organize data into bronze, silver, and gold layers.
5. Store data in Azure Blob Storage in multiple formats.
6. Load silver layer data into Azure Table Storage.

## Author

Created by: Peyton Roehnelt  
Date: 11/8/2025

## Notes

- This notebook is intended for demonstration purposes only.
- Ensure you have the required Azure credentials and Databricks secret scope configured.
