# Release Notes for DolphinDB Plugins

- [AWSS3](#awss3)
- [HBase](#hbase)
- [HDFS](#hdfs)
- [HDF5](#hdf5)
- [HTTP Client](#http-client)
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
- [Zlib](#zlib)
- [Zip](#zip)
- [ZMQ](#zmq)



## AWSS3

### *Version 2.00.10* <!-- omit from toc --> 

**Enhancement**

-  Temporary files to be loaded with `loadS3Object` will not be removed immediately. 

**Bug Fixes**

- Added limit (10) to parameter *threadCount* of `loadS3Object`.
- Added validation check for the *outputFileName* parameter of `getS3Object`.

## HBase

### *Version 2.00.10* <!-- omit from toc --> 

**Enhancement**

- Enhanced the stability of this plugin during multi-threaded operations.

**Bug Fixes**

- Strings that cannot be converted to MINUTE will not be parsed when using `hbase::load`.
- Calling `hbase:load` to load a table that has been disabled will raise an exception, and terminate the execution, instead of crashing the server.
- Added limit to the string length for its conversion to DolphinDB CHAR. If the length of the string is larger than 1, a NULL value is returned.
- Added check for the conversion of data of SECOND type.
- Calling plugin methods after closing the connection now correctly raises an error instead of crashing the server. 
- Added input validation for the *isFramed* parameter of function `connect`.

## HDFS

### *Version 2.00.10* <!-- omit from toc --> 

**Enhancements**

- Cluster environment can now be configured with cluster IP address specified in function `connect`. 
- Enhanced error messages.

**Bug Fixes**

- Fixed an error when using `getListDirectory` on an empty folder. 
- Fixed the issue that caused the `readFile` function to fail when used within a `do-while` loop. The problem was caused by having too many open file handles, which resulted in an unavailable and disconnected Hadoop data node. 
- Fixed the conflict of two handles returned by `connect` as they shared the same hdfs connection.

## HDF5

### *Version 2.00.10* <!-- omit from toc --> 

**Enhancement**

- Enhanced error texts for `hdf5::saveHDF5`. 

**Bug Fixes**

- Fixed the issue where the server crashed when `hdf5::ls` is used on a specific HDF5 file. 
- Fixed the issue where the server crashed when importing multiple files in parallel. 

## HTTP Client

### *Version 2.00.10* <!-- omit from toc --> 

**New Features**

- Added validation for parameters that use the dictionary data form.
- The plugin now performs a check of the byte length of the data to be sent.

**Enhancement**

- Removed methods `httpCreateSubJob`, `httpCreateMultiParserSubJob`, `httpCancelSubJob` and `httpGetJobStat`.
## Kafka

### *Version 2.00.10* <!-- omit from toc --> 

**Enhancement**

- Added return values for functions `eventGetParts`, `getOffsetPosition`, and `getOffsetCommitted`.

**Bug Fixes**

- Fixed an issue where the interface `kafka::pollByteStream` failed to receive data in non-JSON format. 
- Fixed the issue where the crashes occurred due to multi-threaded operations. 

## kdb+

### *Version 2.00.10* <!-- omit from toc --> 

**New Feature**

- The plugin now supports nested lists containing kdb+ char type elements.

**Bug Fixes**

- Fixed an issue that caused the server to crash when calling `loadTable()` without passing the *symPath* parameter. 
- Fixed an issue where calling `loadTable()` could not correctly parse a kdb+ sym file if the file name is not “sym“.
- Fixed an issue where calling `loadTable()` after terminating the kdb+ process could crash the server. 

## mat

### *Version 2.00.10* <!-- omit from toc --> 

**New Feature**

- Added support for reading *.mat* files using multiple threads.  

**Bug Fix**

- Added input validation for the *varName* parameter of `mat::writeMat`.

## MongoDB

### *Version 2.00.10* <!-- omit from toc --> 


- Enhanced error messages.
- Improved parameter validation for `mongodb:connect`, `mongodb::load` and `mongodb::aggregate`.

## MQTT

### *Version 2.00.10* <!-- omit from toc --> 

**Bug Fixes**

- If an MQTT server is closed, an error message is reported when connecting through `mqtt::connect`.

- Fixed the error message of the default value of the batchSize parameter of method `connect`.

- Fixed the issue where the server crashed or got stuck when NULL values are passed as arguments to `mqtt:publish` or `mqtt::createCsvFormatter`.

- Fixed the issue where the subscriber failed to receive published data containing NULL values.

- Fixed the issue where the subscriber received data of incorrect data types when the published data contained data of CHAR or MONTH type.

## mseed

### *Version 2.00.10* <!-- omit from toc --> 

**Bug Fixes**

- Added input validation for the *startTime* parameter of `mseed::write`.
- An error will be reported when the input data of `mseed::parseStreamInfo` cannot be parsed or the parsed sid (Station Identifier) is invalid.
- Added check for `mseed:parse` when an empty string is passed in, and an error will be reported in this case.
- Added input validation for `mseed::read`.

## MySQL

### *Version 2.00.10* <!-- omit from toc --> 


- Calling plugin methods after closing the connection now correctly raises an error instead of crashing the server.

## ODBC

### *Version 2.00.10* <!-- omit from toc --> 

**Enhancements**

- Enhanced error message.
- Added input validation for `odbc::close`.  

**Bug Fixes**

- Fixed a crash when multiple threads use the same connection to append data concurrently.
- Fixed a server crash which happened occasionally when closing an ODBC connection.

## OPC

### *Version 2.00.10* <!-- omit from toc --> 


- Fixed the issue where the server crashed due to unsubscription after multiple subscriptions through the same connection.

## OPCUA

### *Version 2.00.10* <!-- omit from toc --> 

- Fixed the issue where the server crashed due to multi-threaded jobs.

## ORC

### *Version 2.00.10* <!-- omit from toc --> 

**Enhancement**

- Optimized data processing when importing data of temporal or string type as numeric values.

**Bug Fix**

- Fixed the incorrect outputs when accessing temporal values with NULL.

## Parquet

### *Version 2.00.10* <!-- omit from toc --> 


- Enhanced error messages.


## SchemalessWriter

### *Version 2.00.10* <!-- omit from toc --> 

- Added new plugin SchemalessWriter.

## Signal

### *Version 2.00.10* <!-- omit from toc --> 


**Bug Fixes**

- Fixed a memory leak when calling `signal::secc` frequently.
- Fixed a crash caused by concurrent execution of methods `signal::fft`, `signal::ifft`, and `signal::secc` by multiple threads.
- Fixed the wrong plus and minus signs of the output returned by `signal::fft` when the number of *X* was even.

## SVM

### *Version 2.00.10* <!-- omit from toc --> 

**Enhancement**

- Added input validation for the key-value “nu” in parameter *params* of method `svm:fit`.

**Bug Fix**

- Fixed server crash caused by multi-threaded execution of `svm:fit`.

## Zlib

### *Version 2.00.10* <!-- omit from toc --> 

**New Feature**

- Compressing a folder is now available.

**Enhancement**

- Enhanced error messages.

## Zip

### *Version 2.00.10* <!-- omit from toc --> 

**New Feature**

- The plugin is now compatible with Windows operating systems.

**Enhancements**

- Enhanced error messages. 
- Enhanced the log messages that are printed to the console. 

**Bug Fix**

- Fixed an issue where the plugin did not properly close open file handles when an exception was thrown. This caused the unused open file handles to build up over time.

## ZMQ

### *Version 2.00.10* <!-- omit from toc --> 

**Enhancement**

- Enhanced error messages.

**Bug Fix**

- Added input validation for `zmq::cancelSubJob` that only accepts a scalar.
