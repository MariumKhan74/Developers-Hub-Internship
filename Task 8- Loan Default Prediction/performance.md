# Loan Default Prediction Model Performance Report

## Objective:
The goal of this project was to build a classification model to predict whether a loan applicant would default using financial data. The model was evaluated using the following metrics:

- **Precision**: How many of the instances predicted as positive (default) are actually positive.
- **Recall**: How many of the actual positive instances (defaults) were correctly identified by the model.
- **F1-Score**: A harmonic mean of Precision and Recall, providing a balance between the two.

## Evaluation Metrics:
The model performance was evaluated using the following classification metrics:

### Accuracy Score:
- The accuracy score of the model was calculated as the percentage of correctly predicted instances over the total number of instances.

### Precision, Recall, and F1-Score:
- **Precision**: The proportion of predicted defaults that were correct. It is calculated as:
  - Precision = True Positives / (True Positives + False Positives)
- **Recall**: The proportion of actual defaults that were correctly identified. It is calculated as:
  - Recall = True Positives / (True Positives + False Negatives)
- **F1-Score**: The balance between Precision and Recall. It is calculated as:
  - F1-Score = 2 * (Precision * Recall) / (Precision + Recall)

### Classification Report:
The classification report provides detailed metrics for both the positive (loan default) and negative (no default) classes.
Accuracy: 0.9825
              precision    recall  f1-score   support

           1       0.98      1.00      0.99      1858
           2       1.00      1.00      1.00       104
           3       0.00      0.00      0.00        18
           4       0.00      0.00      0.00         9
           5       0.80      0.36      0.50        11

    accuracy                           0.98      2000
   macro avg       0.56      0.47      0.50      2000
weighted avg       0.97      0.98      0.98      2000

