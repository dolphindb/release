# DolphinDB Release Notes

Release Date : 2019-04-10

Version : 0.95.0

## DolphinDB Server
[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V0.95.0.zip) | 
[Linux32 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux32_V0.95.0.zip) | [Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V0.95.0.zip) | 
[Windows32 binary](http://www.dolphindb.com/downloads/DolphinDB_Win32_V0.95.0.zip) | 
[ARM64 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM64_V0.95.0.zip) | 
[ARM32 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM32_V0.95.0.zip) 

> New Features

* First release of 32 and 64 bit DolphinDB server for ARM on Linux.
* First release of 32 bit DolphinDB server for x86 CPU on Windows and Linux.
* Added the feature of filtering for streaming data subscription. For example, we can specify a list of stocks when subscribing to a table of stock trades. Only data about these stocks will be published to the subscriber. 
* Added cross-sectional aggregator for streaming clients. With this aggregator, we can calculate cross-sectional metrics with built-in or user-defined aggregated functions (e.g. min, max, avg, percentile, median, etc). 
* Added the feature of historical data replay. With this new feature, we can use the same script to process both historical data and real-time data. The related functions include `replay` and `replayDS`.
* Added 3 machine learning methods: generalized linear regression, logistic regression and principal component analysis (PCA).
* Added a synchronized dictionary object that supports concurrent data access and manipulation. Use function `syncDict` to create a synchronized dictionary.
* Added a new type of in-memory table (mvcc table) that can be persisted to disk by write-ahead logging (WAL). When appending, updating or deleting rows of an mvcc table, another version of the table is created so that concurrent reading will not be blocked. The mvcc table is optimal for the use case with frequent read and append, but few update and delete operations.

> Improvements

* Integrated OpenBLAS for matrix multiplication optimization. The performance of large matrix multiplication speeds up 10~20 times.

> Bug fixes
* Fixed a performance issue of IF statement that executes the branch condition twice. (2019-04-15 0.95.2   [Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V0.95.2.zip) | 
[Linux32 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux32_V0.95.2.zip) | [Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V0.95.2.zip) | 
[Windows32 binary](http://www.dolphindb.com/downloads/DolphinDB_Win32_V0.95.2.zip) | 
[ARM64 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM64_V0.95.2.zip) | 
[ARM32 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM32_V0.95.2.zip) )
* Fixed a potential deadlock issue of function `getJobReturn`. (2019-04-15 0.95.2 )

* Fixed a bug of replay function in the case of multiple table replay. With this fix, the playback of all tables keep pace with each other. (2019-04-11 0.95.1   [Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V0.95.1.zip) | 
[Linux32 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux32_V0.95.1.zip) | [Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V0.95.1.zip) | 
[Windows32 binary](http://www.dolphindb.com/downloads/DolphinDB_Win32_V0.95.1.zip) | 
[ARM64 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM64_V0.95.1.zip) | 
[ARM32 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM32_V0.95.1.zip) )



## DolphinDB APIs

Java API

* Support data filtering and auto-reconnect when subscribing to a streaming table.

Python API

* The Python API is rewritten in C++. The read/write performance is greatly improved. For batch data upload, the performance is improved 10-30 times; for batch data download, the performance is improved 5-10 times.
* Python API now supports subscriptions to streaming tables. It also supports filtering for streaming data subscription and automatic reconnection after disconnection. It works with Python 3.4 to 3.7. The current version does not support jupyter notebook under Linux. 

C++ API

* Support data filtering and auto-reconnect when subscribing to a streaming table.

C# API

* Support data filtering and auto-reconnect when subscribing to a streaming table.

## DolphinDB Plugin

* Updated plugin header file:
  
    [DolphinDBPlugin](https://github.com/dolphindb/release/raw/master/0.95/DolphinDB_Plugin_V0.95.0_src.zip)

* Updated plugin binary files:

    [DolphinDB AWS S3 Plugin](http://www.dolphindb.com/downloads/AWSS3_V0.95.0.zip)

    [DolphinDB ZLIB Plugin](http://www.dolphindb.com/downloads/ZLIB_V0.95.0.zip)

    [DolphinDB HDF5 Plugin](http://www.dolphindb.com/downloads/HDF5_V0.95.0.zip)

    [DolphinDB MYSQL Plugin](http://www.dolphindb.com/downloads/MYSQL_V0.95.0.zip)

    [DolphinDB ODBC Plugin](http://www.dolphindb.com/downloads/ODBC_V0.95.0.zip)

