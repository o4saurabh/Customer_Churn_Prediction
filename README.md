# Customer_Churn_Prediction
Project Overview

This project focuses on predicting customer churn using machine learning techniques. The objective is to identify customers who are likely to leave the company, enabling businesses to take proactive retention measures.

The project includes complete data preprocessing, feature engineering, model comparison, evaluation, and prediction on new customer data.

Dataset Description

The dataset contains 10,000 customer records with the following features:

customer_id

credit_score

country

gender

age

tenure

balance

products_number

credit_card

active_member

estimated_salary

churn (Target Variable)

Target Variable:

0 → Customer did not churn

1 → Customer churned

Project Workflow
1. Data Preprocessing

Removed unnecessary columns (e.g., customer_id)

Handled missing values using:

Median imputation for numeric features

Most frequent imputation for categorical features

Applied standard scaling to numeric features

Used one-hot encoding for categorical features

2. Feature Engineering

Created additional features:

balance_per_product

salary_balance_ratio

age_group

tenure_bucket

high_balance

These engineered features improved model interpretability and performance.

3. Model Training

Compared multiple classification models:

Logistic Regression

Random Forest

Gradient Boosting

AdaBoost

Support Vector Classifier (SVC)

Used:

Stratified K-Fold Cross Validation (5 folds)

ROC-AUC as evaluation metric

4. Model Selection

Selected the best model based on mean ROC-AUC score from cross-validation.

The final model was trained on full training data and evaluated on test data.

Model Evaluation Metrics

Evaluated using:

Accuracy

Precision

Recall

F1-Score

ROC-AUC Score

Confusion Matrix

Classification Report

These metrics help assess both overall performance and performance on churned customers specifically.

Feature Importance

For tree-based models, feature importance was extracted to identify the most influential variables affecting churn.

Top contributing features were visualized using a bar plot.

New Customer Prediction

The project includes functionality to:

Accept new customer data

Apply the same feature engineering

Generate churn prediction

Output churn probability

This ensures real-world applicability of the trained model.

Technologies Used

Python

Pandas

NumPy

Scikit-learn

Matplotlib

Seaborn

Key Learnings

Importance of proper preprocessing pipelines

Preventing data leakage using sklearn Pipeline

Handling imbalanced datasets with StratifiedKFold

Using ROC-AUC for churn prediction problems

Interpreting model results using feature importance

Future Improvements

Hyperparameter tuning using GridSearchCV or RandomizedSearchCV

Threshold optimization for business-specific recall/precision tradeoff

Deployment using Streamlit or Flask

Integration with real-time data sources

Conclusion

This project demonstrates an end-to-end machine learning pipeline for customer churn prediction. It covers data preparation, feature engineering, model comparison, evaluation, and real-world prediction use cases.

The workflow follows industry best practices and is suitable for practical business implementation.
