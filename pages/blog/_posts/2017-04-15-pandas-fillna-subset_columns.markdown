---
title: Fill missing values in a subset of columns
layout: post
category: til
tags: [python, pandas]
---

Using *pandas* the missing values in a data frame **df** can be replaced (with e.g. 0) in place using

```
df.fillna(0, inplace=True)
```

To replace missing values only in a subset of columns (e.g. **col 1** and **col 3**), use

```
df.loc[:,["col 1", "col 3"]] = df.loc[:,["col 1", "col 3"]].fillna(0)
```
