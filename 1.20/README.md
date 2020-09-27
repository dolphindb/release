# DolphinDB Release Notes

## DolphinDB Server

Version： 1.20.0

Releate Date： 2020-07-08


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.20.0.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.20.0_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.20.0.zip) |
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.20.0_JIT.zip)

Version： 1.20.1

Releate Date： 2020-07-20


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.20.1.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.20.1_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.20.1.zip) |
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.20.1_JIT.zip)

Version： 1.20.2

Releate Date： 2020-08-15


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.20.2.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.20.2_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.20.2.zip) |
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.20.2_JIT.zip)

> New Features

* In JIT, the parameters of a function are allowed to be another function (user-defined function, lambda function, partial application or dynamic function).
* JIT supports certain matrix operations, such as access and modification of matrix elements, operations such as matrix generation, merge and transpose, and matrix calculations such as addition, subtraction, multiplication, division and inner product.
* Function `integral` now supports double integrals; function `derivative` now supports higher order derivatives.
* Added statistical function `anova`.
* In SQL queries, serial execution can be implemented with HINT_SEQ; in the `mr` function, serial execution can be implemented with the parameter 'parallel' set to false.
* Functions `loadText`, `ploadText` and `loadTextEx` now support new data types: uuid, ipaddr and int128.
* Added new function `cachedTable` to create a special type of in-memory table: cached table. For example, a cache table can be created in DolphinDB to store data imported from a MySQL database. When querying the cached table, if the length of time since the last update exceeds a specified value, the cached table will be automatically updated.
* The use of functions `wavg`, `wsum` and `beta` in the time-series streaming aggregator is optimized. 
* Now can use subscripts to retrieve elements of a string scalar.
* Added function `randMultivariateNormal` to generate multivariate normal random numbers. 
* Added matrix lower–upper (LU) decomposition function `lu`. (**1.20.1**)
* Added function `mprod` to calculate the product of numbers over a moving window. (**1.20.1**)
* Added function `saveModule` to serialize modules into binary format. Added function `loadModule` and added the configuration parameter 'preloadModules', both of which can be used to pre-load modules or plugins. (**1.20.1**)
* Added regression functions `ridge`, `lasso` and `elasticNet`. (**1.20.1**)
* Added matrix factorization functions `schur`, `svd` and `qr`. (**1.20.2**)
* Added function `indexedTable` to create indexed in-memory tables. Queries on indexed in-memory tables are optimized if the filtering conditions include first key column. (**1.20.2**)
* Added functions `autocorr` and `acf` to calculate autocorrelation. (**1.20.2**)
* Added function `sliceByKey` to quickly access keyed tables and indexed in-memory tables. Compared with SQL statements, `sliceByKey` is faster by about 100%. (**1.20.2**)
* Added function `manova` for multivariate analysis of variance. (**1.20.2**)
* Added command `closeSessions`. It allows an administrator to close one or more specified sessions to release resources. (**1.20.2**)
* Added functions `getChunksMeta` and `getTabletsMeta` to obtain metadata of the partitions (chunks) and partitioned subtables (tablets) on the data node, such as the occupied disk space, the number of rows and the version number of each partition. (**1.20.2**) 

> Improvements

