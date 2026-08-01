AML Transaction Monitoring and Data Cleaning Project

Project Overview

This portfolio project demonstrates an end-to-end analysis of a simulated anti-money laundering (AML) transaction dataset using SQL Server, Microsoft Excel, Power Query, and Power BI.

The dataset intentionally contains data-quality problems commonly encountered in financial-crime analytics, including duplicate transaction IDs, missing values, inconsistent country names, capitalization issues, extra whitespace, invalid amounts, and outliers. The objective is to clean and validate the data, explore customer and transaction risk, and develop sample transaction-monitoring scenarios.

Disclaimer: This project uses simulated data for educational and portfolio purposes. The monitoring rules are simplified examples and should not be treated as production AML controls.

Project Objectives

Identify and document data-quality issues.

Standardize transaction, customer, country, status, and channel fields.

Detect duplicate or incomplete transaction records.

Analyse high-risk customers and alert-flagged transactions.

Develop SQL-based sample monitoring scenarios.

Prepare the cleaned data for Power BI reporting.

Demonstrate practical AML domain knowledge alongside SQL and Power BI skills.

Dataset Summary

The source workbook contains:

660 simulated transaction records

17 columns

12 customer IDs

12 account IDs

Transactions dated from January to December 2025

Customer risk ratings: Low, Medium, and High

Multiple transaction types, channels, currencies, countries, and statuses

The workbook also includes a data dictionary explaining the purpose of each field.

Repository Files

File

Description

PowerBI_Messy_AML_Transactions.xlsx

Original simulated dataset containing intentional data-quality issues

Clean DATA.pbix

Power BI file used for data cleaning and visual analysis

AsharAMLDATA.sql

Initial SQL Server database schema

sql/CREATE_AML_RAW_TABLE_AND_VIEW.sql

Suggested raw-data table and cleaned SQL view matching the Excel dataset

sql/AML_DATA_QUALITY_AND_MONITORING.sql

Data-quality checks and sample AML monitoring queries

Main Data Fields

The dataset includes transaction identifiers, dates, account and customer details, customer risk ratings, transaction types, channels, transaction countries, amounts, currencies, statuses, expected monthly volumes, alert flags, and analyst notes.

Data-Quality Issues Included

The dataset intentionally contains:

Duplicate transaction IDs and duplicate records

Null or blank values

Extra spaces in identifier fields

Inconsistent country names, such as UAE, U.A.E., and United Arab Emirates

Inconsistent transaction-type capitalization

Inconsistent status capitalization

Negative, zero, missing, text, and unusually large transaction amounts

Missing customer names, risk ratings, channels, currencies, and transaction countries

Recommended Workflow

Import the raw Excel data.

Profile the data and identify quality issues.

Clean and standardize fields in Power Query or SQL.

Validate duplicates, nulls, invalid amounts, and category inconsistencies.

Analyse customer and transaction risk.

Build monitoring scenarios in SQL.

Present key patterns and findings in Power BI.

Example Monitoring Scenario

The following query identifies UAE transactions between AED 8,000 and AED 10,000 conducted through a branch or ATM:

SELECT
    TransactionID,
    TransactionDate,
    CustomerID,
    CustomerName,
    RiskRating,
    TransactionType,
    Channel,
    TransactionCountry,
    Amount,
    Currency,
    AlertFlag
FROM dbo.vw_AML_Transactions_Clean
WHERE Amount BETWEEN 8000 AND 10000
  AND TransactionCountry = 'UAE'
  AND Channel IN ('Branch', 'ATM')
ORDER BY Amount DESC;

Important Modelling Limitation

The current dataset does not contain a separate Debit/Credit or Transaction Direction field. Therefore, a query cannot reliably identify credits merely from TransactionType.

A future version should add a field such as:

TransactionDirection: Credit / Debit

This would allow accurate monitoring of incoming credits rather than inferring direction from transaction descriptions.

Additional Monitoring Scenarios

The SQL analysis file includes examples for:

Duplicate transaction detection

Missing mandatory fields

Invalid and outlier amounts

High-risk and alert-flagged transactions

High-value cross-border activity

Transactions exceeding expected monthly volume

Multiple same-day transactions by a customer

Ranking the largest transactions for each customer

Suggested Power BI Dashboard Pages

To make the project easier for recruiters to review, the dashboard can include:

Executive Overview — transaction count, total amount, alert rate, high-risk customers, and average transaction amount.

Risk Analysis — transaction values by customer risk rating, country, and customer segment.

Alert Analysis — flagged transactions by transaction type, channel, country, and status.

Data Quality — duplicates, missing values, inconsistent categories, and invalid amounts.

Customer Drill-through — transaction history and risk indicators for an individual customer.

Add at least one dashboard screenshot to the repository so visitors can understand the project without downloading the PBIX file.

Skills Demonstrated

SQL Server

Data profiling and validation

SQL data cleaning

Common table expressions

Aggregations and grouping

Window functions

AML transaction-monitoring logic

Power Query

Power BI data modelling and visualization

Documentation and GitHub project presentation

Future Improvements

Add TransactionDirection and base-currency amount fields.

Add a cleaned CSV or Excel output for easy review.

Add database relationships and an ER diagram.

Separate raw, cleaned, and reporting layers.

Add dashboard screenshots.

Document Power Query transformations and DAX measures.

Include query outputs or screenshots showing identified scenarios.

Add a short conclusions section summarising the most important findings.

Author

Ashar SiddiquiAML professional developing practical skills in SQL, Power BI, and data analytics.
