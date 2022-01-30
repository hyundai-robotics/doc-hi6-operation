# 7.4.8 Collision Detection \(Function to Be Available Later\)

The Hi6 controller has the error detection function for overcurrent, overload, overspeed, position deviation, as well as the collision detection function, as safety functions in preparation for a case in which the robot operates under abnormal conditions or operates abnormally. These two functions will work with each other to enhance the safety of the robot.

In the Hi6 controller, a model-based collision detection function is provided. The model-based collision detection function detects a collision by calculating the difference between the torque that should be normally applied during the robot’s operation and the measured torque based on the dynamics model of the robot. By setting the sensitivity, you can adjust the responsiveness to the collision and make it possible to detect any contact with the outside that occurs when the robot moves at low speed.

However, the collision detection function detects the collision on the robot axis, so if the impact is not transmitted to the robot, the collision will not be detected. Moreover, the following are the points that require you to exercise precautions when using the collision detection function.

* The collision detection function will work only when the motor is turned on.
* You must execute load estimation before using the collision detection function.
* If the tool weight and the additional weight of each axis are different from the actual data, false detection may occur.
* When load estimation and sensor-based/sensorless force control functions are performed, the collision will not be detected.
* Collisions on the positioners, stationary guns, and jigs that are not attached to the robot cannot be detected.
* Special-order robots do not support the model-based collision detection function.

 

The following shows how to set the collision detection function.

1.	Touch the \[3: Robot Parameter &gt; 14: Impact Detection\] menu.

2.	Set whether to use the collision detection function, and set the sensitivity, etc.

![](../../../.gitbook/assets/image%20%28481%29.png)



<table>
  <thead>
    <tr>
      <th style="text-align:left">No.</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../../../.gitbook/assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>This is information on the use options of the collision detection function.
          You can set whether to use this function and set the sensitivity and whether
          to use the low-speed collision detection function.</p>
        <ul>
          <li>[Function to be Used]: You can set whether to use the collision detection
            function.</li>
          <li>[Sensitivity]: You can set the collision detection sensitivity. The larger
            the value, the more sensitive it is to impact (basic setting value: 100%).</li>
          <li>[Low-Speed Impact Detection]: You can set whether to use the low-speed
            collision detection function.</li>
          <li>[Reference Time]: You can set the reference time for determining a collision.
            If an impact force occurs during the reference time, it will be determined
            as a collision.</li>
          <li>[Link Speed]: You can set the reference speed for determining a low speed.
            Slow-speed collision will be inspected only below the reference link speed.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../.gitbook/assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[OK]: You can save the changes.</li>
          <li>[Reset All]: You can initialize the setting values of all the use options.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

