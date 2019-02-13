# aapl-revenue
Predicting Apple (AAPL) revenue from fundamentals data with machine learning

Goal: forecast Apple's revenue for 2018 based on historical fundamentals data

Main notebook: [aapl-quarterly.ipynb](https://github.com/apadkavyrava/aapl-revenue/blob/master/aapl_quarterly.ipynb)

At first the [nyse](https://www.kaggle.com/dgawlik/nyse) dataset seemed more than enough for the job. However:
- it only covers 2012-2016. Forecasting revenue 3 years ahead would be a challenge even for analysts at Apple.
- it is based on SEC 10K annual fillings, so there are at most 5 data points per company
- there is very little homogenuity in revenue dynamics across companies, apart from general market trend

So I used quarterly AAPL fundamentals from Nasdaq obtained from [gurufocus.com](https://www.gurufocus.com/). This gives 4 data points per year since 1988.

I implemented linear regression with Y as revenue and X as all other fundamentals, then played with time range. It can be seen from the chart that revenue grows much faster from around 2004. So if we use only the years after accuracy might increase - which in fact is the case.

------

This linear model is quite simple, so I also implemented regression that uses data from earlier years as features. I used the original NYSE dataset and trained the model on multiple companies. This model didn't achieve good accuracy though.

Multi-company model notebook: 
