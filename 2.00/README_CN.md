# DolphinDB发行说明

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




> 新功能

* 发布TSDB存储引擎。`database`函数提供了一个可选参数engineType，默认值为OLAP，即旧的存储引擎。如果创建基于TSDB存储引擎的数据库，engineType设置为TSDB即可。(**2.00.0**)
* 基于TSDB存储引擎的数据支持新的数据类型BLOB。(**2.00.0**)
* 新增`percentileRank`函数，计算一个值在一个向量中的百分位。(**2.00.1**)
* 新增`zigzag`函数，计算数据中的极值点。(**2.00.1**)
* 新增`lowDouble`和`highDouble`函数，用于将point和complex等16字节的数据类型分解成高位8字节的double类型和低位8字节的double类型。(**2.00.1**)
* 新增`rdp`压缩算法函数。(**2.00.1**)
* 新增计算加权最小二乘回归函数`wls`。(**2.00.1**)
* 流数据引擎支持equal join。(**2.00.1**)
* 新增`ifNull`和`ifValid`函数。(**2.00.1**)
* DolphinDB集群支持新的节点类型：计算节点 (computing node)。与数据节点可同时用于计算引擎和存储引擎不同，计算节点只能用于计算引擎。(**2.00.1**)
* 流计算引擎reateReactiveStateEngine, AnomalyDetectionEngine, SessionWindowEngine, DailyTimeSeriesEngine和TimeSeriesEnginereactive支持高可用。(**2.00.2**)
* 新增功能，跨集群数据异步复制。(**2.00.2**)
* 新增函数`covarMatrix`和`corrMatrix`，来计算pairwise covariance和correlation，性能比直接使用高阶函数cross和covar/corr的组合快1~2个数量级。(**2.00.2**)
* 新增配置项stdoutLog，当取值为true或1时，不再输出系统的日志到文件，而是输出到stdout。(**2.00.2**)
* 新增高阶函数`tmoving`，可以实现时间窗口的滑动。同时响应式状态引擎中实现高阶函数`moving`和`tmoving`对应的状态函数(state function)。(**2.00.2**)
* 新增函数`runScript`，用于执行一段脚本。(**2.00.2**)
* 新增函数`makeUnifiedCall`, `binaryExpr`和`unifiedExpr`用于元编程。(**2.00.2**)
* 新增23个按时间滑动的窗口系列函数，包括`tmove`，`tmfirst`，`tmlast`, `tmsum`, `tmavg`, `tmcount`, `tmvar`, `tmvarp`, `tmstd`, `tmstdp`, `tmprod`, `tmskew`, `tmkurtosis`, `tmmin`, `tmmax`, `tmmed`, `tmpercentile`, `tmrank`, `tmcovar`, `tmbeta`, `tmcorr`, `tmwavg`, `tmwsum`。并在响应式状态引擎中实现对应的状态函数。(**2.00.2**)
* 新增函数`sma`,`wma`, `dema`, `tema`, `trima`, `talib`, `talibNull`和`linearTimeTrend`。(**2.00.2**)
* 新增函数`countNanInf`和`isNanInf`，统计scalar, vector或matrix中包含多少个NaN和Inf值。(**2.00.2**)
* 增加流数据window join引擎。(**2.00.2**)
* 时间序列聚合引擎新增函数实现：`count`, `firstNot`, `ifirstNot`, `ilastNot`, `imax`, `imin`, `lastNot`, `nunique`, `prod`, `quantile`, `sem`, `sum3`, `sum4`, `mode`和`searchK`。(**2.00.2**)
* 增加函数`getConfigure`，传入一个key，返回该配置项信息。如果参数为0，返回所有配置项目信息。(**2.00.2**)
* 新增命令`clearCachedModules`，可以强制清除缓存的module。当缓存清除后，执行use语句时，会重新从文件加载module。这个方法可以在不重启节点的情况下，重新加载已经更新的module。只有admin才有权限执行这个命令。(**2.00.2**)
* 支持新的数据类型array vector，array vector的每一行是具有相同数据类型的不定长的数组。目前分布式表中仅TSDB引擎支持。(**2.00.2**)
* 新增按行聚合函数`rowSize`, `rowStdp`, `rowVarp`, `rowSkew`和`rowKurtosis`。(**2.00.2**)
* 支持匿名的聚合函数定义。(**2.00.3**)
* 支持postStart.dos文件，可用于启动DolphinDB时挂载定时任务。(**2.00.3**)
* 新增tcmalloc控制预留内存配置选项，当内存占用接近maxMemSize的时候，控制能够分配的内存块的最大尺寸，避免因OOM导致crash。(**2.00.3**)
* 增加`cumfirstNot`,`cumlastNot`, `mfirst`，`mlast`等函数，以及在响应式引擎中实现它们的状态函数。(**2.00.3**)
* 新增函数`oneHot`，用于做one hot（独热）编码。(**2.00.3**)
* 新增`setAtomicLevel`函数，用于修改历史数据库的配置以支持并发写入。(**2.00.3**)
* 支持表级别分区粒度，支持同一库中不同的表可以并发写入。（**2.00.4**）
* 往内存表的时间列写入数据时，自动进行时间类型转换。（**2.00.4**）
* 支持在线增量恢复，可以异步地进行节点数据恢复。 （**2.00.4**）
* 支持管理和查询集群中的所有计算任务。（**2.00.4**）
* 内存表和流数据表支持 BLOB 类型。（**2.00.4**）
* 支持真正的快照隔离。（**2.00.4**）
* SQL语句增加标识 [HINT_EXPLAIN]，可以显示 SQL 的执行过程。（**2.00.4**）
* 新增函数streamEngineParser，支持自动分解截面因子成多个内置流计算引擎的流水线。（**2.00.4**）
* 新增函数existSubscriptionTopic，用于判断某一个订阅是否已经创建。（**2.00.4**）
* 新增函数createLookupJoinEngine，支持将流数据表和一个相对稳定的表做左连接。（**2.00.4**）
* 新增函数moveChunksAcrossVolume，在增加新的 volume 后，用于转移旧 volume 的部分 chunk 到新 volume。（**2.00.4**）
* 增加新的 volume 后，可以使用resetDBDirMeta函数转移老的 volume 上的 meta log 目录到新的volume。（**2.00.4**）
* 新增 10 个TopN函数 msumTopN, mavgTopN, mstdpTopN, mstdTopN, mvarTopN, mvarpTopN, mcorrTopN, mbetaTopN, mcovarTopN, mwsumTopN，且 createReactiveStateEngine 引擎支持它们相应的状态函数。（**2.00.4**）
* 新增函数makeKey和makeOrderedKey，可以将多个列合并成一个 BLOB 列，用作字典或集合的键值，其中makeOrderedKey的结果保留了多个字段的排序顺序。（**2.00.4**）
* 新增高阶函数aggrTopN，用以计算根据排序列获取的前N行数据的聚合结果。（**2.00.4**）
* 新增高阶函数window和twindow，支持窗口函数的计算。（**2.00.4**）
* 新增配置项raftElectionTick，用以配置raft切换leader的心跳时间。同时新增函数setCacheEngineMemSize, setTimeoutTick，setTSDBCacheEngineSizesetMaxMemSize，setReservedMemSize和 setMaxBlockSizeForReservedMemory支持在线修改对应的配置项。（**2.00.4**）
* 新增函数fixedLengthArrayVector，支持将多个向量合成一个 array vector。（**2.00.4**）
* 新增函数loadNpz支持导入 numpy 的 npz 文件。（**2.00.4**）
* 新增函数suspendRecovery用于暂停 recovery 任务，新增函数resumeRecovery用于重启recovery任务。（**2.00.4**）
* 新增函数 rowCorr, rowCovar, rowBeta, rowWsum, rowWavg，可以对每行数据进行计算。（**2.00.4**）
* 新增函数 movingWindowIndex 和 movingTopNIndex，用于获取每一个滑动窗口的元素下标，返回一个INDEX[]类型的 array vector。（**2.00.4**）
* 新增fflush函数，帮助将缓存中的数据写入文件系统。（**2.00.4**）

