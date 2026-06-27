# 2.3.1.1 插值

插值是指步骤之间的插值路径，[Step N] 的插值方法决定了 `[Step N-1]` 和 `[Step N]` 之间路径的形式。

* P-PTP \(Point-to-Point\) 这是一般插值模式中最快的，因为它基于各个轴而不是工具提示进行两个步骤之间的路径插值。考虑到由旋转关节组成的工业机器人特性，工具提示的路径通常呈 C 形。




![Figure 15 Example of the Tooltip Path in P-PTP Interpolation](../../../_assets/image_73.png)

* L-线性插值 它在笛卡尔空间内两个步骤之间沿线性路径移动。它用于需要线性路径的情况，如弧焊部分。移动的同时，手腕姿态会自动按如下方式变化。

![Figure 16 Example of L-Linear Interpolation](../../../_assets/image_48.png)

在进行线性插值时，在某些条件下，机器人无法自动改变手腕姿态，这种情况称为奇异姿态。



{% hint style="info" %}
无法执行姿态插值的奇异姿态如下。

* 如果 B 轴接近死区：有关死区设置的详细信息，参见 "[7.4.5 B-axis Deadzone](../../../7-system/4-robot-parameter/5-b-axis-deadzone.md)"。
* 当 B 轴的符号改变时：当 B 轴角度的符号切换 \( - → + \) 或 \( + → - \)
* 当 R2 和 R1 轴的角度变化超过 180 度
* 当 B 轴 \(轴 5\) 的中心或工具提示经过 S 轴 \(轴 1\) 的旋转中心时：姿态和轨迹可能会有误差。
* 当 S 轴的角度变化超过 180 度
{% endhint %}

* C-圆形插值

  它在两个步骤之间创建的圆形路径上移动。确定圆的需要三个点，选择它们的参考如下。



  * 在从 `[Step n]` 移动到 `[Step n+1]` 时，如果 `[Step n+1]` 的插值方法是 C-圆形插值，则需要参考下一个步骤 `[Step n+2]`。

  * 如果 `[Step n+2]` 的插值方法是 C-圆形插值，则需要根据 `[Step n]`、`[Step n+1]` 和 `[Step n+2]` 确定圆，并在它们之间的运动应该沿 `[Step n]` - `[Step n+1]` 的弧进行。

  * 如果 `[Step n+2]` 的插值方法不是圆形插值，则需要参考前一个步骤 `[Step n-1]`，根据 `[Step n-1]`、`[Step n]` 和 `[Step n+1]` 确定圆，并在它们之间的运动应该沿 `[Step n]` - `[Step n+1]` 的弧进行。



![Figure 16 Example 1 of C-Circular Interpolation](../../../_assets/image_338.png)

如果您使用选择确定圆的三个点的标准，即使在连续弧的情况下，也可以通过同一点的双重注册创建程序。

通过考虑沿运动路径确定步骤的插值方法，并使用同一点双重注册功能，可以创建所需的程序。

![Figure 17 Example 2 of C-Circular Interpolation](../../../_assets/image_302.png)

* 静态工具插值

  当机器人拥有工件并使用外部固定工具进行工作时，将使用此方法。在这种情况下，将根据机器人拥有的工件进行插值。

  有关静态工具的插值类型的详细信息，请参见 "[7.3.6.2 Stationary Tool Coordinate System](../../../7-system/3-control-parameter/6-cordsys-reg/2-stationary-tool-crdsys.md)"。