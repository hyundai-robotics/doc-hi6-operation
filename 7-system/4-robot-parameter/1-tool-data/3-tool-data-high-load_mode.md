# 7.4.1.3 High Load Mode

The availability of High Load Mode may vary depending on the robot model. In general, high load mode is supported on medium-sized robots with a payload capacity of 100 kg or more.<br> For models that support high load mode, you can configure "4. High load mode" as shown in the figure below in `[F2: system] - 3: Robot Parameter - 33: Servo parameter - 9: Servo control environment` menu.<br> For models that support high load mode, auto apply is the default setting.

![High Load Mode Setting Screen](../../../_assets/image_high_load_mode_setting_eng.png)

| Setting Value | Operating Characteristics |
| :--- | :--- |
|Disable| Operates in normal mode regardless of tool load. <br>- When the motor is turned ON, warning (W0051) is generated indicating risk of premature robot failure due to high load mode being "Disable".
|Auto apply| Operates in normal mode when the tool load is below the rated load.<br> When the load exceeds the rated value, it switches to high load mode, and the robot's operating speed and acceleration/deceleration are reduced.
|Permit exception| If the tool load is below the maximum allowable ratio for high load mode, it operates the same as auto apply.<br> If the high-load threshold is exceeded, it operates in high load exception mode.<br> -	When the motor is turned ON, warning (W00177) is generated indicating risk of premature robot failure due to high load "Permit exception" mode.

The high load mode application status based on the currently applied tool load can be checked as shown in the figure below.<br>

![Check high load mode application status based on tool load](../../../_assets/home_tool_no_eng.png)


![Normal Mode Tool (regular font)](../../../_assets/tp630/normal_mode_tool_eng.png) : Nomal Mode (regular font)

![High Load Mode (bold font)](../../../_assets/tp630/high_load_mode_tool_eng.png) : **High Load Mode** (bold font)

![High Load Exception Mode (red font)](../../../_assets/tp630/high_load_exception_mode_tool_eng.png) : <span style="color: red; font-weight: bold;">High Load Exception Mode</span> (red font)

{% hint style="info" %}
The allowable ratio for high load mode may vary depending on the robot model and controller software version.
{% endhint %}
