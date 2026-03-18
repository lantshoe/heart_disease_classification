# Heart Disease Prediction / Classification Project

# Project Approach & Lessons Learned

Initially, I built and compared several models (XGBoost, MLP, Logistic Regression) using the dataset.

Despite proper preprocessing and attempts to balance the data (SMOTE), the models failed to achieve good performance, especially for predicting heart disease (class 1).

This led me to question the dataset quality. I then performed exploratory data analysis (EDA) to investigate:

Weak correlations between features and target

Significant class imbalance and missing values

Lesson learned: Performing EDA before building models is crucial — understanding data quality and structure can save time and provide insights into whether ML models are likely to succeed.

## 1. Project Overview

Objective: Predict whether a patient has heart disease based on clinical and lifestyle features.
Note: The dataset has significant limitations, which we explore in this project.

## 2. Dataset
https://www.kaggle.com/datasets/oktayrdeki/heart-disease/data

## 3. Data Analysis (EDA)

Plotted correlation heatmap and KDE plots for numeric features.

Observations:

Most features show weak correlation with the target.

KDE plots show heavy overlap between classes, indicating low separability.

Class imbalance: 0 (No Heart Disease) is much more frequent than 1 (Yes).

## 4.Preprocessing

Handled missing values:

- Option 1: Drop rows with missing values (current branch)
- Option 2: Fill with “Unknown” or mode (future experiments)

Converted categorical features to numeric (0 / 1 or 0 / 1 / 2 for multi-class).

Tried SMOTE to balance the training data (planned in a separate branch).

## 5. Model Experiments

Algorithms test

Observations:
- Models perform poorly due to weak predictive signal 
- Even after balancing the data, recall for class 1 (heart disease) remains very low.
