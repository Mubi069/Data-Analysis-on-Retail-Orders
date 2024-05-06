# Analysis-on-Retail-Orders

## Table of Contents

- [Project Overview](#project-overview))
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning / Preparation](#data-cleaning-or-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results / Findings ](#results-or-findings)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)

### Project Overview

This data analysis project aims to provide insights into the sales performance of a retail company over the past two years. By analyzing various aspects of the retail orders data, we seek to identify trends to answer the objectives (business task) of the project, making data-driven recommendations, and gain a deeper understanding of the company's performance. 

### Data Sources

Retail orders data: The secondary data used for this analysis is the "orders.csv" file published in [kaggle website](https://www.kaggle.com), containing detailed information about each sale made by the company on the basis of categories, sub-categories, region , etc. This file also contains the orders datewise.


### Tools

- Python (Jupyter Notebook) - Data Cleaning
    - [Donwload here](https://www.anaconda.com/anaconda-navigator)
- SQL (BigQuery sandbox) - Data Analysis
    - [link](https://cloud.google.com/bigquery/docs/sandbox#limits)
- Tableau Public - Data Visualization
    - [Donwnload here](https://www.tableau.com/products/public/download)


### Data Cleaning (or) Preparation

In the initial data preparation phase, we performed the following tasks:
1. Data loading and inspection
2. Handling missing or null values
3. Data cleaning and formatting

### Exploratory Data Analysis

EDA involved exploring the sales data to answer key questions (objectives), such as:

- What are the top 10 highest revenue generating products?

![RevGenPro](https://github.com/Mubi069/Data-Analysis-on-Retail-Orders/assets/162678823/fcc2cacb-1baa-4a0b-ab27-13c6777585bf)

- What are the top 5 highest selling products in each region?

![Top_5 sales in each region](https://github.com/Mubi069/Data-Analysis-on-Retail-Orders/assets/162678823/ad72de47-ffb1-4bb1-8507-5bac962e052a)

- Find the monthly growth comparison for 2022 and 2023 sales.

![MonGroCom_22Vs23](https://github.com/Mubi069/Data-Analysis-on-Retail-Orders/assets/162678823/3fca1819-04c8-4d16-aa33-2f9c7cef2f97)
- For each category which month had highest sales?
- Which sub-category had highest growth by profit in 2023 compared to 2022?

### Data Analysis

Include some interesting code/features worked with
  
```sql
WITH tempt as (
  SELECT sub_category, EXTRACT(year FROM order_date) as order_year, SUM(sale_price) as sales  
  FROM my-first-project-419721.Project_1.orders
  GROUP BY sub_category, order_year
), tempt2 as (
  SELECT sub_category,
  SUM(CASE WHEN order_year=2022 THEN sales ELSE 0
  END) as sales_2022,
  SUM(CASE WHEN order_year=2023 THEN sales ELSE 0 END) as sales_2023
  FROM tempt
  GROUP BY sub_category)
SELECT *, ((sales_2023-sales_2022)*100/sales_2022) as growth
FROM tempt2
ORDER BY growth DESC
LIMIT 1
```

### Results (or) Findings

The Analysis results are summarized as follows:
1. Product Category 'Technology' is the best-performing category in terms of revenue whereas,
  - The sub-category 'Copiers' & 'Machines' under Technology ranks the top most in all regions in terms of revenues.


### Recommendations

Based on the analysis, we recommend the following actions:
- Invest in marketing and promotions during peak sales seasons to maximize revenue
- Focus on expanding and promoting products in Technology category.
- Implement a customer segmentation strategy to target high-LTV customers effectively. (change)

### Limitations

I removed a few columns to 

### References
1. SQL [BigQuery_Intro](https://cloud.google.com/bigquery/docs/introduction-sql)
2. Python [Intro](https://docs.python.org/3/tutorial/index.html)
3. [Tableau Public](https://public.tableau.com/app/discover)
4. [Stack Overflow](https://stack.com)
