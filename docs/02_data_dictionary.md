# Data Dictionary

## Dataset Information

Dataset Name:
Online Retail Dataset

Source:
UCI Machine Learning Repository

Dataset Period:
December 2010 - December 2011


## Column Description


| Column | Data Type | Description |
|--------|-----------|-------------|
| InvoiceNo | Object | Unique identifier for each transaction |
| StockCode | Object | Unique code assigned to each product |
| Description | Object | Product name |
| Quantity | Integer | Number of products purchased |
| InvoiceDate | Datetime | Date and time when transaction occurred |
| UnitPrice | Float | Price of one product unit |
| CustomerID | Integer | Unique identifier for each customer |
| Country | Object | Customer's country location |


## Business Meaning


### InvoiceNo

Represents a transaction identifier.

One invoice can contain multiple products.


### StockCode

Represents product identification code used by the company.


### Description

Contains product names that are used for product performance analysis.


### Quantity

Shows how many units were purchased in each transaction.


### UnitPrice

Represents the selling price per unit.


### CustomerID

Used to analyze customer behavior and purchasing patterns.


### Country

Used for geographic sales analysis.