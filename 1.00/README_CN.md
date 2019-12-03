# DolphinDB发行说明

## DolphinDB服务器

版本号： 1.00.0
发行日期： 2019-12-02

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.00.0.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.00.0.zip) | 

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

> Bug修复:

* 对数据表使用`reorderColumns!`函数之后，再进行更新操作会导致crash。

> 改进:

* 允许`scheduleJob`直接或间接调用module中定义的函数。


## DolphinDB GUI

* 支持远程同步 DolphinDB module的功能（Synchronize module to server）。


## DolphinDB plugin binary files

* AWS S3, ZLIB, MYSQL, ODBC, HDF5 等插件已统一打包到 server/plugins 目录下。

* [插件源码](https://github.com/dolphindb/DolphinDBPlugin)

* ODBC

    `append` 方法提供了可选参数insertIgnore, 对于支持insert ignore语法的目标数据库，可以实现忽略主键重复数据的功能。


## DolphinDB APIs

* JAVA

    优化流数据重连稳定性

* C++ 

    优化流数据重连稳定性
   
* C# 

    支持新数据类型 UUID 与 IPADDR

