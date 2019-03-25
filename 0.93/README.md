# DolphinDB Release Notes

Release Date : 2019-03-18

Version : 0.93.4

## DolphinDB Server
[Linux binary](http://www.dolphindb.com/downloads/DolphinDB_Linux_V0.93.4.zip) | [Windows binary](http://www.dolphindb.com/downloads/DolphinDB_Win_V0.93.4.zip)



> New Features

* Add functions "getAggregatorStat, "getAggregator" and "removeAggregator" for streaming aggregator management.

> Improvements

* Optimize the performance of SQL statements with "pivot by" clause.
* Add published streaming tables to the output of function "getStreamingStat". 

> Bug fixes and sub releases

* Fixed the specical characters ('"', '+', etc) handling issue when parsing data with Grafana API. (2019-03-18 0.93.4)
* Fixed a bug that the DolphinDB process may crash when multiple sessions open the same dfs-based database and assign this database object to a variable (2019-03-13 0.93.3  [Linux binary](http://www.dolphindb.com/downloads/DolphinDB_Linux_V0.93.3.zip) | [Windows binary](http://www.dolphindb.com/downloads/DolphinDB_Win_V0.93.3.zip))
* Fixed a bug of SQL statement with "pivot by" clause. With a large pivoting table (with more than millions of rows), the DolphinDB process may crash due to a bug on big array sorting. (2019-03-11 0.93.2 [Linux binary](http://www.dolphindb.com/downloads/DolphinDB_Linux_V0.93.2.zip) | [Windows binary](http://www.dolphindb.com/downloads/DolphinDB_Win_V0.93.2.zip))
* Fixed a bug of nested query on partitioned table join. If one of the table objects to join is a subquery on a distributed table, the query will cause crash. (2019-03-05 0.93.1 [Linux binary](http://www.dolphindb.com/downloads/DolphinDB_Linux_V0.93.1.zip) | [Windows binary](http://www.dolphindb.com/downloads/DolphinDB_Win_V0.93.1.zip))

## DolphinDB APIs

* Add C++ API for streaming.

## DolphinDB Plugin

* Updated plugin header files
  
    [DolphinDBPlugin](https://github.com/dolphindb/release/raw/master/0.93/DolphinDB_Plugin_V0.93_src.zip)

* Updated plugin binary files

    [DolphinDB AWS S3 Plugin](http://www.dolphindb.com/downloads/AWSS3_V0.93.zip)

    [DolphinDB ZLIB Plugin](http://www.dolphindb.com/downloads/ZLIB_V0.93.zip)

    [DolphinDB HDF5 Plugin](http://www.dolphindb.com/downloads/HDF5_V0.93.zip)

    [DolphinDB MYSQL Plugin](http://www.dolphindb.com/downloads/MYSQL_V0.93.zip)

    [DolphinDB ODBC Plugin](http://www.dolphindb.com/downloads/ODBC_V0.93.zip)

