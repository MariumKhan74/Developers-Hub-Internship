# Task 1: Exploratory Data Analysis (EDA) - Titanic Dataset

## 1. Dataset Overview
The Titanic dataset consists of 891 rows and 12 columns. The key target variable is `Survived`.

## 2. Data Cleaning
- **Missing Values:** `Age` had 86 missing values, filled using median imputation. 'Cabin' had 327 missing values, the column was dropped.
- **Duplicates:** No duplicate rows found.
- **Outliers:** Detected in `Fare` and 'Age'.

## 3. Key Insights from Visualizations
- **Bar Chart:** More passengers died in the Titanic disaster than those who survived.
- **Histogram:** `Age` is right-skewed, with most passengers between 20-40 years.
- **Correlation Heatmap:** `Fare` and `Pclass` are inversely correlated, higher class passengers paid more, and lower-class passengers paid less.

## 4. Final Observations
- Higher-class passengers had a better survival rate.
- Women and children had higher chances of survival.

