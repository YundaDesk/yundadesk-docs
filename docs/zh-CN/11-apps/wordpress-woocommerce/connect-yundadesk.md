---
title: 将 WordPress 站点连接到 YundaDesk
description: 将 WordPress 安全绑定到一个工作区，显示 Widget，并验证真实消息闭环。
category: 应用与集成
order: 2
updated_at: 2026-08-05
---

# 将 WordPress 站点连接到 YundaDesk

连接后，当前 WordPress 站点会与一个 YundaDesk 工作区建立独立绑定。站点只会获得显示公开 Widget 所需的受限配置；在你另行批准 WooCommerce 只读授权之前，YundaDesk 无法读取店铺数据。

## 开始前

- 安装并启用 YundaDesk 插件。
- 使用可以管理站点设置的 WordPress 管理员账号。
- 确认服务器可以通过 HTTPS 访问 YundaDesk。
- 先确定由哪个 YundaDesk 工作区管理该站点。同一站点同一时间只能属于一个工作区。

## 连接站点

1. 在 WordPress 后台打开**设置 → YundaDesk**。
2. 选择**连接 YundaDesk**。
3. 登录 YundaDesk；没有账号时可以先注册。
4. 核对站点地址、WordPress 与插件版本、检测到的 WooCommerce 版本和当前工作区。
5. 确认连接。这个步骤不会授予 WooCommerce 权限。
6. YundaDesk 提示授权已准备完成后，点击**返回 WordPress**，回到同一个 WordPress 后台页面并完成安全连接。
7. 确认连接状态为**已连接**。

返回链接只允许回到发起连接的同源 WordPress 后台。如果页面提示请求已过期，请回到**设置 → YundaDesk**重新开始，不要重复使用旧链接。

## 验证前台 Widget

1. 使用无痕窗口打开一个公开页面。
2. 确认页面出现 YundaDesk 聊天入口。
3. 打开 Widget，发送一条唯一的测试消息。
4. 在 YundaDesk 工作台确认正确站点出现新的官网会话。
5. 从工作台回复，并确认访客在 Widget 中真实收到回复。

![WordPress 前台 Widget 收到真实回复](/help/assets/docs/wordpress/zh/storefront-widget.jpg "验证真实前台消息闭环")

插件只在公开渲染页面加载 Widget，不会注入 WordPress 后台、登录页、Feed 或 REST 请求。前台只会获得公开 Widget 标识，站点连接凭据和 WooCommerce 凭据不会出现在页面源码中。

## 连接多个站点

一个工作区可以管理多个 WordPress 站点。请在每个站点安装同一个插件并分别完成连接；每个站点都有独立的连接状态、Widget 配置、WooCommerce 状态和解绑生命周期。

## 下一步

如果站点已启用 WooCommerce，请继续阅读[启用 WooCommerce 只读增强](./enable-woocommerce.md)。
