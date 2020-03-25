# DolphinDB Release Notes

## DolphinDB Server

Version: 1.00.0
Release date: 2019-12-02

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.0.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.0.zip) | 


Version: 1.00.1
Release date: 2019.12.11

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.1.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.1.zip) | 

Version: 1.00.2
Release date: 2019.12.16

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.2.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.2.zip) | 

Version： 1.00.3
Release date： 2019.12.18

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.3.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.3.zip) | 

Version： 1.00.4
Release date： 2019.12.20

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.4.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.4.zip) | 

Version: 1.00.5
Release date: 2019.12.23

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.5.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.5.zip) | 

Version: 1.00.6
Release date: 2020.01.06

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.6.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.6.zip) | 

Version: 1.00.7
Release date: 2020.01.17

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.7.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.7.zip) | 

Version: 1.00.8
Release date: 2020.01.19

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.8.zip) | 
[Linux64 ABI=1 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.8_ABI.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.8.zip) | 

Version: 1.00.9
Release date: 2020.01.30

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.9.zip) | 
[Linux64 ABI=1 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.9_ABI.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.9.zip) | 

Version: 1.00.10
Release date: 2020.02.15

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.10.zip) | 
[Linux64 ABI=1 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.10_ABI.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.10.zip) | 

Version: 1.00.11
Release date: 2020.02.28

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.11.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.11.zip) | 

Version: 1.00.12
Release date: 2020.03.05

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.12.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.12.zip) | 

Version: 1.00.13
Release date: 2020.03.15

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.13.zip) | 
[Linux64 ABI=1 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.13_ABI.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.13.zip) | 

Version: 1.00.14
Release date: 2020.03.24

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.14.zip) | 
[Linux64 ABI=1 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.14_ABI.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.14.zip) | 

> New feature

* Support high-availability of streaming based on Raft protocol.

* New functions:
    * Temporal functions: `dayOfYear,dayOfMonth,
quarterOfYear,monthOfYear,weekOfYear,hourOfDay,minuteOfHour,secondOfMinute,weekday,yearBegin,yearEnd,businessYearBegin,businessYearEnd,monthBegin,monthEnd,semiMonthBegin,semiMonthEnd,businessMonthBegin,businessMonthEnd,quarterBegin,quarterEnd,quarterBusinessBegin,quarterBusinessEnd,week,lastWeekOfMonth,weekOfMonth,
fy5253,fy5253Quarter,isYearStart,isYearEnd,isQuarterStart,isQuarterEnd,isMonthStart,isMonthEnd,isLeapYear,daysInMonth,weekBegin`
    * String functions: `isUpper,isLower,isTitle,isSpace,isAlpha,isNumeric,isDigit,isAlNum,isDecimal`
    * Window functions: `ewmMean,ewmStd,ewmVar,ewmCov,ewmCorr`
    * Math functions: `isMonotonic,isMonotonicIncreasing,isMonotonicDecreasing,quantile,quantileSeries`
    * Function `nunique` calculates the number of unique elements in a vector    
    * Function `interpolate`
* SQL statements support 3 new types of hint constants: HINT_KEEPORDER, HINT_HASH and HINT_SNAPSHOT. Please refer to function `sql` in user manual. 
* Added functions `getOS`, `getOSBit`, `parseExpr`, and `dayOfWeek` (**1.00.1**)
* Can specify the startup script through the system parameter 'startup' (**1.00.1**)
* Functions `cancelJob` and `cancelConsoleJob` can cancel tasks that cannot be decomposed into subtasks in for loops (**1.00.1**)
* Added function mmse(**1.00.3**)
* Function `replay` adds the parameter of 'absoluteRate', which supports replaying data at the specified times of the speed of data generation (**1.00.4**)
* Added function `fill!` (**1.00.5**)
* Added math functions:`sinh, cosh, tanh, asinh, acosh, atanh, deg2rad, rad2deg`. (**1.00.7**)
* Added linear programming function: `linprog`. (**1.00.7**)
* Added function `hashBucket` to calculate the partition index of the data to be written, which is convenient for parallel writing. (**1.00.8**)
* Added function `capacity` to get the capacity of a vector, i.e. the number of elements it can hold based on the current memory allocation. (**1.00.9**)
* Added `keyedTable`. When the newly added data has the same primary key value in the keyedTable, it will overwrite the data of the same primary key. (**1.00.10**)
* Added 3 new parameters for function `linprog`: `lb`, `ub` and `method`. `lb` represents the lower bound of the variable; `ub` represents the upper bound of the variable;  `method` represents the optimization algorithm and currently supports 'simplex' and 'interior-point'. (**1.00.11**)


> Improvement:

