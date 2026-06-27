# 7.7.5 重力方向自动设置

${cont_model} 控制器基于动力学，因此设置重力方向非常重要。

一般而言，机器人安装方向垂直于重力方向，如下所示。如果机器人斜置于地面，则应在机器人控制器中设置重力方向。此时，可以使用自动重力方向设置功能。

![图74 安装在地面上的机器人重力方向 \(左\) / 安装在斜坡上的机器人重力方向 \(右\)](../../_assets/image_507.png)

设置重力方向的方法如下。

1. 在外部附上一个重物以指示重力方向，然后在重力作用方向上教导两个点 \(步骤1，步骤2\)。

2. 触摸 `[6: Auto Calibration - 8: Automatic setting of gravity direction] ([6: Auto Calibration  - 8: Automatic setting of gravity direction])` 菜单。

3. 输入程序编号后，触摸 `[Execute]` 按钮。然后，方向向量将被计算并显示。

    ![](../../_assets/tp630/system-calib-gravity_eng.png)

4. 检查方向向量值后，触摸 `[OK]` 按钮。然后，方向将被设置为重力方向。