# 在不平坦的表面上轻松校准投影仪

> 原文：<https://hackaday.com/2012/02/29/projector-calibration-on-uneven-surfaces-made-easy/>

![projector-calibrator](img/06f4054886c0240ede13ab3ab002d8ac.png "projector-calibrator")

如果你想在家里建立自己的飞行/比赛模拟系统，你可能想看看这个。[Alex]来自巴西圣保罗的 Garoa Hackerspace，他组装了一个精巧的装置，使投影仪图像校准变得轻而易举。

在为这种模拟器构建环绕屏幕时，您可能会遇到图像重叠和弯曲投影失真的问题。有一些投影仪可以很容易地调整自己以适应这种设置，但它们通常非常昂贵，所以[Alex]认为他应该自己构建一个解决方案。

在研究了 2004 年由约翰尼·李中写的一篇论文后，他于去年为 T2 制造了一个原型显示器校准器，使用了相似的方法，尽管稍微做了些调整。这一次，[Alex]改进了他的校准器，使过程更加精确和快速。

光传感器和 Arduino 连接到投影介质的背面，投影仪对屏幕进行大范围扫描。然后，他的代码触发每个角的额外扫描，以更好地估计投影表面的精确边缘。由于视频是在软件中调整的，而不是依靠投影仪硬件来处理任务，因此结果既便宜又非常准确。

不过不要相信我们的话，看看下面的[Alex 的]视频演示，看看他的校准器在起作用。

[https://www.youtube.com/embed/CvOBGdnUEzw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CvOBGdnUEzw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)