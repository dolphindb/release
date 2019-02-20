# DolphinDB Release Notes

Release Date : 2019.02.18

Version : 0.9

## DolphinDB Server
[Linux binary](http://www.dolphindb.com/downloads/DolphinDB_Linux_V0.90.zip) | [Windows binary](http://www.dolphindb.com/downloads/DolphinDB_Win_V0.90.zip)

> New Features

* Support dynamically adding new columns in distributed tables and streaming tables. 
* A new type of in-memory table that supports concurrent read and write: mvccTable.
* Left join now includes left join (lj) and left semi join (lsj).
* New keyword "csort" in SQL for in-group sorting of the result of "context by" clauses.
* New function "isSorted" to judge if a vector has been sorted.
* New configuration parameter "webLoginRequired". 
* New function "getSessionMemoryStat" for memory usage monitoring.

> Improvements

* Optimize the performance of "select top ..." statements.
* Optimize the performance of functions "find", "asof" and "binarySearch" on subarrays. 

## DolphinDB GUI
[binary](http://www.dolphindb.com/downloads/DolphinDB_GUI_V0.90.zip)

*  Support adjusting font size.
*  Support adjusting tab size.

## DolphinDB APIs

JDBC [source](https://github.com/dolphindb/jdbc)
* Implement method "setQueryTimeout" of java.sql.Statement, which prevents the system from waiting too long for running queries. 


C# API [source](https://github.com/dolphindb/api-csharp)
* Add "initialScript" mode to automatically execute the initialization script when reconnecting to DolphinDB server.

## DolphinDB Plugins

* Provide MySql plugin to import data or query results from MySql to DolphinDB. 
MySql Plugin [binary](http://www.dolphindb.com/downloads/MYSQL_V0.90.zip) | [source](https://github.com/dolphindb/DolphinDBPlugin/tree/master/mysql)

  