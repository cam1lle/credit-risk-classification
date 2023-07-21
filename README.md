# Credit Risk Analysis Project
## Overview
In this project, I completed a credit risk analysis using machine learning models to predict the risk associated with borrowers' loans. The dataset provided financial information on borrowers, such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. The goal was to predict whether a loan is healthy (0) or has a high risk of default (1).

## Data and Methodology
The data was first loaded into a Pandas DataFrame, and I performed data preprocessing to separate the features and labels. To evaluate the class distribution, I used the value_counts() function to check the balance of the labels.

I created two machine learning models:

1. Logistic Regression Model with Original Data: I trained a logistic regression model using the original data. This model helped me understand the baseline performance and identify potential areas of improvement.
 <img width="470" alt="Screenshot 2023-07-21 at 5 15 15 PM" src="https://github.com/cam1lle/credit-risk-classification/assets/117128707/dadd3407-b1e2-4401-9ff2-c10d2ae2453d">
2. Logistic Regression Model with Resampled Data: To address the class imbalance issue in the dataset, I employed the RandomOverSampler from the imblearn library to resample the data. The logistic regression model was then trained on the resampled data.
<img width="457" alt="Screenshot 2023-07-21 at 5 15 34 PM" src="https://github.com/cam1lle/credit-risk-classification/assets/117128707/ccc5c6f4-bb90-47f5-880e-92d715a6b7e2">
## Results
Both models showed promising results in predicting credit risk. Here are the performance metrics:

Model 1: Logistic Regression with Original Data

Model 2: Logistic Regression with Resampled Data

## Summary and Recommendation
Model 2, the logistic regression model trained with resampled data, outperformed Model 1 in terms of balanced accuracy, precision, and recall scores. It demonstrated improved performance in predicting both healthy and high-risk loans, especially in identifying high-risk loans (label 1).

Considering the importance of correctly identifying high-risk loans to minimize potential losses due to default, I recommend using Model 2 for credit risk analysis. It provides better overall performance and effectively addresses the class imbalance problem.

To further enhance the model's performance, hyperparameter tuning and exploration of other machine learning algorithms could be considered. Additionally, continuous monitoring and model updates are recommended to adapt to changing trends and patterns in financial data.

## Usage
You can use the provided Jupyter Notebook and Python code to replicate the credit risk analysis. Ensure you have the necessary dependencies installed, including numpy, pandas, scikit-learn, and imbalanced-learn. The lending_data.csv file in the Resources folder contains the dataset used in this analysis.

Feel free to modify the code, experiment with different models, or use other data to conduct further credit risk analysis tailored to your specific needs.