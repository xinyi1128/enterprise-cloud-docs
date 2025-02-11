---
title: "账户管理"
description: 账户管理
keyword: 青云,anybox,账户管理
weight: 10
draft: false
---

## 账户设置

作为管理员，你可以添加⾃己企业的标志以替换 ANYBOX 的标志，之后企业成员发出的所有共享链接上所展示的企业标志将都展示替换后的企业标志。

<img src="../../../_images/manager_menber16.png" style="zoom:50%;" />

点击左侧导航中的**设置** > **账户**这个页面下，可以对企业名称、企业标志进行修改。

- 修改企业名称
  
  在**企业名称**项后，点击**更新**，会弹出对企业名称的设置信息，可以对企业名称进行修改后，点击**确定**，即可企业名称进行修改保存。
  
- 修改企业标志
  
  在**企业标志**项后，点击**上传**，会弹出选择本地图片入口，选择完图片后根据系统规定大小进行裁剪，点击**确定**，即可企业标志进行修改保存。

## 登录设置

作为管理员，您可以添加⾃己企业的用户登录提示信息和设置用户登录方式。

<img src="../../../_images/manager_menber17.png" style="zoom:50%;" />

点击左侧导航中的**设置** > **登录**这个页面下，可以对登录页问候语、登录方式进行修改。

- 登录页问候语设置
  
  在**登录页问候语**项后，可以根据企业要求设置提示用户用户如何登录，即可在下面的**登录页预览**中查看修改后的展示效果。
  
- 登录方式设置
  
  在**登录方式**项后，可以根据企业要求选择登录方式（所有、邮箱/密码方式、用户名/密码方式）后，点击**保存修改**，即可对对登录页问候语、登录方式进行修改保存。

## 安全设置

ANYBOX 提供足够的安全设置以保障企业成员账户的安全，作为管理员可以对 ANYBOX 做以下安全设置。

<img src="../../../_images/manager_menber18.png" style="zoom:50%;" />

点击左侧导航中的设置 > **安全**这个页面下，可以对密码强度、IP黑名单、IP白名单进行设置。

- 密码强度设置
  
  在**密码强度**项后，点击**设置**，会弹出对密码强度的设置信息，可以根据企业要求设置密码最小长度。选择包含的格式类型后，点击**确定**，即可对密码强度进行设置保存。
  
  <img src="../../../_images/manager_menber19.png" style="zoom:50%;" />
  
- IP黑名单设置
  
  在**IP黑名单**项后，点击**管理**，会弹出对访问系统的 IP 黑名单的设置信息。点击**添加**，添加 IP 地址，点击**确定**，即可将此IP地址设置成此用户的 IP 地址黑名单。
  
  用户不能通过此IP地址访问 ANYBOX 系统。可以一次添加多个 IP 地址。
  
- IP白名单设置
  
  在**IP白名单**项后，点击**管理**，会弹出对访问系统的 IP 白名单的设置信息。点击**添加**，添加 IP 地址，点击**确定**，即可将此IP地址设置成此用户的 IP 地址白名单，则不在白名单内的 IP 禁止访问 ANYBOX 系统。可以一次添加多个IP地址。
  
- 短信认证设置
  
  在**短信认证项**后，可以选择是否开启登录进行短信二次认证，开启后，会根据**开启短信认证的密码错误次数设置**进行短信二次认证。

## 认证设置

作为管理员可以对 ANYBOX 的登录认证方式进行设置。

<img src="../../../_images/manager_menber20.png" style="zoom:50%;" />

点击左侧导航中的**设置** > **认证**页面下，可以对系统登录认证方式进行设置。

**系统登录认证方式包括但不限于：**

1. Local：采用 ANYBOX 系统自有的认证方式。

2. LDAP：采用企业自建的 LDAP 组织系统认证方式。

3. 企业微信：采用腾讯企业微信 APP 认证方式。

4. AD：采用企业自建的 AD 域认证方式。

5. HTTP：采用外部portal的认证方式。

   > **注意：**
   >
   > 通过 LDAP 和 AD 认证时，需要填写相关配置信息数据后，进行同步组织结构与用户信息后才能使用此认证方式。

## 设备管理

作为管理员，可以在控制台限制企业成员关联账户的设备数量，帮助企业管理企业成员账户在桌面及移动设备上的使用情况。

<img src="../../../_images/manager_menber21.png" style="zoom:50%;" />

点击左侧导航中的**设置** > **设备**页面下，可以管理企业成员账户在多设备上的使用情况进行设置。

- 移动设备
  
  在**移动设备**项，修改每位成员可关联的移动设备数量，系统会限制用户关联的桌面及移动设备的连接数量。
  
- API 请求次数限制
  
  在**API请求次数限制**项，可以根据企业要求选择每位成员每小时内 API 请求次数限制（1万次、2万次、10万次、50万次、1百万次），系统会限制用户每小时内发起API请求的请求次数。
  
- 用户访问速度限制
  
  在**用户访问速度限制**项，可以根据企业网络环境要求选择每位成员通过桌面及移动设备访问网盘的速度限制（500KB/s、1MB/s、10MB/s、20MB/s、50MB/s、100MB/s、无限制），系统会限制每位成员通过桌面及移动设备网盘上行和下行速度。

## 内容管理

作为企业管理员，可以在控制台**设置**对内容安全进行设置。

<img src="../../../_images/manager_menber22.png" style="zoom:50%;" />

点击左侧导航中的**设置** > **内容**这个页面下，可以对系统共享协作安全进行设置，包含：空间容量、外部共享链接、限制可被共享部门范围、上传文件大小限制、上传文件格式限制、文件版本限制、评论。

**系统登录认证方式包括但不限于：**

1. 空间容量
   
   对每位成员在 ANYBOX 中**个人工作空间**的可用的存储空间大小进行限制。
   
2. 外部共享链接

   对每位成员在 ANYBOX 中是否允许任何人访问共享链接的控制。

   开启后，企业外部用户也能访问共享链接。

   关闭后，只能是企业内部用户登录后才能访问共享链接。

3. 限制可被共享部门范围

   对每位成员在 ANYBOX 中是否允许共享给自己所在的部门及子部门以外的成员的控制。

   开启后，用户只能共享给自己所在的部门及子部门成员。

   关闭后，用户可以共享给自己所在的部门及子部门以外的成员。

4. 上传文件大小限制

   对每位成员在 ANYBOX 中通过网页端、桌面客户端、移动端应用可上传的最大文件大小进行限制。

5. 上传文件格式限制

   对每位成员在 ANYBOX 中用户不可上传的文件格式的限制。

   点击**管理文件格式**，在填写需要阻止上传的文件格式后缀。

   点击**添加**，即可限制此文件格式的文件上传至 ANYBOX 中。

   <img src="../../../_images/manager_menber23.png" style="zoom:50%;" />

6. 文件版本限制

   对在 ANYBOX 中，每个文件可保存的最多版本数量的限制，文件会自动保存最新的版本个数。

7. 评论

   对在 ANYBOX 中每个文件是否允许企业成员对可查看的企业文件进行评论。

   开启后，允许企业成员对可查看的企业文件进行评论。

   关闭后，禁止企业成员对可查看的企业文件进行评论，并且隐藏该文件夹中的所有评论。
