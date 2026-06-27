# 6.3.3.1 基本功能

##### 查找变量

如果由于变量数量众多而难以查找所需的变量，请在顶部的过滤器中输入变量名称的一部分。仅以您输入的过滤器字符串开头的变量将显示在屏幕上，方便您找到它们。

![](../../../_assets/tp630/panel-gvar/gv-find.png)

##### 更改变量的值（对于 bool, int, double, string 类型）

选择所需变量的 `值 (value)` 列并输入新值。
按 ENTER 键将所输入的值应用于变量。

![](../../../_assets/tp630/panel-gvar/gv-edit-value.png)

##### 更改变量的值（对于 pose, shift 类型）

选择所需姿态或位移变量的 `值 (value)` 列。

![](../../../_assets/tp630/panel-gvar/gv-edit-pose1.png)

按 ENTER 键打开姿态或位移属性窗口。
编辑后，点击 [F7: OK] 按钮。

![](../../../_assets/tp630/panel-gvar/gv-edit-pose2.png)

##### 更改变量类型

选择所需变量的 `类型 (type)` 列并按 ENTER。将出现如下所示的创建变量对话框。

![](../../../_assets/tp630/panel-gvar/gv-edit-type.png)

![](../../../_assets/tp630/panel-gvar/gv-create-var.png)

从类型列表中选择所需类型，然后点击 OK 按钮以更改变量的类型。请注意，如果类型更改，值将被初始化。

您还可以为多个变量选择类型并按 ENTER 一次性更改它们。
（您可以通过按 SHIFT+上/下箭头键选择多个连续单元格。或者，您可以在按住 CTRL 键的同时触摸多个单元格进行选择。）

![](../../../_assets/tp630/panel-gvar/gv-sel-multi-type.png)

##### 重命名变量

选择您想要的变量的 `名称 (name)` 列，然后打开软键盘以输入新名称。
按 ENTER 键将其更改为您输入的名称。

![](../../../_assets/tp630/panel-gvar/gv-edit-name.png)

##### 创建变量

在顶部的过滤器中，输入您想要创建的变量名称。

![](../../../_assets/tp630/panel-gvar/gv-new.png)

验证没有具有重复名称的变量后，点击过滤器旁边的 + 按钮。变量将使用默认类型 `int`（整数）创建。使用上述方法更改创建变量的类型。

![](../../../_assets/tp630/panel-gvar/gv-new2.png)

##### 删除变量

选择您想要删除的变量。
按 DEL (CTRL+BACKSPACE) 键显示确认/取消对话框。在确认变量名称后，按 OK 按钮。

![](../../../_assets/tp630/panel-gvar/gv-delete.png)