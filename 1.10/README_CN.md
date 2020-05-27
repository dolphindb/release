# DolphinDB发行说明

## DolphinDB服务器

版本号： 1.10.0

发行日期： 2020-03-16


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.0.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.0_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.0.zip) |
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.0_JIT.zip)


版本号： 1.10.1

发行日期： 2020-03-24


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.1.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.1_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.1.zip) |
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.1_JIT.zip)

版本号： 1.10.2

发行日期： 2020-03-27


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.2.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.2_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.2.zip) |
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.2_JIT.zip)

版本号： 1.10.3

发行日期： 2020-03-30


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.3.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.3_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.3.zip) |
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.3_JIT.zip)


版本号： 1.10.4

发行日期： 2020-04-08


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.4.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.4_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.4.zip) |
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.4_JIT.zip)

版本号： 1.10.5

发行日期： 2020-04-14


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.5.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.5_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.5.zip) |
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.5_JIT.zip)


版本号： 1.10.6

发行日期： 2020-04-22


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.6.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.6_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.6.zip) |
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.6_JIT.zip)


版本号： 1.10.7

发行日期： 2020-05-23


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.7.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.7_JIT.zip) |
[Linux64 ABI=1 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.7_ABI.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.7.zip) |
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.7_JIT.zip)


> 新功能

* DolphinDB脚本抛出异常时，显示调用的stack。
* 允许 context by limit 语句中的limit值为负数，表示取每个组的最后几行数据。
* 即时编译(JIT)版本增加大量数学函数：支持所有累积分布函数及其反函数，以及`sinh`, `cosh`, `tanh`, `asinh`, `acosh`, `atanh`, `deg2rad`, `rad2deg`函数。 
* 新增数学函数：`exp2`, `expm1`, `log2`, `log10`, `log1p`, `cbrt`, `square`。
* 新增函数：`mmad`, `groups`, `ifirstNot`, `ilastNot`, `kama`, `trueRange`。(**1.10.3**)
* 新增`segment`函数，对向量分组，每组为相邻的相同值。例如，[1,1,2,2,1,1,1]被分为3组：[1,1]，[2,2]与[1,1,1]。(**1.10.4**)
* 支持在SQL查询中用top/limit 0或在where条件中使用不成立的标量条件譬如1=0获取一个空表。(**1.10.4**)
* 新增设置参数remoteHost和remotePort。若启动DolphinDB时指定，DolphinDB程序可以作为远端服务器的终端使用。(**1.10.4**)
* 允许对一个矩阵使用lambda函数对其列进行过滤。(**1.10.5**)
* 新增数学函数`integral`和`derivative`，用于计算积分和导数。(**1.10.6**)
* 新增函数`getEnv`，用于获取系统环境变量。例如，在Linux环境下，getEnv("PATH")会返回环境变量PATH的值。(**1.10.6**)
* 新增函数`conditionalFilter(X,condition,filterMap)`。根据给定的字典参数filterMap，若向量condition中某元素为该字典的key，而且向量X中相应位置元素为字典中该key值对应的value中一个元素时，返回true，否则返回false。(**1.10.6**)
* SQL语句增加map子句。使用map子句后，SQL将在相应的分区上分别执行，并简单的将每个分区的执行结果合并。(**1.10.7**)
* SQL语句增加`cgroup by`子句。`cgroup`是`cumulative group`的缩写，表示累计分组。譬如对数据按小时累计分组，并求和，则分别计算第1个小时，前2个小时，前3个小时，...， 直至所有时间之和。(**1.10.7**)
* 新增函数`covertExcelFormula`，将Excel中的公式转化为DolphinDB中的表达式。(**1.10.7**)
* 新增函数`coevent`，统计给定的时间间隔内出现的事件对的次数。(**1.10.7**)
* 新增函数`signum`，返回数据的正负号标志。正数为1，0为0，负数为-1，空值返回空值。(**1.10.7**)
* 新增按行处理数据的横向聚合函数: `rowAnd`，`rowOr`，`rowXor`，`rowProd`。(**1.10.7**)
* 新增滑动窗口函数: `mwavg`和`mwsum`。(**1.10.7**)
* 新增累计窗口函数: `cumavg`, `cumstd`, `cumvar`, `cummed`, `cumsum2`, `cumsum3`, `cumsum4`, `cumwavg`, `cumwsum`, `cumbeta`, `cumcorrr`, `cumcovar`, `cumpercentile`。(**1.10.7**)
 

> 改进

