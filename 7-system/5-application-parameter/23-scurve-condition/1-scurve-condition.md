# 7.5.23.1 S-curve condition

S-curve condition settings allow you to define the characteristics of the acceleration and deceleration phases that occur when the robot is operating in detail. Configure the items below to match each process's required characteristics (such as path accuracy or vibration reduction).

![](../../../_assets/tp630/s-curve_condition.png)

  * Condition Name: 输入条件名称。
  * Path Accuracy <br>
    确定机器人跟随指定轨迹的忠实程度。对于如加工或精密组装等必须最小化轨迹偏差的过程，建议使用较高的值。
    较大的值增加路径准确性，但也可能导致相对较高的振动。
  * Smooth Motion <br>
    确定加速和减速变化的平稳程度。在需要保护易碎工件（例如，玻璃）、过程对振动敏感，或希望减少对机器人硬件的机械冲击时，使用较高的值。较大的值产生更平稳的运动，但也会增加周期时间。将值设置得过高可能会阻止机器人进行连续运动，导致其以不连续的方式移动。

### Example Settings

* Precision machining and dispensing (path accuracy priority)
  * 机器人必须准确地跟随预定轨迹。

  * Recommended settings:
    * Path accuracy: 高 (例如，80 ~ 100)
    * Smooth motion: 低到中等 (例如，20 ~ 40)

  * Use case: 沿着复杂的汽车零件曲线应用密封剂，或进行激光切割。为了最小化轨迹误差，设置高精度；维持路径比轻微振动更重要。

  * Caution: 根据实际机器人的振动行为和特定过程规格调整参数。

* Sensitive cargo transport (vibration-reduction, smooth motion priority)
  * 一个过程，其中振动可能会损坏产品或导致位移错误。

  * Recommended settings:
    * Path accuracy: 中等 (例如，50)
    * Smooth motion: 高 (例如，80 ~ 100)

  * Use case: 运输半导体晶圆、大型玻璃面板 (LCD/OLED) 或容易溢出的液体容器。在加速/减速期间最小化冲击，以防止滑移或摇晃。

  * Caution: 由于运动变得更平滑，总体周期时间（操作时间）可能会增加，或可能需要执行不连续的运动。