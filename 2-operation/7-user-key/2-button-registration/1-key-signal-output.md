# 2.7.2.1 关键信号输出功能区域

`键信号输出 (Key Signal Output)` 是一个允许您将所需变量分配给 F键并通过按钮操作将该变量的值设置为 1 或 0 的功能。 主要用于通过操作分配了输出变量的 F键打开或关闭 I/O 输出信号。 （所有类型的变量都可以被指定，包括一般变量、别名和输出变量。）

您可以通过按 HOME 屏幕右侧的 `[R4: User Key]` 打开 `键信号输出 (Key Signal Output)` 按钮。 如果没有进行任何设置，所有按钮将为空。

您可以按如下方式配置按钮：

1. 在 `键信号输出 (Key Signal Output)` 按钮开启的情况下，触摸 `[CTRL] + [User Key]`。 `键信号输出设置` 窗口出现。

2. 设置要显示在按钮上的功能名称和选项，然后触摸 `[F7: 确认] ([F7: OK])`。

![](../../../_assets/tp630/ctrl-key-outsignal_eng.png)

* `标题 (title)`：显示在按钮上的名称
* `on-var`：当指定变量名时，按钮打开时会将值 1 分配给该变量。
* `off-var`：当指定变量名时，按钮关闭时会将值 1 分配给该变量。
* `切换 (toggle)`：
  + Checked: 按钮每次按下时在开启和关闭之间切换。
  + Unchecked: 按钮被按下时开启，释放时关闭。
* `允许 在 自动 模式 (Permit on auto mode)`：
  + Checked: 此功能在自动模式下也可操作。
  + Unchecked: 此功能在自动模式下不操作。
* `关闭 开启 自动 模式 (OFF on auto mode)`：切换到自动模式时，此功能设置的所有变量将被关闭。

{% hint style="info" %}
对于 `on-var` 和 `off-var`，例如，如果您输入 3.5 并按下 `[ENTER]`，则 fb3.do5 被输入。 如果您输入 5 并按下 `[ENTER]`，则 do5 被输入。 或者，您可以使用屏幕底部的 F 键 [fb]、[do] 和 [so] 输入值。
{% endhint %}

3. 打开 `键信号输出 (Key Signal Output)` 按钮，并触摸注册的 F 键和 `[SHIFT]` 键以验证设置是否正确应用。

![](../../../_assets/tp630/rbt-userkey-keysig_eng.png)

{% hint style="info" %}
您还可以通过 `[F2: 系统] - 2: 控制参数 - 2: 输入/输出信号设置 - 5: 关键信号输出 ([F2: system] - 2: Control parameter - 2: Input/Output signal setting - 5: Key signal output)` 访问相同的设置界面。 有关更多详细信息，请参阅 "[7.3.2.8 Key Signal Output](../../../7-system/3-control-parameter/2-io-signal-setting/8-key-signal-output.md)"。
{% endhint %}