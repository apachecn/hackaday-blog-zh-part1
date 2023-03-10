# 考虑激光切割时的材料损失

> 原文：<https://hackaday.com/2011/07/12/accounting-for-material-loss-when-laser-cutting/>

当你切掉一些东西时，你会在这个过程中损失一些材料。想想台锯和它产生的锯屑，那是在锯片宽度范围内损失的废料。这很容易测量，只需测量刀刃。但是[詹姆士]开始思考[测量激光切割机材料损耗的好方法。](http://www.redtorope.com/2011/07/laser-cutter-kerf-measurement/)

为什么重要？如果你设计的零件应该相互吻合，材料的损失会导致连接不紧密。[James]发现可以通过在矩形框架内进行多次切割来测量损失。你可以在上面看到他的测试片，每一帧都剪下了十条。当激光完成它的工作后，只需将所有部件滑动到一起，测量一端产生的开口。让[有一个增强的卡尺](http://hackaday.com/2011/01/12/hold-fast-and-max-features-on-a-digital-caliper/)有助于使测量结果易于读取。现在将该距离除以激光通过的次数，并在下次为刀具设计零件时考虑该尺寸。