---
title: "NAT网关"
weight: 2
description: NAT网关能够为公有云VPC网络中虚拟机提供IP地址转换功能，使虚拟机可以访问外网或提供互联网服务。
---

NAT网关能够为公有云VPC网络中虚拟机提供IP地址转换功能，使虚拟机可以共享弹性公网IP访问Internet或使虚拟机提供互联网服务。

目前支持管理阿里云和华为云平台的NAT网关，只读同步AWS的NAT网关。

NAT网关提供SNAT（Source Network Address Translation，源网络地址转换）、DNAT（Destination Network Address Translation，目的网络地址转换）等功能。

- SNAT：SNAT适用于VPC中的虚拟机访问互联网。即VPC中的多个虚拟机共享同一公网IP主动访问互联网。

- DNAT：DNAT适用于从互联网访问VPC中的虚拟机。即将NAT网关上的公网IP映射给虚拟机使用。

**入口**：在云管平台单击左上角![](../../../images/intro/nav.png)导航菜单，在弹出的左侧菜单栏中单击 **_"网络/网络服务/NAT网关"_** 菜单项，进入NAT网关页面。

  ![](../../../images/network/nat1.png)

## 新建NAT网关

该功能用于新建NAT网关，目前支持创建阿里云和华为云的NAT网关。

1. 在NAT网关页面，单击列表上方 **_"新建"_** 按钮，进入新建NAT网关页面。
2. 配置以下参数：
    - 域：在管理后台视图下新建NAT网关时，需要设置文件系统的所属域。
    - 名称：NAT网关的名称。
    - 计费方式：包括按量计费和包年包月。
        - 按量付费：按NAT网关的实际使用率收费，此模式适用于需求量会瞬间大幅度增大的场景，价格对比包年包月要贵。阿里云按量付费的NAT网关按小时收费，华为云按量付费的NAT网关按天收费，不足一天的按一天计算，反复创建NAT网关将重复收费。
        - 包年包月：是一种预付费的模式，提前一次性支付一个月、一年乃至多年的费用，该模式适用于设备需求比较平稳的场景，价格相对按量付费更便宜。选择包年包月后还需要设置购买时长。
    - 到期释放：设置新建的NAT网关的使用时长，超过设置时间后的NAT网关将会被删除。仅按量付费的NAT网关支持到期释放。
    - 区域：设置NAT网关所在的区域和可用区。
    - 套餐：选择NAT网关的规格。
        - 阿里云：按量付费支持按使用量计费、小型、中型、大型。包年包月支持小型、中型、大型。
        - 华为云：按量付费和包年包月都只支持小型、中型、大型、超大型。
    - 网络：选择VPC和IP子网。
    - 弹性公网IP（阿里云）：选择要绑定到NAT网关的弹性公网IP，默认暂不需要，当选择“新建弹性公网IP”时，需要配置以下参数。
        - 网络计费方式：设置弹性公网IP的计费方式，包括按量计费和按带宽计费。
            - 按流量计费：按实际传输流量收费，可限制峰值带宽避免意外流量带来的费用，当瞬间带宽超过该值时将丢包，适用于网络波动大的场合。
            - 按带宽计费：按传输速率计费，选择固定带宽，超过带宽时将丢包，适用于网络波动较小的场景。
        - 带宽：设置带宽的大小。
3. 单击 **_"确定"_** 按钮，完成操作。

## 同步状态

该功能用于获取NAT网关的当前状态。

**单个同步状态**

1. 在NAT网关页面，单击NAT网关右侧操作列 **_"同步状态"_** 按钮，同步NAT网关状态。

**批量同步状态**

1. 在NAT网关列表列表中选择一个或多个NAT网关，单击列表上方 **_"同步状态"_** 按钮，批量同步状态。 

## 到期释放

到期释放即设置NAT网关的使用时长，当超过设置期限时，NAT网关将会被自动删除。

1. 在NAT网关页面，单击NAT网关右侧操作列 **_"更多"_** 按钮，选择下拉菜单 **_"到期释放"_** 菜单项，弹出到期释放对话框。
2. 选择是否勾选到期释放，勾选后设置释放时间，单击 **_"确定"_** 按钮。
    - 单击释放时间输入框，显示日历等内容，支持直接在释放时间输入框中输入日期和时间，格式为yyyy-mm-dd hh:mm:ss，单击 **_"确定"_** 按钮。 
    - 在日历框中选择日期，单击 **_选择时间_** 按钮，将跳转到设置时间界面，选择时间后，单击 **_"确定"_** 按钮。
    - 支持快速选择“1小时”、“2小时”、“3小时”、 “6小时”、 “1天”、“2天”、 “1周”按钮，释放时间将设置为对应时间范围内的时间，单击 **_"确定"_** 按钮。
