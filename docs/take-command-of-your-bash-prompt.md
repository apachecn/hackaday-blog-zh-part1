# 掌控您的 BASH 提示符

> 原文：<https://hackaday.com/2009/09/05/take-command-of-your-bash-prompt/>

![color_bash_prompt](img/d1eb1fdad8dd014e60731c74712e3e54.png "color_bash_prompt")

[Joshua]已经整理出了一个定制 BASH 提示符的列表。命令行界面中的命令提示符用于显示系统已准备好执行下一个命令。通常这只不过是用户名、主机名和工作目录:

mike@krusty:~$

[Joshua 的]定制示例可用于对提示中的信息进行颜色编码，更改显示的信息，并在键入无效命令时使提示做出不同的响应。BASH 提示参考有助于理解这些命令的作用。最简单的简化就是理解非打印字符(比如颜色代码)被转义的方括号包围。例如，第 1 行是红色的序列，第 2 行是深灰色的序列，第 3 行设置一个简单的提示，以红色显示，其后的所有文本以深灰色显示:

```
\[\e[0;31m\]
\[\e[1;33m\]
PS1="\[\e[0;31m\]\u@\h:\w\$ \[\e[1;30m\]"
```

![bad_command_prompt](img/15a59705bfb0a5dd0e9a93c428313748.png "bad_command_prompt")

上面你会注意到一个附加的通知，我们输入了一个无效的命令。该提示由以下代码生成:

```
PS1="\`if [ \$? != 0 ]; then echo \[\e[33m\]---=== \[\e[31m\]Oh noes, bad command \[\e[33m\]===---; fi\`\n\[\e[1;30m\]XX \[\e[0;32m\]Hack a Day \[\e[1;30m\]XX\n\[\e[0;37m\][\[\e[1;31m\]\@\[\e[0;37m\]] \[\e[0;32m\]\u@\h \[\e[0;37m\][\[\e[1;34m\]\w\[\e[0;37m\]] \[\e[0;32m\]\$ \[\e[0m\] "
```

我们经常使用 shell，这将提示符从我们通常忽略的东西变成了一个有用的工具。在 shell 中键入命令只会更改当前会话的提示符。如果你想要一个更永久的改变，把这一行加到你的~/的底部。bashrc 文件。

[via [Digg](http://digg.com/linux_unix/8_Useful_and_Interesting_Bash_Prompts_u2013_Make_Tech_Easie)