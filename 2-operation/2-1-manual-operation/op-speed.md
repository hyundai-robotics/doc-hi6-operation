# 2.1.2 Operation Speed Adjustment

In manual mode, you can operate the robot using the step forward/backward operation and manual jog operation. With the function button on the left side of the Hi6 teach pendant screen, you can check and adjust the step forward/backward speed limit \(![](../../.gitbook/assets/c1.png)\) and the jog’s speed level \(![](../../.gitbook/assets/c2.png)\).

![](../../.gitbook/assets/image%20%28310%29.png)

To set the step speed limit, touch the \[Speed Adjustment\] button and then input the speed value in the setting window. The step forward/backward speed limit will be displayed in numbers along with the unit \(mm/sec\) on the \[Speed Adjustment\] button. The maximum speed of the robot tool and link will be limited below the speed limit.

![](../../.gitbook/assets/image%20%28299%29.png)

For example, if the speed limit in manual mode is set to 250 mm/s and the recorded step speed is 1,000 mm/s, the moving speed of the step will be limited to 250 mm/s during the step forward/backward operation. When the recorded speed is 100 mm/s, the robot will move at 100 mm/s because the recorded speed does not exceed the speed limit.

{% hint style="info" %}
In automatic mode, the \[Speed Adjustment\] button will display the playback speed \(%\) instead of the step speed limit \(mm/sec\).
{% endhint %}

To set the jog speed level \(1: Low to 8: High\), touch the \[ / \] button repeatedly until the desired speed level appears. The jog speed level will be displayed in numbers between the \[ / \] buttons. Even in this case, the maximum speed of the robot tool and link will be limited below the speed limit.

![](../../.gitbook/assets/lbt-spd-bar2%20%281%29.png)

{% hint style="warning" %}
If the length and angle in the tool data are set differently from the actual values, the tool may operate too fast in manual mode. Before operating the robot, you must make sure that the tool data is set correctly.
{% endhint %}



