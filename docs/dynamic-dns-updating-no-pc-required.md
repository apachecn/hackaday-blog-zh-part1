# 动态 DNS 更新–不需要电脑

> 原文：<https://hackaday.com/2011/04/12/dynamic-dns-updating-no-pc-required/>

![arduino_ddns](img/58b26520fd0122818c3aaa58d8849fb0.png "arduino_ddns")

Open Electronics 的[Boris]最近写信给我们分享他们的最新创作。像我们中的许多人一样，他使用 DynDNS 来保持他的家庭网络在 FQDN 伸手可及的地方。虽然 DynDNS 是一项非常方便的服务，但许多人不喜欢让他们的计算机一直开着以保持 IP 更新。这就是 Arduino DDNS 模块发挥作用的地方。

该模块使用安装了 Arduino bootloader 的标准 ATMega328 构建，定期检查用户的 IP 是否已更改，并根据需要更新 DynDNS 条目。Arduino 通过 WIZnet 以太网分线板与网络对话，通过一系列标准 HTTP 请求联系 DynDNS 的服务器来检查和更新用户的 IP。

我们知道一些路由器固件包，如 DD-WRT，内置了这种功能，但当这些资源不可用时，这个项目是一个很好的替代方案。

与往常一样，材料清单、PCB 布局和 Arduino 草图代码都可以从开放电子网站下载。