---
layout: post
title:  'USA Labor Market'
date:   2017-11-26 06:49:00 +1000
categories: 'python'
---

This post highlights the USA Labor Market shown by a comparison between the Unemployment Rate and Participation Rate
 with data sourced from [FRED](https://fred.stlouisfed.org/){:target="_blank"}{:rel="noopener"} Economic Data.

![USA Labor Market](/images/us-labor-market-participation-vs-unemployment.png)

```python
"""USA Labor Market: Unemployment Rate versus Participation Rate."""

from datetime import date
from pandas_datareader.data import DataReader
import matplotlib.pyplot as plt


# Set the start date
start = date(1950, 1, 1)

# Define the series codes
series = ['UNRATE', 'CIVPART']

# Import the data
econ_data = DataReader(series, 'fred', start)

# Assign new column labels
econ_data.columns = ['Unemployment Rate', 'Participation Rate']

# Plot econ_data
econ_data.plot(subplots=True)
plt.title('USA Labor Market', fontsize=20, y=2.25)
plt.xlabel('Date')
plt.ylabel('Percent')

# save plot
fig = plt.gcf()
fig.set_size_inches(9, 9)
fig.savefig('images/us-labor-market-participation-vs-unemployment.png', dpi=80)

```
