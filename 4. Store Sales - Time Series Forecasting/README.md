## [Spaceship Titanic](https://www.kaggle.com/competitions/spaceship-titanic)
>  Predict which passengers are transported to an alternate dimension

### Jupyter Notebook Versions
 
| Notebook Name                  |   Feature Engineering   |         Model        |
|         :---:                  |          :----:         |        :----:        |
| Spaceship Titanic - Solution 1 |         Version 1       | Multiple Classifiers |
| Spaceship Titanic - Solution 2 |         Version 2       | Multiple Classifiers |
| Spaceship Titanic - Solution 3 |         Version 3       | Multiple Classifiers |

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
- Best model with tuned parameter: **Blended Model with a customized regressor**\
- Best score (Root Mean Squared Logarithmic Error) on the evaluation dataset: **0.40419**
- Best rank on the leaderboard: **top 7%**

