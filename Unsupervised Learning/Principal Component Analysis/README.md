# Principal Component Analysis (PCA)

## Introduction
Principal Component Analysis (PCA) is a dimensionality reduction technique that transforms data into a set of linearly uncorrelated principal components. PCA is widely used for visualization, feature extraction, and noise reduction.

---

## Dataset
The Iris dataset is used for this implementation. It contains measurements of 150 samples from three species of Iris flowers:
- **Features**: Sepal length, sepal width, petal length, petal width
- **Classes**: Setosa, Versicolour, Virginica

---

## PCA Process
1. **Standardization**:
   - Standardizes the dataset to ensure features have a mean of 0 and a variance of 1.
2. **Principal Components**:
   - PCA is applied to reduce the dataset to 2 components for visualization.
   - All 4 components are computed to analyze the explained variance.

---

## Training Output
1. **Explained Variance Ratio**:
   - Displays the proportion of variance captured by each principal component:
     ```
     PC1: 72.96%
     PC2: 23.11%
     PC3: 3.68%
     PC4: 0.25%
     ```

2. **Cumulative Explained Variance**:
   - Shows the cumulative proportion of variance captured by adding principal components.

---

## Results
### 1. Pairplot of Standardized Features
- Visualizes the relationships between all pairs of features in the Iris dataset.
- Highlights the class separability before applying PCA.

### 2. PCA 2D Visualization
- Displays the reduced dataset in 2D space using the first two principal components.
- The first two components explain ~96% of the variance.

### 3. Explained Variance Bar Chart
- Illustrates the variance explained by each principal component.

### 4. Cumulative Explained Variance
- Shows how many components are needed to explain most of the variance.

