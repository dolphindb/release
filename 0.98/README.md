# DolphinDB Release Notes


## DolphinDB Server


Version : 0.98.0

Release Date : 2019-09-23


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V0.98.0.zip) | 
[Linux32 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux32_V0.98.0.zip) | [Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V0.98.0.zip) | 
[Windows32 binary](http://www.dolphindb.com/downloads/DolphinDB_Win32_V0.98.0.zip) | 
[ARM64 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM64_V0.98.0.zip) | 
[ARM32 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM32_V0.98.0.zip) | [Loongson64 binary](http://www.dolphindb.com/downloads/DolphinDB_Loongson64_V0.97.0.zip) 


> New Features

* Added meta data high availability.

* Added data cache to improve writing performance.

* Added DFS database support in single node mode.

* Added function addRangePartition to extend RANGE partition.

* Added function textChunkDS to split a text file into multiple data sources.

* Added function migrate for data migration.

* Added statement `go` to support step-by-step execution of scripts.

* Added function eye to generate unit matrix.

* Added function diag to generate diagonal matrix.

* Added snapshot engine to maintain the latest state of the inserted data sequence, suitable for scenarios such as iot.


> Improvements

* To improve security, when the configuration option webLoginRequired is enabled, user must log in to execute scripts and functions.


> Bug fixes

* For a table that does not contain a column of symbol type, when adding a symbol column to it through function addColumn and no data is added, searching the table will cause an exception.

* When using the function toStdJson to convert an empty table to a JSON string, a non-standard JSON string will be returned.

## DolphinDB GUI

* Added highligt for keyword `go`.
 
* Fixed a bug that function plot cannot draw charts other than a line chart when the x-axis is temporal data type.
 
* Added a checkbox on whether function parameter prompt is enabled to solve the problem that the smart reminder panel does not disappear on a few Linux desktops.
 
* Added a database panel to browse distributed databases and table structures.

* Added a button to try to cancel a running task.
 
* Added the option to allow forced exit of GUI.

* Added the login menu to the VSCode plugin.

## DolphinDB plugin binary files:

[DolphinDB AWS S3 Plugin](http://www.dolphindb.com/downloads/AWSS3_V0.98.0.zip)

[DolphinDB ZLIB Plugin](http://www.dolphindb.com/downloads/ZLIB_V0.98.0.zip)

[DolphinDB MYSQL Plugin](http://www.dolphindb.com/downloads/MYSQL_V0.98.0.zip)

[DolphinDB ODBC Plugin](http://www.dolphindb.com/downloads/ODBC_V0.98.0.zip)

[DolphinDB HDF5 Plugin](http://www.dolphindb.com/downloads/HDF5_V0.98.0.zip)

[DolphinDBPlugin](https://github.com/dolphindb/release/raw/master/0.98/DolphinDB_Plugin_V0.98.0_src.zip)


## DolphinDB APIs

* Added go api.