改进

* createTimeSeriesEngine和createDailyTimeSeriesEngine函数新增参数forceTriggerTime。(**2.00.1**)

* 缩短了scheduleJob的间隔时间到5分钟。(**2.00.1**)

* timeSeriesEngine 和 DailyTimeSeriesEngine支持多个keyColumn。(**2.00.1**)

* upsert!函数ignoreNull字段支持DFS表。(**2.00.1**)

* parseExpr新增可选参数modules和overloadedOperators，可加载模块，重载运算符，且支持使用字典来给表达式中的变量赋值。(**2.00.1**)

* sql 函数新增可选参数exec，支持生成exec语句。(**2.00.1**)

* TSDB引擎去重策略支持KEEP_FIRST，重复数据仅保留第一条数据。(**2.00.1**)

* `temporalAdd`支持增加与减去工作日（BusinessDay），支持时间类型DATEHOUR。(**2.00.1**)

* 控制节点的元数据信息新增修改时间戳。(**2.00.1**)

* SQL GROUPBY子句中的interval函数支持step参数，以滑动窗口的方式计算聚合结果。(**2.00.1**)

* `sql`函数中当参数groupFlag为PIVOTBY时，参数groupBy支持选择多列。(**2.00.1**)

* createReactiveStateEngine新增字段keyPurgeFilter和keyPurgeFreqInSecond，以支持响应式状态引擎（reactive state engine）自动清理key。(**2.00.1**)

