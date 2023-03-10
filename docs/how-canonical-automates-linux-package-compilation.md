# Canonical 如何自动化 Linux 包编译

> 原文：<https://hackaday.com/2011/06/12/how-canonical-automates-linux-package-compilation/>

![pandaboard](img/96eb9f5160efcbb200aa88f412a81b27.png "pandaboard")

当需要将最流行的 Linux 发行版移植到一个完全不同的架构时，你会怎么做？Canonical 员工[David Mandalla]在他们的 ARM 开发团队工作，[最近与他的同事](http://thetanktheory.squarespace.com/this-8-bit-life/2011/6/10/ubuntu-linux-pandabuilder.html)[Dallas makers space 成员](http://dallasmakerspace.org/wiki/Main_Page)分享了这个问题的答案。

Canonical 需要一种方法来为 ARM 平台编译大约 20，000 多个包，但是他们不想交叉编译，这相当耗时。相反，他们选择构建一个本地解决方案来处理负载，同时确保所有的包都被安全地编译。为了解决这个巨大的任务，[David]和他的团队构建了一个 4U 服务器，同时运行 20 个完全独立的 ARM 开发平台。

该服务器由 21 个 PandaBoards 组成，这是一种小型 OMAP 开发板，采用双核 ARM cortex 处理器，几乎具有您可能要求的所有连接选项。一个板作为服务器头运行，跟踪其他 20 个模块。当有人请求服务器时间来构建一个包时，主板会检查未使用的服务器，触发一个继电器来重新启动它，然后服务器会自动重新映像。一旦原始、安全的环境准备就绪，它就被移交给请求它的客户。

如果你有兴趣了解更多关于构建过程的信息，[David]已经整理了一个包含更多细节的博客。

[谢谢利兰]