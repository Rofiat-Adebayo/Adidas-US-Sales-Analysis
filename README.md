# 👟 Adidas US Sales Performance Dashboard — Power BI
Interactive Power BI dashboard analyzing Adidas US retail performance, uncovering product, region, and channel profitability insights.

## 📚 Table of Contents
- [Dataset](#dataset)
- [Overview](#overview)
- [Live Dashboard](#live-dashboard)
- [Objectives](#objectives)
- [Key Performance Indicators (KPIs)](#-key-performance-indicators-kpis)
- [Tools & Techniques](#-tools--techniques)
- [Key DAX Calculations](#-key-dax-calculations)
- [Product Performance Page](#product-performance-page)
- [Regional & Retailer Insights Page](#regional--retailer-insights-page)
- [Trend Analysis Page](#trend-analysis-page)
- [Key Insights](#key-insights)
- [Business Impact](#business-impact)
- [Conclusion](#-conclusion)
- [Recommendations](#-recommendations)
- [Acknowledgment](#acknowledgment)
- [Author](#author)
- [Project Type](#project-type)


## Dataset
Source(The dataset was provided during the Analytics Corpers Workshop bootcamp)
It contains transaction-level sales data for Adidas’ US operations with the following details:
- Retailer and Retailer ID
- Product information
- Sales Method (In-store, Online, Outlet)
- Location (State and Region)
- Sales, Operating Profit, Operating Margin, and Units Sold


## Overview
- This project provides a **comprehensive retail performance analysis** of Adidas’ US sales operations.  
- It focuses on **product mix, regional contribution, sales channels, and profitability trends** to uncover insights that guide marketing, supply chain, and pricing strategies.

---<img width="960" height="425" alt="Screenshot 4" src="https://github.com/user-attachments/assets/afff82ec-9143-4d4d-9915-8d8e44db8616" />
- Displays overall KPIs and interactive navigation buttons.
- Includes a regional map showing total sales across the US.

📌 Sets the tone for an interactive user experience.


## Live Dashboard
Explore the interactive version hosted on Microsoft Fabric:  
👉 [View Dashboard](https://app.fabric.microsoft.com/reportEmbed?reportId=00994adb-de07-47fa-97c6-77465ed13b7d&autoAuth=true&ctid=37d7521a-5079-48af-9131-4ac2cb6f1e3a)

---

##  Objectives
- Evaluate Adidas US sales performance across **regions, retailers, and product categories**  
- Assess **channel effectiveness** (In-store, Online, Outlet) in driving revenue  
- Identify **top-performing regions and retailers** to prioritize resource allocation  
- Analyze **profitability and operating margins** for cost efficiency  
- Build an **interactive Power BI dashboard** for real-time business monitoring  


## 📊 Key Performance Indicators (KPIs)

| KPI | Description |
|------|-------------|
| **Total Sales** | Overall revenue generated across all channels |
| **Total Profit** | Net operational profit after expenses |
| **Operating Margin %** | Efficiency ratio showing profit per dollar of sales |
| **Units Sold** | Product sales volume |
| **Average Price per Unit** | Revenue per item sold |
| **MoM Growth %** | Month-on-month change in sales and profit |
| **Top Retailers / Regions** | Performance ranking for partners and territories

## 🧰 Tools & Techniques

**Tools Used**
- Microsoft Power BI  
- Power Query (for data cleaning and transformation)  
- DAX (Data Analysis Expressions for calculated KPIs and measures)  
- Microsoft Fabric (for dashboard hosting and sharing)  
- Excel (for initial exploration and data verification)

**Techniques Applied**
- Data Cleaning and Preparation  
- Data Modeling (Star Schema)  
- DAX Measure Creation (Total Sales, MoM Growth, Operating Margin)  
- Exploratory Data Analysis (EDA)  
- Data Visualization and Dashboard Design  
- Business Performance Analysis and Storytelling


## 🧮 Key DAX Calculations
DAX
Total Sales = SUM('Data Sales Adidas'[Total Sales])

Total Profit = SUM('Data Sales Adidas'[Operating Profit])

Avg Operating Margin = AVERAGE('Data Sales Adidas'[Operating Margin])

Total Units Sold = SUM('Data Sales Adidas'[Units Sold])

Sales MoM % =
VAR PM= CALCULATE([Total Sales],DATEADD('Date'[Date],-1,MONTH))
VAR CM= CALCULATE([Total Sales])
RETURN
IF(AND(CM,PM),CM/PM-1) 

UnitsSold MoM % =
VAR PM= CALCULATE([Total Unit Sold],DATEADD('Date'[Date],-1,MONTH))
VAR CM= CALCULATE([Total Unit Sold])
RETURN
IF(AND(CM,PM),CM/PM-1)
Average Price =
DIVIDE([Total Sales], [Total Units Sold], 0)



## Product Performance Page
- Focuses on product-level sales and growth rates.
- Men’s Athletic Footwear dominates with 436K units sold and $153.7M in sales.
- Channel breakdown: In-store ($59M) · Outlet ($53M) · Online ($42M).

📌 Highlights product contribution and sales distribution.
<img width="551" height="333" alt="corper 2" src="https://github.com/user-attachments/assets/43fc6fd1-8bb2-48b4-a2b9-d4c0fa0c8918" />

## Regional & Retailer Insights Page
- Ranks top-performing regions and retailers.
- Top Retailers: West Gear ($14M), Kohl’s ($11M), Foot Locker ($10M).
- Top Regions: West ($16M) and Midwest ($12M).
- Map visualization reveals regional dominance and performance clusters.

📌 Supports decisions on resource allocation and territory performance.
<img width="614" height="328" alt="corper3" src="https://github.com/user-attachments/assets/edf0e0a6-edbd-4d03-8df3-8aa6fd40b585" />


## Trend Analysis Page
- Tracks monthly sales, profit, and margin trends.
- Total Sales: $899.9M | Profit: $332.1M | Units Sold: 2M.
- Stable 43% operating margin showing consistent cost efficiency.
- Visible seasonal peak from April–August with gradual year-end decline.

📌 Analyzes performance cycles and profitability trends.
<img width="960" height="540" alt="Screenshot 1" src="https://github.com/user-attachments/assets/8bafc0aa-3c50-4c33-9dc4-cb67e28b38f3" />

## 💡Key Insights

- Seasonal sales pattern: Peaks during April–August reflect strong mid-year demand.

- Footwear dominance: Men’s Street and Athletic lines contribute most to total sales.

- Channel mix: In-store remains the main revenue driver, while Online shows growing potential.

- Regional leaders: The West region leads revenue; Louisiana and Hawaii perform exceptionally.

- Profit stability: Consistent 43% margin demonstrates cost control and effective pricing.


## Business Impact
This analysis provides business leaders with:

- Clear visibility into regional and product-level performance.

- Insight into channel profitability to guide marketing and digital strategy.

- Data to optimize retailer partnerships and inventory distribution.

- A foundation for seasonal campaign planning and performance tracking.


 ## 💬 Conclusion

- The Adidas US Sales Analysis demonstrates how data-driven insight can enhance retail operations and profitability.

- Mid-year demand spikes present marketing and supply opportunities.

- In-store channels dominate but digital channels are rapidly scaling.

- Stable margins prove strong operational efficiency.

- Insight-led decision-making can further strengthen Adidas’ US market position.

📌 A well-balanced, performance-focused dashboard that supports strategic business growth.


## 💡 Recommendations

Based on the analysis, the following actions are recommended to improve Adidas’ US sales performance and profitability:

1. **Boost marketing and inventory efforts during mid-year (April–August)**  
   - Sales consistently peak in this period; increasing stock and promotions can maximize revenue.

2. **Strengthen digital sales channels (Online)**  
   - Online sales show steady growth; investing in e-commerce infrastructure and targeted campaigns will accelerate digital revenue.

3. **Optimize underperforming regions**  
   - Focus on training and resource allocation for weaker regions to balance overall performance.

4. **Leverage top-performing retailers**  
   - Strengthen partnerships with West Gear, Kohl’s, and Foot Locker through joint promotions and exclusive releases.

5. **Introduce dynamic pricing for low-margin products**  
   - Use data-driven pricing strategies to improve profit margins while maintaining competitiveness.

6. **Enhance demand forecasting and logistics planning**  
   - Use Power BI insights to align supply chain activities with seasonal and regional demand trends.

 *These recommendations aim to help Adidas sustain profitability, expand digital presence, and maintain operational efficiency across regions.*

---
## Acknowledgment

This project was completed as part of the Analytics Corpers Workshop program.
Special thanks to Extra Joseph, Fadero, Tina Okonkwo, and the facilitator team for their mentorship and hands-on Power BI guidance.


##  Author
**Rofiat Adebayo**  
Data Analyst | Power BI · SQL · Excel · DAX  
📧 [adebayorofiat004@gmail.com](mailto:adebayorofiat004@gmail.com)  
🔗 [LinkedIn – Rofiat Adebayo](https://linkedin.com/in/rofiat-adebayo)

---

##  Project Type
**Business Performance & Retail Operations Dashboard**  
*(Descriptive and Exploratory Data Analysis with KPI Monitoring)*
