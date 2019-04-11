# DolphinDB Release Notes

Release Date : 2019-04-10

Version : 0.95.0

## DolphinDB Server
[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V0.95.0.zip) | 
[Linux32 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux32_V0.95.0.zip) | [Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V0.95.0.zip) | 
[Windows32 binary](http://www.dolphindb.com/downloads/DolphinDB_Win32_V0.95.0.zip) | 
[ARM64 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM64_V0.95.0.zip) | 
[ARM32 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM32_V0.95.0.zip) | 

> New Features

* First release of 32 and 64 bit DolphinDB server for ARM on linux.
* First release of 32 bit DolphinDB server for x86 CPU on windows and linux.
* Added the feature of filtering for streaming data subscription. For example, we can specify a list of stocks when subscribing to a table of stock trades. Only data about these stocks will be published to the subscriber. 
* Added cross-sectional aggregator for streaming clients. With this aggregator, we can easily use built-in or user-defined aggregated functions (e.g. min, max, avg, percentile, median, etc) to process snapshot data cross sectionally. 
* Added the feature of historical data replay. With this new feature, we can use the same script to process both historical data and real-time data. The related functions include `replay` and `replayDS`.
* Added 3 machine learning methods: generalized linear regression, logistic regression and principal component analysis(PCA).
* Added a synchronized dictionary object that supports concurrent data access and manipulation. Use function `syncDict` to create a synchronized dictionary.
* Added a new type of in-memory table (mvcc table) with disk persistence by write-ahead logging (WAL). When appending, updating or deleting rows of a table, another version of the table is created so that concurrent read will not be blocked. The mvcc table is optimal for the use case with frequent read and append, but few update and delete operations.

> Improvements

* Integrated OpenBLAS for matrix multiplication optimization. The performance of large matrix multiplication speeds up 10~20 times.

## DolphinDB APIs

Java API

* Support data filtering when subscribing to a streaming table.

Python API

* The Python API is rewritten in C++. The read/write performance is greatly improved. For batch data upload, the performance is improved 10-30 times; for batch data download, the performance is improved 5-10 times.

C++ API

* Support data filtering when subscribing to a streaming table.

C# API

* Support data filtering when subscribing to a streaming table.

## DolphinDB Plugin

* Updated plugin header file:
  
    [DolphinDBPlugin](https://github.com/dolphindb/release/raw/master/0.95/DolphinDB_Plugin_V0.95.0_src.zip)

* Updated plugin binary files:

    [DolphinDB AWS S3 Plugin](http://www.dolphindb.com/downloads/AWSS3_V0.95.0.zip)

    [DolphinDB ZLIB Plugin](http://www.dolphindb.com/downloads/ZLIB_V0.95.0.zip)

    [DolphinDB HDF5 Plugin](http://www.dolphindb.com/downloads/HDF5_V0.95.0.zip)

    [DolphinDB MYSQL Plugin](http://www.dolphindb.com/downloads/MYSQL_V0.95.0.zip)

    [DolphinDB ODBC Plugin](http://www.dolphindb.com/downloads/ODBC_V0.95.0.zip)

