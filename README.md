# 🧠 Customer Segmentation with Clustering – Commerce-e Project

This project focuses on unsupervised learning techniques to perform customer segmentation based on transaction data from an online retail store. 
Using data preprocessing, feature engineering, and clustering algorithms like KMeans and Hierarchical Clustering, we uncover patterns in customer behavior to support personalized marketing strategies. The project includes exploratory data analysis, outlier detection, dimensionality reduction, and interactive visualizations for business insights.

![Startup](https://github.com/user-attachments/assets/29a8570b-6ac9-49b5-b30b-d45e1c963c37)


## 📋 Project Description

As part of the data team at Commerce-e, we were asked by the VP of Marketing and Sales to analyze customer purchase data and segment customers based on purchasing behavior. This will enable the company to create **personalized advertising strategies**.

The analysis includes:

1. **Data Exploration**
2. **Feature Engineering**
3. **Customer Segmentation**
4. **Clustering Algorithms**
5. **Visualization of Clustering Results**

## 🧾 Data Source

- `OnlineRetail.csv`: Contains purchase transactions including customer IDs, invoice dates, item details, and revenue.
- The project uses customer transaction history up to `19-01-2025`.

## ⚙️ Main Steps and Techniques

### 1. 🕵️ Data Exploration

- Checked for missing values (percentage per column).
- Cleaned the data based on in-class guidelines.

### 2. 🛠️ Feature Engineering

For each customer, we calculated:
- Total revenue (sum of all transactions).
- Number of transactions.
- Days since last transaction (relative to `19-01-2025`).

### 3. 🧹 Data Cleaning & Outlier Removal

- Removed the customer ID column.
- Checked if any column can be predicted from others (correlation).
- Detected outliers using IQR/z-score.
- Removed customers who were outliers in **2 or more** features.

### 4. 🔍 Determining Number of Clusters

- Used **Elbow Method** and **Dendrogram** (Hierarchical Clustering) to decide on optimal number of clusters.

### 5. 🤖 Clustering

- Used **KMeans** algorithm with optimal K.
- Calculated evaluation metrics:
  - Silhouette Score
  - Davies-Bouldin Index
  - Calinski-Harabasz Score
- Stored the cluster assignments alongside the original features.

### 6. 📊 Visualization

Plotted cluster assignments using:
- Revenue vs. Number of Transactions
- Revenue vs. Days Since Last Transaction
- Days Since Last Transaction vs. Number of Transactions
- **3D Visualization** with all three features
