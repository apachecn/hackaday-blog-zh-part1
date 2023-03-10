# 苹果 II 天气显示器(第三部分)

> 原文：<https://hackaday.com/2011/04/20/apple-ii-weather-display-part-3/>

![](img/df237896ee86d620381044289aca9b97.png "Exif JPEG")

在第 1 和第 2 部分中，我讨论了 lua 在 PC 端的重要部分。虽然不是 110%详细，但我希望它能让你了解数据是如何处理的，以便 Apple II 计算机可以快速消化它。现在是时候看看串行电缆的另一端会发生什么了。我用的是 basic，但它不是 100%的 rom Applesoft basic，那会更慢，所以我用的是编译器和快速图形驱动程序。这两个软件都来自“Beagle Compiler ”,它是由令人敬畏的 Beagle Bro 软件公司生产的，尽管仍然受版权保护，出版商已经允许使用他们的软件(在合理的范围内，我不认为你会把它卖得很远)。

Beagle 编译器不像其他编译器那样处理机器码，所以它有一点开销，但我选择它是因为它有一些有趣的插件，如 fast hplot(快速绘图)，input anything(默认情况下 basic 只接受字母数字输入)，以及 128K 或更多机器的内存驱动程序，所有我认为我可能需要的。最终版本不需要额外的输入，因为所有发送到计算机的数据都是字母数字，但我确实使用了快速 hplot，它使计算机绘制单个像素的速度翻倍，并且使用了一个内存管理器。

磁盘上有两个 COM 程序，都是编译好的基本脚本，一个是启动程序，一个是客户端程序。启动是 prodos 在启动磁盘时运行的第一个程序，它只执行一些基本的启动任务。

```

REM LOAD THE FAST GRAPHICS ROUTINE
11 PRINT CHR$(4)&quot;BLOAD FAST.HPLOT&quot;
REM YAP
12 HOME:VTAB 3
13 PRINT &quot; Please type in IN#n (where n = the ssc&quot;
14 PRINT &quot; slot number, then hold control hit A, &quot;
15 PRINT &quot; and type in 7B (600 baud) at the SSC&quot;
16 PRINT &quot; or ? prompt.&quot; :PRINT &quot;&quot;
17 PRINT &quot; (you may or may not need to press&quot;
18 PRINT &quot; return depending on model)&quot;:PRINT &quot;&quot;
19 PRINT &quot; Then type the following to run &quot;:PRINT &quot;&quot;
20 PRINT &quot; -CLIENT&quot;

```

如你所见，它加载速度很快。HPLOT 程序，它是一个二进制程序，所以我加载了它(二进制加载)，为了这样做，我们必须打印一个(ctrl +D)来告诉解释器这是一个 dos 命令，然后是我们想要的命令。

第 12 行清除了苹果当前的文本屏幕，并将提示放在屏幕的顶部，VTAB 3 只是将光标向下移动了 3 行。

然后我们有一些指令，这可以/应该能够自动完成，我记得小时候用我的 apple IIe 做过，但无论我在当前的//c 上做什么，我都无法通过脚本设置该死的串行端口。我想如果我真的让它工作了，它会很奇怪，没有其他苹果会自动设置串行端口，所以你必须手动设置。

接下来，也是更重要的是客户端程序

