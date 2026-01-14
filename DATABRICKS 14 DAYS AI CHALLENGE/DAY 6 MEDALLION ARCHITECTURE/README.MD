### Day 6 – Medallion Architecture
📅 14/01/26

<img src="https://github.com/Tungana-Bhavya/DATABRICKS_14_DAYS_AI_CHALLENGE/blob/main/DATABRICKS%2014%20DAYS%20AI%20CHALLENGE/DAY%206%20MEDALLION%20ARCHITECTURE/IMAGES/1.png" alt="Image" width="500" height="520">

## Topics Covered
- Bronze (raw) → Silver (cleaned) → Gold (aggregated)
- Best practices for each layer
- Incremental processing patterns

## Hands-On
- Loaded raw CSV data into Bronze with metadata and extracted product names.
- Filtered, deduplicated, and enriched data in Silver with derived columns (event_date, price_tier).
- Aggregated, calculated, and rounded product-level metrics in Gold, including views, purchases, revenue, and conversion rate.
- Stored all layers in Delta format for further use.

## Learning Resources
https://www.databricks.com/glossary/medallion-architecture

https://www.youtube.com/watch?v=njjBdmAQnR0

https://youtu.be/yy9H4mlOG6I?si=cuo_wiQtW0XpbbYU

https://youtu.be/GjV2m8b9fNY?si=-3g7rbtbj9i3axJG
