# 更新:50MHz 到 100Mhz 范围转换

> 原文：<https://hackaday.com/2010/03/31/update-50mhz-to-100mhz-scope-conversion/>

将这台 50 兆赫的 Rigol 示波器换成更大、更贵的同类产品[变得简单多了。当](http://www.eevblog.com/2010/03/31/eevblog-70-turn-your-rigol-ds1052e-oscilloscope-into-a-100mhz-ds1102e/)[我们最初研究这个黑客](http://hackaday.com/2010/03/10/50mhz-to-100mhz-scope-conversion/)时，它需要从电路板上取下一些电容。现在只需通过串行终端连接发送三条命令。

休息之后，请观看视频演示。你会看到有一个芯片需要不同的设置来改变功能。移除电容实际上改变了上电时初始化芯片的命令。现在，您只需通过终端更改型号和序列号的一个字母，固件就会将其识别为更贵的 DS1102E。

[https://www.youtube.com/embed/LnhXfVYWYXE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LnhXfVYWYXE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[谢谢零功率]