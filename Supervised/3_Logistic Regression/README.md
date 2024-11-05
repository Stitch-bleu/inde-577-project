# Logistic Regression

## Introduction

Logistic regression is a statistical method used for binary classification problems. It predicts the probability that a given input belongs to a particular category. Although it's called "regression," logistic regression is primarily a classification tool, mapping input features to a probability score between 0 and 1, representing the likelihood of belonging to a particular class.

Unlike linear regression, where outputs can range across all real values, logistic regression uses the **logistic (sigmoid) function** to squash output values into the [0,1] interval, making it suitable for binary outcomes. Logistic regression is widely used in areas like medical diagnosis, fraud detection, and predictive maintenance, where classifying between two states is essential.

## Theory

### Sigmoid Function

At the core of logistic regression is the sigmoid (logistic) function, which transforms any real-valued number into a value between 0 and 1:

**σ(x) = 1 / (1 + e^(-x))**

In logistic regression, the sigmoid function converts the linear combination of input features into a probability score. This score represents the probability of a data point belonging to the positive class.

### Decision Boundary

The probability output of the sigmoid function is used to classify instances based on a **decision boundary**. Typically, if the output probability is greater than 0.5, the instance is classified as belonging to the positive class; otherwise, it is classified as the negative class. The threshold (often set to 0.5) can be adjusted based on specific requirements of the application to optimize precision or recall.

### Log-Odds and Logistic Function

Logistic regression calculates the probability of an instance belonging to the positive class using **log-odds**. The relationship between log-odds and probability is given by:

**log-odds = ln(p / (1 - p)) = w₀ + w₁x₁ + w₂x₂ + ... + wₙxₙ**

Here:
- **p** is the probability of the positive class.
- **w₀, w₁, ..., wₙ** are the weights learned by the model.
- **x₁, x₂, ..., xₙ** are the feature values.

The logistic function is derived from the log-odds formula, mapping any linear combination of inputs to a probability between 0 and 1.

### Cost Function

To optimize the logistic regression model, we minimize the **logistic loss (log-loss)**, which measures the difference between predicted probabilities and actual outcomes. For a dataset with **n** instances, the log-loss cost function **J** is:

**J(θ) = - (1/n) Σ [yᵢ log(h_θ(xᵢ)) + (1 - yᵢ) log(1 - h_θ(xᵢ))]**

where:
- **yᵢ** is the actual label for instance **i**,
- **h_θ(xᵢ)** is the predicted probability,
- **θ** represents the model parameters (weights).

### Gradient Descent

Logistic regression parameters (weights) are updated using **gradient descent**, an optimization technique that iteratively adjusts weights to minimize the cost function. In each iteration, the weights are adjusted in the direction that reduces the log-loss:

**w ← w - α ∂J(θ)/∂w**

where:
- **α** is the learning rate,
- **∂J(θ)/∂w** is the gradient of the cost function with respect to the weights.

## Advantages and Limitations

**Advantages:**
- **Interpretability:** Logistic regression is highly interpretable, providing insights into how each feature impacts the prediction.
- **Efficiency:** It’s computationally efficient, suitable for large datasets with many features.
- **Probabilistic Output:** The output probabilities are useful for applications requiring probability-based decisions.

**Limitations:**
- **Linearity Assumption:** Logistic regression assumes a linear relationship between the features and the log-odds, making it unsuitable for complex, nonlinear relationships without feature engineering.
- **Binary Classification Only:** Standard logistic regression is limited to binary classification, though it can be extended to multiclass problems through variants like multinomial logistic regression.

## Applications

- **Medical Diagnosis:** Predicting the presence or absence of a disease based on symptoms and test results.
- **Customer Retention:** Identifying customers likely to churn based on behavior patterns.
- **Fraud Detection:** Classifying transactions as legitimate or fraudulent based on transaction characteristics.
- **Credit Scoring:** Estimating the likelihood that a borrower will default on a loan.

## Conclusion

Logistic regression is a powerful yet simple model for binary classification tasks. Its interpretability and probabilistic output make it a foundational algorithm in machine learning. Despite its limitations, logistic regression remains widely used, particularly for problems requiring high interpretability and probabilistic predictions.
