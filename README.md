# Retail Customer Segmentation and High-Value Customer Prediction

## Project Overview

This project analyzes retail transaction data from a fashion store to understand customer purchasing behavior, perform customer segmentation, and identify high-value customers using machine learning techniques.

Customer segmentation helps businesses understand different types of customers and design targeted marketing strategies. By identifying high-value customers, businesses can improve customer retention, personalize marketing campaigns, and increase profitability.

The project combines **data preprocessing, feature engineering, clustering, predictive modeling, and Tableau visualizations** to analyze and present insights from the dataset.

---

# Dataset Description

The dataset contains retail transaction records where each row represents a purchase made by a customer.

## Dataset Features

| Feature | Description |
|------|------|
| Customer Reference ID | Unique identifier for each customer |
| Item Purchased | Product purchased by the customer |
| Purchase Amount (USD) | Amount spent on the purchase |
| Date Purchase | Date of the transaction |
| Review Rating | Rating given by the customer |
| Payment Method | Payment method used (Credit Card or Cash) |

This information allows analysis of customer purchasing patterns and spending behavior.

---

# Project Objectives

The main objectives of this project are:

- Perform **data cleaning and preprocessing**
- Conduct **exploratory data analysis**
- Identify customer behavior patterns
- Perform **RFM-based customer segmentation**
- Apply **machine learning models** to predict high-value customers
- Evaluate model performance using classification metrics
- Visualize insights using **Tableau**

---

# Technologies Used

The following tools and technologies were used in this project:

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Tableau
- Jupyter Notebook

---

# Project Workflow

## 1 Data Loading

The dataset is loaded into a Pandas DataFrame for analysis.

```python
import pandas as pd

df = pd.read_csv("data/Fashion_Retail_Sales.csv")
```

---

## 2 Data Cleaning

Data preprocessing ensures that the dataset is accurate and ready for analysis.

Cleaning steps include:

- Converting purchase dates into datetime format
- Handling missing values
- Removing duplicates
- Ensuring correct data types for numerical columns

---

## 3 Feature Engineering

Additional features are extracted from the purchase date to capture temporal purchasing patterns.

Examples:

```python
df["PurchaseDate"] = pd.to_datetime(df["Date Purchase"])

df["Month"] = df["PurchaseDate"].dt.month
df["DayOfWeek"] = df["PurchaseDate"].dt.day_name()
df["Quarter"] = df["PurchaseDate"].dt.quarter
```

These features help analyze seasonal purchasing behavior.

---

## 4 Customer Segmentation (RFM Analysis)

Customers are segmented using **RFM analysis**, which evaluates customer value using three metrics:

| Metric | Meaning |
|------|------|
| Recency | How recently the customer made a purchase |
| Frequency | How often the customer purchases |
| Monetary | How much the customer spends |

Using these metrics, customers are grouped into segments such as:

- Champions
- Loyal Customers
- Potential Loyalists
- Recent Customers
- At Risk
- Lost Customers

This segmentation helps businesses understand which customers require retention strategies or marketing campaigns.

---

## 5 Predictive Modeling

Machine learning models are used to identify **high-value customers**.

Model evaluation includes metrics such as:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC Curve

Threshold tuning is also performed to optimize model performance.

---

# Tableau Visualizations

The following visualizations were created using **Tableau** to present insights from the analysis.

---

## Customer Distribution by RFM Segment

![Customer Distribution by RFM Segmentation](https://github.com/LipnaRoshmi/retail-customer-segmentation-ml/blob/main/visualizations/Customer%20Distribution%20by%20RFM%20Segmentation.png)

This chart shows the proportion of customers in each RFM segment such as Champions, Potential Loyalists, At Risk, Lost Customers, Recent Customers, and Loyal Customers.

It helps businesses identify which customer groups require engagement, retention strategies, or loyalty programs.

---

## Customer Value Distribution (Frequency vs Spending)

![Customer Value Distribution](https://github.com/LipnaRoshmi/retail-customer-segmentation-ml/blob/main/visualizations/Customer%20value%20distribution.png)

This scatter plot visualizes the relationship between **purchase frequency and monetary value**.

Insights from this visualization include:

- Customers who purchase frequently and spend more represent high-value customers.
- Some customers spend large amounts but purchase less frequently.
- Others purchase often but spend smaller amounts.

---

## Purchase Amount vs Customer Rating

![Purchase Amount vs Customer Rating](https://github.com/LipnaRoshmi/retail-customer-segmentation-ml/blob/main/visualizations/Purchase%20amount%20vs%20Customer%20Rating.png)

This visualization compares **purchase amounts for different product categories with customer ratings**.

It highlights:

- High-revenue products
- Products with high customer satisfaction
- Categories where revenue and customer satisfaction may not align.

---

# Outputs

The `outputs` folder contains results generated from the analysis.

### fashion_cluster_summary.csv

Contains summary statistics for each customer cluster.

### fashion_high_value_predictions.csv

Contains predictions identifying which customers are classified as high-value customers.

### fashion_threshold_tuning_results.csv

Contains evaluation results for different classification thresholds.

---

# Project Structure

```
retail-customer-segmentation-ml
│
├── data
│   └── Fashion_Retail_Sales.csv
│
├── notebooks
│   └── Fashion_Retail.ipynb
│
├── outputs
│   ├── fashion_cluster_summary.csv
│   ├── fashion_high_value_predictions.csv
│   └── fashion_threshold_tuning_results.csv
│
├── visualizations
│   ├── Customer Distribution by RFM Segmentation.png
│   ├── Customer value distribution.png
│   └── Purchase amount vs Customer Rating.png
│
└── README.md
```

---

# Key Learning Outcomes

This project demonstrates several important data science skills:

- Data cleaning and preprocessing
- Feature engineering
- Exploratory data analysis
- Customer segmentation
- Machine learning classification
- Model evaluation
- Data visualization using Tableau

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
