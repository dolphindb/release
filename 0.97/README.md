# DolphinDB Release Notes



## DolphinDB Server

Version : 0.97.2
Release Date : 2019-07-24

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V0.97.2.zip) | 
[Linux32 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux32_V0.97.2.zip) | [Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V0.97.2.zip) | 
[Windows32 binary](http://www.dolphindb.com/downloads/DolphinDB_Win32_V0.97.2.zip) | 
[ARM64 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM64_V0.97.2.zip) | 
[ARM32 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM32_V0.97.2.zip) | [Loongson64 binary](http://www.dolphindb.com/downloads/DolphinDB_Loongson64_V0.97.2.zip) 

Version : 0.97.0
Release Date : 2019-07-09

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V0.97.0.zip) | 
[Linux32 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux32_V0.97.0.zip) | [Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V0.97.0.zip) | 
[Windows32 binary](http://www.dolphindb.com/downloads/DolphinDB_Win32_V0.97.0.zip) | 
[ARM64 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM64_V0.97.0.zip) | 
[ARM32 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM32_V0.97.0.zip) | [Loongson64 binary](http://www.dolphindb.com/downloads/DolphinDB_Loongson64_V0.97.0.zip) 



> New Features
* Added data retention policy that enables the system to automatically delete expired data according to the given data expiration policy.
* Added function `saveAsNpy` to save DolphinDB objects as npy files(numpy data files). 
* Added function `loadNpy` to load npy files as DolphinDB objects.
* Now supports dynamically adding new partitions based on new data for the VALUE partition type. Use parameter 'newValuePartitionPolicy' to enable this feature
* Added new function `firstNot`.
* Added 3 new machine learning algorithms: K-Means, Naive Bayes and K-nearest neighbors(KNN).

> Improvements
* For COMPO partitions, function `repartitionDS` allows re-partitioning according to the original partition scheme of a given partition layer.
* When writing to a partition on a node and the node becomes unavailable due to reasons such as power outage, as long as the partition has at least one copy on available data nodes, the writing operation will finish successfully.
* Redo log configuration parameter name changes: 'logDir' is now 'redoLogDir', 'redoLogGCInterval' is now 'redoLogPurgeInterval', 'redoLogMx' is now 'redoLogPurgeLimit'.
* Can set priority and parallelism of jobs in APIs (**0.97.2 2019.07.24**). 

> Bug fixes
* Fixed the bug that the command `addFunctionView` fails when a functionView depends on another functionView.
* Fixed a bug with command `dropTable`. Dropping a dfs table for multiple times may cause version inconsistency of tablet chunks. (**0.97.2 2019.07.24**)

## DolphinDB GUI

* Added keyword highlights for `limit`, `VALUE`, `RANGE` and `LIST`.
* Published the visual studio code plugin to support editing and executing DolphinDB scripts in visual studio code. [Plugin installation](https://marketplace.visualstudio.com/items?itemName=dolphindb.dolphindb-vscode)

## DolphinDB Plugin

* Updated plugin binary files:

    [DolphinDB AWS S3 Plugin](http://www.dolphindb.com/downloads/AWSS3_V0.97.0.zip)

    [DolphinDB ZLIB Plugin](http://www.dolphindb.com/downloads/ZLIB_V0.97.0.zip)

    [DolphinDB MYSQL Plugin](http://www.dolphindb.com/downloads/MYSQL_V0.97.0.zip)

    * Supports converting the long type in MySQL directly into the timestamp type of DolphinDB.

    [DolphinDB ODBC Plugin](http://www.dolphindb.com/downloads/ODBC_V0.97.0.zip)

    [DolphinDB HDF5 Plugin](http://www.dolphindb.com/downloads/HDF5_V0.97.0.zip)

    [DolphinDBPlugin](https://github.com/dolphindb/release/raw/master/0.97/DolphinDB_Plugin_V0.97.0_src.zip)

## DolphinDB APIs

Java API

* Fixed a bug in streaming API unsubscription: ThreadedClient cannot successfully unsubscribe when parameter 'actionName' is not specified.

C# API

*  IVector can use method `add` to dynamically append rows.
