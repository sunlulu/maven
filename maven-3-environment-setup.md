#<center>Maven 环境配置
Maven 是一个基于 Java 的工具，所以要做的第一件事情就是安装 JDK。

##系统要求

项目              | 要求
---------------- | -----------------------
JDK              | 1.5 or above.
Memory           | no minimum requirement.
Disk Space       | no minimum requirement.
Operating System | no minimum requirement.

##步骤1：检查 Java 安装
现在打开控制台，执行下面的 java 命令。

操作系统  | 任务                   | 命令
------- | ---------------------- | -------------------------------
Windows | 打开命令控制台           | c:\> java -version
Linux   | 打开命令终端             | $ java -version
Mac     | 打开终端                | machine:~ joseph$ java -version

我们来验证一下所有平台上的输出：

操作系统 | 输出
--------|---------------------------------------------------------
Windows | java version "1.6.0_21"<br/>Java(TM) SE Runtime Environment (build 1.6.0_21-b07)<br/>Java HotSpot(TM) Client VM (build 17.0-b17, mixed mode, sharing)
Linux   | java version "1.6.0_21"<br/>Java(TM) SE Runtime Environment (build 1.6.0_21-b07)<br/>Java HotSpot(TM) Client VM (build 17.0-b17, mixed mode, sharing)
Mac     | java version "1.6.0_21"<br/>Java(TM) SE Runtime Environment (build 1.6.0_21-b07)<br/>Java HotSpot(TM)64-Bit Server VM (build 17.0-b17, mixed mode, sharing)

如果你没有安装 Java，从以下网址安装 Java 软件开发套件（SDK）：[**http://www.oracle.com/technetwork/java/javase/downloads/index.html**](http://www.oracle.com/technetwork/java/javase/downloads/index.html)。我们假定你安装的 Java 版本为1.6.0_21。

##步骤2：设置 Java 环境
设置 JAVA_HOME 环境变量，并指向你机器上的 Java 安装目录。例如：

操作系统 | 输出
--------|---------------------------------------------------------
Windows | Set the environment variable JAVA_HOME to C:\Program Files\Java\jdk1.6.0_21
Linux   | export JAVA_HOME=/usr/local/java-current
Mac     | export JAVA_HOME=/Library/Java/Home

将 Java 编译器地址添加到系统路径中。

操作系统 | 输出
--------|---------------------------------------------------------
Windows | 将字符串“;C:\Program Files\Java\jdk1.6.0_21\bin”添加到系统变量“Path”的末尾
Linux   | export PATH=$PATH:$JAVA_HOME/bin/
Mac     | not required

使用上面提到的 **java -version** 命令验证 Java 安装。

##步骤3：下载 Maven 文件
从以下网址下载 Maven 2.2.1：[**http://maven.apache.org/download.html**](http://maven.apache.org/download.html)

操作系统  | 文档名称
--------|-------------------------------
Windows | apache-maven-2.0.11-bin.zip
Linux   | apache-maven-2.0.11-bin.tar.gz
Mac     | apache-maven-2.0.11-bin.tar.gz

##步骤4：解压 Maven 文件
解压文件到你想要的位置来安装 Maven 2.2.1，你会得到 apache-maven-2.2.1 子目录。

操作系统  | 位置 (根据你的安装位置而定)
--------|---------------------------------------------------------------
Windows | C:\Program Files\Apache Software Foundation\apache-maven-2.2.1
Linux   | /usr/local/apache-maven
Mac     | /usr/local/apache-maven

##步骤5：设置 Maven 环境变量
添加 M2_HOME、M2、MAVEN_OPTS 到环境变量中。

操作系统 | 输出
--------|-------------------------------------------------------
Windows | 使用系统属性设置环境变量。<br/>M2_HOME=C:\Program Files\Apache Software Foundation\apache-maven-2.2.1<br/>M2=%M2_HOME%\bin<br/>MAVEN_OPTS=-Xms256m -Xmx512m
Linux   | 打开命令终端设置环境变量。<br/>export M2_HOME=/usr/local/apache-maven/apache-maven-2.2.1<br/>export M2=$M2_HOME/bin<br/>export MAVEN_OPTS=-Xms256m -Xmx512m
Mac     | 打开命令终端设置环境变量。<br/>export M2_HOME=/usr/local/apache-maven/apache-maven-2.2.1<br/>export M2=$M2_HOME/bin<br/>export MAVEN_OPTS=-Xms256m -Xmx512m

##步骤6：添加 Maven bin 目录到系统路径中
现在添加 M2 变量到系统“Path”变量中

操作系统 | 输出
--------|-------------------------------------------------------
Windows | 添加字符串 “;%M2%” 到系统“Path”变量末尾
Linux   | export PATH=$M2:$PATH
Mac     | export PATH=$M2:$PATH

##步骤7：验证 Maven 安装
现在打开控制台，执行以下 mvn 命令。

操作系统 | 输出          | 命令
--------|--------------|----------------------------------------
Windows | 打开命令控制台 | c:\> mvn --version
Linux   | 打开命令终端   | $ mvn --version
Mac     | 打开终端      | machine:~ joseph$ mvn --version

最后，验证以上命令的输出，应该是像下面这样：

操作系统 | 输出
--------|-------------------------------------------------------
Windows | Apache Maven 2.2.1 (r801777; 2009-08-07 00:46:01+0530)<br/>Java version: 1.6.0_21<br/>Java home: C:\Program Files\Java\jdk1.6.0_21\jre
Linux   | Apache Maven 2.2.1 (r801777; 2009-08-07 00:46:01+0530)<br/>Java version: 1.6.0_21<br/>Java home: C:\Program Files\Java\jdk1.6.0_21\jre
Mac     | Apache Maven 2.2.1 (r801777; 2009-08-07 00:46:01+0530)<br/>Java version: 1.6.0_21<br/>Java home: C:\Program Files\Java\jdk1.6.0_21\jre

恭喜！你完成了所有的设置，开始使用 Apache Maven 吧。