Credit Card Fraud Detection System
Project Overview
This project develops a fraud detection system using the Credit Card Fraud Dataset. The system:
✔️ Trains a machine learning model to detect fraudulent transactions
✔️ Uses data preprocessing techniques to handle class imbalance
✔️ Evaluates model performance using precision, recall, and F1-score
✔️ Provides a simple command-line interface to test transactions

Dataset
Source: Credit Card Fraud Detection Dataset

Features:

Time: Time elapsed since the first transaction

V1 to V28: PCA-transformed numerical features

Amount: Transaction amount

Class: 0 (Legitimate) / 1 (Fraudulent)

Project Steps
1️ Data Preprocessing

Load dataset and explore class imbalance

Handle imbalance using SMOTE (Synthetic Minority Over-sampling Technique)

Normalize the Amount feature

2️⃣ Model Training

Train Random Forest or Gradient Boosting model

Save the trained model as fraud_detection_model.pkl

3️⃣ Model Evaluation

Compute Precision, Recall, F1-score

4️⃣ Testing Interface

Create a simple command-line interface (test.py)

Allow users to enter transaction details

Predict whether a transaction is fraudulent or legitimate

How to Run the Project
🔹 1. Install Dependencies
Run the following command to install required libraries:

bash
Copy
Edit
pip install numpy pandas scikit-learn imbalanced-learn
🔹 2. Train the Model
Run the training script:

bash
Copy
Edit
python train.py
This will:
✔️ Load and preprocess the dataset
✔️ Train the fraud detection model
✔️ Save the trained model (fraud_detection_model.pkl)

3. Test Transactions
Run the test script:

bash
Copy
Edit
python test.py
The script will ask for 4 key inputs:

Time

V1, V2, V3 (PCA








