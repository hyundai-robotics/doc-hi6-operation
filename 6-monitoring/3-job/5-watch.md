# 6.3.5 观察

您可以将变量或表达式注册到观察面板以监控或更改值。


#### 打开观察面板

1. 分割屏幕并按左下角的 [选择] 按钮。

![](../../_assets/tp630/panel-split.png)
&nbsp;
![](../../_assets/tp630/panel-sel.png)

2. 在面板选择窗口中触摸 `Watch`。各种数据窗口打开。

![](../../_assets/tp630/panel-watch/panel-watch.png)

![](../../_assets/tp630/panel-watch/panel-watch-mon.png)


#### 如何使用

在顶部输入框中输入所需的变量或表达式，然后单击 '+' 按钮将新项目输入到表中。

![](../../_assets/tp630/panel-watch/panel-watch2.png)


您可以通过再次单击 `名称 (Name)` 列来修改您输入的变量名称或表达式。

![](../../_assets/tp630/panel-watch/panel-watch-rename.png)

如果您在 `力控制变量 (Value)` 列中单击以输入新值，您将更改该变量的值。更改表达式的值将被忽略。

选择姿态/偏移变量或表达式的 `力控制变量 (Value)` 列，然后按 `确认 (ENTER)` 键打开姿态/偏移属性窗口以查看和修改值。

![](../../_assets/tp630/panel-gvar/gv-edit-pose2.png)

要删除一行，选择该行并按 `SHIFT+DEL` 键。

如果您按下底部 F 按钮上的 [F7: 保存所有] 按钮，输入的变量和表达式列表将保存在 `cfg/watch.json` 文件中。此文件将在电源重启时自动加载。
您还可以通过 FTP 接收并编辑列表。如果您用编辑过的文件覆盖 `cfg/` 文件夹并单击 [F1: 加载所有] 按钮，它将应用于观察面板。

![](../../_assets/tp630/panel-watch/panel-watch-fbt.png)

单击 [F2: 向上交换] 和 [F3: 向下交换] 按钮以在与顶部和底部行交换的同时移动当前选定行的位置。  

在各种数据窗口中共有 10 页，因此您可以分组和管理您想要显示的变量或表达式。单击 [F4: 页面] 按钮以显示下一页，单击 `SHIFT`+[F4: 页面] 按钮以显示上一页。

可以使用 [F6: 子级] 按钮或 `确认 (ENTER)` 键查看数组或对象的元素，并可以使用 [F5: 上级] 按钮或 `ESC` 键上移到上一级。

您可以在 `起始索引` 编辑框中输入一个值，以从特定索引显示数组。([全局变量](3-global-variable/README?cont_model=${cont_model}) 窗口也有相同的操作方法。)

{% hint style="warning" %}
* 要更新结果值的显示，表达式会在快速的周期内反复计算。请注意不要在表达式中包含会导致系统特定创建或更改的函数，例如 mkucs()。
{% endhint %}