# K-Means Clustering

## Introduction
K-Means Clustering is an unsupervised learning algorithm used for grouping data points into a predefined number of clusters. This implementation uses scikit-learn's `KMeans` class to perform clustering on a synthetic dataset.

---

## Dataset
The dataset is synthetically generated using scikit-learn's `make_blobs` function. It consists of data points grouped into four distinct clusters.

- **Number of samples**: 300  
- **Number of features**: 2  
- **Number of clusters**: 4  

---

## Algorithm
### K-Means Clustering
1. Randomly initializes cluster centroids.
2. Assigns each data point to the nearest centroid.
3. Updates centroids by calculating the mean of data points within each cluster.
4. Repeats steps 2 and 3 until convergence (when centroids no longer change significantly).

---

## Training Process
1. **WCSS (Within-Cluster Sum of Squares)**:
   - Measures the variance within clusters.
   - Used to evaluate the clustering performance.
2. **Elbow Method**:
   - Determines the optimal number of clusters by plotting WCSS against the number of clusters.


---

## Results
### 1. Clustering Visualization
- Data points are colored based on their assigned clusters.
- Centroids are displayed as red `X` markers.

### 2. Elbow Method Visualization
- Identifies the "elbow point," which indicates the optimal number of clusters.

