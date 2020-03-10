# DolphinDB发行说明

## DolphinDB服务器

版本号： 1.01.0

发行日期： 2020-01-19


# DolphinDB Release Notes

## DolphinDB Server

版本号： 1.01.0

发行日期： 2020-01-19


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.0.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.0.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.0_JIT.zip) | 
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.0_JIT.zip) | 


版本号： 1.01.1

发行日期： 2020-01-30


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.1.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.1.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.1_JIT.zip) | 
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.1_JIT.zip) | 


版本号： 1.01.2

发行日期： 2020-02-15


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.2.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.2.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.2_JIT.zip) | 
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.2_JIT.zip) | 

版本号： 1.01.3

发行日期： 2020-02-28

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.3.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.3.zip) | 

版本号： 1.01.4

发行日期： 2020-03-05

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.4.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.4.zip) | 


> 新功能

* 发布了DolphinDB server 即时编译(JIT)版。详情请参阅 [DolphinDB即时编译(JIT)教程](https://github.com/dolphindb/Tutorials_CN/blob/master/jit.md)。

* 新增函数`capacity`,用于查看一个vector在当前分配的内存中的容量，即可以容纳元素的个数。(**1.01.1**)

* 即时编译(JIT)版本支持'break'和'continue'语句。(**1.01.2**) 

* 新增函数`keyedTable`以提供键值表。新增数据的主键值若在键值表中已存在，新增数据会覆盖表中相同主键的数据。(**1.01.2**)
 
* `linprog`函数新增三个参数：lb, ub 与 method。lb表示变量的下界。ub表示变量的上界。method表示算法，目前支持'simplex'和'interior-point'。(**1.01.3**)


> 改进

* 字典(Dictionary)和集合(Set)现在支持新的键值类型: UUID, IPADDR 以及 INT128。

* 提升共享内存表的并发性能。(**1.01.1**)

* 提升vector和matrix的内存使用效率。(**1.01.1**)

* 增加对matrix行数的校验，不允许创建行数为0的matrix。(**1.01.1**)

* 函数`createTimeSeriesAggregator`增加了updateTime和useWindowStartTime参数。updateTime可用于设置采用比参数step规定更小的时间间隔触发计算。useWindowStartTime用于设置输出表中的时间列采用计算窗口的起始时间或结束时间。(**1.01.2**)

* 完善delete语句的反序列化，取消了where子句过滤条件必须是一个表达式（有运算符）的规则。(**1.01.2**)

* `getSessionMemoryStat`函数会输出客户端的IP地址和端口。(**1.01.2**)

* 对llvm的使用方式进行调优，JIT的性能得到大幅提升。(**1.01.2**)    

* 改进了`loadText`的一个功能：对只包含header的文本文件，若用户指定了schema, `loadText`函数不再抛出异常，而是返回一个空表。(**1.01.3**)

* 改进了流数据时间序列聚合引擎。当时间列出现空值或前后两条数据时间跨度较大时，性能不会下降。(**1.01.3**)


> bug 修复

* 增加了`linprog`函数的参数校验，修复非法参数导致crash的问题。(**1.01.2**)

* 修复了在自定义函数中调用函数`parseExpr`导致crash的bug。(**1.01.2**)

* 修复了`loadText`的一个bug：为nanotimestamp数据类型指定format时出现解析错误。(**1.01.3**) 

* 修复了向键值表中追加(append)数据会产生重复键值的问题。(**1.01.4**)
 
* 修复了在SQL语句中对SYMBOL类型字段使用`iif`函数时，发生crash的问题。(**1.01.4**)

* 修复了已存有数据的维度表被删除并重建后，查询数据时，显示该表不存在的bug。此bug仅发生在重建维度表之后，未写入数据之前。(**1.01.4**)

* 修复了在使用context by的SQL语句中对字符串或SYMBOL类型字段分组求聚合时，系统报告列长不一致的bug。(**1.01.4**)
 

## DolphinDB orca

* 发布了[DolphinDB orca](https://github.com/dolphindb/Orca)项目: 该项目为DolphinDB提供了pandas API，使用户能更方便、更高效地在pandas中使用DolphinDB分析处理海量数据。

* 发布了DolphinDB NumPy。DolphinDB NumPy函数相比NumPy函数可更高效处理orca对象。(**1.01.2**)

* 新增`read_shared_table`函数，用于读取DolphinDB共享流数据表。(**1.01.2**)
 


