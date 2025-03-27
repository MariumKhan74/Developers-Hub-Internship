# Exploratory Data Analysis (EDA) - Titanic Dataset

## Project Overview
This project involves performing **Exploratory Data Analysis (EDA)** on the Titanic dataset to uncover key insights using data cleaning, visualizations, and statistical analysis.

## Dataset Overview
- The dataset contains **891 rows** and **12 columns**.
- The target variable is **Survived**, which indicates whether a passenger survived (1) or not (0).

## Steps
### 1. Data Cleaning
- **Handling Missing Values:**
  - `Age` had **86 missing values**, filled using **median imputation**.
  - `Cabin` had **327 missing values**, and was **dropped** due to excessive missing data.
- **Removing Duplicates:**
  - No duplicate rows found.
- **Outlier Detection:**
  - Outliers were found in `Fare` and `Age` columns using statistical methods.

### 2. Data Visualizations
- **Bar Chart:**
  - More passengers **died** in the Titanic disaster than those who survived.
- **Histogram:**
  - The `Age` distribution is **right-skewed**, with most passengers aged between **20-40 years**.
- **Correlation Heatmap:**
  - `Fare` and `Pclass` are **inversely correlated**—higher-class passengers paid **higher fares**, while lower-class passengers paid **less**.

## Final Observations
- **Higher-class passengers had a better survival rate.**
- **Women and children had a higher chance of survival compared to men.**

## How to Run the Project
### Prerequisites
Ensure you have the following installed:
- Python 3.x
- Jupyter Notebook
- Required libraries: Pandas, Matplotlib, Seaborn

### Steps to Execute
1. Clone this repository:
   ```sh
   git clone <repository-link>
   ```
2. Navigate to the project folder:
   ```sh
   cd Titanic-EDA
   ```
3. Install required dependencies:
   ```sh
   pip install -r requirements.txt
   ```
4. Open Jupyter Notebook and run the scripts:
   ```sh
   jupyter notebook
   ```

