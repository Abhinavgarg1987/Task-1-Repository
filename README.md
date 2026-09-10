# E-Commerce Sales Analysis & Dashboard

## Project Overview
This project provides a comprehensive end-to-end data analysis of e-commerce transactions. The main objective is to perform data cleaning, exploratory data analysis (EDA), statistical modeling, and interactive visualization using Python and Power BI to extract meaningful business trends, identify top-performing product categories, and deliver strategic recommendations.

## Problem Statement
E-commerce platforms generate vast amounts of transactional data, but unstructured or unclean data prevents business leaders from making informed decisions. Common issues include missing category labels, invalid negative transaction amounts, duplicate records, and low customer retention rates. This analysis aims to clean raw transactional logs, analyze sales distributions, and build visual dashboards to optimize revenue strategies.

## Dataset Description
The dataset contains transaction-level e-commerce order records with the following primary features:
- **OrderID**: Unique identifier for each transaction.
- **Customer_Name**: Name of the customer placing the order.
- **Category**: Product classification (Electronics, Clothing, Home, etc.).
- **Sales_Amount**: Revenue generated from the transaction (in INR).
- **Order_Date**: Date when the order was placed (YYYY-MM-DD).

## Tools Used
- **Programming Language**: Python
- **Data Manipulation**: Pandas, NumPy
- **Data Visualization**: Matplotlib, Seaborn
- **Interactive Dashboards**: Power BI Desktop
- **Environment**: Jupyter Notebook
- **Version Control**: Git & GitHub

## Data Cleaning Process
1. **Duplicate Removal**: Identified and dropped duplicate order entries (e.g., redundant OrderID `105`).
2. **Invalid Value Handling**: Corrected negative sales figures (e.g., converted or imputed invalid `-500` sales values).
3. **Missing Value Imputation**: Imputed missing `Category` entries with the label `'Unknown'` and missing numerical `Sales_Amount` values using median imputation ($\text{Rs. } 4,500$).
4. **Data Type Conversion**: Parsed `Order_Date` into a standard datetime object for time-series trend analysis.

## Exploratory Data Analysis (EDA)
- **Descriptive Statistics**: Analyzed key metrics including mean ($\text{Rs. } 5,514.28$), median ($\text{Rs. } 4,500$), and standard deviation across sales amounts.
- **Category Performance**: Aggregated total sales per product line to identify high-margin vs. low-performing segments.
- **Outlier Detection**: Utilized the Interquartile Range (IQR) method to flag extreme high-value transactions ($\text{Rs. } 12,000$ order by Aarav exceeding upper bound of $\text{Rs. } 11,650$).

## Visualizations & Dashboard
- **Bar Chart**: Total revenue breakdown by category.
- **Histogram & KDE Plot**: Frequency distribution and density of sales order amounts.
- **Box Plot**: Outlier detection and spread analysis for transaction values.
- **Line Chart**: Daily sales timeline tracking revenue spikes over time.
- **Pie / Donut Chart**: Percentage share of total store revenue by category.
- **Power BI Dashboard**: Consolidated dashboard incorporating KPI cards (Total Revenue, Total Orders, Average Order Value), interactive category slicers, and customer order frequency charts.

## Key Insights
- **Electronics Domination**: Electronics is the top revenue generator, contributing over $65\%$ ($\text{Rs. } 25,400$) of total sales.
- **Skewed Average Order Value**: The AOV of $\text{Rs. } 5,514$ is heavily driven by a few large-value purchases rather than uniform spending.
- **Underperforming Segments**: Home ($\text{Rs. } 4,500$) and Clothing ($\text{Rs. } 6,000$) lag significantly behind in revenue volume.
- **Single-Order Behavior**: Customer activity exhibits low repeat purchasing, indicating a need for retention strategies.

## Business Recommendations
1. **Cross-Selling & Product Bundling**: Create promotional packages combining high-demand Electronics with lower-performing Home or Clothing items to boost basket size.
2. **Customer Loyalty Program**: Implement targeted discount incentives (e.g., $10\%$ off on second order within 30 days) to convert one-time buyers into recurring customers and raise LTV.

## Conclusion
Through systematic data cleaning and multi-chart visualizations, this project successfully transformed raw sales data into strategic business insights. Addressing category imbalances and focusing on customer retention will enable sustainable revenue growth for the platform.