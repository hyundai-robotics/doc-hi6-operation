# 7.3.2.8 键信号输出

`键信号输出 (Key Signal Output)` 是一个功能，允许您将所需变量分配给 F-key，并通过按键操作将该变量的值设置为 1 或 0。
它主要用于通过操作已分配输出变量的 F-key 来开启或关闭 I/O 输出信号。
（可以指定所有类型的变量，包括一般变量、别名和输出变量。）

您可以通过在 HOME 屏幕右侧按下 `[R4: User Key]` 打开 `键信号输出 (Key Signal Output)` 按钮。
如果未进行任何设置，所有按钮将为空。

您可以按如下方式配置按钮：

1. 触摸菜单 `[F2: 系统] - 2: 控制参数 - 2: 输入/输出信号设置 - 5: 关键信号输出 ([F2: system] - 2: Control parameter - 2: Input/Output signal setting - 5: Key signal output)`。

2. 设置要在按钮上显示的功能名称和选项，然后触摸 `[F7: 确认] ([F7: OK])` 按钮。

![](../../../_assets/tp630/ctrl-key-outsignal_eng.png)

* `标题 (title)`：显示在按钮上的名称
* `on-var`：当指定变量名称时，按钮打开时该变量的值被分配为 1。
* `off-var`：当指定变量名称时，按钮关闭时该变量的值被分配为 1。
* `切换 (toggle)`：
  + 已选中：每次按下按钮时，它在开启和关闭之间切换。
  + 未选中：按钮按下时开启，释放时关闭。
* `允许 在 自动 模式 (Permit on auto mode)`：
  + 已选中：此功能即使在自动模式下也会操作。
  + 未选中：此功能在自动模式下不操作。
* `关闭 开启 自动 模式 (OFF on auto mode)`：切换到自动模式时，为此功能设置的所有变量将被关闭。

{% hint style="info" %}
对于 `on-var` 和 `off-var`，例如，如果您输入 3.5 并按下 `[ENTER]`，则 fb3.do5 被输入。
如果您输入 5 并按下 `[ENTER]`，则 do5 被输入。
另外，您可以使用屏幕底部的 F-keys [fb]、[do] 和 [so] 来输入值。
{% endhint %}

3. 打开 `键信号输出 (Key Signal Output)` 按钮，并按住 `[SHIFT]` 键触摸注册的 F-key，以验证设置是否已正确应用。

![](../../../_assets/tp630/rbt-userkey-keysig_eng.png)

{% hint style="info" %}
您可以在 ${cont_model} 教导挂件的用户键区域用按钮注册所需的输出信号。有关注，请参考 " [2.7.2.1 键信号输出功能区域](../../../2-operation/7-user-key/2-button-registration/1-key-signal-output.md)"。
{% endhint %}