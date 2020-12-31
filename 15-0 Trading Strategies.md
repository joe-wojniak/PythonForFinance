# Trading Strategies

This demo utilizes the Coinbase Pro public end points and the Coinbase Pro client for Python 
* (https://github.com/danpaquin/coinbasepro-python)

## Reference: Chapter 15 Trading Strategies, Python For Finance, 2nd edition

The data files used are provided for convenience:
* [BTC-USD Data](https://github.com/joe-wojniak/PythonForFinance/blob/main/Trading%20Strategies/BTC-USD.csv)
* [Coinbase Products](https://github.com/joe-wojniak/PythonForFinance/blob/main/Trading%20Strategies/products.csv)

## Case 1: 
An SMA Strategy is Backtested using Bitcoin-US Dollar (BTC-USD) data from Coinbase Pro public data-endpoint.
![BTC-USD SMA Plot](https://github.com/joe-wojniak/PythonForFinance/blob/main/Trading%20Strategies/4-BTC-USD_LongVsSMA.png)
```
Cumulative:
Returns     1.199487
Strategy    1.027011

Volatility:
Returns     0.140443
Strategy    0.140796
```

The log returns for BTC-USD are shown in a histogram, illustrating 'fat-tails'.
![BTC-USD Returns](https://github.com/joe-wojniak/PythonForFinance/blob/main/Trading%20Strategies/5-BTC-USD_Hist.png)

## Case 2: 
Linear Ordinary Least Squares (OLS) Regression is backtested and compared to daily returns
![OLS Backtest Results](https://github.com/joe-wojniak/PythonForFinance/blob/main/Trading%20Strategies/7-BTC-USD_OLS_ReturnsVsDirection.png)
```
Cumulative:
returns        1.254766
strat_ols_1    1.322613
strat_ols_2    1.229719
```

## Case 3: 
k-means clustering is demonstrated and compared to OLS results
![k-means clustering](https://github.com/joe-wojniak/PythonForFinance/blob/main/Trading%20Strategies/9-BTC-USD_K-Means_ClusteringVsBenchmark.png)
```
Cumulative:
returns       1.254766
strat_clus    1.396107
```
## Jupyter Lab Notebook:
The notebook contains all the source code to reproduce the results summarized above.  The data files need to be saved in the same directory as the notebook.
The data files can be refreshed using the Coinbase Pro public data end points, which are referenced in comments through-out the notebook.
[Notebook](https://github.com/joe-wojniak/PythonForFinance/blob/main/Trading%20Strategies/coinbaseSandboxBacktesting.ipynb)

