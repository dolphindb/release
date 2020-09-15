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

版本号： 1.20.2

发行日期： 2020-08-15


[Linux64 binary](http://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.20.2.zip) | 
[Linux64 JIT binary](http://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.20.2_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.20.2.zip) |
[Windows64 JIT binary](http://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.20.2_JIT.zip)

版本号： 1.20.3

发行日期： 2020-08-31


[Linux64 binary](http://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.20.3.zip) | 
[Linux64 JIT binary](http://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.20.3_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.20.3.zip) |
[Windows64 JIT binary](http://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.20.3_JIT.zip)

版本号： 1.20.4

发行日期： 2020-09-14


[Linux64 binary](http://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.20.4.zip) | 
[Linux64 JIT binary](http://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.20.4_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.20.4.zip) |
[Windows64 JIT binary](http://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.20.4_JIT.zip)

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
* 新增矩阵分解函数`schur`, `svd`和`qr`。(**1.20.2**)
* 新增函数`indexedTable`，用于创建内存索引表。内存索引表的键值字段用树结构进行排序，允许使用包含第一个键值字段的若干键值字段进行快速查找。(**1.20.2**)
* 新增函数`autocorr`和`acf`，用于计算时间序列的自相关性。(**1.20.2**)
* 新增函数`sliceByKey`，用于快速访问键值表和内存索引表。与通过SQL语句查询相比，耗时降低约50%。(**1.20.2**)
* 新增函数`manova`，用于多元方差分析。(**1.20.2**)
* 增加新函数`closeSessions`，允许管理员关闭指定的一个或多个会话，以释放连接和内存。(**1.20.2**)
* 新增函数`getChunksMeta`和`getTabletsMeta`，以获取数据节点上分区(chunk)和分区子表(tablet)的元数据和统计信息，譬如分区占用的磁盘空间、数据表的行数和版本号等。(**1.20.2**)
 
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
* 使用OpenBLAS和LAPACK改进以下矩阵相关函数的性能：`inverse`, `solve`, `det`和`cholesky`。用于大矩阵时，性能有10~50倍的提升。(**1.20.2**)
* 函数`lu`可以分解一个不是方阵的矩阵。(**1.20.2**)
* `schema`函数的输出中增加一个标签partitionTypeName，用以描述分区类型。(**1.20.2**)
* 函数`in`和`find`支持对键值表和内存索引表按键值进行查找。(**1.20.2**)
* 函数`syncDict`增加一个可选参数sharedName。如果指定参数sharedName，那么创建的字典将被节点上的所有会话共享。(**1.20.2**)
* 函数`getSessionMemoryStat`的输出增加了两个字段createTime和lastActiveTime，分别记录会话创建时间和最近一次访问时间。并且更正了字段remotePort的输出值。(**1.20.2**)
* 函数`getConsoleJobs`的输出增加了两个字段remoteIP和remotePort。(**1.20.2**)
* 函数`backup`支持并行备份，以提升效率。(**1.20.2**)
* 常量赋值给一个变量时，会复制一个对象，避免在多线程并行计算时因对引用计数进行并发修改导致的系统效率降低。(**1.20.2**)
* 提升了RAFT一致性协议实现的稳定性。(**1.20.2**)
* 使用TCMalloc管理内存池。提升了内存分配效率，尤其在多线程并行计算时小内存的分配效率有大幅提升。同时解决了DolphinDB实际占用的内存超过配置参数maxMemSize设定值的问题，以及尚有内存剩余时创建字符串出现OOM的问题。(**1.20.3**)
* 使用函数`saveText`将DOUBLE类型数据保存到文件时，保留小数点后最多15位的精度。(**1.20.3**)
* 横截面聚合引擎引入了可选参数useSystemTime。当该参数为false时，结果中的时刻为数据中的时刻。本功能可以更好的支持回放历史数据进行仿真。(**1.20.3**)
* 高斯朴素贝叶斯（gaussianNB）模型进行分类预测时，使用likelihood的对数形式，使得高维度的情况下仍然可以使用该模型进行分类。(**1.20.3**)
* 主成分分析（`pca`函数）改用lapack的svd算法提升性能。(**1.20.3**)
* `pca`函数新增 svdSolver, randomState 两个参数。(**1.20.3**)
* `logisticRegression`函数新增 regularizationCoeff 参数。(**1.20.3**)
* `backup`函数新增parallel参数，以支持并行备份。(**1.20.3**)
* 配置项 dfsReplicaReliabilityLevel 增加了可配置项 `=2`，在资源允许情况下，副本优先使用多物理机分布策略。(**1.20.3**)
* SQL语句中的PIVOT BY子句的行分组从一个字段扩展到多个字段，输出的指标也从一个扩展到多个。(**1.20.4**)
* unionAll函数增加了可选参数byColName。当这个参数为true时，多个表的列按照字段名称而不是字段的顺序来对齐。这种情况下，也允许多个表有不同的列，缺失的列用空值填充。(**1.20.4**)
* 允许三个以上参数的自定义聚合函数在dolphindb.dos中声明map reduce和running aggregation的实现。(**1.20.4**)
* 大幅提升了有问题的数据节点重新接入集群后数据恢复的性能。避免了个别分区由于数据恢复时间过长导致的写入中断。(**1.20.4**)
* 支持从外网订阅DolphinDB节点上的流数据表。(**1.20.4**)

> Bug fixes:

* 函数`mmax`和`mmin`的输入数据类型为bool，char或short，并且设置了可选参数minPeriods时，输出结果的第一个值若预期为空，实际结果与预期不符。(**1.20.1**)
* 开启控制节点高可用后，若单个事务涉及太多分区导致RAFT消息长度超过64K，重启后重放RAFT消息时，元数据会被截断。(**1.20.1**)
* 若SQL语句中启用了 WHERE 子句，GROUP BY 子句包含多个字段，并且第二个或其后的分组字段使用了`segment`函数，输出的结果不符合预期。(**1.20.1**)
* 所有数据相同时，函数`mvar`和`cumvar`的结果可能会出现极小负值；`mstd`和`cumstd`的结果可能会出现空值。(**1.20.2**)
* socket连接时可能会产生内存泄漏。(**1.20.2**)
* 1.20.1版本中引入的`ridge`, `lasso`和`elasticNet`三个回归函数的若干稳定性问题。(**1.20.2**)
* `adaBoostRegressor`函数在某些情况下运行时崩溃。(**1.20.2**)
* 高可用集群在线增加一个数据节点后，创建新的数据库分区到新节点时，可能导致新增节点崩溃。(**1.20.2**)
* 使用JSON进行web调用时，如果没有指定tag 'functionName' 会导致节点崩溃。在使用Grafana访问DolphinDB时，可能遇到这个问题。(**1.20.3**)
* 日期和时间类型函数（`date`, `timestamp`等）处理一组字符串时，如果某些字符串无法被转换为日期和时间类型，那么相应的元素返回空值，但返回的vector内部未设置包含空值元素的标志，导致`isValid`和`isNull`等函数的返回与预期不符。(**1.20.3**)
* 使用`fromJson`函数处理JSON字符串时，若没有包含tag 'value'，可能导致节点崩溃。(**1.20.3**)
* 修复RAFT的snapshot checkpoint实现中的一个bug。它可能导致leader切换时耗时特别长。(**1.20.3**)
* 若配置项newValuePartitionPolicy=add（允许系统自动增加值分区），当有多个并发写入线程在短时间内快速增加大量新分区时（通常是在压力测试或开发环境中），有可能出现分区丢失的现象，即无法查询到写入数据库的数据。(**1.20.4**)
* replace和replace!函数的新值为浮点数时，小数部分会被忽略，造成错误结果。(**1.20.4**)
* 使用内存分区表作为mr和imr函数的数据源会导致系统crash。。(**1.20.4**)

#### DolphinDB 插件

* Mysql插件

    * 要求MySQL插件函数`load`和`loadEx`中参数startRow必须为非负整数。

* HDF5插件    

    * LoadHDF5EX 函数增加了 transform 参数，支持在导入时自定义数据转换逻辑。(**1.20.4**)

* httpClient插件    

    * 增加邮件发送函数 `sendEmail` 。(**1.20.4**)
    * `httpGet`, `httpPost`函数增加了 headers 参数用于填写http请求的头部信息。(**1.20.4**)


#### 客户端工具

* Web集群管理器

    * 开启控制节点高可用后，若重新选举了控制节点leader，访问集群管理器首页时，校验集群管理器地址对应的控制节点是否为控制节点leader，若不是则提示控制节点leader信息。(**1.20.1**)
    * 修复了高可用集群中在线增加数据节点后，无法动态加载的问题。(**1.20.2**)
    * 在高可用集群中的follower控制节点中登录时，返回的用户名密码错误的信息，修改为返回正确的提示信息，并给出当前activeMaster的别名信息。(**1.20.2**)。

* GUI

    * 增加了用户手册和GUI帮助的链接
    * 柱状图的柱形宽度随x轴数值自动调整。
    * 在状态栏显示当前连接的会话ID

#### API 

* Python API

    * 修复使用`session.loadTable`加载指定分区抛出异常。(**0.1.15.23**)
    * 增加支持 ipaddr, uuid, int238类型。(**0.1.15.23**)
    * 增加支持 month 数组。(**0.1.15.23**)
    * 增加`hashBucket`函数。(**0.1.15.23**)
    * 发布1.20.2.0对应DolphinDB 1.20.2
    * 发布1.10.12.0对应DolphinDB 1.10.12
    * 发布1.0.24.1对应DolphinDB 1.00.24
    

* Orca:

    * 修复了`rolling`函数当输入类型为float32并存在nan时，计算出错的问题。(**0.1.15.23**)
    * 修复了`read_table`加载分布式表报参数异常的问题。(**0.1.15.23**)
    * 发布1.20.2.0对应DolphinDB Server 1.20.2
    * 发布1.10.12.0对应DolphinDB Server 1.10.12
    * 发布1.0.24.1对应DolphinDB Server 1.00.24

* C++ API 

    * 修复从C++ API订阅流数据，无法正常退出的bug。(**1.20.2**)
    * 去除了C++ API动态库对openssl的依赖。(**1.20.2**)
    * Linux C++ API动态库增加支持 D_GLIBCXX_USE_CXX11_ABI=1的版本。(**1.20.2**)

* Java API

    * 增加了Upload返回值反序列化处理，不影响用户调用接口。(**1.20.2**)

* C# API

    * 增加了Upload返回值反序列化处理，不影响用户调用接口。(**1.20.2**)

* Node.js API

    * 新增了API支持Node.js运行环境下连接DolphinDB。(**1.20.2**)


