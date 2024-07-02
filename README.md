# 📊 Sales Performance Analysis

## 📕 Table of Contents
- [Problem Statement](#-problem-statement)
- [Objective](#-objective)
- [Tools Used](#%EF%B8%8F-tools-used)
- [Dataset Overview](#-dataset-overview)
- [Key Findings](#-key-findings)
- [Recommendations](#-recommendations)
- [Project Presentation](#-project-presentation)
- [Project Learnings](#-project-learnings)
- [Installation and Usage](#-installation-and-usage)
- [Dashboard](#-dashboard)

## ❓ Problem Statement
In a competitive market, understanding the factors driving sales performance, profitability, and customer satisfaction is crucial for sustainable growth. Our organization faces challenges in identifying top-performing products, optimizing inventory, recognizing top-performing regions, and identifying top customers. Additionally, we need to understand the financial impact of discounts to enhance our profit margins.

## 🎯 Objective
The primary objective of this analysis is to provide actionable insights into our sales performance, identify areas for improvement, and develop strategies to boost revenue and profitability. By examining key performance indicators (KPIs) and detailed sales metrics, we aim to:

1. Identify best-selling products and high-revenue generators.
2. Assess total revenue and profit margins to gauge financial health.
3. Understand the impact of shipping methods, category, customer segments, and discounts on sales.
4. Develop targeted strategies to reduce losses and enhance customer satisfaction.

## 🛠️ Tools Used
- **Analytical:**  MySQL\
  <img src="data:image/png;base64,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"> 
- **Presentation:** Microsoft Power Point\
  <img width="96" height="96" src="https://img.icons8.com/fluency/96/microsoft-powerpoint-2019.png" alt="microsoft-powerpoint-2019"/>

## 📅 Dataset Overview
- **Data source:** Internet
- **Time period:** 2014-2017
- **Data size:** Orders Table (5009,22), Returns Table (296,2)
- **Key columns:** Order Id, Ship Mode, Segment, City, Region, Category, Sub-Category, Sales, Quantity, Discount, Profit
- **Calculated columns:** Profit Margin, Average Order Value, Order Completion Rate, Actual Sales, Actual Profit, Amount Lost, Order Complete, Profit on No Discount, Sales on No Discount
- [**Data set Link**](https://github.com/amanat-mahmud/Sales_Performance_Analysis_SQL/blob/main/Superstore.csv)

## 🔎 Key Findings
- Total sales: $9.79M
- Profit margin: 2.88%
- Best-selling product: Canon image CLASS 2200 Advanced Copier
- Preferred shipping mode: Standard class
- Regional performance: East and West regions outperform others
- Product categories: Technology leads in sales
- Customer segments: Consumer segment accounts for half of total sales
- Top customers: Adrian Barton, Tamara Chand, Kelly Collister, and Sean Miller
- Seasonal trends: Last quarter (Oct-Dec) shows significantly higher sales
- City-wise performance: New York City leads in revenue generation
- Discounting strategy: Current approach results in losses for top discounted products
- Most profitable product: Xerox 20 leads in profit margin

## 💡 Recommendations
1. Optimize inventory and marketing for top-performing products
2. Focus on expanding in high-performing regions (East and West) while developing strategies for underperforming areas
3. Reevaluate the discounting strategy to minimize losses and maximize profitability
4. Capitalize on the strong performance during the last quarter with targeted marketing campaigns and adequate inventory
5. Maintain the success of non-discounted products while gradually adjusting strategies for other items
6. Enhance the performance of other shipping modes to balance out the heavy reliance on Standard class
7. Create tailored loyalty programs and personalized marketing for top customers in each segment

## 📌 Project Presentation

### Slides
The detailed presentation slides for this project can be found [here](https://github.com/amanat-mahmud/Sales_Performance_Analysis_SQL/blob/main/sales%20performance%20analysis.pdf)

## 🧠 Project Learnings
1. Crreating new schema and table.
2. Data cleaning (fixing date).
3. Group by.
4. Common Table Expressions (CTE).
5. Window function.
8. Data storytelling.
9. Sharpened analytical and problem-solving abilities.
10. Strengthened strategic planning and  presentation skill.
11. Enhanced communication skills.
12. Actionable Insights Generation.

## 💻 Installation and Usage
- Open MySQL Workbench
- Create new schema
- Create new table
- Import CSV into the table
