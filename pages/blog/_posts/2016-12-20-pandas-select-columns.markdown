---
title: Selecting columns in dataframes
layout: post
category: til
tags: [python, pandas]
---
Select columns in a DataFrame that start with "abc"

+ option 1: using regex
```
df.filter(regex='^abc')
```
+ option 2: using select
```
df.select(lambda col: col.startswith('abc'), axis=1)
```
