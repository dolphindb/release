# DolphinDB Release Notes

Release Date : 2019-07-09

Version : 0.97.0

## DolphinDB Server
[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V0.97.0.zip) |
 [Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V0.97.0.zip) 

> New Features
* Added settings for data retention policy, with which an user can periodically delete the partition data before a specified time in the database.
* Added a new data type : datehour. User can use hour with VALUE partition to partition a database table. 
* Added support for numpy data format. You can now  call function `saveAsNpy` to save DolphinDB object as .npy suffix file, then you can load .npy file by calling function `loadNpy`.
* Added dynamically adding partition support for VALUE-based partition.
* Added new function firstNot. [For details, please refer to](https://www.dolphindb.cn/cn/help/firstNot.html)
* Added three new machine learning algorithms: K-Means, Naive Bayes, and K-nearest neighbors(KNN)

> Improvements
* RepartitionDS is fully functional and supports repartitioning by the original partition schema of the database. [Please refer the manual for the details] (https://www.dolphindb.cn/cn/help/repartitionDS.html)
* Added the support for high availability of data nodes: Even if some nodes are not available due to power outage or other reasons, as long as each partition has at least one copy in the cluster, the normal write and read of the cluster can be guaranteed.
* Redo log configuration parameter naming changes: logDir changed to redoLogDir, redoLogGCInterval changed to redoLogPurgeInterval, and redoLogMx changed to redoLogPurgeLimit.

> Bug fixes
* Fixed a synatx error with the functionView nested call. 

## DolphinDB GUI

* Added limit, VALUE, RANGE, LIST keyword support.

## DolphinDB Plugin

* Updated plugin binary files:

    [DolphinDB AWS S3 Plugin](http://www.dolphindb.com/downloads/AWSS3_V0.97.0.zip)

    [DolphinDB ZLIB Plugin](http://www.dolphindb.com/downloads/ZLIB_V0.97.0.zip)

    [DolphinDB MYSQL Plugin](http://www.dolphindb.com/downloads/MYSQL_V0.97.0.zip)

    * Added the support of converting the long type in mysql directly into the timestamp type of DolphinDB

    [DolphinDB ODBC Plugin](http://www.dolphindb.com/downloads/ODBC_V0.97.0.zip)

    [DolphinDB HDF5 Plugin](http://www.dolphindb.com/downloads/HDF5_V0.97.0.zip)

    [DolphinDBPlugin](https://github.com/dolphindb/release/raw/master/0.97/DolphinDB_Plugin_V0.97.0_src.zip)

## DolphinDB APIs

java API

* Fixed the streaming API unsubscription bug: ThreadedClient unsubscribe fails when the actionName parameter is not set.

C# API

* Optimizatized C# API interface: IVector supports the `add` method to dynamically increase row records.
