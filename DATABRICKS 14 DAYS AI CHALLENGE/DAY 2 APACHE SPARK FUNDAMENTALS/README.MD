### Day 2 – Apache Spark Fundamentals 
📅 10/01/26

This document demonstrates basic e-commerce data analysis using PySpark in a Databricks environment.

<img src="https://github.com/Tungana-Bhavya/DATABRICKS_14_DAYS_AI_CHALLENGE/blob/main/DATABRICKS%2014%20DAYS%20AI%20CHALLENGE/DAY%202%20APACHE%20SPARK%20FUNDAMENTALS/IMAGES/1.png" alt="Image" width="500" height="520">

## Topics Covered
- Spark architecture (driver, executors, DAG)
- DataFrames vs RDDs
- Lazy evaluation
- Notebook magic commands (`%sql`, `%python`, `%fs`)

## Important Notes
### 1. Spark Architecture
- Driver: Orchestrates, schedules, holds SparkContext.
- Executors: Run tasks, store intermediate data.
- DAG: Shows task dependencies ; Spark optimizes execution.</br>
Insight: Monitor memory, reduce shuffles, repartition wisely.

### 2. Dataframes vs RDDs
- RDD: Low-level, functional, no schema.
- DataFrame: High-level, optimized, supports SQL & aggregations.</br>
Insight: Use DataFrames for ETL/analytics; RDDs for custom transformations.

### 3. Lazy Evaluation
- Transformations (filter, select) : Lazy
- Actions (show, count) : Trigger execution
Insight: Combine transformations, cache reused DataFrames

### 4. Notebook Magic Commands
- %python : Run PySpark/Python
- %sql : Run SQL queries
- %fs : File system operations in DBFS</br>
Insight: Mix SQL for analytics, Python for ETL, FS for file ops

## Hands-on
- Loaded the e-commerce dataset into a Spark DataFrame.
- Displayed sample rows to inspect the dataset.
- Performed Basic Analysis:
  - Filtered high-value products using filter.
  - Aggregated events by type using groupBy.
  - Selected key columns using select.
  - Ordered results to find top brands using orderBy.

## Study Resources
https://docs.databricks.com/pyspark/

https://spark.apache.org/docs/latest/sql-programming-guide.html
