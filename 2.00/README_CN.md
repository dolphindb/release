# DolphinDB发行说明

## DolphinDB服务器

版本号： 2.0.0

发行日期： 2021-07-31

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.0.0.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.0.0_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.0.0_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.0.0.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.0.0_JIT.zip)



> 新功能

* 发布TSDB存储引擎。`database`函数提供了一个可选参数engineType，默认值为OLAP，即旧的存储引擎。如果创建基于TSDB存储引擎的数据库，engineType设置为TSDB即可。(**2.00.0**)
* 基于TSDB存储引擎的数据支持新的数据类型BLOB。(**2.00.0**)