```

REM STARTUP 0-6
REM ENTER HIGH RES PAGE ONE AND TURN OFF THE 4 LINE TEXT DISPLAY
REM PAGE 2, NORMALLY FULL SCREEN, IS OCCUPIED AND I DONT FEEL
REM LIKE MESSING WITH MOVING STUFF AROUND IN MEMORY
0 HGR:POKE -16302,0
REM LOAD SPLASH SCREEN BINARY INTO HIGH RES PAGE 1 MEMORY
2 PRINT CHR$(4)&quot;BLOAD SPLASH.HGR,A$2000&quot;
REM DELAY
4 FOR I = 0 TO 30000
6 NEXT

REM MAKE A PALETTE 10-12
10 DIM CL(5): CL(1) = 0:CL(2) = 5
12 CL(3) = 2:CL(4) = 1:CL(5) = 6

REM CLEAR HIGH RES GRAPHICS PAGE 1 100-105
100 HGR:POKE -16302,0:HCOLOR = 7
102 FOR Y = 0 TO 138 STEP 2
104 HPLOT 0,Y TO 140,Y
105 NEXT

REM TEMP AND ALERT TEXT GRAPHICS INPUT DECODING 110-125
110 FOR Y = 0 TO 137
112 TB = 140:INPUT TS$
114 FOR X = 1 TO LEN(TS$)
REM CHARACTER --&gt; ASCII VALUE
116 TC$ = MID$(TS$,X,1):TA = ASC(TC$)
REM IF NEW CODE BLOCK
118 IF TC$ = &quot;b&quot; THEN TB = TB + 35
REM DRAW PIXEL
120 IF (TA &lt; 65) AND (TA &gt;= 49) THEN HPLOT((TA - 48) + TB), Y
122 IF (TA &gt;= 65) AND (TA &lt;= 90) THEN HPLOT((TA - 55) + TB),Y
124 NEXT X:NEXT Y

REM BOTTOM TEXT GRAPHICS INPUT DECODING 130-144
130 FOR Y = 139 TO 191
132 BB = 0:INPUT BS$
134 FOR X = 1 TO LEN(BS$)
REM CHARACTER --&gt; ASCII VALUE
136 BC$ = MID$(BS$,X,1):BA = ASC(BC$)
REM IF NEW CODE BLOCK
138 IF BC$ = &quot;b&quot; THEN BB = BB + 35
REM DRAW PIXEL
140 IF (BA &lt; 65) AND (BA &gt;= 49) THEN HPLOT((BA - 48) + BB), Y
142 IF (BA &gt;= 65) AND (BA &lt;= 90) THEN HPLOT((BA - 55) + BB),Y
144 NEXT X:NEXT Y

REM RADAR GRAPHICS INPUT DECODING 150-166
150 FOR C = 1 TO 5:HCOLOR = CL(C)
152 FOR Y = 0 TO 138 STEP 2
154 RB = 0:INPUT RS$
156 FOR X = 1 TO LEN(RS$)
REM CHARACTER --&gt; ASCII VALUE
158 RC$ = MID$(RS$,X,1):RA = ASC(RC$)
REM IF NEW CODE BLOCK
160 IF RC$ = &quot;b&quot; THEN RB = RB + 35
REM DRAW PIXEL
162 IF (RA &lt; 65) AND (RA &gt;= 49) THEN HPLOT((RA - 48) + RB), Y
164 IF (RA &gt;= 65) AND (RA &lt;= 90) THEN HPLOT((RA - 55) + RB),Y
166 NEXT X:NEXT Y:NEXT C

REM WAIT FOR UPDATE LOOP
200 INPUT UD$
210 IF UD$ = &quot;update&quot; THEN GOTO 100
220 GOTO 200

```

它有更多的肉。我从最上面开始(HGR:POKE -16302，0)。HGR 命令清除并将苹果发送到高 GRapichs 模式 1。模式 1 进入存储器第 1 页(80 列文本或高分辨率图形共有 2 页)，并将显示设置为 280×160，底部有 4 行文本。如前所述，我不想要四行文本，所以我戳 location -16302，0 来关闭它。

也许现在有人在对自己说“他为什么不用 HGR2？”HGR2(模式 2)默认为第二页，默认为全屏，但我不想使用它，因为 Apple II 上没有专用的视频内存，而且有东西已经在使用该内存空间，所以似乎更简单的是使用 screen 1 并将其设为全屏，而不是移动内存中的所有该死的东西来释放 HGR2。

