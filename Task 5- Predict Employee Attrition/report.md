# 📘 Report: IBM HR Attrition Prediction

## 1. 📁 Dataset Overview

- Source: [IBM HR Analytics on Kaggle](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
- Objective: Identify key drivers of employee attrition and predict at-risk individuals using machine learning.

## 2. 📊 Exploratory Data Analysis (EDA)

### Key Visual Insights:

- **Job Role vs Attrition**:
  - `Sales Executive` and `Laboratory Technician` had the highest number of employees leaving.
  
- **Gender vs Attrition**:
  - Males showed slightly higher attrition, although not drastically skewed.
  
- **Overall Attrition Rate**:
  - The dataset had a **class imbalance** with significantly fewer "Yes" (attrition) instances.

### Top Influencing Features (Observed via SHAP + Correlation):
- OverTime
- JobSatisfaction
- MonthlyIncome
- Age
- WorkLifeBalance

## 3. 🤖 Model Training

### Model: Random Forest Classifier
- Chosen for its robustness and ability to handle non-linear feature interactions.
- Achieved high performance in classifying attrition vs non-attrition cases.

### Evaluation:
- Model was trained using stratified sampling and validated using accuracy, precision, recall, and F1-score.
- SHAP was used to explain feature-level impacts.

## 4. 🧠 SHAP Analysis

- SHAP values revealed that:
  - **OverTime** had the highest impact — those working overtime were much more likely to leave.
  - **MonthlyIncome** and **JobSatisfaction** had moderate influence.
  - SHAP values were mostly small (~ -0.02 to 0), indicating that attrition decisions are multifactorial and cumulative.

## 5. 💡 Key Challenges

- **Class Imbalance**: Significant skew toward "No" in attrition.
- **Interpretability**: SHAP helped bridge the gap between accuracy and explainability.
- **Feature Engineering**: Needed to convert several categorical columns to numeric for modeling.

## 6. ✅ Recommendations

- Focus retention efforts on employees with:
  - High Overtime
  - Low Job Satisfaction
  - Roles like Sales Executive & Lab Technician

- Adopt a **data-driven retention program** using model outputs and SHAP visualizations.
- Continue refining the model by integrating real-time employee feedback data.

---
