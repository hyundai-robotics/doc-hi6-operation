# 2.7.1 Jog Keys

It will be used in manual mode. When you are holding the enabling switch while the motor is turned on, the &lt;enter&gt;, &lt;esc&gt;, and &lt;←/→&gt; keys and number keys on the teach pendant will operate as “jog keys.”

![Figure 25 Jog Keys on the Teach Pendant](../../_assets/image%20%2895%29.png)

* The name of the axis assigned to each key will be displayed in the jog bar at the right edge of the display.
* The operation keys on the right are for the direction of increase \(+\), and the operation keys on the left are for the direction of decrease \(-\).

Only in the case in which the selected mechanism is mechanism \[0\] robot selected during jogging, if the total number of axes of the next mechanism \[1\] is less than two, they will be assigned according to the order of the registered additional axes. At this time, if unassigned keys remain in the mechanism \[1\] and the next mechanism has room, in terms of the number of axes to which the remaining axes can be assigned, they will be sequentially assigned.

For example, whether to perform an assignment for the axes J7 and J8 according to the number of axes of the mechanisms for the additional axes will be as follows.

| Mechanism \[0\] | Mechanism \[1\] | Mechanism \[2\] | Whether to assign for J7 axis / J8 axis |
| :--- | :--- | :--- | :--- |
| 6-axis robot | Travel axis, Axis 1 | Positioner, Axis 1 | J7: Travel axis / J8: Positioner |
| 6-axis robot | Travel axis, Axis 1 | Positioner, Axis 2 | J7: Travel axis / J8: Not assigned |
| 6-axis robot | Travel axis, Axis 2 | Positioner, Axis 2 | J7: Travel axis 1 / J8: Travel axis 2 |
| 6-axis robot | Travel axis, Axis 3 | Positioner, Axis 1 | J7: Not assigned / J8: Not assigned |







