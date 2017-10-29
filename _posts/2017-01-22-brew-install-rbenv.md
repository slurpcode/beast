---
layout: post
title:  'brew install rbenv'
date:   2017-01-22 01:00:00 +1000
categories: 'ruby'
---

Installing [rbenv](https://github.com/rbenv/rbenv){:target="_blank"} is easy with [Homebrew](http://brew.sh/){:target="_blank"} with the next two commands:

```
$ brew update
$ brew install rbenv
```

Then to install the latest current version of Ruby 2.4 type:

```
$ rbenv install 2.4.0
```

Full information on the rbenv command below:

```
$ rbenv
rbenv 1.1.0
Usage: rbenv <command> [<args>]

Some useful rbenv commands are:
   commands    List all available rbenv commands
   local       Set or show the local application-specific Ruby version
   global      Set or show the global Ruby version
   shell       Set or show the shell-specific Ruby version
   install     Install a Ruby version using ruby-build
   uninstall   Uninstall a specific Ruby version
   rehash      Rehash rbenv shims (run this after installing executables)
   version     Show the current Ruby version and its origin
   versions    List all Ruby versions available to rbenv
   which       Display the full path to an executable
   whence      List all Ruby versions that contain the given executable

See `rbenv help <command>' for information on a specific command.
For full documentation, see: https://github.com/rbenv/rbenv#readme
$
```
