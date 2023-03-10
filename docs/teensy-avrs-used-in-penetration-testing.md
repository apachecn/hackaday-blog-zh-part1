# 渗透测试中使用的小型 AVR

> 原文：<https://hackaday.com/2011/06/28/teensy-avrs-used-in-penetration-testing/>

![netragard_penetration_testing_mouse](img/c0d310b922771c3d57333426a99d7151.png "netragard_penetration_testing_mouse")

虽然有些人知道你应该小心来历不明的 USB 驱动器，但同样的小心很少，如果曾经行使与 USB 外设。安全公司 [Netragard 最近在客户的设施上执行渗透测试时利用了这一点。当客户从测试中排除了许多常见攻击媒介的使用，包括社交网络、电话、社会工程和未经授权的物理访问时，Netragard 的团队知道他们必须发挥创造力。](http://www.theregister.co.uk/2011/06/27/mission_impossible_mouse_attack/)

他们购买了一个罗技 USB 鼠标，并将其拆开，以便添加他们聪明的有效载荷。Teensy uC 被编程为模拟键盘输入，一旦连接到计算机上，就可以通过鼠标的 USB 连接输入命令。利用 McAfee 防病毒套件中一个未记录的漏洞，他们能够在系统输入命令从藏在青少年身边的闪存盘安装恶意软件时逃避检测。

鼠标重新组装后，他们将其与一些营销材料一起重新包装，使其看起来像促销活动的一部分。他们购买了一份详细的员工名单，并挑选了一个简单的目标，让他们的恶意鼠标上路。三天之内，他们的恶意软件被加载到受害者的电脑上，他们的测试被认为是成功的。

[谢谢，亚伦]