* 响应式状态引擎（reactive state engine）支持输出结果到分布式表和流数据表，支持接受来自replay的输入。(**2.00.1**)

* delete语句支持map子句，将delete语句下沉到各分区执行。(**2.00.1**)

* 用户自定义函数的输入参数支持默认值。(**2.00.1**)

* Windows安装包的dolphindb.cfg、controller.cfg、cluster.cfg默认配置项中移除redolog配置参数。(**2.00.1**)

* 改进redo log的回放性能。在有大量小事务的情况下，性能有10倍以上的提升。(**2.00.1**)

* 修改`iif`函数在condition包含空值时的行为。旧版本中condition的元素包含空值被当作false处理。新版本中如果为空值，对应的结果也为空值。(**2.00.2**)

* 矩阵进行`accumulate`等计算时放开8192行的限制。(**2.00.2**)

* 对维度表的并发执行写入、更新等操作时，不再抛出事务冲突异常。(**2.00.2**)

* 数据节点重启时，redolog的回放会在日志中输出详细的进度。(**2.00.2**)

* SQL语句中的`interval`功能（按时间聚合）移除range参数，同时增加可选参数explicitOffset，默认值为false。当该参数为true时，可以将第一个窗口的起始位置指定为where指定的窗口的起始位置。(**2.00.2**)

* `ols`和`wls`在mode为2的时候，新增一个输出Residual。同时新增一个函数`residual`用于计算回归的残差。。(**2.00.2**)

* in(X, Y)函数的参数Y支持为NULL，当Y为无类型的NULL时，函数的返回值为false或每一个值为false的vector。(**2.00.2**)

* 计算节点(computing node)支持客户端的所有操作。(**2.00.2**)

* SQL pivot产生的表列名不再特殊处理，即直接使用pivot的值作为列名。(**2.00.2**)

* 函数`rank`, `denseRank`, `cumrank`, `rowRank`和`rowDenseRank`支持percent形式。(**2.00.2**)

* kmeans支持自定义质心。(**2.00.2**)

* window join增加对`varp`, `stdp`, `prod`，`skew`和`kurtosis` 5个聚合函数的优化。(**2.00.2**)

* 支持对非数值类型进行`unpivot`。(**2.00.2**)

* 滑动窗口函数系列如`msum`，当输入数据为indexed matrix或indexed series时，窗口支持时间偏移窗口类型。(**2.00.2**)

