---
layout: post
title:  'Automobile weight versus horsepower'
date:   2018-01-03 04:21:12 +1000
categories: python
---

Using [seaborn](https://seaborn.pydata.org/){:target="_blank"}{:rel="noopener"}, I have plotted automobile weight versus horsepower grouped by continent as shown below.

```python
import seaborn as sns
import pandas as pd
import matplotlib.pyplot as plt


auto = pd.read_csv('data/auto.csv')
sns.lmplot(x='weight', y='hp', data=auto, hue='origin')
plt.title('Automobile weight versus horsepower by Continent')
plt.ylabel('Horsepower (hp)')
plt.xlabel('Weight')
fig = plt.gcf()
fig.set_size_inches(8, 8)
fig.savefig('images/automobile-weight-versus-horsepower-by-continent.png', dpi=80)
```

![Automobile weight versus horsepower](/images/automobile-weight-versus-horsepower-by-continent.png)
