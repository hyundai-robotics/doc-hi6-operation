# 2.7.2.1 Key Signal Output Function Area

`KEY 信号输出 (Key Signal Output)` 是一个允许您将所需变量分配给 F 键并通过按钮操作将该变量的值设置为 1 或 0 的功能。 它主要用于通过操作分配了输出变量的 F 键来打开或关闭 I/O 输出信号。 （可以指定所有类型的变量，包括一般变量、别名和输出变量。）

您可以通过按 HOME 屏幕右侧的 `[R4: User Key]` 打开 `KEY 信号输出 (Key Signal Output)` 按钮。 如果没有进行设置，则所有按钮将为空。

您可以按如下方式配置按钮：

1. 打开 `KEY 信号输出 (Key Signal Output)` 按钮，轻触 `[CTRL] + [User Key]`。 `Key Signal Output Setting` 窗口将出现。

2. 设置要在按钮上显示的功能名称和选项，然后轻触 `[F7: 确定] ([F7: OK])`。

![](../../../_assets/tp630/ctrl-key-outsignal_eng.png)

* `标题 (title)`: 显示在按钮上的名称
* `on-var`: 当指定变量名称时，按钮打开时会将值 1 分配给该变量。
* `off-var`: 当指定变量名称时，按钮关闭时会将值 1 分配给该变量。
* `切换 (toggle)`:
  + Checked: 每次按下按钮时，按钮在 ON 和 OFF 之间切换。
  + Unchecked: 按下按钮时变为 ON，释放时变为 OFF。
* `自动 模式下 允许 (Permit on auto mode)`:
  + Checked: 该功能在自动模式下也能操作。
  + Unchecked: 该功能在自动模式下不操作。
* `自动 模式下 关闭 (OFF on auto mode)`: 切换到自动模式时，为此功能设置的所有变量都将被关闭。

{% hint style="info" %}
对于 `on-var` 和 `off-var`，例如，如果您输入 3.5 并按下 `[ENTER]`，则输入 fb3.do5。 如果您输入 5 并按下 `[ENTER]`，则输入 do5。 或者，您可以使用屏幕底部的 F 键 [fb]、[do] 和 [so] 输入值。
{% endhint %}

3. 打开 `KEY 信号输出 (Key Signal Output)` 按钮，并同时触摸注册的 F 键和 `[SHIFT]` 键，以确认设置已正确应用。

![](../../../_assets/tp630/rbt-userkey-keysig_eng.png)

{% hint style="info" %}
您也可以从 `[F2: 系统] - 2: 控制参数 - 2: 输入/输出信号设置 - 5: 键信号输出 ([F2: system] - 2: Control parameter - 2: Input/Output signal setting - 5: Key signal output)` 访问相同的设置屏幕。 有关更多详细信息，请参阅 "[7.3.2.8 Key Signal Output](../../../7-system/3-control-parameter/2-io-signal-setting/8-key-signal-output.md)"。
{% endhint %}