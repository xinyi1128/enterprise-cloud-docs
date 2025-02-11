---
title: "概述"
description: 本小节主要介绍 ChronusDB 冷热数据存储基本信息。 
keyword: ChronusDB 冷热数据存储；冷热存储；冷热分离；数据冷热分类
weight: 05
collapsible: false
draft: false
---



ChronusDB 内核使用 MergeTree 系列表引擎，支持将数据存储到多个对象存储中，提供数据多磁盘存储和数据冷热分层存储的功能，可大大降低海量数据存储的成本。

## 冷热数据

- 热数据
  
  访问频次较高的数据，对存储硬盘性能要求比较高，需满足高性能访问的需求，需存储到高性能热数据盘中，例如高性能 SSD 云盘和本地盘。

- 冷数据
  
  访问频次较低的数据，需满足高性价比存储需求，可存储到冷存储盘中，例如对象存储。

## 存储策略

ChronusDB 的数据存储提供了三种存储策略。

- 默认存储策略

  未开启对象存储策略，以及开启对象存储策略但未关联到表时，默认为 `default` 存储策略。`default` 存储表示新写入的数据直接存储在热数据盘中，可提供高效查询。

- 对象存储策略
  
  创建对象存储策略，且建表关联对象存储策略后，新写入的数据直接存储到冷数据盘，即存储到对象存储桶中。

- 冷热存储策略

  创建对象存储策略后，将生成`xxxx_hot_to_cold`冷热存储策略。建表通过配置冷热存储策略，系统可根据存储盘容量、存储时间等策略指标判断，进行冷热数据的迁移，实现冷热数据的分离，提供高性价比存储策略。
  
  - 基于磁盘容量
  
     当数据盘存储容量达到使用阈值时，自动将最早写入的数据迁移，实现冷热数据的自动分离。建表时支持指定存储数据盘，包括 **default** 默认磁盘或对象存储。

  - 基于 TTL 时间
  
     基于 TTL 时间的冷热存储策略，是通过添加 TTL 语句，设置数据存储生命周期，将指点时间之前的所有冷数据进行转移，实现数据的指定时间转移存储。

## 注意事项

- 对象存储策略适用于 ChronusDB `v1.0.8`及以上版本。若低于该版本，请先[升级集群版本](../../cluster_lifecycle/upgrade)。

- 创建对象存储策略，集群将自动重启。为避免数据丢失，请在业务低峰期操作。

- 当多个表共用一个存储策略时，在对象存储桶的数据统一存在同一目录下，不会按照表进行划分目录，可能对运维不友好。
