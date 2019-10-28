---
layout: post
title:  Hexbin jointplot of horsepower versus miles per gallon
date:   2018-01-16 04:21:12 +1000
categories: python
---


Using [seaborn](https://seaborn.pydata.org/), I have plotted a hexbin style jointplot of automobile horsepower versus miles per gallon.


```python
import seaborn as sns
import pandas as pd
import matplotlib.pyplot as plt


auto = pd.read_csv('data/auto.csv')

sns.jointplot(x='hp', y='mpg', data=auto, kind='hex')
plt.xlabel('Horsepower (hp)')
plt.ylabel('Miles per gallon (mpg')

fig = plt.gcf()
fig.set_size_inches(8, 8)
fig.savefig('images/hexbin-jointplot-hp-versus-mpg.png', dpi=80)
```

![Hexbin style jointplot of horsepower versus miles per gallon](/images/hexbin-jointplot-hp-versus-mpg.png)
