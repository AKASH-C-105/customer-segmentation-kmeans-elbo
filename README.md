# Mall Customer Segmentation using K-Means Clustering

## 📋 Overview

This project implements **customer segmentation** for a mall using the **K-Means Clustering** algorithm. The goal is to identify distinct groups of customers based on their demographic and behavioral characteristics, enabling targeted marketing strategies and improved customer experience.

## 🎯 Objective

The primary objective of this analysis is to segment mall customers into distinct groups based on:
- **Age**
- **Annual Income**
- **Spending Score**

This segmentation helps in understanding customer behavior and enables data-driven decision-making for marketing campaigns.

## 🛠️ Technology Used

### K-Means Clustering

**K-Means** is an unsupervised machine learning algorithm used for partitioning data into K distinct clusters. It works by:

1. **Initialization**: Randomly selecting K initial centroids
2. **Assignment**: Assigning each data point to the nearest centroid
3. **Update**: Recalculating centroids based on the mean of assigned points
4. **Iteration**: Repeating steps 2-3 until convergence

#### Key Features of K-Means:
- **Unsupervised Learning**: No labeled data required
- **Scalability**: Efficient for large datasets
- **Simplicity**: Easy to implement and interpret
- **K-Means++**: Advanced initialization technique used to improve convergence

### Libraries Used
- **Pandas**: Data manipulation and analysis
- **Scikit-learn**: K-Means implementation and preprocessing
- **Matplotlib**: Data visualization

## 📊 Dataset

**File**: `Mall_Customers.csv`

### Features:
| Column | Description |
|--------|-------------|
| CustomerID | Unique identifier for each customer |
| Gender | Male/Female |
| Age | Customer's age in years |
| Annual_Income_(k$) | Annual income in thousands of dollars |
| Spending_Score | Score assigned by the mall (1-100) based on spending behavior |

## 📈 Analysis Workflow

### 1. Data Preprocessing
- Removed CustomerID (not relevant for clustering)
- Encoded Gender using LabelEncoder (Female=0, Male=1)
- Verified no missing values

### 2. Finding Optimal Clusters
- Used the **Elbow Method** to determine optimal K
- Plotted WCSS (Within-Cluster Sum of Squares) for K = 1 to 12
- Identified optimal K = 5 from the elbow curve

### 3. K-Means Clustering
- Applied K-Means with:
  - `n_clusters=5`
  - `init='k-means++'`
  - `max_iter=300`
  - `n_init=10`
  - `random_state=0`

### 4. Visualization
- Scatter plot showing 5 distinct customer segments
- Centroids marked for each cluster

## 🔍 Key Findings

The analysis identified **5 distinct customer segments**:

1. **Cluster 1 (Red)**: Low income, low spending
2. **Cluster 2 (Blue)**: High income, high spending (Premium customers)
3. **Cluster 3 (Green)**: Medium income, medium spending
4. **Cluster 4 (Cyan)**: Low income, high spending
5. **Cluster 5 (Gold)**: High income, low spending (Potential targets)

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas scikit-learn matplotlib
```

### Running the Notebook
1. Clone this repository
2. Open `Kmeans.ipynb` in Jupyter Notebook or JupyterLab
3. Run all cells to reproduce the analysis

## 📁 Repository Structure

```
mall-customer-segmentation-kmeans/
│
├── Kmeans.ipynb           # Main analysis notebook
├── Mall_Customers.csv     # Dataset
└── README.md              # Project documentation
```

## 📌 Business Applications

- **Targeted Marketing**: Customize promotions for each segment
- **Resource Allocation**: Focus resources on high-value customers
- **Product Recommendations**: Personalize offerings based on segment
- **Customer Retention**: Develop segment-specific retention strategies

## 🤝 Contributing

Feel free to fork this repository and submit pull requests for improvements!

## 📜 License

This project is open-source and available under the MIT License.

---

*Created as part of AI/ML Training*
