# Analysis Approach – Chocolate Sales

**Author:** Anzela Rizakova  
**Project:** Chocolate Sales  
**Dataset:** Chocolate_sales.csv  
**The dataset source:** https://www.kaggle.com/datasets/atharvasoundankar/chocolate-sales


## 1. Project Objective

The objective of this analysis was to evaluate the performance of a global chocolate sales business by identifying key revenue drivers, product performance trends, geographical patterns, and salesperson effectiveness. The analysis aimed to transform transactional sales data into actionable business insights using Power BI.

## 2. Dataset Overview

- **Source File:** Chocolate_sales.csv
- **Records:** 1094 orders
- **Time Period:** January – August 2022
- **Key Variables:**
  - Date
  - Salesperson
  - Product
  - Amount
  - Boxes Shipped
  - Country

## 3. Analysis Workflow

### Step 1: Environment Setup & Imports

The analysis was conducted using **Microsoft Power BI Desktop**

### Step 2: Data Loading

The dataset was loaded using into Power BI Desktop using the **Get Data/(Text/CSV)** feature. **Power Query Editor** was used for data inspection, transformation, and preparation.

### Step 3. Initial Data Exploration

- Reviewing available fields and metrics
- Examining data types
- Identifying the number of records and variables
- Understanding relationships between products, countries, salespersons, and revenue

### Step 4: Missing Value Handling

- Checked for missing value across all columns (not found)

### Step 5: Data type conversion and transformation

- Removing unnecessary columns (not identified)
- Converting data types to Date, Decimal Numbers and Text
- Creating calculated columns (**Price per Box**) to support analysis and reporting
- Creating a **Month column** from the Date field to support monthly revenue and sales trend analysis.

### Step 6: DAX Measures

DAX measures were created to support advanced analysis and KPI reporting within Power BI. These measures enabled the calculation of key business metrics, performance comparisons, and statistical indicators used throughout the dashboard.

**Key DAX Measures**

- Total Sales Revenue
- Total Boxes Shipped
- Average Monthly Revenue
- Revenue Contribution (%) by Country, Product, and Salesperson
- Top-Performing Country, Product, and Salesperson (by Revenue)
- Top-Performing Country, Product, and Salesperson (by Boxes Shipped)
- Sales Z-Score for outlier detection
- Most Consistent Salesperson Identification
- Most Stable Product Identification
- Standard Deviation Measures for sales stability analysis
- Coefficient of Variation (CV%) Measures for consistency assessment

## Step 7: Visual and Statistical Analysis

### 7.1 Executive Dashboard:

- **Cards/KPIs** for displaying key metrics, including Total Sales, number of Countries, Products, Salespersons, and Boxes Shipped.
- **Line charts** for analysing revenue trends over time, both overall and by Country.
- **Stacked bar charts** for visualising Revenue and Country contribution.
- **Tables and matrices** for displaying the top 5 Countries, Products, and Salespersons by Revenue.
- **Map visual** for illustrating sales distribution across Countries.
- **Pie chart** for sales distribution by Country (%)

#### Key Observation:

##### KPIs:

- Total Sales reached $6.18M across 6 countries, 22 products, and 25 salespersons.
- Average monthly sales amounted to $0.77M.
- A total of 1.09M boxes were shipped, with an average revenue of $105.72 per box.
- Australia was the top-performing country by revenue.
- Smooth Silky Salty was the top-performing product by revenue.
- Chess Bonnell was the top-performing salesperson by revenue.

##### Sales trend:

- Revenue peaked in January, driven by strong sales in the UK, New Zealand, and India. A notable decline followed in February, primarily due to reduced sales in these same markets.
- Revenue remained below the monthly average from February to May.
- April recorded the lowest revenue of the year. While India and the USA experienced sales growth, substantial declines across other markets led to an overall decrease in revenue.
- Revenue increased significantly in June and reached its highest level, largely due to higher sales in the UK and New Zealand.
- Revenue remained above the monthly average in July. Despite significant sales declines in the UK and New Zealand, robust growth across other markets supported overall revenue performance.
- August revenue dropped below the average level, following a widespread decline in sales across almost all markets.

##### Limitation:

- No historical sales data was available for prior years, limiting the ability to assess seasonality and evaluate performance relative to previous periods.
- The analysis is based on a single reporting period and therefore reflects short-term trends rather than long-term sales patterns.

### 7.2 Product Analysis:

- **Line and stacked column chart** for comparing sales trends against boxes shipped over time.
- **Card/KPI** for displaying the average revenue per box.
- **Stacked bar chart** for visualising sales performance by product.
- **Scatter plot** for analysing the relationship between average sales and sales variability, helping identify stable and volatile products.
- **Decomposition tree** for exploring the distribution of boxes shipped across products and countries.
- **Tables and matrices** for displaying detailed product-level metrics, including Sales Revenue, Revenue Contribution (%), Sales Variability (%), Boxes Shipped, and Minimum, Maximum, and Average Revenue per Box.

#### Key Observation:

- Smooth Silky Salty was the top-selling product during the reporting period, generating the highest revenue among all products.
- 70% Dark Bites generated the lowest sales revenue among all products
- **Revenue was influenced by both product pricing and shipment volume, as high-value orders were not always associated with large quantities.**
- **Price per box ranged from £0.01 to £4,291 (average: £105.72), indicating substantial variation in product pricing.**
- **Order sizes ranged from 1 to 709 boxes (average: 162), suggesting a mix of small and bulk purchasing patterns across customers.**
- A minimum variation of 53% and a maximum variation of %86 was observed across products, indicating that product demand fluctuated considerably throughout the reporting period (53% - White Choc, 86% - Organic Choco Syrup)
- Further investigation using interactive dashboard filters revealed that 85% Dark Bars became the top-selling product in the UK during June, contributing significantly to the country's sales spike. This represented an unusual sales pattern, as the product was only sold in the UK during June and July.

