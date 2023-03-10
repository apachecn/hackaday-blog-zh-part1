# 构建您自己的 USB 转串行加密狗

> 原文：<https://hackaday.com/2012/03/09/build-your-own-usb-to-serial-dongle/>

![](img/bb159369fda752c4ad2784187f5ca012.png "make-you're-own-USB-to-serial-tool")

[Johan von Konow]发现他在许多项目中使用 FTDI USB 转串行芯片，并希望手头有一个简单的原型制作组件来实现这一点。他想出的是上面看到的[极小的 USB 转串行转换器](http://vonkonow.com/wordpress/2012/03/usbserial-pcb/)。铜制的手指可以插入你的 USB 接口。如果你有一个未使用的拇指驱动器(我们有一个 128mb 的版本，已经尘封多年)，它将成为该设备的完美外壳。

他使用的是 LQFP-32 封装的 FT232BL 芯片。这是 0.8 毫米的间距，所以要确保你有一个稳定的手，一个良好的顶端的烙铁，并在一些焊接灯芯在手。0603 无源元件在焊接过程中也可能会让你跑一圈，但总的来说，我们认为只要稍加练习，每个人都能成功组装。芯片是最昂贵的部件，价格略低于 6 美元。但好消息是，董事会是片面的，只需要一个跨接线，使非常少的钻井和容易的家庭制造。

如果你要下零件订单，我们建议将电阻和电容加倍。很有可能你会丢掉一些，再也看不到它们了。我们还强烈建议查看[Gerrit 的] [表面贴装元件夹具](http://hackaday.com/2010/12/13/diy-clamp-helps-with-surface-mount-soldering/)。