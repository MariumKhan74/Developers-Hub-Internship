# Predicting House Prices Using the Boston Housing Dataset

## Description
This project aims to build a regression model from scratch to predict house prices using the Boston Housing Dataset. It involves data preprocessing, implementing regression models without built-in libraries, evaluating performance, and visualizing feature importance.

## Steps

### 1. Data Preprocessing
- Normalize numerical features to ensure consistent scaling.
- Encode categorical variables using one-hot encoding.
- Split the dataset into training and testing sets.

### 2. Model Implementation
Implemented the following regression models from scratch:
- **Linear Regression**: Uses gradient descent for optimization.
- **Random Forest**: Constructs multiple decision trees and averages predictions.
- **XGBoost**: Implements gradient boosting with decision trees.

### 3. Performance Comparison
Evaluated model performance using:
- **Root Mean Squared Error (RMSE)**: Measures prediction error.
- **R² Score**: Indicates goodness of fit.

### 4. Feature Importance
- Computed feature importance for tree-based models.
- Visualized feature contributions using bar plots.

## How to Run the Scripts
1. Install dependencies: `pip install numpy matplotlib`
2. Download the Boston Housing Dataset.
3. Run the Python script:
   ```sh
   python house_price_prediction.py
   ```
4. View performance metrics and visualizations.

## Observations
- Normalization significantly improves model performance.
- Random Forest and XGBoost outperform Linear Regression in capturing complex relationships.
- Feature importance analysis provides insights into key predictors of house prices.

This project demonstrates a custom approach to regression modeling without relying on built-in ML libraries, ensuring a deeper understanding of algorithm implementation.

