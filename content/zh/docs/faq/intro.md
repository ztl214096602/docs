---
title: "快速入门"
linktitle: "快速入门"
weight: 1
date: 2019-08-29T18:50:55+08:00
description: >
 简单介绍var_oem_name产品以及用户可以获取的帮助文档。
---

## 本产品可以解决的问题？

- 云化企业私有基础设施
  - 虚拟化平台（KVM、VMware）云化管理
  - 物理资源的云化管理
  - 生产级Kubernetes运行环境（网络和存储方案）
  - 轻量级产品化私有云交付
- 统一多云环境
  - 统一裸机和虚拟机镜像
  - 统一API
  - 统一监控告警
  - 统一计费
- 解决企业跨云痛点
  - 便捷的跨云迁移
  - 跨云帐号体系安全
- 业务视角的资源管理
  - 基于项目的资源管理
  - 对接企业LDAP

## 产品架构及功能有哪些？

多云运维管理平台产品结构图如下所示：   
![](../image/架构图.png)

- 在{{<oem_name>}}主要解决提供以下主要功能：
    - VMware，KVM和裸机等计算资源的统一纳管(批量创建/删除/监控等) ；
    - KVM，VMware，Kubernetes等计算节点的自动部署扩容；
    - 基于扁平网络的自动化IP地址管理；
    - 跨平台的统一镜像支持；
    - 支持复杂调度策略，满足企业对计算资源分配的复杂需求；
    - 资源创建的自动化流程；
    - 支持实时监控宿主机与云资源的CPU、内存、存储使用率等；
    - 支持对虚拟机和裸金属的生命周期管理；
    - 账号体系与企业现有账号体系（LDAP）对接；

- 基于项目的多租户体系与工单自助服务；
  - 支持监控告警等。

## 云管平台能干什么？

{{<oem_name>}}管理平台是混合云环境中统一管理服务和资源的运维系统，全面纳管公有云，私有云，混合云资源。是您多云时代的最佳云计算合作伙伴。

- 云管平台支持实时监控基础设施中物理资源的使用情况以及公有云账户余额状态，当余额不足或资源不够时，云管平台将立即向管理源发送告警信息；
- 云管平台内置镜像市场功能，用户可快速导入可用镜像创建虚拟机；
- 云管平台支持对虚拟机生命管理操作；
- 云管平台以项目为单位进行租户隔离，不同项目的用户仅可以看到属于项目中的资源信息；
- 云管平台支持安全组、EIP、负载均衡等网络设置，仅需在UI界面上进行鼠标配置，无需复杂繁琐的步骤过程即可快速搭建灵活多样的网络场景；
- 云管平台支持部署在Kubernetes集群上，天然具有高可用，水平扩展的能力，灵活控制版本升级回滚等；
- 云管平台支持Kubernetes集群管理，支持基于Chart快速编排应用。

## 产品特色有哪些？

- 统一全面
  - 物理机/虚拟机/容器全面纳管
  - 统一API／镜像／控制台/监控
- 可扩展性架构
  - 基于Region和Zone的分层架构，能够在集群、机房、区域等层次平行扩容，支持万台以上宿主机规模；
  - 支持部署在Kubernetes集群之上，以pod的形式运行{{<oem_name>}}的组件，天然具有高可用，水平扩展的能力。
  - 平台支持KVM、VMware、OpenStack、Kubernetes等不同的资源类型统一管理；
- 便于部署运维
  - 支持物理机和宿主机节点自动部署，单台物理机部署时间小于30分钟，大大提升运维效率；
  - 支持基于扁平网络的IP管理；
  - 云管平台提供自服务portal，便于用户管理和使用虚拟机和裸金属资源；
  - 云管平台提供统一的系统监控和展示功能；
  - 提供统一的镜像支持，不同平台（公有云平台和私有云平台）、不同资源（物理机和虚拟机）可以共享同一个镜像，便于运维标准化；
  - 支持复杂的调度策略，满足企业对计算资源分配的复杂需求，单台虚拟机创建时间小于1分钟，500台虚拟机并发创建时间小于30分钟；
- 完善的安全设计
  - 虚拟机具备完整的物理资源。虚拟机之间、虚拟机和宿主机之间相互隔离，互不影响
  - 账户采用基于项目的多租户隔离体系，支持跟企业现有账号体系(LDAP/AD)对接，实现资源和运维管理的区分隔离；
  - 统一账户权限管理体系，降低跨云账户管理安全隐患；
- 开放
  - 所有功能都是基于API访问，便于协作，实现IT自动化；
  - 系统扩展性好，业务部门方便调用；

## 有哪些文档？用户应该看什么？

有如下文档：**安装部署**、**管理手册**、**快速使用**、**用户手册**、**常见问题**、**开发文档**

- 安装部署：主要介绍{{<oem_name>}}平台容器化部署的安装、系统初始化部署以及升级内容等。
- 管理手册：管理手册帮助管理员快速搭建{{<oem_name>}}环境，内容涵盖，KVM平台配置、私有云、公有云平台配置、镜像制作、服务配置、climc命令等内容。
- 快速使用：帮助普通用户快速使用{{<oem_name>}}平台虚拟机以及相关功能等。
- 用户手册：供管理员和普通用户使用，用户手册涵盖系统所有功能的使用步骤、注意事项以及参数说明等内容。
- 常见问题：摘选出用户在实际使用过程中的常见问题集锦，并给出解决方案。
- 开发文档：面向基于{{<oem_name>}}的生态对接与二次开发，主要从API层面带你认识{{<oem_name>}}产品，方便云计算配套产品与技术深入对接。

阅读建议如下：

- 对于普通用户：
  - 首先应该了解IaaS的概念，了解{{<oem_name>}}是什么，{{<oem_name>}}用途等。
  - 可参考安装部署手册，快速安装部署云管平台。
  - 安装成功后，安装管理手册中内容对接多云平台，纳管物理机和宿主机等。
  - 资源纳管完成后，即可使用普通用户按照快速使用内容使用{{<oem_name>}}平台。
  - 如需功能的详细说明，可参考用户手册。
- 对于开发者：
  - 可参考开发者手册了解API文档。
  - 开发者手册和climc命令行工具是必须的工具
- 对于老司机：
  - 快速阅读安装部署文档后，按照需求搭建自己的云管平台。
  - 在使用过程中，遇到问题都可以先参考常见问题。  
