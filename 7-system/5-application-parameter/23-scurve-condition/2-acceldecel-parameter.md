# 7.5.23.2 Acceleration/Deceleration Parameters

S-curve conditions and **maximum jerk** complement each other. When optimizing a process with only the S-curve setting proves difficult, or when you need to adjust the maximum jerk limit for each joint, you adjust the parameters.

![](../../../_assets/tp630/s-curve_acceldecel_parameter.png)

Relationship Between Jerk and Motion
Jerk is the rate of change of acceleration, and modifying this value produces the following characteristic changes.

- **Decrease maximum jerk (↓):** Acceleration changes more gradually, making motion smoother and reducing vibration. However, it takes longer to reach the target speed, which can increase cycle time.

- **Increase maximum jerk (↑):** Provides a more responsive motion, but if the value is too high the "smooth motion" effect of the S-curve condition is diminished, leading to greater mechanical impact.

Automatic Update of Maximum Jerk
The system automatically recalculates the maximum jerk value whenever key parameters change to maintain equipment stability.

{% hint style="warning" %}
**Caution:** When you manually set a value, modifying the top speed or acceleration time will overwrite the manually entered maximum jerk with the system-calculated value. If you have optimized the jerk value for a specific process, be sure to back up the existing value before making changes.
{% endhint %}


{% hint style="info" %}
Because acceleration/deceleration parameters have a large impact on robot motion characteristics, they are only enabled in Engineering mode or higher.
{% endhint %}
