# 7.7.2 Positioner Calibration

Positioner calibration is a function that enables the robot to perform a synchronized follow-up with the operation of a jig device installed outside the robot or to perform a linear or circular operation relative to the jig device. The external jig device in which the positioner calibration function will be applied to is called a positioner or station.

Using the positioner calibration function makes it possible to compensate for the operational difficulties because of the limitation of the robot operation area. In other words, even if the positioner moves while the workpiece is fixed onto it, the robot can still perform a linear or circular operation on the workpiece by following up with the movement of the positioner.

You can simply set the positioner’s coordinate system by performing the positioner calibration by teaching three points for a 1-axis positioner and five points for a 2-axis positioning.

![Figure 68 1-Axis Positioner \(Left\) / 2-Axis Positioner \(Right\)](../../_assets/image%20%28244%29.png)

The information on the main functions of the positioner calibration is as follows.

| Main Functions | Description |
| :--- | :--- |
| Positioner group | 1–4 groups are supported |
| Positioner axis count | 1-axis positioner and 2-axis positioner are supported \(rotation axis\) |
| Interpolation mode | Linear interpolation and circular interpolation are supported |

{% hint style="info" %}
* The positioner calibration function can be used while the positioner group is set.
* For more details, refer to the “Hi6 Controller Positioner Sync Function Manual.”
{% endhint %}

