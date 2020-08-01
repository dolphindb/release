# DolphinDB发行说明

## DolphinDB服务器

版本号： 1.20.0

发行日期： 2020-07-08


[Linux64 binary](http://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.20.0.zip) | 
[Linux64 JIT binary](http://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.20.0_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.20.0.zip) |
[Windows64 JIT binary](http://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.20.0_JIT.zip)

版本号： 1.20.1

发行日期： 2020-07-20


[Linux64 binary](http://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.20.1.zip) | 
[Linux64 JIT binary](http://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.20.1_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.20.1.zip) |
[Windows64 JIT binary](http://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.20.1_JIT.zip)


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
* 新增矩阵LU分解函数`lu`。(**1.20.1**)
* 新增函数`mprod`计算滑动窗口内数字的累乘。(**1.20.1**)
* 新增函数`saveModule`将模块序列化成二进制格式；新增函数`loadModule`与配置变量preloadModules，两者皆可用来预加载模块或插件。(**1.20.1**)
* 新增回归函数`ridge`, `lasso`和`elasticNet`。(**1.20.1**)

 

> 改进

* 以下滑动窗口函数增加可选参数minPeriods：`mmed`,`mavg`,`mmin`,`mmax`,`mimin`,`mimax`,`msum`,`mstd`,`mvar`,`mmad`,`mmse`,`mpercentile`,`mcorr`,`mcovar`,`mwsum`,`mwavg`,`mbeta`。
* 以下按行处理函数可用于矩阵：`rowSum`,`rowSum2`,`rowAvg`,`rowCount`,`rowStd`,`rowVar`,`rowMin`,`rowMax`,`rowAnd`,`rowOr`,`rowXor`,`rowProd`。
* SQL语句的limit子句允许使用变量。
* 可使用`tableInsert`函数向内存表插入一个字典。字典的键值必须是表的字段名称，字典的值必须是一个tuple。
* 函数`dictUpdate!`增加一个可选参数initFunc。当要更新的键值不存在时，执行initFunc。
* 高阶求导时使用基于LU分解的矩阵求逆，以提高计算精度。(**1.20.1**)
* SQL UPDATE语句增加了校验，要求更新的对象必须为表(table)类型。(**1.20.1**)
* 时间类型转换函数支持使用tuple（元组）作为输入参数，涉及的函数包括：`date`,`month`,`year`,`hour`,`minute`,`second`,`time`,`datetime`,`datehour`,`timestamp`,`nanotime`,`nanotimestamp`,`weekday`,`dayOfWeek`,`dayOfYear`,`dayOfMonth`,`quarterOfYear`,`monthOfYear`,`weekOfYear`,`hourOfDay`,`minuteOfHour`,`secondOfMinute`,`millisecond`,`microsecond`,`nanosecond`。(**1.20.1**)
* 提升分布式数据库的稳定性，包括提升了数据版本不一致时事务决议的稳定性，以及减少了心跳发送延迟的可能性。(**1.20.1**)
* `contextby`函数允许输入的groupingCol参数为空数组。(**1.20.1**)

> Bug fixes:

* 函数`mmax`和`mmin`的输入数据类型为bool，char或short，并且设置了可选参数minPeriods时，输出结果的第一个值若预期为空，实际结果与预期不符。(**1.20.1**)
* 开启控制节点高可用后，若单个事务涉及太多分区导致RAFT消息长度超过64K，重启后重放RAFT消息时，元数据会被截断。(**1.20.1**)
* 若SQL语句中启用了 WHERE 子句，GROUP BY 子句包含多个字段，并且第二个或其后的分组字段使用了`segment`函数，输出的结果不符合预期。(**1.20.1**)

> Web集群管理器

* 开启控制节点高可用后，若重新选举了控制节点leader，访问集群管理器首页时，校验集群管理器地址对应的控制节点是否为控制节点leader，若不是则提示控制节点leader信息。(**1.20.1**)

> 插件

* 要求MySQL插件函数`load`和`loadEx`中参数startRow必须为非负整数。


> Python API

* 修复使用session方法loadTable以加载指定分区时，抛出非正确异常的bug。

> C++ API 

* 修复从C++ API订阅流数据，无法正常退出的bug。
* 去除了C++ API动态库对openssl的依赖。
* Linux C++ API动态库增加支持 D_GLIBCXX_USE_CXX11_ABI=1的版本。
