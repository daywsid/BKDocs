# 新手必读

运维的职能通常包含 **应用发布** 、 **变更** 、 **故障处理** 以及 **日常需求处理**等 ，覆盖研发运营生命周期的 **持续集成** （CI）、 **持续部署** （CD）、 **持续运营** （CO）三个阶段，从研发代码构建到产物包交付再到测试环境部署，将验证通过的版本部署到生产环境，以及提供业务上线后的运维基础支撑和增强服务。

蓝鲸致力于打造研发运营一体化平台，在 6.0 对外之后，我们将蓝鲸产品拆分成了套餐模式，以便满足不同企业或用户的场景需求；7.0容器化版推出之后，部署方案仍然沿用套餐的模式进行可插拔式的组合，可以灵活选择部署需要的套餐。

## 一、基础套餐

持续部署场景（CD），主要覆盖应用发布变更、基础管控等运维自动化阶段，比如：
- 配置资源管理，如主机设备、业务模块、服务进程端口、自定义CI模型等
- 基础运维管控，如脚本执行、文件分发、定时任务等场景
- 细粒度的权限管控以及用户体系自主建设
- 任务调度编排和执行，如编排一个完整的应用自动发布流程，包括备份、版本更新、配置变更、服务上线等流程节点
- 流程服务管理，如发布变更、工单事件、问题管理等
- 自定义 SaaS 开发及公司内第三方系统联动对接

包含产品：蓝鲸 PaaS 平台、配置平台、作业平台、权限中心、用户管理、节点管理、标准运维、ITSM（流程服务管理）

## 二、监控日志套餐

持续运营场景（CO），主要覆盖监控&告警处理、日志检索分析，比如：
- 不同业务场景下的监控配置、告警通知、报表视图展示、分析定位及自定义的采集上报等
- 日志采集&检索查询、关键字的日志监控、日志提取等日志服务
- 故障自动处理，包括实时发现告警、预诊断分析、自动恢复故障

包含产品：监控平台、日志平台

Ps:`7.0之后，原故障自愈产品整体合并到监控平台，不再提供单独的产品部署。`

容器管理的运维进阶场景，主要覆盖基于原生 K8S 的容器编排，比如：

- 管理自建云原生及各个云服务商K8S集群
- 基于Helm管理业务应用
- 提供容器监控告警与容器日志采集与查询

包含产品：蓝鲸容器管理平台（BCS）

## 四、持续集成套餐

持续集成场景（CI），主要覆盖自动化代码构建-测试-发布工作流，比如：

- 工程编译
- 代码库托管
- 制品库
- 流水线

包含产品：蓝盾（bkci）

**需要说明的是，在7.0容器化部署版本中，监控日志套餐、持续集成套餐、容器管理套餐均是依赖基础套餐，同时，监控平台的容器监控功能强依赖容器管理套餐，所以建议的部署顺序是基础套餐-->容器管理套餐-->监控日志套餐或持续集成套餐。**

## 快速预览蓝鲸各产品功能

<table><tbody>
<tr><td width="15%">产品</td><td width="85%">功能简述</td></tr>
<tr><td width="15%"><a href="https://bk.tencent.com/docs/markdown/用户管理/产品白皮书/产品简介/README.md">用户管理</a></td><td width="85%">蓝鲸提供的企业组织架构、多用户目录等集中的用户管理解决方案</td></tr>
<tr><td width="15%"><a href="https://bk.tencent.com/docs/markdown/权限中心/产品白皮书/产品简介/README.md">权限中心</a></td><td width="85%">蓝鲸体系集中权限管理服务，细化到资源实例级别的访问权限控制</td></tr>
<tr><td width="15%"><a href="https://bk.tencent.com/docs/markdown/配置平台/产品白皮书/产品简介/Overview.md">配置平台</a></td><td width="85%">提供主机、进程、模型等各种运维场景的配置数据服务管理，是蓝鲸体系的基石</td></tr>
<tr><td width="15%"><a href="https://bk.tencent.com/docs/markdown/节点管理/产品白皮书/Introduce/Overview.md">节点管理</a></td><td width="85%">批量快速地部署蓝鲸 Agent，覆盖 Linux、Windows 操作系统</td></tr>
<tr><td width="15%"><a href="https://bk.tencent.com/docs/markdown/作业平台/产品白皮书/Introduction/What-is-Job.md">作业平台</a></td><td width="85%">提供批量脚本执行、文件分发、文件拉取、定时任务等基础操作的原子平台</td></tr>
<tr><td width="15%"><a href="https://bk.tencent.com/docs/markdown/标准运维/产品白皮书/产品简介/README.md">标准运维</a></td><td width="85%">可视化的图形界面流程编排、跨系统调度利器</td></tr>
<tr><td width="15%"><a href="https://bk.tencent.com/docs/markdown/监控平台/产品白皮书/intro/README.md">监控平台</a></td><td width="85%">提供丰富的数据采集能力、大规模的数据处理能力，致力于满足不同场景的监控需求</td></tr>
<tr><td width="15%"><a href="https://bk.tencent.com/docs/markdown/日志平台/产品白皮书/intro/README.md">日志平台</a></td><td width="85%">基于业界主流的全文检索引擎，提供多种场景化的采集、查询功能</td></tr>
<tr><td width="15%"><a href="https://bk.tencent.com/docs/markdown/流程服务/产品白皮书/产品简介/README.md">流程服务</a></td><td width="85%">灵活自定义设计流程模块，覆盖 IT 服务中的不同管理流程或应用场景</td></tr>
<tr><td width="15%"><a href="https://bk.tencent.com/docs/markdown/管控平台/产品白皮书/产品简介/README.md">管控平台</a></td><td width="85%">蓝鲸体系的底层管控系统，是蓝鲸所有其他服务的基础（GseAgent）</td></tr>
<tr><td width="15%"><a href="https://bk.tencent.com/docs/markdown/持续集成平台/产品白皮书/产品简介/README.md">bkci（蓝盾）</a></td><td width="85%">免费并开源的 CI 服务，助力自动化构建-测试-发布工作流，持续、快速、高质量地交付产品</td></tr>
<tr><td width="15%"><a href="https://bk.tencent.com/docs/markdown/容器管理平台/产品白皮书/Introduction/README.md">BCS（容器管理平台）</a></td><td width="85%">高度可扩展、灵活易用的容器管理服务平台，支持社区原生 Kubernetes 编排引擎</td></tr>
</tbody></table>
