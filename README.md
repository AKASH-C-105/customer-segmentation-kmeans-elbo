# Customer Segmentation Using K-Means Clustering

## Overview

This project implements **K-Means clustering**, an unsupervised machine learning algorithm, to perform customer segmentation on mall customer data. The objective is to identify distinct customer groups based on demographic and spending patterns to support data-driven business and marketing decisions.

---

## Business Objective

Customer segmentation helps organizations:
- Understand customer behavior
- Identify high-value customer segments
- Design targeted marketing strategies
- Improve customer engagement and retention

This project demonstrates how clustering techniques can extract meaningful insights from customer data.

---

## Dataset

**Dataset Name:** Mall Customers Dataset  
**File:** `Mall_Customers.csv`

### Features:
- `CustomerID`
- `Gender`
- `Age`
- `Annual Income (k$)`
- `Spending Score (1–100)`

---

## Methodology

### K-Means Clustering
- Data loading and preprocessing
- Feature selection for clustering
- Identification of optimal number of clusters using the **Elbow Method**
- Training the K-Means model
- Assigning cluster labels to customers
- Visualization of clusters and centroids
