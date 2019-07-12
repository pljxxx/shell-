## Bash陷阱命令

通常情况下，您希望在脚本中捕获特殊信号/中断/用户输入以防止出现不可预测的情况。

陷阱是你尝试的命令：

- ```trap <arg/function> <signal>```

### 例
  
 ```shell
#!/bin/bash
# traptest.sh
# notice you cannot make Ctrl-C work in this shell, 
# try with your local one, also remeber to chmod +x 
# your local .sh file so you can execute it!

trap "echo Booh!" SIGINT SIGTERM
echo "it's going to run until you hit Ctrl+Z"
echo "hit Ctrl+C to be blown away!"

while true:         
do
    sleep 60       
done
 ```
  
当然你可以替换“ ```echo Booh！```” 功能：

```shell
function booh {
  echo "booh!"
}
```

并在陷阱中调用它：

```shell
trap booh SIGINT SIGTERM
```

您可以捕获的一些常见信号类型：

-  ```SIGINT ```：用户发送中断信号（Ctrl + C）

-  ```SIGQUIT ```：用户发送退出信号（Ctrl + C）

-  ```SIGFPE ```：尝试非法数学运算

您可以输入以下命令检出所有信号类型：

```shell
kill -l
```

注意每个信号名称前的数字，您可以使用该数字来避免在陷阱中键入长字符串：

```shell
#2 corresponds to SIGINT and 15 corresponds to SIGTERM
trap booh 2 15
```

trap的常见用法之一是清理临时文件：

```shell
trap "rm -f folder; exit" 2
```

### 练习

本节没有练习。