* 优化了TSDB引擎中`dropPartition`的性能。(**2.00.2**)

* TSDB新增配置选项TSDBBlockSize，可以指定TSDB存储时一个block的大小。(**2.00.2**)

* `database`函数新增可选参数atomic。当atomic取值为'CHUNK'时，写入操作只保准分区的原子性，此时也允许多个并发线程同时写入该数据库的同一个分区。(**2.00.2**)

* 时序聚合引擎的forceTriggerTime参数计算规则修改，设置updateTime时，不再限制输出表为keyedTable。(**2.00.3**)

* 横截面引擎添加是否触发有效计算的开关。(**2.00.3**)

* 响应式引擎中增加支持`mmad`状态函数。(**2.00.3**)

* 时序聚合引擎新增对nanotimestamp的规整。(**2.00.3**)

* 共享流表新增权限控制。(**2.00.3**)

* getStreamingStat().subWorkers的结果表中增加以下参数：msgAsTable, batchSize, throttle, hash, filter, persistOffset, timeTrigger, handlerNeedMsgId, raftGroup, 用于对流数据的监控。(**2.00.3**)

* `sma, wma, dema, tema, trima, t3, ma, talib, talibNull, linearTimeTrend`增加流数据中对应的state function。(**2.00.3**)

* 分布式join改进，支持更多的场景，支持的函数包括 `lj`, `lsj`, `ej`, `aj`和`wj`，可以对不同分区方案的表，分区列不是连接列的表，或者不在同一库中的分布式表做join。(**2.00.3**)

* 维度表的delete支持并发操作。(**2.00.3**)

* array vector的index支持slice。(**2.00.3**)

* string类型支持直接与NULL进行比较。(**2.00.3**)

* 提升`stdp`, `std`, `varp`, `var`, `skew`, `kurtosis`, `mskew`, `mkurtosis`, `tmskew`, `tmkurtosis`，以及window join中`skew`和`kurtosis`等函数的精度。(**2.00.3**)

* 支持更多与array vector相关计算，包括`groups`, `distinct`, `nunique` 和 `at`。(**2.00.3**)

* 高阶函数的第一个参数会被强制解析成函数。(**2.00.3**)

* `distinct`函数可与group by配合使用，其结果为一个array vector。(**2.00.3**)

* `nunique`函数支持分布式计算。(**2.00.3**)

* UDF函数支持keyword arguments。(**2.00.3**)

* 新增对`qr`, `ols`, `dot`函数输入的校验，不允许行数或列数为0的矩阵作为输入。(**2.00.3**)

* TSDB 引擎优化查询某个字段对应的最新数条记录的性能，性能提升数倍至数百倍。（**2.00.4**）

* 优化 TSDB 在调用 top 子句查询数据时的性能。（**2.00.4**）

* 提升 TSDB 存储引擎中查询预计算数据的速度。（**2.00.4**）

* 使用赋值语句对内存表进行更新时，支持在行过滤条件中输入 BOOL 类型数组，形如：t[`y, t[`y]>0] = 0，其中 t 是表变量，y 是 t 的列名。（**2.00.4**）

* upsert!函数新增可选参数 *sortColumns*，更新后的表可根据该指定列进行排序。（**2.00.4**）

* cancelJob, cancelConsoleJob支持同时取消多个任务，且优化了集群阻塞时取消任务的性能。（**2.00.4**）

* loadText支持 *schema* 中指定数据类型为 array vector。（**2.00.4**）

* set支持 BLOB 类型的值。（**2.00.4**）

* keyedStreamTable 一次性批量插入多条键值相同的新记录，出现插入会失败。（**2.00.4**）

* 优化了atImin和atImax在window join中的使用性能。（**2.00.4**）

* run函数新增可选参数 *clean*，控制是否清理当前session中的变量。（**2.00.4**）

* wj函数，duration 支持设置为 y（年），M（月），B（工作日）。（**2.00.4**）

* loadText支持字符串包含 ASCII 码为 0 的字符。（**2.00.4**）

