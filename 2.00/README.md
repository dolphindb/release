# DolphinDB Release Notes

## DolphinDB Server

Version: 2.00.7 &nbsp;&nbsp;&nbsp; [Compatibility Level 1](./../DolphinDB_compatibility_levels_EN.md#31-compatibility-level-1) with 2.00.6

Release Date: 2022-07-14

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.7.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.7_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.7_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.00.7.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.00.7_JIT.zip)

Version: 2.00.6 &nbsp;&nbsp;&nbsp; [Compatibility Level 2](./../DolphinDB_compatibility_levels_EN.md#32-compatibility-level-2) with 2.00.5

Release Date: 2022-05-09

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.6.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.6_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.6_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.00.6.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.00.6_JIT.zip)

Version: 2.00.5 &nbsp;&nbsp;&nbsp; [Compatibility Level 2](./../DolphinDB_compatibility_levels_EN.md#32-compatibility-level-2) with 2.00.4/1.30.16/1.30.17

Release Date: 2022-03-29

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.5.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.5_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V2.00.5_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.00.5.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V2.00.5_JIT.zip)

Version: 2.00.4

Release Date: 2022-01-10

[Linux64 binary](https://www.dolphindb.com/downloads/DolphinDB_Linux64_V2.00.4.zip) | 
[Linux64 JIT binary](https://www.dolphindb.com/downloads/DolphinDB_Linux64_V2.00.4_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.com/downloads/DolphinDB_Linux64_V2.00.4_ABI.zip) 

Version: 2.0.0

Release Date: 2021-07-31

[Linux64 binary](https://www.dolphindb.com/downloads/DolphinDB_Linux64_V2.0.0.zip) | 
[Linux64 JIT binary](https://www.dolphindb.com/downloads/DolphinDB_Linux64_V2.0.0_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.com/downloads/DolphinDB_Linux64_V2.0.0_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.com/downloads/DolphinDB_Win64_V2.0.0.zip) |
[Windows64 JIT binary](https://www.dolphindb.com/downloads/DolphinDB_Win64_V2.0.0_JIT.zip)


> New Features

- Added new configuration parameters *memLimitOfQueryResult* and *memLimitOfTaskGroupResult* to restrict the memory usage of the intermediate and final results of queries; new function `getQueryStatus` to monitor the memory usage and execution status of the query. (**2.00.7**)
- Added new function `getTSDBCompactionTaskStatus` to check the status of level file compaction tasks in the TSDB engine. (**2.00.7**)
- Added new functions `isPeak` and `isValley` to determine if the current element is the peak/valley of the neighboring elements. (**2.00.7**)
- Added new function `rowAt(X, Y)`. Return the element in each row of *X* based on the index specified by the corresponding element of Y. (**2.00.7**)
- Added new functions `rowImin` and `rowImax` to get the index of the extreme value in each row. (**2.00.7**)
- Added new machine learning function `gmm` to support Gaussian mixture model (GMM) clustering algorithms. (**2.00.7**)
- Added new function `valueChanged` to detect the change between elements by comparing the current element with adjacent elements.  (**2.00.7**)
- Added new functions `msum2` and `tmsum2` to calculate the sum of squares in a sliding window. (**2.00.7**)
- Added new functions `prevState` and `nextState` to find the element with a different state before/after the current element. (Consecutive elements with the same value are considered to be of the same state.)  (**2.00.7**)
- Added new function `getSupportBundle`. Return a file of support bundle containing system configuration and database information. (**2.00.7**)
- Added new functions `topRange` and `lowRange`. For each element in *X*, return the maximum length of a window to the left of *X* where it is the max/min. The functions are also supported in the reactive state engine (`createReactiveStateEngine`). (**2.00.7**)
- Added interpolation functions `spline`, `neville`, `dividedDifference`, and `loess`. (**2.00.7**)
- Added new parameter `cumPositiveStreak` for the reactive state engine (`createReactiveStateEngine`). (**2.00.7**)
- Added new streaming engine dual ownership reactive state engine (`createDualOwnershipReactiveStateEngine`) with support for parallel computing of data with 2 grouping methods and different metrics. (**2.00.7**)
- Introduced new table object “IPCInMemoryTable“, interprocess in-memory table. Added related functions `createIPCInMemoryTable`, `loadIPCInMemoryTable`, `dropIPCInMemoryTable` and `readIPCInMemoryTable`. Interprocess in-memory table can be used in streaming scenarios to enable efficient data transfer between the DolphinDB server and client on the same machine. (**2.00.7**)
- Added new function `stretch` to stretch a vector evenly to the specified length. (**2.00.7**)
- Added new function `getTransactionStatus` to get the status of transactions. Added new command `imtForceGCRedolog` to skip the garbage collection of a transaction with the specified ID. (**2.00.7**)
- Added new module "ops" for database operations. This module contains some commonly-used scripts for operations such as cancelling unfinished jobs in the cluster, viewing disk usage of a DFS table, deleting recovering partitions, closing inactive sessions, etc. (**2.00.7**)
- Added new function `setLogLevel` to dynamically adjust the log level on the current node. (**2.00.7**)
* Added new function `cells` to retrieve multiple cells from a matrix by the specified row and col indices. (**2.00.6**)
* Added new function `randDiscrete` for sampling from a discrete probability distribution. (**2.00.6**)
* Added new functions `dynamicGroupCumsum` and `dynamicGroupCumcount`, and their state functions in the reactive state streaming engine. (**2.00.6**)
* Added new function `getTSDBCompactionTaskStatus` to get the status of level file compaction tasks of the TSDB engine. (**2.00.6**)
* Added new function `createDistributedInMemoryTable` to create a distributed in-memory table. (**2.00.6**)
* Support tiered storage to store cold data on slow hard disks or object storage (Amazon S3). These data are read-only. (**2.00.6**)
* Added new parameter *sortKeyMappingFunction* to function `createPartitionedTable` in the TSDB engine to apply mapping functions to the sortKey for optimal performance. (**2.00.6**)
* Optimized the update performance in the TSDB engine. (**2.00.6**)
* Added new function `toCharArray` to split a string into a vector of characters. (**2.00.6**)
* Added new configuration parameter *maxDynamicLocalExecutor* to specify the maximum number of dynamically-generated local executors and the frequency at which they are generated. (**2.00.6**)
* Added `transaction` statement to encapsulate multiple SQL statements on an in-memory table or a shared table into one transaction. (**2.00.6**)
* Support asynchronous data sorting in the TSDB cache engine. Specify the configuration parameter *TSDBAsyncSortingWorkerNum* as the number of threads for asynchronous sorting, and the default value is 1. (**2.00.5**)
* Snapshot isolation is supported in the TSDB engine. (**2.00.5**)
* The TSDB engine can be used on Windows. (**2.00.5**)
* You can enable dataSync for the OLAP engine by setting configuration parameter *dataSync* = 1 on Windows. (**2.00.5**)
* Added new parameters *userId* and *password* to function `subscribeTable`. The system will attempt to log in after a user is logged out accidentally to make sure the subscribed data can be written to a DFS table. (**2.00.5**)
* You can specify a function returning array vector for the parameter *metrics* of the reactive state streaming engine (`createReactiveStateEngine`). (**2.00.5**)
* Function `getStreamingStat().subWorkers` returns throttle in milliseconds. (**2.00.5**)
* You can specify multiple matching columns for the asof join engine. (**2.00.5**)
* Added new parameters *snapshotDir* and *snapshotIntervalInMsgCount* to the cross-sectional streaming engine to enable snapshot; Added new parameter *raftGroup* to enable high availability. (**2.00.5**)
* Added new functions `getLeftStream` and `getRightStream` to support cascade of join engines. (**2.00.5**)
* If a function with multiple returns is specified for the parameter *metrics* of a cross-sectional streaming engine (`createCrossSectionalEngine`) or a time-series streaming engine (`createTimeSeriesEngine`), the returned column names can be unspecified when creating the streaming engine. (**2.00.5**)
* Added new command `addAccessControl` to add access control on a shared in-memory table (stream table included) or the streaming engine object. (**2.00.5**)
* When applying an aggregate function, such as `quantile`, to a column in a table, if the data type of the column is not supported, the result is a NULL value. (**2.00.5**)
* The SQL `pivot by` clause supports columns of UUID type. (**2.00.5**)
* The upper limit of the result of function `ceil` or `floor` is raised to 2^53. (**2.00.5**)
* If the last column of a `pivot by` clause is a partitioning column, and no aggregate or order-sensitive functions are included in the `select` clause, the performance has been optimized by nearly five times. (**2.00.5**)
* Function `med`, `kama` and `wma` now support vectors of BOOL type. (**2.00.5**)
* The parameter *colNames* of command `addColumn` can start with a digit. (**2.00.5**)
* When loading a csv file with function `loadText` or `loadTextEx`,  the upper limit for the first row of data is raised to 256 KB. (**2.00.5**)
* Aggregate functions, window functions and vectorized functions support table as an input. (**2.00.5**)
* The parameter *count* of function `rand` or `normal` supports a pair to specify the dimension of a matrix. (**2.00.5**)
* Row-based logic functions (`rowAnd`, `rowOr` and `rowXor`) support input of INT type. (**2.00.5**)
* Added new parameter *arrayDelimiter* to functions `loadText` and `loadTextEx` to load csv files containing array vectors. (**2.00.5**)
* Added new parameter *closed* to function `bar` to specify whether the left or right boundary is inclusive in each group. (**2.00.5**)
* For a moving function, when *X* is an indexed series or an indexed matrix and *window* is a positive integer, the window slides over the index. (**2.00.5**)
* The parameters of a user-defined function can be defined across multiple lines and separated by a comma. (**2.00.5**)
* For a SQL `order by` clause, you can refer to a column by its name or the `as` alias. (**2.00.5**)
* You can now specify a vector of SECOND, TIME or NANOTIME type for the parameter *X* of function `dailyAlignedBar`. (**2.00.5**)
* The server can transfer tables containing array vectors to Python API in pickle format. (**2.00.5**)
* Added new parameter *forceTriggerSessionEndTime* to the daily time-series streaming engine to specify the waiting time to trigger calculation in the window containing *sessionEnd*. (**2.00.5**)
* Modified the parameter *forceTriggerTime* of the daily time-series streaming engine and the time-series streaming engine. The calculation in an uncompleted window of a group can be triggered by the latest ingested data of any other group. If the parameter *fill* is set, the specified filling methods are used to fill the results of the empty windows in the meantime. (**2.00.5**)
* Tables in the same partition can now be updated, written and deleted concurrently. (**2.00.4**)
* The type of data written into a temporal column of an in-memory table will be automatically converted to the data type of the column. (**2.00.4**)
* Data node can now be recovered online with the latest data from other nodes. You can also enable asynchronous recovery via configuration. (**2.00.4**)
* You can now manage and query all computing tasks in a cluster. (**2.00.4**)
* In-memory tables and stream tables now support data type BLOB. (**2.00.4**)
* You can now use a new tag [HINT_EXPLAIN] in your SQL statement to return a JSON string indicating the execution process of the statement. (**2.00.4**)
* Added new function `streamEngineParser` to decompose a cross-sectional factor into a pipeline with multiple built-in streaming engines. This function parses the specified metrics to construct a calculation pipeline, where multiple built-in engines process the streaming data in sequence. (**2.00.4**)
* Added new function `existSubscriptionTopic` to check whether a subscription topic has been created. (**2.00.4**)
* Added new function `createLookupJoinEngine` to support left join of a stream table and a table with infrequent data updates.  (**2.00.4**)
* Added new function `moveChunksAcrossVolume`. When a new volume is added, use this function to move chunks in the old volume to the new one.  (**2.00.4**)
* When a new volume is added, you can now use function `resetDBDirMeta` to move the old volume's meta log to the new one.  (**2.00.4**)
* Added 10 new TopN functions, `msumTopN`, `mavgTopN`, `mstdpTopN`, `mstdTopN`, `mvarTopN`, `mvarpTopN`, `mcorrTopN`, `mbetaTopN`, `mcovarTopN`, and `mwsumTopN`. These functions can be used as state functions in the reactive state engine. (**2.00.4**)
* Added new functions `makeKey` and `makeOrderedKey` to combine multiple columns into a BLOB column, so it can be used as the key of a dictionary or a set. (**2.00.4**)
* Added new higher-order function `aggrTopN`, which sorts data based on the specified sorting column and returns aggregate calculation results of the first N rows in the table. (**2.00.4**)
* Added new higher-order functions `window` and `twindow` for more general scenarios than `move` and `tmove`, with slightly different handling of window boundaries. (**2.00.4**)
* Added new configuration parameter *raftElectionTick*, which specifies the waiting time to receive a heartbeat from the leader in a raft group before the followers switch to a new leader. Added new functions `setCacheEngineMemSize`, `setTimeoutTick`, `setTSDBCacheEngineSize`, `setMaxMemSize`, `setReservedMemSize` and `setMaxBlockSizeForReservedMemory` to support modifying the associated configuration online. (**2.00.4**)
* Added new function `fixedLengthArrayVector` to combine multiple vectors into an array vector. (**2.00.4**)
* Added new function `loadNpz` to import *.npz* files from NumPy. (**2.00.4**)
* Added new function `suspendRecovery` to suspend node recovery tasks and added `resumeRecovery` to resume recovery tasks. (**2.00.4**)
* Added new functions `rowCorr`, `rowCovar`, `rowBeta`, `rowWsum` and `rowWavg` for row-based calculation. (**2.00.4**)
* Added new functions `movingWindowIndex` and `movingTopNIndex` to obtain index of the elements in a moving window. The result is an array vector of INDEX[] type. (**2.00.4**)
* Added new function `fflush` to flush buffer data to your file system. (**2.00.4**)
* Released the TSDB storage engine. The `database` function provides an optional parameter engineType, the default value is OLAP, which is the old storage engine. If you create a database based on the TSDB storage engine, set the engineType to TSDB. (**2.00.0**)
* The data based on the TSDB storage engine supports the new data type BLOB. (**2.00.0**)

> Improvements

- `getClusterPerf(true)` returns the information on all controllers in a high-availability cluster. This function also adds a return value *isLeader* to indicate whether the controller is the leader of the raft group. (**2.00.7**)
- Now when connecting to a controller of a high-availability cluster on the web-based cluster manager, you will be redirected to the leader where information on all nodes are displayed. (**2.00.7**)
- When using function `restore`, `loadBackup`, or `getBackupMeta` to access the backup partitions in a database whose chunk granularity is at TABLE level, the physical index is no longer required when specifying the parameter *partition*. (**2.00.7**)
- Function `getRecoveryTaskStatus` adds a new return value *FailureReason* to display the reason for the recovery task failure. (**2.00.7**)
- Optimized the compression algorithm for `backup`. (**2.00.7**)
- If a *jobId* does not exist when using `cancelJob`, the system no longer throws an exception. Instead, it outputs the error message with the *jobId* to the log. (**2.00.7**)
- Now can specify the configuration parameter *persistenWorkerNum* for a high-availability stream table. (**2.00.7**)
- Added new parameter *forceTriggerTime* to `createSessionWindowEngine` to trigger the calculation in the last window if *useSystemTime*=false. (**2.00.7**)
- When processing standard stream tables with `streamFilter`, you can now specify metacode of Boolean expressions for the filter condition. (**2.00.7**)
- You can include the time column and/or join column from the left or right table as the output column(s) in the the parameter *metrics* of functions `createEqualJoinEngine`, `createAsofJoinEngine` and `createLookupJoinEngine`. (**2.00.7**)
- `replay` supports heterogeneous stream tables with columns of array vectors. (**2.00.7**)
- The parameter *keyPurgeFilter* of `createReactiveStateEngine` must be metacode of Boolean expressions, otherwise an error will be raised. (**2.00.7**)
- The parameter *metrics* of `createLookupJoinEngine` can be a tuple. (**2.00.7**)
- Optimized the performance of `select count(*)` when the time granularity of a `group by` clause is more coarse-grained than that of a partition. (**2.00.7**)
- Optimized the performance of querying the latest n records sorted in descending order with the `top` or `limit` clause. (**2.00.7**)
- Optimized the performance of the following functions when calling function `rolling`: `cumsum`, `cummax`, `cummin`, `cumprod`, and `mcount`. (**2.00.7**)
- tar.gz file for offline server installation. (**2.00.7**)
- Renamed the following configuration parameters and functions for the OLAP storage engine and the original names are used as aliases: *chunkCacheEngineMemSize* to *OLAPCacheEngineSize*, `purgeCacheEngine` to `flushOLAPCache`, `setCacheEngineMemSize` to `setOLAPCacheEngineSize`, and `getCacheEngineMemSize` to `getOLAPCacheEngineSize`. (**2.00.7**)
- Optimized the query performance by 2 times when the `context by` clause specifies a partitioning column. (**2.00.7**)
- Added configuration parameter *enableDropPartitionSchema* to delete the corresponding partitionSchema returned by function `schema` after calling `dropPartition`. (**2.00.7**)
- A subscription starts from the latest incoming data if the persisted offset cannot be found. (**2.00.7**)
- You can specify 00:00:00 for the parameter *sessionEnd* of function `createDailyTimeSeriesEngine` to indicate the end time is 00:00:00 of the next day (i.e., 24:00:00 of the day). (**2.00.7**)
- Function `trueRange` can be used as state function in the reactive state engine. (**2.00.7**)
* Optimized the performance of `select count(*)` on a table in the TSDB database. (**2.00.6**)
* Reduced the time to load the index of the TSDB storage engine. (**2.00.6**)
* Improved the performance of writing and reading SYMBOL type of data. (**2.00.6**)
* The window functions `cummed` and `cumpercentile` can now be used as state functions in the reactive state streaming engine (`createReactiveStateEngine`). (**2.00.6**)
* Added new parameter *closed* to time-series streaming engines (`createTimeSeriesEngine` and `createDailyTimeSeriesEngine`) to specify whether the left boundary or right boundary of the calculation window is inclusive. (**2.00.6**)
* The *keyColumn* parameter of `streamEngineParser` is now case-insensitive. (**2.00.6**)
* Added new parameter *keyPurgeFreqInSec* to time-series streaming engines (`createTimeSeriesEngine` and `createDailyTimeSeriesEngine`) to remove groups with no incoming data for a long time. (**2.00.6**)
* Optimized the performance for using user-defined functions in time-series streaming engines (`createTimeSeriesEngine` and `createDailyTimeSeriesEngine`). (**2.00.6**)
* `streamFilter` now supports processing columns of standard stream tables. Previously it only processes the output of heterogeneous `replay()`. (**2.00.6**)
* The *metrics* parameter of `createTimeSeriesEngine` and `createDailyTimeSeriesEngine` now supports matrices. (**2.00.6**)
* Now support queries where (1) the `group by` columns are not the partitioning columns, and (2) order-sensitive functions are applied to the queried columns. (**2.00.6**)
* The rule parameter of `resample` now supports "H", "L", "U", "min", "N", and "S". Added new parameters *closed*, *label*, and *origin* to set the interval of groups. (**2.00.6**)
* Function `byRow` now supports the array vector. (**2.00.6**)
* If an error is raised during the execution of the `replay` function, a runtime exception will be thrown. (**2.00.6**)
* Function `matrix` can convert a fixed length array vector to a matrix. (**2.00.6**)
* Optimized the performance of generating random integers. (**2.00.6**)
* The performance of querying the latest records of a certain column with TSDB engine is improved by up to hundreds of times. (**2.00.4**)
* Improved query performance of *top* clause in TSDB engine. (**2.00.4**)
* Improved performance of accessing precomputed data in TSDB engine. (**2.00.4**)
* When updating in-memory tables with assignment statements, you can now use BOOL arrays in row filters. For example, *t[`y, t[`y]>0] = 0* where *t* is a table and *y* is a column of *t*. (**2.00.4**)
* New optional parameter *sortColumns* is added to function `upsert!`. Use this parameter to specify the sorting columns based on which the updated table will be sorted. (**2.00.4**)
* `cancelJob` and `cancelConsoleJob` now support cancelling multiple jobs. Job cancelling is also faster when cluster is stuck. (**2.00.4**)
* The parameter *schema* in function `loadText` now supports array vector. (**2.00.4**)
* Function `set` now supports the BLOB data type. (**2.00.4**)
* Now multiple records with identical key values are not allowed to insert into a keyed stream table in one batch. (**2.00.4**)
* Faster execution speed for using functions `atImin` and `atImax` in widow join parameter *aggs*. (**2.00.4**)
* Added new optional parameter *clean* to the command `run` to control whether to clear the variables in current session. (**2.00.4**)
* The *window* parameter in function `wj` now supports duration types *y* (year), *M* (month) and *B* (business day). (**2.00.4**)
* Function `loadText` now supports strings containing characters with ASCII value 0. (**2.00.4**)
* You can now use conditional assignments on matrices. (**2.00.4**)
* Added a new optional parameter *atomic* to function `loadTextEx`. The default value is "false". When loading a large file, specify this parameter as "false" to split the loading transaction into multiple transactions. (**2.00.4**)
* Added new column *remoteIP* to the return value of functions `getCompletedQueries` and `getRunningQueries`. (**2.00.4**)
* Now you can specify the configuration parameter *stdoutLog* as "2" to print system log to both stdout and the log file. (**2.00.4**)
* The parameter *metrics* in anomaly detection engines can now contain sequence-related functions. (**2.00.4**)
* When the time-series engine parameter *windowSize* is a vector, the elements can take the same values. (**2.00.4**)
* Cross-sectional engine parameter *keyColumn* now supports vector type. (**2.00.4**)
* Records in tuple form can now be inserted to streaming engines. (**2.00.4**)
* New field *memoryUsed* is added to the return value of function `getStreamEngineStat().CrossSectionalEngine`, indicating the consumned memory of the cross-sectional engine. (**2.00.4**)
* In asof join engines, parameter *metrics* can now include the right table's temporal column. (**2.00.4**)
* Added read-only privilege for shared stream tables. (**2.00.4**)
* Improved stability of controller nodes in high availability clusters. (**2.00.4**)
* Information on delete and update operations can be printed in log. (**2.00.4**)
* Added subscription topic information to the error messages of the stream subscription task in the log. (**2.00.4**)
* UI enhancements for the Web-Based Cluster Manager. With the integrated user interface, you can now view, suspend and cancel jobs (running, submitted or scheduled) in DolphinDB. Note that after you have upgraded the server version, the "web" folder must be updated as well. The new version of Web-Based Cluster Manager uses the WebSocket protocol to enhance its support for binary protocols. Your web browser may need to be updated to the latest version. We recommend using the latest version of Chrome or Edge.  (**2.00.4**)

> Issues Fixed

* An OOM error caused by concurrent writes, queries or calculations may lead to a server hang-up. (**2.00.6**)
* If data deduplication is enabled in the TSDB engine, when writes and reads are conducted at the same time, the result may be incorrect. (**2.00.6**)
* When writes and reads are conducted in the OLAP engine at the same time, the result may be incorrect. (**2.00.6**)
* A query using `exec` with `limit 1` in the TSDB engine returns a table rather than a vector. (**2.00.6**)
* When writing to an OLAP cache engine, if an exception other than OOM occurs, the system will repeatedly attempt to rewrite, which leads to a server hang-up. (**2.00.6**)
* If a data node is started via the web interface or a cluster is restarted repeatedly, defunct processes are generated. (**2.00.6**)
* If `moveReplicas` is called after executing `suspendRecovery`, it fails to move some of the chunks. (**2.00.6**)
* If a cluster is rebooted after submitting concurrent tasks, some chunks are always in the status of RECOVERING. (**2.00.6**)
* If `delete` is used to delete large amount of data, incorrect information may be written to the checkpoint file, which causes a node to crash and cannot be restarted. (**2.00.6**)
* If snapshot is enabled in the reactive state streaming engine, resubscription to a table with different metrics causes a server crash. (**2.00.6**)
* Appending a single record to the lookup join engine may cause a server crash. (**2.00.6**)
* If the data written to a high-availability stream table are in different schema, they can still enter the persistent queue, and the error “Can't find the object with name” is reported after a leader switch. (**2.00.6**)
* If the parameter *fill* is specified for `createDailyTimeSeriesEngine`, the result of date without data is filled. (**2.00.6**)
* A non-admin user can use function `createUser`. (**2.00.6**)
* The command `changePwd` does not limit the length of the new password. (**2.00.6**)
* If an array vector takes up large amount of memory but does not reach warningMemSize, an OOM error is raised. (**2.00.6**)
* `matrix([],[])` leads to a server crash. (**2.00.6**)
* When using `exec` with `pivot by`, if no function is used on the `exec` column, the statement will generate a table, rather than a matrix. (**2.00.6**)
* If numJobs > 1 or numJobs = -1 is set in function `randomForestClassifier` for concurrent jobs, a repeated use of dataSource leads to a server crash. (**2.00.6**)
* If the parameter duration of function `interval` has different precision with that of the parameter X, a crash occurs. (**2.00.6**)
* When creating an in-memory keyed table with `keyedTable(keyColumns, table)`, if the keyColumns in the table have duplicate values, a memory leak occurs. (**2.00.6**)
* For moving functions that can be used on matrices, such as `mcorr` and `mwavg`, when calculating on indexed matrices, the label column may be lost in the result. (**2.00.6**)
* Function `LoadTextEx` does not report an error when an exception of data loading occurs since 2.00.4. (**2.00.6**)
* A redo log recovery timeout may occur when a transaction is slowly synchronized to disk, resulting in data loss after the server restarts. (**2.00.4**)
* A data node fails to start and reports the error message "Failed to open public key file. No such file or directory" when starting multiple DolphinDB clusters on one server. (**2.00.4**)
* A scheduled job on a high availability cluster may fail to execute due to authentication failure of the switched leader because the initial UUIDs are different between controllers. (**2.00.4**)
* After a data node crashes, the agent node reboots the offline node every second instead of at specified intervals configured in parameter *datanodeRestartInterval*. (**2.00.4**)  
* When the parameter *jobFunc* of `scheduleJob` contains a SQL update statement and a where clause with functions, the deserialization fails after the system restarts. (**2.00.4**)
* After updating a distributed table, the original physical directories are not recycled if the transaction fails to commit.  (**2.00.4**)
* In a high concurrency scenario, a fully-occupied disk of the redo log may cause deadlock in the redo log recovery thread.  (**2.00.4**)
* If an OOM event occurs when writing to a data node, the node crashes after being stuck for a while instead of reporting the error. (**2.00.4**)  
* For a table partitioned by *timeCol* with more than 2 *sortColumns* (where the *timeCol* is the last column), the TSDB engine may crash when querying the table to obtain the first k rows of records grouped by *sortColumns* and sorted by *timeCol* (`context by sortColumns csort timeCol limit k`). (**2.00.4**) 
* When conducting concurrent modifications to the edit log in the TSDB engine, the data node fails to restart. (**2.00.4**)
* The chunk state is wrongly set when a transaction rollback times out, causing persistence failure in the stream table. (**2.00.4**)
* Parameter validation error with function `createCrossSectionalEngine`: When *timeColumn* is specified without setting *useSystemTime* to be true, the error is not raised. (**2.00.4**)  
* For a time-series streaming engine, when *useSystemTime* is set to be true and *outputTable* is a distributed table, an exception of data type mismatch may be raised. (**2.00.4**)
* If *delayedTime* is specified in the asof join streaming engine, write operations may lead to server crash. (**2.00.4**)
* When appending more than 65536 rows of records to a high availability stream table twice and rollback occurs, the index.log reports an error "index.log contains invalid data" as two identical indices are written. (**2.00.4**)
* Writing to a time-series streaming engine, daily time-series streaming engine or asof join streaming engine may lead to a server crash on Windows. (**2.00.4**)
* When the subExecutor thread still has tasks in progress, after successfully executing `unsubscribeTable`, `getStreamingStat().subWorkers` still returns the unsubscribed topics. (**2.00.4**)
* Loading a high availability stream table may fail after a node restarts. (**2.00.4**)
* Reconnection fails after switching leaders in the raft groups of the stream table and the subscriber. (**2.00.4**)
* When *triggeringPattern* = 'keyCount' and *triggeringInterval* is a tuple, `createCrossSectionalEngine` returns duplicate results. (**2.00.4**)
* Error "Failed to decompress the vector. Invalid message format" occurs when loading a persisted stream table containing BLOB data. (**2.00.4**)
* Crash occurs when writing BLOB data to a stream table and a single record exceeds 64KB. (**2.00.4**)
* After assigning values to an added column in an in-memory table with `select` statement instead of `exec` statement, the node crashes when loading the table. (**2.00.4**)
* When accessing an in-memory table with array vectors via GUI, the session is disconnected from the server. (**2.00.4**)
* An error "Read only object or object without ownership can't be applied to mutable function readRecord!" occurs when loading binary files with function `readRecord!`. (**2.00.4**)
* The parser may report an error for function calls when the right bracket is not placed on the same line as the left bracket. (**2.00.4**)
* Executing function `replayDS` on a table with array vectors causes a node crash. (**2.00.4**)
* When querying a partitioned table with value domain for the last k rows of records in each group (`context by partitionCol limit -k`), some of the results do not satisfy the where conditions if no eligible data exists in a partition. (**2.00.4**)
* An error "More than one column has the duplicated name" occurs when calling function `rolling` or `moving` in SQL statement without specifying the generated column name. (**2.00.4**)
* NULL values are generated if no data is found in a *step* duration of function `interval`. (**2.00.4**)
* Wrongly-specified parameter *rowKeys* of function `sliceByKey` leads to server crash. (**2.00.4**)
* Null flag is not set after `replace!` a vector with NULL values. (**2.00.4**)
