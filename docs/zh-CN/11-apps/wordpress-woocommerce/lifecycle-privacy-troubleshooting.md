---
title: 停用、解绑、卸载和使用隐私工具
description: 安全管理 YundaDesk 插件生命周期、WordPress 隐私请求、重新授权与常见故障。
category: 应用与集成
order: 5
updated_at: 2026-09-07
---

# 停用、解绑、卸载和使用隐私工具

停用、解绑和删除插件的效果不同。请根据你是要暂时暂停、迁移站点还是彻底移除集成，选择对应操作。

## 区分各项生命周期操作

| 操作 | WordPress Widget | WooCommerce 增强 | 本地连接信息 |
|---|---|---|---|
| 停用 YundaDesk | 停止加载 | 暂停同步与 YundaDesk 创建的事件 | 保留，便于恢复 |
| 解绑站点 | 停止加载 | 暂停并撤销 YundaDesk 连接 | 解绑完成后移除 |
| 删除插件 | 停止加载 | 删除插件拥有的事件配置 | 删除插件保存的连接设置与临时数据 |
| 仅停用 WooCommerce | 继续工作 | 暂停 | WordPress 连接保留 |

要解绑站点，请打开**设置 → YundaDesk**，选择解绑操作，并在收到成功确认后再删除插件。如果曾授权 WooCommerce，还需要打开**WooCommerce → 设置 → 高级 → REST API**，在解绑后删除 YundaDesk key。

解绑一个站点不会影响同一 YundaDesk 工作区中的其他 WordPress 站点。

YundaDesk 站点列表中的**前往 WordPress 断开**是前往站点后台的入口，并非平台直接解绑。断开尚未完成时，列表保留该站点并显示**正在断开**；请等待完成，长时间未完成时回到 WordPress 重试。断开完成后该站点退出日常列表，历史会话不删除。暂时不可达、停用或授权异常的当前站点仍会显示，不能把它们当作已断开。

全部站点断开完成后，应用卡恢复最初的官方安装入口，不再显示为已安装。入口可用时，**前往 WordPress 安装**直接在新标签页打开 WordPress.org 插件目录，不会打开连接说明弹窗。已有插件无需重装，也可以直接在目标 WordPress 后台的**设置 → YundaDesk**重新发起连接。

## 导出个人数据

1. 在 WordPress 后台打开**工具 → 导出个人数据**。
2. 输入已经核实身份的请求者 email。
3. 使用 WordPress 标准流程发送或确认请求。
4. WordPress 将请求标记为已确认后，生成导出文件。

YundaDesk exporter 只返回与当前连接站点相关的客服数据，不会包含同一客户在其他连接站点中独立产生的数据。

## 删除个人数据

1. 打开**工具 → 删除个人数据**。
2. 输入已经核实身份的请求者 email。
3. 完成 WordPress 标准确认流程。
4. 执行删除，并查看每个参与插件返回的结果。

YundaDesk eraser 只作用于当前站点连接。远程删除无法完成时会报告为未完成，管理员可以重试。站点管理员仍需核实请求者，并判断是否因法律义务需要保留部分数据。

![WordPress 个人数据导出与删除工具](/help/assets/docs/wordpress/zh/privacy-tools.jpg "为当前连接站点使用 WordPress 隐私工具")

## 将站点迁移到其他域名

WordPress 改用新的网站地址后，打开新地址的**设置 → YundaDesk**。如果仍显示**已连接**，先断开当前站点并等待成功提示，再选择**连接 YundaDesk**。在**确认站点地址变更**页面核对原地址、当前地址和聊天渠道，选择**确认更新并连接**，再点击**返回 WordPress**。原聊天渠道和历史会话会保留，不需要新建另一条渠道。

如果原连接已经断开，按[重新连接或恢复历史站点](./connect-yundadesk.md#重新连接或恢复历史站点)选择正确目标。不要只按相同地址判断归属，不要重复使用旧配对链接，也不要复制其他站点的连接设置。

完成后验证一条新的前台消息。如果使用 WooCommerce，请另外[重新授予只读访问](./enable-woocommerce.md#重新授权已有店铺)，并核对当前店铺的订单。

## 故障排查

### Widget 没有出现

- 在**设置 → YundaDesk**确认站点状态为**已连接**。
- 使用公开页面测试，不要在 WordPress 后台、登录页、Feed 或 REST 响应中测试。
- 连接后清除页面缓存与 CDN 缓存。
- 确认站点内容安全策略允许[数据和权限](./data-and-permissions.md)中列出的 YundaDesk API 与 Widget loader。

### 未检测到 WooCommerce

- 确认 WooCommerce 在同一个 WordPress 站点中处于启用状态。
- 将 WooCommerce 升级到 8.2 或更高版本。
- 重新加载**设置 → YundaDesk**。

### 显示需要重新授权

再次选择 WooCommerce 只读连接并批准 **Read**。不要自行创建 Consumer Key 或 Consumer Secret 后粘贴到 YundaDesk。

### 重新连接时列出了多个历史站点

核对工作区、原站点地址、渠道和上次连接时间，选择本次要恢复的网站。如果不确定，先联系工作区管理员；不要随意选择第一项或删除其他历史站点。

### WordPress 已连接，但订单仍无法读取

分别检查站点连接和 WooCommerce 授权状态。先在当前站点完成只读授权，再按[验证订单查询](./enable-woocommerce.md#验证订单查询)核对店铺、客户邮箱和订单。若页面提示暂时不可用，请稍后重试；持续失败时联系支持，不要发送店铺密钥。

### 同步或事件状态异常

打开**设置 → YundaDesk**刷新状态，并使用页面提供的恢复操作。如果问题持续存在，请在联系 [YundaDesk 支持](https://yundadesk.com/contact/)前记录站点地址、大致时间、YundaDesk 插件版本、WordPress 版本、WooCommerce 版本和页面显示的非敏感错误。不要在工单中发送密码、API key、客户地址或完整订单记录。
