# DolphinDB Release Notes

Release Date : 2018-12-24

Version : 0.8

## DolphinDB Server
[Linux binary](http://www.dolphindb.com/downloads/DolphinDB_Linux_V0.8.zip) | [Windows binary](http://www.dolphindb.com/downloads/DolphinDB_Win_V0.8.zip)

> New Features

* DolphinDB driver for Grafana to present streaming data more conveniently.
* Add an aggregation engine for streaming data.
* Add function quadprog for quadratic programming.
* Add the feature of resource scheduling and management.
* Add function addValuePartitions to dynamically add partitions for value domain. 
* Add 14 cumulative distribution functions, 12 inverse cumulative distribution functions and 13 random numbers generator functions for frequently used distributions.
* Add aggregated functions atImax and atImin.
* Add aggregated functions skew and kurtosis.
* Support Chinese column names and variable names.

> Improvements

* Warning about insufficient disk space in log files.
* Enhance distributed file system stability under stress tests.

> Fixed

* Error message on the web interface when the web server log file reaches certain size.
* RSA decryption bug.

## DolphinDB GUI
[binary](http://www.dolphindb.com/downloads/DolphinDB_GUI_V0.8.zip)

 *  Improve formatting when INT and CHAR data types are exported to EXCEL.
 *  Support script with UTF-8 encoding.

## DolphinDB APIs
JDBC [source](https://github.com/dolphindb/jdbc)

 * new released.

C# API [source](https://github.com/dolphindb/api-csharp)
 
 > Improvements
 * Support UTF-8 encoding.
 * Try reconnect and login when network anomaly detected.

Python API [source](https://github.com/dolphindb/api-python3)
 
 > Improvements
 * Support UTF-8 encoding.
 * Add Nan value for every data type. 
 > Fixed 
 * NULL value upload error 

## DolphinDB Plugins

* Excel add-in [binary](http://www.dolphindb.com/downloads/DolphinDB_Excel_V0.8.zip) | [source](https://github.com/dolphindb/release/blob/master/0.8/DolphinDB_Excel_V0.8_src.zip)
* ODBC plugin [binary](http://www.dolphindb.com/downloads/ODBC_V0.8.zip) | [source](https://github.com/dolphindb/release/blob/master/0.8/DolphinDB_Plugin_V0.8_src.zip)
* AWS S3 plugin [binary](http://www.dolphindb.com/downloads/AWSS3_V0.8.zip) | [source](https://github.com/dolphindb/release/blob/master/0.8/DolphinDB_Plugin_V0.8_src.zip)
* zlib plugin [binary](http://www.dolphindb.com/downloads/ZLIB_V0.8.zip) | [source](https://github.com/dolphindb/release/blob/master/0.8/DolphinDB_Plugin_V0.8_src.zip)
* HDF5 Plugin [binary](http://www.dolphindb.com/downloads/HDF5_V0.8.zip) | [source](https://github.com/dolphindb/release/blob/master/0.8/DolphinDB_Plugin_V0.8_src.zip)
