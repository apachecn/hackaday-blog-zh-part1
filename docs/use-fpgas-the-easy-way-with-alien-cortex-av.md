# 通过 Alien Cortex AV 轻松使用 FPGAs

> 原文：<https://hackaday.com/2011/06/23/use-fpgas-the-easy-way-with-alien-cortex-av/>

![alien_cortex_av_fpga_board](img/553bad0cddc7e080b2219e00cac34b5c.png "alien_cortex_av_fpga_board")

Hackaday 读者[Louis]来信提醒我们注意 Kickstarter 上的一个整洁的项目，他认为他的读者朋友会感兴趣。AlienCortex AV 是来自[Bryan Pape]的预建 FPGA 板,具有大量端口和巨大潜力。该板的核心是 Xilinx PQ208 Spartan 3e 500k FPGA，可以配置为执行任意数量的功能。正如您所料，该板配备了大量模拟和数字 I/O 引脚，以及 PS/2 输入、VGA 输出，甚至还有一对 Atari 兼容的操纵杆端口。

AlienCortex 软件包允许用户轻松地将项目加载到 FPGA 中，FPGA 可以同时运行多达四个不同的仿真微控制器。该软件自带六个预先配置的内核，其他内核在构建时可供下载。默认的内核集包括从 32 通道逻辑分析仪到四处理器 Arduino-sketch 兼容机器的一切。

现在，在你抱怨他在强大而昂贵的 FPGA 上模拟 Arduinos 的事实之前，没有什么可以阻止你创建一个由你碰巧更喜欢的微控制器组成的军队。我们猜测，如果你可以在这个板上同时运行四个 Arduinos，那么在你的下一个机器人项目中，可以同时模拟大量的图片以及你可能需要的任何其他 uC。一块主板同时集成几个不同的微控制器对我们来说听起来还不错。