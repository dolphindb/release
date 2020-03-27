# DolphinDB Release Notes

## DolphinDB Server


Version: 1.10.0

Release date: 2020-03-16


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.0.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.0_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.0.zip) 


Version: 1.10.1

Release date: 2020-03-24


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.1.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.1_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.1.zip) 


Version: 1.10.2

Release date: 2020-03-27


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.2.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.2_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.2.zip) 



> New Features

* When an exception is thrown, the call stack is displayed.
* Allow the limit value in the 'context by limit' statement to be negative, which means the last few rows of data of each group are selected.
* Just-in-time compilation (JIT) version added new mathematical functions: all cumulative distribution functions and their inverse functions, and functions `sinh`, `cosh`, `tanh`, `asinh`, `acosh`, `atanh`, `deg2rad`, `rad2deg`. 
* Added mathematical functions: `exp2`, `expm1`, `log2`, `log10`, `log1p`, `cbrt`, `square`.
 

> Improvements

* The parameters 'rowIndex' and 'colIndex' of the function `slice` now support arrays.
* Improved the performance of certain 'context by' statements by 5-10 times.
* Improved the performance of higher-order function `moving` by about 20%.
* Improved the stability of DFS and RAFT.
* Improved the performance of "in" filtering condition when querying a keyed table with multiple keys. (**1.10.1**)
* An empty subarray can be obtained by specifying the same value for the starting and the ending position for the subarray in function `subarray`. For example: subarray(x, 0:0). (**1.10.2**) 
* In function `subarray`, the starting or the ending position of the subarray can now be empty. For examples: subarray(x, 2 :) or subarray(x,: 5). (**1.10.2**)


> Bug Fixes

* Fixed the problem that the performance of function `backup` deteriorates after running for a period of time.
* Fixed a bug that an out-of-memory problem during concurrent reading of a segmented table may cause deadlocks.
* Fixed a bug that when function `sum` or `avg` is used in function `createTimeSeriesAggregator` and all rows in a group contain NULL values, the result should be a NULL value instead of 0. (**1.10.1**)
* Fixed a bug in the computation of `sum` or `avg` using a hash approach in SQL statements. If all rows in a group contain NULL values, the result should be a NULL value instead of 0. (**1.10.1**)
* Fixed a bug in Windows version of DolphinDB server where closing a client subscription would cause other subscribers on the same node to fail to accept new messages. (**1.10.1**)
* Fixed parsing errors for strings ending with '\\\\', e.g., "hello\\\\". It no longer throws an exception. (**1.10.1**)
* Fixed the problem that if a function in a module is used in a scheduled job, the module cannot be used after server restart. (**1.10.1**)
* Fixed a bug in linear programming (`linprog`) that the accumulation of rounding errors in iterations may lead to incorrect results. (**1.10.1**)
* Fixed a bug in selecting the top rows after sorting string arrays and non-string arrays sequentially. It may lead to incorrect results of function `isortTop`. (**1.10.1**)
* Fixed a bug where the system would register duplicate module functions when a module file is executed in the console or GUI multiple times. It may lead to system crash or thrown exceptions. (**1.10.1**)
* Removed unnecessary output in the console in certain situations when function `slice` is applied to a matrix. (**1.10.1**)
* Fixed a crash bug in the Windows jit version. The system would crash if a user-defined jit function throws an exception. (**1.10.1**)
* Fixed a bug that function `update!` used with multiple filtering conditions generates incorrect result. (**1.10.2**)
* Fixed a bug that queries throw exceptions after inserting an empty table into an empty dimension table. (**1.10.2**)
* Fixed a bug with function `iterate`. The system may erroneously determine the parameter 'input' contains Null value, which causes parameter validation failure. (**1.10.2**)




## DolphinDB GUI

> Bug Fixes

* Fixed the bug that the row numbers of the beginning row and the ending row of the selected script for execution are not displayed correctly in the log panel.




 
