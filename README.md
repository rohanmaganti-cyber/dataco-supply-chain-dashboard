# Supply Chain Executive Dashboard & SQL Analytics

![Dashboard Preview](assets/dashboard_preview.png)

## Executive Summary
This project transforms raw supply chain data (~180,519 records) into an interactive Power BI executive dashboard driven by PostgreSQL views. The primary objective was to identify fulfillment bottlenecks and quantify profit leakage across global supply operations.

## Key Insights & Business Impact
* **Total Operations Scope:** Tracked **$36.78M** in total revenue and **$3.97M** in net profit.
* **Fulfillment Failure Rate:** Identified an overall late delivery rate of **54.83%**. **First Class** shipments experienced the highest delay variance, missing scheduled windows by an average of **1.6 days**.
* **Profit Leakage Drivers:** Product categories such as **Cleats** and **Men's Footwear** generated high revenue volume but carried disproportionately high rates of loss-making individual orders.

## Tech Stack & Architecture
* **Database:** PostgreSQL (UTF8/WIN1252 data ingestion, schema validation)
* **Transformation & Aggregation:** SQL Views (`view_shipping_performance`, `view_category_profitability`, `view_delivery_delays`)
* **Business Intelligence:** Power BI Desktop (DAX measures, interactive slicers, cross-filtering)

## Data Pipeline Steps
1. Ingested raw supply chain dataset into PostgreSQL.
2. Built custom SQL views to compute pre-aggregated summary statistics directly on the database engine for optimal Power BI performance.
3. Connected Power BI directly to PostgreSQL using optimized import modes.
4. Engineered custom DAX measures for core KPIs (`Total Revenue`, `Total Profit`, `Late Delivery Rate %`).
5. Designed executive layout with dynamic region slicers and conditional visual formatting.
