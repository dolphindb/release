# DolphinDB发行说明

## DolphinDB服务器

版本号： 1.20.0

发行日期： 2020-07-08


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.20.0.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.20.0_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.20.0.zip) |
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.20.0_JIT.zip)



> 新功能

* JIT中，允许一个函数的参数是另一个函数（用户自定义函数，lambda函数，部分应用或动态函数）。
* JIT支持某些矩阵操作，例如矩阵元素的访问和修改，矩阵的生成、合并、转置，以及矩阵的加减乘除和内积等基本运算。
* 函数`integral`新增二重积分功能；函数`derivative`新增高阶导数功能。
* 新增统计函数`anova`。 
* 为节约内存、CPU等资源，可将并行执行的任务强制串行执行。在SQL查询语句中可通过提示HINT_SEQ实现串行执行；在`mr`函数中可将参数parallel设置为false实现串行执行。
* 函数`loadText`, `ploadText`, `loadTextEx`支持数据类型uuid，ipaddr和int128。
* 新增函数`cachedTable`用于创建一种特殊的内存表：缓存表(cached table)。例如可在DolphinDB中创建缓存表以存储从MySQL数据库中读取的数据。查询缓存表时，若与上次数据更新相距超过一定时间，会自动更新数据。
* 时间序列聚合引擎新增对`wavg`, `wsum`, `beta`三个函数的优化。
* 支持通过下标访问字符串标量中的元素。
* 新增函数`randMultivariateNormal`以生成多元正态分布随机数。

 

> 改进

* 以下滑动窗口函数增加可选参数minPeriods：mmed, mavg, mmin, mmax, mimin, mimax, msum, mstd, mvar, mmad, mmse, mpercentile, mcorr, mcovar, mwsum, mwavg, mbeta。
* 以下按行处理函数可用于矩阵：rowSum, rowSum2, rowAvg, rowCount, rowStd, rowVar, rowMin, rowMax, rowAnd, rowOr, rowXor, rowProd。
* SQL语句的limit子句允许使用变量。
* 可使用`tableInsert`函数向内存表插入一个字典。字典的键值必须是表的字段名称，字典的值必须是一个tuple。
* 函数`dictUpdate!`增加一个可选参数initFunc。当要更新的键值不存在时，执行initFunc。





