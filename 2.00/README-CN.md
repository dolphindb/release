# DolphinDB发行说明

- [DolphinDB发行说明](#dolphindb发行说明)
  - [DolphinDB服务器](#dolphindb服务器)
  - [GUI](#gui)

## DolphinDB服务器

版本号： 2.00.0

发行日期： 2021-07-31

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.0.0.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.0.0_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.0.0_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.0.0.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.0.0_JIT.zip)

版本号： 2.00.1

发行日期： 2021-08-25

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.1.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.1_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.1_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.00.1.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.00.1_JIT.zip)

版本号： 2.00.2

发行日期： 2021-11-05

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.2.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.2_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.2_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.00.2.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.00.2_JIT.zip)

版本号： 2.00.3

发行日期： 2021-11-22

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.3.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.3_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.3_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.00.3.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.00.3_JIT.zip)

版本号： 2.00.4

发行日期： 2022-01-10

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.4.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.4_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.4_ABI.zip) | 

版本号： 2.00.5 &nbsp;&nbsp;&nbsp; [二级兼容](./../DolphinDB_compatibility_levels.md/#32-二级兼容性标准) 2.00.4, 1.30.16 和 1.30.17

发行日期： 2022-03-29

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.5.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.5_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.5_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.00.5.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.00.5_JIT.zip)

版本号： 2.00.6 &nbsp;&nbsp;&nbsp; [二级兼容](./../DolphinDB_compatibility_levels.md/#32-二级兼容性标准) 2.00.5

发行日期： 2022-05-09

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.6.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.6_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.6_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.00.6.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.00.6_JIT.zip)

> 新功能

* 发布TSDB存储引擎。`database` 函数提供了一个可选参数 engine，默认值为 `OLAP`，即旧的存储引擎。如果创建基于 TSDB 存储引擎的数据库，engine 设置为 `TSDB` 即可。(**2.00.0**)

* 基于 TSDB 存储引擎的数据支持新的数据类型 BLOB。(**2.00.0**)

* 新增 `percentileRank` 函数，计算一个值在一个向量中的百分位。(**2.00.1**)

* 新增 `zigzag` 函数，计算数据中的极值点。(**2.00.1**)

* 新增 `lowDouble` 和 `highDouble` 函数，用于将 POINT 和 COMPLEX 等16字节的数据类型分解成高位8字节的 DOUBLE 类型和低位8字节的 DOUBLE 类型。(**2.00.1**)

* 新增 `rdp` 压缩算法函数。(**2.00.1**)

* 新增计算加权最小二乘回归函数 `wls`。(**2.00.1**)

* 流数据引擎支持 equal join。(**2.00.1**)

* 新增 `ifNull` 和 `ifValid` 函数。(**2.00.1**)

* DolphinDB 集群支持新的节点类型：计算节点 (computing node)。与数据节点可同时用于计算引擎和存储引擎不同，计算节点只能用于计算引擎。(**2.00.1**)

* 流计算引擎 reateReactiveStateEngine, AnomalyDetectionEngine, SessionWindowEngine, DailyTimeSeriesEngine 和 TimeSeriesEngine 支持高可用。(**2.00.2**)

* 新增功能，跨集群数据异步复制。(**2.00.2**)

* 新增函数 `covarMatrix` 和 `corrMatrix`，来计算 pairwise covariance 和 correlation，性能比直接使用高阶函数 `cross` 和 `covar/corr` 的组合快1~2个数量级。(**2.00.2**)

* 新增配置项 stdoutLog，当取值为 true 或 1 时，不再输出系统的日志到文件，而是输出到 stdout。(**2.00.2**)

* 新增高阶函数 `tmoving`，可以实现时间窗口的滑动。同时响应式状态引擎中实现高阶函数 `moving` 和 `tmoving` 对应的状态函数(state function)。(**2.00.2**)

* 新增函数 `runScript`，用于执行一段脚本。(**2.00.2**)

* 新增函数 `makeUnifiedCall`, `binaryExpr` 和 `unifiedExpr` 用于元编程。(**2.00.2**)

* 新增23个按时间滑动的窗口系列函数，包括 `tmove`, `tmfirst`, `tmlast`, `tmsum`, `tmavg`, `tmcount`, `tmvar`, `tmvarp`, `tmstd`, `tmstdp`, `tmprod`, `tmskew`, `tmkurtosis`, `tmmin`, `tmmax`, `tmmed`, `tmpercentile`, `tmrank`, `tmcovar`, `tmbeta`, `tmcorr`, `tmwavg`, `tmwsum`。并在响应式状态引擎中实现对应的状态函数。(**2.00.2**)

* 新增函数 `sma`, `wma`, `dema`, `tema`, `trima`, `talib`, `talibNull` 和 `linearTimeTrend`。(**2.00.2**)

* 新增函数 `countNanInf` 和 `isNanInf`，统计 scalar, vector 或 matrix 中包含多少个 NaN 和 Inf 值。(**2.00.2**)

* 增加流数据 window join 引擎。(**2.00.2**)

* 时间序列聚合引擎新增函数实现：`count`, `firstNot`, `ifirstNot`, `ilastNot`, `imax`, `imin`, `lastNot`, `nunique`, `prod`, `quantile`, `sem`, `sum3`, `sum4`, `mode` 和 `searchK`。(**2.00.2**)

* 增加函数 `getConfigure`，传入一个 key，返回该配置项信息。如果参数为0，返回所有配置项目信息。(**2.00.2**)

* 新增命令 `clearCachedModules`，可以强制清除缓存的 module。当缓存清除后，执行 use 语句时，会重新从文件加载 module。这个方法可以在不重启节点的情况下，重新加载已经更新的 module。只有 admin 才有权限执行这个命令。(**2.00.2**)

* 支持新的数据类型 array vector，array vector 的每一行是具有相同数据类型的不定长的数组。目前分布式表中仅 TSDB 引擎支持。(**2.00.2**)

* 新增按行聚合函数 `rowSize`, `rowStdp`, `rowVarp`, `rowSkew` 和 `rowKurtosis`。(**2.00.2**)

* 支持匿名的聚合函数定义。(**2.00.3**)

* 支持 postStart.dos 文件，可用于启动 DolphinDB 时挂载定时任务。(**2.00.3**)

* 新增 tcmalloc 控制预留内存配置选项，当内存占用接近 `maxMemSize` 的时候，控制能够分配的内存块的最大尺寸，避免因 OOM 导致 crash。(**2.00.3**)

* 增加 `cumfirstNot`,`cumlastNot`, `mfirst`, `mlast`等函数，以及在响应式引擎中实现它们的状态函数。(**2.00.3**)

