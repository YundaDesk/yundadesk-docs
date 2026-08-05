---
title: 启用 WooCommerce 只读增强
description: 以只读方式授权 WooCommerce，并检查店铺数据、购物车上下文和事件状态。
category: 应用与集成
order: 3
updated_at: 2026-08-05
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

YundaDesk 不申请 **Write** 或 **Read/Write** 权限。你不需要把 Consumer Key 或 Consumer Secret 粘贴到 YundaDesk 表单中，WooCommerce 凭据也不会保存在 WordPress options 中。

## 等待首次同步

首次同步按以下顺序读取店铺：

1. 店铺信息；
2. 客户；
3. 商品与变体；
4. 订单。

授权完成后，**设置 → YundaDesk** 会确认 WooCommerce 只读访问已经连接。回到 YundaDesk，打开**应用 → WordPress**，选择对应站点，并确认 WooCommerce 增强状态为**已连接**。后续同步只读取变化，不会每次重建整个店铺。事件通知只包含最小资源引用，YundaDesk 会再从 WooCommerce 读取当前数据。

WordPress 设置页只确认授权状态，不会逐资源显示同步进度。请使用合成测试数据验证每类受支持资源都能进入 YundaDesk，不要把授权成功本身当作所有资源已同步的证明。

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
