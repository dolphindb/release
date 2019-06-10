# DolphinDB Release Notes

Release Date : 2019-06-03

Version : 0.96.0

## DolphinDB Server
[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V0.96.0.zip) | 
[Linux32 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux32_V0.96.0.zip) | [Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V0.96.0.zip) | 
[Windows32 binary](http://www.dolphindb.com/downloads/DolphinDB_Win32_V0.96.0.zip) | 
[ARM64 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM64_V0.96.0.zip) | 
[ARM32 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM32_V0.96.0.zip) | [Loongson64 binary](http://www.dolphindb.com/downloads/DolphinDB_Loongson64_V0.96.0.zip) 

> New Features

* Added a new higher order function `pcross`. It is the parallel computing version of function `cross`. (2019-06-10 0.96.1   [Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V0.96.1.zip) | 
[Linux32 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux32_V0.96.1.zip) | [Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V0.96.1.zip) | 
[Windows32 binary](http://www.dolphindb.com/downloads/DolphinDB_Win32_V0.96.1.zip) | 
[ARM64 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM64_V0.96.1.zip) | 
[ARM32 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM32_V0.96.1.zip) | [Loongson64 binary](http://www.dolphindb.com/downloads/DolphinDB_Loongson64_V0.96.1.zip)
* Now support connection from Redash via JSON or URL. Redash is an open source application to query your data sources, visualize the results, build dashboards and share data with your team. (2019-06-10 0.96.1)
* Released DolphinDB Loongson Edition.
* Supports dynamically adding data nodes to a running DolphinDB cluster without restarting the cluster.
* Provide a set of functions to rebalance data across nodes in case of data skew.
* Provide Spark connector to access data in DolphinDB from Spark.
* DFS tables support backup and recovery.
* Added anomaly detection engine for real-time anomaly detection in streaming data.


> Improvements

* Performance improvements for the R API.
* Improved the performance of the time-series aggregator for streaming data by 5-27 times.
* Command `dropPartition` now supports removing any level of partitions with specified filter.
* Added redo log for  distributed tables to ensure newly written data will not be lost in case of power outage.
* The cross-sectional aggregator now can be used as a cross-sectional snapshot table. Metric expressions and grouping columns can be empty.
* Support cleaning up stream table persistence log files according to given retention policy.


> Bug fixes

* Fixed the issue that the DFS Explorer in cluster manager does not support table names in Chinese.
* Fixed a bug of SQL query with top clause or where clause on dynamically added columns.

## DolphinDB GUI

* Fixed the issue that setting the font size only works for currently open files.

## DolphinDB Plugin

* Added the new plugin of trade matching engine, which matches up bids and offers to complete trades. (2019-06-10 0.96.1)

* Updated plugin header file:
  
    [DolphinDBPlugin](https://github.com/dolphindb/release/raw/master/0.96/DolphinDB_Plugin_V0.96.1_src.zip)

* Updated plugin binary files:

    [DolphinDB AWS S3 Plugin](http://www.dolphindb.com/downloads/AWSS3_V0.96.0.zip)

    [DolphinDB ZLIB Plugin](http://www.dolphindb.com/downloads/ZLIB_V0.96.0.zip)

    [DolphinDB MYSQL Plugin](http://www.dolphindb.com/downloads/MYSQL_V0.96.0.zip)

    [DolphinDB ODBC Plugin](http://www.dolphindb.com/downloads/ODBC_V0.96.0.zip)

* ODBC plugin now supports unicode and gb2312 encoding. 