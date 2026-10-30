
# Customer, Regional, and Sales Performance Dashboard

## Project Overview

This Power BI project analyzes customer behavior, regional sales performance, product revenue, income-level profitability, and age-based revenue contribution. The dashboard provides business insights into monthly revenue trends, regional performance, product profitability, and customer segments that drive the most value.

The goal of this project is to help stakeholders quickly understand where revenue and profit are coming from, identify top-performing customer groups, and support better sales and marketing decisions.

## Source of Data

The dataset used for this electronic sales performance analysis was sourced from Kaggle, a public data platform that provides datasets for data analysis, machine learning, and business intelligence projects. The data contains customer information, product details, and sales transaction records, which were used to build the Power BI dashboard.

The dataset was cleaned, transformed, and modeled in Power BI to analyze customer demographics, regional sales performance, monthly revenue trends, product profitability, and income-level contribution. The data source supports the objective of generating meaningful business insights and recommendations from electronic sales transactions.

## Problem Statement

- Retail businesses often generate large volumes of customer, product, and sales data, but struggle to convert this information into clear insights for decision-making. Without a centralized view of revenue trends, regional performance, product profitability, and customer segment behavior, it becomes difficult to identify which markets, products, and customer groups are driving business growth.

- This project addresses the need to analyze electronic sales performance by combining customer, product, and transaction data into an interactive Power BI dashboard. The analysis focuses on understanding monthly revenue trends, comparing regional sales performance, identifying profitable income-level segments, evaluating revenue contribution by customer age, and assessing product-level sales and profit performance.

- The dashboard helps answer key business questions such as which region generates the highest revenue, which customer demographic contributes the most sales, which income group delivers the strongest profit, and which products perform best across sales, revenue, and profit. By uncovering these insights, the business can make more informed decisions about customer targeting, regional sales strategy, product prioritization, and revenue improvement.

- Based on the analysis, the business can focus marketing efforts on high-value customer segments, strengthen performance in leading regions, investigate declining monthly revenue patterns, and improve data consistency across regional categories. This enables stakeholders to move from raw sales data to actionable recommendations that support profitability, customer growth, and better strategic planning.

---

## Dashboard Preview
<img width="960" height="540" alt="ELECT G" src="https://github.com/user-attachments/assets/ef396e09-90cf-4aba-a04e-3fc6e3ea0a54" />

<img width="970" height="542" alt="image" src="https://github.com/user-attachments/assets/e22248c5-b2a8-426a-960a-0780bdb66d83" />


---

## Data Model

The dashboard uses a simple star-schema style model with three main tables:

<img width="983" height="524" alt="DATA ELEC" src="https://github.com/user-attachments/assets/c345e5a1-4bac-47d0-afc8-93919d723acf" />


### Tables Used

- **Customers**
  - CustomerID
  - CustomerName
  - Gender
  - Age
  - IncomeLevel
  - Region
  - SignupDate

- **Sales**
  - SaleID
  - CustomerID
  - ProductID
  - SaleDate
  - Month
  - Quantity
  - Unit Cost
  - Total Revenue
  - Profit

- **Products**
  - ProductID
  - ProductName
  - Brand
  - Category
  - Color
  - Weight

### Relationships

- `Customers[CustomerID]` connects to `Sales[CustomerID]`
- `Products[ProductID]` connects to `Sales[ProductID]`

This structure allows sales performance to be analyzed by customer demographics, product details, and regional segments.

---

## Key Business Questions

This dashboard answers the following questions:

- Which month generated the highest and lowest revenue?
- Which region contributed the most sales revenue?
- Which customer age group drives the highest revenue?
- Which income level contributes the most profit?
- Which products generate the highest sales, revenue, and profit?
- How does regional performance compare across locations?

---

## Dashboard Insights

### Monthly Revenue Performance

- **May recorded the highest monthly revenue** with approximately **$1.15M**.
- Revenue declined in June and July.
- **July showed the lowest revenue**, at approximately **$0.96M**.
- This suggests a downward revenue trend after May that may require further investigation.

### Revenue by Age

- Customers aged **35** generated the highest revenue, contributing approximately **$0.92M**.
- Customers aged **40** followed with approximately **$0.79M**.
- The age group around **35 years old** appears to be the strongest revenue-driving segment.

### Regional Sales Performance

- The **East region** led total revenue with approximately **$0.80M**.
- South and West followed with approximately **$0.70M** and **$0.64M** respectively.
- North/north regions showed comparatively lower performance, suggesting a potential need for regional data cleaning or naming standardization.

### Profit by Income Level

- **Medium-income customers generated the highest profit**, contributing approximately **$889K**.
- High-income customers followed with approximately **$772K**.
- Low-income customers contributed approximately **$721K**.
- This indicates that the medium-income customer segment may be the most profitable target group.

### Product Performance

The product table shows performance across sales amount, revenue, and profit.

| Product | Sales Amount | Revenue | Profit |
|---|---:|---:|---:|
| Headphones | $182,800 | $558,550 | $430,590 |
| Keyboard | $132,200 | $395,400 | $302,860 |
| Laptop | $120,500 | $357,800 | $273,450 |
| Monitor | $181,200 | $554,550 | $427,710 |
| Mouse | $127,200 | $381,250 | $292,210 |
| Phone | $118,350 | $343,450 | $260,605 |
| Tablet | $171,900 | $515,350 | $395,020 |
| **Total** | **$1,034,150** | **$3,106,350** | **$2,382,445** |

---

## Tools Used

- **Power BI Desktop**
- **Power Query**
- **DAX**
- **Data Modeling**
- **Interactive Visualizations**
- **Dashboard Design**

---

## Dashboard Features

- Interactive regional slicer
- Monthly revenue trend visualization
- Revenue by age analysis
- Profit by income level breakdown
- Product-level sales, revenue, and profit table
- Regional revenue comparison
- Customer and product relationship model

  ## Business Recommendations

Based on the dashboard insights:

- Focus marketing efforts on customers around age 35, as they generate the highest revenue.

- Strengthen sales strategies in the East region, which currently leads regional revenue.

- Investigate the revenue decline from May to July to identify possible seasonal or operational causes.
Prioritize the medium-income customer segment, as it contributes the highest profit.

- Review regional naming consistency, especially values like north and North, to improve data quality.
  
- Prioritize the medium-income customer segment, as it contributes the highest profit.

---

## Sample DAX Measures

```DAX
Total Revenue = SUM(Sales[Total Revenue])





