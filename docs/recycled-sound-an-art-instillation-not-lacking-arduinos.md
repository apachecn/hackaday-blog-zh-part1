# 循环声音——一个不缺少 arduino 的艺术装置

> 原文：<https://hackaday.com/2011/03/17/recycled-sound-an-art-instillation-not-lacking-arduinos/>

![](img/ad50d7415f33c09f8653ee4d36451100.png "01")

[oakkar7]来信向我们展示了[Ben Johansen]和[Jonathan Snow]的互动艺术装置，Recycled Sound(网站有病毒)。该展览将于 3 月 25 日下午 5-7 点在 [TWU 艺术三角徒步之旅](http://www.twu.edu/triangle/)中首映。

目前一项工作正在进行中，最终的计划是室外安装，以一个旋转顶部的中心平台和周围的各种岛屿为特色。随着讲台顶部的旋转，周围的岛屿随着各种各样的灯光和声音显示变得栩栩如生，这些灯光和声音显示随着讲台的旋转而变化。虽然电子产品没有被回收，但实际的雕塑和音乐制作元素本身是由废车场零件和工厂废料组成的。

整个显示运行了 12..是的，12 台带 Arduino 引导加载程序的 Atmel 328s！中央指挥台内有一个发射电路，由两个带 Arduino boot loaders 共享一个晶体的 atmega 328s、一个 hmc 6532 磁力计[分线板](http://www.sparkfun.com/products/7915)和*两个 RF 发射器组成。显然，每个岛都包含一个带有 Arduino 和 RF 接收器的接收模块。接收 Arduinos 连接到电机和照明的光隔离开关模块。查看[Ben]的[博客](http://www.benjohansen.com/archives/category/installation-art)中正在进行的快照、代码和构建信息。*

如果你想用你的 5V Arduino 控制一些 12V 电机/灯，一定要看看博客里的图片。虽然我们在 Hackaday 可能会很快进入焊接领域，但[Ben]会严格遵循适当的开发进度。每个方面都是面包板，然后提炼，然后转移到焊接性能板。

更新:他的网站有某种恶意软件。在 Firefox 中，我们没有人注意到它，但在投诉之后，我们启动了 ol IE。是的，那里很脏。如果你敢的话，可以点击下面的链接[去那里。](http://www.benjohansen.com/recycled-sound)

跳跃后的更多内容:

这里是所有硬件的一个镜头，没有微控制器:

![](img/5fcb1d9157f2cfec952a75785e1b7691.png "06")

他们还设计了在胶合板上安装电机的巧妙方法，用角铁固定电机，并用软管夹将其固定。马达要么摆动链条敲击回收的木琴键，要么用硬纸板轻弹调好的 PVC 管。

![](img/0f11b46b92d51781945e45a753ef7765.png "02")

![](img/7f5e2fb98ef28d96391d4387776ad0be.png "03")

每个噪声制造者(我们假设照明)都有一个开关电路:

![](img/03f334dc2d0f732a3b235b1e7466b8dd.png "04")

射频通信是使用 Sparkfun 的[射频链路发射器](http://www.sparkfun.com/products/8945)和[射频链路接收器](http://www.sparkfun.com/products/8948)(目前缺货)在 315 MHz 和 434 MHz 的口味。我们很想知道发射机将位于全金属底座的什么位置，因为它有可能充当一个巨大的射频笼。这些图片似乎表明，他们正在使用 1/2 波线天线，但正在将其缠绕成一个线圈。在许多令人头痛的射频模块之后，我们建议将线状天线切成两半(1/4 波长)，将它们拉直并偷偷放在旋转鼓外面，以获得更好的接收效果。

我们迫不及待地想看到最终的安装结果！