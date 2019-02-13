# aapl-revenue
Predicting Apple (AAPL) revenue for 2018 with machine learning

[aapl-quarterly.ipynb](https://github.com/apadkavyrava/aapl-revenue/blob/master/aapl_quarterly.ipynb)

The original dataset seemed not enough for good prediction:
- it only covers 2012-2016, so we're missing 2 years of data
- it is based on annual data, so there are 5 or less data points per company

So I used quarterly AAPL fundamentals from Nasdaq. This gives 4 data points per year since 1988.

I implemented linear regression with Y as revenue and X as all other fundamentals, then played with time range. It can be seen from the chart that revenue grows much faster from around 2004. So if we use only the years after accuracy might increase - which in fact is the case.

------

This linear model is quite simple, so I also implemented regression that uses nested data from earlier years as features. I used the original NYSE dataset and trained the model on multiple companies. This model didn't achieve good accuracy though.

Multi-company model notebook: [aapl-multicompany.ipynb](https://github.com/apadkavyrava/aapl-revenue/blob/master/apple_multicompany.ipynb)

------

- Original dataset: [NYSE](https://www.kaggle.com/dgawlik/nyse)
- Nasdaq dataset obtained from [gurufocus.com](https://www.gurufocus.com/)
