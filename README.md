# 📊 Data Warehouse Analytics SQL Project
A comprehensive collection of SQL scripts for data exploration, analytics, and reporting. These scripts cover various analyses such as database exploration, measures and metrics, time-based trends, cumulative analytics, segmentation, and more.
This repository contains SQL queries designed to help data analysts and BI professionals quickly explore, segment, and analyze data within a relational database. Each script focuses on a specific analytical theme and demonstrates best practices for SQL queries.

---

## 🚀 Getting Started

### ⚠️ Prerequisites

- **SQL Server** (with BULK INSERT access)
- Access to the **`master`** database
- CSV files stored


---

## 🛠️ Setup Instructions

> ⚠️ **WARNING:** Running the initialization script will **DROP** the existing `DataWarehouseAnalytics` database if it exists.

Run the following script first:


This script:
- Creates a new database: `DataWarehouseAnalytics`
- Defines the `gold` schema
- Creates and loads data into:
  - `gold.dim_customers`
  - `gold.dim_products`
  - `gold.fact_sales`

---

## 📁 Script Overview

| Script | Description |
|--------|-------------|
| `00_init_database.sql` | Initializes and loads the data warehouse |
| `01_database_exploration.sql` | Explore schema and table metadata |
| `02_dimensions_exploration.sql` | Analyze dimension tables (countries, categories, etc.) |
| `03_date_range_exploration.sql` | Analyze data timelines and date ranges |
| `04_measures_exploration.sql` | Compute key KPIs like sales, orders, and averages |
| `05_magnitude_analysis.sql` | Group totals by dimensions like country, gender, etc. |
| `06_ranking_analysis.sql` | Rank top/bottom products and customers |
| `07_change_over_time_analysis.sql` | Analyze sales over time (monthly trends) |
| `08_cumulative_analysis.sql` | Track running totals and moving averages |
| `09_performance_analysis.sql` | Year-over-year and average performance comparisons |
| `10_data_segmentation.sql` | Segment customers and products |
| `11_part_to_whole_analysis.sql` | Contribution of parts to total sales |
| `12_report_customers.sql` | Create customer-level summary report view |
| `13_report_products.sql` | Create product-level summary report view |

---

## 🗃️ Core Tables

### `gold.dim_customers`
Stores customer demographic and identity information.

### `gold.dim_products`
Stores product details, cost, and category information.

### `gold.fact_sales`
Contains sales transaction data with measures like quantity, price, and dates.

---

## 📈 Business Insights

The scripts provide insights such as:

- Total and average revenue
- Customer and product segmentation (VIP, High-Performer, etc.)
- Top/bottom customers and products
- Monthly trends and seasonality
- YoY performance comparisons
- Cumulative and moving averages
- Part-to-whole category contributions

---

## 📊 Reports

Two report views are generated:

- `gold.report_customers`: Customer KPIs, segmentation, recency, AOV, etc.
- `gold.report_products`: Product performance, segmentation, recency, etc.

---

## ✅ Usage Tips

- Run scripts in numerical order: `00` to `13`
- Confirm your CSV file paths match the script's `BULK INSERT` statements
- Use SQL Server Management Studio (SSMS) for better visualization

---
  
## 🛡️ License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and share this project with proper attribution.

## 🌟 About Me

Hi there! I'm **Rasheeda Sultana**. I’m a fresher in Data Analytics and passionate learner on a mission to share knowledge to help others learn and make working with data enjoyable and engaging. Contributions are welcome! Please open an issue or pull request.

Happy querying! 🎯
