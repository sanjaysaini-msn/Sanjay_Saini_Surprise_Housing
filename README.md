# Assignment Part-I 
A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price. For the same purpose, the company has collected a data set from the sale of houses in Australia. The data is provided in the CSV file below.

The company is looking at prospective properties to buy to enter the market. You are required to build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.

**The company wants to know:**

* Which variables are significant in predicting the price of a house, and
* How well those variables describe the price of a house.

Also, determine the optimal value of lambda for ridge and lasso regression.

**Business Goal**

You are required to model the price of houses with the available independent variables. This model will then be used by the management to understand how exactly the prices vary with the variables. They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.


## Table of Contents
* [General Information](#general-information)
* [Technologies Used](#technologies-used)
* [Steps involved to meet the goal](#steps-involved-to-meet-the-goal)
* [Conclusions](#conclusions)
* [Suggestions & Interpretation of the result](#suggestions)
* [Contributors](#contributors)


## General Information
- The project imports the data from train.csv. 
- The goal is to model the price of houses with the available independent variables. This model will then be used by the management to understand how exactly the prices vary with the variables
- Identify the indepandent feature's respective coefficient using Ridge Regression. 
- Identify the indepandent feature's respective coefficient using Lasso Regression. 
- Compare both regressions and select the most efficient model and most significant features.


## Technologies Used
- pandas library - version 1.3.4
- numpy library - version 1.20.3
- statsmodels - version 0.12.2
- sklearn - version 0.24.1
- matplotlib library - version 3.4.3
- seaborn library - version 0.11.2

## Steps involved to meet the goal
*    Data Load, understanding and exploration
*    Data cleaning
*    Data preparation
*    Model building and evaluation

## Conclusions
	- Variables/features that drives the prediction: ['OverallQual_9', 'GrLivArea', 'OverallQual_8', 'Neighborhood_Crawfor','CentralAir_Y', 'Neighborhood_Somerst', 'Functional_Typ', 'TotalBsmtSF','Exterior1st_BrkFace', 'Condition1_Norm']

	- The housing data is read and analyzed divided into numerical and categorical types.
	- The traget column of was `SalePrice`.
	- All the features are then analyzed, data handling for missing values, detected the outliers and date cleaned. SalePrice Trend is observed for change in various features.
	- Extracted New features, redundant features dropped and categorical features are splitted in to many other individual feature for beter performance and optimum preditons. Data splitted into train and test data and feature scaling was performed.
	- The traget column `SalePrice` was skiewed in right, so natural log was used for model building and natural log of `SalePrice` was considered.
	- Ridge and Lasso Regression Model are built with optimum alpha calculated in GridSearchCV method. Optimum alpha = 10.0 for ridge and 0.001 for lasso model.


## Suggestions & Interpretation of the result

	- Model evaluation is done with R2 score, RSS and Root Mean Square Error.
	- Lasso Regression is chosen as final model for having slightly better R-square value on test data.
	- Out of 50 features in the final model, top 10 features in order of descending importance are ['OverallQual_9', 'GrLivArea', 'OverallQual_8', 'Neighborhood_Crawfor','CentralAir_Y', 'Neighborhood_Somerst', 'Functional_Typ', 'TotalBsmtSF','Exterior1st_BrkFace', 'Condition1_Norm']
	- Predicted value of `SalePrice` is tranformed into its original scale by performing exponential (antilog).

## Contributors
- <a href="https://github.com/sanjaysaini-msn">Sanjay Saini</a>

