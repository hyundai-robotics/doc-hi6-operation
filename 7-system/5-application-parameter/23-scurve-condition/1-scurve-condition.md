# 7.5.23.1 S-curve condition

S-curve condition settings allow you to define the characteristics of the acceleration and deceleration phases that occur when the robot is operating in detail. Configure the items below to match each process's required characteristics (such as path accuracy or vibration reduction).

![](../../../_assets/tp630/s-curve_condition.png)

  * Condition Name: Enter the name of the condition.
  * Path Accuracy <br>
    Determines how faithfully the robot follows the specified trajectory. A higher value is recommended for processes such as machining or precision assembly where trajectory deviation must be minimized.
    A larger value increases path accuracy, but it may also cause relatively higher vibration.
  * Smooth Motion <br>
    Determines how gently the acceleration and deceleration change. Use a higher value when you need to protect fragile workpieces (e.g., glass), when the process is sensitive to vibration, or when you want to reduce mechanical shock to the robot hardware. A larger value yields smoother motion, but it also increases cycle time. Setting the value too high may prevent the robot from performing continuous motions, causing it to move in a discontinuous manner.

## Example Settings

* Precision machining and dispensing (path accuracy priority)
  * The robot must follow a predetermined trajectory accurately.

  * Recommended settings:
    * Path accuracy: High (e.g., 80 ~ 100)
    * Smooth motion: Low-to-medium (e.g., 20 ~ 40)

  * Use case: Applying sealant along complex curves of automotive parts, or performing laser cutting. To minimize trajectory error, set accuracy high; maintaining the path is more important than slight vibration.

  * Caution: Adjust parameters according to the actual robot's vibration behavior and the specific process specifications.

* Sensitive cargo transport (vibration-reduction, smooth motion priority)
  * A process where vibration can damage the product or cause mis-placement.

  * Recommended settings:
    * Path accuracy: Medium (e.g., 50)
    * Smooth motion: High (e.g., 80 ~ 100)

  * Use case: Transporting semiconductor wafers, large glass panels (LCD/OLED), or containers with easily spilling liquid. Minimize shock during acceleration/deceleration to prevent slip or shaking.

  * Caution: As motion becomes smoother, overall cycle time (operation time) may increase, or discontinuous motions may need to be performed.