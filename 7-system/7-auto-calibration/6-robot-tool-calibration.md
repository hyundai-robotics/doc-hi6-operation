# 7.7.6 机器人的校准和工具

机器人和工具的校准功能将在可以使用 3D 测量设备测量机器人位置的环境中使用。

1. 在机器人工具提示下选择要测量的位置，移动机器人的位置和姿势以多种方式测量超过 15 个点的位置，并将机器人的位置记录为程序。

    ![](../../_assets/image_245.png)

2. 将测量到的机器人位置数据（测量点数据）整理为 X、Y 和 Z 格式，然后创建一个文件（格式：ASCII 扩展名：MSR）。

    ![](../../_assets/tp630/system-calib-robottool-msr.png)

3. 将位置数据文件保存到可移动存储设备中，然后将可移动存储设备连接到教学挂件。状态栏中将出现 `[USB]` 图标（）。

4. 点击 `[6: 自动校准 - 9: 机器人和工具校准条件] ([6: Auto Calibration  - 9: Robot and Tool calibration condition])` 菜单。

5. 点击 `[Explorer]` 按钮选择一个位置数据文件，并设置用于测量的机器人程序。

    ![](../../_assets/tp630/system-calib-robottool_eng.png)

6. 点击 `[OK]` 按钮。然后，屏幕将切换到机器人和工具校准屏幕。

7. 点击机器人和工具校准执行屏幕上的 `[Execute]` 按钮。然后，校准结果将出现。

    ![](../../_assets/tp630/system-calib-robottool-exe_eng.png)

8. 检查校准结果后，点击 `[OK]` 按钮。然后，校准结果将自动应用于轴原点和工具整数。

9. 点击 `[3: 机器人参数 - 1: 工具数据] ([3: Robot Parameter  - 1: Tool Data])` 菜单。然后，您可以检查机器人校准执行结果。

    ![](../../_assets/tp630/system-calib-robottool-toolinfo_eng.png)

<Br>

{% hint style="info" %}
校准参数的轴原点和工具长度 X、Y 和 Z 值为轴 2-5（H、V、R2 和 B 轴）所选。仅校准工具时，需在取消选择每个轴的值后再执行。
{% endhint %}

<br>

#### 恢复校准数据

在执行机器人和工具校准时，校准数据作为 calibration.json 文件单独存储在路径 /ata0:2/lib/hi6/backup/ 中。<br>
如果因为系统初始化等操作而丢失校准数据，可以使用存储的文件进行恢复。（但是，如果通过执行串行编码器重置初始化了编码器数据，则无法恢复。）

1. 如果路径 /ata0:2/lib/hi6/backup/ 中存在 calibration.json 文件，则“恢复”按钮将被激活。
2. 在进行恢复并重新上电后，先前执行的机器人和工具校准数据将被应用。

![](../../_assets/tp630/robot_calib_recover.png)