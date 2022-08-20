## [Store Sales - Time Series Forecasting](https://www.kaggle.com/competitions/store-sales-time-series-forecasting)
>  Use machine learning to predict grocery sales

### Jupyter Notebook Versions
 
| Notebook Name                  |                    Versions                     |
|         :---:                  |                     :----:                      |
| Store Sales - Hyperparamatered Solution |         Final Solution                 |
| Store Sales - Getting Started with Time Series | Final Solution, Simplified Code |
| Others                         |                    Version 3                    |

### Input Data
- Training set (train.csv)
  - Features: passenger information, such as ID, HomePlanet, Age, etc.
  - Label: whether transported to another dimension (bool)
- Test set (test.csv)\
  Same features as in the training set without label (to be predicted)

### Feature Engineering
- Missing values were filled using various strategies
- Three more features were created in Version 3
  - Adult: True if Age >= 18, else False
  - TotalSpend: the sum of all the bill amount onboard
  - FamilyMember: the count of the same family name

### Machine Learning Model
Multiple models tested in all the notebooks:
- LogisticRegression
- DecisionTreeClassifier
- RandomForestClassifier
- XGBClassifier
- GradientBoostingClassifier
- LGBMClassifier
- CatBoostClassifier
- HistGradientBoostingClassifier
- StackingClassifier with CatBoostClassifier or RandomForestClassifier

### Performance
- Best model with tuned parameter: **Blended Model with a customized regressor**
- Best score (Root Mean Squared Logarithmic Error) on the evaluation dataset: **0.40419**
- Best rank on the leaderboard: **top 7%**
