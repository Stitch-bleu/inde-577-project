# Decision Trees

## Introduction

Decision trees are a popular supervised learning algorithm used for both classification and regression tasks. They work by recursively splitting data into subsets based on feature values, creating a tree-like structure where each node represents a decision based on a feature, and each branch represents an outcome of that decision. The final nodes, or leaves, represent the predicted class (for classification) or value (for regression).

Decision trees are highly interpretable and can model non-linear relationships without requiring feature scaling.

## Key Concepts

1. **Root Node**: The topmost node representing the entire dataset. It is split based on the feature that provides the highest information gain or lowest impurity.

2. **Decision Nodes**: These nodes represent splits based on feature values. Each decision node creates branches that represent the possible outcomes of that split.

3. **Leaf Nodes**: Also known as terminal nodes, they represent the final prediction or output once no further splits are needed.

4. **Splitting**: The process of dividing a node into sub-nodes based on specific features to minimize impurity or maximize information gain.

5. **Pruning**: A technique to prevent the tree from overfitting by reducing its complexity, either by limiting its depth or by removing nodes that provide little predictive power.

## Metrics for Splitting

Several metrics help in selecting the best features for splitting nodes:

- **Gini Impurity**: Measures the probability of incorrectly classifying a randomly chosen element from the dataset if it were randomly labeled according to the distribution of labels in the dataset. The Gini Impurity is given by:
  
$$ \( Gini = 1 - \sum_{i=1}^{C} p_i^2 \)$$

 where:
- **C** is the number of classes.
- **p<sub>i</sub>** is the probability of selecting an element of class **i**.

- **Entropy**: Used in information gain calculations, entropy quantifies the disorder or uncertainty of a dataset. The formula for entropy is:

  **Entropy = -∑<sub>i=1</sub><sup>C</sup> p<sub>i</sub> log<sub>2</sub>(p<sub>i</sub>)**

  where:
  - **C** is the number of classes.
  - **p<sub>i</sub>** is the probability of class **i**.

- **Information Gain**: Measures the reduction in entropy before and after a dataset is split on a feature. It helps in choosing the best feature for a split. 

  **Information Gain = Entropy(parent) - ∑<sub>i=1</sub><sup>k</sup> ( |child<sub>i</sub>| / |parent| ) × Entropy(child<sub>i</sub>)**

  where:
  - **k** is the number of children nodes,
  - **|child<sub>i</sub>|** is the size of each child node,
  - **|parent|** is the size of the parent node.


## Advantages and Limitations

### Advantages
- **Interpretability**: Decision trees are easy to interpret and visualize, making them popular for understanding model decisions.
- **Non-parametric**: They do not assume any specific data distribution and can model complex relationships.
- **Handles Categorical Features**: Decision trees can work with both continuous and categorical data.

### Limitations
- **Overfitting**: Decision trees are prone to overfitting, especially when the tree is too deep and captures noise in the data.
- **Instability**: Small variations in data can lead to different splits and, thus, significantly different trees.
- **Biased with Imbalanced Data**: Decision trees can be biased when classes are imbalanced; they tend to favor majority classes.

## Conclusion

Decision trees are a powerful and interpretable model suitable for a wide range of tasks. However, care must be taken to avoid overfitting, especially in scenarios with complex data. Techniques such as pruning, setting a maximum depth, or using ensemble methods (like Random Forests) can help mitigate these limitations and improve performance.
