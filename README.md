# Loan Default Prediction

## Project Overview

This project aims to predict whether a borrower will default on a loan using their financial history, credit scores, and other personal attributes. By developing a machine learning model, the goal is to assist lenders in identifying high-risk borrowers and making informed decisions to minimize financial losses. The model is built using a dataset containing borrower-specific features and a Random Forest Classifier to predict loan defaults.

## Problem Statement

Loan defaults represent a significant risk to financial institutions, often resulting in substantial losses. Accurately predicting which borrowers are likely to default on their loans is essential for mitigating this risk. This project utilizes historical financial data, credit scores, and other borrower characteristics to classify whether a borrower is likely to default on a loan or not. The predictive model helps lenders make data-driven decisions and reduce financial risks.

## Methodology

The project follows a structured machine learning pipeline:

1. **Data Preprocessing**:
   - Handling missing values through forward filling.
   - Converting categorical variables into numerical format using one-hot encoding.
   - Converting binary 'Yes'/'No' columns into 1/0.
   - Downcasting numeric columns to optimize memory usage.

2. **Exploratory Data Analysis (EDA)**:
   - Visualizing feature distributions and correlations to gain insights into the data.
   
3. **Modeling**:
   - Splitting the dataset into training and testing sets.
   - Using a **Random Forest Classifier** to train the model due to its effectiveness in handling both numerical and categorical features.

4. **Evaluation**:
   - Evaluating the model's performance using metrics such as accuracy, classification report, and ROC AUC score.
   - Analyzing feature importance to understand the key factors contributing to loan defaults.

## Requirements

To run this project, you'll need the following Python libraries:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `sklearn`
##Output
Columns: ['LoanID', 'Age', 'Income', 'LoanAmount', 'CreditScore', 'MonthsEmployed', 'NumCreditLines', 'InterestRate', 'LoanTerm', 'DTIRatio', 'Education', 'EmploymentType', 'MaritalStatus', 'HasMortgage', 'HasDependents', 'LoanPurpose', 'HasCoSigner', 'Default']
✅ Classification Report:
              precision    recall  f1-score   support

         0.0       0.88      1.00      0.94      1762
         1.0       1.00      0.00      0.01       238

    accuracy                           0.88      2000
   macro avg       0.94      0.50      0.47      2000
weighted avg       0.90      0.88      0.83      2000

✅ ROC AUC Score: 0.733007277826
<ipython-input-12-8e4d351572c8>:84: FutureWarning: 

Passing `palette` without assigning `hue` is deprecated and will be removed in v0.14.0. Assign the `y` variable to `hue` and set `legend=False` for the same effect.

  sns.barplot(x=importances[indices], y=features, palette='viridis')
