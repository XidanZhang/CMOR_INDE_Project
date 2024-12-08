# Logistic Regression Algorithm

## Introduction
Logistic regression is a supervised learning algorithm used for binary classification. It predicts the probability of belonging to a particular class using the sigmoid function and optimizes the model using gradient descent. In this project, we implement logistic regression from scratch, visualize the decision boundary, and analyze the training process using a loss curve.

---

## Dataset
The dataset used in this project is synthetically generated using scikit-learn's `make_classification` function. It consists of two features and one binary target variable.

- **Number of samples**: 200
- **Number of features**: 2
- **Classes**: 0 and 1

### Data Preprocessing
- **Train-Test Split**: 70% training, 30% testing.
- **Feature Standardization**: Data is standardized using `StandardScaler` to improve model performance.

---

## Logistic Regression Implementation
The logistic regression algorithm is implemented from scratch using Python. Key components include:
1. **Sigmoid Function**:
   - Converts linear outputs to probabilities between 0 and 1.
   - \( \sigma(z) = \frac{1}{1 + e^{-z}} \)

2. **Loss Function**:
   - Cross-entropy loss is used to measure the difference between predicted probabilities and true labels.
   - \( \text{Loss} = - \frac{1}{n} \sum_{i=1}^{n} \left( y_i \log(\hat{y}_i) + (1 - y_i) \log(1 - \hat{y}_i) \right) \)

3. **Gradient Descent**:
   - Optimizes weights and bias using gradients of the loss function.

4. **Decision Boundary**:
   - A visualization of the model's classification ability.

---

## Training Process
- **Learning Rate**: 0.01
- **Epochs**: 1000

During training, the model minimizes the cross-entropy loss, and the loss is visualized in a **loss curve**.

---

## Results
### 1. Loss Curve
The loss curve demonstrates how the model converges over the epochs.

### 2. Decision Boundary
The decision boundary plot shows the separation between the two classes.

---

## Files Included
- `logistic_regression.ipynb`: Contains the full implementation of logistic regression, including data preprocessing, model training, and visualization.
- `logistic_regression_dataset.csv`: The generated dataset used for training and testing.
- `README.md`: Documentation of the project.

---

## How to Run
1. Clone this repository and navigate to the `Supervised_Learning/logistic_regression` directory:
   ```bash
   cd Supervised_Learning/logistic_regression

