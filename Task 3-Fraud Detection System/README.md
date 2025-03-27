Credit Card Fraud Detection System
Project Overview
This project develops a fraud detection system using the Credit Card Fraud Dataset. The system trains a machine learning model to detect fraudulent transactions, uses data preprocessing techniques to handle class imbalance, evaluates model performance using precision, recall, and F1-score, and provides a simple command-line interface to test transactions.

Dataset
Source: Credit Card Fraud Detection Dataset

Features:

Time: Time elapsed since the first transaction

V1 to V28: PCA-transformed numerical features

Amount: Transaction amount

Class: 0 for Legitimate and 1 for Fraudulent

Project Steps
Data Preprocessing

Load the dataset and explore class imbalance

Handle imbalance using SMOTE (Synthetic Minority Over-sampling Technique)

Normalize the Amount feature

Model Training

Train a Random Forest or Gradient Boosting model

Save the trained model as fraud_detection_model.pkl

Model Evaluation

Compute Precision, Recall, and F1-score

Testing Interface

Create a simple command-line interface (test.py)

Allow users to enter transaction details

Predict whether a transaction is fraudulent or legitimate

How to Run the Project
Step 1: Install Dependencies
Run the following command to install required libraries:

nginx
Copy
Edit
pip install numpy pandas scikit-learn imbalanced-learn
Step 2: Train the Model
Run the training script:

nginx
Copy
Edit
python train.py
This will load and preprocess the dataset, train the fraud detection model, and save the trained model as fraud_detection_model.pkl.

Step 3: Test Transactions
Run the test script:

nginx
Copy
Edit
python test.py
The script will ask for four key inputs:

Time

V1, V2, V3 (PCA-transformed features)

Amount

Example Input
yaml
Copy
Edit
Enter Time: 1000  
Enter Feature V1: -2.1  
Enter Feature V2: 1.5  
Enter Feature V3: -1.7  
Enter Amount: 120.0  
Example Output
makefile
Copy
Edit
Prediction: Fraudulent Transaction  
or

makefile
Copy
Edit
Prediction: Legitimate Transaction  
Observations
The dataset is highly imbalanced, with very few fraudulent transactions.

Using SMOTE helps improve model performance by balancing the dataset.

Random Forest and Gradient Boosting both provide good results, but the choice depends on the evaluation metrics.

The testing interface provides a quick way to check transactions without requiring all features.

This project demonstrates a basic fraud detection system that can be further improved with advanced feature engineering, deep learning models, and real-time transaction analysis.
