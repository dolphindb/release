# DolphinDB Release Notes

Release Date : 2019-03-13

Version : 0.93.3

## DolphinDB Server
[Linux binary](http://www.dolphindb.com/downloads/DolphinDB_Linux_V0.93.3.zip) | [Windows binary](http://www.dolphindb.com/downloads/DolphinDB_Win_V0.93.3.zip)


> Bug fixes

* Fixed a concurrency issue of dfs database
* Fixed a bug in LocklessBoundlessQueue
* Fixed the null crash bug in TableJoiner

Release Date : 2019-03-11

Version : 0.93.2

## DolphinDB Server
[Linux binary](http://www.dolphindb.com/downloads/DolphinDB_Linux_V0.93.2.zip) | [Windows binary](http://www.dolphindb.com/downloads/DolphinDB_Win_V0.93.2.zip)


> Bug fixes

* Fixed a crashing bug caused by nested query
* Fixed the bug of lockless version SymbolBase
* Fixed the bug of function drop
* Fixed a crashing bug of hash partition
* Fixed the bug of sort function on big arrays
* Fixed the bug of batch-mode remote call
* Fixed the overflow bug of function wsum
* Fixed the bug of append method of symbol vector


Release Date : 2019-03-05

Version : 0.93.1

## DolphinDB Server
[Linux binary](http://www.dolphindb.com/downloads/DolphinDB_Linux_V0.93.1.zip) | [Windows binary](http://www.dolphindb.com/downloads/DolphinDB_Win_V0.93.1.zip)


> Bug fixes

* Fix a crashing bug caused by nested query


Release Date : 2019-03-04

Version : 0.93

## DolphinDB Server
[Linux binary](http://www.dolphindb.com/downloads/DolphinDB_Linux_V0.93.zip) | [Windows binary](http://www.dolphindb.com/downloads/DolphinDB_Win_V0.93.zip)

> New Features

* Add functions including "getAggregatorStat, "getAggregator", and "removeAggregator" for streaming aggregator management

> Improvements

* Optimize the performance of SQL statement: pivot by.
* Add published streaming tables to the output of getStreamingStat function

> Bug fixes

* Fixed a bug in sorting of bigarray
* Fixed the bug of pivot by clause
* Fixed a bug of SQL Engine. It would cause crash of a query with recusive table join on streaming tables
* Fixed the bug of lowerBound method in bigarray
* Fixed a bug of parsing a function call that doesn't exist in sql statement


## DolphinDB APIs

C++ API

* Add C++ API for Streaming.

## DolphinDB Plugin

* Updated plugin header files
  
    [DolphinDBPlugin](https://github.com/dolphindb/release/raw/master/0.93/DolphinDB_Plugin_V0.93_src.zip)

* Updated plugin binary files

    [DolphinDB AWS S3 Plugin](http://www.dolphindb.com/downloads/AWSS3_V0.93.zip)

    [DolphinDB ZLIB Plugin](http://www.dolphindb.com/downloads/ZLIB_V0.93.zip)

    [DolphinDB HDF5 Plugin](http://www.dolphindb.com/downloads/HDF5_V0.93.zip)

    [DolphinDB MYSQL Plugin](http://www.dolphindb.com/downloads/MYSQL_V0.93.zip)

    [DolphinDB ODBC Plugin](http://www.dolphindb.com/downloads/ODBC_V0.93.zip)

