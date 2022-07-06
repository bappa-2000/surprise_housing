# Surprise Housing - Regression Model
A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price. For the same purpose, the company has collected a data set from the sale of houses in Australia. 

The company is looking at prospective properties to buy to enter the market. I am required to build a model in order to predict the actual value of the prospective properties and decide whether to invest in them or not.

The company wants to know:
* Which variables are significant in predicting the price of a house, and
* How well those variables describe the price of a house.

Also, determine the optimal value of lambda for ridge and lasso regression.


## Table of Contents
* [General Info](#general-information)
* [Libraries/Packages Used](#libraries-packages-used)
* [Conclusions](#conclusions)

## General Information
- The project uses train.csv as the source data set. 
- We need to create Ridge and Lasso regression models to identify the variables that are significant in predicting the price of a house, intrepret the impact of those variables on the price and determine the optimial value of lambda for ridge and lasso regression. 


## Libraries-Packages Used
- pandas library - version 1.3.4
- numpy library - version 1.20.3
- matplotlib library - version 3.4.3
- seaborn library - version 0.11.2
- statsmodels - version 0.12.2
- sklearn - version 0.24.2
  - Ridge and Lasso from sklearn.linear_model
  - StandardScaler from sklearn.preprocessing
  - train_test_split and GridSearchCV from  sklearn.model_selection
  - r2_score and mean_squared_error from sklearn.metrics


## Conclusions
- Significant features for prediction are:
  - GrLivArea
  - OverallQual_9
  - OverallQual_8
  - Neighborhood_Crawfor
  - Functional_Typ
  - OverallCond_9
  - Exterior1st_BrkFace
  - TotalBsmtSF
  - Neighborhood_Somerst
  - CentralAir_Y
- Some readings from the models:
  - GrLivArea: An increase of 1 sqft of the living area will increase the sale price by 1.09 (Ridge) to 1.11 (Lasso) times
  - Neighborhood_Crawfor: If Crawford is a nearby location to a house, the sale price of house will increase by 1.07 to 1.09 times
  - OverallQual_8: If the overall material and finish of the house is "Very Good", the sale price will increase by 1.08 to 1.11 times. In case of OverallQual_9 ("Excellent"), the sale price will increase by 1.08 to 1.14
  - Functional_Typ: For a house with "Typical Functionality", the sale price will increase by 1.06 to 1.08 times
  - Exterior1st_BrkFace: For a house with "Brick Face" exterior covering, the sale price will increase by 1.06 to 1.07 times.
  - TotalBsmtSF: An increase of 1 sqft of basement area will increase the sale price by 1.04 times
- Optimal Lambda Value
  - Ridge: 9
  - Lasso: 0.001


