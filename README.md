# Stock_price_with_XGBoost

How to train, validate, and predict the stock data?

1. I took the past 1 year of NVDA stock prices data for daily interval from Yahoo Finance python. The aim is to input lag close price features and output future close prices.

2. I took 5 days lag Close price as features (lag by 5 days, lag by 4 days, lag by 3 days, lag by 2 days, lag by 1 day).

3. I used XGBoost as the model to find feature importances, and found that lag by 1 day feature is the most important feature.

4. I used XGBoost to train and validate with time series split, and got their root mean square error for each fold.

5. The XGBoost is then used to predict the next 50 days stock prices using recursive or direct method. Recusive method is not recommended as it can accumulate errors from previous days' predictions.
