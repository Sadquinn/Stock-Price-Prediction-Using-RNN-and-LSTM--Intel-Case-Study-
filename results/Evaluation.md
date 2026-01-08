# Performance Evaluation Using MSE (Mean Squared Error)

To evaluate the performance of the proposed models, we use **Mean Squared Error (MSE)** as the primary evaluation metric. MSE is a widely adopted loss function for regression problems and is commonly used to assess the overall performance of AI and machine learning models.

### Definition of MSE

Mean Squared Error (MSE) measures the average of the squared differences between predicted values and actual observed values. It focuses on the magnitude of prediction errors without considering their direction.

Key characteristics of MSE include:

- It is calculated as the average of the squared errors between predictions and true values.
- It effectively reflects the degree of variation in the data.
- It has favorable mathematical properties, making gradient computation and model optimization easier.

Because errors are squared, predictions that deviate significantly from the true values are penalized more heavily than smaller deviations. This property makes MSE particularly sensitive to large prediction errors.

---

### Mathematical Interpretation

Given a dataset consisting of *n* input–output pairs \([P_i, T_i]\), where \(i = 1, 2, ..., n\):

- \(T_i\) represents the true target value
- \(Y_i\) represents the model’s predicted output after training

The Mean Squared Error is defined as:

\[
MSE = \frac{1}{n} \sum_{i=1}^{n} (Y_i - T_i)^2
\]

In statistical terms, MSE represents the expected value of the squared difference between an estimated parameter and its true value. A smaller MSE indicates that the prediction model fits the experimental data more accurately.

---

### Interpretation in Model Evaluation

MSE serves as the **performance function** of the neural network in this study. It provides a convenient and effective way to quantify average prediction error and assess model accuracy.

A lower MSE value implies:

- Better predictive precision
- Stronger alignment between model outputs and actual observations
- Improved generalization performance

Related evaluation metrics include **Root Mean Squared Error (RMSE)** and **Mean Absolute Percentage Error (MAPE)**, which are often used as complementary measures.

---

### MSE as a Loss Function

Mean Squared Error is the most commonly used loss function for regression-based neural networks. It is calculated by summing the squared distances between predicted values and ground-truth values and then taking the average.

Due to its smooth and differentiable nature, MSE enables efficient gradient-based optimization during model training and is well-suited for deep learning architectures.

---

### Summary

In this study, MSE is employed to evaluate the overall performance of the proposed AI models. Its ability to penalize large errors, measure data variability, and facilitate stable optimization makes it an appropriate and reliable metric for regression-based stock price prediction tasks.
