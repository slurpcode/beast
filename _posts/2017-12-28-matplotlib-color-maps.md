---
layout: post
title:  "Matplotlib Color Maps"
date:   2017-12-28 11:49:00 +1000
categories: 'python'
---

Matplotlib provides a variety of color maps that you can style your content with.

The next nine lines of code produces the image below: 

```python
import matplotlib.pyplot as plt


img = plt.imread('images/thebeast.png')
lum_img = img[:, :, 0]
plt.imsave('images/thebeast-plasma.png', lum_img, cmap='plasma')
plt.imsave('images/thebeast-PuRd_r.png', lum_img, cmap='PuRd_r')
plt.imsave('images/thebeast-bupu.png', lum_img, cmap='BuPu')
plt.imsave('images/thebeast-greens.png', lum_img, cmap='Greens')
plt.imsave('images/thebeast-oranges.png', lum_img, cmap='Oranges')
plt.imsave('images/thebeast-ocean.png', lum_img, cmap='ocean')
```

![Plasma Beast](/images/thebeast-plasma.png){:style="float:left;"}
![Pink Beast](/images/thebeast-PuRd_r.png){:style="float:left;"}
![Blue Beast](/images/thebeast-bupu.png){:style="float:left;"}
![Green Beast](/images/thebeast-greens.png){:style="float:left;"}
![Orange Beast](/images/thebeast-oranges.png){:style="float:left;"}
![Ocean Beast](/images/thebeast-ocean.png)



