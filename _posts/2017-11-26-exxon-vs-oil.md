---
layout: post
title:  'Exxon versus Oil'
date:   2017-11-26 02:39:00 +1000
categories: 'python'
---

This post shows the Exxon Mobile Corporation share price versus the West Texas Intermediate oil price displayed using Matplotlib and the Pandas DataReader.  The data comes from both
 Google finance and [FRED](https://fred.stlouisfed.org/){:target="_blank"}{:rel="noopener"} Economic Data.

![Exxon Mobile Corporation share price versus the West Texas Intermediate oil price](
/images/exxon-vs-oil-price.png)

```python
"""Exxon versus Oil"""

from datetime import datetime, timedelta
from pandas_datareader.data import DataReader
import matplotlib.pyplot as plt
import pandas as pd


# set the dates
now = datetime.now()
start = (now - timedelta(days=365)).date()
end = now.date()

series = 'DCOILWTICO' # West Texas Intermediate Oil Price

oil = DataReader(series, 'fred', start)

ticker = 'XOM' # Exxon Mobile Corporation
stock = DataReader(ticker, 'google', start)

data = pd.concat([stock[['Close']], oil], axis=1)
data.columns = ['Exxon', 'Oil Price']
data.plot(title="Exxon stock price versus Oil price")

fig = plt.gcf()
fig.set_size_inches(9, 9)
fig.savefig('images/exxon-vs-oil-price.png', dpi=80)
```
