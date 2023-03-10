# 防御状态 16:起搏器-B-消失

> 原文：<https://hackaday.com/2008/08/09/defcon-16-pacemaker-b-gone/>

![](img/32d8f048b69e3aaf152e1d8e1dbd1ffc.png)

学术领域的各种医学研究人员的合作已经证明[心脏起搏器可以用简单易得的设备远程入侵](http://venturebeat.com/2008/08/08/defcon-excuse-me-while-i-turn-off-your-pacemaker/)。马萨诸塞大学阿默斯特分校的副教授凯文·傅(Kevin Fu)领导了这个团队。[Kevin]首先试图从制造商那里获得文档，相信他们会支持这项工作，但他们没有兴趣提供帮助。他们被迫接触一个旧的起搏器并对其进行逆向工程。他们发现用于远程编程设备的通信协议是未加密的。然后，他们使用一个 [GNU 无线电系统](http://www.hackaday.com/2007/08/11/cccamp-2007-gsm-a5-cracking/)来访问机器的一些可重编程功能，包括访问病人数据甚至关闭它。

虽然这只是用一个特定的起搏器完成的，但它证明了这个概念，生产这些设备的医疗公司应该认真对待。如果你对技术方面感兴趣，[看看该团队在五月份发布的论文，其中披露了这些方法](http://www.secure-medicine.org/icd-study/icd-study.pdf)。

*   [永久链接](http://venturebeat.com/2008/08/08/defcon-excuse-me-while-i-turn-off-your-pacemaker/)