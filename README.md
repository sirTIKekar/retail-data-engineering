# End-to-End Retail Data Engineering Pipeline

## Overview

This project demonstrates a complete end-to-end data engineering pipeline built using Python and Pandas.

The pipeline processes raw retail sales data through structured layers:

Raw → Cleaned → Validated → Curated → Star Schema Warehouse → Business Analysis

The objective of this project is to showcase data ingestion, transformation, validation, feature engineering, and dimensional modeling skills using a reproducible and production-style workflow.

---

## Architecture

Raw Data  
   ↓  
Data Cleaning  
   ↓  
Data Validation  
   ↓  
Feature Engineering  
   ↓  
Star Schema Modeling  
   ↓  
Business Analysis  

---

## Project Structure

retail-data-engineering/

│  
├── data/  
│   ├── raw/  
│   ├── cleaned/  
│   └── curated/  
│  
├── notebooks/  
│   ├── 01_data_ingestion.ipynb  
│   ├── 02_data_cleaning.ipynb  
│   ├── 03_data_validation.ipynb  
│   ├── 04_feature_engineering.ipynb  
│   ├── 05_data_modeling_star_schema.ipynb  
│   └── 06_business_analysis.ipynb  
│  
├── warehouse/  
│   ├── dim_customer.csv  
│   ├── dim_product.csv  
│   ├── dim_location.csv  
│   ├── dim_date.csv  
│   └── fact_sales.csv  
│  
├── requirements.txt  
└── README.md  

---

## Pipeline Stages

### 1. Data Ingestion
- Load raw CSV dataset
- Store it in the data/raw layer
- Establish base structure for pipeline

### 2. Data Cleaning
- Remove duplicates
- Standardize column names
- Convert date formats
- Handle missing values
- Normalize schema

### 3. Data Validation
- Null value checks
- Data type enforcement
- Negative value detection
- Schema validation
- Basic data quality checks

### 4. Feature Engineering
- Extract year and month from order date
- Create high-value order flag
- Create sales buckets
- Add time-based attributes

### 5. Dimensional Modeling (Star Schema)

Created warehouse tables:

- dim_customer
- dim_product
- dim_location
- dim_date
- fact_sales

This models the dataset into an analytics-ready format.

### 6. Business Analysis
- Revenue trends
- Customer insights
- Sales segmentation
- Time-based analysis

---

## Tech Stack

- Python
- Pandas
- Jupyter Notebook
- Dimensional Modeling (Star Schema)
- Git and GitHub

---

## How to Run This Project

1. Clone the repository

   git clone https://github.com/sirTIKekar/retail-data-engineering.git

2. Install dependencies

   pip install -r requirements.txt

3. Run notebooks in the following order:

   01_data_ingestion  
   02_data_cleaning  
   03_data_validation  
   04_feature_engineering  
   05_data_modeling_star_schema  
   06_business_analysis  

---

## Key Skills Demonstrated

- Structured data pipeline design
- Schema validation
- Data quality checks
- Feature engineering
- Dimensional modeling
- Reproducible workflow
- Version control using Git

---

## Author

Saurabh Tikekar  
Data Engineer  
GitHub: https://github.com/sirTIKekar  

---

## Future Enhancements

- Add SQLite warehouse integration
- Convert pipeline to PySpark
- Add logging framework
- Orchestrate using Airflow
- Add Docker containerization
- Implement automated testing
