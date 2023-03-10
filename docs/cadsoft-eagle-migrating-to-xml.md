# Cadsoft Eagle 迁移到 XML

> 原文：<https://hackaday.com/2010/10/14/cadsoft-eagle-migrating-to-xml/>

![](img/c80d6da39441a98d979ce0648385a318.png "eagle2")

[PT] [发布了 Cadsoft](http://www.element-14.com/community/message/15751#15751) 的一项激动人心的发展，即向基于 XML 的器件、原理图和电路板布局的迁移。这种开放标准的采用与像[PT]这样的人一直在推动的[开放硬件倡议](http://www.openhardwaresummit.org/)齐头并进。

Cadsoft Eagle 是我们的首选原理图和 PCB 软件。我们甚至有一个教程，指导你如何准备 PCB 制造文件。但包含器件库、原理图和电路板布局的文件一直是二进制文件。向 XML 的过渡意味着很多事情。它们将更容易编辑，对于使用版本控制系统如 SVN、CVS、Mercurial SCM、Git 等来跟踪变更也更友好。但是我们首先想到的是黑客的可及性。想想在 Python 这样的程序中 XML 解析是多么容易。随心所欲地编写脚本以任何想象得到的方式操作 XML 文件应该是轻而易举的事情。这并没有低估 Eagle 的价值，它扩展了可用性，远远超出了 Cadsoft 的任何一个工程师团队自己所能生产的。为此，我们说好极了。