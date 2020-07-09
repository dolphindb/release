# DolphinDB Release Notes

## DolphinDB Server

Version： 1.20.0

Releate Date： 2020-07-08


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.20.0.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.20.0_JIT.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.20.0.zip) |
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.20.0_JIT.zip)



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

 

> Improvments

* Added the optional parameter 'minPeriods' for moving window functions: mmed, mavg, mmin, mmax, mimin, mimax, msum, mstd, mvar, mmad, mmse, mpercentile, mcorr, mcovar, mwsum, mwavg, mbeta.
* Added support for matrix operations for row-wise functions: rowSum, rowSum2, rowAvg, rowCount, rowStd, rowVar, rowMin, rowMax, rowAnd, rowOr, rowXor, rowProdk.
* The 'limit' clause of SQL statements allows the use of variables. 
* Can insert a dictionary into an in-memory table with function `tableInsert`. The keys of the dictionary should contain the column names of the table. The values of the dictionary must be a tuple. 
* Added a new optional parameter 'initFunc' for function `dictUpdate!`. If update operation involves new keys that did not exist in the dictionary to be updated, execute 'initFunc' for these keys.






