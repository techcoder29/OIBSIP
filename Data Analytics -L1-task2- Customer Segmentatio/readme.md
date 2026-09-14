# Task 2 - Customer Segmentation Analysis

## 📌 Project Overview

This project focuses on segmenting customers of an e-commerce company based on their purchasing behaviour.

The objective is to use **RFM (Recency, Frequency, Monetary) analysis** and **K-Means clustering** to identify distinct customer groups. These segments can help businesses develop targeted marketing strategies and improve customer engagement.

---

## 🎯 Objective

The main objectives of this project are:

- Analyze customer purchasing behaviour
- Create meaningful RFM features
- Standardize the selected features
- Use the Elbow Method to determine the optimal number of clusters
- Apply K-Means clustering
- Visualize the identified customer segments
- Profile each customer segment
- Recommend suitable marketing strategies for each segment

---

## 🛠️ Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## 📂 Dataset

The dataset contains customer-level information including:

- Customer ID
- Recency
- Product purchase information
- Web purchases
- Catalog purchases
- Store purchases
- Spending across different product categories
- Other customer-related attributes

The dataset contains **2,240 customer records and 29 variables**.

---

## 📊 RFM Analysis

Three behavioural features were selected for customer segmentation:

### Recency

Recency represents the number of days since the customer's most recent purchase.

- Lower Recency → More recently active customer
- Higher Recency → Less recently active customer

### Frequency

Frequency represents the number of purchases made by a customer.

It was calculated using:

- Web purchases
- Catalog purchases
- Store purchases

### Monetary

Monetary represents the total amount spent by each customer across the available product categories.

The following spending columns were combined:

- MntWines
- MntFruits
- MntMeatProducts
- MntFishProducts
- MntSweetProducts
- MntGoldProds

---

## 🔄 Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the dataset using Pandas
2. Inspected the dataset structure
3. Checked for missing values
4. Checked for duplicate records
5. Handled missing values
6. Created Frequency and Monetary features
7. Constructed the RFM dataset
8. Standardized the RFM features using `StandardScaler`

---

## 📈 Elbow Method

The Elbow Method was used to determine a suitable number of clusters for K-Means.

Different values of K were tested and their inertia values were compared.

Based on the resulting elbow curve, **4 clusters** were selected for the final segmentation.

---

## 🤖 K-Means Clustering

K-Means clustering was applied to the standardized RFM features.

```python
KMeans(n_clusters=4, random_state=42, n_init=10)
