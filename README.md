# RTR Review Prediction and Items Recommender

## Overview
### Goal
The goal of this project is to predict ratings on RentTheRunway and to recommend items based on user profile.

### Data
The dataset was downloaded from [UCSD Recommender Systems Datasets](https://cseweb.ucsd.edu/~jmcauley/datasets.html#clothing_fit) with total 190K reviews, 100K users on 5.8K items.

## Review Prediction
To predict the rating, we had the baseline model to be always predicting the mean rating. With that, we got a RMSE of 0.715. We also tried different regression algorithms: linear regression, decision tree and random forest. Random forest had the best performance RMSE 0.682.

| | Baseline | Linear Regression |  Decision Tree | Random Forest | 
| --- | --- |  --- | --- | --- |
| RMSE | 0.715 | 0.691 |  0.685 | 0.682 |

## Items Recommender
The recommender was built for new users.
1. New user inputs their height, weight, size and age.
2. Recommender searchs for the 100 most similar users in the database using cosine similarity.
3. Recommender returns the top 10 rated items based on similar users' ratings.