* Added the optional parameter 'minPeriods' for moving window functions: `mmed`,`mavg`,`mmin`,`mmax`,`mimin`,`mimax`,`msum`,`mstd`,`mvar`,`mmad`,`mmse`,`mpercentile`,`mcorr`,`mcovar`,`mwsum`,`mwavg`,`mbeta`.
* Added support for matrix operations for row-wise functions: `rowSum`,`rowSum2`,`rowAvg`,`rowCount`,`rowStd`,`rowVar`,`rowMin`,`rowMax`,`rowAnd`,`rowOr`,`rowXor`,`rowProd`.
* The 'limit' clause of SQL statements allows the use of variables. 
* Can insert a dictionary into an in-memory table with function `tableInsert`. The keys of the dictionary should contain the column names of the table. The values of the dictionary must be a tuple. 
* Added a new optional parameter 'initFunc' for function `dictUpdate!`. If update operation involves new keys that did not exist in the dictionary to be updated, execute 'initFunc' for these keys.
* Matrix inversion based on LU decomposition is used in the calculation of higher order derivatives to improve accuracy. (**1.20.1**)
* The SQL UPDATE statement now requires that the object to be updated must be a table. (**1.20.1**)
* Temporal type conversion functions now support tuple as the input. The functions involved include: `date`, `month`, `year`, `hour`, `minute`, `second`, `time` ,`datetime`,`datehour`,`timestamp`,`nanotime`,`nanotimestamp`,`weekday`,`dayOfWeek`,`dayOfYear`,`dayOfMonth`,`quarterOfYear`,`monthOfYear`,`weekOfYear`,`hourOfDay`,`minuteOfHour`,`secondOfMinute`,`millisecond`,`microsecond`,`nanosecond`. (**1.20.1**)
* Improved the stability of the distributed database. Specifically, improved the stability of transaction resolution when the chunk versions are inconsistent; reduced the chances that heartbeat transmission is delayed. (**1.20.1**)
* The parameter 'groupingCol' of function `contextby` is allowed to be an empty array. (**1.20.1**)
* Use OpenBLAS and LAPACK to improve the performance of the following matrix related functions: `inverse`, `solve`, `det` and `cholesky`. When used on a large matrix, the performance of these functions is improved by 10 to 50 times. (**1.20.2**)
* The function `lu` can decompose a matrix that is not a square matrix. (**1.20.2**)
* Added a label 'partitionTypeName' to the output of function `schema` to describe the partition type. (**1.20.2**)
* Functions `in` and `find` support searching for key values in keyed tables and indexed in-memory tables. (**1.20.2**)
* Added an optional parameter 'sharedName' to function `syncDict`. If it is specified, the dictionary will be shared across all sessions on the node. (**1.20.2**)
* Added 2 columns ('createTime' and 'lastActiveTime') to the output of function `getSessionMemoryStat` to record the session creation time and the last access time respectively. Corrected the value of the column 'remotePort'. (**1.20.2**)
* Added 2 columns ('remoteIP' and 'remotePort') to the output of function `getConsoleJobs`. (**1.20.2**)
* Function `backup` now supports parallel backup to improve efficiency. (**1.20.2**)
* When a constant is assigned to a variable, an object will be copied to avoid the reduction in system efficiency caused by concurrent modification of the reference count during multi-threaded parallel computing. (**1.20.2**)
* Improved the stability of the implementation of the RAFT consensus protocol. (**1.20.2**)
* Used TCMalloc to manage the in-memory pool, which improved in-memory allocation efficiency, especially the allocation efficiency of small in-memory during multi-threaded parallel computing. Meanwhile, two problems were solved, firstly, the situation where the actual memory occupied by DolphinDB exceeds the set value of the configuration parameter maxMemSize, and secondly, the OOM issue where there is still in-memory remaining when creating a string. (**1.20.3**)
* When using the function `saveText`, the maximum precision of a double type variable retains 15 digits. (**1.20.3**)
* Imported an optional parameter 'useSystemTime' in crossSectionalAggregator. When it set to false, the output calculation time is the time of the event itself. This function could better support the playback of historical data for simulation. (**1.20.3**)
* Use the logarithmic form of likelihood when using gaussianNB moudle for classification prediction, that makes it possible to use the model for classification in high-dimensional situations. (**1.20.3**)
* Improved performance of `pca` function as changed to use the svd algorithm of lapack. (**1.20.3**)
* Added parameters 'svdSolver' and 'randomState' to function `pca`. (**1.20.3**)
* Added parameter 'regularizationCoeff' to function `logisticRegression`. (**1.20.3**)
* Added parameter 'parallel' to function `backup` to support parallel backup. (**1.20.3**)
* The configuration parameter 'dfsReplicaReliabilityLevel' now can take the value of 2, which means the replicas are distributed to different machines if resources permit. (**1.20.3**)

> Bug fixes:

