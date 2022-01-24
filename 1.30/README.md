
# DolphinDB Release Notes

## DolphinDB Server

Version: 1.30.16

Release Date: 2022-01-10

[Linux64 binary](https://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.30.16.zip) | 
[Linux64 JIT binary](https://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.30.16_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.30.16_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.com/downloads/DolphinDB_Win64_V1.30.16.zip) |
[Windows64 JIT binary](https://www.dolphindb.com/downloads/DolphinDB_Win64_V1.30.16_JIT.zip)



> New Features

* The type of data written into a temporal column of an in-memory table will be automatically converted to the data type of the column. (**1.30.16**)
* Tables in the same partition can now be updated, written and deleted concurrently. (**1.30.16**)
* Data node can now be recovered online with the latest data from other nodes. You can also enable asynchronous recovery via configuration. (**1.30.16**)
* You can now use a new tag *[HINT_EXPLAIN]* in your SQL statement to return a JSON string indicating the execution process of the statement. (**1.30.16**)
* You can now manage and query all computing tasks in a cluster. (**1.30.16**)
* Added new function `streamEngineParser` to decompose a cross-sectional factor into a pipeline with multiple built-in streaming engines. This function parses the specified metrics to construct a calculation pipeline, where multiple built-in engines process the streaming data in sequence. (**1.30.16**)
* Added new function `existSubscriptionTopic` to check whether a subscription topic has been created. (**1.30.16**)
* Added new function `createLookupJoinEngine` to support left join of a stream table and a table with infrequent data updates. (**1.30.16**)
* Added new function `moveChunksAcrossVolume`. When a new volume is added, use this function to move chunks in the old volume to the new one. (**1.30.16**)
* When a new volume is added, you can now use function `resetDBDirMeta` to move the old volume's meta log to the new one. (**1.30.16**)
* Added 10 new TopN functions, `msumTopN`, `mavgTopN`, `mstdpTopN`, `mstdTopN`, `mvarTopN`, `mvarpTopN`, `mcorrTopN`, `mbetaTopN`, `mcovarTopN`, and `mwsumTopN`. These functions can be used as state functions in the reactive state engine. (**1.30.16**)
* Added new functions `makeKey` and `makeOrderedKey` to combine multiple columns into a BLOB column, so it can be used as the key of a dictionary or a set. (**1.30.16**)
* Added new higher-order function `aggrTopN`, which sorts data based on the specified sorting column and returns aggregate calculation results of the first N rows in the table. (**1.30.16**)
* Added new higher-order functions `window` and `twindow` for more general scenarios than move and tmove, with slightly different handling of window boundaries. (**1.30.16**)
* Added new configuration parameter *raftElectionTick*, which specifies the waiting time to receive a heartbeat from the leader in a raft group before the followers switch to a new leader. Added new functions `setCacheEngineMemSize`, `setTimeoutTick`, `setTSDBCacheEngineSize`, `setMaxMemSize`, `setReservedMemSize` and `setMaxBlockSizeForReservedMemory` to support modifying the associated configuration online. (**1.30.16**)
* Added new function `fixedLengthArrayVector` to combine multiple vectors into an array vector. (**1.30.16**)
* Added new function `loadNpz` to import *.npz* files from NumPy. (**1.30.16**)
* Added new function `suspendRecovery` to suspend node recovery tasks and added `resumeRecovery` to resume recovery tasks. (**1.30.16**)
* Added new functions `rowCorr`, `rowCovar`, `rowBeta`, `rowWsum` and `rowWavg` for row-based calculation. (**1.30.16**)
* Added new function `fflush` to flush buffer data to your file system. (**1.30.16**)

> Improvements

* When updating in-memory tables with assignment statements, you can now use BOOL arrays in row filters. For example, *t[\`y, t[\`y]>0] = 0* where *t* is a table and *y* is a column of *t*. (**1.30.16**)
* New optional parameter *sortColumns* is added to function `upsert!`. Use this parameter to specify the sorting columns based on which the updated table will be sorted.  (**1.30.16**)
* `cancelJob` and `cancelConsoleJob` now support cancelling multiple jobs. Job cancelling is also faster when cluster is stuck. (**1.30.16**)
* Function ``set`` now supports the BLOB data type.  (**1.30.16**)
* Now multiple records with identical key values are not allowed to insert into a keyed stream table in one batch. (**1.30.16**)
* Faster execution speed for using functions `atImin` and `atImax` in widow join parameter *aggs*. (**1.30.16**)
* Added new optional parameter *clean* to the command `run` to control whether to clear the variables in current session. (**1.30.16**)
* The *window* parameter in function `wj` now supports duration types y (year), M (month) and B (business day). (**1.30.16**)
* Function `loadText` now supports strings containing characters with ASCII value 0. (**1.30.16**)
* You can now use conditional assignments on matrices. (**1.30.16**)
* Added a new optional parameter *atomic* to function `loadTextEx`. The default value is "false". When loading a large file, specify this parameter as "false" to split the loading transaction into multiple transactions. (**1.30.16**)
* Added new column *remoteIP* to the return value of functions `getCompletedQueries` and `getRunningQueries`. (**1.30.16**)
* Now you can specify the configuration parameter *stdoutLog* as "2" to print system log to both stdout and the log file. (**1.30.16**)
* The parameter *metrics* in anomaly detection engines can now contain sequence-related functions. (**1.30.16**)
* When the time-series engine parameter *windowSize* is a vector, the elements can take the same values.  (**1.30.16**)
* Cross-sectional engine parameter *keyColumn* now supports vector type. (**1.30.16**)
* Records in tuple form can now be inserted to streaming engines. (**1.30.16**)
* New field *memoryUsed* is added to the return value of function `getStreamEngineStat().CrossSectionalEngine`, indicating the consumned memory of the cross-sectional engine. (**1.30.16**)
* In asof join engines, parameter *metrics* can now include the right table's temporal column. (**1.30.16**)
* Added read-only privilege for shared stream tables. (**1.30.16**)
* Improved stability of controller nodes in high availability clusters. (**1.30.16**)
* Information on delete and update operations can be printed in log. (**1.30.16**)
* Added subscription topic information to the error messages of the stream subscription task in the log. (**1.30.16**) 
* UI enhancements for the Web-Based Cluster Manager. With the integrated user interface, you can now view, suspend and cancel jobs (running, submitted or scheduled) in DolphinDB. Note that after you have upgraded the server version, the "web" folder must be updated as well.
The new version of Web-Based Cluster Manager uses the WebSocket protocol to enhance its support for binary protocols. Your web browser may need to be updated to the latest version. We recommend using the latest version of Chrome or Edge. (**1.30.16**)

> Issues Fixed

* A redo log recovery timeout may occur when a transaction is slowly synchronized to disk, resulting in data loss after the server restarts. (**1.30.16**)
* A data node fails to start and reports the error message "Failed to open public key file. No such file or directory" when starting multiple DolphinDB clusters on one server. (**1.30.16**)
* A scheduled job on a high availability cluster may fail to execute due to authentication failure of the switched leader because the initial UUIDs are different between controllers. (**1.30.16**)
* After a data node crashes, the agent node reboots the offline node every second instead of at specified intervals configured in parameter *datanodeRestartInterval*. (**1.30.16**)  
* When the parameter *jobFunc* of `scheduleJob` contains a SQL update statement and a where clause with functions, the deserialization fails after the system restarts. (**1.30.16**)
* After updating a distributed table, the original physical directories are not recycled if the transaction fails to commit.  (**1.30.16**)
* In a high concurrency scenario, a fully-occupied disk of the redo log may cause deadlock in the redo log recovery thread.  (**1.30.16**)
* If an OOM event occurs when writing to a data node, the node crashes after being stuck for a while instead of reporting the error. (**1.30.16**)  
* The chunk state is wrongly set when a transaction rollback times out, causing persistence failure in the stream table. (**1.30.16**)
* Parameter validation error with function `createCrossSectionalEngine`: When *timeColumn* is specified without setting *useSystemTime* to be true, the error is not raised. (**1.30.16**)
* For a time-series streaming engine, when *useSystemTime* is set to be true and *outputTable* is a distributed table, an exception of data type mismatch may be raised. (**1.30.16**)
* If *delayedTime* is specified in the asof join streaming engine, write operations may lead to server crash. (**1.30.16**)
* When appending more than 65536 rows of records to a high availability stream table twice and rollback occurs, the index.log reports an error "index.log contains invalid data" as two identical indices are written. (**1.30.16**)
* Writing to a time-series streaming engine, daily time-series streaming engine or asof join streaming engine may lead to a server crash on Windows. (**1.30.16**)
* When the subExecutor thread still has tasks in progress, after successfully executing `unsubscribeTable`, `getStreamingStat().subWorkers` still returns the unsubscribed topics. (**1.30.16**)
* Loading a high availability stream table may fail after a node restarts. (**1.30.16**)
* Reconnection fails after switching leaders in the raft groups of the stream table and the subscriber. (**1.30.16**)
* When *triggeringPattern* = 'keyCount' and *triggeringInterval* is a tuple, `createCrossSectionalEngine` returns duplicate results. (**1.30.16**)
* Error "Failed to decompress the vector. Invalid message format" occurs when loading a persisted stream table containing BLOB data. (**1.30.16**)
* Crash occurs when writing BLOB data to a stream table and a single record exceeds 64KB. (**1.30.16**)
* After assigning values to an added column in an in-memory table with `select` statement instead of `exec` statement, the node crashes when loading the table. (**1.30.16**)
* An error "Read only object or object without ownership can't be applied to mutable function readRecord!" occurs when loading binary files with function `readRecord!`. (**1.30.16**)
* The parser may report an error for function calls when the right bracket is not placed on the same line as the left bracket. (**1.30.16**)
* Executing function `replayDS` on a table with array vectors causes a node crash. (**1.30.16**)
* When querying a partitioned table with value domain for the last k rows of records in each group (`context by partitionCol limit -k`), some of the results do not satisfy the where conditions if no eligible data exists in a partition. (**1.30.16**)
* An error "More than one column has the duplicated name" occurs when calling function `rolling` or `moving` in SQL statement without specifying the generated column name. (**1.30.16**)
* NULL values are generated if no data is found in a *step* duration of function `interval`. (**1.30.16**)
* Wrongly-specified parameter *rowKeys* of function `sliceByKey` leads to server crash. (**1.30.16**)
* Null flag is not set after `replace!` a vector with NULL values. (**1.30.16**)