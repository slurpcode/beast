---
layout: post
title:  Apple vs Adobe vs Google vs Microsoft - Stock Prices
date:   2017-10-25 11:14:00 +1000
categories: python
---

Demonstration of using subplots with [Matplotlib](https://matplotlib.org/) to show stock prices of four of the biggest companies in the world.

```python
from pandas_datareader.data import DataReader
from datetime import datetime, timedelta
import matplotlib.pyplot as plt

# set the dates
now = datetime.now()
start = (now - timedelta(days=365)).date()
end = now.date()

# Set the ticker
ticker = 'AAPL', 'ADBE', 'GOOGL', 'MSFT'
# Set the data source
data_source = 'google'  #use google finance
# Import the stock prices
stock_prices = DataReader(ticker, data_source, start, end)
# Plot Close
stock_prices['Close'].plot(title=ticker, subplots=True)
fig = plt.gcf()
fig.set_size_inches(9, 9)
fig.savefig('images/apple-adobe-google-microsoft.png', dpi=80)
```

![Stock prices of Apple, Adobe, Google and Microsoft](/images/apple-adobe-google-microsoft.png)
