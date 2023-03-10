# USB 控制的回流焊炉

> 原文：<https://hackaday.com/2012/02/01/a-usb-controlled-solder-reflow-oven/>

[![](img/604c38b903544887a63e42064d42a07c.png "HU-320 solder reflow oven controller")](http://hackaday.com/2012/02/01/a-usb-controlled-solder-reflow-oven/screenshot-at-2012-01-31-210116/)

[Helion Microsystems]的[Joel]用他的[USB 控制的回流焊炉](http://www.helionmicro.com/pages/hu320-example-pcb-reflow-oven-control)再次做到了这一点。你可能会从他疯狂的[推特伊沃克人](http://hackaday.com/2011/12/27/a-little-tweeting-ewok/)模型中想起他。虽然这两个项目非常不同，但他们都使用了 [HU-320 USB 转接板](http://www.pozible.com/index.php/archive/index/4416/description/0/0)，他正在通过【Pozible】或澳大利亚 Kickstarter 为美国佬筹集资金。

回流焊炉使用支持热电偶的 RS-232 电压表将温度输出到 HU-320 板。如果你想实现一个类似的项目，[Joel]很好地为我们提供了与许多万用表接口的 C#代码。温度由一个机械继电器控制，这看起来像是一个穷人的 PID 控制器。

可悲的是，福禄克米似乎没有列出，但你的工作场所可能希望他们的米无论如何回来！对于另一个[多士炉回流焊炉](http://hackaday.com/2011/11/15/solder-reflow-toaster-oven/)的实现，查看这篇【HAD】文章。请务必在休息后观看视频，观看设置视频！(热处理工程师可能会觉得“配方”格式很幽默)。

 [https://www.youtube.com/embed/syUO3RcDsQw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/syUO3RcDsQw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)