# Module 12 Report Template

## Overview of the Analysis

In this analysis, the purpose was to develop machine learning models to predict credit risk based on financial information provided in the dataset. The dataset contains various financial features of borrowers, such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. The goal was to predict the risk associated with each loan, where a value of 0 in the "loan_status" column indicates a healthy loan and a value of 1 indicates a high-risk loan with a potential of default.

The analysis proceeded through the following stages:

1. Data Preprocessing: The data was read into a Pandas DataFrame, and the labels (y) and features (X) were separated accordingly. The balance of the labels was checked using the value_counts() function to understand the class distribution.

2. Logistic Regression Model with Original Data: A logistic regression model was trained using the original data. The accuracy, precision, and recall scores were computed to evaluate the model's performance in predicting both healthy and high-risk loans.

3. Logistic Regression Model with Resampled Data: To address the imbalanced class distribution, the data was resampled using the RandomOverSampler from the imblearn library. The logistic regression model was then trained using the resampled data, and its performance was evaluated.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1: Logistic Regression with Original Data
 <img width="470" alt="Screenshot 2023-07-21 at 5 15 15 PM" src="https://github.com/cam1lle/credit-risk-classification/assets/117128707/dadd3407-b1e2-4401-9ff2-c10d2ae2453d">

* Machine Learning Model 2: Logistic Regression with Resampled Data
<img width="457" alt="Screenshot 2023-07-21 at 5 15 34 PM" src="https://github.com/cam1lle/credit-risk-classification/assets/117128707/ccc5c6f4-bb90-47f5-880e-92d715a6b7e2">

## Summary

Both machine learning models, the logistic regression with original data and the logistic regression with resampled data, showed promising results in predicting credit risk.

The results of Model 2, the logistic regression with resampled data, outperformed Model 1, the logistic regression with original data, in terms of balanced accuracy, precision, and recall scores. This indicates that the model trained with the resampled data, which addressed the class imbalance issue, demonstrated improved performance in identifying both healthy and high-risk loans.

In this credit risk prediction scenario, it is crucial to correctly predict high-risk loans (label 1) to minimize the potential losses due to default. Model 2 achieved higher recall scores for the high-risk label, indicating its ability to better capture and predict these risky loans. Therefore, Model 2 is recommended for use by the company as it provides better overall performance and addresses the class imbalance problem effectively.

It is important to note that the model's performance could further improve with hyperparameter tuning and the exploration of other machine learning algorithms. Additionally, considering the dynamic nature of credit risk, continuous monitoring and model updates are recommended to adapt to changing trends and patterns in financial data.
