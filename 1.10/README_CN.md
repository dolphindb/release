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


> 新功能

* DolphinDB脚本抛出异常时，显示调用的stack。
* 允许 context by limit 语句中的limit值为负数，表示取每个组的最后几行数据。
* 即时编译(JIT)版本增加大量数学函数：支持所有累积分布函数及其反函数，以及`sinh`, `cosh`, `tanh`, `asinh`, `acosh`, `atanh`, `deg2rad`, `rad2deg`函数。 
* 新增数学函数：`exp2`, `expm1`, `log2`, `log10`, `log1p`, `cbrt`, `square`。
* 新增函数：`mmad`, `groups`, `ifirstNot`, `ilastNot`, `kama`, `trueRange`。(**1.10.3**)
* 新增`segment`函数，对向量分组，每组为相邻的相同值。例如，[1,1,2,2,1,1,1]被分为3组：[1,1]，[2,2]与[1,1,1]。(**1.10.4**)
* 支持在SQL查询中用top/limit 0或在where条件中使用不成立的标量条件譬如1=0获取一个空表。(**1.10.4**)
* 新增设置参数remoteHost和remotePort。若启动DolphinDB时指定，DolphinDB程序可以作为远端服务器的终端使用。(**1.10.4**)

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
* 函数`loadText`支持以carriage return （'\r'）为换行符的文件。(**1.10.4**)
* 把空字符串解析为IP地址时，不再抛出异常，而是解析为空IP地址。(**1.10.4**)
* 函数`char`, `short`, `int`, `long`, `float`和`double`解析字符串时，如果输入的字符串为空或者不是一个数值，返回相应数据类型的空值而不是0。(**1.10.4**)
* 在使用函数`restore`数据的过程中，如果出错会抛出异常。之前只记log。(**1.10.4**)
* 函数`migrate`新增支持一次性回复备份文件夹内所有数据库和表。(**1.10.4**)
* 函数`dropDatabase`和`existsDatabase`的路径最后一个字符如果是斜杠或反斜杠，会自动删除。(**1.10.4**)


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
* 修复bug: 修复在context by查询语句中使用`trueRange`函数结果可能不正确的bug。(**1.10.4**)
* 修复bug: 当在API或`remoteRun`函数中远程调用一个部分应用函数时，如果生成部分应用函数之时抛出异常，会导致系统crash。该bug自版本1.10.0中引入。(**1.10.4**)

## DolphinDB GUI

> bug 修复

* GUI中选择部分代码执行后，log窗口未能正确显示代码的起始及结束行号。



