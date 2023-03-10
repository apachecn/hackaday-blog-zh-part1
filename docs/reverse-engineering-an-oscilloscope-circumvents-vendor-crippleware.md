# 对示波器进行逆向工程可以规避供应商的限制

> 原文：<https://hackaday.com/2012/03/05/reverse-engineering-an-oscilloscope-circumvents-vendor-crippleware/>

匈牙利自主知识中心(H.A.C.K .)的工作人员表示，他们并不是那里资金最充足的组织，所以当他们发现他们能够负担得起将一台稍微用过的 UNI-T UT2025B 数字示波器带进商店时，他们非常兴奋。当他们开始修补它时，这个示波器暴露了一个主要的缺点——屏幕截图只能通过 USB 连接到 Windows 电脑上。

因为他们的房子里没有任何 Windows 盒子， [[András Veres-Szentkirályi]决定尝试逆向工程协议](http://techblog.vsza.hu/posts/Reverse_engineering_chinese_scope_with_USB.html)，这样他们就可以使用这个有用的功能。

他设置了一个 Windows 虚拟机，并在主机 Linux 机器上使用 Wireshark，[András]嗅探了通过示波器 USB 接口传递的数据。他能够识别发送到虚拟机的图像包，并使用一个小的 Python 脚本对其进行解码。最终的图像是单色的，看起来不太对，但这是一个开始。随着他进一步挖掘，安德拉什发现他忽略了图像中的一些颜色数据，经过一点摆弄，他得到了你在上面看到的清晰、多彩的图像。

原来，虽然示波器有一个单色 LCD，但它通过 USB 接口发送 16 位彩色图像 Windows 客户端在屏幕上显示图像之前会对图像进行降级。所以最终，他不仅能够让 scope 在任何能够运行 Python 的操作系统上工作，他还能够捕获比制造商预期的好得多的图像——如果我们这么说的话，这是一个非常好的黑客技术。

如果你有一台这样的示波器，并希望从硬件中获得一些更好的图像，请务必访问一下 H.A.C.K. wiki 以及该项目的 T2 github 库。