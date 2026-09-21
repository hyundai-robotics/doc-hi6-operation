# 7.7.4.2 Teaching based Base Axis Calibration

{% hint style="info" %}
* This section covers the \[Teaching based Base Axis Calibration\] feature. For details on the \[Sensor based Base Axis Calibration\] feature, please refer to the next page.
{% endhint %}

#### Base Axis Calibration Program Teaching

1.	Make a reference point in space, and then record the first reference point.

2.	Move the base axis more than 200 mm and record the same point as the second step.

3.	While moving 200 mm or more in the same direction as the direction you moved in step 2, record the same point as the third and fourth steps.

![](../../../_assets/image_526.png)

{% hint style="warning" %}
* Teach the travel axis calibration program using a tool for which robot calibration \(optimization of the axis origin and tool length\) has been completed.
* When recording a step, record it using a tool number for base axis calibration.

* Record the position by setting the moving distance of the base axis between recording steps as far as possible.
{% endhint %}

#### Base Axis Calibration Execution

1.	Touch the `[6: Auto Calibration  - 6: Base Axis Calibration - 1: Sensor based Calibration]` menu.

2.	After inputting the program number for the base axis calibration, touch the `[Auto Setting]` button.

    ![](../../../_assets/tp630/system-calib-base_eng.png)

3.	After checking the installation direction vector value of the base axis, touch the `[OK]` button.

#### Operation After Base Axis Calibration

If you jog the base axis after performing base axis calibration, the distance traveled in the created direction vector of the base axis will be converted into the current coordinate value.

![Operation After Calibration of the Base Axis](../../../_assets/image_528.png)

1.	Touch the `[+]` button at the top right of the panel stack in the work area, and then touch `[Pose]` in the panel selection window.

2.	Jog the base axis. The distance traveled in the direction of the base axis will be converted into X, Y, and Z values and displayed in the pose information window.

3.	Record and play back the steps in the usual way.

{% hint style="warning" %}
Set the jog coordinate system as the tool coordinate system and jog the base axis to check whether the base axis is properly calibrated. If the tooltip fixing operation is executed, it means that the base axis has been properly calibrated.
{% endhint %}