---
title: Replace empty space with end-of-line using ```sed```
layout: post
category: til
tags: [unix, sed]
---
This is MacOS specific (its simpler on unix)

```
sed -e 's/ /'$'\n\g' < old_file > new_file
```

will replace empty spaces between words with end-of-line (\n). The result is a new file with only one word per line
