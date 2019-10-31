# DolphinDB Release Notes

## DolphinDB Server

Version: 0.99.0

Release Date: 2019-10-25

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V0.99.0.zip) | 
[Linux32 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux32_V0.99.0.zip) | [Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V0.99.0.zip) | 
[Windows32 binary](http://www.dolphindb.com/downloads/DolphinDB_Win32_V0.99.0.zip) | 
[ARM64 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM64_V0.99.0.zip) | 
[ARM32 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM32_V0.99.0.zip) | [Loongson64 binary](http://www.dolphindb.com/downloads/DolphinDB_Loongson64_V0.97.0.zip) 


> New Features

* Added 3 new 16-byte data types: UUID, IP and INT128. These data types can be used to create partitioned tables with HASH domain. 

* Added function `createTable` to create dimension tables (non-partitioned tables) in a partitioned database.

* Added function `keyedStreamTable`. A keyedStreamTable does not allow rows with duplicate values of keyColumn. A new record cannot be written to a keyedStreamTable if it has identical value of keyColumn as a row in the keyedStreamTable.

* Added encoding conversion functions: `toUTF8`, `fromUTF8`, and `convertEncode`. For Windows version, only the conversion between gbk and utf-8 is supported. For Linux version, conversions between any encoding are supported.

* Added function `replaceColumn!` to change the content or data type of a column of an in-memory table.

* Added function `reorderColumn!` to adjust the column order of an in-memory table.

* Added function `evaltimer` to assign the execution time of a function to a variable.

* Added function `setColumnComment` to comment on columns of a DFS table.

* Added string functions `md5` and `crc32` to hash a string.

* Added function `hex` to display integers in hexadecimal format.

* Added function `concatDateTime` that combines a DATE-type object and an object of type SECOND, TIME or NANOTIME to one object.  

* Added function `isDuplicated` to mark duplicate values in one or multiple vectors.

> Improvements

* Added function `enableTableShareAndPersistence` to guarantee the atomicity of two operations(`share` and `enableTablePersistence`) on a streaming table, thus solving the problem that concurrent subscriptions may fail due to lack of atomicity.

* Improved the performance of string functions including left, right, startsWith, endsWith, substr, substru, lpad, rpad, strReplace, and strpos

* Function `transpose` now supports dictionaries and tables.

> Upgrade Instructions

* Many new features such as the new data types, dimension table and column comments in this release require the latest version of GUI.

* Must use the latest version of GUI to browse partitioned tables in the variable panel.

* The folder server/web needs to be updated.

## DolphinDB GUI

* Added keywords: UUID, IP and INT128.

* Support schema browsing for partitioned tables.

* Support browsing of dimension tables.

* When there are multiple controllers in a cluster, the web-based cluster manager will automatically locate and jump to the leader controller's URL.

* Added a button to cancel interactive tasks.

* Can close GUI even if a task is running.

## DolphinDB plugin binary files:

[DolphinDB AWS S3 Plugin](http://www.dolphindb.com/downloads/AWSS3_V0.99.0.zip)

[DolphinDB ZLIB Plugin](http://www.dolphindb.com/downloads/ZLIB_V0.99.0.zip)

[DolphinDB MYSQL Plugin](http://www.dolphindb.com/downloads/MYSQL_V0.99.0.zip)

[DolphinDB ODBC Plugin](http://www.dolphindb.com/downloads/ODBC_V0.99.0.zip)

[DolphinDB HDF5 Plugin](http://www.dolphindb.com/downloads/HDF5_V0.99.0.zip)

[DolphinDBPlugin](https://github.com/dolphindb/release/raw/master/0.99/DolphinDB_Plugin_V0.99.0_src.zip)

## DolphinDB APIs

* JAVA API:

    Now support login information loss detection and automatic re-login. 

* C# API:
 
    Now support login information loss detection and automatic re-login.
