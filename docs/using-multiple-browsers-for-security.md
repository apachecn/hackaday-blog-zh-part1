# 为安全起见使用多个浏览器

> 原文：<https://hackaday.com/2008/06/03/using-multiple-browsers-for-security/>

Securosis 的[Rich]带我们了解他的一些[浏览器偏执练习](http://securosis.com/2008/06/03/making-the-move-to-multiple-browsers/)。他对不同类型的网络活动使用不同的浏览器配置文件。基于潜在的风险，各种任务被分开，以保护从 [CSRF 攻击](http://en.wikipedia.org/wiki/Cross-site_request_forgery)和更多。日常浏览与低风险密码是在一个。没有密码的 RSS 阅读是在另一个网站上完成的。他在一个专用浏览器上运行他的个人博客。

For high risk research, he uses virtual machines to further minimize any potential nasty code getting through. Very high risk sites are browsed through a non-persistent read-only Linux virtual machine. While these techniques can be less effective if the entire OS is comprised, they can still provide a few layers of additional security.

患有浏览器妄想症的同胞们可能会考虑火狐插件，如 [NoScript](https://addons.mozilla.org/en-US/firefox/addon/722) 和来自[铁杆](http://diehard-software.org/)的内存保护。

*   [永久链接](http://securosis.com/2008/06/03/making-the-move-to-multiple-browsers/)