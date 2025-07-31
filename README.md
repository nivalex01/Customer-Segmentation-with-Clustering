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
  <img width="565" height="448" alt="image" src="https://github.com/user-attachments/assets/6d3f58e4-2eb6-4c49-85d5-fb9e098185cf" />
  <img width="2027" height="989" alt="image" src="https://github.com/user-attachments/assets/aa001fe1-9d87-477a-a6ef-d9277fe8314c" />


### 5. 🤖 Clustering

- Used **KMeans** algorithm with optimal K.
- Calculated evaluation metrics:
  - Silhouette Score
  - Davies-Bouldin Index
  - Calinski-Harabasz Score
- Stored the cluster assignments alongside the original features.

### 6. 📊 Visualization

Plotted cluster assignments using:
- Scatterplot of the total amount spent against the count invoice based off of the clusters prediction:
  
  <img width="997" height="692" alt="image" src="https://github.com/user-attachments/assets/19301dc5-88d8-4a8e-bc15-d01a2e3f937c" />

- Scatterplot of the total amount spent against the last transaction based off of the clusters prediction:
  
  <img width="997" height="692" alt="image" src="https://github.com/user-attachments/assets/f10f63f1-4bd6-4954-919a-cde787b15fe3" />

- Scatterplot of the last transaction against the Count invoice based off of the clusters prediction:
  
  <img width="997" height="692" alt="image" src="https://github.com/user-attachments/assets/e4ea14fd-0fc0-4863-8a2e-6ff3b40abfe3" />

- **3D Visualization** with all three features:
  
  <img width="997" height="750" alt="image" src="https://github.com/user-attachments/assets/98ef38c4-ca27-46c1-b488-a0b2e34d22fc" />


---

## 🧠 Summary

We segmented customers into distinct groups based on their total spending, transaction frequency, and recency of purchase. This allowed us to distinguish:
- High-value, loyal customers
- Inactive or one-time customers
- Moderate buyers with potential for growth

These insights support personalized marketing strategies and data-driven business decisions.

---

## ▶️ How to Run the Project

Follow the instructions below to run the project locally:

### ✅ Prerequisites

Make sure you have **Python 3.7 or higher** installed along with the following libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy plotly
```

### 📂 Clone the Repository
```bash
git clone https://github.com/nivalex01/Customer-Segmentation-with-Clustering.git
cd commercee-customer-segmentation
```

### 📄 Add the Dataset
Place the OnlineRetail.csv file in the root directory of the project.
If it's not included, you can download it from the UCI Machine Learning Repository or another reliable source.

### 🚀 Run the Jupyter Notebook
```bash
jupyter notebook
```

Then open the notebook file (e.g., Customer_Segmentation_CommerceE.ipynb) and execute the cells step by step.

### 📊 Explore and Modify
* Visualize clustering results using 2D and 3D plots.
* Experiment with different numbers of clusters or features.
* Change the reference date (e.g., 19-01-2025) to update recency calculations.
