# 7.4.5 B-Axis Deadzone

在 B 轴的 0 度附近，R1 轴的旋转中心和 R2 轴的旋转中心轴几乎是平行的。当机器人的 TCP 进行线性插补或圆形插补等插补操作时，即使是小的移动，手腕轴也会迅速移动。

设置 B 轴无使用区域。

1.	触摸 `[3: Robot Parameter - 5: B-axis Deadzone] ([3: Robot Parameter  - 5: B-axis Deadzone])` 菜单。

2.	在设置确定无使用区域的角度和设置插补处理模式后，触摸 `[OK]` 按钮。

    ![](../../_assets/tp630/robot-baxis-deadz_eng.png)



* `[Setting Value]`: 您可以输入用于确定 B 轴无使用区域的角度。
* 
  `[Dead zone interpolation]`: 当机器人的轨迹必须在插补操作中经过 B 轴无使用区域时，您可以执行关于错误处理和机器人停止的设置。