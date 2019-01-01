## 版本控制系统(VCS)

> 版本控制是一种记录一个或若干文件内容变化， 以便将来查阅特定版本修订情况的系统

### 人工版本控制

复制整个项目目录的方式来保存不同的版本，或许还会改名加上备份时间以示区别。 

优点: 简单，不需要任何工具

缺点: 容易犯错，版本多易乱

### 本地版本控制系统

在本地采用某种简单的数据库来记录文件的历次更新差异。

![本地版本控制系统](https://ws3.sinaimg.cn/large/006tNbRwgy1fyqwrs845cj30yk0u0myz.jpg)

其中比较出名的一个叫RCS，它的工作原理是在硬盘上保存补丁集(补丁是指文件修订前后的变化);通过应用所有的补丁，可以重新计算出各个版本的文件内容。

优点: 解决了人工版本控制容易犯错以及乱的问题

新的问题: 如何让在不同系统上的开发者协同工作。

### 集中式版本控制系统(CVCS)

![集中式版本控制系统](https://ws1.sinaimg.cn/large/006tNbRwgy1fyqx7hn0evj311i0tu76t.jpg)

比较出名的有CVS和Subversion(SVN)

优点：跨系统协作，权限管理

缺点: 单点故障: 机器宕机，无法提交; 磁盘损坏，会丢失项目的整个变更历 史，只剩下人们在各自机器上保留的单独快照。

### 分布式版本控制系统(DVCS)

![分布式版本控制系统](https://ws3.sinaimg.cn/large/006tNbRwgy1fyqxm0ecvaj30u00vgwhx.jpg)

比较出名的有Git。

特点: 客户端并不只提取最新版本的文件快照，而是把代码仓库完整地镜像下来。 这么一来，任何一处协同工作用的服务器发生故障， 事后都可以用任何一个镜像出来的本地仓库恢复。 因为每一次的克隆操作，实际上都是一次对代码仓库的完整备份。更进一步，许多这类系统都可以指定和若干不同的远端代码仓库进行交互。
