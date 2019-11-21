# DolphinDB发行说明

## DolphinDB服务器

版本号 : 0.99.0
发行日期 : 2019-10-25

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V0.99.0.zip) | 
[Linux32 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux32_V0.99.0.zip) | [Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V0.99.0.zip) | 
[Windows32 binary](http://www.dolphindb.com/downloads/DolphinDB_Win32_V0.99.0.zip) | 
[ARM64 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM64_V0.99.0.zip) | 
[ARM32 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM32_V0.99.0.zip) | [Loongson64 binary](http://www.dolphindb.com/downloads/DolphinDB_Loongson64_V0.97.0.zip) 

版本号 : 0.99.1
发行日期 : 2019-11-5

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V0.99.1.zip) | [Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V0.99.1.zip) 

版本号 : 0.99.2
发行日期 : 2019-11-10

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V0.99.2.zip) | [Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V0.99.2.zip) 

版本号 : 0.99.3 [官网下载]
发行日期 : 2019-11-14

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V0.99.3.zip) | [Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V0.99.3.zip) 

版本号 : 0.99.4 [西部数据紧急修复]
发行日期 : 2019-11-19

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V0.99.4.zip) 


> 新功能

* 增加了 UUID, IP, INT128 三种16字节数据类型。 支持用新数据类型对数据库进行HASH分区。

* 新增函数`createTable`， 用于支持分区数据库中创建维度表（非分区表）。

* 新增带关键列流数据表`keyedStreamTable`，可以支持定义表关键列。当数据写入流表时，对于关键列重复的数据，仅保留最早进入的一条。

* 新增`toUTF8`, `fromUTF8`, `convertEncode`转换编码函数。对于Windows目前支持支gbk和utf-8之间的相互转换。对于Linux版本，支持任意encoding之间的转换。

* 新增函数 `replaceColumn!`，用于更换内存表原有字段的数据类型 。

* 新增函数 `reorderColumn!`，用于调整内存表原有字段顺序。

* 增加`evalTimer`函数，返回函数的执行时间。

* 增加`setColumnComment`函数，用于对DFS表的字段注释。

* 增加了字符串函数`md5`和`crc32`，用于对字符串进行哈希。

* 增加了`hex`函数，用于以16进制方式显示整型数据。
 
* 增加了`concatDateTime`函数，将Date和Second、Time、Nanotime等时间类型合并。

* 新增dailyAlignedBar, charAt, weekOfMonth 函数(**0.99.4**)



> 改进

* 增加了`enableTableShareAndPersistence`函数，用于保证流数据表`share`和`enableTablePersistence`的两个操作的原子性，从而解决多客户端并发订阅时可能导致订阅失败的问题。

* 优化了字符串操作函数的性能，这些函数包括`left`, `right`, `startsWith`, `endsWith`, `substr`, `substru`, `lpad`, `rpad`, `strReplace`,`strpos`。
 
* `transpose`(`flip`)函数增加了对 dictionary 和 table 的支持。

* 增加了`isDuplicated`函数，标记出向量中重复值或表中的重复行。

* streReplace参数允许SYMBOL类型 (**0.99.1**)

* flip函数支持tuple类型(**0.99.4**)

* 优化 recorderColumns!函数，重排列序时不需要指定所有列。(**0.99.4**)

* 当使用update创建新的列时，即使数据为空向量，也创建新列。(**0.99.4**)

> Bug fix:

* 当symbol数量超出限制时，抛出异常之后再次尝试写入成功，导致后续访问越界crash (**0.99.1**)

* 修复mpercentile函数对有空值的向量操作时，多次重复执行会发生crash的问题 (**0.99.2**)

* 修复流数据订阅下标为-1时重连失败的问题。(**0.99.2**)

* 在高写入压力下, 高可用集群有小概率发生控制节点死锁。(**0.99.3**)


> 升级说明

* 此版本中新增的数据类型、维度表、列注释等功能需要最新版本的GUI支持。
 
* Server更新到此版本后，GUI中变量面板查看分区表功能需要最新版本的GUI才能使用。

* 此版本升级时需要更新server/web目录。

## DolphinDB GUI

* 支持了UUID, IP, INT128三种新数据类型。

* 增加了对分布式数据表浏览Schema。

* 支持维度表的数据查看。

* 当集群中有多个controller时，集群管理器会自动定位并跳转到leader controller的网址。

* 增加取消交互任务功能。

* 增加任务执行中强制退出功能。

## DolphinDB plugin binary files:

[DolphinDB AWS S3 Plugin](http://www.dolphindb.com/downloads/AWSS3_V0.99.0.zip)

[DolphinDB ZLIB Plugin](http://www.dolphindb.com/downloads/ZLIB_V0.99.0.zip)

[DolphinDB MYSQL Plugin](http://www.dolphindb.com/downloads/MYSQL_V0.99.0.zip)

[DolphinDB ODBC Plugin](http://www.dolphindb.com/downloads/ODBC_V0.99.0.zip)

[DolphinDB HDF5 Plugin](http://www.dolphindb.com/downloads/HDF5_V0.99.0.zip)

[DolphinDBPlugin](https://github.com/dolphindb/release/raw/master/0.98/DolphinDB_Plugin_V0.99.0_src.zip)

## DolphinDB APIs

* JAVA

    增加登录信息丢失检测及自动重登录功能
    
* C# 

    增加登录信息丢失检测及自动重登录功能

