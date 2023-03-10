# 超声波组合锁

> 原文：<https://hackaday.com/2011/12/14/ultrasonic-combo-lock/>

![](img/adcda6ed5ea89de9871b62d7f5b31dd7.png "ultrasonic-combo-lock")

[约翰·鲍克夏尔]对单输入密码锁采取了不同的路线。该单元使用 Ping [超声波测距仪输入四位数字代码](http://tronixstuff.wordpress.com/2011/12/13/project-ultrasonic-combination-switch/)。这是一次硬件升级，但使用了与[基于按钮的组合锁](http://hackaday.com/2011/07/14/building-a-single-button-combination-lock/)相同的基本概念。该设计使用 Arduino 来测量您按住单个按钮多长时间，输入之间有一秒钟的停顿，以输入代码。这一个也使用定时来建立每个数字被读取的时间，但是那个数字是作为你的手和传感器之间的距离被抓取的。

重新设计有我们喜欢和不喜欢的地方。这显然比其他基于按钮的锁贵得多，比如我们做的这个车库开门器。如果我们使用[John 的]设计，我们可能会选择 Ping 传感器(因为它是一个非常酷的输入)，并用一两个 LED 取代字符 LCD。我们在这里看到的另一个缺点是，有人可能很容易通过远程观察来窃取您的代码。尽管如此，我们喜欢这个项目，并认为你会在看到下面的演示剪辑。

[https://www.youtube.com/embed/gEh48itDV8E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gEh48itDV8E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)