# 通过 ICMP 隧道传输 IP 流量

> 原文：<https://hackaday.com/2009/08/21/tunneling-ip-traffic-over-icmp/>

![icmptx](img/9e76aea2a9d099758f1b9919d24ada14.png "icmptx")

当我们在最喜欢的咖啡店、餐厅、机场或其他场所找到未加密的 WiFi 网络，却发现存在流量限制时，我们都很讨厌。大多数受限网络只允许 HTTP 和 HTTPS 流量，这是一个普遍的误解。在大多数情况下，ICMP 流量也被允许，允许用户 ping 网站和 IP 地址。你可能会问，“好吧，那这有什么关系？”你所有的 IP 流量都可以通过 ICMP 隧道，把你所有的网上冲浪伪装成简单的 ping 数据包。[Thomer]有一个关于如何使用 ICMPTX 创建和利用这样一个隧道的详细指南。所以，下次你在当地的咖啡馆，想在家里的电脑上打开 VLC 看电视节目的时候，快速阅读一下这个指南。