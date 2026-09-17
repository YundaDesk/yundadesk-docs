---
title: 启用 WooCommerce 只读增强
description: 以只读方式授权 WooCommerce，并检查店铺数据、购物车上下文和事件状态。
category: 应用与集成
order: 3
updated_at: 2026-09-07
---

# 启用 WooCommerce 只读增强

WooCommerce 是同一个 YundaDesk 插件中的可选模式。WordPress Widget 不依赖它；只有管理员单独批准 WooCommerce **Read（读取）**权限后，店铺数据访问才会开始。

## 开始前

- 已将 WordPress 站点连接到 YundaDesk。
- 已安装并启用 WooCommerce 8.2 或更高版本。
- 当前账号可以同时管理 WordPress 设置与 WooCommerce。

## 授权 WooCommerce

1. 打开**设置 → YundaDesk**。
2. 找到 **WooCommerce 增强**。
3. 选择**连接 WooCommerce（只读）**。
4. 在 WooCommerce 授权页确认申请的权限为 **Read**。
5. 批准连接，然后返回**设置 → YundaDesk**。

![WooCommerce 只申请 Read 权限](/help/assets/docs/wordpress/zh/woocommerce-read-authorization.jpg "批准 WooCommerce 只读访问")

YundaDesk 不申请 **Write** 或 **Read/Write** 权限。你不需要创建或粘贴 Consumer Key、Consumer Secret；请通过上述授权页完成连接。

## 等待首次同步

授权完成后，**设置 → YundaDesk** 会确认 WooCommerce 只读访问已经连接。回到 YundaDesk，打开**应用 → WordPress → 管理站点**，核对对应地址的 **WooCommerce 只读数据**状态。也可以从 WooCommerce 应用卡的**查看店铺状态**进入同一管理界面。若仍显示同步中，请稍后刷新。

**站点聊天**和店铺数据授权相互独立。需要只读授权时，点击**打开 WordPress 设置**，在该站点单独批准授权；不要因为另一个站点已连接就认为当前店铺也已授权。

WordPress 设置页确认的是授权状态，不代表所有店铺数据已经可见。请在 YundaDesk 中核对对应店铺的商品和订单，再验证实际查单结果。

## 重新授权已有店铺

站点断开后重新连接、恢复历史连接或更换网站地址后，WooCommerce 可能需要重新授权。WordPress 显示**已连接**不代表店铺读取权限也已恢复。

1. 核对当前 WordPress 网站地址和 YundaDesk 中所选站点。
2. 在**设置 → YundaDesk**重新选择 WooCommerce 只读连接。
3. 在当前店铺的授权页批准 **Read**，然后返回设置页。
4. 回到 YundaDesk，刷新对应站点的状态并验证一笔该店铺的订单。

请分别处理每个站点，不要使用另一家店铺的授权代替当前店铺连接。

## 验证订单查询

1. 选择一笔用于验收的 WooCommerce 订单，核对订单号、下单邮箱、金额和当前状态。
2. 在 YundaDesk 中打开该客户的会话，确认客户邮箱与订单下单邮箱一致。
3. 在工作台右栏的店铺订单中核对所属店铺及订单信息。
4. 另外使用一个没有订单的测试邮箱，确认没有显示其他客户的订单。

如果仍然无法读取订单，请先核对店铺和邮箱，再检查是否提示重新授权。历史订单曾经显示过，不能代替本次连接的读取验证；不要将暂时无法读取理解为客户一定没有订单。

## 验证店铺上下文

1. 新建或修改测试商品、客户和订单。
2. 确认变化后的资源会在同步后出现在 YundaDesk。
3. 让已有 YundaDesk 会话的访客打开店铺前台。
4. 在站点实际使用的经典购物车和 Cart 区块中添加、修改并移除商品。
5. 确认当前购物车上下文会更新，且不发送地址、email 或电话。

购物车上下文会短期保存，并只属于当前访客会话。YundaDesk 不会把购物车标记为“弃购”。

## WooCommerce 被停用时

WordPress Widget 会继续工作，店铺同步与 WooCommerce 事件投递会暂停。重新启用 WooCommerce 后，请回到**设置 → YundaDesk**刷新授权状态，再在 YundaDesk 中核对站点增强和实时数据能力。

完整数据边界请阅读[WordPress 与 WooCommerce 数据和权限](./data-and-permissions.md)。
