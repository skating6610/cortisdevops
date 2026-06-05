
# cortisdevops

<p align="center">
    <a href="https://www.cortisdevops.cn/">
        <!-- <img width="200" src="https://www.cortisdevops.cn/images/head_logo.png"> -->
    </a>
</p>

[![Python3](https://img.shields.io/badge/Python-3.9-green.svg?style=plastic)](https://www.python.org/)
[![Golang](https://img.shields.io/badge/golang-1.23-brightgreen.svg?style=plastic)](https://golang.google.cn/)
[![Tornado](https://img.shields.io/badge/Tornado-6.0-brightgreen.svg?style=plastic)](https://www.tornadoweb.org)
[![Vue.js](https://img.shields.io/badge/Vuejs-2.5-brightgreen.svg?style=plastic)](https://cn.vuejs.org)
[![Ant-Design.js](https://img.shields.io/badge/Ant--Design-4.8-blue.svg?style=plastic)](https://ant-design.antgroup.com/)
[![Iview](https://img.shields.io/badge/iview-3.2.0-blue.svg?style=plastic)](https://www.iviewui.com/)
[![LICENSE](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE)
![star](https://img.shields.io/github/stars/cortisdevops-cn/cortisdevops.svg)
[![Video](https://img.shields.io/badge/Player-Video-red.svg?style=plastic)](https://www.bilibili.com/video/BV1rp4y1v7fa/)

## 架构总图

![架构总图](../../../images/S8Z-bGcARhN740JA.png)

----

### 项目概述

cortisdevops 是一款专为企业设计的开源全球一站式运维平台，支持多混合云环境和自动化运维，为企业提供跨地域、跨云的统一管理能力。

### 技术架构与优势

- **前端**：基于 Vue + iView 和 React + Ant Design 开发，提供直观友好的操作界面，显著提升用户体验和工作效率。
- **后端**：采用 Python Tornado 和 Golang Gin，具备轻量级、简洁清晰和异步非阻塞的特点，实现高并发和快速响应。
- **微服务网关**：基于 OpenResty + Lua，提供统一的 API 网关和服务治理能力，其优势在于高性能、灵活扩展和优秀的负载均衡支持。
- **微前端基座**：基于阿里乾坤框架，负责统一纳管前端应用，支持微前端架构，具备模块化管理、动态加载及高效集成的能力。

### 核心功能模块

1. **自动化运维**：支持任务调度、批量操作和流程编排，提升工作效率。
2. **实时观测与预警**：跨地域、跨云实时监控，保障稳定性。
3. **配置管理**：集中管理云资源配置，减少人为错误，提升合规性。
4. **云原生管理**：支持容器化与云原生技术，简化 Kubernetes 和微服务管理。
5. **日志与审计**：提供统一的日志存储、分析及审计能力，确保安全性与可追溯性。
6. **安全管理**：强化权限控制与访问管理。
7. **多云管理**：整合多云环境，实现资源优化与高效管理。

### 项目亮点

- **高效统一管理**：支持跨地域、跨云环境，简化多云资源运维。
- **可观测与智能化**：全面覆盖实时监控、预警与性能分析。
- **强大自动化能力**：一站式自动化工具提升运维效率，降低操作复杂性。
- **云原生支持**：优化容器化与微服务管理，为企业数字化转型赋能。

众多功能模块我们一直在不停的调研和开发，如果你对此项目感兴趣可以加入我们的社区QQ交流群：18252156

同时也希望你能给我们项目一个star，为贡献者加油⛽️！为运维干杯🍻！

## 模块介绍

```plaintext
cortisdevops
├── cortisdevops-admin               # 管理后台
├── cortisdevops-agent-server        # 底层管控
├── cortisdevops-cloud-agent-operator # 云原生任务执行
├── cortisdevops-cmdb                # 多云资源管理
├── cortisdevops-cnmp                # 云原生管理平台
├── cortisdevops-flow-servers        # 任务调度与流程管理
├── cortisdevops-monitor             # 可观测平台
├── cortisdevops-notice              # 通知中心
├── cortisdevops-frontend            # 前端流量入口
├── cortisdevops-gateway             # API网关
└── cortisdevops-kerrigan            # 配置中心
```

1. [**cortisdevops-admin**](https://github.com/cortisdevops-cn/cortisdevops-admin/blob/main/README.md)
   用于管理后台的操作平台，提供高效的管理界面和用户友好的操作体验。

2. [**cortisdevops-agent-server**](https://github.com/cortisdevops-cn/cortisdevops-agent-server/blob/main/README.md)
   底层管控模块，负责与主机或环境进行通信，实现资源的统一管理。

3. [**cortisdevops-cloud-agent-operator**](https://github.com/cortisdevops-cn/cortisdevops-agent-server/blob/main/README.md)
   负责执行云原生相关任务，支持 Kubernetes 等容器化任务的操作和调度。

4. [**cortisdevops-cmdb**](https://github.com/cortisdevops-cn/cortisdevops-cmdb/blob/main/README.md)
   数据资产管理平台，提供多云资源管理、CMDB 数据整合及资产统一视图。

5. [**cortisdevops-cnmp**](https://github.com/cortisdevops-cn/cortisdevops-cnmp/blob/main/README.md)
   云原生管理平台，专注于容器化、微服务及 Kubernetes 集群的管理。

6. [**cortisdevops-flow-servers**](https://github.com/cortisdevops-cn/cortisdevops-flow/blob/main/README.md)
   任务平台模块，支持任务调度、流程管理及批量作业执行。

7. [**cortisdevops-monitor**](https://github.com/cortisdevops-cn/cortisdevops-monitor/blob/main/README.md)
   可观测平台模块，提供实时监控、预警和性能分析能力，保障系统稳定性。

8. [**cortisdevops-notice**](https://github.com/cortisdevops-cn/cortisdevops-notice/blob/main/README.md)
   通知中心模块，支持多渠道通知推送，实现高效的事件响应。

9. [**cortisdevops-frontend**](https://github.com/cortisdevops-cn/cortisdevops-frontend/blob/main/README.md)
   前端应用和流量入口模块，处理 API 流量并路由至网关，支持模块化前端开发。

10. [**cortisdevops-gateway**](https://github.com/cortisdevops-cn/cortisdevops-gateway/blob/main/README.md)
    API 网关模块，负责统一流量入口和服务治理，提供高性能路由与认证支持。

11. [**cortisdevops-kerrigan**](https://github.com/cortisdevops-cn/kerrigan/blob/main/README.md)
    配置中心模块，用于集中管理配置项，实现动态配置更新和分布式配置下发。

## 使用指南
- [系统架构](./1-architectures/README.md)
- [安装说明](./2-install/README.md)
  - [docker安装说明](./2-install/docker.md)
  - [k8s安装说明](./2-install/k8s.md)
- [admin - 管理用户权限](./3-admin/README.md)
  - [使用admin配置权限](./3-admin/role-auth.md)
- [CMDB - 管理数据资源](./4-cmdb/README.md)
  - [使用CMDB管理云上数据资产](./4-cmdb/cloud-asset.md)
  - [使用CMDB管理业务树](./4-cmdb/biz-tree.md)
- [flow - 编排自动化工作流](./5-cortisdevops-flow/README.md)
  - [安装 cortisdevops-agent](./5-cortisdevops-flow/cortisdevops-agent.md)
  - [案例 - 使用 cortisdevops-flow 实现 golang 应用自动化CI/CD](./5-cortisdevops-flow/example-cicd.md)
  - [案例 - 使用 cortisdevops-flow + cmdb 实现 跨地区应用部署](./5-cortisdevops-flow/example-distribute-deploy.md)
  - [案例 - 使用 cortisdevops-flow + notice 实现 高效流程审批](./5-cortisdevops-flow/example-flow-audit.md)
- [配置中心 - 管理配置](./6-config-center/README.md)
- [通知中心 - 完成高效率告警](./7-notice/README.md)
- [云原生管理平台 - 管理多地集群](./8-cloud-native-management/README.md)
