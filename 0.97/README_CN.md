# DolphinDB发行说明

## DolphinDB服务器

版本号 : 0.97.2
发行日期 : 2019-07-24

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V0.97.2.zip) | 
[Linux32 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux32_V0.97.2.zip) | [Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V0.97.2.zip) | 
[Windows32 binary](http://www.dolphindb.com/downloads/DolphinDB_Win32_V0.97.2.zip) | 
[ARM64 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM64_V0.97.2.zip) | 
[ARM32 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM32_V0.97.2.zip) | [Loongson64 binary](http://www.dolphindb.com/downloads/DolphinDB_Loongson64_V0.97.2.zip) 


版本号 : 0.97.1
发行日期 : 2019-07-15

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V0.97.1.zip) | 
[Linux32 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux32_V0.97.1.zip) | [Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V0.97.1.zip) | 
[Windows32 binary](http://www.dolphindb.com/downloads/DolphinDB_Win32_V0.97.1.zip) | 
[ARM64 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM64_V0.97.1.zip) | 
[ARM32 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM32_V0.97.1.zip) | [Loongson64 binary](http://www.dolphindb.com/downloads/DolphinDB_Loongson64_V0.97.1.zip) 

版本号 : 0.97.0
发行日期 : 2019-07-09

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V0.97.0.zip) | 
[Linux32 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux32_V0.97.0.zip) | [Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V0.97.0.zip) | 
[Windows32 binary](http://www.dolphindb.com/downloads/DolphinDB_Win32_V0.97.0.zip) | 
[ARM64 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM64_V0.97.0.zip) | 
[ARM32 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM32_V0.97.0.zip) | [Loongson64 binary](http://www.dolphindb.com/downloads/DolphinDB_Loongson64_V0.97.0.zip) 


> 新功能

* 新增数据保留策略，允许系统自动删除过期数据。

* 新增了saveAsNpy和loadNpy函数用于保存和加载numpy数据文件(npy 文件)。

* VALUE分区类型支持按新增数据动态新增分区。通过`newValuePartitionPolicy`参数启用此功能。

* 增加firstNot函数。[具体信息](https://www.dolphindb.cn/cn/help/firstNot.html)

* 支持三种机器学习算法 K-Means，Naive Bayes，K-nearest neighbors(KNN)。

> 改进

* 完善repartitionDS功能，对复合分区，支持按其某一层分区模式重新分区。[具体信息](https://www.dolphindb.cn/cn/help/repartitionDS.html)

* 若正在进行写入操作时因断电等原因导致写入节点无法使用，只要被写入分区在可用节点上还有至少一份副本，写入操作就不会失败，会顺利完成。

* redo log 配置参数命名变更： logDir变更为redoLogDir，redoLogGCInterval变更为redoLogPurgeInterval，redoLogMx变更为redoLogPurgeLimit。
* 新增在API中设置作业的优先级和并行性的功能 (**0.97.1 2019.07.15**)。

> Bug修复

* 解决当一个functionView依赖另一个functionView时，会导致addFunctionView失败的bug。
* 修复了dropTable的错误。多次删除dfs表可能会导致数据块的版本不一致(**0.97.2 2019.07.24**)。

## DolphinDB GUI

* 增加关键字高亮 `limit`，`VALUE`，`RANGE`，`LIST`。

## DolphinDB plugin binary files:
[DolphinDB AWS S3 Plugin](http://www.dolphindb.com/downloads/AWSS3_V0.97.0.zip)

[DolphinDB ZLIB Plugin](http://www.dolphindb.com/downloads/ZLIB_V0.97.0.zip)

[DolphinDB MYSQL Plugin](http://www.dolphindb.com/downloads/MYSQL_V0.97.0.zip)


    支持将mysql中long类型直接转换成DolphinDB的timestamp类型

[DolphinDB ODBC Plugin](http://www.dolphindb.com/downloads/ODBC_V0.97.0.zip)

[DolphinDB HDF5 Plugin](http://www.dolphindb.com/downloads/HDF5_V0.97.0.zip)

[DolphinDBPlugin](https://github.com/dolphindb/release/raw/master/0.97/DolphinDB_Plugin_V0.97.0_src.zip)


## DolphinDB APIs
Java API
* 修复 streaming API 反订阅失败问题：当没有设置 actionName 参数时，ThreadedClient反订阅会失败。
C# API
* IVector支持add方法动态增加行记录。
