# 当有人侵犯她的私人空间时，她的裙子会亮起来——退后，书呆子们！

> 原文：<https://hackaday.com/2011/06/01/jeris-dress-lights-up-when-someone-invades-her-personal-space-step-back-nerds/>

![](img/91306a6110a5ca4a39c71f3fe6083265.png "jeri-builds-a-light-up-dress")

[Jeri]通过[制造这款 LED 增强型连衣裙](http://www.youtube.com/watch?v=RLFLwZ-JGaU)向极客时尚挑战。她选择为她 2011 年的 BarBot 之旅组装该项目，我们想不出更合适的设置来制作这样的服装。它使用一个运动传感器来触发隐藏在织物下的蓝光延迟模式。最棒的是 instamatic 相机。它看起来像一个时尚配件，但它实际上隐藏了所有的灯光电路。

在相机内部，PIR 传感器会等待，直到检测到运动，通过运算放大器向触发电路发送信号。74LS14 施密特触发器芯片与一些电阻电容定时器电路合作，为 led 构建延迟链。这样，在检测到运动后，led 以交错的模式打开和关闭，不需要微控制器，非常悦目。休息之后，请亲自观看模拟比赛。

[https://www.youtube.com/embed/RLFLwZ-JGaU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RLFLwZ-JGaU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)