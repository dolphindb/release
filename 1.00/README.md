# DolphinDB Release Notes

## DolphinDB Server

Version: 1.00.0
Release date: 2019-12-02

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.0.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.0.zip) | 

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

> Bug fix:

* Fixed the bug that causes system crash when updating a table after using function `reorderColumns!`. 
* Fixed the bug that causes system crash when SQL update and delete statements on partitioned in-memory tables are used with local variables. (**1.00.1**)
* Fixed memory leaking problem of Raft follower nodes. (**1.00.1**)
* Fixed problems from using module when jobs are serialized to disk. (**1.00.1**)

> Improvement:

* `scheduleJob` can call functions defined in DolphinDB modules. 


## DolphinDB GUI

* SQL statements support 3 new types of constants: HINT, HINT_KEEPORDER, HINT_HASH and HINT_SNAPSHOT.

* Support synchronizing DolphinDB module to remote server.


## DolphinDB plugin binary files

*  Plugins including AWS S3, ZLIB, MYSQL, ODBC and HDF5 are packaged under the folder "server/plugins" for this release. 

* [Plugin source code](https://github.com/dolphindb/DolphinDBPlugin)

* ODBC

   The odbc::append method provides an optional parameter 'insertIgnore'. For target databases that support the 'insert ignore' syntax, when parameter 'insertIgore' is specified, duplicate data on the primary key will be ignored. 

## DolphinDB APIs

* JAVA

    Optimize streaming reconnection stability

* C++ 

    Optimize streaming reconnection stability
   
* C# 

    Support for new data types UUID and IPADDR

