# Ames Housing Data and Kaggle Challenge

---

## Table of Contents

1. [Problem Statement](#Problem-Statement)
2. [Preprocessing and Modeling](#Preprocessing-and-Modeling)
3. [Conclusion and Recommendations](#Conclusion-and-Recommendations)
4. [Datasets](#Datasets)

---

## Problem Statement

There are many things to consider when a person is looking for a home or a homeowner is looking to sell. In this analysis we must find the features that most impact a home's sale price.

---

## Preprocessing and Modeling

Data cleaning included dummying and binarizing numerical features, missing data was imputed, and unwanted features were dropped. There were a few outliers within the dataset and only the extreme outliers were dropped. 

The models used were Linear Regression, Lasso, and Ridge. In addition, these models were also tested with a transformed target value to create a normal distribution for the target. First, a basline model was established using a dummy regressor, then the models were run to find the best scores.

|Model             |R2 traing score   |R2 testing score  |Average Cross Val Score    |
|---               |---               |---               |---                        |
|MLR               |0.928             |0.902             |0.832                      |
|Lasso             |0.925             |0.905             |0.873                      |
|Ridge             |0.928             |0.903             |0.851                      |

---

## Conclusion and Recommendations

The Lasso model performed the best with a testing score of .91, and cross val score of .87. The ultimate sale price of a home is highly dependent upon the neighborhood, total square footage, the number of basement bathrooms, the number of main floor bathrooms, the overall quality of the property, the number of fireplaces, and having a paved driveway, all of which are positively correlated with the sale price. The Lasso model is able to predict most sale prices plus or minus $24699.36.

---

## Datasets

* [test.csv]('../data/test.csv'): Testing Data 
* [train.csv]('../data/train.csv'): Training Data
* [clean_test.csv]('../data/clean_test.csv'): Testing Data Cleaned
* [clean_train.csv]('../data/clean_train.csv'): Training Data Cleaned
* [lr_submission.csv]('../data/lr_submission.csv'): Linear Regession Kaggle Submission
* [lasso_submission.csv]('../data/lasso_submission.csv'): Lasso Regession Kaggle Submission
* [ridge_submission.csv]('../data/ridge_submission.csv'): Ridge Regession Kaggle Submission
