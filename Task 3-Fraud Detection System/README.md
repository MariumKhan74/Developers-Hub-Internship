# Credit Card Fraud Detection System

## Project Overview
This project develops a **fraud detection system** using machine learning to classify transactions as **legitimate** or **fraudulent**. The dataset used is the [Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud). The model is trained using **Random Forest** or **Gradient Boosting** to improve detection accuracy.

## Steps

### 1. Data Preprocessing
- Load the dataset and explore class imbalance  
- Handle imbalance using **SMOTE (Synthetic Minority Over-sampling Technique)**  
- Normalize the **Amount** feature  

### 2. Feature Engineering
- Select relevant numerical features for training  
- Standardize transaction amounts  

### 3. Model Training
- Split data into **training and testing** sets  
- Train a **Random Forest**.
- Save the trained model as `fraud_detection_model.pkl`  

### 4. Model Evaluation
- Evaluate the model using **accuracy, precision, recall, and F1-score**  

### 5. Fraud Detection Interface
- Implement a **command-line interface** to test transactions  
- Allow users to input transaction details and receive a prediction  

## How to Run the Scripts

### Step 1: Install Dependencies
Run the following command to install required libraries:

pip install numpy pandas scikit-learn imbalanced-learn

shell
Copy
Edit

### Step 2: Train the Fraud Detection Model
Execute the training script:

python train.py

markdown
Copy
Edit

This will **load and preprocess** the dataset, train the fraud detection model, and save it as `fraud_detection_model.pkl`.

### Step 3: Test Transactions
Run the test script:

python test.py

markdown
Copy
Edit

The script will prompt you to **enter key transaction details**:  
- **Time**  
- **V1, V2, V3** (PCA-transformed numerical features)  
- **Amount**  

### Example Input

Enter Time: 2000
Enter Feature V1: -1.5
Enter Feature V2: 2.0
Enter Feature V3: -0.8
Enter Amount: 250.0

### Expected Output

Prediction: Fraudulent Transaction

or  

Prediction: Legitimate Transaction

## Observations
- The dataset is highly **imbalanced**, with very few fraudulent transactions.  
- Using **SMOTE** improves the model’s ability to detect fraud.  
- **Random Forest** perform well, with 99% accuracy.  
- The **testing interface** allows quick verification of transactions without requiring all features.  

This project demonstrates a **basic fraud detection system** that can be further enhanced with **real-time transaction monitoring** and **deep learning techniques**.
