## 特殊命令sed，awk，grep，sort

此部分尚不存在。

要提供教程，只需分叉以下存储库：

<https://github.com/ronreiter/interactive-tutorials>

然后，您可以添加或编辑教程，然后向我发送拉取请求。

要编写教程，只需在```tutorials```目录中的相关目录下创建Markdown页面，然后在相关部分的欢迎屏幕中将其链接。 添加后，请确保通过运行Flask Web服务器正确链接。

要链接到您创建的教程，请使用双括号从您要链接的页面（通常是```Welcome.md```页面）创建链接。

每个教程都包含对主题的简要说明，以及一个测试用户的简短练习。 一旦用户根据练习完成修改代码，它就应该执行以打印出您将提供的预期输出。

每个教程必须具有以下结构：

### 文件名.md

```shell
Tutorial
--------
Here you may write text that explains a certain feature.

Exercise
--------
Here you will need to write the purpose of the exercise. Finishing the exercise correctly
must be accomplished using the new feature that you are explaining.

Tutorial Code
-------------
Write a code block that will appear on the interpreter window. For example, you may
write an empty function, which the user must complete in order to finish the exercise.

Expected Output
---------------
Write a code block that will describe the exact output expected from the modified code,
if it has been modified correctly.

Solution
--------
Write the solution code to the problem.
```
