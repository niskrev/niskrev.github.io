---
title: Create conda environment from yaml file
layout: post
category: til
tags: [unix, conda, yaml]
---
In the directory containing the yaml file, run

```
conda-env create -f environment.yaml
```
environment.yaml is the file listing the required libraries
