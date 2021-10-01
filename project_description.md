# Predicting the Domestic Box Office Gross of the film

## Abstract

The goal of this project is to use linear regression model to predict the domestic box office gross of the film based on factors known before it is released. 
The main question will be:
1. What factors affect the domestic box office gross?
2. How do these factors affect it? How does the change in one of them changes the target?

## Design

In order to accomplish this data needs to be obtained from BoxOfficeMojo.com using web scraping. The data includes 1600 top grossing movies for the last 8 years. Data needs to be evaluated, cleaned and filtered. Some of the features will be dropped from analysis during initial eda.

## Data

The final dataset used for modeling contains 917 movies with 6 features, 2 of which are categorical. A few features removed at this stage to avoid collinearity issues.

## Algorithm

Data is splitted into train (80 percent) and test (20 percent) before dummy variables creation and feature engineering. Then 2 categorical fields transformed into binary dummy variables and model evaluated using Cross Validation. 

Initial Scores are: (0.50306615, 0.54855404, 0.53364658, 0.53056607, 0.49837769)

Feature engineering is performed on the model. 5 features created: 3 polynomial terms and 2 interaction terms. Cross Validation is performed after each feature is created.

Final Scores after feature engineering is done are: (0.65998075, 0.58696461, 0.70132508, 0.65017495, 0.64270971)

Model fitted using Linear Regression. The score is 0.6937576010108419

Testing - test data goes through the same process as train. Dummy variables created and initial scoring is done. 

The score before feature engineering - 0.5549083347918176

The score after feature engineering - 0.679166035007529

In attempt to improve results of our modeling regularization is performed. 

Lasso - suggested alpha value is 0.01 score is 0.5298218155044118

Ridge - suggested alpha value is 0.01 score is 0.5332018104674825

Results of regularization suggest that our Linear Model performs better than regularized one. We will continue to use the Linear Model approach for this project.

## Tools

- Numpy and Pandas for data manipulation\n
- Sklearn for modeling\n
- Statsmodels for evaluating individual characteristics of the model\n
- Matplotlib and Seaborn for plotting\n

## Communication

Graph below represents predicted vs actuals values for domestic box office gross. It will also be included in the presentation slides for this project.

![actual_vs_predicted](https://github.com/sambu2010/linear_regression_movies_analysis/blob/main/actual_vs_predicted.png)