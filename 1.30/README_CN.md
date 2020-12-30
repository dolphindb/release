# DolphinDB发行说明

## DolphinDB服务器

版本号： 1.30.0

发行日期： 2020-12-29

[Linux64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.0.zip) | 
[Linux64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.0_JIT.zip) | 
[Linux64 ABI binary](https://www.dolphindb.cn/downloads/DolphinDB_Linux64_V1.30.0_ABI.zip) | 
[Windows64 binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.0.zip) |
[Windows64 JIT binary](https://www.dolphindb.cn/downloads/DolphinDB_Win64_V1.30.0_JIT.zip)

> 新功能


* 新增两个数据结构索引矩阵（indexed matrix）和索引序列（indexed series）用于面板数据的处理。索引矩阵之间，索引序列之间，以及索引矩阵和索引序列之间的二元操作，支持按行列标签自动对齐。

* 新增函数`panel`，`indexedSeries`, `setIndexedMatrix!`, `setIndexedSeries!`, `isIndexedMatrix`, `isIndexedSeries`，`dropna`，`resample`，`asFreq`，`merge`等用于处理索引矩阵和索引序列。

* 新增函数`renameTable`，允许分布式的维度表和分区表改名。

* 新增高价函数`withNullFill`。
* 新增权限DB_OWNER。拥有该权限的用户可以创建自己的数据库，并进行管理。
* 新增函数`upsert!`往键值表或索引表添加或更新记录。
* `schema`函数增加了分区列类型(partitionColumnType)信息输出。

> 改进
* 优化SYMBOL类型的数据序列化/反序列化。这个优化使DolphinDB数据节点之间以及数据节点和API之间传输SYMBOL类型数据时性能有5~10倍的提升。
* 提升了并行作业和分布式作业的稳定性。
* 允许矩阵的行数或列数为0。
* 优化`isDuplicated`去重函数，针对低重复率的数据去重性能提升1倍。

### DolphinDB 插件

* Python 插件

    * 支持在DolphinDB中直接调用python库。

### 客户端工具

* GUI
    * **注意** , 1.30及以上版本的Server不兼容低于1.30.0版本的GUI，若需要请从官网下载最新版本GUI客户端。

### API 

* Java API

    * 提供分布式库并行写入接口，自动按分区规划数据通过连接池并行入库。

* Python API

    * 优化数据传输性能




