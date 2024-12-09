# Logistic Regression Algorithm

## Introduction
Logistic regression is a supervised learning algorithm used for binary classification. It predicts probabilities using the sigmoid function and optimizes parameters with gradient descent. The goal is to minimize the cross-entropy loss to classify data points correctly.

---

## Dataset
The dataset was synthetically generated using scikit-learn's `make_classification`. It contains two features and one binary target variable.

- **Number of samples**: 200  
- **Number of features**: 2  
- **Classes**: 0 and 1  

---

## Logistic Regression Implementation
The logistic regression algorithm was implemented from scratch with the following components:

### 1. Hypothesis Function
The hypothesis maps input features to probabilities using the sigmoid function:  
\[ \sigma(z) = \frac{1}{1 + e^{-z}} \]

### 2. Loss Function
The cross-entropy loss measures the difference between predicted probabilities and true labels:  
\[ \text{Loss} = -\frac{1}{n} \sum \left( y \log(\hat{y}) + (1 - y) \log(1 - \hat{y}) \right) \]

### 3. Gradient Descent
The gradients of the loss function are used to update the model parameters:  
\[ w = w - \alpha \cdot \frac{\partial \text{Loss}}{\partial w} \]  
\[ b = b - \alpha \cdot \frac{\partial \text{Loss}}{\partial b} \]  
where \( \alpha \) is the learning rate.

---

## Training Process
- **Learning Rate**: 0.01  
- **Epochs**: 1000  


---

## Results
### 1. Loss Curve
The loss curve shows the model converging over the training epochs.

### 2. Decision Boundary
The decision boundary demonstrates how the model separates the two classes.


