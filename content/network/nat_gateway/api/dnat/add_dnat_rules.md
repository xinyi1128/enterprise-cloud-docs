---
title: "AddDnatRules"
description: 新增 DNAT 规则
draft: false
weight: 22
keyword: 青云, QingCloud, 云计算, API, NFV, NAT 网关, 网络组件, DNAT
---

新增 DNAT 规则。

**Request Parameters**

| Parameter name | Type | Description | Required |
| --- | --- | --- | --- |
| natgw_id | String | NAT 网关的 ID | Yes |
| name | String | DNAT 的 ID | No |
| public_port | String | 公网端口号 1-65535, 端口号或者范围, 如 80 或者 80-85 | Yes |
| private_port | String | 内网端口号 1-65535, 端口号或者范围, 如 8080 或者 8080-8085 | Yes |
| private_ip| String | 内网 IP 地址。 | Yes |
| protocol| String | 协议类型, tcp 或者 udp。 | Yes |
| eip_id| String | 公网 IP 的 ID。 | Yes |

[_公共参数_](../../get_api/parameters/)

**Response Elements**

| Name | Type | Description |
| --- | --- | --- |
| action | String | 响应动作 |
| dnat_ids | String | 新增 DNAT 规则的 ID |
| ret_code | Integer | 执行成功与否，0 表示成功，其他值则为错误代码 |

**Example**

_Example Request_

```
https://api.qingcloud.com/iaas/?action=AddDnatRules
&natgw_id=nfv-1234abcd
&name=test_dnat
&public_port=80-85
&private_port=80-85
&private_ip=172.17.0.2
&protocol=tcp
&eip_id=eip-9m3skybb
&COMMON_PARAMS
```

_Example Response_:

```
{
  "action":"AddDnatRuleResponse",
  "dnat_ids":[
    "dnat-p8zf9ytc"
  ],
  "ret_code":0
}
```
