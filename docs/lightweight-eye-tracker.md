# 轻型眼球跟踪器

> 原文：<https://hackaday.com/2006/01/13/lightweight-eye-tracker/>

![eyetrack](img/249f7fcbd79868bebbdb55d9cb44bbfe.png "eyetrack")

[Jason S. Babcock]和[Jeff B. Pelz]共同撰写了这篇关于[构建一个简单、轻量级眼球跟踪器](http://www.cis.rit.edu/people/faculty/pelz/publications/ETRA04_babcock_pelz.pdf) (PDF)的论文，以促进开源眼球跟踪软件的创建。所有的部件都安装在一副廉价的安全眼镜上。眼球跟踪器使用一种叫做“暗瞳”照明的技术。红外发光二极管用于照亮眼睛。瞳孔呈现为一个黑点，因为它不反射光线。一个亮点也出现在角膜上，在那里红外线被直接反射。一个眼睛摄像头安装在红外 LED 旁边，以记录这两个点的眼睛图像。软件跟踪两个点之间的差异，以确定眼睛的方向。安装在框架上的激光器有助于初始校准过程。放置在眼睛上方的场景摄像机记录下眼睛正在观看的内容。来自这两个摄像机的视频可以实时比较，也可以在实验结束后进行比较。

[谢谢奥斯汀 y.]

*   [永久链接](http://www.cis.rit.edu/people/faculty/pelz/publications/ETRA04_babcock_pelz.pdf)