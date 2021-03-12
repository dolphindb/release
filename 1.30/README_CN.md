# DolphinDB发行说明

## DolphinDB服务器

版本号： 1.30.0

发行日期： 2020-12-29

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.0.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.0_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.0_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.0.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.0_JIT.zip)

版本号： 1.30.1

发行日期： 2021-01-12

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.1.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.1_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.1_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.1.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.1_JIT.zip)

版本号： 1.30.2

发行日期： 2021-01-25

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.2.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.2_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.2_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.2.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.2_JIT.zip)

版本号： 1.30.3

发行日期： 2021-02-28

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.3.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.3_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.3_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.3.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.3_JIT.zip)

> 新功能

* 新增数据结构索引矩阵（indexed matrix）和索引序列（indexed series）用于面板数据的处理。索引矩阵之间、索引序列之间、以及索引矩阵和索引序列之间的二元操作，支持按行列标签自动对齐。
* 新增函数`panel`，`indexedSeries`, `setIndexedMatrix!`, `setIndexedSeries!`, `isIndexedMatrix`, `isIndexedSeries`，`dropna`，`resample`，`asFreq`，`merge`等用于处理索引矩阵和索引序列。
* 新增函数`renameTable`，允许分布式的维度表和分区表改名。
* 新增高阶函数`withNullFill`。
* 新增权限DB_OWNER。拥有该权限的用户可以创建数据库并进行管理。
* 新增函数`upsert!`向键值表或索引表中添加或更新记录。
* `schema`函数增加了分区列类型(partitionColumnType)的输出。
* 新增响应式状态引擎（reactive state engine）用于流计算。相关的函数包括`createReactiveStateEngine`和`warmupStreamEngine`。(**1.30.2**)
* 新增函数`ema`，`mskew`，`mkurtosis`和`mslr`。(**1.30.2**)
* 支持新的数据类型复数(COMPLEX)和点(POINT)。使用函数complex和point分别构造上述两种数据类型。(**1.30.3**)
* 响应式状态引擎和时间序列聚合引擎支持快照，用于保存这些引擎的状态，以便在流计算出现异常时，快速从上一个快照处恢复。(**1.30.3**)
* 新增函数`mskew`，`mkurtosis`，`mvarp`, `mstdp`, `cumvarp`, `cumstdp`，并且在响应式状态引擎中支持上述函数。(**1.30.3**)
* 新增函数`winsorize`。(**1.30.3**)
* 新增高阶函数`byRow`，使得一个列式函数，可用于矩阵按行计算。(**1.30.3**)
* 内置的流数据计算引擎包括时间序列聚合引擎、横截面引擎、异常检测引擎和响应式状态引擎，支持多个引擎串联。(**1.30.3**)

> 改进

* 优化SYMBOL类型的数据序列化/反序列化。这个优化使DolphinDB数据节点之间以及数据节点和API之间传输SYMBOL类型数据时性能有5~10倍的提升。
* 提升了并行作业和分布式作业的稳定性。
* 允许矩阵的行数或列数为0。
* 函数subscribeTable增加了可选参数timeTrigger。当参数为true时，即便没有新的消息进入，到达设定的时间间隔后，也会触发消息处理函数。
* 当需要序列化的字符串标量长度超过65535个字节时，自动转化为BLOB类型进行序列化。(**1.30.1**)
* window join的自定义指标函数支持多个返回值。(**1.30.2**)
* 若`concat`函数拼接的字符串长度超过65535或包含ASCII值0，自动将返回值改为BLOB类型，以避免输出到客户端时出现问题。(**1.30.2**)
* 时间序列聚合引擎的自定义函数指标支持多个返回值，同时也支持接受带有别名的指标，例如：avg(price) as price。(**1.30.2**)
* 调整了检查日志文件大小的频率，避免日志大小超过设定值。(**1.30.3**)
* 画图函数plot增加了可选参数stacking。线状图（line chart，柱状图（bar chart）和面积图（area chart）支持该参数。(**1.30.3**)
* 新增函数`getRequiredAPIVersion`，以配合API检查是否需要更新版本来兼容DolphinDB server。(**1.30.3**)
* 函数`subscribeTable`的可选参数offset取值为-2时，如果找不到持久化的offset，不再抛出异常，而是用-1取代。(**1.30.3**)
* windows版本的cpu绑定，从最多支持32核增加到64核。(**1.30.3**)
* 调用函数`addMetrics`为时间序列聚合引擎动态增加指标时，如果windowSize和原先的定义不同，系统报异常。(**1.30.3**)
* `subscribeTable`函数的filter参数，在值过滤的基础上增加了哈希和范围过滤。(**1.30.3**)
* 横截面引擎在支持聚合函数的基础上，增加对向量化函数的支持。(**1.30.3**)
* 时序聚合引擎允许在一个引擎中使用多个窗口。(**1.30.3**)
 
