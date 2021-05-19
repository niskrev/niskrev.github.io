---
title: Download files with wget
layout: post
category: til
tags: [unix, wget]
---

Basic usage of wget

```
wget http://www.site-name.com/file-name
```

To save under different name

```
$ wget -O new-name http://www.site-name.com/file-name
```

To save in a different directory

```
$ wget -P directory http://www.site-name.com/file-name
```

To download only if the web file is with different time stamp than previously downloaded file

```
wget -N http://www.site-name.com/file-name
```

To download all files of a given type _ftype_

```
wget -r -nd -A ftype --accept-regex ".*\.ftype" http://www.site-name.com/
```
