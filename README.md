# Airbnb Project

With the increasing global popularity of Airbnb, hosts, real-estate investors and other stakeholders are presented with an easily accessible opportunity to supplement or diversify their income streams through short-term rentals of their properties.

This project analyzed the most influential factors contributing to revenue generation, presenting patterns and insights from the available data to formulate a predictive model based on advanced machine learning techniques, generating insights for property owners and investors. 

__Highlights__
- __Machine Learning Methods:__ linear regression, Lasso regression, Ridge regression, Random Forests, XGBoost, LightGBM and Model stacking
- __Feature engineering__ was conducted for the different machine learning methods based on their characteristics and assumptions to maximise the predictive power of the models while maintaining reasonable computational costs.
- __Best model:__ model stacking
- __Data mining:__ based on feature importance, there were three features that most significantly influenced the price, the number of bedrooms, if the listing was for a private room, and the cleaning fee as a percentage of the listing price. 

## 2 Data Preprocessing
## 3 EDA
## 4 Feature Engineering
## 5 Models
### 5.1 Model Results
RMSE:
- Model Stacking: 0.325
- XGBoost: 0.326
- LightGBM: 0.327
- Random Forest: 0.355 
- Lasso: 0.391
- Ridge: 0.395

The model stack demonstrated the best generalisation performance, showing an improvement over the benchmark XGBoost model of 0.0014. This result suggests that the ensemble was able to improve the likelihood of achieving the best performance by combining the learning algorithms. One caveat, however, is that a complex meta-model may lead to overfitting concerns, thus affecting its performance on the test dataset. Therefore, this should be taken into account if the company wishes to continue using this model in the future.

## 6 Data Mining - Best Hosts
Of the three best performing non-ensemble models (XGBoost, LightGBM, random forest), three variables were identified as having the most importance: the cleaning fee of the listing as a percentage of the price, if the listing was for a private room, and the number of bedrooms within the listing. 

Of these three variables, the number of bedrooms had a feature importance rating of almost 100 in both the random forest and the XGBoost and is hence likely the most significant factor for hosts aiming to increase their listing price.

Then, used linear regression to further explore their relationships with price.

## 7 Future Works
1. find a better way to deal with missing values and explore the correlation between variables.
2. improve their data recording and scraping practices and obtain necessary information such as the occupancy rate of each house to answer the substantive question better
3. Try neural network: due to the nature of Airbnb's business, the data of the house is very stable, and there is no need for real-time training on the newly generated data. Therefore, Airbnb can use historical data to train neural networks offline, significantly reducing the level of required resources. 
4. the model can be improved by finely tuning more hyperparameters with the help of more computing resources.
