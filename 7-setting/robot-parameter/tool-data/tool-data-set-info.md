# 7.4.1.2 Tool Data Setting Information

* \[Weight\]: Weight of the tool \(kg\)
* \[Length\]: Length of the tool \(mm\). You can set it using the automatic calibration function or the auto calibration.
* \[Angle\]: Angle of the tool \(deg\). You can set it using the automatic calibration function or the angle calibration function.
* \[Center\]: Position of the center of gravity of the tool based on the center of the flange \(mm\). You can set it using the load estimation function.
* \[Inertia\]: The moment of inertia \(kg/m2\) of the tool with respect to the tool coordinate. You can set it using the load estimation function.
* Allowable Ratio: \(Only for the robot models to which high-load mode is applied\) This is the ratio of the current setting against the allowable reference value. The robot operation, according to the allowable ratio, is as follows.

| Classification | Normal | High-load mode | Exception allowable mode | Playback impossible \(Large size\) |
| :--- | :--- | :--- | :--- | :--- |
| Weight ratio \(%\) | - 100 | 100–120 | 100–120 | 120 - |
| Moment ratio \(%\) | - 100 | 100–110 | 100–115 \(150\) | 115 \(150\) - |
| Inertia ratio \(%\) | - 100 | 100–130 | 100–150 \(600\) | 150 \(600\) - |

{% hint style="info" %}
The allowable ratio can be changed depending on the robot model and controller software version.
{% endhint %}



