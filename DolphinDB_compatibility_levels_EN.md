- [DolphinDB Compatibility Levels](#DolphinDB-Compatibility-Levels)
  - [1. Background](#1-Background)
  - [2. Terms and Definitions](#2-Terms-and-Definitions)
  - [3. Compatibility Level](#3-Compatibility-Level)
    - [3.1 Compatibility Level 1](#31-Compatibility-Level-1)
    - [3.2 Compatibility Level 2](#32-Compatibility-Level-2)
    - [3.3 Compatibility Level 3](#33-Compatibility-Level-3)
    - [3.4 Compatibility Level 4](#34-Compatibility-Level-4)
    - [3.5 Compatibility Level 5](#35-Compatibility-Level-5)
    - [3.6 Overview of Compatibility Levels](#36-Overview-of-Compatibility-Levels)
  - [4. Commitment](#4-Commitment)

## 1. Background

This tutorial mainly explains the compatibility levels of DolphinDB servers, SDKs, and plug-ins. You can refer to the requirements of each compatibility level to quickly learn the potential risks of upgrades. For security update, the latest and stable versions of DolphinDB server ensure backward compatibility.

Starting from version 1.30.17 and 2.00.5, DolphinDB will specify the compatibility level of each version in the release notes. Incompatibilities will be specified, and corresponding solutions will be provided. The release candidates and stable versions of DolphinDB server ensure backward compatibility at a minimum.

## 2. Terms and Definitions

**Backward Compatibility** refers to the ability of a newer version of the software to accept configurations, data, and programs that worked of the old version.

**Forward Compatibility** refers to the ability of the old version of the software to accept configurations, data, and programs of the new version.

**Rollback** is an operation which rolls back to the old version when risks are found after the upgrade. It can be categorized into three cases according to whether the database files are updated.

(1) **Unconditional rollback**. If the new version does not update the format of data files, log files and metadata, you can always roll back to the old version regardless of whether the data has been written after the upgrade.

(2) **Rollback after backing up metadata**. Data file format remains the same, while metadata format has been updated. During the restart process after the upgrade, the system will perform a checkpoint on the edit log to generate new metadata. After rolling back to the old version, however, the metadata file in the new format will not be readable. We can back up the metadata before upgrading in case of this situation.

(3) **Rollback after graceful shutdown**. The data file format has been updated. Even if the user does not write data after the restart, it is possible that data will be written to the database file by redo log. This way the data cannot be read after rolling back to the old version. To solve this problem, DolphinDB has supported graceful shutdown since version 1.30.17 and 2.00.5 to ensure that all data in redo log is written to the database file before shutting down the node.

**Rolling upgrade**: The traditional way to upgrade a cluster usually shuts down all nodes and then upgrades them to the new version before restarting. Upgrading in this way, however, will cause service interruption. Rolling upgrade means that upgrades can be performed on a node-by-node basis with uninterrupted service. After a node is upgraded and operates smoothly, another node is upgraded, and so on until all nodes are upgraded.

Supporting rolling upgrades requires that in-memory data formats, including transmission protocols, serialization protocols, etc., need to be fully compatible between the new and the old version.

During a rolling upgrade, the system remains online. This requires that the new version has a high compatibility level and the cluster must be deployed for high availability.

**Plugins and SDKs compatibility**: Plugins and SDKs compatibility includes binary compatibility and source compatibility. 

For plugins, binary compatibility means that the old version of plugins (dynamic library) can be loaded and run on the new version of the server. Source compatibility means that the code written with the old plugin version can be run on the new plugin version without any modifications. When upgrading the database server, you can choose not to upgrade plugins if they satisfy by binary compatibility conditions.

As for SDKs (Python, C++, Java, C#, etc.), binary compatibility means that the old version of the SDK (usually in the form of dynamic libraries) is compatible with the new version of the server. Source compatibility means that SDK interfaces are compatible with the existing client codes.

## 3. Compatibility Level

There are 5 compatibility levels in DolphinDB. A higher compatibility level has stricter requirements. If a version satisfies a specific compatible level, all lower compatible levels are also satisfied.。

### 3.1 Compatibility Level 1

Compatibility level 1 generally guarantees backward compatibility for DolphinDB server to ensure that data and codes of the old version can be used in the new version with the following exception:

(1)	Some built-in functions declared as deprecated for over 1 year may be dropped. 
(2)	Source compatibility of plugins may not be supported, which means that binary library files may need to be updated and the script that calls the plugin function may need to be modified. 
(3)	Binary compatibility of SDKs may not be supported, i.e., the dynamic library of SDKs must be updated, whereas the code compatibility can be guaranteed.

The compatibility level requirements of plugins and APIs are different because plugins run in the same process as DolphinDB server and the header files of plugins often change as the server changes, while SDKs only need to be compatible with the server communication protocol.

- **Requirements:**

1. Compatible with the configurations of the old version. Configuration parameter names and default values cannot be modified.
2. Compatible with functions and codes of the old version. The function names cannot be modified. Function parameters can only be added, and new parameters need to have default values. The usage of scripts cannot be modified. Some functions declared as deprecated for over 1 year may not be supported.
3. Compatible with data of the old version, including DFS tables, persisted stream table, scheduled tasks, function views, and user access control.
4. Source compatibility of SDKs is supported. The client programs written with SDKs can continue to run after recompiling and linking.

- **Upgrade Guide:**

1. Level 1 does not support source compatibility of plugins and binary compatibility of API. When upgrading the server, the binary library files of plugins and APIs must be upgraded. The API client needs to be recompiled, and scripts of plugins may need to be modified.
2. The database file format may have changed. To ensure rollback safety, a graceful shutdown must be completely before upgrading to ensure that all redo logs have been garbage-collected.

### 3.2 Compatibility Level 2

Compatibility level 2 ensures full backward compatibility. In additions to all requirements of level 1, level 2 requires that DolphinDB server is compatible with all functions and codes of the old version. Source compatibility of plugins and SDKs is supported. After binary files of plugins are upgraded, the codes written with plugins can continue to be run.

- **Requirements:**

1.	Compatible with the configurations of the old version. 
2.	Compatible with functions and codes of the old version. 
3.	Compatible with data of the old version, including DFS tables, persisted stream table, scheduled tasks, function views, and user access control.
4.	Source compatibility of plugins is supported, i.e., the binary files need to be upgraded, but codes that call the plugins do not need to be modified.
5.	Source compatibility of SDKs is supported. Client codes can connect to the new version of the server if they are compiled and linked with the new SDK.

- **Upgrade Guide:**

1.	When upgrading, the binary library files of plugins may need to be upgraded.
2.	The database file format may have changed. To ensure rollback safety, a graceful shutdown must be completely before upgrading to ensure that all redo logs have been garbage-collected.

### 3.3 Compatibility Level 3

Based on compatibility level 2, level 3 supports binary compatibility of plugins and SDKs.

**Requirements:**

1.	Compatible with the configurations of the old version. 
2.	Compatible with functions and codes of the old version. 
3.	Compatible with data of the old version, including DFS tables, persisted stream table, scheduled tasks, function views, and user access control.
4.	Binary compatibility of plugins and SDKs is supported, which means that plugins and SDKs can run without upgrading.

**Upgrade Guide:**

Backing up your metadata of the controller and data nodes before the upgrade. After rolling back, you need to restore backups of the old version first.

### 3.4 Compatibility Level 4

Based on compatibility level 3, level 4 requires that the new version can be conditionally rolled back to the old version and supports rolling upgrades, which means that DolphinDB clusters can be upgraded node by node. After a node updates and operates smoothly, another node is upgraded. During the upgrade process, if an exception occurs, you can quickly roll back to the old version, which greatly reduces the upgrade risks.

In addition, it should be noted that supporting rolling upgrade requires the data format and transfer protocols in memory to be fully compatible.

**Requirements:**

1.	Compatible with the configurations of the old version. 
2.	Compatible with functions and codes of the old version. 
3.	Compatible with data of the old version, including DFS tables, persisted stream table, scheduled tasks, function views, and user access control.
4.	Binary compatibility of plugins and SDKs is supported, which means that plugins and SDKs can run without upgrading.
5.	Support conditional rollback. You can roll the new version back to the old version to continue running, provided that the data have not been written in.
6.	Compatible with the in-memory data of the old version, including in-memory tables, matrices, vectors, and the transfer protocols, etc., to support rolling upgrades for each node of the cluster.

### 3.5 Compatibility Level 5

Compatibility level 5 is the highest-level of DolphinDB server, which supports rolling upgrades and unconditional rollback.

**Requirements:**

1.	Compatible with the configurations of the old version. 
2.	Compatible with functions and codes of the old version. 
3.	Compatible with data of the old version, including DFS tables, persisted stream table, scheduled tasks, function views, and user access control.
4.	Binary compatibility of plugins and SDKs is supported, which means that plugins and SDKs can run without upgrading.
5.	Compatible with the in-memory data of the old version, including the data of in-memory tables, variables such as matrices and vectors, and the transmission protocol, etc., to support rolling upgrades for each node of the cluster.
6.	Support unconditional rollback. After the upgrade, even if the data has been written to the database of the new version, the system can continue to run after rolling back to the old version.

### 3.6 Overview of Compatibility Levels

The requirements for different levels of compatibility are shown in the table below:

|              | **Configuration** | **Functions and Scripts**                             | **Stored Data** | **Plugins**       | **SDK**  | **Rolling Upgrade** | **Rollback**     |
| ------------ | -------- | ------------------------------------------ | ------------ | -------------- | -------- | ------------ | ---------------- |
| **Level 1** | Compatible     | Built-in functions declared as deprecated for over 1 year may be dropped. | Backward Compatible     | Source Code Potentially Incompatible | Source Code Compatible | Potentially Unsupported  | Rollback after Graceful Shutdown   |
| **Level 2** | Compatible     | Compatible                                       | Backward Compatible     | Source Code Compatible       | Source Code Compatible | Potentially Unsupported  | Rollback after Graceful Shutdown   |
| **Level 3** | Compatible     | Compatible                                       | Forward Compatible     | Upgrade Not Required       | Upgrade Not Required  | Potentially Unsupported   | Rollback after Metadata Backup |
| **Level 4** | Compatible     |Compatible                                       | Forward Compatible     | Upgrade Not Required       | Upgrade Not Required  | Supported         | Rollback after Metadata Backup |
| **Level 5** | Compatible     | Compatible                                       | Forward Compatible     | Upgrade Not Required       | Upgrade Not Required  | Supported         | Unconditional Rollback       | 

## 4. Commitment

There are 3 types of DolphinDB major versions: stable releases, release candidates, and beta releases. 

A major version upgrade of the DolphinDB server, such as from 1.20 to 1.30, from 1.30 to 2.00, usually meets Level 1 standards, and occasionally meets Level 2 standards. Level 1 may not support source code compatibility of plugins or binary code compatibility of SDKs. When upgrading DolphinDB, you may need to upgrade the binary library files of plugins and SDKs, recompile API clients and update the scripts calling plugin functions. Please refer to the release notes for details. Note that rollback is supported at Compatibility Levels 1 and 2, but it's required to back up the metadata of the controller and data nodes and shutdown gracefully before upgrading.

A patch version upgrade of the DolphinDB server, such as from 1.30.17 to 1.30.18, usually meets Level 4 or 5 standards, and occasionally only meets Level 3 standards. However, a minor version upgrade of the DolphinDB beta releases may have significant modifications and can only meet Compatibility Level 1 or 2 standards.

If an upgrade skips versions, the compatibility standards take the minimum of the compatibility levels between the adjacent versions. For example, the compatibility level is 4 when upgrading from 1.30.16 to 1.30.17, and 3 from 1.30.17 to 1.30.18, then the upgrade from 1.30.16 to 1.30.18 meets Level 3 standards. To upgrade with multiple versions skipped, you can contact DolphinDB technical support for risk assessment.

 

 

 

 

 

 

 

 

 

 

 

 