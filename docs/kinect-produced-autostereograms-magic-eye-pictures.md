# Kinect 制作自动立体图(电眼图片)

> 原文：<https://hackaday.com/2011/04/01/kinect-produced-autostereograms-magic-eye-pictures/>

![](img/2ece3a3907ceaf97eee6878f51d57f08.png "kinect-produced-stereograms")

[Kyle McDonald]与[Golan Levin]在 Creative Inquiry 工作室合作，开发出了一个可以生成自动立体图的应用程序。这些照片看起来是三维的，这要归功于通过迫使你的眼睛以不同于正常情况的方式调整焦距和聚散度而产生的视觉错觉。这个程序叫做 ofxAutostereogram，它有几个例子。两者都出现在[凯尔的]视频中(插播在休息之后)，从鲨鱼的深度图像开始。这与纹理贴图相结合，然后通过软件包中的 openFrameworks 软件进行处理，以生成最终图像。

如果这就是它所做的一切，你可能会发现它相当不起眼…这些图像已经存在了一段时间，尽管它们从来没有这么容易在你的家用电脑上制作。但是第二个例子非常奇妙。您可以使用来自 Kinect 的深度图像作为起点。如上所示，有一个预览窗口，您可以在其中调整裁剪平面，以包含正确的深度。这也允许你预览你的姿势。一旦刚刚好，就拿起拨片，通过软件进行处理。

【维梅奥 http://vimeo.com/21666082 w = 470】

[感谢 AnarchyAngel via[Kinect Hacks](http://www.kinect-hacks.com/kinect-hacks/2011/03/30/create-your-own-magic-eye-images-your-kinect-using-ofxautostereogram)