* 函数`slice`的参数 rowIndex 和 colIndex 新增了对数组的支持。
* 简单的 context by 语句（select字段中不包含聚合运算或序列相关运算）的性能提升5-10倍。
* 高阶函数`moving`的性能提升约20%。
* 提升了DFS和Raft的稳定性。
* 优化了查询多字段键值内存表时使用in谓词过滤的性能。(**1.10.1**)
* 函数`subarray`中子数组的起始与结束位置相同，可以指定一个空的子数组。例如：subarray(x, 0:0)。(**1.10.2**)
* 函数`subarray`中子数组允许不指定开始或结束位置。例如：subarray(x, 2:) 或 subarray(x, :5)。(**1.10.2**)
* 函数`iterate`的input参数允许包含空值。空值在计算时视为0处理。(**1.10.3**)
* 提高了函数`iif`的性能。大部分情况下可以提升1倍的性能。(**1.10.4**)
* 函数`loadText`支持以carriage return ('\r')为换行符的文件。(**1.10.4**)
* 把空字符串解析为IP地址时，不再抛出异常，而是解析为空IP地址。(**1.10.4**)
* 函数`char`, `short`, `int`, `long`, `float`和`double`解析字符串时，如果输入的字符串为空或者不是一个数值，返回相应数据类型的空值而不是0。(**1.10.4**)
* 函数`restore`执行过程中，如果出错会抛出异常。(**1.10.4**)
* 函数`migrate`新增支持一次性恢复备份文件夹内所有数据库和表。(**1.10.4**)
* 函数`dropDatabase`和`existsDatabase`中表示数据库路径的参数最后一个字符如果是斜杠或反斜杠，会自动删除。(**1.10.4**)
* 函数`rank`的输入为空的向量时，不再抛出异常，而是返回空的向量。(**1.10.5**)
* 函数`dropPartition`的参数forceDelete为true时，即使指定的partition的副本数为0，也允许删除。(**1.10.5**)
* 函数`dropPartition`的partitionPaths参数表示过滤条件时，如果含有空值则抛出异常。(**1.10.5**)
* 限制分布式数据库操作相关函数(包括 `addValuePartitions`, `addRangePartitions`, `append!`, `createPartitionedTable`, `createTable`, `database`, `dropDatabase`, `setColumnComment`, `setRetentionPolicy`, `tableInsert`) 只能在数据节点上运行。(**1.10.5**)
* 改进if/else语句错误提示：如果if分支或else分支含有不合法内容，会抛出异常。(**1.10.5**)
* 使用函数`submitJob`提交作业时，若同一个jobId参数值被反复使用，允许自动生成的以该jobId参数值与当日日期为前缀的 job ID 数量从1000个增加到10000个。(**1.10.6**)
* 在 SQL 的 update 和 delete 语句中允许使用基于标量的逻辑表达式。例如：1=1，1=0。(**1.10.7**)
* `getStreamingStat().subWorkers` 返回的有关负责订阅的执行线程的数据表中，每个订阅的topic为一行。(**1.10.7**)
* 反订阅流数据表（`unsubscribeTable`）时，会删除执行线程队列中该topic的所有消息。(**1.10.7**)
* 若SQL语句涉及一个表的多个分区，禁止在 where 子句中使用对行序敏感的序列函数，例如`mavg`，`isDuplicated`等。(**1.10.7**)
* 函数`sqlColAlias`增加对 composite column 的支持。(**1.10.7**)
* SQL语句分组计算（context by 或 group by）时，如果个别组因为数据的原因导致计算异常（例如对singluar matrix求逆），不再抛出异常中断SQL语句的执行，而是将该组的计算结果设为空值。(**1.10.7**)
* 执行函数`clearTablePersistence`时，不再阻塞其他函数（例如`getStreamingStat`）访问persistence manager。(**1.10.7**)

> bug 修复

