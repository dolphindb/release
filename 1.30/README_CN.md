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

版本号： 1.30.4

发行日期： 2021-03-29

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.4.zip) 

版本号： 1.30.5

发行日期： 2021-03-30

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.5.zip) 

版本号： 1.30.6

发行日期： 2021-04-07

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.6.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.6_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.6_ABI.zip) 

版本号： 1.30.7

发行日期： 2021-04-21

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.7.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.7_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.7_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.7.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.7_JIT.zip)

版本号： 1.30.8

发行日期： 2021-04-28

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.8.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.8_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.8_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.8.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.8_JIT.zip)

版本号： 1.30.9

发行日期： 2021-05-17

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.9.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.9_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.9_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.9.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.9_JIT.zip)

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
* 修改upsert！函数，支持对DFS表（包括维度表和分区表）进行修改。(**1.30.6**)
* 支持使用SQL update和delete语句修改DFS表（包括维度表和分区表）。(**1.30.6**)
* 新增函数`sqlUpdate`和`sqlDelete`，动态创建SQL update和delete语句。(**1.30.6**)
* 新增函数`createSessionWindowEngine`用于创建流数据会话窗口引擎。(**1.30.6**)
* 支持客户端数据压缩上传到服务端，也支持数据压缩后输出到客户端。(**1.30.6**)
* 支持新数据类型DURATION， 表达时间范围更加简练。(**1.30.7**)
* 支持节点间通过压缩方式传输数据。(**1.30.7**)
* temporalAdd,dailyAlignedBar,bar,wj,pwj 函数支持DURATION类型参数。(**1.30.7**)
* keyedStreamTable支持多个key列。(**1.30.7**)
* SQL提供interval关键字支持插值查询。(**1.30.7**)
* `CrossSectionalEngine` 新增参数 lastBatchOnly。(**1.30.8**)
* `createReactiveStateEngine` 增加了可选参数 keepOrder。(**1.30.8**)
* 新增 `spearmanr`和`mutualInfo` 两个相关性的计算函数。	**(1.30.9)**
* 新增函数createDailyTimeSeriesEngine，用于创建支持会话的时间序列聚合引擎。每个会话的结束点和开始点可以做一些特殊处理。 **(1.30.9)**
* 增加函数getStreamTableFilterColumn用于取得流数据Filter列信息。**(1.30.9)**
* 新增函数`varp` 和 `stdp`。**(1.30.9)**

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
* 时序聚合引擎允许在一个引擎中使用多个不同长度窗口。(**1.30.3**)
* 改进了部分应用（partial application）的显示，除了显示函数名称，也会显示已经固定的参数。(**1.30.6**)
* 对时间类型的分区字段进行剪枝时，允许在分区字段上使用相应的时间函数（目前支持date, month和datahour函数），方便用户操作。例如，数据库在时间维度上按日期（DATE类型）进行分区，数据表的分区字段是TIMESTAMP类型，允许在时间列上先使用date函数再进行过滤， date(time) = 2021.03.02。(**1.30.6**)
* 数据表按照时间类型字段进行值分区或者范围分区时，通过对where子句中的过滤条件剪枝（如果所涉及分区的时间范围必然满足过滤条件，则可以在该分区的子查询上删除该过滤条件），改进查询性能。(**1.30.6**)
* 修改了cache engine的回收算法，提升了事务回收的效率，避免了不必要的OOM。(**1.30.6**)
* 流数据时间序列聚合引擎增加可选参数fill，可选的fill方法包括none，null和ffill。默认值是none，也即某一个key在某个时间窗口中没有数据时，不输出任何结果。(**1.30.6**)
* 函数`compress`和`decompress`支持table作为输入。(**1.30.6**)
* 单个事务涉及的元数据大小从最大16MB增加到128MB，避免出现一些大表不能删除的情况。(**1.30.6**)
* 异常检测引擎（函数createAnomalyDetectionEngine） 支持快照（snapshot）(**1.30.6**)
* 函数createCrossSectionalAggregator 改名为createCrossSectionalEngine，原名作为别名。(**1.30.6**)
* maxConnections默认值改成512。(**1.30.7**)
* createTimeSeriesAggregator 改名为createTimeSeriesEngine，原函数名作为alias。(**1.30.7**)
* 针对多列宽表优化sql性能。(**1.30.8**)
* Reactive state engine 支持指定多个keyColumn。(**1.30.8**)
* CrossSectionalEngine 支持聚合和非聚合混用。(**1.30.8**)
* `skew`和`kurtosis`分布式的聚合函数支持校正偏差。	**(1.30.9)**
* 检测同一个update语句对同一列重复更新，并给出异常提示。**(1.30.9)**
* createTimeSeriesEngine支持timeColumn指定2列，比如 date 和 time 列。**(1.30.9)**
* `sqlUpdate` 函数 where 条件中允许使用函数。**(1.30.9)**
* `firstNot`和`lastNot`分布式聚合时支持指定第2个参数。**(1.30.9)**
* `tableInsert`往分布式表写入数据时，返回值从写入记录数改为成功写入的记录数。	**(1.30.9)**
* 写入数据若在分区之外没有成功写入，会在日志中记录warning。**(1.30.9)**
* 高可用流表的引用变量被 undef后，仍然可以通过 `dropStreamTable` 删除该表。 **(1.30.9)**
> Bug fixes:

