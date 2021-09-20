# 2.3.1.3 Speed

The operation speed of the robot can be displayed using the following four types of units. They can be used in all interpolation methods.

* ㎜/sec, ㎝/min: Sets the maximum speed of the TCP \(Tool Center Point\) of the robot.   The maximum speed of the robot will be automatically calculated by the controller based on the position and acceleration/deceleration parameters. If the setting value is larger than the maximum speed limit of the performance of the robot, the robot will operate only at the maximum speed limit.



* sec: Sets the robot moving time.  The shortest robot moving time will be automatically calculated by the controller based on the position and acceleration/deceleration parameters. If the setting value is shorter than the shortest time limit of the performance of the robot, the robot will operate only at the shortest time limit.



* %: Sets the ratio of the robot moving speed to the maximum speed at which the robot can operate.  When this is set to 100%, the robot will operate at the maximum speed within the allowable range.





