---
title: 在 BigCommerce 使用 YundaDesk
description: 同步只读店铺数据，为兼容店面启用 Widget，并在 YundaDesk 工作台查看客服上下文。
category: 应用与集成
order: 2
updated_at: 2026-09-08
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
4. 核对**店铺数据**连接。**前台聊天**下方会按店面显示地址、聊天状态和**打开店铺并检测**按钮。
5. 对已启用的兼容店面，选择其卡片中的**打开店铺并检测**，在新标签页打开该店面并检查聊天入口。**上次验证通过**表示此前的检测结果；要确认当前状态，请再次检测。 如果没有自动打开新标签页，请点击同一位置的**继续打开店铺**；它会继续本次检测，不需要重新创建检测。
6. 选择底部的**设置店铺前台聊天**，在新标签页打开该店铺的 YundaDesk 应用配置页，在其中分别管理各店面。未启用的店面需要先在这里启用，才能进行检测。

超过三个店面时，选择**展开其余店面**查看完整列表；超过五个时，展开后的列表可以内部滚动。底部左侧的**帮助中心**打开 BigCommerce 帮助，右侧的刷新按钮更新连接状态。

YundaDesk 卡片用于快速查看已绑定店铺的连接与店面聊天状态。资源同步、Webhook 修复、各店面启停和 Script 修复等 BigCommerce 专属操作，仍从 BigCommerce 控制面板的 **Apps → My Apps → YundaDesk** 完成。

## 管理多家店铺

一个工作区可以连接多家 BigCommerce 店铺；每家店铺还可以包含多个店面。店铺列表会显示当前店铺数量，每家店铺的连接状态、店面地址和操作分别展示。

- **连接新店铺**：在列表底部选择此按钮，前往 BigCommerce 登录并选择要安装的店铺。确认实际店铺和目标工作区后完成连接；返回 YundaDesk 时会定位刚连接的店铺。
- **前往 BigCommerce 卸载**：在要移除的店铺卡片底部、**设置店铺前台聊天**左侧选择此按钮，打开该店铺的 **Apps → My Apps**。确认当前店铺名称，再从 YundaDesk 应用菜单执行卸载。卸载影响这家店铺的全部店面，不影响其他独立店铺。
- **查看结果**：返回 YundaDesk 后查看或刷新状态。打开后台页面本身不代表已卸载；确认卸载结果后，该店铺会从当前列表移除。最后一家店移除后，仍可重新连接店铺。

如果 BigCommerce 要求登录、切换店铺或申请权限，请在 BigCommerce 完成这些操作。没有应用管理权限的 YundaDesk 成员可以查看连接状态和帮助，但不能使用连接、卸载引导或聊天设置入口。

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
5. 等待状态变为 **Enabled**。这表示该店面已启用，接着还需要打开店面验证聊天是否加载。

YundaDesk 通过 BigCommerce Scripts API 创建自己的 functional、footer、deferred Script。你不需要复制 JavaScript。BigCommerce 可能需要短暂时间刷新新脚本；请等待一分钟后再测试公开店面。

Stencil 和已确认版本的 Catalyst 店面受支持。Blueprint 与未经验证的 headless 店面会显示为不支持，不能强制启用。

## 验证 Widget 和真实消息

在对应店面选择 **Open storefront and check**，或在 YundaDesk 的店面行选择**打开店铺并检测**。浏览器会打开该店面，并检查聊天是否加载。

- **Verification pending / 已启用 · 待验证**：已启用聊天，尚未完成本次检测。
- **Verified in this check / 已嵌入**：本次打开店面已检测到聊天加载。
- **Previously verified / 上次验证通过**：此前检测成功，不能据此判断当前页面。
- **Widget not detected / 未检测到嵌入**：本次没有检测到聊天，请核对店面、浏览器拦截和聊天状态后重试。

每个店面要分别检测。关闭一个店面的聊天不会断开店铺数据，也不会关闭其他店面的聊天。

继续验证真实消息：

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

## 重新连接后的聊天状态

普通重新授权后，原工作区中仍然正常的已启用店面会保留启用状态，已停用店面保持停用。脚本缺失需要确认修复；店面地址变化需要重新确认启用。

如果先卸载再重新安装，需要重新确认工作区，并逐个启用所需店面；旧的启用选择不会自动恢复。