* 新增函数 `oneHot`，用于做 one hot（独热）编码。(**2.00.3**)

* 新增 `setAtomicLevel` 函数，用于修改历史数据库的配置以支持并发写入。(**2.00.3**)

* 支持表级别分区粒度，支持同一库中不同的表并发进行增删改操作。（**2.00.4**）

* 往内存表的时间列写入数据时，自动进行时间类型转换。（**2.00.4**）

* 支持在线增量恢复，可以异步地进行节点数据恢复。 （**2.00.4**）

* 支持管理和查询集群中的所有计算任务。（**2.00.4**）

* 内存表和流数据表支持 BLOB 类型。（**2.00.4**）

* SQL 语句增加标识 [HINT_EXPLAIN]，可以显示 SQL 的执行过程。（**2.00.4**）

* 新增函数 `streamEngineParser`，支持自动分解截面因子成多个内置流计算引擎的流水线。（**2.00.4**）

* 新增函数 `existSubscriptionTopic`，用于判断某一个订阅是否已经创建。（**2.00.4**）

* 新增函数 `createLookupJoinEngine`，支持将流数据表和流数据表、内存表或者分布式表（目前只支持维度表）做左连接。（**2.00.4**）

* 新增函数 `moveChunksAcrossVolume`，在增加新的 volume 后，用于转移旧 volume 的部分 chunk 到新 volume。（**2.00.4**）

* 增加新的 volume 后，可以使用 `resetDBDirMeta` 函数转移老的 volume 上的 meta log 目录到新的 volume。（**2.00.4**）

* 新增 10 个 TopN 函数 `msumTopN`, `mavgTopN`, `mstdpTopN`, `mstdTopN`, `mvarTopN`, `mvarpTopN`, `mcorrTopN`, `mbetaTopN`, `mcovarTopN`, `mwsumTopN`，且 `createReactiveStateEngine` 引擎支持它们相应的状态函数。（**2.00.4**）

* 新增函数 `makeKey` 和 `makeOrderedKey`，可以将多个列合并成一个 BLOB 列，用作字典或集合的键值，其中 `makeOrderedKey` 的结果保留了多个字段的排序顺序。（**2.00.4**）

* 新增高阶函数 `aggrTopN`，用以计算根据排序列获取的前N行数据的聚合结果。（**2.00.4**）

* 新增高阶函数 `window` 和 `twindow`。与 `move` 与 `tmove` 类似，但适用于更通用的场景，对于窗口边界的处理稍有不同。（**2.00.4**）

* 新增配置项 raftElectionTick，用以配置 raft 切换 leader 的心跳时间。同时新增函数 `setCacheEngineMemSize`, `setTimeoutTick`, `setTSDBCacheEngineSize`, `setMaxMemSize`, `setReservedMemSize` 和 `setMaxBlockSizeForReservedMemory` 支持在线修改对应的配置项。（**2.00.4**）

* 新增函数 `fixedLengthArrayVector`，支持将多个向量合成一个 array vector。（**2.00.4**）

* 新增函数 `loadNpz` 支持导入 numpy 的 npz 文件。（**2.00.4**）

* 新增函数 `suspendRecovery` 用于暂停 recovery 任务。新增函数 `resumeRecovery` 用于重启 recovery 任务。（**2.00.4**）

* 新增函数 `rowCorr`, `rowCovar`, `rowBeta`, `rowWsum`, `rowWavg`，可以对每行数据进行计算。（**2.00.4**）

* 新增函数 `movingWindowIndex` 和 `movingTopNIndex`，用于获取每一个滑动窗口的元素下标，返回一个 INDEX[] 类型的 array vector。（**2.00.4**）

* 新增 `fflush` 函数，帮助将缓存中的数据写入文件系统。（**2.00.4**）

* 新增命令 `enableTSDBAsyncSorting` 和 `disableTSDBAsyncSorting` 用于开启和关闭 TSDB 引擎 cache engine 的异步数据排序功能。（**2.00.5**）

* 新增函数 `getRecoveryWorkerNum` 获取当前用于 chunk 恢复的工作线程数。（**2.00.5**）

* 新增命令 `resetRecoveryWorkerNum` 动态修改用于 chunk 恢复的工作线程数。（**2.00.5**）

* TSDB 引擎支持在线增量恢复。（**2.00.5**）

* 新增运维函数 `getLevelFileIndexCacheStatus` 查询当前 TSDB 引擎索引内存占用情况。（**2.00.5**）

* 支持使用命令 `kill -15 $PID` 或集群 web 管理界面安全关机。（**2.00.5**）

* 新增函数 `rebalanceChunksAmongDataNodes`，用于新增数据节点后平衡数据节点间的数据量。（**2.00.5**）

* 新增函数 `rebalanceChunksWithinDataNode`，用于数据节点上新增磁盘卷后平衡磁盘卷之间的数据量。（**2.00.5**）

* 新增运维函数 `imtUpdateChunkVersionOnDataNode`，修改数据节点上对应 chunkId 的版本号。维护集群中多副本数据之间，或数据节点与控制节点之间的版本一致性。（**2.00.5**）

* 函数 `replay` 支持多表回放到异构流数据表，并按照时间顺序输出。（**2.00.5**）

* 新增函数 `concatMatrix`，支持水平或垂直拼接多个矩阵。（**2.00.5**）

* 新增距离计算函数欧氏距离 `euclidean` 、谷本距离 `tanimoto` 以及按行计算的欧式距离 `rowEuclidean` 和谷本距离 `rowTanimoto`。（**2.00.5**）

* 新增按行计算内积的函数 `rowDot`。（**2.00.5**）

* 新增高阶函数 `firstHit` 和 `ifirstHit`，用于返回 X 中第一个满足条件的元素。（**2.00.5**）

* 新增函数 `getCurrentSessionAndUser`，获取当前 session 对应的 sessionID 和 userID。（**2.00.5**）

* 支持 SQL Join 的标准写法。（**2.00.5**）

* 新增 SQL 语句 `alter`，用于在已有的表中添加列。（**2.00.5**）

* 新增 SQL 语句 `create`，用于创建数据库或表。（**2.00.5**）

* 新增函数 `cells`，使矩阵输出由参数 row 和 col 指定位置的元素值。（**2.00.6**）

* 新增函数 `randDiscrete`，支持按指定概率分布离散抽样。（**2.00.6**）

* 新增计算函数 `dynamicGroupCumsum` 和 `dynamicGroupCumcount`，并在响应式状态引擎中增加了对应的状态函数。（**2.00.6**）

