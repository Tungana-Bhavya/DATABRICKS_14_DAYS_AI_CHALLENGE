# AI-Driven Framework for Underpriced Fitness Products
## Databricks 14 Days AI Challenge – Phase II Capstone Project

### Challenge: 
Built a PySpark-based workflow to analyze Amazon fitness product prices and identify underpriced products using machine learning.

### Project Title

#### AI-Driven Framework for Underpriced Fitness Products

### About the Project

This project was completed as part of <b>Phase II of the Databricks 14 Days AI Challenge.</b> The goal of the project is to analyze pricing inconsistencies in Amazon fitness products and identify products that are priced below their fair market value.

Using <b>PySpark</b> and <b>Databricks</b>, the project predicts fair prices, detects underpriced products, and presents value-based insights. The workflow is organized using a <b>Bronze</b>, <b>Silver</b>, and <b>Gold </b>data structure for better data management.

### Problem Statement

Fitness product pricing in the market is inconsistent, making it difficult for buyers to identify fair deals. Price variations exist for similar products, manual comparison is time-consuming, and high-value deals are often hidden among overpriced listings.

### Objective

Build an AI-driven solution to:
- Predict fair market prices for fitness products
- Detect underpriced products
- Generate a value score to highlight the best deals

### Dataset Details

<b>Dataset Name:</b> Amazon Product Sales Dataset</br>
<b>Data Source Platform:</b> Kaggle</br>
<b>Dataset Link:</b></br>
https://www.kaggle.com/datasets/rajeevmishragwl/amazon-product-sales
<b>Dataset Size:</b> ~179 MB</br>
<b>Total Records Imported:</b> 551,585</br>
<b>Fitness Products Used:</b> 12,496</br>

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
1. <b>Bronze Layer – Data Ingestion</b>
- Imported Amazon product data into Databricks
- Added ingestion timestamp for tracking
- Stored raw data in Delta tables

2. <b>Silver Layer – Data Cleaning</b>
- Filtered Sports & Fitness products
- Removed duplicates and unnecessary columns
- Standardized product sub-categories
- Cleaned and converted price and rating fields
- Handled missing values

3. <b>Gold Layer – Feature Engineering</b>
- Encoded categorical features
- Combined numerical features using VectorAssembler
- Removed extreme price outliers
- Prepared data for training and testing

### Machine Learning Models
<b>Models Trained</b>
1. <b>Linear Regression</b>
- R² = 0.8776
- RMSE = ₹2,292

2. <b>Random Forest Regressor</b>
- R² = 0.7688
- RMSE = ₹2,533

3. <b>Gradient Boosted Trees (GBT)</b>
- R² = 0.8280
- RMSE = ₹2,500

<img src="https://github.com/Tungana-Bhavya/DATABRICKS_14_DAYS_AI_CHALLENGE/blob/main/CAPSTONE_PROJECT/PROJECT/IMAGES/MODEL_TRAINING_RESULT.jpg" alt="Image" width="1000" height="800">

<b>Final Model Selection</b>
<b>Linear Regression</b> was selected due to better results and easier interpretation compared to other models.

### AI Valuation Logic

- Predicted Price: Estimated fair market value
- Price Gap: Predicted Price − Current Price
- Value Score (%):
(Price Gap / Predicted Price) × 100
Higher value scores indicate better pricing opportunities.

<img src="https://github.com/Tungana-Bhavya/DATABRICKS_14_DAYS_AI_CHALLENGE/blob/main/CAPSTONE_PROJECT/PROJECT/IMAGES/UNDERVALUED_FITNESS_PRODUCTS_ANALYSIS.jpg" alt="Image" width="500" height="1000">

### Key Insights
- Identified multiple underpriced fitness products
- Observed price gaps ranging from ₹7,000 to ₹35,000
- Cardio and strength training categories showed strong value potential

### GitHub Folder Structure
DATABRICKS_14_DAYS_AI_CHALLENGE/</br>
└── CAPSTONE_PROJECT/</br>
    ├── Notebook/</br>
    │   └── UNDERVALUED_FITNESS_PRODUCTS_ANALYSIS.ipynb</br>
    │</br>
    ├── Images/</br>
    │</br>
    └── DATA/</br>
        ├── dataset_link.txt</br>
        └── Presentation/</br>
            └──AI-Driven Framework for Underpriced Fitness Products.pdf</br>

### What I Completed

- Completed a <b>Phase II capstone project</b> under the <b>Databricks 14 Days AI Challenge</b>
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
