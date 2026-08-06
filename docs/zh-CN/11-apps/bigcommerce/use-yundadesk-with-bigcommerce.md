---
title: 在 BigCommerce 使用 YundaDesk
description: 同步只读店铺数据，为兼容店面启用 Widget，并在 YundaDesk 工作台查看客服上下文。
category: 应用与集成
order: 2
updated_at: 2026-08-06
---

# 在 BigCommerce 使用 YundaDesk

完成安装和工作区绑定后，可以在 BigCommerce 内管理同步、Webhook 与店面聊天，也可以从 YundaDesk 应用中心快速查看连接状态，再到 YundaDesk 工作台接待客户。

## 打开应用状态页

1. 登录 BigCommerce 控制面板。
2. 打开 **Apps → My Apps → YundaDesk**。
3. 确认 **BigCommerce authorization** 和 **YundaDesk workspace** 均显示 **Connected**。

只有已连接到该工作区的 YundaDesk 成员才能查看工作区状态。同步、Webhook 修复和店面变更还需要管理应用的权限。

## 从 YundaDesk 应用中心管理

1. 登录 YundaDesk，打开**应用**。
2. 找到显示**已安装**的 **BigCommerce** 卡片。
3. 选择**查看店铺状态**。
4. 核对**店铺数据**连接和**前台聊天**状态；需要时刷新状态或打开店面进行验证。

YundaDesk 卡片用于快速查看已绑定店铺的连接与店面聊天状态。资源同步、Webhook 修复、各店面启停和 Script 修复等 BigCommerce 专属操作，仍从 BigCommerce 控制面板的 **Apps → My Apps → YundaDesk** 完成。

## 同步只读店铺数据

在 **Commerce data** 区域，依次为以下资源选择 **Sync now**：

- **Store**：店铺基本信息；
- **Customers**：用于识别和服务客户的最小资料；
- **Orders**：订单状态、金额和商品摘要；
- **Products**：商品与变体的客服上下文。

首次同步会排队处理。稍后选择 **Refresh status** 查看最新状态。重复同步会更新已有记录，不会创建重复的店铺对象。

**Carts** 和 **Abandoned checkouts** 使用安装后的实时事件，不提供历史回填，也没有手动全店同步按钮。只有 Webhook 处于健康状态后产生的新事件才会开始记录。

## 检查 Webhook 状态

**Webhook subscriptions** 显示 YundaDesk 所需订阅是否全部健康。Webhook 用于保持客户、订单、商品、库存、购物车和卸载状态为最新。

状态检查是只读的，不会自动重建缺失订阅。如果页面显示 **Repair required**：

1. 使用具有应用管理权限的 YundaDesk 成员账号打开应用。
2. 选择 **Repair webhooks**。
3. 阅读确认提示后再次确认。
4. 完成后刷新状态。

## 为店面启用在线客服

YundaDesk 会在 **Storefront chat** 中列出检测到的店面。每个店面都要单独启用。

1. 找到主店面或要启用的其他店面。
2. 核对店面地址和类型。
3. 选择 **Enable storefront chat**。
4. 如果是 Catalyst，确认该店面运行 Catalyst 1.1 或更高版本。
5. 等待状态变为 **Active**。

YundaDesk 通过 BigCommerce Scripts API 创建自己的 functional、footer、deferred Script。你不需要复制 JavaScript。BigCommerce 可能需要短暂时间刷新新脚本；请等待一分钟后再测试公开店面。

Stencil 和已确认版本的 Catalyst 店面受支持。Blueprint 与未经验证的 headless 店面会显示为不支持，不能强制启用。

## 验证 Widget 和真实消息

1. 使用隐私浏览窗口打开刚启用的店面地址。
2. 接受或设置店面的 Cookie 选择；YundaDesk Script 会遵循 BigCommerce 的 functional consent 配置。
3. 确认页面只显示一个 YundaDesk 聊天入口。
4. 发送一条不包含个人隐私的测试消息。
5. 登录 YundaDesk，打开**工作台**，确认新会话进入正确工作区。
6. 从工作台回复，再确认店面 Widget 收到回复。

如果一个工作区连接了多家店，请在工作台核对会话的店铺来源。只有平台已经验证并同步的客户或订单信息才应作为店铺上下文显示。

## 在工作台查看订单上下文

在 YundaDesk 工作台打开来自 BigCommerce 的客户会话。客户侧栏会在可关联时显示只读店铺上下文，例如订单状态、金额、商品摘要和更新时间。

这些信息用于帮助客服回答“订单状态如何”“买了什么”等问题。YundaDesk 不提供退款、取消订单、修改地址、改库存、改客户、改折扣或付款操作。

## 管理多个店面

- 逐个启用需要在线客服的兼容店面。
- 每个店面使用自己的地址和脚本状态；启用一个店面不会自动启用其他店面。
- 选择 **Disable** 后，该店面的 YundaDesk Widget 会停止加载，不影响其他已启用店面。
- 如果管理员在 BigCommerce Script Manager 中删除了 YundaDesk Script，应用只会显示 **Script missing**，不会自动写回。确认后选择 **Repair Script** 才会重建。

继续阅读[数据权限、多人访问与卸载说明](./data-permissions-and-lifecycle.md)。