* `scheduleJob` can call functions defined in DolphinDB modules. 
* Functions `isMonotonic` and `isMonotonicIncreasing` now return true for weakly increasing vectors; function  `isMonotonicDecreasing` now returns true for weakly increasing vectors. (**1.00.2**)
* Besides vector and matrix, functions `nullFill!`, `bfill!`, `ffill!` and `lfill!` can accept in-memory tables as an input parameter and support replacing NULL values in all columns in the entire table. (**1.00.2**)
* Improved time-series aggregator engine to support handling data that are ordered within each group but not in the entire table (**1.00.3**). 
* The window alignment scale of the time-series aggregator engine has been extended to support the minute level. (**1.00.3**)
* Improved the functions for importing text files: `loadText`, `ploadText`, `loadTextEx`, `textChunkDS` and `extractTextScheama`. (**1.00.6**)
    * Can skip a specified number of rows at the beginning of the input files.
    * Can specify a parsing format for date and time types.
    * Can import only the specified columns.
    * For a column that is specified as numeric type, non-numeric characters are ignored. If there are no numbers, a NULL value is returned (previous versions return 0).
    * Can parse comma separators in integers or floating point numbers.
    * Can specify a conversion function in `loadTextEx`. The imported data is processed and then appended to the database table.
*  Modified functions `sum3` and `sum4`. When applied to a matrix, `sum3` and `sum4` calculate the statistics of each row instead of the entire matrix. (**1.00.7**)
*  Modified functions `percentile` and `mpercentile`. Now they use the interpolation method to be consistent with Python pandas instead of the nearest rank method. The interpolation method has 5 options: 'linear', 'lower', 'higher', 'midpoint' and 'nearest'. (**1.00.7**)
*  Improved performance of concurrent operations (query and append) on shared in-memory tables. (**1.00.9**)
*  Improved the efficiency of vector and matrix memory usage. (**1.00.9**)
*  Added checks on the number of rows of a matrix. Now it is not allowed to create a matrix with zero rows. (**1.00.9**)
* Function `createTimeSeriesAggregator` now supports 2 new parameters: 'updateTime' and 'useWindowStartTime'. 'updateTime' can trigger calculations at intervals shorter than those specified by parameter 'step'. 'useWindowStartTime' specifies whether to use the start time or end time of moving windows as the temporal column in the output table. (**1.00.10**)
* Improved deserialization for 'delete' statements by removing the requirement that the 'where' clause of a 'delete' statement must be an expression object. (**1.00.10**)
* Function `getSessionMemoryStat` can now output the IP address and port number of the client. (**1.00.10**)
* Improved function `loadText`. When importing a text file with only the header row and the schema is specified, an empty table is returned instead of throwing an exception. (**1.00.11**)
* Improved the time-series aggregator for streaming data. If there are NULL values in the temporal column or if there are large gaps between two adjacent timestamps, the performance is not affected. (**1.00.11**)
* Improved the data type recognition algorithm of the loadText function. Avoid misrecognizing numeric types as strings or symbol types due to occasional occurrences of symbols representing null values such as null, N / A, etc. (**1.00.13**)
* Improved the function isDuplicated so that it can accept subarray, which is used in partitioned or in-memory tables. (**1.00.13**)
* Function createPartitionedTable can now take a stream table or a mvcc table as a model table. (**1.00.13**)
* Improved code deserialization. That is, when the code is deserialized, if it refers to a shared table that does not exist, an exception is no longer thrown, but the shared table is obtained by calling the function objByName, so that deserialization can continue. (**1.00.13**)




> Bug fix:

* Fixed a bug that causes system crash when updating a table after executing function `reorderColumns!`. 
* Fixed a bug that causes system crash when SQL update or delete statements on partitioned in-memory tables are used with local variables. (**1.00.1**)
* Fixed a memory leaking problem of Raft follower nodes. (**1.00.1**)
* Fixed problems from using module when jobs are serialized to disk. (**1.00.1**)
* Fixed the problem that the server may take longer than usual to restart due to check point issue. (**1.00.1**)
* Fixed a crashing problem when function `createTimeSeriesAggregator` specified multiple keyColumns. (**1.00.2**)
* Fixed the empty data problem of using `loadTableBySQL` to read data from a partitioned table using COMPO partition. (**1.00.2**)
* When a partitioned database contains multiple tables, the cached data may be corrupted after executing `dropPartition` and writing data to one of the tables multiple times. (**1.00.4**)
* Fixed a potential crashing issue in SQL with data prior to the year of 1970. (**1.00.5**)
* Fixed a bug in assignment statements in serialized function views. If the right-hand side of the assignment statement is a constant array and the function view is executed multiple times after serialization, this array may be modified. This may lead to incorrect result or a crash. (**1.00.6**)
* Fixed a bug related to function `loadTable`. When using `loadTable` to load a disk-based sequential (SEQ) partitioned table, if parameter 'partitions' is a vector with N elements, then the first N partitions are loaded instead of the partitions specified in 'partitions'. (**1.00.7**)
* Fixed a scheduled job loading problem. If scheduled jobs use function views, data nodes would fail to restart as these scheduled jobs cannot be loaded. (**1.00.7**)
* Fixed a bug of `dropDatabase`: If the data of a partitioned database only exist in a subset of data nodes in the cluster, empty chunk numbers will be written to the metadata log of the controller node when `dropDatabase` is executed. This will cause the controller node to fail to restart as it fails to replay the log. (**1.00.7**)
* Fixed a potential memory leak problem for string arrays. If some strings in an array or column are longer than 22 bytes, the following operations involving the string array or column may cause a memory leak: (**1.00.8**)
    * In SQL statements, 'group by' is used on the string column and is implemented by a sorting method.
    * In SQL statements, 'order by' is used on multiple columns and the first column is the string column.
    * In SQL statements, 'pivot by' is used on the string column.
    * Apply functions `pivotby`, `contextby`, `groupby`, `semgentby` or `cutpoints` on the string column or array. 
