# Superstore Sales — Exploratory Data Analysis
 
## Overview
This project performs an end-to-end exploratory data analysis (EDA) on a retail Superstore sales dataset, uncovering patterns in shipping preferences, customer segments, and regional sales performance. The analysis moves from data cleaning through univariate, bivariate, and multivariate analysis, translating each finding into concrete business recommendations.
 
## Dataset
- **Source:** Superstore sales dataset (`superstore_final_dataset.csv`)
- **Fields include:** Order Date, Ship Date, Ship Mode, Segment, Region, Sales, and other order-level attributes
- Dropped non-analytical identifier columns (`Postal_Code`, `Row_ID`) during cleaning
## Tools & Libraries
- **Python** — pandas, NumPy
- **Visualization** — Matplotlib, Seaborn
- **Data quality** — missingno (missing value visualization)
## Methodology
 
### 1. Data Cleaning & Validation
- Inspected data structure, types, and missing values
- Removed non-informative identifier columns
- Converted `Order_Date` and `Ship_Date` to datetime format
- Separated numeric and categorical columns for validation (e.g., checking for invalid negative sales values)
### 2. Univariate Analysis
- Distribution of **Ship Mode**: Standard Class is the most used shipping method, followed by Second Class, with Same Day the least used — reflecting customer preference for cost over speed.
- Distribution of **Segment**: Consumer segment drives the highest order volume, followed by Corporate and Home Office.
### 3. Bivariate Analysis
- Created a `Sales_Category` feature (Low / Medium / High) by binning the `Sales` column
- Analyzed the relationship between Segment and Sales Category
- Compared total sales by Segment and by Region
### 4. Multivariate Analysis
- Examined Sales across the combination of Region, Segment, and Ship Mode using a stacked bar chart
- Identified the West region as the top performer, driven mainly by Consumer and Corporate customers using Standard Class shipping
## Key Findings & Business Recommendations
 
**Shipping Mode**
- Standard Class dominates due to its lower cost; premium shipping options (First Class, Same Day) are underused.
- *Recommendation:* Review pricing on premium shipping tiers and use promotions to encourage adoption; investigate whether faster shipping options provide adequate value for their cost.
**Customer Segment**
- The Consumer segment generates the most orders, indicating a predominantly consumer-driven business.
- *Recommendation:* Optimize the buying experience (pricing, support, availability) for consumers, while pursuing targeted, segment-based marketing to grow Corporate and Home Office volume.
**Regional Performance**
- The West region leads in total sales, followed by East, Central, and South (South lags significantly).
- *Recommendation:* Study West region's marketing strategy for replication elsewhere; run A/B tests and targeted promotions/discounts in underperforming regions like the South.
**Cross-Cutting Insight**
- Across all regions, Standard Class shipping dominates regardless of segment, reinforcing a broad customer preference for affordability over speed — signaling an opportunity to grow premium shipping through bundling and incentives.
## Project Structure
```
├── data_eda.ipynb           # Full analysis notebook
├── superstore_final_dataset.csv   # Source data (not included in repo)
└── README.md                # Project documentation
```
 
## Skills Demonstrated
- Data cleaning and validation
- Exploratory data analysis (univariate, bivariate, multivariate)
- Data visualization with Matplotlib/Seaborn
- Feature engineering (binning/categorization)
- Translating data insights into actionable business recommendations
