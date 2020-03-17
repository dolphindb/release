# DolphinDB发行说明

## DolphinDB服务器

版本号： 1.10.0

发行日期： 2020-03-16


# DolphinDB Release Notes

## DolphinDB Server

版本号： 1.10.0

发行日期： 2020-03-16


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.0.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.10.0_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.10.0.zip) 


> 新功能

* DolphinDB脚本抛出异常时，显示调用的stack。

* 允许 context by limit 语句中的limit值为负数，表示取每个组的最后几行数据。

* 即时编译(JIT)版本增加大量数学函数：支持所有累积分布函数及其反函数，以及`sinh`, `cosh`, `tanh`, `asinh`, `acosh`, `atanh`, `deg2rad`, `rad2deg`函数。 

* 新增数学函数：`exp2`, `expm1`, `log2`, `log10`, `log1p`, `cbrt`, `square`。
 
> 改进

* 函数`slice`的行列的下标参数 rowIndex 和 colIndex 新增了对数组的支持。

* 简单的 context by 语句（select字段中不包含聚合运算或序列相关运算）的性能提升5-10倍。

* 高阶函数`moving`的性能提升约20%。

* 提升了DFS和Raft的稳定性。

> bug 修复

* 修复`backup`函数长时间运行性能逐步下降的问题。 

* 修复了多个线程并行读取同一个分区表时，若内存不足有可能会导致死锁的问题。

## DolphinDB GUI

> bug 修复

* GUI中选择部分代码执行后，log窗口未能正确显示代码的起始及结束行号。




 