3. 设置完成后，在计费方式列显示NAT网关还有多久时间释放等信息。
4. 若不再需要到期释放功能，可在释放之前，在弹出的到期释放对话框中取消勾选到期释放，单击 **_"确定"_** 按钮。

## 续费

该功能用于为包年包月的NAT网关进行续费操作。

1. 在NAT网关页面，单击NAT网关右侧操作列 **_"更多"_** 按钮，选择下拉菜单 **_"续费"_** 菜单项，弹出续费对话框。
2. 选择续费时长，单击 **_"确定"_** 按钮，完成续费操作。

## 自动续费设置

该功能用于为包年包月的NAT网关进行自动续费操作。

{{% alert title="说明" %}}
阿里云平台按周购买的虚拟机续费周期是一周，按月购买的虚拟机续费周期是一个月，按年购买的虚拟机续费周期是一年；其他平台续费周期均为一个月。后续虚拟机在每次到期之前都会自动续费。
{{% /alert %}}

1. 在NAT网关页面，单击NAT网关右侧操作列 **_"更多"_** 按钮，选择下拉菜单 **_"自动续费设置"_** 菜单项，弹出自动续费设置对话框。
2. 自动续费：勾选自动续费，单击 **_"确定"_** 按钮，设置自动续费。
3. 取消自动续费：取消勾选自动续费，单击 **_"确定"_** 按钮，取消自动续费。

## 设置删除保护

该功能用于设置NAT网关的删除保护。当NAT网关启用删除保护后，NAT网关无法被删除；当NAT网关禁用删除保护后，NAT网关才可以被删除。

**单个NAT网关设置删除保护**

1. 禁用删除保护：
    - 单击NAT网关名称右侧带有![](../../images/computing/delprotect1.png)图标时，单击NAT网关右侧操作列 **_"更多"_** 按钮，选择下拉菜单 **_"设置删除保护"_** 菜单项，弹出设置删除保护对话框。
    - 选择"禁用"删除保护，单击 **_"确定"_** 按钮。
2. 启用删除保护：
    - 当NAT网关名称右侧不带![](../../images/computing/delprotect1.png)图标时，单击NAT网关右侧操作列 **_"更多"_** 按钮，选择下拉菜单 **_"设置删除保护"_** 菜单项，弹出设置删除保护对话框。
    - 选择"启用"删除保护，单击 **_"确定"_** 按钮。

**批量设置删除保护**

1. 禁用删除保护：
    - 在NAT网关列表中勾选一个或多个NAT网关，单击列表上方 **_"批量操作"_** 按钮，选择下拉菜单 **_"设置删除保护"_** 菜单项，弹出设置删除保护对话框。
    - 选择"禁用"删除保护，单击 **_"确定"_** 按钮，批量为NAT网关禁用删除保护。
2. 启用删除保护：
    - 在NAT网关列表中勾选一个或多个NAT网关，单击列表上方 **_"批量操作"_** 按钮，选择下拉菜单 **_"设置删除保护"_** 菜单项，弹出设置删除保护对话框。
    - 选择"启用"删除保护，单击 **_"确定"_** 按钮，批量为NAT网关启用删除保护。

## 删除

该功能用于删除NAT网关，当NAT网关名称项右侧有![](../../images/computing/delprotect1.png)图标，表示NAT网关启用了删除保护，无法删除NAT网关，如需删除NAT网关，需要先禁用删除保护。

**单个删除**

1. 在NAT网关页面，单击NAT网关右侧操作列 **_"更多"_** 按钮，选择下拉菜单 **_"删除"_** 菜单项，弹出操作确认对话框。
2. 单击 **_"确定"_** 按钮，完成操作。

**批量删除**

1. 在NAT网关列表中选择一个或多个NAT网关，单击列表上方 **_"删除"_** 按钮，弹出操作确认对话框。
2. 单击 **_"确定"_** 按钮，完成操作。

## 查看NAT网关详情

1. 单击NAT网关名称项，进入NAT网关详情页面。
2. 查看以下信息：
    - 基本信息：包括云上ID、ID、名称、状态、域、项目、共享范围、平台、计费方式、区域、可用区、云账号、云订阅、创建时间、更新时间、备注。
    - 配置信息：包括VPC、IP子网、内网IP地址、规格。
    - 其他信息：支持开启或关闭删除保护。

{{% alert title="说明" %}}
NAT网关的共享范围与VPC保持一致，即，当VPC更改共享范围时，NAT网关的共享范围也会改变。
{{% /alert %}}

## SNAT管理

该功能基于已有NAT网关的情况下，通过创建SNAT条目使VPC中IP子网的虚拟机可以通过NAT网关绑定的弹性公网IP访问公网。一条IP子网对应一条SNAT条目，如有多个IP子网需要访问公网，需要创建多个SNAT条目。

