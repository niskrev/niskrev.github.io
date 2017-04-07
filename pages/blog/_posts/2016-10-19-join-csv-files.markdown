---
title: Joining CSV files
layout: post
category: til
tags: [unix,csv]
---

I have a bunch of csv files each having two columns: date and value. I want to create a single csv file with date as first column and the value columns from the many files. This is straightforward to do with say pandas in python, or excel, but I was looking for a simple command line approach. One way is using [csvkit](https://github.com/wireservice/csvkit) utilities.

```
csvjoin -c 1,1 file1.csv file2.csv | csvcut -c 1,2,4 > file1_2.csv
```
The first instruction tells csvjoin to join the files using the first column of each. The result has 4 columns with the same column date in the first and third position. The second instruction uses another utility - csvcut, to keep only columns 1,2 and 4, which are then saved as the new csv file.
