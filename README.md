# Falcon-Sales
Sales Insights Dashboard – Business Insights Report

# Sales Insights Dashboard – Business Insights Report

## 1. Business Problem Statement

The sales organization was experiencing a decline in overall business performance, creating concerns among leadership regarding revenue growth and profitability. Decision-makers lacked a centralized reporting system and relied on multiple disconnected Excel files to analyze sales performance.

As a result:

* Business users spent significant time consolidating data from different sources.
* Reports were inconsistent across teams, leading to confusion and delays in decision-making.
* Management lacked visibility into key performance indicators such as revenue, sales quantity, profit, and profit margin.
* It was difficult to identify underperforming markets, products, and customer segments.

The Sales Director required a single, interactive dashboard capable of providing concise and actionable insights to answer critical business questions:

* What are the current sales, revenue, profit, and profit margin figures?
* Which markets are driving the highest revenue and profitability?
* Which products contribute the most to overall business performance?
* Which customer segments generate the highest revenue?
* What trends can be observed over time?

## 2. Project Overview

The objective of this project was to analyze sales performance across customers, markets, and product categories using Power BI and MySQL. The dashboard helps stakeholders monitor revenue trends, profitability, customer contribution, and market performance to support data-driven decision-making.

---

## 3. Tools & Technologies Used

* MySQL
* Power BI
* Power Query
* DAX

---

##  4. Data Architecture

The project follows a Star Schema data model for efficient reporting and analysis in Power BI.

### Fact Table
- **transactions**
  - Contains transactional sales data such as:
    - product_code
    - customer_code
    - market_code
    - order_date
    - sales_qty
    - sales_amount
    - cost_price
    - profit_margin
    - profit_margin_percent

### Dimension Tables

#### customers
Contains customer-related information:
- customer_code
- customer_name
- customer_type

#### products
Contains product-related information:
- product_code
- product_type

#### markets
Contains market and regional information:
- markets_code
- markets_name
- zone

#### date
Date dimension table used for time intelligence analysis:
- date
- year
- month_name
- quarter

### Relationships
- transactions[customer_code] → customers[customer_code]
- transactions[product_code] → products[product_code]
- transactions[market_code] → markets[markets_code]
- transactions[order_date] → date[date]

### Data Flow
MySQL Database → Power BI Power Query → Data Modeling → DAX Measures → Interactive Dashboard

---

## 5. Data Preparation & Cleaning

The following data preparation activities were performed:

* Removed duplicate transaction records
* Standardized currency values
* Handled missing product master records
* Added calculated fields:

  * Cost Price
  * Profit
  * Profit Margin %
* Created relationships between fact and dimension tables
* Built date table for time intelligence calculations

---

## 6. Key KPIs

| KPI                  | Value   |
| -------------------- | ------- |
| Total Revenue        | ₹985M   |
| Total Sales Quantity | 2M      |
| Total Profit         | ₹149.7M |
| Profit Margin %      | 15.2%   |

---

## 7. Key Business Insights

### Revenue Trends

* Revenue increased significantly in 2018.
* Revenue started declining after 2018 and continued downward through 2020.
* The trend indicates possible reduction in customer demand or market performance in recent years.

### Market Performance

* Delhi NCR contributes the highest revenue and sales volume.
* Mumbai and Nagpur are also strong-performing markets.
* Some smaller markets contribute low revenue and may require strategic evaluation.

### Product Analysis

* Own Brand products contribute the majority of total revenue.
* Distribution products contribute a smaller portion of revenue but still play an important supporting role.

### Customer Insights

* Revenue is concentrated among a few major customers.
* Heavy dependency on top customers may increase business risk if customer retention declines.

### Profitability Analysis

* Overall profit margin is approximately 15%.
* Certain markets generate high revenue but comparatively lower profit margins.
* This indicates potential issues such as high operational costs or aggressive discounting.

---

## 8. Recommendations

* Focus on improving revenue growth in declining years.
* Increase profitability in low-margin markets.
* Expand high-performing Own Brand product categories.
* Improve customer retention strategies for top customers.
* Investigate operational costs in low-profit regions.

---

## 9. Screenshots

<img width="1332" height="752" alt="image" src="https://github.com/user-attachments/assets/cfd7ffad-9196-4211-b61d-abe41d16f3f5" />

