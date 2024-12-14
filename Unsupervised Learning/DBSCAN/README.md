# DBSCAN (Density-Based Spatial Clustering of Applications with Noise)

## Introduction
DBSCAN is a density-based clustering algorithm that can find arbitrarily shaped clusters and identify noise points. Unlike K-Means, DBSCAN does not require specifying the number of clusters beforehand, making it suitable for datasets with complex distributions.

---

## Dataset
The dataset is synthetically generated using scikit-learn's `make_moons` function, which creates a two-moon-shaped dataset ideal for testing DBSCAN's ability to detect non-linear clusters.

- **Number of samples**: 300  
- **Features**: 2  
- **Noise level**: 0.05  

---

## Algorithm
### How DBSCAN Works:
1. For each data point, the algorithm calculates the density of its neighborhood using a distance metric.
2. **Parameters**:
   - **`eps`**: The radius of the neighborhood.
   - **`min_samples`**: The minimum number of points required to form a dense region.
3. Points are classified as:
   - **Core Points**: Points with at least `min_samples` neighbors within the `eps` radius.
   - **Border Points**: Points within the `eps` radius of a core point but do not meet the density requirement themselves.
   - **Noise Points**: Points that are neither core points nor border points.
4. Clusters are formed by connecting core points and their neighbors iteratively.

---

## Training Process
- The dataset is first standardized to ensure features have similar scales.
- DBSCAN is applied to find clusters and noise points.
- Results are visualized with a scatter plot.

---

## Results
### 1. Clustering Visualization
- Clusters are visualized with different colors.
- Noise points are shown in black.

