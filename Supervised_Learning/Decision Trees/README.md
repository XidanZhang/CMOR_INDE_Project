# Decision Trees / Regression Trees

## Introduction
Decision trees are a versatile machine learning algorithm capable of performing both classification and regression tasks. They partition the feature space into a set of rectangles and assign a prediction value for each region.

---

## Dataset
The dataset is synthetically generated using scikit-learn's `make_classification`. It contains two features and one binary label.

- **Number of samples**: 200  
- **Number of features**: 2  
- **Classes**: 0 and 1  

---

## Decision Tree Implementation
### 1. Splitting Criteria
The tree splits data at each node based on the Gini impurity or information gain (entropy).

### 2. Tree Depth
The maximum depth of the tree is limited to prevent overfitting. In this example:
- **Max Depth**: 4

### 3. Visualization
- **Decision Boundary**: Displays the classification regions created by the decision tree.
- **Tree Structure**: Shows the hierarchical structure of the decision tree.

---

## Training Process
- **Train-Test Split**: 80% training, 20% testing  
- **Performance Metric**: Accuracy  

---

## Results
### 1. Decision Boundary
The decision boundary illustrates the regions classified by the tree.

### 2. Tree Structure
The tree structure demonstrates how the data is split at each node, including thresholds, sample counts, and class distributions.


