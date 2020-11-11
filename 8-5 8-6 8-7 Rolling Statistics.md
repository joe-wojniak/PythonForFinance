# Rolling Statistics

![min mean max](https://github.com/joe-wojniak/PythonForFinance/blob/main/rollingStat1.PNG)

![position](https://github.com/joe-wojniak/PythonForFinance/blob/main/rollingStat2.PNG)

```python
######################################################################################
# Python for Finance, 2nd ed., Hilpisch, Yves
# Chapter 8 - Financial Time Series: Rolling Statistics
#             a.k.a. financial indicators or financial studies
#
# Figure 8-5 Rolling statistics for minimum, mean, maximum values
# Figure 8-6 Apple stock price and two simple moving averages
# Figure 8-7 Apple stock price, two simple moving averages and positions
#
# https://stooq.com/db/h/
# https://www.datacamp.com/community/tutorials/pandas-tutorial-dataframe-python
# Python 3, Jupyter Lab
######################################################################################

%matplotlib inline
import numpy as np
import pandas as pd
from pylab import mpl, plt

plt.style.use('seaborn')
mpl.rcParams['font.family']='serif'

data=pd.read_csv('./data_all.csv', index_col=0, parse_dates=True)

data.info()

sym = 'aapl.us.txt'
data1 = pd.DataFrame(data[sym].dropna())
data1.tail()

window = 20
data1['min'] = data1[sym].rolling(window=window).min()
data1['mean'] = data1[sym].rolling(window=window).mean()
data1['std'] = data1[sym].rolling(window=window).std()
data1['median'] = data1[sym].rolling(window=window).median()
data1['max'] = data1[sym].rolling(window=window).max()
data1['ewma'] = data1[sym].ewm(halflife=0.5, min_periods=window).mean()

data1.dropna().head()

ax = data1[['min', 'mean', 'max']].iloc[-200:].plot(figsize=(10,6), style=['g--','r--','g--'], lw = 0.8)
data1[sym].iloc[-200:].plot(ax=ax, lw=2.0)

data1['SMA_short'] = data[sym].rolling(window=42).mean()
data1['SMA_long'] = data[sym].rolling(window=252).mean()
data1[[sym, 'SMA_short', 'SMA_long']].tail()

data1[[sym, 'SMA_short', 'SMA_long']].loc['2007-09':'2020'].plot(figsize=(10,6));

data1.dropna(inplace=True)

#data1.insert(3, 'positions', "")

data1['positions'] = np.where(data1['SMA_short'] > data1['SMA_long'], 1, -1)

ax = data1[[sym, 'SMA_short', 'SMA_long', 'positions']].loc['2011':'2020'].plot(figsize=(10,6), secondary_y='positions')
ax.get_legend().set_bbox_to_anchor((0.25, 0.85));

```

