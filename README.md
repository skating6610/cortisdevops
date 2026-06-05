# cortisdevops

cortisdevops 是一套面向企业多云管理、DevOps 流水线与自动化运维场景的开源平台。项目目标是把资产管理、权限治理、任务编排、配置管理、通知告警和云原生运维能力整合到一个统一入口中，帮助团队降低平台建设与日常运维成本。

## 项目定位

cortisdevops 适合用于以下场景：

- 企业内部 DevOps 平台建设
- 多云资源与主机资产统一管理
- CMDB、业务树和资源拓扑维护
- 自动化作业、脚本执行与流程编排
- 应用发布、审批、审计和通知联动
- Kubernetes 多集群与云原生运维管理

## 核心能力

| 模块 | 说明 |
| --- | --- |
| 统一门户 | 通过前端基座与 API 网关整合多个运维模块，减少系统切换成本。 |
| 权限管理 | 支持用户、角色、菜单、接口、应用和业务维度的 RBAC 权限治理。 |
| CMDB | 管理业务树、云资产、主机、集群等资源数据，为自动化流程提供基础数据。 |
| 工作流 | 支持脚本执行、文件分发、接口编排、审批流、定时任务和 CI/CD 场景。 |
| 配置中心 | 集中维护业务配置与平台配置，便于统一管理和变更追踪。 |
| 通知中心 | 对接审批、任务结果、告警消息等通知场景，提高事件响应效率。 |
| 云原生管理 | 支持 Kubernetes、Helm、多集群和云原生资源管理。 |
| Agent 管控 | 支持跨网络通道、主机任务执行和节点管理。 |

## 技术栈

- 前端：Vue、iView、React、Ant Design
- 后端：Python Tornado、Golang Gin
- 网关：OpenResty、Lua
- 微前端：qiankun
- 中间件：MySQL、Redis、RabbitMQ
- 部署：Docker Compose、Kubernetes、Helm

## 系统架构

```text
用户 / 浏览器
   |
   v
前端基座 / 管理控制台
   |
   v
API 网关（OpenResty + Lua）
   |
   +-- admin             用户、权限、应用、业务管理
   +-- cmdb              资产、业务树、云资源管理
   +-- flow              任务调度、脚本执行、流程编排
   +-- config-center     配置中心
   +-- notice            通知中心
   +-- cnmp              Kubernetes / 云原生管理
   +-- agent-server      Agent 管控中心
   |
   v
MySQL / Redis / RabbitMQ / Kubernetes / 云厂商资源 / 主机 Agent
```

## 快速开始

> 当前项目支持 Docker Compose 与 Kubernetes Helm 部署，生产环境建议优先选择 Kubernetes Helm，并将数据库、Redis、RabbitMQ 等中间件纳入统一备份与监控。

- 在线文档：[docs.cortisdevops.cn](https://docs.cortisdevops.cn/)
- Docker Compose 部署：[docs/zh/guide-v2/2-install/docker.md](docs/zh/guide-v2/2-install/docker.md)
- Kubernetes Helm 部署：[docs/zh/guide-v2/2-install/k8s.md](docs/zh/guide-v2/2-install/k8s.md)
- 架构说明：[docs/zh/guide-v2/1-architectures/README.md](docs/zh/guide-v2/1-architectures/README.md)

## 本地文档开发

本仓库包含 VuePress 文档站点，可使用以下命令在本地预览或构建：

```bash
npm install
npm run dev
```

构建静态文档：

```bash
npm run build
```

> 注意：`npm run deploy` / `npm run depoly` 会执行发布脚本，日常修改文档时请谨慎使用。

## 模块仓库

项目采用模块化、微服务化设计，主要模块包括：

- 管理后台：admin
- 资产管理：cmdb
- 工作流：flow
- 配置中心：config-center
- 通知中心：notice
- 云原生管理：cnmp
- Agent 管控：agent-server
- API 网关：gateway
- 前端基座：home-index

## 贡献指南

欢迎以 Issue、Pull Request、文档补充、部署验证、问题反馈和最佳实践分享等方式参与项目建设。

贡献建议：

1. 提交变更前先说明问题背景和目标。
2. 保持提交内容聚焦，避免一次 PR 混合多个无关改动。
3. 文档、部署脚本和配置示例需要尽量提供可复现说明。
4. 涉及权限、执行任务、凭证、Agent、网关等能力的改动，需要额外关注安全边界。
5. 提交代码前尽量运行相关测试或构建检查。

## 贡献者

感谢所有参与过项目建设、问题反馈、部署验证和文档完善的社区成员。贡献者名单不再按个人排名展示，后续以 Git 提交记录、Issue、Pull Request 和发布说明作为主要贡献追踪方式。

## License

本项目基于 [GPL-3.0](LICENSE) 协议开源。
