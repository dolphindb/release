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


> 新功能

* 发布了DolphinDB server 即时编译(JIT)版。详情请参阅 [DolphinDB即时编译(JIT)教程](https://github.com/dolphindb/Tutorials_CN/blob/master/jit.md)。

* 新增函数`capacity`,用于查看一个vector在当前分配的内存中的容量即可以容纳元素的个数。(**1.01.1**)


> 改进

* 字典(Dictionary)和集合(Set)现在支持新的键值类型: UUID、IPADDR、 以及INT128。

* 提升共享内存表的并发性能。(**1.01.1**)

* 提升vector和matrix对内存的使用效率。(**1.01.1**)

* 增加对matrix行数的校验，不允许创建行数为0的matrix。(**1.01.1**)


## DolphinDB Orca

* 发布了[DolphinDB Orca](https://github.com/dolphindb/Orca)项目: 该项目在DolphinDB之上实现了pandas API，使用户能更方便、更高效地分析处理海量数据。
 


