# K-Nearest Neighbors (KNN)

## Introduction
K-Nearest Neighbors (KNN) is a simple, yet powerful, supervised learning algorithm used for both **classification** and **regression** tasks. It works by identifying the nearest neighbors of a data point and making predictions based on majority voting (for classification) or averaging (for regression).

In this implementation, we:
1. Use the **`make_moons`** dataset to demonstrate KNN's non-linear classification ability.
2. Tune the **number of neighbors (K)** to find the optimal value.
3. Compare different **distance metrics** (Euclidean, Manhattan, Chebyshev).
4. Visualize results with learning curves and performance comparisons.

---

## Dataset
- **Dataset**: Generated using `make_moons` from `sklearn.datasets`.
- **Description**: 
   - Two classes of data distributed in a crescent shape.
   - Noise is added to make the classification problem more challenging.

---

## Steps and Implementation

### 1. Data Visualization
The dataset is visualized to show its crescent shape:

![Input Data](knn_input_data.png)

---

### 2. Data Splitting
The dataset is split into training and testing sets using an 80/20 ratio.

---

### 3. Choosing the Optimal K Value
We perform **cross-validation** on the training set to evaluate different values of K (1 to 20). The K value that yields the **highest cross-validation accuracy** is chosen.


- **Best K Value**:
Best K Value: 16

---

### 4. Model Training and Evaluation
Using the optimal K value, we train the KNN model and evaluate its performance on the testing set.

- **Test Accuracy**:
Test Accuracy: 0.98

---

### 5. Learning Curve
We plot the **learning curve** to observe how the training and validation accuracies change as the training set size increases.

---

### 6. Comparison of Distance Metrics
We compare the performance of KNN using three common distance metrics:
1. **Euclidean Distance**
2. **Manhattan Distance**
3. **Chebyshev Distance**

- **Results**:
Accuracy for different distance metrics:
Euclidean: 0.98
Manhattan: 0.98
Chebyshev: 0.99

---

## Results Summary
1. **Best K Value**: 7
2. **Test Accuracy**: 96%
3. **Distance Metric Comparison**:
- Euclidean performs slightly better than Manhattan and Chebyshev distances.
4. **Learning Curve**: 
- The model performs well with sufficient training data and shows minimal overfitting.

---

## Future Improvements
1. Apply KNN to larger and more complex datasets.
2. Experiment with **weighted KNN**, where closer neighbors have higher influence.
3. Visualize decision boundaries for better interpretability.
4. Optimize KNN using techniques like **KD-Trees** or **Ball Trees** for faster predictions on large datasets.

