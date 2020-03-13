# DolphinDB Release Notes

## DolphinDB Server

Version: 1.01.0

Release date: 2020-01-19


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.0.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.0.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.0_JIT.zip) | 
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.0_JIT.zip) | 


Version: 1.01.1

Release date: 2020-01-30


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.1.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.1.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.1_JIT.zip) | 
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.1_JIT.zip) | 


Version: 1.01.2

Release date: 2020-02-15


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.2.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.2.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.2_JIT.zip) | 
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.2_JIT.zip) | 

Version: 1.01.3

Release date: 2020-02-28

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.3.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.3.zip) | 

Version: 1.01.4

Release date: 2020-03-05

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.4.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.4.zip) | 


> New features

* Support Just-In-Time (JIT) compiling. For details please refer to [DolphinDB Tutorial: Just-in-time (JIT) Compilation](https://github.com/dolphindb/Tutorials_EN/blob/master/jit.md)
* Added function `capacity` to get the capacity of a vector, i.e., the number of elements it can hold based on the current memory allocation for the vector. (**1.01.1**)
* Support 'break' and 'continue' statements in JIT. (**1.01.2**) 
* Added function `keyedTable` to create a keyed table. When appending to a keyed table, if a new row has the same primary key value as an existing row, the existing row will be overwritten with the new row. (**1.01.2**)
* Added 3 new parameters for function `linprog`: 'lb', 'ub' and 'method'. 'lb' represents the lower bound of the variable; 'ub' represents the upper bound of the variable;  'method' represents the optimization algorithm and currently supports 'simplex' and 'interior-point'. (**1.01.3**)

> Improvements

* Dictionaries and sets support the following new key types: UUID, IPADDR and INT128.
* Improved performance of concurrent operations (query and append) on shared in-memory tables. (**1.01.1**)
* Improved the efficiency of vector and matrix memory usage. (**1.01.1**)
* Added checks on the number of rows of a matrix. Now it is not allowed to create a matrix with zero rows. (**1.01.1**)
* Function `createTimeSeriesAggregator` now supports 2 new parameters: 'updateTime' and 'useWindowStartTime'. 'updateTime' can trigger calculations at intervals shorter than those specified by parameter 'step'. 'useWindowStartTime' specifies whether to use the start time or end time of moving windows as the temporal column in the output table. (**1.01.2**)
* Improved deserialization for 'delete' statements by removing the requirement that the 'where' clause of a 'delete' statement must be an expression object. (**1.01.2**)
* Function `getSessionMemoryStat` can now output the IP address and port number of the client. (**1.01.2**)
* Optimized the use of llvm, which significantly improved the performance of JIT. (**1.01.2**)    
* Improved function `loadText`. When importing a text file with only the header row and the schema is specified, an empty table is returned instead of throwing an exception. (**1.01.3**)
* Improved the time-series aggregator for streaming data. If there are NULL values in the temporal column or if there are large gaps between two adjacent timestamps, the performance is not affected. (**1.01.3**)

> Bug fix

* Fixed the bug that certain invalid parameters for function `linprog` would cause system crash. (**1.01.2**)
* Fixed the bug that causes system crash when user-defined functions call function `parseExpr`. (**1.01.2**)
* Fixed a bug of function `loadText`: when format is specified for nanotimestamp data type, a parsing error will occur. (**1.01.3**)
* Fixed an issue of inserting duplicate keys to a keyed table. (**1.01.4**)
* Fixed a crashing bug of calling functions over a symbol-typed grouping column in SQL statements with 4 or more grouping columns.  (**1.01.4**)
* Fixed the false reporting of nonexistent table upon querying an empty dimension table when it is recreated after dropping it. (**1.01.4**)
* Fixed a bug of string vector ingestion, which affects the use of aggregate function (e.g. last) over string or symbol columns in SQL statements with context-by clause. (**1.01.4**)

## DolphinDB orca

* Released [DolphinDB orca](https://github.com/dolphindb/Orca). It implements a pandas API on top of DolphinDB, enabling users to utilize DolphinDB to process and analyze massive amounts of data more conveniently and efficiently in pandas.
* Released DolphinDB NumPy. DolphinDB NumPy functions can work with orca objects more efficiently than NumPy functions. (**1.01.2**)
* Added function `read_shared_table` to read shared stream table in DolphinDB. (**1.01.2**)


