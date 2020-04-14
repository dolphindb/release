# DolphinDB Release Notes

## DolphinDB Server


Version: 1.10.0

Release date: 2020-03-16


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.0.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.0_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.0.zip) |
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.0_JIT.zip)


Version: 1.10.1

Release date: 2020-03-24


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.1.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.1_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.1.zip) |
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.1_JIT.zip)


Version: 1.10.2

Release date: 2020-03-27


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.2.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.2_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.2.zip) |
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.2_JIT.zip)

Version: 1.10.3

Release date: 2020-03-30

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.3.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.3_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.3.zip) |
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.3_JIT.zip)


Version: 1.10.4

Release date: 2020-04-08

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.4.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.4_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.4.zip) |
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.4_JIT.zip)

Version: 1.10.5

Release date: 2020-04-14

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.5.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.5_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.5.zip) |
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.5_JIT.zip)

> New Features

* When an exception is thrown, the call stack is displayed.
* Allow the limit value in the 'context by limit' statement to be negative, which means the last few rows of data of each group are selected.
* Just-in-time compilation (JIT) version added new mathematical functions: all cumulative distribution functions and their inverse functions, and functions `sinh`, `cosh`, `tanh`, `asinh`, `acosh`, `atanh`, `deg2rad`, `rad2deg`. 
* Added mathematical functions: `exp2`, `expm1`, `log2`, `log10`, `log1p`, `cbrt`, `square`.
* Added functions: `mmad`, `groups`, `ifirstNot`, `ilastNot`, `kama` and `trueRange`. (**1.10.3**)
* Added function `segment` to divide a vector into groups. Each group is composed of identical values next to each other. For example, [1,1,2,2,1,1,1] is divided into 3 groups: [1,1], [2,2] and [1,1,1]. (**1.10.4**)
* Can use top/limit 0 or an invalid where condition such as 1=0 in a SQL query to generate an empty table. (**1.10.4**)
* Added configuration parameters 'remoteHost' and 'remotePort'. If these parameters are specified, DolphinDB program can be started as a terminal for a remote server. (**1.10.4**)
* Allow filtering the columns of a matrix with a lambda function. (**1.10.5**)
 

> Improvements

* The parameters 'rowIndex' and 'colIndex' of the function `slice` now support arrays.
* Improved the performance of certain 'context by' statements by 5-10 times.
* Improved the performance of higher-order function `moving` by about 20%.
* Improved the stability of DFS and RAFT.
* Improved the performance of "in" filtering condition when querying a keyed table with multiple keys. (**1.10.1**)
* An empty subarray can be obtained by specifying the same value for the starting and the ending position for the subarray in function `subarray`. For example: subarray(x, 0:0). (**1.10.2**) 
* In function `subarray`, the starting or the ending position of the subarray can now be empty. For examples: subarray(x, 2 :) or subarray(x,: 5). (**1.10.2**)
* Parameter 'input' of function `iterate` can contain NULL values. A NULL value is treated as 0 in calculation. (**1.10.3**)
* Improved the performance of function `iif`. In most cases, performance can be doubled. (**1.10.4**)
* Function `loadText` supports files with carriage return ('\r') as line breaks. (**1.10.4**)
* When using an empty string as an IP address, it no longer throws an exception, but returns an empty IP address. (**1.10.4**)
* For functions `char`, `short`, `int`, `long`, `float` and `double`, if the input string is empty or not a numeric value, a Null value is returned instead of 0. (**1.10.4**)
* If an error occurs in the execution of function `restore`, an exception will be thrown. (**1.10.4**)
* Function `migrate` can restore all databases and tables in a backup folder. (**1.10.4**)
* If the last character of the parameter indicating database path in functions `dropDatabase` and `existsDatabase` is a slash or a backslash, it will be automatically removed. (**1.10.4**)
* If the input of function `rank` is an empty vector, it returns an empty vector instead of throwing an exception. (**1.10.5**)
* When the parameter 'forceDelete' of function `dropPartition` is set to be true, partition deletion is allowed even if the number of copies of the specified partition is 0. (**1.10.5**)
* An exception is thrown if the parameter 'partitionPaths' of function `dropPartition` contains a NULL value. (**1.10.5**)
* Added the restriction that functions related to DFS database operations (including `addValuePartitions`, `addRangePartitions`, `createPartitionedTable`, `createTable`, `database`, `dropDatabase`, `setColumnComment` and `setRetentionPolicy`) can only be executed on data nodes. (**1.10.5**)
* If the 'if' branch or 'else' branch of an if/else statement contains illegal components, an exception will be thrown. (**1.10.5**)

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
* Fixed a bug with function `array`. For a FLOAT or DOUBLE array, if parameter 'defaultValue' of function `array` is set to between 0 and 0.5, the elements of the array will be erroneously assigned the value of 0. (**1.10.3**)
* Fixed a bug introduced in version 1.10.0. When some columns in a SQL query explicitly or implicitly use the same alias, the system crashes. (**1.10.3**)
* Fixed a bug about using order by after context by or group by. If the field to be sorted is already in the order specified by the user (no need to rearrange), the generated query result (in-memory table) will continue to be used for calculation. Fields may produce incorrect results. (**1.10.4**)
* Fixed a bug that the result of function `trueRange` in a SQL query with 'context by' clause may be incorrect. (**1.10.4**)
* Fixed a bug introduced in version 1.10.0. When remotely calling a partial application function in API or with function `remoteRun`, if an exception is thrown during the construction of the partial application function, the system may crash. (**1.10.4**)
* Fixed a bug introduced in version 1.00.6. Functions `loadText`, `ploadText` and `loadTextEx` generate incorrect result when loading strings representing DOUBLE or FLOAT types starting with '.' or '-.'. For example, '.12' and '-.12' are incorrectly parsed as 12. (**1.10.4**) 
* Fixed a bug that function `convertEncode` does not work in Linux version. (**1.10.5**)
* Fixed a bug that when the parameter 'msgAsTable' of funciton `subscribeTable` is set to false, and if only one message in the new batch satisfies the filtering condition, a message that does not necessarily satisfies the filtering condition is sent to the client. (**1.10.5**)
* Fixed a bug that execution of aggregate functions with partitioned tables may cause error of duplicate column names. For example, if MapReduce is used in the execution of a group by statement with a partitioned table, the names of intermediate columns are "col"+number, such as "col1", "col2", etc. If a group-by column happens to have the same name as an intermediate column, an error message about duplicate column names is generated. (**1.10.5**)
* Fixed a bug that function `loadText` may parse DOUBLE type as DATE type in rare cases. (**1.10.5**)


## DolphinDB GUI

> Bug Fixes

* Fixed the bug that the row numbers of the beginning row and the ending row of the selected script for execution are not displayed correctly in the log panel.




 
