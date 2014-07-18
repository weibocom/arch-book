
# 分布式海量存储

## Redis

### 管理及运维问题
rdb 丢数据？
aof 重启慢?
Redis 2.8 psync 部分复制

### 存储空间
rediscounter的实现
eredis?

rediscounter的故障，hash插入很慢导致全部请求卡住

### 性能
### 冷热分离

- 管理及运维问题
- 存储空间问题
- 冷热分离问题

- Redis rolling counter for hot data (v1)
- redis-counter (v2)
  - save storage space
  - incremental replication
  - hot update
- Counter as a service (v3?)


- redis long－set data structure support
- Redis feed viewer(uv) counter
- Redis timer queue design pattern


## MySQL

- weibo graph index
- mysql slave load balance optimization
- mysql ha for big data
- mysql handler socket practice

保存全量计数器
问题：存储空间偏大，multi get性能一般，数据滚动维护不便；没有自然的冷热设计，需要按时间sharding。

- mysql master HA by architecture
- binary content storage
  - protocol buffers
  - varbinary replace varchar
- Sharding design
  - hot/normal data separate
  - sharding by date
  - second index for large dataset

## HBase

- HBase as a key list service (repost storage)
- HBase long-tail data optimization

## Queue

- Weibo firehose(streaming) service
- Weibo trigger(Successor of firehose)
- mytriggerq(mysql binlog message queue)
3月20日mytriggerq delay

https://github.com/Terry-Mao/MySQL-Syncer


- multi idc data bus(weibus)

## 架构、设计、存储选型
- 冷热分离
  - Redis数据滚动
  - MySQL按时间归档 
  
- Vector storage(and computing) as a service
- online data migration
- cell storage and computing
- auto increment id generator (multi idc)
- multi idc data storage arch
- SLA(Service Level Agreement) impl.
- Snapshot based unread feed counter
- DNS load balance for data service
chenbo 方案

一致性问题

- mytriggerq 延迟
- mytriggerq 多级部署结构