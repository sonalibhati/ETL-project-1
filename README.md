# Finance Data Engineering ETL Pipeline

## Project Overview
This project demonstrates an end-to-end ETL pipeline built using Databricks, PySpark, SQL, and Delta Lake. It processes 500 rows of synthetic finance transaction data, performs data cleaning and validation, and generates business-ready summary tables.

## Business Objective
The objective is to transform raw financial transaction data into clean, reliable, and analysis-ready data for financial reporting.

## Technology Stack
- **Databricks** — Data processing environment
- **PySpark** — Data cleaning and transformation
- **SQL** — Data querying and aggregation
- **Delta Lake** — Storage of processed data
- **GitHub** — Version control and project documentation

## Dataset
The project uses a synthetic finance dataset containing 500 transaction records.

Key columns include:
- Transaction ID
- Transaction Date
- Department
- Transaction Type
- Vendor/Customer
- Amount
- Currency
- Payment Method
- Cost Center
- Transaction Status
- Invoice Number

The dataset contains sample data-quality issues such as missing values, duplicate records, inconsistent text formatting, and invalid dates.

## Pipeline Architecture

### 1. Raw Data
Load the finance transaction CSV file into Databricks.

### 2. Silver Layer
Clean and transform the data by:
- Standardizing text fields
- Converting data types
- Handling invalid dates
- Identifying missing values
- Detecting duplicate records
- Adding data-quality flags

### 3. Gold Layer
Create a business summary grouped by department and currency, including:
- Total transaction count
- Total transaction amount

Amounts are grouped by currency to avoid incorrectly combining different currencies.

## Output Tables
- `finance_transactions_silver` — Cleaned finance transaction data
- `finance_transactions_gold` — Department-wise financial summary

## Key Learning Outcomes
- Building an ETL data pipeline
- Using PySpark DataFrames for transformations
- Applying SQL for data analysis
- Working with Delta tables
- Implementing basic data-quality checks
- Organizing and documenting a data engineering project

## Future Enhancements
- Automate pipeline execution
- Add incremental data processing
- Implement logging and error handling
- Add unit tests and data-quality assertions
- Process larger datasets and measure performance

## Disclaimer
This project uses synthetic data for educational and portfolio purposes. It does not contain actual company financial records.