* 支持对矩阵的条件赋值。（**2.00.4**）

* loadTextEx新增可选参数 *atomic*，默认值是false。加载大文件的情景下，设置该参数为false，将文件加载事务拆分为多个事务。（**2.00.4**）

* getCompletedQueries函数和 getRunningQueries函数返回值中添加remoteIP字段。（**2.00.4**）

* 配置项参数 *stdoutLog* 支持设置为 2，表示同时打印日志到标准输出和日志文件。（**2.00.4**）

* 异常检测引擎（anomaly detection engine）*metrics* 参数支持序列相关函数。（**2.00.4**）

* 时序引擎（time-series engine）*windowSize* 为向量时，各元素取值可相同。（**2.00.4**）

* 横截面引擎（ cross-sectional engine）支持 *keyColumn* 输入一个向量。（**2.00.4**）

* 支持向流数据引擎插入 tuple 类型的记录。（**2.00.4**）

* 函数getStreamEngineStat返回的横截面引擎的统计信息添加了memoryUsed 字段，可以查看横截面引擎所占内存。（**2.00.4**）

* createAsofJoinEngine 在 *metrics* 中支持输出右表的时间列。（**2.00.4**）

* 共享内存表（共享流表）新增可读不可写的权限管理。（**2.00.4**）

* 提升了控制节点高可用的稳定性。（**2.00.4**）

* 日志中新增打印delete和update操作信息。（**2.00.4**）

* 输出日志中流订阅任务的报错信息增加订阅主题。（**2.00.4**）

* Web任务管理界面优化。重新设计、整合了 Web 管理界面，增加了作业管理功能，支持查看、停止、取消 DolphinDB 运行中、已提交和定时触发的作业。

  新版本 server 端对于 http://ip:port/ 默认渲染 index.html (原来会根据结点类型默认渲染 default.html 或者 nodedetail.html), 因此需要用户在升级的同时更新替换 web 文件夹，不能只替换 server 可执行文件，否则访问网页会报错 cannot find file index.html

  如果用户在收藏夹中保存了旧的带有路径的链接 (default.html 和 nodedetail.html)，可能出现打开后缺少导航栏，无法登陆的问题，需要用户去掉地址栏后面的路径，直接访问 http://ip:port/

  新版本使用了 WebSocket 协议，增加了对 DolphinDB 二进制协议的支持，对浏览器的要求也随之提高，可能需要用户更新浏览器到最新的版本，推荐使用 Chrome 最新版或 Edge 最新版。（**2.00.4**）

Bug fixes:

