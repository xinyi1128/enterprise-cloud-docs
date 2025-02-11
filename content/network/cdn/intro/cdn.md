---
title: "什么是CDN"
description: 介绍 CDN 服务的工作原理及应用场景。
keyword: QingCloud, 青云, 云计算, 网络, CDN 服务
draft: false
weight: 1
---

## 产品概述

CDN 的全称是 Content Delivery Network，即内容分发网络。通过在网络各处放置节点服务器所构成的在现有的互联网基础之上的一层智能虚拟网络， CDN 系统能够实时地根据网络流量和各节点的连接、负载状况以及到用户的距离和响应时间等综合信息将用户的请求重新导向离用户最近的服务节点上。其目的是使用户可就近取得所需内容，解决 Internet 网络拥挤的状况，提高用户访问网站的响应速度。

QingCloud CDN 服务支持用户自定义配置缓存策略规则、访问规则、防盗链、内容刷新等配置，灵活使用 CDN。并提供访问省份、访问文件次数、流量、带宽等丰富的监控统计，帮助用户时刻了解 CDN 使用情况。

## 工作原理

![](/network/cdn/_images/cdn_principle.png)

* **缓存服务器:** 用户直接获取资源的节点，如果用户访问资源在缓存服务器中不存在，则缓存服务器会向源站请求资源并缓存，然后返回给用户，下次用户访问时，缓存服务器可直接返回资源，不需要请求源站。
*   **源站:** 源站指发布内容的原始站点。添加、删除和更改网站的文件，都是在源站上进行的。缓存服务器所缓存的全部数据均是从源站获取。（图中的 web 站点）
*   **智能DNS:** 他的作用是根据用户的网络状况，把用户的请求指向最适合用户的缓存服务器。




## 应用场景

应用 QingCloud CDN 服务可以在以下几个场景中有效提升互联网业务中的访问效率：

- 用户与业务服务器所在地域间物理距离较远，需要进行多次网络转发，传输延时较高且不稳定。
- 用户使用的网络运营商与业务服务器所在运营商不同，请求需要运营商之间进行互联转发。
- 业务服务器所在网络的带宽和处理能力有限，当接收到海量用户请求时，导致响应速度降低、可用性降低。
