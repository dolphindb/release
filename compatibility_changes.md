# Compatibility Changes

This file provides an overview of the new features and changes (including updates to match industry standards) in version 1.30.22/2.00.10 that may impact your existing scripts and configurations. 

Please review the file carefully to understand how your current setup may be affected by upgrading to this version.

- [Version 2.00.10.2](#version-200102)
- [Version 2.00.10.1](#version-200101)
- [Version 2.00.10](#version-20010)
- [Version 1.30.22.2](#version-130222)
- [Version 1.30.22.1](#version-130221)
- [Version 1.30.22](#version-13022)

## Version 2.00.10.2

### Changes Made to Match Industry Practices or SQL Standards

- Removed function `getClusterReplicationMetrics`. Added function `getSlaveReplicationQueueStatus` as an inheritance of `getClusterReplicationMetrics`.

- When calling function `toStdJson`:
  - For Boolean values, previous versions returned 1 and 0, but now returns true and false.
  - For NULL values, previous versions only converted Integral, Floating and Boolean NULL values to JSON null, other types were converted to "". Now NULL values of all types except STRING are converted to null.

### System Impacts Caused by Bug Fixes

- The `license` function now returns the license information in memory by default, instead of that from the .lic file as in previous versions.

## Version 2.00.10.1

### Changes Made to Match Industry Practices or SQL Standards

- Changed the behaviors of the `join`, `join!` and `append!` functions when merging two tuples.

    ```
    a =  [[1,2],[3,4]]
    b = [[5,6],[7,8]]
    a.join(b)
    //Output (previous versions): ([1,2],[3,4],([5,6],[7,8]))
    //Output (since this version): ([1,2],[3,4],[5,6],[7,8])
    
    a.join!(b)
    a
    //Output (previous versions):([1,2],[3,4],([5,6],[7,8]))
    //Output (since this version): ([1,2],[3,4],[5,6],[7,8])
    
    a.append!(b)
    a
    //Output (previous versions):([1,2],[3,4],([5,6],[7,8]))
    //Output (since this version): ([1,2],[3,4],[5,6],[7,8])
  ```

### System Impacts Caused by Bug Fixes

- When the *triggeringPattern* parameter of `streamEngineParser` is set to ‘keyCount', the *keepOrder* parameter now must be set to true. Setting *triggeringPattern* = 'keyCount’ with *keepOrder* = false raises an error.

- When using the `accumulate` higher-order function in the *metrics* parameter of `createReactiveStateEngine`, the *consistent* parameter of `accumulate` can no longer be set to false. 

## Version 2.00.10

### Changes Made to Match Industry Practices or SQL Standards

- Sharing the same stream table multiple times using the `share` function/statement or `enableTableShareAndPersistence` function will now result in an error.

    ```
    n=10000;
    t=streamTable(2020.01.01T00:00:00 + 0..(n-1) as timestamp, rand(`IBM`MS`APPL`AMZN,n) as symbol, rand(10.0, n) as value)
    share t as t1
    share t as t2 
    //In previous versions, the script above can be successfully executed.
    //Since this version, the second share operation would raise the error: This stream has already been shared as 't1'.
    //This change applies not only to the "share" statement, but also the share() and enableTableShareAndPersistence() functions.
    ```

    To re-share a stream table, it must first be unshared.

- Sum of a DECIMAL64 column has been changed from DECIMAL64 to DECIMAL128 even when the sum does not overflow the DECIMAL64 range.

    ```
    d1=decimal64(10015.555 514796.1186,3)
    re=sum(d1)
    typestr(re)  
    //Previous versions would return DECIMAL64 whereas the current version returns DECIMAL128
    ```

- Validation for appending data to stream tables has been enhanced.<br/>

    Previously, it was possible to append data with an older schema (fewer columns) to a stream table after the schema had been modified to add new columns. This is no longer allowed.

    ```
    t = streamTable(1:0, `id`val, [INT, INT])
    enableTableShareAndPersistence(t, `st)
    go
    data1 = table(1..10 as id, 11..20 as val)
    t.append!(data1)
    addColumn(st, `price, DOUBLE)
    t.append!(data1)
    data2 = table(1..10 as id, 11..20 as val, 21..30 as price)
    t.append!(data2)
    t.append!(data1)
    //Since this version, the script above will raise the error: The number of columns of the table to insert must be the same as that of the original table.
    //In previous versions, the script above can be successfully executed.
    ```

- In previous versions, when casting SYMBOL or STRING values to DECIMAL type, the values were truncated from the scale position. Since this version, the values are first rounded to the scale position then truncated.

    ```
    symbol(["1.34", "4.5677"])$DECIMAL32(2)
    //Output (previous versions): [1.34, 4.56]
    //Output (since this version): [1.34, 4.57]
    ```

- Added parameter validations for user-defined functions which can only take scalars or regular arrays. Dictionaries, function definitions or tuples are no longer allowed.

- Modified the return value of function `avg`: If the input argument is of STRING type, a NULL value is now returned. An exception was raised in previous versions.

- The behavior of `SELECT * FROM a JOIN b` statements has been changed to match standard SQL semantics:

    - If an ON condition is not specified, a cross join will be performed between a and b;

    - If an ON condition is specified, an inner join will be performed between a and b.

    Since this version, if "join" is used in a SQL FROM clause, it is treated as a table join keyword instead of function `join`.

    ```
    select * from a join b
    //In previous versions, the above statement is equivalent to "select * from join(a, b)"
    //Since this version, it is equivalent to "select * from cj(a, b)"
    ```

- Columns used in JOIN conditions can no longer be of BLOB data type. This behavior matches standard SQL semantics.

    Added error message: "Key must be integer, date/time, or string."

- Join (including left join, left semi join, right join, equi join and full join) behavior for NULL values has been updated to match standard SQL semantics.

    In previous versions, NULL values in join columns would be matched between the two joined tables. Since this version, NULL values will not be matched when joining.

- For the table returned by RIGHT JOIN:

  - In previous versions, the columns of right table were placed before those of the left table.

  - Since this version, columns from left table are listed first.

- When joining two tables with RIGHT JOIN, if the qualifier is not specified for a column existing in both tables, it is treated as the column from the table where it first appears (from left to right).

    ```
    t1 = table(1..10 as id, 11..20 as val1)
    t2 = table(6..15 as id, 21..30 as val2)
    select avg(val1+val2) from t1 right join t2 on t1.id=t2.id group by id

    // In previous versions, it was equivalent to select avg(val1+val2) from t1 right join t2 on t1.id=t2.id group by t2.id
    // Since this version, it is equivalent to select avg(val1+val2) from t1 right join t2 on t1.id=t2.id group by t1.id
    ```

    When joining multiple tables, the qualifier must be specified for a column existing in multiple tables. This behavior matches standard SQL semantics.

- When a temporal scalar is used after the `in` predicate in a SQL statement, elements of the condition column are no longer matched with the scalar. Instead, the scalar is treated as a one-element vector to check if the elements of the condition column are contained in that vector.

    ```
    vec = [2012.01.01T00:00:00, 2012.01.01T23:59:59, 2012.01.10T00:00:00, 2012.01.10T23:59:59, 2012.01.31T00:00:00, 2012.01.31T23:59:59, 2012.02.01T00:00:00, 2012.02.01T23:59:59, 2012.02.15T00:00:00, 2012.02.15T23:59:59, 2012.02.29T00:00:00, 2012.02.29T23:59:59]
    t = table(1..size(vec) as uid, vec as pcol)
    select * from t where pcol in 2012.01.01
    //In previous versions, the above statement is equivalent to "select * from t where pcol == 2012.01.01" that returns 1 record
    //Since this version, it is equivalent to "select * from t where pcol in [2012.01.01]" that returns 0 record
    ```

- Aggregate functions cannot be used in the where condition when joining multiple in-memory tables since this version.

    ```
    t1 = table(1..10 as id,take(`a`b`c,10) as sym,string((1..10)+5) as val,take(14 10 18 23,10) as price)
    t2 = table(3..12 as id2,take(`b`c`d,10) as sym,string((3..12)+5) as val2,take(34 30 38 33,10) as price2)
    t3 = table(5..14 as id3,take(`c`d`e,10) as sym,string((5..14)+5) as val3,take(54 50 58 53,10) as price3)

    select * from t1 inner join t2 on t1.id = t2.id2 inner join t3 on t2.id2 = t3.id3 where t1.price>avg(t1.price) 
    //An error will be reported since this version.
    ```

### System Impacts Caused by Bug Fixes

- To upgrade to this version, the dolphindb.dos file must be replaced. Otherwise the server cannot be started.

- The validation for the schema parameter of loadTextEx has been made stricter.
    
    Since this version, the table specified by schema MUST NOT be empty, and the "name" and "type" columns must be of STRING type.

- The `take` function no longer accepts passing in a pair for the X parameter.

    ```
    take(pair(1, 3), 10)
    //output (previous versions): [1,3,1,3,1,3,1,3,1,3]
    //An error will be raised since this version: Usage: take(X, n). X must be a scalar or a non-empty vector.
    ```

- The handling of NULL values passed to the S parameter in mTopN functions and movingTopNIndex has changed.
    
    In previous versions, NULL values are treated as the smallest values. Since this version, NULL values passed in S are excluded from the sorting and do not impact the determination of the top N values. 

    ```
    X = [2, 1, 5, 3, 4, 3, 1, 9, 0, 5, 2, 3]
    S = [5, 8, 1, 9, 7, 3, 1, NULL, 0, 8, 7, 7]
    msumTopN(X, S, window=6, top=3)

    //Output (previous versions): [2, 3, 8, 8, 11, 10, 9, 15, 10, 10, 10, 10]
    //Output (since this version): [2, 3, 8, 8, 11, 10, 9, 9, 4, 4, 4, 3]
    ```

- The result of `cast("", BOOL)` can now be correctly returned as NULL. "false" was returned in previous versions.

- Added parameter validation for function genericTStateIterate: The parameter T must be strictly increasing since this version.

- Modified functions t3 and kama to be consistent with Python syntax: Continuous NULL values at the beginning are skipped, and the remaining NULL values are treated as 0 for calculation.

- An exception will be thrown when updating a table from a table join where the left table is a dimension table, and the right one is a DFS table. In previous versions, the update operation did not take effect without any error message reported.

- Function `distinct` cannot be nested with another aggregate function in a SQL query applied on a DFS table.

- Possible parsing error will be reported when a SELECT or EXEC statement is passed to a function with at least two arguments, for the comma (,) may be parsed as CROSS JOIN. You need to add a pair of parentheses for the statement to separate it from the other parameters as appropriate.

    ```
    mr(sqlDS(<select * from pt>),x->select top 1 * from x,,unionAll{,false})
    // The script below can be parsed correctly.
    mr(sqlDS(<select * from pt>),(x->select top 1 * from x),,unionAll{,false})

    n=1000
    t1=table(rand(100, n) as id, rand(100, n) as val)
    t2=table(rand(100, n) as id, rand(100, n) as val)

    re3=select * from t1  where val in select val from t2, val gt select first(val) from t2 where id = 1
    // The script below can be parsed correctly.
    re3=select * from t1  where val in (select val from t2), val gt (select first(val) from t2 where id = 1)
    ```

- Column aliases defined in the SELECT clause can no longer be referenced in the WHERE clause. This behavior matches standard SQL semantics.

    ```
    id = [1, 1, 2, 6, 8, 3, 2, 5, 3, 8]
    v1 = take(1..5, 10)
    t = table(id as `id, v1 as `v1)
    re1 = select id as i from t where i > 1

    // In the 1.30.21/2.00.9 version, the above SQL statement can be successfully executed.
    // Since this version, an error will be raised: Unrecognized column name i
    ```

- Since a NULL value now cannot be matched to another NULL, when inserting records with function `upsert!`, a new record is returned if the key column of the original table and table to be inserted contain NULL values.

    ```
    n=5
    t1 = table(n:n,`date`id`sym,[DATE,INT,STRING])
    t1[`date] = take((2020.05.01..2020.05.05),n)
    t1[`id] = take(int(),n)
    t1[`sym] = "A"+string(1..n)
    login("admin", "123456")
    dbPath = "dfs://upsert_test"
    if(existsDatabase(dbPath))
    dropDatabase(dbPath)
    db = database(dbPath, VALUE, 2020.05.01..2020.05.10)
    pt = db.createPartitionedTable(t1, `pt, `date).append!(t1)
    login("admin", "123456")
    pt = loadTable("dfs://upsert_test", "pt")
    newdata=table(take(2020.05.01..2020.05.05,5) as date,take(int(),5) as id,"B"+string(1..5) as sym)
    pt.upsert!(newdata,true,`id)
    select * from pt
    // In previous versions, five records were returned.
    // Since this version, ten records are returned.
    ```

- Added validation for `upsert!`: The number of newData columns must be consistent with that of the original table. In previous versions, table with fewer columns can be upserted.

- An error will be reported when filtering data with a where condition in columns from a partitioned table.

    ```
    login("admin","123456")
    if(existsDatabase("dfs://test_in")){
        dropDatabase("dfs://test_in")
    }
    db=database("dfs://test_in", VALUE, 2015.01M..2016.01M)
    t=table(take(2015.01M..2016.01M,10000) as date, 1..10000 as id, rand(100,10000) as v)
    db.createPartitionedTable(t,`pt,`date).append!(t)
    temp_t = db.loadTable(`pt)
    select distinct date from temp_t where date in temporalAdd(date, 2M) 
    //An error is reported: Can't use 'in' precidate with partitioned table columns in where condition, please use sub query to do that.
    //SQL statement using a subquery after "in" can be executed properly
    select distinct date from temp_t where date in select temporalAdd(date, 2M) from temp_t
    ```

- The right table of `wj`/`pwj` cannot be a DFS table.

### Plguins

- Removed methods `httpCreateSubJob`,` httpCreateMultiParserSubJob`, `httpCancelSubJob` and `httpGetJobStat` from the httpClient plugin.

---

## Version 1.30.22.2

### Changes Made to Match Industry Practices or SQL Standards

- Removed function `getClusterReplicationMetrics`. Added function `getSlaveReplicationQueueStatus` as an inheritance of `getClusterReplicationMetrics`.

- When calling function `toStdJson`:
  - For Boolean values, previous versions returned 1 and 0, but now returns true and false.
  - For NULL values, previous versions only converted Integral, Floating and Boolean NULL values to JSON null, other types were converted to "". Now NULL values of all types except STRING are converted to null.

### System Impacts Caused by Bug Fixes

- The `license` function now returns the license information in memory by default, instead of that from the .lic file as in previous versions.


## Version 1.30.22.1

### Changes Made to Match Industry Practices or SQL Standards

- Changed the behaviors of the `join`, `join!` and `append!` functions when merging two tuples.

    ```
    a =  [[1,2],[3,4]]
    b = [[5,6],[7,8]]
    a.join(b)
    //Output (previous versions): ([1,2],[3,4],([5,6],[7,8]))
    //Output (since this version): ([1,2],[3,4],[5,6],[7,8])
    
    a.join!(b)
    a
    //Output (previous versions):([1,2],[3,4],([5,6],[7,8]))
    //Output (since this version): ([1,2],[3,4],[5,6],[7,8])
    
    a.append!(b)
    a
    //Output (previous versions):([1,2],[3,4],([5,6],[7,8]))
    //Output (since this version): ([1,2],[3,4],[5,6],[7,8])
  ```

### System Impacts Caused by Bug Fixes

- When the *triggeringPattern* parameter of `streamEngineParser` is set to ‘keyCount', the *keepOrder* parameter now must be set to true. Setting *triggeringPattern* = 'keyCount’ with *keepOrder* = false raises an error.

- When using the `accumulate` higher-order function in the *metrics* parameter of `createReactiveStateEngine`, the *consistent* parameter of `accumulate` can no longer be set to false. 

## Version 1.30.22

### Changes Made to Match Industry Practices or SQL Standards

- Sharing the same stream table multiple times using the `share` function/statement or `enableTableShareAndPersistence` function will now result in an error.

    ```
    n=10000;
    t=streamTable(2020.01.01T00:00:00 + 0..(n-1) as timestamp, rand(`IBM`MS`APPL`AMZN,n) as symbol, rand(10.0, n) as value)
    share t as t1
    share t as t2 
    //In previous versions, the script above can be successfully executed.
    //Since this version, the second share operation would raise the error: This stream has already been shared as 't1'.
    //This change applies not only to the "share" statement, but also the share() and enableTableShareAndPersistence() functions.
    ```

    To re-share a stream table, it must first be unshared.

- Validation for appending data to stream tables has been enhanced.

    Previously, it was possible to append data with an older schema (fewer columns) to a stream table after the schema had been modified to add new columns. This is no longer allowed.

    ```
    t = streamTable(1:0, `id`val, [INT, INT])
    enableTableShareAndPersistence(t, `st)
    go
    data1 = table(1..10 as id, 11..20 as val)
    t.append!(data1)
    addColumn(st, `price, DOUBLE)
    t.append!(data1)
    data2 = table(1..10 as id, 11..20 as val, 21..30 as price)
    t.append!(data2)
    t.append!(data1)
    //Since this version, the script above will raise the error: The number of columns of the table to insert must be the same as that of the original table.
    //In previous versions, the script above can be successfully executed.
    ```

- Added parameter validations for user-defined functions which can only take scalars or regular arrays. Dictionaries, function definitions or tuples are no longer allowed.

- Modified the return value of function `avg`: If the input argument is of STRING type, a NULL value is now returned. An exception was raised in previous versions.

- The behavior of `SELECT * FROM a JOIN b` statements has been changed to match standard SQL semantics:

    - If an ON condition is not specified, a cross join will be performed between a and b;

    - If an ON condition is specified, an inner join will be performed between a and b.

    Since this version, if "join" is used in a SQL from clause, it is treated as a table join keyword instead of function `join`.

    ```
    select * from a join b
    //In previous versions, the above statement is equivalent to "select * from join(a, b)"
    //Since this version, it is equivalent to "select * from cj(a, b)"
    ```

- Join (including left join, left semi join, equi join and full join) behavior for NULL values has been updated to match standard SQL semantics.<br/>

    In previous versions, NULL values in join columns would be matched between the two joined tables. Since this version, NULL values will not be matched when joining.

- When a temporal scalar is used after the `in` predicate in a SQL statement, elements of the condition column are no longer matched with the scalar. Instead, the scalar is treated as a one-element vector to check if the elements of the condition column are contained in that vector.

    ```
    vec = [2012.01.01T00:00:00, 2012.01.01T23:59:59, 2012.01.10T00:00:00, 2012.01.10T23:59:59, 2012.01.31T00:00:00, 2012.01.31T23:59:59, 2012.02.01T00:00:00, 2012.02.01T23:59:59, 2012.02.15T00:00:00, 2012.02.15T23:59:59, 2012.02.29T00:00:00, 2012.02.29T23:59:59]
    t = table(1..size(vec) as uid, vec as pcol)
    select * from t where pcol in 2012.01.01
    //In previous versions, the above statement is equivalent to "select * from t where pcol == 2012.01.01" that returns 1 record
    //Since this version, it is equivalent to "select * from t where pcol in [2012.01.01]" that returns 0 record
    ```

### System Impacts Caused by Bug Fixes

- To upgrade to this version, the dolphindb.dos file must be replaced. Otherwise the server cannot be started.

- The validation for the schema parameter of `loadTextEx` has been made stricter.
    
    Since this version, the table specified by schema MUST NOT be empty, and the "name" and "type" columns must be of STRING type.

- The `take` function no longer accepts passing in a pair for the X parameter.

    ```
    take(pair(1, 3), 10)
    //output (previous versions): [1,3,1,3,1,3,1,3,1,3]
    //An error will be raised since this version: Usage: take(X, n). X must be a scalar or a non-empty vector.
    ```

- The handling of NULL values passed to the *S* parameter in mTopN functions and `movingTopNIndex` has changed.
    
    In previous versions, NULL values are treated as the smallest values. Since this version, NULL values passed in S are excluded from the sorting and do not impact the determination of the top N values. 

    ```
    X = [2, 1, 5, 3, 4, 3, 1, 9, 0, 5, 2, 3]
    S = [5, 8, 1, 9, 7, 3, 1, NULL, 0, 8, 7, 7]
    msumTopN(X, S, window=6, top=3)

    //Output (previous versions): [2, 3, 8, 8, 11, 10, 9, 15, 10, 10, 10, 10]
    //Output (since this version): [2, 3, 8, 8, 11, 10, 9, 9, 4, 4, 4, 3]
    ```

- The result of `cast("", BOOL)` can now be correctly returned as NULL. "false" was returned in previous versions.

- Added parameter validation for function genericTStateIterate: The parameter T must be strictly increasing since this version.

- Modified functions t3 and kama to be consistent with Python syntax: Continuous NULL values at the beginning are skipped, and the remaining NULL values are treated as 0 for calculation.

- An exception will be thrown when updating a table from a table join where the left table is a dimension table, and the right one is a DFS table. In previous versions, the update operation did not take effect without any error message reported.

- Function `distinct` cannot be nested with another aggregate function in a SQL query applied on a DFS table.

- Possible parsing error will be reported when a SELECT or EXEC statement is passed to a function with at least two arguments, for the comma (,) may be parsed as CROSS JOIN. You need to add a pair of parentheses for the statement to separate it from the other parameters as appropriate.

    ```
    mr(sqlDS(<select * from pt>),x->select top 1 * from x,,unionAll{,false})
    // The script below can be parsed correctly.
    mr(sqlDS(<select * from pt>),(x->select top 1 * from x),,unionAll{,false})

    n=1000
    t1=table(rand(100, n) as id, rand(100, n) as val)
    t2=table(rand(100, n) as id, rand(100, n) as val)

    re3=select * from t1  where val in select val from t2, val gt select first(val) from t2 where id = 1
    // The script below can be parsed correctly.
    re3=select * from t1  where val in (select val from t2), val gt (select first(val) from t2 where id = 1)
    ```

- Column aliases defined in the SELECT clause can no longer be referenced in the WHERE clause. This behavior matches standard SQL semantics.

    ```
    id = [1, 1, 2, 6, 8, 3, 2, 5, 3, 8]
    v1 = take(1..5, 10)
    t = table(id as `id, v1 as `v1)
    re1 = select id as i from t where i > 1

    // In the 1.30.21/2.00.9 version, the above SQL statement can be successfully executed.
    // Since this version, an error will be raised: Unrecognized column name i
    ```

- Since a NULL value now cannot be matched to another NULL, when inserting records with function `upsert!`, a new record is returned if the key column of the original table and table to be inserted contain NULL values.

    ```
    n=5
    t1 = table(n:n,`date`id`sym,[DATE,INT,STRING])
    t1[`date] = take((2020.05.01..2020.05.05),n)
    t1[`id] = take(int(),n)
    t1[`sym] = "A"+string(1..n)
    login("admin", "123456")
    dbPath = "dfs://upsert_test"
    if(existsDatabase(dbPath))
    dropDatabase(dbPath)
    db = database(dbPath, VALUE, 2020.05.01..2020.05.10)
    pt = db.createPartitionedTable(t1, `pt, `date).append!(t1)
    login("admin", "123456")
    pt = loadTable("dfs://upsert_test", "pt")
    newdata=table(take(2020.05.01..2020.05.05,5) as date,take(int(),5) as id,"B"+string(1..5) as sym)
    pt.upsert!(newdata,true,`id)
    select * from pt
    // In previous versions, five records were returned.
    // Since this version, ten records are returned.
    ```

- Added validation for `upsert!`: The number of newData columns must be consistent with that of the original table. In previous versions, table with fewer columns can be upserted.

- An error will be reported when filtering data with a where condition in columns from a partitioned table.

    ```
    login("admin","123456")
    if(existsDatabase("dfs://test_in")){
        dropDatabase("dfs://test_in")
    }
    db=database("dfs://test_in", VALUE, 2015.01M..2016.01M)
    t=table(take(2015.01M..2016.01M,10000) as date, 1..10000 as id, rand(100,10000) as v)
    db.createPartitionedTable(t,`pt,`date).append!(t)
    temp_t = db.loadTable(`pt)
    select distinct date from temp_t where date in temporalAdd(date, 2M) 
    //An error is reported: Can't use 'in' precidate with partitioned table columns in where condition, please use sub query to do that.
    //SQL statement using a subquery after "in" can be executed properly
    select distinct date from temp_t where date in select temporalAdd(date, 2M) from temp_t
    ```

- The right table of `wj`/`pwj` cannot be a DFS table.

### Plguins

- Removed methods `httpCreateSubJob`,` httpCreateMultiParserSubJob`, `httpCancelSubJob` and `httpGetJobStat` from the httpClient plugin.
