# Neural Network Algorithm

## Introduction
A neural network is a computational model inspired by the structure and functions of the human brain. It consists of layers of interconnected neurons that transform input data through weighted connections and non-linear activation functions. This implementation uses a simple feedforward neural network with one hidden layer for binary classification.

---

## Dataset
The dataset used for training and testing is a synthetic dataset generated using scikit-learn's `make_moons`. It is a binary classification dataset that is not linearly separable, making it suitable for testing the neural network's non-linear decision boundary.

- **Number of samples**: 500  
- **Number of features**: 2  
- **Classes**: 0 and 1  

---

## Neural Network Implementation
### 1. Architecture
- **Input layer**: 2 neurons (one for each feature).  
- **Hidden layer**: 10 neurons with sigmoid activation.  
- **Output layer**: 1 neuron with sigmoid activation.

### 2. Training Process
The network is trained using backpropagation to minimize the binary cross-entropy loss:
\[ \text{Loss} = -\frac{1}{n} \sum \left( y \log(\hat{y}) + (1 - y) \log(1 - \hat{y}) \right) \]

Weights are updated using the following gradient descent rules:
- Hidden-to-output weights:
\[ w_{ho} = w_{ho} - \alpha \cdot \Delta_{output} \]
- Input-to-hidden weights:
\[ w_{ih} = w_{ih} - \alpha \cdot \Delta_{hidden} \]

---

## Results
### 1. Loss Curve
The loss curve shows the convergence of the model during training.

### 2. Decision Boundary
The decision boundary demonstrates how the neural network separates the two classes.

---

