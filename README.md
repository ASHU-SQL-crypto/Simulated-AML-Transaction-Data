AML Transaction Monitoring & Data Cleaning Project
Overview

This project uses a simulated AML transaction dataset to demonstrate data cleaning, analysis, and basic transaction-monitoring scenarios using SQL Server, Excel, Power Query, and Power BI.

The dataset contains common data-quality issues such as duplicate records, missing values, inconsistent formatting, invalid amounts, and outliers.

Disclaimer: The dataset is simulated, and the monitoring rules are simplified examples for learning purposes.

Project Highlights
660 transactions from January–December 2025
12 customers and 12 accounts
17 data fields
Low, Medium, and High customer-risk ratings
Multiple countries, currencies, channels, and transaction types


Work Completed
Identified duplicates, missing values, and invalid amounts
Standardized country names, transaction types, statuses, and channels
Analysed high-risk customers and alert-flagged transactions
Created SQL monitoring queries using CTEs, aggregations, and window functions
Prepared the cleaned data for Power BI reporting


Sample Monitoring Scenarios
High-value cross-border transactions
Transactions exceeding expected monthly volume
Multiple same-day transactions
High-risk and alert-flagged activity
Largest transactions by customer
Duplicate and incomplete records


Repository Files
File	Description
PowerBI_Messy_AML_Transactions.xlsx	Original dataset with intentional quality issues
Clean DATA.pbix	Power BI analysis and data cleaning
AsharAMLDATA.sql	Initial SQL Server schema
sql/CREATE_AML_RAW_TABLE_AND_VIEW.sql	Raw table and cleaned SQL view
sql/AML_DATA_QUALITY_AND_MONITORING.sql	Data-quality checks and monitoring queries


Tools and Skills
SQL Server • Excel • Power Query • Power BI • Data Cleaning • Data Validation • CTEs • Window Functions • AML Transaction Monitoring


Author

Ashar Siddiqui
AML professional developing practical skills in SQL, Power BI, and data analytics.
