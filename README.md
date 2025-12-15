# advanced-sql-data-analysis
Advanced SQL data analysis project using SQL Server
# Advanced SQL Data Analysis Project

## 🚀 Project Overview

This project showcases advanced SQL data analysis techniques applied to a structured sales database.
It focuses on exploratory analysis, performance evaluation, segmentation, and advanced analytical patterns
to extract meaningful business insights.

The project is designed as a **portfolio-level Advanced SQL project**, demonstrating strong analytical thinking
and real-world SQL use cases.

---

## 🗂 Project Structure

The analysis is organized into modular SQL scripts, each focusing on a specific analytical concept:

sql-scripts/
│
├── 00_init_database.sql
├── 01_database_exploration.sql
├── 02_dimensions_exploration.sql
├── 03_date_range_exploration.sql
├── 04_measures_exploration.sql
├── 05_magnitude_analysis.sql
├── 06_ranking_analysis.sql
├── 07_change_over_time_analysis.sql
├── 08_cumulative_analysis.sql
├── 09_performance_analysis.sql
├── 10_data_segmentation.sql
├── 11_part_to_whole_analysis.sql
├── 12_report_customers.sql
└── 13_report_products.sql

markdown
Copy code

---

## 🛠 Technologies Used

- SQL Server (T-SQL)
- Advanced SQL querying techniques
- Git & GitHub for version control

---

## 🔍 Analysis Breakdown

### 🧱 00. Database Initialization

- Database setup and preparation
- Ensuring clean execution environment

### 🔎 01–02. Data & Dimensions Exploration

- Understanding database structure
- Exploring fact and dimension tables
- Validating relationships and data integrity

### 📅 03. Date Range Analysis

- Identifying available date ranges
- Analyzing data coverage across time
- Supporting time-based trend analysis

### 📐 04. Measures Exploration

- Examining key metrics (sales, quantities, revenue)
- Identifying distributions and outliers

### 📊 05. Magnitude Analysis

- Measuring totals and aggregates
- Comparing volumes across categories and dimensions

### 🏆 06. Ranking Analysis

- Ranking products and categories
- Using window functions (RANK, DENSE_RANK, ROW_NUMBER)
- Identifying top and bottom performers

### 📈 07. Change Over Time Analysis

- Year-over-Year and Month-over-Month comparisons
- Trend detection using date functions
- Growth and decline analysis

### 📉 08. Cumulative Analysis

- Running totals and cumulative metrics
- Business performance tracking over time
- Window functions with cumulative frames

### ⚙️ 09. Performance Analysis

- Performance benchmarking
- Comparing entities against averages and targets
- Identifying high and low efficiency segments

### 🧩 10. Data Segmentation

- Segmenting customers and products
- Behavioral and value-based segmentation
- Supporting targeted business decisions

### 🧮 11. Part-to-Whole Analysis

- Contribution analysis
- Percentage of total calculations
- Category and product share evaluation

### 📑 12–13. Business Reports

- Customer-level analytical report
- Product-level analytical report
- Queries designed for direct business consumption

---

## 🧠 Advanced SQL Concepts Demonstrated

- Common Table Expressions (CTEs)
- Window Functions
- Aggregation & Grouping
- Subqueries
- Time Series Analysis
- Part-to-Whole Calculations
- Analytical Reporting Queries

---

## 📊 Sample Advanced Query

```sql
WITH category_sales AS (
    SELECT
        category,
        SUM(sales_amount) AS total_sales
    FROM fact_sales f
    JOIN dim_products p
        ON f.product_key = p.product_key
    GROUP BY category
)
SELECT
    category,
    total_sales,
    ROUND(
        total_sales * 100.0 / SUM(total_sales) OVER (),
        2
    ) AS contribution_percentage
FROM category_sales;
🎯 Project Level
Advanced SQL Data Analysis Project

This project is suitable for:

Data Analyst roles

Business Intelligence roles

SQL-heavy analytics positions

👤 Author
Mohamed_Asaad
SQL & Data Analysis Enthusiast

📌 GitHub Portfolio Project
```
