## 2.1.8

*发布日期: 2024-09-09*

### Features
- 实现 `Key-Value` 存储模型，协议层完全兼容 Redis 协议，详见[Key-Value](../key-value-data-model/overview.md)。
- 实现 `information_schema` 数据库，以方便对元数据进行管理（暂不支持对 information_schema 中的表进行聚合、投影等操作，预计下个版本支持）。

### 增强
- 对配置文件的层级关系进行了优化。
- 对于系统中一些无效的元数据进行快速回收、清理。

### 修复
- 修复 TIMESTAMP 转换可能导致 `panic` 的问题。



## 2.1.7

*发布日期: 2024-08-23*

### Features
- 支持 `trim database` 语句，实现对资源进行加速回收。
- 在集群模式下，对于存储的数据支持混合缓存（内存与磁盘），提升数据查询效率。 
- 在本次发版本中，增加了对 ARM 的支持。
- 在 `dlsql` 中，支持通过`\G`对数据进行格式化输出。
- 支持与 EMQX 进行对接，可通过  EMQX 的规则引擎将数据持久化到 Datalayers 中。

### 增强
- 对 HTTP 返回的结构进行调整。
- 优化 InfluxDB 行协议写入。


### 修复
- 在 `dlsql`中，当返回结果为空时的显示问题。
