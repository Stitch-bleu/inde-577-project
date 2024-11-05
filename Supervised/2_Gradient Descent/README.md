# Gradient Descent Theory

Gradient Descent is a fundamental optimization algorithm widely used in machine learning and deep learning to minimize a cost function and improve model performance. This README explores the theoretical foundations of gradient descent, its variants, and applications in machine learning.

## 1. Introduction

Gradient Descent aims to find the minimum of a cost function by iteratively adjusting model parameters (weights and biases) in the direction that reduces error. It is essential for training models in supervised learning, particularly in regression and neural networks.

## 2. Gradient

The gradient represents the slope of the cost function with respect to the model's parameters. It indicates the direction and rate of the steepest ascent. By moving in the opposite direction (steepest descent), we aim to reach the minimum of the cost function.

The gradient of the cost function **J(θ)** with respect to a parameter **θ** is denoted by:

**∂J / ∂θ**

## 3. Learning Rate (**α**)

The learning rate, **α**, controls the step size in each iteration. A smaller **α** makes the training process more stable but slower, while a larger **α** can speed up training but may lead to instability or overshooting the minimum.

## 4. Cost Function

In linear regression, the cost function is often Mean Squared Error (MSE), which measures the average squared difference between actual and predicted values.

**MSE = (1 / n) Σ(yᵢ - ŷᵢ)²**

where:
- **yᵢ** is the actual value,
- **ŷᵢ** is the predicted value, and
- **n** is the number of data points.

## 5. Types of Gradient Descent

### Batch Gradient Descent
Uses the entire dataset to compute the gradient in each iteration, providing stable convergence but requiring more computation.

### Stochastic Gradient Descent (SGD)
Updates parameters using one sample at a time, making it faster but noisier.

### Mini-Batch Gradient Descent
A compromise between Batch and SGD, Mini-Batch Gradient Descent updates parameters using small batches, balancing convergence speed and stability.

## 6. Applications

Gradient Descent is integral to training various machine learning models, including:
- Linear Regression
- Logistic Regression
- Neural Networks

Its versatility and efficiency make it a core technique for optimization in machine learning.

## 7. Practical Considerations

Choosing the right learning rate and gradient descent variant is crucial for effective training. Techniques like learning rate schedules and momentum are often used to improve convergence and avoid local minima.

---
