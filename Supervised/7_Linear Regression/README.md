# Linear Regression

## Overview

Linear regression is a supervised learning algorithm used for modeling the relationship between a dependent variable \( y \) and one or more independent variables \( X \). The goal is to find the best-fitting line, represented by a linear equation, that predicts the value of \( y \) based on \( X \).

## Theory

### Linear Equation

For a simple linear regression with one predictor, the relationship is modeled as:

**\( y = w_0 + w_1 x \)**

where:
- **\( y \)** is the predicted value.
- **\( w_0 \)** is the intercept.
- **\( w_1 \)** is the coefficient for the predictor **\( x \)**.

For multiple predictors, this generalizes to:

**\( y = w_0 + w_1 x_1 + w_2 x_2 + \dots + w_n x_n \)**

where:
- **\( x_i \)** represents the i-th predictor.
- **\( w_i \)** represents the coefficient for predictor **\( x_i \)**.

### Objective: Minimizing the Cost Function

The most common approach to finding the best-fitting line is by minimizing the **Mean Squared Error (MSE)**, which measures the average squared difference between the predicted values and the actual values. 
**Mean Squared Error (MSE)** is given by:

**MSE = (1/n) Σ (yᵢ - ŷᵢ)²**

where:
- **yᵢ** is the actual value,
- **ŷᵢ** is the predicted value, and
- **n** is the number of data points.

### Gradient Descent for Optimization

Gradient Descent is an iterative optimization algorithm used to minimize the cost function (MSE) by adjusting the model's parameters (weights and bias). 

In each iteration, weights are updated using:

**wⱼ = wⱼ - α ⋅ (∂J/∂wⱼ)**

where:
- **wⱼ** is the current weight,
- **α** is the learning rate, controlling the step size,
- **J** is the cost function, and
- **∂J/∂wⱼ** is the gradient of the cost function with respect to **wⱼ**.

The process repeats until the cost function converges to a minimum, indicating that the model has found the optimal line for prediction.

## Key Concepts

- **Intercept (w₀)**: The point where the line crosses the y-axis when all predictors are zero.
- **Slope (wⱼ)**: Represents the effect of each predictor on the target variable, indicating the change in **y** for a one-unit change in **xⱼ**.
- **Learning Rate (α)**: A hyperparameter that determines the size of the steps during gradient descent. Small values of **α** lead to slower convergence, while larger values can cause the model to overshoot the optimal solution.


## Applications

Linear regression is widely used in various fields, including economics (predicting costs, prices), healthcare (estimating risks), and social sciences (analyzing relationships between variables).

