## [House Prices - Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques)
> Predict sales prices and practice feature engineering, RFs, and gradient boosting

### Jupyter Notebook Versions

| Notebook Name            |   Model   |
|         :---:            |   :----:  |
| HousePrices - Solution 1 | ElasticNet + XGBoost |
| HousePrices - Solution 2 | Blended Model with Stacking Regressor |

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
- Elastic Net
- XGBoost Regressor
- Elastic Net + XGBoost Regressor
- Light Gradient Boosting Regressor
- Ridge Regressor
- Support Vector Regressor
- Gradient Boosting Regressor
- Random Forest Regressor
- Stacking CV Regressor optimized using XGBoost

### Performance
- Best model with tuned parameter: **Blended Model with Stacking Regressor**
- Best score (RMSE of log(y-y_pred)) on the evaluation dataset: **0.11949**
- Best rank on the leader board: **top 5%**
