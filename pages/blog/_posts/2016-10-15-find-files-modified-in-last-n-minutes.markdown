---
title: Find Files Modified in last N Minutes
layout: post
category: til
tags: [bash]
---

# This snippet was taken from the [TIL of Timothy Hopper](http://til.tdhopper.com/)

I've been using Bash's [`find`](http://www.freebsd.org/cgi/man.cgi?find(1)) command a lot more regularly lately. I've always been scared off by its syntax, but it's great once you've learned it.

Today I learned how to filter the results by files changed in the last N minutes: the `cmin` flag:

```
 -cmin [-|+]n
 True if the difference between the time of last change of file
 status information and the time find was started, rounded up to
 the next full minute, is more than n (+n), less than n (-n), or
 exactly n minutes ago.
```

For example:

```
find . -cmin +5 # Files modified more than 5 minutes ago
find . -cmin -5 # Files modified less than than 5 minutes ago
find . -cmin  5 # Files modified exactly 5 minutes ago
```
