# Linear Regression Algorithm

## Introduction
Linear regression is a supervised learning algorithm used for predicting a continuous target variable. It models the relationship between input features and the target variable by fitting a straight line to the data. In this project, we implemented linear regression from scratch using Python, trained the model using gradient descent, and visualized the regression line and loss curve.

---

## Dataset
The dataset was synthetically generated with the following linear relationship:  
\[ y = 4 + 3x + \text{noise} \]  
where noise is Gaussian noise added to simulate real-world variability.

- **Number of samples**: 100  
- **Features**: 1  
- **Target Variable**: Continuous  

---

## Linear Regression Implementation
The linear regression algorithm was implemented from scratch with the following components:

### 1. Hypothesis Function
The hypothesis predicts the target variable as a linear combination of features:  
\[ h(x) = w \cdot x + b \]  
where \( w \) is the weight (slope) and \( b \) is the bias (intercept).

### 2. Loss Function
The Mean Squared Error (MSE) was used to measure the error between predicted and actual values:  
\[ \text{MSE} = \frac{1}{n} \sum_{i=1}^{n} (y_i - h(x_i))^2 \]

### 3. Gradient Descent
The gradients of the loss function with respect to \( w \) and \( b \) were computed to update the model parameters:  
\[ w = w - \alpha \cdot \frac{\partial \text{MSE}}{\partial w} \]  
\[ b = b - \alpha \cdot \frac{\partial \text{MSE}}{\partial b} \]  
where \( \alpha \) is the learning rate.

---

## Training Process
- **Learning Rate**: 0.01  
- **Epochs**: 1000  

The model was trained by minimizing the Mean Squared Error (MSE). 

---

## Results
### 1. Loss Curve
The loss curve demonstrates the convergence of the model during training.

### 2. Regression Line
The regression line was visualized against the dataset to demonstrate the model's performance in fitting the data.

---

## Files Included
- `linear_regression.ipynb`: Contains the full implementation of linear regression, including data generation, training, and visualization.
- `linear_regression_dataset.csv`: The dataset used for training and testing.
- `README.md`: Documentation for the project.
