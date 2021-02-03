# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 2: Ames Housing Data and Kaggle Challange

Dominika Jones 

### Problem Statement

The purpose of this analysis is to construct a regression model that will predict the house sale prices as accuratley as possible. For best results I will compare three models based on their prediction scores: Linear Regression Model, Ridge Regression Model, and Lasso model. 

The data used for this project was Ames Housing Data which included a training and testing datasets.
The training dataset included 2051 observations (houses) 80 features and the Sale Price of each obversation. The testing dataset had the same 80 features but exluded the Sale Price and had 878 houses observed. 

The goal is to evaluate all the features and datermine which are stronly correlated with the sale prices and what variables will increase the models' prediction scores. 

---

### Datasets


* [`train.csv`](./data/train.csv): Ames House Prices ([source](https://www.kaggle.com/c/dsir-1019-project-2-regression-challenge/data))
* [`test.csv`](./data/test.csv): Ames House Prices ([source](https://www.kaggle.com/c/dsir-1019-project-2-regression-challenge/data))


--- 

### The Process

- Data Cleaning
- EDA
- Exploratory Visuals
- Model Prepping
- Model Fitting 

### Models Used

- Linear Regression
- Ridge Regression
- Lasso Regression 

---


### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|saleprice|int|train|Sale Price of each house in USD| 
|gr_liv_area|int|train/test|Above grade (ground) living area in square feet|
|total_baths|float|train/test|Total number of bathrooms in the house (full and half bathrooms)|
|has_bsmt|int|train/test|Indicates if the house has a basement included or not|
|has_fireplace|int|train/test|Indicates if the house has a fireplace(s) included or not|
|has_2nd_flr|int|train/test|Indicates if the house has a 2nd floor included or not|
|house_age|int|train/test|The age of the house at time of sale|
|remod_age|int|train/test|The time of when the house was remodeled at time of sale|

---


**Outside Research**
- https://www.homelight.com/ames-ia/housing-market
- CityData.com/city/Ames-Io


### Conclusion and Recommendation

When comparing the three models and their RMSE, the Lasso model had the lowest RMSE score (very small difference). The high RMSE score most likely means that the models were overfitted. However, compared to the baseline, the models had the smaller RMSE. I believe the models would make a better prediction if the neighboorhood feature was not dummified since it only added numerous uncorrelated variables that decreased the effectives of the models.

The variable that is most reliable feature that increases the sale price is above grade (ground) living area square feet, 'gr_liv_area. That would be expected as the sale price of real estate property is strongly corrareled with its living space. The neighborhoods had the lower correlation with the price as well as having a second floor. We can confidently conclude that home buyers prefer one level houses with larger lviing area.

Other variables such as pool or basement made little to no difference in the prediction. Having a basement or its ordinal features made little difference when predicting the price since almost every house in the data had a basement. Pool was the opposite, it was a feature only a few houses had.


### Includes: 

1. 1_cleaning.ipynp 
2. 2_eda.ipynp
3. 3_models.ipynp
4. data folder - contains the original datasets and cleaned/saved versions of the datasets
5. model scores - contains datasets of the model scores for the keggle competition