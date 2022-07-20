## [Titanic - Machine Learning from Disaster](https://www.kaggle.com/competitions/titanic)
> Create a model that predicts which passengers survived the Titanic shipwreck.

### Jupyter Notebook Versions

| Notebook Name | Feature Engineering | Model |
|         :---          |     :----    |     :----    |
| getting-started-with-titanic | None  | Random Forest Classifier |
| titanic-solution-2           | Basic | Linear SVC |
| titanic-solution-3           | Basic | Random Forest Classifier |
| titanic-solution-4           | More  | Multiple Classifier |
| titanic-solution-5           | Advanced | Multiple Classifier |

### Input Data
- Training set (train.csv)
  - Features: passenger information (ticket, sex, age, cabin, etc.)
  - Label: survival status (0 or 1)
- Test set (test.csv)\
  Same features as in the training set without label (to be predicted)

### Feature Engineering
Advanced feature engineering was applied in **titanic-solution-5**:
- Age: null values filled based on Sex and Pclass features, binned to 13 categories
- Fare: null value filled with median of all the rows, binned to 10 categories
- Deck: inferred by Cabin, null values set to M
- Name: title extracted and grouped
- Family Size: calculated by SibSp and Parch, grouped
- Ticket Type: determined by type of ticker number
- Ticket Frequency: determined by occurence of the same ticket number
- Embarked: null values filled with S as the case of the majority of the rows
- Survival Rate: encoded based on the same family name (extracted by Name) and ticket number

### Machine Learning Model
Multiple models tested in **titanic-solution-5**, the accuracy scores on test data (test_size = 20%) are:

| Model | Score |
| :---- | :---- |
| GBM  | 87.15 |
| Catboost  | 87.15 |
| Logistic Regression  | 85.47 |
| Random Forest  | 84.92 |
| Decision Tree  | 84.36 |
| LightGBM  | 84.36 |
| HistBoost  | 84.36 |
| XGBoost  | 83.80 |

The top 4 models were chosen to perform Grid Search for parameter tuning, and retrained on the complete dataset

### Performance
- Best model with tuned parameter: **Random Forest Classifier**
- Best accuracy on the evaluation dataset: **0.79425**
- Best ranking on the leader board: **top 5%**
