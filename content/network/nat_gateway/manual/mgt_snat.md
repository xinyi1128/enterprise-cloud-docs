---
title: "管理 SNAT 规则"
descriptipn: 介绍如何进行 SNAT 规则的添加、修改、删除等操作。
draft: false
weight: 20
keyword: QingCloud, 云计算, 青云, NAT网关, NAT, SNAT, DNAT
---

## 前提条件

- 添加 SNAT 规则前，请确保您已经创建了 NAT 网关并绑定了公网 IP。具体操作，请参见[创建 NAT 网关](../../manual/mge_nat/create_nat/)及[绑定公网 IP](../../manual/mge_nat/bind_unbind_eip/)。
- 请检查**相关路由**标签页中是否有指向当前 NAT 网关的路由。如无，您还需要配置路由表规则，将私有网络流量指向 NAT 网关，SNAT 规则才生效。具体配置操作，请参考[配置指向 NAT 网关的路由](../mge_nat/nat_route/)。

## 注意事项

- SNAT 规则和 DNAT 规则一般面向不同的业务，如果使用相同的公网 IP，会面临业务相互抢占问题，故请尽量避免 SNAT 规则和 DNAT 规则共用一个公网 IP。

- 当云服务器同时配置公网 IP 服务和 NAT 网关服务时，数据均通过公网 IP 转发。

##  添加 SNAT 规则

1. 登录 [QingCloud 管理控制台](https://console.qingcloud.com/login)，在控制台导航栏中，选择**产品与服务** > **网络服务** > **NAT 网关**，进入 **NAT 网关**页面。

2. 在 NAT 网关列表中，点击目标 NAT 网关的 ID，进入详情页面。

3. 在 **SNAT 规则**标签页，点击**添加规则**。

   ![](../../_images/create_snat.png)

4. 按照下表说明，配置 SNAT 规则。

   | 参数              | 说明                                                         |
   | ----------------- | ------------------------------------------------------------ |
   | 名称              | SNAT 规则名称。<br>名称长度为2~128个字符，以大小写字母或中文开头， 可包含数字、下划线（_）和短划线（-）。 |
   | 资源类型          | <ul><li>**私有网络**：当选择私有网络时，私有网络所关联的路由表必须指向该 NAT 网关，私有网络下的云服务器均按照 SNAT 规则访问外网。</li><li>**云服务器**：当选择云服务器时，云服务器所属私有网络所关联的路由表必须指向该 NAT 网关，只有选定的云服务器按照 SNAT 规则访问外网。</li></ul> |
   | 私有网络/云服务器 | 根据所选择的资源类型，选择具体的私有网络或云服务器。可选择多个私有网络/云服务器，当选择多个时，将使用相同的公网 IP 创建多条 SNAT 规则。 |
   | 公网 IP           | 指定访问公网的公网 IP。<br/>可选择多个公网 IP。SNAT 规则使用多个公网 IP 时，业务运行时会随机选取其中的一个。 |

4. 点击**添加**。
5. 在 NAT 网关的基本信息区域右上方点击**应用修改**使配置生效。

## 修改 SNAT 规则

> **注意**
>
> 修改已有 SNAT 规则中的公网 IP，可能导致原有业务连接中断，重连后即可恢复，请谨慎操作。

1. 登录 [QingCloud 管理控制台](https://console.qingcloud.com/login)，在控制台导航栏中，选择**产品与服务** > **网络服务** > **NAT 网关**，进入 **NAT 网关**页面。

2. 在 NAT 网关列表中，点击目标 NAT 网关的 ID，进入详情页面。

3. 在 **SNAT 规则** 标签页，点击**操作**列的**修改**。

   ![](../../_images/mdy_snat.png)

4. 在弹出的窗口中，修改 SNAT 规则。

   可修改**名称**及**公网 IP**。

5. 点击**确定**。

## 禁用/启用 SNAT 规则

1. 登录 [QingCloud 管理控制台](https://console.qingcloud.com/login)，在控制台导航栏中，选择**产品与服务** > **网络服务** > **NAT 网关**，进入 **NAT 网关**页面。
2. 在 NAT 网关列表中，点击目标 NAT 网关的 ID，进入详情页面。
3. 在 **SNAT 规则**标签页，点击**操作**列的**禁用**/**启用**。
4. 在弹出的确认窗口中，点击**确定**。

5. 点击**应用修改**，等待 NAT 网关更新完成。

   禁用成功后， SNAT 规则状态变更为**已禁用**。

   启用成功后， SNAT 规则状态变更为**活跃**。

## 删除 SNAT 规则

1. 登录 [QingCloud 管理控制台](https://console.qingcloud.com/login)，在控制台导航栏中，选择**产品与服务** > **网络服务** > **NAT 网关**，进入 **NAT 网关**页面。

2. 在 NAT 网关列表中，点击目标 NAT 网关的 ID，进入详情页面。

3. 在 **SNAT 规则**标签页，点击**操作**列的**删除**，弹出确认框。

   若要批量删除多条规则，则勾选需要删除的规则，点击列表上方的**删除**。

4. 在弹出的确认窗口中，点击**确定**。

