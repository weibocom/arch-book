# 缓存的可扩展性

## 缓存模型
* 按read through的方式来区分
* 按分布式方法来区分

## 容量设计
考虑内存分配
mc slab

![image](http://docs.oracle.com/cd/E17952_01/refman-5.6-en/images/memcached-memalloc.png)

Redis jemalloc

![image](https://fbcdn-sphotos-h-a.akamaihd.net/hphotos-ak-xap1/t1.0-9/167209_490348547199_7377432_n.jpg)

扩容与缩容

slab overflow

如何评估缓存的效能？

* 100M
* 50kqps

不可复制
commons工程

eviction策略，LRU

mc没有持久化功能（需要预热，但是需要delete或者ttl）
没有复制功能（但是复制带来延迟及一致性问题）

扩容容量的方法

* 按业务垂直拆分
* 单个业务增加节点

扩容访问量的方法

* 增加节点，但是批量取效率低
* 分层访问，保证批量效率，但是实现及维护复杂


## 一致性问题

## 讨论题


## 练习题