# Zomato Global Restaurant Insights — Power BI Dashboard

An interactive, corporate-grade Business Intelligence solution built using **Power BI** to analyze Zomato's global restaurant footprint. This dashboard ingests raw restaurant profiles, geographical metrics, operational characteristics, and customer rating distributions to deliver comprehensive market-gap analysis and commercial insights for restaurant consulting and investment strategies.

---

## 📌 Business Case & Core Problems Solved
The food and beverage market is highly volatile, with profitability heavily reliant on demographic alignment and feature integrations. This dashboard serves as a strategic decision tool to:
* **Identify Global Sweet Spots:** Analyze pricing models across different countries and currencies (`USD`, `INR`, `AED`, etc.) to find lucrative market opportunities.
* **Feature Optimization:** Measure the performance lift in engagement and ratings for restaurants that provide *Online Delivery* or *Table Booking* services against those that do not.
* **Cuisine Saturation Mapping:** Pinpoint which cuisines (`Italian`, `Mughlai`, `Continental`, etc.) hold strong consumer sentiment (`Rating Text` and `Aggregate Rating`) within specific cities.

---

## 🛠️ Technical Implementation & Power BI Features

### 1. Data Transformation & ETL (Power Query)
* **Unstructured Text Parsing:** Handled high-cardinality multi-valued fields within the `Cuisines` column by implementing string splitting and unpivoting to establish clean categories.
* **Normalization & Schema Design:** Sanitized missing entries in cost values, aligned complex rating scales, and organized data with structural filtering to optimize calculations.
* **Geographical Grouping:** Organized messy address strings into clean hierarchical tiers (`Country` ➡️ `City` ➡️ `Locality`) for robust geospatial analysis.

### 2. Data Modeling & DAX Measures
Structured a high-performance data model using optimized explicit **DAX (Data Analysis Expressions)** to dynamicize calculations across visual visuals:
* **Weighted Market Rating:** `Average Rating = AVERAGE(ZomatoData[Aggregate Rating])`
* **Engagement Volumetrics:** `Total Interactions = SUM(ZomatoData[Votes])`
* Created calculated segments for `Price Range` (`1` to `4`) to cluster restaurants by pricing tiers instead of arbitrary cost ranges.

### 3. Visualizations & Interactivity
* **Executive Summary:** High-impact KPI cards representing active restaurants, average ratings, and market reach.
* **Geospatial Intelligence:** Maps filtering performance across international regions using localized currency metrics.
* **Feature Deep-Dive:** Comparative matrix grids showing the cross-correlation of `Has Online Delivery` and `Has Table Booking` with final customer loyalty parameters (`Rating Text`).

---

## 📈 Key Market Insights Delivered
1. **The Operational Lift:** Across majority locations, restaurants featuring **Online Delivery** and **Table Booking** show a dramatic **20-30% increase in aggregate user ratings** and customer feedback density.
2. **Value vs. Luxury Paradox:** Data trends confirm that higher `Price Range` tiers do not automatically yield a "Excellent" or "Very Good" rating. Mid-tier restaurants (`Price Range 2 & 3`) consistently hold high volume stability and positive customer satisfaction.
3. **Rating Discrepancies:** Identified market clusters where high voting activity is linked with "Average" text reviews, indicating severe service/delivery gaps despite strong initial consumer interest.

---
