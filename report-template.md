# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

The purpose of the analysis was to build and evaluate machine learning models capable of predicting credit risk. Using historical lending activity data from a peer-to-peer lending services company, we aimed to classify the creditworthiness of borrowers, thereby predicting the likelihood of default.

The dataset contained financial information such as loan size, interest rate, borrower income, debt-to-income ratio, number of 
accounts, derogatory marks, and total debt. Our target variable was loan_status, which indicates whether a loan is healthy (0) or 
has a high risk of defaulting (1).

## Several stages of the machine learning process, including:

Data preprocessing, where we split the data into features and labels.
Splitting the data into training and testing sets to ensure model validation.

Implementing a Logistic Regression model to predict the loan status.
Resampling the training data using RandomOverSampler to address class imbalance.

We employed LogisticRegression from scikit-learn for our predictive model and RandomOverSampler for resampling to create balanced 
training data, which is crucial for addressing the imbalance in the dataset.


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
The model produced an accuracy score of 0.94.
Precision for predicting high-risk loans (1's) was 0.87, and for healthy loans (0's) was 1.00.
Recall for high-risk loans was 0.89, and for healthy loans was 1.00.



* Machine Learning Model 2:
The model produced an accuracy score of 0.99.
Precision for predicting high-risk loans (1's) was 0.87, and for healthy loans (0's) was 1.00.
Recall for high-risk loans was 1.00, and for healthy loans was 1.00.

## Summary

The analysis involved two machine learning models designed to predict credit risk. Both models were evaluated based on their accuracy, precision, and recall scores.

Machine Learning Model 1 utilized the original dataset. It achieved a high accuracy score of 0.94, demonstrating its ability to correctly identify most loans as either high-risk or healthy. The precision was excellent for healthy loans and very good for high-risk loans, indicating a low number of false positives in both cases. The recall scores were equally impressive, particularly for healthy loans, suggesting that the model was able to identify the majority of actual positive cases correctly.

Machine Learning Model 2 was developed using resampled data to correct for imbalances in the training set. This model showed a remarkable improvement in overall accuracy, achieving a near-perfect score of 0.99. Notably, the precision scores were identical to those of Model 1, but the recall for high-risk loans reached 1.00, indicating that every actual high-risk loan was correctly identified by the model. There were no false negatives for high-risk loans in Model 2.

Given the critical nature of predicting high-risk loans accurately to avoid financial losses, the improvement in recall for high-risk loans without any loss in precision is significant. Machine Learning Model 2 outperforms the first model, particularly in its recall for high-risk loans, which is a crucial metric for a lending institution that aims to minimize the risk of default.

In conclusion, Machine Learning Model 2 is the recommended model for identifying credit risk. Its perfect recall for high-risk loans ensures that all potential defaults could be flagged for further review, potentially saving the company from significant financial hardship. The consistent precision across both models also ensures that the number of false positives remains low, which is important for maintaining customer relations and avoiding unnecessary reviews of healthy loans.
