---
layout: post
title:  rbenv help command
date:   2017-01-24 01:00:00 +1000
categories: ruby
---

List all [rbenv](https://github.com/rbenv/rbenv) commands:

```
$ rbenv commands
commands
completions
exec
global
help
hooks
init
install
local
prefix
realpath.dylib
rehash
root
shell
shims
uninstall
version
--version
version-file
version-file-read
version-file-write
version-name
version-origin
versions
whence
which
$
```
To bring up further information on the versions command use the following:

```
$ rbenv help versions
Usage: rbenv versions [--bare] [--skip-aliases]

Lists all Ruby versions found in `$RBENV_ROOT/versions/*'.
$
```
