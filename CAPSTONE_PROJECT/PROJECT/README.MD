## AI-Driven Framework for Underpriced Fitness Products
### Problem Statement
Fitness product pricing in the market is inconsistent, making it difficult for buyers to identify fair deals. Wide price variations exist for similar products, manual comparisons are slow and error-prone, and high-value deals are often hidden among overpriced listings.</br>

### Objective: 
Build an AI-powered solution to:
•	Predict fair market prices for fitness products.</br>
•	Detect underpriced products with actionable insights.</br>
•	Generate a Value Score metric to highlight the best deals.</br>

### Project Overview
- Data Engineering & Lakehouse Architecture
- Databases & Tables</br>

### Processing Steps:
o	Imported Amazon e-commerce data (~551,585 records).</br>
o	Filtered fitness-related products for analysis (~12,496 records).</br>
o	Handled missing values and removed nulls (ratings, price columns).</br>
o	Outlier detection: Removed extreme prices (e.g., ₹6.1 Crore).</br>
o	Dropped irrelevant/zero-variance columns (image, link, _c0, main_category).</br>
o	Categorical encoding: sub_category_standardized → numerical sub_cat_index.</br>
o	VectorAssembler used to combine numerical features (sub_cat_index, ratings, no_of_ratings, discount_price) into a single feature vector.</br>

### Machine Learning Models
#### Models Trained:
1.	Linear Regression – Transparent and explainable, R² = 0.8776, RMSE = ₹2292.00</br>
2.	Random Forest Regressor – Captures non-linear relationships, R² = 0.7688, RMSE = ₹2,533.29</br>
3.	Gradient Boosted Trees (GBT) – Strong performance with moderate complexity, R² = 0.8280, RMSE = ₹2,500.68</br>
•	Final Model: Linear Regression selected for its accuracy, simplicity, and interpretability.</br>
•	Feature Importance (Weights)</br>

### AI Valuation Logic
- Predicted Price: Estimated fair market value for each product.</br>
- Price Gap: Predicted Price – Current Market Price.</br>
- Value Score (%): (Price Gap / Predicted Price) × 100 to highlight undervaluation.</br>

### Business Insights & Impact
- Consumer Perspective: Identify top underpriced products and make data-backed purchasing decisions.</br>
- Retailer Perspective: Detect mispriced inventory and optimize pricing strategy.</br>

### Automation & Scalability
- Daily ingestion and cleaning via Databricks Jobs.
- End-to-end traceability with MLflow and Delta Lake.
- Bronze → Silver → Gold workflow ensures consistent data quality.

### Technologies Used
•	Data Engineering: PySpark, Delta Lake, Databricks Lakehouse.
•	Machine Learning: PySpark MLlib (Linear Regression, Random Forest, GBT).
•	Visualization: Databricks display, Matplotlib / Seaborn (optional).

### Future Scope
•	Real-time pricing updates.
•	Expansion to other e-commerce categories.
•	Integrating external market data for improved predictions.

