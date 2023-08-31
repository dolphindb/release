# DolphinDB 发行说明

- [DolphinDB 发行说明](#dolphindb-发行说明)
  - [版本兼容性说明列表](#版本兼容性说明列表)
  - [DolphinDB 服务器](#dolphindb-服务器)
    - [新功能](#新功能)
    - [改进](#改进)
    - [故障修复](#故障修复)
  - [DolphinDB 插件](#dolphindb-插件)
  - [客户端工具](#客户端工具)
    - [GUI](#gui)
    - [WEB](#web)
  - [API](#api)
    - [Java API](#java-api)
    - [Python API](#python-api)
    - [C++ API](#c-api)
    - [C# API](#c-api-1)
    - [Go API](#go-api)

## 版本兼容性说明列表

详见 [版本兼容性说明列表](./../compatibility_changes_CN.md/#13022-版本)

## DolphinDB 服务器

版本号： 1.30.22 &nbsp;&nbsp;&nbsp; [一级兼容](./../DolphinDB_compatibility_levels.md/#32-一级兼容性标准) 1.30.21

发行日期： 2023-07-20

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.22.1.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.22.1_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.22.1_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.22.1.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.22.1_JIT.zip)
[Linux ARM64](https://www.dolphindb.cn/downloads/DolphinDB_ARM64_V1.30.22.zip)

版本号： 1.30.21 &nbsp;&nbsp;&nbsp; [二级兼容](./../DolphinDB_compatibility_levels.md/#32-二级兼容性标准) 1.30.20

发行日期： 2023-02-15

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.21.6.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.21.6_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.21.6_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.21.6.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.21.6_JIT.zip)
[Linux ARM64](https://www.dolphindb.cn/downloads/DolphinDB_ARM64_V1.30.21.1.zip)

版本号： 1.30.20 &nbsp;&nbsp;&nbsp; [二级兼容](./../DolphinDB_compatibility_levels.md/#32-二级兼容性标准) 1.30.19

发行日期： 2022-09-30

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.20.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.20_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.20_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.20.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.20_JIT.zip)
[Linux ARM64](https://www.dolphindb.cn/downloads/DolphinDB_ARM64_V1.30.20.zip)

版本号： 1.30.19 &nbsp;&nbsp;&nbsp; [一级兼容](./../DolphinDB_compatibility_levels.md/#32-一级兼容性标准) 1.30.18

发行日期： 2022-07-14

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.19.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.19_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.19_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.19.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.19_JIT.zip)
[Linux ARM64](https://www.dolphindb.cn/downloads/DolphinDB_ARM64_V1.30.19.zip)

版本号： 1.30.18 &nbsp;&nbsp;&nbsp; [二级兼容](./../DolphinDB_compatibility_levels.md/#32-二级兼容性标准) 1.30.17

发行日期： 2022-05-09

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.18.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.18_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.18_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.18.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.18_JIT.zip)

版本号： 1.30.17 &nbsp;&nbsp;&nbsp; [三级兼容](./../DolphinDB_compatibility_levels.md/#33-三级兼容性标准) 1.30.16

发行日期： 2022-03-29

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.17.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.17_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.17_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.17.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.17_JIT.zip)

版本号： 1.30.16

发行日期： 2022-01-10

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.16.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.16_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.16_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.16.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.16_JIT.zip)

版本号： 1.30.15

发行日期： 2021-11-22

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.15.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.15_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.15_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.15.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.15_JIT.zip)

版本号： 1.30.14

发行日期： 2021-11-05

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.14.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.14_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.14_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.14.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.14_JIT.zip)

版本号： 1.30.13

发行日期： 2021-08-25

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.13.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.13_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.13_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.13.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.13_JIT.zip)

版本号： 1.30.12

发行日期： 2021-07-31

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.12.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.12_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.12_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.12.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.12_JIT.zip)

版本号： 1.30.11

发行日期： 2021-06-15

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.11.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.11_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.11_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.11.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.11_JIT.zip)

版本号： 1.30.10

发行日期： 2021-05-31

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.10.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.10_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.10_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.10.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.10_JIT.zip)

版本号： 1.30.9

发行日期： 2021-05-17

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.9.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.9_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.9_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.9.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.9_JIT.zip)

版本号： 1.30.8

发行日期： 2021-04-28

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.8.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.8_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.8_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.8.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.8_JIT.zip)

版本号： 1.30.7

发行日期： 2021-04-21

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.7.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.7_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.7_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.7.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.7_JIT.zip)

版本号： 1.30.6

发行日期： 2021-04-07

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.6.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.6_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.6_ABI.zip) 

版本号： 1.30.5

发行日期： 2021-03-30

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.5.zip) 

版本号： 1.30.4

发行日期： 2021-03-29

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.4.zip) 

版本号： 1.30.3

发行日期： 2021-02-28

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.3.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.3_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.3_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.3.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.3_JIT.zip)

版本号： 1.30.2

发行日期： 2021-01-25

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.2.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.2_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.2_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.2.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.2_JIT.zip)

版本号： 1.30.1

发行日期： 2021-01-12

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.1.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.1_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.1_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.1.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.1_JIT.zip)

版本号： 1.30.0

发行日期： 2020-12-29

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.0.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.0_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.0_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.0.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.0_JIT.zip)

### 新功能

* 新增配置项 *enableCoreDump*，设置是否生成 coredump。仅支持 Linux 系统。（**1.30.22**）
* 新增配置项 *disableCoreDumpOnShutdown*，设置安全关机时是否产生 coredump。仅支持 Linux 系统。（**1.30.22**）
* 新增配置项 *allowMissingPartitions*，设置是否忽略新增数据中所包含的分区方案外的数据。（**1.30.22**）
* 新增配置项 *volumeUsageThreshold*，设置数据节点磁盘卷的可使用率。（**1.30.22**）
* 新增函数 `listRemotePlugins` 和 `installPlugin`，分别用于查询可用的插件信息和下载插件。（**1.30.22**）
* 新增函数 `writeLogLevel`，能够将指定级别的文本写入日志文件中。（**1.30.22**）
* 新增函数 `sessionWindow`，对一个时间序列根据会话时间间隔进行分组。（**1.30.22**）
* 新增函数 `summary`，生成输入数据的汇总统计信息，包含最小值、最大值、计数、均值、标准差和指定的百分位数。（**1.30.22**）
* 新增函数 `encodeShortGenomeSeq`, `decodeShortGenomeSeq` 分别用于对 DNA 序列进行编解码。同时新增函数 `genShortGenomeSeq`，可在滑动窗口内进行编码。（**1.30.22**）
* 新增函数 `gramSchmidt`，实现施密特正交化计算。（**1.30.22**）
* 新增与 `lasso` 功能等价的函数 `lassoBasic`，其参数支持输入向量。（**1.30.22**）
* 新增26个 TopN 系列函数（**1.30.22**）
    * m系列：`mskewTopN`, `mkurtosisTopN`
    * cum系列：`cumsumTopN`, `cumavgTopN`, `cumstdTopN`, `cumstdpTopN`, `cumvarTopN`, `cumvarpTopN`, `cumbetaTopN`, `cumcorrTopN`, `cumcovarTopN`, `umwsumTopN`, `cumskewTopN`, `cumkurtosisTopN`
    * tm系列：`tmsumTopN`, `tmavgTopN`, `tmstdTopN`, `tmstdpTopN`, `tmvarTopN`, `tmvarpTopN`, `tmbetaTopN`, `tmcorrTopN`, `tmcovarTopN`, `tmwsumTopN`, `tmskewTopN`, `tmkurtosisTopN`
* 新增 `initcap` 函数，将字符串的第一个字母变成大写，其他字母变小写。（**1.30.22**）
* 新增三次样条插值函数 `splrep` 和 `splev`。（**1.30.22**）
* 新增函数 `scs`，用于求解一次或二次规划函数在线性约束条件下的最优解。（**1.30.22**）
* 新增函数 `temporalSeq`，按指定的间隔生成时间序列。（**1.30.22**）
* 新增函数 `base64Encode和base64Decode`，支持 base64 加密与解密。（**1.30.22**）
* 新增函数 `addFunctionTypeInferenceRule`，用于在 JIT 中添加自定义函数类型推导规则。（**1.30.22**）
* JIT 支持 COMPLEX 类型。
* 新增创建流数据多线程分发引擎的函数 `createStreamDispatchEngine`。（**1.30.22**）
* 新增配置项 `logicOrIgnoreNull`，设置 `or` 函数在操作数中包含 NULL 时的处理方式。默认值为 true：当另一个操作数非零或为零时，返回 true 或 false。若需要 `or` 函数的行为和旧版本保持一致，则应该将该配置设置为 false。（**1.30.21.4**）
* `case when` 语句后支持使用 `is null` 判断。（**1.30.21.4**）
* 对 MVCC 表，新增配置项 `mvccCheckpointThreshold` 用于设置创建检查点的操作次数阈值；新增函数 `forceMvccCheckpoint`，用于手动触发创建 MVCC 表的检测点。（**1.30.21.3**）
* 新增功能 License Server，用于根据 license 的限制分配节点的硬件资源。新增相关函数 `getLicenseServerResourceInfo`，`getRegisteredNodeInfo`，相关配置项 `licenseServerSite`，`bindCores`。（**1.30.21**）
* 新增配置项 `thirdPartyAuthenticator`，用于第三方系统校验用户权限。通过指定该参数，在用户登录时，系统会通过第三方系统进行权限验证。（**1.30.21**）
* 插件启动时会自动检查版本。（**1.30.21**）
* 新增集群间数据异步复制功能，将主集群数据复制到从集群，且保证主、从集群数据一致，实现了集群异地容灾。（**1.30.21**）
* 新增对 arrow 格式的支持。（**1.30.21**）
* 新增命令 `setMaxConnections` 用于在线修改当前节点的最大连接数。（**1.30.21**）    
* 新增函数 `demean`，用于对数据去均值化处理。同时在响应式状态引擎中支持该函数。（**1.30.21**）   
* 函数 `dict` 和 `syncDict` 新增参数 `ordered` 用于创建有序字典，支持键值对的顺序与输入顺序保持一致；支持两个字典的二元操作，以及字典和 scalar, vector的二元操作。（**1.30.21**）    
* 新增累计窗口函数 `cumnunique`，用于统计元素累积的唯一值数量。同时在响应式状态引擎中支持该函数。 （**1.30.21**）       
* 新增函数 `stringFormat`，用于动态字符串的构建。（**1.30.21**）    
* 新增函数 `nanInfFill` 用于替换 NaN 和 Inf 值。（**1.30.21**）
* 新增函数 `byColumn`，使高阶函数支持列内竖向计算。同时在流计算中支持该函数。（**1.30.21**）    
* 新增函数 `volumeBar` 用于数据的累积分组。（**1.30.21**）    
* 新增函数 `enlist` 用于将标量或向量，转化为由其作为元素值的向量或元组。（**1.30.21**） 
* 新增运算符 `eachAt(@)`，支持访问向量、矩阵、表、元组、字典和函数。    （**1.30.21**）
* 新增函数 `latestKeyedTable`, `latestIndexedTable`，用于创建时间序列相关的键值表和索引表。支持按时间列进行条件更新，只有值更大的新记录才会更新具有相同主键的原表中的记录。（**1.30.21**）
* 新增部分兼容标准 SQL 的功能。包括（**1.30.21**）：    
    * 新增语句：`drop`（支持删库，删表操作），`create local temporary table`（支持创建本地临时内存表），`alter`（新增支持列名重命名，删除列），`case when`, `union/union all`, `join on`, `with as`（支持 `with` 关键字使用参数对列重命名）        
    * 新增谓词：`(not) between and`, `is null/is not null`, `(not) exists/not exist`, `any/all`       
    * 新增函数：`nullIf`, `coalesce`        
    * 新增关键字：`distinct`（单个或多个字段去重），`nulls first/nulls last`（`order by` 关键字）  
* 支持多表 `join` 语句，`join` 语法支持使用别名，且支持 `join` 的对象是一个 SQL 子查询。（**1.30.21**）
* 支持 `select` 常量时不指定别名，此时常量值将作为列名。（**1.30.21**）    
* 支持条件语句中 `in` 等谓词以及运算符对 SQL 子查询返回的结果表进行操作。 （**1.30.21**）   
* 每次对 DFS 表进行 update/upsert/delete 操作，都会产生一个版本。系统会回收历史版本，回收时间由新增配的置项 `oldChunkVersionRetentionTime` 控制。用于设置历史版本 chunk 的保存时间。（**1.30.21**）    
* 提供各大交易所的交易日历及用户自定义交易日历的功能，支持在函数 `temporalAdd`, `resample`, `asfreq`, `transFreq` 中根据用户及定义的交易日历进行计算。新增相关置项 `marketHolidayDir`，新增相关函数 `addMarketHoliday`, `updateMarketHoliday`, `getMarketCalendar` 用于增加更新和获取自定义交易日历信息。（**1.30.21**）
* 新增函数 `genericStateIterate`, `genericTStateIterate` 流数据中窗口迭代计算。（**1.30.21**）  
* 响应式状态引擎中支持 `if-else` 语句的计算。（**1.30.21**）
* 新增函数 `truncate` 用于清空分布式表数据，但仍保留表结构。（**1.30.20**）
* 新增函数 `checkBackup `检查备份文件的完整性和正确性；新增函数 `getBackupStatus` 查询数据库备份和恢复任务详情。（**1.30.20**）
* 新增函数 `backupDB/restoreDB/backupTable/restoreTable`，用于备份恢复整库/表。（**1.30.20**）
* 新增配置项 `logRetentionTime`，设置系统日志的保留时间。（**1.30.20**）
* 新增函数 `triggerNodeReport`，强制触发 datanode 向 controller 汇报分区信息。（**1.30.20**）
* 新增函数 `getUnresolvedTxn` 查看当前进行中的事务决议任务状态。（**1.30.20**）
* `streamEngineParser` 支持用户自定义函数中嵌套因子的解析。（**1.30.20**）
* 新增函数 `conditionalIterate`，可通过条件迭代实现因子中的递归。仅可用于响应式状态引擎 (`createReactiveStateEngine`) 。（**1.30.20**）
* 新增函数 `stateMavg`，可计算基于历史结果的移动平均。仅可用于响应式状态引擎 (`createReactiveStateEngine`) 。（**1.30.20**）
* 新增函数 `stateIterate`，通过线性迭代实现线性递归。仅可用于响应式状态引擎 (`createReactiveStateEngine`) 。（**1.30.20**）
* 响应式状态引擎 (`createReactiveStateEngine`) 支持 `mmaxPositiveStreak`。（**1.30.20**）
* `createWindowJoinEngine` 参数 window=0:0 时，右表的计算窗口由左表相连两条数据的时间戳确定。（**1.30.20**）
* 新增函数 `sumbars`，支持统计向前累加到指定值的周期数。（**1.30.20**）
* 新增函数 `regroup`，按给定的行/列标签对矩阵进行分组聚合的操作。（**1.30.20**）
* 新增滑动窗口函数 `mifirstNot`，`milastNot`，用于计算窗口内第一个和最后一个非空值。（**1.30.20**）
* 新增函数 `loc`，通过标签或布尔向量获取矩阵指定的行和列的元素。（**1.30.20**）
* 新增函数 `til`，用于生成一个从 0 开始的连续整型序列。（**1.30.20**）
* 新增函数 `pack/unpack`，用于二进制字节流间的打包/解包。（**1.30.20**）
* 新增函数 `align`，将两个矩阵按照两个指定方式连接，并根据行列标签对齐。（**1.30.20**）
* JIT 支持使用索引向量或数据对访问向量。（**1.30.20**） 
* 新增配置项 `memLimitOfQueryResult` 和 `memLimitOfTaskGroupResult` 以限制查询结果和子查询结果的内存占用；新增函数getQueryStatus 用于监控查询过程的内存占用及执行进度等信息。（**1.30.19**）  
* 新增函数 `isPeak` 和 `isValley`，判断当前元素是否是相邻元素中的峰值/谷值。（**1.30.19**）
* 新增函数 `rowAt(X, Y)`，以 Y 为索引，逐行获取 X 中对应索引的元素。（**1.30.19**）
* 新增函数 `rowImin` 和 `rowImax`，逐行获取最值点的索引。（**1.30.19**）
* 新增机器学习相关函数 `gmm`，支持通过高斯混合模型来实现聚类算法。（**1.30.19**）
* 新增函数 `valueChanged`，通过比较当前元素和相邻元素，计算元素间的变化。（**1.30.19**）
* 新增函数 `msum2` 和 `tmsum2`，支持在滑动窗口内计算平方和。（**1.30.19**）
* 新增函数 `prevState` 和 `nextState`，以连续且值相同的元素作为状态标识，寻找当前元素相邻前/后一个状态的元素值。（**1.30.19**）
* 新增函数 `getSupportBundle`，返回系统基本的配置信息和数据库信息。（**1.30.19**）
* 新增函数 `topRange` 和 `lowRange`，统计序列中的当前值是前多少周期内的最大/小值。并在 ReactiveStateEngine 中支持了该函数。（**1.30.19**）
* 新增流数据引擎 dual-ownership reactive state engine (`createDualOwnershipReactiveStateEngine`)，支持按两种不同的分组方式分别应用不同的指标进行并行计算。（**1.30.19**）
* 引入新的表对象：跨进程共享内存表 IPCInMemoryTable，并新增四个相关函数 `createIPCInMemoryTable`, `loadIPCInMemoryTable`, `dropIPCInMemoryTable`，分别用于创建跨进程共享内存表，加载跨进程共享内存表，销毁跨进程共享内存表。跨进程共享内存表可用于在流计算场景下，使 DolphinDB 服务端与同一个物理机上的客户端程序间能够高效地传递数据。（**1.30.19**）
* 新增函数 `stretch`，将向量拉伸到指定长度。（**1.30.19**）
* 新增函数 `getTransactionStatus`，获取事务的状态。新增命令 `imtForceGCRedolog`，取消等待指定编号的事务回收。（**1.30.19**）
* 新增数据库运维模块 ops，包含一些用户常用的运维脚本，如：取消集群中未完成的作业，查看内存占用，删除未完成恢复的分区，关闭不活跃的会话等。（**1.30.19**）
* 新增函数 `setLogLevel` 动态调整 server log 级别。（**1.30.19**）
* 新增函数 `getRedoLogGCStat` 用于获取 redo log 垃圾回收的状态。（**1.30.19**）
* ReactiveStateEngine 支持 `cumPositiveStreak` 函数。（**1.30.19**）
* 新增 mmaxPositiveStreak 函数，计算在给定长度（以元素个数衡量）的滑动窗口内统计 X 中连续正数之和的最大值，并在响应式状态引擎中增加了对应的状态函数。（**1.30.19**）
* 新增函数 `cells`，使矩阵输出由参数 *row* 和 *col* 指定位置的元素值。（**1.30.18**）
* 新增函数 `randDiscrete`，支持按指定概率分布离散抽样。（**1.30.18**）
* 新增计算函数 `dynamicGroupCumsum` 和 `dynamicGroupCumcount`，并在响应式状态引擎中增加了对应的状态函数。（**1.30.18**）
* 新增函数 `createDistributedInMemoryTable` 支持创建分布式共享内存表。（**1.30.18**）
* 新增分级存储功能，可以将冷数据存储到低速硬盘或者对象存储（比如 Amazon S3）上，且这些冷数据只读不可写。（**1.30.18**）
* 新增配置项 maxDynamicLocalExecutor 限制本地动态执行线程的产生频率与数量上限。（**1.30.18**）
* 新增 `transaction` 语句，将对单个内存表（或共享内存表）操作的多个 SQL 语句封装为一个事务 （**1.30.18**）
* 新增函数 `getRecoveryWorkerNum` 获取当前用于 chunk 恢复的工作线程数。（**1.30.17**）
* 新增命令 `resetRecoveryWorkerNum` 动态修改用于 chunk 恢复的工作线程数。（**1.30.17**）
* 支持使用命令 `kill -15 $PID` 或集群 web 管理界面安全关机。（**1.30.17**）
* 新增运维函数 `imtUpdateChunkVersionOnDataNode`，修改数据节点上对应 chunkId 的版本号。维护集群中多副本数据之间，或数据节点与控制节点之间的版本一致性。（**1.30.17**）
* 函数 `replay` 支持多表回放到异构流数据表，并按照时间顺序输出。（**1.30.17**）
* 新增函数 `concatMatrix`，支持水平或垂直拼接多个矩阵。（**1.30.17**）
* 新增高阶函数 `firstHit` 和 `ifirstHit`，用于返回 *X* 中第一个满足条件的元素。（**1.30.17**）
* 新增函数 `getCurrentSessionAndUser`，获取当前 session 对应的 sessionID 和u serID。（**1.30.17**）
* 支持 SQL Join 的标准写法。（**1.30.17**）
* 新增 SQL 语句 `alter`，用于在已有的表中添加列。（**1.30.17**）
* 新增 SQL 语句 `create`，用于创建数据库或表。（**1.30.17**）
* 往内存表的时间列写入数据时，自动进行时间类型转换。（**1.30.16**）
* 支持表级别分区粒度，支持同一库中不同的表并发进行增删改操作。（**1.30.16**）
* 支持在线增量恢复，可以异步地进行节点数据恢复。 （**1.30.16**）
* SQL 语句增加标识 [HINT_EXPLAIN]，可以显示 SQL 的执行过程。（**1.30.16**）
* 支持管理和查询集群中的所有计算任务。（**1.30.16**）
* 新增函数 `streamEngineParser`，支持自动分解截面因子成多个内置流计算引擎的流水线。（**1.30.16**）
* 新增函数 `existSubscriptionTopic`，用于判断某一个订阅是否已经创建。（**1.30.16**）
* 新增函数 `createLookupJoinEngine`，支持将流数据表和流数据表、内存表或者分布式表（目前只支持维度表）做左连接。（**1.30.16**）
* 新增函数 `moveChunksAcrossVolume`，在增加新的 volume 后，用于转移旧 volume 的部分 chunk 到新 volume。（**1.30.16**）
* 新增 10 个 TopN 函数 `msumTopN`, `mavgTopN`, `mstdpTopN`, `mstdTopN`, `mvarTopN`, `mvarpTopN`, `mcorrTopN`, `mbetaTopN`, `mcovarTopN`, `mwsumTopN`，且 `createReactiveStateEngine` 引擎支持它们相应的状态函数。（**1.30.16**）
* 新增函数 `makeKey` 和 `makeOrderedKey`，可以将多个列合并成一个 BLOB 列，用作字典或集合的键值，其中 `makeOrderedKey` 的结果保留了多个字段的排序顺序。（**1.30.16**）
* 新增高阶函数 `aggrTopN`，用以计算根据排序列获取的前N行数据的聚合结果。（**1.30.16**）
* 新增高阶函数 `window` 和 `twindow`。与 `move` 与 `tmove` 类似，但适用于更通用的场景，对于窗口边界的处理稍有不同 。（**1.30.16**）
* 新增配置项 raftElectionTick，用以配置 raft 切换 leader 的心跳时间。同时新增函数 `setCacheEngineMemSize`, `setTimeoutTick`, `setMaxMemSize`, `setReservedMemSize` 和 `setMaxBlockSizeForReservedMemory` 支持在线修改对应的配置项。（**1.30.16**）
* 新增函数 `loadNpz`支持导入 numpy 的 npz 文件。（**1.30.16**）
* 新增函数 `suspendRecovery` 用于暂停 recovery 任务，新增函数 `resumeRecovery` 用于重启 `recovery` 任务。（**1.30.16**）
* 新增函数 `rowCorr`, `rowCovar`, `rowBeta`, `rowWsum`, `rowWavg`，可以对每行数据进行计算。（**1.30.16**）
* 新增 `fflush` 函数，帮助将缓存中的数据写入文件系统。（**1.30.16**）
* 支持匿名的聚合函数定义。(**1.30.15**)
* 新增配置参数 postStart，可以支持 postStart.dos 文件，用于启动 DolphinDB 时挂载定时任务。(**1.30.15**)
* 新增配置参数 reservedMemSize 和 maxBlockSizeForReservedMemory，当内存占用接近 maxMemSize 的时候，控制能够分配的内存块的最大尺寸，避免因 OOM 导致 crash。(**1.30.15**)
* 增加 `cumfirstNot`, `cumlastNot`, `mfirst`, `mlast` 等函数，以及在响应式引擎中实现它们的状态函数。(**1.30.15**)
* 新增函数 `oneHot`，用于做 one hot（独热）编码。(**1.30.15**)
* 新增 `setAtomicLevel` 命令，用于修改历史数据库的 atomic 参数，实现是否支持并发写入分布式表的分区。(**1.30.15**)
* 流计算引擎 ReactiveStateEngine, AnomalyDetectionEngine, SessionWindowEngine, DailyTimeSeriesEngine 和 TimeSeriesEngine支持高可用。(**1.30.14**)
* 新增功能：跨集群数据异步复制。(**1.30.14**)
* 新增函数 `covarMatrix` 和 `corrMatrix`，来计算 pairwise covariance 和 correlation，性能比直接使用高阶函数 cross 和 covar/corr 的组合快1~2个数量级。(**1.30.14**)
* 新增配置项 stdoutLog，当取值为 true 或1时，不再输出系统的日志到文件，而是输出到 stdout。(**1.30.14**)
* 新增高阶函数 `tmoving`，将一个对象按照时间窗口进行滑动计算。同时响应式状态引擎中实现高阶函数 `moving` 和 `tmoving` 对应的状态函数（state function）。(**1.30.14**)
* 新增函数 `runScript`，用于执行一段脚本。(**1.30.14**)
* 新增函数 `makeUnifiedCall`, `binaryExpr` 和 `unifiedExpr` 用于元编程。(**1.30.14**)
* 新增23个按时间滑动的窗口系列函数，包括 `tmove`，`tmfirst`，`tmlast`, `tmsum`, `tmavg`, `tmcount`, `tmvar`, `tmvarp`, `tmstd`, `tmstdp`, `tmprod`, `tmskew`, `tmkurtosis`, `tmmin`, `tmmax`, `tmmed`, `tmpercentile`, `tmrank`, `tmcovar`, `tmbeta`, `tmcorr`, `tmwavg`, `tmwsum`。并在响应式状态引擎中实现它们对应的状态函数。(**1.30.14**)
* 新增函数 `sma`, `wma`, `dema`, `tema`, `trima`, `talib`, `talibNull` 和 `linearTimeTrend`。(**1.30.14**)
* 新增函数 `countNanInf` 和 `isNanInf`，统计 scalar, vector 或 matrix 中包含的 NaN 和 Inf 值的数量。(**1.30.14**)
* 增加流数据 window join 引擎。(**1.30.14**)
* 时间序列聚合引擎新增优化以下函数：`count`, `firstNot`, `ifirstNot`, `ilastNot`, `imax`, `imin`, `lastNot`, `nunique`, `prod`, `quantile`, `sem`, `sum3`, `sum4`, `mode` 和 `searchK`。(**1.30.14**)
* 增加函数 `getConfigure`，当传入一个 key 时，返回该配置项的配置信息。如果参数为空，则返回所有配置项目信息。(**1.30.14**)
* 新增命令 `clearCachedModules`，可以强制清除缓存的 module。当缓存清除后，执行 use 语句时，会重新从文件加载 module。这个方法可以在不重启节点的情况下，重新加载已经更新的 module。只有 admin 才有权限执行这个命令。(**1.30.14**)
* 新增按行聚合函数 `rowSize`, `rowStdp`, `rowVarp`, `rowSkew` 和 `rowKurtosis`。(**1.30.14**)
* 新增 `percentileRank` 函数，计算一个值在一个向量中的百分位。(**1.30.13**)
* 新增 `zigzag` 函数，计算数据中的极值点。(**1.30.13**)
* 新增 `lowDouble` 和 `highDouble` 函数，用于将 point 和 complex 等16字节的数据类型分解成高位8字节的 DOUBLE 类型和低位8字节的 DOUBLE 类型。(**1.30.13**)
* 新增 `rdp` 压缩算法函数。(**1.30.13**)
* 新增计算加权最小二乘回归函数 `wls`。(**1.30.13**)
* 新增支持流数据 equal join 引擎。(**1.30.13**)
* 新增 `ifNull` 和 `ifValid` 函数。(**1.30.13**)
* 新增配置 enableConcurrentDimensionalTableWrite，用于开启维度表并行写入。(**1.30.13**)
* 提供 `isDataNodeInitialized` 函数用于查看数据节点是否已经完成初始化。(**1.30.12**)
* 函数 `replay` 回放历史数据时，支持一种新的模式：即多个 schema 相同的数据源按照事件的时间顺序回放到同一个流表. (**1.30.12**)
* 新增函数 `distance` 计算两个用经纬度表示的点之间的距离。(**1.30.12**)
* 流数据订阅端的计算引擎支持高可用。(**1.30.12**)
* 新增函数 `denseRank`, `rowDenseRank`。(**1.30.11**)
* 替换 license 后，支持不停机在线更新。(**1.30.11**)
* Agent 可自动启动数据节点，可在数据节点意外关闭时把它重启，controller.cfg 中新增配置项 `datanodeRestartInterval`。(**1.30.11**)
* 内存表字段中支持超长字符串（blob）。(**1.30.11**)
* 支持实时流数据 join，新增函数 `createAsofJoinEngine` 和 `appendForJoin`。**(1.30.10)**
* 增加 `getConnections` 函数，获取节点当前所有连接信息。**(1.30.10)**
* `interval` 函数新增支持在指定的范围内进行插值。**(1.30.10)**
* 增加高阶函数 `unifiedCall`，将函数的参数集以tuple方式传入。**(1.30.10)**
* 新增 `spearmanr` 和 `mutualInfo` 两个相关性的计算函数。(**1.30.9**)
* 新增函数 `createDailyTimeSeriesEngine`，用于创建支持会话的时间序列聚合引擎。每个会话的结束点和开始点可以做一些特殊处理。 (**1.30.9**)
* 增加函数 `getStreamTableFilterColumn` 用于取得流数据 Filter 列信息。(**1.30.9**)
* 新增函数 `varp` 和 `stdp`。(**1.30.9**)
* `CrossSectionalEngine` 新增参数 lastBatchOnly。(**1.30.8**)
* `createReactiveStateEngine` 增加了可选参数 keepOrder。(**1.30.8**)
* 支持新数据类型 DURATION， 表达时间范围更加简练。(**1.30.7**)
* 支持节点间通过压缩方式传输数据。(**1.30.7**)
* `temporalAdd`, `dailyAlignedBar`, `bar`, `wj`, `pwj` 函数支持 DURATION 类型参数。(**1.30.7**)
* `keyedStreamTable` 支持多个 key 列。(**1.30.7**)
* SQL 提供 `interval` 关键字，支持插值查询。(**1.30.7**)
* 修改 `upsert!` 函数，支持对 DFS 表（包括维度表和分区表）进行修改。(**1.30.6**)
* 支持使用 SQL update 和 delete 语句修改 DFS 表（包括维度表和分区表）。(**1.30.6**)
* 新增函数 `sqlUpdate` 和 `sqlDelete`，动态创建 SQL update 和 delete 语句。(**1.30.6**)
* 新增函数 `createSessionWindowEngine` 用于创建流数据会话窗口引擎。(**1.30.6**)
* 支持客户端数据压缩上传到服务端，也支持数据压缩后输出到客户端。(**1.30.6**)
* 支持新的数据类型：复数（COMPLEX）和点（POINT）。使用函数 `complex` 和 `point` 分别构造上述两种数据类型。(**1.30.3**)
* 新增函数 `getRequiredAPIVersion`，以配合 API 检查是否需要更新版本来兼容 DolphinDB server。(**1.30.3**)
* 响应式状态引擎和时间序列聚合引擎支持快照，用于保存这些引擎的状态，以便在流计算出现异常时，快速从上一个快照处恢复。(**1.30.3**)
* 新增函数 `mskew`, `mkurtosis`, `mvarp`, `mstdp`, `cumvarp`, `cumstdp`，并且在响应式状态引擎中支持上述函数。(**1.30.3**)
* 新增函数 `winsorize`。(**1.30.3**)
* 新增高阶函数 `byRow`，使得一个列式函数，可用于矩阵按行计算。(**1.30.3**)
* 内置的流数据计算引擎包括时间序列聚合引擎、横截面引擎、异常检测引擎和响应式状态引擎，支持多个引擎串联。(**1.30.3**)
* 新增响应式状态引擎（reactive state engine）用于流计算。相关的函数包括 `createReactiveStateEngine` 和 `warmupStreamEngine`。(**1.30.2**)
* 新增函数 `ema`, `mskew`, `mkurtosis` 和 `mslr`。(**1.30.2**)  
* 新增数据结构：索引矩阵（indexed matrix）和索引序列（indexed series），用于面板数据的处理。索引矩阵之间、索引序列之间、以及索引矩阵和索引序列之间的二元操作，支持按行列标签自动对齐。(**1.30.1**)
* 新增函数`panel`，`indexedSeries`, `setIndexedMatrix!`, `setIndexedSeries!`, `isIndexedMatrix`, `isIndexedSeries`，`dropna`，`resample`，`asFreq`，`merge`等用于处理索引矩阵和索引序列。(**1.30.1**)
* 新增函数`renameTable`，允许分布式的维度表和分区表改名。(**1.30.1**)
* 新增高阶函数`withNullFill`。(**1.30.1**)
* 新增权限 DB_OWNER。拥有该权限的用户可以创建数据库并进行管理。(**1.30.1**)
* 新增函数 `upsert!` 向键值表或索引表中添加或更新记录。(**1.30.1**)
* `schema` 函数增加了分区列类型（partitionColumnType）的输出。(**1.30.1**)
  
### 改进

* 自定义函数支持空的 tuple（[]）作为参数默认值。（**1.30.22.1**）
* 在使用 `loadText` 函数时，添加对用户权限的检查机制。（**1.30.22.1**）
* 记录用户权限发生变更的信息到日志中。（**1.30.22.1**）
* `resample` 函数支持输入具有非严格递增行标签的矩阵。（**1.30.22.1**）
* 优化 any vector 拼接的行为。（**1.30.22.1**）
* 在状态引擎中，可以指定一个三元函数作为 `accumulate` 的参数。（**1.30.22.1**）
* `streamEngineParser` 增加参数校验：若 *triggeringPattern*='keyCount'，则 *keepOrder* 必须为 true。（**1.30.22.1**）
* 配置项 `localExecutors` 和 `maxDynamicLocalExecutor` 停止使用。（**1.30.22**）
* 响应式状态引擎新增支持状态函数 `window` 和 `percentChange`。（**1.30.22**）
* 支持多个分区表之间进行连接。（**1.30.22**）
* 优化了通过 `dropTable` 函数删除一个具有大量分区的表的性能。（**1.30.22**）
* SQL 相关的关键词支持全部大写或全部小写。（**1.30.22**）
* 支持使用逗号（,）操作符实现 `CROSS JOIN` 连接。例如：`select * from table1, table2`。（**1.30.22**）
* SQL 语句支持换行。但由多个词组成的关键字，比如 `ORDER BY`, `GROUP BY`, `UNION ALL`, `INNER JOIN` 等不可拆分换行。（**1.30.22**）
* SQL中支持运算符 `<>`，行为等价于 `!=`。（**1.30.22**）
* SQL 支持 `NOT LIKE` 关键字。（**1.30.22**）
* `sqlDS` 作用于对按 DATEHOUR 值分区的分布式表时，按日期进行过滤查询时，没有进行分区剪枝。（**1.30.22**）
* `getRecoveryTaskStatus` 函数的返回值 Status 中的 Finish 改成 Finished，Abort 改成 Aborted。（**1.30.22**）
* `HINT_EXPLAIN` 在 `GROUP BY` 部分，当分组算法为 “sort” 时，添加了 *inplaceOptimization* 和 *optimizedColumns* 字段，显示相关优化信息（**1.30.22**）
* `rename!`, `replaceColumn!`, `dropColumns!` 函数不再对列名大小写敏感。（**1.30.22**）
* `lasso`, `elasticNet` 新增参数 *swColName* 和 *checkInput*，分别用于指定样本权重列和是否对参数进行合法性验证。`ridge` 新增参数了 *swColName*。（**1.30.22**）
* `qclp` 新增参数 *x0*, *c*, *eps* 和 *alpha*，分别用于指定绝对值的约束条件、求解精度和松弛参数。（**1.30.22**）
* `loadText`，`pLoadText`, `extractTextSchema` 等函数，支持加载一条记录中包含多个换行符的数据文件。（**1.30.22**）
* 函数 `loadText`, `pLoadText`, `loadTextEx`, `textChunkDS`, `extractTextSchema` 的 *delimiter* 参数可以指定多个字符。（**1.30.22**）
* 通过 `loadTextEx` 导入数据表时，当导入的数据表各列类型与数据库表的类型不匹配时，增加报错提示。（**1.30.22**）
* 如下 TopN 系列函数新增参数 *tiesMethod*，可以指定排序中存在多个相同值时的处理方式：`mstdTopN`, `mstdpTopN`, `mvarTopN`, `mvarpTopN`,`msumTopN`, `mavgTopN`, `mwsumTopN`, `mbetaTopN`, `mcorrTopN`, `mcovarTopN`。（**1.30.22**）
* 提升 `knn` 函数的预测速度。（**1.30.22**）
* 时序聚合引擎（`createTimeSeriesEngine` 和 `createDailyTimeSeriesEngine`）支持输出 array vector 类型数据列。（**1.30.22**）
* 优化状态响应引擎 (ReactiveStateEngine) 中 `moving` 函数性能。（**1.30.22**）
* 异常检测引擎（`createAnomalyDetectionEngine`）的 *keyColunm* 参数支持指定多个字段。（**1.30.22**）
* `createWindowJoinEngine` 和 `createAsOfJoinEngine` 新增参数 *sortByTime*，用于设置数据是否在全局范围内按时间顺序进行输出。（**1.30.22**）
* 支持通过 `share` 函数或语句将流计算引擎共享，以支持对其并发写入。
* windowJoin 引擎（`createWindowJoinEngine`）因插入数据类型不对（要求插入 SYMBOL 类型，而实际插入 INT）导致插入失败时，增加报错提示。（**1.30.22**）
* JIT 支持运算符 join（`<-`）。（**1.30.22**）
* JIT 版本的 `isort` 函数，支持由多个等长向量组成的元组作为参数。（**1.30.22**）
* JIT 中 `if` 表达式支持使用运算符 `in`。（**1.30.22**）
* JIT 中向量支持使用布尔数组进行索引。（**1.30.22**）
* 支持脚本内一行有多段如 /\**/ 的注释。（**1.30.22**）
* `stringFormat` 函数新增以下功能：支持类型匹配，格式化对齐，指定小数输出位数，进制转换。（**1.30.22**）
* `concat` 函数的第二个参数可以为空。（**1.30.22**）
*  `take` 函数支持输入元组或表；`stretch` 函数支持输入矩阵或表。（**1.30.22**）
*  函数 `in` 和 `find` 支持单列 table。（**1.30.22**）
*  配置项 *moduleDir* 指定为相对目录时，系统寻找模块的默认路径为 *homeDir/modules*。（**1.30.22**）
*  `in`, `binsrch`, `find`, `asof` 函数的返回值形式与入参 Y 的形式保持一致。（**1.30.22**）
*  当 `rank` 输入 Any Vector 类型参数时，增加报错提示。（**1.30.22**）
* 支持 `distinct` 关键字，用于对单个或多个字段去重。暂时不支持其与 `group by`, `context by` 或 `pivot by` 配合使用。（**1.30.21.6**）
* `createTimeSeriesEngine`, `createDailyTimeSeriesEngine` 的耗时统计参数由 "outputElapsedInMicroseconds" 修正为 "outputElapsedMicroseconds"。（**1.30.21.4**）
* `getSessionMemoryStat` 函数返回的 createTime 和 lastActiveTime 字段，由零时区时间改为当前时区的时间。（**1.30.21.4**）
* DolphinDB 的 `between and` 语句与标准 SQL 的 `between and` 语句兼容。（**1.30.21.4**）
* 添加了与创建、加载、删除跨进程共享内存表（IPCInMem 表）相关的日志信息，以便更好地跟踪和调试这些操作。（**1.30.21.4**）
* `getClusterDFSTables` 仅显示对用户可见的表。（**1.30.21.3**）
* `subscribeTable` 的 *handler* 参数支持指定为共享内存表、共享键值表或共享索引表。（**1.30.21.3**）
* `cut` 函数支持切分表和矩阵。（**1.30.21.3**）
* 有序字典支持单目窗口函数 `cumsum` 等。（**1.30.21.3**）
* 元数据文件添加 checksum。（**1.30.21**）    
* 清空由 controller 转变为 follower 的控制节点的恢复事务，以避免 follower 节点的恢复日志过多地占用磁盘空间。（**1.30.21**）    
* 支持在日志文件中输出备份恢复过程的相关信息。（**1.30.21**）
* 函数 `interval` 新增参数 `closed`, `label`, `origin`。（**1.30.21**）    
* 函数 `getRecentJobs` 新增返回值字段 clientIp 和 clientPort 用于获取客户端的 IP 和 Port 信息。（**1.30.21**）    
* 函数 `ema` 新增参数 `warmup`，配置后前 *window* - 1 个窗口也会计算输出。（**1.30.21**）    
* 高阶函数 `accumulate` 和 `reduce` 支持输入一元函数和三元函数。（**1.30.21**）    
* 响应式状态引擎和时间序列聚合引擎新增参数 `outputElapsedMicroseconds` 用于计算耗时统计。（**1.30.21**）    
* 函数 `rank` 和 `rowRank` 新增参数 `precision`，用于设置排序值的精度。（**1.30.21**）    
* 函数 `groups` 参数 `mode` 支持 "vector", "tuple"。（**1.30.21**）    
* 函数 `linearTimeTrend` 支持对矩阵和表的计算。（**1.30.21**）    
* 对高阶函数做了以下修改：（**1.30.21**）
  * 支持高阶函数迭用， `eachLeft`, `eachRight`, `eachPre`, `eachPost`, `reduce` 新增参数 `consistent`，支持子任务结果的类型和形式可以不一致。
  * 在默认情况下，`eachLeft`, `eachRight`, `eachPre`, `eachPost`, `cross`, `accumulate`, `reduce` 不再根据第一个子任务的计算结果来决定输出对象的形式，而是根据所有结果来决定输出对象的形式。
  * `accumulate` 计算规则做了调整。若输入参数为矩阵，不再根据每一行来处理空值，而是在每次迭代中按列处理。
* 函数 `rank` 和 `rowRank` 的参数 `tiesMethod` 支持使用 first 按照原数据的顺序排名。（**1.30.21**）    
* 函数 `cut` 支持将数据拆分成标量。（**1.30.21**）   
* 函数 `rowAt` 支持以数组向量为索引。（**1.30.21**）    
* 矩阵支持以 slice 方式取行元素。（**1.30.21**）    
* 取消了创建 tuple 时其 size 不能超过1048576的限制。（**1.30.21**）   
* 用函数 `array` 创建 tuple 时支持默认值为 STRING 类型。（**1.30.21**）    
* 函数 `memSize` 可以显示 any vector 的内存占用。（**1.30.21**）
* 支持通过多线程 merge 不同分区的结果。降低了当列数较多的情况下查询最后数据合并的耗时。（**1.30.21**）    
* `getSessionMemoryStat` 返回值增加了缓存状态的打印，包含维度表，表数据，cache engine，字典编码等缓存占用信息，以及流数据发布和订阅队列深度的信息。（**1.30.21**）    
* 函数 `setColumnComment` 支持为 mvccTable 增加注释信息。（**1.30.21**）  
* 矩阵支持混合使用 pair 和 vector 作为行列索引的值。（**1.30.21**）    
* 支持在数据节点上调用权限相关的函数。（**1.30.21**）    
* 调整了 `regularArrayMemoryLimit` 实际生效的参数值为配置值与 maxMemSize/2 中的较小值。（**1.30.21**）    
* `streamFilter` 的参数 `condition` 支持传入内置函数。 （**1.30.21**）   
* 函数 `replay` 新增参数 `sortColumns`，相同回放时间戳的数据将根据该参数指定的字段进行排序。（**1.30.21**）    
* 支持同构 N 对 1 回放和异构流表回放数据源时的数据源的自动对齐。（**1.30.21**）
* 在流计算引擎中调用滑动窗口函数时，window 的上限修改为 102400。（**1.30.21**）
* 优化了异构流表的回放性能。（**1.30.21**）    
* `streamEngineParser` 支持解析 `byRow` 嵌套 `contextby` 函数，放入横截面引擎进行计算。（**1.30.21**）
* 响应式状态引擎使用 moving 函数时，支持计算数组向量。（**1.30.21**）    
* 优化 `createWindowJoinEngine` 在 *window* = 0:0 时的计算延迟。（**1.30.21**）    
* 支持在流计算中使用高阶函数 `accumulate`。（**1.30.21**）    
* 优化了 `streamEngineParser` 的解析性能。（**1.30.21**）
* 共享表 append/insert into 语句支持通过 `transaction` 语句实现事务。（**1.30.21**）    
* 支持使用 `select` 子句中的列别名或者新创建的列作为 where 的过滤条件。（**1.30.21**）    
* 优化了当 `pivot by` 最后一列为分区列时的性能。（**1.30.21**）    
* `context by` 支持 matrix 和 table 的输入形式。（**1.30.21**）    
* 提高了`context by` 和 `group by` 的查询性能。（**1.30.21**）    
* 优化了 `lsj` 在大数据量下的性能。（**1.30.21**）    
* 支持 SQL 语句 where 条件里时间类型可以自动转换为 interval 分组的时间类型。（**1.30.21**）
* 为兼容标准 SQL，对部分函数行为做了调整：（**1.30.21**）  
  * 通过 `join` 函数进行连接时，必须为临时表指定表名。
  * `distinct` 语句返回的结果列列名会在原始列名前加“distinct_”。
  * `in` 语句后跟单列表，而无需将其转换为向量。
* `func` 为内置函数名。（**1.30.21**） 
* 以 `x[start:end]` 的形式访问 array vector 的结果发生变化。如果 end>size(x)，不再抛出异常，而是将超出范围的位置填充 NULL。（**2.00.9**） 
* `contextSum2` 函数传入 array vector 时，会抛出异常而不是返回空值。（**2.00.9**）
* 在定义包含特殊符号的字符串时，使用双引号（""）来包裹字符串，而不是使用反引号（`）。（**1.30.21**）
* `interval` 函数增加校验，当 X 输入数据为整型数据时，不能指定 explicitOffset=true。（**1.30.21**）
* 改进了函数 `getSystemCpuUsage` 的返回值。（**1.30.21**）  
* 改进了权限管理功能，包括（**1.30.21**）：    
    * 新增了更细粒度的表权限（TABLE\_INSERT/TABLE\_UPDATE/TABLE\_DELETE），以及库权限（DB\_INSERT/DB\_UPDATE/DB\_DELETE）。        
    * 修改了 DB\_MANAGE 的权限，不再支持创库，只支持对库进行 DDL 级别的操作管理。        
    * 修改了 DB\_OWNER 的权限，支持用户创建指定前缀的库，且会为 admin 用户自动赋予 DB\_OWNER 权限。       
    * 增加以下函数权限校验：getAllDBs, getClusterDFSDatabases, getDFSDatabases, getDFSTablesByDatabase，只有拥有 DB_MANAGE 或 DB_OWNER 权限的用户才能调用。        
    * 新增了权限类型 QUERY\_RESULT\_MEM\_LIMIT，TASK\_GROUP\_MEM\_LIMIT 用于约束用户查询内存的上限。        
    * 修改了 DDL/DML 操作的权限校验机制。    
    * 增加参数校验：
      * 当 objs 的颗粒度与 accessType不匹配时，会报错。
      * 当赋予 TABLE_READ/TABLE_WRITE/DBOBJ_*/VIEW_EXEC 权限时，会检查对应的对象（DB/table/functionView）是否存在，如果不存在会报错。
      * 当对象（DB/table/functionView）被删除时，会回收对应的权限。如果再次创建同名的 db/table/functionView，则需要重新赋予权限。
      * 当 table 改名后，对应的权限依然保留。
    * 如果某个用户 grant 了某个表的权限，deny 了另一个表的权限，则升级到新版本后，该用户会拥有所有表的这个权限。
    * 权限管理相关函数可以在数据节点上执行。
* 使用 JIT 来增强流数据引擎中自定义函数的性能。（**1.30.21**）    
* JIT 支持 ratio operator。（**1.30.21**） 
* JIT 支持 `sum`, `avg`, `count`, `size`, `min`, `max`, `iif` 等常用函数。（**1.30.21**）
* JIT 支持 `moving`。（**1.30.21**）
* `backup` 支持通过拷贝分区文件方式进行备份，且可通过 restore/migrate 进行恢复。（**1.30.20**）
* 调用 `dropDatabase` 删除数据库时，删除 database 所有相关的物理文件夹。（**1.30.20**）
* `saveText` 支持传入 SQL 元代码，支持并行读取分布式表数据并存入磁盘。（**1.30.20**）
* 使用宏变量<ALIAS>为单个节点配置 volumes 时增加错误提示。（**1.30.20**）
* `replayDS` 函数的 *timeRepartitionSchema* 参数支持更多时间类型。（**1.30.20**）
* 优化 window join 引擎垃圾回机制。（**1.30.20**）
* 响应式状态引擎（`createReactiveStateEngine`）中包含自定义的相同表达式时不再重复计算。（**1.30.20**）
* 新增加 HINT_VECTORIZED 来启用 vectorizedGrouping。（**1.30.20**）
* 优化 `rolling` 函数的计算性能。（**1.30.20**）
* `getBackupList` 返回的表增加字段 *updateTime* 和 *row*，分别记录分区最近一次修改时间和分区行数信息。（**1.30.20**）
* `getBackupMeta` 返回的字典增加键值 rows 用于显示分区行数信息。（**1.30.20**）
* 为 31 个内置函数增加了权限控制，需登录或管理员权限才可调用。（**1.30.20**）
* `updateLicense` 时，若 license 授权类型改变，添加错误提示。（**1.30.20**）
* 对 vector 进行切片时，如果指定的索引超出向量的索引范围，则返回空值，不再抛出异常。（**1.30.20**）
* `subarray` 函数输入的范围越界，会返回空值，不再不抛出异常。（**1.30.20**）
* JIT 版本以索引方式读取 vector 某一元素时，若索引超过 index 的范围，用 NULL 填充。（**1.30.20**）
* crc32 算法优化。（**1.30.20**）
* 优化函数 `mrank`。（**1.30.20**）
* `toJson` 函数可转换的数据取消最大长度为1000的限制。（**1.30.20**）
* `max` 和 `min` 函数处理时间类型数据的行为由统一转换为长整型改为统一时间类型精度后比较。（**1.30.20**）
* `getClusterPerf(true)` 返回高可用集群下所有控制节点的信息，且返回值新增 isLeader 字段，显示该控制节点是否为 raft 组的 leader。（**1.30.19**）
* 调用 `restore`, `loadBackup`, `getBackupMeta` 等函数查询备份的表级分区数据时，partition 参数无需指定物理索引名。（**1.30.19**）
* `getRecoveryTaskStatus` 返回值新增 FailureReason 字段显示 recovery 任务失败的原因。（**1.30.19**）
* 优化 `backup` 备份数据时的压缩功能。（**1.30.19**）
* `cancelJob` 取消不存在的 job 时，系统不再抛出异常，而是打印错误信息到 log 文件。（**1.30.19**）
* 高可用流表可通过配置项 *persistenceWorkerNum* 指定其持久化到磁盘的工作线程数量。（**1.30.19**）
* `createSessionWindowEngine` 新增参数 *forceTriggerTime*，在 *useSystemTime=false* 时，强制触发最后一个窗口的计算输出。（**1.30.19**）
* `streamFilter` 分发普通流表时，*filter* 参数的 *condition* 支持输入布尔表达式的元代码。（**1.30.19**）
* `createEqualJoinEngine`, `createAsofJoinEngine` 和 `createLookupJoinEngine` 的 *metrics* 参数可以指定输出左表或右表的时间列/连接列。（**1.30.19**）
* `createReactiveStateEngine` 的 *keyPurgeFilter* 参数必须输入布尔类型的表达式，否则会报错。（**1.30.19**）
* `createLookupJoinEngine` 的 *metrics* 参数支持输入元组。（**1.30.19**）
* `dropStreamEngine` 若传入不存在不存在的引擎名称，则会抛出异常。（**1.30.19**）
* 当 group by 子句的时间粒度大于分区时间粒度时，优化了 select count(*) 语句的性能。（**1.30.19**）
* 修改 `rolling` 函数行为：（**1.30.19**）
  * `rolling` 的 *funArgs* 参数只能是向量或矩阵。如果需要输入多个向量，则用元组表示。
  * 如果输入参数中包含矩阵，根据矩阵的每一列分别计算，返回具有相同列数的矩阵。
  * *func* 的输出结果只能是标量或向量。如果输出结果是向量，则 *window* 与 *step* 必须相等。
  * 优化以下函数调用 `rolling` 函数时的计算性能：`cumsum`, `cummax`, `cummin`, `cumprod`, `mcount` 等。
* 流数据订阅时若无法获取持久化的 offset ，则从当前最新的开始订阅。（**1.30.19**）
* `createDailyTimeSeriesEngine` 的参数 *sessionEnd* 支持指定 00:00:00 作为当天的 24:00:00（即第二天的 00:00:00）。（**1.30.19**）
* `createReactiveStateEngine` 支持状态函数 `trueRange`；若 *metrics* 中指定返回常量的状态函数，则会抛出异常。（**1.30.19**）
* 提升了 SYMBOL 数据类型的读写性能。（**1.30.18**）
* 响应式状态引擎支持 `cummed` 和 `cumpercentile` 两个窗口函数。（**1.30.18**）
* 时序引擎（`createTimeSeriesEngine` 和 `createDailyTimeSeriesEngine`）新增参数 closed 来控制计算窗口的闭合边界。（**1.30.18**）
* `streamEngineParser` 的 keyColumn 参数取消对传入列名的大小写判断。（**1.30.18**）
* `createTimeSeriesEngine` 和 `createDailyTimeSeriesEngine` 新增参数 keyPurgeFreqInSec, 用于清理长时间无数据的分组。（**1.30.18**）
* 优化时序聚合引擎自定义函数性能。（**1.30.18**）
* 通过 `share` 语句将普通内存表共享时，增加共享表变量名校验。（**1.30.18**）
* `streamFilter` 支持对普通流表的列数据进行过滤、分发。（**1.30.18**）
* `createTimeSeriesEngine` 和 `createDailyTimeSeriesEngine` 的 metrics 支持对矩阵进行运算。（**1.30.18**）
* `resample` 函数的 rule 参数支持 "H", "L", "U", "min", "N" 以及 "S"，且新增了参数 closed，label 和 origin，可以对分组区间进行设置。（**1.30.18**）
* `replay` 函数在执行过程中如果报错，则直接抛出异常。（**1.30.18**）
* `tmbeta(T, X, Y, window)`, `cumbeta(X, Y)`, `rowBeta(X, Y)` 函数的参数位置调整为 `tmbeta(T, Y, X, window)`, `cumbeta(Y, X)`, `rowBeta(Y, X)`。（**1.30.18**）
* 在集群模式下，若 `redoLogDir` 配置为相同路径，则会报错。（**1.30.18**）
* `contextSum` 和 `contextSum2` 的输入参数是表时，只有对应列都是数值类型时才返回结果。（**1.30.18**）
* 优化了生成随机整数的性能。（**1.30.18**）  
* OLAP 引擎支持在 Windows 环境中开启 dataSync（即设置配置项 dataSync = 1）。（**1.30.17**）
* 函数 `subscribeTable` 新增可选参数 userId 和 password，系统在用户退出后自动尝试重新登录，保证订阅数据成功写入分布式表。（**1.30.17**）
* `getStreamingStat().subWorkers` 函数返回结果 throttle 统一为以毫秒为单位。（**1.30.17**）
* asof join 引擎支持指定多个连接列。（**1.30.17**）
* 横截面引擎（cross-sectional engine）新增参数 snapshotDir 和 snapshotIntervalInMsgCount 支持快照机制，新增参数 raftGroup 支持计算引擎高可用。（**1.30.17**）
* 新增函数 `getLeftStream` 和 `getRightStream` 支持 join 引擎的级联。（**1.30.17**）
* 若横截面引擎（cross-sectional streaming engine）和时间序列引擎（time-series streaming engine）参数 metrics 指定的函数有多个返回值，创建引擎时无需指定列名。（**1.30.17**）
* 新增命令 `addAccessControl` 对共享内存表（包括共享流表）或流数据引擎对象增加权限控制。（**1.30.17**）
* SQL `pivot by` 语句支持转换 UUID 类型的列。（**1.30.17**）
* `rowNo` 函数应用于 SQL 查询语句中时，将按照序列相关函数处理。（**1.30.17**）
* 函数 `ceil` 和 `floor` 结果的范围上限提升为2^53。（**1.30.17**）
* 若 SQL `pivot by` 语句最后一列为分区列，且 `select` 字段不包含聚合函数或序列函数，`pivot by` 语句性能提升近五倍。（**1.30.17**）
* 函数 `med` 参数支持 BOOL 类型。（**1.30.17**）
* 函数 `ema`, `kama` 和 `wma` 支持计算 BOOL 类型向量。（**1.30.17**）
* 调用 `slice` 函数时 ，当 rowIndex 或 colIndex 越界时，不再抛出异常，而是返回空值。（**1.30.17**）
* 调用 `spearmanr` 函数时，当 X 是矩阵，Y 是标量时，返回结果由 NULL 变成 0。（**1.30.17**）
* 调用 `mutualInfo` 函数时，当 X 是矩阵，Y 是标量时，返回结果由标量变成向量。（**1.30.17**）
* `listTables` 函数返回的表名调整为对大小写敏感。（**1.30.17**）
* 性能监控度量值（metrics） 若小于0，则返回0。（**1.30.17**）
* 命令 `addColumn` 新增列名支持以数字开头。（**1.30.17**）
* 函数 `loadText` 和 `loadTextEx` 导入 csv 文件时，第一行数据的读取上限为 256 KB。（**1.30.17**）
* 聚合函数、窗口函数和向量函数支持表作为输入参数。（**1.30.17**）
* 函数 `rand` 和 `norm` 的参数 count 支持输入数据对，用于指定生成矩阵的维度。（**1.30.17**）
* row 系列逻辑函数（`rowAnd`, `rowOr`, `rowXor`）支持输入整数。（**1.30.17**） 
* `bar` 函数新增参数 closed，用于指定分组包含左边界或右边界。（**1.30.17**）
* 滑动窗口函数的参数 X 是索引序列或索引矩阵，且 window 是正整数时，窗口按照索引滑动。（**1.30.17**）
* 自定义函数的参数可以分行书写，每行以逗号结束。（**1.30.17**）
* SQL `order by` 语句支持使用 as 改名前和改名后的字段。（**1.30.17**）
* 函数 `dailyAlignedBar` 参数 X 新增支持 SECOND, TIME, NANOTIME 类型向量。（**1.30.17**）
* 日级时间序列聚合引擎（daily time-series streaming engine）新增参数 forceTriggerSessionEndTime，用于指定强制触发 sessionEnd 的窗口。（**1.30.17**）
* 日级时间序列聚合引擎（daily time-series streaming engine）和时间序列聚合引擎（time-series streaming engine）修改参数 forceTriggerTime，未计算的窗口由计算结束后的最新数据触发。若设置了参数 fill，则同时填充无数据的窗口。（**1.30.17**）
* 使用赋值语句对内存表进行更新时，支持在行过滤条件中输入 BOOL 类型数组，形如：t[`y, t[`y]>0] = 0，其中 t 是表变量，y 是 t 的列名。（**1.30.16**）
* `upsert!` 函数新增可选参数 sortColumns，更新后的表可根据该指定列进行排序。（**1.30.16**）
* `cancelJob`, `cancelConsoleJob` 支持同时取消多个任务，且优化了集群阻塞时取消任务的性能。（**1.30.16**）
* `set` 支持 BLOB 类型的值。（**1.30.16**）
* `keyedStreamTable` 一次性批量插入多条键值相同的新记录，出现插入会失败。（**1.30.16**）
* 优化了 `atImin` 和 `atImax` 在 window join 中的使用性能。（**1.30.16**）
* `run` 命令新增可选参数 clean，控制是否清理当前 session 中的变量。（**1.30.16**）
* `wj` 函数，duration 支持设置为 y（年），M（月），B（工作日）。（**1.30.16**）
* `loadText` 支持字符串包含 ASCII 码为 0 的字符。（**1.30.16**）
* 支持对矩阵的条件赋值。（**1.30.16**）
* `getCompletedQueries` 函数和 `getRunningQueries` 函数返回值中添加 remoteIP 字段。（**1.30.16**）
* 配置项参数 stdoutLog*支持设置为 2，表示同时打印日志到标准输出和日志文件。（**1.30.16**）
* 异常检测引擎（anomaly detection engine）metrics 参数支持序列相关函数。（**1.30.16**）
* 时序引擎（time-series engine）windowSize 为向量时，各元素取值可相同。（**1.30.16**）
* 横截面引擎（cross-sectional engine）支持 keyColumn 输入一个向量。（**1.30.16**）
* 支持向流数据引擎插入 tuple 类型的记录。（**1.30.16**）
* 函数 `getStreamEngineStat` 返回的横截面引擎的统计信息添加了 memoryUsed 字段，可以查看横截面引擎所占内存。（**1.30.16**）
* `createAsofJoinEngine` 在 metrics 中支持输出右表的时间列。（**1.30.16**）
* 共享内存表（共享流表）新增可读不可写的权限管理。（**1.30.16**）
* 提升了控制节点高可用的稳定性。（**1.30.16**）
* 日志中新增打印 delete 和 update 操作信息。（**1.30.16**）
* 输出日志中流订阅任务的报错信息增加订阅主题。（**1.30.16**）
* 时序聚合引擎的 forceTriggerTime 参数计算规则修改，设置 updateTime 时，不再限制输出表为 keyedTable。(**1.30.15**)
* 横截面引擎（`createCrossSectionalEngine`）添加是否触发有效计算的开关。(**1.30.15**)
* 响应式状态引擎（`createReactiveStateEngine`）中增加支持 `mmad` 状态函数。(**1.30.15**)
* 时序聚合引擎新增对 nanotimestamp 的规整。(**1.30.15**)
* 共享流表新增权限控制。(**1.30.15**)
* getStreamingStat().subWorkers 的结果表中增加以下参数：msgAsTable, batchSize, throttle, hash, filter, persistOffset, timeTrigger, handlerNeedMsgId, raftGroup, 用于对流数据的监控。(**1.30.15**)
* `sma`, `wma`, `dema`, `tema`, `trima`, `t3`, `ma`, `talib`, `talibNull`, `linearTimeTrend` 增加流数据中对应的 state function。(**1.30.15**)
* 维度表支持并发 delete 操作。(**1.30.15**)
* STRING 类型支持直接与 NULL 进行比较。(**1.30.15**)
* 提升 `stdp`, `std`, `varp`, `var`, `skew`, `kurtosis`, `mskew`, `mkurtosis`, `tmskew`, `tmkurtosis`，以及 window join 中 `skew` 和 `kurtosis` 等函数的精度。(**1.30.15**)
* 高阶函数的第一个参数会被强制解析成函数。(**1.30.15**)
* UDF 函数支持 keyword arguments。(**1.30.15**)
* 新增对 `qr`, `ols`, `dot` 函数输入的校验，不允许行数或列数为0的矩阵作为输入。(**1.30.15**)
* 修改 `iif` 函数在 condition 包含空值时的行为。旧版本中 condition 元素包含空值被当作 false 处理。新版本中如果为空值，对应的结果也为空值。(**1.30.14**)
* `in` 函数的参数Y可以输入一个标量，支持为 NULL。当 Y 为无类型的 NULL 时，函数的返回值为 false 或每一个值都为 false 的 vector。(**1.30.14**)
* 矩阵进行 `accumulate` 等计算时放开8192行的限制。(**1.30.14**)
* 对维度表的并发执行写入、更新和删除等操作时，不再抛出事务冲突异常。(**1.30.14**)
* 数据节点重启时，会在日志中输出 redo log 回放的详细的进度。(**1.30.14**)
* SQL 语句中的 `interval` 功能（按时间聚合）移除 range 参数，同时增加可选参数 explicitOffset，默认值为 false。当该参数为 true 时，可以将第一个窗口的起始位置指定为 where 指定的窗口的起始位置。(**1.30.14**)
* `ols` 和 `wls` 在 mode 为2的时候，新增一个输出 Residual。对分布式表中的列，新增一个函数 `residual` 用于计算回归的残差。(**1.30.14**)
* 计算节点(computing node)支持客户端的所有操作。(**1.30.14**)
* SQL pivot 产生的表列名不再特殊处理，即直接使用 pivot 的值作为列名。(**1.30.14**)
* 函数 `rank`, `denseRank`, `cumrank`, `rowRank` 和 `rowDenseRank` 支持 percent 形式显示排名。(**1.30.14**)
* `kmeans` 支持自定义质心。(**1.30.14**)
* window join 增加对 `varp`, `stdp`, `prod`, `skew` 和 `kurtosis` 5个聚合函数的优化。(**1.30.14**)
* 支持对非数值类型进行 `unpivot`。(**1.30.14**)
* 部分滑动窗口函数系列如 `msum`，当输入数据为 indexed matrix 或 indexed series 时，窗口支持时间偏移窗口类型。(**1.30.14**)
* `database` 函数新增可选参数 atomic。当 atomic 取值为 'CHUNK' 时，写入操作只保准分区的原子性，此时也允许多个并发线程同时写入该数据库的同一个分区。(**1.30.14**)
* 函数 `createTimeSeriesEngine` 和 `createDailyTimeSeriesEngine` 新增参数 forceTriggerTime。(**1.30.13**)
* `scheduleJob` 的 scheduleTime 指定的任务之间的最小时间间隔缩短为5分钟。(**1.30.13**)
* `createTimeSeriesEngine` 和 `createDailyTimeSeriesEngine` 支持多个 keyColumn。(**1.30.13**)
* 函数 `upsert!` 的 ignoreNull 字段支持分布式表。(**1.30.13**)
* 函数 `parseExpr` 新增可选参数 modules 和 overloadedOperators，用于加载模块，且支持使用字典来给表达式中的变量赋值。(**1.30.13**)
* `sql` 函数新增可选参数 exec，支持生成 exec 语句。(**1.30.13**)
* `temporalAdd` 支持增加与减去工作日（BusinessDay），支持时间类型 DATEHOUR。(**1.30.13**)
* SQL group by 子句中的 `interval` 函数支持 step 参数，以滑动窗口的方式计算聚合结果。(**1.30.13**)
* `delete` 语句支持 `map` 子句，将 `delete` 语句下发到各分区执行。(**1.30.13**)
* 用户自定义函数的输入参数支持默认值。(**1.30.13**)
* 时序聚合引擎支持高可用。(**1.30.13**)
* `sql` 函数中当参数 groupFlag 为 PIVOTBY 时，参数 groupBy 支持选择多列。(**1.30.13**)
* 响应式状态引擎（`createReactiveStateEngine`）新增字段keyPurgeFilter和keyPurgeFreqInSecond，以支持响应式状态引擎自动清理key。(**1.30.13**)
* 响应式状态引擎（`createReactiveStateEngine`）支持输出结果到分布式表和流数据表，支持接受来自replay的输入。(**1.30.13**)
* Windows 安装包的 dolphindb.cfg, controller.cfg, cluster.cfg 默认配置项中移除 redolog 配置参数。(**1.30.13**)
* 改进 redo log 的回放性能。在有大量小事务的情况下，性能有10倍以上的提升。(**1.30.13**)
* 与标准 SQL 兼容，当 select 子句中包含的列与分组字段（group by）重名时，不再抛出异常。(**1.30.12**)
* 放开 API 和 GUI 提交脚本长度不能超过64K的限制。(**1.30.12**)
* `window join` 的聚合指标支持以元组的方式输入，也即元组的每一个元素表示一个聚合指标。(**1.30.12**)
* 横截面引擎（`createCrossSectionalEngine`）收到的数据中出现乱序时则丢弃乱序数据。(**1.30.12**)
* `setStreamTableFilterColumn` 支持高可用流表。(**1.30.12**)
* `addVolumes` 函数增加了校验，不允许在控制节点上执行。(**1.30.12**)
* 优化 `skew`, `kurtosis` 函数在时间序列聚合引擎中使用时的性能。(**1.30.11**)
* 优化时间序列聚合引擎在 useSystemTime=true 时的性能。(**1.30.11**)
* `createTimeSeriesEngine`, `createCrossSectional`,`createDailyTimeSeriesEngine`, `createAnomalyDetectionEngine`, `createSessionWindowEngine` 支持输出结果表为分布式表。(**1.30.11**)
* 横截面引擎（`createCrossSectionalEngine`）新增可选参数 contextbycolumn 作为分组字段，如果设置了该参数，按照分组字段来做计算。(**1.30.11**)
* server log 中重新规划输出日志，将一部分事务处理细节信息归入 DEBUG 类型。避免日志增长过快。(**1.30.11**)
* `haStreamTable` 支持多个 keyColumn。(**1.30.10**)
* `createTimeSeriesEngine`, `createDailyTimeSeriesEngine`, `createCrossSectionalEngine` , `createAnomalyDetectionEngine`, `createSessionWindowEngine` 的 metrics 参数支持 tuple。(**1.30.10**)
* 新增配置参数 useHardLink，在 `sqlUpdate` 时，可以不使用 hardlink。(**1.30.10**)
* 优化 ContextBy 搭配 `limit` 使用的性能。(**1.30.10**)
* `createTimeSeriesEngine` 和 `createDailyTimeSeriesEngine` 支持指标中指定各自的 fill 方法。(**1.30.10**)
* 异常检测引擎（`createAnomalyDetectionEngine`）的 outputTable 的时间列与 dummyTable 不一致时抛出异常提示。(**1.30.10**)
* 分布式表中使用 `skew` 和 `kurtosis` 时支持偏差校正。(**1.30.9**)
* 同一个 update 语句对同一列进行了重复更新时，会抛出异常提示。(**1.30.9**)
* 时间聚合引擎支持 timeColumn 指定2列，比如同时指定 date 和 time 列。(**1.30.9**)
* `sqlUpdate` 函数 where 条件中允许调用函数。(**1.30.9**)
* `firstNot` 和 `lastNot` 用于分布式表时，支持指定第2个参数。(**1.30.9**)
* `tableInsert` 往分布式表写入数据时，返回值从写入记录数改为成功写入的记录数。(**1.30.9**)
* 若由于数据在分区之外而没有成功写入，会在日志中记录 warning。(**1.30.9**)
* 高可用流表的引用变量使用 `undef` 取消定义后，仍然可以通过 `dropStreamTable` 删除该表。 (**1.30.9**)
* 针对多列宽表进行 SQL 性能的优化。(**1.30.8**)
* 响应式状态引擎（`createReactiveStateEngine`）支持指定多个 keyColumn。(**1.30.8**)
* 横截面引擎（`createCrossSectionalEngine`）的指标支持聚合和非聚合混用。(**1.30.8**)
* maxConnections 默认值改成512。(**1.30.7**)
* 函数 `createTimeSeriesAggregator` 改名为 `createTimeSeriesEngine`，原名作为别名。(**1.30.7**)
* 改进了部分应用（partial application）的显示，除了显示函数名称，也会显示已经固定的参数。(**1.30.6**)
* 对时间类型的分区字段进行剪枝时，支持在分区字段上使用相应的时间函数（目前支持 `date`, `month` 和 `datahour` 函数），方便用户操作。例如，数据库在时间维度上按日期（DATE 类型）进行分区，数据表的分区字段是 TIMESTAMP 类型，允许在时间列上先使用 `date` 函数再进行过滤，比如：date(time) = 2021.03.02。(**1.30.6**)
* 数据表按照时间类型字段进行值分区或者范围分区时，根据 where 子句中的过滤条件剪枝（如果所涉及分区的时间范围必然满足过滤条件，则可以在该分区的子查询上删除该过滤条件），改进查询性能。(**1.30.6**)
* 修改了 cache engine 的回收算法，提升了事务回收的效率，避免了不必要的 OOM。(**1.30.6**)
* 流数据时间序列聚合引擎增加可选参数 fill，可选的 fill 方法包括 'none', 'null' 和 'ffill'。默认值是 'none'，即某一个 key 在某个时间窗口中没有数据时，不输出任何结果。(**1.30.6**)
* 函数 `compress` 和 `decompress`支持 table 类型。(**1.30.6**)
* 单个事务涉及的元数据大小从最大16MB增加到128MB，避免出现一些大表不能删除的情况。(**1.30.6**)
* 异常检测引擎（`createAnomalyDetectionEngine`）支持快照（snapshot）(**1.30.6**)
* 函数 `createCrossSectionalAggregator` 改名为 `createCrossSectionalEngine`，原名作为别名。(**1.30.6**)
* 调整了系统自动检查日志文件大小的频率，避免日志大小超过设定值。(**1.30.3**)
* 画图函数 `plot` 新增可选参数 stacking。目前线状图（line chart，柱状图（bar chart）和面积图（area chart）支持该参数。(**1.30.3**)
* 函数 `subscribeTable` 的可选参数 offset 指定为-2时，若找不到持久化的 offset，不再抛出异常，而是用-1取代，即从最新的数据开始订阅。(**1.30.3**)
* windows 版本的 cpu 绑定，上限从32核增加到64核。(**1.30.3**)
* 调用函数 `addMetrics` 为时间序列聚合引擎动态增加指标时，如果 windowSize 和原先的定义不同，系统报异常。(**1.30.3**)
* `subscribeTable` 函数的 filter 参数，在值过滤的基础上增加了哈希过滤和范围过滤。(**1.30.3**)
* 横截面引擎（`createCrossSectionalEngine`）在支持聚合函数的基础上，增加对向量化函数的支持。(**1.30.3**)
* 时序聚合引擎支持在一个引擎中使用多个不同长度的窗口。(**1.30.3**)
* window join 的自定义指标函数支持多个返回值。(**1.30.2**)
* `concat` 函数拼接的字符串长度超过65535或字符串内包含 ASCII 值0，返回值将自动转化为 BLOB 类型。(**1.30.2**)
* 时间序列聚合引擎的自定义指标函数支持多个返回值，同时也支持接受带有别名的指标，例如：avg(price) as price。(**1.30.2**)
* 优化 SYMBOL 类型的数据序列化/反序列化过程。该优化提升了 DolphinDB 数据节点之间以及数据节点和API之间传输 SYMBOL 类型数据的性能，提升约有5~10倍。(**1.30.1**)
* 增强了并行作业和分布式作业的稳定性。(**1.30.1**)
* 数据结构支持行数或列数为0的矩阵类型。(**1.30.1**)
* 函数 `subscribeTable` 新增可选参数 timeTrigger，支持定时触发消息处理函数。(**1.30.1**)
* 长度超过65535个字节的字符串标量在序列化时将自动转化为 BLOB 类型。(**1.30.1**)
  
### 故障修复

* Windows 系统下，通过 `files` 函数查询大于 2GB 的文件时，返回的 fileSize 值不正确。（**1.30.22.1**）
* 在高可用集群下，使用 `addFunctionView` 时，若序列化出现问题，则不会清理序列化未完成的函数。（**1.30.22.1**）
* 在高可用集群下，一个控制节点添加使用了插件的函数视图时，会导致其它控制节点宕机。（**1.30.22.1**）
* 拥有 DB_MANAGE 权限的用户无法给其它用户赋权。（**1.30.22.1**）
* 添加节点后，进行备份可能会报错。（**1.30.22.1**）
* 查询采用 COMPO 分区的分布式表，若查询语句同时满足以下条件，则查询结果可能会出现数据缺失：（**1.30.22.1**）
  * select 不使用聚合函数、序列相关函数、row reduce 函数（如 rowSum）、填充函数（如 ffill）
  * 使用了 pivot by 语句，且 pivot by 的列是 COMPO 分区列中除最后一个分区列外的其他列。
* 2.00.10版本，使用例如 `... and not like(id, '%a')，not like, not in, not between` 的语句时，解析会出现报错。（**1.30.22.1**）
* `createReactiveStateEngine` 的 *metrics* 参数以 tuple 形式给出，且 tuple 中包含返回多个值的函数或表达式时，会出现 server 崩溃。（**1.30.22.1**）
* 当 symbolbase 文件出现问题时，再次加载该文件会导致 server 崩溃。（**1.30.22.1**）
* 当查询分布式表的数据量比较大时，若查询语句中使用了 `TOP` 和 `GROUP BY`，则可能报错找不到某列。（**1.30.22**）
* SQL 查询时报错找不到某个列，但列名可能不正确。（**1.30.22**）
* 向列数较多的分布式表的一个分区写入较多数据时，可能出现因写入失败而导致系统崩溃的问题。（**1.30.22**）
* 并发加载和删除同一个数据库下的不同表后，再通过 `loadTable` 加载一个表，可能报找不到 *.tbl* 文件的错误。（**1.30.22**）
* 在聚合函数中无法用 `head` 和 `tail` 函数。此为 1.30.18 引入的问题。（**1.30.22**）
* 对维度表通过 `renameTable` 修改表名的同时进行查询，会导致死锁。（**1.30.22**）
* 当分区个数过多时，SQL 查询通过 `BETWEEN AND` 进行剪枝操作会报错：`The number of partitions [xxxxx] relevant to the query is too large. `。（**1.30.22**）
* `CASE WHEN` 语句中若使用运算、函数，会导致服务器崩溃。（**1.30.22**）
* SQL 查询时使用 `DISTINCT` 关键字，在某些场景下可能结果不正确。（**1.30.22**）
* 当查询采用 VALUE 或 RANGE 分区的分布式表时，若 `SELECT` 语句中的分区列使用了时间转换函数，并且在 `GROUP BY` 语句中对该列也使用了相同的时间函数，同时取了与 `SELECT` 语句中字段名称不同的别名，导致查询结果错误。（**1.30.22**）
* 通过 SQL `DELETE` 语句删除数据时，若相关分区所有副本都下线，则会报错： `chunktype mismatched for path`。（**1.30.22**）
* local executor 在进行任务调度时可能产生死锁。（**1.30.22**）
* 响应式状态引擎中使用 JIT 用户自定义函数，当单次写入大量数据时，输出结果不正确。（**1.30.22**）
* 多个节点同时执行 `unsubscribeTable` 时，可能出现死锁。（**1.30.22**）
* 对持久化流表并发进行追加数据和保存流表，会出现 server 崩溃。（**1.30.22**）
* `createWindowJoinEngine` 的 *metrics* 中若使用了列的别名，则聚合计算的结果错误。（**1.30.22**）
* 通过 `DROP table` 语句删除流表，出现该流表无法被删除，也无法被取消订阅。（**1.30.22**）
* 修复了一些语法（比如 "/" == "a"）解析的问题。（**1.30.22**）
* 当 `ols` 第二个参数全是0时，输出的结果会多一列。（**1.30.22**）
* `wj` 的 *aggs* 参数输入不规范时，因解析失败而导致 server crash。（**1.30.22**）
* `expr` 函数中若传入了 DATEHOUR 类型，则结果不正确。（**1.30.22**）
* *webLoginRequired* 启用时 web 无法正常加载。（**1.30.22**）
* 使用 `cast` 转换 SYMBOL 数据时结果不正确。（**1.30.22**）
* `nullFill` 对 `bucket` 函数返回值中的空值填充失败。（**1.30.22**）
* 自定义函数中使用 `twindow` 调用了一个自定义匿名聚合函数，出现报错：`func must be an aggregate function.`。（**1.30.22**）
* 启动 DolphinDB 进程时通过 *run* 参数指定运行脚本，若脚本包含 `submitJob`，则会导致 server 崩溃。（**1.30.22**）
* 修复在同时满足以下条件时，server 重启会产生函数视图与 module 函数名冲突的问题：

  * 单节点模式
  * 添加 module 中的函数到 functionView 后再删除该函数视图
  * 配置项 `preloadModules` 指定了预加载该 module

  同时优化了在其它情况下，当函数视图与 module 函数发生冲突时的报错信息。（**1.30.21.6**）
* 服务器与客户端通过 SSL 通讯时，如果从服务器传输到客户端的数据量很大，可能会导致会话断开连接。（**1.30.21.6**）
* 在集群模式且设置数据库为 atomic='CHUNK' 的情况下，对于同一个数据库下分区数据分布在不同节点上的不同表进行连接时，结果有时不正确。（**1.30.21.6**）
* 状态引擎未处理 metrics 中的用户自定义函数的命名空间。（**1.30.21.6**）
* 通过 `mskew` 或 `mkurtosis` 计算的数据中，若某个数据列连续存在相同值，且相同值的个数大于窗口长度（window），则计算结果不正确。（**1.30.21.6**）
* 查询 MVCC 表，对字符串类型列使用 `order by` 时，不支持同时搭配 limit 0, k（或 limit k）。（**1.30.21.5**）
* 删除一个视图（`dropFunctionView`）时，由于写日志时未加锁，导致偶发宕机。 （**1.30.21.5**）
* 等值连接（`equi join`, `inner join`）两个表，其中第一个连接列为 STRING 类型，第二个连接列为 NANOTIMESTAMP 类型时，返回结果不正确。（**1.30.21.5**）
* 通过 `loadTable` 加载表时，由于对表名校验不严格，导致分级存储数据丢失。（**1.30.21.5**）
* 禁用 SQL 的 `select distinct` 语句。SQL 语句中出现的 `distinct` 将按照函数的逻辑执行，即结果中返回的顺序不保证和原表中的相同，且列名为 distinct_xxx。（**1.30.21.5**）
* 如果 `datanodeRestartInterval` 的设置时间小于系统预定义值100，在安全关机情况下或重启集群时，数据节点会立刻被控制节点启动。（**1.30.21.4**）
* `toJson` 传入的 tuple 中包含数值型标量时，转换结果错误。（**1.30.21.4**）
* 如果字典中的 value 是ANY类型的向量，则使用 toJson 转换后会出现缺失元素的情况。（**1.30.21.4**）
* 使用 `bar` 查询分区表时，如果将 `bar` 的 interval 参数设置为 0，则可能会导致 server 崩溃。（**1.30.21.4**）
* 通过 `replay` 函数进行异构回放时，若输入标识为 SYMBOL 类型，则出现报错。此为 1.30.21 版本引入的 bug。（**1.30.21.4**）
* 因部分定时作业序列化失败而导致在重启后所有定时作业反序列化失败。（**1.30.21.4**）
* 通过 `scheduleJob` 设置的定时任务序列化失败但仍然生效。（**1.30.21.4**）
* `array` 函数的 defaultValue 参数指定为向量，导致 server 崩溃。（**1.30.21.4**）
* `upsert!` 函数的 newData 参数为非表类型时，导致 server 崩溃。（**1.30.21.4**）
* 使用 upsert! 更新表数据时，同时满足以下条件，导致更新失败（**1.30.21.4**）：
  * 仅更新一条数据
  * newData 表中含有 NULL 值
  * 设置 ignoreNull=true
* 通过 `update` 对 mvcc 表一次新增多列时出现类型不匹配的报错。（**1.30.21.4**）
* `group by` 一个包含特殊字符（控制字符、标点符号、数学符号和其它特殊符号等）的列时，返回结果里会忽略这些特殊字符。（**1.30.21.4**）
* `dropColumns!` 不能删除顺序分区内存表。（**1.30.21.4**）
* 控制节点在加载本地磁盘分区表时可能出现宕机。（**1.30.21.4**）
* `getClusterDFSTables` 函数会返回已经删除或不存在的表。（**1.30.21.4**）
* 添加新的数据节点并执行 `moveReplicas()` 后，出现分区物理路径和元数据记录不一致。（**1.30.21.4**）
* N 对 N 流表回放时，如果某个 timePartition 中输入数据源为空表，则出现输出表数据错位。（**1.30.21.4**）
* 创建流数据引擎时，因未对某个内部变量进行初始化导致引擎偶尔创建失败。（**1.30.21.4**）
* 分区物理文件夹不存在（手动删除）后，可能导致 flush 数据到磁盘时丢数据或者主动进行 flush 的操作（如 dropTable）卡住。（**1.30.21.4**）
* `temporalAdd` 函数的 unit 指定为 "M" 时，结果不正确。（**1.30.21.4**）
* 不同事务操作相同分区时，偶尔出现存储数据错误。（**1.30.21.3**） 
* 对用户赋予 DB_READ 或 TABLE_READ 权限后，偶尔出现无法查询数据。（**1.30.21.3**） 
* 在高可用集群环境中，若控制器节点在关闭时，raft 日志未能完全写入，当其重新启动时发生崩溃。（**1.30.21.3**） 
* `loadText` 加载的 csv 文件中包含未配对的引号（""），导致 server 崩溃。（**1.30.21.3**） 
* MVCC 表新增列后，通过 `schema` 查看表结构，或者通过 `setColumnComment` 对新增的列添加注释时，导致 server 崩溃。（**1.30.21.3**） 
* 分区字段包含不可见字符导致 controller 和 datanode 版本号不一致。（**1.30.21.3**） 
* 更新内存表越界索引的数据，导致 server 崩溃。（**1.30.21.3**） 
* 在高并发场景下，频繁登录用户，可能导致 server 崩溃。（**1.30.21.3**）
* `StreamEngineParser` 使用嵌套 UDF 函数 导致 server 崩溃。（**1.30.21.3**）
* 更新 XSHG 和 XSHE 的 holiday 日历。（**1.30.21.3**）
* parseExpr 转换包含 lambda 函数的字符串，导致 server 崩溃。（**1.30.21.3**）
* parseExpr 转换的字符串末尾带分号时，出现报错。（**1.30.21.3**）
* `RepartitionDS` 通过 *query* 参数查询连接（join）表，且 *partitionType* 参数指定为 VALUE 分区时，出现 server 崩溃。（**1.30.21.3**）
* 分区表的连接列未包含所有分区字段，且左、右表的部分分区字段具有相同的列名，对右表部分分区列进行过滤时，查询结果不正确。（**1.30.21.3**）
* 对按月进行值分区的 DFS 表，通过 where 条件对某月第一天数据进行过滤，查询结果不正确。（**1.30.21.3**）
* 查询语句中通过 `order by` 对列名为 DATE（大小写敏感）的列倒序排序，且搭配 `limit` 使用，导致 server 崩溃。（**1.30.21.3**）
* 分组（group by）对多个查询列进行时间序列相关（例如 `pre`, `rank` 等）的聚合计算，查询结果不正确。（**1.30.21.3**）
* 高可用方案中客户端重复提交写入任务。（**1.30.21**）    
* 聚合函数运算得到的内存表，后续参与 move 等移动函数的运算时会修改本身内存表数据。（**1.30.21**）    
* window join 的 metric 用匿名聚合函数时报错。（**1.30.21**）    
* 按月分区，where 条件的时间类型和列的时间类型不同时且为当月的最后一天时，查询结果有缺失。（**1.30.21**）    
* `ols` 自变量为字符串类型会导致 crash。（**1.30.21**）    
* 在 `transaction` 语句中使用 mvcc 表会导致 crash。（**1.30.21**）    
* `corr` 函数与 `deltas` 函数联用，加了 as 之后结果不正确。（**1.30.21**）    
* kill -9 直接关闭 server 后会导致一些 redo log 不回收。（**1.30.21**）    
* 响应式状态引擎计算时，若表里面有 STRING 类型，偶尔会导致 crash。（**1.30.21**）    
* `submitJob` 时，若 metacode 包含未定义变量，执行时会导致 crash。（**1.30.21**）    
* 集群网络故障后网络恢复，有时会导致节点 crash。（**1.30.21**）    
* 元编程计算时使用 partial function 并启用 context by 会导致结果不正确。（**1.30.21**）    
* `replayDS`中 `sqlObj` 无法识别为 metacode，导致错误的报错。（**1.30.21**）       
* 若 lj 的左表为内存表，右表为分布式表，且右表的数据库路径包含多层目录（如数据库路径 dfs://mydbs/quotedb)，则会报错。（**1.30.21**）    
* `createTimeSeriesAggregator`，当 `metric` 包含 keyColumn 时，会报错。（**1.30.21**）
* 高可用集群下当两个节点同时执行 `getClusterPerf` 函数会导致死锁。（**1.30.21**）    
* `accumulate` 多次执行时偶尔会 crash。（**1.30.21**）    
* `createDailyTimeSeriesEngine` 计算完成后，在一些场景下查询结果中的时间类型数据会报错。（**1.30.21**）
* 两个空的字符串相加后，`isValid` 判断结果为非空。    
* SQL 查询时多个过滤条件使用 or 连接，超过 128 个后返回结果为空。（**1.30.21**）    
* `loadText` 时若抛出异常，在高压力下有时会导致死锁。（**1.30.21**）    
* 函数添加到 FunctionView 后，查询得到的 body 少了一对括号。（**1.30.21**）    
* `ftest` 的结果会出现 inf。（**1.30.21**）    
* 字符串向量超出索引切片时会导致 crash。（**1.30.21**）    
* 高阶函数 `each` 作用于自定义函数，且输入参数为 table 类型时，有时会 crash。（**1.30.21**）    
* 创建 `CrossSectionalEngine` 后如果 append 的数据和 dummyTable 表结构不一致，不会抛出异常。（**1.30.21**）    
* `loadTextEx` 导入数据时若数据库为值分区，且导入的数据包含建库时分区列未覆盖的部分，则查询不到该部分对应数据。（**1.30.21**）    
* join 分布式表时，列为非分区列，`order by` 分区列且查询中有 `top` 子句，结果不正确。（**1.30.21**）
* 序列化 `rpc` 或 `remoteRun` 返回的部分应用函数（partial application）时报错。（**1.30.21**）    
* 在 job log 达到 1G 后，生成新的 job log 时，旧的 job log 会被丢弃。（**1.30.21**）
* 根据配置项 `openblasThreads` 创建 open blas 线程数，而不是根据 CPU 核数创建。（**1.30.21**）
* 数据节点（datanode）序列化超过128M的分区元数据时，导致序列化失败。（**1.30.20**）
* 回放 redo log 失败，导致 datanode 上分区状态错误。（**1.30.20**）
* 启用分级存储功能，当分区转移到 coldVolume 时失败，会导致分区被误删。（**1.30.20**）
* 建库时指定 atomic=‘CHUNK’ 时，控制节点元数据过大，导致启动慢。（**1.30.20**）
* 进行 update 操作后，旧版本的数据被提前回收。（**1.30.20**）
* `renameTable` 后旧表未及时回收。（**1.30.20**）
* `dropPartition` 时分区以 "/" 结尾会导致 server crash。（**1.30.20**）
* `dropPartition` 通过指定条件的方式无法删除创建分布式表（VALUE 分区）时自动新增的分区。（**1.30.20**）
* 对同一张空表多次删除数据，会导致数据节点（datanode）元数据中表的 cid 错误。（**1.30.20**）
* `dfsRecoveryConcurrency` 配置项设置后不生效。（**1.30.20**）
* 响应式状态引擎（`createReactiveStateEngine`）metrics 中包含 talibNull 状态因子时，会创建失败。（**1.30.20**）
* 创建 `streamEngineParser` 引擎时，若 metrics 使用外部变量，会导致 server crash。（**1.30.20**）
* window join 左表行数小于 window 时会导致 server crash。（**1.30.20**）
* exec 与 limit 一起使用，当返回条数不足 limit 限制条数会导致 server crash。（**1.30.20**）
* `isDuplicated`, `nunique` 函数对 DOUBLE，FLOAT 类型数据计算结果不正确。（**1.30.20**）
* 用户自定义函数内调用 `parseExpr` 无法解析。（**1.30.20**）
* `getClusterPerf` 返回值字段 `maxRunningQueryTime` 显示结果不正确。（**1.30.20**）
* `loadNpy` 读取过大的文件会crash。（**1.30.20**）
* JIT 版本无法在 for 循环外部访问循环内部变量。（**1.30.20**）
* 向 OLAP 引擎持续写入数据时，出现 redo log 回收被卡住。（**1.30.19**）
* 节点安全关机后，仍被控制节点判断为存活。（**1.30.19**）
* 事务决议未完成前，分区锁因超时被释放，导致数据无法写入。（**1.30.19**）
* `backup` 函数按条件备份数据时，对查询条件处理错误。（**1.30.19**）
* 机器负载（load）过高情况下会导致 crash。（**1.30.19**）
* 同时满足以下条件时出现 server crash：API 开启压缩选项，只查询1个分区的数据，查询的数据并不在 API 所在节点，且查询语句包含 group by 操作。（**1.30.19**）
* 分布式表更新后重启集群，更新过程中产生的旧的物理目录有时不会被回收。（**1.30.19**）
* 修复因 symbol base 序列化出错导致数据读取出错。（**1.30.19**）
* 流数据订阅不到持久化流表内存中还存在但是磁盘上已删除的数据。（**1.30.19**）
* `appendForJoin` 插入数据的列数若与 JoinEngine 的 leftTable, rightTable 的列数不一致，会导致 crash。（**1.30.19**）
* 修复 `createSessionWindowEngine` 设置 *updateTime*，但输出表不是 keyedTable 时，一条数据到达引擎之后经过 2*updateTime仍未参与计算，不会触发计算。（**1.30.19**）
* DailyTimeSeriesEngine 在 SessionEnd 之后仍有数据输入可能会导致 crash。（**1.30.19**）
* `createLookupJoinEngine` rightTable 是共享键值内存表时创建引擎会失败。（**1.30.19**）
* 持久化流表写入过程中重启节点，重新加载过程因丢失部分数据导致解压失败而报错。（**1.30.19**）
* `replay` 回放时，指定 *dateColumn* 和 *timeColumn* 为同一个 big array 类型的时间列，且设置 *absoluteRate=false* 时，server 会 crash。（**1.30.19**）
* `createReactiveStateEngine` 的 *metrics* 参数指定为返回一个常量向量的自定义函数时未报错。（**1.30.19**）
* `createAnomalyDetectionEngine` 的 *metrics* 参数中包含临时变量会导致 crash。（**1.30.19**）
* 异常检测引擎(AnomalyDetectionEngine)启用 snapshot，重新创建引擎时指定不同于上个引擎的 metrics，没有抛出异常。（**1.30.19**）
* update 语句与 context by 配合使用时，若 set 的第一列为整数列，后面的列为浮点数列，则会对后面的列进行取整操作。（**1.30.19**）
* 当 worker 数量非常少的时候，并发做 pivot by 查询，则可能会卡死。（**1.30.19**）
* 对查询三级分区表数据语句使用 HINT_EXPLAIN 时，出现 server crash。（**1.30.19**）
* STRING 类型的 subarray 调用 `binsrch` 函数时，结果不正确。（**1.30.19**）
* 将 STRING 类型的向量通过 `cast` 函数转换为 tuple 时，结果为空。（**1.30.19**）
* 对内存表的多个类型为 INT128 的列进行聚合计算时，出现报错：“The function min for reductive operations does not support data type INT128”。（**1.30.19**）
* 通过 `getFunctionView` 获取函数视图时，返回结果中部分函数没有显示 body。（**1.30.19**）
* 向一个空的 tuple append 它自己后，再加载该 tuple，server 发生 crash。（**1.30.19**）
* SQL 查询调用 `interval` 插值场景下，当 where 子句指定的时间范围数据类型的粒度比 `interval` 的 *duration* 参数指定的时间粒度更大时，导致的 sever crash。（**1.30.19**）
* sql 查询语句中调用 `twindow` 函数时，server 会 crash。（**1.30.19**）
* update 分布式表时，set 后的列名与分布式表的列名大小写不一致，导致数据更新失败。（**1.30.19**）
* 响应式状态引擎的 metrics 中包含函数 `iterate` 时，若启用了数据清理机制，且正在清理数据时插入了数据会报错："vector::_M_default_append"。（**1.30.19**）
* 调用 `matrix([[datehour(0)],[datehour(0)]])` 创建 matrix 时，报错：“The data object for matrix function can't be string or any type”。（**1.30.19**）
* `wj` 参数 *aggs* 指定为 countNanInf 报错："An window join function must be an aggregate function"。（**1.30.19**）
* `createDailyTimeSeriesEngine` 不指定分组时，将前一天未计算的数据合入了第二天的第一个窗口。（**1.30.19**）
* `createDailyTimeSeriesEngine` 跨天第一个窗口的数据计算结果不正确，且调用 fill 填充时，输出了 session 时间段外的数据。（**1.30.19**）
* online recovery 过程中，部分处于 In-Progress 状态的任务无法恢复。（**1.30.19**）
* `createTimeSeriesEngine` 指定 *useSystemTime=true* 时， *metrics* 中调用 `mode` 函数导致 server crash。（**1.30.19**）
* `createReactiveStateEngine` 参数 *metrics* 包含 `tmove` 和 `move` 函数, 且 X 为 STRING, SYMBOL 类型时，会 crash。（**1.30.19**）
* 通过 `streamFilter` 引擎分发普通流表时，调用 `tableInsert` 插入数据报错。（**1.30.19**）
* `streamFilter` 插入失败时由于报错信息过长导致 session 断开。（**1.30.19**）
* `createTimeSeriesEngine` 和 `createDailyTimeSeriesEngin`e 参数 *metrics* 包含函数 `firstNot`, `lastNot`，并指定 *fill=`ffill* 时，输出不符合预期。（**1.30.19**）
* `createReactiveStateEngine` 参数 *metrics* 包含 `mfirst`, `mlast`，且函数输入参数 X 的数据类型为 FLOAT, LONH, SHORT, CHART, BOOL, INT128, STRING, SYMBOL 时导致 server crash。
* 增加 `fj` 对结果集行数的限制，不超过20亿行。（**1.30.19**）
* 通过 `tableInsert` 插入数据到表，导致数据库的 atomic level 从 ‘CHUNK’ 转变为 ‘TRANS’ 。（**1.30.19**）
* `createReactiveStateEngine` 参数 *metrics* 包含 tm 系列函数时，tm 系列函数参数 *window* 精度为 y, M, B 时计算结果不正确。（**1.30.19**）
* 修复浏览 online Recovery 重启节点后，两副本 string 列数据不一致。（**1.30.19**）
* `resample` 函数输入索引是 TIME 类型的时间数据，参数 *origin* 指定 "end"，*rule* 指定为 "D"，查看返回结果报错："Invalid value for HourOfDay (valid values 0 - 23): 39"。（**1.30.19**）
* 非 admin 管理员 grant/deny/revoke 自身权限时报错。（**1.30.19**）
* 当矩阵的某一行全为空，`byRow` 计算 `imin`, `imax` 时结果不正确。（**1.30.19**）
* controller 节点宕机时，使用 `getControllerPref` 获取到的 agentsite 不正确。（**1.30.19**）
* 未配置 *dataSync* 动态调用 `addNode` 函数增加节点报错。（**1.30.19**）
* 并发进行写入、查询或计算时，有时出现因 Out of memory 导致系统卡住。（**1.30.18**）
* 数据持续写入 OLAP 存储引擎导致 Cache Engine 刷盘的同时进行查询，查询结果有时会不正确。（**1.30.18**）
* 向 OLAP 引擎 Cache Engine 中写入数据时，若抛出非 out of memory 的异常，则会一直重试导致系统卡住。（**1.30.18**）
* `suspendRecovery` 后调用 `moveReplicas` 函数，部分 chunk 未转移。（**1.30.18**）
* 提交并行任务后重启集群，重启后有几个 chunk 一直处于 RECOVERING 状态。（**1.30.18**）
* 使用 `delete` 语句删除大量数据时，会出现因 checkpoint 文件写入错误信息而导致节点 crash，无法再次启动的问题。（**1.30.18**）
* `createReactiveStateEngine` 中开启 snapshot，当取消订阅之后再次订阅时，若 metrics 与第一次订阅不同，则会导致 server crash。（**1.30.18**）
* lookup join 引擎插入单条数据可能导致 server crash。（**1.30.18**）
* 即使写入高可用流表 schema 不一致，仍然会被放到持久化队列，导致 leader 切换后会报错："Can't find the object with name"。（**1.30.18**）
* `createDailyTimeSeriesEngine` 如果指定 fill，会对输入表中间不包含数据的日期进行填充。（**1.30.18**）
* `createDailyTimeSeriesEngine` 若指定 windowSize 大于 step，fill="none"，在指定 forceTriggerTime 后，没有触发最后一个滑动了 step 之后的窗口的计算。（**1.30.18**）
* 非 admin 用户可以调用 `createUser` 函数。（**1.30.18**）
* `changePwd` 没有限制新密码的长度。（**1.30.18**）
* `loadText` 加载数据到内存表时，若某列数据全部为中文字符，或同时包含中文字符和数字时，会忽略中文字符。（**1.30.18**）
* 使用 matrix([],[]) 语句会导致 crash。（**1.30.18**）
* `exec` 搭配 `pivot by`，若不对 `exec` 选择的列字段调用函数，不会生成一个矩阵，而是生成一个 table。（**1.30.18**）
* 从分布式表 exec 单列时，返回的类型为内存表。（**1.30.18**）
* `randomForestClassifier` 如果设置 numJobs > 1 或者 numJobs=-1，当重复使用同一个 dataSource 进行训练时，则会导致 server crash。（**1.30.18**）
* `interval`函数的 duration 的时间精度与实际数据的精度不匹配导致 crash。（**1.30.18**）
* keyedTable(keyColumns, table) 创建键值内存表时，若 table 存在重复键值，发生内存泄露。（**1.30.18**）
* 调用 `olsEx` 方法，传入一个查询结果为空的数据源后，数据节点发生 crash。（**1.30.18**）
* 为 `addFunctionView`  传入自定义函数包含超过64k的字符串时，会导致 server crash。（**1.30.18**）
* `mcorr`, `mwavg`等支持矩阵计算的 m 系列函数对索引矩阵做计算时，计算结果 lable 列会丢失。（**1.30.18**）
* Web 管理界面：文件系统 (DFS) 白屏、任务展开异常、交互编程界面执行结果是包含 NULL 值的 vector 时表格无法显示。（**1.30.18**）
* 集群间在线同步数据时，若使用 `mr` 并行计算，可能导致节点崩溃。（**1.30.17**）
* 若在 1.30.16 之前版本中对分区名带有“.”字符的数据库分区进行 `backup` 备份，在 1.30.16 版本中通过 `migrate` 恢复数据时，可能报错。（**1.30.17**）
* 由于 1.30.16 引入的新功能，导致从 1.30.16 升级到 1.30.16 版本时出现兼容性问题。（**1.30.17**）
* 查询数据库时，有时会出现报错：“The remote call task doesn't associate any site.”。（**1.30.17**）
* 进行过 `upsert` / `update` / `delete` 操作的数据库，若使用 `imtUpdateChunkVersionOnDataNode` 更新了数据节点上的版本号，可能导致数据读取错误。（**1.30.17**）
* 由于 raft log 追加写有问题，导致高可用集群有时重启后无法正常启动。（**1.30.17**）
* 在 Windows 系统中，通过 `dropTable` 成功删除空表后，若通过 `renameTable` 把另一个表命名为此表，会报错提示文件已存在。（**1.30.17**）
* 具有 TABLE_WRITE 权限的用户在写入数据时，因数据库无法自动添加 VALUE 分区，导致写入失败。（**1.30.17**）
* 当时间序列引擎（time-series streaming engine）的 windowSize 参数是一个向量，且 metrics 参数为自定义函数时，可能导致系统崩溃。（**1.30.17**）
* 流数据高可用计算引擎中，当 follower 在写快照时有可能会死锁，导致后续收到的 raft log 无法被处理，占用内存不断增大。（**1.30.17**）
* 往高可用流表写入数据时，写入数据已经持久化，但 log 还未发送到 follower 时，若所有数据节点宕机，重启后节点间数据会不一致。（**1.30.17**）
* 重启节点后从磁盘加载持久化数据时，需要删除过期的 rowIndex 时误将最后一个 rowIndex 删除，导致数据缺失。（**1.30.17**）
* 流数据高可用状态下，两次 append 数据，每次数据都超过 65536 行，且leader 节点数据同步到 follower 上时发生了 leader 切换，会导致原 leader 节点重启后自动加载持久化流表失败。（**1.30.17**）
* 当高可用流表所在的 raft 组和高可用订阅的 raft 组不同时，如果两组 leader 同时切换或重启，而高可用流表所在 raft 组的 leader 节点竞选成功晚于高可用订阅的 raft 组，会导致自动重订阅失败。（**1.30.17**）
* 订阅（`subscribeTable`）时设置参数 offset=-2，参数设置无效。（**1.30.17**）
* 修正了 `atImax` 和 `atImin` 在参数为多列矩阵时的计算方式。自本版本起，这两个函数将对矩阵的每一列分别查找最值，并以向量的形式返回每一列的计算结果。（**1.30.17**）
* 对内存表和共享流表做表连接，可能导致系统崩溃。（**1.30.17**）
* SQL 查询中，`select` 与 `pivot by` 一起使用时，若在 `select` 子句中增加一列常量，会导致系统崩溃。（**1.30.17**）
* 提交定时任务时，若定时任务的函数有使用{}来生成字典，则会报错无法序列化。（**1.30.17**）
* 连接两个共享表时会报错：“Unrecognized column name”。（**1.30.17**）
* 使用 `sql` 函数生成查询，当 from 参数指定为表连接时，执行结果有误。（**1.30.17**）
* 当一个分布式表按时间进行值分区，且分区粒度大于分区列的时间精度时，跨库表连接时会报错。（**1.30.17**）
* `mmad` 和 `mad` 函数在 useMedian 参数为 true 时计算结果有误。同时在流数据引擎中修复了此问题。（**1.30.17**）
* 函数 `sqlDS` 中，在 `where` 条件语句中使用运算符过滤时间列时，没有正确分区剪枝。（**1.30.17**）
* 函数 `replayDS` 数据源解析时，对 `where` 条件语句中的 date col 表达式解析有误，没有正确分区剪枝。（**1.30.17**）
* 当函数中包含 window join 计算，且窗口参数 window 为 duration 数据对时，则添加函数视图（addFunctionView）时 server 端会在反序列化时报错。（**1.30.17**）
* 对时间分区列进行查询，当查询条件的时间粒度大于分区列的时间粒度时，查询结果有误。（**1.30.17**）
* `zigzag` 函数中，当参数 percent 为 false，参数 retrace 为 true 时，计算结果有误。（**1.30.17**）
* 函数 `loadText` 读取文件第一行时，“-”开头的负数识别为列名。（**1.30.17**）
* 在 SQL `group by` 语句中使用 `min` 或 `max` 函数时，向函数传入两个参数时，计算结果错误。（**1.30.17**）
* 当事务刷盘过慢，可能会出现 redo log 回收超时，导致重启后数据丢失。（**1.30.16**）
* 通过一个 dolphindb server 同时启动多个 dolphindb 集群，出现数据节点无法启动的报错：”Failed to open public key file. No such file or directory.”。（**1.30.16**）
* 高可用集群设置了定时任务（scheduled job），有时会出现因为各个控制节点初始用户的 uuid 不同，导致切换 leader 后，原有的定时任务在新 leader 上认证失败而无法执行的问题。（**1.30.16**）
* 数据节点崩溃之后，代理节点每隔一秒而不是按照参数 datanodeRestartInterval 配置的时间来重启数据节点。（**1.30.16**）
* 定时任务（scheduled job）如果包含了 SQL update 语句，且 where 条件中使用了函数，则在系统重启时反序列化会失败。（**1.30.16**）
* 对分布式表更新后，若提交事务（commit）失败，则旧的物理目录不会被回收。（**1.30.16**）
* 高并发写入场景下，当 redo log 所在磁盘占满时，会概率性导致 redo log 回收线程死锁。（**1.30.16**）
* 数据节点写入数据时内存不足时，未报错 Out of Memory，而是卡住一段时间后崩溃。（**1.30.16**）
* OLAP 存储引擎在各种并发操作时出现节点随机下线的情况。等待一段时间后节点上线，`getTabletsMeta` 返回结果显示丢失一个副本的数据，但实际上并没有丢失。（**1.30.16**）
* 事务回滚出现超时场景下，chunk 的状态设置错误，导致流表持久化报错。（**1.30.16**）
* 横截面引擎（cross-sectional engine）参数校验出错，指定 timeColumn 的情况下，没有指定 useSystemTime 或者指定 useSystemTime 为true，未抛出异常。（**1.30.16**）
* 时间序列引擎（time-series engine）中当指定 useSystemTime 为 true, 且 outputTable 是分布式表时，有时会抛出类型不匹配的异常。（**1.30.16**）
* 用于流数据处理的 Asof Join Engine 指定 delayedTime 的情况下，有时写入数据会出现 crash。（**1.30.16**）
* 流数据高可用，两次 append 的数据都超过65536，如果此时发生 rollback, index.log 会重复写入两条一样的 index 导致报错："index.log contains invalid data."。（**1.30.16**）
* windows 系统下，向 time-series engine, daily time-series engine 和 asof join engine 写入数据，有时会发生 crash。（**1.30.16**）
* subExecutor 还有任务在执行，此时，使用 unsubscribeTable 成功取消订阅，但 getStreamingStat().subWorkers 仍能查询到被取消订阅的 topic。（**1.30.16**）
* 节点重启之后，高可用流表有时会加载失败；流表和订阅的 raft 组都切换 leader 之后，高可用订阅自动重连失败。（**1.30.16**）
* 横截面引擎 triggeringPattern 为 'keyCount' 且 *riggeringInterval 为 tuple 时，会输出重复数据。（**1.30.16**）
* 流表包含 BLOB 类型，从磁盘中加载报错：“Failed to decompress the vector. Invalid message format”。（**1.30.16**）
* 流表在写入 BLOB 数据且单行数据大于 64KB 时会 crash。（**1.30.16**）
* 给内存表增加的新列赋值时，错误的使用了 select 而不是 exec，加载该内存表时出现节点 crash。（**1.30.16**）
* 使用  `readRecord!` 导入二进制文件，会报错：“Read only object or object without ownership can‘t be applied to mutable function readRecord!”。（**1.30.16**）
* 函数调用时，若右括号不在同一行，有时解析会报错。（**1.30.16**）
* 查询一个值分区的分布式表，按分区列分组获取每个组最后的K条记录（context by partitionCol limit -k），且在某个分区里不存在满足 where 条件的数据时，会查到不满足条件的数据。（**1.30.16**）
* SQL 中调用 `rolling`/`moving` 函数时，若不指定生成列的列名，则会报错："More than one column has the duplicated name"。（**1.30.16**）
* `interval` 在某个 step 区间内没有数据时，会生成空值。（**1.30.16**）
* `sliceByKey` 的 rowKeys 的参数设置错误时，server 会 crash。 （**1.30.16**）
* 函数 `replace!` 修改一个向量，引入空值后，没有正确设置空值标志。（**1.30.16**）
* 修复了写入、删除、checkpoint、恢复并发的场景下数据库不稳定的问题。(**1.30.15**)
* 高可用集群有时候控制节点无法启动，报错："Failed to read rsa public key file"。(**1.30.15**)
* 集群 Python API 多并发有时候会出现数据节点死锁。(**1.30.15**)
* 控制节点上关于 chunk 的信息落后于数据节点。(**1.30.15**)
* 系统恢复之后发生了事务决议导致数据错乱。(**1.30.15**)
* redolog 在系统恢复之后再重放，可能导致数据丢失。(**1.30.15**)
* 时序聚合引擎中 append 的 table 的列数小于 dummyTable 的列数时会 crash。(**1.30.15**)
* 流数据高可用，将发布端的 leader 多次 kill 之后，再往发布端写入数据，订阅端有时收不到新数据。(**1.30.15**)
* `interval` 在指定线性填充方式，同时 where 指定的开始时间没有数据，且 group by 多个字段的时候，会出现错误的结果。(**1.30.15**)
* 当特殊字符作为列名时，`sqlCol` 会错误地把字段名称当作共享表的引用来处理。(**1.30.15**)
* 当 Y 中的数据为连续的相等数据时，`mslr` 计算会产生正无穷。(**1.30.15**)
* `eachPre` 函数在计算矩阵时，如果矩阵行数过多，则会导致 crash。(**1.30.15**)
* `mpercentile` 计算偶尔会卡住。(**1.30.15**)
* `temporalParse` 对时间向量转换失败的情况下，返回的结果不正确，应该为 NULL。(**1.30.15**)
* 对空表进行 update 时，使用 context by 语句，不能产生新的列。(**1.30.15**)
* where 条件中"!="前面没有空格时解析失败。(**1.30.15**)
* 大压力写入数据时，偶发写任务卡住的情况。(**1.30.14**)
* Cache Engine 处理不当，导致 symbose base 一直无法被回收。如果随着时间推移，包含 SYMBOL 类型的分区一直增加，导致内存使用量一直缓慢上升。(**1.30.14**)
* 如果事务有 rollback，则 redo log 不会被回收。(**1.30.14**)
* 写入更新删除并发时，读取文件时会出现有时读到的数据比预期少，或者某些表会有空行，或者有些 chunk 状态不正确。(**1.30.14**)
* 多次写入时重启会报：“returned from name node didn't contain any site”。(**1.30.14**)
* 控制节点高可用，重启 leader，偶尔会导致数据节点 crash。(**1.30.14**)
* 由于 raft 模块在 leader 切换时处理不当，导致控制节点在高可用的情况下，同一个 chunk 在数据节点上有时候会对应多个 chunkId。(**1.30.14**)
* 控制节点在高可用的情况下，频繁切换 leader，导致写入或查询过程中任务卡住。(**1.30.14**)
* 在大量并发线程同时增加不存在的值分区时，由于线程的冲突和重试时间太短，导致某些新增值分区添加失败，抛出异常。(**1.30.14**)
* 使用非字符串非 SYMBOL 类型的值去更新分布式表的 SYMBOL 类型列，会导致 symbol base 被破坏。(**1.30.14**)
* 集群的数据节点在重启时收到大量的客户端请求，有可能在后续的鉴权中，出现登录了却当作 guest 处理的情况。(**1.30.14**)
* `tableInsert` 将一个包含多行数据但某些列缺失的字典插入内存表时报异常。(**1.30.14**)
* `replay` 回放三个数据表表时，会出现两个表的回放速度明显快于第三个表。(**1.30.14**)
* `replay` 回放到持久化流表log会报错：“Error in Replayer::output: Immutable sub vector doesn't support method serialize”。(**1.30.14**)
* `kurtosis`和`skew`在流计算引擎中结果精度较低。(**1.30.14**)
* `createDailyTimeSeriesEngine`使用 force Trigger 导致计算结果有 session 区间之外的时间。(**1.30.14**)
* TimeSeriesEngine 指定 fill 并且两个分组之间时间相差较大，计算结果可能出错。(**1.30.14**)
* `createAsofJoinEngine` 数据乱序时结果不对。(**1.30.14**)
* 没有输出表时，横截面引擎作为返回表会报字段缺失错误。(**1.30.14**)
* 一个引用的数据表调用函数 `colNames` 无法返回列名。(**1.30.14**)
* `saveText` 保存空表时候会抛异常。(**1.30.14**)
* `cumvarp` 和 `cumstdp` 应用在矩阵上时错误地调用了 `cumvar` 和 `cumstd`，导致结果不正确。(**1.30.14**)
* `try catch` 语句的 catch 部分包含多行代码时，实际上只有第一行代码会被执行。(**1.30.14**)
* 模块中有系统同名函数时，`parseExpr` 指定模块，没有优先取模块中的函数。(**1.30.14**)
* `interval` 函数在时间列为分区列且 duration 可以整除分区列的单位时，会多生成数据，这个 bug 是在 1.30.13 中引入的。(**1.30.14**)
* 当 `interval` 函数指定 step 参数且处理的列存在缺失的区间时，结果不正确。(**1.30.14**)
* order by 在第二列为负数时，且第二列或之后的数据为浮点数(DOUBLE 或 FLOAT)，且一个小组的数据的个数小于等于7个，且包含两个以上的负数，会导致负数之间的相对排序错误。(**1.30.14**)
* 诸如 exec col1 from t  group by col1 的 sql 语句返回结果不是向量。(**1.30.14**)
* 对 huge temporal vector 使用 `min` 和 `max` 函数，应该返回对应的时间类型，但实际上返回一个长整型。(**1.30.14**)
* `mskew` 输入的值过大会出现非法值 INF。(**1.30.14**)
* 使用 `funcByName` 且参数为聚合函数时，和 context by 同时使用结果只会返回一行。(**1.30.14**)
* window join 在右表时间列有重复值时计算结果不正确。(**1.30.14**)
* 自定义函数中的常量均被标记为 static，使用时必须先复制。函数序列化时丢失了 static 标记。(**1.30.14**)
* JIT 版本的数据节点在 `loadColumn` 的时候，若发生 OOM，则会 crash。(**1.30.14**)
* 删除分布式表（使用 `dropTable` 或 `dropPartition`）在提交时失败，导致事务回滚后，再次查询该表时结果不符合预期。删除该表缓存后，查询恢复正常。(**1.30.13**)
* 配置参数 datanodeRestartInterval 后，在高可用环境下会一直重启数据节点, 数据节点无法关闭。(**1.30.13**)
* 键值表（keyed table）或索引表（indexed table）和内存表等值关联时，抛出 OOM 异常或导致系统崩溃。(**1.30.13**)
* Reactive state engine, cross sectional engine, equal join engine, asof join engine 输出到异步持久化流表时 crash。(**1.30.13**)
* 当最近一个事务操作是删除表的分区，且事务处于决议状态，数据节点有可能给出错误的决议结果。(**1.30.13**)
* 当使用 `remoteRun` 函数远程取消流表订阅时，远程连接可能卡死。(**1.30.13**)
* 当多个数据节点向控制节点汇报元数据，如果时间相差很大，会出现元数据一直处于 recovering状态。(**1.30.13**)
* 恢复某个分区后立刻进行 checkpoint， 并且后续该分区没有再写入，会导致元数据和数据不一致。(**1.30.13**)
* 对空矩阵进行行操作如 `rowSum` 会导致系统崩溃。(**1.30.13**)
* 高可用流表使用函数 `setStreamTableFilterColumn` 设置 filter 后, 重启节点后 filter 字段消失。(**1.30.13**)
* python api 序列化时间类型时，由于发生内存踩踏而导致 api 收到错误消息。(**1.30.13**)
* 多副本集群，设置 dataSync=1 时可能出现读取数据失败或者读取到全部空值。(**1.30.13**)
* `mr` 函数中数据源的脚本长度超过1024字节时，远程执行的数据源错误的将脚本字符串作为执行结果。(**1.30.13**)
* 系统参数 `localExecutors` 设置为0时，在执行 cancelJob 等功能时，导致系统崩溃。 (**1.30.12**)
* 修复分布式表在反复执行删除、更新、新增和节点重启操作时，可能出现的下列状况：（1）The symbol column xxx  or the associated symbol base [] is corrupted. （2）Failed to load column. Expected xxx rows, but actually loaded xxx rows. （3）sym.col contains \(xxx rows\) than requested \(xxx rows\).\] （4）Invalid symbol file. （5）某些分区只有部分副本汇报成功。（6）节点重启时日志中出现错误 Invalid log entry type，导致无法重启。(**1.30.12**)
* 修复了几个导致部分 chunk 一直处于 recovering（恢复中）状态的场景。(**1.30.12**)
* SQL 语句 exec count\(\*\) from t（t为分布式表）被多个线程同时执行时，某些线程产生的结果可能是一个向量（分别记录每个分区的记录数）。正确的结果应该是一个标量（总的记录数量）。(**1.30.12**)
* SQL 语句分组计算（group by）时，如果系统采用了哈希算法，对 SYMBOL 类型的字段使用 `count` 函数，计算结果可能不正确，空值会当作非空值计数。(**1.30.12**)
* 使用 SQL delete 语句对一个包含字符串列（SYMBOL 类型的列没有影响）的大内存表（通常几千万行以上）执行删除操作时（通过 where 语句指定过滤条件)，有概率出现系统崩溃。 (**1.30.12**)
* 分布式表（左表）与未分区内存表（右表）关联（join），连接的列为分区列，where子 句中包含了非分区列，而且该列同时出现在两个表中，计算结果不正确。(**1.30.12**)
* 未分区内存表（左表）和分布式表（右表）关联（join），且分组子句（group by）中包含了分区列，计算结果不正确。(**1.30.12**)
* 版本 1.30.6 中引入的会话窗口引擎（`createSessionWindowEngine`）计算有误，输出结果不正确。(**1.30.12**)
* `replay` 函数回放历史数据到共享的输出表时，应该在 append 数据时对数据表加锁，但实际没有加锁。如果有多个任务都在往共享表 append 数据，可能导致节点崩溃。 (**1.30.12**)
* 往异常检测引擎输入乱序数据时可能发生计算的死循环，导致执行 `getStreamEngineSta` `等其它功能时卡住。(**1.30.12**)
* 用 API 往高可用流表写入数据，反复切换流表 raft 组中的 leader，有概率出现数据丢失。(**1.30.12**)
* `dropStreamTable` 不能删除内存中的流数据表。(**1.30.12**)
* 先 append 数据到右表，再 append 数据到左表，且时间类型为4字节类型时（例如 DATETIME 和 TIME 类型），`AsofJoinEngine` 可能输出错误结果。(**1.30.12**)
* 持久化元代码（Meta Code）时没有持久化包含的自定义函数。导致加载持久化的元代码时，可能出现系统崩溃（找不到自定义函数导致）. (**1.30.12**)
* for 语句在 for(index in start:end) 这种模式下，index 使用了同一个 Constant 对象（循环时修改 Consant 的值）。如果循环语句异步执行（譬如 submitJob 函数提交任务），可能导致 index 对象被多个线程并发调用，计算结果与期望不一致。(**1.30.12**)
* `eqFloat` 返回的值类型错误，应该是 BOOL 类型（true 或 false），实际返回 DOUBLE 类型（0或1）。(**1.30.12**)
* `gram` 函数多次执行，出现计算结果有误的情况。(**1.30.12**) 
* `dropStreamTable` 删除不存在的表 crash，此问题由 1.30.9 的修复代码引入。(**1.30.11**)
* 通过 insert into 方式向 CrossSectionalEngine 写入长度不一致的向量会引发 crash。(**1.30.11**)
* `addColumn` 后多次插入数据，查询会报错："The source vector has been shortened and the sub vector is not valid any more" 。(**1.30.11**)
* 更新空的维度表报错: "Failed to retrieve the size and path for tablet chunk dfs://dbName/\_\_tbName/tbName"。(**1.30.11**)
* 集群中的维度表和分布式表做关联报错: "getFileBlocksMeta on path '/dbpath/tbName.tbl' failed, reason: path does not exist"。(**1.30.11**)
* C++ 标准库 string 的实现存在缺陷，当节点内存满负荷运转时，使用字符串(String)会导致数据节点crash，通过重新实现 string 修复。(**1.30.11**)
* 分区被完全删除后，`first` 和 `last` 取值到长度为1的 NULL 向量，预期为空。(**1.30.11**)
* 节点重启后重新定义流数据持久化时报告 "contain invalid data" 异常。(**1.30.11**)
* `dropPartition` 时报错："Failed to find physical table from Table\_Name when delete tablet chunk"。(**1.30.11**) 
* 对新建的维度表做 `upsert!` 时报错。(**1.30.11**)
* 修复当表达式结果为 NULL 时，逻辑判断默认为 true 的问题。**(1.30.10)**
* 修复时序聚合引擎，聚合函数嵌套序列相关函数导致数据错误，比如 min(next(voltage))。**(1.30.10)**
* 修复流数据计算引擎写入乱序数据导致计算错误，现对乱序数据做忽略处理。**(1.30.10)**
* 修复流数据高可用切换 leader 后接受不到数据。**(1.30.10)**
* 修复当 rand(uplimit, n) 的 uplimit 超过 INT_MAX 时，产生的随机数分布不是均匀的。**(1.30.10)**
* 修复 `createTimeSeriesEngine` 指定 updateTime，不指定 keyColumn 时，最后一批数据时间窗口长度未超过 updateTime，经过 2*updateTime 其仍未强制触发计算。**(1.30.10)**
* `createTimeSeriesEngine` 启用 fill 选项，当实时数据存在多个连续的空窗口时，计算结果有误。(**1.30.9**)
* 设置系统定期回收策略的数据库，被删除后未及时清理回收策略。(**1.30.9**)
* 一库多表，并发写入和删除不同分区，重启后查询报错 symbol base is corrupted。(**1.30.9**)
* 持续的重复下列操作：删除一个分布式表的分区，写入数据到这个分区，重启数据库进程，有几率出现元数据和数据不一致的情况。(**1.30.9**)
* 多线程并发执行 `share` 语句共享一个表和查询一个共享表两个操作时，有几率导致系统奔溃。(**1.30.9**)
* `mcorr` 计算相关性时，如果某一列的数完全相同，应该返回空值。但由于判断浮点数是否为0的阈值设置不合理，导致结果变成0或非常接近于0的数。(**1.30.9**)
* 在启用 dataSync 的情况下，使用 `loadTextEx` 导入大文件后，会导致 redolog 不释放。(**1.30.9**)
* 异常检测引擎在指定多个 keyColumn，计算复合表达式指标时，计算结果有误。(**1.30.9**)
* 执行 continue 之后无法进入下一次循环。此问题从 1.30.6 版本引入。(**1.30.9**)
* 流数据高可用切换 leader 后在某些场景下订阅客户端接受不到数据。 (**1.30.9**)
* 高可用流表不指定 keyColumn 会 crash。(**1.30.9**)
* 矩阵按布尔条件取列数据时结果不符合预期。(**1.30.9**)
* `dictUpdate` 函数针对值为任意类型（ANY）的字典，如果 initFunc 抛出异常，继续操作字典会导致c rash。(**1.30.9**)
* 键值表（keyedTable）更新已有的数据行时，如果输入数据是长度为1的字符串（STRING）列或符号（SYMBOL）列，系统报错：incompatible between index and value。 (**1.30.9**)
* 修复节点掉线后执行 `dropTable` 失败导致节点恢复后该表也无法被删除。(**1.30.8**)
* `cutPoints` 在 sql 句中使用结果有误。(**1.30.8**)
* 修复当写入 keyed table 的 tuple 中包含 subarray 时，返回的表结果不正确。(**1.30.8**)
* 修复多层循环时，在内层循环使用 break，会退出最外层循环, 此问题是由于 1.30.6 版本引入。(**1.30.8**)
* update 分布式表失败时有几率导致在 append 数据时候 server 报告异常 "appendCommittedVersion",此问题由 1.30.6 的分布式表支持 update 功能引入。(**1.30.8**)
* 修复异常检查引擎全局不按时间排序时，输出表缺少第一组和最后一组时间数据。(**1.30.7**)
* 修复并发调用 `dropTable`, `getTables` 会导致 crash 的问题。(**1.30.7**)
* 修复当发布节点 host 定义为 localhost 时，远程订阅无法取消问题。(**1.30.7**)
* 修复使用 `nunique` 查询时报错：Immutable sub vector doesn't support method getDataSegment。(**1.30.7**)
* 数据表按照日期（DATE）进行分区，分区字段 ts 的数据类型是 TIMESTAMP，过滤条件 ts > 2021.03.02没有包含（应该包含）2021.03.02这个分区。(**1.30.6**)
* 一个数据库被删除后，如果在被回收之前，系统重启了，查询时该数据库又会展现给用户。(**1.30.6**)
* 自定义函数用于 `pcross`, `ploop` 和 `peach` 等并行计算的高阶函数时，可能出现自定义函数返回值为空的情况。(**1.30.6**)
* `rank` 函数指定 tiesMethod 为 max 时，可能导致系统崩溃。(**1.30.6**)
* 当输入为单个元素的 tuple 时，`flatten` 函数的结果不正确，直接返回了 tuple，而不是 tuple 中的元素。(**1.30.6**)
* 客户端为 python 时，month/datetime/date/minute/time/second 等时间类型数据在高压力情况下可能出现输出结果不正确。(**1.30.6**)
* 时间序列聚合引擎的一个批次的输入数据包含多个时间窗口时，输出的结果没有按时间排序。(**1.30.6**)
* 横截面引擎一个批次的输入数据包含多个时间点，且均满足 keyCount 的触发条件，则输出结果有重复。(**1.30.6**)
* 系统若开启了 cache engine，短时间内反复多次删除和创建同一个数据库表，可能导致旧表的数据写入到新创建的同名表中。(**1.30.6**)
* `replay` 无法指定 select 中定义的列名作为 dateColumn 和 timeColumn。(**1.30.6**)
* 修复创建数据库和表时潜在的丢失元数据的风险。(**1.30.5**)
* 当输入的数据包含多个 key，每个 key 的数据按时间升序排列，但是全部数据并非按时间顺序排列时，时间序列聚合引擎输出的结果缺失部分数据。(**1.30.4**)
* 同一客户端对同一流表有多个订阅且流数据的队列满时，可能出现订阅不能删除的情况。(**1.30.4**)
* 当输入的数据小于一个窗口，指定的指标包含聚合和非聚合两种，异常检测引擎会崩溃。(**1.30.4**)
* 键值表和索引表在以下场景导致系统崩溃：包含多个键值列，查询时一个键值列是包含单个元素的向量，其他键值列的值是标量。(**1.30.3**)
* 内置的哈希表使用的内存超过2G时可能导致系统崩溃，影响的函数包括 `isDuplicated`。(**1.30.3**)
* 函数 `searchK` 在应用到 big array（非连续的数组）时可能出现结果不正确。(**1.30.3**)
* 订阅时启用 filter，并且同一个流表被同一个节点的多个应用订阅时，只有按照订阅的顺序，依次反订阅（unsubcribeTable）才可以取消订阅。修复后的版本没有顺序要求。(**1.30.3**)
* `mr` 函数和 `imr` 函数在以下场景导致系统崩溃：启用了 `reduce` 函数，但没有启用 `final` 函数，`map` 函数没有返回值。(**1.30.3**)
* 事务管理器、任务调度器和缓存管理器在内存严重不足时出现内部状态不一致，导致死锁或者系统崩溃。(**1.30.3**)
* 当磁盘被占满后，redo log 内部状态出现不一致，导致重启后数据库无法启动。(**1.30.3**)
* ewm 系列函数包括 `ewmMean`, `ewmVar`, `ewmStd`, `ewmCov`, `ewmCorr` 没有注册成为顺序敏感（order sensitive）的函数，导致在 sql 语句中和 context by 子句配合使用时结果不正确。(**1.30.3**)
* sql 中分组计算时，如果聚合函数 `sum`, `max`, `min`, `avg`, `count`, `std` 等的参数用到了顺序敏感的函数如 `next`, `prev` 等，系统错误的使用了哈希分组优化算法，导致结果不正确。(**1.30.3**)
* 使用顺序敏感的函数（如 `mstd`, `mavg`）构造部分应用（partial application）时，没有正确设置顺序敏感标志，导致启用 context by 子句的 sql 语句应用此类函数的部分应用时，结果不正确。(**1.30.3**)
* Delta 压缩算法连续两次增加的记录数小于3时，解压函数无法解压，报异常。(**1.30.2**)
* 个别函数最后一个参数的名称解析有误，导致使用键值参数时报找不到参数的异常。(**1.30.2**)
* 极端内存不足的情况下可能导致 redo log 写入失败。(**1.30.2**)
* 系统启动时删除不必要的异常警告 \<WARNING\> : failed to remove public key file。(**1.30.2**)
* 修复无法将一个带有 SYMBOL 类型字段的空表序列化到 Python API 的问题。(**1.30.1**)
* 处理流数据时，如果订阅端处理太慢，发布端在磁盘保留消息的时间又太短，需要发布的消息在磁盘和内存中都已经不存在了，会导致系统崩溃。(**1.30.1**)
* 修复 redo log 和 cache engine 在内存不足时导致系统死锁的问题。(**1.30.1**)

## DolphinDB 插件

* Python 插件

    * 支持在 DolphinDB 中直接调用Python库。    

* ODBC 插件

    * odbc 插件导出数据到 mysql 时，对 \ 和 ' 进行转义。(**1.30.12**)

* MySQL 插件
    * `mysql::load` 中添了 allowEmptyTable 参数，可以设置是否返回一个空表。(**1.30.12**)

* JDBC 插件

    * 新增支持 DECIMAL128 数据类型。（**1.30.22.1**）
    * 新增支持连接属性 sqlStd，用于指定解析 SQL 语句的语法。（**1.30.22.1**）
    * 方法 getObject 新增支持日期时间类型 LocalDate, LocalTime, LocalDateTime, java.util.Date, Timestamp。（**1.30.21.4**）
    * 修复连接 DolphinDB 时若指定 database 和 tableName，在断开重连后出现查询数据异常的问题。（**1.30.21.4**）
    * 修复 JDBC PrepareStatement 使用 setString() 时存在字符串类型转换的问题。（**1.30.21.4**）
    * 修复了执行 SQL 语句时，语句中与关键字相同的字符串被转成小写的问题。 （**1.30.21.3**）
    * 修复若 URL 设置的 databasePath 中包含无权限的表，则出现报错且无法连接的问题。（**1.30.21.1**）
    * 新增连接属性 tableName，可以加载指定的表。（**1.30.21.1**）
    * 改进：只连接一个节点时，若未设置高可用参数，则默认在连接失败或因网络问题导致连接断开时，都会自动进行重连。（**1.30.21.1**）
    * 新增高可用配置参数 *enableHighAvailability*，与 *highAvailability* 功能相同。使用时只需设置其中一个参数即可（推荐使用 *enableHighAvailability*），若配置冲突则会报错。（**1.30.21.1**）
    * 新增支持 Decimal 数据类型，用户可以对 Decimal 类型数据进行查询、更新等 SQL 操作。（**1.30.20.1**）
    * JDBC 中的 Java API 升级后，Vector 中的 get 方法返回值由 Scalar 变成 Entity。其中在用到如下函数时须将数据强转为 Scalar。
    isNull, setNull, getNumber, getTemporal, hashBucket, getJsonString, getScale（**1.30.20.1**）
    * 不区分以下 SQL 关键字大小写：select, from, where, as, last, or, order, group, by, interval, cgroup, having, update, set,  insert, into, values, delete, limit, top, map, pivot, partition, sample。(**1.30.17.1**)
    * JDBCDataBaseMetaData 类新增 getSchemas 方法，用来获取当前连接 server 下的所有分布式数据库和数据表。(**1.30.17.1**)
    * 新增支持 SYMBOL, BLOB, DATEHOUR, COMPLEX, DURATION, INT128, IPADDR 和 POINT 数据类型。(**1.30.17.1**)
    * 修复写入 STRING 类型时出现报错的问题。(**1.30.17.1**)
    * 修复 setNull 接口传入TIMESTAMP 类型空值报错的问题。(**1.30.17.1**)


## 客户端工具

### GUI

  * 新增支持 DECIMAL128 数据。（**1.30.22.1**）
  * 语言选择下拉框新增 Oracle、MySQL 选项。（**1.30.22.1**）
  * 新增支持 select Null 语句。（**1.30.22.1**）
  * 新增支持以下关键字高亮。（**1.30.22.1**）

    JOIN、FULL JOIN、LEFT SEMI JOIN、DECIMAL128、DATEHOUR、IS、CREATE DATABASE、create database、inner join、sub、full outer join、right outer join、left outer join、drop table、if exists 、drop database、update...set、alter xxx drop/rename/add、create table、nulls first

  * 新增 refresh 选项 ，支持刷新功能。（**1.30.22.1**）
  * 新增加密同步选项“Encrypt and synchronized to server”，支持同步 module 到 server 并保存为加密 .dom 文件。（**1.30.22.1**）
  * 优化了 #include 导入脚本的逻辑。（**1.30.22.1**）
  * 优化了 SSL 功能相关的报错信息。（**1.30.22.1**）
  * 修复了同步 modules 时目标路径错误的问题。（**1.30.21.3**）
  * 支持将内存表以 DolphinDB 私有格式保存到本地或上传至服务器。(**1.30.21.1**)
  * 支持部分标准 SQL 的关键字高亮。（**1.30.21.1**）
  * 支持查看 DECIMAL 类型数据。（**1.30.21.1**）
  * 支持 DECIMAL32 和 DECIMAL64 关键字高亮。（**1.30.21.1**）
  * 支持查看列类型为 ANY VECTOR 的表。（**1.30.21.1**）
  * 修复了 Data Browser 中 NULL 值显示不正确。（**1.30.21.1**）
  * 修复了解析服务器返回的 month(0)~month(11) 的结果显示数据不正确。（**1.30.21.1**）
  * 修复通过 GUI 变量浏览器无法查看 array vector 类型变量的问题。（**1.30.19.1**）
  * 优化报错信息显示。（**1.30.19.1**）
  * 当 Server 重启后，实现 GUI 自动重连。（**1.30.19.2**）
  * 优化export table信息显示，在GUI下方的log窗口中显示成功与失败的文件。（**1.30.19.2**）
  * 增加export前的路径检查功能。（**1.30.19.2**）
  * 修复 python 模式下，GUI 端运行 nanotimestamp(-1)出现计算错误的问题。（**1.30.19.2**）
  * GUI 画图函数 plot 多曲线可共享y轴。(**1.30.13**)
  * 增加下载查询结果到 GUI 本地 csv 功能。
  * 1.30.7 及以上版本的 Server, 需要配合 GUI1.30.7 版本使用 DURATION 类型。
  * **注意**：1.30 及以上版本的 Server 不兼容低于 1.30.0 版本的 GUI，请从官网下载最新版本 GUI 客户端。

### WEB
    
  > 新功能
      
  * 通过 WEB 连接数据库时，增加 DolphinDB License 过期预警的提示弹窗。（**1.30.22**）
  * 通过界面方式建表时，数据列的数据类型中增加 DECIMAL128 类型。（**1.30.22**）
  * 增加通过界面方式创建数据库、数据表的功能。（**1.30.22**）
  * 数据库界面可以展示系统中所有数据库、数据表（包含表结构，列、分区）等内容。（**1.30.22**）
  * 编辑器界面增加执行代码、代码地图和回车补全设置按键。（**1.30.22**）
  * 支持 `SELECT NULL` 语句。（**1.30.22**）
  * 支持 SQL 关键字以大写形式使用。（**1.30.22**）
  * 支持创建并显示 DECIMAL 数据类型。（**1.30.22**）
  * 编辑器顶栏增加代码地图、回车补全配置，显示代码执行状态、支持点击取消执行中的作业。（**1.30.21**）
  * 增加复制行、删除行功能。（**1.30.21**）
  * 用户在字典中可选中文本。（**1.30.21**）
  * 支持显示 decimal32/64 数据及由其组成的 array vector。（**1.30.21**）
  * 新增查看数据表结构的功能，用户可以查看前一百行数据，添加列。（**1.30.21**）
  * 数据库表再展开后为列，并支持修改注释。（**1.30.21**）
  * 终端的输出结果支持颜色。（**1.30.21**）
  * 交互编程：新增数据库管理，支持查看数据库及表。（**1.30.20**）
  * 新增设置面板，支持自定义小数展示位数，如固定显示两位小数 1.00。（**1.30.20**）
  * 支持词典 (dict) 的可视化展示。（**1.30.20**）
  * 点击错误代码（例如 ‘RefId: S00001’） 可跳转至解释文档。（**1.30.20**）
  
  > 改进

  * 优化右上角版本信息/节点信息菜单的显示样式。（**1.30.22**）
  * 在数据库浏览器面点击展开表的同时，在数据浏览界面展示表内容。（**1.30.22**）
  * 数据浏览界面中限制表格、向量、字典中的字符串可显示的最大长度为10000 个。（**1.30.22**）
  * 控制节点和数据节点配置界面补全了所有可用的配置选项。（**1.30.22**）
  * `regularArrayMemoryLimit` 配置参数的输入方式修改为输入框。（**1.30.22**）
  * 取消参数配置界面对部分参数输入值的限制。（**1.30.22**）
  * 在节点配置界面，若配置项的值为空，则不会将该配置写入配置文件。（**1.30.22**）
  * 取消在功能面板中展示文件系统列表，并将文件系统功能整合到交互编程中的数据库中。（**1.30.22**）
  * 日志浏览器调整至网页右边；数据浏览器调整至网页下方。（**1.30.22**）
  * 日志浏览器中最多可显示 100000 行日志。（**1.30.22**）
  * 布局优化，表格移至底部以显示更多列。（**1.30.21**）
  * 代码编辑器统一改为自动保存，无需手动保存。（**1.30.21**）
  * 优化了页面加载速度。（**1.30.21**）
  * 用户需要先登录才能查看数据节点日志。（**1.30.21**）
  * 优化数据视图显示：表格底部显示表的行、列、类型信息；当表内容高度溢出时，总是显示水平滚动条。（**1.30.21**）
  * 优化字体，降低了文件大小。（**1.30.21**）
  * 变量面板变量显示更紧凑。（**1.30.21**）
  * 导航栏顶部显示节点类型。（**1.30.21**）
  * 优化了数据库无权限的错误提示。（**1.30.21**）
  * 路径中含有“.”的数据库支持分级展示，如 dfs://aaa.bbb.ccc。（**1.30.21**）
  * 作业管理中任务状态汉化，支持根据状态搜索。（**1.30.21**）
  * 官网用户手册中的函数文档已同步至最新。（**1.30.21**）
  * 优化代码高亮。（**1.30.20**）
  * 数值支持千分位号（,）分隔，如 1,000,000,000。（**1.30.20**）
  * 关键字、函数提示、函数文档更新。（**1.30.20**）
  * 优化代码执行结果显示，使显示更紧凑。（**1.30.20**）
  * 优化状态管理面板，可分类显示状态信息。（**1.30.20**）
  * 优化了表格分页显示样式，并为新窗口打开等图标增加 tooltip。（**1.30.20**）
  * 作业管理: 优化任务字段名称，支持根据客户端 IP 搜索任务。（**1.30.20**）
  * 在高可用集群环境下，通过 web 访问任意 controller 节点，会重定向到 leader 节点，能在 web 页面展示所有节点信息。（**1.30.19**）
  * Web 任务管理界面优化：重新设计、整合了 Web 管理界面，增加了作业管理功能，支持查看、停止、取消 DolphinDB 运行中、已提交和定时触发的作业。升级 server 版本后，需要同步更新 web 文件夹。
    新版本使用了 WebSocket 协议，增加了对 DolphinDB 二进制协议的支持，对浏览器的要求也随之提高，可能需要用户更新浏览器到最新的版本，推荐使用 Chrome 最新版或 Edge 最新版。（**1.30.16**）

  > Bug Fix
  
  * 数据库浏览界面中的维度表菜单下会显示分区。（**1.30.22**）
  * 在未登录状态下，启动数据节点却没有弹框提示需要登录。（**1.30.22**）
  * 当查询包含 DATE 类型数据的表时，在数据浏览界面，DATE 类型的 NULL 显示为 'null' 而不是空。（**1.30.22**）
  * 向量中若包含单独的符号 `，则编辑器中部分文本的颜色显示不正确。（**1.30.22**）
  * 在数据库浏览界面下，array vector 类型的列不会在列菜单中显示。（**1.30.22**）
  * 本地变量中点击空的 SYMBOL 变量，会报错。（**1.30.22**）
  * 日志浏览器和编辑器中的字体显示非等宽。（**1.30.22**）
  * 当本地变量过多时，由于本地变量界面没有滚动条，导致变量溢出到共享变量界面显示。（**1.30.22**）
  * 异步复制相关配置项的名称不正确。（**1.30.22**）
  * 修复鼠标悬浮在 append! 等函数时没有正确显示函数提示的问题。（**1.30.21**）
  * 修复矩阵最后一页数据显示异常的问题。（**1.30.21**）
  * 修复终端 refid 错误链接需要点击两次的问题。（**1.30.21**）
  * 修复终端字体显示异常的问题。（**1.30.21**）
  * 关键字高亮逻辑修改，解决了set(), values() 函数被高亮的问题。（**1.30.21**）
  * 修复了绘制k线图时横坐标不对的问题。（**1.30.21**）
  * 修复顶部导航栏样式泄漏到编辑器的函数文档区域的问题，修复后编辑器的函数文档顶部高度恢复正常。（**1.30.21**）
  * 修复终端和数据视图中时间显示不正确的问题。（**1.30.21**）
  * 优化了登录错误时显示的错误信息。（**1.30.21**）
  * 数据库面板高度可调整。（**1.30.21**）
  * 数据库列表解决了卡顿问题。（**1.30.21**）
  * 修复了左侧数据库、变量、共享变量面板、高度、宽度及滚动操作相关的缺陷。（**1.30.21**）
  * 修复通过 plot 画图传入时间类型的 labels 时，labels 未正确格式化的问题。（**1.30.20**）
  * web 界面启用数据节点或反复重启集群，代理节点会产生僵尸子进程。（**1.30.18**）

## API

### Java API

  - 新功能：新增开启高可用后，API 将优先随机连接低负载节点。（**1.30.22.2**）
  - 新功能：部分数据类型新增获取数值的方法。（**1.30.22.2**）

    BasicDouble, BasicFloat, BasicInt, BasicLong, BasicShort, BasicByte
    
  - 功能优化：升级 FastJson 版本至2.0.33。（**1.30.22.2**）
  - 新功能：新增支持 DECIMAL128 数据类型。（**1.30.22.1**）
  - 新功能：DBConnection 方法新增参数 *sqlStd*，用于解析 SQL 语句。（**1.30.22.1**）
  - 功能优化：优化了 BasicDBTask 的性能。（**1.30.22.1**）
  - Float 和 Double 类型的数据在满足绝对值小于0.000001或者大于1000000.0时，使用 getString 的返回值不再使用科学计数法。（**1.30.21.3**）
  - 所有 Vector 类新增 `Append` 方法。（**1.30.21.1**）
  - 新增 `AutoFitTableUpsert` 类。（**1.30.21.1**）
  - `MultithreadedTableWriter` 新增以 upsert 模式插入数据。（**1.30.21.1**）
  - `MultithreadedTableWriter` 新增回调接口。（**1.30.21.1**）
  - 支持通过 `PartitionedTableAppender` 向分布式表中插入 array vector。（**1.30.21.1**）
  - 支持 DECIMAL 类型数据。（**1.30.21.1**）
  - 支持流订阅通过 API 发起的连接接收数据。（**1.30.21.1**）
  - 优化了 array vector 应用 `getRowJson` 后的结果，使其符合 JSON 规范。（**1.30.21.1**）
  - 优化了 API 交互流程，避免高可用场景下重复提交数据。（**1.30.21.1**）
  - 修复错误：解析服务器返回 month(0)~month(11) 的结果时，显示数据不正确。（**1.30.21.1**）
  - 修复错误：`MultithreadedTableWriter` 向表中写入大量 array vector 数据时，报错 "connection has been closed"。（**1.30.21.1**）
  - 修复错误：查询结果达到 268,435,455（即(2^32-1)/16）以上时发生数据紊乱。（**1.30.21.1**）
  - 新增 BasicDecimal32, BasicDecimal64, BasicDecimal32Vector 和 BasicDecimal64Vector 类，用于创建 Decimal 类型数据。支持压缩后上传及下载 Decimal 类型数据。（**1.30.20.2**）
  - `MultithreadedTableWriter` 类新增参数 *callbackHandler* 支持回调。（**1.30.20.2**）
  - `MultithreadedTableWriter` 类支持写入 Decimal 类型数据。（**1.30.20.2**）
  - `MultithreadedTableWriter` 类新增参数 *mode* 和 *pModeOption* 支持 append! 或 upsert! 两种方式更新表。（**1.30.20.2**）
  - 新增 `AutoFitTableUpsert` 类及其 `upsert` 方法，以单线程方式 upsert! 表数据。（**1.30.20.2**）
  - 修复 `BasicTable` 的 `getRowJson` 方法返回不规范 JSON 的问题。（**1.30.20.2**）
  - 新增 `Append` 方法，支持向 Vector 种追加数据。（**1.30.20.2**）
  - 支持通过 `partitionedTableApender` 向分布式表中写入 array vector 类型数据。（**1.30.20.2**）
  - 通过 API 连接集群服务器时，实现请求的负载均衡。（**1.30.19.1**）
  - 新增 `StreamDeserializer` 类，实现对异构流表的解析，同时，`subscribe` 函数新增 deserializer 参数，接收经 `StreamDeserializer` 解析后的数据。（**1.30.19.1**）
  - 流订阅 `subscribe` 函数新增参数 *userName* 和 *passWord* 支持输入登录用户名密码。（**1.30.19.1**）
  - `DBConnection.connect` 支持 *reconnect* 参数，实现非高可用场景下，自动重连节点。（**1.30.19.1**）
  - 改进 `ExclusiveDBConnectionPool` 类，实现后台并发运行多个 DBConnection。（**1.30.19.1**）
  - `ExclusiveDBConnectionPool` 新增支持以下参数：*highAvailabilitySites*, *initialScript*, *compress*, *useSSL*, *usePython*。（**1.30.19.1**）
  - `DBConnection.connect` 支持 *usePython* 参数，支持解析 python 脚本。（**1.30.19.1**）
  - 新增 `BasicTableSchema` 类用于存储 BasicTable 的 rows, cols, colName, colType 等信息。（**1.30.19.1**）
  - 在DBConnection.run中增加参数tableName参数用于在查询表时只读取表的schema信息而不读取整个表的数据，目前只支持内存表。（**1.30.19.1**）
  - `MultithreadedTableWriter` 对象写入内存表时，参数 *dbPath* 和 *tableName* 的设置发生改变：*dbPath* 需设置为空，*tableName* 需为内存表表名。（**1.30.19.1**）
  - `subscribe` 函数支持批量处理订阅消息。（**1.30.19.1**）
  - 提供分布式库并行写入接口，数据自动按分区规划通过连接池并行入库。
  - 新增支持 COMPLEX, POINT, SYMBOL 数据类型；（**1.30.17.1**）
  - 增加 `MultithreadedTableWriter` 类，支持对分布式表、内存表、维度表的多线程写入。且实现了加密通信、压缩传输和写入高可用等功能。（**1.30.17.1**）
  - `DBConnection` 对象增加 *compress* 参数，支持数据的压缩上传与下载。（**1.30.17.1**）
  - 修复 API 高可用模式下，当数据节点安全关机后，Java API 无法切换到正常节点继续写入的问题。（**1.30.17.1**）
  - 修复 API 订阅流表时出现的问题（**1.30.17.1**）：
    - 订阅 window 版本 server 发布的流表时，出现 “Connection reset” 报错的问题；
    - 订阅 linux 版本 server 发布的流表时，出现因 API 卡住导致无法接收订阅数据的问题。

### Python API

  - Session 和 DBConnectionPool 中 run 方法新增支持指定任务的并行度和优先级。（**1.30.22.2**）
  - Session 新增支持使用锁以保证线程安全。（**1.30.22.2**）
  - 调整 numpy 依赖版本为1.18.0~1.24.4。（**1.30.22.2**）
  - 调整构造 Table 类时，传入参数 dbPath, data 时加载数据表的逻辑与Session.loadTable 的逻辑一致。（**1.30.22.2**）
  - 使用 where 方法只添加一个筛选条件时生成语句将不包含括号。（**1.30.22.2**）
  - 修复使用 where 方法拼接多个筛选条件后生成语句不符合预期逻辑的问题。（**1.30.22.2**）
  - 修复 Table 类 drop 方法在某些情况下不执行的问题。（**1.30.22.2**）
  - 修复 TableUpdate、TableDelete 对象使用 where 方法，对其使用 showSQL 方法后返回错误 SQL 语句的问题。（**1.30.22.2**）
  - 修复使用 upload 方法上传非 Table 对象时错误进行压缩上传的问题。（**1.30.22.2**）
  - 修复 Table 类对象拼接 SQL 字符串时出现不合理书写方式的问题。（**1.30.22.2**）
  - 修复构造 Table 类时内部参数设置有误导致使用 showSQl 后输出逻辑不正常的问题。（**1.30.22.2**）
  - 更新 Python API 用户手册。（**1.30.22.1**）
  - 调整类名 tableUpsert 为 TableUpserter，与原有类名兼容。（**1.30.22.1**）
  - 调整类名 tableAppender 为 TableAppender，与原有类名兼容。（**1.30.22.1**）
  - 调整类名 session 为 Session，与原有类名兼容。（**1.30.22.1**）
  - Session 和 DBConnectionPool 均新增参数 *show_output*，其用于指定是否在 Python 客户端展示脚本的输出内容。（**1.30.22.1**）
  - TableAppender（原类名 tableAppender）, TableUpserter（原类名 tableUpsert）和 PartitionedTableAppender 新增支持写入数据时根据表结构自动进行类型转换。（**1.30.22.1**）
  - 新增支持 Numpy 的 C order 模式。（**1.30.22.1**）
  - 新增支持在上传 DataFrame 时，通过设置属性 __DolphinDB_Type__ 指定列类型以实现强制类型转换。（**1.30.22.1**）
  - 新增支持 MultithreadedTableWriter 在写入流表时，若连接断开将自动进行重连。（**1.30.22.1**）
  - 优化了部分报错信息。（**1.30.22.1**）
  - 优化下载乱码字符串时的处理逻辑。（**1.30.22.1**）
  - 删除了 Table 类在析构时的打印信息。（**1.30.22.1**）
  - 若流订阅中 handler 发生错误将报错并打印异常信息。（**1.30.22.1**）
  - 修复查询表时若添加多个 where 条件执行优先级异常的问题。（**1.30.22.1**）
  - 修复在调用 TableAppender（原类名 tableAppender）, TableUpserter（原类名 tableUpsert）或 PartitionTableAppender 上传 BLOB, INT128, UUID 和 IPADDR 对应的 arrayVector 型的数据时提示警告信息的问题。（**1.30.22.1**）
  - 修复流订阅中偶现提示解析消息失败的问题。（**1.30.22.1**）
  - 修复 DBConnectionPool 在析构时未调用 shutDown 导致进程卡住的问题。（**1.30.22.1**）
  - 修复了 TableAppender（原类名 tableAppender）, TableUpserter（原类名 tableUpsert） 和 PartitionedTableAppender 在引用 Session 或 DBConnectionPool 时，由于 Session 或 DBConnectionPool 提前析构导致无法使用的问题。（**1.30.22.1**）
  - 修复当 MultithreadedTableWriter 写入失败时，调用 getUnwrittenData 方法会导致段错误的问题。（**1.30.21.2**）
  - 修复无法下载超长 BLOB 数据（超过 64K长度）的问题。（**1.30.21.2**）
  - 修复 Mac  ARM 版本中在订阅 1.30.21、2.00.9及之后版本的 DolphinDB 时出现内存越界的问题。（**1.30.21.2**）
  - 修复上传 np.datetime64 类型的空值数据被识别为错误类型的问题。（**1.30.21.2**）
  - 修复上传第一个元素为 Decimal(“NaN“) 的 Vector 时发生数值溢出的问题。（**1.30.21.2**）
  - 修复通过 PROTOCOL_DDB 协议下载 BLOB 类型的集合出现段错误的问题。（**1.30.21.2**）
  - 修复调用 loadTableBySQL 方法时会覆盖当前 session 中变量”db”值的问题。（**1.30.21.2**）
  - 修复 DBConnectionPool 调用 addTask 添加任务后若不取出数据则会导致进程卡住的问题。（**1.30.21.2**）
  - 调整 Python API 依赖库pandas 的版本为不小于1.0.0。（**1.30.21.2**）
  - 新增支持 Python3.10。（**1.30.21.1**）
  - `Session` 和 `DBConnectionPool` 新增 `protocol` 参数，在构建函数时进行使用，可指定数据格式的传输协议。（**1.30.21.1**）
  - 支持流订阅通过 API 发起的连接接收数据。（**1.30.21.1**）
  - `DBConnectionPool.addTask` 新增 `args` 参数，可以接收已定义的对象。（**1.30.21.1**）
  - 支持 `tableAppender`, `tableUpsert` 和 `PartitionedTableAppender` 上传 IPADDR, UUID 和 INT128 类型的数据。（**1.30.21.1**）
  - 支持基于 Apache Arrow 协议下载数据。（**1.30.21.1**）
  - 支持使用 DolphinDB 自定义的数据报文格式（简称 DDB 协议）下载和上传 DECIMAL 类型数据。（**1.30.21.1**）
  - 优化了报错信息。（**1.30.21.1**）
  - 修复错误：macOS 重复创建 MultithreadedTableWriter 后提示创建信号量失败。（**1.30.21.1**）
  - 修复错误：开启 pickle 后下载包含 STRING 类型列的空表提示 "unmarshall failed"。（**1.30.21.1**）
  - 修复错误：流订阅中包含 array vector 数据时发生 API Abort。（**1.30.21.1**）
  - 修复错误：在 uWSGI 中调用 Python API 执行 SQL，API 发生段错误。（**1.30.21.1**）
  - 修复错误：上传数据中包含空值 np.nan 时，服务器结果产生字符 NaN 而非空值。（**1.30.21.1**）
  - 流订阅指定 *msgAsTable* = True 且指定 *batchSize* 为正整数时，将基于消息块处理记录。（**1.30.19.4**）
  - python API 最高支持 NumPy 1.23.4 和 pandas 1.5.2。（**1.30.19.4**）
  - 优化上传数据报错信息。（**1.30.19.4**）
  - 优化 Mac python API 报错信息。（**1.30.19.4**）
  - 修复下载的数据中时间戳小于1970时，会报错的问题。（**1.30.19.4**）
  - 修复通过 `tableAppender`, `tableUpsert`, `PartitionedTableAppender` 写入包含 INT128, IPADDR, UUID, BLOB 类型列时，写入失败的问题。（**1.30.19.4**）
  - 流订阅指定 *batchSize* 为小数时增加报错提示。（**1.30.19.4**）
  - 修复通过 `s.dropPartition` 删除分区，或通过 `s.loadTable` 加载表时，由于创建的临时 database handle 和 table handle 未销毁而造成 server 内存泄漏的问题。（**1.30.19.4**）
  - `session` 类新增 `setTimeOut` 方法，用于设置 TCP 连接的 TCP_USER_TIMEOUT 选项。仅 Linux 系统生效。（**1.30.19.3**）
  - `createPartitionedTable` 新增参数 *sortKeyMappingFunction*，支持对 sortKey 降维。（**1.30.19.3**）
  - DataFrame 在指定 `__DolphinDB_Type__` 属性后，可以按照指定类型上传。（**1.30.19.3**）
  - 修复 Python API 上传 object 类型的 Bool 数据时出现数值错误的问题。（**1.30.19.3**）
  - 为函数添加注解，支持在调用函数时提示函数用法。（**1.30.19.2**）
  - Windows 系统下，Python API 新增支持官网 Python3.8, Python3.9。（**1.30.19.2**）
  - DBConnectionPool 的 runTaskAsync 函数支持上传数据。（**1.30.19.2**）
  - session 增加 enableJobCancellation 方法，仅支持 Linux 系统，通过 Ctrl+C 取消进程中所有正在执行的 session.run() 的任务。（**1.30.19.2**）
  - 解决了 Table 对象被删除后，服务器端不会自动释放资源的问题。（**1.30.19.2**）
  - Linux aarch64 系统下，Python API 支持 conda 环境的 Python3.7-Python3.9。（**1.30.19.2**）
  - `session` 对象 *enableASYN* 参数名调整为 enableASYNC。（**1.30.19.1**）
  - 新增系统变量 version，通过 dolphindb.\__version\__ 可以查看 API 的版本号。（**1.30.19.1**）
  - `MultithreadedTableWriter` 对象写入内存表时，参数 dbPath 和 tableName 的设置发生改变： dbPath 需设置为空，tableName 需为内存表表名。（**1.30.19.1**）
  - API 端支持返回 `s.run `的 print 结果。（**1.30.19.1**）
  - (1) 新增 `tableUpsert` 对象，(2) `MultithreadedTableWriter` 新增参数 *mode* 和 *modeOption*，均可实现对索引内存表、键值内存表，或者 DFS 表通过 `upsert` 方式进行更新。（**1.30.19.1**）
  - 支持上传或读取 INT128, UUID, IP 类型的数组向量，但上传或读取这些类型的数组向量时需设置 *enablePickle*=false。（**1.30.19.1**）
  - 规范 API 空值处理方式。（**1.30.19.1**）
  - `session.connect` 支持 *reconnect* 参数，实现非高可用场景下，自动重连节点。（**1.30.19.1**）
  - 新增 `streamDeserializer` 类，实现对异构流表的解析，同时，`subscribe` 函数新增 *streamDeserializer* 参数，接收经 `streamDeserializer` 解析后的数据。（**1.30.19.1**）
  - 解决通过 API 查询到的数据存在乱码时，无法下载数据的问题。（**1.30.19.1**）
  - 解决 session 关闭后，端口没有及时释放的问题。（**1.30.19.1**）
  - `tableAppender` 支持写入 array vector 类型数据。（**1.30.19.1**）
  - 通过 API 连接集群服务器时，实现请求的负载均衡。（**1.30.19.1**）
  - 修复上传 DataFrame 数据，且它的字符串类型列的首行为 None 时，出现上传失败的问题。（**1.30.17.4**）
  - 指定 DBConnectionPool 的 loadBalance 为 True 时，线程池创建失败。（**1.30.17.3**）
  - 支持最新 Numpy 版本 1.22.3 和最新 Pandas 版本 1.4.2。仍旧不支持 Pandas 1.3.0 版本。（**1.30.17.2**）
  - 支持上传 array vector 到 server 端，支持 DataFrame 内嵌数组方式创建包含 array vector 字段的表。修复 any vector 上传和下载的问题。（**1.30.17.2**）
  - `ErrorCodeInfo` 类的 `errorCode` 由整数类型调整为字符串类型，并增加 `hasError` 和 `succeed` 方法来获取数据写入是否正常。（**1.30.17.2**）
  - 增加 MultithreadedTableWriter 类，支持对分布式表、内存表、维度表的多线程写入。且实现了加密通信、压缩传输和写入高可用等功能。（**1.30.17.1**）
  - session 对象增加 compress 参数，支持数据的压缩下载。（**1.30.17.1**）
  - 减少了 session 对 Python 全局锁的占用时间。（**1.30.17.1**）
  - Table 新增 `toList` 方法，可将 array vector 的数据转换为二维数组，方便使用。（**1.30.17.1**）
  - `PartitionedTableAppender` 支持写入表时自动转换日期时间类型。（**1.30.17.1**）
  - session.database 新增 engine, atomic, enableChunkGranularityConfig 参数。仅 2.00.0 及以上版本 server 的 TSDB 引擎支持这些参数。（**1.30.17.1**）
  - `Database.createPartitionedTable` 新增 compressMethods, sortColumns, keepDuplicates 参数。仅 2.00.0 及以上版本 server 的 TSDB 引擎支持这些参数。（**1.30.17.1**）
  - 修正 session.subscribe 存在数据丢失的问题。（**1.30.17.1**）
  - 版本命名规则进行了调整，与服务器版本保持一致。（**1.30.16.1**）
  - 支持200及以上版本的服务器。（**1.30.16.1**）
  - 支持数组向量（array vector）的上传与下载。（**1.30.16.1**）
  - session 对象增加了 keepAliveTime 参数，设置检测 TCP 存活的时间间隔，默认为30秒。在大数据量访问时，给该参数设置一个较大值，可以避免 TCP 连接掉线。（**1.30.0.15**）
  - orca: 修复 orca.panel 函数。(**1.30.0.10**)
  - orca: 添加 rolling rank 函数。(**1.30.0.9**)
  - orca: rolling mean 增加支持加权平均值功能。(**1.30.0.9**)
  - orca: 新增函数 orca.read_in_memory_table: 支持读取 DolphinDB 内存表。(**1.30.0.9**)
  - orca: 新增 orca.panel 函数。(**1.30.0.9**)
  - orca: 修复 window join 中 where 失效的问题。(**1.30.0.9**)
  - orca: 移除 groupby 中 lazy 参数，groupby 只支持以 lazy 方式进行计算。(**1.30.0.9**)
  - DBConnectionPool 新增了 `runTaskAsyn` 函数，实现并行异步任务调用接口简化。(**1.30.0.8**)
  - 修复 `update` 函数 where 条件不生效的问题。(**1.30.0.8**)
  - 修复使用 Python API 异步追加数据时，客户端会 crash 的问题。(**1.30.0.8**)
  - 修复使用 Python API 两次 upload 同一个名字的 named object, 报错该 named object 无法找到的问题。(**1.30.0.8**)
  - 取消 Python API 安装时 pandas 版本必须低于1.0的限制。(**1.30.0.7**)
  - 提供 `partitionTableAppender` 支持向分布式表并发写入数据。(**1.30.0.6**)
  - `run` 函数提供 fetchSize 参数，支持每次读取 fetchSize 行记录。(**1.30.0.6**)
  - 流数据订阅时支持批量处理。(**1.30.0.6**)
  - `run` 执行完毕后自动清除本会话内生成的变量。(**1.30.0.6**)
  - 连接时进行 Server 版本的兼容性检查。(**1.30.0.6**)
  - `tableAppender` 函数提供写入数据时自动转换时间类型功能。(**1.30.0.6**)
  - 优化数据传输性能, 最新Server版本请升级 Python API 到1.30.0.5
    pip3 install dolphindb==1.30.0.5。 (**1.30.0.5**)
  
### C++ API

  - `MultithreadedTableWriter` 新增回调接口。（**1.30.21.1**）
  - 新增工具类 `DdbVector`，用于创建 DolphinDB 常用的各种类型的 Vector。（**1.30.21.1**）
  - 新增工具类 `Executor`，用于创建 DolphinDB 的匿名线程。（**1.30.21.1**）
  - 新增工具类 `ResultSet`，用于对表进行按行遍历。（**1.30.21.1**）
  - 新增工具类 `enumVectorData`，用于快速遍历 Vector 的元素。（**1.30.21.1**）
  - 优化了取消订阅高可用流表的步骤，不再必须传入 Leader 节点的地址和端口，可以使用订阅传入的 Follower 节点的地址和端口。（**1.30.21.1**）
  - 支持 DECIMAL 类型的 array vector 的上传、下载、压缩和解压缩。（**1.30.21.1**）
  - 支持流订阅通过 API 发起的连接接收数据。（**1.30.21.1**）
  - 修复错误：在使用 Visual Studio 编译 API 时，_USRDLL 发生冲突。已修改为_DDBAPIDLL。（**1.30.21.1**）
  - 修复错误：使用 `PartitionedTableAppender` 接口频繁读写表数据，发生内存泄漏。（**1.30.21.1**）
  - 修复错误：取消流订阅时，未及时释放占用的端口。（**1.30.21.1**）
  - 优化高可用流表取消订阅的步骤，可以使用 Leader 节点或发起订阅的 Follower 节点的地址和端口。（**1.30.21.1**）
  - `MultithreadedTableWriter` 对象写入内存表时，参数 *dbPath* 和 *tableName* 的设置发生改变：*dbPath* 需设置为空，*tableName* 需为内存表表名。（**1.30.19.1**）
  - API 端支持打印 `DBConnection.run` 的 中间结果信息。（**1.30.19.1**）
  - (1) 新增 `tableUpsert` 对象，(2) `MultithreadedTableWriter` 新增参数 *mode* 和 *modeOption*，均可实现对索引内存表、键值内存表，或者 DFS 表通过 `upsert` 方式进行更新。（**1.30.19.1**）
  - 支持上传或读取 INT128, UUID, IP 类型的数组向量。（**1.30.19.1**）
  - `DBConnection.connect` 支持 *reconnect* 参数，实现非高可用场景下，自动重连节点。（**1.30.19.1**）
  - 新增 `StreamDeserializer` 类，实现对异构流表的解析，同时，`subscribe` 函数新增 *streamDeserializer* 参数，接收经 `StreamDeserializer` 解析后的数据。（**1.30.19.1**）
  - 解决 DBConnection 关闭后，端口没有及时释放的问题。（**1.30.19.1**）
  - `tableAppender` 支持写入 array vector 类型数据。（**1.30.19.1**）
  - 通过 API 连接集群服务器时，实现请求的负载均衡。（**1.30.19.1**）
  - 支持线程通过 `setAffinity` 方法绑定到指定 CPU 核。（**1.30.19.1**）
  - 时间类型的 array vector 支持自动转换类型。（**1.30.19.1**）
  - 解决了流订阅无法取消、线程卡死、Crash 等问题。（**1.30.19.1**）
  - 流订阅 `subscribe` 函数新增参数 *userName* 和 *password*，支持输入登录用户名密码。（**1.30.19.1**）
  - 调整 array vector 创建方法。（**1.30.19.1**）
  - 新增 `setColumnCompressTypes` 方法，实现表的各列数据按照指定的压缩方式压缩后上传。（**1.30.19.1**）
  - 新增 `IPCInMemoryStreamClient` 支持订阅跨进程共享内存表。该功能仅 Linux 系统支持。（**1.30.19.1**）
  - 支持通过 DDB_VERSION 宏定义指定 API 编译版本号（130或200）。（**1.30.19.1**）
  - 新增支持数组向量（array vector）。（**1.30.17.1**）
  - 增加 MultithreadedTableWriter 类，支持对分布式表、内存表、维度表的多线程写入。且实现了加密通信、压缩传输和写入高可用等功能；（**1.30.17.1**）
  - DBConnection 对象增加 compress 参数，支持数据的压缩上传与下载。（**1.30.17.1**）
  - 修复 API 高可用模式下，当数据节点安全关机后，C++ API 无法切换到正常节点继续写入的问题。（**1.30.17.1**）
  - 新增 `batchTableWriter` (**1.30.12**)

### C# API

  - 在 NET Core 版本的 C# API 中，DBConnection 新增异步接口。（**1.30.21.1**）
  - MultithreadedTableWriter 新增回调接口。（**1.30.21.1**）
  - 新增 AutoFitTableUpsert 类。（**1.30.21.1**）
  - `MultithreadedTableWriter` 新增以 upsert 模式插入数据。（**1.30.21.1**）
  - 支持流订阅通过 API 发起的连接接收数据。（**1.30.21.1**）
  - 支持以 Apache Arrow 的数据格式下载数据。（**1.30.21.1**）
  - 修复错误：由于订阅的偏移量处理错误，导致流数据订阅失败。（**1.30.21.1**）
  - 通过 API 连接集群服务器时，实现请求的负载均衡。（**1.30.19.1**）
  - 新增 `StreamDeserializer` 类，实现对异构流表的解析，同时，`subscribe` 函数新增 *deserializer* 参数，接收经 `StreamDeserializer` 解析后的数据。（**1.30.19.1**）
  - 流订阅 `subscribe` 函数新增参数 *userName* 和 *password* 支持输入登录用户名密码。（**1.30.19.1**）
  - IVector 增加 `getEntity` 的方法。（**1.30.19.1**）
  - `DBConnection.connect` 支持 *reconnect* 参数，实现非高可用场景下，自动重连节点。（**1.30.19.1**）
  - 改进 `ExclusiveDBConnectionPool` 类，实现后台并发运行多个 DBConnection。（**1.30.19.1**）
  - `ExclusiveDBConnectionPool` 增加 `run` 方法，支持将脚本发送至 DolphinDB 服务器运行。（**1.30.19.1**）
  - `ExclusiveDBConnectionPool` 新增支持以下参数：*highAvailabilitySites*, *startup*, *compress*, *useSSL*, *usePython*。（**1.30.19.1**）
  - `DBConnection.connect` 新增 *usePython* 参数，支持解析 python 脚本。（**1.30.19.1**）
  - `MultithreadedTableWriter` 对象写入内存表时，参数 *dbPath* 和 *tableName* 的设置发生改变：*dbPath* 需设置为空，*tableName* 需为内存表表名。（**1.30.19.1**）
  - 新增支持数组向量（array vector）。（**1.30.17.1**）
  - 增加 `MultithreadedTableWriter` 类，支持对分布式表、内存表、维度表的多线程写入。且实现了加密通信、压缩传输和写入高可用等功能；（**1.30.17.1**）
  - `DBConnection` 对象增加 *compress* 参数，支持数据的压缩上传与下载。（**1.30.17.1**）
  - 修复 API 高可用模式下，当数据节点安全关机后，C++ API 无法切换到正常节点继续写入的问题。（**1.30.17.1**）
  - 修复流数据订阅发生断线重连时，API 出现 crash 的问题。（**1.30.17.1**）
  - 提升了 SYMBOL 类型向量在 API 和 server 之间的传输效率。（**1.30.17.1**）
  - 新增支持 UUID, IPADDR, INT128 和 DATEHOUR 类型。（**1.30.17.1**）
  - 增加 `BatchTableWriter` 类，支持批量异步写入数据到内存表、分区表。（**1.30.17.1**）

### Go API

  - 提供 RunScript 及 RunFile 接口支持发送脚本至服务器运行、提供 RunFunc 接口支持在服务器上执行内置或自定义函数、提供 Upload 接口支持上传本地变量至服务器。（**1.30.19**）
  - 支持流数据订阅。（**1.30.19**）
    - 支持三种订阅方式：返回订阅信息的 PollingClient、单协程回调 GoroutineClient 和多协程回调 GoroutinePooledClient
    - 支持断线重连
    - 不支持订阅异构流表
    - 不支持自动将订阅信息封装成 Table 对象
  - 支持连接池 partitionedTableAppender。（**1.30.19**）
    - 连接池支持负载均衡
    - 支持自定义负载均衡地址
    - 不支持以下功能：压缩，SSL，异步通讯，设置 TCP Keepalive（仅支持长连接）
  - 支持 7 种 DataForm：Scalar, Table, Vector, Set, Pair, Dictionary, Matrix, Chart。（**1.30.19**）
  - 支持 29 种 DataType：VOID, BOOL, CHAR, SHORT, INT LONG, DATE, MONTH, TIME, MINUTE, SECOND, DATETIME, TIMESTAMP, NANOTIME, NANOTIMESTAMP, FLOAT, DOUBLE SYMBOL, STRING, UUID, ANY, DATEHOUR, DATEMINUTE, IP, INT128, BLOB, COMPLEX, POINT, DURATION。（**1.30.19**）
