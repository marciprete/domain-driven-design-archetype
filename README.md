domain-driven-design-archetype
====================
基于领域驱动设计六边形架构实现的 Maven 原型模版

### 构建方式

mvn archetype:generate \
    -DarchetypeGroupId=cn.moyada \
    -DarchetypeArtifactId=domain-driven-design-archetype \
    -DarchetypeVersion=1.0-SNAPSHOT

### 层次概述

#### bom
管理外部依赖

#### domain
领域模型层，负责维护实体、值对象、聚合、聚合根，以及资源获取的抽象接口。

#### service
领域服务层，用于支撑领域业务的生命周期，如实体的创建。

#### repository
数据资源层，负责提供获取数据资源的实现，如 mysql 的数据操作。

#### remote
远程资源层，负责提供获取协调资源的实现，如 dubbo 服务的调用。

#### infrastructure
基础设施层，提供业务无关的底层组件，如 util、io、mail、mq。

#### application
应用服务层，提供业务的访问入口，负责协调业务逻辑。

#### client
展现层，提供业务服务的外部访问方式。