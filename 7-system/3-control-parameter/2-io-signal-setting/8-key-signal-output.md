# 7.3.2.8 Key Signal Output

`KEY 信号输出 (Key Signal Output)` 是一个功能，允许您将所需变量分配给 F-key 并通过按钮操作将该变量的值设置为 1 或 0。
它主要用于通过操作分配了输出变量的 F-key 来打开或关闭 I/O 输出信号。
(可以指定所有类型的变量，包括一般变量、别名和输出变量。)

您可以通过在主页屏幕右侧按下 `[R4: User Key]` 打开 `KEY 信号输出 (Key Signal Output)` 按钮。
如果没有进行任何设置，所有按钮将为空。

您可以按如下方式配置按钮：

1. 触摸菜单 `[F2: 系统] - 2: 控制参数 - 2: 输入/输出信号设置 - 5: 键信号输出 ([F2: system] - 2: Control parameter - 2: Input/Output signal setting - 5: Key signal output)`。

2. 设置要显示在按钮上的功能名称和选项，然后触摸 `[F7: 确定] ([F7: OK])` 按钮。

![](../../../_assets/tp630/ctrl-key-outsignal_eng.png)

* `标题 (title)`: 显示在按钮上的名称
* `on-var`: 当指定变量名称时，在按钮打开时变量的值被赋值为 1。
* `off-var`: 当指定变量名称时，在按钮关闭时变量的值被赋值为 1。
* `切换 (toggle)`:
  + 选中: 按钮每次被按下时在 ON 和 OFF 之间切换。
  + 未选中: 按下按钮时打开，释放时关闭。
* `自动 模式下 允许 (Permit on auto mode)`:
  + 选中: 此功能即使在自动模式下也可以操作。
  + 未选中: 此功能在自动模式下不操作。
* `自动 模式下 关闭 (OFF on auto mode)`: 切换到自动模式时，所有为此功能设置的变量都关闭。

{% hint style="info" %}
对于 `on-var` 和 `off-var`，例如，如果您输入 3.5 并按 `[ENTER]`，则输入 fb3.do5。
如果您输入 5 并按 `[ENTER]`，则输入 do5。
另外，您可以使用屏幕底部的 F-keys [fb], [do], 和 [so] 来输入值。
{% endhint %}

3. 打开 `KEY 信号输出 (Key Signal Output)` 按钮，并同时按下注册的 F-key 和 `[SHIFT]` 键，以确认设置已正确应用。

![](../../../_assets/tp630/rbt-userkey-keysig_eng.png)

{% hint style="info" %}
您可以在 ${cont_model} 教学终端的用户键区域注册所需的输出信号。有关详细信息，请参阅 "[2.7.2.1 Key Signal Output Function Area](../../../2-operation/7-user-key/2-button-registration/1-key-signal-output.md)"。
{% endhint %}