# Fashion Retail Customer Value Analysis and Segmentation

## Project Overview

This project analyzes customer purchasing behavior in a fashion retail dataset and applies machine learning techniques to identify high-value customers. The analysis includes data preprocessing, exploratory data analysis, clustering, and predictive modeling.

Understanding customer value is essential for businesses because it helps them focus on customers who generate the most revenue. By identifying high-value customers, companies can develop targeted marketing strategies and improve customer retention.

This project demonstrates a complete data science workflow using Python, from raw data analysis to machine learning model evaluation.

---

# Dataset Description

The dataset contains transaction records from a fashion retail store. Each row represents a purchase made by a customer.

## Dataset Features

| Feature | Description |
|------|------|
| Customer Reference ID | Unique identifier for each customer |
| Item Purchased | Product purchased by the customer |
| Purchase Amount (USD) | Amount spent by the customer |
| Date Purchase | Date of the transaction |
| Review Rating | Rating given by the customer |
| Payment Method | Payment method used (Credit Card or Cash) |

These variables allow us to analyze customer purchasing patterns and identify valuable customers.

---

# Project Objectives

The main objectives of this project are:

- Perform **data cleaning and preprocessing**
- Conduct **exploratory data analysis**
- Identify patterns in customer purchasing behavior
- Perform **customer segmentation using clustering**
- Build a **machine learning model to predict high-value customers**
- Evaluate model performance using classification metrics

---

# Technologies Used

The project was implemented using the following tools and libraries:

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

---

# Project Workflow

The project follows a structured data science workflow.

---

## 1 Data Loading

The dataset is loaded using the Pandas library.

```python
import pandas as pd

df = pd.read_csv("data/fashion_retail_sales.csv")
```

---

## 2 Data Cleaning

Data preprocessing is performed to ensure data quality.

Cleaning steps include:

- Converting purchase date to datetime format
- Ensuring numerical variables are correctly formatted
- Checking for missing values
- Removing duplicate records
- Standardizing column names

These steps ensure that the dataset is reliable for further analysis.

---

## 3 Feature Engineering

Additional features are extracted from the purchase date to capture time-based purchasing patterns.

Example features include:

- Month of purchase
- Day of the week
- Quarter of the year

Example code:

```python
df["PurchaseDate"] = pd.to_datetime(df["Date Purchase"])

df["Month"] = df["PurchaseDate"].dt.month
df["DayOfWeek"] = df["PurchaseDate"].dt.day_name()
df["Quarter"] = df["PurchaseDate"].dt.quarter
```

Feature engineering helps reveal seasonal trends and improves model performance.

---

## 4 Exploratory Data Analysis

Exploratory Data Analysis (EDA) is performed to understand patterns in the dataset.

Key analyses include:

- Distribution of purchase amounts
- Customer spending patterns
- Payment method usage
- Customer review ratings

Visualizations help identify trends and insights in customer behavior.

---

## 5 Customer Segmentation

Customer segmentation is performed using clustering techniques to group customers with similar purchasing behaviors.

This allows businesses to identify:

- High-value customers
- Medium-value customers
- Low-value customers

Principal Component Analysis (PCA) is used to visualize clusters in two dimensions.

---

## 6 Predictive Modeling

A classification model is trained to identify high-value customers based on their purchasing behavior.

Model performance is evaluated using:

- Confusion Matrix
- ROC Curve
- Classification metrics

Threshold tuning is performed to improve prediction accuracy.

---

# Project Structure

```
retail-customer-segmentation-ml
│
├── data
│
├── notebooks
│
├── outputs
│   ├── fashion_cluster_summary.csv
│   ├── fashion_high_value_predictions.csv
│   └── fashion_threshold_tuning_results.csv
│
├── visualizations
│   ├── PCA projection.png
│   ├── ROC curve.png
│   └── confusion matrix.png
│
└── README.md
```

---

# Outputs

The **outputs** folder contains the main results generated from the project.

### fashion_cluster_summary.csv

Contains summary statistics of the identified customer clusters.

### fashion_high_value_predictions.csv

Contains predictions identifying high-value customers.

### fashion_threshold_tuning_results.csv

Contains results from threshold tuning used to optimize classification performance.

---

# Visualizations

## PCA Projection

This visualization shows customer clusters projected into two dimensions using **Principal Component Analysis (PCA)**.

![PCA Projection](https://github.com/LipnaRoshmi/retail-customer-segmentation-ml/blob/main/visualizations/PCA%20projection.png)

---

## ROC Curve

The ROC curve illustrates the performance of the classification model across different thresholds.

![ROC Curve](https://github.com/LipnaRoshmi/retail-customer-segmentation-ml/blob/main/visualizations/ROC%20curve.png)

---

## Confusion Matrix

The confusion matrix summarizes the performance of the classification model.

![Confusion Matrix](https://github.com/LipnaRoshmi/retail-customer-segmentation-ml/blob/main/visualizations/confusion%20matrix.png)

---

# Key Learning Outcomes

This project demonstrates important data science skills such as:

- Data cleaning and preprocessing
- Feature engineering
- Exploratory data analysis
- Customer segmentation
- Machine learning classification
- Model evaluation
- Data visualization

---

# Future Improvements

This project can be extended by implementing:

- Advanced clustering techniques
- Customer lifetime value prediction
- Recommendation systems
- Deep learning models for customer analytics

---

# Author

Lipna Sahayaraj 

MSc Data Science
