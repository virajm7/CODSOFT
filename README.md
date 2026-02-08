TASK 1 
Bank Customer Churn Prediction
Introduction

This project focuses on predicting customer churn for a bank using historical customer data.
Customer churn refers to customers who stop using the bank’s services. Predicting churn helps banks take early action to retain customers.

This project is completed as Task 1 of the CODSOFT Machine Learning Internship.

Objective

The main objectives of this project are:

To understand the bank customer dataset

To analyze factors that influence customer churn

To build machine learning models to predict churn

To compare different models using suitable evaluation metrics

Dataset Description

The dataset contains information about bank customers, including demographic details and account-related data.

Target variable:
Exited
1 indicates the customer has left the bank
0 indicates the customer is still with the bank

Features Used

The following features were used for model training:

CreditScore

Geography

Gender

Age

Tenure

Balance

NumOfProducts

HasCrCard

IsActiveMember

EstimatedSalary

The following columns were removed because they do not help in prediction:

RowNumber

CustomerId

Surname

Exploratory Data Analysis

Exploratory data analysis was performed to understand the dataset.
Key observations include:

The dataset is moderately imbalanced

Customers from certain regions show higher churn

Older customers and inactive members tend to churn more

Customers with higher balances show a higher chance of leaving

Handling Class Imbalance

The target variable was imbalanced, with fewer churned customers.
To address this, SMOTE was applied only to the training data.
This helps the model learn churn patterns without affecting test data fairness.

Models Used

Logistic Regression
This model was used as a baseline. It is simple and easy to interpret but struggles with complex patterns.

Random Forest Classifier
This model captures non-linear relationships and performs better on churn prediction.

Model Evaluation

The models were evaluated using the following metrics:

Accuracy

Precision for churned customers

Recall for churned customers

F1-score

ROC-AUC score

Recall was given more importance because missing a churn customer leads to business loss.

Results Summary
Model	Accuracy	Recall (Churn)	F1-Score	ROC-AUC
Logistic Regression	0.80	Low	Low	0.77
Random Forest	0.86	Higher	Higher	0.86

Random Forest performed better in identifying churned customers.

Conclusion

Random Forest outperformed Logistic Regression in all important churn-related metrics.
It detected more churned customers and showed better overall performance.
This model can be used to help banks take preventive actions to reduce customer churn.
