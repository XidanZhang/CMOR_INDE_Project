# K-Nearest Neighbors Algorithm

## Introduction
K-Nearest Neighbors (KNN) is a simple, non-parametric, and lazy learning algorithm used for classification and regression tasks. It classifies a sample based on the majority vote of its nearest neighbors.

---

## Dataset
The dataset used for training and testing is synthetically generated using scikit-learn's `make_classification` function. It contains two features and one binary label.

- **Number of samples**: 200  
- **Number of features**: 2  
- **Classes**: 0 and 1  

---

## KNN Implementation
### 1. Algorithm
For a given sample \( x \), the KNN algorithm performs the following steps:
1. Calculate the distance between \( x \) and all training samples.
2. Select the \( k \) nearest neighbors.
3. Assign \( x \) to the most common class among its \( k \) nearest neighbors.

### 2. Distance Metric
The Euclidean distance is used to measure the distance between two points:
\[ d(x_1, x_2) = \sqrt{\sum_{i=1}^n (x_{1i} - x_{2i})^2} \]

---

## Training Process
- **Number of neighbors (k)**: 5  
- **Train-Test Split**: 80% training, 20% testing  


---

## Results
### 1. Decision Boundary
The decision boundary illustrates how the KNN algorithm classifies samples based on their proximity to neighbors.

### 2. Accuracy
The accuracy of the model on the test set is reported in the console.



