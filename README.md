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
  @mysql.svg
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
  <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="96" height="96" viewBox="0,0,256,256" style="fill:#000000;">
      <g fill="#ffffff" fill-rule="nonzero" stroke="none" stroke-width="1" stroke-linecap="butt" stroke-linejoin="miter" stroke-miterlimit="10" stroke-dasharray="" stroke-dashoffset="0" font-family="none" font-weight="none" font-size="none" text-anchor="none" style="mix-blend-mode: normal"><g transform="scale(5.33333,5.33333)"><path d="M0.002,35.041h1.92v-7.085l2.667,6.057c0.329,0.755 0.779,1.022 1.662,1.022c0.883,0 1.315,-0.267 1.644,-1.022l2.667,-5.902v6.93h1.92v-7.258c0,-0.697 -0.277,-1.035 -0.849,-1.209c-1.367,-0.43 -2.285,-0.059 -2.7,0.872l-2.735,6.16l-2.649,-6.16c-0.398,-0.93 -1.332,-1.302 -2.7,-0.872c-0.572,0.174 -0.849,0.511 -0.849,1.208v7.258h0.002z"></path><path d="M13.441,29.281h1.92v4.055c-0.015,0.2 0.064,0.731 0.99,0.745c0.472,0.008 2.821,0 2.85,0v-4.8h1.92c0.008,0 0,5.968 0,5.993c0.01,1.472 -1.828,1.662 -2.673,1.687h-5.006v-0.96c0.01,0 4.787,0.001 4.801,0c1.088,-0.115 0.959,-0.714 0.959,-0.896v-0.064h-3.012c-1.67,-0.015 -2.735,-0.751 -2.747,-1.59c-0.002,-0.078 0.036,-4.134 -0.002,-4.17z"></path><path d="M22.081,35.041h4.807c0.63,0 1.242,-0.132 1.728,-0.36c0.81,-0.372 1.144,-0.875 1.144,-1.536v-1.368c0,-1.476 -1.83,-1.536 -2.88,-1.536h-1.92c-0.755,0 -0.87,-0.456 -0.96,-0.96v-0.96c0.09,-0.384 0.258,-0.9 0.923,-0.96c0.773,0 4.836,0 4.836,0v-0.96h-4.566c-0.755,0 -3.114,0.09 -3.114,1.92v1.187c0,0.84 0.738,1.524 2.34,1.692c0.18,0.012 0.36,0.024 0.539,0.024c0,0 1.866,-0.036 1.92,-0.024c1.08,0 0.96,0.84 0.96,0.96v0.96c0,0.132 -0.03,0.96 -0.971,0.96c-0.072,0 -4.789,0 -4.789,0v0.961z"></path><path d="M40.32,33.08c0,1.159 0.655,1.809 2.392,1.939c0.162,0.011 0.325,0.021 0.488,0.021h4.8v-0.96h-4.435c-0.991,0 -1.325,-0.416 -1.325,-1.011v-6.669h-1.92z"></path><path d="M30.704,33.121v-4.8c0,-1.02 0.5,-1.724 1.916,-1.92h0.672h3.447h0.525c1.416,0.196 2.08,0.899 2.08,1.92v4.782c0,0.827 -0.215,1.271 -0.916,1.559l1.488,1.338h-2.16l-1.07,-0.96h-1.257l-2.136,0.012c-0.309,0 -0.635,-0.043 -0.993,-0.141c-1.074,-0.293 -1.596,-0.857 -1.596,-1.79zM32.624,33.121c0.098,0.467 0.473,0.96 1.14,0.96h1.864l-1.068,-0.96h2.175l0.519,0.482c0,0 0.186,-0.152 0.186,-0.482c0,-0.33 -0.016,-4.8 -0.016,-4.8c-0.098,-0.434 -0.538,-0.96 -1.188,-0.96h-2.471c-0.749,0 -1.14,0.548 -1.14,1.058l-0.001,4.702z"></path><path d="M46.199,25.389c-1.031,-0.028 -1.818,0.068 -2.491,0.351c-0.191,0.081 -0.496,0.083 -0.528,0.323c0.105,0.11 0.121,0.275 0.205,0.41c0.16,0.26 0.432,0.609 0.674,0.791c0.265,0.2 0.538,0.414 0.821,0.587c0.504,0.307 1.067,0.483 1.553,0.791c0.286,0.181 0.57,0.411 0.85,0.615c0.138,0.102 0.23,0.259 0.41,0.323c0,-0.01 0,-0.019 0,-0.029c-0.094,-0.12 -0.119,-0.285 -0.205,-0.411c-0.127,-0.127 -0.254,-0.254 -0.381,-0.381c-0.372,-0.494 -0.846,-0.929 -1.348,-1.289c-0.401,-0.288 -1.298,-0.677 -1.466,-1.143c-0.01,-0.01 -0.019,-0.019 -0.03,-0.03c0.284,-0.032 0.617,-0.135 0.879,-0.205c0.441,-0.118 0.834,-0.087 1.289,-0.205c0.205,-0.059 0.41,-0.117 0.615,-0.176c0,-0.039 0,-0.078 0,-0.117c-0.23,-0.236 -0.395,-0.548 -0.645,-0.762c-0.657,-0.559 -1.373,-1.117 -2.11,-1.583c-0.409,-0.258 -0.915,-0.426 -1.348,-0.645c-0.146,-0.074 -0.402,-0.112 -0.498,-0.234c-0.228,-0.29 -0.351,-0.659 -0.527,-0.996c-0.368,-0.708 -0.73,-1.482 -1.055,-2.227c-0.223,-0.508 -0.368,-1.01 -0.645,-1.466c-1.331,-2.188 -2.764,-3.509 -4.982,-4.807c-0.472,-0.276 -1.041,-0.385 -1.642,-0.528c-0.323,-0.019 -0.645,-0.039 -0.968,-0.059c-0.197,-0.083 -0.401,-0.323 -0.587,-0.44c-0.735,-0.465 -2.621,-1.475 -3.165,-0.147c-0.344,0.838 0.514,1.656 0.821,2.081c0.215,0.298 0.491,0.632 0.645,0.968c0.101,0.22 0.119,0.441 0.205,0.674c0.213,0.574 0.55,1.228 0.826,1.759c0.139,0.269 0.293,0.551 0.469,0.791c0.108,0.147 0.293,0.212 0.323,0.44c-0.181,0.253 -0.191,0.646 -0.293,0.968c-0.458,1.445 -0.285,3.24 0.381,4.308c0.204,0.328 0.686,1.032 1.348,0.762c0.579,-0.236 0.45,-0.967 0.615,-1.612c0.037,-0.146 0.014,-0.253 0.088,-0.351c0,0.01 0,0.019 0,0.03c0.176,0.351 0.351,0.704 0.528,1.055c0.391,0.629 1.084,1.286 1.67,1.73c0.304,0.23 0.544,0.628 0.938,0.762c0,-0.01 0,-0.019 0,-0.03c-0.01,0 -0.019,0 -0.03,0c-0.076,-0.119 -0.196,-0.168 -0.293,-0.264c-0.229,-0.225 -0.485,-0.504 -0.674,-0.762c-0.534,-0.725 -1.006,-1.519 -1.436,-2.345c-0.205,-0.395 -0.384,-0.829 -0.557,-1.231c-0.067,-0.155 -0.066,-0.389 -0.205,-0.469c-0.19,0.294 -0.468,0.532 -0.615,0.879c-0.234,0.555 -0.265,1.233 -0.351,1.934c-0.052,0.018 -0.029,0.006 -0.059,0.029c-0.408,-0.099 -0.552,-0.518 -0.704,-0.879c-0.384,-0.912 -0.455,-2.38 -0.117,-3.429c0.087,-0.272 0.482,-1.127 0.323,-1.378c-0.076,-0.251 -0.328,-0.396 -0.468,-0.587c-0.175,-0.236 -0.348,-0.548 -0.469,-0.821c-0.314,-0.711 -0.612,-1.538 -0.943,-2.257c-0.158,-0.344 -0.425,-0.691 -0.645,-0.996c-0.243,-0.338 -0.516,-0.587 -0.704,-0.996c-0.067,-0.145 -0.158,-0.378 -0.059,-0.528c0.032,-0.101 0.076,-0.143 0.176,-0.176c0.17,-0.132 0.643,0.043 0.821,0.117c0.47,0.195 0.862,0.381 1.26,0.645c0.191,0.127 0.384,0.372 0.615,0.44c0.088,0 0.176,0 0.264,0c0.413,0.095 0.875,0.03 1.26,0.147c0.682,0.207 1.292,0.529 1.846,0.879c1.69,1.067 3.071,2.585 4.016,4.397c0.152,0.292 0.218,0.57 0.351,0.879c0.27,0.624 0.611,1.266 0.879,1.876c0.268,0.609 0.53,1.223 0.909,1.73c0.2,0.266 0.97,0.409 1.319,0.557c0.245,0.104 0.647,0.211 0.879,0.351c0.444,0.268 0.874,0.587 1.289,0.879c0.212,0.147 0.851,0.468 0.883,0.733z"></path><path d="M33.098,14.223c-0.215,-0.004 -0.367,0.023 -0.528,0.059c0,0.01 0,0.019 0,0.03c0.01,0 0.019,0 0.03,0c0.103,0.21 0.283,0.347 0.41,0.528c0.098,0.205 0.195,0.41 0.293,0.615c0.01,-0.01 0.019,-0.019 0.029,-0.029c0.181,-0.128 0.265,-0.332 0.264,-0.645c-0.073,-0.077 -0.084,-0.173 -0.147,-0.264c-0.084,-0.123 -0.246,-0.192 -0.351,-0.294z"></path></g></g>
      </svg>
@mysql.svg
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
