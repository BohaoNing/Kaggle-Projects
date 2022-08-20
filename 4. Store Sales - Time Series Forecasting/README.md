## [Store Sales - Time Series Forecasting](https://www.kaggle.com/competitions/store-sales-time-series-forecasting)
>  Use machine learning to predict grocery sales

### Jupyter Notebook Versions
 
| Notebook Name                  |                    Versions                     |
|         :---:                  |                     :----:                      |
| Store Sales - Hyperparamatered Solution |         Final Solution                 |
| Store Sales - Getting Started with Time Series | Final Solution, Simplified Code |
| Others                         |             Resources and References            |

### Input Data
- Training set (train.csv)\
  Comprising time series of features store_nbr, family, and onpromotion as well as the target sales
- Test set (test.csv)\
  Same features as in the training set without target (to be predicted)
- Store set (stores.csv)\
  Store metadata, including city, state, type, and cluster
- Oil set (oil.csv)\
  Daily oil price
- Holiday set (holidays_events.csv)\
  Holidays and Events, with metadata

### Feature Engineering
- Average oil price using a 7-day rolling window
- 3 lags for oil prices
- National holidays with some adjustments
- A "school_season" feature for school fluctuations
- Deterministic process with order=3 CalendarFourier 
- Training period was from 2017-04-30 to 2017-08-15 based on sales plots

### Machine Learning Model
A custom regressor:
- 

### Performance
- Best model with tuned parameter: **Blended Model with a customized regressor**
- Best score (Root Mean Squared Logarithmic Error) on the evaluation dataset: **0.40419**
- Best rank on the leaderboard: **top 7%**
