# DolphinDB Release Notes

Release Date : 2019-03-25

Version : 0.94.0

## DolphinDB Server
[Linux binary](http://www.dolphindb.com/downloads/DolphinDB_Linux_V0.94.0.zip) | [Windows binary](http://www.dolphindb.com/downloads/DolphinDB_Win_V0.94.0.zip)

> New Features

* Support streaming connection recovery from network interruption. If there is a network interruption, the system will automatically re-subscribe when the network is reconnected.

> Improvements

* Send sub tasks between nodes in batch mode, which improves the execution performance of jobs containing large number of sub tasks.
* Improve the performance of SQL statement with GROUP BY clause which generates a large number of groups.
* Boost the performance of symbol function and loadText function.

> Bug fixes

* When using function "publishTable", the subscription fails if offset=-1, persistence is enabled and getStreamingStat().MemoryOffset > 0. 
(2019-03-27 0.94.1
[Linux binary](http://www.dolphindb.com/downloads/DolphinDB_Linux_V0.94.1.zip) | [Windows binary](http://www.dolphindb.com/downloads/DolphinDB_Win_V0.94.1.zip) )
## DolphinDB GUI
[binary](http://www.dolphindb.com/downloads/DolphinDB_GUI_V0.94.zip)

*  Add new functions and keywords to autocompletion.
  

## DolphinDB Web Management

> Improvements

* Show query log in reverse chronological order.
* Add "maxPartitionNumPerQuery" option to the panel of node configuration.

## DolphinDB APIs

C# API

* Add C# API for Streaming.

Python API

* Add encryption of user login info when connecting to the DolphinDB server.
* The session object can use setInitScript/getInitScript method to specify a script to be executed automatically when reconnecting.

Java API

* Improve vector reading speed when downloading data.
* Fixed a bug of java streaming API. On some machines, the ip address of the machine will be incorrectly judged as 127.0.0.1, resulting in streaming subscribe and unsubscribe failure.


## DolphinDB Plugin

* Updated plugin header files
  
    [DolphinDBPlugin](https://github.com/dolphindb/release/raw/master/0.94/DolphinDB_Plugin_V0.94.0_src.zip)

* Updated plugin binary files

    [DolphinDB AWS S3 Plugin](http://www.dolphindb.com/downloads/AWSS3_V0.94.0.zip)

    [DolphinDB ZLIB Plugin](http://www.dolphindb.com/downloads/ZLIB_V0.94.0.zip)

    [DolphinDB HDF5 Plugin](http://www.dolphindb.com/downloads/HDF5_V0.94.0.zip)

    [DolphinDB MYSQL Plugin](http://www.dolphindb.com/downloads/MYSQL_V0.94.0.zip)

    [DolphinDB ODBC Plugin](http://www.dolphindb.com/downloads/ODBC_V0.94.0.zip)

