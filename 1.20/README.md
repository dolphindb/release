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


> Bug fixes:

* When the data types of the inputs of functions `mmax` and `mmin` are BOOL, CHAR or SHORT and the optional parameter 'minPeriods' is specified, if the first element of the result is expected to be empty, the result does not match the expectation. (**1.20.1**)
* After enabling high availability for the controller node, if a transaction involves too many partitions so the RAFT message length exceeds 64K, the metadata will be truncated when the RAFT message is replayed after restarting the system. (**1.20.1**)
* If a SQL statement has the WHERE clause, and if the GROUP BY clause contains multiple fields, and if the second or a subsequent field in the GROUP BY clause uses function `segment`, the result does not match the expectation. (**1.20.1**)


> Web-based cluster manager

* After enabling high availability for the controller node, if a re-election of the controller leader occurs, when the user accesses the homepage of the web-based cluster manager, the system checks whether the controller node at the address of the cluster manager is the controller leader. If not, it will display information about the current controller leader. (**1.20.1**)


> Plugins

* Added the requirement that the parameter 'startRow' for MySQL plug-in functions `load` and `loadEx` must be a nonnegative integer. 



> Python API

* Fixed the bug that in the Python API exceptions are thrown when the session method loadTable is used to load specified partitions.

> C++ API

* Fixed the bug that a process cannot exit normally when subscribing to a stream table from C++ API.
* Removed the dependency of C++ API dynamic library (libDolphinDBAPI.so) on openssl.
* Linux C++ API dynamic library added support for D_GLIBCXX_USE_CXX11_ABI=1.

