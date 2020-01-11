# DolphinDB发行说明

## DolphinDB服务器

版本号： 1.00.0
发行日期： 2019-12-02

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.0.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.0.zip) | 


版本号： 1.00.1
发行日期： 2019.12.11

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.1.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.1.zip) | 

版本号： 1.00.2
发行日期： 2019.12.16

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.2.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.2.zip) | 

版本号： 1.00.3
发行日期： 2019.12.18

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.3.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.3.zip) | 


版本号： 1.00.4
发行日期： 2019.12.20

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.4.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.4.zip) | 

版本号： 1.00.5
发行日期： 2019.12.23

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.5.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.5.zip) | 

版本号： 1.00.6
发行日期： 2020.1.6

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.6.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.6.zip) | 

> 新功能

* 增加了基于Raft协议的流数据高可用。 

* 新增以下函数：

    * 时间处理函数`dayOfYear,dayOfMonth,
quarterOfYear,monthOfYear,weekOfYear,hourOfDay,minuteOfHour,secondOfMinute,weekday,yearBegin,yearEnd,businessYearBegin,businessYearEnd,monthBegin,monthEnd,semiMonthBegin,semiMonthEnd,businessMonthBegin,businessMonthEnd,quarterBegin,quarterEnd,quarterBusinessBegin,quarterBusinessEnd,week,lastWeekOfMonth,weekOfMonth,
fy5253,fy5253Quarter,isYearStart,isYearEnd,isQuarterStart,isQuarterEnd,isMonthStart,isMonthEnd,isLeapYear,daysInMonth,weekBegin`

    * 字符串相关函数`isUpper,isLower,isTitle,isSpace,isAlpha,isNumeric,isDigit,isAlNum,isDecimal,charAt`
    * 窗口相关函数`ewmMean,ewmStd,ewmVar,ewmCov,ewmCorr`
    * 数学类函数`isMonotonic,isMonotonicIncreasing,isMonotonicDecreasing,quantile,quantileSeries,cumcount,percentChange,sem,mad`
    * 向量判重函数`nunique`
    * 插值函数`interpolate`

* SQL中支持hint常量 HINT_HASH，HINT_SNAPSHOT，HINT_KEEPORDER，具体用法参考用户手册`sql`函数。

* 新增函数`getOS`, `getOSBit`, `parseExpr`, `dayOfWeek` (**1.00.1**)

* 对于不可分解的简单任务，其循环执行过程也可以被`cancelJob`与`cancelConsoleJob`函数终止。 (**1.00.1**)

* 增加了函数`mmse`(**1.00.3**)

* `replay`函数增加了 absoluteRate 参数，支持以数据产生速度的指定倍数进行回放。 (**1.00.4**)

* 增加了`fill!`函数。 (**1.00.5**)

> Bug修复:

* 对数据表使用`reorderColumns!`函数之后，再进行更新操作会导致crash。

* 针对内存分区表的sql update和sql delete语句如果使用了本地变量会导致crash。 (**1.00.1**)

* 修复在元数据高可用场景下，Follower控制节点内存泄漏问题。 (**1.00.1**)

* 修复job序列化问题。 当一个module函数被多个module调用导致反序列化失败。 (**1.00.1**)

* 修复 single mode 元数据未及时做checkpoint导致重启慢的问题。(**1.00.1**)

* 修复 `createTimeSeriesAggregator` 函数指定多个keyColumn时引起crash问题。(**1.00.2**)

* 修复在多层分区数据库中使用`loadTableBySQL`读取数据为空的问题。 (**1.00.2**)

* 包含多表的分布式库，多次对其中一个表做dropPartition和写入数据后，可能发生缓存数据corrupted异常。 (**1.00.4**)

* 修复sql中涉及1970年之前的日期数据时可能引起crash的问题。 (**1.00.5**)

* 修复了序列化函数视图中赋值语句的一个bug。如果赋值语句右边是常数组，序列化后多次运行该视图函数，这个常数组可能会被修改，导致计算结果有误或crash。 (**1.00.6**)

> 改进:

* 允许`scheduleJob`直接或间接调用module中定义的函数。

* `isMonotonic`, `isMonotonicIncreasing`, `isMonotonicDecreasing`函数由严格单调递增或递减改为非严格递增或递减。(**1.00.2**)

* 除了vector和matrix, `nullFill!`, `bfill!`, `ffill!`, `lfill!` 可以接受内存表作为输入参数，支持对整表所有列替换null值。(**1.00.2**)

* 完善了时序聚合引擎，可以处理仅能保证时间戳在分组内有序的数据流（即不是全局有序数据流）。(**1.00.3**)

* 时序聚合引擎的窗口对齐尺度扩展到支持分钟级别。(**1.00.3**)

* 改进了文本文件数据导入的相关函数`loadText`、`ploadText`、`loadTextEx`、`textChunkDS`以及`extractTextScheama`。（**1.00.6**） 
    * 允许忽略文件开始指定行数。
    * 允许为日期和时间类型指定解析格式。
    * 允许仅导入指定的部分列。
    * 整型或者浮点类型前后有非数字字符则忽略，如果不包含任何数字则返回空值（以前版本返回0）。
    * 可以解析整数或浮点数中的逗号分隔符。
    * `loadTextEx`可以指定一个转换函数。导入的数据转换后再追加到数据库表中。




## DolphinDB GUI

* 支持远程同步 DolphinDB module的功能(Synchronize module to server)。

* 修复保存用户名密码后不生效的问题。


## DolphinDB plugin binary files

* AWS S3, ZLIB, MYSQL, ODBC, HDF5 等插件已统一打包到 server/plugins 目录下。

* [插件源码](https://github.com/dolphindb/DolphinDBPlugin)

* ODBC

    `append` 方法提供了可选参数insertIgnore, 对于支持insert ignore语法的目标数据库，可以实现忽略主键重复数据的功能。


## DolphinDB APIs

* JAVA

    优化流数据重连稳定性
    
    修复了1970年之前的日期转换错误的问题

* C++ 

    优化流数据重连稳定性
   
* C# 

    支持新数据类型 UUID 与 IPADDR