### 7.3 Country Analysis:

- **Cards/KPIs** for highlighting the top-performing countries by Revenue and Boxes Shipped.
- **Ribbon chart** for visualising changes in country revenue rankings over time.
- **Scatter chart for** assessing sales stability by country, comparing Average Revenue against Sales Variability.
- **Clustered bar chart** for visualising country Z-scores and identifying markets with unusually high or low sales performance relative to the overall average.
- **Matrix** for displaying detailed country-level metrics, including Revenue, Revenue Contribution (%), Boxes Shipped, Average Revenue per Box, Top Product, and Sales Variability (%).

#### Key Observation:

- Although Australia generated the highest revenue, the narrow Z-score range (-0.04 to 0.06) indicates that overall sales performance remained relatively balanced across markets, with no extreme outliers.
- Australia, Canada, and New Zealand were the most consistent markets, exhibiting the lowest sales variability based on standard deviation analysis.
- India, the UK, and the USA contributed significantly to overall revenue but showed greater variability in sales performance, making them key markets for monitoring future growth trends.

### 7.4 Salesperson Analysis:

- **Card/KPI and stacked column chart** for highlighting the top-performing salesperson and visualising their monthly sales performance.
- **Matrix (filtered)** for identifying the most consistent salesperson based on the highest number of active sales months and the lowest sales variability.
- **Stacked bar chart** for visualising salesperson revenue performance, with products used as the legend to illustrate sales composition.
- **Matrix** for displaying detailed salesperson-level metrics, including Sales Trend Sparklines, Revenue, Revenue Contribution (%), Average Sales, Boxes Shipped, Average Revenue per Box, Top Product, Top Country, and Sales Variability (%).

#### Key Observation:

- Salesperson revenue contributions were relatively balanced, with no individual contributing more than 5.19% of total revenue.
- Chess Bonnell generated the highest revenue contribution, accounting for 5.19% of total sales.
- Madelene Upcott delivered the most consistent performance, contributing 5.11% of total revenue while exhibiting the lowest sales variability among all salespersons.
- Wilone O'Kielt contributed 2.24% of total revenue, representing the lowest revenue contribution among all salespersons.
- Every salesperson recorded sales across all product categories and maintained activity for at least one month during the analysis period.
- Further investigation using interactive dashboard filters revealed that the number of active salespersons each month is consistent (25) except only one month - March (24).

## 8. Conclusion

- Revenue growth appears to be driven by specific products, markets, and time periods rather than consistent performance throughout the year.
- Volatile but high-performing markets such as the UK, USA, and India offer growth opportunities but require careful monitoring.
- Stable markets such as Australia, Canada, and New Zealand provide a reliable revenue foundation.
- The consistent number of active salespersons across all months suggests that revenue fluctuations are unlikely to be driven by salesperson participation levels. As total revenue contributions were relatively balanced across salespersons, a monthly performance analysis may provide deeper insights into individual performance patterns and revenue drivers.
- The wide variation in revenue per box, ranging from £0.01 to £4,291, highlights the need for further investigation into pricing consistency, product segmentation, and potential data quality issues. Understanding the drivers behind these extreme values may help optimise pricing strategies and improve revenue performance.
- Significant variation in product demand highlights the importance of targeted inventory, pricing, and marketing strategies.

## 9. Tools & Technique used

- **Power BI Desktop** for data modelling, analysis, and dashboard development.
- **Power Query** for data cleaning and transformation.
- **DAX** for KPI creation, statistical calculations, and performance analysis.
- **Data visualisation techniques**, including KPI cards, line charts, scatter plots, decomposition trees, maps, and matrices.
- **Analytical techniques**, including trend analysis, contribution analysis, ranking, Standard Deviation, Coefficient of Variation (CV%), and Z-Score analysis.
- **Interactive data visualisation** through page navigation buttons, filters and cross-filtering

## 10. Key Takeaways from the Approach

- **Data Quality First** – Data cleaning, transformation, and validation were performed before analysis to ensure reliable and accurate insights.
- **Progressive Analysis** – The analysis progressed from high-level business performance metrics to detailed product, country, and salesperson investigations.
- **Visual Storytelling** – Multiple visualisation techniques were used to communicate trends, comparisons, rankings, and patterns in an intuitive and actionable way.
- **Statistical Analysis** – Traditional sales performance analysis was complemented with Standard Deviation, Coefficient of Variation (CV%), and Z-Score analysis.
- **Actionable Insights** – Focused on findings that help stakeholders understand performance, identify opportunities, and support strategic decision-making.

## 11. Files Related to this Analysis
- **PBIX File:** [Chocolate_Sales_Analysis.pbix](PBIX/Chocolate_Sales_Analysis.pbix)
- **Source Dataset:** [Chocolate_Sales.xlsx](Data/Chocolate_Sales.xlsx)
- **Dashboard PDF:** [Chocolate_Sales_Dashboard.pdf](Docs/Chocolate_Sales_Dashboard.pdf)

---
<sub> This document outlines the structured analytical approach followed throughout the project. <sub/>

<sub> Created by [Anzela Rizakova](https://github.com/anzelary) | Power BI Portfolio Project | 2026 <sub/>
