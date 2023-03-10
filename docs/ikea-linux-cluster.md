# 宜家 Linux 集群

> 原文：<https://hackaday.com/2008/05/25/ikea-linux-cluster/>

构建一个渲染集群并不意味着你要花很多钱，即使你正在购买全新的硬件。[Janne]将这个 [6 单元组合](http://helmer.sfe.se/)放在一个 6 抽屉宜家 Helmer 橱柜内。他希望集群是低功耗、低成本的。在找到 6 个 65 纳米英特尔酷睿 2 CPUs 的好价格后，他找到了 6 块便宜的千兆主板。每块主板上的内存最大为 8GB。24 个 2.4GHz 内核消耗 400W，功耗和成本并不比高端 PC 高多少。每个主板都运行 Fedora 8，并安装了一个 NFS 共享。 [Dr Queue](http://drqueue.org/cwebsite/) 用于管理渲染农场的进程。[Janne]说以前需要通宵的工作现在只需要 10-12 分钟。预计容量为 186Gflops，但 12t flops 版本的计划已经在进行中。

他的网站还计划建造一个水下摄像机外壳，就像我们最近的文章《T2》中的那样。如果你想看到更多的宜家虐待，请查看[宜家黑客](http://ikeahacker.blogspot.com/)，即使它不是很专业。

[via [Hackzine](http://www.hackszine.com/blog/archive/2008/05/helmer_render_cluster_186_gflo.html?CMP=OTC-7G2N43923558)

更新:是的，[我们欺骗了自己](http://www.hackaday.com/2008/04/23/24-core-ikea-cluster/)

*   [永久链接](http://helmer.sfe.se/)