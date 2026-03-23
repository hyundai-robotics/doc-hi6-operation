# 2.9 轴原点和工具长度的优化

您可以使轴整数和工具长度自动设置，以提高线性插值轨迹和坐标偏移的准确性。

* 您可以使工具提示的距离（在3D中难以测量）自动设置。要校准的参数是H、V、R2和B轴的轴原点以及X、Y和Z方向的工具长度。
* 您可以执行“轴原点和工具长度的优化”和“工具长度的优化”。

{% hint style="warning" %}
您应该在教学机器人程序之前优化“轴原点和工具长度”。如果在已经创建机器人的程序时优化了“轴原点和工具长度”，现有程序中的位置可能会发生变化。
{% endhint %}

以下显示了如何设置轴原点和工具长度的优化：

1. 使用教学 pendant 上的模式开关将操作模式设置为手动模式。

2. 在JOB程序窗口中，按住 `[SHIFT]` 并触摸 `[PROG]` 键，输入程序编号，然后触摸 `[OK]` 按钮。

    ![](../_assets/tp630/k-prog-step_eng.png)

    ![](../_assets/tp630/dlg-prog-sel_eng.png)

3. 按下教学 pendant 上的 `[motor]` 键，然后电机指示灯会闪烁。

* 如果电机未开启，请查看日志条上的错误信息并解决问题。

4. 在按住教学 pendant 背面的启用开关时，使用 jog 键操作机器人。

5. 在机器人操作范围内的任意位置放置一个尖针，然后将机器人的工具提示对准它。机器人前端到匹配工具提示的距离将被优化。

6. 通过触摸键盘上的 `[REC]` 键记录步骤。

    ![](../_assets/tp630/k-record_eng.png)

7. 改变机器人的姿势，并重复以上步骤 5-6 四次以上。

* 尽可能使用所有六个轴来改变机器人的姿势。此外，将轴角度至少改变 30 度。

8. 触摸 `[system]` 按钮 - `[6: Auto Calibration - 1: Optimize axis origin and tool length] ([6: Auto Calibration  - 1: Optimize axis origin and tool length])` 菜单。

    ![](../_assets/tp630/menu-axis-origin-tool-opt_eng.png)

9. 设置为自动校准创建的程序编号、工具编号和步骤位置误差允许范围，然后触摸 `[Execute]` 按钮。然后所选的轴原点和工具长度将被设置。

    ![](../_assets/tp630/axis-origin-tool-opt_eng.png)

* 当您使用多个工具时，应在第二个工具的 `[Optimization Selection]` 选项中选择工具长度。如果您选择了轴原点和工具长度，则之前设置的工具信息将会不正确。

{% hint style="info" %}
有关此功能的详细信息，请参阅 "[7.7.1 轴原点和工具长度的优化](../7-system/7-auto-calibration/1-axis-origin-tool-length-optimization.md)。"
{% endhint %}