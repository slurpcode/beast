---
layout: post
title:  Joint plot of automobile horsepower versus miles per gallon
date:   2018-01-08 05:21:12 +1000
categories: python
---

Using [seaborn](https://seaborn.pydata.org/){:target="_blank"}{:rel="noopener"}, I have plotted a jointplot of automobile horsepower versus miles per gallon.

```python
import seaborn as sns
import pandas as pd
import matplotlib.pyplot as plt

auto = pd.read_csv('data/auto.csv')
sns.jointplot(x='hp', y='mpg', data=auto)
plt.xlabel('Horsepower (hp)')
plt.ylabel('Miles per gallon (mpg)')
fig = plt.gcf()
fig.set_size_inches(8, 8)
fig.savefig('images/jointplot-horsepower-versus-mpg.png', dpi=80)
```

![Joint plot of automobile horsepower versus miles per gallon](/images/jointplot-horsepower-versus-mpg.png)
