# 6.3.6 调用堆栈

在面板选择窗口中点击 `[Call Stack]` 以显示调用堆栈窗口。要理解本节内容，必须先了解 `call`~`return` 语句和 hrscript 的局部变量。

[调用、跳转语句和子程序](https://hrbook-hrc.web.app/#/view/doc-hrscript/zh/3-flowcontrol-subprogram/7-call-jump/README?cont_model=${cont_model})

[局部变量](https://hrbook-hrc.web.app/#/view/doc-hrscript/zh/3-flowcontrol-subprogram/8-local-global-var/1-local-variables?cont_model=${cont_model})


### 机器人语言的调用和返回

在机器人语言中，可以使用 `call` 语句调用一个子作业程序。当执行 `end` 或 `return` 语句时，子程序返回到调用它的 `call` 语句的下一语句位置。例如，在下图中，您可以看到作业 5 调用作业 8，运行到 `return` 语句，然后继续执行作业 5 的 `call` 语句的下一语句。

![子作业的调用和返回](../../_assets/call-return.png)

绘制在程序旁边的容器形状是一个称为调用堆栈的存储空间。调用堆栈构建当前运行程序的调用帧。调用帧包含一组实际参数和局部变量以及作业程序的返回地址。  
因为在调用子程序时，新调用帧被推到顶部，所以调用它的程序的局部变量被保留，并准备了一个新的局部变量空间。  
当子程序返回时，顶部的调用帧被丢弃（弹出），下面的调用帧再次变为顶部。因为调用帧保留了调用前的实际参数和区域变量，并且还具有返回的位置信息，所以被调用的程序可以继续执行在调用之前正在进行的任务。


### 调用堆栈面板

您可以在调用堆栈面板中查看当前调用堆栈的内容。
<br><br>

0001_main.job
```python
var n_work=10
call 0005_init,12
end
```

0005_init.job
```python
param mode
var sensor_id
call 0008_go_home
for sensor_id=1 to 5
  call 0009_check_sensor,sensor_id # --------- (A)
next
end
```

0008_go_home.job
```python
var pos1, pos2
# 做某事
end
```

0009_check_sensor.job
```python
param id
var sensor_value
# 做某事 --------- (B)
end
```

在作业编辑窗口、调用堆栈面板和局部变量面板打开的情况下，如果当前程序处于作业 5 的 `for`~`next` 循环中第三次执行的 `call` 语句并执行到 (B) 位置，教学挂件屏幕将显示如下状态。

![作业编辑、调用堆栈、局部变量](../../_assets/call-stack.png)


调用堆栈的底部帧是作业 1，中间帧是作业 5，顶部帧是作业 9。> 形状的光标指向作业 9，并且局部变量面板显示参数 ` (id)` 和局部变量 `sensor_value` 的值。因此，您可以检查作业 9 是被作业 5 调用的，而作业 5 是被作业 1 调用的。  
如果您想查看作业 5 调用的位置，请选择作业 5 的帧并按 `确认 (ENTER)` 键。作业编辑面板中的光标将立即移动到 (A) 位置，以显示调用的位置。局部变量面板显示作业 5 的帧内容，即参数 `模式 (mode)` 和局部变量 `sensor_id`，分别为 12 和 3 的值。

![作业编辑、调用堆栈、局部变量- 2](../../_assets/call-stack2.png)

通过选择被调用作业的帧，您可以轻松理解到目前为止的程序流。

{% hint style="warning" %}
`[caution]` 在进行步进向前 (Step-FWD) 或播放操作时，确保在恢复操作时将 > 光标恢复到顶部帧位置。否则，将认为作业光标的位置发生了变化，并将初始化调用堆栈。
{% endhint %}