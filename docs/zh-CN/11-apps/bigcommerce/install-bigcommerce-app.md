---
title: 安装并授权 YundaDesk BigCommerce 应用
description: 从 BigCommerce 安装 YundaDesk，核对权限，并把店铺安全绑定到一个 YundaDesk 工作区。
category: 应用与集成
order: 1
updated_at: 2026-08-06
---

# 安装并授权 YundaDesk BigCommerce 应用

安装使用 BigCommerce 的单击授权流程。你不需要创建 API 账号、复制密钥或手动粘贴 Widget 代码。

## 开始之前

请准备：

- 可以为当前店铺安装应用的 BigCommerce 店铺所有者或已获授权用户；
- 一个现有 YundaDesk 账号，或用于创建新账号的公司邮箱；
- 一个你有权管理应用的 YundaDesk 工作区；
- 浏览器允许 `app.yundadesk.com` 打开新的安全标签页。

如果你计划显示店面聊天，请使用 Stencil 店面或 Catalyst 1.1 及以上版本。Blueprint 和未经验证的 headless 店面不能启用 YundaDesk Widget。

## 选择安装入口

你可以从 BigCommerce Marketplace 搜索 YundaDesk，也可以从 YundaDesk 应用中心开始。两个入口都会打开同一个 BigCommerce 官方应用详情和授权流程，不会创建两份安装。

### 从 YundaDesk 应用中心开始

1. 登录 YundaDesk，打开**应用**。
2. 找到 **BigCommerce** 卡片。
3. 如果按钮显示**前往 BigCommerce 安装**，选择它并在新标签页继续 BigCommerce 官方安装流程。

如果卡片显示**待平台上架**，表示公开 Marketplace 地址尚未可用，按钮会保持禁用。此时不要填写店铺标识、创建 API 账号或从第三方下载安装包；请等待正式上架或联系 YundaDesk 支持确认可用性。

YundaDesk 卡片不会直接索取 BigCommerce 店铺标识或 API 密钥。它只在应用公开后跳转官方安装页；安装并绑定工作区后，同一张卡片会切换为**已安装**和**查看店铺状态**。

### 从 BigCommerce 安装

1. 登录 BigCommerce 控制面板。
2. 打开 **Apps → Marketplace**，搜索 **YundaDesk**。
3. 打开 YundaDesk 应用详情页，选择安装。
4. 核对授权说明，然后确认安装。

![在 BigCommerce 中核对 YundaDesk 的安装权限](/help/assets/docs/bigcommerce/shared/01-install-permissions.jpg "安装前核对权限")

5. 如果 BigCommerce 继续显示访问更新确认页，请再次核对权限并选择 **Confirm**。这是 BigCommerce 完成单击 OAuth 授权的第二次确认，不需要复制 API 密钥。

![确认 YundaDesk 对 BigCommerce 店铺的访问](/help/assets/docs/bigcommerce/shared/02-confirm-access.jpg "确认 OAuth 访问")

YundaDesk 只读取客服上下文所需的店铺、客户、订单、商品、购物车和店面信息。BigCommerce 会自动为所有应用授权加入平台的基础店铺访问，因此安装页可能显示 **View and modify basic store information**；YundaDesk 不使用这项基础访问修改店铺设置。另一个内容修改权限仅用于通过 BigCommerce Scripts API 管理 YundaDesk 自己的店面脚本。YundaDesk 不修改订单、退款、库存、客户、结账或付款。

如果 Marketplace 中尚未显示 YundaDesk，表示该应用当前还未对你的店铺公开。不要从第三方下载非官方安装包；请联系 YundaDesk 支持确认可用性。

## 连接 YundaDesk 工作区

授权完成后，BigCommerce 会在控制面板中打开 YundaDesk 应用。

1. 选择 **Connect YundaDesk account**。
2. 在新打开的安全标签页中登录 YundaDesk，或创建新账号。
3. 核对由 BigCommerce 验证的店铺名称和店铺地址。这两项只读，不能在绑定页修改。
4. 选择应该管理该店铺的 YundaDesk 工作区。
5. 明确确认绑定。
6. 返回 BigCommerce 控制面板，选择 **I completed account linking**；如果页面已经关闭，也可以从 **Apps → My Apps → YundaDesk** 重新打开。

账号连接页在新标签页打开，不会嵌入第三方 iframe。BigCommerce 登录身份本身不会自动获得 YundaDesk 工作区权限。

## 完成首次设置

连接成功后，YundaDesk 应用会显示：

- BigCommerce 授权和 YundaDesk 工作区均为 **Connected**；
- Store、Customers、Orders 和 Products 的只读同步入口；
- Webhook 订阅健康状态；
- 检测到的 BigCommerce 店面及其兼容性；
- Installation Guide、User Guide 和联系支持入口。

接下来请[同步店铺数据并启用店面聊天](./use-yundadesk-with-bigcommerce.md)。主店面不会仅因安装而自动加载 Widget，仍需工作区管理员明确启用。

## 安装问题

### 没有安装权限

请让店铺所有者授予当前 BigCommerce 用户安装应用的权限，或由店铺所有者完成安装。

### 账号连接页没有打开

允许浏览器为 `app.yundadesk.com` 打开新标签页，然后再次选择 **Connect YundaDesk account**。不要把连接地址复制给其他人。

### 店铺已经连接到其他工作区

一个 BigCommerce 店铺同一时间只能绑定一个 YundaDesk 工作区。请先由原工作区管理员解除旧连接，再重新安装或绑定。

### 页面要求重新授权

店铺所有者需要从 BigCommerce 重新安装或重新授权 YundaDesk。重新授权前，数据同步和店面状态检查会暂停。
