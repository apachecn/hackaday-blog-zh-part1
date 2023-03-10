# 在评估机器人上搜索 ADK

> 原文：<https://hackaday.com/2011/08/31/google-adk-on-an-evalbot/>

![evalbot_google_adk](img/03d4e6261d995016f459448a3b7462ea.png "evalbot_google_adk")

在得知谷歌的 ADK 依赖于使用 Arduino 兼容板后，[Benjamin]对其他微控制器平台没有被邀请参加派对感到失望。他没有换阵营，而是自己让 ADK 和他的评估机器人一起工作。事实上，他的修改应该允许 ADK 与几乎任何 Stellaris 手臂套件一起工作。

黑客由两部分组成。第一点，也是最重要的一点，是他为 ADK 开发的 USB 主机驱动程序。该代码借用了德州仪器的一些内容，一旦他有机会稍微清理一下源代码，就会发布在 GitHub 上。为了让他的手机与 EvalBot 一起工作，他还调整了外部 USB 电源，以提供与其他 USB 连接的硬件正常工作所需的电流。

当使用谷歌的 ADK 时，有更多的选择总是好的，而且[Benjamin]的工作可能是任何 Stellaris 开发人员工具包的一个受欢迎的补充。

继续阅读，观看他的 EvalBot ADK 演示的快速视频。

[https://www.youtube.com/embed/WNTX-VOAEh0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WNTX-VOAEh0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)