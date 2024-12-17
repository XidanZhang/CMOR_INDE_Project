# Decision Trees

## Introduction
Decision Trees are one of the most popular supervised learning algorithms for classification and regression tasks. They are intuitive, easy to interpret, and can handle both numerical and categorical data.

This implementation includes:
1. Training a Decision Tree model using the Iris dataset.
2. Hyperparameter tuning with GridSearchCV.
3. Visualizing the Decision Tree structure and feature importance.
4. Generating a learning curve to evaluate model performance.
5. Comparing Decision Trees with other models like Random Forests and Logistic Regression.

---

## Dataset
The Iris dataset is used in this implementation:
- **Features**:
  - Sepal Length
  - Sepal Width
  - Petal Length
  - Petal Width
- **Target**:
  - Three classes of Iris flowers: Setosa, Versicolor, and Virginica.

---

## Steps and Implementation

### 1. Model Training
The Decision Tree model is trained using the **Gini** or **Entropy** criterion. The maximum depth of the tree is set to 4 to avoid overfitting.

- **Code Snippet**:
    ```python
    clf = DecisionTreeClassifier(max_depth=4, random_state=42)
    clf.fit(X_train, y_train)
    ```

### 2. Decision Tree Visualization
The trained Decision Tree structure is visualized using the `plot_tree` function.

- **Visualization**:
    - Each node contains:
        - The decision rule (e.g., `Petal Width <= 1.75`)
        - Class prediction
        - Gini index
        - Sample count per class

---

### 3. Hyperparameter Tuning
Hyperparameters like `max_depth`, `min_samples_split`, and `criterion` are optimized using **GridSearchCV**.

- **Best Parameters Output**:
    ```
    Best Parameters: {'criterion': 'gini', 'max_depth': 4, 'min_samples_split': 5}
    Best Cross-Validation Score: 0.97
    ```

- **Code Snippet**:
    ```python
    param_grid = {
        'max_depth': [2, 4, 6, 8],
        'min_samples_split': [2, 5, 10],
        'criterion': ['gini', 'entropy']
    }
    grid_search = GridSearchCV(DecisionTreeClassifier(), param_grid, cv=5, scoring='accuracy')
    grid_search.fit(X_train, y_train)
    ```

---

### 4. Learning Curve
A **learning curve** is generated to evaluate the model's training and validation performance as the training size increases. This helps identify underfitting or overfitting.

- **Learning Curve Example**:

![Learning Curve](learning_curve_example.png)

---

### 5. Feature Importance Analysis
The importance of each feature in the decision-making process is calculated and visualized.

- **Feature Importance Example**:
    ```
    Feature Importance:
    Petal Length: 0.72
    Petal Width: 0.18
    Sepal Length: 0.06
    Sepal Width: 0.04
    ```

- **Visualization**:

![Feature Importance](feature_importance.png)

---

### 6. Model Comparison
The performance of the Decision Tree is compared with:
1. **Random Forests**
2. **Logistic Regression**

- **Performance Comparison**:
    ```
    Decision Tree Testing Accuracy: 0.98
    Random Forest Testing Accuracy: 1.00
    Logistic Regression Testing Accuracy: 0.98
    ```

- **Visualization**:

![Model Comparison](model_comparison.png)

---

## Results Summary
1. **Decision Tree Accuracy**:
   - Training Accuracy: 100%
   - Testing Accuracy: ~98%
2. **Feature Importance**:
   - Petal Length and Petal Width are the most important features.
3. **Model Comparison**:
   - Random Forests slightly outperform Decision Trees in this dataset.


---

## Future Improvements
1. Extend to handle larger and more complex datasets.
2. Compare performance with Gradient Boosting and XGBoost models.
3. Implement ensemble methods like Bagging and Boosting for further improvement.

---

## References
1. [Scikit-learn Documentation: Decision Trees](https://scikit-learn.org/stable/modules/tree.html)
2. [Iris Dataset](https://archive.ics.uci.edu/ml/datasets/iris)
3. [Understanding Decision Trees](https://en.wikipedia.org/wiki/Decision_tree_learning)
