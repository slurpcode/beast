---
layout: post
title:  "Matplotlib Color Maps"
date:   2017-12-28 11:49:00 +1000
categories: 'python'
---

Matplotlib provides a variety of color maps that you can style your content with.

The next four lines of code produces the image below: 

```python
import matplotlib.pyplot as plt


img = plt.imread('images/thebeast.png')
lum_img = img[:, :, 0]
plt.imsave('images/thebeast-plasma.png', lum_img, cmap='plasma')
```

![Plasma Beast](/images/thebeast-plasma.png)