* 修复无法将一个带有SYMBOL类型字段的空表序列化到Python API的问题。(**1.30.1**)
* 处理流数据时，如果订阅端处理太慢，发布端在磁盘保留消息的时间又太短，需要发布的消息在磁盘和内存中都已经不存在了，会导致系统崩溃。(**1.30.1**)
* 修复redo log和cache engine在内存不足时导致系统死锁的问题。(**1.30.1**)
* Delta压缩算法连续两次增加的记录数小于3时，解压函数无法解压，报异常。(**1.30.2**)
* 个别函数最后一个参数的名称解析有误，导致使用键值参数时报找不到参数的异常。(**1.30.2**)
* 极端内存不足的情况下可能导致redo log写入失败。(**1.30.2**)
* 系统启动时删除不必要的异常警告 \<WARNING\> : failed to remove public key file。(**1.30.2**)
* 键值表和索引表在以下场景导致系统崩溃：包含多个键值列，查询时一个键值列是包含单个元素的向量，其他键值列的值是标量。(**1.30.3**)
* 内置的哈希表使用的内存超过2G时可能导致系统崩溃，影响的函数包括`isDuplicated`。(**1.30.3**)
* 函数`searchK`在应用到big array（非连续的数组）时可能出现结果不正确。(**1.30.3**)
* 订阅时启用filter，并且同一个流表被同一个节点的多个应用订阅时，只有按照订阅的顺序，依次反订阅（unsubcribeTable）才可以取消订阅。修复后的版本没有顺序要求。(**1.30.3**)
* `mr`函数和`imr`函数在以下场景导致系统崩溃：启用了`reduce`函数，但没有启用`final`函数，`map`函数没有返回值。(**1.30.3**)
* 事务管理器、任务调度器和缓存管理器在内存严重不足时出现内部状态不一致，导致死锁或者系统崩溃。(**1.30.3**)
* 当磁盘被占满后，redo log内部状态出现不一致，导致重启后数据库无法启动。(**1.30.3**)
* ewm系列函数包括`ewmMean`, `ewmVar`, `ewmStd`, `ewmCov`, `ewmCorr`没有注册成为顺序敏感（order sensitive）的函数，导致在sql语句中和context by子句配合使用时结果不正确。(**1.30.3**)
* sql中分组计算时，如果聚合函数sum，max，min，avg，count，std等的参数用到了顺序敏感的函数如next，prev等，系统错误的使用了哈希分组优化算法，导致结果不正确。(**1.30.3**)
* 使用顺序敏感的函数（如mstd，mavg）构造部分应用（partial application）时，没有正确设置顺序敏感标志，导致启用context by子句的sql语句应用此类函数的部分应用时，结果不正确。(**1.30.3**)
* 当输入的数据包含多个key，每个key的数据按时间升序排列，但是全部数据并非按时间顺序排列时，时间序列聚合引擎输出的结果缺失部分数据。(**1.30.4**)
* 同一客户端对同一流表有多个订阅且流数据的队列满时，可能出现订阅不能删除的情况。(**1.30.4**)
* 当输入的数据小于一个窗口，指定的指标包含聚合和非聚合两种，异常检测引擎会崩溃。(**1.30.4**)
* 修复创建数据库和表时潜在的丢失元数据的风险。(**1.30.5**)
* 数据表按照日期（DATE）进行分区，分区字段ts的数据类型是TIMESTAMP，过滤条件 ts > 2021.03.02没有包含（应该包含）2021.03.02这个分区。(**1.30.6**)
* 一个数据库被删除后，如果在被回收之前，系统重启了，查询时该数据库又会展现给用户。(**1.30.6**)
* 自定义函数用于pcross，ploop和peach等并行计算的高阶函数时，可能出现自定义函数返回值为空的情况。(**1.30.6**)
* rank函数指定tiesMethod为max时，可能导致系统崩溃。(**1.30.6**)
* 当输入为单个元素的tuple时，flatten函数的结果不正确，直接返回了tuple，而不是tuple中的元素。(**1.30.6**)
* 客户端为python时，month/datetime/date/minute/time/second等时间类型数据在高压力情况下可能出现输出结果不正确。(**1.30.6**)
* 时间序列聚合引擎的一个批次的输入数据包含多个时间窗口时，输出的结果没有按时间排序。(**1.30.6**)
* 横截面引擎一个批次的输入数据包含多个时间点，且均满足keyCount的触发条件，则输出结果有重复。(**1.30.6**)
* 系统若开启了cache engine，短时间内反复多次删除和创建同一个数据库表，可能导致旧表的数据写入到新创建的同名表中。(**1.30.6**)
* replay无法指定select中定义的列名作为dateColumn和timeColumn。(**1.30.6**)
* 修复异常检查引擎全局不按时间排序时，输出表缺少第一组和最后一组时间数据。(**1.30.7**)
* 修复并发调用`dropTable`，`getTables`会导致crash的问题。(**1.30.7**)
* 修复当发布节点host定义为localhost时，远程订阅无法取消问题。(**1.30.7**)
* 修复使用`nunique`查询时报错：Immutable sub vector doesn't support method getDataSegment。(**1.30.7**)
* 修复节点掉线后执行dropTable失败导致节点恢复后该表也无法被删除。(**1.30.8**)
* cutPoints 在sql语句中使用结果有误。(**1.30.8**)
* 修复当写入keyed table的tuple中包含subarray时，返回的表结果不正确。(**1.30.8**)
* 修复多层循环时，在内层循环使用break，会退出最外层循环, 此问题是由于1.30.6 版本引入。(**1.30.8**)
* update分布式表失败时有几率导致在append数据时候server报告异常"appendCommittedVersion",此问题由1.30.6的分布式表支持update功能引入。(**1.30.8**)
* createTimeSeriesEngine启用fill选项，当实时数据存在多个连续的空窗口时，计算结果有误。**(1.30.9)**
* 设置系统定期回收策略的数据库，被删除后未及时清理回收策略。**(1.30.9)**
* 一库多表，并发写入和删除不同分区，重启后查询报错symbol base is corrupted	**(1.30.9)**
* 持续的重复下列操作：删除一个分布式表的分区，写入数据到这个分区，重启数据库进程，有几率出现元数据和数据不一致的情况。**(1.30.9)**
* 多线程并发执行share语句共享一个表和查询一个共享表两个操作时，有几率导致系统奔溃。**(1.30.9)**
* mcorr计算相关性时，如果某一列的数完全相同，应该返回空值。但由于判断浮点数是否为0的阈值设置不合理，导致结果变成0或非常接近于0的数。**(1.30.9)**
* 在启用dataSync的情况下，使用loadTextEx导入大文件后，会导致redolog不释放。**(1.30.9)**
* 异常检测引擎在指定多个keyColumn，计算复合表达式指标时，计算结果有误。**(1.30.9)**
* 执行continue之后无法进入下一次循环。此问题从1.30.6版本引入。	**(1.30.9)**
* 流数据高可用切换leader后在某些场景下订阅客户端接受不到数据。 **(1.30.9)**
* 高可用流表不指定keyColumn会crash。	**(1.30.9)**
* 矩阵按布尔条件取列数据时结果不符合预期。**(1.30.9)**
* dictUpdate函数针对值为任意类型（ANY）的字典，如果initFunc抛出异常，继续操作字典会导致crash。**(1.30.9)**
* 键值表（keyedTable）更新已有的数据行时，如果输入数据是长度为1的字符串（STRING）列或符号（SYMBOL）列，系统报错incompatible between index and value。 **(1.30.9)**

### DolphinDB 插件

* Python 插件

    * 支持在DolphinDB中直接调用Python库。

### 客户端工具

* GUI
    * **注意**：1.30及以上版本的Server不兼容低于1.30.0版本的GUI，请从官网下载最新版本GUI客户端。
    * 1.30.7 及以上版本的Server, 需要配合GUI1.30.7版本使用DURATION类型。
    * 增加下载查询结果到GUI本地csv功能。

### API 

* Java API

    * 提供分布式库并行写入接口，数据自动按分区规划通过连接池并行入库。

* Python API

    * 优化数据传输性能, 最新Server版本请升级Python API到1.30.0.5
    ```
    pip3 install dolphindb==1.30.0.5
    ```
    * 提供partitionTableAppender支持向分布式表并发写入数据 (**1.30.0.6**)
    * run函数提供fetchSize参数，支持每次读取fetchSize行记录 (**1.30.0.6**)
    * 流数据订阅时支持批量处理 (**1.30.0.6**)
    * run执行完毕后自动清除本会话内生成的变量 (**1.30.0.6**)
    * 连接时进行Server版本的兼容性检查(**1.30.0.6**)
    * `tableAppender`函数提供写入数据时自动转换时间类型功能(**1.30.0.6**)
