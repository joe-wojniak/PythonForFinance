![OHLC plot](https://github.com/joe-wojniak/PythonForFinance/blob/main/7-27%20OHLC%20EUR-USD%20wBB.PNG)
```
######################################################################################
# Python for Finance, 2nd ed., Hilpisch, Yves
# Chapter 7 - Data Visualization
#
# Figure 7-27 OHLC plot of EUR/USD data with Bollinger band and RSI
#
# https://stooq.com/db/h/
# https://jpoles1.github.io/cufflinks/html/cufflinks.quant_figure.html
#
# Python 3, Jupyter Lab
#######################################################################################

import pandas as pd
import cufflinks as cf
import plotly.offline as plyo

filename = './data/daily/world/currencies/major/eurusd.txt'

raw = pd.read_csv(filename, index_col=2, parse_dates=True)

quotes = raw[['<OPEN>', '<HIGH>', '<LOW>', '<CLOSE>']]
quotes = quotes.iloc[-60:]

qf = cf.QuantFig(quotes, title='EUR/USD Exchange Rate', legend='top', name='EUR/USD')
qf.add_bollinger_bands(periods=15, boll_std=2)
qf.add_rsi(periods=14, showbands=False)

plyo.iplot(qf.iplot(asFigure=True), image='png', filename='qf_01')
```
