# Employee Attrition Analysis

This project analyzes employee attrition using a dataset from IBM, with the goal of uncovering the factors that lead to attrition and providing actionable insights. The analysis is performed using **Random Forest** for prediction and **SHAP** for interpretability.

## Dataset Overview

The dataset contains information about employee characteristics, including demographic data, job satisfaction, work-life balance, and more. The main goal is to predict whether an employee will leave the company (attrition). The dataset includes features such as:

- **Age**: The age of the employee.
- **Attrition**: Whether the employee left the company (binary: Yes/No).
- **BusinessTravel**: The frequency of business travel (e.g., Travel_Rarely, Travel_Frequently).
- **DistanceFromHome**: The distance between the employee's home and the workplace.
- **Education**: The education level of the employee.
- **JobInvolvement**: The level of involvement the employee feels in their job (Low to Very High).
- **JobSatisfaction**: The employee’s satisfaction with their job (Low to Very High).
- **PerformanceRating**: The performance rating of the employee (Low to Outstanding).
- **WorkLifeBalance**: The employee’s balance between work and personal life (Bad to Best).

## Methodology

1. **Data Preprocessing**: The data was cleaned, and categorical variables were encoded. We handled missing values and ensured that features were in the correct format for the model.
   
2. **Random Forest Model**: A **Random Forest Classifier** was trained on the data to predict the likelihood of employee attrition. The model was evaluated using metrics such as accuracy and F1 score.

3. **SHAP (SHapley Additive exPlanations)**: SHAP was used to interpret the model’s predictions and determine the most influential features affecting attrition. SHAP values provide feature-level contributions to the prediction for each instance.

## Key Insights

Based on the model’s interpretation using SHAP, the following actionable insights were uncovered to help reduce employee attrition:

### 1. **Job Satisfaction and Job Involvement**
- **Insight**: Employees with **low job satisfaction** or **low job involvement** are more likely to leave the company.
- **Action**: Implement programs to improve job satisfaction such as:
  - Regular performance feedback and recognition
  - Providing career growth opportunities
  - Offering employees more responsibility and involvement in decision-making
  
### 2. **Distance from Home**
- **Insight**: Employees who live farther away from the office tend to have higher attrition rates.
- **Action**: Consider the following:
  - Offer **remote work** or **hybrid work** options
  - Provide **transportation assistance** or flexible working hours
  - Promote **flexible work arrangements** to accommodate long commutes

### 3. **Work-Life Balance**
- **Insight**: Employees with poor work-life balance are more likely to leave the company.
- **Action**: Enhance work-life balance by:
  - Offering **flexible working hours** or the ability to work remotely
  - Introducing **wellness programs** to support employees' mental and physical health
  - Reducing excessive workloads and ensuring that employees have time to recharge

### 4. **Employee Development and Training**
- **Insight**: Employees who feel that their skills are not being developed or who have lower opportunities for advancement are more likely to leave.
- **Action**:
  - Create **career development programs** and offer **training opportunities**
  - Provide **mentorship** or coaching to support employees' growth within the company

## Conclusion

By focusing on the most influential features—**job satisfaction**, **commute distance**, and **work-life balance**—companies can take proactive steps to reduce employee attrition. These insights can be used to design targeted interventions that improve employee retention and overall satisfaction.

## Future Work

- Experiment with other machine learning models (e.g., Gradient Boosting, XGBoost) to compare performance.
- Further analysis could be conducted to examine the effects of **EmployeeCount**, **EducationField**, and **PerformanceRating** on attrition.

## Technologies Used

- **Python**: For data analysis and machine learning.
- **pandas**: For data manipulation and preprocessing.
- **scikit-learn**: For building the Random Forest model.
- **SHAP**: For model interpretability.
- **Matplotlib / Seaborn**: For data visualization.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

