# Home_Sales

## Overview
This project analyzes house sales data with Apache Spark and PySpark SQL. The dataset contains a variety of variables, including price, bedrooms, baths, square footage, and view ratings. The analysis includes queries for determining average house prices using various parameters, improving speed using caching, and splitting data for increased efficiency.

## Technologies Used
- **Python** (Jupyter Notebook)
- **Apache Spark** (PySpark SQL)
- **Parquet File Format**
- **Google Colab** (or any Spark-enabled environment)

## Steps Performed

### 1. Load and Explore the Data
- Read home sales data into a Spark DataFrame
- Display schema and basic statistics

### 2. Perform SQL Queries
- Calculate average home price per year for 4-bedroom houses
- Analyze pricing based on home construction year, floors, and square footage
- Group and filter home sales by view rating

### 3. Optimize Performance
- Cache the `home_sales` table for faster queries
- Compare runtimes between cached and uncached queries
- Partition the dataset by `date_built` and save it in Parquet format

### 4. Work with Parquet Data
- Read the partitioned Parquet file
- Create a temporary table (`p_home_sales`) for SQL queries
- Run performance tests on Parquet-based queries

## Performance Comparison
| Query Type       | Execution Time (seconds) |
|-----------------|------------------------|
| Uncached Query  | 1.5346 |
| Cached Query    | 0.9856 |
| Parquet Query   | 0.9640 |

## How to Run
1. Install dependencies (if running locally):
   ```bash
   pip install pyspark
   ```
2. Open the Jupyter Notebook or Colab.
3. Run all cells in order to execute the full analysis.

