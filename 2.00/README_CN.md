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
* 新增函数`sma`,`wma`, `dema`, `tema`, `trima`, `talib`, `talibNull`和`linearTimeTrend`。并在响应式状态引擎中实现对应的状态函数(**2.00.2**)
* 新增函数`countNanInf`和`isNanInf`，统计scalar, vector或matrix中包含多少个NaN和Inf值。(**2.00.2**)
* 增加流数据window join引擎。(**2.00.2**)
* 时间序列聚合引擎新增函数实现：`count`, `firstNot`, `ifirstNot`, `ilastNot`, `imax`, `imin`, `lastNot`, `nunique`, `prod`, `quantile`, `sem`, `sum3`, `sum4`, `mode`和`searchK`。(**2.00.2**)
* 增加函数`getConfigure`，传入一个key，返回该配置项信息。如果参数为0，返回所有配置项目信息。(**2.00.2**)
* 新增命令`clearCachedModules`，可以强制清除缓存的module。当缓存清除后，执行use语句时，会重新从文件加载module。这个方法可以在不重启节点的情况下，重新加载已经更新的module。只有admin才有权限执行这个命令。(**2.00.2**)
* 支持新的数据类型array vector，array vector的每一行是具有相同数据类型的不定长的数组。目前分布式表中仅TSDB引擎支持。(**2.00.2**)
* 新增按行聚合函数`rowSize`, `rowStdp`, `rowVarp`, `rowSkew`和`rowKurtosis`。(**2.00.2**)

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

> GUI

* GUI画图函数plot多曲线可共享y轴。(**2.00.1**)
