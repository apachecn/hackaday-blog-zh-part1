# 蓝牙手环被黑

> 原文：<https://hackaday.com/2009/12/18/bluetooth-bracelet-hacked/>

![](img/f81b2a54fb76ee143ec084b9b90d3704.png "bluetooth-bracelet-hacked")

[Jeffery]黑掉了蓝牙标准，目的是为了[把这个手环当做定制显示器](http://ffejery.wordpress.com/2009/12/18/custom-alerts-on-a-bluetooth-enabled-bracelet/)。当我们在二月份第一次看到这个设备时，他接受了[的挑战，破解了这个设备](http://hackaday.com/2009/02/17/hackit-hackable-bluetooth-bracelet/)。

为了显示他自己的消息，他研究了如何在[蓝牙栈](http://www.bluez.org/)中实现 [HFP](http://en.wikipedia.org/wiki/Bluetooth_profile#Hands-Free_Profile_.28HFP.29) 。细节分享在他的[自述文件](http://adrestia.creativemisconfiguration.com/files/ffejery/misc/bracelet-hack/readme)中，但它是这样的:Bluez 包需要用一个非手机专用的虚拟后端编译，然后将允许发送的数据的外部操作。这提供了某种 Python 脚本可以操作的 API。他的概念验证允许使用您希望显示为命令行参数的消息来调用脚本。这应该足够简单，可以满足你的任何需求。不幸的是，以这种方式搞乱蓝牙包会使你的手机无法使用其他设备，但这是另一天的黑客。