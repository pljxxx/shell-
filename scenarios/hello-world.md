## Hello,World!

本教程一般讨论shell编程，重点关注Bash（“Bourne Again Shell”）shell作为主shell解释器。使用其他常见shell（如sh，csh，tcsh）进行Shell编程也会被引用，因为它们有时与bash不同。
Shell编程可以通过在shell提示符下直接执行shell命令，或者按照执行顺序，在文本文件（称为shell脚本）中存储它们，然后执行shell脚本来完成。要执行，只需在文件具有执行权限（chmod + x filename）后编写shell脚本文件名即可。
shell脚本文件的第一行以“sha-bang”（＃！）开头，它不作为注释读取，后面是shell解释器所在的完整路径。该路径告诉操作系统该文件是一组要输入指示的解释器的命令。请注意，如果“sha-bang”中给出的路径不正确，则会出现错误消息，例如“未找到命令。”，可能是脚本执行的结果。通常将shell脚本命名为“.sh”扩展名。第一行可能如下所示：

#### #!/bin/bash

添加注释：“＃”后面的任何文本都被视为注释
要找出当前活动的shell以及它的路径是什么，请在shell提示符下键入突出显示的命令（示例响应如下）：

#### ps | grep $$

987 tty1 00:00:00 bash
此响应显示您使用的shell是'bash'类型。接下来找出shell解释器的完整路径

#### which bash

/bin/bash
此响应显示shell解释器的完整执行路径。确保脚本开头的“sha-bang”行与此相同的执行路径匹配。

### 练习

使用“echo”命令打印“Hello，World！”行。