* 删除分布式表（使用dropTable或dropPartition）在提交时失败，导致事务回滚后，再次查询该表时结果不符合预期。删除该表缓存后，查询恢复正常。(**2.00.1**)
* TSDB Engine的TSDBRedoLogDir 配置不生效。(**2.00.1**)
* 配置参数datanodeRestartInterval后,在高可用环境下会一直重启数据节点, 数据节点无法关闭。(**2.00.1**)
* 通过`append!`函数往响应式状态引擎（reactive state engine）写入数据时，如果输入的每列数据是scalar，会导致系统崩溃。(**2.00.1**)
* 创建流数据引擎后，调用函数`getAggregatorStat`导致系统崩溃。(**2.00.1**)
* 键值表（keyed table）或索引表（indexed table）和内存表等值关联时，抛出OOM异常或导致系统崩溃。(**2.00.1**)
* 当最近一个事务操作是删除表的分区，且事务处于决议状态，数据节点有可能给出错误的决议结果。(**2.00.1**)
* 当使用remoteRun函数远程取消流表订阅时，远程连接可能卡死。(**2.00.1**)
* Asof join engine写入异步持久化流表时导致系统崩溃。(**2.00.1**)
* 当多个数据节点向控制节点汇报元数据，如果时间相差很大，会出现元数据一直处于recovering状态。(**2.00.1**)
* 恢复某个分区后立刻进行checkpoint， 并且后续该分区没有再写入，会导致元数据和数据不一致。(**2.00.1**)
* SQL语句中使用interval子句插值时，分组字段可能出现空值。(**2.00.1**)
* `mr`函数中数据源的脚本长度超过1024字节时，远程执行的数据源错误的将脚本字符串作为执行结果。(**2.00.1**)
* TSDB引擎生成的文件非常多（超过1亿个）的时候，重启会卡住。(**2.00.2**)
* TSDB引擎的checkPoint文件堆积而没有删除。(**2.00.2**)
* TSDB引擎下删除文件时，如果与后台的merge操作并发，有时候会导致merge尝试读取已被删除的文件而crash。(**2.00.2**)
* TSDB引擎下，写入有时会有对应事务处于pending状态，导致该分区无法写入数据。(**2.00.2**)
* TSDB引擎在数据库中有blob列时，有时查询数据或者后台merge的时候会报错。(**2.00.2**)
* 大压力写入数据时，偶发写任务卡住的情况。(**2.00.2**)
* Cache Engine处理不当，导致symbose base一直无法被回收。如果随着时间推移，包含SYMBOL类型的分区一直增加，导致内存使用量一直缓慢上升。(**2.00.2**)
* 如果事务有rollback，则redo log不会被回收。(**2.00.2**)
* 写入更新删除并发时，读取文件时会出现有时读到的数据比预期少，或者某些表会有空行，或者有些chunk状态不正确。(**2.00.2**)
* 多次写入时重启会报“returned from name node didn't contain any site”。(**2.00.2**)
* 控制节点高可用，重启leader，偶尔会导致数据节点 crash。(**2.00.2**)
* 由于raft模块在leader切换时处理不当，导致控制节点在高可用的情况下，同一个chunk在数据节点上有时候会对应多个chunkId。(**2.00.2**)
* 控制节点在高可用的情况下，频繁切换leader，导致写入或查询过程中任务卡住。(**2.00.2**)
* 在大量并发线程同时增加不存在的值分区时，由于线程的冲突和重试时间太短，导致某些新增值分区添加失败，抛出异常。(**2.00.2**)
* 使用非字符串非SYMBOL类型的值去更新分布式表的SYMBOL类型列，会导致symbol base被破坏。(**2.00.2**)
* 集群的数据节点在重启时收到大量的客户端请求，有可能在后续的鉴权中，出现登录了却当作guest处理的情况。(**2.00.2**)
* `tableInsert`将一个包含多行数据但某些列缺失的字典插入内存表时报异常。(**2.00.2**)
* replay回放三个数据表表时，会出现两个表的回放速度明显快于第三个表。(**2.00.2**)
* replay回放到持久化流表log会报错“Error in Replayer::output: Immutable sub vector doesn't support method serialize”。(**2.00.2**)
* `kurtosis`和`skew`在流计算引擎中结果精度较低。(**2.00.2**)
* `createDailyTimeSeriesEngine`使用force Trigger导致计算结果有session区间之外的时间。(**2.00.2**)
* TimeSeriesEngine指定fill 并且两个分组之间时间相差较大，计算结果可能出错。(**2.00.2**)
* `createAsofJoinEngine`数据乱序时结果不对。(**2.00.2**)
* 没有输出表时，横截面引擎作为返回表会报字段缺失错误。(**2.00.2**)
* 一个引用的数据表调用函数`colNames`无法返回列名。(**2.00.2**)
* `saveText`保存空表时候会抛异常。(**2.00.2**)
* `cumvarp`和`cumstdp`应用在矩阵上时错误地调用了`cumvar`和`cumstd`，导致计算结果变成基于样本的方差和标准差。(**2.00.2**)
* `try catch`语句的catch部分包含多行代码时，实际上只有第一行代码会被执行。(**2.00.2**)
* 模块中有系统同名函数时，`parseExpr`指定模块，没有优先取模块中的函数。(**2.00.2**)
* `interval`函数在时间列为分区列且duration可以整除分区列的单位时，会多生成数据，这个bug是在1.30.13中引入的。(**2.00.2**)
* 当`interval`函数指定step参数且处理的列存在缺失的区间时，结果不正确。(**2.00.2**)
* order by在第二列为负数时，且第二列或之后的数据为浮点数(double或float)，且一个小组的数据的个数小于等于7个，且包含两个以上的负数，会导致负数之间的相对排序错误。(**2.00.2**)
* 诸如exec col1 from t  group by col1的sql语句返回结果不是向量。(**2.00.2**)
* 对huge temporal vector使用min和max函数，应该返回对应的时间类型，但实际上返回一个长整型。(**2.00.2**)
* `mskew`输入的值过大会出现非法值INF。(**2.00.2**)
* 使用`funcByName`且参数为聚合函数时，和context by同时使用结果只会返回一行。(**2.00.2**)
* window join在右表时间列有重复值时计算结果不正确。(**2.00.2**)
* 自定义函数中的常量均被标记为static，使用时必须先复制。函数序列化时丢失了static标记。(**2.00.2**)
* JIT版本的数据节点在`loadColumn`的时候，若发生OOM，则会crash。(**2.00.2**)
* TSDB存储引擎下，compact和dropPartition并发会导致元数据错误。(**2.00.3**)
* TSDB存储引擎下，有时重启后数据节点无法启动，报iotCheckPointFile.meta无法初始化。(**2.00.3**)
* 修复了写入、删除、checkpoint、恢复并发的场景下数据库不稳定的问题。(**2.00.3**)
* 高可用集群有时候控制节点无法启动，报错"Failed to read rsa public key file"。(**2.00.3**)
* 集群Python API多并发有时候会出现数据节点死锁。(**2.00.3**)
* 控制节点上关于chunk的信息落后于数据节点。(**2.00.3**)
* 系统恢复之后发生了事务决议导致数据错乱。(**2.00.3**)
* OLAP存储引擎下，redolog在系统恢复之后再重放，可能导致数据丢失。(**2.00.3**)
* 时序聚合引擎中append的table的列数小于dummyTable的列数时会crash。(**2.00.3**)
* 流数据高可用，将发布端的leader多次kill之后，再往发布端写入数据，订阅端有时收不到新数据。(**2.00.3**)
* `interval`在指定线性填充方式，同时where指定的开始时间没有数据，且group by多个字段的时候，会出现错误的结果。(**2.00.3**)
* 当特殊字符作为列名时，`sqlCol`会错误地把字段名称当作共享表的引用来处理。(**2.00.3**)
* 当y中的数据为连续的相等数据时，`mslr`计算会产生正无穷。(**2.00.3**)
* `eachPre`函数在计算矩阵时，如果矩阵行数过多，则会导致crash。(**2.00.3**)
* `mpercentile`计算偶尔会卡住。(**2.00.3**)
* `temporalParse`对时间向量转换失败的情况下，返回的结果不正确，应该为NULL。(**2.00.3**)
* 对空表进行update时，使用context by语句，不能产生新的列。(**2.00.3**)
* where 条件中"!="前面没有空格时解析失败。(**2.00.3**)
* 当事务刷盘过慢，可能会出现 redo log 回收不及时，导致重启后数据丢失。（**2.00.4**）
* 通过一个dolphindb server同时启动多个dolphindb 集群，出现数据节点无法启动的报错”Failed to open public key file. No such file or directory.”。（**2.00.4**）
* 高可用集群设置了定时任务（ scheduled job），有时会出现因为各个控制节点初始用户的uuid不同，导致切换leader后，原有的定时任务在新leader上认证失败而无法执行的问题。（**2.00.4**）
* 数据节点崩溃之后，代理节点每隔一秒而不是按照参数 datanodeRestartInterval配置的时间来重启数据节点。（**2.00.4**）
* 定时任务（ scheduled job）如果包含了SQL update语句，且 where 条件中使用了函数，则在系统重启时反序列化会失败。（**2.00.4**）
* 对分布式表更新后，若提交事务（commit）失败，则旧的物理目录不会被回收。（**2.00.4**）
* 高并发写入时，当 redo log 所在磁盘占满时，会概率性导致 redo log 回收线程死锁。（**2.00.4**）
* 数据节点写入数据时内存不足时，未报错 Out of Memory，而是卡住一段时间后崩溃。（**2.00.4**）
* OLAP 存储引擎在各种并发操作时出现节点随机下线的情况。等待一段时间后节点上线， getTabletsMeta返回结果显示丢失一个副本的数据，但实际上并没有丢失。（**2.00.4**）
* TSDB存储引擎，若数据按照时间列（*timeCol*）分区，排序列（ *sortColumns* ）有两列以上，且最后一列为 timeCol，此时若查询语句为 context by sortColumns csort timeCol limit k(k为整数)，有时会 crash。（**2.00.4**）
* TSDB 存储引擎并发修改 edit log，导致数据节点无法重启。（**2.00.4**）
* 事务回滚出现超时场景下，chunk 的状态设置错误，导致流表持久化报错。（**2.00.4**）
* 流数据引擎写入持久化流表时，若压缩失败，系统可能会 crash。（**2.00.4**）
* 横截面引擎（ cross-sectional engine ) 参数校验出错，指定 *timeColumn* 的情况下，没有指定 *useSystemTime* 或者指定 *useSystemTime* 为true，未抛出异常。（**2.00.4**）
* 时间序列引擎（ time-series engine )中当指定 *useSystemTime* 为true且 *outputTable* 是分布式表时，有时会抛出类型不匹配的异常。（**2.00.4**）
* 用于流数据处理的Asof Join Engine指定 *delayedTime* 的情况下，有时写入数据会出现 crash。（**2.00.4**）
* 流数据高可用，两次append的数据都超过65536，如果此时发生rollback，index.log会重复写入两条一样的index导致报错”index.log contains invalid data.“。（**2.00.4**）
* Windows系统使用time-series engine, daily time-series engine, asof join engine写入数据有时会发生 crash。（**2.00.4**）
* unsubscribeTable 取消订阅，当消费队列有数据堆积时，会导致 subworker 里面残留过期的信息。（**2.00.4**）
* 节点重启之后，高可用流表有时会加载失败；流表和订阅的 raft 组都切换 leader 之后，高可用订阅自动重连失败。（**2.00.4**）
* 横截面引擎 *triggeringPattern* 为 keyCount 且 *triggeringInterval* 为 tuple 时，会输出重复数据。（**2.00.4**）
* 流表包含 BLOB 类型，从磁盘中加载报错“Failed to decompress the vector. Invalid message format”。（**2.00.4**）
* 流表在写入 BLOB 数据且单行数据大于 64KB 时会 crash。（**2.00.4**）
* 给内存表增加的新列赋值时，错误的使用了 select 而不是 exec，再次查询该内存表时出现节点crash。（**2.00.4**）
* GUI 上访问包含 array vector 的内存表 session 会断开。（**2.00.4**）
* 使用readRecord!导入二进制文件，会报错“Read only object or object without ownership can‘t be applied to mutable function readRecord!”。（**2.00.4**）
* 函数调用时，若右括号不在同一行，有时解析会报错。（**2.00.4**）
* 表中包含 array vector 时，执行 replayDS 函数会导致节点 crash。（**2.00.4**）
* 查询一个值分区的分布式表，按分区列分组获取每个组最后的K条记录（context by partitionCol limit -k），且在某个分区里不存在满足 where 条件的数据时，会查到不满足条件的数据。（**2.00.4**）
* SQL中调用rolling/moving函数时，若不指定生成列的列名，则会报错”More than one column has the duplicated name”。（**2.00.4**）
* interval在某个 *step* 区间内没有数据时，会生成空值。（**2.00.4**）
* sliceByKey的 *rowKeys* 的参数设置错误时，server 会 crash。 （**2.00.4**）
* 函数replace!修改一个向量，引入空值后，没有正确设置空值标志。（**2.00.4**）

> GUI

* GUI画图函数plot多曲线可共享y轴。(**2.00.1**)