# DolphinDB Release Notes

## DolphinDB Server


Version: 1.10.0

Release date: 2020-03-16


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.0.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.0_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.0.zip) 




> New Features

* When an exception is thrown, the call stack is displayed.
* Allow the limit value in the 'context by limit' statement to be negative, which means the last few rows of data of each group are selected.
* Just-in-time compilation (JIT) version added new mathematical functions: all cumulative distribution functions and their inverse functions, and functions `sinh`, `cosh`, `tanh`, `asinh`, `acosh`, `atanh`, `deg2rad`, `rad2deg`. 
* Added mathematical functions: `exp2`, `expm1`, `log2`, `log10`, `log1p`, `cbrt`, `square`.
 

> Improvements

* The parameters 'rowIndex' and 'colIndex' of the function `slice` now support arrays.
* Improved the performance of certain 'context by' statements by 5-10 times.
* Improved the performance of higher-order function `moving` by about 20%.
* Improved the stability of DFS and Raft.


> Bug Fixes

* Fixed the problem that the performance of function `backup` deteriorates after running for a period of time.
* Fixed a bug that an out-of-memory problem during concurrent reading of a segmented table may cause deadlocks.




## DolphinDB GUI

> Bug Fixes

* Fixed the bug that the row numbers of the beginning row and the ending row of the selected script for execution are not displayed correctly in the log panel.




 
