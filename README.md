# Facebook-Comment-Volume-Prediction

## Problem Statement

Data in the social networking services is increasing day by day. So, there is heavy requirement to study the highly dynamic behavior of the users towards these services. The task here is to estimate the comment count that a post is expected to receive in next few(H) hours. Data has been scraped from one of the most popular social networking sites - Facebook.

## Dataset Source Link

https://archive.ics.uci.edu/ml/datasets/Facebook+Comment+Volume+Dataset

## Approach

- Cleaning the data [Adding feature names, Dropping static columns, Standardization(Optional)]
- Merging the training data variants
- Using Hold Out Cross Validation to split training data into train and test data. Test Cases provided are used as validation set
- Performing regression using following techniques-
  - Linear Regression
  - Decision Tree Regressor
  - Random Forest Regressor (BEST MODEL)
  - XGB Regressor
- Determining Feature Importances 

Note: 
1. Regression techniques like SVR due to their extensive memory requirement and hence are not suitable for large dataset.
2. Even though Random Forest Regressor gave the best results from the selected algorithms, it still is not able to extrapolate the information gained on unseen data.

## Evaluation Metric

- For the given problem statement, I have chosen Root Mean Squared Error and Mean Squared Error as my evaluation metric as the goal is not to predict the exact number of comments a facebook post receives but a value which can be used as a target value by business users to monitor their page engagement rate.
- Since RMSE/MSE metric greatly penalizes outlier values, I have chosen the given metric as the dataset consists of very few values which are not really outliers but have an effect on regression models.

## Inferences

- Through this project we have inferred that contrary to popular beliefs, the number of post likes and page visitors are not influential features when determining the predicting the number of facebook comments. 
- Instead the share count is one of the important features. Talking from a business perspective, while likes determine the reach of a post, the share count is an important metric which determines the reach and engagement rate.
- The base time selected is another important feature for determining the number of comments a post receives. The base time and share count combined will determine how often a post trends and in view on the audiences feed.
- Another important feature is C2: Comment count in last 24 hrs with respect to selected base date/time

## Research Paper Link

Do give the below research paper from which this project was inspired a read as well. It uses a different and more advanced approach.
https://ijssst.info/Vol-16/No-5/paper16.pdf
