# retail-customer-segmentation-ml
This project focuses on analyzing retail transaction data to understand customer behavior, segment customers based on their purchasing patterns, and build a predictive model to identify high-value customers.

## Project Overview
This project performs exploratory data analysis and customer segmentation on a fashion retail transaction dataset. The goal is to understand customer purchasing behavior and identify different customer segments using the RFM (Recency, Frequency, Monetary) model.

Customer segmentation helps businesses identify high-value customers, at-risk customers, and loyal buyers, allowing companies to design targeted marketing strategies.

This project was developed as part of an MSc Data Science coursework project.

---

## Dataset Description

The dataset contains retail transaction records including purchase details, customer identifiers, and payment methods.

### Features

| Feature | Description |
|------|------|
| Customer Reference ID | Unique identifier for each customer |
| Item Purchased | Product purchased by the customer |
| Purchase Amount (USD) | Amount spent in USD |
| Date Purchase | Date of the transaction |
| Review Rating | Customer rating of the purchased item |
| Payment Method | Payment type used (Credit Card / Cash) |

Example dataset records:

| CustomerID | ItemPurchased | PurchaseAmount | PurchaseDate | ReviewRating | PaymentMethod |
|---|---|---|---|---|---|
| 4018 | Handbag | 4619 | 05-02-2023 | NaN | Credit Card |
| 4115 | Tunic | 2456 | 11-07-2023 | 2 | Credit Card |
| 4019 | Tank Top | 2102 | 23-03-2023 | 4.1 | Cash |

---

## Project Workflow

### 1 Data Loading
The dataset is loaded using **Pandas** for data manipulation.

```python
df = pd.read_csv('/content/Fashion_Retail_Sales.csv')
