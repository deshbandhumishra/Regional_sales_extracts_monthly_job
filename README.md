# Regional Sales Reporting Pipeline

This project provides an automated monthly **Regional Sales Reporting Pipeline** built on **Databricks Serverless (Free Edition)**. It extracts transactional sales data, applies business filters, aggregates monthly metrics, generates a CSV report, stores it in DBFS, and emails the output using SendGrid.

## Features
- Automated monthly extraction of sales & return data  
- Filters based on country, region, product, and date range  
- Default date handling (uses previous full month)  
- Aggregated monthly metrics (quantity & revenue)  
- CSV generation and volume storage  
- Automatic email delivery via SendGrid  
- Fully parameterized pipeline  

## Tech Stack
- Databricks Serverless (Free Tier)
- PySpark / SQL
- SendGrid API
- Databricks Workflows
- DBFS Volumes

## Key Files
- Notebook: **Sales_Extract**
- Pipeline YAML: **wf_regional_sales_extract**
- Output: **Monthly aggregated sales CSV**

## How to Run
1. Import notebook into Databricks Workspace  
2. Configure pipeline parameters (dates, region, product)  
3. Run workflow manually or via scheduled monthly trigger  
4. Check Volume output and email delivery  

## Requirements
- SendGrid API key  
- Access to UC table: `uc_sp.sales_reporting.regional_sales_data`  
- Databricks Free Serverless environment  

## Output
- CSV file with monthly metrics  
- Automated email with attachment  

