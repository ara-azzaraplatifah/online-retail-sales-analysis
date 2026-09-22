# Data Quality Report


## Overview

Before performing analysis, the dataset was inspected to identify data quality issues that may affect business insights.


## Data Quality Issues


## 1. Missing Values


| Column | Issue |
|--------|-------|
| Description | Missing product information |
| CustomerID | Missing customer identifier |


### Handling Decision

Description:
Rows with missing Description will be removed because product information is required for product analysis.


CustomerID:
Missing CustomerID values will be retained for sales analysis but excluded during customer behavior analysis.



## 2. Duplicate Data


The dataset contains duplicate transaction records.

Duplicate rows will be removed to prevent inaccurate revenue calculation.



## 3. Cancelled Transactions


Transactions with InvoiceNo starting with "C" represent cancelled orders.

These transactions will be excluded from sales performance analysis.



## 4. Invalid Values


Transactions with:

- Quantity <= 0
- UnitPrice <= 0

will be removed because they do not represent valid sales.


## Cleaning Strategy Summary


| Issue | Treatment |
|------|-----------|
| Duplicate rows | Remove |
| Missing Description | Remove |
| Missing CustomerID | Keep for sales analysis |
| Cancelled invoice | Remove |
| Invalid Quantity | Remove |
| Invalid UnitPrice | Remove |