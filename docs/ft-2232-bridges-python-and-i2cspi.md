# FT-2232 连接了 Python 和 I2C/SPI

> 原文：<https://hackaday.com/2011/11/14/ft-2232-bridges-python-and-i2cspi/>

![](img/7e7e2bbb91822fa038f4316532603ccc.png "ft-2232-i2c-spi")

你手头可能已经有了硬件，可以在你的电脑上用 Python 脚本轻松地将 I2C 和 SPI 设备连接起来。上面看到的板是 FT-2232 分线板。这些芯片通常用于通过 USB 来方便 JTAG 编程，但它们还有其他可能对您有用的功能。该芯片具有多协议同步串行引擎(MPSSE ),可以支持 I2C 和 SPI 协议，您只需知道如何在代码中激活它们。

[Craig]用他的 MPSSE Python 包装器使这变得简单。只需安装他的模块，你就可以导入所有你需要的命令。他演示了如何从 1 MB SPI 闪存芯片中读取数据。这可以用于更多的地方，包括调试总线盗版的外围设备，或者重新编程芯片以添加到您的项目中(我们正在考虑显示器的字体阵列和精灵，或者查找表)。

如果你没有意识到，这些 FTDI 芯片在很长一段时间内都是 USB 支持的首选。我们已经有了使用这个硬件进行[钻头撞击的指南。最近，更多内置 USB 硬件的芯片已经上市。它们非常有用，也很划算，尤其是有了像](http://hackaday.com/2009/09/22/introduction-to-ftdi-bitbang-mode/)[LUFA 项目](http://hackaday.com/2011/11/11/lufa-open-source-usb-stack-now-for-nxp-arm-processors/)这样的开源栈。