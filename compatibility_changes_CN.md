# 兼容性列表

此文件概述了版本 1.30.22/2.00.10 中可能影响您现有脚本和配置的新功能和更改（包括符合行业标准的更新）。

请仔细查看该文件，以了解升级到此版本可能会对您当前的设置产生的影响。

- [兼容性列表](#兼容性列表)
  - [2.00.10 版本](#20010-版本)
    - [为匹配行业实践或 SQL 标准而进行的更改](#为匹配行业实践或-sql-标准而进行的更改)
    - [Bug 修复造成的系统影响](#bug-修复造成的系统影响)
    - [插件](#插件)
  - [1.30.22 版本](#13022-版本)
    - [为匹配行业实践或 SQL 标准而进行的更改](#为匹配行业实践或-sql-标准而进行的更改-1)
    - [Bug 修复造成的系统影响](#bug-修复造成的系统影响-1)
    - [插件](#插件-1)


## 2.00.10 版本

### 为匹配行业实践或 SQL 标准而进行的更改

- `share` 语句/函数和 `enableTableShareAndPersistence` 函数将同一个表共享多次，增加了报错提示。

    ```
    n=10000;
    t=streamTable(2020.01.01T00:00:00 + 0..(n-1) as timestamp, rand(`IBM`MS`APPL`AMZN,n) as symbol, rand(10.0, n) as value)
    share t as t1
    share t as t2 
    //旧版本可以执行
    //新版本第二次share会报错This stream has already been shared as 't1'.
    //除了share语句，share函数和enableTableShareAndPersistence函数也加了这样的校验
    ```

    若需要重新共享该表，可先取消当前的共享。

- DECIMAL64 类型数据的向量应用 `sum` 函数求和后的结果类型由 DECIMAL64 修改为 DECIMAL128。

    ```
    d1=decimal64(10015.555 514796.1186,3)
    re=sum(d1)
    typestr(re)  
    //旧版本返回 DECIMAL64，而新版本返回 DECIMAL128
    ```

- 流数据表写入数据时增加校验：在对流表新增列后，如果写入了符合新 schema 的数据后，不能再写入符合旧 schema 的数据。

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
    //新版本报错The number of columns of the table to insert must be the same as that of the original table.
    //旧版本允许执行
    ```

- SYMBOL 和 STRING 类型转换成 DECIMAL 类型的行为发生变化：旧版本从 scale 的位置截断，新版本从 scale 位置四舍五入后截断。

    ```
    symbol(["1.34", "4.5677"])$DECIMAL32(2)
    //旧版本结果: [1.34, 4.56]
    //新版本结果: [1.34, 4.57]
    ```

- 对自定义函数的参数默认值增加了校验。在新版本中，参数默认值只能是标量或常规数组，不能为字典、函数定义和元组。

- 修改 avg 函数输入字符串类型后的返回结果。在新版本中，avg 函数输入字符串类型后将返回NULL；而在旧版本中将抛出异常。

- DolphinDB JOIN 语句与标准 SQL 保持一致：
- 
  - 当不指定 ON 连接条件时，执行 CROSS JOIN 连接，返回两个表的笛卡尔积的结果集。
  - 当指定 ON 连接条件时，执行 INNER JOIN 连接，返回连接表中满足限制条件的行的结果集。

    在新版本中，将 SQL 语句中的 “join” 视为表连接关键字而不是函数连接。

    ```
    select * from a join b
    //旧版本相当于select * from join(a, b)
    //新版本相当于 select * from cj(a, b)
    ```

- 和标准 SQL 保持一致，不支持连接列的数据类型为 BLOB。

    增加了报错提示：Key must be integer, date/time, or string.

- 和标准 SQL 保持一致，修改 LEFT JOIN, LEFT SEMI JOIN, RIGHT JOIN, EQUI JOIN, FULL JOIN 中空值的匹配行为。

    两表中的空值，在旧版本中被视为匹配成功，在新版本中被视为匹配不成功。

- 修改 RIGHT JOIN 的结果显示和标准 SQL 保持一致.

  - 旧版本先显示右表的列，再显示左表的列
  - 新版本先显示左表的列，再显示右表的列。

- 两个表进行右连接时，如果某列存在于两表，且列名不指定 qualifier，按照从左往右的第一个包含该列的表来处理.

    ```
    t1 = table(1..10 as id, 11..20 as val1)
    t2 = table(6..15 as id, 21..30 as val2)
    select avg(val1+val2) from t1 right join t2 on t1.id=t2.id group by id

    // 老版本相当于select avg(val1+val2) from t1 right join t2 on t1.id=t2.id group by t2.id
    // 新版本相当于select avg(val1+val2) from t1 right join t2 on t1.id=t2.id group by t1.id
    ```

    多于两个表进行连接时，如果某列存在于多个表中，必须为列名指定 qualifier，否则会报错。此行为与标准 SQL 保持一致。

- 在 SQL 语句中使用 `in` 谓词时，若 `in` 后面是标量，则不再判断条件列的元素是否等于该标量，而是将该标量视为向量，检查条件列的元素是否在这个向量中。

    ```
    vec = [2012.01.01T00:00:00, 2012.01.01T23:59:59, 2012.01.10T00:00:00, 2012.01.10T23:59:59, 2012.01.31T00:00:00, 2012.01.31T23:59:59, 2012.02.01T00:00:00, 2012.02.01T23:59:59, 2012.02.15T00:00:00, 2012.02.15T23:59:59, 2012.02.29T00:00:00, 2012.02.29T23:59:59]
    t = table(1..size(vec) as uid, vec as pcol)
    select * from t where pcol in 2012.01.01
    //老版本相当于select * from t where pcol == 2012.01.01，查出1条数据
    //新版本相当于select * from t where pcol in [2012.01.01],查出0条数据
    ```

- 在多个内存表进行内连接的查询语句中，不允许在 where 子句中使用聚合函数。

    ```
    t1 = table(1..10 as id,take(`a`b`c,10) as sym,string((1..10)+5) as val,take(14 10 18 23,10) as price)
    t2 = table(3..12 as id2,take(`b`c`d,10) as sym,string((3..12)+5) as val2,take(34 30 38 33,10) as price2)
    t3 = table(5..14 as id3,take(`c`d`e,10) as sym,string((5..14)+5) as val3,take(54 50 58 53,10) as price3)

    select * from t1 inner join t2 on t1.id = t2.id2 inner join t3 on t2.id2 = t3.id3 where t1.price>avg(t1.price) 
    //旧版本执行最后一行代码，可以返回结果；而新版本会报错
    ```

### Bug 修复造成的系统影响

- 本次升级必须更新 dolphindb.dos，否则节点无法启动。

- `loadTextEx`  的 *schema* 参数增加了更为严格的校验。
    
    新版本要求指定的表是非空表，并且 "name" 和 "type" 列是 STRING 类型。

- `take` 函数不支持输入 pair。

    ```
    take(pair(1, 3), 10)
    //旧版本结果[1,3,1,3,1,3,1,3,1,3]
    //新版本报错Usage: take(X, n). X must be a scalar or a non-empty vector.
    ```

- 修改 mTopN 和 `movingTopNIndex` 函数的 *S* 参数中 NULL 值的行为。
    
    在旧版本中，NULL 值被当作最小值参与排序，而新版本中，NULL 不参与排序，对应 X 中的值不参与计算。

    ```
    X = [2, 1, 5, 3, 4, 3, 1, 9, 0, 5, 2, 3]
    S = [5, 8, 1, 9, 7, 3, 1, NULL, 0, 8, 7, 7]
    msumTopN(X, S, window=6, top=3)

    //老版本结果 [2, 3, 8, 8, 11, 10, 9, 15, 10, 10, 10, 10]
    //新版本结果 [2, 3, 8, 8, 11, 10, 9, 9, 4, 4, 4, 3]
    ```

- 修改 cast(““, BOOL) 的结果。旧版本返回 false，而新版本返回 NULL。

- `genericTStateIterate` 的 *T* 参数增加校验。旧版本不要求 *T* 必须严格递增；而新版本要求 *T* 必须严格递增。

- 修改 `kama` 和 `t3` 函数对于 NULL 值的处理与 Python 保持一致。新版本中 `kama` 和 `t3` 函数将跳过开头传入的连续的 NULL 值，将剩余的 NULL 值视为0进行计算。

- 对左表是维度表，右表是分布式表的连接表进行 update 更新的行为修改为抛出异常。旧版本可以执行 update 语句，但数据没有更新。新版本会抛出异常。

- 旧版本的 SQL 语句中 `distinct` 函数应用于分布式表时，可以和其它聚合函数嵌套使用。而新版本禁止使用。

- 在新版本中，`select` 或 `exec` 语句应用于不少于2个参数的函数时，在部分情况下，会出现语法解析错误（将其后的逗号（,）解析为了 `cross join`）。此时，需要使用括号包裹 `select` 或 `exec` 语句，以规避错误。

    ```
    mr(sqlDS(<select * from pt>),x->select top 1 * from x,,unionAll{,false})
    //上条语句加括号包裹后可正常解析
    mr(sqlDS(<select * from pt>),(x->select top 1 * from x),,unionAll{,false})

    n=1000
    t1=table(rand(100, n) as id, rand(100, n) as val)
    t2=table(rand(100, n) as id, rand(100, n) as val)
    re3=select * from t1  where val in select val from t2, val gt select first(val) from t2 where id = 1
    //上条语句加括号包裹后可正常解析
    re3=select * from t1  where val in (select val from t2), val gt (select first(val) from t2 where id = 1)
    ```

- 和标准 SQL 保持一致，修改 `select` 子句中定义的列别名不能在 `where`子句中引用。

    ```
    id = [1, 1, 2, 6, 8, 3, 2, 5, 3, 8]
    v1 = take(1..5, 10)
    t = table(id as `id, v1 as `v1)
    re1 = select id as i from t where i > 1

    //旧版本（1.30.21/2.00.10）可以执行
    //新版本会报错Unrecognized column name i
    ```

- 修改 `upsert!` 函数插入记录时，空值得匹配行为。在旧版本中，空值与空值视为匹配，因为不会更新记录；而在新版本中，空值与空值视为不匹配，因此会增加新记录。

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
    //老版本返回5条记录
    //新版本返回10条记录
    ```

- `upsert!` 函数增加列数校验。在旧版本中，newData 的列数可以比原表少；而在新版本中，newData 的列数必须与原表的列数一致。

- 新版本中，在 where 过滤条件中，当使用 in 谓词指定分布式表中的列作为查询范围时，会报错。

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
    //报错： Can't use 'in' precidate with partitioned table columns in where condition, please use sub query to do that.
    //修改为子查询后可以正常执行
    select distinct date from temp_t where date in select temporalAdd(date, 2M) from temp_t
    ```

- `wj` 和 `pwj` 不支持右表为分布式表。

### 插件

- httpClient 插件删除 `httpCreateSubJob`, `httpCreateMultiParserSubJob`, `httpCancelSubJob`, `httpGetJobStat` 接口。

---

## 1.30.22 版本

### 为匹配行业实践或 SQL 标准而进行的更改

- `share` 语句/函数和 `enableTableShareAndPersistence` 函数将同一个表共享多次，增加了报错提示。

    ```
    n=10000;
    t=streamTable(2020.01.01T00:00:00 + 0..(n-1) as timestamp, rand(`IBM`MS`APPL`AMZN,n) as symbol, rand(10.0, n) as value)
    share t as t1
    share t as t2 
    //旧版本可以执行
    //新版本第二次share会报错This stream has already been shared as 't1'.
    //除了share语句，share函数和enableTableShareAndPersistence函数也加了这样的校验
    ```

    若需要重新共享该表，可先取消当前的共享。

- 流数据表写入数据时增加校验：在对流表新增列后，如果写入了符合新 schema 的数据后，不能再写入符合旧 schema 的数据。

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
    //新版本报错The number of columns of the table to insert must be the same as that of the original table.
    //旧版本允许执行
    ```

- 对自定义函数的参数默认值增加了校验。在新版本中，参数默认值只能是标量或常规数组，不能为字典、函数定义和元组。

- 修改 avg 函数输入字符串类型后的返回结果。在新版本中，avg 函数输入字符串类型后将返回NULL；而在旧版本中将抛出异常。

- DolphinDB JOIN 语句与标准 SQL 保持一致：
- 
  - 当不指定 ON 连接条件时，执行 CROSS JOIN 连接，返回两个表的笛卡尔积的结果集。
  - 当指定 ON 连接条件时，执行 INNER JOIN 连接，返回连接表中满足限制条件的行的结果集。

    在新版本中，将 SQL 语句中的 “join” 视为表连接关键字而不是函数连接。

    ```
    select * from a join b
    //旧版本相当于select * from join(a, b)
    //新版本相当于 select * from cj(a, b)
    ```

- 和标准 SQL 保持一致，修改 LEFT JOIN, LEFT SEMI JOIN, RIGHT JOIN, EQUI JOIN, FULL JOIN 中空值的匹配行为。

    两表中的空值，在旧版本中被视为匹配成功，在新版本中被视为匹配不成功。

- 在 SQL 语句中使用 `in` 谓词时，若 `in` 后面是标量，则不再判断条件列的元素是否等于该标量，而是将该标量视为向量，检查条件列的元素是否在这个向量中。

    ```
    vec = [2012.01.01T00:00:00, 2012.01.01T23:59:59, 2012.01.10T00:00:00, 2012.01.10T23:59:59, 2012.01.31T00:00:00, 2012.01.31T23:59:59, 2012.02.01T00:00:00, 2012.02.01T23:59:59, 2012.02.15T00:00:00, 2012.02.15T23:59:59, 2012.02.29T00:00:00, 2012.02.29T23:59:59]
    t = table(1..size(vec) as uid, vec as pcol)
    select * from t where pcol in 2012.01.01
    //老版本相当于select * from t where pcol == 2012.01.01，查出1条数据
    //新版本相当于select * from t where pcol in [2012.01.01],查出0条数据
    ```

### Bug 修复造成的系统影响

- 本次升级必须更新 dolphindb.dos，否则节点无法启动。

- `loadTextEx`  的 *schema* 参数增加了更为严格的校验。
    
    新版本要求指定的表是非空表，并且 "name" 和 "type" 列是 STRING 类型。

- `take` 函数不支持输入 pair。

    ```
    take(pair(1, 3), 10)
    //旧版本结果[1,3,1,3,1,3,1,3,1,3]
    //新版本报错Usage: take(X, n). X must be a scalar or a non-empty vector.
    ```

- 修改 mTopN 和 `movingTopNIndex` 函数的 *S* 参数中 NULL 值的行为。
    
    在旧版本中，NULL 值被当作最小值参与排序，而新版本中，NULL 不参与排序，对应 X 中的值不参与计算。

    ```
    X = [2, 1, 5, 3, 4, 3, 1, 9, 0, 5, 2, 3]
    S = [5, 8, 1, 9, 7, 3, 1, NULL, 0, 8, 7, 7]
    msumTopN(X, S, window=6, top=3)

    //老版本结果 [2, 3, 8, 8, 11, 10, 9, 15, 10, 10, 10, 10]
    //新版本结果 [2, 3, 8, 8, 11, 10, 9, 9, 4, 4, 4, 3]
    ```

- 修改 cast(““, BOOL) 的结果。旧版本返回 false，而新版本返回 NULL。

- `genericTStateIterate` 的 *T* 参数增加校验。旧版本不要求 *T* 必须严格递增；而新版本要求 *T* 必须严格递增。

- 修改 `kama` 和 `t3` 函数对于 NULL 值的处理与 Python 保持一致。新版本中 `kama` 和 `t3` 函数将跳过开头传入的连续的 NULL 值，将剩余的 NULL 值视为0进行计算。

- 对左表是维度表，右表是分布式表的连接表进行 update 更新的行为修改为抛出异常。旧版本可以执行 update 语句，但数据没有更新。新版本会抛出异常。

- 旧版本的 SQL 语句中 `distinct` 函数应用于分布式表时，可以和其它聚合函数嵌套使用。而新版本禁止使用。

- 在新版本中，`select` 或 `exec` 语句应用于不少于2个参数的函数时，在部分情况下，会出现语法解析错误（将其后的逗号（,）解析为了 `cross join`）。此时，需要使用括号包裹 `select` 或 `exec` 语句，以规避错误。

    ```
    mr(sqlDS(<select * from pt>),x->select top 1 * from x,,unionAll{,false})
    //上条语句加括号包裹后可正常解析
    mr(sqlDS(<select * from pt>),(x->select top 1 * from x),,unionAll{,false})

    n=1000
    t1=table(rand(100, n) as id, rand(100, n) as val)
    t2=table(rand(100, n) as id, rand(100, n) as val)
    re3=select * from t1  where val in select val from t2, val gt select first(val) from t2 where id = 1
    //上条语句加括号包裹后可正常解析
    re3=select * from t1  where val in (select val from t2), val gt (select first(val) from t2 where id = 1)
    ```

- 和标准 SQL 保持一致，修改 `select` 子句中定义的列别名不能在 `where`子句中引用。

    ```
    id = [1, 1, 2, 6, 8, 3, 2, 5, 3, 8]
    v1 = take(1..5, 10)
    t = table(id as `id, v1 as `v1)
    re1 = select id as i from t where i > 1

    //旧版本（1.30.21/2.00.10）可以执行
    //新版本会报错Unrecognized column name i
    ```

- 修改 `upsert!` 函数插入记录时，空值得匹配行为。在旧版本中，空值与空值视为匹配，因为不会更新记录；而在新版本中，空值与空值视为不匹配，因此会增加新记录。

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
    //老版本返回5条记录
    //新版本返回10条记录
    ```

- `upsert!` 函数增加列数校验。在旧版本中，newData 的列数可以比原表少；而在新版本中，newData 的列数必须与原表的列数一致。

- 新版本在 where 过滤条件中，对分区表的列使用了 in 谓词时，会报错。

- `wj` 和 `pwj` 不支持右表为分布式表。

### 插件

- httpClient 插件删除 `httpCreateSubJob`, `httpCreateMultiParserSubJob`, `httpCancelSubJob`, `httpGetJobStat` 接口。
