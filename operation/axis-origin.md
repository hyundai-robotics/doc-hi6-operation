# 2.8 Optimization of the Axis Origin and Tool Length

You can make it possible for the axis integer and tool length to be automatically set to improve the accuracy of the linear interpolation trajectory and coordinate shifting.

* You can make it possible for the distance to the tooltip, which is difficult to measure in 3D, to be automatically set. The parameters to be calibrated are the axis origins of the H, V, R2, and B axes and the tool length in the X, Y, and Z directions.
* You can perform “optimization of axis origin and tool length” and of “tool length.”

{% hint style="warning" %}
You should optimize the “axis origin and tool length” before teaching the robot program. If the “axis origin and tool length” is optimized while a robot program has been created already, the position in the existing program may change.
{% endhint %}

The following shows how to set the optimization of the axis origin and tool length:

1.	Set the operation mode to manual mode using the mode switch on the teach pendant.

2.	After touching the \[Prog\] button in the JOB program window, input the program number, and then touch the \[OK\] button.



![](../.gitbook/assets/image%20%28314%29.png)

3.	Press the &lt;motor&gt; key on the teach pendant, and then the motor lamp will blink.

* If the motor is not turned on, check the error message on the log bar and resolve the trouble.

4.	Operate the robot using the jog key while holding the enabling switch on the back of the teach pendant.

5.	Place a pointed needle at an arbitrary location within the operation range of the robot, and then match the tooltip of the robot to it. The distance from the front end of the robot to the matched tooltip will be optimized.

6.	Record the step by touching the \[Record\] button on the right side of the Hi6 teach pendant screen.

![](../.gitbook/assets/image%20%28316%29.png)

7.	Change the robot’s posture and repeat the above steps 5–6 more than four times.

* Change the robot’s posture using all six axes as much as possible. Moreover, change the axis angle by at least 30 degrees.

8.	Touch the \[Set up\] button &gt; \[6: Auto Calibration &gt; 1: Optimize axis origin and tool length\] menu.

![](../.gitbook/assets/image%20%28324%29.png)

9.	Set the program number, tool number, and step position error allowable range created for the automatic calibration, and then touch the \[Execute\] button. Then the selected axis origin and tool length will be set.

![](../.gitbook/assets/image%20%28330%29.png)

* You should select Tool Length in the \[Optimization Selection\] option, starting from the automatic calibration of the second tool, when you use multiple tools. If you select Axis Origin and Tool Length, the previously set tool information will not match.

{% hint style="info" %}
For details on this function, refer to “[7.7.1 Optimization of Axis Origin and Tool Length](../7-setting/7-7-auto-calibration/axis-origin-tool-length-optimization.md).”
{% endhint %}