* 修复`backup`函数长时间运行性能逐步下降的问题。
* 修复多个线程并行读取同一个分区表时，若内存不足有可能会导致死锁的问题。
* 修复bug：在函数`createTimeSeriesAggregator`中进行`sum`或者`avg`运算时，当一组中所有行的某个被计算列均为空值时，应该返回空值而不是返回0。(**1.10.1**)
* 修复bug：在SQL语句中，通过哈希算法计算`sum`或者`avg`，并且一组中所有行的某个被计算列均为空值时，应该返回空值而不是返回0。(**1.10.1**)
* 修复bug：Windows版本中，一个客户端订阅关闭导致同一个节点上其它订阅端无法继续接受消息。(**1.10.1**)
* 修复对以字符'\\\\'结尾的字符串（例如"hello\\\\"）的解析错误，不再抛出异常。(**1.10.1**)
* 修复bug：定时作业（scheduled job）中，如果用到了一个module中的函数，server重启后无法使用该module。(**1.10.1**)
* 修复bug：线性规划（`linprog`）中，迭代计算中的舍入误差累积可能会导致计算错误。(**1.10.1**)
* 修复bug：字符串数组与非字符串数组先后进行排序后，选择位置最前的指定数量的行的结果有误。这个bug会影响`isortTop`函数的正确性。(**1.10.1**)
* 修复bug：若通过console或者GUI多次运行module文件，系统会重复注册module函数，导致系统crash或者抛出异常。(**1.10.1**)
* 删除对矩阵应用`slice`函数的某些情况下console中不必要的输出。(**1.10.1**)
* 修复bug：Windows jit版本因为jit用户自定义函数抛出异常导致系统crash。(**1.10.1**)
* 修复bug：函数`update!`在有多个过滤条件时结果不正确。(**1.10.2**)
* 修复bug：对空的维度表插入空表导致查询抛出异常。（**1.10.2**）
* 修复bug：函数`iterate`的参数input不含空值时，系统可能会误认为含有空值，导致参数校验失败。（**1.10.2**）
* 修复bug：对一个FLOAT或DOUBLE向量，当`array`函数的default参数设为0-0.5之间时，会错误地对该向量元素赋值为0。(**1.10.3**)
* 修复bug：若SQL查询语句中列出的字段显式或隐式的使用了相同的别名，会导致系统崩溃。该bug自版本1.10.0中引入。(**1.10.3**)
* 修复bug：在context by或group by之后使用order by，如果需要排序的字段已经是用户指定的顺序（不需要重排），产生的查询结果（内存表）若继续用于计算，在对排序字段进行处理时可能产生不正确的结果。(**1.10.4**)
* 修复bug: 在context by查询语句中使用`trueRange`函数结果可能不正确。(**1.10.4**)
* 修复bug: 当在API或`remoteRun`函数中远程调用一个部分应用函数时，如果生成部分应用函数之时抛出异常，会导致系统crash。该bug自版本1.10.0中引入。(**1.10.4**)
* 修复bug: 函数`loadText`, `ploadText`以及`loadText`解析以'.'或者'-.'为起始的代表数字的字符串会出现错误。例如，'.12'或者'-.12'会被错误地解析为12。该bug自版本1.00.6中引入。(**1.10.4**)
* 修复bug: 函数`convertEncode`在Linux版本不起作用。(**1.10.5**)
* 修复bug: 若流数据订阅函数(`subscribeTable`)的参数msgAsTable为false，并且最新一批次输入的消息只有一条满足过滤条件时，会把一条不一定满足过滤条件的消息发送给客户端。(**1.10.5**)
* 修复bug: 分区表使用聚合函数时可能产生重复字段异常。例如：在分布式表的group by计算过程中，如果用到MapReduce，中间过程产生的临时字段名为col+数字，例如col1，col2，等等。如果恰巧和分组字段名相同，会产生字段重复错误。(**1.10.5**)
* 修复bug: 极小概率下函数`loadText`将DOUBLE类型解析为DATE类型。(**1.10.5**)
* 修复bug: 若共享内存表中至少一列为大数组(big array)，删除全部数据时会出现内存泄漏。(**1.10.6**)
* 修复bug: JIT中若无法确定变量类型，可能会在后续编译时发生错误，导致运行时crash或者执行效率降低等情况。修复bug后，若无法确定变量类型，会中止编译并报告该变量名称。(**1.10.6**)
* 修复bug: 在key为LONG类型，value为ANY类型的字典中查找一个key值时可能找不到数据。这是版本1.10.3引入的bug。(**1.10.6**)
* 修复bug: 修复共享内存表进行等值关联（`ej`）时可能导致crash的bug。若一个线程删除两个共享内存表的全部数据然后添加新数据，而另一个线程对这两个共享内存表按多个字段进行等值关联，并且关联字段中包括字符串类型字段，可能导致系统crash。(**1.10.6**)
* 修复bug：流数据横截面聚合引擎按时间间隔定时输出模式下，每次输入数据时均有可能触发计算。(**1.10.7**)
* 修复bug：rpc调用时如果部分应用（partial application）的参数不规范可能导致系统crash。(**1.10.7**)
* 修复bug: 数据表采用值分区时，SQL的where子句如果使用or连接多个同时包含分区字段和非分区字段的过滤条件，可能导致输出的行数比预期更多。(**1.10.7**)
* 修复bug: `wsum`函数的参数均为空值时返回0，应返回空值。(**1.10.7**)

## DolphinDB GUI

> bug 修复

* GUI中选择部分代码执行后，log窗口未能正确显示代码的起始及结束行号。



