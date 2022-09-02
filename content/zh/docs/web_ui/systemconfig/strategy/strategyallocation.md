---
title: "策略分配"
weight: 2
description: 策略分配即为策略设置应用范围，在应用范围内策略才会生效。
---

策略分配即为策略设置应用范围，在应用范围内策略才会生效。

{{% alert title="说明" %}}
- 同一类型的策略在同一个应用范围中只能存在一条。
- 当在全局、域、域下的项目同时应用了不同的策略，在项目下，应用范围为该项目的策略生效。在域下其他项目，应用范围为该域的策略生效。在其他域下将应用全局范围的策略。
{{% /alert %}}

**入口**：在云管平台单击左上角![](../../../images/intro/nav.png)导航菜单，在弹出的左侧菜单栏中单击 **_"系统配置/UI策略/策略分配"_** 菜单项，进入策略分配页面。

![](../../../images/system/strategyallocation.png)

## 删除策略分配

该功能用于删除策略的应用范围，即取消策略的分配。

1. 在策略分配页面，单击策略右侧操作列 **_"删除"_** 按钮，弹出操作确认对话框。
2. 单击 **_"确定"_** 按钮，完成操作。

## 查看策略分配详情

该功能用于查看已设置应用范围的策略的详细信息。

1. 在策略分配页面，单击策略名称项，进入策略详情页面。
2. 查看策略的基本信息，包括云上ID、ID、名称、策略类型、策略定义、应用范围、创建时间、更新时间。

## 查看操作日志

该功能用于查看策略分配的操作日志。

1. 在策略分配页面，单击策略名称项，进入策略分配详情页面。
2. 单击“操作日志”页签，进入操作日志页面。
    - 加载更多日志：列表默认显示20条操作日志信息，如需查看更多操作日志，请单击 **_"加载更多"_** 按钮，获取更多日志信息。
    - 查看日志详情：单击操作日志右侧操作列 **_"查看"_** 按钮，查看日志的详情信息。支持复制详情内容。
    - 查看指定时间段的日志：如需查看某个时间段的操作日志，在列表右上方的开始日期和结束日期中设置具体的日期，查询指定时间段的日志信息。
    - 导出日志：目前仅支持导出本页显示的日志。单击右上角![](../../../images/system/download.png)图标，在弹出的导出数据对话框中，设置导出数据列，单击 **_"确定"_** 按钮，导出日志。