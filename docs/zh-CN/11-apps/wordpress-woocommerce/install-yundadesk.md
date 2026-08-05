---
title: 在 WordPress 安装 YundaDesk 插件
description: 安装一个 YundaDesk 插件，启用 WordPress 在线客服和可选的 WooCommerce 增强。
category: 应用与集成
order: 1
updated_at: 2026-08-05
---

# 在 WordPress 安装 YundaDesk 插件

YundaDesk 只使用一个 WordPress 插件。它可以为普通 WordPress 站点添加在线客服与 AI 客服；检测到 WooCommerce 后，再提供可选的只读店铺能力。你不需要安装第二个 WooCommerce 插件。

## 开始前

你需要：

- WordPress 6.2 或更高版本；
- PHP 7.4 或更高版本；
- 可以安装插件并管理站点设置的 WordPress 管理员；
- 仅在使用店铺增强时需要 WooCommerce 8.2 或更高版本。

未安装或停用 WooCommerce 时，WordPress 基础连接仍可正常使用。

## 目录正式发布后从 WordPress.org 安装

WordPress.org 正式发布插件后才能使用这个方式。在私有审核或受控测试阶段，请改用 YundaDesk 提供的 ZIP。

1. 在 WordPress 后台打开**插件 → 安装插件**。
2. 搜索 **YundaDesk**。
3. 确认插件名称为 **YundaDesk**，目录 slug 为 `yundadesk`。
4. 选择**立即安装**，然后选择**启用**。
5. 打开**设置 → YundaDesk**。

![在 WordPress 插件页面搜索并安装 YundaDesk](/help/assets/docs/wordpress/zh/install-plugin.jpg "安装 YundaDesk 插件")

## 安装 YundaDesk 提供的 ZIP

如果 YundaDesk 支持团队向你提供了安装 ZIP：

1. 打开**插件 → 安装插件**。
2. 选择**上传插件**。
3. 选择 YundaDesk ZIP，点击**立即安装**，然后启用插件。
4. 打开**设置 → YundaDesk**。

不要修改 ZIP 内的文件名，也不要为 WooCommerce 另装一个包。

## 启用插件时会发生什么

启用操作只在 WordPress 本地准备插件，不会连接站点、加载前台 Widget、读取 WooCommerce 数据或联系 YundaDesk。只有管理员明确点击**连接 YundaDesk**后，外部请求才会开始。

![尚未连接时的 YundaDesk 原生设置页](/help/assets/docs/wordpress/zh/settings-unconnected.jpg "YundaDesk 已安装但尚未连接")

在 WordPress 多站点环境中，请逐个启用并连接需要使用 YundaDesk 的子站。网络启用不会自动把所有子站绑定到同一个工作区。

## 下一步

继续阅读[将 WordPress 站点连接到 YundaDesk](./connect-yundadesk.md)。
