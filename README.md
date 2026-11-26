# TechNova-Gadget-Sales-Performance-Revenue-Leakage-Analysis
# TechNova Gadgets | Sales Performance & Revenue Leakage Analysis

## Project Overview

TechNova Gadgets is a Nigerian technology and gadget retailer selling smartphones, laptops, tablets, audio devices, smartwatches, chargers, power banks, cables, and computer accessories.

The company operates through four sales channels: Physical Store, Website, WhatsApp, and Social Media, serving customers across Nigeria's six geopolitical zones.

This project analyses 12 months of transaction-level sales data to evaluate business performance, identify revenue leakage, assess discount effectiveness, and uncover operational weaknesses affecting sales fulfilment.

The primary business question was:

**Where is TechNova Gadgets losing the most potential revenue through cancelled orders, and what actions can management take to reduce these losses?**

Additional areas of investigation included:

- Discount effectiveness and profit margin impact.
- Product and regional sales performance.
- Sales channel efficiency.
- Returned sales and revenue impact.
- Customer segment value.
- Product performance.
- Pending orders.
- Revenue versus profit analysis.

## Dataset Overview

The analysis was conducted using a transaction-line-level dataset covering **1 September 2025 to 31 August 2026**.

Key dataset characteristics:

- One row represents an individual product within an order, rather than an entire order.
- Order IDs appear across multiple rows. Distinct count was therefore used to calculate the actual number of orders.
- Sales transactions cover four sales channels.
- Products span 10 technology categories.
- Customers are distributed across Nigeria's six geopolitical zones.
- All monetary values are denominated in Nigerian Naira (NGN).
- A data dictionary was included in the Excel workbook.

The dataset contained some data quality issues, including missing Customer Segment, City, and Payment Method values, as well as inconsistent city spellings and spacing.

## Data Cleaning and Preparation

Data cleaning and transformation were performed using **Power Query**.

Key activities included:

- Handling missing values using the modal value for the affected columns.
- Standardising inconsistent city names and removing unnecessary spaces.
- Assigning appropriate data types to columns.
- Extracting year and month from the Order Date.
- Validating the cleaned dataset before loading it into the Data Model.

## Data Modelling and Analysis

After cleaning, the dataset was loaded into Excel's Data Model to support relationships, calculations, and interactive reporting.

The following activities were performed:

- Created a Calendar Table using Power Pivot.
- Established a relationship between the Calendar Table and the sales dataset using Order Date.
- Arranged months chronologically for accurate time-based analysis.
- Created DAX measures for key performance indicators.
- Used Pivot Tables to summarise and analyse business performance.
- Created dynamic dashboard subheadings using INDEX, MATCH, MAX, and MIN functions.
- Connected dashboard charts to Pivot Tables and configured interactive slicers.

### Key Performance Indicators (KPIs)

The following measures were developed:

- Total Revenue
- Lost Revenue
- Returned Revenue
- Total Lost Profit
- Total Discount Amount
- Total Customers
- Total Orders
- Cancelled Orders
- Returned Orders
- Average Order Value (AOV)
- Total Units Sold
- Total Product Categories
- Total Products
- Total States
- Total Cities
- Cancellation Rate
- Returned Rate

## Interactive Dashboards

The project contains four interactive dashboards.

### 1. Sales Performance Dashboard

![Sales Performance Dashboard](images/sales-performance-dashboard.png)

**Key Findings**

- iPhones generated the highest product profit of ₦441,215,500.
- Osogbo recorded the highest city-level revenue among the leading five cities, generating ₦437,124,850.
- Oyo State recorded the highest revenue among the five leading states, generating ₦437,627,450.
- The South-West geopolitical zone generated the highest regional revenue and profit, at ₦2,608,652,950 and ₦571,432,950, respectively.
- Individual customers contributed the highest revenue and profit among customer segments, generating ₦3,032,257,150 and ₦671,548,150, respectively.

### 2. Discount and Profit Margin Dashboard

![Discount and Profit Margin Dashboard](images/discount-profit-margin-dashboard.png)

**Key Findings**

- Higher discount tiers generally corresponded with lower net profit and revenue across the analysed items.
- Social Media transactions at the 25% discount tier recorded the highest profit margin of 4.80%.

### 3. Revenue Leakage Dashboard

![Revenue Leakage Dashboard](images/revenue-leakage-dashboard.png)

**Key Findings**

**Product-Level Revenue Leakage**

