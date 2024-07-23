# Flood Prediction Model for Kerala
## Overview
This project aims to predict the occurrence of floods in Kerala using historical rainfall data. Various machine learning models were implemented and evaluated to identify the most effective model for predicting floods based on different sets of monthly rainfall data.

## Data
The dataset used in this project is kerala.csv, which contains the following columns:

1. SUBDIVISION: Name of the subdivision
2. YEAR: Year of the data
3. JAN to DEC: Monthly rainfall data
4. ANNUAL RAINFALL: Total annual rainfall
5. FLOODS: Indicator if floods occurred in the year (YES or NO)
## Steps and Methodology
### 1. Data Import and Preprocessing
Imported necessary libraries: numpy, pandas, seaborn, matplotlib
Loaded the dataset and displayed basic statistics using head(), columns, and describe()
Transformed the target variable FLOODS into binary numbers (1 for YES, 0 for NO)
Calculated the correlation matrix and visualized it using a heatmap to identify relationships between variables
### 2. Feature Selection
Used SelectKBest with the chi2 score function to select the top 3 features most correlated with the target variable FLOODS
Identified MAY, JUN, and SEP as the most significant features
### 3. Model Building and Evaluation
Split the data into training and testing sets using train_test_split
Implemented and evaluated three machine learning models: K-Nearest Neighbors (KNN), Logistic Regression, and Random Forest
Used metrics such as F1 score, ROC AUC score, and Cross-Validation score to evaluate the models
### 4. Insights and Findings
1. Logistic Regression performed the best overall with balanced performance across all metrics
2. Random Forest and KNN exhibited overfitting, as indicated by the disparity between cross-validation scores and test set scores
3. Evaluated the performance of Logistic Regression using different subsets of the data (quarterly and half-yearly data) to understand the impact of incomplete data on prediction accuracy
### Key Results
Logistic Regression is the most suitable model for predicting floods in this dataset
Second quarter data (April, May, June) is most predictive when full-year data is not available, likely due to the significant correlation between these months' rainfall and annual rainfall