* 新增函数 `createDistributedInMemoryTable` 支持创建分布式共享内存表。（**2.00.6**）

* 新增分级存储功能，可以将冷数据存储到低速硬盘或者对象存储（比如 Amazon S3）上，且这些冷数据只读不可写。（**2.00.6**）

* 新增 `transaction` 语句，将对单个内存表（或共享内存表）操作的多个 SQL 语句封装为一个事务 （**2.00.6**）


改进

* `createTimeSeriesEngine` 和 `createDailyTimeSeriesEngine` 函数新增参数 forceTriggerTime。(**2.00.1**)

* 缩短了 `scheduleJob` 的间隔时间到5分钟。(**2.00.1**)

* timeSeriesEngine 和 DailyTimeSeriesEngine 支持多个 keyColumn。(**2.00.1**)

* `upsert!` 函数 `ignoreNull`字段支持 DFS 表。(**2.00.1**)

* `parseExpr` 新增可选参数 modules 和 overloadedOperators，可加载模块，重载运算符，且支持使用字典来给表达式中的变量赋值。(**2.00.1**)

* `sql` 函数新增可选参数 exec，支持生成 exec 语句。(**2.00.1**)

* TSDB 引擎去重策略支持 KEEP_FIRST，重复数据仅保留第一条数据。(**2.00.1**)

* `temporalAdd` 支持增加与减去工作日（BusinessDay），支持时间类型 DATEHOUR。(**2.00.1**)

* 控制节点的元数据信息新增修改时间戳。(**2.00.1**)

* SQL GROUPBY 子句中的 `interval` 函数支持 step 参数，以滑动窗口的方式计算聚合结果。(**2.00.1**)

* `sql` 函数中当参数 groupFlag 为 PIVOTBY 时，参数 groupBy 支持选择多列。(**2.00.1**)

* `createReactiveStateEngine` 新增字段 keyPurgeFilter 和 keyPurgeFreqInSecond，以支持响应式状态引擎（reactive state engine）自动清理 key。(**2.00.1**)

* 响应式状态引擎（reactive state engine）支持输出结果到分布式表和流数据表，支持接受来自 `replay` 的输入。(**2.00.1**)

* `delete` 语句支持 `map` 子句，将 `delete` 语句下沉到各分区执行。(**2.00.1**)

* 用户自定义函数的输入参数支持默认值。(**2.00.1**)

* Windows 安装包的 dolphindb.cfg, controller.cfg, cluster.cfg 默认配置项中移除 redolog 配置参数。(**2.00.1**)

* 改进 redo log 的回放性能。在有大量小事务的情况下，性能有10倍以上的提升。(**2.00.1**)

* 修改 `iif` 函数在 condition 包含空值时的行为。旧版本中 condition 的元素包含空值被当作 false 处理。新版本中如果为空值，对应的结果也为空值。(**2.00.2**)

* 矩阵进行 `accumulate` 等计算时放开8192行的限制。(**2.00.2**)

* 对维度表的并发执行写入、更新等操作时，不再抛出事务冲突异常。(**2.00.2**)

* 数据节点重启时，redolog 的回放会在日志中输出详细的进度。(**2.00.2**)

* SQL 语句中的 `interval` 功能（按时间聚合）移除 range 参数，同时增加可选参数 explicitOffset，默认值为 false。当该参数为 true 时，可以将第一个窗口的起始位置指定为 where 指定的窗口的起始位置。(**2.00.2**)

* `ols` 和 `wls` 在 mode 为2的时候，新增一个输出 Residual。同时新增一个函数 `residual` 用于计算回归的残差。(**2.00.2**)

* in(X, Y) 函数的参数 Y 支持为 NULL，当 Y 为无类型的 NULL 时，函数的返回值为 false 或每一个值为 false 的 vector。(**2.00.2**)

* 计算节点(computing node)支持客户端的所有操作。(**2.00.2**)

* SQL pivot 产生的表列名不再特殊处理，即直接使用 pivot 的值作为列名。(**2.00.2**)

* 函数 `rank`, `denseRank`, `cumrank`, `rowRank` 和 `rowDenseRank` 支持 percent 形式。(**2.00.2**)

* `kmeans` 支持自定义质心。(**2.00.2**)

* window join 增加对 `varp`, `stdp`, `prod`, `skew` 和 `kurtosis` 5个聚合函数的优化。(**2.00.2**)

* 支持对非数值类型进行 `unpivot`。(**2.00.2**)

* 滑动窗口函数系列如 `msum`，当输入数据为 indexed matrix 或 indexed series 时，窗口支持时间偏移窗口类型。(**2.00.2**)

* 优化了 TSDB 引擎中 `dropPartition` 的性能。(**2.00.2**)

* TSDB 新增配置选项 TSDBBlockSize，可以指定 TSDB 存储时一个 block 的大小。(**2.00.2**)

* `database` 函数新增可选参数 atomic。当 atomic 取值为 'CHUNK' 时，写入操作只保证分区的原子性，此时也允许多个并发线程同时写入该数据库的同一个分区。(**2.00.2**)

* 时序聚合引擎的 forceTriggerTime参 数计算规则修改，设置 updateTime 时，不再限制输出表为 keyedTable。(**2.00.3**)

* 横截面引擎添加是否触发有效计算的开关。(**2.00.3**)

* 响应式引擎中增加支持 `mmad` 状态函数。(**2.00.3**)

* 时序聚合引擎新增对 nanotimestamp 的规整。(**2.00.3**)

* 共享流表新增权限控制。(**2.00.3**)

* getStreamingStat().subWorkers 的结果表中增加以下参数：msgAsTable, batchSize, throttle, hash, filter, persistOffset, timeTrigger, handlerNeedMsgId, raftGroup, 用于对流数据的监控。(**2.00.3**)

