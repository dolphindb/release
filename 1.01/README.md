# DolphinDB Release Notes

## DolphinDB Server

Version: 1.01.0

Release date: 2020-1-19


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.0.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.0.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.0_JIT.zip) | 
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.0_JIT.zip) | 


Version: 1.01.1

Release date: 2020-1-30


[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.1.zip) | 
[Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.1.zip) | 
[Linux64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V1.01.1_JIT.zip) | 
[Windows64 JIT binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V1.01.1_JIT.zip) | 


> New features

* Support Just-In-Time (JIT) compiling. 
* Added function `capacity` to get the capacity of a vector, i.e. the number of elements it can hold based on the current memory allocation. (**1.01.1**)

> Improvements

* Dictionaries and sets support the following new key types: UUID, IPADDR and INT128.
*  Improved performance of concurrent operations (query and append) on shared in-memory tables. (**1.01.1**)
*  Improved the efficiency of vector and matrix memory usage. (**1.01.1**)
*  Added checks on the number of rows of a matrix. Now it is not allowed to create a matrix with zero rows. (**1.01.1**)


## DolphinDB Orca

* Released [DolphinDB Orca](https://github.com/dolphindb/Orca) project. It implements a pandas API on DolphinDB, enabling users to process and analyze massive amounts of data more conveniently and efficiently.



