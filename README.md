# Mobile_sales_analysis

## Overview:
**This is a sales report for Mobile Sales products**

---

## Contents
Project Overview | Data Source | Tools Used | Table Outlay | Query Langaues (SQL) | Visualization

---

## Project Overview:
> > This project analyzes the sales of Mobile Sales Products to uncover insights on sales distribution by various attributes such as Brands, Customer Gender and Payment Method, Using pivot tables, I explored metrics like total sales by Payment Method and Gender, average income of buyers, gender distribution, and overall revenue. This analysis helps to understand the key factors driving sales in the dataset provided.

## Data Source:
www.kaggle.com/dataset

## Tools Used:
+	Pivot Table / Charts
+	+	PowerBI
  +	+ SQL
   
## Table Outlay:
First Three Records
|TransactionID|	Date	|MobileModel	|Brand	|Price	|UnitsSold|	TotalRevenue	|CustomerAge|	CustomerGender|	Location	|PaymentMethod|
|-------|------|------|------|-----|------|------|-------|------|------|------|
|79397f68-61ed-4ea8-bcb2-f918d4e6c05b|	1/6/2024|	direction	|Green Inc|	1196.95|	85	|28002.8	|32	|Female|	Port Erik|	Online|
|4f87d114-f522-4ead-93e3-f336402df6aa	|4/5/2024	|right	|Thomas-Thompson	|1010.34|	64|	2378.82|	55	|Female	|East Linda	|Credit Card|
|6750b7d6-dcc5-48c5-a76a-b6fc9d540fe1	|2/13/2024	|summer|	Sanchez-Williams	|400.8	|95	|31322.56	|57	|Male|	East Angelicastad	|Online|

## Query Langaue: (SQL)
Some of the query languages to retrieve records are displayed here

```SQL
---Calculate Total Revenue by paymentmethod---
SELECT paymentmethod, SUM(price) AS TotalRevenue
FROM mobile_sales
GROUP BY paymentmethod
ORDER BY TotalRevenue DESC;