* Lingpro adds parameter verification, otherwise illegal parameters may cause crash. (**1.00.10**)
* Fixed a bug of function `loadText`: when format is specified for nanotimestamp data type, a parsing error will occur. (**1.00.11**)
* Fixed the problem of duplicate key values when appending data to a keyed table. (**1.00.12**)
* Fixed the problem that when applying function `iif` on SYMBOL columns in SQL statements, the server will crash. (**1.00.12**)
* Fixed the problem that when a dimension table is deleted and then recreated, querying the table before the table is populated with data will throw an exception that the table does not exist. (**1.00.12**)
* Fixed a bug: the system throws an exception about inconsistent column lengths when conducting aggregation on a SYMBOL column or a STRING column with a context by clause. (**1.00.12**)
* Fix the bug that parameter `hash` of function `subscribeTable` does not work. (**1.00.13**)
* Fix the bug of calling function `std` in the time series aggregation engine, which returns 0 instead of null when all values are the same. (**1.00.13**)
* Fixed a bug where deserializing a partial application could cause the system to crash. (**1.00.13**)
* Fixed a bug that when function `sum` or `avg` is used in function `createTimeSeriesAggregator` and all rows in a group contain NULL values, the result should be a NULL value instead of 0. (**1.00.14**)
* Fixed a bug in the computation of `sum` or `avg` using a hash approach in SQL statements. If all rows in a group contain NULL values, the result should be a NULL value instead of 0. (**1.00.14**)
* Fixed a bug in Windows version of DolphinDB server where closing a client subscription would cause other subscribers on the same node to fail to accept new messages. (**1.00.14**)
* Fixed parsing errors for strings ending with '\\\\', e.g., "hello\\\\". It no longer throws an exception. (**1.00.14**)
* Fixed the problem that if a function in a module is used in a scheduled job, the module cannot be used after server restart. (**1.00.14**)
* Fixed a bug in linear programming (`linprog`) that the accumulation of rounding errors in iterations may lead to incorrect results. (**1.00.14**)
* Fixed a bug in selecting the top rows after sorting string arrays and non-string arrays sequentially. It may lead to incorrect results of function `isortTop`. (**1.00.14**)
* Fixed a bug where the system would register duplicate module functions when a module file is executed in the console or GUI multiple times. It may lead to system crash or thrown exceptions. (**1.00.14**)




## DolphinDB GUI

* Support synchronizing DolphinDB modules to remote servers.

* Fixed an issue that saving password doesn't take effect. 

* Fixed the problem that module synchronization fails under Microsoft Windows OS enviroment. (**1.00.10**)

* Added the web performance monitoring interface for single mode dolphindb server. (**1.00.10**)

## DolphinDB plugin binary files

*  Plugins including AWS S3, ZLIB, MYSQL, ODBC and HDF5 are packaged under the folder "server/plugins" for this release. 

* [Plugin source code](https://github.com/dolphindb/DolphinDBPlugin)

* ODBC

   The odbc::append method provides an optional parameter 'insertIgnore'. For target databases that support the 'insert ignore' syntax, when parameter 'insertIgore' is specified, duplicate data on the primary key will be ignored. 

## DolphinDB APIs

* JAVA

    Optimized streaming reconnection stability.
    
    Added function `hashBucket` to calculate the partition index of the data to be written, which is convenient for parallel writing. (**1.00.8**)

* C++ 

    Optimized streaming reconnection stability.
    
    Added function `hashBucket` to calculate the partition index of the data to be written, which is convenient for parallel writing. (**1.00.8**)
    
* go 

    Added function `hashBucket` to calculate the partition index of the data to be written, which is convenient for parallel writing. (**1.00.8**)
    
* C# 

    Support new data types UUID and IPADDR.

