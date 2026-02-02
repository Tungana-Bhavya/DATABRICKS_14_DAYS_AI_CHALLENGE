# AI-Driven Framework for Underpriced Fitness Products
## Databricks 14 Days AI Challenge – Phase II Capstone Project

### Challenge: Built a PySpark-based workflow to analyze Amazon fitness product prices and identify underpriced products using machine learning.

### Project Title

#### AI-Driven Framework for Underpriced Fitness Products

### About the Project

This project was completed as part of Phase II of the Databricks 14 Days AI Challenge. The goal of the project is to analyze pricing inconsistencies in Amazon fitness products and identify products that are priced below their fair market value.

Using PySpark and Databricks, the project predicts fair prices, detects underpriced products, and presents value-based insights. The workflow is organized using a Bronze, Silver, and Gold data structure for better data management.

### Problem Statement

Fitness product pricing in the market is inconsistent, making it difficult for buyers to identify fair deals. Price variations exist for similar products, manual comparison is time-consuming, and high-value deals are often hidden among overpriced listings.

### Objective

Build an AI-driven solution to:
- Predict fair market prices for fitness products
- Detect underpriced products
- Generate a value score to highlight the best deals

### Dataset Details

Dataset Name: Amazon Product Sales Dataset</br>
Data Source Platform: Kaggle</br>
Dataset Link:</br>
https://www.kaggle.com/datasets/rajeevmishragwl/amazon-product-sales

### Dataset Size: ~179 MB

Total Records Imported: 551,585</br>
Fitness Products Used: 12,496</br>

<b>Note:</b>
The dataset file was not added to the GitHub repository due to size limitations.
The dataset link is provided, and a sample reference image is available in the DATA folder.

### Requirements

- Databricks Workspace
- Apache Spark (PySpark)
- Python
- Delta Lake
- MLflow

### Project Architecture

Databricks Lakehouse Architecture (Bronze → Silver → Gold)
- Bronze Layer: Raw data ingestion
- Silver Layer: Cleaned and standardized data
- Gold Layer: Feature-engineered data used for machine learning

### Data Processing Steps
1. Bronze Layer – Data Ingestion
- Imported Amazon product data into Databricks
- Added ingestion timestamp for tracking
- Stored raw data in Delta tables

2. Silver Layer – Data Cleaning
- Filtered Sports & Fitness products
- Removed duplicates and unnecessary columns
- Standardized product sub-categories
- Cleaned and converted price and rating fields
- Handled missing values

3. Gold Layer – Feature Engineering
- Encoded categorical features
- Combined numerical features using VectorAssembler
- Removed extreme price outliers
- Prepared data for training and testing

### Machine Learning Models
Models Trained
1. Linear Regression
- R² = 0.8776
- RMSE = ₹2,292

2. Random Forest Regressor

- R² = 0.7688
- RMSE = ₹2,533

3. Gradient Boosted Trees (GBT)

- R² = 0.8280
- RMSE = ₹2,500

Final Model Selection
Linear Regression was selected due to better accuracy and easier interpretation compared to other models.

### AI Valuation Logic

- Predicted Price: Estimated fair market value
- Price Gap: Predicted Price − Current Price
- Value Score (%):
(Price Gap / Predicted Price) × 100
Higher value scores indicate better pricing opportunities.

### Key Insights
- Identified multiple underpriced fitness products
- Observed price gaps ranging from ₹7,000 to ₹35,000
- Cardio and strength training categories showed strong value potential

### GitHub Folder Structure
DATABRICKS_14_DAYS_AI_CHALLENGE/
└── CAPSTONE_PROJECT/
    ├── Notebook/
    │   └── UNDERVALUED_FITNESS_PRODUCTS_ANALYSIS.ipynb
    │
    ├── Images/
    │
    └── DATA/
        ├── dataset_link.txt
        └── Presentation/
            └──AI-Driven Framework for Underpriced Fitness Products.pdf

### What I Completed

- Completed a Phase II capstone project under the Databricks 14 Days AI Challenge
- Imported and processed large Amazon product data
- Cleaned and standardized pricing information
- Trained and evaluated multiple machine learning models
- Identified underpriced fitness products
- Documented findings using visuals and a presentation

### Technologies Used

- PySpark
- Databricks
- Delta Lake
- PySpark MLlib
- MLflow
