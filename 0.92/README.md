# DolphinDB Release Notes

Release Date : 2019-02-28

Version : 0.92

## DolphinDB Server
[Linux binary](http://www.dolphindb.com/downloads/DolphinDB_Linux_V0.92.zip) | [Windows binary](http://www.dolphindb.com/downloads/DolphinDB_Win_V0.92.zip)

> New Features

* New functions for calculations on the dimension of rows: rowMin, rowMax, rowCount, rowSum, rowSum2, rowAvg, rowStd, rowVar
* Extended SQL PIVOT BY clause to make pivoting, null filling and row level reductive operation complete in one step. Right now, "pivot by" can be used together with ffill, fill,  and lfill, as well as the following 5 row-dimension functions: rowSum, rowMin, rowMax, rowCount, rowSum2. 
* New higher order function pcall
* New function subtuple

> Improvements

* Optimize the performance of return statement to avoid unnecessary data copy

## DolphinDB Plugin

* Updated include header files

[DolphinDBPlugin](https://github.com/dolphindb/release/blob/master/0.92/DolphinDB_Plugin_V0.92_src.zip)
