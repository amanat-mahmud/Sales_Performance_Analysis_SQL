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
 <div style="width: 96px; height: 96px;">
  <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="96" height="96" viewBox="0,0,256,256" style="fill:#000000;">
    <g fill="#ffffff" fill-rule="nonzero" stroke="none" stroke-width="1" stroke-linecap="butt" stroke-linejoin="miter" stroke-miterlimit="10" stroke-dasharray="" stroke-dashoffset="0" font-family="none" font-weight="none" font-size="none" text-anchor="none" style="mix-blend-mode: normal">
      <g transform="scale(5.33333,5.33333)">
        <path d="M0.002,35.041h1.92v-7.085l2.667,6.057c0.329,0.755 0.779,1.022 1.662,1.022c0.883,0 1.315,-0.267 1.644,-1.022l2.667,-5.902v6.93h1.92v-7.258c0,-0.697 -0.277,-1.035 -0.849,-1.209c-1.367,-0.43 -2.285,-0.059 -2.7,0.872l-2.735,6.16l-2.649,-6.16c-0.398,-0.93 -1.332,-1.302 -2.7,-0.872c-0.572,0.174 -0.849,0.511 -0.849,1.208v7.258h0.002z"></path>
        <path d="M13.441,29.281h1.92v4.055c-0.015,0.2 0.064,0.731 0.99,0.745c0.472,0.008 2.821,0 2.85,0v-4.8h1.92c0.008,0 0,5.968 0,5.993c0.01,1.472 -1.828,1.662 -2.673,1.687h-5.006v-0.96c0.01,0 4.787,0.001 4.801,0c1.088,-0.115 0.959,-0.714 0.959,-0.896v-0.064h-3.012c-1.67,-0.015 -2.735,-0.751 -2.747,-1.59c-0.002,-0.078 0.036,-4.134 -0.002,-4.17z"></path>
        <path d="M22.081,35.041h4.807c0.63,0 1.242,-0.132 1.728,-0.36c0.81,-0.372 1.144,-0.875 1.144,-1.536v-1.368c0,-1.476 -1.83,-1.536 -2.88,-1.536h-1.92c-0.755,0 -0.87,-0.456 -0.96,-0.96v-0.96c0.09,-0.384 0.258,-0.9 0.923,-0.96c0.773,0 4.836,0 4.836,0v-0.96h-4.566c-0.755,0 -3.114,0.09 -3.114,1.92v1.187c0,0.84 0.738,1.524 2.34,1.692c0.18,0.012 0.36,0.024 0.539,0.024c0,0 1.866,-0.036 1.92,-0.024c1.08,0 0.96,0.84 0.96,0.96v0.96c0,0.132 -0.03,0.96 -0.971,0.96c-0.072,0 -4.789,0 -4.789,0v0.961z"></path>
        <path d="M40.32,33.08c0,1.159 0.655,1.809 2.392,1.939c0.162,0.011 0.325,0.021 0.488,0.021h4.8v-0.96h-4.435c-0.991,0 -1.325,-0.416 -1.325,-1.011v-6.669h-1.92z"></path>
        <path d="M30.704,33.121v-4.8c0,-1.02 0.5,-1.724 1.916,-1.92h0.672h3.447h0.525c1.416,0.196 2.08,0.899 2.08,1.92v4.782c0,0.827 -0.215,1.271 -0.916,1.559l1.488,1.338h-2.16l-1.07,-0.96h-1.257l-2.136,0.012c-0.309,0 -0.635,-0.043 -0.984,-0.126c-0.696,-0.161 -1.253,-0.666 -1.253,-1.627v-0.065c0.011,-0.915 0.855,-1.202 1.824,-1.318c0.07,-0.008 0.142,-0.014 0.214,-0.014h4.812v-0.96h-4.836c-0.683,0 -0.96,0.471 -0.96,0.84v1.92h0.841v0.062c0,0.202 -0.047,0.624 -0.896,0.825c-0.382,0.09 -0.963,0.129 -1.109,0.129h-1.392c-0.66,-0.189 -0.944,-0.504 -1.08,-0.825v-0.06h0.001v-4.84h-1.92v7.041h1.92v-1.92v0.002z"></path>
        <path d="M43.051,30.064c0.151,-0.256 0.347,-0.446 0.568,-0.601c0.448,-0.301 1.029,-0.353 1.569,-0.23c0.571,0.132 1.026,0.493 1.354,1.055l2.732,4.8h2.16l-4.057,-7.043h-0.037c-0.202,-0.306 -0.456,-0.566 -0.754,-0.773c-0.456,-0.323 -1.035,-0.447 -1.625,-0.345c-0.573,0.099 -1.037,0.422 -1.365,0.914l-4.566,7.247h2.16z"></path>
        <path d="M48.005,24.045c-1.416,0 -2.565,1.151 -2.565,2.567c0,1.417 1.149,2.566 2.565,2.566c1.417,0 2.566,-1.149 2.566,-2.566c0,-1.416 -1.149,-2.567 -2.566,-2.567zm0,4.8c-1.224,0 -2.222,-0.998 -2.222,-2.232c0,-1.233 0.998,-2.232 2.222,-2.232c1.234,0 2.232,0.999 2.232,2.232c0,1.234 -0.998,2.232 -2.232,2.232z"></path>
      </g>
    </g>
  </svg>
</div>

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