### 新建SNAT条目

该功能用于创建SNAT条目，使VPC内的IP子网下虚拟机或虚拟机可以通过NAT网关绑定的弹性公网IP访问公网。

1. 在NAT网关列表，单击NAT网关名称项，进入NAT网关详情页面。
2. 单击SNAT页签，进入SNAT页面。
3. 单击列表上方 **_"新建"_** 按钮，弹出创建SNAT条目对话框。
4. 配置以下信息：
    - 名称：设置SNAT条目的名称。
    - 类型：包括IP子网和虚拟机。
        - 当类型选择“IP子网”时，需要选择具体的IP子网，该IP子网下的虚拟机可以访问公网。
        - 当类型选择“虚拟机”时，需要选择具体的虚拟机，则只有该虚拟机可以访问公网。
    - 公网IP地址：选择永磊提供互联网访问的弹性公网IP。
5. 单击 **_"确定"_** 按钮，创建SNAT条目。

{{% alert title="说明" %}}
用于创建DNAT条目的公网IP不能再用来创建SNAT条目。
{{% /alert %}}

### 删除SNAT条目

该功能用于删除SNAT条目。

**单个删除**

1. 在NAT网关列表，单击NAT网关名称项，进入NAT网关详情页面。
2. 单击SNAT页签，进入SNAT页面。
2. 单击SNAT条目右侧操作列 **_"删除"_** 按钮，弹出操作确认对话框。
3. 单击 **_"确定"_** 按钮，完成操作。

**批量删除**

1. 在NAT网关列表，单击NAT网关名称项，进入NAT网关详情页面。
2. 单击SNAT页签，进入SNAT页面。
3. 在SNAT条目列表中选择一个或多个SNAT条目，单击列表上方 **_"删除"_** 按钮，弹出操作确认对话框。
4. 单击 **_"确定"_** 按钮，完成操作。

## DNAT管理

该功能基于已有NAT网关的情况下，通过创建DNAT条目使VPC内的虚拟机可以向外提供互联网访问服务。一个虚拟机绑定一条DNAT条目，如有多个虚拟机需要为互联网提供服务，则需要创建多条DNAT条目。

### 新建DNAT条目

1. 在NAT网关列表，单击NAT网关名称项，进入NAT网关详情页面。
2. 单击DNAT页签，进入DNAT页面。
3. 单击列表上方 **_"新建"_** 按钮，弹出创建DNAT条目对话框。
4. 设置以下参数：
    - 条目名称：DNAT条目名称。
    - 公网IP地址：选择未被绑定的弹性公网IP。
{{% alert title="说明" %}}
用于创建SNAT条目的公网IP不能再用来创建DNAT条目。
{{% /alert %}}
    - 虚拟机：选择提供互联网服务的虚拟机。
    - 公网端口：进行端口转发的外部端口。
    - 私网端口：进行端口转发的内部端口
    - 协议类型：转发端口的协议类型。
5. 单击 **_"确定"_** 按钮，创建DNAT条目。

### 删除DNAT条目


该功能用于删除DNAT条目。

**单个删除**

1. 在NAT网关列表，单击NAT网关名称项，进入NAT网关详情页面。
2. 单击DNAT页签，进入DNAT页面。
2. 单击DNAT条目右侧操作列 **_"删除"_** 按钮，弹出操作确认对话框。
3. 单击 **_"确定"_** 按钮，完成操作。

**批量删除**

1. 在NAT网关列表，单击NAT网关名称项，进入NAT网关详情页面。
2. 单击DNAT页签，进入DNAT页面。
3. 在DNAT条目列表中选择一个或多个DNAT条目，单击列表上方 **_"删除"_** 按钮，弹出操作确认对话框。
4. 单击 **_"确定"_** 按钮，完成操作。

## 查看操作日志

该功能用于查看NAT网关相关操作的日志信息

1. 在NAT网关列表，单击NAT网关名称项，进入NAT网关详情页面。
2. 单击“操作日志”页签，进入操作日志页面。
    - 加载更多日志：列表默认显示20条操作日志信息，如需查看更多操作日志，请单击 **_"加载更多"_** 按钮，获取更多日志信息。
    - 查看日志详情：单击操作日志右侧操作列 **_"查看"_** 按钮，查看日志的详情信息。支持复制详情内容。
    - 查看时间段的日志：如需查看某个时间段的操作日志，在列表右上方的开始日期和结束日期中设置具体的日期，查询时间段的日志信息。
    - 导出日志：目前仅支持导出本页显示的日志。单击右上角![](../../../images/system/download.png)图标，在弹出的导出数据对话框中，设置导出数据列，单击 **_"确定"_** 按钮，导出日志。