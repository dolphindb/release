# DolphinDB发行说明

## DolphinDB服务器

版本号： 1.00.0
发行日期： 2019-12-02


# DolphinDB Release Notes

## DolphinDB Server

Version: 1.01.0

Release date: 2020-1-19


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.0.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.0.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.0_JIT.zip) | 
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.0_JIT.zip) | 


Version: 1.01.1

Release date: 2020-1-30


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.1.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.1.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.1_JIT.zip) | 
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.1_JIT.zip) | 


Version: 1.01.2

Release date: 2020-2-15


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.2.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.2.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.2_JIT.zip) | 
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.2_JIT.zip) | 


> 新功能

* 发布了DolphinDB server 即时编译(JIT)版。详情请参阅 [DolphinDB即时编译(JIT)教程](https://github.com/dolphindb/Tutorials_CN/blob/master/jit.md)。

* 新增函数`capacity`,用于查看一个vector在当前分配的内存中的容量即可以容纳元素的个数。(**1.01.1**)

* 即时编译(JIT)版本支持'break'和'continue'语句。(**1.01.2**) 

* 新增函数`keyedTable`以提供键值表。新增数据的主键值若在键值表中已存在，新增数据会覆盖表中相同主键的数据。(**1.01.2**)


> 改进

* 字典(Dictionary)和集合(Set)现在支持新的键值类型: UUID、IPADDR、 以及INT128。

* 提升共享内存表的并发性能。(**1.01.1**)

* 提升vector和matrix对内存的使用效率。(**1.01.1**)

* 增加对matrix行数的校验，不允许创建行数为0的matrix。(**1.01.1**)

* 函数`createTimeSeriesAggregator`增加了updateTime和useWindowStartTime参数。updateTime可用于设置采用比参数step规定更小的时间间隔触发计算。useWindowStartTime用于设置输出表中的时间列采用计算窗口的起始时间或结束时间。(**1.01.2**)

* 完善delete语句的反序列化，取消了where子句过滤条件必须是一个表达式（有运算符）的规则。(**1.01.2**)

* `getSessionMemoryStat`函数会输出客户端的IP地址和端口。(**1.01.2**)

* 对llvm的使用方式进行调优，JIT的性能得到大幅提升。(**1.01.2**)    


> bug 修复

* 增加了`linprog`函数的参数校验，修复非法参数导致crash的问题。(**1.01.2**)

* 修复了在自定义函数中调用函数`parseExpr`导致crash的bug。(**1.01.2**)

## DolphinDB orca

* 发布了[DolphinDB orca](https://github.com/dolphindb/Orca)项目: 该项目在DolphinDB之上实现了pandas API，使用户能更方便、更高效地分析处理海量数据。
* 发布了DolphinDB NumPy。DolphinDB NumPy函数相比NumPy函数能更高效处理orca对象。(**1.01.2**)
* 新增`read_shared_table`函数，用于读取DolphinDB共享流表。(**1.01.2**)
 


