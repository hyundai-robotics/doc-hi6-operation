# 7.7.4 Base Axis Calibration

Base axis calibration is a function to calibrate the installation direction of the axis.

It is almost impossible to install the base axis to exactly match one direction \(X, Y, or Z\) of the robot coordinate system. When you calculate the direction of the base axis in the controller using the base axis calibration function, you can improve the performance of the linear interpolation trajectory of the system including the base axis.

After the robot is installed on the base axis, this function makes it possible to perform position interpolation by finding the direction vector of any base axis on which the robot is installed.

![Figure 72 Base Axis Calibration](../../../_assets/image%20%28497%29.png)


In general, the base axis is used to move the robot to the operation position. In special cases, the base axis can also be used in a case in which a linear trajectory should be guaranteed while the robot is moving on the base axis.

* When two robots with the base axis calibrated deliver the workpiece \(multi-robots will be supported in the future\)
* When you need to perform interpolation while operating the base axis





