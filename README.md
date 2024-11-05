# FutureIntern_DS_01
![image](https://github.com/user-attachments/assets/2713d922-7a13-4a37-98c9-4f6284c3e43d)


# Credit Card Fraud Detection


# Overview

This project aims to build a machine learning model to detect fraudulent credit card transactions, using a dataset of anonymized transaction data. Fraud detection is critical for financial institutions to protect users and mitigate financial loss due to unauthorized transactions. This project focuses on accurately identifying fraudulent transactions despite the highly imbalanced nature of the dataset.


# Table of Contents

         Project Structure

         Business Understanding

         Data Understanding

         Exploratory Data Analysis (EDA)

         Data Preprocessing

         Modeling

         Evaluation

         Results and Insights

         Conclusion


Project Structure

creditcard.csv/: Contains the dataset file

notebooks/: Jupyter notebooks for EDA, modeling, and results.

src/: Python scripts for preprocessing, model training, and evaluation.

README.md: Project documentation.


# Business Understanding

Credit card fraud detection is essential for reducing financial losses for both institutions and customers. Fraudulent transactions are challenging to identify due to the high imbalance in data, with only a tiny fraction of transactions being fraudulent. This project aims to:

     Build a model that accurately distinguishes between fraudulent and legitimate transactions.

     Explore techniques for handling imbalanced data.

     Provide actionable insights on fraud detection strategies.



# Data Understanding

The dataset consists of 284,807 credit card transactions with the following columns:

    Time: The elapsed time since the first transaction.
     
     V1 - V28: Anonymized transaction features derived from Principal Component Analysis (PCA).

    Amount: The transaction amount, which can be a distinguishing factor for fraud.

    Class: The target variable, where 1 indicates fraud and 0 indicates a legitimate transaction.


# Key Insights

The dataset is highly imbalanced, with only 0.17% of transactions marked as fraudulent.

Features V1 to V28 are already scaled, while Amount and Time are not.


# Exploratory Data Analysis (EDA)

Key steps and findings from the EDA include:

    Class Imbalance: Visualization and quantification confirm a severe imbalance in the target classes.

    Transaction Patterns: Analysis of Amount and Time features for potential patterns related to fraud.

    Correlation Analysis: Review of the PCA components (V1 to V28) for any useful associations.

    Distribution of Features: Investigation into whether fraud and non-fraud transactions display different statistical patterns.


# Data Preprocessing

    Handling Imbalance: Techniques like SMOTE (Synthetic Minority Over-sampling Technique) or undersampling were considered to balance the dataset.

    Scaling: Normalization was applied to Amount and Time for consistency with other features.

    Splitting: The dataset was split into training and test sets to evaluate the model performance.


# Modeling

Several classification models were tested to identify the best performer:

    Logistic Regression: Baseline model for comparison.

     Random Forest: Ensemble model to capture complex interactions.

    Neural Network: Deep learning approach for complex feature interactions.


# Evaluation

The models were evaluated using the following metrics:

Confusion Matrix: To visualize true positives, false positives, true negatives, and false negatives.

Precision, Recall, F1-Score: Recall was particularly prioritized for fraud detection, as missing a fraud is more costly than a false positive.

ROC-AUC Score: Evaluated model's discriminatory ability for fraud detection.


# Results and Insights

The [Best Model] achieved a balance between recall and precision, with a high ROC-AUC score, indicating effective fraud detection without excessive false positives.

Feature Insights: Some features (like Amount and specific PCA components) displayed notable variations between fraud and non-fraud transactions, suggesting these features' 
importance in identifying fraud.


# Conclusion

This project successfully identified fraudulent transactions with high accuracy, focusing on recall to avoid missing fraud cases. The final model provides a valuable tool for flagging suspicious transactions, and the analysis offers insights that could guide further improvements.


# Future directions could involve:

Real-time Detection: Adapting the model to work with streaming data for real-time fraud detection.

Feature Engineering: Further analysis of interaction terms between features for more detailed insights.

Deployment: Creating an API or a deployment pipeline to integrate the model into financial systems.
