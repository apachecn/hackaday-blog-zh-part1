# Apple II 天气显示(第一部分)

> 原文：<https://hackaday.com/2011/04/18/apple-ii-weather-display-part-1/>

![](img/59bb0e5fd8503a53b6d8001298186a79.png "HADWEATHER")

由于电脑问题，我不得不从我的“电子”电脑上抢走一些部件，这并不坏，因为我当时没有做任何事情，我感觉到一个软件项目很痒。我还想用我电脑桌上的苹果//c 做点什么，于是这个用 25 年的旧电脑来显示天气的野蛮“解决方案”就出现了。

简而言之，有 Apple II，一根串行电缆，一台运行 linux mint 10 的 PC 和一些命令行实用程序。我的具体苹果是//c 的第一个版本，这意味着它有一个错误的 rom 和串行端口可能是麻烦的，我能得到的最好速度是 600 波特，只有基本的，虽然其他型号可能会更快一点。

在 linux 端，wget 从 [Weather Underground 的移动网站](http://m.wund.com/)下载 html 和雷达图像，这不是一个完美的来源，但很容易。一个 lua 脚本将文本和图形组合成字符串模式，Apple II 可以将其作为键盘输入进行处理，并通过串行电缆将其发送到 basic 中的屏幕上。

是的，它相当慢…通常需要大约 8 到 12 分钟来重绘屏幕，考虑到正在发生的事情，这并不是那么可怕(在我看来)，但任何对此更认真的人都可以找到许多方法来优化它，我只是想看看它会是什么样子。

休息之后，请加入我们，观看一段简短的视频，并阅读有关这一切如何运作的所有细节！

[https://www.youtube.com/embed/35rJoMLGz1U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/35rJoMLGz1U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

你需要的东西:

*带有串行端口的 nix PC 以及带有以下软件的设备

[GNU Wget](http://www.gnu.org/software/wget/)

[GNU 核心实用程序](http://www.gnu.org/software/coreutils/)

(两者可能都已经安装了)

[Lua 5.1](http://www.lua.org/) (我用 sudo apt-get 安装 Lua 5.1)

[ImageMagick](http://www.imagemagick.org/script/index.php) (再次 sudo apt-get install imagemagick)

Lynx (我只是用它来剥离 html 标签，并不想使用任何“合适的”东西)

Sjinn ，这是一个漂亮的小命令行程序，可以让你处理串口，而不必手动设置和在终端重定向 i/o。

[和我的项目文件夹](http://cheesefactory.us/filecenter/hadimg/Apple_II_Weather.zip)。【T2

在 Apple II 方面，您需要 128k IIe 或更高版本、磁盘驱动器/控制器、串行卡、空白磁盘和高分辨率图形。对于软件，你需要 [ADT Pro](http://adtpro.sourceforge.net/) ，还有我做的磁盘镜像。ADT Pro 是目前开发的 Apple Disk Transfer 实用程序，允许您将磁盘映像复制到 Apple II 或从 Apple II 复制，磁盘映像包含在上面的 zip 文件中。

将磁盘映像转移到苹果电脑，并在驱动器中重新启动该磁盘，一旦屏幕出现在白盒中，您就可以在 PC 上自由运行“lua a2weather.lua”。lua 脚本获取数据，通过管道传输到 Apple，然后使用 gnu sleep()命令休眠 45 分钟。

既然 lua 正在做所有的提升工作，我想这是一个很好的起点。此外，让我们把这种方式，以防你错过了它，我不是一个程序员，很像我的写作，准备好看到一些巨大的罪恶！

首先是主要的 a2weather.lua 脚本(我发现 wordpress 会谋杀我的格式化)

```

-- Weather Underground to Apple //
-- 2011 Kevin Dady
--
-- main script:
-- read data off of the http://www.wunderground.com/ mobile site
-- phrase it
-- process text &amp; graphics
-- send
-- sleep
-- loop
--
-- This software is provided 'as-is', without any express or implied
-- warranty.  In no event will the authors be held liable for any damages
-- arising from the use of this software.
--
-- Permission is granted to anyone to use this software for any purpose,
-- including commercial applications, and to alter it and redistribute it
-- freely, subject to the following restrictions:
--
-- 1\. The origin of this software must not be misrepresented; you must not
--    claim that you wrote the original software. If you use this software
--    in a product, an acknowledgment in the product documentation would be
--    appreciated but is not required.
-- 2\. Altered source versions must be plainly marked as such, and must not be
--    misrepresented as being the original software.
-- 3\. This notice may not be removed or altered from any source distribution.
require(&quot;req/web&quot;)
require(&quot;req/text&quot;)
require(&quot;req/radar&quot;)
require(&quot;req/os_commands&quot;)

graphicsKey = &quot;123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ&quot;

cmd.serialPort = &quot;/dev/ttyS0&quot;
cmd.webURL = &quot;http://m.wund.com/US/FL/Orlando.html&quot;
--cmd.webURL = &quot;http://m.wund.com/cgi-bin/findweather/getForecast?brand=mobile&amp;query=West+Yellowstone%2C+MT&quot;

while true do
 web.get()
 web.sortTXT()
 web.cleanTXT()

 text.createIMG()
 text.convertIMG()
 text.sortIMG()
 text.packageIMG()
 text.sendIMG()

 radar.convertIMG()
 radar.sortIMG()
 radar.packageIMG()
 radar.send()

 -- clean up data
 radar.data.input  = {}
 radar.data.packed = {}
 radar.data.apl2 = {{},{},{},{},{},{}}
 text.data.input  = {}
 text.data.packed = {{},{},{},{}}
 text.data.apl2   = {{},{},{}}

 cmd.sleep(&quot;45m&quot;)
 -- after sleep do tell the apple and do it again
 cmd.sjinn(&quot;update&quot;)
end

```

…非常简单，一些注释，zlib 许可证，啊，必需的文件！这些只是其他 lua 脚本中的函数和变量，虽然没有理由所有这些函数不能在这个脚本中，我只是觉得它更容易处理。

web.lua 从 weather underground 下载 html 和雷达图像，通过 lynx 剥离 HTML 标签，搜索关键字，并将这些关键字打包到一个表中(lua 中的表就像数组，但是您可以在其中放入几乎任何您想要的东西，甚至是函数)

text.lua 获取 web.lua 中收集的文本数据，并将其传递给 ImageMagick，以制作简单的文本图像，然后将这些图像转换为数据字符串，并将这些数据传输到 Apple。

radar.lua 使用 ImageMagick 抖动雷达图像，对该文件进行短语化，构建数据字符串，并将该图像数据传输到 Apple。

os_commands.lua 包含运行 wget、lynx 等命令行程序的函数。

图形键需要保持不变，稍后我会详细说明这是如何工作的，但每个字符代表屏幕 35 像素列中的一个数值，Apple // high res graphics 中有 280 个水平像素。它是从 [base36，](http://en.wikipedia.org/wiki/Base_36)缺少零值，你不把数字加起来，每个都是它自己的。

还有一个字符串用来定义你的串口，还有一个字符串用来放置你想看的区域的 url，进入 [Weather Underground 的移动网站](http://m.wund.com/)搜索 anywhere(我不知道它在北美以外的地方效果如何),然后复制/粘贴得到的页面 url。

接下来是一个无限 while 循环和包含在上述脚本中的各种函数。然后，我定义了一堆空表(这只是我再次保证表是新的，我没有出错)。

接下来是 web.lua

```

-- Weather Underground to Apple //
-- 2011 Kevin Dady
--
-- Web Processing:
-- get text data
-- get radar image
-- phrase text for apple //

web = {}

web.data = {}
web.keywords =
{
&quot;National Weather Service:&quot;,
&quot;Updated&quot;,&quot;Windchill&quot;,&quot;Temperature&quot;,&quot;Humidity&quot;,
&quot;Conditions&quot;,&quot;Dew Point&quot;,&quot;animated radar image&quot;}

web.get = function()
-- download html from website
cmd.wget(cmd.webURL, &quot;text.html&quot;)
-- look for the radar image url
local file = io.open(&quot;temp/text.html&quot;)
local image = &quot;&quot;
for line in file:lines() do
if string.find(line, &quot;jpg&quot;) then
image = line
break
end
end
file:close()
-- remove the html tags from image url
local firstQuote = string.find(image, &quot;\&quot;&quot;) + 1
local secondQuote = string.find(image, &quot;\&quot;&quot;, firstQuote) - 1
image = string.sub(image, firstQuote, secondQuote)
-- download image
cmd.wget(image, &quot;radar.jpg&quot;)
end

web.sortTXT = function()
local fileLines = {}
-- use lynx to strip html tags
cmd.lynx(&quot;temp/text.html&quot;)
-- dump the lynx output file into a table
local file = io.open(&quot;temp/text.txt&quot;)
for line in file:lines() do
table.insert(fileLines, line)
end
-- look for keywords and scrape data
for y = 1, #fileLines do
local sub = &quot;&quot;
-- storm advisory
if string.find(fileLines[y], web.keywords[1]) ~= nil and web.data[1] == nil then
sub = string.gsub(fileLines[y + 1], &quot;%d&quot;, &quot;!&quot;)
sub = string.gsub(sub, &quot; , &quot;, &quot; &quot;)
table.insert(web.data, 1, sub)
-- last updated date and time
elseif string.find(fileLines[y], web.keywords[2]) ~= nil then
table.insert(web.data, 2, fileLines[y])
-- windchill
elseif string.find(fileLines[y], web.keywords[3]) ~= nil then
sub = string.gsub(fileLines[y], web.keywords[3], &quot;&quot;)
table.insert(web.data, 3, sub)
-- everything but forecast
else
for keyWord = 4, (#web.keywords - 1) do
if string.find(fileLines[y], web.keywords[keyWord]) ~= nil and web.data[keyWord] == nil then
sub = string.gsub(fileLines[y], web.keywords[keyWord], &quot;&quot;)
table.insert(web.data, keyWord, sub)
end
end
end
end
end

web.cleanTXT = function()
for y = 1, #web.data do
if web.data[y] ~= nil then
-- remove extra spaces from start of each string
while (string.sub(web.data[y], 1, 1) == &quot; &quot;) do
web.data[y] = string.sub(web.data[y], 2, -1)
end
-- remove degrees character
web.data[y] = string.gsub(web.data[y], &quot;°&quot;, &quot;&quot;)
end
end
-- Add keywords back in (skipping nill values, and tempature)
for keyWord = 3, (#web.keywords - 1) do
if web.data[keyWord] ~= nil then
if keyWord ~= 4 then
web.data[keyWord] = web.keywords[keyWord] .. &quot;: &quot; ..web.data[keyWord]
end
end
end
-- remove / from Temperature
web.data[4] = string.gsub(web.data[4], &quot; / &quot;, &quot; &quot;)
end

```

是的，我知道这是一个烂摊子，WordPress 是忽略标签，它只有 40 列，如果我不得不猜测。在顶部有一个名为 web.get()的函数，该函数使用 wget 从 weather underground 下载 html 页面，然后打开该文件并扫描其中的 JPG 图像，幸运的是，整个页面上唯一的 jpg 是 radar。一旦它有了雷达的 URL，它就剥离 HTML 标签并再次使用 wget 来下载雷达图像。

下一个函数是 web.sortTXT()，它将下载的 HTML 文件发送到 lynx，在那里去掉标签并输出一个纯文本文件。然后，该函数读取每一行，寻找关键字。有些关键词需要特殊操作…比如，如果它发现了风暴警报，它就知道跳到下一行，因为那一行只是说“国家气象局:”并将 lynx 插入的链接号改为“！”。在函数的末尾有一个小循环，它寻找其余的关键字，然后删除实际的关键字，这是删除关键字和数据之间不需要的空格所必需的。

最后一个函数是 web.cleanTXT()，它遍历所有的数据行并删除所有的前导空格。然后，它将关键字添加回适当的行，同时忽略不存在的空值(如 advisories 或 windchill)。它还忽略了温度关键字，因为我不需要显示温度这个词。最后，我删除了温度数据中的“/”，因为它使图形格式变得有趣，这只是为了分隔原始字符串中的 F 和 C 值。

所以我们现在已经安装并运行了软件，从 weather underground 下载了数据和雷达，删除了文本数据，进行了分类和清理，现在我们准备制作一些图形了！

加入我的第二部分，我将解释图形是如何在 Apple II 电脑上缩小、编码和绘制的。

 ******