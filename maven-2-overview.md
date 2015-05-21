#<center>Maven - 概述
##Maven 是什么？
Maven 是一个项目管理和整合工具。Maven 为开发者提供了一套完整的构建生命周期框架。开发团队几乎不用花多少时间就能够自动完成工程的基础构建配置，因为 Maven 使用了一个标准的目录结构和一个默认的构建生命周期。

在有多个开发团队环境的情况下，Maven 能够在很短的时间内使得每项工作都按照标准进行。因为大部分的工程配置操作都非常简单并且可复用，在创建报告、检查、构建和测试自动配置时，Maven 可以让开发者的工作变得更简单。

Maven 能够帮助开发者完成以下工作：

* 构建
* 文档生成
* 报告
* 依赖
* SCM
* 发布
* 分发
* 邮件列表

总的来说，Maven 简化了工程的构建过程，并对其标准化。它无缝衔接了编译、发布、文档生成、团队合作和其他任务。Maven 提高了重用性，负责了大部分构建相关的任务。

##Maven 的历史
Maven 最初是在 Jakarta Turbine 项目中为了简化构建过程而设计的。项目中有几个子工程，每个工程包含稍有不同的 ANT 文件。JAR 文件使用 CVS 管理。

Apache 小组随后开发了 Maven，能够同时构建多个工程、发布工程信息、部署工程、在几个工程中共享 JAR 文件，并且协助团队合作。

##Maven 的目标
Maven 的主要目的是为开发者提供

* 一个可复用、可维护、更易理解的工程综合模型
* 与这个模型交互的插件或者工具

Maven 工程结构和内容被定义在一个 xml 文件中 － pom.xml，是 Project Object Model (POM) 的简称，此文件是整个 Maven 系统的基础组件。详细内容请参考 [**Maven - POM**](maven-4-pom.md) 部分。

##约定优于配置
Maven 使用约定而不是配置，意味着开发者不需要再自己创建构建过程。

开发者不需要再关心每一个配置细节。Maven 为工程提供了合理的默认行为。当创建 Maven 工程时，Maven 会创建默认的工程结构。开发者只需要合理的放置文件，而在 pom.xml 中不再需要定义任何配置。

举例说明，下面的表格展示了工程源码文件、资源文件的默认配置，和其他一些配置。假定 ${basedir} 表示工程目录：


配置项              | 默认值
------------------ | -------------
source code        | ${basedir}/src/main/java
resources	         | ${basedir}/src/main/resources
Tests              | ${basedir}/src/test
Complied byte code | ${basedir}/target
distributable JAR  | ${basedir}/target/classes

为了构建工程，Maven 为开发者提供了选项来配置生命周期目标和工程依赖（依赖于 Maven 的插件扩展功能和默认的约定）。大部分的工程管理和构建相关的任务是由 Maven 插件完成的。

开发人员不需要了解每个插件是如何工作的，就能够构建任何给定的 Maven 工程。详细内容请参考 [**Maven - 插件**](maven-8-plug-ins.md) 部分。