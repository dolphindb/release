# DolphinDB发行说明

## DolphinDB服务器

版本号： 1.10.0

发行日期： 2020-03-16


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.0.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.0_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.0.zip) 


版本号： 1.10.1

发行日期： 2020-03-24


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.1.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.1_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.1.zip) 

版本号： 1.10.2

发行日期： 2020-03-27


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.2.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.2_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.2.zip) 



> 新功能

* DolphinDB脚本抛出异常时，显示调用的stack。
* 允许 context by limit 语句中的limit值为负数，表示取每个组的最后几行数据。
* 即时编译(JIT)版本增加大量数学函数：支持所有累积分布函数及其反函数，以及`sinh`, `cosh`, `tanh`, `asinh`, `acosh`, `atanh`, `deg2rad`, `rad2deg`函数。 
* 新增数学函数：`exp2`, `expm1`, `log2`, `log10`, `log1p`, `cbrt`, `square`。
 
> 改进

* 函数`slice`的参数 rowIndex 和 colIndex 新增了对数组的支持。
* 简单的 context by 语句（select字段中不包含聚合运算或序列相关运算）的性能提升5-10倍。
* 高阶函数`moving`的性能提升约20%。
* 提升了DFS和Raft的稳定性。
* 优化了查询多字段键值内存表时使用in谓词过滤的性能。(**1.10.1**)
* 允许用subarray表示一个空的子数组。子数组的范围允许不指定开始和结束位置。例如:subarray(1..10, 2:)或 subarray(1..10, :5)。(**1.10.2**)

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
* 修复windows jit版本因为jit用户自定义函数抛出异常导致系统crash的bug。(**1.10.1**)
* 修复函数`update！`在有多个过滤条件时更新不正确的bug。(**1.10.2**)
* 修复维度表插入空表导致查询抛出异常的问题。（**1.10.2**）
* 修复函数`iterate`中对参数`input`是否含有空值的错误判断。（**1.10.2**）

## DolphinDB GUI

> bug 修复

* GUI中选择部分代码执行后，log窗口未能正确显示代码的起始及结束行号。