- Smartphones were the largest contributor to lost potential revenue, accounting for ₦203,944,450 across 231 cancelled line items.
- Laptops ranked second, contributing ₦58,053,700 across 42 cancelled line items.
- Smartphones, Laptops, Tablets, and Audio Devices collectively accounted for 95.4% of lost potential revenue.

**Regional Revenue Leakage**

- The South-West accounted for ₦109,773,300 (34.42%) in lost potential revenue across 83 cancelled orders.
- North Central followed with ₦59,625,350 across 44 cancelled orders.
- South-East and South-South accounted for ₦50,393,100 and ₦44,160,300, respectively.
- North-East and North-West recorded the lowest absolute revenue leakage.

**Sales Channel Revenue Leakage**

- Physical Stores accounted for ₦151,896,500 (48%) in lost revenue across 106 cancelled orders.
- The Website contributed ₦84,707,150 (26.56%) across 62 cancelled orders.
- Social Media and WhatsApp contributed ₦46,049,400 and ₦36,300,050, respectively.

**Temporal Trends**

- Revenue leakage peaked in May 2026 (₦41,852,850), February 2026 (₦35,250,250), and September 2025 (₦34,005,300).
- December 2025 recorded the lowest lost revenue at ₦14,267,800 across 13 cancelled orders.

### 4. Returned Sales Dashboard

![Returned Sales Dashboard](images/returned-sales-dashboard.png)

This dashboard examines returned orders and their financial implications, including returned revenue, unrealised profit, and return patterns across the business.

## Executive Summary

Between September 2025 and August 2026, TechNova Gadgets generated:

| Performance Metric | Value |
|---|---:|
| Gross Sales Revenue | ₦7,020,681,400 |
| Total Profit | ₦1,554,557,400 |
| Total Discount | ₦439,772,600 |
| Unique Orders | 5,659 |
| Customers | 1,186 |
| Units Sold | 12,173 |
| Product Categories | 10 |
| Products | 37 |
| States | 37 |
| Cities | 44 |

However, cancelled and returned orders resulted in substantial financial losses.

| Revenue Leakage Metric | Value |
|---|---:|
| Lost Potential Revenue from Cancelled Orders | ₦318,953,100 |
| Unrealised Profit from Cancelled Orders | ₦69,211,100 |
| Cancelled Orders | 246 |
| Cancellation Rate | 4.35% |
| Returned Potential Revenue | ₦181,514,700 |
| Unrealised Profit from Returned Orders | ₦41,266,700 |
| Returned Orders | 135 |
| Return Rate | 2.39% |

The analysis revealed that revenue leakage was concentrated in high-value technology products and major sales channels. Smartphones accounted for 63.9% of lost revenue, while Physical Store and Website transactions collectively contributed 74.2% of total revenue leakage.

## Business Recommendations

Based on the findings, the following recommendations were proposed:

### 1. Reduce High-Value Smartphone and Laptop Order Cancellations

- Introduce a 5–10% commitment deposit for high-value pre-orders exceeding ₦500,000.
- Implement real-time stock reservations across Website, WhatsApp, and Physical Store inventory systems.
- Improve order confirmation and payment processes for high-value products.

### 2. Improve Physical Store Operations

- Introduce dual-SIM POS terminals and alternative offline payment solutions to reduce transaction failures.
- Establish express Click-and-Collect counters to reduce waiting times for customers collecting reserved products.

### 3. Improve WhatsApp and Social Media Sales Processes

- Replace manual bank account sharing with automated payment links.
- Introduce a short price-lock window to encourage prompt payment.
- Provide upfront delivery fee estimates to reduce cancellations caused by unexpected logistics costs.

### 4. Optimise Regional Inventory and Fulfilment

- Prioritise inventory buffers in South-West distribution hubs.
- Improve stock availability and delivery capacity in regions with high-value cancelled orders.

## Tools and Technologies

- **Microsoft Excel:** Data analysis, Pivot Tables, advanced formulas, and dashboard development.
- **Power Query:** Data cleaning and transformation.
- **Power Pivot:** Data modelling and relationship management.
- **DAX:** KPI and business performance calculations.
- **VBA:** Dashboard navigation macros and dynamic insight text boxes.
- **Excel Slicers:** Interactive filtering and dashboard exploration.

## Project Outcome

The project transformed raw transaction-level sales data into an interactive business intelligence solution that identifies sales trends, evaluates profitability, measures revenue leakage, and provides actionable recommendations.

It demonstrates practical skills in data cleaning, data modelling, analytical reporting, KPI development, dashboard design, and business-oriented data storytelling.
