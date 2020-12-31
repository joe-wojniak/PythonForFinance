# Trading Strategies

This demo utilizes the Coinbase Pro public end points and the Coinbase Pro client for Python (https://github.com/danpaquin/coinbasepro-python)

## Reference: Chapter 15 Trading Strategies, Python For Finance, 2nd edition

The data files used are provided for convenience:
* [BTC-USD Data](https://github.com/joe-wojniak/PythonForFinance/blob/main/Trading%20Strategies/BTC-USD.csv)
* [Coinbase Products](https://github.com/joe-wojniak/PythonForFinance/blob/main/Trading%20Strategies/products.csv)

## Case 1: An SMA Strategy is Backtested using Bitcoin-US Dollar (BTC-USD) data from Coinbase Pro public data-endpoint.
![BTC-USD SMA Plot](https://github.com/joe-wojniak/PythonForFinance/blob/main/Trading%20Strategies/3-BTC-USD_SMA_Position.png)

The log returns for BTC-USD are shown in a histogram, illustrating 'fat-tails'.
![BTC-USD Returns](https://github.com/joe-wojniak/PythonForFinance/blob/main/Trading%20Strategies/5-BTC-USD_Hist.png)

## Case 2: Linear Ordinary Least Squares (OLS) Regression is backtested and compared to cumulative returns
![OLS Backtest Results](https://github.com/joe-wojniak/PythonForFinance/blob/main/Trading%20Strategies/7-BTC-USD_OLS_ReturnsVsDirection.png)

## Case 3: k-means clustering is demonstrated and compared to OLS results
![k-means clustering](https://github.com/joe-wojniak/PythonForFinance/blob/main/Trading%20Strategies/9-BTC-USD_K-Means_ClusteringVsBenchmark.png)

## Jupyter Lab Notebook:
[Notebook](https://github.com/joe-wojniak/PythonForFinance/blob/main/Trading%20Strategies/coinbaseSandboxBacktesting.ipynb)
