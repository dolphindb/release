# DolphinDB 插件发行说明

- [DolphinDB 插件发行说明](#dolphindb-插件发行说明)
  - [AmdQuote](#amdquote)
  - [AWSS3](#awss3)
  - [CTP](#ctp)
  - [HBase](#hbase)
  - [HDF5](#hdf5)
  - [HDFS](#hdfs)
  - [HTTP Client](#http-client)
  - [INSIGHT](#insight)
  - [Kafka](#kafka)
  - [kdb+](#kdb)
  - [mat](#mat)
  - [MongoDB](#mongodb)
  - [MQTT](#mqtt)
  - [mseed](#mseed)
  - [MySQL](#mysql)
  - [ODBC](#odbc)
  - [OPC](#opc)
  - [OPCUA](#opcua)
  - [ORC](#orc)
  - [Parquet](#parquet)
  - [SchemalessWriter](#schemalesswriter)
  - [Signal](#signal)
  - [SVM](#svm)
  - [Zip](#zip)
  - [Zlib](#zlib)
  - [ZMQ](#zmq)

## AmdQuote

### *2.00.10* <!-- omit from toc -->

**新功能**

* 新增支持接收委托表（order）和成交表（trade ）按交易所原始频道代码（ChannelNo）多线程异步写入 server 中的目标表。同一个原始频道代码的委托表和成交表将写入同一张表，且保证其写入顺序。
* 接口 amdQuote::connect 新增支持参数 *outputElapsed*，用于统计插件内部的时延。
* 新增支持订阅输出至非流数据表。

**故障修复**

* 修复在订阅一个错误市场后，无法使用 amdQuote::unsubscribe 取消该订阅的问题。
* 修复了在长时间订阅后，行情数据偶现无法正确写入流表的问题。

## AWSS3

### *2.00.10* <!-- omit from toc -->

**故障修复**

* 接口 loadS3Object 增加对参数 threadCount 可用最大线程数的限制。
* 接口 getS3Object 增加对参数 outputFileName 有效性的检查。

**功能优化**

* 优化了 loadS3Object 对临时文件的处理方法。

## CTP

### *2.00.10* <!-- omit from toc -->

**功能优化**

* 优化了部分报错信息，同时增加了一些捕获自第三方库函数调用异常的报错信息。
* CTP 的连接优化为单例模式，用户在同一 DolphinDB 进程中只能连接一个 CTP 源。
* 优化了输出表的字段类型，将 CTP 插件输出表中 TradingDay 的字段类型由 DT_STRING 更改为 DT_DATE。

## HBase

### *2.00.10* <!-- omit from toc -->

**故障修复**

* 避免下载数据时对非法格式的 minute 类型数据进行解析。
* 修复在使用 hbase::load 导入 disable table 捕获到异常后未中止运行，导致后续 server 宕机的问题。
* 增加下载数据时对 CHAR 类型数据的转换限制，若输入 string 值的长度超过1，则将返回空值。
* 增加下载数据时对 SECOND 类型转换的检查。
* 增加对连接有效性的检查。
* connect 函数增加对参数 isFramed 非法输入值的检查。

**功能优化**

* 增强了多线程并行时的稳定性。

## HDF5

### *2.00.10* <!-- omit from toc -->

**故障修复**

* 修复使用方法 hdf5::ls 执行特定类型的 hdf5文件后 server 宕机的问题。
* 修复并行导入多个文件时 server 宕机的问题。

**功能优化**

* 优化接口 hdf5::saveHDF5 的报错信息。

## HDFS

### *2.00.10* <!-- omit from toc -->

**故障修复**

* 修复对空文件夹调用 getListDirectory 时报错的问题。
* 修复使用 readFile 循环读取文件时，由于未关闭文件句柄导致打开的文件句柄过多，进而导致 hadoop 数据节点不可用、连接断开无法继续读取文件的问题。
* 修复了由于 connect 底层共用 hdfs 连接导致的函数行为混乱的问题。

**功能优化**

* connect 函数新增支持配置集群环境。
* 优化部分报错信息。
  
## HTTP Client

### *2.00.10* <!-- omit from toc -->

**新功能**

* 增加对传入字典类型参数的校验。
* 增加对待发送数据的字节长度的校检。

**功能优化**

* 删除接口 httpCreateSubJob，httpCreateMultiParserSubJob，httpCancelSubJob，httpGetJobStat。

## INSIGHT

### *2.00.10* <!-- omit from toc -->

**故障修复**

* 修复了在断网时取消订阅失败的问题。
* 修复了在执行 insight::close 后，再次执行 insight::getStatus 时 server 宕机的问题。
* 修复了当首次连接时输入错误密码，后续连接一直报错的问题。

## Kafka

### *2.00.10* <!-- omit from toc -->

**故障修复**

* 修复了接口 kafka::pollByteStream 不能接收非 JSON 格式数据的问题。
* 修复了多线程操作导致的 server 宕机问题。

**功能优化**

* 函数 eventGetParts , getOffsetPosition , getOffsetCommitted 增加了返回值。

## kdb+

### *2.00.10* <!-- omit from toc -->

**新功能**

* 新增支持读取 kdb+ char 型 nested list。

**故障修复**

* 修复调用 loadTable 时不指定参数 *symPath* 导致 server 宕机的问题。
* 修复 loadTable 无法正确解析用户自定义 sym 文件名的问题。
* 修复在关闭插件 kdb+的进程后，再次执行 loadTable 导致 server 宕机的问题。

## mat

### *2.00.10* <!-- omit from toc -->

**新功能**

* 新增支持多线程读写 mat 文件。

**故障修复**

* 接口 mat::writeMat 新增对参数 *varName* 非法输入值的报错。

## MongoDB

### *2.00.10* <!-- omit from toc -->

**功能优化**

* 优化了部分报错信息。
* 加强了 mongodb::aggregate, mongodb::load, mongodb::connect 的参数校检。

## MQTT

### *2.00.10* <!-- omit from toc -->

**故障修复**

* 当 MQTT 服务器关闭时，通过 mqtt::connect 进行连接将收到错误提示。
* 优化了 connect 函数中关于参数 batchsize 默认值的报错信息。
* 修复了当 mqtt::publish, mqtt::createCsvFormatter 参数的输入值为 NULL 时可能出现的宕机或卡住的问题。
* 修复了若发布消息中包含空值，订阅端无法接收到数据的问题。
* 修复了若发布数据中包含类型为 CHAR, MONTH 数据时，订阅端会接收到错误类型数据的问题。

**功能优化**

* 优化了部分场景下的报错信息。

## mseed

### *2.00.10* <!-- omit from toc -->

**故障修复**

* 接口 mseed::write 新增对参数 *startTime* 非法输入值的报错。
* 接口 mseed::parseStreamInfo 新增对非法数据或非法 SID（Station Identifier）的报错。
* 接口 mseed::parse 新增对空字符串数据的检查。
* 接口 mseed::read 新增对非法参数输入值的检查。

## MySQL

### *2.00.10* <!-- omit from toc -->

**故障修复**

* 增加对传入连接有效性的校检。

## ODBC

### *2.00.10* <!-- omit from toc -->

**故障修复**

* 修复了关闭 ODBC 的连接时偶现 server 宕机的问题。
* 修复了读取 Oracle 的中文标点数据时出现乱码的问题。
* 修复了多个线程共用一个连接进行并发查询和写入时 server 宕机的问题。

**功能优化**

* 优化了部分报错信息。
* 增加对接口 odbc::close 输入参数的校验。

## OPC

### *2.00.10* <!-- omit from toc -->

**故障修复**

* 修复了用同一个连接多次订阅后取消订阅时 server 宕机的问题。

## OPCUA

### *2.00.10* <!-- omit from toc -->

**故障修复**

* 修复了多线程作业相关的 server 宕机的问题。

## ORC

### *2.00.10* <!-- omit from toc -->

**故障修复**

* 修复了读取时间类型空值数据时输出结果不正确的问题。

**功能优化**

* 优化了时间类型和字符串类型数据导入为数值类型的处理方法。

## Parquet

### *2.00.10* <!-- omit from toc -->

**功能优化**

* 优化了部分报错信息。

## SchemalessWriter

### *2.00.10*<!-- omit from toc -->

**新功能**

* 新增无模式写入插件 SchemalessWriter。

## Signal

### *2.00.10* <!-- omit from toc -->

**故障修复**

* 修复了频繁调用 signal::secc 等接口时内存泄漏的问题。
* 修复多线程并发访问 signal::fft, signal::ifft, signal::secc 等接口时 Signal 插件宕机的问题。
* 修复当 signal::fft 函数的输入数据为偶数个时，输出值的正负符号错误的问题。

## SVM

### *2.00.10* <!-- omit from toc -->

**故障修复**

* 修复了多线程执行 svm::fit 导致 server 宕机的问题。

**功能优化**

* 接口 svm::fit 新增对参数 *params* 中键值"nu"输入值范围的检查。

## Zip

### *2.00.10* <!-- omit from toc -->

**新功能**

* 新增支持 Windows 系统。

**故障修复**

* 修复使用 zip::unzip 时若抛出异常时，已有 handle 未及时关闭的问题。

**功能优化**

* 优化了部分报错信息。
* 优化了终端的输出日志。

## Zlib

### *2.00.10* <!-- omit from toc -->

**新功能**

* 新增支持压缩同一个文件下的所有文件。

**功能优化**

* 优化了部分报错信息。

## ZMQ

### *2.00.10* <!-- omit from toc -->

**故障修复**

* 接口 zmq::cancelSubJob 增加传入参数限制，只接受标量。

**功能优化**

* 优化了部分报错信息。
