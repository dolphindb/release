# DolphinDB Release Notes

Release Date : 2018-12-24

Version : 0.8

## DolphinDB Server
[Linux binary](http://www.dolphindb.com/downloads/DolphinDB_Linux_V0.8.zip) | [Windows binary](http://www.dolphindb.com/downloads/DolphinDB_Win_V0.8.zip)

> New Features

* DolphinDB driver for Grafana to display streaming data more conveniently.
* Add a streaming data aggregation engine.
* Add function quadprog for quadratic programming.
* Add many functions for job scheduling.
* Add machine learning functions randomForestClassifier and randomForestRegressor.
* Add function addValuePartitions to dynamically increase partitions for value domain. 
* Add 14 cumulative distribution functions, 12 inverse cumulative distribution functions and 13 random numbers generator functions for frequently used distributions.
* Add functions atImax and atImin.
* Add functions skew and kurtosis.
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
* Java API [source](https://github.com/dolphindb/api-java)

* C# API [source](https://github.com/dolphindb/api-csharp)

* Python API [source](https://github.com/dolphindb/api-python3)

* JSON API [source](https://github.com/dolphindb/api-json)

* C++ API [source](https://github.com/dolphindb/api-cplusplus)

* R API [source](https://github.com/dolphindb/api-r)

## DolphinDB Plugins
* JDBC [binary](http://www.dolphindb.com/downloads/DolphinDB_JDBC_V0.8.zip) | [source](https://github.com/dolphindb/release/blob/master/0.8/DolphinDB_JDBC_V0.8_src.zip)
* Excel add-in [binary](http://www.dolphindb.com/downloads/DolphinDB_Excel_V0.8.zip) | [source](https://github.com/dolphindb/release/blob/master/0.8/DolphinDB_Excel_V0.8_src.zip)
* ODBC plugin [binary](http://www.dolphindb.com/downloads/ODBC_V0.8.zip) | [source](https://github.com/dolphindb/release/blob/master/0.8/DolphinDB_Plugin_V0.8_src.zip)
* AWS S3 plugin [binary](http://www.dolphindb.com/downloads/AWSS3_V0.8.zip) | [source](https://github.com/dolphindb/release/blob/master/0.8/DolphinDB_Plugin_V0.8_src.zip)
* zlib plugin [binary](http://www.dolphindb.com/downloads/ZLIB_V0.8.zip) | [source](https://github.com/dolphindb/release/blob/master/0.8/DolphinDB_Plugin_V0.8_src.zip)
* HDF5 Plugin [binary](http://www.dolphindb.com/downloads/HDF5_V0.8.zip)|[source](http://www.dolphindb.com/downloads/HDF5_V0.8_src.zip)]
