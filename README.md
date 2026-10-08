# Superstore Sales Dashboard | Power BI

## Overview

An interactive Power BI dashboard designed to analyze and visualize Superstore sales performance across products, categories, customers, regions, segments, and time periods.

The dashboard provides both high-level business KPIs and detailed sales analysis to help identify trends, top-performing products, customer patterns, and regional performance.

## Dashboard Pages

### 1. Sales Overview

Provides a high-level view of overall sales performance, including:

- Total Sales
- Total Orders
- Total Customers
- Average Order Value
- Sales by Category
- Top 10 Products by Sales
- Monthly Sales Trends
- Year, Region, and Segment filters

### 2. Customer & Geography

Provides deeper analysis of customers and geographical performance, including:

- Sales by Region
- Sales by Customer Segment
- Top Customers by Sales
- Sales by Sub-Category
- Sales by State
- Geographic sales visualization
- Interactive Year, Region, and Segment filters

## Tools & Skills

- Microsoft Power BI
- Power Query
- DAX
- Data Modeling
- Data Visualization
- Business Intelligence

## Dataset

Superstore Sales Dataset from Kaggle by Rohit Sahoo, containing sales data from 2015–2018.

## Data Preparation

- Converted Order Date and Ship Date to proper date types using the appropriate locale
- Set Postal Code as text
- Created a dedicated Date table
- Established a Many-to-One relationship between the Date table and sales table
- Prepared the dataset for time-based analysis

## DAX Measures

Key measures created for the dashboard include:

- Total Sales
- Total Orders
- Total Customers
- Average Order Value
- Sales LY
- YoY Growth %

Example:

```DAX
Total Sales = SUM(train[Sales])

Total Orders = DISTINCTCOUNT(train[Order ID])

Total Customers = DISTINCTCOUNT(train[Customer ID])

Avg Order Value = DIVIDE([Total Sales], [Total Orders])