> Bug fixes:

* 修复无法序列化一个带有symbol类型字段的空表到python api的问题。(**1.30.1**)
* 处理流数据时，如果订阅端处理太慢，发布端在磁盘保留消息的时间又太短，需要发布的消息在磁盘和内存中都已经不存在了，会导致系统崩溃。(**1.30.1**)
* 修复redo log和cache engine在内存不足时导致系统死锁的问题。(**1.30.1**)
* Delta压缩算法连续两次增加的记录数小于3时，解压函数无法解压，报异常。(**1.30.2**)
* 个别函数最后一个参数的名称解析有误，导致使用键值参数时报找不到参数的异常。(**1.30.2**)
* 极端内存不足的情况下可能导致redo log写入失败。(**1.30.2**)
* 系统启动时删除不必要的异常警告 \<WARNING\> : failed to remove public key file。(**1.30.2**)
* 键值表和索引表在下面的情况下导致系统崩溃：包含多个键值列，查询时一个键值列是包含单个元素的向量，其他键值列的值是标量。(**1.30.3**)
* 内置的哈希表使用的内存超过2G时可能导致系统崩溃，影响的函数包括`isDuplicated`。(**1.30.3**)
* 函数`searchK`在应用到big array（非连续的数组）时可能出现结果不正确。(**1.30.3**)
* 订阅时启用filter，并且同一个流表被同一个节点的多个应用订阅时，只有按照订阅的顺序，依次反订阅（unsubcribeTable）才可以取消订阅。修复后的版本没有顺序要求。(**1.30.3**)
* mr函数和imr函数在下面的情况下导致系统崩溃：启用了`reduce`函数，但没有启用`final`函数，`map`函数没有返回值。(**1.30.3**)
* 事务管理器、任务调度器和缓存管理器在内存严重不足时出现内部状态不一致，死锁或者系统崩溃。(**1.30.3**)
* 当磁盘满时，redo log内部状态出现不一致，导致重启后数据库无法启动。(**1.30.3**)
* ewm系列函数包括`ewmMean`, `ewmVar`, `ewmStd`, `ewmCov`, `ewmCorr`没有注册成为顺序敏感（order sensitive）的函数，导致在sql语句中和context by子句配合使用时结果不正确。(**1.30.3**)
* sql中分组计算时，如果聚合函数sum，max，min，avg，count，std等的参数用到了顺序敏感的函数如next，prev等，系统错误的使用了哈希分组优化算法，导致结果不正确。(**1.30.3**)
* 使用顺序敏感的函数（如mstd，mavg）构造部分应用（partial application）时，没有正确设置顺序敏感标志，导致启用context by子句的sql语句应用此类函数的部分应用时，结果不正确。(**1.30.3**)

### DolphinDB 插件

* Python 插件

    * 支持在DolphinDB中直接调用python库。

### 客户端工具

* GUI
    * **注意**：1.30及以上版本的Server不兼容低于1.30.0版本的GUI，请从官网下载最新版本GUI客户端。

### API 

* Java API

    * 提供分布式库并行写入接口，数据自动按分区规划通过连接池并行入库。

* Python API

    * 优化数据传输性能




