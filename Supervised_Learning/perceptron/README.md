# Perceptron Algorithm

## Introduction
The Perceptron is a supervised learning algorithm used for binary classification. It iteratively adjusts weights and biases based on misclassified samples until the data becomes linearly separable.

---

## Dataset
The dataset was synthetically generated using scikit-learn's `make_classification`. It contains two features and one binary target variable.

- **Number of samples**: 200  
- **Number of features**: 2  
- **Classes**: -1 and 1  

---

## Perceptron Implementation
The Perceptron algorithm was implemented with the following components:

### 1. Activation Function
The Perceptron uses a step function to classify inputs:
\[ f(x) = \begin{cases} 
1 & \text{if } x \geq 0 \\
-1 & \text{otherwise} 
\end{cases} \]

### 2. Weight Update Rule
Weights and biases are updated for misclassified samples:
\[ w = w + \alpha \cdot (y - \hat{y}) \cdot x \]  
\[ b = b + \alpha \cdot (y - \hat{y}) \]

---

## Training Process
- **Learning Rate**: 0.01  
- **Epochs**: 1000  


---

## Results
### 1. Errors Per Epoch
The error curve shows the number of misclassifications decreasing over training epochs.

### 2. Decision Boundary
The decision boundary illustrates how the Perceptron separates the two classes.



