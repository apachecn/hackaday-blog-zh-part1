# 如何销毁文件系统

> 原文：<https://hackaday.com/2008/11/09/how-to-destroy-a-filesystem/>

![rmrf](img/163751f52acb5cb59f4c197f41010bc6.png "rmrf")

“G1”[执行你输入的每一个命令](http://hackaday.com/2008/11/09/android-executes-everything-you-type/ "Android executes everything you type  - Hack a Day")的错误自然衍生出“rm -rf /”的笑话。 [rm](http://en.wikipedia.org/wiki/Rm_(Unix) "rm (Unix) - Wikipedia, the free encyclopedia") 是删除文件的 Linux 命令。-r 和-f 标志将导致它递归地删除文件并忽略确认。以 root 用户身份执行时，它将清除整个文件系统。不会吗？[乔恩·霍勒]决定[测试一下这个命令对*nix 系统的破坏力到底有多大。之后，该系统的功能如何？他将它与 Windows 的对等物“format c:”和“del /F /S /Q”一起进行了测试。他想知道有哪些保护措施可用，哪些措施仍然有效。Linux 最终彻底崩溃，而 Windows，由于文件锁定，实际上干净地关闭了…并且再也没有回来。有些操作系统，](http://hohle.net/scrap_post.php?post=23&m=full)[如 Solaris](http://blogs.sun.com/jbeck/date/20041001#rm_rf_protection "Meddling in the Affairs of Wizards") ，拒绝运行命令‘RM-RF/’以防止意外。