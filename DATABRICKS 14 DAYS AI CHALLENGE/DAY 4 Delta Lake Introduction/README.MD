### Day 4 – Delta Lake Introduction
📅 12/01/26

<img src="https://github.com/Tungana-Bhavya/DATABRICKS_14_DAYS_AI_CHALLENGE/blob/main/DATABRICKS%2014%20DAYS%20AI%20CHALLENGE/DAY%204%20Delta%20Lake%20Introduction/IMAGES/1.png" alt="Image" width="500" height="520">

## Topics Covered
- What is Delta Lake?
- ACID transactions
- Schema enforcement
- Delta vs Parquet

## Takeaways
- Delta Lake
Keywords: Reliable, Manageable, Transactional, Scalable</br>
Delta Lake is a storage layer on top of cloud data lakes that adds ACID transactions, schema control, and versioning to Parquet.

- ACID Transactions
Keywords: Consistency, Safe writes, Concurrency, Reliability</br>
Delta Lake ensures atomic writes, snapshot isolation, and durable commits, enabling multiple jobs to safely read and write the same table.

- Schema Enforcement
Keywords: Schema-on-write, Data quality, Controlled ingestion</br>
Delta Lake rejects invalid schemas and data types, preventing silent data corruption in batch and streaming pipelines.

- Delta vs Parquet
Parquet: Fast, Columnar, Storage format</br>
Delta: Parquet + Transactions, Updates, Deletes, Time travel</br>
Delta adds reliability and governance to data lakes.

## Hands-on
- Imported PySpark and Delta Lake libraries in Databricks.
- Defined an explicit schema and read CSV data into Spark DataFrames.
- Converted CSV data to Delta format and stored it in Delta Lake.
- Created managed Delta tables using PySpark and Spark SQL.
- Tested schema enforcement by attempting writes with an incompatible schema.
- Handled duplicate inserts using deduplication logic and validated results.

## Study Resources
https://docs.databricks.com/delta/

https://docs.databricks.com/delta/tutorial.html
