**操作模式**

开始之前，有必要了解一下Storm的操作模式。有下面两种方式。

**本地模式**

在本地模式下，Storm拓扑结构运行在本地计算机的单一JVM进程上。这个模式用于开发、测试以及调试，因为这是观察所有组件如何在一起工作的最简单方法。在这种模式下，我们可以调整参数，观察我们的拓扑结构如何在不同的Storm配置环境下运行。要在本地模式下运行，我们要下载Storm开发依赖，用来开发并测试我们的拓扑结构。我们创建了第一个Storm工程以后，很快就会明白如何使用本地模式了。

**NOTE**: 在本地模式下，跟在集群环境运行很像。不过很有必要确认一下所有组件都是线程安全的，因为当把它们部署到远程模式时它们可能会运行在不同的JVM进程甚至不同的物理机上，这个时候它们之间没有直接的通讯或共享内存。

我们要在本地模式运行本章的所有例子。


**远程模式**


在远程模式下，我们向Storm集群提交topology（译者注：以后所有的topology不再翻译），它由许多通常运行在不同的机器上的流程组成。远程模式不会出现调试信息， 因此它也称作生产模式。不过在单一开发机上建立一个Storm集群是一个好主意，可以在部署到生产环境之前，用来确认topology在集群环境下没有任何问题。

你将在第六章学到更多关于远程模式的内容，并在附录B学到如何安装一个Storm集群。