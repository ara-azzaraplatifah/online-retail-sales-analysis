# Data Quality Report


## Overview

Before performing analysis, the dataset was inspected to identify data quality issues that may affect business insights.


## Data Quality Issues


## 1. Missing Values


The dataset contains missing values in two columns:


| Column | Missing Values | Percentage |
|--------|---------------|------------|
| Description | 1,454 | 0.27% |
| CustomerID | 135,080 | 24.93% |


### Handling Decision


Description:

Rows with missing Description will be removed because product information is required for product analysis.


CustomerID:

Missing CustomerID values will be retained for sales analysis but excluded during customer behavior analysis.



## 2. Duplicate Data


The dataset contains 5,268 duplicate records (0.97% of total data).


### Handling Decision

Duplicate rows will be removed to prevent double counting during revenue and sales performance analysis.


## 3. Transaction Validation


### Negative Quantity

The dataset contains transactions with negative Quantity values.

Minimum Quantity:
-80,995

These records represent returns or cancelled transactions and will be removed.


### Invalid Unit Price

The dataset contains invalid UnitPrice values.

Minimum UnitPrice:
-11,062.06

Transactions with UnitPrice <= 0 will be removed.


### Cancelled Transactions

There are 9,288 cancelled transactions identified from InvoiceNo starting with "C".

These records will be excluded during data cleaning.



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