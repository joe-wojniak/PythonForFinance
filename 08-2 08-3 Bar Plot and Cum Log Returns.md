# Percentage Change Bar Plot and Cumulative Log Returns Plot

*Figure 8-2: Mean values of percentage changes as bar plot*

*Figure 8-3: Cumulative log returns over time*

![Percent Changes](https://github.com/joe-wojniak/PythonForFinance/blob/main/Financial%20Time%20Series/PFF_Ch8_Fig_8-2.png)

![Log Returns](https://github.com/joe-wojniak/PythonForFinance/blob/main/Financial%20Time%20Series/PFF_Ch8_Fig_8-3.png)

```python
# Python for Finance, 2nd ed., Hilpisch, Ives
# Chapter 8 - Financial Time Series
# Figure 8-2 Mean values of percentage changes as bar plot
# Figure 8-3 Cumulative log returns over time
# https://stooq.com/db/h/
# https://www.datacamp.com/community/tutorials/pandas-tutorial-dataframe-python
# Python 3

%matplotlib inline
import numpy as np
import pandas as pd
import matplotlib
import matplotlib.pyplot as plt

import warnings
warnings.filterwarnings('ignore')

plt.style.use('seaborn')
mpl.rcParams['font.family']='serif'

data = pd.read_csv('data.csv', index_col=0, parse_dates=True)

# Percentage Returns
data.pct_change().mean().plot(kind='bar', figsize=(9.7,6))
plt.savefig('PFF_Ch8_Fig_8-2.png')

# Log Returns
rets = np.log(data/data.shift(1))
rets.cumsum().apply(np.exp).plot(figsize=(10,6))
plt.savefig('PFF_Ch8_Fig_8-3.png')
```
