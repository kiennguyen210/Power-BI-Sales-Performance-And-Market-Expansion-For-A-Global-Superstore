# Sales Performance & Market Expansion For A Global Superstore | Power BI

<img width="992" height="649" alt="image" src="https://github.com/user-attachments/assets/db90a366-25ae-4606-a189-488632f718c3" />

*How to understand current market position and growth opportunities for market expansion by using Power BI?*

---

**Author:** Nguyễn Duy Kiên

**Date:** October 2025

**Tools Used:** Power BI

---

## 📑 Table of Contents  
1. [📌 Background & Overview](#1--background--overview)  
2. [📂 Dataset Description & Data Structure](#2--dataset-description--data-structure)  
3. [🧠 Design Thinking Process](#3--design-thinking-process)  
4. [📊 Key Insights & Visualizations](#4--key-insights--visualizations)  
5. [🔎 Final Conclusion & Recommendations](#5--final-conclusion--recommendations)

---

## 1. 📌 Background & Overview

### 1.1. Objective

This project is centered on creating a dynamic business intelligence dashboard to help Superstore, a rapidly growing global retailer, understand its current market position and growth opportunities for market expansion.

### 1.2. Business Problem

The Business Problem: Superstore aims to significantly boost revenue and expand its market footprint across different continents. To achieve this effectively, the Senior Manager needs clear, data-driven insights to answer three core questions:

✔️ What is the overall financial health and growth momentum of the company?

✔️ Which global markets/countries should we prioritize for investment and expansion?

✔️ Which product groups should be selected as strategic products to maximize future profit and support market entry?

### 1.3. Why is this important?

By transforming complex global sales data (Revenue, Profit, Trends) into actionable visual insights, this dashboard ensures that critical decisions on budget allocation, expansion strategy, and inventory focus are based on objective performance metrics, directly driving success and market penetration.

### 1.4. Who is this project for?

👤 Senior Manager: The primary user, responsible for setting overall business direction, approving market expansion budgets, and determining the company's long-term product strategy.

👤 Business Development Team: Uses the dashboard to monitor the performance of target markets, assess the potential of new regions, and align sales efforts with the company's strategic product priorities.

👤 Sales and Marketing Leadership: Utilizes the dashboard to understand profit drivers, identify high-growth segments, and allocate marketing spend effectively to support profitable products and markets.

## 2. 📂 Dataset Description & Data Structure

### 2.1. Data Source  
- Source: Source: Kaggle
- Size: The Orders table contains 51,290 records.
- Format: CSV

### 2.2. Data Structure & Relationships 

#### 1️⃣ Tables Used:  

The dataset consists of three tables:

**🛒 Orders – Contains detailed transaction and customer information (51,290 records).**

<details>
  <summary>
    Table 1: Orders (Click to expand)
  </summary>
  
| Column Name   | Data Type | Description                                          |
|---------------|-----------|------------------------------------------------------|
| Order ID      | VARCHAR   | Unique identifier for each order.                    |
| Order Date    | DATE      | Date when the order was placed.                      |
| Ship Date     | DATE      | Date when the order was shipped.                     |
| Ship Mode     | VARCHAR   | Shipping method used for delivery.                   |
| Customer ID   | VARCHAR   | Unique identifier for each customer.                 |
| Customer Name | VARCHAR   | Full name of the customer.                           |
| Segment       | VARCHAR   | Customer segment (e.g., Consumer, Corporate).        |
| City          | VARCHAR   | City where the order was placed.                     |
| State         | VARCHAR   | State where the order was placed.                    |
| Country       | VARCHAR   | Country where the order was placed.                  |
| Postal Code   | VARCHAR   | Postal code of the shipping address.                 |
| Market        | VARCHAR   | Market region (e.g., APAC, EMEA).                    |
| Region        | VARCHAR   | Geographical region of the order.                    |
| Product ID    | VARCHAR   | Unique identifier for each product.                  |
| Category      | VARCHAR   | Product category (e.g., Furniture, Office Supplies). |
| Sub-Category  | VARCHAR   | Sub-category of the product.                         |
| Product Name  | VARCHAR   | Name of the product ordered.                         |
| Sales         | DECIMAL   | Revenue generated from the order.                    |
| Quantity      | INT       | Number of items ordered.                             |
| Profit        | DECIMAL   | Profit earned from the order.                        |

</details>

**🔄 Returns – Stores data on returned orders.**

<details>
  <summary>
    Table 2: Returns (Click to expand)
  </summary>
  
| Column Name | Data Type | Description                                                     |
|-------------|-----------|-----------------------------------------------------------------|
| Returned    | VARCHAR   | Indicates whether the order was returned (e.g., 'Yes' or 'No'). |
| Order ID    | VARCHAR   | Unique identifier for each order.                               |

</details>

**👥 People – Holds information about sales representatives.**

<details>
  <summary>
    Table 3: People (Click to expand)
  </summary>
  
| Column Name | Data Type | Description                                       |
|-------------|-----------|---------------------------------------------------|
| Person      | VARCHAR   | Name of the salesperson.                          |
| Region      | VARCHAR   | Geographic region where the salesperson operates. |

</details>

#### 3️⃣ Data Relationships

<img width="1942" height="1189" alt="image" src="https://github.com/user-attachments/assets/9a5df353-e503-4738-8df5-7aa80d93c37b" />

## 3. 🧠 Design Thinking Process

### 3.1. Empathize  

<img width="1920" height="1080" alt="pic 1 1" src="https://github.com/user-attachments/assets/c95ce6ec-98a8-4349-8975-1bbfcef2985e" />

### 3.2. Define point of view  

<img width="1920" height="1080" alt="pic 1 2" src="https://github.com/user-attachments/assets/5e8afb6c-0b78-4d47-8713-689bf752cc33" />

### 3.3. Ideate 

<img width="1920" height="1080" alt="pic 1 3" src="https://github.com/user-attachments/assets/13cda2c1-8100-42bb-b394-32d4614f05bf" />

## 4. 📊 Key Insights & Visualizations

### 4.1. Overview

<img width="13195" height="7508" alt="Final_Page_1" src="https://github.com/user-attachments/assets/cf4d62bc-6d64-4d44-87c4-3676f6744f10" />

This page confirms strong scale growth but highlights an efficiency challenge.

| Metric        | Value (2014) | YoY% Trend | Strategic Insight                                                                                                                                                                         |
|---------------|--------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Total Revenue | $4.30M       | 26.26%     | Excellent Scale Growth: High revenue growth confirms successful market penetration and expansion efforts.                                                                                 |
| Total Profit  | $504.16K     | 23.90%     | Healthy Absolute Profit: Profit growth closely tracks revenue, indicating that the expansion is financially sound.                                                                        |
| Profit Margin | 11.73%       | -1.86%     | CRITICAL ALERT: Efficiency Erosion. The decreasing Margin Trend (cost growth exceeding sales growth) requires immediate investigation into operational costs and/or discounting strategy. |

**🔎 Detailed Insights**

- Growth Markets (Scale + Momentum): The Top 5 Countries table reveals crucial targets:

  - India (Rank #2): Shows extraordinary growth momentum at 48.4%, making it the highest priority market for expansion investment to capitalize on this trend.

  - Germany (Rank #5): Follows closely with robust growth at 33.4%.

- Segment Profitability: The Home Office (46.1%) segment is the strongest profit driver by far, followed by Consumer (23.6%) and Corporate (11.5%).

  - Action: This confirms a successful strategy in supporting remote work/small businesses. Future marketing efforts should leverage this success.

- Operational Efficiency: The Profit Trend by Ship Mode shows Standard Class (+1.6%) has the lowest growth.

  - Action: This mode may be disproportionately incurring hidden costs or servicing low-margin orders, directly contributing to the negative Profit Margin trend.

### 4.2. Market

<img width="13195" height="7508" alt="Final_Page_2" src="https://github.com/user-attachments/assets/f488e775-2b04-47b6-8e7e-77a68a8626d1" />

This page provides the roadmap for expansion and resource allocation.

**🔎 Detailed Insights**

- Strategic Growth Matrix (Distribution Profit by Market):

  - APAC (Highest Profit Scale): This region is the current profit pillar (Cash Cow) and requires optimization for efficiency to protect the Margin.

  - LATAM, Africa, EMEA: These regions are likely the Rising Stars/Frontier Markets with lower absolute profit but high growth potential (if the X-axis represents YoY Growth).

  - Action: Allocate expansion budgets to LATAM, Africa, and EMEA to capture future scale, while implementing profit-protection measures in APAC/EU.

- Profit Decomposition (Segment & Category):

  - Profit in the EU is diversified across Technology and Office Supplies.

  - Profit in the US is heavily concentrated in Furniture.

  - Action: Product strategy must be localized. For instance, push Technology products strongly in the EU but focus heavily on the Furniture supply chain and market share in the US.

- Distribution Profit by Customer: The scatter plot visually identifies a large concentration of customers in the Red Area (Low Profit).

  - Action: This indicates widespread discounting or poor pricing for a majority of customers. This customer base is the likely culprit behind the -1.86% Profit Margin and must be reviewed immediately.

### 4.3. Product

<img width="13195" height="7508" alt="Final_Page_3" src="https://github.com/user-attachments/assets/b02d9b4d-c838-45d2-b38c-b7a8f88161e8" />

This page defines the strategic product portfolio for focused investment.

**🔎 Detailed Insights**

- Profit Pillars (Sub-Category Scale):

  - Copiers (20.64%) and Phones (14.02%) are the highest absolute profit contributors, confirming Technology as the indispensable core category.

  - Action: All resource priority (Inventory, R&D, Marketing) must be directed toward maintaining leadership in these two sub-categories.

- Strategic Products (Top 15 Ranking):

  - High Scale + High Momentum: Canon imageCLASS 220 (Ranked #1 by Current Profit) shows outstanding growth at +64.7%.

    - Action: This product represents the ideal strategic asset—high scale today, high momentum for tomorrow. Push aggressively into high-growth markets like India.

  - High Scale + Risk: Motorola Smart Phone (Ranked #3) shows a sharp negative trend of -16.2%.

    - Action: Immediate "deep dive" investigation is needed to determine if this is due to cost increases, aggressive competitor pricing, or excessive internal discounting. This product is a significant drag on future profit.

- Profit Distribution (Profit vs. Revenue):

  - The density of products in the Red Area (low profit/low revenue) is significant.

  - Action: Products in the Red Area must be reviewed for potential discontinuation or re-pricing to instantly boost the overall Profit Margin. They are tying up inventory and capital with little return.
 
  ## 5. 🔎 Final Conclusion & Recommendations

### 5.1. Final Conclusion

| Metric        | Value (2014) | YoY% Trend | Conclusion                                                                                                                   |
|---------------|--------------|------------|------------------------------------------------------------------------------------------------------------------------------|
| Total Revenue | $4.30M       | 26.26%     | Strong Momentum: The company successfully achieved high scale growth, confirming its development phase.                      |
| Total Profit  | $504.16K     | 23.90%     | Healthy Absolute Profit: Growth is sustainable and closely tracks revenue.                                                   |
| Profit Margin | 11.73%       | -1.86%     | KEY CHALLENGE: Profitability efficiency is eroding. This is the main priority for cost control and discount strategy review. |

### 5.2. Recommendations

**🎯 1. Target Markets for Expansion**

The decision is based on identifying markets with a high combination of Profit Scale (Current Profit Rank) and Growth Momentum (YoY% Trend), derived from the Overview and Market pages.

| Market/Country    | Current Profit Rank           | YoY% Trend               | Strategic Role                         | Recommendation                                                                                                                           |
|-------------------|-------------------------------|--------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| India             | #2 (High Scale)               | 48.4% (Highest Growth)   | Primary Expansion Target / Rising Star | Immediately allocate the largest share of the new expansion budget (Marketing/Sales) to India to capitalize on its exceptional momentum. |
| Germany           | #5 (Good Scale)               | 33.4% (Very High Growth) | Secondary Expansion Target             | Invest resources to push growth and stabilize its position in the top tier, following the India model.                                   |
| APAC Region       | #1 by Region (Highest Profit) | N/A                      | Profit Pillar / Optimization Focus     | Implement strict cost control measures and optimize operations here to protect the overall company Profit Margin (11.73%).               |
| LATAM/EMEA/Africa | Low Scale                     | High Growth (Implied)    | Frontier Markets / Pilot Investment    | Deploy small, focused pilot projects to assess sales models before large-scale investment.                                               |

**🚀 2. Strategic Product Portfolio**

The decision is based on identifying products with high Profit Contribution and strong YoY% Growth from the Product page.

| Product/Category     | Contribution / Trend              | Strategic Role                     | Recommendation                                                                                                                                                                    |
|----------------------|-----------------------------------|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Technology Category  | Copiers (20.64%), Phones (14.02%) | Core Profit Pillar                 | Defend the Core: Ensure guaranteed inventory supply and prioritize R&D/Marketing to maintain dominance in these high-value categories.                                            |
| Canon imageCLASS 220 | Ranked #1 Profit, +64.7% Trend    | Flagship Product / Strategic Asset | Aggressive Push: Feature this product heavily in marketing campaigns directed at high-growth markets (India, Germany). Use it as a key offering for market entry.                 |
| Motorola Smart Phone | Ranked #3 Profit, -16.2% Trend    | High-Risk Product                  | Urgent Review: Immediate investigation into its negative trend (pricing, discounting, or cost issues). Prepare a plan for replacement or restructuring to prevent profit erosion. |

**📈 3. Efficiency Improvement & Risk Mitigation**

- Action on Margin: The highest priority is investigating the -1.86% Profit Margin trend. This is driven by either excessive discounting (needs review via Distribution Profit by Customer) or high operational costs (needs review via Standard Ship Mode performance).

- Customer Optimization: Use the Distribution Profit by Customer chart to identify high-revenue customers who are currently low-profit, and adjust pricing/discounting policies to convert them into higher-margin accounts.