* `sma`, `wma`, `dema`, `tema`, `trima`, `t3`, `ma`, `talib`, `talibNull`, `linearTimeTrend state function。(**2.00.3**)

* 分布式 join 改进，支持更多的场景，支持的函数包括 `lj`, `lsj`, `ej`, `aj` 和 `wj`，可以对不同分区方案的表，分区列不是连接列的表，或者不在同一库中的分布式表做 join。(**2.00.3**)

* 维度表的 `delete` 支持并发操作。(**2.00.3**)

* array vector 的 index 支持 slice。(**2.00.3**)

* STRING 类型支持直接与 NULL 进行比较。(**2.00.3**)

* 提升 `stdp`, `std`, `varp`, `var`, `skew`, `kurtosis`, `mskew`, `mkurtosis`, `tmskew`, `tmkurtosis`，以及 window join 中 `skew` 和 `kurtosis` 等函数的精度。(**2.00.3**)

* 支持更多与 array vector 相关计算，包括 `groups`, `distinct`, `nunique` 和 `at`。(**2.00.3**)

* 高阶函数的第一个参数会被强制解析成函数。(**2.00.3**)

* `distinct` 函数可与 group by 配合使用，其结果为一个 array vector。(**2.00.3**)

* `nunique` 函数支持分布式计算。(**2.00.3**)

* UDF 函数支持 keyword arguments。(**2.00.3**)

* 新增对 `qr`, `ols`, `dot` 函数输入的校验，不允许行数或列数为0的矩阵作为输入。(**2.00.3**)

* TSDB 引擎优化查询某个字段对应的最新数条记录的性能，性能提升数倍至数百倍。（**2.00.4**）

* 优化 TSDB 在调用 `top` 子句查询数据时的性能。（**2.00.4**）

* 提升 TSDB 存储引擎中查询预计算数据的速度。（**2.00.4**）

* 使用赋值语句对内存表进行更新时，支持在行过滤条件中输入 BOOL 类型数组，形如：t[`y, t[`y]>0] = 0，其中 t 是表变量，y 是 t 的列名。（**2.00.4**）

* `upsert!` 函数新增可选参数 sortColumns，更新后的表可根据该指定列进行排序。（**2.00.4**）

* `cancelJob`, `cancelConsoleJob` 支持同时取消多个任务，且优化了集群阻塞时取消任务的性能。（**2.00.4**）

* `loadText` 支持 schema 中指定数据类型为 array vector。（**2.00.4**）

* `set` 支持 BLOB 类型的值。（**2.00.4**）

* `keyedStreamTable` 一次性批量插入多条键值相同的新记录，出现插入会失败。（**2.00.4**）

* 优化了 `atImin` 和 `atImax` 在 window join 中的使用性能。（**2.00.4**）

* `run` 命令新增可选参数 clean，控制是否清理当前 session 中的变量。（**2.00.4**）

* `wj` 函数，duration 支持设置为 y（年），M（月），B（工作日）。（**2.00.4**）

* `loadText` 支持字符串包含 ASCII 码为 0 的字符。（**2.00.4**）

* 支持对矩阵的条件赋值。（**2.00.4**）

* `loadTextEx` 新增可选参数 atomic，默认值是 false。加载大文件的情景下，设置该参数为 false，将文件加载事务拆分为多个事务。（**2.00.4**）

* `getCompletedQueries` 函数和 `getRunningQueries` 函数返回值中添加 remoteIP 字段。（**2.00.4**）

* 配置项参数 *tdoutLog*支持设置为 2，表示同时打印日志到标准输出和日志文件。（**2.00.4**）

* 异常检测引擎（anomaly detection engine）metrics 参数支持序列相关函数。（**2.00.4**）

* 时序引擎（time-series engine）windowSize 为向量时，各元素取值可相同。（**2.00.4**）

* 横截面引擎（ cross-sectional engine）支持 keyColumn 输入一个向量。（**2.00.4**）

* 支持向流数据引擎插入 tuple 类型的记录。（**2.00.4**）

* 函数 `getStreamEngineStat` 返回的横截面引擎的统计信息添加了 memoryUsed 字段，可以查看横截面引擎所占内存。（**2.00.4**）

* `createAsofJoinEngine` 在 metrics 中支持输出右表的时间列。（**2.00.4**）

* 共享内存表（共享流表）新增可读不可写的权限管理。（**2.00.4**）

* 提升了控制节点高可用的稳定性。（**2.00.4**）

* 日志中新增打印 delete 和 update 操作信息。（**2.00.4**）

* 输出日志中流订阅任务的报错信息增加订阅主题。（**2.00.4**）

* Web 任务管理界面优化。重新设计、整合了 Web 管理界面，增加了作业管理功能，支持查看、停止、取消 DolphinDB 运行中、已提交和定时触发的作业。升级 server 版本后，需要同步更新 web 文件夹。

  新版本使用了 WebSocket 协议，增加了对 DolphinDB 二进制协议的支持，对浏览器的要求也随之提高，可能需要用户更新浏览器到最新的版本，推荐使用 Chrome 最新版或 Edge 最新版。（**2.00.4**）


* TSDB 引擎支持 cache engine 的异步数据排序功能，可使用配置项 TSDBAsyncSortingWorkerNum 指定异步排序的线程数，默认值为1。（**2.00.5**）

* TSDB 引擎支持快照隔离。（**2.00.5**）

* TSDB 引擎支持 Windows 系统。（**2.00.5**）

* OLAP 引擎支持在 Windows 环境中开启 dataSync（即设置配置项 dataSync = 1）。（**2.00.5**）

* 函数 `subscribeTable` 新增可选参数 userId 和 password，系统在用户退出后自动尝试重新登录，保证订阅数据成功写入分布式表。（**2.00.5**）

* 响应式状态引擎（reactive state streaming engine）支持参数 metrics 指定函数的返回值为 array vector。（**2.00.5**）

* `getStreamingStat().subWorkers` 函数返回结果 throttle 统一为以毫秒为单位。（**2.00.5**）
  
* asof join 引擎支持指定多个连接列。（**2.00.5**）

* 横截面引擎（cross-sectional engine）新增参数 snapshotDir 和 snapshotIntervalInMsgCount 支持快照机制，新增参数 raftGroup 支持计算引擎高可用。（**2.00.5**）

* 新增函数 `getLeftStream` 和 `getRightStream` 支持 join 引擎的级联。（**2.00.5**）

* 若横截面引擎（cross-sectional streaming engine）和时间序列引擎（time-series streaming engine）参数 metrics 指定的函数有多个返回值，创建引擎时无需指定列名。（**2.00.5**）

* 新增命令 `addAccessControl` 对共享内存表（包括共享流表）或流数据引擎对象增加权限控制。（**2.00.5**）

* 对表应用 `quantile` 等聚合函数时，不符合条件的列在输出结果中保持不变。（**2.00.5**）

* SQL `pivot by` 语句支持转换 UUID 类型的列。（**2.00.5**）

* array vector 支持更多的切片写法。（**2.00.5**）

* 函数 `ceil` 和 `floor` 结果的范围上限提升为2^53。（**2.00.5**）

* 若 SQL `pivot by` 语句最后一列为分区列，且 `select` 字段不包含聚合函数或序列函数，`pivot by` 语句性能提升近五倍。（**2.00.5**）

* 函数 `med` 参数支持 BOOL 类型。（**2.00.5**）

* 函数 `ema`、`kama` 和 `wma` 支持计算 BOOL 类型向量。（**2.00.5**）

* 命令 `addColumn` 新增列名支持以数字开头。（**2.00.5**）

* 函数 `loadText` 和 `loadTextEx` 导入 csv 文件时，第一行数据的读取上限为 256 KB。（**2.00.5**）

* 聚合函数、窗口函数和向量函数支持表作为输入参数。（**2.00.5**）

* 函数 `rand` 和 `normal` 的参数 count 支持输入数据对，用于指定生成矩阵的维度。（**2.00.5**）

* 函数 `loadText` 和 `loadTextEx` 新增参数 arrayDelimiter，支持导入包含 array vector 的 csv 文件。（**2.00.5**）

* row 系列逻辑函数（`rowAnd`, `rowOr`, `rowXor`）支持输入整数。（**2.00.5**）

* `bar` 函数新增参数 closed，用于指定分组包含左边界或右边界。（**2.00.5**）

* 滑动窗口函数的参数 X 是索引序列或索引矩阵，且 window 是正整数时，窗口按照索引滑动。（**2.00.5**）

* 自定义函数的参数可以分行书写，每行以逗号结束。（**2.00.5**）

* SQL `order by` 语句支持使用 as 改名前和改名后的字段。（**2.00.5**）

* 函数 `dailyAlignedBar` 参数 X 新增支持 SECOND，TIME，NANOTIME 类型向量。（**2.00.5**）

* 服务端支持以 pickle 格式传输包含 array vector 的表到 Python API。（**2.00.5**）

* 日级时间序列聚合引擎（daily time-series streaming engine）新增参数 forceTriggerSessionEndTime，用于指定强制触发 sessionEnd 的窗口。（**2.00.5**）

* 日级时间序列聚合引擎（daily time-series streaming engine）和时间序列聚合引擎（time-series streaming engine）修改参数 forceTriggerTime，未计算的窗口由计算结束后的最新数据触发。若设置了参数 fill，则同时填充无数据的窗口。（**2.00.5**）

* 提升了 SYMBOL 数据类型的读写性能。（**2.00.6**）

* 响应式状态引擎支持 `cummed` 和 `cumpercentile` 两个窗口函数。（**2.00.6**）

* 时序引擎（`createTimeSeriesEngine` 和 `createDailyTimeSeriesEngine`）新增参数 closed 来控制计算窗口的闭合边界。（**2.00.6**）

* `streamEngineParser` 的 keyColumn 参数取消对传入列名的大小写判断。（**2.00.6**）

* `createTimeSeriesEngine` 和 `createDailyTimeSeriesEngine` 新增参数 keyPurgeFreqInSec, 用于清理长时间无数据的分组。（**2.00.6**）

* 优化时序聚合引擎自定义函数性能。（**2.00.6**）

* `streamFilter` 支持对普通流表的列数据进行过滤、分发。（**2.00.6**）

* `createTimeSeriesEngine` 和 `createDailyTimeSeriesEngine` 的 metrics 支持对矩阵进行运算。（**2.00.6**）

* `resample` 函数的 rule 参数支持 "H", "L", "U", "min", "N" 以及 "S"，且新增了参数 closed，label 和 origin，可以对分组区间进行设置。（**2.00.6**）

* 优化了生成随机整数的性能。（**2.00.6**）

Bug fixes:

* 删除分布式表（使用 `dropTable` 或 `dropPartition`）在提交时失败，导致事务回滚后，再次查询该表时结果不符合预期。删除该表缓存后，查询恢复正常。(**2.00.1**)

* TSDB Engine 的 TSDBRedoLogDir 配置不生效。(**2.00.1**)

* 配置参数 datanodeRestartInterval 后,在高可用环境下会一直重启数据节点, 数据节点无法关闭。(**2.00.1**)

* 通过 `append!` 函数往响应式状态引擎（reactive state engine）写入数据时，如果输入的每列数据是 scalar，会导致系统崩溃。(**2.00.1**)

* 创建流数据引擎后，调用函数 `getAggregatorStat` 导致系统崩溃。(**2.00.1**)

* 键值表（keyed table）或索引表（indexed table）和内存表等值关联时，抛出 OOM 异常或导致系统崩溃。(**2.00.1**)

* 当最近一个事务操作是删除表的分区，且事务处于决议状态，数据节点有可能给出错误的决议结果。(**2.00.1**)

* 当使用 `remoteRun` 函数远程取消流表订阅时，远程连接可能卡死。(**2.00.1**)

* Asof join engine 写入异步持久化流表时导致系统崩溃。(**2.00.1**)

* 当多个数据节点向控制节点汇报元数据，如果时间相差很大，会出现元数据一直处于 recovering 状态。(**2.00.1**)

* 恢复某个分区后立刻进行 checkpoint， 并且后续该分区没有再写入，会导致元数据和数据不一致。(**2.00.1**)

* SQL 语句中使用 `interval` 子句插值时，分组字段可能出现空值。(**2.00.1**)

* `mr` 函数中数据源的脚本长度超过1024字节时，远程执行的数据源错误的将脚本字符串作为执行结果。(**2.00.1**)

* TSDB 引擎生成的文件非常多（超过1亿个）的时候，重启会卡住。(**2.00.2**)

* TSDB 引擎的 checkPoint 文件堆积而没有删除。(**2.00.2**)

* TSDB 引擎下删除文件时，如果与后台的 merge 操作并发，有时候会导致 merge 尝试读取已被删除的文件而 crash。(**2.00.2**)

* TSDB 引擎下，写入有时会有对应事务处于 pending 状态，导致该分区无法写入数据。(**2.00.2**)

* TSDB 引擎在数据库中有 blob 列时，有时查询数据或者后台 merge 的时候会报错。(**2.00.2**)

* 大压力写入数据时，偶发写任务卡住的情况。(**2.00.2**)

* Cache Engine 处理不当，导致 symbose base 一直无法被回收。如果随着时间推移，包含 SYMBOL 类型的分区一直增加，导致内存使用量一直缓慢上升。(**2.00.2**)

* 如果事务有 rollback，则 redo log 不会被回收。(**2.00.2**)

* 写入更新删除并发时，读取文件时会出现有时读到的数据比预期少，或者某些表会有空行，或者有些 chunk 状态不正确。(**2.00.2**)

* 多次写入时重启会报：“returned from name node didn't contain any site”。(**2.00.2**)

* 控制节点高可用，重启 leader，偶尔会导致数据节点 crash。(**2.00.2**)

* 由于 raft 模块在 leader 切换时处理不当，导致控制节点在高可用的情况下，同一个 chunk 在数据节点上有时候会对应多个 chunkId。(**2.00.2**)

* 控制节点在高可用的情况下，频繁切换 leader，导致写入或查询过程中任务卡住。(**2.00.2**)

* 在大量并发线程同时增加不存在的值分区时，由于线程的冲突和重试时间太短，导致某些新增值分区添加失败，抛出异常。(**2.00.2**)

* 使用非字符串非 SYMBOL 类型的值去更新分布式表的 SYMBOL 类型列，会导致 symbol base 被破坏。(**2.00.2**)

* 集群的数据节点在重启时收到大量的客户端请求，有可能在后续的鉴权中，出现登录了却当作 guest 处理的情况。(**2.00.2**)

* `tableInsert` 将一个包含多行数据但某些列缺失的字典插入内存表时报异常。(**2.00.2**)

* `replay` 回放三个数据表表时，会出现两个表的回放速度明显快于第三个表。(**2.00.2**)

* `replay` 回放到持久化流表log会报错：“Error in Replayer::output: Immutable sub vector doesn't support method serialize”。(**2.00.2**)

* `kurtosis` 和 `skew` 在流计算引擎中结果精度较低。(**2.00.2**)

* `createDailyTimeSeriesEngine` 使用 force Trigger 导致计算结果有 session 区间之外的时间。(**2.00.2**)

* TimeSeriesEngine 指定 fill 并且两个分组之间时间相差较大，计算结果可能出错。(**2.00.2**)

* `createAsofJoinEngine` 数据乱序时结果不对。(**2.00.2**)

* 没有输出表时，横截面引擎作为返回表会报字段缺失错误。(**2.00.2**)

* 一个引用的数据表调用函数 `colNames` 无法返回列名。(**2.00.2**)

* `saveText` 保存空表时候会抛异常。(**2.00.2**)

* `cumvarp` 和 `cumstdp` 应用在矩阵上时错误地调用了 `cumvar` 和 `cumstd`，导致计算结果变成基于样本的方差和标准差。(**2.00.2**)

* `try catch` 语句的 catch 部分包含多行代码时，实际上只有第一行代码会被执行。(**2.00.2**)

* 模块中有系统同名函数时，`parseExpr` 指定模块，没有优先取模块中的函数。(**2.00.2**)

* `interval` 函数在时间列为分区列且 duration 可以整除分区列的单位时，会多生成数据，这个 bug 是在 2.00.1 中引入的。(**2.00.2**)

* 当 `interval` 函数指定 step 参数且处理的列存在缺失的区间时，结果不正确。(**2.00.2**)

* order by 在第二列为负数时，且第二列或之后的数据为浮点数(DOUBLE 或 FLOAT)，且一个小组的数据的个数小于等于7个，且包含两个以上的负数，会导致负数之间的相对排序错误。(**2.00.2**)

* 诸如 exec col1 from t  group by col1 的 sql 语句返回结果不是向量。(**2.00.2**)

* 对 huge temporal vector 使用 `min` 和 `max` 函数，应该返回对应的时间类型，但实际上返回一个长整型。(**2.00.2**)

* `mskew` 输入的值过大会出现非法值INF。(**2.00.2**)

* 使用 `funcByName` 且参数为聚合函数时，和 context by 同时使用结果只会返回一行。(**2.00.2**)

* window join 在右表时间列有重复值时计算结果不正确。(**2.00.2**)

* 自定义函数中的常量均被标记为 static，使用时必须先复制。函数序列化时丢失了static标记。(**2.00.2**)

* JIT 版本的数据节点在 `loadColumn` 的时候，若发生 OOM，则会 crash。(**2.00.2**)

* TSDB 存储引擎下，`compact` 和 `dropPartition` 并发会导致元数据错误。(**2.00.3**)

* TSDB 存储引擎下，有时重启后数据节点无法启动，报 "iotCheckPointFile.meta" 无法初始化。(**2.00.3**)

* 修复了写入、删除、checkpoint、恢复并发的场景下数据库不稳定的问题。(**2.00.3**)

* 高可用集群有时候控制节点无法启动，报错："Failed to read rsa public key file"。(**2.00.3**)

* 集群 Python API 多并发有时候会出现数据节点死锁。(**2.00.3**)

* 控制节点上关于 chunk 的信息落后于数据节点。(**2.00.3**)

* 系统恢复之后发生了事务决议导致数据错乱。(**2.00.3**)

* OLAP 存储引擎下，redolog 在系统恢复之后再重放，可能导致数据丢失。(**2.00.3**)

* 时序聚合引擎中 append 的 table 的列数小于 dummyTable 的列数时会 crash。(**2.00.3**)

* 流数据高可用，将发布端的 leader 多次 kill 之后，再往发布端写入数据，订阅端有时收不到新数据。(**2.00.3**)

* `interval` 在指定线性填充方式，同时 where 指定的开始时间没有数据，且 group by 多个字段的时候，会出现错误的结果。(**2.00.3**)

* 当特殊字符作为列名时，`sqlCol` 会错误地把字段名称当作共享表的引用来处理。(**2.00.3**)

* 当y中的数据为连续的相等数据时，`mslr` 计算会产生正无穷。(**2.00.3**)

* `eachPre` 函数在计算矩阵时，如果矩阵行数过多，则会导致 crash。(**2.00.3**)

* `mpercentile` 计算偶尔会卡住。(**2.00.3**)

* `temporalParse` 对时间向量转换失败的情况下，返回的结果不正确，应该为 NULL。(**2.00.3**)

* 对空表进行 update 时，使用 context by 语句，不能产生新的列。(**2.00.3**)

* where 条件中"!="前面没有空格时解析失败。(**2.00.3**)

* 当事务刷盘过慢，可能会出现 redo log 回收超时，导致重启后数据丢失。（**2.00.4**）

* 通过一个 dolphindb server 同时启动多个 dolphindb 集群，出现数据节点无法启动的报错：”Failed to open public key file. No such file or directory.”。（**2.00.4**）

* 高可用集群设置了定时任务（ scheduled job），有时会出现因为各个控制节点初始用户的uuid不同，导致切换 leader 后，原有的定时任务在新 leader 上认证失败而无法执行的问题。（**2.00.4**）

* 数据节点崩溃之后，代理节点每隔一秒而不是按照参数 datanodeRestartInterval 配置的时间来重启数据节点。（**2.00.4**）

* 定时任务（ scheduled job）如果包含了 SQL update 语句，且 where 条件中使用了函数，则在系统重启时反序列化会失败。（**2.00.4**）

* 对分布式表更新后，若提交事务（commit）失败，则旧的物理目录不会被回收。（**2.00.4**）

* 高并发写入场景下，当 redo log 所在磁盘占满时，会概率性导致 redo log 回收线程死锁。（**2.00.4**）

* 数据节点写入数据时内存不足时，未报错 Out of Memory，而是卡住一段时间后崩溃。（**2.00.4**）

* OLAP 存储引擎在各种并发操作时出现节点随机下线的情况。等待一段时间后节点上线， `getTabletsMeta` 返回结果显示丢失一个副本的数据，但实际上并没有丢失。（**2.00.4**）

* TSDB存储引擎，若数据按照时间列（timeCol）分区，排序列（sortColumns）有两列以上，且最后一列为 timeCol，此时若按照排序列（sortColumns）分组，取每个分组内按照分区列（timeCol）排序后的前 k 条记录（`context by sortColumns csort timeCol limit k`），有时会 crash。（**2.00.4**）

* TSDB 存储引擎并发修改 edit log，导致数据节点无法重启。（**2.00.4**）

* 事务回滚出现超时场景下，chunk 的状态设置错误，导致流表持久化报错。（**2.00.4**）

* 横截面引擎（ cross-sectional engine ) 参数校验出错，指定 timeColumn 的情况下，没有指定 useSystemTime 或者指定 useSystemTime 为 true，未抛出异常。（**2.00.4**）

* 时间序列引擎（ time-series engine )中当指定 useSystemTime 为 true 且 outputTable 是分布式表时，有时会抛出类型不匹配的异常。（**2.00.4**）

* 用于流数据处理的 Asof Join Engine 指定 delayedTime 的情况下，有时写入数据会出现 crash。（**2.00.4**）

* 流数据高可用，两次 append 的数据都超过65536，如果此时发生 rollback，index.log 会重复写入两条一样的 index 导致报错：”index.log contains invalid data.“。（**2.00.4**）

* windows 系统下，向 time-series engine, daily time-series engine 和 asof join engine 写入数据，有时会发生 crash。（**2.00.4**）

*  subExecutor 还有任务在执行，此时，使用 `unsubscribeTable` 成功取消订阅，但 getStreamingStat().subWorkers 仍能查询到被取消订阅的 topic。（**2.00.4**）

* 节点重启之后，高可用流表有时会加载失败；流表和订阅的 raft 组都切换 leader 之后，高可用订阅自动重连失败。（**2.00.4**）

* 横截面引擎 triggeringPattern 为 'keyCount' 且 triggeringInterval 为 tuple 时，会输出重复数据。（**2.00.4**）

* 流表包含 BLOB 类型，从磁盘中加载报错：“Failed to decompress the vector. Invalid message format”。（**2.00.4**）

* 流表在写入 BLOB 数据且单行数据大于 64KB 时会 crash。（**2.00.4**）

* 给内存表增加的新列赋值时，错误的使用了 select 而不是 exec，加载该内存表时出现节点 crash。（**2.00.4**）

* GUI 上访问包含 array vector 的内存表 session 会断开。（**2.00.4**）

* 使用 `readRecord!` 导入二进制文件，会报错 ：“Read only object or object without ownership can‘t be applied to mutable function readRecord!”。（**2.00.4**）

* 函数调用时，若右括号不在同一行，有时解析会报错。（**2.00.4**）

* 表中包含 array vector 时，执行 `replayDS` 函数会导致节点 crash。（**2.00.4**）

* 查询一个值分区的分布式表，按分区列分组获取每个组最后的K条记录（context by partitionCol limit -k），且在某个分区里不存在满足 where 条件的数据时，会查到不满足条件的数据。（**2.00.4**）

* SQL 中调用 `rolling/moving` 函数时，若不指定生成列的列名，则会报错："More than one column has the duplicated name"。（**2.00.4**）

* `interval` 在某个 step 区间内没有数据时，会生成空值。（**2.00.4**）

* `sliceByKey` 的 rowKeys 的参数设置错误时，server 会 crash。 （**2.00.4**）

* 函数 `replace!` 修改一个向量，引入空值后，没有正确设置空值标志。（**2.00.4**）

* 修复了几个 TSDB 引擎的问题：（**2.00.5**）

    * SQL 查询时，若 `where` 过滤条件中包含 array vector 类型的列，可能导致 crash；

    * level file 合并后重启数据库，再次写入数据时，已经合并的 level file 不会被回收；

    * 从旧集群同步数据至新集群时，新集群各节点上的部分内存不释放；

    * SQL 查询时，若 `where` 条件的数据格式为 timestamp，而实际数据是 nanotimestamp 格式，则查询结果不正确；

    * 查询数据量比较大时，若查询语句包含 `group by`, `context by` 或 `pivot by` 操作，且操作的列包含多个 sortColumns 参数中指定的排序列，查询结果可能不完整；

    * 用 `group by` 分组查询 `count` 数目，可能导致 crash。

* 集群各节点之间在线同步数据时，若使用 `mr` 并行计算，可能导致节点崩溃。（**2.00.5**）

* 若在 1.30.16 之前版本中对分区名带有“.”字符的数据库分区进行 `backup` 备份，在 1.30.16 版本中通过 `migrate` 恢复数据时，可能报错。（**2.00.5**）

* 由于 1.30.16 引入的新功能，导致从 1.30.16 升级到 2.00.4 版本时出现兼容性问题。（**2.00.5**）

* 查询数据库时，有时会出现报错：“The remote call task doesn't associate any site.”。（**2.00.5**）

* 进行过 `upsert` / `update` / `delete` 操作的数据库，若使用 `imtUpdateChunkVersionOnDataNode` 更新了数据节点上的版本号，可能导致数据读取错误。（**2.00.5**）

* 修复了几个 array vector 的问题：（**2.00.5**）

    * 将 array vector 从一个数据节点发送到另一个数据节点时，可能导致 crash；

    * 对 array vector 的 subarray 求 `count` 数目，结果不正确；

    * 从空表中取 array vector 值导致结果不正确

* 由于 raft log 追加写有问题，导致高可用集群有时重启后无法正常启动。（**2.00.5**）

* 在 Windows 系统中，通过 `dropTable` 成功删除空表后，若通过 `renameTable` 把另一个表命名为此表，会报错提示文件已存在。（**2.00.5**）

* 具有 TABLE_WRITE 权限的用户在写入数据时，因数据库无法自动添加 VALUE 分区，导致写入失败。（**2.00.5**）

* 当时间序列引擎（time-series streaming engine）的 windowSize 参数是一个向量，且 metrics 参数为自定义函数时，可能导致系统崩溃。（**2.00.5**）

* 流数据高可用计算引擎中，当 follower 在写快照时有可能会死锁，导致后续收到的 raft log 无法被处理，占用内存不断增大。（**2.00.5**）

* 往高可用流表写入数据时，写入数据已经持久化，但 log 还未发送到 follower 时，若所有数据节点宕机，重启后节点间数据会不一致。（**2.00.5**）

* 重启节点后从磁盘加载持久化数据时，需要删除过期的 rowIndex 时误将最后一个 rowIndex 删除，导致数据缺失。（**2.00.5**）

* 流数据高可用状态下，两次 append 数据，每次数据都超过 65536 行，且leader 节点数据同步到 follower 上时发生了 leader 切换，会导致原 leader 节点重启后自动加载持久化流表失败。（**2.00.5**）

* 当高可用流表所在的 raft 组和高可用订阅的 raft 组不同时，如果两组 leader 同时切换或重启，而高可用流表所在 raft 组的 leader 节点竞选成功晚于高可用订阅的 raft 组，会导致自动重订阅失败。（**2.00.5**）

* 订阅（`subscribeTable`）时设置参数 offset=-2，参数设置无效。（**2.00.5**）

* 修正了 `atImax` 和 `atImin` 在参数为多列矩阵时的计算方式。自本版本起，这两个函数将对矩阵的每一列分别查找最值，并以向量的形式返回每一列的计算结果。（**2.00.5**）

* 对内存表和共享流表做表连接，可能导致系统崩溃。（**2.00.5**）

* SQL 查询中，`select` 与 `pivot by` 一起使用时，若在 `select` 子句中增加一列常量，会导致系统崩溃。（**2.00.5**）

* 提交定时任务时，若定时任务的函数有使用{}来生成字典，则会报错无法序列化。（**2.00.5**）

* 连接两个共享表时会报错：“Unrecognized column name”。（**2.00.5**）

* 使用 `sql` 函数生成查询，当 *from* 参数指定为表连接时，执行结果有误。（**2.00.5**）

* 当一个分布式表按时间进行值分区，且分区粒度大于分区列的时间精度时，跨库表连接时会报错。（**2.00.5**）

* `mmad` 和 `mad` 函数在 useMedian 参数为 true 时计算结果有误。同时在流数据引擎中修复了此问题。（**2.00.5**）

* 函数 `sqlDS` 中，在 `where` 条件语句中使用运算符过滤时间列时，没有正确分区剪枝。（**2.00.5**）

* 函数 `replayDS` 数据源解析时，对 `where` 条件语句中的 date col 表达式解析有误，没有正确分区剪枝。（**2.00.5**）

* 当函数中包含 window join 计算，且窗口参数 window 为 duration 数据对时，则添加函数视图（addFunctionView）时 server 端会在反序列化时报错。（**2.00.5**）

* 对时间分区列进行查询，当查询条件的时间粒度大于分区列的时间粒度时，查询结果有误。（**2.00.5**）

* `zigzag` 函数中，当参数 percent 为 false，参数 retrace 为 true 时，计算结果有误。（**2.00.5**）

* 函数 `loadText` 读取文件第一行时，“-”开头的负数识别为列名。（**2.00.5**）

* 在 SQL `group by` 语句中使用 `min` 或 `max` 函数时，向函数传入两个参数时，计算结果错误。（**2.00.5**）

* 并发进行写入、查询或计算时，有时出现因 Out of memory 导致系统卡住。（**2.00.6**）

* 数据持续写入 OLAP 存储引擎导致 Cache Engine 刷盘的同时进行查询，查询结果有时会不正确。（**2.00.6**）

* 向 OLAP 引擎 Cache Engine 中写入数据时，若抛出非 out of memory 的异常，则会一直重试导致系统卡住。（**2.00.6**）

* web 界面启用数据节点或反复重启集群，代理节点会产生僵尸子进程。（**2.00.6**）

* `suspendRecovery` 后调用 `moveReplicas` 函数，部分 chunk 未转移。（**2.00.6**）

* 提交并行任务后重启集群，重启后有几个 chunk 一直处于 RECOVERING 状态。（**2.00.6**）

* 使用 `delete` 语句删除大量数据时，会出现因 checkpoint 文件写入错误信息而导致节点 crash，无法再次启动的问题。（**2.00.6**）

* `createReactiveStateEngine` 中开启 snapshot，当取消订阅之后再次订阅时，若 metrics 与第一次订阅不同，则会导致 server crash。（**2.00.6**）

* lookup join 引擎插入单条数据可能导致 server crash。（**2.00.6**）

* 即使写入高可用流表 schema 不一致，仍然会被放到持久化队列，导致 leader 切换后会报错："Can't find the object with name"。（**2.00.6**）

* `createDailyTimeSeriesEngine` 如果指定 fill，会对输入表中间不包含数据的日期进行填充。（**2.00.6**）

* 非 admin 用户可以调用 `createUser` 函数。（**2.00.6**）

* `changePwd` 没有限制新密码的长度。（**2.00.6**）

* `loadText` 加载数据到内存表时，若某列数据全部为中文字符，或同时包含中文字符和数字时，会忽略中文字符。（**2.00.6**）

* array vector 占用内存非常大，但没有达到 warningMemSize，出现："out of memory" 的报错。（**2.00.06**）

* 使用 `matrix([],[])` 语句会导致 crash。（**2.00.6**）

* `exec` 搭配 `pivot by`，若不对 `exec` 选择的列字段调用函数，不会生成一个矩阵，而是生成一个 table。（**2.00.6**）

* `randomForestClassifier` 如果设置 numJobs > 1 或者 numJobs=-1，当重复使用同一个 dataSource 进行训练时，则会导致 server crash。（**2.00.6**）

* `interval`函数的 duration 的时间精度与实际数据的精度不匹配导致 crash。（**2.00.6**）

* keyedTable(keyColumns, table) 创建键值内存表时，若 table 存在重复键值，发生内存泄露。（**2.00.6**）

* 调用 `olsEx` 方法，传入一个查询结果为空的数据源后，数据节点发生 crash。（**2.00.6**）

* 为 `addFunctionView`  传入自定义函数包含超过64k的字符串时，会导致 server crash。（**2.00.6**）

* `mcorr`, `mwavg`等支持矩阵计算的 m 系列函数对索引矩阵做计算时，计算结果 lable 列会丢失。（**2.00.6**）

* Web 管理界面：文件系统 (DFS) 白屏、任务展开异常、交互编程界面执行结果是包含 NULL 值的 vector 时表格无法显示。（**2.00.6**）

## GUI

* GUI画图函数plot多曲线可共享y轴。(**2.00.1**)