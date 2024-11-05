# Perceptron Model for Binary Classification

## Introduction

The perceptron is a fundamental type of artificial neural network designed for binary classification tasks. It was one of the earliest models for supervised learning and forms the foundation of many more complex neural networks. The perceptron model is simple yet effective for linearly separable data, where a linear decision boundary can separate two classes. This project explores the use of the perceptron algorithm in binary classification and demonstrates how it can be extended to handle imbalanced data and multi-class classification using techniques like SMOTE (Synthetic Minority Over-sampling Technique) and Principal Component Analysis (PCA).

## Project Structure

1. **Data Preparation**: Import and preprocess data to make it suitable for training.
2. **Perceptron Model Training**: Train a basic perceptron model on the prepared data.
3. **Class Balancing with SMOTE**: Use SMOTE to address class imbalance, followed by re-training the model.
4. **Dimensionality Reduction with PCA**: Apply PCA to reduce feature space for visualization and explore the decision boundaries.

## Theory and Key Concepts

### The Perceptron Algorithm

The perceptron is a single-layer neural network model for binary classification. Its objective is to learn weights that produce the optimal decision boundary for class separation. The model's decision rule is based on a weighted sum of input features, passed through an activation function, which in the basic perceptron is the step function. During training, the perceptron iteratively updates its weights to reduce classification errors based on a learning rate.

**w ← w + α × (y - ŷ) × x**

where:
- **w** represents the weights of the model.
- **α** is the learning rate.
- **y** is the true label.
- **ŷ** is the predicted label.
- **x** is the input vector.

### Data Preprocessing and Encoding

Data used in this project includes categorical features that are converted into numeric form through one-hot encoding, and continuous features that are scaled to standardize their values. This preprocessing ensures that the perceptron model efficiently handles the dataset.

### Addressing Class Imbalance with SMOTE

Class imbalance, where some classes are underrepresented, can affect the perceptron’s performance, as it may be biased towards majority classes. To address this, we employ SMOTE, which synthetically generates new samples of minority classes, balancing the class distribution in the training dataset. By training on this augmented dataset, the perceptron model can better learn to recognize minority classes.

### Dimensionality Reduction with PCA

PCA reduces the feature space, capturing the variance in the data with fewer components. This is useful for visualizing high-dimensional data in a two-dimensional space, allowing us to see how well the perceptron’s decision boundary separates different classes. After applying SMOTE, we used PCA to project the data into two principal components and plotted the decision boundary learned by the perceptron.

