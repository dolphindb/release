# DolphinDB Release Notes

## DolphinDB Server

Version: 1.00.0
Release date: 2019-12-02

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.0.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.0.zip) | 


Version： 1.00.1
Release date： 2019.12.11

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.1.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.1.zip) | 

Version： 1.00.2
Release date： 2019.12.16

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

Version： 1.00.5
Release date： 2019.12.23

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.5.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.5.zip) | 

Version： 1.00.6
Release date： 2020.1.6

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.6.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.6.zip) | 
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
* Added functions `getOS`, `getOSBit`, `parseExpr`, and `dayOfWeek` (**1.00.1**)
* Can specify the startup script through the system parameter 'startup' (**1.00.1**)
* Functions `cancelJob` and `cancelConsoleJob` can cancel tasks that cannot be decomposed into subtasks in for loops (**1.00.1**)
* Added function mmse(**1.00.3**)
* Function `replay` adds the parameter of 'absoluteRate', which supports replaying data at the specified times of the speed of data generation (**1.00.4**)
* Added function `fill!` (**1.00.5**)

> Bug fix:

* Fixed the bug that causes system crash when updating a table after using function `reorderColumns!`. 
* Fixed the bug that causes system crash when SQL update and delete statements on partitioned in-memory tables are used with local variables. (**1.00.1**)
* Fixed memory leaking problem of Raft follower nodes. (**1.00.1**)
* Fixed problems from using module when jobs are serialized to disk. (**1.00.1**)
* Fixed the problem that the server may take longer than usual to restart due to check point issue. (**1.00.1**)
* Fixed a crashing problem when function `createTimeSeriesAggregator` specified multiple keyColumns. (**1.00.2**)
* Fixed the empty data problem of using `loadTableBySQL` to read data from a partitioned table using COMPO partition. (**1.00.2**)
* When a partitioned database contains multiple tables, the cached data may be corrupted after executing `dropPartition` and writing data to one of the tables multiple times. (**1.00.4**)
* Fixed a potential crashing issue in SQL with data prior to the year of 1970. (**1.00.5**)
* Fixed a bug in assignment statements in serialized function views. If the right-hand side of the assignment statement is a constant array and the function view is executed multiple times after serialization, this array may be modified. This may lead to incorrect result or a crash. (**1.00.6**)


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


## DolphinDB GUI

* SQL statements support 3 new types of hint constants: HINT_KEEPORDER, HINT_HASH and HINT_SNAPSHOT. Please refer to function `sql` in user manual. 

* Support synchronizing DolphinDB modules to remote servers.


## DolphinDB plugin binary files

*  Plugins including AWS S3, ZLIB, MYSQL, ODBC and HDF5 are packaged under the folder "server/plugins" for this release. 

* [Plugin source code](https://github.com/dolphindb/DolphinDBPlugin)

* ODBC

   The odbc::append method provides an optional parameter 'insertIgnore'. For target databases that support the 'insert ignore' syntax, when parameter 'insertIgore' is specified, duplicate data on the primary key will be ignored. 

## DolphinDB APIs

* JAVA

    Optimized streaming reconnection stability.

* C++ 

    Optimized streaming reconnection stability.
   
* C# 

    Support for new data types UUID and IPADDR.

