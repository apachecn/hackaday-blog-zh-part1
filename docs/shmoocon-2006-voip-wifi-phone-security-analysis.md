# Shmoocon 2006: VoIP WiFi 电话安全分析

> 原文：<https://hackaday.com/2006/02/02/shmoocon-2006-voip-wifi-phone-security-analysis/>

![shmoocon](img/1fec66925413280789d4705df172a095.png)

Shawn Merdinger 介绍了他的个人研究项目，内容涉及 VoIP WiFi 手机的安全性。在最初的调查中，他采用了“一级”方法。这些攻击来自中低技能的黑客，黑客对设备的“第一眼”:寻找开放的端口，寻找开发者遗留的东西，以及误用功能。所有手机都有一个共同点，那就是它们很容易遭受 DOS 攻击。他谈到了几款特定手机的问题。许多人打开了端口 17185，这是 VxWorks 数据库调试端口。最受欢迎的是 Clipcomm CPW-100E，它提供[未经认证的访问调试帐户](http://seclists.org/lists/fulldisclosure/2006/Jan/0552.html)，让你阅读通话记录，甚至拨打电话，把它变成一个远程监听设备。你可以在[蓝箱播客#13](http://www.blueboxpodcast.com/2006/01/blue_box_podcas_2.html) 中听到肖恩谈论他的项目。蓝盒子里还有一份肖恩的[详细幻灯片](http://www.blueboxpodcast.com/files/shmoocon_preso_voip_wifi_phone_merdinger.pdf)。这是一份由 Shmoocon 发布的新的[手机安全威胁列表。](http://voipsa.org/pipermail/voipsec_voipsa.org/2006-January/001109.html)

*   [永久链接](http://www.blueboxpodcast.com/2006/01/blue_box_podcas_2.html)