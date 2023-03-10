# Python 3000 正式发布

> 原文：<https://hackaday.com/2008/12/03/python-3000-release-imminent/>

![python3k](img/39fcc29ec00f1e6c58090cba7fb48ae5.png "python3k")

[Python 3000](http://python.org/ "Python Programming Language -- Official Website") 已经[正式发布](http://python.org/download/releases/3.0/)。最后一个 bug， [Issue2306](http://bugs.python.org/issue2306 "Update What's new in 3.0 - Python tracker") ，“更新 3.0 新功能”已经关闭。Python 3000，py3k，Python 3.0，是社区的一个主要版本。杰里米·希尔顿最早提到野兽的时间是 2000 年 1 月。这个新版本是在 2006 年 4 月发布的 PEP 3000 的基础上发展而来的。

Py3k 打破了与以前版本的向后兼容性，以减少功能重复并促进一种显而易见的完成工作的方式。第一个主要变化是`print`现在是一个内置函数，而不是一个语句。`int`和`long`已经统一，整数除法现在返回浮点数。Py3k 使用“文本”和“数据”的概念，而不是“Unicode 字符串”和“8 位字符串”。你可以阅读[中的许多变化，Python 3.0 中的新特性](http://docs.python.org/dev/3.0/whatsnew/3.0.html "What’s New In Python 3.0 — Python v3.0c3 documentation")。一些新特性已经被移植到 Python 2.6，因此您可以开始在当前代码中实现它们，以简化过渡。2.6 也有`-3`命令行开关来警告你正在被删除或改变的特性。最后，工具 2to3 是一个源代码到源代码的翻译器，它应该可以自动完成许多更改。

新版本的文档已经上线。[源码包](http://www.python.org/ftp/python/3.0/ "Index of /ftp/python/3.0")和二进制文件现在可用。

[via [johl](http://twitter.com/johl/status/1037010773 "http:...")