* When the data types of the inputs of functions `mmax` and `mmin` are BOOL, CHAR or SHORT and the optional parameter 'minPeriods' is specified, if the first element of the result is expected to be empty, the result does not match the expectation. (**1.20.1**)
* After enabling high availability for the controller node, if a transaction involves too many partitions so the RAFT message length exceeds 64K, the metadata will be truncated when the RAFT message is replayed after restarting the system. (**1.20.1**)
* If a SQL statement has the WHERE clause, and if the GROUP BY clause contains multiple fields, and if the second or a subsequent field in the GROUP BY clause uses function `segment`, the result does not match the expectation. (**1.20.1**)
* When all elements of a vector are identical, the results of functions `mvar` and `cumvar` may have extremely small negative values; the results of functions `mstd` and `cumstd` may have NULL values. (**1.20.2**)
* A memory leak may occur during socket connection. (**1.20.2**)
* Several stability issues of functions `ridge`, `lasso` and `elasticNet` introduced in version 1.20.1. (**1.20.2**)
* Function `adaBoostRegressor` may crash under certain circumstances. (**1.20.2**)
* After a high-availability cluster adds a data node online, creating a new database partition on a new node may cause the new node to crash. (**1.20.2**)
* When using JSON to make web calls, if the tag'functionName' is not specified, the node will crash. This might occur when using grafana to access DolphinDB. (**1.20.3**)
* When the date and time type functions (`date`, `timestamp`, etc.) process a set of strings, if the string does not conform to the date and time type, the corresponding element returns a null value, but the returned vector does not set the flag containing the null value element, which causes the return of `isValid` and `isNull` to be inconsistent with expectations. (**1.20.3**)
* When using `fromJson` function to process JSON strings, if the tag 'value' is not included, the node may crash. (**1.20.3**)
* Fixed a bug in the implementation of snapshot checkpoint of RAFT. This may lead to a particularly long time-consuming leader switching. (**1.20.3**)

#### Plugins

* MySQL

    * Added the requirement that the parameter 'startRow' for MySQL plug-in functions `load` and `loadEx` must be a nonnegative integer. 

#### Client softwares

* Web-based cluster manager

    * After enabling high availability for the controller node, if a re-election of the controller leader occurs, when the user accesses the homepage of the web-based cluster manager, the system checks whether the controller node at the address of the cluster manager is the controller leader. If not, it will display information about the current controller leader. (**1.20.1**)
    * Fixed the problem that data nodes cannot be dynamically loaded after adding data nodes in a high-availability cluster online. (**1.20.2**)
    * When logging onto a follower control node in a high-availability cluster, sometimes the system erroneously return an error message that user name or password is wrong. Now it returns the correct prompt message together with the alias of the current active controller. (**1.20.2**).

* GUI

    * Added links to user manual and GUI help.
    * Column width of the histogram is automatically adjusted based on number of data points on the x-axis.

#### APIs

* Python API and orca

    * Fixed the bug that in the Python API exceptions are thrown when the session method `loadTable` is used to load specified partitions. (**0.1.15.23**)
    * Added support for ipaddr, uuid and int128 data types. (**0.1.15.23**)
    * Added support for arrays of month type. (**0.1.15.23**)
    * Added `hashBucket` function. (**0.1.15.23**)
    * Orca: Fixed the problem of calculation errors in `rolling` function when the input type is float32 with nan values. (**0.1.15.23**)
    * Orca: Fixed the problem of erroneous error message when `read_table` is used to load a distributed table. (**0.1.15.23**)
    * Released version 1.20.2.0 corresponds to DolphinDB 1.20.2; released version 1.10.12.0 corresponds to DolphinDB 1.10.12; 
      released version 1.0.24.1 corresponds to DolphinDB 1.00.24.
    * Added support for python3.8. (**1.20.4.0, 1.10.15.0, 1.0.24.2**)
    * Added native methods for creating DolphinDB databases and partitioned tables. (**1.20.4.0, 1.10.15.0, 1.0.24.2**)


* C++ API

    * Fixed the bug that a process cannot exit normally when subscribing to a stream table from C++ API. (**1.20.2**)
    * Removed the dependency of C++ API dynamic library (libDolphinDBAPI.so) on openssl. (**1.20.2**)
    * Linux C++ API dynamic library added support for D_GLIBCXX_USE_CXX11_ABI=1. (**1.20.2**)

* Java API
    * Added 'Upload' return value deserialization processing, which does not affect the call of the interface. (**1.20.2**)

* C# API

    * Added 'Upload' return value deserialization processing, which does not affect the call of the interface. (**1.20.2**)

* Node.js API

    * Added Node.js API for DolphinDB. (**1.20.2**)
