# Automotive Industry Trends Analysis

## 📋 Executive Summary

This repository hosts an advanced data analytics project focused on the **Automotive Industry**. By leveraging a rich dataset of vehicle sales and specifications, this project utilizes complex **Structured Query Language (SQL)** scripts to unearth high-value insights regarding market trends, depreciation curves, fuel efficiency analytics, and pricing strategies.

The core objective is to demonstrate high-proficiency SQL capabilities—including Window Functions, Common Table Expressions (CTEs), and predictive modeling proxies—to derive actionable business intelligence from raw automotive data.

-----

## 🗂️ Data Architecture

The analysis is built upon a robust dataset containing granular details on vehicle transactions.

**File:** `Exploring Trends in the Automotive Industry.csv`

| Attribute | Data Type | Description |
| :--- | :--- | :--- |
| **Name** | `VARCHAR` | Make and model of the vehicle |
| **Year** | `INT` | Year of manufacture |
| **Selling\_Price** | `DECIMAL` | Transaction price of the vehicle |
| **Km\_Driven** | `INT` | Odometer reading at time of sale |
| **Fuel** | `VARCHAR` | Fuel propulsion type (Petrol/Diesel/CNG/Electric) |
| **Seller\_Type** | `VARCHAR` | Individual or Dealer |
| **Transmission** | `VARCHAR` | Manual or Automatic |
| **Owner** | `VARCHAR` | Ownership history (First, Second, etc.) |
| **Mileage** | `FLOAT` | Fuel efficiency (kmpl) |
| **Engine** | `INT` | Engine displacement (CC) |
| **Max\_Power** | `FLOAT` | Peak power output (bhp) |

-----

## 🧠 Advanced Analytical Framework

The project's logic is encapsulated in `Exploring Trends in the AutomotiveIndustry.sql`. The script moves beyond basic CRUD operations to perform sophisticated statistical analysis.

### [cite\_start]Key Analytical Modules[cite: 2]:

1.  **Multi-Dimensional Aggregation:**

      * Analysis of average selling prices segmented by transmission type, ownership status, and fuel category to determine market valuation baselines.

2.  **Performance Benchmarking:**

      * Identification of top-performing vehicle models based on average mileage, specifically filtering for high-capacity vehicles (seats \> 5) to target the family/utility segment.

3.  **Volatility & Variance Analysis:**

      * Utilization of `HAVING` clauses to isolate car models exhibiting extreme price volatility (Max vs. Min selling price differentials exceeding threshold values).

4.  **Market Quadrant Segmentation:**

      * Subquery-based filtering to identify "Premium Value" vehicles—those commanding above-average selling prices while maintaining below-average odometer readings.

5.  **Cumulative Growth Metrics (Window Functions):**

      * Implementation of `SUM() OVER (PARTITION BY ...)` to calculate the cumulative sales volume/revenue accumulation for specific models over chronological timeframes.

6.  **Price Sensitivity & Deviation:**

      * Statistical queries to detect models trading within a tight 10% margin of the population's average selling price.

7.  **Exponential Moving Average (EMA):**

      * *Advanced Technique:* Application of sliding window functions (`ROWS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW`) to calculate smoothing averages, essential for trend forecasting.

8.  **Year-over-Year (YoY) Depreciation:**

      * Usage of the `LAG()` analytical function to compare current year pricing against previous years, identifying specific models facing accelerated depreciation.

9.  **Category Dominance (CTEs):**

      * Common Table Expressions are used to rank and retrieve vehicles with the highest total mileage usage per transmission category, highlighting durability leaders.

10. **Top-Tier Performance Trends:**

      * Ranking algorithms (`RANK() OVER`) combined with CTEs to determine the longitudinal average pricing of the top 3 highest-grossing car models.

-----

## 🚀 Usage & Installation

1.  **Clone the Repository**

    ```bash
    git clone https://github.com/yourusername/Automotive-trends-analytics.git
    ```

2.  **Data Import**

      * Import `Exploring Trends in the Automotive Industry.csv` into your RDBMS (PostgreSQL, MySQL, SQL Server).
      * Ensure the table name matches `car_info` as referenced in the scripts.

3.  **Execution**

      * Run the scripts within `Exploring Trends in the AutomotiveIndustry.sql` sequentially to generate the analysis reports.

-----

## 🛠️ Technology Stack

  * **Database Engine:** SQL (Compatible with MySQL/PostgreSQL)
  * **Data Format:** CSV (Comma Separated Values)
  * **Concepts Applied:** OLAP, Data Warehousing, Statistical Analysis

## 🔮 Future Roadmap

  * **Visualization:** Integration with Tableau/PowerBI for dashboarding the SQL outputs.
  * **Predictive Modeling:** Python integration (Scikit-Learn) to predict future selling prices based on the SQL-derived features.
  * **ETL Pipeline:** Automating the ingestion of new sales data using Apache Airflow.
