# PredictiveModelingForElections

This project aims to predict the outcomes of US county-level elections using various machine learning models. The focus is on data preprocessing, model evaluation, tuning, and generating final predictions while addressing the challenges of imbalanced datasets.

## Table of Contents

- [Introduction](#introduction)
- [Data](#data)
- [Preprocessing](#preprocessing)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Results](#results)
- [Conclusion](#conclusion)
- [Future Work](#future-work)

## Introduction

This project utilizes demographic and voting data to build predictive models for election outcomes. The primary goal is to achieve high accuracy in predicting whether a county is won by a particular candidate.

## Data

The dataset includes:
- Total votes cast in each county (`total_votes`)
- Total population estimate (`0001E`)
- Population 25 years and over with a high school degree or higher (`C01_014E`)
- Median age of the population (`0018E`)
- Percentage of the white population (`0037PE`)

## Preprocessing

Key preprocessing steps:
- Handling missing values
- Feature engineering (e.g., creating percentage features for demographics)
- Standardizing numerical features
- Encoding categorical variables

## Modeling

The following models were evaluated:
1. Generalized Linear Model (glm)
2. K-Nearest Neighbors (knn)
3. Random Forest (rf)
4. Support Vector Machine with Radial Kernel (svmRadial)
5. Gradient Boosting Machine (gbm)
6. Tuned Random Forest (rf_tuned)

## Evaluation

Models were evaluated using v-fold cross-validation with accuracy and Kappa as metrics. Hyperparameter tuning was performed for the Random Forest model.

## Results

The tuned Random Forest model achieved the highest accuracy and was selected for generating final predictions.

| Model       | Accuracy | Kappa   |
|-------------|----------|---------|
| glm         | 0.9019   | 0.6123  |
| knn         | 0.9121   | 0.6420  |
| rf          | 0.9186   | 0.7064  |
| svmRadial   | 0.9202   | 0.6874  |
| gbm         | 0.9212   | 0.6713  |
| rf_tuned    | 0.9239   | 0.7000  |

## Conclusion

The Random Forest model with tuned hyperparameters was selected as the final model due to its superior performance. 

