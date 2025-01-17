## [House Prices - Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques)
> Predict sales prices and practice feature engineering, RFs, and gradient boosting

### Jupyter Notebook Versions

| Notebook Name            |   Model   |
|         :---:            |   :----:  |
| HousePrices - Solution 1 | ElasticNet + XGBRegressor |
| HousePrices - Solution 2 | Blended Model with StackingCVRegressor |

### Input Data
- Training set (train.csv)
  - Features: house conditions
  - Label: sale prices
- Test set (test.csv)\
  Same features as in the training set without label (to be predicted)

### Feature Engineering
- Features with high percentage of missing were dropped (more than 30%)
- Missing values were filled with mean values (continuous features) and majority values (categorical features)
- The Sale Price and many continous feature are skewed, data scaling were applied using log1p and boxcox1p functions

### Machine Learning Model
Multiple models tested in **HousePrices - Solution 1** and **HousePrices - Solution 2**:
- ElasticNet
- XGBoostRegressor
- ElasticNet + XGBoostRegressor
- LGBMRegressor
- XGBRegressor
- RidgeCV
- SVR
- GradientBoostingRegressor
- RandomForestRegressor
- StackingCVRegressor optimized by XGBRegressor

### Performance
- Best model with tuned parameter: **Blended Model with StackingCVRegressor**
- Best score (RMSE of log(y-y_pred)) on the evaluation dataset: **0.11880**
- Best rank on the leaderboard: **top 4%**
