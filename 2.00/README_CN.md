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
* `sql`函数中当参数groupFlag为PIVOTBY是，参数groupBy持选择多列。(**2.00.1**)
* createReactiveStateEngine新增字段keyPurgeFilter和keyPurgeFreqInSecond，以支持响应式状态引擎（reactive state engine）自动清理key。(**2.00.1**)
* 响应式状态引擎（reactive state engine）支持输出结果到分布式表和流数据表，支持接受来自replay的输入。(**2.00.1**)
* delete语句支持map子句，将delete语句下沉到各分区执行。(**2.00.1**)
* 用户自定义函数的输入参数支持默认值。(**2.00.1**)
* Windows安装包的dolphindb.cfg、controller.cfg、cluster.cfg默认配置项中移除redolog配置参数。(**2.00.1**)

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

> GUI

* GUI画图函数plot多曲线可共享y轴。(**2.00.1**)
