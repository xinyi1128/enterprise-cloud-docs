---
title: "命名空间授权"
description: 如何对不同的命名空间向不同用户进行授权。
keyword: 青云, QingCloud, 云计算, Docker, 镜像仓库，命名空间
draft: false
weight: 6
---

您可以针对不同的命名空间对不同用户进行授权。

## 前提条件

添加授权前，请确保已[创建用户](/container/dockerhub/manual/user_manage/)。

## 添加授权

1. 登录 [QingCloud 管理控制台](https://console.qingcloud.com/login)。

2. 在控制台顶部的菜单栏中，选择**产品与服务** > **容器服务** > **公有云镜像仓库**，进入**镜像仓库**页面。

3. 在页面左侧导航栏，点击**命名空间**，进入**命名空间**页面。

4. 点击需要进行授权操作的命名空间，进入命名空间的授权管理页面。

5. 点击**添加授权**。

   <img src="../../_images/add_auth.png" alt="添加授权" style="zoom:50%;" />

6. 选择需要授权的用户及权限。

   - Pull + Push：表示用户对命名空间下的镜像仓库既有访问和下载权限，还有推送权限。

   - Pull：表示用户对命名空间下的镜像仓库仅有访问和下载权限。

7. 点击**提交**。

## 修改授权

1. 在**授权管理**页面，勾选需要修改（可多选）的记录，点击**修改**。
2. 修改权限。
3. 点击**提交**。

## 移除授权

1. 在**授权管理**页面，勾选需要删除（可多选）的记录，点击 **移除授权**，弹出确认提示框。
2. 确认无误后，点击**确认**。
