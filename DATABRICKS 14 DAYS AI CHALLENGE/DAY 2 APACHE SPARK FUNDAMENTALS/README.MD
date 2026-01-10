### Day 2 – Apache Spark Fundamentals 
📅 10/01/26

<img src="https://github.com/Tungana-Bhavya/DATABRICKS_14_DAYS_AI_CHALLENGE/blob/main/DATABRICKS%2014%20DAYS%20AI%20CHALLENGE/DAY%202%20APACHE%20SPARK%20FUNDAMENTALS/IMAGES/1.png" alt="Image" width="500" height="520">

## Topics Covered
- Spark architecture: driver, executors, DAG
- DataFrames vs RDDs
- Lazy evaluation in Spark
- Notebook magic commands (%sql, %python, %fs)

## Tasks Completed
1. Uploaded the sample e-commerce CSV
2. Read data into PySpark DataFrame
3. Applied basic PySpark operations:
   - **select** specific columns
   - **filter** rows
   - **groupBy** and aggregate
   - **orderBy** to sort results
4. Exported results

## Activities & Exploration
- Inspected CSV and DataFrame schema
- Extracted **product_name** from **category_code**
- Removed null product names
- Filtered expensive products (**price > 100**)
- Counted events by **event_type**
- Identified top 5 products using **groupBy** and **orderBy**

## Hands-On Highlights
- Added new column **product_name**
- Displayed first 10 rows
- Counted high-value products
- Aggregated events by its type
- Retrieved top 5 products by occurrence

## Summary
- Loaded, cleaned, and transformed e-commerce data
- Applied PySpark operations (**select**, **filter**, **groupBy**, **orderBy`**)
- Performed analytics and identified top products