接下来，我加载了 Hack A Day 和 Weather Underground 的图标。这张图片是在 gimp 中制作的，由我制作的一个旧的图像转换器脚本转换成 10 倍速度的模拟器。一旦图像被绘制在模拟器上，我[将它保存到磁盘上，现在在客户端脚本中，我只是将数据复制回视频内存来生成图像。basic 没有时间参考，所以只有一个空循环来延迟闪屏几秒钟。](http://en.wikipedia.org/wiki/BSAVE_%28graphics_image_format%29)

奇怪的是，对于一台在高分辨率图形中总共有 6 种独特颜色的机器来说，我需要做一个调色板。Apple II 上的颜色没有按照我想要的方式排列，我也没有按照准确的颜色顺序发送。DIM 是对一个数组进行尺寸标注，后面的值是我们想要使用的苹果颜色值，并且按照我们想要的顺序排列，对于一个循环来说很好很整洁。

脚本的其余部分只是根据下一个图像重复自己，首先是温度和风暴咨询图形，它的 2 个文件在 pc 端，但由于它们的宽度相同，并且在屏幕的同一个块中，我在它进入串行端口之前将它们集中在一起作为一个图像。变量与其他基于微软的 8 位 basic 类似，只有变量的前两个字符是它的名称，所以虽然你可以用漂亮的描述性词语命名一切，但你会很快遇到冲突。

我遍历图形的每一行，每次都等待来自串行端口的输入。使用 MID 函数(它的 like 子串)读取行中的每个字符，我还使用 ASC 函数获取每个字符的 ASCII 值。如果字符是“b ”,则当前闭塞计数器加 35(TB、BB 或 RB 表示温度、底部或雷达闭塞)。

如果字符的 ASCII 值小于 65，但至少是 49，那么它是一个 1-9 的数字，所以我们可以从表面上看，画出点，然后继续。如果字符的 ASCII 值在 65 到 90 之间，这意味着它是一个大写字母(这里是一个[图表](http://www.downloads.reactivemicro.com/Public/Apple%20II%20Items/Documentation/Books/Beagle%20Brothers%20-%20Colors%20and%20ASCII%20Values.png) btw)。我取 ascii 值并从中减去 55，65–55 = 10，A 是我的图形键中的第 10 个字符，ASCII 值为 65，依此类推。现在我可以画出重点了。

雷达是完全一样的东西，但它包裹在一个 5 计数循环中，在图像的一种颜色被绘制后改变颜色。它的 Y 计数器也前进了 2 步，因为我们只有偶数行，如果我没有“第 2 步”，图像将被压扁，现在它只是用黑色代替奇数行。

最后的想法:我从编写蹩脚的代码中获得了很多乐趣，尽管它运行起来非常慢。我希望我知道更多关于 Apple II 编程的知识，但是我在这上面花了这么多年，现在它只是作为一种爱好出现。也许很快有一天，我会笑着用 C 语言疯狂地编码来制作一个令人敬畏的视频游戏或演示，但这在我的列表中有点低。Apple II 是我最喜欢的小电脑之一，它将继续留在我的桌子上相当一段时间，如果你有办法并且喜欢复古电脑，Apple II 是丰富和令人惊讶的。

陷阱和问题:

我花了很长时间才确定一种图形格式，更糟糕的是，我编写并测试了其中的 5 种。RLE，二进制，高级 ascii，苹果上的 XPM 解码，最后是 36 进制。

我可能花了 3 个晚上试图通过基本脚本让愚蠢的串口工作，正如你所看到的，从来没有工作。

浪费了两个晚上，把各种疯狂的东西捅进苹果，试图踢开它的彩色杀手电路，只是发现这是我的电视调谐器应用程序在从图形转换到文本时没有从 NTSC 切换到 RS170(在文本模式下启用彩色突发信号，你看不到任何东西)

我的电脑死机了！是的，在开始时，我禁用了我的台式电脑，因为我妻子的机器突然断电了，我的机器也有一点点断电，因为我正坐在那里写东西(可能是图形代码)，然后电脑就关机了。长话短说，在一个工作日的晚上 11 点左右，我正在切换主板，我的 2.8ghz 双核处理器可以在不到 10 秒的时间内从室温升至 100C 以上！

我认为最后一次大失败是为了视频，除了 durn 猫撞了几次相机，我花了几个小时把所有东西都放到我的“厕所”上，并在客厅里设置好。在做了一些测试拍摄后，摆弄照明现在是晚上 10 点，我准备好了…除了我没有 Apple II 磁盘上的闪屏图形。幸运的是，我找不到我的 USB 驱动器(两个都在工作),那天下午，我刚刚把我的 WIFI 卡卖给了一个同事，因为我有一个内部卡正在路上。所以，是的，我把一个 8k 的文件刻录到一个 cd rom 上，匆匆忙忙地修补了基本脚本，把它发送过来并正常工作，然后在凌晨 2 点左右打扫完客厅。

哦，那很有趣。

[第二部分](http://hackaday.com/2011/04/19/apple-ii-weather-display-part-2/)和[第一部分](http://hackaday.com/2011/04/18/apple-ii-weather-display-part-1/)可以在这里找到。