# shmoocon 2006:Wi-Fi 的教堂呈现:一个邪恶的杂种，一条彩虹和一只大丹狗！

> 原文：<https://hackaday.com/2006/01/29/shmoocon-2006-the-church-of-wi-fi-presents-an-evil-bastard-a-rainbow-and-a-great-dane/>

![shmoocon](img/6ed9477e02cfaf4dd0ceb73d31cf1e67.png)

无线教堂展示了他们最近的一些项目。第一个是 [coWPAtty](http://www.churchofwifi.org/default.asp?PageLink=Project_Display.asp?PID=86) ，一个暴力破解 WPA-PSK 的程序。为了加速这个过程，他们为预先散列的 WPA-PSK 创建了一个表。WPA-PSK 使用路由器的 SSID 作为种子，所以他们从 Wigle.net 的[抓取了前 1000 个 SSID，并使用 170，000 字的字典计算哈希。现在他们能够每秒检查 18，000 个键，而不是每秒 12 个键。](http://wigle.net/)

下一个项目是邪恶的混蛋，一个定制的 WRT 固件。它类似于[流氓中队](http://tinfoilhat.shmoo.com/rogue_squadron/)这是一种固件，旨在欺骗接入点，通过网络钓鱼收集用户信息。邪恶的混蛋甚至有更多的工具，如飞机和流网。它甚至有一个“Point 'n 0wn”界面，让你只需点击你想自动欺骗的目标。

CoWF 还负责 Windows 的 Kismet，这样你就不用安装 Cygwin 了。

*   [永久链接](http://www.churchofwifi.org/)