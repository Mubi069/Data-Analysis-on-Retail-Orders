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

Retail orders data: The secondary data used for this analysis is the "orders.csv" file [Donwload here](https://www.kaggle.com/datasets/ankitbansal06/retail-orders?select=orders.csv ) published in kaggle website, containing detailed information about each sale made by the company on the basis of categories, sub-categories, region , etc. This file also contains the orders datewise.


### Tools

- Python (Jupyter Notebook) - Data Cleaning
    - [Download here](https://www.anaconda.com/anaconda-navigator)
- SQL (BigQuery sandbox) - Data Analysis
    - [link](https://cloud.google.com/bigquery/docs/sandbox#limits)


### Data Cleaning (or) Preparation

In the initial data preparation phase, we performed the following tasks:
1. Data loading and inspection
2. Handling missing or null values
3. Data cleaning and formatting

### Exploratory Data Analysis

EDA involved exploring the sales data to answer key questions (objectives), such as:

- What are the top 10 highest revenue generating products?
- What are the top 5 highest selling products in each region?
- Find the monthly growth comparison for 2022 and 2023 sales.
- For each category which month had highest sales?
- Which sub-category had highest growth by profit in 2023 compared to 2022?

### Data Analysis

Include some interesting code/features worked with
  
```sql
SELECT * FROM
```

### Results (or) Findings

The Analysis results are summarized as follows:
1. Product Category 'Technology' is the best-performing category in terms of revenue whereas,
  - The sub-category 'Copiers' & 'Machines' under Technology ranks the top most in all regions in terms of revenues.


### Recommendations

Based on the analysis, we recommend the following actions:
- Invest in marketing and promotions during peak sales seasons to maximize revenue
- Focus on expanding and promoting products in Technology category.
- Implement a customer segmentation strategy to target high-LTV customers effectively.

### Limitations

I removed a few columns to 

### References
1. SQL [BigQuery_Intro](https://cloud.google.com/bigquery/docs/introduction-sql)
2. [Stack Overflow](https://stack.com)
3. 
