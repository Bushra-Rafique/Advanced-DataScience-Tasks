# Task 4: Loan Default Risk with Business Cost Optimization

## Objective:
Predict the likelihood of a customer defaulting on a loan and optimize the classification threshold to minimize overall business cost by considering the financial implications of false positives and false negatives.

## Dataset:
- **Name:** UCI_Credit_Card.csv
- **Source:** UCI / Kaggle
- **Content:** Customer attributes such as credit history, education, income type, loan amount, previous defaults, etc.

## Data Preparation:
- Loaded and preprocessed the dataset:
  - Handled missing values
  - Encoded categorical features using LabelEncoder / OneHotEncoding
  - Scaled numerical features for model compatibility
  - Split dataset into training and testing sets

## Modeling:
Trained the following binary classification models:
- **Logistic Regression**
- **CatBoost Classifier**

### Evaluation Metrics:
- Accuracy
- Confusion Matrix
- ROC-AUC
- Classification Report

## Business Cost Optimization:
Defined the following cost structure:
- **False Positive (FP)** – Approving a bad loan → high cost
- **False Negative (FN)** – Rejecting a good loan → moderate cost

### Steps:
- Calculated total cost for different threshold values
- Identified **optimal threshold** minimizing business cost
- Visualized cost vs. threshold trade-off

## Feature Importance:
Used:
- **CatBoost’s built-in feature importance** to identify top predictors
- **Visualization** of important features driving loan defaults

## Skills Gained:
- Binary classification using Logistic Regression and CatBoost
- Cost-sensitive decision-making
- Threshold optimization for business benefit
- Feature importance analysis for risk modeling
