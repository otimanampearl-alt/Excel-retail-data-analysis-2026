# Franova Retail Sales Analysis

## Project Overview

This project analyzes a retail sales dataset to demonstrate a practical data analytics workflow: data cleaning, exploratory analysis, KPI development, and business insight generation.

The original dataset contained **20,400 rows and 37 columns**. After removing **392 exact duplicate rows**, the cleaned dataset contains **20,008 rows**.

A public-safe version is provided for portfolio use. Direct customer contact information and employee names have been removed.

## Business Objective

The objective is to understand sales performance, customer/order behavior, regional performance, payment methods, returns, and data-quality issues that could affect business decisions.

## Data Cleaning

The following cleaning steps were performed:

- Removed exact duplicate records.
- Standardized order-status values, including `cancelled` → `Cancelled`.
- Standardized region values and removed accidental leading/trailing spaces.
- Standardized payment methods such as `Pos` → `POS` and transfer variants → `Bank Transfer`.
- Standardized return-status values into `Yes` and `No`.
- Converted dates into proper date formats.
- Converted numeric fields such as revenue, quantity, discount and unit price into numeric types.
- Recalculated delivery duration from order date and delivery date.
- Flagged records where delivery dates occur before order dates.
- Removed direct personal information from the public GitHub version.

## Key KPIs

| KPI | Result |
|---|---:|
| Total Revenue | ₦27,209,038,365 |
| Unique Orders | 19,442 |
| Average Order Value | ₦1,399,498 |
| Return Rate | 40.0% |
| Top Revenue Category | Electronics |
| Top Revenue Region | North |
| Top Payment Method by Revenue | Bank Transfer |
| Highest Revenue Month | September |

## Business Insights

### 1. Category Performance
**Electronics** generated the highest revenue at approximately **₦4,607,627,214**. Fashion was a close second.

**Business implication:** Management should protect availability and customer experience in the strongest categories while identifying the factors behind their performance.

### 2. Regional Performance
**North** generated the highest regional revenue at approximately **₦6,958,813,613**, while West recorded the lowest.

**Business implication:** The relatively close regional results suggest an opportunity to compare product mix, demand and sales execution rather than focusing only on revenue totals.

### 3. Return Rate
Approximately **40.0%** of records with a return-status value were marked as returned.

**Business implication:** Returns are a significant operational signal. The next analysis should break returns down by product, category, state and order status to identify the main drivers.

### 4. Payment Methods
**Bank Transfer** generated the most revenue at approximately **₦7,593,806,282**.

**Business implication:** The business should continue monitoring payment-method performance and customer adoption to identify opportunities to improve payment convenience and conversion.

### 5. Monthly Sales
**September** recorded the highest monthly revenue, while **November** recorded the lowest.

**Business implication:** These differences can support inventory, promotional and staffing decisions during stronger and weaker demand periods.

### 6. Data Quality
The raw dataset contained **392 exact duplicate rows**. There were also **5,657 records where the delivery date occurred before the order date**.

**Business implication:** Delivery-performance metrics should not be treated as fully reliable until the date anomalies are investigated and corrected at source.

## Tools

- Microsoft Excel
- PivotTables
- Data cleaning and standardization
- KPI analysis
- Exploratory data analysis
- Business insight generation

## Project Structure

```text
franova-retail-analysis/
├── README.md
├── data/
│   └── franova_retail_github_ready.xlsx
└── documentation/
    └── data_quality_and_business_insights.md
```

## Important Note

This repository contains a portfolio-safe version of the dataset. Personally identifiable customer information and employee names were removed before public sharing.

## Conclusion

The analysis shows that Franova's sales performance is spread across several strong categories and regions, while returns and data-quality issues require further investigation. The project demonstrates how data cleaning and exploratory analysis can be converted into practical business questions and recommendations.
