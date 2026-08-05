---
title: WordPress 与 WooCommerce 数据和权限
description: 了解 YundaDesk 插件会发送什么、会读取哪些 WooCommerce 数据，以及绝不会修改什么。
category: 应用与集成
order: 4
updated_at: 2026-08-05
---

# WordPress 与 WooCommerce 数据和权限

YundaDesk 把 WordPress 站点连接与 WooCommerce 店铺访问分开。连接 WordPress 只会启用 Widget；只有店铺管理员批准只读权限后，WooCommerce 数据才会开启。

## WordPress 站点连接

管理员发起连接时，插件会发送站点地址、随机站点标识，以及当前 YundaDesk 插件、WordPress、PHP 和可选 WooCommerce 版本。连接完成后，受限状态检查只报告版本与可用性，用于判断集成是否健康。

只有完成连接后，前台才会加载 YundaDesk 托管的 Widget。访客主动通过 Widget 提交的消息和资料会作为客户支持数据处理。

## WooCommerce 只读数据

| 资源 | YundaDesk 使用的数据 | 重要边界 |
|---|---|---|
| 店铺 | 币种和非敏感店铺信息 | 不修改店铺设置 |
| 客户 | email、展示名、国家或地区 | 此集成不保留电话号码 |
| 商品与变体 | 商品名、SKU、价格、库存和变体信息 | 不修改商品或库存 |
| 订单 | 订单号、金额、币种、状态、商品项和允许的身份字段 | 不保留收货地址或电话 |
| 购物车 | 当前商品、SKU、数量、金额、币种和页面上下文 | 仅对已有 Widget 会话的访客发送；不含地址、email 或电话 |

YundaDesk 不修改订单、不执行退款、不修改客户，也不编辑商品。WooCommerce Core 没有权威的弃购记录，因此 YundaDesk 不会根据购物车活动伪造弃购。

## 同步与事件

首次读取会分页进行，后续读取使用变化标记，避免重复创建同一对象。WooCommerce 事件只通知 YundaDesk 某个受支持的客户、商品或订单发生变化，事件中使用最小标识而不是完整业务记录；YundaDesk 随后从店铺读取最新版本。

如果读取权限被撤销或过期，WooCommerce 区域会显示**需要重新授权**，并停止读取店铺数据，直到管理员再次批准只读权限。

## 外部服务

完成连接后，插件会使用以下 YundaDesk 服务：

- `app.yundadesk.com`：管理员登录与工作区确认；
- `api.yundadesk.com`：站点连接、状态、隐私请求与 WooCommerce 同步；
- `cdn.yundadesk.com`：公开 Widget loader。

请阅读 [YundaDesk 隐私政策](https://yundadesk.com/privacy/)与[服务条款](https://yundadesk.com/terms/)，并在向访客提供服务前，在自己站点的隐私政策中加入合适说明。

## 隐私责任

插件会提供隐私政策建议文本，并接入 WordPress 个人数据工具。这些工具可以帮助站点管理员处理请求，但安装插件不会自动使站点符合 GDPR、CCPA 或其他法律。你的组织仍需负责确认合法依据、提供通知、核实请求者、选择保留期限，并完成站点所需的响应。
