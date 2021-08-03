# DolphinDB Release Notes

## DolphinDB Server

Version： 2.0.0

Releate Date： 2021-07-31

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.0.0.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.0.0_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.0.0_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.0.0.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.0.0_JIT.zip)



> New Features

* Released the TSDB storage engine. The `database` function provides an optional parameter engineType, the default value is OLAP, which is the old storage engine. If you create a database based on the TSDB storage engine, set the engineType to TSDB. (**2.00.0**)
* The data based on the TSDB storage engine supports the new data type BLOB. (**2.00.0**)
