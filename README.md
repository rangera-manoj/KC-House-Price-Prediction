# King-County-House-Price-Prediction
The  house price prediction of King-County based on the data 'KC_Housesales_Data' from kaggle

Basic Predictive Modeling using different Machine Learning Algorithms(RandomForestRegressor, XGBRegressor, KNeighborsRegressor) and Parameter tuning using GridSearchCV and RandomizedSearchCV.

## Feature importance and Model Training
first we find out the feature importance of every feature in our dataset using correlation matrix, then train the model for 3 highly correlated features and by adding 1 feature and train the model corresponding to it and do it by adding every feature. then find out the maximum R2-score and corresponding to that features and tune the model on only that features and improve the performance of the model. 

## 1. RandomForestRegressor
selecting fetures which give maximum model score and after that tune model corresponding to that features.

Max R2-Score = 0.853603

cols_rf =                        ['sqft_living','grade','sqft_above','sqft_living15','bathrooms','view','sqft_basement','bedrooms','lat','waterfront','floors','yr_renovated','sqft_lot','sqft_lot15','yr_built','condition','long','year']

### RandomForestRegressor fine-tunning
MAE: 69115.63485263214

MSE: 16485435443.318863

RMSE: 128395.62081052011

R-squared score: 0.8688127402530751

### best model hyperparameters
{'max_depth': None, 'max_features': 0.5, 'min_samples_leaf': 1, 'min_samples_split': 5, 'n_estimators': 400}

## 2. XGBRegressor
selecting fetures which give maximum model score and after that tune model corresponding to that features.

Max R2-Score = 0.855639

cols_xgb = ['sqft_living','grade','sqft_above','sqft_living15','bathrooms','view','sqft_basement','bedrooms','lat','waterfront','floors','yr_renovated','sqft_lot','sqft_lot15','yr_built','condition','long','year']

### XGBRegressor fine-tunning
MAE: 64405.91650993441

MSE: 12395531673.783403

RMSE: 111335.22207182866

R-squared score: 0.9013592428916465

### best model hyperparameters
{'learning_rate': 0.1, 'max_depth': 5, 'n_estimators': 500, 'reg_lambda': 10.0}

## 3. KNeighborsRegressor
selecting fetures which give maximum model score and after that tune model corresponding to that features.

Max R2-Score = 0.783069

cols_knn = ['sqft_living','grade','sqft_above','sqft_living15','bathrooms','view','sqft_basement','bedrooms','lat','waterfront','floors','yr_renovated','sqft_lot','sqft_lot15','yr_built','condition','long']

### KNeighborsRegressor fine-tunning
MAE: 89896.66655643741

MSE: 25852651824.071915

RMSE: 160787.5984772206

R-squared score: 0.7942706116770583

### best model hyperparameters
{'n_neighbors': 7}

## dataset
The dataset for this project originates from the UCI Machine Learning Repository. It serves to show a basic trend in the house pricing in terms of its location, the area of construction, its interior, etc.

Raw dataset is available into this repository as kc_house_data.csv and cleaning dataset as df_final.csv
