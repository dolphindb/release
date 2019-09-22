# DolphinDB发行说明

## DolphinDB服务器

版本号 : 0.98.0
发行日期 : 2019-09-23

[Linux64 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux64_V0.98.0.zip) | 
[Linux32 binary](http://www.dolphindb.com/downloads/DolphinDB_Linux32_V0.98.0.zip) | [Windows64 binary](http://www.dolphindb.com/downloads/DolphinDB_Win64_V0.98.0.zip) | 
[Windows32 binary](http://www.dolphindb.com/downloads/DolphinDB_Win32_V0.98.0.zip) | 
[ARM64 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM64_V0.98.0.zip) | 
[ARM32 binary](http://www.dolphindb.com/downloads/DolphinDB_ARM32_V0.98.0.zip) | [Loongson64 binary](http://www.dolphindb.com/downloads/DolphinDB_Loongson64_V0.97.0.zip) 


> 新功能

* 新增元数据高可用。

* 增加了data cache, 提升了数据写入的性能。

* 新增了在单节点模式下启用分布式数据库的功能。

* 新增addRangePartition函数，用于扩展Range类型分区。

* 新增函数textChunkDS, 用于将一个文本文件分割生成多个数据源。

* 新增数据迁移函数：Migrate。

* 新增 go 语句，支持分阶段执行脚本。

* 新增eye函数生成单位矩阵。

* 新增diag函数生成对角矩阵。

* 新增snapshot engine, 用于维护插入数据序列的最新状态，适合iot等场景。


> 改进

* 提升安全性，在配置项webLoginRequired启用时，必须登录才能执行脚本和调用函数。

> Bug修复

* 对一个不存在symbol类型的表,通过函数addColumn增加一个symbol类型字段, 如果不添加数据，马上查询会抛出chunk.dict不存在的异常。

* 当使用函数toStdJson,将一个空表转化为JSON字符串时，返回了非标准的JSON字符串。

## DolphinDB GUI

* 增加关键字高亮 `go`。
 
* 修复了bug: plot函数在x轴为时间时无法绘制除折线图之外的图形。
 
* 增加了配置是否启用函数参数提示选项，用于解决在少数linux桌面上智能提示Panel不消失的问题。
 
* GUI 增加了database面板，可以浏览分布式数据库及表结构。
* 新增尝试取消正在运行任务按钮。
 
* 新增允许强制退出GUI选项。

* VSCode 插件增加了Login菜单。

## DolphinDB plugin binary files:

[DolphinDB AWS S3 Plugin](http://www.dolphindb.com/downloads/AWSS3_V0.98.0.zip)

[DolphinDB ZLIB Plugin](http://www.dolphindb.com/downloads/ZLIB_V0.98.0.zip)

[DolphinDB MYSQL Plugin](http://www.dolphindb.com/downloads/MYSQL_V0.98.0.zip)

[DolphinDB ODBC Plugin](http://www.dolphindb.com/downloads/ODBC_V0.98.0.zip)

[DolphinDB HDF5 Plugin](http://www.dolphindb.com/downloads/HDF5_V0.98.0.zip)

[DolphinDBPlugin](https://github.com/dolphindb/release/raw/master/0.98/DolphinDB_Plugin_V0.98.0_src.zip)

## DolphinDB APIs

* 新增 go api
