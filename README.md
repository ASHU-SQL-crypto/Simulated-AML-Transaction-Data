# AML Transaction Monitoring & Data Analytics

An end-to-end AML transaction monitoring and data analytics project using **Microsoft SQL Server, Excel, Power Query and Power BI**.

The project demonstrates how data analytics techniques can support financial crime compliance through data cleaning, data quality assessment, customer risk analysis and transaction monitoring.

## Business Objective

To transform an intentionally messy simulated AML transaction dataset into structured, analysis-ready data and develop monitoring queries that help identify potentially unusual transaction activity.

## Dataset Overview

| Attribute | Details |
|---|---|
| Dataset | Simulated AML transactions |
| Period | January–December 2025 |
| Transactions | 660 |
| Customers | 12 |
| Accounts | 12 |
| Data fields | 17 |
| Data type | Synthetic training data |

The dataset contains intentional data-quality issues, including duplicate records, missing values, inconsistent formats, invalid transaction amounts and outliers.

## Technology Stack

- **SQL Server:** Data querying, validation, CTEs, aggregations and window functions
- **Excel:** Initial data inspection and validation
- **Power Query:** Data cleaning and transformation
- **Power BI:** Data modelling, visualisation and reporting

## Analysis Performed

### 1. Data Cleaning and Quality Assessment
- Identified duplicate and incomplete records
- Investigated invalid transaction amounts and outliers
- Standardised country names, transaction types, statuses and channels
- Prepared the cleaned dataset for analytical reporting

### 2. SQL-Based Transaction Monitoring
Developed SQL queries to investigate:
- High-value cross-border transactions
- Transactions exceeding expected monthly activity
- Multiple transactions occurring on the same day
- Activity involving high-risk customers
- Alert-flagged transactions
- Largest transactions by customer

SQL techniques applied include:
- Joins and aggregations
- CASE expressions
- Common Table Expressions (CTEs)
- Subqueries
- Window functions

### 3. Power BI Reporting
Used Power Query and Power BI to prepare and present the cleaned transaction data.



## Repository Structure

```text
Simulated-AML-Transaction-Data/
│
├── AsharAMLDATA.sql
├── PowerBI_Messy_AML_Transactions.xlsx
├── Clean DATA.pbix
├── Clean Data Snapshot.png
├── Power BI Compliance Snapshot.png
├── Ashar_Digital_PJSC_AML_CFT_Policy_Manual.pdf
├── README.md
└── sql/
    ├── CREATE_AML_RAW_TABLE_AND_VIEW.sql
    └── AML_DATA_QUALITY_AND_MONITORING.sql
```

*Update this structure to match the actual folders and filenames in the repository.*

## Key Learning Outcomes

- Applied SQL to investigate transaction-monitoring scenarios.
- Used data-quality checks to identify and address common data issues.
- Transformed raw transaction data into an analysis-ready dataset.
- Applied AML/KYC domain knowledge to analytical use cases.
- Developed a foundation for compliance-focused Power BI reporting.

## Disclaimer

This project uses simulated data for educational and portfolio purposes. The monitoring scenarios are illustrative and do not represent production banking rules or regulatory determinations.

## Author

**Ashar Siddiqui**

AML/KYC and Financial Crime Compliance Professional | CAMS Certified

Developing practical expertise in SQL Server, Power BI and data analytics, with a focus on financial crime analytics and transaction monitoring.
