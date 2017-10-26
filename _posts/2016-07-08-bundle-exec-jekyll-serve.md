---
layout: post
title:  'bundle exec jekyll serve'
date:   2016-07-08 04:21:12 +1000
categories: 'bundler jekyll ruby'
---

I use the command

```
bundle exec jekyll serve
```

to build this website locally for testing into the _site directory.
The directory structure is shown below:

```
C:\work\github\jbampton.github.io>dir
 Volume in drive C has no label.
 Volume Serial Number is 19DE-8B12

 Directory of C:\work\github\jbampton.github.io

09/21/2016  02:57 PM    <DIR>          .
09/21/2016  02:57 PM    <DIR>          ..
07/08/2016  04:21 AM                35 .gitignore
07/08/2016  04:21 AM    <DIR>          .sass-cache
09/21/2016  02:57 PM            11,856 about.md
09/13/2016  05:55 PM                13 CNAME
07/08/2016  04:21 AM    <DIR>          css
07/08/2016  11:05 AM                47 devrun.sh
07/08/2016  04:21 AM             1,291 feed.xml
07/08/2016  09:56 AM                95 Gemfile
07/08/2016  09:55 AM             3,154 Gemfile.lock
07/11/2016  03:27 AM               529 index.html
07/08/2016  04:38 AM    <DIR>          js
09/13/2016  05:55 PM             1,045 _config.yml
07/08/2016  04:21 AM    <DIR>          _includes
07/08/2016  04:21 AM    <DIR>          _layouts
10/25/2016  05:59 AM    <DIR>          _posts
07/11/2016  03:27 AM    <DIR>          _sass
10/25/2016  07:06 AM    <DIR>          _site
               9 File(s)         18,065 bytes
              10 Dir(s)  84,169,297,920 bytes free

C:\work\github\jbampton.github.io>
```

Then in '.gitignore' as seen below we ignore the _site directory from version control.

```
_site
.sass-cache
.jekyll-metadata
```
