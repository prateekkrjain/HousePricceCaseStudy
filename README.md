# House Prices Case Study
> To build regression models to understand the factors which influence the house prices and how well the factors describe the price of a house.

## Table of Contents
* [General Info](#general-information)
* [Dataset Details](#dataset-details)
* [Methodology](#methodology)
* [Conclusions](#conclusions)
* [Technologies Used](#technologies-used)
* [Contact](#contact)
* [License](#license)

## General Information
> Client is looking to expand to Australlian markets and want to buy the properties at the lower prices, so, that those can be later sold at higher prices.
> For the same, client wants to understand the following:
+ Which variables are significant in predicting the price of a house, and
+ How well those variables describe the price of a house.

> It is expected to build the regression models to understand the factors which influence the house prices.

## Dataset Details
> Details of the features are mentioned in "data_description.txt"

## Methodology

> Following steps were implemented:
- EDA:
    - Fix data types
    - Remove outliers
    - Fix null values
- Modeling:
    - Split the data into Train and Test datasets
    - Create modeling pipeline
        + Create Polynomial features (number of degrees is a hyper-parameter tuned via Grid search)
        + Standardize numerical features
        + One hot encode categorical features
        + Ridge or Lasso model  
    - Run GridSearch: to find the optimal parameters like lambda/alpha values of Ridge or Lasso Regression
    - Hyper-parameters checked for:
        - Lambda/Alpha: the penalty term for Lasso or Ridge regression
        - Degrees: Polynomial Degress of features to be created
- Evaluation:
    - Evaluate performance on Train and Test datasets
    - Check Feature importances
    - Residual Analysis
        - Check for Normality of Residuals
        - Check Predictions vs. Residuals, to check for any patterns or homoscedasticity

## Conclusions
+ Ridge has higher accuracy on Test data which is 86%.
+ Lasso has lower accuracy on Test as compared to Ridge, which is 84%.
+ But, Lasso regression has found and set 50 features as redundant i.e. set their coefficients as 0, while Ridge only set for single feature.
+ Since, the purpose of this case study is to understand the influential factors, it is best to use Lasso Regression as compared to Ridge regression.

## Technologies Used
- Python - version 3.8.3
- Numpy - version 1.18.5
- Pandas - version 1.0.5
- Seaborn - version 0.11.0
- Wordcloud - version 1.8.1
- Matplotlib - version 3.2.2
- Statsmodel - version 0.11.1

## Contact
Created by [@prateekkrjain](http://prateekkrjain.com) - feel free to contact me!)
