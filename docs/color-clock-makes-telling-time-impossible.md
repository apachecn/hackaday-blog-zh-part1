# 彩色时钟让看时间变得不可能

> 原文：<https://hackaday.com/2010/06/07/color-clock-makes-telling-time-impossible/>

![](img/da99b7a861c10a9387752cb5fa7924ef.png "hopeless-binary-clock")

[Bogdan] set out to build the all-too-familiar binary clock. But, he didn’t want to be ordinary, and set the goal of making the clock as hard to read as possible. [What he ended up with is a clock](http://www.electrobob.com/combi-clock/) that is almost impossible to read correctly.He’s using colors to tell the time. We immediately thought this might make use of [resistor codes as the display](http://hackaday.com/2010/01/15/know-your-resistors-tell-the-time/) but it doesn’t. Red shows the hours, green for minutes, and blue for seconds. Now stack all of them on top of each other in binary and you’ve got the time. That means you’ve got to know all of your color combinations, plus read the binary value correctly, to decipher the time. Add to that the display changing every second and we’re in trouble.Aside from the user difficulty level, this is a really clean build. It uses an ATmega8535 in conjunction with our favorite DS3232 RTC chip. The etched board is nice and clean, making for an aesthetically pleasing clock.