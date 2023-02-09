# PREDICTION-OF-CRIMES


# Project Description

## Data Set Information:

Many variables are included so that algorithms that select or learn weights for 
attributes could be tested. However, clearly unrelated attributes were not included; 
attributes were picked if there was any plausible connection to crime (N=122), plus 
the attribute to be predicted (Per Capita Violent Crimes). The variables included in 
the dataset involve the community, such as the percent of the population considered 
urban, and the median family income, and involving law enforcement, such as per capita 
number of police officers, and percent of officers assigned to drug units.

The per capita violent crimes variable was calculated using population and the sum of 
crime variables considered violent crimes in the United States: murder, rape, robbery, 
and assault. There was apparently some controversy in some states concerning the 
counting of rapes. These resulted in missing values for rape, which resulted in 
incorrect values for per capita violent crime. These cities are not included in the 
dataset. Many of these omitted communities were from the midwestern USA.

Data is described below based on original values. All numeric data was normalized into 
the decimal range 0.00-1.00 using an Unsupervised, equal-interval binning method. 
Attributes retain their distribution and skew (hence for example the population 
attribute has a mean value of 0.06 because most communities are small). E.g. An 
attribute described as 'mean people per household' is actually the normalized (0-1) 
version of that value.

The normalization preserves rough ratios of values WITHIN an attribute (e.g. double 
the value for double the population within the available precision - except for 
extreme values (all values more than 3 SD above the mean are normalized to 1.00; all 
values more than 3 SD below the mean are nromalized to 0.00)).

However, the normalization does not preserve relationships between values BETWEEN 
attributes (e.g. it would not be meaningful to compare the value for whitePerCap with 
the value for blackPerCap for a community)

A limitation was that the LEMAS survey was of the police departments with at least 100 
officers, plus a random sample of smaller departments. For our purposes, communities 
not found in both census and crime datasets were omitted. Many communities are missing 
LEMAS data.



## Objective
The project had **2 distinct objectives**:
1. Derive **statistically significant insights** from a database.
2. Model a **regression analysis** for a variable (in this project, we have chosen to do use the linear regression to predict the probability of a crime to happen in a given date with some given circunstances.)





### Task performed
- importing required models
- Uploading datasets
- performing EDA
- Removing and combining the data
- Feature extractions
- Model selection and implementing the best model
- Predicting and visualing



### steps we did in this project
- Uploading the datasets
- Cleaning and converting the data types
- correlation between target variable and all features
- Preprocessing the data
- Encoding 
- spliting the data
- Model selection and implementing the best model
- Feature selection
- Regression using dimensionality reduction on features
- Models used : Linear Regression, Support Vector Regression using Grid Search, K Nearest Neighbors using Grid Search, Gradient Boosting using Grid Search, MLP using Grid Search
- Performing of best model on test set
- Predicting and visualing the results...




### Analysis
#### Result analysis:

- Root mean squared errors are generally low due to normalized target variable.
SVR, MLP and gradient boosting algorithms perform well with this data. Linear regression performs the worst and is too simple a model for this data.
As expected, for different train-test sets, SVR worked best when using all 100 features for regression.
- Feature selection using correlation works best overall. However, it's performance worsens if the number of features is too low due to loss of important information within the smaller subset of features.
- For the dimensionality reduction case, as expected, SVR performs best when number of features is set higher, whereas MLP works better when number of features is set lower. 
- Overall, dimensionality reduction using PCA gave the worst results among the three methods used.
The algorithms perform decently on the test set but relatively poorly compared to the training set. Overall, I would choose SVR algorithm with feature selection based on correlation for regression on this dataset as it has consistently given the best performance over multiple iterations of regression.
Extending the regression analysis:

- Look further into multicollinearity, and further refine feature set by removing features with high collinearity. Also explore other methods of feature selection.
More thorough grid search (or random search) for hyperparameters, and error analysis to compare the movement of training and testing errors.
- Increase number of splits in k-fold cross validation for more stable and consistent results.
- If possible, collect more data samples, and information on missing values. Plus work with unnormalized data.






## 🏗️ Built with
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)



## 👩‍💻 Libraries used
![Pandas](https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=purple)
![Numpy](https://img.shields.io/badge/Numpy-777BB4?style=for-the-badge&logo=numpy&logoColor=yellow)
![Matplotlib](https://img.shields.io/badge/Matplotlib-F7931E.svg?style=for-the-badge&logo=Matplotlib&logoColor=orange) 
![seaborn](https://img.shields.io/badge/Seaborn-2C2D72?style=for-the-badge&logo=Seaborn&logoColor=blue)
![scikitLearn](https://img.shields.io/badge/scikitLearn-2C2D72?style=for-the-badge&logo=scikitLearn&logoColor=blue)



### Important models were used in this project:

- OneHotEncoder
- train_test_split
- metrics - mean_squared_error
- LinearRegression
- KNeighborsRegressor
- SVR
- GradientBoostingRegressor
- MLPRegressor
- Principle Compound Analysis
- train_test_split 
- GridSearchCV
- KFold
- cross_val_score





## Find the datasets From Chicago Data Portal here 
https://data.cityofchicago.org/

https://data.cityofchicago.org/browse?limitTo=datasets



## Organization
-  you may find the main Python Notebooks produced by the team members to realize the analysis, visualisations and predictive models.

Repository --------(https://github.com/hariramgit/PREDICTION-OF-CRIMES/blob/master/crime_regression_analysis.ipynb)

- *Group project.* 
HARIRAM

PALLAVI SHARMA

NIKITHA



* [Email](mailto:hariramhdmp@gmail.com)



## 🤝 Support
Contributions, issues, and feature requests are welcome!
Give a STAR if you like this project! and FOLLOW do SUPPORT Friends.

