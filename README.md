# creditcard_default
Build a model to predict the likelihood of default, a model which can generalize to
other data points. The column to be predicted is `default payment next month`
In this data set,Follwing data features are provided
X1: Amount of the given credit (NT dollar): it includes both the individual consumer credit and his/her family (supplementary) credit.
X2: Gender (1 = male; 2 = female).
X3: Education (1 = graduate school; 2 = university; 3 = high school; 4 = others).
X4: Marital status (1 = married; 2 = single; 3 = others).
X5: Age (year).
X6 - X11: History of past payment. We tracked the past monthly payment records (from April to September, 2005) as follows: X6 = the repayment status in September, 2005; X7 = the repayment status in August, 2005; . . .;X11 = the repayment status in April, 2005. The measurement scale for the repayment status is: -1 = pay duly; 1 = payment delay for one month; 2 = payment delay for two months; . . .; 8 = payment delay for eight months; 9 = payment delay for nine months and above.
X12-X17: Amount of bill statement (NT dollar). X12 = amount of bill statement in September, 2005; X13 = amount of bill statement in August, 2005; . . .; X17 = amount of bill statement in April, 2005. 
X18-X23: Amount of previous payment (NT dollar). X18 = amount paid in September, 2005; X19 = amount paid in August, 2005; . . .;X23 = amount paid in April, 2005.

Steps followed in this project
1.As a first step,Data analysis was done and data cleaning and feature engineering was done on the data and the modeled data was written into an excel file (Generic ETL process was followed).The data that we are dealing is of imbalanced class
2.The written excel file was then passed as input to different machine learning models, and their results were interpreted.
3.For model,I started of with Randomforest classifier ,XGboost and logistic regression model.
4.For each model of Randomforest and Xgboost,three iterations were followed.They are Undersampling,oversampling and all of given data.
5.After modeling,it was found that the Xgboost with all of data was performing well.The evaluation was solely based on recall score and AUC score and not accuracy score as we are dealing with imbalanced data set.The reason for recall score is that we do not want to predict more false negatives as the bank will lose money in case of default.
